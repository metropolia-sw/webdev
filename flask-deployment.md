# Deploying a Flask based web application on the Web

## Publish a Flask Application on Render

In this guide, you will publish your Flask application online using **Render** service. After deployment, your application will be accessible through a public `onrender.com` URL.

Render is one of the cloud platforms that allows you to deploy web applications and services. The free tier is suitable for small projects and course assignments.

There are other cloud platforms that can be used to deploy Flask applications, such as **Heroku** and **PythonAnywhere**. And if you are familiar with cloud computing, you can also use **AWS**, **Google Cloud** or **Microsoft Azure**. The choice of platform is up to you, but this guide focuses on Render.

### 1. Make sure your project works locally

Before deploying, make sure your Flask application works on your own computer.

For example:

```dir
my-project-app/
├── app.py
├── requirements.txt
└── static/
    ├── index.html
    ├── style.css
    └── script.js
```

Your Flask application should have an `app` object in your main Python file `app.py`, for example:

```python
from flask import Flask, send_from_directory

app = Flask(__name__)

@app.route('/')
def home():
    return send_from_directory('static', 'index.html')

@app.route('/<path:filename>')
def serve_static(filename):
    return send_from_directory('static', filename)

@app.route('/hello')
def hello_world():
    return 'Hello, World!'

if __name__ == '__main__':
    app.run(use_reloader=True, host='127.0.0.1', port=3000)
```

In this example, the Flask application serves static files from the `static` folder and has a simple `/hello` route. For example, if you run the application locally, you can access it at:

```text
http://localhost:3000/ -> displays index.html
http://localhost:3000/index.html -> displays index.html
http://localhost:3000/style.css -> displays style.css
http://localhost:3000/script.js -> displays script.js
http://localhost:3000/hello -> displays "Hello, World!"
```

### 2. Create `requirements.txt`

Render needs to know which Python packages your application uses.

Create a file called `requirements.txt` and add following lines for a basic Flask application:

```text
Flask
gunicorn
```

If your project uses other packages, add them as well, for example:

```text
Flask
gunicorn
requests
```

You can also generate the file automatically based on the current locally installed packages with terminal command:

```sh
pip freeze > requirements.txt
```

Make sure that `requirements.txt` is committed to your Git repository.

### 3. Put your project on GitHub

Create a repository on GitHub and upload your Flask project.

Make sure the repository contains at least:

```text
app.py
requirements.txt
static/
```

Do **not** upload passwords, API keys, or other secrets to GitHub.

### 4. Create a Render account and deploy your app

Go to: [Render.com](https://render.com/) and create an account. You can sign up with your GitHub account or create a new account with your email.

Note: if you sign up with your GitHub account, Render will ask for permission to access your repositories. This is necessary for Render to deploy your Flask application from GitHub when using public repositories.

In the Render Dashboard:

1. Choose _New Web Service_
1. Connect your GitHub repository
1. Check the settings
   - use free compute option
   - otherwise, default values should be ok for simple project like in this example
1. Click **Deploy web service**.

Wait for the deployment, Render will now:

1. Download your GitHub repository
1. Install Python dependencies (based on listing in `requirements.txt`)
1. Start your Flask application
1. Give your application a public URL

The URL will look something like: `https://my-flask-game.onrender.com`. Open the URL in your browser and test your application.

### 5. Updating your application

**Before updating your application, make sure it works locally first!**

One of the useful features of Render is automatic deployment. After you connect your GitHub repository, Render can automatically deploy new commits pushed to the selected branch.

By default, if you do following in your `main` branch:

```bash
git add .
git commit -m "Add new game feature"
git push
```

render detects the new commit and starts a new deployment. You can monitor the deployment from the **Deploys** section of your Render service.

If automatic deployment is set off or not working, manual deployment is also possible. Just click _Manual Deploy_ button on the _Deploys_ tab.

---

## Common Problems

### Important: Using filesystem on Render

If/when your project uses files for permanent data storage, be aware that a deployed web service should **not be treated like your local computer's permanent filesystem**. Files do work but they can be cleared without a warning anytime or when the application is redeployed.

For a simple course project, storing data to files is ok, but you should not assume that data will persist indefinitely on a free deployment.

### `ModuleNotFoundError`

If Render says:

```text
ModuleNotFoundError: No module named ...
```

the package is probably missing from `requirements.txt`. Add the missing package and push the changes again.

Render specifically requires Python dependencies to be declared in the project's dependency file.

### `gunicorn: command not found`

Make sure `gunicorn` is included in:

```text
requirements.txt
```

Then redeploy.

### Application starts locally but not on Render

Check the **Deploy Logs** in Render.

A common problem is an incorrect start command.

If your main Python file is `app.py` and it contains:

```python
app = Flask(__name__)
```

the start command should normally be: `gunicorn app:app`.

The format is:

```text
gunicorn <python_file>:<flask_app_variable>
```

For example, if you have `server.py` file and your app variable is named:

```python
application = Flask(__name__)
```

the command would be: `gunicorn server:application`

You can fix these errors by changing your variable/filenames in your application or the _Start Command_ value in Render settings.

### The application uses the wrong Python version

Render uses some Python version as the default for newly created services. If your project requires another version, you can specify it using a `.python-version` file or the `PYTHON_VERSION` environment variable.

For a course project default should be fine but if having problems it is a good idea to specify the version you have tested locally.

---

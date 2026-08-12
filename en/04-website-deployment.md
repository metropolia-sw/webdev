# Deploying your website

## Using Metropolia Home pages for students (users.metropolia.fi)

You can publish your website on Metropolia’s server using the users.metropolia.fi service as follows:

1. Upload your website files (all html, css and image files, etc.) to a directory named `public_html` located in your home directory (NOTE: do not delete that folder in any case).
   - You can access your home directory by logging into the server `shell.metropolia.fi` for example via SSH. For file transfer, you can use scp or sftp programs (you need to create an SSH key pair first, check links below).
   - Another (and easier for beginners) option is to use <https://webdisk.metropolia.fi/> website

2. Your published website can be found at: <https://users.metropolia.fi/~yourusername>, where `yourusername` is replaced with you Metropolia username.
   - For example, if your username is "janedoe", your site address is: <https://users.metropolia.fi/~janedoe>

More information is available in Metropolia Helpdesk's wiki:

- [Home Page, Shell and MySQL Services](https://wiki.metropolia.fi/spaces/itservices/pages/8552770/Home+Page+Shell+and+MySQL+Services)
- [Creating an SSH Key Pair and Logging in on a Linux Server (shell.metropolia.fi)](https://wiki.metropolia.fi/spaces/itservices/pages/307791540/Creating+an+SSH+Key+Pair+and+Logging+in+on+a+Linux+Server+shell.metropolia.fi)
- [Webdisk Service Quick Instructions](https://wiki.metropolia.fi/spaces/itservices/pages/181375282/Webdisk+Service+Quick+Instructions)

You can also use Helpdesk's AI service to ask for help: <https://mikko.metropolia.fi/>

## Other services (not supported by Metropolia/teacher)

There are also other services that provide web-site hosting (some free options or student plans might be available), such as:

- Azure Static Web Apps: <https://azure.microsoft.com/en-us/services/app-service/static/>
- GitHub Pages: <https://pages.github.com/>
- Netlify: <https://www.netlify.com/>
- Vercel: <https://vercel.com/>
- Firebase Hosting: <https://firebase.google.com/products/hosting>
- Heroku: <https://www.heroku.com/>

These are 3rd party services and you need to create an account to use them. They also have their own documentation on how to deploy your website, so please refer to their documentation for more details.

They are not supported by Metropolia or the teacher, so you may need to seek help from their support if you encounter any issues.

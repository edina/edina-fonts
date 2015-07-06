# edina-fonts

Bower packge containing fonts used by EDINA


## How to use package

*bower install https://github.com/edina/edina-fonts.git --save*

**NOTE:** It is **very** important you use --save and not --save-dev


You need to then add a reference to the CSS file to your HTML e.g.

    <link rel="stylesheet" href="../../../../bower_components/edina-fonts/edina-fonts.css">

The fonts file(s) also need to be added to your project, however there are a number
of way in which your project can be structured, so it is impossible to define it here.
Using a build tool such as **Gulp** and it's plugins will greatly simplify your build
and make it repeatable.  The current project this package was built for makes it very
easy, in fact, you do nothing apart from the above **bower install** command.


## Directory Structure

    PROJECT_ROOT
        css
        fonts
        bower.json
    
This should be quite self-explanatory, any css file(s) are under the **css** directory
and any fonts reside under the **fonts** directory. The **bower.json** file defines
the project for bower.


## Update package

To update the package I assume you already have the fonts and associated CSS file(s).
Using a tool like icomoon (https://icomoon.io/) is an easy way to generate fonts and CSS
from source SVG images. What is produced is a zip file with a number of files, the only
really necessary files are all files under the **fonts** directory and  **style.css**.

Once the downloaded file has been unzipped, 

1. Rename all font files edina-fonts.*
2. Rename **style.css** to **edina-fonts.css**
3. Edit this CSS file and replace any reference to **icomoon** with **edina-fonts**
4. Copy font file(s) to the **fonts** directory of this project
5. Copy edina-fonts.css to the **css** directory of this project
6. Add and commit file(s) to GIT:

    *git add .*
    *git commit -m "Explain what you have done"*

7. Tag your change(s) (Not every commit needs tagged, the decision to tag is left to your discretion):

    *git tag -a v0.0.1 -m 'Minimum set of fonts and associated CSS.'*

    **NOTE:** You **must** use semantic versioning e.g. v0.0.1 (http://semver.org/). The version you choose 
    very much depends on what changes were made.

8. Push changes and tags to GitHub:

    *git push --tags*

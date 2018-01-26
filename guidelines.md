# OpenConnect Repo Guidelines
Follow these guidelines when working with repositories (repos) in the PureStorage-OpenConnect organization.

## Creating a New Repo
The following steps provide the specific details when creating a new repository.

### Add New Repo 
Navigate to https://github.com/purestorage-openconnect to get started.

### New Repo Setup
Required properties for the repository.


* Repo Name
Use as concise a name as possible. The context of the org is Pure Storage so there is no need to include that in the repo name. Eg. \PureStorage-OpenConnect\sap-tools. 

* Description
This is the summary description. Should be short. Use the readme.md file to explain the repo in more detail. 

* Public or Private
If the project is ready for the community then make public. When making a repo public please follow the Making Repo Public section. 

If you are just beginning a project make Private until ready for first release. 

* Initialize README, always yes.

* .gitignore
This is optional but recommended. If you are not familiar with gitignore see https://help.github.com/articles/ignoring-files. For gitignore templates check, https://github.com/github/gitingore.

* License
Pure Storage legal has recommended the use of the Apache License 2.0 for the PureStorage-OpenConnect organization. Use this license for any new project. 




# Add Readme.md
Now commit or upload the project to the new repo. Use git locally to continue development. When creating a readme.md file use markdown. See https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet.

Example readme.md, https://github.com/PureStorage-OpenConnect/powershell-toolkit.

/Users/barkz/Documents/GitHub/OpenConnect-Guide/images/new-repo-setup.png

# Making Repo Public
Before making the repo public create a release. See https://help.github.com/articles/creating-releases/ for steps. 

After creating the release flip the switch to make repo public. Once public the project should be placed on the Pure/Code() site for community access. There are templates located at https://github.com/PureStorage-OpenConnect/OpenConnect-Templates to ensure the repo displays.

Review the readme.md in the (https://github.com/PureStorage-OpenConnect/OpenConnect-Templates) repo. 

Example
Make the repo card header creative and aligned to the project. FlashStache is a great example.
<graphic>


# Publish to Pure/Code()

## OpenConnect-Templates

These templates can be used to setup your repo for public viewing. They include:
* settings.json - Used with code.purestorage.com.
* template-header.png - Use with code.purestorage.com. Header graphic should adhere to the dimensions.

### settings json
```
{
    "id": "REPO NAME", <-- Repositry name
    "filter": "TAG(S)",  <-- Choose one or more tags. microsoft cisco containers devops database
    "image": "http://code.purestorage.com/images/REPO-NAME-HEADER.png", <--
    "featured": 1, <-- do not change
    "priority": 1  <-- do not change
} 
```

### template-header.png
This graphic file has the proper dimensions for the header graphics on the individual cards on http://core.purestorage.com. This file needs to be committed to https://github.com/PureStorage-OpenConnect/purestorage-openconnect.github.io/tree/master/images. 


# Using Git
If not already installed get started using git locally for development. 
*	https://git-scm.com/downloads -- Downloads for OS platforms.
*	https://git-scm.com/doc - git documentation.







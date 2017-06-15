# IntelliJ Setup Guide

1. [Downloading and Installing IntelliJ](#1---downloading-and-installing-intellij)
1. [Getting the Source Code](#2---getting-the-source-code)
1. [Linking Gradle](#3---linking-gradle)
1. [Using IntelliJ](#4---using-intellij)

# 1 - Downloading and Installing IntelliJ

First, head to the
[download page on the IntelliJ website](https://www.jetbrains.com/idea/download/).
From here, you will download the latest version of the IntelliJ Community
Edition for your platform by clicking the "DOWNLOAD" button.

Once downloaded, open the installer and go through the install proccess.
Depending on your operating system, you may be required to enter an admin
password to finish the installation.

# 2 - Getting the Source Code

To get the source code, click on "Check out from Version Control" > "GitHub" on
the IntelliJ welcome screen. You may be asked to enter your GitHub username and
password (Note: if you're using GitHub 2FA, you'll need to enter a Personal
Access Token, which you can create from your GitHub Setting page). Then, enter
the link for the GitHub repository you're looking to clone (e.g.
https://github.com/SouthEugeneRoboticsTeam/Robot-Base). Change the parent
directory or directory name if you would like. You'll be asked whether you would
like to open the project. Select "Yes". Now the project should be open in a new
window.

# 3 - Linking Gradle

Gradle is the dependency manager we now use after the 2017 season. After opening
the project, you should see a dialog in the lower right corner of the window
warning you about an "Unlinked Gradle Project". Press on the "Import Gradle
project" link and press "OK" on the dialog that appears. The neccessary external
dependencies will begin downloading.

# 4 - Using IntelliJ

To open up the Project Tree for the project, press <kbd>alt</kbd> +
<kbd>1</kbd>.

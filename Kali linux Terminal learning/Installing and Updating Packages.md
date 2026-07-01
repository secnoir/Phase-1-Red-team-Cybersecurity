Here we will learn how to install and update Tools :

sudo apt update -> This command finds updates and checks packages for updates.

sudo apt upgrade -> after you run the apt update command and you have new updates you can update it by running apt upgrade.

These commands can be used together at once (sudo apt update && sudo apt upgrade).

sudo apt install -> This is used to install a package. Example : sudo apt install wireshark

*Note that we don't need the sudo for these commands but we may need to use it if it says permission denied when we run these commands.

git -> We use this command to manage our code , tools and notes. A reason pentesters might use this tool is because many of the security tools are not available to install with apt install thats why we can use git command to clone (download) the repositories from github which contains the files required to install the tool. Github is a website that hosts git repositories.

- When we want to install a tool from GitHub using Git it usually includes the steps to correctly install that tool.
- Common steps to download a tool are :

1.we first need to install the git tool to clone(download) the repositories from GitHub.

(sudo apt install git)

2.After we install git , we can run a command such as -> git clone (repository url)

3.The further instructions are normally provided in the repository's README.md and it may be different from the other repositories.
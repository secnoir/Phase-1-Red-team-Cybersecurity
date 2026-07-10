Commands :

pwd -> (print working directory) it shows what directory we are at.Example : if i am at the user folder i can run pwd and it will print /home/user

cd .. -> goes back one directory. If i want to go to home folder from the Desktop folder i can run cd ..

cd -> used to change directory.Example : cd Desktop/

ls -> lists everything in a folder except hidden files.If i want to list everything on a folder from a different folder for example i want to list everything in downloads folder from the home folder i can run ls Downloads/

ls -a -> lists everything in a folder included hidden files.

ls -la -> lists everything in a folder included hidden files and thier details like permissions , user and last modified date..

mkdir -> used to make your own directory(Folder).Example : mkdir cybersec , this creates a folder named cybersec.

rmdir -> used to remove a directory(Folder).Example : rmdir cybersec , this removes the cybersec folder. Sometimes when the folder contains files it might not get deleted by the command rmdir so we may need to use rm -rf , this forcefully deletes a file or folder so you need to be careful with this command as it can delete important files and folders permanently without asking twice.

locate -> It finds a specific file name that you input for example : i create a new file test.txt and later i want to know where that file is i can run (locate test.txt) . For locate command to work properly always run the command (sudo updatedb) before you run the locate command.

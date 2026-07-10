adduser -> This command is used to make a new user. Example : sudo adduser john

su -> This command is used to switch user , lets say we are currently operating as the user john and we want to switch to user bob we can run a command such as :
sudo su bob 

chmod -> It stands for change mode , it is used to change file's permissions for owner , group and other users. A file has 3 permissions for owner , group and other users and those are read , write and execute (rwx). read has the value of 4 , write has the value of 2 and execute has the value of 1 . This values help us run these commands in a simple form. Example : chmod 764 hello.txt , the owner gets all permissions , group gets read and write permissions and other users only get read permission. when we want to give a user all permissions we can simply combine the r,w,x which adds upto 7.




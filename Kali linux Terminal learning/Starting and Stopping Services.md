This is for learning how to start and stop services in kali linux :

service -> This command is used to start and stop different services. Example : service apache2 start , this starts a apache2 service which you can see by copying your ipv4 address and pasting it on your browser.

When i want to stop the service i can just use service apache2 stop.

python -m http.server 80 -> this is a command that opens a http web server.

systemctl -> this command is used to enable and disbale services , the difference from the command service is that this enables a service so that when you boot your computer the service starts automatically. Example systemctl enable postgresql.This can also be used just like the service command one example is systemctl start apache2 you can then stop the service using systemctl stop apache2 and if you want to disable a service so it doesnt start on boot you can use systemctl disable postgresql.

systemctl status postgresql is also a command used to check the status of a service whether it is disabled or enabled.

it may also show if a service is currently running or not.

systemctl restart postgresql is used to restart a service.

the systemctl enable command doesn't start a service directly but when you reboot it will start automatically.

* Here postgresql is used as an example service

* systemctl does the same job as service command , systemctl is a new tool and is preferred over the service command as it offers more features.
# Aneeshwar Botla
# ITMO-556 Week-13-Lab-2

1.
```
GRUB_BACKGROUND= "/usr/share/background/Candy_by_Bernhard_Hanakam.jpg"
sudo update-grub 
```
![1](https://user-images.githubusercontent.com/33158558/33519372-22dc5c28-d76b-11e7-8393-2426d9c83a15.JPG)

2.
```
systemd-analyse time
```
![2](https://user-images.githubusercontent.com/33158558/33519373-22eab39a-d76b-11e7-9fc2-3cc30d906a02.JPG)

3. 
```
sudo dnf install mariadb mariadb-server
systemctl status mariadb.service
systemctl  start mariadb.service
systemctl status mariadb.service
```
![3](https://user-images.githubusercontent.com/33158558/33519374-22f7975e-d76b-11e7-9f75-b83b4e00d51e.JPG)

4. 
```
systemd-analyse time
```
![4-a](https://user-images.githubusercontent.com/33158558/33519375-2304677c-d76b-11e7-8977-80eeae259f30.JPG)
```As we can see there is 8 second delay in bootup``` 
![4-b](https://user-images.githubusercontent.com/33158558/33519376-2313a0b6-d76b-11e7-8ee7-a39d20073a15.JPG)

5. 
```
systemd-analyse blame
```
![5](https://user-images.githubusercontent.com/33158558/33519377-231fbfa4-d76b-11e7-9056-61fe6bb3e8f5.JPG)

6. 
```
systemctl start httpd.service
systemctl status httpd.service
```
![6](https://user-images.githubusercontent.com/33158558/33519378-232e6bbc-d76b-11e7-9ec3-7cf443854fa9.JPG)

7. 
```
systemctl kill -s SIGHUP httpd.service
systemctl status httpd.service
```
![7](https://user-images.githubusercontent.com/33158558/33519379-23429722-d76b-11e7-9a24-4d8a2bd4e4fa.JPG)

8.
```
systemctl get-default
systemctl set-default multi-user.target
systemctl get-default
systemctl set-default runlevel5.target
```
![8](https://user-images.githubusercontent.com/33158558/33519380-234f4b8e-d76b-11e7-8d38-052353d76e35.JPG)

9.
```
systemctl enable sshd.service
systemctl start sshd.service
systemctl show -p "Wants" -p "After" sshd.service
```
![9](https://user-images.githubusercontent.com/33158558/33519381-235f458e-d76b-11e7-9891-08b05dd9f34f.JPG)

10. 
```
Low Priority Command
nice -n 19 ./a.out
```
![10a](https://user-images.githubusercontent.com/33158558/33519867-7ced6aa4-d775-11e7-89d8-c8e60adccd18.JPG)
```
High Priority Command
nice -n -20 ./a.out
```   
![10b](https://user-images.githubusercontent.com/33158558/33519680-579e53f2-d771-11e7-9e4c-503281ac2899.JPG)

11. 
```
ps -ef
kill -2 3497 3554
```
![11](https://user-images.githubusercontent.com/33158558/33519383-237c4242-d76b-11e7-9976-1686338143cd.JPG)

12.
```
lsmod | grep vbox*
```
![12](https://user-images.githubusercontent.com/33158558/33519384-23887454-d76b-11e7-856e-e089d8270d48.JPG)

13. 
```
lspci
```
![13](https://user-images.githubusercontent.com/33158558/33519385-2396f786-d76b-11e7-9f5e-44b24f5b929d.JPG)

14.
```
cat /proc/cpuinfo | grep flags
```
![14](https://user-images.githubusercontent.com/33158558/33519386-23a3a9cc-d76b-11e7-8047-5376a6892d59.JPG)

15.
```
systemd-cgls
systemctl kill -s SIGHUP httpd.service
```
![15](https://user-images.githubusercontent.com/33158558/33519846-19b8104c-d775-11e7-96c2-4d25d6785a3d.JPG)

16. 
```
systemd-cgls | grep httpd.service
```
![16](https://user-images.githubusercontent.com/33158558/33519388-23c444fc-d76b-11e7-9846-ff6ed1e242a7.JPG)

17.
```
sudo dnf install procinstall
procinfo
```
![17](https://user-images.githubusercontent.com/33158558/33519389-23d1cf28-d76b-11e7-904b-c796c4139927.JPG)

18.
```
timedatectl
timedatectl set-timezone UTC
timedatectl
```
![18](https://user-images.githubusercontent.com/33158558/33519390-23deae78-d76b-11e7-83b8-1a62667a338c.JPG)

19.
```
hostnamectl set-hostname itmo-556-abotla
hostnamectl set-location Chicago
hostnamectl set-chassis VM
```
![19](https://user-images.githubusercontent.com/33158558/33519391-23f1e57e-d76b-11e7-9609-c3966b8fcc30.JPG)

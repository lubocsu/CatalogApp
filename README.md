# Item Catalog Project

## Introduction ##
This film item catalog is a full stack application that allows users to login into the system and add films to the database. Logged-in users may modify and delete the items they have created. Only authenticated users are allowed to make any changes to the database.

## To do list ##
- Allows users to login into the system via Google or Facebook account.
- Registered user can add/delete/update film categories.
- Registered user can add/delete/update films of the specific category.
- Above all the data is stored in database file.

## What's included ##
- [VirtualBox(5.1+)](https://www.virtualbox.org/wiki/Downloads)
- [Vagrant(2.1.1+)](https://www.vagrantup.com/downloads.html)
- Python(3.6+)
- Unix shell(Mac or Linux system)
- Git bash（Windows system）
- [Vagrantfile](https://github.com/udacity/fullstack-nanodegree-vm)
## Python Module ##
- sqlalchemy (1.2.9)
- flask(1.0.2)
- oauth2client(4.1.2)
- requests(2.19.1)
- pip(10.0.1)

## Project Structure ##
```
.
├── app.py
├── database_setup.py
├── database_populator.py
├── fb_client_secrets.json
├── client_secrets.json
├── filmcatalog.db
├── README.md
├── static
│   └── style.css
└── templates
    ├── base.html
    ├── delete.html
    ├── delete_category.html
    ├── edit_category.html
    ├── index.html
    ├── items.html
    ├── login.html
    ├── new_category.html
    ├── new_item.html
    ├── new_item2.html
    ├── update_item.html
    └── view_item.html
```
## Quick Start ##
1.Clone or download the VM configuration file 'Vagrantfile' which resides in the directory `fullstack/vagrant/`.
   ```bash
   git clone https://github.com/udacity/fullstack-nanodegree-vm  fullstack
   ```
2.Download above Project Files in the directory `fullstack/vagrant/catalog`.

3.Change current directory to `fullstack/vagrant/`.
   ```bash
   vagrant up
   ```
  This will cause Vagrant to download the Ubuntu operating system and install it.
 ,then open up the VM.
4.After successfully installed,type code below to connect to the VM.
   ```bash
   vagrant ssh
   ```
5.Type code below to change to the shared directory.
   ```bash
   cd /vagrant
   ```
6.Change the current directory to the `fullstack/vagrant/catalog` and

7.Install and update **pip** module.
   ```bash
    curl https://bootstrap.pypa.io/get-pip.py | sudo python3.6
   ```
8.Install **sqlalchemy** module.
   ```bash
    sudo pip3 install sqlalchemy
   ```
9.Install **flask** module.   
   ```bash
    sudo pip3 install flask
   ```
10.Install **oauth2client** module.    
   ```bash
    sudo pip3 install oauth2client
   ```    
11.run the below command to set up database.
   ```bash
    python3.6 database_setup.py
   ```     
12.run the below command to populate data set.
   ```bash
    python3.6 database_populator.py
   ```
13.run the below command to generate a web server.
   ```bash
    python3.6 app.py
   ```
14.Open terminal, and type url:`http://localhost:5000/` to use this app.

## Necessary Steps ##  

### Google credentials file
* Go to `https://console.developers.google.com/` to add a Web APP named 'Favourite Film APP'and activate Google OAuth Authorization.
* Add `http://localhost:5000` as Authorized JavaScript origins and  Website URL.
* Add `http://localhost:5000/`  `http://localhost:5000/login/`  `http://localhost:5000/gconnect`  `http://localhost:5000/logout` as Authorized redirect URIs.
* After saving, download JSON and rename the file to ```client_secrets.json``` and replace the file with the same name in the project directory.

### Facebook credentials file
* Go to `https://developers.facebook.com/apps`to add a Web APP named 'Favourite Film APP'and activate Facebook OAuth Authorization.
* Add `http://localhost:5000` as Authorized JavaScript origins and  Website URL.
* Add `http://localhost:5000/`  `http://localhost:5000/login/`  `http://localhost:5000/fbconnect`  `http://localhost:5000/logout` as Authorized redirect URIs.
* Add your Client_id and Client_secret in the ```fb_client_secrets.json``` file and replace the file with the same name in the project directory.

## Helpful Resources ##
* [Google OAuth Credentials](https://console.cloud.google.com/apis/credentials/oauthclient)
* [Facebook Deveopers](https://developers.facebook.com/apps)
* [Bootstrap Chinese Documentation](http://www.bootcss.com/)
* [jquery Documentation](https://jquery.com/)
* [Flask Documentation](http://flask.pocoo.org/)

## Reference ##
* [BootCDN](https://v3.bootcss.com/getting-started/)
* [ Udacity course Full-Stack Foundations Code repository](https://github.com/udacity/ud330)

## Notice
- The version of Flask 1.x is necessary.
- The version of Python 3.6.x is necessary.
- The first time you run this project you must follow above 14 steps,but when you run next time you can only run step 3/4/5/6/13/14 in order.
- Type `vagrant halt`in terminal when you need to close VM .

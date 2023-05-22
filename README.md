# apache2
How to install and run Apache web server in ubuntu localhost
1. Install Apache
    sudo apt update
    sudo apt install apache2
    Then test it out by typing in our IP address for the web server.
2. Creating own website
    sudo mkdir /var/www/sitename/
    cd /var/www/sitename/
    nano index.html
    use this code
    <html>
    <head>
      <title> This is my wedsite! </title>
    </head>
    <body>
      <p> I'm running this website on an Ubuntu Server!
    </body>
    </html>
3. Setup VirtualHost
    cd /etc/apache2/sites-available/
    sudo cp 000-default.conf sitename.conf
    sudo nano sitename.conf
    Now Edit this file
    ServerName sitename.com
    ServerAdmin yourname@sitename.com
    DocumentRoot /var/www/sitename/
4. Activating VirtualHost
    sudo a2ensite sitename.conf
    service apache2 reload
5. SetUp Host name
    sudo nano /etc/hosts
    Now Edit: 127.0.0.1       sitename.com
6. Disable defalt site
    sudo a2dissite 000-default.conf
    service apache2 reload
    
Now type sitename on you browser. It wis running in localhost.
    
    

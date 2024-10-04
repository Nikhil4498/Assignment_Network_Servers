# Assignment_Network_Servers
#verify that Apache2 is running
sudo systemctl status apache2
# Create a DNS Name ‘awesomeweb’
sudo nano /etc/hosts
127.0.0.1 awesomeweb
# Creating Website Files
sudo mkdir /var/www/awesomeweb
# Set the correct permissions
sudo chown -R $USER:$USER /var/www/awesomeweb
sudo chmod -R 755 /var/www/awesomeweb
# Creating a simple HTML file
nano /var/www/awesomeweb/index.html

<!DOCTYPE html>
<html>
<head>
    <title>Welcome to AwesomeWeb</title>
</head>
<body>
    <h1>Hello, this is AwesomeWeb!</h1>
</body>
</html>

# Configure Apache to Serve Website
sudo nano /etc/apache2/sites-available/awesomeweb.conf

<VirtualHost *:80>
    ServerAdmin webmaster@localhost
    ServerName awesomeweb
    DocumentRoot /var/www/awesomeweb
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>

# Enabling the new site and disable the default
sudo a2ensite awesomeweb.conf
sudo a2dissite 000-default.conf
sudo systemctl reload apache2

#Accessing Website
Open a browser and type http://awesomeweb


# Installing Tor Service with aaPanel

This bash script is only **compatible only with Ubuntu 20.04 LTS** for now.

This script will update Ubuntu sources.list, update all repositories and install Tor service in its latest available version as per Tor Source at: https://www.torproject.org/download/tor/

After the Tor service is installed, it will generate a .onion V3 domain and enable the Tor service on the server.

Finally it will install [aaPanel](https://www.aapanel.com), at the end of the installation it will show the aaPanel login data and the .onion domain configured on the server.

To finish the installation, go to aaPanel, choose your web server between Apache or Nginx, PHP Version and Database type, Tor service is compatible with all services except email services.

After completing the installation of your web server, access the "Website" tab and add your .onion domain generated at the end of the installation. Ready! You can access your domain using the Tor browser.

You can easily create FTP users and database using aaPanel, you can manage everything with phpMyAdmin.

You can also create a mirror of your .onion domain on common domains like .com or others. Create a second site within the "Website" tab of aaPanel, and in the "Website Path" option, set the same directory as your .onion domain. Ready! You can now access your surfaceweb and .onion domains showing the same content.

Need help, visit our website https://impreza.host/ and chat with us or open a ticket and we'll be happy to help.

Script maintained and updated by Murilo / Impreza Host

# How to use:

Access your server via SSH and run:
```
git clone https://github.com/ifanhua/tor.git
cd tor
bash tor.sh
```

```
git clone https://github.com/ifanhua/tor.git
cd tor
bash tor2.sh
```
After completion, you will see aaPanel login data and generated .onion domain, please keep this information safe.

Now you have a complete control panel to manage your Tor server :)

**Note that you need to have git installed on your server, if not, run it before starting the Tor installation:**
```
sudo apt install git
```
```
sudo apt-get install python
sudo apt update
sudo apt install python3-pip
pip3 --version
pip install aliyun-python-sdk-core
btpip install cryptography==39.0.2
```


For security advice, change aaPanel username, password and port.

Do not use the https protocol for .onion domains, or try to install SSL for a .onion domain. Let's Encrypt does not support .onion domains, if you need to use the https protocol with SSL, talk to our team and we can help, but remember that Tor network encryption alone is enough to keep you, your users safe and anonymous.

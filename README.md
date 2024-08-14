# networking-and-servers-assignment_herovired
## Steps for deploy a website on localhost using apache2 and create a DNS name for this website as ‘awesomeweb’. 
### 1.Open the Ubuntu OS inside the Virtual Box.
### 2.Open the terminal in the Ubuntu OS.
## 3.Update the Package List
- sudo apt-get update
### 4.Install the apache2
```
sudo apt-get install apache2
```
### 5.Start and Enable Apache2
```
sudo systemctl start apache2
sudo systemctl enable apache2
```
### 6.Verify Apache2 Installation
- Search http://localhost in browser
### 7. Configure Apache2 to Serve a Custom HTML Page
```
cd /var/www/html/
ls
sudo rm -rf index.html
sudo nano index.html
```
### 8.Write the html code inside the nano text editor.
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Awesome Web</title>
</head>
<body>
    <h1>Welcome to Awesome Web!</h1>
    <p>This is a simple HTML page served from localhost.</p>
</body>
</html>
```
### 9.Restart Apache2
```
sudo systemctl restart apache2
```
### 10.Set Up a Local DNS Name
```
sudo nano /etc/hosts
```
### 11.Add the Custom DNS Name
- 127.0.0.1    awesomeweb
### 12.Test the Setup
- Open a web browser and navigate to http://awesomeweb.

# Getting-started-with-EC2
At first make an account on AWS(Amazon Web Services).

# Launch an Instance 
1. Login to AWS Console

2. Navigate to **EC2** and click **Launch Instance**.

3. Choose an AMI (Amazon Machine Image) eg: UBUNTU. 

5. Configure Security Group
   - Create a security group with the following rules:
     - **SSH** 
     - **HTTP** 
     - **HTTPS**
     - **Custom TCP**
     - **All traffic**

6. Create a new **key pair** and download the `.ppk` file.

7. Launch the Instance

# Connect to EC2 Using PuTTY

1. Open PuTTY

2. In **Host Name (or IP address)**, enter your instance's **public IP**.

3. In the left sidebar, navigate to **Connection > SSH > Auth**. Then, Click **Browse** and select the `.ppk` file.

4. Click **Open** and use `ubuntu` as the username when prompted.

# Install Apache2 on the EC2 Instance

Update the package list and install Apache2:
```bash
sudo apt update
sudo apt install apache2
 -y
```

# Delete Default index.html and Create a New One
1. Navigate to the Apache directory:
   cd /var/www/html
2. Delete the default index.html:
   sudo rm index.html
3. Create a new HTML file:
   sudo vi index.html
4. Add your HTML code:
   - Example:
   ```
     <html>
       Helloo 
     </html>
   ```
5. Save and exit.

# Access Your Website
1. Open a Browser.

2. Visit Your Website 
    Enter your EC2 Public IP in the browser:
3. Your HTML website will be visible now. 

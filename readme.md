SWE 645-ASSIGNMENT 1

README FILE

Manasa Motepalli, G01450942

Main webpage URL: https://swe645-assignment1manasa.s3.us-east-2.amazonaws.com/part-1.html

URL of application deployed on EC2: http://13.58.93.114/form.html

Creation of an EC2:

1.	Created EC2 instance with an Elastic IP and enabled HTTPS traffic:

I have created a new instance and named it.
Under the key pair section, I have created a new key pair.
Under the network settings I enabled ‘allow HTTPS traffic from the internet’ and then I clicked on launch instance.

Then I created an elastic IP for the instance so that I have a fixed IP address.
Once the elastic IP address is created, I have associated it with the instance

2.	Installed Apache (httpd) on the instance and started the service:

Next, I launched the virtual machine by opening the instance and clicking on connect.

Once the virtual machine is launched, in the terminal I have executed few commands:
•	sudo su-: It switches the root user and loads the root user’s full environment
•	sudo yum install httpd: It downloads the http package to access the server
•	sudo systemctl start httpd: It starts the server

3.	Uploaded form.html to the EC2 instance using the private key for secure access:

Next, I uploaded the files (form.html) from my local terminal using the private key that I created earlier to the server hosted in the instance.

4.	Successfully made the form.html accessible as a survey form via the EC2 public IP.


Creation of an S3 bucket:

1.	Created an S3 bucket with public access permissions:

In the Amazon S3 section, under the bucket section, I created a bucket where I have given the bucket a name. under the section of Block public access settings for this bucket, I have disabled the block all public access check box so that my files have the permission to be accessed by the public and then I have clicked on create bucket. So now my bucket is created. 

2.	Uploaded files, including part-1.html (main webpage) and error.html:

I have uploaded the files related to the part-1of the assignment, apart from the form.HTML (part-2) that was launched in the EC2 instance. Once the files are uploaded into the bucket, they are displayed as objects in the bucket. 

In the permissions tab, in the object ownership section, I have enabled the ACLs and in the ACL section, I have given the public read only access.

3.	Configured Static Website Hosting in S3, with part-1.html as the index document and error.html as the error document.

Under the property section, we have a tab called static website hosting. I have enabled the static website hosting permission and under the index document, I have uploaded the main webpage that has to be hosted, which is the part1.html file and in the error document section I have uploaded the error.html file.

4.	Launched the main webpage by accessing the object URL of part-1.html:

Now the website is ready to launch
I have selected all the files and under the actions tab, I have selected the option ‘make public using ACL’ so that my files are accessible by the public. 
Now I open the part-1.html file and click on the object URL and the website gets launched.

The website has a survey form page button, which when clicked is directed to the form.html webpage which was launched in the EC2 instance.





# Cloud_Academy_Projects

######################################################################################
## Google Cloud Essential Skills: Challenge Lab                                     ##
######################################################################################


====================== Task 1: Create a Compute Engine instance, add necessary firewall rules ======================

//Goto Compute Engine -> VM Instannces -> Create Instance.

   Name : dev-vm
   Zone : us-east4-b
   Series : N1
   Boot Disk : Linux 9 (stretch)
   
   Tick : Allow HTTP Traffic
          Allow HTTPS Traffic
          
//Click Create.

====================== Task 2: Configure Apache2 Web Server in your instance ======================

// SSH to 'apache' instance and run:-

sudo apt-get update
sudo apt-get install apache2 -y

![alt text](https://github.com/AiIkram/Cloud_Academy_Projects/blob/main/g%C3%A9.PNG?raw=true)

![alt text](https://github.com/AiIkram/Cloud_Academy_Projects/blob/main/G3.PNG?raw=true)
------------------------------------------------------------------------------

to host the website with images i created a bucket called vm-bucket-123

//Goto Cloud Storage -> Bucket -> Create Bucket.

Name: vm-bucket-123.
then let the default conditions and click create.

upload my folder "Cloud_academy_project" with my files of the websites.


upload the folder to ssh of the vm 

sudo gsutil cp -r gs://vm-bucket-123/Cloud_academy_project/* /var/www/html

![alt text](https://github.com/AiIkram/Cloud_Academy_Projects/blob/main/G6.PNG?raw=true)

I exectuted this command to sudo chown -R wwww-data:www-data /var/www

to set "Cloud_academy_project" as the default folder for apache server.
====================== Task 2: Test your server ======================

/open the external IP/

![alt text](https://github.com/AiIkram/Cloud_Academy_Projects/blob/main/G5.PNG?raw=true)




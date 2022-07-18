### Connect to EC2 using Putty and PuttyGen
- Download and install putty and puttygen
- Go to the EC2 page. On the left hand side scroll down to Network and Security. Click on `key pairs`
- Click on create key pair, name the key pair etc. Make sure to download the key file when the option is presented.
- Now go to the folder where you downloaded the key pair from AWS. Copy and paste that into a location where you would like to securely store your keys.
- Open puttygen while you are in the correct folder.
- In puttygen click `load`. In the popup window make sure to change the file type to All Files. Select the key pair information you downloaded from AWS.
- Open the key pair file, click `ok`
- On the next popup window puttygen will ask if you are sure you want to save the key without a passphrase. Click yes. Using a passphrase on the key is more secure but will cause issues with automation because it will require manual intervention. So just click yes and keep going.
- Name the key file and make sure to save it as a `.ppk` file.
- Now open putty.
- Now go back to the page for your EC2 instance. 
- Go to the instance details page. Click on `connect`.
- At line 4, where it says "Connect to your instance using its Public DNS:" a string of characters will be displayed. Something like: `ec2-xx-yy-zzz-aaa.compute-1.amazonaws.com` and a little icon you can use to copy this. Copy it.
- In putty, the screen should have an area for `hostname`. Enter *instance-user-name@instance-public-dns-name*. To find the instance user names of typical [AWS instances go here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/connection-prereqs.html#connection-prereqs-get-info-about-instance) or use one of these:
For Amazon Linux 2 or the Amazon Linux AMI, the user name is ec2-user.
For a CentOS AMI, the user name is centos or ec2-user.
For a Debian AMI, the user name is admin.
For a Fedora AMI, the user name is fedora or ec2-user.
For a RHEL AMI, the user name is ec2-user or root.
For a SUSE AMI, the user name is ec2-user or root.
For an Ubuntu AMI, the user name is ubuntu.
For an Oracle AMI, the user name is ec2-user.
For a Bitnami AMI, the user name is bitnami.
Otherwise, check with the AMI provider.
- In putty make sure that port 22 is selected.
- Then on the left within putty, click on the plus sign next to SSH.
- Then click on `auth`. Do not click on the plus sign next to `auth`, just click on `auth`.
- On the right side within putty, next to the field for `Private key for authentication` there will be a button called `browse`. Click it.
- In the popup window, find your key file, the one with the `.ppk` file extension and double click on it.
- Then, on the left hand side scroll back up to `session`, click `session`.
- Then on the right side in the field for `Saved Sessions` enter a session name that makes sense for this key and EC2 instance and save it.
- This way the connection and relevant key information will be saved and you don't have to do this rigamarole every time.
- Now select the connection you just named and click `open`.
- In the security popup click `yes`.
- A terminal window will open and connect to your EC2 instance.
 
Boom shakalaka 

### Additional stuff
- To disconnect from the instance type `exit` in the terminal window. This will close the connection.
- Then go to your running instance in the AWS cloud console.
- Select your particular instance (little box on the left is blue), then at the top of the screen where it says `Actions`, click the arrow and from the dropdown select `instance state` ===> `stop`
- You will be prompted to confirm that you do in fact want to stop the instance, do so.
- Sign out

Done

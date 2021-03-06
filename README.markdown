# Accessing the Build Server
http://tcarbonxtreme.tk/

# Authenticating to the Build Server
You must be a member of the androidarmv6 organization.  
Your membership must be "publicized". https://github.com/androidarmv6  
Jenkins will authorize using OAuth to GitHub.

You must also make sure your androidarmv6 membership is not concealed. You can do that here:  
https://github.com/androidarmv6  

# Using the Build Server
Click the "android" job.  
Configure what you want to build.  
Build it.  

# Modifying the local_manifest.xml
Edit ics.xml (the ics local_manifest.xml) and submit a pull request.  
Or edit gingerbread.xml (the gingerbread local_manifest.xml) and submit a pull request.  

# Adding Nodes to the Build Server
More nodes the better.  
To add a node, please open an issue (or do it yourself within Jenkins) with a externally accessible username and host name that Hudson can use to connect via SSH.  
Your build machine must also be completely/properly set up to support building Android. sudo/root access is not required.  
You can also configure your node to only perform builds during certain hours. This will prevent your machine from being swamped when during the hours you are planning on using it.  

The login provided should use allow access to the following public key via the authorized_keys file:  
https://github.com/TeamCarbonXtreme/hudson/blob/master/authorized_keys  

# Jenkins Job Setup
The job uses the following script:

```bash
curl -O -L https://raw.github.com/TeamCarbonXtreme/hudson/master/job.sh
. ./job.sh
```

# SSH access from Windows

## First, choose either EC2 or Ubuntu per these instructions

[What kind of Linux machine do I have?](./8-3-SSH-determining-your-machine.md)

## With Windows 10, a lot has been simplified for us in this workshop!

Please enable ssh on your machine:
https://www.howtogeek.com/336775/how-to-enable-and-use-windows-10s-built-in-ssh-commands/

If the above is successful, you will see this in your command line:

![alt text](/images/ssh_image.jpg)

### 1) Find your EC2 instance's Public IP
In AWS Click on EC2

Go to the Running Instances

Find and select your EC2 instance

Copy your EC2 instance's IPv4 Public IP

### 2) Log in from the command line

From your Downloads folder on the command line, use one of the following:

`ssh -i <keyname.pem> ec2-user@<IPv4 Public IP address>`

or

`ssh -i <keyname.pem> ubuntu@<IPv4 Public IP address>`

Example:
```
ssh -i ~/Downloads/leorentanyag.pem ec2-user@13.55.214.58
```

___

## Lower versions of windows

Unfortunately, the best SSH client for Windows also requires its own format. So the Windows steps will have two parts: A.) Generating the key, and B.) Using the key.

## A. Generate the key

### 1.) Go to the Putty webpage

Open up your browser and go to: http://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html

### 2.) Download PuTTY

Right-click and *Save As* the links for the latest installer. As of time of writing, it's **putty-0.67-installer.msi**

### 3.) Run the installer

Execute the MSI file, and go through the installation. It should install a couple of programs, but we only need two: *PuTTY* and *PuTTYGen*

### 4.) Start PuTTYGen

From the *Start* menu, choose **All Programs > PuTTY > PuTTYGen**.

Under **Type of key to generate**, select **SSH-2 RSA**.

### 5.) Load your Key Pair

Click on **Load**. By default, PuTTYgen displays only files with the extension `.ppk`. To locate your .pem file, select the option to display *All Files*.

Go to the directory where you downloaded your Key Pair, open the file, and click on *Open*.

### 6.) Save your private key

Choose **Save private key** to save the key in the format that PuTTY can use. PuTTYgen displays a warning about saving the key without a passphrase. Choose *Yes*.

### 7.) Name your key

Specify the same name for the key that you used for the key pair (for example, `banana-smith-keypair`)


## B. Logging in

### 1.) Start PuTTY

From the Start menu, choose **All Programs > PuTTY > PuTTY**

### 2.) Set your login

In the *Category* pane, select **Session** and complete the following fields based on your image type as per [these instructions](./8-3-SSH-determining-your-machine.md):


```
 Host: ec2-user@[PUBLIC IP]
 Port: 22
 Connection type: SSH
```


Make sure you replace *[PUBLIC IP]* with the *Public IP* of your EC2 instance. For example:

```
 Host: ec2-user@22.33.44.55
 Port: 22
 Connection type: SSH
```

OR

```
 Host: ubuntu[PUBLIC IP]
 Port: 22
 Connection type: SSH
```

### 3.) Select your key file

In the *Category* pane, expand **Connection**, expand **SSH**, and then select **Auth**.

Click on **Browse**. Select the `.ppk` file that you generated for your key pair, and then choose **Open**.

### 4.) Save your session

In the *Category* pane, select **Session**. Enter a name for the session under **Saved Sessions**.

Choose **Save**.

### 5.) Login!

Finally, that's all done. Click on **Open** to start the SSH session - it will display a security alert that you can safely ignore (at least for this session).

# Deploy a static website to S3

## Key Concepts

Before we get started, let's go over some basic concepts first:

 - *An EC2 Instance is a server in the cloud*. Think of it as a computer - your laptop, for example - that's installed somewhere else, and is available for you to access and manage. You can install and do whatever you want to that server.

 - *SSH is a way to remotely access that server*. You can either use a password or a key pair to access that server. Think of a key pair as a file that functions as a set of keys; you can duplicate, or transfer it to another computer, but you'll need that key to access your server.

 - *Security groups are like your firewall*. It's essentially a list of what kind of traffic you're allowing to your instance. This is important: you want remote *management* access to be narrowed down as much as possible.

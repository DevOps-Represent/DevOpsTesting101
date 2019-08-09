# Glossary

## AMI

**Amazon Machine Image**

AMIs are like a template of a computer's root drive. They contain the operating system and can also include software and layers of your application, such as database servers, middleware, web servers, and so on.

https://docs.aws.amazon.com/general/latest/gr/glos-chap.html#A

## EC2
**Elastic Compute Cloud**

A web service that enables you to launch and manage Linux/UNIX and Windows Server instances in Amazon's data centers.
https://aws.amazon.com/ec2/

## Keypair

A form of encryption that permit the "keys to the door". There are two keys (public and private) that act in a pair; which is why it's known as a keypair.

More here: https://www.ssl2buy.com/wiki/what-is-a-public-and-private-key-pair


## Security Groups

**Security groups are like your firewall**

It's essentially a list of what kind of traffic you're allowing to your instance. This is important: you want remote *management* access to be narrowed down as much as possible.

Each security group consists of a list of protocols, ports, and IP address ranges. A security group can apply to multiple instances, and multiple groups can regulate a single instance.

https://docs.aws.amazon.com/general/latest/gr/glos-chap.html#S

## SSH

**Secure Shell**

SSH, or Secure Shell, is a remote administration protocol that allows users to control and modify their remote servers over the Internet. The service was created as a secure replacement for the unencrypted Telnet and uses cryptographic techniques to ensure that all communication to and from the remote server happens in an encrypted manner. It provides a mechanism for authenticating a remote user, transferring inputs from the client to the host, and relaying the output back to the client.

https://www.hostinger.com/tutorials/ssh-tutorial-how-does-ssh-work

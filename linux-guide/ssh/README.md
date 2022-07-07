# SSH connection

SSH provides a secure way to connect dirrectly to remote server through port 22. In practice, SSH is usually used in private network environment with logical IP.

## SSH using symetric key (SSH key):

* Prerequisites:
  * openssh 
  * ssh-keygen

**step 1**:

Generate a key pair to indentify your machine

```
> ssh-keygen -t rsa -b 4096
```

The key pair is then stored in `~/.ssh` as `id_rsa` and `id_rsa.pub` (private and public key) 

**step 2**:

Print out the value of the public key 

```
> cat ~/.ssh/id_rsa.pub
```

**step 3**:

At remote machine - in case, you haven't accessed the remote yet, contact remote machine owners, give them the key and they will do step 3 for you.
Copy the value in step 2 and move to `~/.ssh` and paste it in `authorized_keys` (if the file doesn't exist, create a new one).

```
#  
> nano ~/.ssh/authorized_keys
```

## Let's SSH

```
> ssh <username>@<ip-address | hostname>
```


## SSH Tuneling:

When you want to forward port from remote host to local or vice versa, SSH Tuneling will do the job for you.

```
> ssh -N -L <local ipadd | local hostname>:<local port>:<remote ipadd | remote hostname>:<remote port> <remote username>:<remote ipadd | remote hostname> 

# e.g:
# ssh -N -L localhost:8088:localhost:8088 root@node1 
```


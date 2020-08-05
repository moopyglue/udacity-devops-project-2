# udacity-devops-project-2

## For Review

The code for reveiwing is in the final_submission folder

## Alternative with bastion

An alternative version which provides a bastion host is in the non_rubic_solution_with_bastion folder.

the 'diff' of these 2 folders is in the 'diff.txt' file

## Script usage notes:

### 'stack'

```bash
$ ./stack create udacity-devops-project-2 --capabilities CAPABILITY_IAM
$ ./stack update udacity-devops-project-2 --capabilities CAPABILITY_IAM
$ ./stack delete udacity-devops-project-2
```

```bash
$ ./stack create bastion 
$ ./stack update bastion
$ ./stack delete bastion
```

### 'jump'

```bash
$ ./jump 34.219.36.119
scp -i ~/.ssh/udp2-ssh-bastion.pem /home/simon/.ssh/udp2-ssh-privatesubnet.pem ubuntu@34.219.36.119:
The authenticity of host '34.219.36.119 (34.219.36.119)' can't be established.
ECDSA key fingerprint is SHA256:kE38009qNM36JTthUbZJHcimJ07wHp27xdr6iLcMmpk.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '34.219.36.119' (ECDSA) to the list of known hosts.
udp2-ssh-privatesubnet.pem                                                            100% 1674     8.3KB/s   00:00
ssh -i ~/.ssh/udp2-ssh-bastion.pem ubuntu@34.219.36.119
Welcome to Ubuntu 18.04.4 LTS (GNU/Linux 4.15.0-1065-aws x86_64)
```
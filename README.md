# AWS Bastion host

A simple aws ec2 instance running Ubuntu in a public subnet accessible via SSH.
To generate a key use

```
ssh-keygen -t rsa -b 2048 -m PEM -f terraform_ec2_key
```

which generates in the current directory a public (terraform_ec2_key.pub) and private key.
Use the private key to connect via SSH to the instance with:

```
ssh -i terraform_ec2_key ubuntu@<public_ip_address>
```

The public IP address of the instance is visible via the AWS console.

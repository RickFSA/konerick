# Create SSH Keys (Linux and MacOS)

[Documentation](https://cloud.google.com/compute/docs/connect/create-ssh-keys)

### Create .ssh/ folder in your home directory
```shell
mkdir .ssh/
```

### Navigate to .ssh/ folder
```shell
cd .ssh/
```

### Generate SSH keys
```shell
ssh-keygen -t rsa -f ~/.ssh/<KEY_FILENAME> -C <USERNAME> -b 2048
```

* `KEY_FILENAME`: the name for SSH key file
* `USERNAME`: your username on the Virtual Machine(VM)

The above action will generate 2 files on the .ssh/ folder
* `KEY_FILENAME` This is your private key
* `KEY_FILENAME.pub` This is your public key

### Add public SSH Key to your GCP > Compute Engine > Metadata > SSH KEYS
```shell
cat <KEY_FILENAME>.pub
```
Use command `cat` to open the public key
# Create SSH Keys 

Follow the [link][https://cloud.google.com/compute/docs/connect/create-ssh-keys] to documentation

```shell
ssh-keygen -t rsa -f ~/.ssh/<KEY_FILENAME> -C <USERNAME> -b 2048
```

    * `KEY_FILENAME`: the name for SSH key file
    * 
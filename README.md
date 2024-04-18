# Homeserver setup

## Using Ansible Vault

Create an executable file `vault_pass.sh`
```sh
#!/bin/sh
keepassxc-cli show -y 2:xxxxxxx ~/Documents/Safe.kdbx "/Homeserver/Ansible vars" -a Password
```


## Tags

| Tag              | Description                                              | Run on service |
| ---------------- | -------------------------------------------------------- | -------------- |
| `$service-start`  | Run service                                              | x              |
| `$service-stop`   | Stop service                                             |                |

## Acknowledgements

Inspiration is taken from [davestephens/ansible-nas](https://github.com/davestephens/ansible-nas).

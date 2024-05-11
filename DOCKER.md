
Install docker:

```bash
curl -sSL https://get.docker.com | sh
```

Add our current user to the docker group by using the usermod command as shown below. By using “$USER” we are inserting the environment variable that stores the current users name.
```bash
sudo usermod -aG docker $USER
```

Then logout using the command:
```bash
logout
```

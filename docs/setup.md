## Docker Setup For Linux

> Ref Link : https://docs.docker.com/engine/install/

### Update & Upgrade The Syatem(Optional)

```bash
sudo apt-get remove docker docker-engine docker.io containerd runc
```

### Set Up The Repository

```bash
sudo apt-get update
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

### Install Docker Engine

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io
```

### Add User To Docker Group

```bash
sudo usermod -aG docker $USER
su - $USER
```

### To Test
```
docker run akshayithape/hello-docker
```

## Docker Setup For Windows

> Ref Link : https://docs.docker.com/docker-for-windows/install/

> Note : Follow The Step's Which Given In Above Link.

## Play With Docker

> Ref Link : https://labs.play-with-docker.com/

1. Create A Docker Hub ID.(https://hub.docker.com/signup/)
2. Verify Email Address
3. Accessing Docker Lab(https://labs.play-with-docker.com/)
4. Add a Docker Instance(Click on ‘ADD NEW INSTANCE’ label under Instance in the left hand side navbar. This will spawn up a docker instance for running lab tasks.)

> Congratulations ! You have successfully setup your lab. 
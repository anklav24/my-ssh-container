```bash
docker build -t my-ssh-container .
docker run --rm -d -p 2222:22 --name my-ssh-container my-ssh-container

sudo nmap -p 2222 localhost  # check
ssh root@localhost -p 2222  # check
```

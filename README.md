```bash
docker build -t my-ssh-container .
docker run --rm -d -p 2222:22 --network=YOUR_NETWORK --name my-ssh-container my-ssh-container  # on remote pc with docker

sudo nmap -p 2222 localhost  # check on your local pc
ssh root@localhost -p 2222  # check on your local pc

ssh root@your_server_ip_or_domain_name -L 2222:localhost:2222  # Create ssh tunnel pass 2222 from remote pc to your pc, need to run on your local pc
# Go to db manager (DBeaver or DataGrip)
# Create a connection with ssh forward to my-ssh-container
# Add db with port and name your db container
```

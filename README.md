# docker swarm app
TODO: Build and run manually
- Needs local version of redis + mongo
- Run all services, visit port 4000

Build all images and push to dockerhub
- Update build instructions to push to your own dockerhub (probably super slow)
- quick command `npm run deploy`
- update docker compose to pull from your images
- Run on ec2

# ec2 instructions
## Set permissions (if linux/mac)
- `sudo chmod 400 <keyname>.pem`
## Connect to instance
- `ssh -i "keyname.pem" ubuntu@youripaddress`
## Setup instance
- https://docs.docker.com/engine/install/ubuntu/ but add the folling certificats below
- `sudo apt-get update`
- `sudo apt-get upgrade`
- `sudo apt install apt-transport-https ca-certificates curl software-properties-common`
- `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`
- `sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu eoan test"`
## Clone repo
- `git clone <repo>`
- cd into repo
## Initialize swarm
- `sudo docker swarm init`
- `npm run deploy`
- `sudo npm run deploy`
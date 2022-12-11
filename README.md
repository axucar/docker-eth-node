To create the containers:
- `sudo docker-compose up -d` where `d` is a silencer (Docker runs in background)

To monitor logs:
- `sudo docker-compose logs --tail 10` , shows the most recent 10 lines from each container

To stop containers:
- `sudo docker-compose stop`    
    - `sudo docker-compose start` resumes the clients (containers)
    - Furthermore, one can use `sudo docker-compose down` after stopping (say if you made changes to the yaml file) to remove the containers

To see status of containers:
- `sudo docker-compose ps` shows what containers are running

To see syncing status: run `geth attach` to open Geth’s Javascript console
- `sudo docker-compose exec geth geth attach`
- Run `eth.syncing` in the Javascript console 
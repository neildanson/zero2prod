Install PSQL

https://www.timescale.com/blog/how-to-install-psql-on-mac-ubuntu-debian-windows/


On Windows - 

* Use WSL (2). 
* Docker inside WSL
    * Docker must be running on Windows host. 
* Additional commands required -    
    - apt-get
        * openssl
        * libssl-dev


DOCKER Commands
Start Postgres & update DB

`./scripts/init_db.sh`

Just update DB

`SKIP_DOCKER=true ./scripts/init_db.sh`
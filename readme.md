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

curl -i -X POST -d 'email=thomas_mann@hotmail.com&name=Tom' http://127.0.0.1:8000/subscriptions


    {"v":0,"name":"zero2prod","msg":"[ADDING A NEW SUBSCRIBER - START]","level":30,"hostname":"WINDOWS-IUONSS7","pid":3253,"time":"2023-05-19T15:56:42.01385883Z","target":"zero2prod::routes::subscriptions","line":12,"file":"src/routes/subscriptions.rs","subscriber_email":"neil.danson@gmail.com.com","subscriber_name":"Tom","request_id":"f7444167-77a0-49f1-acb1-174fe5986afc"}

    {"v":0,"name":"zero2prod","msg":"[SAVING NEW SUBSCRIBER DETAILS IN THE DATABASE - START]","level":30,"hostname":"WINDOWS-IUONSS7","pid":3253,"time":"2023-05-19T15:56:42.013937439Z","target":"zero2prod::routes::subscriptions","line":28,"file":"src/routes/subscriptions.rs","subscriber_email":"neil.danson@gmail.com.com","subscriber_name":"Tom","request_id":"f7444167-77a0-49f1-acb1-174fe5986afc"}

    {"v":0,"name":"zero2prod","msg":"[SAVING NEW SUBSCRIBER DETAILS IN THE DATABASE - EVENT] INSERT INTO subscriptions (id, …; rows affected: 1, rows returned: 0, elapsed: 1.408ms\n\nINSERT INTO\n  subscriptions (id, email, name, subscribed_at)\nVALUES\n  ($1, $2, $3, $4)\n","level":30,"hostname":"WINDOWS-IUONSS7","pid":3253,"time":"2023-05-19T15:56:42.016858411Z","target":"log","line":null,"file":null,"log.module_path":"sqlx::query","log.target":"sqlx::query","subscriber_email":"neil.danson@gmail.com.com","subscriber_name":"Tom","request_id":"f7444167-77a0-49f1-acb1-174fe5986afc"}

    {"v":0,"name":"zero2prod","msg":"[SAVING NEW SUBSCRIBER DETAILS IN THE DATABASE - END]","level":30,"hostname":"WINDOWS-IUONSS7","pid":3253,"time":"2023-05-19T15:56:42.016936171Z","target":"zero2prod::routes::subscriptions","line":28,"file":"src/routes/subscriptions.rs","subscriber_email":"neil.danson@gmail.com.com","subscriber_name":"Tom","elapsed_milliseconds":2,"request_id":"f7444167-77a0-49f1-acb1-174fe5986afc"}

    {"v":0,"name":"zero2prod","msg":"[ADDING A NEW SUBSCRIBER - END]","level":30,"hostname":"WINDOWS-IUONSS7","pid":3253,"time":"2023-05-19T15:56:42.01699327Z","target":"zero2prod::routes::subscriptions","line":12,"file":"src/routes/subscriptions.rs","subscriber_email":"neil.danson@gmail.com.com","subscriber_name":"Tom","elapsed_milliseconds":3,"request_id":"f7444167-77a0-49f1-acb1-174fe5986afc"}

    {"v":0,"name":"zero2prod","msg":"127.0.0.1 \"POST /subscriptions HTTP/1.1\" 200 0 \"-\" \"curl/7.81.0\" 0.003372","level":30,"hostname":"WINDOWS-IUONSS7","pid":3253,"time":"2023-05-19T15:56:42.017065849Z","target":"log","line":null,"file":null,"log.module_path":"actix_web::middleware::logger","log.file":"/home/neild/.cargo/registry/src/index.crates.io-6f17d22bba15001f/actix-web-4.3.1/src/middleware/logger.rs","log.target":"actix_web::middleware::logger","log.line":421}
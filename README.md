# turtl-docker

Docker file to run turtl (turtl.it) api server

## How to run ?

```
sudo docker run -d -p 443:443 -v $(pwd)/uploads:/opt/api/uploads -v $(pwd)/volume:/var/lib/rethinkdb/instance1 -t turtl_docker
```

-e LOCAL_UPLOAD_URL=http://turtl.domain.com/api

## Configuration

The image supports the following environment variables that will be injected in the configuration at each restart of the container :

- PIDFILE: defaults to 'nil'
- BINDADDR: defaults to '0.0.0.0'
- BINDPORT: defaults to '8181'
- PROD_ERR_HANDLING: defaults to 't'
- FQDN: defaults to 'turtl.local'
- SITE_URL: defaults to 'http://turtl.local'
- SMTP_HOST: default to 'localhost'
- ADMIN_EMAIL: defaults to 'root@example.com'
- EMAIL_FROM: defaults to 'noreply@example.com'
- SMTP_USER: defaults to empty
- SMTP_PASS: defaults to empty
- DISPLAY_ERRORS: defaults to 't'
- DEFAULT_STORAGE_LIMIT: defaults to 100
- STORAGE_INVITE_CREDIT: defaults to 25
- LOCAL_UPLOAD_URL: defaults to http://turtl.local
- LOCAL_UPLOAD_PATH: defaults to "/opt/api/uploads"
- AWS_S3_TOKEN: defaults to "(:token ''
                              :secret ''
                              :bucket ''
                              :endpoint 'https://s3.amazonaws.com')"

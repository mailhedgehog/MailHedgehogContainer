# MailHedgehog docker compose configuration

## Usage
```shell
mkdir mailhedgehog
cd mailhedgehog
git clone https://github.com/mailhedgehog/MailHedgehogContainer.git .
chmod +x entrypoint.sh
# Add auth files
mkdir storage
touch storage/.mh-config.yml
touch storage/.mh-authfile
# Or use some repo for this
#git clone host:package/MailHedgehogThink.git storage
docker-compose pull
docker-compose up -d
```

## Email sending examples

Laravel:

```dotenv
# http://XX.XX.XX.XX:1034/box
MAIL_MAILER=smtp
MAIL_HOST=XX.XX.XX.XX
MAIL_PORT=1033
MAIL_USERNAME=username_XXXX-XXXX-XXXX-XXX
MAIL_PASSWORD=*****************
MAIL_ENCRYPTION=null
```

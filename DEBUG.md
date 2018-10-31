
Build debug image

````
make binary

docker build -t reg-dhc.app.corpintra.net/sbuerin/traefik:v1.6.5 .                      
docker --config ~/.docker-sbuerin push reg-dhc.app.corpintra.net/sbuerin/traefik:v1.6.5                      

/tmp/dlv attach "$(ps aux | grep 'traefik --configFile' | grep -v grep | awk '{print $2}')" --api-version=2 --listen=:2345 --headless

````
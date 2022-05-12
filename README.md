# Broker MQTT 

This is a docker-compose file to run a mosquitto mqtt broker in a docker container

# Initialization

### Clone repo and create dirs and password file

```
git clone https://github.com/devnido/mosquitto-docker

cd mosquitto-docker

mkdir data

mkdir log

mv ./config/pwfile.example ./config/pwfile
```

### Start container

```
docker-compose up -d
```

### Encrpyt password file

```
docker exec -it mqtt mosquitto_passwd -U /mosquitto/config/pwfile

docker restart mqtt
```

# Authentication

default credentials

```
username: admin
password: 1234567890
```



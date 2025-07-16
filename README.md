
## <p align="center">eXo platform Community Edition</p>

This repository is a helper to deploy an eXo Platform using a docker compose file and traefik.

## 🧐 Features    
- Using docker compose version 2
- Traefik as an tcp/http edge proxy
- eXO Platform CE
        
## 🛠️ Tech Stack
- [eXo Platform 7.0.0 on docker](https://hub.docker.com/r/exoplatform/exo-community)
- [Traefik edge proxy](https://doc.traefik.io/traefik/)
- [MySQL](https://www.mysql.com/)
- [Elasticsearch](https://www.elastic.co)
- [ONLYOFFICE Document Server](https://www.onlyoffice.com)

## 🧑🏻‍💻 Usage

```Bash
# Build
$ docker compose build
```

```Bash
# Launch
$ docker compose up -d
```

```Bash
# Cleaning all volumes
$ docker compose down -v
```

## 🛠️ Connection

### Database
Access the MySQL database using a SQL client like [DBeaver](https://dbeaver.io/).


### Administration portal
Access the eXo platform using [this URL](http://exoapp.localtest.me)

## 🧑🏻‍💻 Security notice

- This configuration uses default credentials that MUST be changed
- SSL/TLS is not configured - HTTPS is strongly recommended
- Database ports are exposed with default passwords
- JWT secrets are hardcoded in this configuration

### Before deployment
- Thanks to localhost.me no need to add 'exoapp.localtest.me' to your hosts file (or configure proper DNS)
- Configure firewall rules for ports 80 (HTTP) and 443 (HTTPS)
- Generate proper SSL certificates for production use with traefik
- Replace all default passwords and secrets

### Production recommendations
- Use external secret management (e.g: docker secret using docker Swarm)
- Implement proper backup strategy
- Configure resource limits
- Set up monitoring and logging
- Enable HTTPS with Let's Encrypt or other CA with traefik

## 🍰 Contributing    
Contributions are what make the open source community such an amazing place to be learn, inspire, and create. 
Any contributions you make are **greatly appreciated**.

## 🙇 Author
#### JS
- Github: [@jsminet](https://github.com/jsminet)
        
## ➤ License
Distributed under the MIT License. See [LICENSE](LICENSE) for more information.
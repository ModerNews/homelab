# Homelab configs
This repository contains basic configuration files for monitoring/managing/git of home server.

## Services
### Monitoring
- [x] [Prometheus](https://prometheus.io/)
- [x] [Grafana](https://grafana.com/)
- [x] Node Exporter
- [ ] Alert Manager
- [ ] Nginx Monitoring
- [x] Gitea Monitoring

### Git & CI/CD
Git server is running a [Gitea](https://gitea.io/) instance. CI/CD is still awaiting configuration.

### Reverse Proxy
Reverse proxy is handled by Nginx:
- [ ] "/" -> home page
- [x] "/grafana" -> Grafana
- [ ] "/prometheus" -> Prometheus
- [x] "/git" -> Gitea

## Configuration Files:
- compose.yaml: Docker compose file for services
- prometheus.yml: Prometheus configuration file
- grafana.ini: Grafana configuration file
- app.ini: Gitea configuration file
- reverse-proxy/*: Nginx configs & logs

## Usage
1. Clone the repository
2. Modify the configuration files as needed (passwords, domain, etc.; inner routing is pre-configured)
3. Run `docker-compose up -d` in the repository directory
4. Access services via reverse proxy as configured above

## TODO
- [ ] Add CI/CD configuration
- [ ] Replace empty fields in configs with env variables

## Useful Scripts
- [github2gitea-mirror.sh](https://github.com/maxkratz/github2gitea-mirror): Mirror whole GitHub Users/Organizations to Gitea

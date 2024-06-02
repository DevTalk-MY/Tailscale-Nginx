# Tailscale-Nginx

### Pre-requisites :
1. one cloud vm
2. Tailscale account

### Step-by-step : 

#### 1. Local Device

- [x] Deploy a service locally
- [x] Add local device into tailscale 

#### 2. Cloud server

- [x] Register another Tailscale account
- [x] Install Tailscale [here](https://tailscale.com/download/linux)
- [x] Connect to Tailscales - [CLI Reference](https://tailscale.com/kb/1241/tailscale-up)
```bash
sudo tailscale up
```
- [x] Check whether device is connected to Tailscale
```bash
tailscale status
```
- [x] Install NGINX - [reference here](https://ubuntu.com/tutorials/install-and-configure-nginx#2-installing-nginx)
- [x] Use `proxy_pass` to pass a request to proxied server (local) - [reference here](https://docs.nginx.com/nginx/admin-guide/web-server/reverse-proxy/)
- [x] Restart Nginx service
```bash
sudo service nginx restart
```
- [x] Install Let's Encrypt certbot [tutorials here](https://sheraziqbal.medium.com/adding-free-ssl-from-lets-encrypt-to-your-domain-with-nginx-on-ubuntu-ec2-509d9dc7b193)
```
sudo certbot --nginx -d devtalk-26.malaysia-ai.org -d devtalk-26.malaysia-ai.org
```
- [x] Re-configure nginx configuration
- [x] Enable port 443 on lightsail firewall
- [x] Restart Nginx service

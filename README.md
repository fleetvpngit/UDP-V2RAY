ABRIR UDP NO SERVIDOR

Configure o json do servidor v2ray, /etc/v2ray/config.json. Adicione o udp true depois do ],

```sh
"settings": {

  "clients": [
  
    {
	
      "id": "UUID-do-cliente",
	  
      "alterId": 64
	  
    }
	
  ],
  
  "udp": true
  
},
```

```sh
sudo systemctl restart v2ray
sudo service v2ray restart
```

SER USAR UFW
```sh
sudo ufw allow 22/tcp
sudo ufw status
sudo ufw enable
```

LIBERAR TUDO NO UFW
```sh
sudo ufw allow proto udp from any to any
sudo ufw allow proto tcp from any to any
```
```sh
sudo ufw reload
sudo ufw status verbose
```



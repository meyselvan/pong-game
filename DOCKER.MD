# Dockerlaştırma Rehberi

Bu projedeki websitesi docker içinde çalışmalı ve tek komut ile ayağa kalkmalıdır. Docker için gereken root yetkisinden dolayı kampüs bilgisayarlarında kullanılabilecek farklı çözümler vardır.

- 


## 📁 Docker Yapısı

```
pong-game-v2/
├── backend/         
│   ├── src/       
│   	└── services/
│   		└── auth-service/
│   		└── chat-service/
│   		└── friend-service/
│   		└── game-service/
│   		└── user-service/
├── frontend/       
│   ├── src/        
│   	└── nginx/
│   		└── nginx.conf
│   		└── setup.sh
│   		└── Dockerfile
└── docker-compose.yml
```

### Host bilgisayardan VM'e klasör gönderme komutu:

```bash
scp -r -P 3022 ./ml relvan@127.0.0.1:/home/relvan/
```

## 1. Backend Servisleri

## 2. Frontend Servisleri

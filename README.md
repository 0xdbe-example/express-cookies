# Express Cookies

This application is a demonstration prototype just to show how to use cookie with ExpressJS

- Create self-signed certificate (prime256v1)

```
openssl req \
  -x509 \
  -subj "/C=FR/ST=Paris/L=Paris/O=Security/OU=IT Department/CN=www.example.com" \
  -nodes \
  -days 365 \
  -newkey ec:<(openssl ecparam -name prime256v1) \
  -keyout tls/key.pem \
  -out tls/cert.pem 
```

- Install Express

```
npm install
```

- Run

```
node app.js
```

- Open https://localhost:3000/

- Check security properties for ``connect.sid`` cookie (HttpOnly, Secure and SameSite = Strict)

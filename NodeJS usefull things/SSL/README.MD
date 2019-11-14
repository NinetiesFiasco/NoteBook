Сервер с SSL на 443 порту
-

'''
const https = require("https");
const fs = require("fs");
const port = 443;
const express = require("express");
const app = express();


var privateKey = fs.readFileSync( 'privateKey.key' );
var certificate = fs.readFileSync( 'sert.crt' );

app.get("/",function(request,response){
    response.send("<h2>Hello here</h2>");
});


https.createServer({
    key: privateKey,
    cert: certificate
}, app).listen(port);
'''


### Тут можно сгенерить халявный сертификат
https://regery.com.ua/ru/security/ssl-tools/self-signed-certificate-generator  
Домен и поддомен должен обязательно совпадать с имеющимся

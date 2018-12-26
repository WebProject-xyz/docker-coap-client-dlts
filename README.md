# docker-coap-client-dlts (LIBCOAP)
https://github.com/home-assistant/libcoap/tree/dtls with DLTS dockerized

## Credits
all credits go to https://github.com/home-assistant/libcoap/graphs/contributors

## Usage
##### Build 
`docker build -t webproject/coap-client:latest . `

#### Run command in Docker
#### Generate API User and <COAP_API_KEY> (Shared Key)
`docker run --rm --net=host --name coap-client webproject/coap-client -m post -u "Client_identity" -k "<COAP_GATEWAY_SECRET>" -e '{"9090":"php-api-user"}' "coaps://<COAP_GATEWAY_IP>:5684/15011/9063""`

#### Get all api endpoints
`docker run --rm --net=host --name coap-client webproject/coap-client -m get -u "php-api-user"  -k "<COAP_API_KEY>" "coaps://<COAP_GATEWAY_IP>:5684/.well-known/core"` 

#### Show help
`docker run -rm --net=host --name coap-client webproject/coap-client`

## License
see creators licence: at https://github.com/home-assistant/libcoap/tree/dtls 
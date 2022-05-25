##Build

This application uses the OpenAPI and AsyncAPI Generator CLI to generate the respective server code. Listed below are the steps to: <br />
1) Generate RestAPI server code. <br />
2) Generate AsyncAPI server code. <br />

###Generate Rest API

1) Pull the OpenAPI Generator CLI docker image
```sh
docker pull openapitools/openapi-generator-cli
```

2) Run a container with the following arguments:
- -i: Location of OpenAPI spec. <br />
- -g: The server implementation (eg go, go-gin-server) <br />
- -o: The output location <br />

```sh
docker run --rm -v "${PWD}:/local" openapitools/openapi-generator-cli generate \
-i /local/api/openapi.yaml \
-g go-gin-server \
-o /local/out/go
```

###Generate Async API - [WIP]

1) [WIP]
```sh
npm install -g @asyncapi/generator
# clone this repository and navigate to this repository
ag test/asyncapi.yaml @asyncapi/go-watermill-template -o /path/to/generated-code -p moduleName=your-go-module-name
```

##Run [WIP]
###Locally
1) [WIP]

##Docker [WIP]
1) [WIP]

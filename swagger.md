## swagger-editor

https://github.com/swagger-api/swagger-editor

run command prompt

```
docker pull swaggerapi/swagger-editor
docker run -d -p 1000:8080 swaggerapi/swagger-editor
```

This will run Swagger Editor (in detached mode) on port 1000 on your machine, so you can open it by navigating to http://localhost:1000 in your browser.

[http://localhost:1000/](http://localhost:1000/)


## swagger-viewer

### how to generate swagger documents(html file)

#### run visual studio code

##### install Extension

- Swagger viewer
- swagger-doc-viewer
- swaggitor


#### open terminal

```
npm install -g bootprint
npm install -g bootprint-openapi
bootprint openapi [yaml file path] [output path]
```

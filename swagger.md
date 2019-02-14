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

## swagger-codegen

### YAMLからSwaggerCodegen によって、コードを生成する方法

以下をDownloadする。

[http://repo1.maven.org/maven2/io/swagger/swagger-codegen-cli/2.4.1/swagger-codegen-cli-2.4.1.jar](http://repo1.maven.org/maven2/io/swagger/swagger-codegen-cli/2.4.1/swagger-codegen-cli-2.4.1.jar)

```
./swagger_codegen
```

に置く

./swagger_codegen/config.jsonを以下の内容で作成する。

```
{
  "packageName": "Hogehoge.IO.Swagger"
}
```

※Hogehoge.IO.Swagger は任意

```
cd ./swagger_codegen
java -jar swagger-codegen-cli-2.4.1.jar generate -l csharp -i [yaml file path] -o Output -c config.json
```

output フォルダが出力される。

```
cd output
build.bat
```


#### View Help

java -jar swagger-codegen-cli-2.4.1.jar config-help -l csharp

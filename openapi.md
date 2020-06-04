
https://openapi-generator.tech/docs/generators/

https://github.com/OpenAPITools/openapi-generator

```
git clone https://github.com/openapitools/openapi-generator
cd openapi-generator
mvn clean package
java -jar modules/openapi-generator-cli/target/openapi-generator-cli.jar generate \
   -i [yaml file path]
   -g [ref https://openapi-generator.tech/docs/generators/ ] \
   -o [output dir path]
```

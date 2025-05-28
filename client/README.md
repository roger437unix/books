![](https://cdn.prod.website-files.com/6746e4625c4bb3fb49ba7f5b/676d3ea364ffa788c0227f94_Blockchain%20Main%20Image%20(1).webp)

# nodebooks Front-end

### Alterar o endereço do Back-end

./src/components/Books.vue [Linha 200]

### Executar o Frontend local

npm i

npm run dev -- --host

# Criar e enviar para ACR imagem Docker

### No terminal Shell

$SERVER="Servidor de logon"

echo $SERVER

docker login $SERVER

docker build --tag $SERVER/front-vue-9000 .

docker images

docker run -d --rm --name vue-9000 -p 9000:9000 $SERVER/front-vue-9000

http://localhost:9000/books

docker push $SERVER/front-vue-9000

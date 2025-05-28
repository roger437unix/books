![](https://blog.appseed.us/content/images/2021/08/icons-flask-x500w.png)

# pybooks Back-end

# Executar local em Debian GNU/Linux

python -m venv .venv

source .venv/bin/activate

python3 -m pip install --upgrade pip

pip install -r requirements.txt

python3 app.py

http://127.0.0.1:8080/ping

http://127.0.0.1:8080/books


# Criar e enviar para ACR imagem Docker utilizando WSL

### No terminal Shell

export SERVER="Servidor de logon"

echo $SERVER

docker login $SERVER

docker build --tag $SERVER/api-flask-8080 .

docker images

docker run -d --rm --name api -p 8080:8080 $SERVER/api-flask-8080

http://localhost:8080/books

docker push $SERVER/api-flask-8080

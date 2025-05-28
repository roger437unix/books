![](https://blog.appseed.us/content/images/2021/08/icons-flask-x500w.png)

# pybooks Back-end

# Executar local

python -m venv .venv

.venv\Scripts\activate

python -m pip install --upgrade pip

pip install -r requirements.txt

python app.py

http://127.0.0.1:8080/ping <br>
http://127.0.0.1:8080/books


# Criar e enviar para ACR imagem Docker utilizando WSL

### No Windows PowerShell

$Env:SERVER="Servidor de logon"

$Env:SERVER

wsl docker login $Env:SERVER

wsl docker build --tag $Env:SERVER/apiflask-8080 .

wsl docker images

wsl docker run -d --rm --name api -p 8080:8080 $Env:SERVER/apiflask-8080

http://localhost:8080/books

wsl docker push $Env:SERVER/apiflask-8080

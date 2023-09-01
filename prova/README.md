# Prova

### Backend

O Dockerfile do backend é baseado na imagem oficial do Python 3.9. Essa escolha foi feita porque a aplicação backend é escrita em Python 3.9. Além disso, o Dockerfile copia o arquivo `main.py`, `usuarios.db` e o `requirements.txt` para o contêiner. O arquivo `requirements.txt` é usado para instalar as dependências Python necessárias para o projeto.

### Frontend

O Dockerfile do frontend é baseado na imagem oficial do Node.js 14. Essa escolha foi feita porque a aplicação frontend é escrita em JavaScript e usa o ambiente Node.js. O Dockerfile copia os arquivos `index.html`, `server.js`, `package.json` para o contêiner. Em seguida, ele executa o comando `npm install` para instalar as dependências do frontend.

## docker-compose.yml

O arquivo docker-compose.yml é responsável por definir e gerenciar os serviços e a rede do projeto.

### Backend

O serviço backend é definido usando a imagem criada a partir do Dockerfile.backend. Ele também mapeia a porta 8000 do contêiner para a porta 8000 do host para que a aplicação backend possa ser acessada externamente.

### Frontend

O serviço frontend é definido usando a imagem criada a partir do Dockerfile.frontend. Ele também mapeia a porta 3000 do contêiner para a porta 3000 do host para que a aplicação frontend possa ser acessada externamente.

### Comandos 

docker-compose up
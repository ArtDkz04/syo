# backend/Dockerfile

# Use uma imagem base do Node.js leve e segura
FROM node:18-alpine

# Define o diretório de trabalho dentro do contêiner
WORKDIR /app

# Instala ferramentas necessárias: Cliente PostgreSQL (pg_dump) e Bzip2
RUN apk add --no-cache postgresql-client bzip2

# Copia os arquivos de definição de pacotes
COPY package*.json ./

# Instala as dependências da aplicação
RUN npm install

# Copia todos os outros arquivos da aplicação
COPY . .

# Cria a pasta de backups dentro do container para garantir permissões
RUN mkdir -p /app/backups

# Expõe a porta que a aplicação vai rodar
EXPOSE 3000

# Comando para iniciar a aplicação quando o contêiner iniciar
CMD [ "node", "server.js" ]
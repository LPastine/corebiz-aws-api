# Corebiz AWS API

## Instalar serverless framework

```zsh
npm install -g serverless
```

MacOS/Linux

```zsh
sudo npm install -g serverless
```

## Instalar dependências

```zsh
npm install aws-sdk
npm install uuidv4
```

## Verificar versão e instalação

```zsh
serverless
serverless --version
```

## Configurar IAM credentials em AWS

1. Procurar por IAM em AWS Services
2. Entrar em Usuários
3. Adicionar novo usuário
4. User name => serverless
5. Click em acesso programático
6. Next
7. Attach policy => AdministratorAccess
8. Next
9. Criar usuário

```zsh
serverless config credentials --provider aws --key {Access Key ID} --secret {Access Secret}
```

## Criar projeto e boilerplate

```zsh
mkdir {nome_do_projeto}
cd {nome_do_projeto}
sls create -t aws-nodejs
```

## Deploy

```zsh
sls deploy
```

## Endpoints da API

POST - https://se3l85r4x5.execute-api.us-east-2.amazonaws.com/dev/leads
GET - https://se3l85r4x5.execute-api.us-east-2.amazonaws.com/dev/leads
PUT - https://se3l85r4x5.execute-api.us-east-2.amazonaws.com/dev/leads/{id}
DELETE - https://se3l85r4x5.execute-api.us-east-2.amazonaws.com/dev/leads/{id}

## Testar CORS

Tem que ter "Access-Control-Allow-Origin: \*" na resposta.

### Obter dados de permissões GET

```zsh
curl -H "Origin: http://localhost" \
-H "Access-Control-Request-Method: GET" \
-H "Access-Control-Request-Headers: X-Requested-With" \
-X OPTIONS --verbose \
https://se3l85r4x5.execute-api.us-east-2.amazonaws.com/dev/leads
```

### Obter dados de permissões POST

```zsh
curl -H "Origin: http://localhost" \
-H "Access-Control-Request-Method: POST" \
-H "Access-Control-Request-Headers: X-Requested-With" \
-X OPTIONS --verbose \
https://se3l85r4x5.execute-api.us-east-2.amazonaws.com/dev/leads
```

### Obter dados de permissões PUT

```zsh
curl -H "Origin: http://localhost" \
-H "Access-Control-Request-Method: PUT" \
-H "Access-Control-Request-Headers: X-Requested-With" \
-X OPTIONS --verbose \
https://se3l85r4x5.execute-api.us-east-2.amazonaws.com/dev/leads/{id}
```

### Obter dados de permissões DELETE

```zsh
curl -H "Origin: http://localhost" \
-H "Access-Control-Request-Method: DELETE" \
-H "Access-Control-Request-Headers: X-Requested-With" \
-X OPTIONS --verbose \
https://se3l85r4x5.execute-api.us-east-2.amazonaws.com/dev/leads/{id}
```

# Corebiz AWS API

## Instalar serverless framework

```zsh
npm install -g serverless
```

MacOS/Linux

```zsh
sudo npm install -g serverless
```

## Verificar versão e instalação

```zsh
serverless
serverless -- version
```

## Configurar IAM credentials

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

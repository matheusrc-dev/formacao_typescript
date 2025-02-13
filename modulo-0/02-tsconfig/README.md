# Criando o primeiro projeto TypeScript
[TSConfig Reference - Docs on every TSConfig option](https://www.typescriptlang.org/tsconfig/)

Utilizando a versão 20.6.0 do NodeJS

Na pasta tsconfig executar o comando:

```bash
npm init -y
npm install -D typescript@5.2.2
npx tsc -init
```

Isso irá iniciar um projeto em typescript

O TypeScript não é executado nativamente, ou seja, não precisamos te-lo em produção, por isso instalamos ele como dependência de desenvolvimento.

Para executar o typescript executamos através do comando `tsc`, porém se tentarmos executar ele diretamente na linha de comando, ele vai falhar. O Typescript quando é instalado vai para a `node_modules/`. Porém ele também instala um binário chamado tsc (Typescript compiler). Ele fica em `node_modules/.bin/tsc` e pode ser executado no terminal dessa forma:

```bash
./node_modules/.bin/tsc --version
```

Output: ❯ Version 5.2.2

Porém para facilitar vamos utilizar uma ferramenta fornecida pelo próprio npm chamada de npx, o npx vai buscar no projeto se tenho o binário localmente instalado, caso contrário ele vai tentar buscar da web.

Por isso iniciamos o repositório com `npx tsc --init`.
Após isso, é criado um arquivo `tsconfig.json` que é a raiz do nosso projeto, é onde fica toda a configuração do typescript.

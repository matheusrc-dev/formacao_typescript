# Entendendo o TSConfig
Não é necessário ficar compilando arquivos direto pela linha de comando.

Para isso temos o tsconfig.

Ele é o arquivo de configuração do typescript.

Pode existir mais de um arquivo .tsconfig dentro de um projeto dependendo do objetivo.

Se cria uma vez e raramente será editado (sensible default).

Verificar o [guia de referência do TSConfig](https://www.typescriptlang.org/tsconfig/)

[Recomendações para a criação de bases de um TSConfig](https://github.com/tsconfig/bases?tab=readme-ov-file)

### Lista de opções do tsconfig.json
- **incremental** - Permite que a construção dos projetos de forma incremental, ele compila o projeto em partes. Compila apenas alguns arquivos e não todos. É bom para projetos grandes. Toda vez que você remover a pasta dist/ ele não vai assumir que a pasta dist está criada, é necessário cria-la novamente.
- **target** - define a versão do javascript que será emitida no build do projeto.
- **lib** - Permite a adição de bibliotecas, por exemplo algum arquivo que vai rodar no es3 (que é bem antigo).
- **rootDir** - É onde fica todo o nósso código, geralmente vamos utilizar a pasta "./src". Significa que o typescript Define que todos os arquivos que serão transpilados estarão dentro do diretório `rootDir`.
- **outDir** - É o diretório de saída, para onde os códigos transpilados vão.

Se a pasta dist for removida não será possível criar uma pasta /dist novamente, para isso acontecer é necessário remover o arquivo .tsbuildinfo que funciona como um cache para o projeto.

Para incluir um script de build basta adicionar no package.json:
```json
"scripts": {
  "build": "tsc"
}
```
Quando estamos trabalhando com typescript, ele não sabe em que ambiente precisamos executar a aplicação. Como estamos no node precisamos instalar a tipagem do node:
```
npm install -D @types/node
```

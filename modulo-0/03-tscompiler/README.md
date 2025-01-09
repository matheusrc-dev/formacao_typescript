# O TS Compiler
O **TSC** (TypeScript Compiler) é a ferramenta que compila código escrito em **TypeScript** para **JavaScript**.

Ele é configurado por meio de um arquivo chamado `tsconfig.json` nele, por exemplo, você pode configurar qual versão do JavaScript será gerada (ex.: ES5, ES6).

Ele realiza **type checking**, ou seja, verifica o código em tempo de desenvolvimento para identificar possíveis erros relacionados a tipos (como tentar somar uma string com um número). Isso ajuda a evitar erros em tempo de execução.

Ele pode funcionar como um **watcher**: recompila automaticamente o código sempre que detecta alterações nos arquivos.

O TSC não executa código, apenas o transpila. Para executar o código, é necessário um runtime JavaScript, como o Node.js.

Documentação do tsc CLI

[Documentation - tsc CLI Options](https://www.typescriptlang.org/docs/handbook/compiler-options.html)

`npx tsc --noEmit` Faz a checagem de tipos no arquivo .ts

`npx tsc —outDir dist` Compila os arquivos typescript e coloca-os em uma pasta dist

Adicionar ao package.json os scripts:

```json
"scripts": {
  "build": "tsc --outDir dist",
  "build:watch": "tsc --outDir dist --watch"
}
```

Assim quando o comando `npm run build:watch` for executado, o código será recompilado automaticamente.

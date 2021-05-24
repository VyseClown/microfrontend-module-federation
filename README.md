## Criando Micro-Front-Ends com Webpack5 Module Federation

Criar 3 micro-front-ends com compartilhamento de código de forma bidirecional,
a ideia é de no final da dessa aula ter um modelo de e-commerce bem simples onde teremos
a mesma experiência sendo criada e compartilhada entre os nossos MFE's, compartilhando código em tempo de execução sem perda de desempenho.

## Aplicação Final 🎬

<img src="./misc/Application.gif" />

Observe aqui que estamos navegando em diferentes servidores, mas a experiência final.

Instale as dependências do diretório principal do projeto:

|**⚠️ usaremos yarn para gerenciar nossos pacotes**

```sh
yarn install
```

em seguida, entre no diretório dos nossos MFE's

```sh
cd  shared-routing
```

Instale as dependencias

```sh
yarn install
```

Inicie o servidor de desenvolvimento:

```sh
yarn  start
```

Com isso, você terá os aplicativos em execução em:

- [localhost:3000](http://localhost:3000/) (aplicativo host) - `shell`
- [localhost:3001](http://localhost:3001/) (aplicativo autônomo remoto) - `ProductList`
- [localhost:3002](http://localhost:3002/) (aplicativo autônomo remoto) - `ProductDetails`

Abra uma dessas portas no navegador de sua escolha e você estará pronto para integrar com o aplicativo inicial 🚀.

## Estrutura do Projeto 🏗

Conforme descrito, criaremos uma estrutura MFE com hosts host bidirecionais
podemos ver aqui o gráfico de como nossos MFE's vão ser divididos

<img src="./misc/mfe.png" />

Na pasta `Container/shared-routing`, temos os nossos MFE's:

- `Shell`: **MFE** Onde vamos criar o nosso application shell
- `ProductList /`: **MFE** responsavel pela listagem de produtos
- `ProductDetails /`: **MFE** responsavel pelo detalhamento de produtos

```md
├── ProductDetails
│   ├── package.json
│   ├── public
│   ├── src
│   └── webpack.config.js
├── ProductList
│   ├── package.json
│   ├── public
│   ├── src
│   └── webpack.config.js
├── Shell
│   ├── package.json
│   ├── public
│   ├── src
│   └── webpack.config.js
├── package.json
└── yarn.lock
```

## Ferramentas Utilizadas 🧰

- [x] React como uma linguagem de IU
- [x] Webpack5 como module bundler
- [x] Prettier como formatador de código
- [x] Lerna para gerenciar o monorepo
- [x] TailwindCss UI como nosso kit de ferramentas de design

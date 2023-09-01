Vamos usar o Creat React App

    npx-react-app portfolio --template typescript

Acessar a pasta do projeto

    cd ,/portfolio

vamos instalar o editorconfig

O EditorConfig é um padrão de formatação de código que visa manter a consistência nas configurações de estilo de código em projetos de desenvolvimento. Ele fornece um arquivo de configuração chamado ".editorconfig" que pode ser incluído no repositório do projeto para definir regras de formatação específicas para diferentes tipos de arquivos.

A ideia por trás do EditorConfig é garantir que todos os membros de uma equipe de desenvolvimento usem as mesmas convenções de estilo, independentemente do editor de texto ou ambiente de desenvolvimento que estejam usando. Isso é particularmente útil quando equipes trabalham com diferentes ferramentas ou quando um projeto envolve múltiplas linguagens de programação.

No arquivo ".editorconfig", você pode definir regras para coisas como indentação, estilo de quebra de linha, caracteres de fim de arquivo (EOL), espaçamento e muito mais. Cada regra é associada a um ou mais padrões de arquivo, permitindo ajustar as configurações com base no tipo de arquivo. Por exemplo, você pode ter regras diferentes para arquivos JavaScript e arquivos CSS.


Criamos um arquivo .editorconfig

    dentro do arquivo

        root = true

        [*]
        indent_style = space
        indent_size = 2
        end_of_line = lf
        charset =utf-8 
        trim_trailing_whitespace = true 
        insert_final_inline = true

Instalamos o plug-in do editorconfig no vs code.

Vamos instalar o ESLint 

O ESLint é uma ferramenta de linting para JavaScript e TypeScript. O linting é um processo de análise estática de código para identificar problemas, padrões não conformes e possíveis erros em um código-fonte. O ESLint é usado principalmente para melhorar a qualidade do código, promovendo boas práticas de programação e evitando erros comuns.

Comando 

    npx eslint --init

Irá aparecer um aquivo que precisa ser configurado, para ele funcionar com react

    vamos alterar em:

    ,
    "extends": [
        "eslint:recommended",
        "plugin:react/recommended",
        "plugin:@typescript-eslint/recommended",
        "plugin:prettier/recommended"
    ],
    "plugins": [
        "react",
        "@typescript-eslint",
        "react-hooks"
    ],
    "rules": {
        "react-hooks/rules-of-hooks": "error",
        "react-hooks/"exhaustive-deps": "warn",
        "react/prop-types": "off",
        "react/react-in-jsx-scope": "off",
        "@typescript-eslint/explicit-modules-boundary-types": "off"
    }, 
    "settings": {
        "react": {
            "version": "detect"
        }
    }


Vamos instalar um plug-in ESLint 

    npm install --save-dev eslint-plugin-react-hooks

Fazemos a instalação do plug-in ESLint no VSCode.

Vamos instalar o Prettier

O Prettier é uma ferramenta de formatação de código que tem como objetivo principal padronizar automaticamente o estilo de código em projetos. Ao contrário de outras ferramentas de formatação ou linters que permitem personalizações extensas, o Prettier adota uma abordagem "opinião sobre formatação" muito rigorosa. Ele não apenas ajusta a indentação e a quebra de linhas, mas também reescreve o código por completo para seguir um conjunto específico de regras de formatação.

Para instalar 

    npn install --save-dev eslint-plugin-react-hooks

    npn install --save-dev eslint-plugin-prettier eslint-config-hooks

Criamos um novo arquivo

    .prettier

    configuramos 

    {
        "trailingComma": "nome",
        "semi": false,
        "singleQuote": true
    }

Criamos uma Pasta .vscode com um arquivo dentro chamado settings.json

    configuração do settings.json

    {
        "editor.formatOnSace": false,
        "editor.codeActionsOnSave": {
            "source.fixAll.eslint": true 
        }
    }

Damos o comando no terminal 

    npx eslint .

    npx prettier --write .\src\

Inicializamos o nosso projeto

    npm run start

No google instalar a extensão 

    React developers tools



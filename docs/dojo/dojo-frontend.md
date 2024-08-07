# Dojo de Next.js - Introdução

## Introdução

Este documento representa contéudo apresentado durante a elaboração do dojo de markdown feito pela equipe de EPS para os integrantes de MDS.

Reunião foi realizada no dia **22/06/2024**

## O que é Next.js?

Next.js é um framework de React que permite a criação de aplicações web rápidas e eficientes. Ele fornece funcionalidades como renderização do lado do servidor (SSR), geração estática de páginas (SSG), roteamento baseado em arquivos e muito mais, facilitando o desenvolvimento de aplicações web modernas.

## Pré-requisitos

- Node.js e npm instalados.
- Conhecimento básico de JavaScript/TypeScript e React.
- Editor de código (recomendado: VS Code).

## Passo 1: Configuração do Ambiente

1. **Criar um novo projeto Next.js**:
    ```bash
    npx create-next-app@latest my-blog
    ```

2. **Navegar até o diretório do projeto**:
    ```bash
    cd my-blog
    ```

3. **Iniciar o servidor de desenvolvimento**:
    ```bash
    npm run dev
    ```

    Abra o navegador e acesse `http://localhost:3000` para ver a página inicial do Next.js.

## Passo 2: Estrutura de Páginas

1. **Criar a página de Listagem de Posts** (`pages/index.js`):
    ```javascript
    import Link from 'next/link';

    const posts = [
      { id: 1, title: 'Meu Primeiro Post' },
      { id: 2, title: 'Aprendendo Next.js' },
      { id: 3, title: 'Dojo de Next.js' },
    ];

    export default function Home() {
      return (
        <div>
          <h1>Blog</h1>
          <ul>
            {posts.map(post => (
              <li key={post.id}>
                <Link href={`/posts/${post.id}`}>
                  <a>{post.title}</a>
                </Link>
              </li>
            ))}
          </ul>
        </div>
      );
    }
    ```

2. **Criar a página de Post** (`pages/posts/[id].js`):
    ```javascript
    import { useRouter } from 'next/router';

    const posts = [
      { id: 1, title: 'Meu Primeiro Post', content: 'Conteúdo do meu primeiro post.' },
      { id: 2, title: 'Aprendendo Next.js', content: 'Conteúdo sobre como aprender Next.js.' },
      { id: 3, title: 'Dojo de Next.js', content: 'Conteúdo do dojo de Next.js.' },
    ];

    export default function Post() {
      const router = useRouter();
      const { id } = router.query;
      const post = posts.find(post => post.id === parseInt(id));

      if (!post) {
        return <p>Post não encontrado.</p>;
      }

      return (
        <div>
          <h1>{post.title}</h1>
          <p>{post.content}</p>
        </div>
      );
    }
    ```

## Passo 3: Estilização

1. **Adicionar estilos globais** (`styles/globals.css`):
    ```css
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
    }

    ul {
      list-style: none;
      padding: 0;
    }

    li {
      margin: 10px 0;
    }

    a {
      text-decoration: none;
      color: blue;
    }

    a:hover {
      text-decoration: underline;
    }
    ```

2. **Importar o arquivo de estilos globais** (`pages/_app.js`):
    ```javascript
    import '../styles/globals.css';

    function MyApp({ Component, pageProps }) {
      return <Component {...pageProps} />;
    }

    export default MyApp;
    ```

## Passo 4: Navegação entre Páginas

1. **Adicionar um link de volta à página inicial** (`pages/posts/[id].js`):
    ```javascript
    import Link from 'next/link';
    import { useRouter } from 'next/router';

    const posts = [
      { id: 1, title: 'Meu Primeiro Post', content: 'Conteúdo do meu primeiro post.' },
      { id: 2, title: 'Aprendendo Next.js', content: 'Conteúdo sobre como aprender Next.js.' },
      { id: 3, title: 'Dojo de Next.js', content: 'Conteúdo do dojo de Next.js.' },
    ];

    export default function Post() {
      const router = useRouter();
      const { id } = router.query;
      const post = posts.find(post => post.id === parseInt(id));

      if (!post) {
        return <p>Post não encontrado.</p>;
      }

      return (
        <div>
          <h1>{post.title}</h1>
          <p>{post.content}</p>
          <Link href="/">
            <a>Voltar para a página inicial</a>
          </Link>
        </div>
      );
    }
    ```

## Passo 5: Testar a Aplicação

1. **Iniciar o servidor de desenvolvimento**:
    ```bash
    npm run dev
    ```

2. **Testar os endpoints**:
    - **Página inicial**: `http://localhost:3000/` - Lista todos os posts.
    - **Página do post**: `http://localhost:3000/posts/1` - Exibe o conteúdo do post com ID 1.

## Conclusão

Você criou uma aplicação básica de blog usando Next.js. A partir daqui, você pode expandir a aplicação adicionando funcionalidades como autenticação, persistência de dados, e muito mais.

## Recursos Adicionais

- [Documentação oficial do Next.js](https://nextjs.org/docs)
- [Repositório do GitHub do Next.js](https://github.com/vercel/next.js)

|**Data**|**Descrição**|**Autor(es)**|
|--------|-------------|--------------|
|07/08/2024| Criação do Documento | João Victor Max |
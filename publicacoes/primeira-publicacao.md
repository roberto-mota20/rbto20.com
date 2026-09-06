# Primeira Publicação

Esta é a primeira publicação de teste do site. O sistema agora lê e renderiza arquivos Markdown (.md) e MDX (.mdx) diretamente da pasta de publicações.

---

## Como adicionar novos textos

Para publicar um novo conteúdo, basta criar um arquivo com extensão `.md` ou `.mdx` dentro da pasta `publicacoes/`. O sistema reconhece o conteúdo, extrai o título e a descrição automaticamente a partir das primeiras linhas de texto.

### Exemplo de Código

Você pode incluir blocos de código com destaque e botão de cópia:

```javascript
// Exemplo de execução no Cloudflare Workers
export default {
  async fetch(request, env, ctx) {
    const url = new URL(request.url);
    if (url.pathname.startsWith('/publ')) {
      return new Response('Publicações ativas!', {
        headers: { 'content-type': 'text/plain; charset=utf-8' },
      });
    }
    return fetch(request);
  },
};
```

### Tabelas e Formatação

| Recurso | Suporte |
| :--- | :--- |
| **Renderização Markdown** | Nativa |
| **Indexação Automática** | Direta da pasta |
| **Extração de Resumo** | Primeiras linhas |
| **Blocos de Código** | Com botão de cópia |

> "A simplicidade é o último grau de sofisticação." — Leonardo da Vinci

Para retornar à listagem, utilize o botão **Voltar** no topo da página.

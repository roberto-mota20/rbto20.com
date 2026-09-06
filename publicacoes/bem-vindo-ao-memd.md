---
title: Bem-vindo ao memd
date: 2026-09-06
description: Apresentando o memd, o módulo de publicações em Markdown e MDX do rbto20.com.
tags: [memd, markdown, cloudflare, web]
author: Roberto Mota
---

# Bem-vindo ao memd

Este é o **memd**, um módulo minimalista para leitura e publicação de notas e artigos escritos em **Markdown** (`.md`) e **MDX** (`.mdx`).

---

## O que é o memd?

O **memd** foi construído para se integrar perfeitamente à estética do site, trazendo:

- ⚡ **Renderização rápida e sob demanda** no navegador.
- 🎨 **Estilo visual integrado**: paleta escura, fontes em *JetBrains Mono* e detalhes em verde-azulado (*teal*).
- 📱 **Totalmente responsivo** para qualquer tamanho de tela.
- 🔗 **Links diretos compartilháveis** para cada artigo.

> "A simplicidade é o último grau de sofisticação." — Leonardo da Vinci

---

## Exemplo de Código

Você pode incluir snippets de código formatados com facilidade:

```javascript
// Exemplo de função assíncrona no Cloudflare Workers
export default {
  async fetch(request, env, ctx) {
    const url = new URL(request.url);
    
    if (url.pathname.startsWith('/memd')) {
      return new Response('Módulo memd ativo!', {
        headers: { 'content-type': 'text/plain; charset=utf-8' },
      });
    }

    return fetch(request);
  },
};
```

Também há suporte para comandos em terminal:

```bash
# Como adicionar uma nova publicação:
# 1. Crie um arquivo .md ou .mdx na pasta publicacoes/
# 2. Registre-o no publicacoes/manifest.json (ou acesse diretamente pelo slug)
```

---

## Tabelas e Estruturas

| Recurso | Suporte | Descrição |
| :--- | :---: | :--- |
| **Markdown Padrão** | ✅ | Títulos, listas, ênfases, citações e links |
| **Código Formatado** | ✅ | Blocos de código com destaque e rolagem |
| **Frontmatter** | ✅ | Metadados como título, data e tags |
| **Deep Linking** | ✅ | URLs permanentes para cada artigo |

---

## Lista de Tarefas

- [x] Criar estrutura de publicações
- [x] Implementar renderizador dinâmico de Markdown
- [x] Adicionar suporte a metadados (Frontmatter)
- [x] Configurar roteamento com URLs amigáveis

Para voltar à listagem de publicações, basta usar o botão **Voltar** no topo da página.

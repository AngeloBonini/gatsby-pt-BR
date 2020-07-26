---
title: Auditoria com o Lighthouse
---

Citando o [site do Lighthouse](https://developers.google.com/web/tools/lighthouse/):

> O Lighthouse é uma ferramenta automatizada de código aberto para aprimorar a qualidade de páginas da web. O lighthouse pode ser executado em qualquer página pública ou que exija autenticação. Ele tem auditorias de performance, acessibilidade, progressive web apps (PWAs) e mais.

O Lighthouse é incluido por padrão no Chrome DevTools. Executar as auditorias dele, abordar os erros encontrados e então implementar as melhorias sugeridas é uma maneira excelente de preparar seu site para ir ao ar. Ele te ajuda a garantir que seu site seja o mais rápido e acessível possível.

Caso você não tenha ainda, você precisa criar pacote de produção do seu site Gatsby. O servidor de desenvolvimento do Gatsby é perfeito para agilizar o desenvolvimento, mas o site gerado, apesar de se assemelhar muito à versão de produção do site, não é otimizado.

## Crie um pacote de produção

1.  Pare o servidor de desenvolvimento (caso ainda esteja em execução) e então execute:

```shell
gatsby build
```

> 💡 Esse comando cria um pacote de produção do seu site e envia os arquivos estáticos criados para o diretório `public`.

2.  Sirva o pacote de produção localmente. Execute:

```shell
gatsby serve
```

Uma vez iniciado, você poderá visualizar seu site em `http://localhost:9000`.

## Execute o Lighthouse

Agora execute sua primeira auditoria Lighthouse.

1.  Se você ainda não abriu, abra o seu site e o Chrome DevTools (Cmd+Opt/Shift+I)

2.  Clique na aba "Lighthouse" e então você verá uma tela parecida com esta:

![Lighthouse audit start](./images/lighthouse-audit.png)

3.  Clique no botão "Generate report" para executar os testes (todas as auditorias disponíveis devem estar selecionados por padrão). Quando os testes estiverem concluídos, você verá resultados parecidos com estes:

![Lighthouse audit results](./images/lighthouse-audit-results.png)

Como poderão comprovar, o Gatsby proporciona por padrão uma performance excelente. Entretanto ainda falta algumas melhorias de acessibilidade, SEO, PWA e boas práticas que irão melhorar suas pontuações e consequentemente fazer seu site mais amigável aos visitantes e aos motores de busca. Para melhorar ainda mais suas pontuações, consulte os links em "Próximas etapas" abaixo:

Próximas etapas:

- [Adicionando o Arquivo de Manifesto](/docs/add-a-manifest-file/)
- [Adicionando o modo off-line](/docs/add-offline-support-with-a-service-worker/)
- [Adicionando metadados da página](/docs/add-page-metadata/)

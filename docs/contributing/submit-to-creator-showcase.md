---
title: Submeter ao Mostruário de Criadores
---

Quer fazer parte do [Mostruário de Criadores?](/creators)? Siga essas instruções.

## Passos

Há apenas dois passos :)

1.  Se esta é sua primeira contribuição para o repositório _open source_ do Gatsby, siga as [Orientações de Contribuição](/contributing/code-contributions/).

2.  Envie uma foto sua ou um logo da sua empresa/agência para [`esse diretório`](https://github.com/gatsbyjs/gatsby/tree/master/docs/creators/images). Imagens devem ter um aspecto quadrado de proporção com uma resolução mínima de 500px (ex: 500px X 500px) e máxima de 1000px. A imagem deve possuir o mesmo nome que você colocar no campo "nome" em creators.yml, substituindo espaços por hífens.

    Por exemplo,

    **se o nome é:** _Fabian Schultz_

    **o nome da imagem deve ser,** _fabian-schultz.jpg_

    **se o nome é:** _Iron Cove Solutions_

    **o nome da imagem deve ser,** _iron-cove-solutions.jpg_

3.  Edite o arquivo [`creators.yml`](https://github.com/gatsbyjs/gatsby/blob/master/docs/creators/creators.yml) adicionando sua submissão no fim da lista de sites no seguinte formato:

```yaml:title=docs/creators/creators.yml
- name: Your Name

  # Você pode escolher um dos 3 tipos `types`: agency, company, or individual
  type: agency
  description: >-
    We help agencies and companies with JAMStack tools. This includes web
    development using Static Site Generators, Headless CMS, CI / CD and CDN
    setup.
  location: Poland
  website: "https://yourname.io/"
  github: "https://github.com/githubusername"
  image: images/image.jpg

  # Agora, você pode escolher true apenas para `for_hire` ou para `hiring`, mas não para ambos.
  for_hire: true
  hiring: false

  # Se você marcar `portfolio: true`, qualquer site que você tem no Mostruário de Sites será mostrado com `built_by: [imagine seu nome aqui]` será relacionado ao seu Perfil de Criador. Então certifique-se de que o `name` em `creators.yml` é exatamente o mesmo de `built_by` em `sites.yml`.
  portfolio: true
```

Use o seguinte modelo para garantir que os campos obrigatórios estão preenchidos:

```yaml:title=docs/creators/creators.yml
- name: (required)
  type: (required - agency, company, or individual)
  image: (required - images/{filename}.{ext})
  description: >-
    (optional)
  location: (optional)
  website: (optional)
  github: (optional)
  for_hire: (optional)
  hiring: (optional)
  portfolio: (optional)
```

4. Se você enviou seus websites para o Mostruário antes mas não preencheu o campo "built_by", você deve editar o arquivo [`sites.yml`](https://github.com/gatsbyjs/gatsby/blob/master/docs/sites.yml) e adicionar seu nome (e o campo `built_by` se ele não estiver presente) para garantir que as peças do seu portifólio estejam ligadas à sua página.

### Processo de revisão

Por padrão, todas as edições enviadas ao Mostruário de Criadores serão revisadas pelos processos regulares de aprovação de _PR_ e de _merge_.

### Mudou de ideia / precisa editar sua submissão?

Se você precisar editar alguma coisa na sua submissão posteriormente, simplesmente edite o arquivo `creators.yml` submetendo outro PR.

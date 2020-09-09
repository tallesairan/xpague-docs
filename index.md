---
layout: default
title: Início
nav_order: 1
description: "XPague Postbacks."
permalink: /
last_modified_date: 2020-04-27T17:54:08+0000
---

# XPague Postbacks
{: .fs-9 }
Documentação para auxiliar na implementação de integrações que são alimentadas através de postbacks

{: .fs-6 .fw-300 }


---

## Começando


### Tipo do postback em objectType 
É possível identificar o tipo do postback no campo "objectType" ele pode conter os valores  'transaction' ou 'cart' sendo cart para recuperação de carrinho e transaction para transações.


### Schemas

Url das schemas:
[Cart](https://pagamento.xpague.com/core/postback-schema-cart.json), enviado no abandono.
[Transaction](https://pagamento.xpague.com/core/postback-schema-transaction.json) enviado em transações.


### Visualizando Schemas
Caso queira visualizar as schemas online, utilize alguma das ferramentas abaixo
[jsonschema]https://jsonschema.net ou
[jsonviewer] https://codebeautify.org/jsonviewer/c6a219 para ver a schema.
 é bem simples  basta copiar o conteúdo dela e colar para uma inspeção


### Delays 
o delay para a transação ser entregue é de 3 minutos após a ação, a recuperação de carrinho é enviada após 20 minutos


### Status 
Possíveis status
"pending", "approved", "rejected", "in_process", "charged_back" 

### Configurando Postbacks na plataforma
A XPague trabalha com postbacks por produto, então você vai cadastrar no seu produto.
Passos para ativar os postbacks no seu produto:
1. Acesse seu produto
2. Clique na aba Postbacks
3. Clique no Botão "Novo Postback", cole a url desejada e clique em salvar.
Pronto agora o sistema vai enviar postbacks para esse produto
Caso queira verificar os postbacks também é enviado um header chamado "xpaguetoken" com o token único.
<small>Você também pode testar suas webhooks, acesse  [Webhooks.site](https://webhook.site/)</small>



### Limites
Nosso sistema aguarda 600 ms de resposta do servidor destino, caso o envio falhe o sistema tenta mais duas vezes entregar a webhook


### Local installation: Use the gem-based theme

1. Install the Ruby Gem
```bash
$ gem install just-the-docs
```
```yaml
# .. or add it to your your Jekyll site’s Gemfile
gem "just-the-docs"
```
2. Add Just the Docs to your Jekyll site’s `_config.yml`
```yaml
theme: "just-the-docs"
```
3. _Optional:_ Initialize search data (creates `search-data.json`)
```bash
$ bundle exec just-the-docs rake search:init
```
3. Run you local Jekyll server
```bash
$ jekyll serve
```
```bash
# .. or if you're using a Gemfile (bundler)
$ bundle exec jekyll serve
```
4. Point your web browser to [http://localhost:4000](http://localhost:4000)

If you're hosting your site on GitHub Pages, [set up GitHub Pages and Jekyll locally](https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll) so that you can more easily work in your development environment.

### Configure Just the Docs

- [See configuration options]({{ site.baseurl }}{% link docs/configuration.md %})

---

## About the project

Just the Docs is &copy; 2017-{{ "now" | date: "%Y" }} by [Patrick Marsceill](http://patrickmarsceill.com).

### License

Just the Docs is distributed by an [MIT license](https://github.com/pmarsceill/just-the-docs/tree/master/LICENSE.txt).

### Contributing

When contributing to this repository, please first discuss the change you wish to make via issue,
email, or any other method with the owners of this repository before making a change. Read more about becoming a contributor in [our GitHub repo](https://github.com/pmarsceill/just-the-docs#contributing).

#### Thank you to the contributors of Just the Docs!

<ul class="list-style-none">
{% for contributor in site.github.contributors %}
  <li class="d-inline-block mr-1">
     <a href="{{ contributor.html_url }}"><img src="{{ contributor.avatar_url }}" width="32" height="32" alt="{{ contributor.login }}"/></a>
  </li>
{% endfor %}
</ul>

### Code of Conduct

Just the Docs is committed to fostering a welcoming community.

[View our Code of Conduct](https://github.com/pmarsceill/just-the-docs/tree/master/CODE_OF_CONDUCT.md) on our GitHub repository.

---
layout: default
title: Dev Docs
nav_order: 1
description: "XPague DevDocs."
permalink: /
last_modified_date: 2020-04-27T17:54:08+0000
---


# XPague Dev Docs
{: .fs-9 }
Referência de api para ajudar nas automações de integrações.

---

## XPague Postbacks
{: .fs-9 }
Documentação para auxiliar em integrações que usam nossos postbacks

{: .fs-6 .fw-300 }


---

#### Começando

Resumo da documentação para utilizar os Postbacks da plataforma

{: .no_toc  }

1. TOC
{:toc}


#### Tipo do Postback em objectType 
É possível identificar o tipo do postback no campo "objectType" ele pode conter os valores  'transaction' ou 'cart' sendo cart para recuperação de carrinho e transaction para transações.


#### Métodos de pagamento 
Possíveis valores
"credit", "billet" 


#### Status 
Possíveis status
"pending", "approved", "rejected", "in_process", "charged_back" 



#### Configurando Postbacks na plataforma

A XPague trabalha com postbacks por produto, então você vai cadastrar no seu produto.
Passos para ativar os postbacks no seu produto:
1. Acesse seu produto
2. Clique na aba Postbacks
3. Clique no Botão "Novo Postback", cole a url desejada e clique em salvar.


Pronto agora o sistema vai enviar postbacks para esse produto.
#### Verificando Postback:

Caso queira verificar os postbacks também é enviado um header chamado "xpaguetoken" com o token único.

#### Testando Postbacks
<small>Você também pode testar seus postbacks, acesse  [Webhooks.site](https://webhook.site/)</small>


###  Schemas

Url das schemas:
1. [Cart](https://pagamento.xpague.com/core/postback-schema-cart.json) enviado no abandono.
2. [Transaction](https://pagamento.xpague.com/core/postback-schema-transaction.json) enviado em transações.


### Visualizando Schemas
Caso queira visualizar as schemas online, utilize alguma das ferramentas abaixo para visualizar a schema
1. [jsonschema](https://jsonschema.net)
2. [jsonviewer](https://codebeautify.org/jsonviewer/c6a219)

é bem simples  basta copiar o conteúdo dela e colar para uma inspeção


### Delays 
o delay para a transação ser entregue é de 3 minutos após a ação, a recuperação de carrinho é enviada após 20 minutos

### Limites
Nosso sistema aguarda 600 ms de resposta do servidor destino, caso o envio falhe o sistema tenta mais duas vezes entregar a webhook

### Endereços IP
Nossas requisições são enviadas através do ip:
*** 68.183.158.198 ***
*** 14061 DIGITALOCEAN-ASN ***
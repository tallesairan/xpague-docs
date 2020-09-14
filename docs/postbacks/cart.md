---
layout: default
title: Abandono de carrinho
permalink: /postbacks/abandono
parent: Postbacks
nav_order: 4
---

# Typography
{: .no_toc }

## Table of contents
{: .no_toc }

1. TOC
{:toc}

---

## Abandono de carrinho



 Duas schemas responsáveis pela estrutura do abandono de carrinho

1. ### Customer Schema 

Dados do cliente, usados em transações e recuperação de carrinho


```txt
    #/properties/customer#/properties/customer
```

Cliente
 
 
 customer Examples

```json
{
  "doc": {
    "raw": "00000000000",
    "formatted": "000.000.000-00"
  },
  "phone": {
    "formatted": "(21) 00000-0000",
    "raw": "21000000000"
  },
  "address": {
    "complementary": "",
    "city": "Nilópolis",
    "country": "br",
    "state": "RJ",
    "address": "Estrada Mirandela",
    "neighborhood": "Centro",
    "zipcode": "26520332",
    "number": "700"
  },
  "docType": "cpf",
  "name": "María Aparecida Murce"
}
```

 Customer Properties

| Property              | Type     | Required | Nullable       | Defined by                                                                                                                                                           |
| :-------------------- | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name)         | `string` | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-customer-properties-name.md "\#/properties/customer/properties/name#/properties/customer/properties/name")          |
| [docType](#docType)   | `string` | Required | cannot be null | [XPague Recuperação de carrinho](cart.md "\#/properties/customer/properties/docType#/properties/customer/properties/docType") |
| [doc](#doc)           | `object` | Required | cannot be null | [XPague Recuperação de carrinho](cart.md "\#/properties/customer/properties/doc#/properties/customer/properties/doc")             |
| [phone](#phone)       | `object` | Required | cannot be null | [XPague Recuperação de carrinho](cart.md "\#/properties/customer/properties/phone#/properties/customer/properties/phone")       |
| [address](#address)   | `object` | Required | cannot be null | [XPague Recuperação de carrinho](cart.md "\#/properties/customer/properties/address#/properties/customer/properties/address") |
| Additional Properties | Any      | Optional | can be null    |                                                                                                                                                                      |

#### name

Nome


`name`

-   is required
-   Type: `string` ([Name](cart-properties-customer-properties-name.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-customer-properties-name.md "\#/properties/customer/properties/name#/properties/customer/properties/name")

name Type

`string` ([Name](cart-properties-customer-properties-name.md))

name Constraints

**minimum length**: the minimum number of characters for this string is: `0`

name Examples

```json
"María Teste Teste"
```

#### docType

.


`docType`

-   is required
-   Type: `string` ([Doctype](cart.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart.md "\#/properties/customer/properties/docType#/properties/customer/properties/docType")

docType Type

`string` ([Doctype](cart.md))

docType Constraints

**minimum length**: the minimum number of characters for this string is: `1`

docType Examples

```json
"cpf"
```

#### doc
CPF formatado e CPF sem máscara


`doc`

-   is required
-   Type: `object` ([Doc](cart.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart.md "\#/properties/customer/properties/doc#/properties/customer/properties/doc")

#### doc Type

`object` ([Doc](cart.md))

doc Constraints

**minimum number of properties**: the minimum number of properties for this object is: `0`

doc Default Value

The default value is:

```json
{}
```

doc Examples

```json
{
  "formatted": "000.000.000-00",
  "raw": "00000000000"
}
```

#### phone

.


`phone`

-   is required
-   Type: `object` ([Phone](cart.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart.md "\#/properties/customer/properties/phone#/properties/customer/properties/phone")

 phone Type

`object` ([Phone](cart.md))

 phone Constraints

**minimum number of properties**: the minimum number of properties for this object is: `0`

 phone Default Value

The default value is:

```json
{}
```

 phone Examples

```json
{
  "formatted": "(21) 00000-0000",
  "raw": "21000000000"
}
```

#### address

Objeto de endereço do cliente


`address`

-   is required
-   Type: `object` ([Address](cart.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart.md "\#/properties/customer/properties/address#/properties/customer/properties/address")

address Type

`object` ([Address](cart.md))

address Constraints

**minimum number of properties**: the minimum number of properties for this object is: `0`

address Default Value

The default value is:

```json
{}
```

address Examples

```json
{
  "complementary": "",
  "city": "Nilópolis",
  "country": "br",
  "state": "RJ",
  "address": "Estrada Mirandela",
  "neighborhood": "Centro",
  "zipcode": "26520332",
  "number": "700"
}
```

2. ### Product Schema


 ## Exemplo

Exemplo da schema do postback de abandono

```json

{
  "objectType": "cart",
  "id": "124016",
  "product": {
    "id": 185917,
    "checkoutId": "145694",
    "productName": "fb 1",
    "description": "fb 1",
    "productPrice": "189.00",
    "productShipping": 0,
    "productCover": "https://static.xpague.com/fb111x3.jpg",
    "productThumbnail": null,
    "productTotal": "189.00",
    "fillableUrl": "https://pagamento.xpague.com/id/185917?ct=124016", /// url de checkout com as informações preenchidas
    "productUrl": "https://pagamento.xpague.com/id/185917" // url do produto
  },
  "customer": {
    "name": "lorem ipsum dolor",
    "email": "loremips@gmail.com",
    "docType": "cpf",
    "doc": {
      "raw": "12345649728",
      "formatted": "123.456.497-28"
    },
    "phone": {
      "raw": "22988718452",
      "formatted": "(22) 98871-8452"
    },
    "address": {
      "address": "XXXX",
      "number": "651",
      "complementary": "XXXXX",
      "neighborhood": "XXXXXX",
      "zipcode": "23520560",
      "city": "Rio de Janeiro",
      "state": "RJ",
      "country": "br"
    },
    "token": "a232029d793fe70bd956155a347a5037"
  },
  "dateQueued": "2020-09-11 02:28:09",
  "dateCreated": "2020-09-11 02:05:23",
  "dateUpdated": "2020-09-11 02:05:23"
}
```
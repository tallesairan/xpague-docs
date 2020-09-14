---
layout: default
title: Postbacks
nav_order: 2
has_children: true
permalink: /postbacks
---

# Postbacks

Nossos Postbacks foram criados para ajudar desenvolvedores, produtores e empresas a consumir de nossos serviços e automatizar seus sistemas
{: .fs-6 .fw-300 }

## Começando

Resumo da documentação para utilizar os Postbacks da plataforma

{: .no_toc  }

1. TOC
{:toc}


o primeiro passo e entender como é a estrutura dos postbacks
no nossos postbacks contamos com a seguinte estrutura:


1. ## Customer Schema 

```txt
    #/properties/customer#/properties/customer
```

Cliente


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                           |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [cart.schema.json\*](cart.md "open original schema") |

#### customer Type

`object` ([Customer](cart.md))

 customer Constraints

**minimum number of properties**: the minimum number of properties for this object is: `0`

 customer Default Value

The default value is:

```json
{}
```

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

**minimum length**: the minimum number of characters for this string is: `0`

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

2. ## Product Schema

```txt
#/properties/product#/properties/product
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                           |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [cart.schema.json\*](../out/cart.schema.json "open original schema") |

#### product Type

`object` ([Objeto do produto])

product Default Value

The default value is:

```json
{}
```

product Examples

```json
{
  "productShipping": "0",
  "productCover": "https://assets.xpague.com/fffff.png",
  "productTotal": "349.00",
  "fillableUrl": "https://pagamento.xpague.com/id/?src=postback&ct=36",
  "productPrice": "349.00",
  "id": 145720,
  "checkoutId":99188,
  "productName": "FB 5",
  "description": "lorem ipsum",
  "productThumbnail": "https://assets.xpague.com/fffff.png"
}
```

#### Objeto do produto Properties

| Property                              | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                 |
| :------------------------------------ | --------- | -------- | -------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [id](#id)                             | `integer` | Required | cannot be null | [XPague Recuperação de carrinho](transaction.md "\#/properties/product/properties/id#/properties/product/properties/id")                                    |
| checkoutId(#checkoutId) | Código do checkout | Required | cannot be null             |
| [productName](#productName)           | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-nome-do-produto.md "\#/properties/product/properties/productName#/properties/product/properties/productName")                |
| [description](#description)           | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-descrição-do-produto.md "\#/properties/product/properties/description#/properties/product/properties/description")           |
| [productPrice](#productPrice)         | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-preço-do-produto.md "\#/properties/product/properties/productPrice#/properties/product/properties/productPrice")             |
| [productShipping](#productShipping)   | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-preço-do-frete.md "\#/properties/product/properties/productShipping#/properties/product/properties/productShipping")         |
| [productCover](#productCover)         | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-imagem-de-capa.md "\#/properties/product/properties/productCover#/properties/product/properties/productCover")               |
| [productThumbnail](#productThumbnail) | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-thumbnail-do-produto.md "\#/properties/product/properties/productThumbnail#/properties/product/properties/productThumbnail") |
| [productTotal](#productTotal)         | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-total-do-produto-com-frete.md "\#/properties/product/properties/productTotal#/properties/product/properties/productTotal")   |
| [fillableUrl](#fillableUrl)           | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](transaction.md "\#/properties/product/properties/fillableUrl#/properties/product/properties/fillableUrl")         |

#### id

ID do produto.


`id`

-   is required
-   Type: `integer` ([The Id Schema](transaction.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](transaction.md "\#/properties/product/properties/id#/properties/product/properties/id")

id Type

`integer` ([The Id Schema](transaction.md))

id Examples

```json
145720
```

### productName

Nome do produto.


`productName`

-   is required
-   Type: `string` ([Nome do produto](cart-properties-objeto-do-produto-properties-nome-do-produto.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-nome-do-produto.md "\#/properties/product/properties/productName#/properties/product/properties/productName")

### productName Type

`string` ([Nome do produto](cart-properties-objeto-do-produto-properties-nome-do-produto.md))

### productName Examples

```json
"Femme Busto Kit 5"
```

#### description

Descrição do produto


`description`

-   is required
-   Type: `string` ([Descrição do produto](cart-properties-objeto-do-produto-properties-descrição-do-produto.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-descrição-do-produto.md "\#/properties/product/properties/description#/properties/product/properties/description")

description Type

`string` ([Descrição do produto](cart-properties-objeto-do-produto-properties-descrição-do-produto.md))

description Examples

```json
"Creme para limpeza facial"
```

#### productPrice

Preço do produto.


`productPrice`

-   is required
-   Type: `string` ([Preço do produto](cart-properties-objeto-do-produto-properties-preço-do-produto.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-preço-do-produto.md "\#/properties/product/properties/productPrice#/properties/product/properties/productPrice")

productPrice Type

`string` ([Preço do produto](cart-properties-objeto-do-produto-properties-preço-do-produto.md))

productPrice Examples

```json
"349.00"
```

#### productShipping

Preço do frete


`productShipping`

-   is required
-   Type: `string` ([Preço do frete](cart-properties-objeto-do-produto-properties-preço-do-frete.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-preço-do-frete.md "\#/properties/product/properties/productShipping#/properties/product/properties/productShipping")

productShipping Type

`string` ([Preço do frete](cart-properties-objeto-do-produto-properties-preço-do-frete.md))

productShipping Examples

```json
"0"
```

#### productCover




`productCover`

-   is required
-   Type: `string` ([Imagem de capa](cart-properties-objeto-do-produto-properties-imagem-de-capa.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-imagem-de-capa.md "\#/properties/product/properties/productCover#/properties/product/properties/productCover")

productCover Type

`string` ([Imagem de capa](cart-properties-objeto-do-produto-properties-imagem-de-capa.md))

productCover Examples

```json
" https://painel.xpague.com/app/uploads/2020/01/FemmeGeFl.png"
```

#### productThumbnail




`productThumbnail`

-   is required
-   Type: `string` ([Thumbnail do produto](cart-properties-objeto-do-produto-properties-thumbnail-do-produto.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-thumbnail-do-produto.md "\#/properties/product/properties/productThumbnail#/properties/product/properties/productThumbnail")

productThumbnail Type

`string` ([Thumbnail do produto](cart-properties-objeto-do-produto-properties-thumbnail-do-produto.md))

productThumbnail Examples

```json
" https://painel.xpague.com/app/uploads/2020/01/FemmeGeFl.png"
```

#### productTotal

`productTotal`

-   is required
-   Type: `string` ([Total do produto com frete](cart-properties-objeto-do-produto-properties-total-do-produto-com-frete.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-total-do-produto-com-frete.md "\#/properties/product/properties/productTotal#/properties/product/properties/productTotal")

ProductTotal Type

`string` ([Total do produto com frete](cart-properties-objeto-do-produto-properties-total-do-produto-com-frete.md))

 productTotal Examples

```json
"349.00"
```

#### fillableUrl




`fillableUrl`

-   is required
-   Type: `string` ([The Fillableurl Schema](transaction.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](transaction.md "\#/properties/product/properties/fillableUrl#/properties/product/properties/fillableUrl")

fillableUrl Type

`string` ([The Fillableurl Schema](transaction.md))

fillableUrl Examples

```json
"https://pagamento.xpague.com/id/?src=postback&ct=36"
```

3. ## Product Schema

Objeto do produto



```txt
#/properties/product#/properties/product
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                           |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [cart.schema.json\*](../out/cart.schema.json "open original schema") |

#### product Type

`object` ([Objeto do produto])

product Default Value

The default value is:

```json
{}
```

product Examples

```json
{
  "productShipping": "0",
  "productCover": "https://painel.xpague.com/app/uploads/2019/11/facereverse.png",
  "productTotal": "349.00",
  "fillableUrl": "https://pagamento.xpague.com/id/?src=postback&ct=36",
  "productPrice": "349.00",
  "id": 145720,
  "checkoutId":99188,
  "productName": "Femme Busto Kit 5",
  "description": "Creme para limpeza facial",
  "productThumbnail": "https://painel.xpague.com/app/uploads/2020/01/FemmeGel.png"
}
```

Properties

| Property                              | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                 |
| :------------------------------------ | --------- | -------- | -------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [id](#id)                             | `integer` | Required | cannot be null | [XPague Recuperação de carrinho](transaction.md "\#/properties/product/properties/id#/properties/product/properties/id")                                    |
| checkoutId(#checkoutId) | Código do checkout | Required | cannot be null             |
| [productName](#productName)           | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-nome-do-produto.md "\#/properties/product/properties/productName#/properties/product/properties/productName")                |
| [description](#description)           | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-descrição-do-produto.md "\#/properties/product/properties/description#/properties/product/properties/description")           |
| [productPrice](#productPrice)         | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-preço-do-produto.md "\#/properties/product/properties/productPrice#/properties/product/properties/productPrice")             |
| [productShipping](#productShipping)   | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart.md "\#/properties/product/properties/productShipping#/properties/product/properties/productShipping")         |
| [productCover](#productCover)         | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](transaction.md "\#/properties/product/properties/productCover#/properties/product/properties/productCover")               |
| [productThumbnail](#productThumbnail) | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart.md "\#/properties/product/properties/productThumbnail#/properties/product/properties/productThumbnail") |
| [productTotal](#productTotal)         | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart.md "\#/properties/product/properties/productTotal#/properties/product/properties/productTotal")   |
| [fillableUrl](#fillableUrl)           | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart.md "\#/properties/product/properties/fillableUrl#/properties/product/properties/fillableUrl")         |

#### id

ID do produto.


`id`

-   is required
-   Type: `integer` ([The Id Schema](transaction.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](transaction.md "\#/properties/product/properties/id#/properties/product/properties/id")

Type

`integer` ([The Id Schema](transaction.md))

Examples

```json
145720
```

#### productName

Nome do produto.


`productName`

-   is required
-   Type: `string` ([Nome do produto](cart-properties-objeto-do-produto-properties-nome-do-produto.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-nome-do-produto.md "\#/properties/product/properties/productName#/properties/product/properties/productName")

productName Type

`string` ([Nome do produto](cart-properties-objeto-do-produto-properties-nome-do-produto.md))

productName Examples

```json
"Femme Busto Kit 5"
```

#### description

Descrição do produto


`description`

-   is required
-   Type: `string` ([Descrição do produto](cart-properties-objeto-do-produto-properties-descrição-do-produto.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-descrição-do-produto.md "\#/properties/product/properties/description#/properties/product/properties/description")

description Type

`string` ([Descrição do produto](cart-properties-objeto-do-produto-properties-descrição-do-produto.md))

description Examples

```json
"Creme para limpeza facial"
```

#### productPrice

Preço do produto.


`productPrice`

-   is required
-   Type: `string` ([Preço do produto](cart-properties-objeto-do-produto-properties-preço-do-produto.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-preço-do-produto.md "\#/properties/product/properties/productPrice#/properties/product/properties/productPrice")

productPrice Type

`string` ([Preço do produto](cart-properties-objeto-do-produto-properties-preço-do-produto.md))

productPrice Examples

```json
"349.00"
```

#### productShipping

Preço do frete


`productShipping`

-   is required
-   Type: `string` ([Preço do frete](cart.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart.md "\#/properties/product/properties/productShipping#/properties/product/properties/productShipping")

productShipping Type

`string` ([Preço do frete](cart.md))

productShipping Examples

```json
"0"
```

#### productCover




`productCover`

-   is required
-   Type: `string` ([Imagem de capa](transaction.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](transaction.md "\#/properties/product/properties/productCover#/properties/product/properties/productCover")

productCover Type

`string` ([Imagem de capa](transaction.md))

productCover Examples

```json
"https://assets.xpague.com/uuuj11j1jx.png"
```

#### productThumbnail




`productThumbnail`

-   is required
-   Type: `string` ([Thumbnail do produto](cart.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart.md "\#/properties/product/properties/productThumbnail#/properties/product/properties/productThumbnail")

productThumbnail Type

`string` ([Thumbnail do produto](cart.md))

productThumbnail Examples

```json
"https://assets.xpague.com/uuuj11j1jx.png"
```

#### productTotal




`productTotal`

-   is required
-   Type: `string` ([Total do produto com frete](cart.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart.md "\#/properties/product/properties/productTotal#/properties/product/properties/productTotal")

#### productTotal Type

`string` ([Total do produto com frete](cart.md))

#### productTotal Examples

```json
"349.00"
```

#### fillableUrl




`fillableUrl`

-   is required
-   Type: `string` ([The Fillableurl Schema](cart.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart.md "\#/properties/product/properties/fillableUrl#/properties/product/properties/fillableUrl")

fillableUrl Type

`string` ([The Fillableurl Schema](cart.md))
fillableUrl Examples

```json
"https://pagamento.xpague.com/id/?src=postback&ct=36"
```
por enquanto é só.

2. ### Transaction

Transação Schema

```txt
#/properties/transaction#/properties/transaction
```

Tudo relacionado a transação está contido aqui

 

#### transaction Examples

```json
{
  "objectType": "transaction",
  "transaction": {
    "id": "2278715",
    "status": "pending",
    "statusDesc": "Pendente",
    "orderType": "normal",
    "paymentMethod": "billet",
    "transactionId": "111333333",
    "authorizationCode": "111333333",
    "token": "qvdh7o4h74brcvtc4l2kgtof6q",
    "items": [
      {
        "id": 185917, // id produto
        "checkoutId": 145694, // id checkout
        "productName": "FB1",
        "description": "Descrição produto.",
        "productPrice": "189.00",
        "productShipping": 0,
        "productCover": "https://static.xpague.com/qvdh7o4h74brcvtc4l2kgtof6qfb.jpg",
        "productThumbnail": "https://static.xpague.com/qvdh7o4h74brcvtc4l2kgtof6qfb.jpg",
        "quantity": 1,
        "paymentMethods": [
          "credit",
          "billet"
        ],
        "url": "https://pagamento.xpague.com/id/185917?src=postback"
      }
    ],
    "total": "189.00",
    "thanksPage": "https://pagamento.xpague.com/b/678715", // pagina obrigado
    "fillableUrl": "https://pagamento.xpague.com/id/185917?fill=678715", // pagina do checkout com informações preenchidas
    "dateCreated": "2020-08-11 13:01:03",
    "dateUpdated": "2020-09-10 13:06:18",
    "billet": "https://pagamento.xpague.com/b/678715?em=1", // boleto html
    "billetPdf": "https://pagamento.xpague.com/b/678715?pd=1", // boleto pdf
    "barcode": "23793.38029 60834.110821 53006.333305 7 83470000018900", // linha digitável
    "barcodeRaw": "23793380296083411082153006333305783470000018900",
    "billetExpire": "2020-08-14 13:01:03" // expiração boleto
  },
  "customer": {
    "name": "lorem ipsum dolor",
    "email": "loremlps@gmail.com",
    "docType": "cpf",
    "doc": {
      "raw": "2213021211",
      "formatted": "22.130.212-11"
    },
    "phone": {
      "raw": "2211230640",
      "formatted": "(22) 1222-0640"
    },
    "address": {
      "address": "Av 25 de março ",
      "number": "2211",
      "complementary": "922211",
      "neighborhood": "Centro",
      "zipcode": "11111111",
      "city": "São Paulo",
      "state": "SP",
      "country": "br"
    },
    "token": "qvdh7o4h74brcvtc4l2kgtof6q" 
  }
}
```

#### Objeto da transação Properties

| Property                                | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                  |
| :-------------------------------------- | -------- | -------- | -------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [id](#id)                               | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/id#/properties/transaction/properties/id")                                              |
| [status](#status)                       | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/status#/properties/transaction/properties/status")                                  |
| [statusDesc](#statusDesc)               | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/statusDesc#/properties/transaction/properties/statusDesc")                      |
| [orderType](#orderType)                 | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/orderType#/properties/transaction/properties/orderType")                         |
| [paymentMethod](#paymentMethod)         | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/paymentMethod#/properties/transaction/properties/paymentMethod")             |
| [transactionId](#transactionId)         | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/transactionId#/properties/transaction/properties/transactionId")             |
| [authorizationCode](#authorizationCode) | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/authorizationCode#/properties/transaction/properties/authorizationCode") |
| [token](#token)                         | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/token#/properties/transaction/properties/token")                                     |
| [items](#items)                         | `array`  | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/items#/properties/transaction/properties/items")                                     |
| [total](#total)                         | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/total#/properties/transaction/properties/total")                                     |
| [thanksPage](#thanksPage)               | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/thanksPage#/properties/transaction/properties/thanksPage")                      |
| [fillableUrl](#fillableUrl)             | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/fillableUrl#/properties/transaction/properties/fillableUrl")                   |
| [dateCreated](#dateCreated)             | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/dateCreated#/properties/transaction/properties/dateCreated")                   |
| [dateUpdated](#dateUpdated)             | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/dateUpdated#/properties/transaction/properties/dateUpdated")                   |
| [billet](#billet)                       | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/billet#/properties/transaction/properties/billet")                                  |
| [billetPdf](#billetPdf)                 | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/billetPdf#/properties/transaction/properties/billetPdf")                         |
| [barcode](#barcode)                     | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/barcode#/properties/transaction/properties/barcode")                               |
| [barcodeRaw](#barcodeRaw)               | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/barcodeRaw#/properties/transaction/properties/barcodeRaw")                      |
| [billetExpire](#billetExpire)           | `string` | Required | cannot be null | [XPague postback](transaction.md "\#/properties/transaction/properties/billetExpire#/properties/transaction/properties/billetExpire")                |
| Additional Properties                   | Any      | Optional | can be null    |                                                                                                                                                                                                             |

#### id

id do pedido


`id`

 

#### status

Status da transação


`status`

-   is required
-   Type: `string` ([Status](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/status#/properties/transaction/properties/status")

 

Status Examples

```json
"pending"
```

```json
"approved"
```

```json
"rejected"
```

```json
"cancelled" // um mês após a expiração
```

```json
"in_process"
```

#### statusDesc

Descrição do status


`statusDesc`

-   is required
-   Type: `string` ([Statusdesc](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/statusDesc#/properties/transaction/properties/statusDesc")

statusDesc Type

`string` ([Statusdesc](transaction.md))

statusDesc Constraints

**minimum length**: the minimum number of characters for this string is: `0`

statusDesc Examples

```json
"Data de vencimento do cartão incorreta"
```

```json
"Número do cartão incorreto"
```

#### orderType

Tipo do pedido.


`orderType`

-   is required
-   Type: `string` ([Ordertype](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/orderType#/properties/transaction/properties/orderType")

orderType Type

`string` ([Ordertype](transaction.md))

orderType Constraints

**minimum length**: the minimum number of characters for this string is: `0`

orderType Default Value

The default value is:

```json
"normal"
```

orderType Examples

```json
"normal" 
```

```json
"upsell" // upsell
```

```json
"callsell" /// televendas
```

#### paymentMethod

Método de pagamento


`paymentMethod`

-   is required
-   Type: `string` ([Paymentmethod](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/paymentMethod#/properties/transaction/properties/paymentMethod")

paymentMethod Type

`string` ([Paymentmethod](transaction.md))

paymentMethod Constraints

**minimum length**: the minimum number of characters for this string is: `0`

paymentMethod Examples

```json
"billet"
```

```json
"creidt"
```

#### transactionId

Número da transação, apartir do processador de pagamentos


`transactionId`

-   is required
-   Type: `string` ([Transactionid](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/transactionId#/properties/transaction/properties/transactionId")

transactionId Type

`string` ([Transactionid](transaction.md))

transactionId Constraints

**minimum length**: the minimum number of characters for this string is: `0`

transactionId Examples

```json
"173575628"
```

#### authorizationCode

Código de autorizaçao, apartir do processador de pagamentos


`authorizationCode`

-   is required
-   Type: `string` ([Authorizationcode](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/authorizationCode#/properties/transaction/properties/authorizationCode")

authorizationCode Type

`string` ([Authorizationcode](transaction.md))

authorizationCode Constraints

**minimum length**: the minimum number of characters for this string is: `0`

authorizationCode Examples

```json
"173575628"
```

#### token

Token de sessão do cliente


`token`

-   is required
-   Type: `string` ([Token](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/token#/properties/transaction/properties/token")

token Type

`string` ([Token](transaction.md))

token Constraints

**minimum length**: the minimum number of characters for this string is: `0`

token Examples

```json
"cd033ef874716ba5a7c57cbab5f95029"
```

#### items

produtos no pedido


`items`

-   is required
-   Type: `object[]` ([Items](transaction-items.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/items#/properties/transaction/properties/items")

items Type

`object[]` ([Items](transaction-items.md))

items Constraints

**minimum number of items**: the minimum number of items for this array is: `0`

items Default Value

The default value is:

```json
[]
```

#### total

Total do pedido


`total`

-   is required
-   Type: `string` ([Total](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/total#/properties/transaction/properties/total")

total Type

`string` ([Total](transaction.md))

total Constraints

**minimum length**: the minimum number of characters for this string is: `0`

total Examples

```json
"149.00"
```

#### thanksPage

Página de obrigado


`thanksPage`

-   is required
-   Type: `string` ([Thankspage](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/thanksPage#/properties/transaction/properties/thanksPage")

thanksPage Type

`string` ([Thankspage](transaction.md))

thanksPage Constraints

**minimum length**: the minimum number of characters for this string is: `0`

thanksPage Examples

```json
"https://pagamento.xpague.com/b/208180"
```

#### fillableUrl

Página do checkout com as informações preenchidas


`fillableUrl`

-   is required
-   Type: `string` ([Fillableurl](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/fillableUrl#/properties/transaction/properties/fillableUrl")

fillableUrl Type

`string` ([Fillableurl](transaction.md))

fillableUrl Constraints

**minimum length**: the minimum number of characters for this string is: `0`

fillableUrl Examples

```json
"https://pagamento.xpague.com/id/185917?src=postback&fill=208180"
```

#### dateCreated

Data de criação do pedido


`dateCreated`

-   is required
-   Type: `string` ([Datecreated](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/dateCreated#/properties/transaction/properties/dateCreated")

dateCreated Type

`string` ([Datecreated](transaction.md))

dateCreated Constraints

**minimum length**: the minimum number of characters for this string is: `0`

dateCreated Examples

```json
"2020-03-20 11:19:26"
```

#### dateUpdated

Data de atualização do pedido


`dateUpdated`

-   is required
-   Type: `string` ([Dateupdated](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/dateUpdated#/properties/transaction/properties/dateUpdated")

dateUpdated Type

`string` ([Dateupdated](transaction.md))

dateUpdated Constraints

**minimum length**: the minimum number of characters for this string is: `0`

dateUpdated Examples

```json
"2020-03-20 14:19:27"
```

#### billet

Url do boleto em html


`billet`

-   is required
-   Type: `string` ([Billet](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/billet#/properties/transaction/properties/billet")

billet Type

`string` ([Billet](transaction.md))

billet Constraints

**minimum length**: the minimum number of characters for this string is: `0`

billet Examples

```json
"https://pagamento.xpague.com/b/208180?em=1"
```

#### billetPdf

URL do boleto em pdf


`billetPdf`

-   is required
-   Type: `string` ([Billetpdf](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/billetPdf#/properties/transaction/properties/billetPdf")

billetPdf Type

`string` ([Billetpdf](transaction.md))

billetPdf Constraints

**minimum length**: the minimum number of characters for this string is: `0`

billetPdf Examples

```json
"https://pagamento.xpague.com/b/208180?pd=1"
```

#### barcode

Código de barras com máscara


`barcode`

-   is required
-   Type: `string` ([Barcode](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/barcode#/properties/transaction/properties/barcode")

barcode Type

`string` ([Barcode](transaction.md))

barcode Constraints

**minimum length**: the minimum number of characters for this string is: `0`

barcode Examples

```json
"23791.22928 60004.715383 92000.046901 4 82030000014900"
```

#### barcodeRaw

Código de barras sem máscara


`barcodeRaw`

-   is required
-   Type: `string` ([Barcoderaw](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/barcodeRaw#/properties/transaction/properties/barcodeRaw")

barcodeRaw Type

`string` ([Barcoderaw](transaction.md))

barcodeRaw Constraints

**minimum length**: the minimum number of characters for this string is: `0`

barcodeRaw Examples

```json
"23791229286000471538392000046901482030000014900"
```

#### billetExpire

Expiração do boleto


`billetExpire`

-   is required
-   Type: `string` ([Billetexpire](transaction.md))
-   cannot be null
-   defined in: [XPague postback](transaction.md "\#/properties/transaction/properties/billetExpire#/properties/transaction/properties/billetExpire")

billetExpire Type

`string` ([Billetexpire](transaction.md))

billetExpire Constraints

**minimum length**: the minimum number of characters for this string is: `0`

billetExpire Examples

```json
"2020-03-23 03:00:00"
```

### qualquer dúvida abra um ticket na plataforma

[XPague Suporte](https://painel.xpague.com/suporte/tickets/#!cnr)
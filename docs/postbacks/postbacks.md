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

{: .no_toc .text-delta }

1. TOC
{:toc}


o primeiro passo e entender como é a estrutura dos postbacks
no nossos postbacks contamos com a seguinte estrutura:


1. ### Customer Schema 

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


2. ### Product Schema

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
  "checkoutId"=>99188,
  "productName": "Femme Busto Kit 5",
  "description": "Creme para limpeza facial",
  "productThumbnail": "https://painel.xpague.com/app/uploads/2020/01/FemmeGel.png"
}
```

Properties

| Property                              | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                 |
| :------------------------------------ | --------- | -------- | -------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [id](#id)                             | `integer` | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-the-id-schema.md "\#/properties/product/properties/id#/properties/product/properties/id")                                    |
| checkoutId(#checkoutId) | Código do checkout | Required | cannot be null             |
| [productName](#productName)           | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-nome-do-produto.md "\#/properties/product/properties/productName#/properties/product/properties/productName")                |
| [description](#description)           | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-descrição-do-produto.md "\#/properties/product/properties/description#/properties/product/properties/description")           |
| [productPrice](#productPrice)         | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-preço-do-produto.md "\#/properties/product/properties/productPrice#/properties/product/properties/productPrice")             |
| [productShipping](#productShipping)   | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-preço-do-frete.md "\#/properties/product/properties/productShipping#/properties/product/properties/productShipping")         |
| [productCover](#productCover)         | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-imagem-de-capa.md "\#/properties/product/properties/productCover#/properties/product/properties/productCover")               |
| [productThumbnail](#productThumbnail) | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-thumbnail-do-produto.md "\#/properties/product/properties/productThumbnail#/properties/product/properties/productThumbnail") |
| [productTotal](#productTotal)         | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-total-do-produto-com-frete.md "\#/properties/product/properties/productTotal#/properties/product/properties/productTotal")   |
| [fillableUrl](#fillableUrl)           | `string`  | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-the-fillableurl-schema.md "\#/properties/product/properties/fillableUrl#/properties/product/properties/fillableUrl")         |

#### id

ID do produto.


`id`

-   is required
-   Type: `integer` ([The Id Schema](cart-properties-objeto-do-produto-properties-the-id-schema.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-the-id-schema.md "\#/properties/product/properties/id#/properties/product/properties/id")

Type

`integer` ([The Id Schema](cart-properties-objeto-do-produto-properties-the-id-schema.md))

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

### productTotal Type

`string` ([Total do produto com frete](cart-properties-objeto-do-produto-properties-total-do-produto-com-frete.md))

### productTotal Examples

```json
"349.00"
```

## fillableUrl




`fillableUrl`

-   is required
-   Type: `string` ([The Fillableurl Schema](cart-properties-objeto-do-produto-properties-the-fillableurl-schema.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-objeto-do-produto-properties-the-fillableurl-schema.md "\#/properties/product/properties/fillableUrl#/properties/product/properties/fillableUrl")

fillableUrl Type

`string` ([The Fillableurl Schema](cart-properties-objeto-do-produto-properties-the-fillableurl-schema.md))
fillableUrl Examples

```json
"https://pagamento.xpague.com/id/?src=postback&ct=36"
```

3. ### Transaction
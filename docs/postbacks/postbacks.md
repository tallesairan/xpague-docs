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

o primeiro passo e entender como é a estrutura dos postbacks
no nossos postbacks contamos com a seguinte estrutura:


1. ### Customer Schema 

```txt
    #/properties/customer#/properties/customer
```

Cliente


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                           |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [cart.schema.json\*](../out/cart.schema.json "open original schema") |

#### customer Type

`object` ([Customer](cart-properties-customer.md))

#### customer Constraints

**minimum number of properties**: the minimum number of properties for this object is: `0`

#### customer Default Value

The default value is:

```json
{}
```

#### customer Examples

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

### Customer Properties

| Property              | Type     | Required | Nullable       | Defined by                                                                                                                                                           |
| :-------------------- | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name)         | `string` | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-customer-properties-name.md "\#/properties/customer/properties/name#/properties/customer/properties/name")          |
| [docType](#docType)   | `string` | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-customer-properties-doctype.md "\#/properties/customer/properties/docType#/properties/customer/properties/docType") |
| [doc](#doc)           | `object` | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-customer-properties-doc.md "\#/properties/customer/properties/doc#/properties/customer/properties/doc")             |
| [phone](#phone)       | `object` | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-customer-properties-phone.md "\#/properties/customer/properties/phone#/properties/customer/properties/phone")       |
| [address](#address)   | `object` | Required | cannot be null | [XPague Recuperação de carrinho](cart-properties-customer-properties-address.md "\#/properties/customer/properties/address#/properties/customer/properties/address") |
| Additional Properties | Any      | Optional | can be null    |                                                                                                                                                                      |

### name

Nome


`name`

-   is required
-   Type: `string` ([Name](cart-properties-customer-properties-name.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-customer-properties-name.md "\#/properties/customer/properties/name#/properties/customer/properties/name")

#### name Type

`string` ([Name](cart-properties-customer-properties-name.md))

#### name Constraints

**minimum length**: the minimum number of characters for this string is: `0`

#### name Examples

```json
"María Teste Teste"
```

### docType

.


`docType`

-   is required
-   Type: `string` ([Doctype](cart-properties-customer-properties-doctype.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-customer-properties-doctype.md "\#/properties/customer/properties/docType#/properties/customer/properties/docType")

### docType Type

`string` ([Doctype](cart-properties-customer-properties-doctype.md))

### docType Constraints

**minimum length**: the minimum number of characters for this string is: `0`

### docType Examples

```json
"cpf"
```

### doc

CPF formatado e CPF sem máscara


`doc`

-   is required
-   Type: `object` ([Doc](cart-properties-customer-properties-doc.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-customer-properties-doc.md "\#/properties/customer/properties/doc#/properties/customer/properties/doc")

#### doc Type

`object` ([Doc](cart-properties-customer-properties-doc.md))

### #doc Constraints

**minimum number of properties**: the minimum number of properties for this object is: `0`

#### doc Default Value

The default value is:

```json
{}
```

#### doc Examples

```json
{
  "formatted": "000.000.000-00",
  "raw": "00000000000"
}
```

### phone

.


`phone`

-   is required
-   Type: `object` ([Phone](cart-properties-customer-properties-phone.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-customer-properties-phone.md "\#/properties/customer/properties/phone#/properties/customer/properties/phone")

#### phone Type

`object` ([Phone](cart-properties-customer-properties-phone.md))

#### phone Constraints

**minimum number of properties**: the minimum number of properties for this object is: `0`

#### phone Default Value

The default value is:

```json
{}
```

#### phone Examples

```json
{
  "formatted": "(21) 00000-0000",
  "raw": "21000000000"
}
```

## address

Objeto de endereço do cliente


`address`

-   is required
-   Type: `object` ([Address](cart-properties-customer-properties-address.md))
-   cannot be null
-   defined in: [XPague Recuperação de carrinho](cart-properties-customer-properties-address.md "\#/properties/customer/properties/address#/properties/customer/properties/address")

#### address Type

`object` ([Address](cart-properties-customer-properties-address.md))

#### address Constraints

**minimum number of properties**: the minimum number of properties for this object is: `0`

#### address Default Value

The default value is:

```json
{}
```

#### address Examples

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

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema

2. ##

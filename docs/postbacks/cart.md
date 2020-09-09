---
layout: default
title: Cart
parent: postbacks
nav_order: 2
---

# Buttons
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Basic button styles

### Links that look like buttons

<div class="code-example" markdown="1">
[Link button](http://example.com/){: .btn }

[Link button](http://example.com/){: .btn .btn-purple }
[Link button](http://example.com/){: .btn .btn-blue }
[Link button](http://example.com/){: .btn .btn-green }

[Link button](http://example.com/){: .btn .btn-outline }
</div>
```markdown
[Link button](http://example.com/){: .btn }

[Link button](http://example.com/){: .btn .btn-purple }
[Link button](http://example.com/){: .btn .btn-blue }
[Link button](http://example.com/){: .btn .btn-green }

[Link button](http://example.com/){: .btn .btn-outline }
```

### Button element

GitHub Flavored Markdown does not support the `button` element, so you'll have to use inline HTML for this:

<div class="code-example">
<button type="button" name="button" class="btn">Button element</button>
</div>
```html
<button type="button" name="button" class="btn">Button element</button>
```

---

## Using utilities with buttons

### Button size

Wrap the button in a container that uses the [font-size utility classes]({{ site.baseurl }}{% link docs/utilities/typography.md %}) to scale buttons:

<div class="code-example" markdown="1">
<span class="fs-6">
[Big ass button](http://example.com/){: .btn }
</span>

<span class="fs-3">
[Tiny ass button](http://example.com/){: .btn }
</span>
</div>
```markdown
<span class="fs-8">
[Link button](http://example.com/){: .btn }
</span>

<span class="fs-3">
[Tiny ass button](http://example.com/){: .btn }
</span>
```

### Schema


<div class="code-example" markdown="1">
 
[Acessar ](https://painel.xpague.com/postback-schema-cart.json){: .btn .btn-blue }
</div>
```markdown

{
    "$schema": "http://json-schema.org/draft-07/schema",
    "$id": "http://painel.xpague.com/postback-schema-cart.json",
    "type": "object",
    "title": "XPague Recuperação de carrinho",
    "description": "Schema recuperação de carrinho.",
    "required": [
        "objectType",
        "product",
        "customer"
    ],
    "properties": {
        "objectType": {
            "$id": "#/properties/objectType",
            "type": "string",
            "title": "Tipo de postback",
            "description": "na recuperação o tipo tem que ser cart.",
            "default": "",
            "examples": [
                "cart"
            ]
        },
        "product": {
            "$id": "#/properties/product",
            "type": "object",
            "title": "Objeto do produto",
            "description": "",
            "default": {},
            "examples": [
                {
                    "productShipping": "0",
                    "productCover": "https://painel.xpague.com/app/uploads/2019/11/facereverse.png",
                    "productTotal": "349.00",
                    "fillableUrl": "https://pagamento.xpague.com/id/?src=postback&ct=36",
                    "productPrice": "349.00",
                    "id": 145720,
                    "checkoutId": 145622,
                    "productName": "Femme Busto Kit 5",
                    "description": "Creme para limpeza facial",
                    "productThumbnail": "https://painel.xpague.com/app/uploads/2020/01/FemmeGel.png"
                }
            ],
            "required": [
                "id",
                "productName",
                "description",
                "productPrice",
                "productShipping",
                "productCover",
                "productThumbnail",
                "productTotal",
                "fillableUrl"
            ],
            "properties": {
                "id": {
                    "$id": "#/properties/product/properties/id",
                    "type": "integer",
                    "title": "The Id Schema",
                    "description": "ID do produto.",
                    "default": 0,
                    "examples": [
                        145720
                    ]
                },
                "productName": {
                    "$id": "#/properties/product/properties/productName",
                    "type": "string",
                    "title": "Nome do produto",
                    "description": "Nome do produto.",
                    "default": "",
                    "examples": [
                        "Femme Busto Kit 5"
                    ]
                },
                "description": {
                    "$id": "#/properties/product/properties/description",
                    "type": "string",
                    "title": "Descrição do produto",
                    "description": "Descrição do produto",
                    "default": "",
                    "examples": [
                        "Creme para limpeza facial"
                    ]
                },
                "productPrice": {
                    "$id": "#/properties/product/properties/productPrice",
                    "type": "string",
                    "title": "Preço do produto",
                    "description": "Preço do produto.",
                    "default": "",
                    "examples": [
                        "349.00"
                    ]
                },
                "productShipping": {
                    "$id": "#/properties/product/properties/productShipping",
                    "type": "string",
                    "title": "Preço do frete",
                    "description": "Preço do frete",
                    "default": "",
                    "examples": [
                        "0"
                    ]
                },
                "productCover": {
                    "$id": "#/properties/product/properties/productCover",
                    "type": "string",
                    "title": "Imagem de capa",
                    "description": "",
                    "default": "",
                    "examples": [
                        " https://painel.xpague.com/app/uploads/2020/01/FemmeGeFl.png"
                    ]
                },
                "productThumbnail": {
                    "$id": "#/properties/product/properties/productThumbnail",
                    "type": "string",
                    "title": "Thumbnail do produto",
                    "description": "",
                    "default": "",
                    "examples": [
                        " https://painel.xpague.com/app/uploads/2020/01/FemmeGeFl.png"
                    ]
                },
                "productTotal": {
                    "$id": "#/properties/product/properties/productTotal",
                    "type": "string",
                    "title": "Total do produto com frete",
                    "description": "",
                    "default": "",
                    "examples": [
                        "349.00"
                    ]
                },
                "fillableUrl": {
                    "$id": "#/properties/product/properties/fillableUrl",
                    "type": "string",
                    "title": "The Fillableurl Schema",
                    "description": "",
                    "default": "",
                    "examples": [
                        "https://pagamento.xpague.com/id/?src=postback&ct=36"
                    ]
                }
            }
        },
        "customer": {
            "$id": "#/properties/customer",
            "type": "object",
            "readOnly": false,
            "writeOnly": false,
            "minProperties": 0,
            "title": "Customer",
            "description": "Cliente",
            "default": {},
            "examples": [
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
            ],
            "additionalProperties": true,
            "required": [
                "name",
                "docType",
                "doc",
                "phone",
                "address"
            ],
            "properties": {
                "name": {
                    "$id": "#/properties/customer/properties/name",
                    "type": "string",
                    "readOnly": false,
                    "writeOnly": false,
                    "minLength": 0,
                    "title": "Name",
                    "description": "Nome",
                    "default": "",
                    "examples": [
                        "María Teste Teste"
                    ]
                },
                "docType": {
                    "$id": "#/properties/customer/properties/docType",
                    "type": "string",
                    "readOnly": false,
                    "writeOnly": false,
                    "minLength": 0,
                    "title": "Doctype",
                    "description": ".",
                    "default": "",
                    "examples": [
                        "cpf"
                    ]
                },
                "doc": {
                    "$id": "#/properties/customer/properties/doc",
                    "type": "object",
                    "readOnly": false,
                    "writeOnly": false,
                    "minProperties": 0,
                    "title": "Doc",
                    "description": "CPF formatado e CPF sem máscara",
                    "default": {},
                    "examples": [
                        {
                            "formatted": "000.000.000-00",
                            "raw": "00000000000"
                        }
                    ],
                    "additionalProperties": true,
                    "required": [
                        "raw",
                        "formatted"
                    ],
                    "properties": {
                        "raw": {
                            "$id": "#/properties/customer/properties/doc/properties/raw",
                            "type": "string",
                            "readOnly": false,
                            "writeOnly": false,
                            "minLength": 0,
                            "title": "Raw",
                            "description": ".",
                            "default": "",
                            "examples": [
                                "00000000000"
                            ]
                        },
                        "formatted": {
                            "$id": "#/properties/customer/properties/doc/properties/formatted",
                            "type": "string",
                            "readOnly": false,
                            "writeOnly": false,
                            "minLength": 0,
                            "title": "Formatted",
                            "description": ".",
                            "default": "",
                            "examples": [
                                "000.000.000-00"
                            ]
                        }
                    }
                },
                "phone": {
                    "$id": "#/properties/customer/properties/phone",
                    "type": "object",
                    "readOnly": false,
                    "writeOnly": false,
                    "minProperties": 0,
                    "title": "Phone",
                    "description": ".",
                    "default": {},
                    "examples": [
                        {
                            "formatted": "(21) 00000-0000",
                            "raw": "21000000000"
                        }
                    ],
                    "additionalProperties": true,
                    "required": [
                        "raw",
                        "formatted"
                    ],
                    "properties": {
                        "raw": {
                            "$id": "#/properties/customer/properties/phone/properties/raw",
                            "type": "string",
                            "readOnly": false,
                            "writeOnly": false,
                            "minLength": 0,
                            "title": "Raw",
                            "description": ".",
                            "default": "",
                            "examples": [
                                "21000000000"
                            ]
                        },
                        "formatted": {
                            "$id": "#/properties/customer/properties/phone/properties/formatted",
                            "type": "string",
                            "readOnly": false,
                            "writeOnly": false,
                            "minLength": 0,
                            "title": "Formatted",
                            "description": ".",
                            "default": "",
                            "examples": [
                                "(21) 00000-0000"
                            ]
                        }
                    }
                },
                "address": {
                    "$id": "#/properties/customer/properties/address",
                    "type": "object",
                    "readOnly": false,
                    "writeOnly": false,
                    "minProperties": 0,
                    "title": "Address",
                    "description": "Objeto de endereço do cliente",
                    "default": {},
                    "examples": [
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
                    ],
                    "additionalProperties": true,
                    "required": [
                        "address",
                        "number",
                        "complementary",
                        "neighborhood",
                        "zipcode",
                        "city",
                        "state",
                        "country"
                    ],
                    "properties": {
                        "address": {
                            "$id": "#/properties/customer/properties/address/properties/address",
                            "type": "string",
                            "readOnly": false,
                            "writeOnly": false,
                            "minLength": 0,
                            "title": "Address",
                            "description": "endereço linha 1",
                            "default": "",
                            "examples": [
                                "Estrada Mirandela"
                            ]
                        },
                        "number": {
                            "$id": "#/properties/customer/properties/address/properties/number",
                            "type": "string",
                            "readOnly": false,
                            "writeOnly": false,
                            "minLength": 0,
                            "title": "Number",
                            "description": "Número",
                            "default": "",
                            "examples": [
                                "700",
                                "S/N"
                            ]
                        },
                        "complementary": {
                            "$id": "#/properties/customer/properties/address/properties/complementary",
                            "type": "string",
                            "readOnly": false,
                            "writeOnly": false,
                            "minLength": 0,
                            "title": "Complementary",
                            "description": "Complemento",
                            "default": "",
                            "examples": [
                                "Casa 01"
                            ]
                        },
                        "neighborhood": {
                            "$id": "#/properties/customer/properties/address/properties/neighborhood",
                            "type": "string",
                            "readOnly": false,
                            "writeOnly": false,
                            "minLength": 0,
                            "title": "Neighborhood",
                            "description": "Bairro",
                            "default": "",
                            "examples": [
                                "Centro"
                            ]
                        },
                        "zipcode": {
                            "$id": "#/properties/customer/properties/address/properties/zipcode",
                            "type": "string",
                            "readOnly": false,
                            "writeOnly": false,
                            "minLength": 0,
                            "title": "Zipcode",
                            "description": "CEP",
                            "default": "",
                            "examples": [
                                "26520332"
                            ]
                        },
                        "city": {
                            "$id": "#/properties/customer/properties/address/properties/city",
                            "type": "string",
                            "readOnly": false,
                            "writeOnly": false,
                            "minLength": 0,
                            "title": "City",
                            "description": "Cidade",
                            "default": "",
                            "examples": [
                                "Nilópolis"
                            ]
                        },
                        "state": {
                            "$id": "#/properties/customer/properties/address/properties/state",
                            "type": "string",
                            "readOnly": false,
                            "writeOnly": false,
                            "minLength": 0,
                            "title": "State",
                            "description": "Estado",
                            "default": "",
                            "examples": [
                                "RJ"
                            ]
                        },
                        "country": {
                            "$id": "#/properties/customer/properties/address/properties/country",
                            "type": "string",
                            "readOnly": false,
                            "writeOnly": false,
                            "minLength": 0,
                            "title": "Country",
                            "description": ".",
                            "default": "",
                            "examples": [
                                "br"
                            ]
                        }
                    }
                }
            }
        }
    }
}
```

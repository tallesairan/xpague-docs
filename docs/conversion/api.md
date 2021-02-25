---
layout: default
title: API De eventos Facebook
nav_order: 8
parent: Conversão
has_children: false
permalink: /conversion/facebook-events-api
---
## API de eventos Facebook

Instalando Pixel do Facebook na XPague usando a API de eventos do Facebook


### o que é a api de eventos do Facebook ?
A  API de conversão permite que os anunciantes enviem eventos da web de seus servidores diretamente para o Facebook. 

Os eventos do servidor são vinculados a um pixel e são processados como eventos de pixel do navegador. 

Isso significa que os eventos do servidor são usados na medição, relatório e otimização da mesma forma que os eventos de pixel do navegador.

### Por que isso é necessário agora?

Com as atualizações do IOS 14 um anunciante não pode mais registrar eventos de domínios que ele não tem permissão.

Porém, o Facebook disponibilizou uma forma de registrar os eventos nos seus anúncios, 
para seu pixel, mesmo que você não tenha como verificar o domínio. 

*(Agora somente um Business Manager pode verificar um domínio)*


 Nesse tutorial, você vai entender como configurar para que seus eventos sejam registrados corretamente.


**(Opcional)** Execute os passos a seguir caso não estiver usando um domínio customizado para suas campanhas.
 

Saiba mais em: [Guia domínios confirmados Facebook]({% link docs/conversion/facebook.md %})
 
 
Para dar a permissão do domínio da XPague é bem simples, confira os passos:          

1. Primeiramente, acesse a página do facebook business e efetue o login em sua conta.         

2. No menu principal, em configurações do negócio acesse Fonte de dados » Pixels.

3. Então, clique em Abrir no Gerenciador de Eventos localizado no canto superior direito.

4. Após abrir o gerenciador de eventos, vá em Configurações, em seguida Criar lista de permissão, conforme imagem abaixo. **(Opcional)**

5. Após clicar em criar lista de permissões, acrescente o domínio da xpague.com na lista de permissão. Não precisa adicionar subdomínios. **(Opcional)**

6. Agora pegue o token de acesso em Configurações » API de Conversões.

### Configurando em campanhas (afiliado e produtor)

* Ao clicar no botão será gerado um código que não será salvo pelo Facebook, portanto copie o conteúdo e em seguida na página do produto, vá em Campanhas, escolha a campanha e clique em Editar, ou na hora de criar sua campanha insira o token

### Configurando direto no produto (produtor)

Com essa regra o pixel fica inserido no produto, quando você realizar uma venda sem campanha automaticamente o pixel do produtor será inserido.

* Ao clicar no botão será gerado um código que não será salvo pelo Facebook, portanto copie o conteúdo e em seguida na página do produto, vá em Checkout, abaixe a página você vai ver dois campos (Pixel de trackeamento facebook e Token de acesso da API de conversões do Facebook, insira o pixel e o token e pronto.

Posso usar dois pixels ou mais como produtor ? **SIM**

Basta inserir uma vírgula separando seus pixels, lembrando que o token do pixel precisa ser separado por vírgulas também e na mesma ordem de inserção dos pixel



### Precisa de alguma ajuda?
Estamos prontos para ajudar, basta enviar um ticket na plataforma será um prazer atende-lo
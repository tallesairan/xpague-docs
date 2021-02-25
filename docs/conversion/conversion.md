---
layout: default
title: Conversão
nav_order: 6
has_children: true
permalink: /conversion
---
## Conversão
Guia para implementar o pixel do facebook em domínios confirmados

### Guia simples para implementação dessa nova estratégia.

Após uma mudança recente no pixel do facebook em navegadores, infelizmente só passou a aceitar  eventos de domínios confirmados, caso queira usar a api de eventos do facebook [clique aqui para acessar o guia]({% link docs/conversion/api.md %})

## Como instalar o código do pixel ?

* 1 Passo 

    Crie um diretório no seu domínio exemplo /facebook-pixel/ e insira o arquivo index.
* 2 Passo 

    Pegue a url do seu diretório exemplo: https://meusite.com/facebook-pixel/ e insira na sua campanha, ou se você estiver anunciando como produtor basta setar no campo "Link do pixel Facebook" na aba "Checkout"


### Informações adicionais.

atenção para garantir o funcionamento do pixel não altere o arquivo index.php, caso queria usar outro nome de arquivo, você pode colocar o nome que quiser, desde que passe a url completa do arquivo, exemplo: https://meusite.com/meu-pixel.php 

### Atenção

*   não inserir nenhum queryString ex https://meusite.com/facebook-pixel/?parametro na url deixar ela limpa!

        Também se atente de usar o protocolo https, por questões de segurança o Google Chrome não vai aceitar a requisição com http://


#### index.php - Copie o código abaixo e salve no seu servidor
```
<?php
/*
* Copyright (c) 2021.
* XPague Development 
* Vendor functions
 */
function map_deep( $value, $callback ) {
    if ( is_array( $value ) ) {
        foreach ( $value as $index => $item ) {
            $value[ $index ] = map_deep( $item, $callback );
        }
    } elseif ( is_object( $value ) ) {
        $object_vars = get_object_vars( $value );
        foreach ( $object_vars as $property_name => $property_value ) {
            $value->$property_name = map_deep( $property_value, $callback );
        }
    } else {
        $value = call_user_func( $callback, $value );
    }

    return $value;
}

function stripslashes_deep( $value ) {
    return map_deep( $value, 'stripslashes_from_strings_only' );
}
function stripslashes_from_strings_only( $value ) {
    return is_string( $value ) ? stripslashes( $value ) : $value;
}

$queryParams = $_REQUEST;

$pixelData = json_decode(stripslashes_deep($queryParams['id']), true);


if (!$pixelData) {
    die('');
}

?>
<!doctype html>
<html lang="en">
<head><meta charset="UTF-8">
<script>
    !function(f,b,e,v,n,t,s){if(f.fbq)return;n=f.fbq=function(){n.callMethod?
n.callMethod.apply(n,arguments):n.queue.push(arguments)};if(!f._fbq)f._fbq=n;
n.push=n;n.loaded=!0;n.version='2.0';n.queue=[];t=b.createElement(e);t.async=!0;
t.src=v;s=b.getElementsByTagName(e)[0];s.parentNode.insertBefore(t,s)}(window,
document,'script','https://connect.facebook.net/en_US/fbevents.js');
    fbq('init', '<?php echo $pixelData['id'];?>');
    fbq('track', 'PageView');
<?php
    foreach($pixelData['track'] as $ptrack):
        if(is_array($ptrack)):
        ?>
                fbq('track', '<?php echo $ptrack['event'];?>', <?php echo  str_replace('"',"'",json_encode($ptrack['params']));?>);
            <?php
        else:
        ?>
                fbq('track', '<?php echo ucfirst($ptrack);?>');
            <?php
        endif;
    endforeach;
?>

    <?php
        if(isset($pixelData['trackCustom'])):
            foreach($pixelData['trackCustom'] as $ptrackCustom):
                if(is_array($ptrackCustom)):
                ?>
                    fbq('trackCustom', '<?php echo $ptrackCustom['event'];?>',<?php echo str_replace('"',"'",json_encode($ptrackCustom['params']));?>);
                <?php
                else:
                ?>
                    fbq('trackCustom', '<?php echo $ptrackCustom;?>');
                <?php
                endif;
            endforeach;
    endif;
?>
</script>



<?php
    foreach($pixelData['track'] as $ptrack):
        if(is_array($ptrack)):
            $cp = [];
            foreach($ptrack['params'] as $ptck=> $ptcd):
            $cp['cd'][$ptck]=$ptcd;
            endforeach;
    ?>
            <noscript><img height='1' width='1' style='display:none' src='https://www.facebook.com/tr?id=<?php echo $pixelData['id']; ?>&ev=<?php echo $ptrack['event'];?>&<?=urldecode(http_build_query($cp,'cd','&'));?>&noscript=1'/></noscript>

        <?php
        endif;
    endforeach;
?>
    <?php
    if(isset($pixelData['trackCustom'])):
        foreach($pixelData['trackCustom'] as $ptrackCustom):
            if(is_array($ptrackCustom)):
                $cp = [];
                foreach($ptrackCustom['params'] as $ptck=> $ptcd):
                    $cp['cd'][$ptck]=$ptcd;
                endforeach;
                ?>
                <noscript><img height='1' width='1' style='display:none' src='https://www.facebook.com/tr?id=<?php echo $pixelData['id']; ?>&ev=<?php echo $ptrackCustom['event'];?>&<?=urldecode(http_build_query($cp,'cd','&'));?>&noscript=1'/></noscript>
            <?php
            endif;
        endforeach;
    endif;

    ?>
</head>
<body>

</body>
</html>
```
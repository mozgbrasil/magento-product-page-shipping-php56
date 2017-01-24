![valid XHTML][checkmark]
[checkmark]: https://raw.githubusercontent.com/mozgbrasil/mozgbrasil.github.io/master/assets/images/logos/Red_star_32_32.png "MOZG"
[requerimentos]: http://mozgbrasil.github.io/requerimentos/
[tickets]: https://cerebrum.freshdesk.com/support/tickets/new
[preco]: http://www.cerebrum.com.br/preco/
[getcomposer]: https://getcomposer.org/
[uninstall-mods]: https://getcomposer.org/doc/03-cli.md#remove

# Mozg\ProductPageShipping

## Sinopse

Visualização dos métodos de entrega na página do produto.

## Motivação

Atender o mercado de módulos para Magento oferecendo melhorias e um excelente suporte

## Suporte / Dúvidas

Para obter o devido suporte [Clique aqui][tickets], relatando o motivo da ocorrência o mais detalhado possível e anexe o print da tela para nosso entendimento

## Preço

[Clique aqui][preco]

## Característica técnica

É exibido na página de visualização do produto especificamente no bloco com o identificador "product.info.extrahint" o formulário para calculo do frete do produto, onde é retornado os serviços de entrega com seus respectivos valores.

## Instalação - Atualização - Desinstalação - Desativação

Este módulo destina-se a ser instalado usando o [Composer][getcomposer]

Antes de executar os processos, [clique aqui][requerimentos] e leia os pré-requisitos e sugestões

--

Certique se da existencia do arquivo composer.json na raiz do projeto Magento e que o mesmo tenha os trechos "minimum-stability", "prefer-stable", "repositories" e '"magento-root-dir":"./"', conforme https://gist.github.com/mozgbrasil/0c9bb8792ea6273ea24aed30b0fbcfba

Caso não exista o arquivo composer.json na raiz do projeto Magento, efetue o download

	wget https://gist.githubusercontent.com/mozgbrasil/0c9bb8792ea6273ea24aed30b0fbcfba/raw/9b514bc896171b6d75833b6f165065356f62ca59/composer.json

--

Para qualquer atualização no Magento sempre mantenha o Compiler e o Cache desativado

--

### Para instalar o módulo execute o comando a seguir no terminal do seu servidor

	composer require mozgbrasil/magento-product-page-shipping-php56:dev-master

Você pode verificar se o módulo está instalado, indo ao backend em:

	STORES -> Configuration -> ADVANCED/Advanced -> Disable Modules Output

--

### Para atualizar o módulo execute o comando a seguir no terminal do seu servidor

	composer clear-cache && composer update

Na ocorrência de erro, renomeie a pasta /vendor/mozgbrasil e execute novamente

Para checar a data do módulo execute o seguinte comando

	grep -ri --include=*.json 'time": "' ./vendor/mozgbrasil

--

### Para [desinstalar][uninstall-mods] o módulo execute o comando a seguir no terminal do seu servidor

	composer remove mozgbrasil/magento-product-page-shipping-php56 && composer clear-cache && composer update

--

### Para desativar o módulo

Renomeie a pasta do módulo

Cada módulo tem a sua pasta no diretório /vendor/mozgbrasil/

## Como configurar o método de entrega

Para configurar o método, acesse no backend em:

	STORES -> Configuration -> MOZG -> Geral -> Visualização dos métodos de entrega na página do produto

Você terá os campos a seguir

### • **Ativar**

Para "ativar" ou "desativar" o uso do método

### • **Debug**

Ative o mesmo para visualizar os nomes dos blocos

### • **Nome do Bloco**

Insira o nome do bloco

## Perguntas mais frequentes "FAQ"

### O recurso está ativo mas não está sendo exibido

Ative o debug, localize o nome do bloco que deseja que seja injetado bloco e na configuração do método altere para o nome do bloco

### Como usar o recurso em layout diferente

1.

Para esconder o bloco de calculo de frete

Aplique no CSS do seu template o seguinte

	.product-view .product-shop .segment { display: none; }

2.

Com o seu layout montado o exemplo a seguir pode ser usado como referencia

	<div>

	 <label for="cep_ajax">Frete:</label>
	 <input type="text" class="input-text" id="cep_ajax">

	 <button onclick="shippingProductView('cep_ajax','retorno-fretes');" class="button " title="Ok" type="button"><span><span>Ok</span></span></button>

	 <div id="retorno-fretes"></div>

	</div>

## Contribuintes

Equipe Mozg

## License

[Comercial License] (LICENSE.txt)

## Badges

[![Join the chat at https://gitter.im/mozgbrasil](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/mozgbrasil/)
[![Latest Stable Version](https://poser.pugx.org/mozgbrasil/magento-product-page-shipping-php56/v/stable)](https://packagist.org/packages/mozgbrasil/magento-product-page-shipping-php56)
[![Total Downloads](https://poser.pugx.org/mozgbrasil/magento-product-page-shipping-php56/downloads)](https://packagist.org/packages/mozgbrasil/magento-product-page-shipping-php56)
[![Latest Unstable Version](https://poser.pugx.org/mozgbrasil/magento-product-page-shipping-php56/v/unstable)](https://packagist.org/packages/mozgbrasil/magento-product-page-shipping-php56)
[![License](https://poser.pugx.org/mozgbrasil/magento-product-page-shipping-php56/license)](https://packagist.org/packages/mozgbrasil/magento-product-page-shipping-php56)
[![Monthly Downloads](https://poser.pugx.org/mozgbrasil/magento-product-page-shipping-php56/d/monthly)](https://packagist.org/packages/mozgbrasil/magento-product-page-shipping-php56)
[![Daily Downloads](https://poser.pugx.org/mozgbrasil/magento-product-page-shipping-php56/d/daily)](https://packagist.org/packages/mozgbrasil/magento-product-page-shipping-php56)
[![Reference Status](https://www.versioneye.com/php/mozgbrasil:magento-product-page-shipping-php56/reference_badge.svg?style=flat-square)](https://www.versioneye.com/php/mozgbrasil:magento-product-page-shipping-php56/references)
[![Dependency Status](https://www.versioneye.com/php/mozgbrasil:magento-product-page-shipping-php56/1.0.0/badge?style=flat-square)](https://www.versioneye.com/php/mozgbrasil:magento-product-page-shipping-php56/1.0.0)

:cat2:

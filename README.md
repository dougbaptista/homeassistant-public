# Projeto Home Assistant - Douglas Machado Baptista

Meu projeto está na versão 0.95.4 do HA com várias configurações baseado totalmente no projeto do Holandês [jimz011](https://github.com/jimz011/homeassistant). É uma cópia com os ajustes necessários para meus dispositivos, e com um pouco mais de comentários no código. O que facilita na hora de entender o projeto.

Se você pretende fazer uma cópia do meu projeto, você precisa entender e aplicar o [mode YAML](https://www.home-assistant.io/lovelace/yaml-mode/).

### Compartilhamento do Projeto

As automações do meu projeto são todas através do Node-RED, com exceção de apenas uma que é quando iniciar o HA. Por equanto ainda estou configurando as automações e relizando muitos ajustes. Caso alguém que conheça alguma automação minha, basta solicitar que eu passo via clipboard o fluxo da autoamação.

### CARDS

Antes de começar, precisa entender os cards que estou utilizando, e o motivo de utilizar para verificar se será preciso aplicar em seu projeto. E caso não utilize, será necessário realizar os ajustes no projeto.

#### HACS

Para iniciar, é preciso utilizar o componente HACS [https://custom-components.github.io/hacs/installation/manual/](https://custom-components.github.io/hacs/installation/manual/). Você até pode instalar manualmente cada card, mas terá que realizar pequenas modificações. Eu estou utilizando o HACS que nada mais é que um gerenciador de CARDS. Com ele você gerencia seus cards da mesma maneira que o HAssio gerencia os Addons. Se você ainda não utiliza, recomendo ao menos conhecer.

Nem todos os cards estarão disponíveis no HACS, porém você pode instalar manualmente para esses casos.

#### Lista de Cards do meu projeto - Suportado pelo HACS

- [Button-Card](https://github.com/custom-cards/button-card): Instalação pelo HACS. Esse cartão é fundamental para o design do projeto. Ele é o card mais utilizado para desenvolver botões, e mostrar algumas informações.
- [Lovelace-Card-Mod](https://github.com/thomasloven/lovelace-card-mod): Instalação pelo HACS. Esse cartão é o substituto do card-modder. Ele serve basicamente para aplicar estilos, sem esse cartão ficará com a aparência bem diferente.
- [Compact-Custom-Header](https://github.com/maykar/compact-custom-header): Instalação pelo HACS. Esse cartão serve apenas para ajustar o cabeçalho (compactar). Não é necessário, mas é interessante, principalmente para que for aplicar em tablets.
- [Lovelace-Markdown-Mod](https://github.com/thomasloven/lovelace-markdown-mod): Instalação pelo HACS. Substituto do useful-markdown-card. Serve para criar títulos personalizados, além de aplicar textos nas views. Recomendo você utilizar, se não pode ter problemas no design.
- [Mini-Media-Player](https://github.com/kalkih/mini-media-player): Instalação pelo HACS. Novamente não é necessário esse card para funcionamento do projeto. Mas está sendo muito utilizado pois deixa o media player mais dinâmico, customizado e bonito. Recomendo!
- [Calendar-Card](https://github.com/ljmerza/calendar-card): Instalação pelo HACS. Apenas para mostrar o calendário que integro com a agenda do Google. Se você não vai utilizar calendário, não é necessário.
- [Simple-Weather-Card](https://github.com/kalkih/simple-weather-card): Instalação pelo HACS. Esse cartão é para mostrar as informações do clima de uma forma mais compacta. É o cartão que uso na view principal. Como eu prefiro ter apenas a informação básica do clima, optei por utilizar esse cartão, ocupa menos espaço.
- [Mini-Graph-Card](https://github.com/kalkih/mini-graph-card): Instalação pelo HACS. Se você perceber, no meu projeto tem vários botões com gráficos. Sem esse cartão não será possível aplicar esses "botões". Além disso, esse card te oferece diversas opções de customizar os seus gráficos, sem dúvida um dos melhores cards para gráficos. Recomendo!
- [Light-Entity-Card](https://github.com/ljmerza/light-entity-card): Instalação pelo HACS. Esse cartão no meu projeto é utilizado para as opções de cores para as lâmpadas, quando abre uma janela (popup) para mostrar as opções de iluminação. Não é necessário, mas se você tem lâmpadas RGB/Dimmer, eu recomendo.
- [Lovelace-Decluttering-Card](https://github.com/custom-cards/decluttering-card): Instalação pelo HACS. Você já ouviu falar em CSS? Então, esse cartão basicamente funciona dessa forma. Você cria os estilos de botões, e usa ele no seu projeto. Se você quer alterar algum estilo do botão, você simplesmente altera nesse cartão. Então você vai personalizar os seus cartões com esse cartão. Não é só design como o CSS que citei, é muito mais. Sem esse cartão, o meu projeto NÃO irá funcionar. Ele foi um substituto das âncoras, que também cheguei a utilizar quando o jimz011 utilizava no projeto dele na versão antiga.
- [Day Countdown](https://github.com/bundito/day-countdown): Instalação pelo HACS. Como você pode perceber na página do desenvolvedor, desde abril o mesmo não está mais realizando ajustes nem dando suporte. Portando, eu pretendo mudar em breve esse cartão. Ele serve apenas para realizar uma contagem em dias para uma determinada data. Se não vai utilizar esse recurso, não é necessário.
- [Ext Weblink](https://github.com/custom-cards/ext-weblink): Instalação pelo HACS. Esse card é super simples, apenas para facilitar a criação de textos e links com imagens. Não é necessário.
- [Lovelace Layout Card](https://github.com/thomasloven/lovelace-layout-card): Instalação pelo HACS. Não estou utilizando esse card no meu projeto, tenho instalado apenas para testes. Não instale se não for utilizar.
- [Lovelace Xiaomi Vacuum Card](https://github.com/benct/lovelace-xiaomi-vacuum-card): Instalação pelo HACS. Apenas para gerenciar as ações do aspirador Vacuum da Xiaomi. Se você não vai aplicar, não é necessário. Futuramente pretendo experimentar o mesmo cartão que o jimz011 está utilizando no projeto dele.
- [Swipe Card](https://github.com/bramkragten/swipe-card): Instalação pelo HACS. Estou utilizando esse card para arrastar e mostrar outras informações. No meu projeto utilizo por exemplo na página principal com o consumo e arrasto para ver o consumo dos equipamentos por mês, por dia e total. Não é necessário.

#### Lista de Cards do meu projeto - Não suportado pelo HACS (Necessita de instalação manual)

- [Card-Tools](https://github.com/thomasloven/lovelace-card-tools): Instalação manual através do HACS. É um requisito para utilizar outros cartões. É obrigado a ter esse cartão instalado.
- [Popup-Card](https://github.com/thomasloven/lovelace-card-tools): Instalação manual através do HACS. Esse cartão é o que faz a mágica para abrir as janelas/modais no meu projeto. Sem isso, os botões da página principal não irão funcionar.
- [Thermostat-Card](https://github.com/thomasloven/lovelace-card-tools): Instalação manual. Esse cartão é uma exceção para realizar a instalação. Não é possível instalar manualmente pelo HACS, nesse caso será preciso voltar a moda "antiga" e baixar os arquivos para instalar manualmente. Esse cartão serve para mostrar a temperatura do ar condicionado. Não é necessário, você pode substituir por outros modelos de climatização.
- [Sun-Card](https://github.com/mishaaq/sun-card): Instalação manual através do HACS. Esse cartão é onde mostra as informações do sol (pôr do sol e nascer do sol). Se você não vai utilizar, não é necessário.

### Imagens e Vídeo

<img src="https://github.com/dougbaptista/homeassistant-public/blob/master/screenshots/01.jpg">
<img src="https://github.com/dougbaptista/homeassistant-public/blob/master/screenshots/02.jpg">
<img src="https://github.com/dougbaptista/homeassistant-public/blob/master/screenshots/03.jpg">
<img src="https://github.com/dougbaptista/homeassistant-public/blob/master/screenshots/04.jpg">
<img src="https://github.com/dougbaptista/homeassistant-public/blob/master/screenshots/05.jpg">
<img src="https://github.com/dougbaptista/homeassistant-public/blob/master/screenshots/06.jpg">
<img src="https://github.com/dougbaptista/homeassistant-public/blob/master/screenshots/07.jpg">
<img src="https://github.com/dougbaptista/homeassistant-public/blob/master/screenshots/08.jpg">
<img src="https://github.com/dougbaptista/homeassistant-public/blob/master/screenshots/09.jpg">
<img src="https://github.com/dougbaptista/homeassistant-public/blob/master/screenshots/10.jpg">

Para que quiser ver algumas telas do meu projeto, pode ser visualizado no vídeo abaixo. Recomendo assistir se realmente tiver interesse em copiar alguma parte do projeto.

Vídeo em breve.

### Dúvidas

Por favor, se você tiver dúvida entre no grupo do [telegram](https://t.me/HomeAssistantbrasil) onde eu e várias outras pessoas compartilham conhecimentos sobre o HA e ajudam na medida do possível nas questões.

### Agradecimentos

- @remontti - Por me ajudar muito a entrar no mundo do Home Assistant, através do seu projeto é que entendi o "poder" do HA.
- @jimz011 - Por compartilhar todo seu projeto, além disso responder todas as minhas dúvidas. Meu projeto é "ctrl+c" e "ctrl+v" do projeto dele.
- Canal Youtube Patte Tech - Foi graças a seus vídeos, grupos que me fez entrar no mundo da automação, ajudam muitas pessoas como eu que querem começar e tem diversas dúvidas.
- @marciogranzotto - Por compartilhar suas automações incríveis, como pegar as taxas de energia elétrica da empresa CELESC.
- @htcheroportugal - Co-Fundador CPHA, uma comunidade portuguesa muito forte com projetos utilizando o HA, e para nós brasileiros é muito importante, pois entendemos perfeitamente seus tutoriais, vídeos etc. São muito atenciosos e organizados. Sempre que precisei me ajudaram de várias formas.

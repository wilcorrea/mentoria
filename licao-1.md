# Web Components

Numa tradução livre "Web Components" seria algo como "Componentes para a Web". Entender o que eles podem fazer por nós pode nos fazer ter um poder maior de controle sobre ferramentas baseadas sobre esse conceito.

## Introdução

As primeiras especificações da W3C acerca de "Web Components" que consegui encontrar datam do início de 2013 e sua adoção, assim como melhorias do projeto, estão caminhando a passos largos. Considerando que componentes são fragmentos de software agnósticos que poderiam ser transpostos e plugados em diferentes projetos de forma transparente, temos que avaliar como isso se daria na web.

Toda as páginas de internet tem o mesmo formato: HTML. Desde o Facebook ao Google passando pelo site do Globo ou CNN são todos iguais! Isso torna a web justa e simples. Não importa o quão grande você seja e todas as peripécias que lance mão para criar um recurso porque se ele for ser acessível através de um browser ele terá que ser uma página HTML como todas as outras.

Inicialmente parece que boa parte do folego do projeto veio do Polyfill e do Polymer, que são projetos pioneiros na área.

## O Problema

Um dos principais desafios das interfaces para a web não é mais a compatibilidade do leiaute, a limitação do hardware ou a insuficiência da banda de rede e sim como produzir interfaces inteligentes. Depois de um primeiro cenário de baixa identidade, no qual o desenvolvimento para a web copiou os comportamentos do ambiente desktop, a web se encontrou e conseguir criar uma cara própria. Porém essa identidade está altamente relacionada a interfaces inteligentes, rápidas e intuitivas para as quais o HTML tornou-se cada vez menos suficiente. Ainda que muitos esforços tenham sido empregados para aprimorar o HTML, Javascript e CSS há uma certa defasagem entre as necessidades dos projetos e o que os navegadores tem a oferecer. Além disso, com a rotineira customização de telas usando CSS e JS, o modelo de desenvolvimento que compreende um WebApp como um único rochedo transforma a vida dos desenvolvedores numa complexa sopa de letrinhas nas quais ferramentas e mais ferramentas tentam suprir a falta de habilidade de modularização nativa dos navegadores.

## HTML

Quando criamos páginas para a web usamos componentes descritos pelo HTML. Ao escrevermos o trecho `<input/>` o navegador interpreta essa marcação (também conhecida como TAG) e renderiza um campo de texto. Embora os recursos entregues por essa espeficação sejam eficientes, é preciso pensar o quanto poderia ser mais produtivo produzir conteúdo para a web se pudéssemos ter o poder de mutar essas marcações a fim de criarmos componentes que se comportem de forma mais conveniente.

A proposta dos "Web Components" é atuar nessa área, permitindo que o desenvolvedor possa evoluir sua aplicação por sobre os componentes básicos criando novas composições reusáveis e plugáveis.

# Os Princípios Básicos

Os "Web Components" são baseados em 4 tecnologias: Custom Elements, HTML Templates, Shadow DOM e HTML Imports. Cada um tem seu papel nessa perspectiva e serão necessários de acordo com o contexto. Um componente pode fazer uso de todos ou de apenas um.

## Custom Elements (Elementos Customizados)

As primeiras versões dos navegadores eram muito severas em relação a interpretação do HTML que recebiam. Com o passar do tempo eles foram se tornando mais inteligentes e hoje conseguem perceber vazamentos de tags e corrigir o código que recebem. Ainda que os interpretadores tornem-se cada vez mais eficientes é preciso perceber que o HTML é um conjunto de tags finito e que para ir além dos componentes tradicionais poderia ser preciso criar novos Elementos. Sendo assim a implementação desse recurso permite que nós informemos ao navegador que estamos usando tags customizadas e inclusive atribuir comportamentos a elas.


# Posicionamento de elementos com Flexbox em CSS

1. Projeto Flex Turismo com base no projeto elaborado por Karen Santos (https://gitlab.com/karensantos/project-flexbox-dio)

2. Aula sobre posicionamento com flexbox em CSS, de forma a deixar uma página responsiva.


### Display: flex

Modifica a posição do item dentro do container, ficando ele alinhado horizontalmente ou verticalmente.
Primeira propriedade a ser modificado no CSS.

### Flex Container

é a tag que envolve os itens, sendo nela aplicada a propriedade <b>display: flex;</b> trasformando os itens filhos em flex-itens.

- display: inicializador do container
- flex-direction: direcionamento dos itens
- flex-wrap: quebra de linha ou não
- flex-flow: abreviação de direction e wrap
- justify-content: alinhamento na direção
- align-items: alinhamento conforme eixo
- align-content: alinhamento de linhas

<b> PROPRIEDADES RELACIONADAS AO FLEX CONTAINER</b>

#### Flex-direction

Estabelece o eixo principal do container.

- row: eixo horizontal, por padrão (>>>)
- row-reverse: eixo horizontal, (<<<)
- column: eixo vertical, para baixo
- column-reverse: eixo vertical, para cima


#### Flex-wrap

Estabelece a quebra de linha ou não dos itens.

- now-wrap: por padrão, não é quebrado - ultrapassa o limite
- wrap: permite a quebra de linha a partir do primeiro elemento que não é comportado
- wrap-reverse: mesma lógica do wrap, porém o contrário (a partir da linha abaixo)


#### Flex-flow
Atalho para flex-direction e flex-wrap, tendo um uso incomum.


#### Justify-content

Alinha os itens dentro do container de acordo com a direção e determina o espaçamento entre eles.
Não se aplica a itens que ocupam 100% do container.
Aceita flex-direction row e column.

- flex-start: alinha no início do container
- flex-end: alinha no final do container, respeitando o limite
- center: centraliza o item
- space-between: alinha com espaçamento igual entre os elementos, mas com o primeiro e último elementos colados as bordas
- space-around: alinha os elementos com o espaçamento do meio duas vezes maior em relação aos espaços inicial e final
- space-evenly: mesmo espaçamento entre todos, incluindo aquele entre a borada e os elementos inicial e final


#### Align-items

Alinha os itens de acordo com o eixo do container, tendo diferença nos eixos vertical e horizontal.
Não precisa ter a altura necessariamente, diferente do justify-content.

- stretch: por padrão, fazendo com que os itens cresçam de forma igual
- center: alinhamento centralizado
- flex-start: alinahmento no início (top)
- flex-end: alinhamento ao final (botton)
- baseline: alinhamento de acordo com a linha do texto contido no item

OBS: para alinhar totalmente ao centro, utilizar : align-itens:center, justify-content: center e flex: 0 (flex: 0 zera as propriedades grow, shrink e basis). alterar o padding também.


#### Align-content

Alinha as linhas no container no eixo vertical, utilizando a quebra de linhas (flex wrap) e a altura.

- center: alinhamento ao centro
- stretch: por padrão, pegando o maior elemento como referência
- flex-start: alinhamento no início
- flex-end: alinhamento ao final
- space-between: espaçamento igual entre os elementos
- space-around: espaçamento duas vezes maior em relação ao inicio e final

###  Flex Items

São os elementos filhos diretos do container, podendo-se aplicar a propriedade <b>display: flex;</b> trasformando os itens filhos em flex-itens, e assim sucessivamente.

- flex-grow: crescimento
- flex-basis: inicial do item antes da distribuição do espaço restante
- flex-shrink: capacidade de redução
- flex: abreviação para grow, basis e shrink
- order: ordem de distribuição e listagem
- align-self: alinhamento de item específico dentro do container

<b> PROPRIEDADES RELACIONADAS AOS FLEX ITEMS</b>

#### Flex-grow

Define a proporção que o item pode ocupar, respeitando o seu tamanho.
Não funciona caso seja usado a propriedade justify-content ao flex-container.
Aceita números, indicando quantas vezes o item irá crescer.

#### Flex-basis

Propriedade que define o tamanho inicial do item antes das distribuições de espaço do restante.

- auto: quando o item não tem tamanho pré-definido, sendo proporcional ao conteúdo
- valores exatos em px, %, em
- zeroo: relacionado a definição do flex-grow



#### Flex-shrink

Propriedade que define a capacidade de redução de um item quando necessário.
Sobrescreve as propriedades widht e height. Respeita min/max-widht/height.

- auto
- zero
- max-content
- min-content


#### Flex

Atalho para grow-basis-shrink.


#### Order

Ordenação dos itens. Aceita valores negativos para posicionamento.


#### Align-self

Alinhamento individual do item.
Não definir align-items no container para usar essa propriedade.

- auto
- center
- flex-start
- flex-end
- stretch
- baseline
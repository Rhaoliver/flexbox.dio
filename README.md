# Posicionamento de elementos com Flexbox em CSS

Aula sobre posicionamento com flexbox em CSS, de forma a deixar uma página responsiva.

### Flex Container

é a tag que envolve os itens, sendo nela aplicada a propriedade <b>display: flex;</b> trasformando os itens filhos em flex-itens.

- display: inicializador do container
- flex-direction: direcionamento dos itens
- flex-wrap: quebra de linha ou não
- flex-flow: abreviação de direction e wrap
- justify-content: alinhamento na direção
- align-items: alinhamento conforme eixo
- align-content: alinhamento de linhas

###  Flex Itens

são os elementos filhos diretos do container, podendo-se aplicar a propriedade <b>display: flex;</b> trasformando os itens filhos em flex-itens, e assim sucessivamente.

- flex-grow: crescimento
- flex-basis: inicial do item antes da distribuição do espaço restante
- flex-shrink: capacidade de redução
- flex: abreviação para grow, basis e shrink
- order: ordem de distribuição e listagem
- align-self: alinhamento de item específico dentro do container
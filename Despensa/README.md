## Contexto Delimitado para Controle de Despensa
### Entidades para o Domínio:
#### Local. Exemplo: Geladeira, Câmara Fria, Freezer, Isopor, Armário, Despensa Física
#### Categoria do Local: [Quente, Frio]
#### Item da Despensa. São os itens armazenados e conservados no Local. Aqui são controladas a data de validade, a retirada e a inserção do produto
#### Produto
#### Categoria do Produto: [Perecível, Não Perecível]
#### Estado do Produto: [Seco, Molhado]


### Cada local irá gerenciar diretamente seus itens, um exemplo:
* Local: Geladeira
* Item da Geladeira: São produtos previamente cadastrados para este local, alguns produtos, podem ser produtos perecíveis. 
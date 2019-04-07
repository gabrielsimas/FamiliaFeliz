- Controle de contas a pagar
- Entrada => Tipo de Conta => Entrada é positivo
-- Salário => Valor e Data de PGTO
- Saida
-- 

=> Entrada
Nome (Texto),
Descrição (Texto),
Data Credito (Data)
Valor Crédito ($)
Habilitado (S/N)

=> Saída
Nome
Descrição
Tipo de Controle (Codigo de Barras, com seus tipos distintos, cada tipo de conta tem um código de barras diferentes)
Valor (Pode ser lido via código de barras direto, ou de início, pode-se colocar manualmente)
Multa por não pagamento
Juros de Mora
Data de Vencimento
Data de Pagamento
Controle (Controle alfanumérico do Banco que registra o pagamento da conta).

Exemplo de entrada e saídas
- EM ABERTO
OBS.: O uso de valores entre [], significa que os valores são de variáveis ou campos no Banco de dados, portanto, são campos mutáveis.
- Cadastro das Contas para Pagamento posterior
Entrada
- Conta: Pagamento Mensal
  - Salário Comp. Março
  - Data de Crédito: 10/04/2019
  - Valor: R$200,00
  - Tipo: Salário Registrado em Carteira (CLT) OU Nota Fiscal de Serviços emitida (PJ) OU Outra natureza (Natureza deve ser programável para que faça os cálculos automáticos)
  - Crédito Efetuado: [N]

Saída
- Conta: Conta de Luz - Light
  - Valor: R$182,00;
  - Data de Vencimento: 15/04/2019
  - Multa por não pagamento: [1%] de 182,00;
  - Juros de mora: [1%] por [dia][corrido/útil] após o vencimento;

Total de Entradas: [R$200,00]
Total de Saídas: [R$182,00]
Total Apurado = SOMA(Entradas) + SOMA(Contas)*-1 = 200 + (-182,00) = 18,00
Ativo (Valor que entrou)=
Passivo (Valor que saiu)=
Porcentagem (Passivo x Ativo) = [182,00 / 200,00] = [91%] = Até 30%, deve-se colocar a cor verde; Acima de 30% pode-se colocar em amarelo; até 60% > acima de 60% deve-se colocar a cor vermelha

- PAGAS
- Cadastro das Contas para Pagamento posterior
Entrada
- Conta: Pagamento Mensal
  - Salário Comp. Março
  - Data de Crédito: 10/04/2019
  - Valor: R$200,00
  - Tipo: Salário Registrado em Carteira (CLT) OU Nota Fiscal de Serviços emitida (PJ) OU Outra natureza (Natureza deve ser programável para que faça os cálculos automáticos)
  - Crédito Efetuado: [S]

Saída
- Conta: Conta de Luz - Light
  - Valor: R$182,00;
  - Data de Vencimento: 15/04/2019
  - Multa por não pagamento: [1%] de 182,00;
  - Juros de mora: [1%] por [dia][corrido/útil] após o vencimento;

Total de Entradas: [R$200,00]
Total de Saídas: [R$182,00]
Total Apurado = SOMA(Entradas) + SOMA(Contas)*-1 = 200 + (-182,00) = 18,00
Ativo (Valor que entrou)=
Passivo (Valor que saiu)=
Porcentagem (Passivo x Ativo) = [182,00 / 200,00] = [91%] = Até 30%, deve-se colocar a cor verde; Acima de 30% pode-se colocar em amarelo; até 60% > acima de 60% deve-se colocar a cor vermelha

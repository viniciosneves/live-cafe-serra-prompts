# Etapa 1 · Análise dos dados

[← voltar](../README.md)

## Prompt

```text
Sou dona do Café Serra, uma cafeteria com duas lojas (Centro e Olaria) e delivery. Daqui a 30 minutos tenho reunião com meu sócio pra decidir o que fazer no próximo trimestre.

Anexei dois arquivos: (1) as vendas de julho a setembro, exportadas do sistema, e o arquivo está bagunçado; (2) as avaliações de clientes do mesmo período.

Tarefa: limpe os dados, cruze as vendas com as avaliações e me traga os 3 achados mais importantes pro negócio. Cada achado precisa do número que o sustenta e de um trecho de avaliação que explique o porquê.

Entrega: uma planilha com os dados limpos e um resumo por mês, loja e canal, e um resumo de meia página pra eu ler antes da reunião.

Antes dos achados, me diga em uma linha o que você precisou corrigir nos dados. Se algum achado tiver pouca evidência, avise.
```

## Amostra do arquivo de vendas (como veio do sistema)

```text
data;loja;canal;produto;qtd;valor
01/07/2026;Centro;Balcão;Café expresso;39;R$ 253,50
2026-07-01;Centro;Balcão;Cappuccino;27;R$ 324,00
01/07/2026;Centro;Balcão;Pão de queijo;56;R$ 308,00
01/07/2026;Centro;Balcão;Bolo de fubá (fatia);21;R$ 189,00
01/07/2026;Centro;Balcão;Croissant;16;R$ 176,00
01/07/2026;Centro;Balcão;Combo Tarde;4;88.00
2026-07-01;Centro;Balcão;Café coado;24;R$ 168,00
01/07/2026;Centro;Balcão;Cold brew;8;112.00
01/07/2026;Centro;Delivery;Café expresso;19;R$ 123,50
18/08/2026;Centro;delivery;Café expresso;10;R$ 65,00
01/07/2026;Centro;Delivery;Cappuccino;12;144.00
2026-07-01;Centro;Delivery;Pão de queijo;25;137.50
01/07/2026;Centro;delivery;Bolo de fubá (fatia);9;R$ 81,00
01/07/2026;centro ;Delivery;Croissant;5;55.00
2026-07-01;Centro;delivery;Combo Tarde;1;R$ 22,00
01/07/2026;CENTRO;Delivery;Café coado;8;R$ 56,00
01/07/2026;Centro;Delivery;Cold brew;4;56.00
01/07/2026;Olaria;Balcão;Café expresso;26;169.00
```

## Resposta

**Correções nos dados:** padronizei datas, nomes das lojas, canais e valores em reais; identifiquei 25 registros duplicados e 12 campos vazios que puderam ser reconstruídos pelos preços unitários. Os duplicados serão excluídos dos totais, mantendo o histórico para auditoria.

A análise vai separar faturamento, volume vendido e experiência do cliente, para que a decisão do próximo trimestre não dependa apenas de opiniões isoladas.

## Os 3 achados mais importantes

### 1. O delivery do Centro é a prioridade mais urgente.

**−31,3%**
Receita de julho a setembro: R$ 21.814,50 → R$ 14.991,00

A nota média desse canal foi 2,33/5, em 12 avaliações, contra 4,25/5 na Olaria, em 4 avaliações.

> “Cappuccino frio pela terceira vez. Vou trocar de cafeteria.” — 22/09, App delivery, Centro

**Decisão:** revisar tempo de preparo, embalagem térmica, conferência e expedição dos pedidos.

### 2. O balcão da Olaria está crescendo e pode servir de referência.

**+15,8%**
Receita de julho a setembro: R$ 39.254,50 → R$ 45.469,00

A experiência presencial da Olaria recebeu média 4,46/5, em 13 avaliações do Google.

> “Melhor café da região. A equipe da Olaria é outro nível.” — 11/08, Google, Olaria

**Decisão:** preservar a qualidade do atendimento e estudar quais práticas podem ser replicadas no Centro.

### 3. A queda do cold brew merece investigação imediata.

**−43,5%**
Unidades vendidas nas duas lojas: 736 em agosto → 416 em setembro

A Olaria caiu de 369 para 205 unidades, e duas avaliações de setembro mencionam a falta do produto.

> “Cadê o cold brew? Disseram que acabou e não tem previsão.” — 03/09, Google, Olaria

**Decisão:** verificar rupturas de estoque e produção antes de investir em divulgação.

**Evidência limitada:** os relatos sugerem falta de estoque, mas não permitem atribuir toda a queda de vendas a esse motivo.

**Ressalva geral:** as avaliações são uma amostra pequena e não estão vinculadas a pedidos específicos. Elas ajudam a explicar possíveis causas, mas não comprovam causalidade.

### Arquivos prontos para a reunião

- **Planilha limpa e consolidada:** Excel com 2.924 registros válidos, resumo por mês, loja e canal, detalhamento por produto, avaliações e histórico de duplicados.
- **Resumo executivo de meia página:** texto pronto para leitura, com os três achados, números, depoimentos, ações e ressalvas.

**Minha sugestão para a reunião:** sair com três responsáveis definidos — um para recuperar o delivery do Centro, outro para investigar a disponibilidade do cold brew e outro para replicar as boas práticas da Olaria. Revisar os resultados semanalmente, antes de decidir novos investimentos.

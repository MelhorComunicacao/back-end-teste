
# Teste de Back-End (NodeJS)

### Proposta

Uma empresa vai lançar um novo app para venda de celulares e com isso gostaríamos que você construísse uma api para gerenciar o cadastro de novos celulares.

### Requisitos

1. A api deverá ser feita em NODE utilizando EXPRESS.
2. Poderá ser utilizado qualquer biblioteca adicional.
3. Deverá ser entregue o link do respositório git com a resolução.

### Solução

A solução consistirá em criar uma api em NODE utilizando EXPRESS.

### Descrição do modelo

| Campo     | Tipo        | Descrição                          | Restrições                                                                                        |
| --------- | ----------- | ---------------------------------- | ------------------------------------------------------------------------------------------------- |
| model     | Texto       | Nome do modelo do celular          | Alfanumérico com no mínimo 2 e no máximo 255 caracteres, desprezando espaço em branco.            |
| price     | Número real | Preço do celular                   | Número positivo                                                                                   |
| brand     | Texto       | Nome da marca do celular           | Alfanumérico com no mínimo 2 e no máximo 255 caracteres, desprezando espaço em branco.            |
| startDate | Data        | Data de início da venda do celular | Data no formato “dd/MM/yyyy” (31/12/2018). A data de início deve ser posterior ao dia 25/12/2018. |
| endDate   | Data        | Data de fim da venda do celular    | Data no formato “dd/MM/yyyy” (31/12/2018). A data de fim deve ser posterior a data de início.     |
| color     | Lista fixa  | Cor do celular                     | Essa campo admite apenas os seguintes valores: BLACK, WHITE, GOLD, PINK.                          |
| code      | Texto       | Código de identificação do celular | Alfanumérico de 8 caracteres. Não deve se repetir.                                                |

### Operações

Deve ser possível:

- **Cadastrar** um celular;
- **Listar** todos os celulares;
- **Ver** um celular;
- **Deletar** um celular;
- **Atualizar** um celular;
- **Toda requisição deve receber no cabeçalho(header) um cpf (não nulo): 
 { cpf : ******* }**


### Validação

O backend deve retornar um resposta com o código HTTP adequado, de acordo com o resultado da validação, além de incluir uma mensagem para cada violação.

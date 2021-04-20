
# Teste de Back-End (NodeJS)

### Proposta

Uma empresa vai lançar um novo app para venda de celulares e com isso gostaríamos que você construísse uma API para gerenciar as informações desse app.

### Requisitos

1. A API deverá ser feita em NODE.
2. A API deverár receber requisições http corretamente e retornar resultados em json.
3. Poderá ser utilizada qualquer biblioteca adicional.
4. Deverá ser entregue o link do respositório git com a resolução.
5. Caso seja necessário algum preparo para rodar a aplicação e os testes, informar num arquivo README.md (por exemplo).


### Descrição dos tipos do modelo

| Campo     | Tipo        | Descrição                          | Restrições                                                                                        |
| --------- | ----------- | ---------------------------------- | ------------------------------------------------------------------------------------------------- |
| id        | uuid        | Código de identificação do celular | Alfanumérico de 8 caracteres. Não deve se repetir.     
|
| model     | text        | Nome do modelo do celular          | Alfanumérico com no mínimo 2 e no máximo 255 caracteres, desprezando espaço em branco.       
|
| price     | decimal     | Preço do celular                   | Número positivo.
|
| brand     | text        | Nome da marca do celular           | Alfanumérico com no mínimo 2 e no máximo 255 caracteres, desprezando espaço em branco.       
|
| start_date| Date        | Data de início da venda do celular | Data no formato “dd/MM/yyyy” (31/12/2018). A data de início deve ser posterior ao dia 25/12/2018. 
|
| end_date  | Date        | Data de fim da venda do celular    | Data no formato “dd/MM/yyyy” (31/12/2018). A data de fim deve ser posterior a data de início.  
|
| available_colors  | Array  | Cor do celular                  | Essa campo admite apenas os seguintes valores: black, white, gold, gay, pink.      
            
            
### Ações que devem ser disponibilizadas para os consumidores da API


```POST /cellphones```

  ENTRADA
  
              { 
                 id: '34bd8824-a1f0-11eb-bcbc-0242ac130002'
                 brand : 'motorola'
                 model : 'one',
                 price : 1000, 
                 start_date: 'dd/MM/yyyy',
                 end_date: 'dd/MM/yyyy',
                 available_colors: [  black, white, gold, gay, pink ]
              } 

  SAÍDA

    Deve retornar um 200 com o registro criado em formato json

```PATCH /cellphones/:id```

  ENTRADA 
  
               {
                  brand : 'motorola'
                  model : 'one',
                  price : 1000, 
                  start_date: 'dd/MM/yyyy',
                  end_date: 'dd/MM/yyyy',
                  available_colors: [  black, white, gold, gay, pink ]
               }

  SAÍDA

    Deve retornar um 200  indicando que as informações foram alteradas com sucesso

```DELETE /cellphones/:id```

    Deve retornar um 200 indicando que o registro foi alterado com sucesso

```GET /cellphones/:id```

    Deve retornar um 200 com o registro referente ao id enviado como parâmetro

```GET /cellphones```

   Deve retornar um 200 com todos os celulares registrados no banco de dados da aplicação


Fique Atento!

- Toda requisição deve receber no cabeçalho (header) um cpf (não nulo): { cpf : ******* }
- O backend deve retornar uma resposta com o código HTTP adequado, de acordo com o resultado da validação, além de incluir uma mensagem para cada violação.

### Sobre Testes

O máximo que conseguir!

### Não é obrigatório mas se conseguir, massa!

- Disponibilizar na aplicação um arquivo de gerenciamento de conteiners docker (ex: docker-compose ) para acessarmos o seu banco de dados (BD) ;)
- Usar migrations para a criação da tabela do BD

### E quanto à Avaliação? 

O objetivo desse teste é verificar como você estrutura o projeto, organiza e testa seu código!

### Uma dica!

Não se prenda à descrição do projeto, seja criativo!!

### Dúvidas?? 

Fique a vontade pra abrir uma nova issue!





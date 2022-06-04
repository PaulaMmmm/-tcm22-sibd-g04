# C4 : Esquema Relacional  

- [Relações](#relações)
  - [Tabela_a](#tabela_a)
  - [Tabela_b](#tabela_b)
- [Vistas](#vistas)

## Relações

### Tabela_a

#### ANIMAL

Consiste numa tabela que armazena todos os dados basicos de cada animal do Zoo

#### COLUNAS 

| ANIMAL     | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------   | :------------------------ | :---------- | :---------- | :--------- | :--- |
| codAnimal  | identificador da tabela A | BIGINT      | -           | Sim        | Não  |
| peso       | Peso do animal            | SMALLINT    | -           | Não        | Não  |
| idade      | Idade do animal           | SMALLINT    | -           | Não        | Não  |
| nome       | Nome centifico            | VARCHAR(50) | -           | Não        | Não  |
| dataNasc   | Data de nascimento        | DATETIME    | now()       | Não        | Não  |
| dataObito  | Data de obito             | DATETIME    | now()       | Não        | Não  |



#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| CodAnimal |

- **Unicidade** (valores únicos)*:

| Nome        | Coluna(s) | Indexar |
| ----------- | --------- | ------- |
| nome_unique | nome      | Sim     |

- **Referêncial** (chaves estrangeiras)*:

| Nome  | Coluna(s) | Tabela referênciada | Coluna(s) referênciada(s) | Indexar |
| ----- | --------- | ------------------- | ------------------------- | ------- |
| ta_fk | tipo      | Tabela_c            | id                        | Não     |

- **Atributos** (check)*:

| Nome | Coluna(s) | condição |
| ---- | --------- | -------- |
|      |           |          |

- **Outros Indices***:

| Nome | Coluna(s) |
| ---- | --------- |
|      |           |

 

### Tabela_b

#### SETOR 

A tabela SETOR armazena os dados referentes aos habitats. Dentro destes existem áreas onde as especies vivem separadamente.

#### COLUNAS 

| SETOR    | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idSetor  | identificador da tabela B | VARCHAR(10) | -           | Sim        | Não  |
| local    | Local do setor            | VARCHAR(50) | -           | Não        | Não  |
| tema     | Tema de cada setor        | VARCHAR(50) | -           | Não        | Não  |


#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| idSetor   |



### Tabela_c

#### ESPECIE   

Armazena dados ainda mais pormenorizados acerca dos animais.

#### COLUNAS 

| ESPECIE          | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------         | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idEspecie        | identificador da tabela D | VARCHAR(109 | -           | Sim        | Não  |
| nome             | nome da especie           | BIGINT      | -           | Não        | Não  |
| quantidadeComida | quantidade da comida      | BIGINT      | -           | Não        | Não  |
| dieta            | dieta do espécie          | VARCHAR(50) | -           | Não        | Não  |
| tipo             | tipo de espécie           | VARCHAR(50) | -           | Não        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| idEspecie |

### Tabela_d

#### VACINA    

Armazena dados das vacinas administradas aos animais.

#### COLUNAS 

| VACINA   | Descrição                 | Domínio      | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :----------  | :---------- | :--------- | :--- |
| idVacina | identificador da tabela E | BIGINT       | -           | Sim        | Não  |
| nome     | nome da vacina            | VARCHART(50) | -           | Não        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| idVacina  |

### Tabela_e

#### AREA    

Armazena dados relativos à area de habitação de cada espécie.

#### COLUNAS 

| AREA            | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------        | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idArea          | identificador da tabela F | BIGINT      | -           | Sim        | Não  |
| numAnimais      | Número de animais na área | SMALLINT    | -           | Não        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| idArea    |


### Tabela_f

#### FUNCIONARIO     

Armazena dados relativos a todos os funcionários do zoo.

#### COLUNAS 

| FUNCIONARIO    | Descrição                          | Domínio     | por Omissão | Automático | Nulo |
| :-------       | :------------------------          | :---------- | :---------- | :--------- | :--- |
| CodFuncionario | identificador da tabela H          | BIGINT      | -           | Sim        | Não  |
| nome           | Nome do funcionario                | VARCHAR(50) | -           | Não        | Não  |
| CC             | CC do funcionario                  | VARCHAR(12) | -           | Não        | Não  |
| contacto       | Contacto do funcionario            | TINYINT     | -           | Não        | Não  |
| horaEntrada    | hora de entrada do funcionario     | TIME        | -           | Não        | Não  |
| horaSaida      | hora de saida do funcionario       | TIME        | -           | Não        | Não  |
| data           | data em que o funcionario trabalha | DATE        | now()       | Não        | Não  |
| funcao         | função do funcionario              | VARCHAR(50) | -           | Não        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s)      |
| ---------      |
| CodFuncionario |

### Tabela_g

#### BILHETE      

Armazena todos os dados relativos aos bilhetes vendidos pelo Zoo.

#### COLUNAS 

| BILHETE    | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------   | :------------------------ | :---------- | :---------- | :--------- | :--- |
| codBilhete | identificador da tabela J | BIGINT      | -           | Sim        | Não  |
| preco      | Preço dos bilhetes        | FLOAT       | -           | Não        | Não  |
| faixaEtaria| faixa etária dos bilhetes | VARCHAR(10) | -           | Não        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s)  |
| ---------  |
| codBilhete |

### Tabela_h

#### DESCONTO       

Armazena o valor dos descontos.

#### COLUNAS 

| DESCONTO | Descrição        | Domínio     | por Omissão | Automático | Nulo |
| :------- | :--------------- | :---------- | :---------- | :--------- | :--- |
| nome     | Nome do desconto | VARCHAR(50) | -           | Não        | Não  |
| valor    | Valor do desconto| TINYINT     | -           | Não        | Não  |

### Tabela_i

#### VISITASGRUPO    

Armazena todos os dados relativos às vistitas marcadas em grupos.

#### COLUNAS 

| VISITASGRUPO        | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------            | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idVG                | identificador da tabela L | VARCHAR(10) | -           | Sim        | Não  |
| nome                | nome do grupo             | VARCHAR(30) | -           | Não        | Não  |
| numeroParticipantes | numero de participantes   | TINYINT     | -           | Não        | Não  |
| horaEntrada         | hora de entrada do grupo  | TIME        | -           | Não        | Não  |
| horaSaida           | hora de saida do grupo    | TIME        | -           | Não        | Não  |
| data                | data da visita            | DATE        | now()       | Não        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| idVG      |


### Tabela_j

#### CLIENTE 

Descrição da Tabela M

#### COLUNAS 

| CLIENTE   | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------  | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idCliente | identificador da tabela M | BIGINT      | -           | Sim        | Não  |
| nome      | Nome do cliente           | DATE        | now()       | Não        | Não  |
| idade     | Idade do cliente          | VARCHAR(50) | -           | Não        | Não  |
| email     | Email do cliente          | TEXT        | -           | Não        | Sim  |
| CC        | CC do cliente             | BIGINT      | -           | Não        | Sim  |
| contacto  | Contacto do cliente       | BIGINT      | -           | Não        | Sim  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| idCliente |

### Tabela_k

#### FUNCAO  

Descrição da Tabela N

#### COLUNAS 

| FUNCAO | Descrição      | Domínio     | por Omissão | Automático | Nulo |
| :----  | :------------- | :---------- | :---------- | :--------- | :--- |
| nome   | nome da função | BIGINT      | -           | Sim        | Não  |


## Vistas



---
| [< Previous](rebd03.md) | [^ Main]() | [Next >](rebd05.md) |
| :---------------------- | :------------------------------------------------------: | ------------------: |

# C4 : Esquema Relacional  

- [Relações](#relações)
  - [Tabela_a](#tabela_a)
  - [Tabela_b](#tabela_b)
- [Vistas](#vistas)

## Relações

### Tabela_a

#### ANIMAL

Descrição da Tabela A

#### COLUNAS 

| ANIMAL     | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------   | :------------------------ | :---------- | :---------- | :--------- | :--- |
| codAnimal  | identificador da tabela A | BIGINT      | -           | Sim        | Não  |
| peso       | Peso do animal            | DATE        | now()       | Não        | Não  |
| idade      | Idade do animal           | VARCHAR(50) | -           | Não        | Não  |
| nome       | Nome centifico            | TEXT        | -           | Não        | Sim  |
| data       | Data de nascimento        | BIGINT      | -           | Não        | Sim  |
| data       | Data de obito             | BIGINT      | -           | Não        | Sim  |



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

Descrição da Tabela B

#### COLUNAS 

| SETOR    | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idSetor  | identificador da tabela B | BIGINT      | -           | Sim        | Não  |
| local    | Local do setor            | DATE        | now()       | Não        | Não  |
| tema     | Tema de cada setor        | VARCHAR(50) | -           | Não        | Não  |


#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| id        |

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

### Tabela_c

#### DIETA  

Descrição da Tabela B

#### COLUNAS 

| DIETA    | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| nomeDieta| identificador da tabela C | BIGINT      | -           | Sim        | Não  |

### Tabela_d

#### ESPECIE   

Descrição da Tabela

#### COLUNAS 

| ESPECIE         | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------        | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idEspecie       | identificador da tabela D | BIGINT      | -           | Sim        | Não  |
| nome            | nome da especie           | BIGINT      | -           | Sim        | Não  |
| quantidadeComida| nome da especie           | BIGINT      | -           | Sim        | Não  |

### Tabela_e

#### VACINA    

Descrição da Tabela

#### COLUNAS 

| VACINA          | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------        | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idVacina        | identificador da tabela E | BIGINT      | -           | Sim        | Não  |
| nome            | nome da vacina            | BIGINT      | -           | Sim        | Não  |

### Tabela_f

#### AREA    

Descrição da Tabela

#### COLUNAS 

| AREA            | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------        | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idArea          | identificador da tabela F | BIGINT      | -           | Sim        | Não  |
| capacidadeMax   | Capacidade maxima da area | BIGINT      | -           | Sim        | Não  |
| quantidadeComida|                           | BIGINT      | -           | Sim        | Não  |

### Tabela_g

#### TIPO     

Descrição da Tabela

#### COLUNAS 

| TIPO            | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------        | :------------------------ | :---------- | :---------- | :--------- | :--- |
| nome            | Nome do tipo de especie   | BIGINT      | -           | Sim        | Não  |

### Tabela_h

#### FUNCIONARIO     

Descrição da Tabela

#### COLUNAS 

| FUNCIONARIO   | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------      | :------------------------ | :---------- | :---------- | :--------- | :--- |
| CodFuncionario| identificador da tabela H | BIGINT      | -           | Sim        | Não  |
| nome          | Nome do funcionario       | BIGINT      | -           | Sim        | Não  |
| CC            | CC do funcionario         | BIGINT      | -           | Sim        | Não  |
| contacto      | Contacto do funcionario   | BIGINT      | -           | Sim        | Não  |

### Tabela_i

#### HORARIO     

Descrição da Tabela

#### COLUNAS 

| HORARIO    | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------   | :------------------------ | :---------- | :---------- | :--------- | :--- |
| data       | Data do evento            | BIGINT      | -           | Sim        | Não  |
| horaEntrada| Hora de entrada no        | BIGINT      | -           | Sim        | Não  |
| horaSaida  | CC do funcionario         | BIGINT      | -           | Sim        | Não  |

### Tabela_j

#### BILHETE      

Descrição da Tabela

#### COLUNAS 

| BILHETE    | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------   | :------------------------ | :---------- | :---------- | :--------- | :--- |
| codBilhete | identificador da tabela J | BIGINT      | -           | Sim        | Não  |
| preço      | Preço dos bilhetes        | BIGINT      | -           | Sim        | Não  |
| faixaEtaria|                           | BIGINT      | -           | Sim        | Não  |


## Vistas



---
| [< Previous](rebd03.md) | [^ Main]() | [Next >](rebd05.md) |
| :---------------------- | :------------------------------------------------------: | ------------------: |

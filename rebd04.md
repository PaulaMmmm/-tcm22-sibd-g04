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

Descrição da Tabela C

#### COLUNAS 

| DIETA    | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| nomeDieta| identificador da tabela C | BIGINT      | -           | Sim        | Não  |

### Tabela_d

#### ESPECIE   

Descrição da Tabela D

#### COLUNAS 

| ESPECIE         | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------        | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idEspecie       | identificador da tabela D | BIGINT      | -           | Sim        | Não  |
| nome            | nome da especie           | BIGINT      | -           | Sim        | Não  |
| quantidadeComida| nome da especie           | BIGINT      | -           | Sim        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| idEspecie |

### Tabela_e

#### VACINA    

Descrição da Tabela E

#### COLUNAS 

| VACINA          | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------        | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idVacina        | identificador da tabela E | BIGINT      | -           | Sim        | Não  |
| nome            | nome da vacina            | BIGINT      | -           | Sim        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| idVacina  |

### Tabela_f

#### AREA    

Descrição da Tabela F

#### COLUNAS 

| AREA            | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------        | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idArea          | identificador da tabela F | BIGINT      | -           | Sim        | Não  |
| capacidadeMax   | Capacidade maxima da area | BIGINT      | -           | Sim        | Não  |
| quantidadeComida|                           | BIGINT      | -           | Sim        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| idArea    |

### Tabela_g

#### TIPO     

Descrição da Tabela G

#### COLUNAS 

| TIPO            | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------        | :------------------------ | :---------- | :---------- | :--------- | :--- |
| nome            | Nome do tipo de especie   | BIGINT      | -           | Sim        | Não  |

### Tabela_h

#### FUNCIONARIO     

Descrição da Tabela H

#### COLUNAS 

| FUNCIONARIO   | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------      | :------------------------ | :---------- | :---------- | :--------- | :--- |
| CodFuncionario| identificador da tabela H | BIGINT      | -           | Sim        | Não  |
| nome          | Nome do funcionario       | BIGINT      | -           | Sim        | Não  |
| CC            | CC do funcionario         | BIGINT      | -           | Sim        | Não  |
| contacto      | Contacto do funcionario   | BIGINT      | -           | Sim        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s)      |
| ---------      |
| CodFuncionario |

### Tabela_i

#### HORARIO     

Descrição da Tabela I

#### COLUNAS 

| HORARIO    | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------   | :------------------------ | :---------- | :---------- | :--------- | :--- |
| data       | Data do evento            | BIGINT      | -           | Sim        | Não  |
| horaEntrada| Hora de entrada no        | BIGINT      | -           | Sim        | Não  |
| horaSaida  | CC do funcionario         | BIGINT      | -           | Sim        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| data      |

### Tabela_j

#### BILHETE      

Descrição da Tabela J

#### COLUNAS 

| BILHETE    | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------   | :------------------------ | :---------- | :---------- | :--------- | :--- |
| codBilhete | identificador da tabela J | BIGINT      | -           | Sim        | Não  |
| preço      | Preço dos bilhetes        | BIGINT      | -           | Sim        | Não  |
| faixaEtaria|                           | BIGINT      | -           | Sim        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s)  |
| ---------  |
| codBilhete |

### Tabela_k

#### DESCONTO       

Descrição da Tabela K

#### COLUNAS 

| DESCONTO | Descrição        | Domínio     | por Omissão | Automático | Nulo |
| :------- | :--------------- | :---------- | :---------- | :--------- | :--- |
| nome     | Nome do desconto | BIGINT      | -           | Sim        | Não  |
| valor    | Valor do desconto| BIGINT      | -           | Sim        | Não  |

### Tabela_l

#### VISITASGRUPO    

Descrição da Tabela L

#### COLUNAS 

| VISITASGRUPO | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------     | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idVG         | identificador da tabela L | BIGINT      | -           | Sim        | Não  |
| nome         | nome do grupo             | BIGINT      | -           | Sim        | Não  |
| numero       | numero de participantes   | BIGINT      | -           | Sim        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| idVG      |

### Tabela_m

#### HORARIOVISITASGRUPO     

Descrição da Tabela M

#### COLUNAS 

| HORARIOVISITASGRUPO  | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------             | :------------------------ | :---------- | :---------- | :--------- | :--- |
| data                 | identificador da tabela M | BIGINT      | -           | Sim        | Não  |
| hora                 | Hora de entrada           | BIGINT      | -           | Sim        | Não  |
| hora                 | Hora de saida             | BIGINT      | -           | Sim        | Não  |

### Tabela_n

#### CLIENTE 

Descrição da Tabela N

#### COLUNAS 

| CLIENTE   | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------  | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idCliente | identificador da tabela N | BIGINT      | -           | Sim        | Não  |
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

### Tabela_o

#### FUNCAO  

Descrição da Tabela O

#### COLUNAS 

| FUNCAO | Descrição      | Domínio     | por Omissão | Automático | Nulo |
| :----  | :------------- | :---------- | :---------- | :--------- | :--- |
| nome   | nome da função | BIGINT      | -           | Sim        | Não  |


## Vistas



---
| [< Previous](rebd03.md) | [^ Main]() | [Next >](rebd05.md) |
| :---------------------- | :------------------------------------------------------: | ------------------: |

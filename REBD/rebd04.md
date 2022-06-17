# C4 : Esquema Relacional  

- [Relações](#relações)
  - [ANIMAL](#ANIMAL)
  - [SETOR](#SETOR)
  - [ESPECIE](#ESPECIE)
  - [VACINA](#VACINA)
  - [AREA](#AREA)
  - [FUNCIONARIO](#FUNCIONARIO)
  - [BILHETE](#BILHETE)
  - [DESCONTO](#DESCONTO)
  - [VISITASGRUPO](#VISITASGRUPO)
  - [CLIENTE](#CLIENTE)
  - [APADRINHA](#APADRINHA)
 

## Relações

### ANIMAL

Consiste numa tabela que armazena todos os dados basicos de cada animal do Zoo

#### COLUNAS 

| ANIMAL     | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------   | :------------------------ | :---------- | :---------- | :--------- | :--- |
| codAnimal  | identificador da tabela A | CHAR(10)    | -           | Sim        | Não  |
| peso       | Peso do animal            | DECIMAL     | -           | Não        | Não  |
| idade      | Idade do animal           | SMALLINT    | -           | Não        | Não  |
| nome       | Nome centifico            | VARCHAR(50) | -           | Não        | Não  |
| dataNasc   | Data de nascimento        | DATETIME    | now()       | Não        | Não  |
| dataObito  | Data de obito             | DATETIME    | -           | Não        | Não  |



#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| CodAnimal |



- **Referêncial** (chaves estrangeiras)*:

| Nome      | Coluna(s) | Tabela referênciada | Coluna(s) referênciada(s) | Indexar |
| -----     | --------- | ------------------- | ------------------------- | ------- |
| idCliente |           | CLIENTE             | codAnimal                 | Não     |




### SETOR 

A tabela SETOR armazena os dados referentes aos habitats. Dentro destes existem áreas onde as especies vivem separadamente.

#### COLUNAS 

| SETOR    | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idSetor  | identificador da tabela B | CHAR(10)    | -           | Sim        | Não  |
| local    | Local do setor            | VARCHAR(50) | -           | Não        | Não  |
| tema     | Tema de cada setor        | VARCHAR(50) | -           | Não        | Não  |


#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| idSetor   |



- **Referêncial** (chaves estrangeiras)*:

| Nome      | Coluna(s) | Tabela referênciada | Coluna(s) referênciada(s) | Indexar |
| -----     | --------- | ------------------- | ------------------------- | ------- |
| idArea    |           | AREA                | idSetor                   | ?       |



### ESPECIE   

Armazena dados ainda mais pormenorizados acerca dos animais.

#### COLUNAS 

| ESPECIE          | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------         | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idEspecie        | identificador da tabela C | CHAR(10)    | -           | Sim        | Não  |
| nome             | nome da especie           | VARCHAR(20) | -           | Não        | Não  |
| quantidadeComida | quantidade da comida      | INT         | -           | Não        | Não  |
| dieta            | dieta do espécie          | VARCHAR(20) | -           | Não        | Não  |
| tipo             | tipo de espécie           | VARCHAR(20) | -           | Não        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| idEspecie |




- **Referêncial** (chaves estrangeiras)*:

| Nome      | Coluna(s) | Tabela referênciada | Coluna(s) referênciada(s) | Indexar |
| -----     | --------- | ------------------- | ------------------------- | ------- |
| codAnimal | ?         | ANIMAL              | idEspecie                 | Sim     |




### VACINA    

Armazena dados das vacinas administradas aos animais.

#### COLUNAS 

| VACINA   | Descrição                 | Domínio      | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :----------  | :---------- | :--------- | :--- |
| idVac    | identificador da tabela D | CHAR(10)     | -           | Sim        | Não  |
| nomeVac  | nome da vacina            | VARCHART(50) | -           | Não        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| idVa      |



- **Referêncial** (chaves estrangeiras)*:

| Nome       | Coluna(s) | Tabela referênciada | Coluna(s) referênciada(s) | Indexar |
| -----      | --------- | ------------------- | ------------------------- | ------- |
| codAnimal  | ?         | ANIMAL              | idVac                     | Não     |





### AREA    

Armazena dados relativos à area de habitação de cada espécie.

#### COLUNAS 

| AREA            | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------        | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idArea          | identificador da tabela E | CHAR(10)    | -           | Sim        | Não  |
| numAnimais      | Número de animais na área | SMALLINT    | -           | Não        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| idArea    |


- **Referêncial** (chaves estrangeiras)*:

| Nome       | Coluna(s) | Tabela referênciada | Coluna(s) referênciada(s) | Indexar |
| -----      | --------- | ------------------- | ------------------------- | ------- |
| idEspecie  | ?         | ESPECIE             | idArea                    | Não     |






### FUNCIONARIO     

Armazena dados relativos a todos os funcionários do zoo.

#### COLUNAS 

| FUNCIONARIO    | Descrição                          | Domínio     | por Omissão | Automático | Nulo |
| :-------       | :------------------------          | :---------- | :---------- | :--------- | :--- |
| codFuncionario | identificador da tabela F          | CHAR(10)    | -           | Sim        | Não  |
| nome           | Nome do funcionario                | VARCHAR(50) | -           | Não        | Não  |
| cc             | CC do funcionario                  | CHAR(12)    | -           | Não        | Não  |
| contacto       | Contacto do funcionario            | CHAR(9)     | -           | Não        | Não  |
| horaEntrada    | hora de entrada do funcionario     | TIME        | -           | Não        | Não  |
| horaSaida      | hora de saida do funcionario       | TIME        | -           | Não        | Não  |
| data           | data em que o funcionario trabalha | DATE        | now()       | Não        | Não  |
| funcao         | função do funcionario              | VARCHAR(50) | -           | Não        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s)      |
| ---------      |
| codFuncionario |





### BILHETE      

Armazena todos os dados relativos aos bilhetes vendidos pelo Zoo.

#### COLUNAS 

| BILHETE    | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------   | :------------------------ | :---------- | :---------- | :--------- | :--- |
| codBilhete | identificador da tabela G | CHAR(15)    | -           | Sim        | Não  |
| preco      | Preço dos bilhetes        | FLOAT       | -           | Não        | Não  |
| faixaEtaria| faixa etária dos bilhetes | VARCHAR(10) | -           | Não        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s)  |
| ---------  |
| codBilhete |


- **Referêncial** (chaves estrangeiras)*:

| Nome       | Coluna(s) | Tabela referênciada | Coluna(s) referênciada(s) | Indexar |
| -----      | --------- | ------------------- | ------------------------- | ------- |
| idCliente  | ?         | CLIENTE             | codBilhete                | Não     |





### DESCONTO       

Armazena o valor dos descontos.

#### COLUNAS 

| DESCONTO     | Descrição        | Domínio     | por Omissão | Automático | Nulo |
| :-------     | :--------------- | :---------- | :---------- | :--------- | :--- |
| nomeDesconto | Nome do desconto | VARCHAR(50) | -           | Não        | Não  |
| valor        | Valor do desconto| TINYINT     | -           | Não        | Não  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s)    |
| ---------    |
| nomeDesconto |



- **Referêncial** (chaves estrangeiras)*:

| Nome       | Coluna(s) | Tabela referênciada | Coluna(s) referênciada(s) | Indexar |
| -----      | --------- | ------------------- | ------------------------- | ------- |
| codBilhete | ?         | BILHETE             | nomeDesconto              | Não     |





### VISITASGRUPO    

Armazena todos os dados relativos às visitas marcadas em grupos.

#### COLUNAS 

| VISITASGRUPO        | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------            | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idVG                | identificador da tabela I | CHAR(10)    | -           | Sim        | Não  |
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



- **Referêncial** (chaves estrangeiras)*:

| Nome      | Coluna(s) | Tabela referênciada | Coluna(s) referênciada(s) | Indexar |
| -----     | --------- | ------------------- | ------------------------- | ------- |
| idCliente | ?         | CLIENTE             | idVG                      | Não     |






### CLIENTE 

Armazena dados relativos aos clientes (visitantes ou padrinhos)

#### COLUNAS 

| CLIENTE   | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :-------  | :------------------------ | :---------- | :---------- | :--------- | :--- |
| idCliente | identificador da tabela J | CHAR(10)    | -           | Sim        | Não  |
| nome      | Nome do cliente           | VARCHAR(50) | -           | Não        | Não  |
| idade     | Idade do cliente          | TINYINT     | now()       | Não        | Não  |
| email     | Email do cliente          | VARCHAR(50) | -           | Não        | Sim  |
| cc        | CC do cliente             | CHAR(12)    | -           | Não        | Não  |
| contacto  | Contacto do cliente       | CHAR(9)     | -           | Não        | Sim  |

#### RESTRIÇÕES DE INTEGRIDADE 

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| idCliente |

- **Unicidade** (valores únicos)*:

| Nome             | Coluna(s) | Indexar |
| ---------------- | --------- | ------- |
| cc_unique        | cc        | Sim     |



### APADRINHA 

A tabela APADRINHA armazena o valor com que o cliente contribui para ajudar o animal escolhido.

#### COLUNAS 

| APADRINHA  | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :--------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| valor      | valor a contribuir        | FLOAT       | -           | Não        | Sim  |


- **Chave Primária**: 

| Coluna(s) |
| --------- |
| idCliente |
| codAnimal |


- **Referêncial** (chaves estrangeiras)*:

| Nome      | Coluna(s) | Tabela referênciada | Coluna(s) referênciada(s) | Indexar |
| -----     | --------- | ------------------- | ------------------------- | ------- |
| idCliente | ?         | CLIENTE             | idVG                      | Não     |
| codAnimal | ?         | ANIMAL              | idVac                     | Não     |


---
| [< Previous](rebd03.md) | [^ Main](https://github.com/PaulaMmmm/-tcm22-sibd-g04/tree/main/REBD) | [Next >](rebd05.md) |
| :---------------------- | :------------------------------------------------------: | ------------------: |


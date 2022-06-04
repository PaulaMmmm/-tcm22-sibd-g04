# C3 : Normalização

## Relações

Supervisiona (FUNCIONARIO, FUNCIONARIO)

Regista (FUNCIONARIO, ANIMAL)

Toma (VACINA, ANIMAL)

Possui (ANIMAL, ESPECIE)

Habita (ESPECIE, AREA)

Contem (AREA, SETOR)

Apadrinha (ANIMAL, CLIENTE)

Compra (CLIENTE, BILHETE)

Tem (BILHETE, DESCONTO)

Responsável (CLIENTE, VISITASGRUPO)


## Normalização do Esquema Relacional

ANIMAL (#idCliente  CLIENTE, codAnimal, peso, idade, nomeCientifico, dataObito, dataNasc)

1NF

Já se encontra na 1NF

2NF

Já se encontra na 2NF

3NF

Já se encontra na 3NF

---

SETOR (#idArea  AREA, idSetor, local, tema) 

1NF
Já se encontra na 1NF

2NF

Já se encontra na 2NF

3NF

Já se encontra na 3NF

---

ESPECIE (#codAnimal  ANIMAL, idEspecie, nomeEspecie, quantidadeComida, dieta, tipo) 

1NF

Já se encontra na 1NF

2NF

Já se encontra na 2NF

3NF

Já se encontra na 3NF

---

VACINA (#codAnimal  ANIMAL, nomeVac, idVac) 

1NF

Já se encontra na 1NF

2NF

VACINA (nomeVac, idVac)

VACINAANIMAL (#codAnimal  ANIMAL, # idVac  VACINA)

3NF

Já se encontra na 3NF

---

AREA (#idEspecie  ESPECIE, idArea, capacidadeMax) 

1NF

Já se encontra na 1NF

2NF

Já se encontra na 2NF

3NF

Já se encontra na 3NF

---

FUNCIONARIO (nomeFuncionario, codFuncionario, CC, contacto, horaEntrada, horaSaida, data, funcao) 

1NF

Já se encontra na 1NF

2NF

Já se encontra na 2NF

3NF

Já se encontra na 3NF

---

BILHETE (#idCliente  CLIENTE, codBilhete, preco, faixaEtaria)

1NF

Já se encontra na 1NF

2NF

Já se encontra na 2NF

3NF

Já se encontra na 3NF

---

DESCONTO (#codBilhete  BILHETE, nomeDesconto, valor) 

1NF

Já se encontra na 1NF

2NF

Já se encontra na 2NF

3NF

Já se encontra na 3NF

---

VISITASGRUPO (#idCliente  CLIENTE, idVG, nomeGrupo, numeroParticipantes, data, horaEntrada, horaSaida) 

1NF

Já se encontra na 1NF

2NF

Já se encontra na 2NF

3NF

Já se encontra na 3NF

---

CLIENTE (nomeCliente, idCliente, idade, email, CC, contacto)

1NF

Já se encontra na 1NF

2NF

Já se encontra na 2NF

3NF

Já se encontra na 3NF



---
[< Previous](rebd02.md) | [^ Main]() | [Next >](rebd04.md)
:--- | :---: | ---: 


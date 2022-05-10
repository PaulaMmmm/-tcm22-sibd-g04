# C3 : Esquema conceptual

## Modelo E/A
_(Introduzir as entidade-tipo e associações do sistema, adicionalmente apresentar o diagrama do modelo Entidade-Associação.)_

Exemplo de inserção de uma imagem:   
![An alternative description](images/image02.png)   

CLIENTE: O Zoo armazena os seguintes atributos dos clientes: nome, idade, email, CC. 

podeFazer: O cliente pode estar associado à entidade APADRINHAMENTO. Apesar de ser necessário um ou mais clientes para um apadrinhamento existir, os clientes não necessitam obrigatoriamente de apadrinhar um animal.

APADRINHAMENTO: Os dados que a base de dados do Zoológico necessita de recolher de forma a ser efetuado um apadrinhamento são a morada do cliente, o telefone, o animal a apadrinhar e o valor a contribuir.

financia: O APADRINHAMENTO permite financiar algumas despesas do animal. Cada animal pode ter um ou mais apadrinhamentos e por sua vez cada apadrinhamento apenas financia um animal. Porém nem todos os animais são apadrinhados. 

ANIMAL: Cada animal é identificado pelo ID, peso, idade, nome científico, nome popular, data de óbito, vacinações e a sua data de nascimento, sendo estes os seus atributos.

tem: Cada animal tem obrigatoriamente necessidades especificas. 

NECESSIDADE: De forma a controlar as necessidades de cada animal, a entidade NECESSIDADE tem os seguintes atributos: o tipo de dieta, a quantidade de comida, a luminosidade necessária, a humidade necessária, a vegetação necessária e área de habitação.

controla: As necessidades dos animais têm de ser controladas pelos funcionários do zoo. As várias necessidades podem ser controladas por vários funcionários. 

FUNCIONARIO: O zoo é composto por vários funcionários cujos atributos são o nome, cartão de cidadão, função, contacto e horário de trabalho. Os voluntários são também considerados funcionários no zoo. 

supervisiona: Esta associação serve para os voluntários, que serão supervisionados por um funcionário do zoo. Por sua vez, o supervisor pode supervisionar vários voluntários. 

cuida: São os funcionários que cuidam dos animais. Vários funcionários podem cuidar de um ou mais animais. 

habita: Cada animal tem de ser alojado numa moradia, podendo morar um ou mais animais da mesma espécie na mesma moradia. 

MORADIA: A moradia é o espaço onde os animais habitam. Cada moradia é distinguida pela capacidade máxima de animais e a espécie que lá mora.

contem:  As moradias estão contidas em diferentes setores do zoo para uma melhor organização do mesmo. Estas existem obrigatoriamente dentro de um setor. Um setor pode conter várias moradias, porém cada moradia só pode pertencer a um setor.


## Regras de negócio adicionais (Restrições)


---
[< Previous](rei02.md) | [^ Main](https://github.com/exemploTrabalho/reportSIBD/) | Next >
:--- | :---: | ---: 

# C1 : Introdução


## Descrição do trabalho
A problemática que o grupo pretende resolver é a gestão da totalidade dos dados de um Zoológico, desde os animais que lá residem, os clientes que visitam o Zoo, até aos funcionários que trabalham lá. Existem vários tipos de animais: aves, mamíferos, repteis e anfíbios. Todos estes animais serão identificados pelo código, peso, idade, nome científico, nome popular e alimentação.  

Os animais do Zoo precisam de habitats específicos de forma a viverem uma vida saudável e feliz. Por isso, existem vários setores que são identificados pelo código de identificação e localização. Estes setores são caracterizados, pela diferença de temas, como por exemplo, a savana, a floresta tropical, a tundra, o deserto e a montanha. Em cada sector existem várias áreas de moradia para animais. Cada animal reside numa área onde podem morar vários animais da mesma espécie, tendo em conta a capacidade máxima de animais. Porém, nem todas as espécies de animais podem coabitar num mesmo setor.

Cada animal, dependendo da sua espécie, tem necessidades especificas como o tipo de dieta (carnívoro, herbívoro, omnívoro, insetívoro, piscívoro), quantidade de comida e área de habitação (m^2). Quem controla as necessidades são os funcionários do Zoo, logo são estes quem têm permissão para alterar, remover ou acrescentar esses dados. Estes são distinguidos pelo nome, cartão de cidadão, função, contacto, horário. É também permitido aos funcionários acrescentar ou alterar informações, tais como adicionar data de óbito, vacinações, datas de nascimento. Porém apenas o gerente pode acrescentar animais (oriundos de outros zoos).

Para além dos funcionários, também trabalham no Zoo voluntários, que são acompanhados por um supervisor, de forma a que tenham ajuda nas suas tarefas.

De forma a haver um controlo sob as visitas efetuadas ao Zoo, pretende-se armazenar os dados dos clientes (nome, idade, email, cartão de cidadão). Relativamente aos bilhetes, o preço destes varia consoante a faixa etária dos clientes (sénior, criança, adulto) e que tipo de bilhete é (apenas visita, bilhete para eventos, visita de grupo) e se o cliente beneficia de algum desconto (bilhete familiar ou bilhete estudante). Se o cliente pretender participar em alguns dos eventos que decorrem no Zoológico como a “Demonstração de Voo Livre”, a “Alimentação dos pinguins”, “Show dos suricatas”, etc., terá de pagar um valor acrescentado. Estes eventos ocorrem em horários e datas especificas.  Empresas, instituições e escolas podem realizar visitas de grupo, sendo importante saber o nome do grupo, nome do responsável, email, contacto telefónico, número de participantes, data em que pretendem efetuar a visita e hora de chegada.

Colocamos à disposição de particulares ou empresas a possibilidade de apadrinhar um animal e desta forma contribuir com os cuidados necessários para o bem-estar dessa ou dessas espécies. Para tal, é necessário apontar o nome, email, morada, telefone, animal a apadrinhar e valor com que quer contribuir.

## Modelação do problema

ANIMAL (ID, peso, idade, nomeCientifico, nomePopular, dataObito, vacinacoes, dataNasc, especie)

NECESSIDADE (tipoDieta, quantidadeComida, areaHab)

SETOR (codID, local, tema)

MORADIA (capacidadeMax, especie)

FUNCIONARIOS (nome, CC, funcao, contacto, horario)

BILHETE (codigo, preco, faixaEtaria, desconto)

EVENTOS (tipo, horario, data)

VISITASGRUPO (nomeGrupo, nomeResponsavel, email, contactoTelefonico, numeroParticipantes, Data, horaChegada)

APADRINHAMENTO (morada, telefone, ID, valorContribuicao)

CLIENTE (nome, idade, email, CC)

VISITA (hora, data)


---
[< Previous](rei00.md) | [^ Main](https://github.com/PaulaMmmm/-tcm22-sibd-g04/tree/main) | [Next >](rei02.md)
:--- | :---: | ---: 

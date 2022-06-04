# C1 : Introdução


## Descrição do trabalho

O trabalho consiste na especificação e desenvolvimento de um sistema relacionado com o tema de um zoológico. A problemática que o grupo pretende resolver é a gestão da totalidade dos dados de um Zoológico, desde os animais que lá residem, os clientes que visitam o Zoo, até aos funcionários que trabalham lá. Existem vários tipos de animais: aves, mamíferos, repteis e anfíbios. Todos estes animais serão identificados pelo código, peso, idade, nome científico, data de nascimento e data de óbito. Os animais também apresentam diferentes características como a espécie (que necessita de diferentes porções de alimento e dieta) e vacina. Estes precisam de habitats específicos de forma a viverem uma vida saudável e feliz. Por isso, existem vários setores que são identificados pelo ID do setor e localização. Estes setores são caracterizados pela diferença de temas, como por exemplo, a savana, a floresta tropical, a tundra, o deserto e a montanha. Em cada setor existem várias áreas. Cada animal reside numa área onde podem morar vários animais da mesma espécie, tendo em conta a capacidade máxima de animais. Porém, nem todas as espécies de animais podem coabitar num mesmo setor.

Quem controla as necessidades são os funcionários do Zoo, logo são estes quem têm permissão para alterar, remover ou acrescentar esses dados. Estes são distinguidos pelo nome, código de funcionário, cartão de cidadão, contacto e função. É também permitido aos funcionários acrescentar ou alterar informações, tais como adicionar data de óbito, vacinações, datas de nascimento. Porém apenas o gerente pode acrescentar animais (oriundos de outros zoos).

Para além dos funcionários habituais, também trabalham no Zoo voluntários, que são acompanhados por um supervisor, de forma a terem ajuda nas suas tarefas.

Todos estes funcionários (sejam voluntários ou não) possuem um horário fixo, com uma hora de entrada, uma hora de saída e uma data. 
De forma a haver um controlo sob as visitas efetuadas ao Zoo, pretende-se armazenar os dados dos clientes (nome, ID de cliente, idade, email, cartão de cidadão e contacto). Relativamente aos bilhetes, são identificados graças ao ID do cliente e código do bilhete, e tem também um preço e uma faixa etária (sénior, criança, adulto), que poderá trazer descontos para os visitantes. Os descontos são verificados com a ajuda do atributo código de funcionário. O cliente pode realizar visitas de grupo (caso o responsável faça parte de uma empresa, escola ou associação), sendo importante saber o nome do grupo e o número de participantes. Estas visitas tem um horário com a data, hora de entrada e hora de saída.

Colocamos à disposição dos clientes de apadrinhar um animal e desta forma contribuir com os cuidados necessários para o bem-estar dessa ou dessas espécies. 

## Descrição dos requisitos do utilizador

O gerente tem acesso a toda a base de dados, podendo alterá-la.

Existem vários tipos de funcionários no zoo. Existem os tratadores que cuidam das necessidades dos animais, gerem as suas informações e podem acrescentar (caso nasçam) ou retirar (caso morram) animais da base de dados. Os voluntários também são considerados funcionários (podem ser tratadores ou secretários), a sua única diferença é que são supervisionados por um superior (supervisor). Os secretários gerem todas as informações relativas aos clientes. Os veterinários estão encarregues de vacinar os animais. Os funcionários de limpeza tratam de higienizar o espaço público. 

Supervisores podem alterar informações relativas aos voluntários, visto que são responsáveis por estes.

Os animais são o foco principal do Zoo. Todos têm requisitos que devem ser cumpridos pelos funcionários do zoo.

Os clientes são os visitantes do zoo. Podem comprar três tipos distintos de bilhetes e podem apadrinhar um ou vários animais do zoo.


---
[< Previous](rebd00.md) | [^ Main]() | [Next >](rebd02.md)
:--- | :---: | ---: 

RCOMP 2023-2024 Project - Sprint 1 
===========================================

## 1. Considerações gerais

Na realização deste projeto, tentei ao máximo seguir todas as normas e pôr em prática todos os conhecimentos da cablagem estruturada lecionados. Em alguns casos específicos, não segui as normas devido a especificações no enunciado.

## 2. Cablagem estruturada

### 2.1 Outlets

Todas as outlets respeitam as normas da cablagem estruturada (exceto exceções indicadas pelo cliente).
- São colocadas a uma distância máxima de 3m das outlets vizinhas.
- A quantidade em cada sala são duas por cada 10 metros quadrados.

#### 2.1.1 Exceções às normas

- No piso 0:
  - Quartos 3.0.1, 3.0.2, 3.0.3 tinham a especificação de terem apenas 2 outlets.
  - Quarto 3.0.14 tinha especificação de ter 0 outlets por se tratar de uma sala de arrumos.
- No piso 1:
  - Quarto 3.1.8 tinha a especificação de ter 0 outlets.

Nota: Arredondei o número de outlets por metro quadrado sempre para cima, exceto na sala 3.1.1.
![img_5.png](img_5.png)
![img_6.png](img_6.png)

As outlets escolhidas apresentam entrada fêmea RJ45. Coloquei todas ao nível do rodapé. No caso do piso 1 também se encontram ao nível do rodapé, mas uma vez que a cablagem vem do teto as conexões individuais de cada outlet encontram-se consolidadas num canto de cada sala apenas.

### 2.2 Intermediate e Horizontal cross-connect

É expresso no enunciado que deve ser realizada a colocação de um IC por edifício, e um HC por piso no edifício. Ambos foram colocados na sala indicada pelo cliente, que representa a sala de arrumos.

### 2.2.1 Intermediate cross connect
Para o  IC escolhi um network switch de 24 entradas. As entradas extras servião caso seja necessário mais conexões.

### 2.2.2 Horizontal cross connect
Tanto no piso 0 como no piso 1 o HC é composto por um network switch de 24 entradas RJ45.

### 2.3 Consolidation points

Na colocação dos CP's tentei fazer uma distribuição equitativa por piso de modo a reduzir a cablagem que atravessa as paredes. Ao mesmo tempo, tentei que cada CP tivesse mais ou menos o mesmo número de entradas a serem usadas (aproximadamente 20). 

### 2.4 Access points

Para poder obter rede Wi-Fi em todos os andares, decidi implementar cerca de 4 access points em cada piso que, individualmente, cobrem 50 metros. A sua distribuição foi feita de maneira a garantir uma cobertura de Wi-Fi consistente em todo o edifício.
Optei por routers de 4 entradas RJ45.

### 2.5 Cablagem horizontal

Seguindo as diretrizes da cablagem estruturada, optei por utilizar cabos de cobre CAT7 para a cablagem horizontal do edifício. O CAT7 foi escolhido devido à sua capacidade de oferecer uma taxa de transferência de dados de até 10 Gb/s e sua construção com quatro pares trançados, protegidos por um escudo externo para reduzir interferências externas. Toda a cablagem do edifício respeita as normas da cablagem estruturada.

### 2.6 Fibra Ótica

Utilizei fibra óptica para fazer a ligação entre o Main connect (no edifício 1) e os Intermediate e Horizontal cross-connect do meu edificio, sendo a fibra do tipo multi-modo.

### 2.7 Telecommunications enclosure

Como consta nas normas utilizei um enclosure de 6U. Este enclosure abriga tanto o IC como o HC no piso 0, o HC no piso 1, como também todas as cps utilizadas de maneira a deixa-las mais protegidas. O enclosure deixa algum espaço para a expansão de mais racks caso seja necessário, obedecendo assim aos conselhos da cablagem estruturada.




## **STRUCTURED CABLING SCHEMATIC PLAN** ##

### FLOOR 0 ###

![img_7.png](img_7.png)

### FLOOR 1 ###

![img_8.png](img_8.png)

## **INVENTORY ** ##


## **Cabos tamanho** ##

### ***Floor 0:*** ###

**Comprimento total de cabo:** 3.96 + 15.81 + 18.37 + 38.75 + 67.35 + 78,25 + 492.4 + 284.6 = 1259.94m

***Cabo de Fibra:*** 59,5m


### ***Floor 1*** ###

**Comprimento total de cabo:** 56 + 18.9 + 19.9 + 22,73 + 22,73 + 109.2 + 1355 = 1604.46m


--------------------------------------------------------------------------------------------------------------------





## **INVENTORY TOTALS** ##

|  FLOOR  | Nº Outlets | Copper Cable (m) | Fiber Cable(m) | Telecommunication Enclosures (6U) | AP |  CP   | HCC | ICC | Switches   | Patch Panels | 
|:-------:|:----------:|:----------------:|:--------------:|:---------------------------------:|:---:|:-----:|:----|-----|------------|--------------|
| Floor 0 |     76     |     1259.94      |      59,5      |                 6                 |  4 | 5     | 1   | 1   | 2(24ports) | 2(48ports)   |
| Floor 1 |     80     |     1604.46      |       0        |                 7                 |  4 |   6   | 1   | 0   | 1(24ports) | 2(48ports)   |
|  Total  |    156     |     2835.16      |      59,5      |                13                 |  8 |  11   | 2   | 1   | 3          | 4            |

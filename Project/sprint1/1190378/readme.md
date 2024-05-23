# Cablagem para o edífico 2
## 0. Organização do relatório

- Ponto 1: Algumas considerações gerais que se aplicam ao edifício todo.

- Ponto 2: Explicação de como a cablagem estruturada foi aplicada neste edifício.

- Ponto 3: Equipamento usado, também com considerações sobre a cablagem estruturada.

- Ponto 4: Imagens dos pisos com cablagem estruturada. (NOTA: nas imagens os cabos encontram-se muito pequenos, aconselho a fazer zoom para visualizar melhor.)

- Ponto 5: Tabelas excel com cálculos relevantes.
## 1. Considerações gerais
Toda a cablagem estruturada do edifício foi realizada respeitando as normas da mesma. Os casos que não obedecem à cablagem estruturada, seja por especificação do cliente, ou por outros motivos justificáveis, são indicados neste relatório. A cablagem estruturada do edíficio inclui a distribuição do equipamento pelo mesmo, assim como o próprio equipamento usado. Todas essas considerações são apresentadas nos pontos abaixo.

É de notar que os cálculos apresentados na secção 5 apresentam uma margem de erro que é indicada nas próprias tabelas excel.

## 2. Cablagem estruturada

### 2.1 Outlets

Todas as outlets respeitam as normas da cablagem estrutrada (exceto onde indicado pelo cliente): apresentam entradas fêmea RJ45; são colocadas a uma distância máxima de 3m das outlets vizinhas; a quantidade em cada sala são duas por cada 10 metros quadrados; contêm um patch cord de cerca de 3m cada uma. 

As outlets foram todas colocadas ao nível do rodapé visto que parece o mais justificável para ligar potênciais utilizadores, e também permite poupar algum cabo no piso 0.

Indico de seguida algumas exceções a estas normas que foram apresentadas pelo cliente.

#### 2.1.1 Exceções às normas
No piso 0:
- Sala 2.0.6 e 2.0.7 indicação do cliente que devem apenas conter 5 outlets distribuídas do mesmo lado da linha subterrânea de cablagem.
- Sala 2.0.11, que é um armazém e não tem outlets.
- Sala 2.0.12, que é o data center e também não tem outlets.

No piso 1:
- Sala 2.1.12, apenas esta não tem outlets dado que é o data center.

Nota: Tentei arredondar o número de outlets por metro quadrado sempre para baixo. Isto é, se existiu, por exemplo, uma área de 25 metros quadrados optei na mesma por colocar apenas 4 outlets. Esta decisão tem a ver com o facto de no edifício se utilizar mais a tecnologia Wifi do que ethernet pelo que a outlet extra não fará grande diferença.

### 2.2 Intermediate e Horizontal cross-connect

É expresso no enunciado que deve ser realizada a colocação de um IC por edifício, e um HC por piso no edifício. Ambos foram colocados na sala indicada pelo cliente, que representa o data center, tal como as normas de cablagem estruturada indicam.

A área total abrangida pelos HC's também respeita a norma de menos de mil metros quadrados.

### 2.3 Consolidation points
Na colocação dos CP's tentei fazer uma distribuição equitativa por piso de modo a reduzir a cablagem que atravessa as paredes. Ao mesmo tempo, tentei que cada CP tivesse mais ou menos o mesmo número de entradas a serem usadas (apróximadamente 20).

### 2.4 Access points
Tentei colocar os access points próximos de cada CP de modo a reduzir o comprimento de cabo utilizado. É claro que não foi uma colocação cega pelo que também tentei minimizar as interferências com o meio físico, e fornecer bom alcançe para o número de conexões necessárias. Daí tanto os CP's como access points encontrarem-se dentro de salas.

Ao mesmo tempo certifiquei-me que existia um número aceitável de access points por piso de modo a não ultrapassar 25-30 utilizadores, tal como indicado nas normas de cablagem estruturada.

### 2.5  Cablagem horizontal
Tal como indicado pelas normas da cablagem estruturada, o material usado para a cablagem horizontal foi o cobre. O tipo de cabo usado foi o CAT7. Esta é a melhor escolha apontada pela cablagem estruturada. O cabo é composto por quatro pares trança com um escudo exterior que permite ainda mais a redução de interferência exterior. Optei também por CAT7 ao invés de CAT6 porque permite uma maior taxa de transferência de dados (10gb/s).

Os cabos CAT7 apresentam conectores RJ45 tal como constatado nos documentos ISO.

Toda a cablagem do edifício respeita as normas da cablagem estruturada, nomeadamente, que a distância máxima de um cabo é 90m; e que a distância máxima vertical entre um outlet e o HC é de 80m; cabos que conectam o HC ao IC devem ter no máximo 500m; o número de cabos que entram qualquer patch panel, nomeadamente os switches, deve ser menor que 200.

Em cada outlet é fornecido um patch cord the 3m de comprimento, respeitando a norma apontada acima.

## 3. Equipamento
### 3.1 Outlets
As outlets escolhidas apresentam entrada fêmea RJ45. Coloquei todas ao nível do rodapé. No caso do piso 1 também se encontram ao nível do rodapé, mas uma vez que a cablagem vem do teto as conexões individuais de cada outlet encontram-se consolidadas num canto de cada sala apenas. Isto permite uma melhor organização de cabos e também é mais apelativo esteticamente na própria sala. Todas estas notas são condsideradas no cálculo da cablagem que se encontra na secção das tabelas.
### 3.2 Telecommunications enclosure
Como consta nas normas utilizei um enclosure com espaco para racks de 19 polegadas. Este enclosure abriga tanto o IC como o HC no piso 0, e apenas o HC no piso 1. O enclosure deixa também algum espaço para a expansão de mais racks caso seja necessãrio obedecendo assim aos conselhos da cablagem estruturada.
### 3.3 Intermediate cross connect
Para o  IC escolhi um network switch de 24 entradas RJ45 e 4 fibra ótica. É também incluido um patch panel com as mesmas entradas. Considerei este número de entradas suficientes porque à partida existirão dois inputs do exterior, uma vez que a cablagem tem de ser redundante. As entradas extras servião caso se expanda o campus com outros MC's sendo necessário então mais conexões.

### 3.4 Horizontal cross connect

### 3.5 Consolidation points
Tanto no piso 0 como no piso 1 o HC é composto por um patch panel de 24 entradas RJ45 e 2 para fibra ótica de 19 polegadas. O patch panel é conectado ao switch por meio de cords de 0.5m. Considirei este número suficiente porque não existem muitas outlets diretamente conectadas ao patch panel. A cablagem foi drasticamente reduzida pelo o uso distribuido de CP's por cada piso.
Dada uma abundância média de 20 conexões em cada CP (contando com os access poitns) optei por usar um patch panel  de 24 entradas RJ45. Este cálculo foi aplicado aos dois pisos pelo que ambos utilizam o mesmo switch para CP. A única exceção encontra-se no CP1 do piso 1 (ver figura). Aqui optei por um switch de 30 entradas dado que foi necessário consolidar mais conexões.

### 3.6 Access points
Os access points à partida só terão a conexão proveniente do CP pelo que optei por routers de 4 entradas RJ45.

## 4. Imagens
### LEGENDA
- Linha tracejada laranja: Cabo CAT7 subterrâneo ou pelo teto no caso do piso 1.
- Linha contínua laranja: Cabo CAT7 exterior.
- Linha tracejada rosa: Cabo fibra ótica subterrâneo ou pelo teto no caso do piso 1.
- Linha contínua rosa: Cabo fibra ótica exterior.
### 4.1 Piso 0
![Piso0](piso0.png)
### 4.2 Piso 1
![Piso1](piso1.png)

## 5. Tabelas com cálculos
### 5.1 Piso 0
![Tabela0](piso0-tabela.png)
### 5.1 Piso 1
![Tabela0](piso1-tabela.png)
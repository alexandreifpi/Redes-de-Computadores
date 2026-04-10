# Endereçamento IP

## Protocolo IP

- Protocolo da **Camada de Rede** do modelo TCP/IP.
- Identifica, de forma única, cada dispositivo em uma rede.
- Consiste de um número de **32 bits (4 bytes)**.
- O formato do endereço é determinado pelo protocolo da camada de rede e visa facilitar a tarefa de roteamento.
- Notação binária do endereço IP.
  - 10000010 10000100 00010011 00011111
  - 11001000 11011001 00010000 00001000
- Normalmente é usada a notação decimal.
- Cada byte do endereço é representado por um número decimal, separados por um ponto.
  - **Ex:** 130.132.9.31 200.241.16.8 10.0.0.0
- Composto por duas partes:
  - **NetID:** identificador da rede à qual a máquina está conectada.
  - **HostID:** identificador da máquina (Id da interface) dentro da rede.

### Conversão Decimal-Binário

- **Decimal:** 10.       1.        23.       19
- **Binário:** 00001010. 00000001. 00010111. 00010011
- **Decimal:** 200.      241.      16.      8
- **Binário:** 11001000. 11101101. 0010000. 00001000
- **Decimal:** 255.      255.      0.       0
- **Binário:** 11111111. 11111111. 0000000. 00000000
- **Decimal:** 127.      0.       0.       1
- **Binário:** 11111111. 0000000. 0000000. 00000001

### Converta os seguintes endereços IP decimal para Binário

- 243.15.63.100
- 10.0.0.5
- 172.16.254.1
- 255.255.255.0
- 127.0.0.1

### Conversão Binário-Decimal

- **Binário:** 1   1  1  1  1 1 1 1
- **Decimal:** 128 64 32 16 8 4 2 1
- **Resultado:** (128 + 64 + 32 + 16 + 8 + 4 + 2 + 1 = 255)

### Converta os seguintes endereços IP decimal para Binário:

- 11000000.10101000.00000001.00000001
- 00001010.00000000.00000000.00000101
- 10101100.00010000.11111110.00000001
- 11111111.11111111.11111111.00000000
- 01111111.00000000.00000000.00000001

## Classes de Endereços IP

- Endereços IP são organizados em classes.
- As classes determinam quantos bits são usados para identificar a rede e quantos para codificar a máquina.
  - **Classe A:** NetID = 8 bits, HostID = 24 bits
  - **Classe B:** NetID = 16 bits, HostID = 16 bits
  - **Classe C:** NetID = 24 bits, HostID = 8 bits
- Esse esquema de endereçamento é chamado de classful.

### Redes de Classe A (Redes/8)

- São redes de grande porte, que contam com um número imenso de máquinas.
  - **Ex:** 12.0.0.0 (AT&T); 13.0.0.0 (Xerox)
- Máximo de 127 redes (2<sup>7</sup>-2).
  - (0 a 127 = 128 redes)
  - 0.0.0.0: rota default
  - 127.0.0.0: função loopback
- Máximo de 16.777.224 (224-2) hosts por rede.
- 2<sup>31</sup> (2.147.483.648) endereços individuais.
- Faixa de NetID’s: 1 a 127.
- De 1.xxx.xxx.xxx até 127.xxx.xxx.xxx

### Redes de Classe B (Redes/16)

- São redes de médio porte;
- Ainda contam com um número ainda muito grande de hosts.
  - **Ex:** 129.188.0.0 (Motorola); 164.41.0.0 (UnB)
- Máximo de 16.384 redes (214).
- Máximo de 65.534 (216-2) hosts por rede;
- 2<sup>30</sup> (1.073.741.824) endereços individuais;
- Faixa de NetID’s: 128 a 191.
- 128.0.xxx.xxx até 191.255.xxx.xxx

### Redes de Classe C (Redes/24)

- São redes de pequeno porte;
- Contam com um pequeno número de hosts;
- Ex: 241.16.18.0; 196.239.26.0
- Máximo de 2.097.152 redes (221);
- Máximo de 254 (28-2) hosts por rede;
- 2<sup>29</sup> (536.870.912) endereços individuais;
- Faixa de NetID’s: 192 a 223:
  - 192.0.0.xxx até 223.255.255.xxx

## Classes de Endereços IP

1. Defina a quais classes os endereços IP's abaixo se referem. Justifique.
- a) 192.168.1.1
- b) 10.0.0.1
- c) 172.16.0.1
- d) 224.0.0.1
  
2. Defina a quais classes os intervalos de endereços IP pertencem. Justifique.
- a) 224.0.0.0 a 239.255.255.255
- b) 192.0.0.0 a 223.255.255.255
- c) 128.0.0.0 a 191.255.255.255
- d) 10.0.0.0 a 10.255.255.255

3. Nos endereços abaixo diga qual deles é um endereço IP válido ou inválido.
Justifique.
- a) 192.168.0.1
- b) 192.168.256.10.1
- c) 10.0.1
- d) 172.16.0.1
- e) 10.9.0.300
- f) 222.222.222.222

## Desvantagens do Endereçamento Classful

- Apenas 2<sup>32</sup> (4.294.967.296) endereços IPv4 disponíveis;
- Eventual exaustão do espaço de endereços;
- Não propicia propicia uma alocação eficiente do espaço de endereços;
- Classe C: apenas 254 hosts (muito pequeno);
- Classe B: 65.534 hosts (muito grande);

## Endereços Especiais

### Endreço de Rede

- As redes também têm o seu próprio endereço IP;
- O endereço IP que tem o HostID com todos os bits iguais a zero é, na realidade, o endereço da rede: 
**- Exemplos:**
  - 200.241.16.0 (classe C)
  - 164.41.0.0 (classe B)
  - 15.0.0.0 (classe A)

### Endereço de Loopback

- É um endereço IP especial usado para testar a comunicação da máquina consigo mesma;
- Permite que um computador envie e receba dados de si mesmo sem precisar acessar a rede;
- Endereço de loopback padrão: 127.0.0.1.

### Endereço de “Broadcast”

- Endereço reservado usado para referenciar todas as máquinas de uma rede:
- Um pacote IP com endereço de broadcast é sempre entregue a todas as máquinas da rede.
- Qualquer endereço cujo campo de HostID possua todos os bits iguais a 1 é um endereço de broadcast.
  - Exemplo: 200.241.16.255 (classe C)
  - Exemplo: 164.41.255.255 (classe B)
  - Exemplo: 10.255.255.255 (Classe A)

### Endereço de “Multicast”

- Referencia um grupo de máquinas de uma rede;
- Um grupo multicast é sempre identificado por um endereço classe D;
- Membros de um grupo ainda retém os seus próprios endereços IP, mas também têm a habilidade de absorver dados que são enviados para os endereços multicast;
- Para terem acesso às mensagens enviadas para endereços multicast as máquinas devem suportar o protocolo **IGMP**.
- Alguns endereços multicast são reservados, estando listados na RFC Internet Assigned Numbers.
  - 224.0.0.2 = todos os roteadores de uma subrede local.
- Diferentemente dos endereços broadcast, os endereços multicast não são restritos à rede local.

### Endereços Privados

- As faixas de endereços começadas com "10", "192.168" ou de "172.16" até "172.31 " são reservadas reservadas para uso em redes locais/intranets e por isso não são usadas na Internet;
  - 10.0.0.0 a 10.255.255.255
  - 172.16.0.0 a 172.31.255.255
  - 192.168.0.0 a 192.168.255.255
- Redes que usam endereços dessa faixa constituem redes privadas e a numeração é denominada de numeração privada.

## Atividades

1. Dado os Ip’s abaixo, indique a qual classes eles pertencem, bem como se é público ou privado.
- a) 10.9.0.44
- b) 200.217.235.80
- c) 127.255.0.128
- d) 172.30.115.254
- e) 205.208.33.1
- f) 8.15.32.1
- g) 192.168.0.20
- h) 192.169.0.33

2. Assinale (V) Verdadeiro ou (F) Falso:
( ) O endereço 127.0.0.1 é usado para testar a conectividade da máquina com ela mesma.
( ) Todos os endereços IP que começam com 192 são públicos.
( ) O hostID define qual parte do IP representa a rede.
( ) O endereço IP 172.16.0.0 é reservado para redes privadas.

3. Analise o seguinte IP: 172.31.100.25/16
a) A que classe pertence esse IP?
b) É um IP público ou privado?
c) Quantos hosts podem existir nessa sub-rede?

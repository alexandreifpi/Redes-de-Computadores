# Elementos de Rede

- São todos os dispositivos físicos e lógicos que fazem parte de uma rede de computadores e permitem a comunicação entre diferentes dispositivos, como computadores, celulares e servidores.
- São divididos em elementos **passivos** e elementos **ativos**.
  
# Elementos Passivos

- São componentes que não precisam de energia elétrica e não processam os dados, apenas permitem a passagem do sinal.

## Cabos de Rede

### 1. Cabo Coaxial Fino (Thinnet) – 10 Base 2

- Utilizado em redes industriais.
- Comprimento máximo de 500 metros.
- Máximo 100 computadores no barramento com distância entre as estações de 2,5 metros.
- Maior proteção contra interferência.
- Capaz de transmitir a 100 Mbps.

<img width="363" height="197" alt="img1" src="https://github.com/user-attachments/assets/5ae0aa3f-772e-4fca-9331-e1ad53e32f24" />

### 2. Cabo Coaxial Grosso (Thick Ethernet) – 10 base 5

- Um dos primeiros cabos utilizados em redes locais na topologia barramento.
- Tamanho máximo desse cabo é 185 metros por segmento.
- Máximo de 30 conexões distanciadas entre as estações de 0,5 metros.
- Proteção contra interferência.
- Velocidade máxima de 10 Mbps.

<img width="400" height="250" alt="img2" src="https://github.com/user-attachments/assets/542e3e2a-47db-4733-99a1-a4731bd660b2" />

### 3. Cabos UTP (Unshielded Twisted Pair)

- Cabos de rede de par trançado sem blindagem.
- É um meio de fio de quatro pares usado em uma variedade de redes.
- Cada um dos 8 fios individuais de cobre no cabo UTP é coberto por material isolante.
- Fácil de ser instalado e mais barato que outros cabos.

<img width="330" height="330" alt="img3" src="https://github.com/user-attachments/assets/f1c2f6ce-407e-43f3-8af5-68012f5cfa98" />

#### Vantagens 

- Baixo custo.
- Fácil manutenção.
- Diâmetro reduzido.
- Utilizado em vários tipos de rede.

#### Desvantagens

- Muito mais propenso a ruídos e interferências externas.
- Não tem muita resistência física.
- Mais susceptível á latência, diafonia, atenuação e ruídos;
- Distância máxima: 100 Metros.

### 4. Cabos STP (Shielded Twisted Pair)

- Possuem uma blindagem individual para cada par de cabos.
- Melhora a tolerância do cabo com relação à distância.
- Pode ser utilizado quando precisar de cabos com mais de 100 metros.

<img width="330" height="330" alt="img4" src="https://github.com/user-attachments/assets/71bd6c3c-eaf1-46bd-9f21-b31931b9e15c" />

## Categorias de Cabos (Cat1-Cat7)

### Cat1

- Utilizado em instalações telefônicas, porém inadequado para transmissão de dados.
- Sem blindagem, apenas uma capa de plástico protegendo os fios de cobre, contém apenas 2 pares.

### Cat2

- Tipo de cabo obsoleto.
- Permite transmissão de dados a até 2.5 megabits e era usado nas antigas redes.
- Sem blindagem, apenas uma capa de plástico protegendo os fios de cobre também apenas 2 pares de fios.

### Cat3

- Par trançado sem blindagem mais usado em redes há uma década.
- Pode se estender por até 100 metros e permite transmissão de dados a até 10 Mbps.

### Cat4

- Cabos com uma qualidade melhor que os cabos de categoria 3.
- Muito usado em redes com topologia anel de 16 megabits.
- Podiam ser usados também em redes Ethernet de 100 megabits.
- Não são mais fabricados.

### Cat5

- Evolução significativa em relação à Categoria 3 (Cat3).
- Possibilita uma taxa de transferência máxima teórica de 100 Mb/s (Conhecido como Fast Ethernet).
- Constituído por quatro pares de condutores, mas apenas dois são efetivamente utilizados para a transmissão e recepção de dados.
- Os pares não utilizados podem ser destinados a alimentação de dispositivos conectados.

### Cat5 E

- Projetado para suportar transmissões de dados com o uso simultâneo dos quatro pares de fios.
- Taxa de transferência máxima teórica de até 1 Gb/s (Gigabit Ethernet).
- A norma ANSI/TIA-568 define a Categoria 5e como a mínima aceitável para aplicações atuais de transmissão de dados.

### Cat6

- Pode permitir uma taxa de transferência máxima teórica de até 10 Gb/s em distâncias reduzidas de até 55 metros.
- Amplamente utilizado em instalações de rede que requerem maior largura de banda e desempenho, especialmente em ambientes empresariais onde a demanda por transferência de dados é alta.
- Ideal para suportar aplicações que envolvem transferência de arquivos grandes, streaming de vídeo em alta definição, videoconferências e outras atividades que exigem uma rede rápida e confiável.

### Cat7

- Suporta taxas de transferência de dados de até 10 Gb/s.
- Altamente imune a interferências eletromagnéticas, garantindo uma transmissão de dados mais estável e confiável.

# Elementos Ativos

- São os dispositivos que precisam de energia elétrica e atuam diretamente no funcionamento da rede, processando ou controlando os dados.

## Conceitos Importantes

### Domínio de colisão

- Um domínio de colisão é o conjunto de dispositivos em uma rede onde, se dois ou mais enviarem dados ao mesmo tempo, os sinais podem colidir.
- É como se tivéssemos uma rua com apenas uma única via e dois carros quisessem passar ao mesmo tempo.

## Hub

<img width="400" height="200" alt="image" src="https://github.com/user-attachments/assets/3b1343a9-2c1b-4dc4-8db2-d7f328c586a8" />

- Foram um dos primeiros dispositivos utilizados para interligar redes Lan's.
- Dispositivo de rede que atua na **Camada Física**.
- O Hub simplesmente **replica o sinal** recebido para todos os dispositivos conectados a ele.
- Possuem um **único domínio de colisão**.
- É como se todas as máquina estivessem enviado dados por um mesmo cabo.
- Os modelos de Hub's se diferenciam pela quantidade de portas (8, 16, 24, 32).
- Pode-se conectar HUBs, usando um cabo comum da porta especial **UPLINK** do Hub a uma porta comum de outro Hub.

### Vantagens

- Computadores podem ser adicionadas ou removidas sem parar a rede.
- Como são mais simples, tendem a custar menos que os Switches.

### Desvantagens

- Lentidão na rede.
- Pacotes enviados para todos os dispositivos.
- Mais suscetível a ações de hackers.
- Apenas uma comunicação por vez.

## Switch

<img width="400" height="200" alt="image" src="https://github.com/user-attachments/assets/de83e541-e66c-4e3e-91eb-d7c4cc3c424c" />

- Atualmente um dos dispositivos mais utilizados para interligar redes Lan's.
- Dispositivo de rede que atua na **Camada de Enlace**.
- Cada porta cria possui um domínio de colisão próprio.
- Diferente do Hub, o switch envia pacote de dados apenas para o dispositivo de destino, reduzindo tráfego de dados e colisões na rede.
- Ele faz isso analisando o endereço MAC do destinatário.

### Vantagens 

- Aumenta o desempenho da rede.
- Comunicação entre máquinas com placas de velocidades diferentes.
- Comunicação simultânea.
- Segurança.

### Desvantagens

- Custo mais elevado.
- Configuração mais difícil.

## Roteador

- Equipamento que serve para conectar diferentes redes.
- Dispositivo que opera na **Camada de Rede**.
- Usado para conectar diferentes redes, bem como traçar as rotas através dos algoritmos de roteamento.
- Alguns modelos de roteadores também incluem funções de Firewall.
- No uso doméstico, o roteador é o equipamento que conecta sua residência ao seu provedor de internet.

### Vantagens 

- Segurança: Estão cada vez mais equipados com "firewalls".
- Acessibilidade: Permite que as redes se comuniquem entre si.

### Desvantagens

- Complexidade de configuração.

### Funcionamento Básico do Roteador

- Os computadores posseum um Default Gateway (Saída Padrão).
- O Default Gateway indica qual endereço IP de saída da rede (**IP do roteador da rede**).
- Quando o computador remetente não encontra o computador de destino na mesma rede, ele envia os dados para o roteador da rede.
- Se o roteador não encontrar o computador destino, ele envia os dados para seu default gateway, até que encontre a máquina destino.

### Analisando o Roteamento na Prática

- Para analisar o roteamento na prática, podemos utilizar o comando **_tracert_** ou _**traceroute**_.

#### _**tracert**_

- Comando utilizado no **_Windows_** para rastrear a rota que os pacotes percorrem até um destino na rede, geralmente um site ou outro computador.

```bash
tracert www.google.com
```

#### **_traceroute_**

- Comando utilizado no **_Linux_** para rastrear a rota que os pacotes percorrem até um destino na rede, geralmente um site ou outro computador.

```bash
traceroute www.google.com
```

```bash
Resultado da execução do comando traceroute www.google.com

~$ traceroute www.google.com
traceroute to www.google.com (142.251.154.119), 30 hops max, 60 byte packets
 1  _gateway (192.168.1.1)  2.120 ms  14.431 ms  14.535 ms
 2  100.64.0.1 (100.64.0.1)  43.055 ms  43.029 ms  43.004 ms
 3  172.27.100.185 (172.27.100.185)  43.510 ms  43.487 ms  43.462 ms
 4  172.27.100.101 (172.27.100.101)  43.465 ms  43.426 ms  43.401 ms
 5  10.22.1.37 (10.22.1.37)  43.319 ms  43.295 ms  43.271 ms
 6  10.55.1.185 (10.55.1.185)  43.203 ms  6.608 ms  19.899 ms
 7  * * *
 8  10.55.0.90 (10.55.0.90)  19.812 ms  19.793 ms  19.773 ms
 9  10.55.1.65 (10.55.1.65)  27.241 ms  27.222 ms  27.203 ms
10  10.55.3.90 (10.55.3.90)  52.176 ms  52.158 ms  56.200 ms
11  173.194.122.156 (173.194.122.156)  54.681 ms  56.494 ms  57.678 ms
12  142.251.154.119 (142.251.154.119)  42.404 ms  42.337 ms  43.952 ms
```

```bash
traceroute www.ifpi.edu.br

traceroute to www.ifpi.edu.br (66.22.76.194), 30 hops max, 60 byte packets
 1  _gateway (192.168.1.1)  1.690 ms  13.871 ms  13.845 ms
 2  100.64.0.1 (100.64.0.1)  15.408 ms  15.384 ms  15.359 ms
 3  172.27.100.181 (172.27.100.181)  15.769 ms  15.745 ms  15.721 ms
 4  172.27.100.101 (172.27.100.101)  15.755 ms  15.821 ms  15.798 ms
 5  10.22.1.37 (10.22.1.37)  19.752 ms  19.729 ms  19.705 ms
 6  10.55.1.185 (10.55.1.185)  19.649 ms  6.627 ms  20.845 ms
 7  * * *
 8  10.55.1.1 (10.55.1.1)  20.793 ms  20.775 ms  20.757 ms
 9  10.55.3.118 (10.55.3.118)  21.028 ms  21.009 ms  22.397 ms
10  10.55.10.190 (10.55.10.190)  30.156 ms  30.302 ms  30.491 ms
11  10.55.3.246 (10.55.3.246)  30.159 ms  30.294 ms *
12  198.18.44.5 (198.18.44.5)  16.950 ms  16.871 ms  16.846 ms
13  ae101.0.edge1.for1.as7195.net (200.25.51.51)  20.342 ms ae1185.0.edge7.gru1.as7195.net (200.25.51.227)  60.438 ms ae101.0.edge1.for1.as7195.net (200.25.51.51)  21.451 ms
14  as15830.saopaulo.sp.ix.br (187.16.208.139)  62.040 ms  57.366 ms  60.643 ms
15  131.100.112.190 (131.100.112.190)  63.167 ms  65.963 ms as15830.saopaulo.sp.ix.br (187.16.208.139)  61.932 ms
16  155.204.216.22 (155.204.216.22)  59.695 ms  62.412 ms  62.890 ms
17  * * 155.204.216.22 (155.204.216.22)  61.269 ms
18  * 172.18.50.113 (172.18.50.113)  59.295 ms 172.18.50.213 (172.18.50.213)  59.389 ms
19  172.18.251.82 (172.18.251.82)  58.730 ms  60.886 ms  59.584 ms
20  172.18.251.82 (172.18.251.82)  61.226 ms 66.22.76.194 (66.22.76.194)  58.422 ms  59.273 ms
```

#### Cada linha indica:

- O número do salto.
- O tempo (em milissegundos) que levou para o pacote chegar até ali.
- O endereço IP ou nome do roteador daquele salto.


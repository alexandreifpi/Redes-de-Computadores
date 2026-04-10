# Introdução a Redes de Computadores

## Contextualização

<img width="500" height="281" alt="image" src="https://github.com/user-attachments/assets/31218862-f29c-424c-acfb-639d1a70ac00" />

## Redes de Computadores

> Sistema que interliga dispositivos computacionais para compartilharem recursos e trocarem informações.
> Permite acessar recursos que estão em um local físico distante.

- Não é uma tecnologia nova, as redes surgiram na mesma época do surgimento dos primeiros computadores.

<img width="500" height="278" alt="image" src="https://github.com/user-attachments/assets/8aa188da-5eb4-4683-ad3b-a9a76fe297de" />

## Tipos de Redes de Computadores (Quanto a Abrangência)

> Redes classificadas de acordo com a área geográfica que elas abrangem.

- **LAN (Local Area Network):** abrangem um espaço de um sala, escritório, casa ou prédio inteiro.
- **WLAN (Wireless Local Area Network):** mesma característica da LAN, mas sem utilização de cabos, utilizam transmissão de radiofrequência (WI-FI).
- **CAN (Campus Area Network):** redes que abrangem mais de um prédio (Universidades, Hospitais, Grandes Empresas, etc).
- **MAN (Metropolitan Area Network):** maior que uma rede de campo, pode abranger uma cidade inteira.
- **Internet:** rede mundial de computadores.
- **Intranet:** rede privada que utiliza o mesmo modelo da internet para acesso privado de dados.

## Tipos de Redes de Computadores (Quanto a Garantia de Entrega de Dados)

> Redes que garantem a entrega de dados são chamadas orientadas a conexão. As que não garantem são chamadas não orientadas a conexão.

- Nas redes orientadas a conexão, a entrega se dá em três etapas (transmissor envia pedido de conexão, receptor envia informação aceitando ou rejeitando conexão, transmissor envia os pacotes de dados).
- Já as redes não orientadas a conexão simplesmente envia os dados, sem se importar com a garantia de entrega.

## Tipos de Redes de Computadores (Quanto a Previsibilidade de Funcionamento)

> Estão relacionados a tempo de entrega ou tempo de espera de um determinado recurso da rede.

- **Determinística:** redes que funcionam de forma previsível.
- **Probabilística:** redes que funcionam de forma imprevisível.

## Componentes de Rede

<img width="500" height="99" alt="image" src="https://github.com/user-attachments/assets/d96a2b76-e53b-4bb1-8b73-32c98a61adcb" />

### Host ou Sistemas Finais

> São os dispositivos que utilizam a rede para enviar e receber dados. Podem ser computadores, notebooks, smartphones, impressoras de rede, câmeras IP, entre outros.

- **Exemplo:** quando um aluno acessa um site pelo navegador, o computador dele é um host.

### Servidor

> É um tipo especial de host que oferece serviços para outros dispositivos na rede.

- **Pode fornecer:** Páginas web, Arquivos, E-mails, Banco de dados, Sistemas internos, dentre outros serviços.
- **Exemplo:** quando acessamos um site, estamos nos conectando a um servidor que hospeda aquele conteúdo.

### Roteador

> É o equipamento responsável por interligar redes diferentes.

- Sua principal função é encaminhar os pacotes de dados pelo melhor caminho até o destino.
- **Exemplo:** A rede interna da sua casa ou escola à Internet.

### Switch

> É o equipamento que conecta vários dispositivos dentro da mesma rede local (LAN).

- Ele permite que computadores e outros dispositivos se comuniquem entre si.
- Diferente do roteador, o switch não conecta redes diferentes — ele organiza a comunicação interna.
- **Exemplo:** em um laboratório de informática, os computadores costumam estar ligados a um switch.

### ISP (Provedor de Internet)

> ISP significa Internet Service Provider (Provedor de Serviços de Internet).

- É a empresa que fornece acesso à internet para residências, escolas e empresas.
- **Exemplo:** Claro Brasil, Vivo, TIM Brasil, Oi, Oxente Net, G3 Telecom, etc.

## Internet

<img width="486" height="648" alt="image" src="https://github.com/user-attachments/assets/106c8b4b-3fb6-44b8-9029-f29d837d2ae9" />

> Rede de computadores que interconecta centenas de milhões de dispositivos de computação ao redor do mundo.

- Computadores, servidores, TVs, laptops, videogames, celulares, automóveis, sensores, etc.

### Serviços da Internet

- Correio eletrônico
- Navegação na Web
- Redes sociais
- Mensagem instantânea
- Vídeos em tempo real
- Jogos distribuídos
- Compartilhamento de arquivos
- Peer-to­‑peer (P2P)
- Televisão pela Internet

## Protocolo

> São conjuntos padronizados de regras que permitem que computadores e dispositivos de diferentes fabricantes se comuniquem, formatando e processando dados.

- Eles atuam em camadas (modelo OSI ou TCP/IP), definindo como as informações são transmitidas, recebidas, estruturadas e protegidas na rede.
- Todas as atividades na Internet que envolvem duas ou mais entidades remotas comunicantes são governadas por um protocolo.

<img width="412" height="260" alt="image" src="https://github.com/user-attachments/assets/aace5e76-d3ec-4ce5-8efa-188361b04842" />

### Exemplo de protocolo de rede

- Quando você digita um endereço de site no navegador, acontece basicamente isso:

1. O computador pede "permissão" para falar com o servidor do site: "Quero me conectar a você.".
2. O servidor recebe esse pedido e responde: "Ok, conexão aceita."
3. O computador envia outra mensagem dizendo qual página ele quer abrir.
4. Essa mensagem é chamada de requisição GET.
5. O servidor recebe o pedido da página.
6. Por fim, o servidor envia de volta o arquivo da página para o computador.
7. O navegador recebe o arquivo e mostra o site na tela.

## Interação entre sistemas finais

<img width="500" height="652" alt="image" src="https://github.com/user-attachments/assets/03198c67-69ac-42d8-acf3-b97f0491bce5" />

## Redes de Acesso

> Redes de acesso (ou rede de borda) conectam os usuários finais (residências, empresas, dispositivos móveis) ao provedor de serviços de internet (ISP) ou ao núcleo da rede.

### Via Rádio

<img width="500" height="281" alt="image" src="https://github.com/user-attachments/assets/3b44d63f-b32f-4b8e-835a-592d07bc74c2" />

> Utiliza ondas de rádio para transmitir o sinal de internet entre uma torre do provedor e uma antena instalada na casa ou empresa do cliente. Muito comum em áreas rurais ou onde não há infraestrutura cabeada.

#### Vantagens

- Pode chegar a locais remotos.
- Instalação relativamente rápida.
- Não depende de cabos físicos longos.
- Custo menor de infraestrutura para o provedor.

#### Desvantagens

- Sensível a interferências (chuva, obstáculos, relevo).
- Estabilidade inferior ao cabeamento.
- Velocidade geralmente menor que fibra.
- Depende de visada direta (linha de visão).

### Acesso Discado (Dial-Up)

> Foi uma das primeiras formas de acesso residencial à Internet, muito usada nos anos 1990 e início dos anos 2000.
> Utilizava a linha telefônica comum.
> O computador usava um modem para “ligar” para o provedor.
> A conexão era estabelecida como se fosse uma chamada telefônica.
> A linha ficava ocupada (não dava para usar o telefone).
> Até 56 Kbps (kilobits por segundo).
> Custo muitas vezes baseado no tempo de uso.

### DSL

> Tecnologia de acesso à Internet que utiliza a linha telefônica de cobre já existente da residência.
> 12 a 24 Mbps (download) - 1,8 a 2,5 Mbps (upload).

#### Vantagens

- Usa infraestrutura telefônica existente.
- Permite usar telefone e internet simultaneamente.
- Conexão dedicada entre casa e central.

#### Desvantagens

- A velocidade diminui conforme aumenta a distância até a central telefônica.

### Cabo UTP/Coaxial

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/793437f1-2bce-42eb-8c30-fbd01f4591ec" />

> Utiliza o mesmo cabo coaxial da TV a cabo. Muito usada por operadoras de TV por assinatura.

#### Vantagens

- Menores custos de instalação.
- Infraestrutura já existente em muitas cidades.

#### Desvantagens

- Alta necessidade de manutenção e troca constante de equipamentos.
- Velocidade limitada a até 100 Mbps.

### Móvel

<img width="500" height="109" alt="image" src="https://github.com/user-attachments/assets/6933c1d0-fbd5-4be6-abf0-a3f055847a8f" />

> Fornecida por operadoras de telefonia móvel, utilizando torres celulares. O acesso pode ser feito por smartphones, modems USB ou roteadores com chip (SIM Card).

#### Vantagens

- Alta mobilidade.
- Fácil de usar e instalar.
- Boa cobertura em áreas urbanas.

#### Desvantagens

- Franquia de dados limitada.
- Velocidade e latência variam bastante.
- Pode ficar lenta em horários de pico.
- Dependente da qualidade do sinal da operadora.
- Necessidade de uma cobertura móvel próxima.

### Satélite

<img width="241" height="241" alt="image" src="https://github.com/user-attachments/assets/51a0b5b6-82b7-4c7e-844c-c04793475945" />

> O sinal é transmitido entre uma antena parabólica na residência e um satélite em órbita. Muito usada em locais extremamente isolados.

#### Vantagens

- Cobertura ampla (inclusive áreas sem infraestrutura).
- Independente de cabos ou torres locais.
- Funciona em regiões remotas.

#### Desvantagens

Alta latência.
Custo elevado.
Sensível a condições climáticas.
Desempenho inferior para jogos e videoconferências.

### Fibra Ótica

<img width="500" height="339" alt="image" src="https://github.com/user-attachments/assets/e43bdce6-ddce-4115-84f9-abcf3e7914a9" />

> Utiliza cabos de fibra óptica, que transmitem dados por meio de pulsos de luz. É a tecnologia mais moderna e eficiente atualmente.

#### Vantagens

Baixo custo de manutenção.
Alta velocidade (cerca de 68% a 70% da velocidade da luz).
Imune a interferências eletromagnéticas.

#### Desvantagens

Custo de implantação mais alto.
Não disponível em todas as regiões.
Reparo pode ser mais complexo.

## Atividades

1. Explique o que é uma rede de computadores e descreva seus principais objetivos.
2. A Internet é frequentemente confundida com uma rede comum. Explique o que é a Internet e destaque as principais diferenças entre Internet e uma rede local (LAN).
3. Descreva a função dos seguintes elementos dentro de uma rede de computadores:
   - Host
   - Servidor
   - Switch
   - Roteador
4. Explique como as redes de computadores e a Internet impactaram a educação, o comércio e a comunicação nas últimas décadas. Dê exemplos práticos.

## Referências

- https://megabyteba.com.br/as-principais-tecnologias-de-acesso-a-internet/


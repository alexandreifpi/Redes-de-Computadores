# Roteamento

- Duas máquinas que utilizam o protocolo IP, e estão em uma mesma rede, se comunicam.
- No entanto, a comunicação entre máquinas que estão em redes diferentes requer o reencaminhamento dos pacotes através dos roteadores.
- Esse processo se chama roteamento.
- Portanto, roteamento é o processo de encaminhar pacotes de dados entre redes diferentes. Sua função é garantir que a informação enviada por um dispositivo chegue corretamente ao destino, escolhendo o melhor caminho possível através de roteadores.

## Como Funciona?

- Esse processo é baseado em tabelas que são configuradas dentro dos roteadores.
- Estas tabelas podem ser configuradas de forma estática (quando raramente se modificam)
- Ou criadas dinamicamente através de programas que são executados em todos os roteadores da rede.
- A tabela é utilizada para cada pacote que chega ao roteador.

## Analogia

- Imagine que você está viajando por várias cidades.
- Normalmente você poderia utilizar um mapa (Físico ou digital).
- Entretanto, ao invés de utilizar um mapa, imagine que cada cidade possui uma tabela indicando qual a próxima cidade dependendo do seu destino?

<img width="740" height="740" alt="image" src="https://github.com/user-attachments/assets/4a8086e8-c37c-444b-a2a8-046d00831314" />

<img width="621" height="273" alt="Captura de tela de 2026-05-07 00-08-47" src="https://github.com/user-attachments/assets/9589265e-fc43-4b69-af15-78fd0aab172d" />

- Imagine que você está na cidade C e deseja ir até a cidade E.

## Rota Padrão (Default Gateway)

- Informa para onde ir caso não exista uma rota específica para o destino.

<img width="555" height="246" alt="Captura de tela de 2026-05-07 00-13-58" src="https://github.com/user-attachments/assets/c4b88aad-3404-4baa-9622-d8075e141a91" />

## Tabela de Roteamento

- Atua como um “mapa” para orientar roteadores até a rede de destino.
- Desta forma, o roteador não precisa conhecer todo o caminho, apenas o próximo roteador nesse caminho.

## Principais Campos de uma tabela de roteamento

- **Endereço IP** junto **máscara de rede** (identificam a rede de destino).
- Gateway (**IP do próximo roteador no caminho**).
- **Interface de saída** (por onde os pacotes são enviados).
- Cada linha da tabela é chamada de rota.

## Rotas para redes diretamente conectadas

- A comunicação ocorre diretamente entre os dispositivos.
- Não há necessidade de roteadores intermediários.
- Os pacotes são enviados localmente (mesmo domínio de rede).
- Não possuem gateway.
- O gateway pode ser substituído pela interface ou pelo valor 0.0.0.0.

## Rotas para redes indiretamente conectadas

- A comunicação precisa passar por um ou mais roteadores.
- Os pacotes são encaminhados de rede em rede até chegar ao destino.
- É necessário o processo de roteamento.

## Tabelas de roteamento em dispositivos

- Dispositivos também precisam decidir para onde enviar seus próprios pacotes.
- Portanto, todos os dispositivos que enviam dados através do protocolo IP possuem tabela de roteamento (não só roteadores).
- A diferença que roteadores encaminham pacotes de terceiros.
- Já os dispositivos usam a tabela apenas para enviar seus próprios pacotes.

## Criação das tabelas de roteamento

- Redes pequenas/médias: configuração manual pelo administrador.
- Redes grandes: configuração automática via software de roteamento.
- Roteadores trocam informações entre si para construir automaticamente as tabelas.

## Rota Padrão

- Um roteador precisa ser capaz de encaminhar pacotes para qualquer rede na internet.
- Desse modo, precisaria existir uma linha na tabela de roteamento de cada roteador para cada rede existente na internet.
- Isso seria impossível.
- Por isso existe a rota padrão, que é uma rota que será utilizada quando não existir nenhuma rota na tabela de roteamento específica para a rede de destino do pacote.
- Essa rota especifica o IP do gateway que deve ser utilizado para esses casos e a interface por onde o gateway é alcançado.
- Os campos endereço de destino e máscara são preenchidos com 0.0.0.0.

<img width="801" height="379" alt="image" src="https://github.com/user-attachments/assets/f1de35fb-4a21-4ec4-8493-1b9fa500cb06" />

<img width="440" height="136" alt="Captura de tela de 2026-05-07 00-35-12" src="https://github.com/user-attachments/assets/0707cf97-63c5-4f53-b6a5-0576767bdb22" />

<img width="440" height="240" alt="Captura de tela de 2026-05-07 00-35-36" src="https://github.com/user-attachments/assets/37a57fc5-c0d8-4761-8538-9f7453284b5d" />

- Observe na tabela de roteamento de R1 que mesmo usando a rota padrão deve ser cadastrada uma rota para a rede 10.1.4.0 / 24, pois o caminho para esta rede é através de R2, e não de R3 que é a rota padrão de R1.

## Consultando a tabela de roteamento

- Define como cada pacote será encaminhado pelo roteador.
- O roteador analisa a tabela linha por linha para cada pacote.
- Aplica a máscara de rede ao IP de destino (AND Binário).

**IP decimal para binário**

10.1.2.130  = 00001010.00000001.00000010.10000010

**Máscara da Rede**

255.255.255.0 = 11111111.11111111.11111111.00000000

**IP da rede**

00001010.00000001.00000010.00000000 = 10.1.2.0

- Compara o resultado com o endereço de rede da rota.
- Se for igual, a rota é escolhida, verifica se contem gateway, o pacote é enviado para outro roteador.
- Se o gateway for 0.0.0.0, o destino é diretamente conectado e o pacote é entregue localmente.
- A rota padrão sempre será verdadeira se nenhuma outra rota bater.
- Garante que todo pacote tenha um caminho.
- As rotas são testadas sequencialmente (de cima para baixo).
- Assim que uma correspondência é encontrada, o processo para.

## Atividades

1. O que é roteamento e qual sua função em redes de computadores?

2. Diferença entre comunicação:
	a) Dentro da mesma rede.
	b) Entre redes diferentes.

3. O que é a tabela de roteamento e qual seu papel no roteador?

4. O que é a rota padrão (default gateway) e por que ela é necessária?

5. Por que dispositivos como computadores também possuem tabela de roteamento?


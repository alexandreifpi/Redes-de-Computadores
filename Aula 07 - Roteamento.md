# Roteamento

- Duas máquinas que utilizam o protocolo IP, e estão em uma mesma rede, se comunicam.
- No entanto, a comunicação entre máquinas que estão em redes diferentes requer o reencaminhamento dos pacotes através dos roteadores.
- Esse processo se chama roteamento.

## Como Funciona?

- Esse processo é baseado em tabelas que são configuradas dentro dos roteadores.
- Estas tabelas podem ser configuradas de forma estática (quando raramente se modificam)
- Ou criadas dinamicamente através de programas que são executados em todos os roteadores da rede.
- A tabela é utilizada para cada pacote que chega ao roteador.

## Analogia

- Imagine que você está viajando por várias cidades.
- Normalmente você poderia utilizar um mapa (Físico ou digital).
- Entretanto, ao invés de utilizar um mapa, imagine que cada cidade possui uma tabela indicando qual a próxima cidade dependendo do seu destino?

<img width="621" height="273" alt="Captura de tela de 2026-05-07 00-08-47" src="https://github.com/user-attachments/assets/9589265e-fc43-4b69-af15-78fd0aab172d" />

- Imagine que você está na cidade C e deseja ir até a cidade E.

## Rota Padrão (Default Gateway)

- Informa para onde ir caso não exista uma rota específica para o destino.

<img width="555" height="246" alt="Captura de tela de 2026-05-07 00-13-58" src="https://github.com/user-attachments/assets/c4b88aad-3404-4baa-9622-d8075e141a91" />

## Tabela de Roteamento

- Atua como um “mapa” para orientar roteadores até a rede de destino.
- O roteador não precisa conhecer todo o caminho, apenas o próximo roteados nesse caminho.

## Principais Campos de uma tabela de roteamento

- **Endereço IP** junto **máscara de rede** (identificam a rede de destino).
- Gateway (**IP do próximo roteador no caminho**).
- **Interface de saída** (por onde os pacotes são enviados).
- Cada linha da tabela é chamada de rota.

## Rotas para redes diretamente conectadas

- Não possuem gateway.
- Pacotes são enviados diretamente à rede destino.
- O gateway pode ser substituído pela interface ou pelo valor 0.0.0.0.

## Tabelas de roteamento em dispositivos

- Todos os dispositivos IP possuem tabela de roteamento (não só roteadores).
- A diferença que roteadores encaminham pacotes de terceiros.
- Os Hosts (computadores) usam a tabela apenas para enviar seus próprios pacotes.

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



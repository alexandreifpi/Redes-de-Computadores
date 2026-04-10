# Modelo de Referência OSI

- Há um tempo atrás, a maioria das soluções em redes de computadores era proprietária. Qualquer equipamento ou software para aquela rede deveria ser adquirido com o mesmo fabricante. Equipamentos e software de fabricantes diferentes não se comunicavam.
- As soluções eram mais caras.
- Dependência total de um fabricante (se aumentar muito os preços? se a empresa falir?).
- Surge a necessidade de padronizar a comunicação entre diferentes redes.

## Reference Model - Open System Interconection

<img width="221" height="228" alt="image" src="https://github.com/user-attachments/assets/21b907f3-ca41-4d0d-aefc-949602c0c974" />

> Modelo de referência - Interconexão de sistemas abertos.
> Desenvolvida pela ISO (International Organization for Standartzation).
> Modelo em camadas que visa fornecer um padrão de comunicação de sistemas de computadores.

### Objetivos:

- Padronização.
- Interoperabilidade.
- Escalabilidade.

### Divisão em Camadas

- Possui 7 camadas, cada uma funciona de forma independente.
- Possuem seus próprios protocolos que são responsáveis por determinadas tarefas. Funções similares agrupadas em uma mesma camada.
- Cada camada só mantém contato com sua camada inferior ou superior.

### Protocol Data Unit - PDU

> PDU: é o nome específico do conjunto de dados e cabeçalho encapsulados em cada camada do modelo OSI.

<img width="500" height="220" alt="image" src="https://github.com/user-attachments/assets/6f84f99a-80c8-4d55-9842-4ee27f84d876" />

## 7 - Camada de Aplicação

- Estabelece uma interface por meio da qual os aplicativos podem se comunicar com a rede. É a interface (porta de entrada) entre o usuário e as outras camadas.
- Nesta camada estão os programas que garantem a comunicação humano-computador.

<img width="500" height="145" alt="image" src="https://github.com/user-attachments/assets/94988852-5658-4028-9391-e86f21c62c47" />

### Exemplos de Protocolos

- **HTTP/HTTPS:** Navegação web
- **FTP**: Transferência de arquivos.
- **SMTP, IMAP e POP3**: Envio e recebimento de e-mails.
- **DNS**: Resolução de nomes de domínio em endereços IPs.
- **Telnet/SSH**: Acesso remoto a dispositivos.

### Navegar na Internet (HTTP/HTTPS)

- Você abre o navegador e acessa um site como "www.google.com".
- O que acontece na camada de aplicação?
- O protocolo HTTP/HTTPS é utilizado para solicitar a página do servidor web e exibir seu conteúdo no navegador. 

## 6 - Camada de Apresentação

- Responsável pela tradução dos dados vindo da camada de aplicação para a próxima camada.

<img width="500" height="159" alt="image" src="https://github.com/user-attachments/assets/1565df70-3291-4f34-9d9f-72e3aec4b811" />

- **Formatação de dados:** Um sistema pode usar texto codificado em ASCII, enquanto outro usa UTF-8. A camada de apresentação realiza a conversão entre os dois formatos.
- **Compactação de dados**: Quando você faz upload de arquivos comprimidos, a camada de apresentação pode compactar os dados para enviá-los mais rapidamente.
- **Criptografia de dados**: Protocolo HTTPS utiliza criptografia para proteger os dados entre o navegador e o servidor.

## 5 - Camada de Sessão

- Responsável pela inicialização, gerenciamento e finalização de sessões entre o transmissor e receptor.
- Uma sessão pode ser iniciada, mantida e finalizada quando não houverem mais dados a serem transmitidos ou quando uma das partes quiserem encerrar a comunicação.
- Permite que dois programas em computadores diferentes estabeleçam uma sessão de comunicação.
- **Analogia:** Ligação telefônica.
- **Exemplo:** Acessar um site.

<img width="500" height="159" alt="image" src="https://github.com/user-attachments/assets/a170d221-2fb3-42fe-90ea-5f0cff043666" />

## 4 - Camada de Transporte

- Responsável pela comunicação de ponta a ponta entre os dois dispositivos.
- Pega os dados da camada de sessão, dividi-os em porções chamadas segmentos antes de enviá-los para a próxima camada.
- A camada de transporte no dispositivo receptor é responsável por remontar os segmentos em dados que a camada de sessão possa consumir.
- A camada de transporte realiza o controle de fluxo, determinando uma velocidade de transmissão ideal para garantir que um remetente com uma conexão rápida não sobrecarregue um receptor com uma conexão lenta.
- Também executa o controle de erros no lado do receptor, garantindo que os dados recebidos estejam completos e solicitando uma retransmissão caso não estejam.

<img width="500" height="159" alt="image" src="https://github.com/user-attachments/assets/8efc4bf5-67ba-44d5-812a-74d4c5924d3e" />

## 3 - Camada de Rede

- Responsável por realizar a transferência de dados entre duas redes diferentes.
- Trata os endereços de rede IP (Internet Protocol).

## 2 - Camada de Enlace

- Transforma/Organiza os pacotes que vêm da camada de rede com endereços IP já definidos em "quadros" ou "frames".
- Os quadros  acrescentam outra forma de endereçamento chamada endereço MAC.

### Mas os endereços já não estavam definidos na camada de rede pelo IP?

- O endereço IP não é suficiente para identificar um computador específico dentro da internet.
- O IP nos diz em qual é a rede que você está.
- Já o MAC diz quem você é.

## 1 - Camada Física

- Trata da transmissão de bits puros por um canal de comunicação. O projeto da rede deve garantir que, quando um lado enviar um bit 1, o outro lado o receba como bit 1, não como bit 0.

### A camada física converte quadros em bits 0 e 1: 

Em sinais elétricos, quando meio físico é cobre.
Em sinais luminosos, quando o meio é fibra ótica.
Em frequência de rádio, quando meio sem fio.

## Atividades

1. Explique o que é o Modelo OSI e qual sua importância para as redes de computadores.
2. Fale sobre 3 camadas do Modelo OSI descrevendo a função de cada uma delas.

## Referências

- https://www.cloudflare.com/pt-br/learning/ddos/glossary/open-systems-interconnection-model-osi/

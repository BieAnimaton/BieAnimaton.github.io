---
title: "Sistemas Distribuídos - Resumão para P1"
excerpt: "Resumo Sistemas Distribuídos"
categories:
  - Sistemas Distribuídos
tags:
  - Sistemas Distribuídos
  - Resumo
  - Teoria

toc: true
---

# Aula I

![imagem da lousa](https://github.com/user-attachments/assets/148d3673-8740-48e8-ac6a-5244bf9e529a)

## Como referenciar o PID?

Através do IP e porta.

## Como compartilhar dados?

Através do envio de pacotes pela rede.

## Como estabelecer relações de precedência e causalidade de eventos?

Através da chegada de pacotes.

## O que é sistema distribuído?

É uma coleção de computadores independentes que aparenta aos usuários como se fosse um único computador.

Integrados por um middleware, uma camada de software que se estende por todas as máquinas do sistemas.

É aquele no qual componentes de hardware e software estão localizados em computadores interligados em rede e se comunicam e coordenam suas ações passando mensagens.

## Apresente as características do sistema distribuído.

### Concorrência

programas executam concorrentemente e compartilham recursos comuns da rede.

### Inexistência de um Relógio Global:

A coordenação entre processos se da por troca de mensagens, o sincronismo de relógios em rede impõe limites de precisão.

### Falhas independentes:

Componentes de um sistema podem falhar mas os outros devem permanecer em funcionamento.

## Desafios

Dever ter os objetivos:

Conectividade

Transparência

Abertura

Escalabilidade

Heterogeneidade

Segurança

Tratamento de falhas

Concorrência

## Conectividade

Um sistema distribuído deve permitir a comunicação entre usuários e recursos compartilhados (impressoras, arquivos, unidades de armazenamento, etc).

Outras aplicações para ambientes distribuídos (redes corporativas, redes sociais e peer-to-peer, armazenamento de dados na nuvem, etc).

## Transparência

Esconde os detalhes específicos do sistema distribuído.

Oferece a visão de um sistema único a usuários e aplicações, escondendo detalhes da distribuição de suas partes.

Poder ser comprometida por fatores de desempenho de canas de comunicação.

### Transparência de Acesso

Permite que recursos locais e remotos sejam acessados através de operações idênticas.

Também esconde diferenças de representação de dados.

Ex: little endian, big endian, diferença entre convenções de nomes de arquivos.

### Transparência de Localização

Esconde detalhes de onde o recurso realmente está.

A localização de um recurso pode mudar sem a necessidade de se reprogramar todo o sistema.

A solução é a aplicação de servidores de nomes - DNS

### Transparência de Concorrência

Permite o compartilhamento de um recurso concorrido por diversos usuários, sem que haja interferência durante o uso.

Realização de operações consistentes podem compor transações.

Qualquer modificação em um sistema deve deixá-lo em um estado consistente.

### Transparência de Replicação

Permite a duplicação de informação para aumentar a disponibilidade e o desempenho do sistema.

Desafio é manter o sincronismo das alterações e a consistência da informação.

As réplicas devem compartilhar uma identificação (nome) única ao usuários.

### Transparência de Falha

Esconde a ocorrência de falhas do sistema.

Estabelece formas de recuperação de estados inconsistentes.

O principal problema em mascarar falhas é em distinguir se o recurso está realmente inacessível ou o acesso está demorado (atraso).

### Transparência de Mobilidade

Permite que um recurso seja movido para outro local, durante o uso.

Atualmente os equipamentos móveis precisam ficar conectados em serviços e ambiente distribuídos enquanto seus usuário se deslocam para os mais diversos lugares.

Característica essencial para sistema de computação ubíqua (onipresente) e pervasiva (que se espalha fácil), incluindo novas aplicações com realidade aumentada e jogos.

### Transparência de Desempenho

Permite que o sistema seka reconfigurado para melhorar o desempenho à medida que as cargas variam

### Transparência de Escalabilidade

Permite que o sistema e os aplicativos se expandam em escala, sem alterar a estruta do sistema ou os algorimos do aplicativo.

## Abertura

Aberto = sistema fácil simples de implementar.

Ex: http.

### Padrões abertos

Oferecimento de serviço com regras padronizadas (protocolos abertos) que descrevem a sintaxe e a semântica do serviço.

### Sintaxe

Especificam nomes de funções, tipos de parâmetros, valores de retornos e exceções previstas.

As interfaces são definidas por uma IDL (interface definition language).

### Semântica

Comportamento do serviço em questão.

## Interoperabilidade e Portabilidade

Afetadas diretamente pela abertura em sistemas distribuídos.

### Interoperabilidade

Habilidade de dois componentes de fornecedores diferentes coexistirem e trabalharem juntos.

Seguem um padrão definido para o serviço em questão.

### Portabilidade

Facilidade de usar sem modificações uma aplicação desenvolvida para o sistema distribuído A no sistema distribuído B.

## Escalabilidade

Pode ser medida em três dimensões:

Tamanho, geográfica e administrativas.

### Limitações de Tamanho

- Refletem a capacidade de expandir um sistema distribuído em numero de usuários e recursos
    
    Alguns recursos podem se tornar um gargalo.
    
    Ao copiar recurso pode trazer aumento das vulnerabilidades.
    
- Alguns exemplo de limitações de escalabilidade
    
    Serviços centralizados, dados centralizados e algoritmos centralizados.
    

### Limitações Geográficas

- Afetam diretamente a sincronização do sistema distribuído.
    
    Redes locais - baixa latência.
    
    Redes esparsa - a comunicação pode ser mais lenta em até 3 ordens de magnitude.
    
- Outro problema é com a forma de transmissão das mensagens
    
    Redes locais - enviar uma mensagem broadcast.
    
    Redes esparsas - ponto-a-ponto.
    

### Limitações Administrativas

Particularidades de cada local integrado integrado pelo sistema distribuído.

Diferentes localidades podem definir politicas particulares relacionadas ao uso de recursos (e o pagamento por ele), gerenciamento e segurança.

Formas de compensação e adaptação devem ser aplicadas às fronteiras de tais localidades, delimitando a interação entre as partes do sistema.

## Técnicas para Escalabilidade

A principal limitação em sistemas distribuídos é a GEOGRÁFICA.

Formas de superar:

### Esconder a latência

- Evita a espera por respostas de solicitações efetuadas a servidores remotos
    
    Realiza outras tarefas que não dependam da comunicação assíncrona.
    
- Uma forma de diminuir o efeito do atraso é diminuir a demanda pela comunicação
    
    Procedimentos movidos para o lado do cliente para encaminhar informações melhor consolidadas.
    

### Distribuição

Limitação de tamanho.

Dividir um recurso em partes menores e espalhar em vários locais do sistema.

Ex: DNS

### Replicação

Limitação de tamanho.

- Manter cópias de um recurso ou componente disponíveis em diversos locais do sistema distribuído
    
    Aumenta a disponibilidade, permitindo balanceamento de carga e melhor desempenho.
    
- Uma das formas especiais de replicação é o caching
    
    Permite manter uma cópia do recurso o mais próximo do cliente.
    
    O maior problema é manter a consistência das cópias atualizadas, já que a alteração deve ser comunicada a todos os lugares.
    
    Exige aplicação de mecanismo globais de sincronização, difíceis de implementar.
    

## Heterogeneidade

Sistemas distribuídos definidos para operação em ambientes heterogêneos quanto:

- Redes
    
    Internet é um bom exemplo.
    
- Hardware
    
    Diferentes plataformas definem formas distintas de representação de dados e bytes.
    
- Sistemas operacionais
    
    Comunicação de dados e sistemas de arquivos são distintos.
    
- Linguagens de programação
    
    Diferentes formas de representação de dados e de conjuntos.
    
- Diversos desenvolvedores
    
    Componentes implementados precisam de padrões de mensagens para se comunicarem.
    

## Segurança

- Avalia as vulnerabilidades em um sistema distribuído
    
    Visibilidade da informação trocada.
    
    Privacidade dos usuários.
    
- Preocupação aumenta de acordo com a disponibilidade e a abrangência da comunicação (diversos endpoints).
- Deve considerar
    
    Diferentes requisitos, para qual serviço e informações.
    
    Elementos que compõem o sistema.
    

## Tratamento de falhas

Falhas do hardware ou software podem comprometer o sistema.

### Técnicas para tratamento

- Detecção de falhas
    
    Método para descoberta de falhas e gerenciamento.
    
- Mascaramento de falhas
    
    Medidas para minimização do efeito da falha.
    
- Tolerância a falhas
    
    Os elementos devem previamente conhecer os planos de contingência.
    
- Recuperação de falhas
    
    Permitem que o sistema nunca conclua a execução em um estado inconsistente.
    
- Redundância
    
    Réplicas de banco de dados e de serviços.
    

## Concorrência

Os sistemas distribuídos devem prever a interação de vários usuários que podem concorrer pelo mesmo recurso.

- O recurso pode ser o próprio sistema ou rede
- Vários usuários podem querer acesso a um mesmo serviço ou sistema.
- Diferentes threads do mesmo aplicativo concorrerão pelos recursos da máquina.
- Muitos usuários acessando pode comprometer a disponibilidade do sistema.

# Aula II

# Sistemas Distribuídos

## Tipos de modelos
Físicos
- forma explícita de modelo.  
- baseia-se na organização do hardware e sua interligação através de redes.  

De arquitetura
- sistemas pelas tarefas computacionais e de comunicação que são realizadas através de computadores individuais ou clusters.  

Fundamentais
- perspectiva abstrata dos aspectos individuais.
- modelos de interação - consideram estrutura e ordenação da comunicação de seus elementos.  
- modelos de falha - consideram as maneiras pelas quais um sistema pode deixar de funcionar.  
- modelos de segurança - como o sistema está protegido contra tentativas de interferências em seu funcionamento.  

## Evolução dos sistemas distribuídos
Sistemas distribuídos primitivos (início 1980)
- Redes locais - ethernet
- 10 a 100 nós - acesso limitado à internet
- Serviços de impressão, arquivos compartilhados e e-mail
Sistemas distribuídos adaptados para a internet (1990)
- Surgimento da Web e dos mecanismos de busca - google
- Maior escala, conjunto grande e extensível de nós conectados
- Serviços globalizados para corporações, dentro e fora de suas redes
- Grande heterogeneidade de hardware, software e redes
- Demanda por padrões e tecnologias de middleware abertos

## Sistemas distribuídos atuais
Surgimento da computação móvel (smartphones e notebooks)
- equipamentos podem mudar de lugar durante a operação.
- demanda por mais recursos e serviços.
Surgimento da computação ubíqua (onipresente)
- permitem seus integrantes serem incorporados em objetos comuns e no ambiente (casas inteligentes).
Surgimento da computação em nuvem
- conjunto de nós agrupados em arquiteturas agregadas (clusters) para determinada tarefa.

## Padrões arquitetonicos
Arquitetura de camadas lógicas (layer)
- camadas verticais de acordo com o nivel de abstração

![image](https://github.com/user-attachments/assets/5fc03c6c-9188-4b9a-ba29-655e07efe740)


- a plataforma é composta pelas camadas mais baixas, de hardware e software - oferece Suporte para integração com periféricos e rede
- middleware é a camada de software que mascara a heterogeneidade e fornece um modelo de programação conveniente para os programadores
Arquitetura de camadas físicas (tier)
- decomposição funcional e distribuição física das partes de um sistema distribuído
- Ex de arq de 2 a 3 camadas
- cliente -> servidor -> banco de dados

![image](https://github.com/user-attachments/assets/c0dc5dae-52c8-48b6-8a3f-44be2a96c55f)


Arquitetura orientadas a serviços (Web)

![image](https://github.com/user-attachments/assets/1deec76d-129b-4641-a675-985dade439eb)


- desacoplamento de aplicações e seu funcionamento em clientes magros
- comunicação HTTP leva vantagem na comunicação entre redes

## Estilos arquitetonicos
Em camadas.  
Baseado em objetos.  
Baseado em eventos.  
De espaço de dados compartilhado.  

![image](https://github.com/user-attachments/assets/dfc15304-db0d-4550-a8f7-06fcaf61efc1)

## Conceitos de hardware
Multiplas CPUs é a caracteristica comum de sistemas distribuidos.  
Duas categorias  
- multiprocessadores - operam em memória compartilhada
- multicomputadores - não usam memória compartilhada
Comunicação
- realizada através de barramento.
- barramento de alta velocidade ou o próprio barramento de uma rede local.

## Multiprocessadores
- Comunicam-se através de um barramento comum que permite acesso à memória compartilhada.  
- Latência é muito pequena.  
- Concorrência entre os processadores pelo barramento para acesso à memória é um grande problema.  
- Problema pode ser minimizado com uso de memória cache, associada a cada processador.  
- Fortemente acoplado, alto nível de interdependência e coordenação contínua.

## Multicomputadores
- Sistema que conecta vários computadores - através de rede, latência é muito maior.  
- sistemas homogêneos  
    aplicados em soluções que demnandam forte acoplamento  
    Ex: supercomputadores muito caros  
- sistemas heterogêneos  
	aplicado em soluções que permitem fraco acoplamento  
    Ex: computação em nuvem, aplicações perr-to-peer  
- Fracamente acoplado, cada um com seu própri processador, memória e SO.


## O que são sistema operacionais distribuídos?
São SO que atuam como gerenciador de recursos permitindo o seu uso como se fosse um sistema único.  
- esconde as diferenças de harware entre seus integrantes.
- fortemente acoplados  
  aplicados ao gerenciamento de multiprocessadores e sistemas de multicomputadores homogêneos.  
  grande dependência entre os nós que o compõem.  
- fracamente acoplados  
	aplicam-se ao gerenciamento de sistemas de multicomputadores heterogêneos.  
	Ex: NOS (Network OS – SO de rede), que disponibilizam serviços locais a clientes remotos, através de redes de computadores.  

## O que são sistemas operacionais de rede?
Surgiram da necessidade de integrar plataformas heterogêneas em um mesmo sistema.  
- os sistemas operacionais devem possuir protocolos comuns para oferecimento de serviços de comunicação em rede.  
- permitir a administração centralizada dos seus recursos.  
- aplicações distribuídas podem ser construídas sobre esse ambiente.  

![image](https://github.com/user-attachments/assets/6167d4f6-84d3-42dc-a3a3-af799b55b063)

## O que é um middleware?
Modelos anteriores com problemas
- multicomputadores homogêneos não pode gerenciar um conjunto de computadores independentes.
- NOS não oferece uma visão coerente de um sistema único.
A solução é juntar o melhor dos dois
- transparência e a facilidade de uso do primeiro.
- escalabilidade e a abertura do segundo.
Middleware oferece
- camada adicional de software que esconde a heterogeneidade dos computadores e oferece transparência de distribuição.
- geralmente é colocado acima de um sistema operacional de rede e abaixo das aplicações que usarão o ambiente.

![image](https://github.com/user-attachments/assets/d4b50da3-f2a2-40af-a76c-0de4654ae011)

## Classifique os middlewares.
Sistema de arquivos distribuidos (NFS. SMB)
- estratégia introduzida pelas sistemas Unix
- todos os recursos do sistema eram representados em arquivos
Chamadas remotas procedimentais (RPC)
- esconde a complexidade da comunição através da rede
- uma aplicação apenas implementa uma chamada a um procedimento que possui um adaptador local que é trocada em tempo de execução por uma chamada ao procedimento remoto
Objetos distribuídos (CORBA, RMI, DCOM)
- cada objeto remoto implementa uma interface que esconde os detalhes do objeto dos usuários
- a aplicação usa a interface localmente e as mensagens são interceptadas pelo middleware e transmitidas pela rede até o objeto que implementa
Documentos/serviços distribuídos (WS)
- introduzido pela Web, cada recurso possui uma referência única (URL)

## Quais são os serviços oferecidos pelo middleware?
São facilidades de comunicação, serviço de nome, persistência, transações distribuídas e segurança.

## Explique cada um dos serviços distribuídos.
Facilidade de comunicação
- transparência de acesso aos serviços de comunicação da rede.
Serviço de nome
- referência independente de endereço de rede
- provê transparência de localização e permite escalabilidade e replicação.
Persistência
- serviço de armazenamento de dados integrados a SGBDs.
Transações distribuídas
- operações compostas podem ser vistas como unidades atômicas (transações), mesmo sendo executadas em várias máquinas.
- levam o sistema a um estado consistente, tanato na conclusão com sucesso quanto no retorno
Segurança
- provê facilidades para autenticação de usuários, controle de acesso, encriptação e assinatura

## O que o middlewre deve prover?
Um middleware deve prover facilidades para comunicação
- acrescenta um nível extra de abstração na plataforma operacional.
- o protocolo de comunicação define o serviço prestado e as regras para a transmissão de mensagens.
- Tcp.

## Quais são os tipos de comunicação:
A base da comunicação é a troca de mensagens.  
Novos tipos podem ser adotados, de acordo com o paradigma estabelecido pelo middleware.  

## O que é memória compartilhada distribuída?
Processo transparente de solicitação de páginas de memória
- ao detectar que um processo local requisita uma página que está em outro computador
- solicita a cópia da página remota
Dois problemas são concorrentes na solução
- performance
- consistência

## Explique troca de mensagens.
Mensagens sãi unidades básicas de comunicação
- carregam dados trocados entre as partes do sistemas distribuído
- comunicam eventos que permitem sincronizar as ações do sistema
Há várias formas de se estabelecer um ponto de sincronismo
- bloqueio do emissor até o buffer estiver disponível
- bloqueio do emissor até a mensagem ser enviada
- bloqueio do emissor até a mensagem ser recebida
- bloqueio do emissor até a mensagem ser respondida

## Diferencie persistência e transiência
Define se as mensagens serão armazenadas pelo meio ou não.
	
Comunicação persistente
- mensagens são armazenadas pelo serviço de comunicação
- mesmo que um dos comunicantes (ou ambos) esteja indisponível
- isso permite que transmissor e receptor operem em tempos distintos
		
Comunicação transiente
- as mensagens são mantidas apenas na memória das partes comunicantes
- para haver comunicação, transmissor e receptor devem estar operantes
- concluído e confirmado o envio, o emissor pode apagar a mensagem da memória

![image](https://github.com/user-attachments/assets/9650c962-504e-4039-927e-1004232a11e2)

![image](https://github.com/user-attachments/assets/22966138-631f-4235-9aa2-9f7b74a770ae)

![image](https://github.com/user-attachments/assets/54f4afbe-534a-4476-a737-344519f1b322)

## Diferencie sincronismo e assincronismo
Formas como as aplicações se comportarão durante o envio da mensagem.
	
Comunicação assíncrona
- o emissor da mensagem não é bloqueado enquanto a resposta não chega
- pode continuar executando outras tarefas
- na prática, geralmente coloca-se um thread para esperar a resposta
		
Comunicação síncrona
- o emissor fica bloqueado enquanto a confirmação não chega
- uma forma mais comum de sincronismo (operações request/reply) exige que o emissor fique bloqueado até a resposta final do destinatário

![image](https://github.com/user-attachments/assets/39f25c8d-45b6-4f0c-8131-80a8542f5f56)

## RPC: exemplo de interação

![image](https://github.com/user-attachments/assets/4a76572e-0262-44af-ad02-069996cf5d7a)

## O que os sockets oferecem?
A interface de sockets oferece apenas um modelo transiente.
- além disso no TCP as primitivas de solicitação e aceite de conexão bem como de escrita e leitura de stream são bloqueantes
- isso impoe ao par comunicante pontos de sincronismo

## O que são mensagens persistentes? Quais as combinações?
MOM (Message-Oriented Middleware)
- serviço de enfileiramento de mensagens (message-queueing systems)
- provê suporte à comunicação persistente assíncrona
- oferece armazenamento intermediário de mensagens
	
Modo geral de operação
- aplicações comunicam-se através da inserção de mensagens em filas
- cada aplicação tem uma fila específica
- é possível o compartilhamento de uma fila por várias aplicações
	
Isso permite a comunicação fracamente acoplada
- não exige que o destinatário esteja executando quando uma mensagem é enviada para a fila
- emissor e destinatário podem executar em tempos distintos

![image](https://github.com/user-attachments/assets/74751f3f-b844-4792-bd64-ebbba948c220)

## Operações básicas com filas

![image](https://github.com/user-attachments/assets/add74cd1-7004-4753-adec-3fb6c9c2502e)

## Arquitetura de servidores de filas

Elementos comuns às arquiteturas de servidores de filas
- Fila de origem: onde emissor coloca (put) mensagem a ser enviada
- Fila de destino: mantida junto ao receptor, onde mensagens chegam
- Serviço de nomes de filas: referência global para localização das filas
- Gerenciador de filas: administra as filas, interagindo com as aplicações

![image](https://github.com/user-attachments/assets/a68d51c6-db99-47bc-930b-bbf61e5b47b2)

## Filas em ambientes esparsos

Um relay (ou repassador) redireciona mensagens para outros gerenciadores de filas

![image](https://github.com/user-attachments/assets/29ac8c53-8a26-491e-bf6c-6e7e44292367)

## Filas e plataformas diferentes

Um message broker integra diferentes plataformas, convertendo padrões de formatos e conteúdos de mensagens

![image](https://github.com/user-attachments/assets/bb6ad51d-8c19-47e5-947f-21beb9e8216b)

## Sistemas de arquivos distribuídos
Requisitos funcionais
- transparência: acesso, localização, mobilidade, desempenho e escala
- atualizações concorrentes de arquivos
- replicação de arquivos
- heterogeneidade de plataformas (hardware e sistema operacional)
- tolerância a falhas
- consistência, segurança (integridade e confidência) e eficiência
Permitem compartilhamento de dados
- processos podem executar em tempos e locais diferentes
- fornecem visão hierárquica de um name space
Paradigma que precede os SGBDs
- uma das primeiras formas de integração/comunicação em middlewares

## Comparação com outras formas de armazenamento

![image](https://github.com/user-attachments/assets/d3cf6140-7b18-47c0-9219-5d773ad08626)

## Arquitetura comum

![image](https://github.com/user-attachments/assets/ecb22767-f61c-4447-bea6-49ff4da594be)

## Modelos de arquivos distribuídos
Modelo de acesso remoto (ex.: NFS)
- a versão atual do arquivo é mantida no servidor
- o acesso ao arquivo remoto é feito pelo serviço de FS em rede
Modelo de carga/atualização (ex.: FTP)
- cliente obtém uma cópia do arquivo e nela realiza alterações
- depois, a nova versão pode substituir a antiga, no servidor
		
![image](https://github.com/user-attachments/assets/fc5f82a7-32c4-4f08-8da0-056f42d6055a)

## Sun NFS

serviço de acesso remoto e armazenamento de arquivos – Primeiro serviço de arquivos distribuídos amplamente divulgado.  
Tornou-se padrão para muitas outras implementações.  
		
Network File System (NFS) Version 4 Protocol (RFC 7530)

Modelo geral
- o acesso é fornecido aos clientes, através de uma abstração do sistema remoto em seu próprio sistema de arquivos
- clientes acessam um VFS (Virtual File System) que verifica se o arquivo requisitado é local ou remoto
- se for remoto, o cliente NFS intercepta a solicitação e estabelece a comunicação com o servidor, através de RPC (Remote Procedure Call)
- no servidor, as solicitações recebidas são passadas ao servidor NFS que as transforma em operações regulares ao VFS

## NFS: cliente x servidor

![image](https://github.com/user-attachments/assets/c5766485-d223-4918-97fa-2198f32ebc44)

## Montagem de FS remoto 
A forma de operação do NFS consiste em montar o FS remoto
- o servidor remoto mantém o registro do ponto de montagem (em /etc/exports)
- o cliente monta (mount –t nfs) o ponto remoto e cria uma abstração em algum ponto do FS local

![image](https://github.com/user-attachments/assets/a9e54e7a-268a-437e-b00d-c2b76908bcd3)

## Montagem aninhada do NFS
O NFS permite criar hierarquias de abstrações aninhadas, obtendo partes das estruturas em diversos servidores.

![image](https://github.com/user-attachments/assets/bfff7e9f-7deb-414b-8db9-977ca309248c)

# Aula III

## Comunicação entre Processos

## Explique o paradgma cliente-servidor

Cliente: tem comportamento ativo (mestre)  
- Solicita conexão e serviços a um servidor  

Servidor: tem comportamento passivo (escravo)  
- Aguarda solicitações do cliente, através de uma porta previamente registrada e informada à camada de transporte  

## Explique a interface de sockets

TSAP – Transport Service Access Point  
- Ponto de acesso aos serviços prestados pela camada de transporte  

![image](https://github.com/user-attachments/assets/082fb0ef-b326-4faf-85e9-36db991a43cf)

Interface da camada de transporte da Internet  
- Oferece acesso aos protocolos de transporte (TCP, UDP) e rede (IP).  

Provê funções (primitivas) e estruturas de dados de alto nível  
- Extensão das abstrações de operações com arquivos.  
- Um descritor de socket é mantido na tabela de arquivos abertos.  
- As operações para ler e escrever em um socket são semelhantes às realizadas em arquivos (read, write, close, p.e).  

Hoje, praticamente todas as plataformas oferecem suporte e às API´s de linguagens de alto nível para uso de sockets  
- Desde PC (Windows, Mac, Linux), smartphones (Android, IOS), até controladores (Arduino, BeagleBone, Raspberry).  

## Modelo de interação

Comportamento solicitação-resposta (request-reply).  
- Cliente demanda um serviço e fica aguardando a resposta.  
- Servidor recebe a solicitação, processa o pedido e envia resposta ao cliente.  

![image](https://github.com/user-attachments/assets/fbc52e29-ce1a-477d-8553-1d5c9962bfba)

Dois tipos de serviços de transporte.  
- Orientados à conexão (SOCK_STREAM) - protocolo TCP.  
- Não-orientado à conexão (SOCK_DGRAM) - protocolo UDP.  

## Modelo do SOCK_STREAM

![image](https://github.com/user-attachments/assets/95ecb0f3-8da2-4789-ad8d-5894d50563e2)

## Modelo do SOCK_DGRAM

![image](https://github.com/user-attachments/assets/dd10a963-7b13-4f10-bff7-cd30f3451d14)

## O que é Projeto de protocolo de aplicação

TCP e UDP não definem  
- Regras para formato (sintaxe) das mensagens entre aplicações.  
- Significado (semântica) do conteúdo das mensagens.  
- Comportamento de clientes ou servidores.  

O projeto do protocolo de aplicação deve prever isso.  

Alguns serviços (aplicações) criaram definições padronizadas.  
para apresentação de dados.  
- Exemplos: MIME, SSL, XDR (do RPC).  

Em sockets, o formato oferecido é de uma sequência de bytes.  

Há três estratégias distintas para formatos de mensagens.  
- Campos de tamanhos fixos.  
- Campos separados por delimitadores.  
- Pares de parâmetro x valor (com delimitadores).  

## Explique campos de tamanhos fixos

O formato e os tamanhos dos campos são fixos.
- Estrutura fixa do cabeçalho é especificada no protocolo.

### Vantagens
Melhora o desempenho para criação e interpretação.
Regras mais rígidas para implementação das aplicações.

### Desvantagens
Demanda a especificação completa da aplicação antes de defini-lo.
Não suporta dados maiores que o tamanho fixo.
Desperdício de espaço, quando os dados são menores.

Ex.:  

![image](https://github.com/user-attachments/assets/8bf25c16-3f4e-4d86-b543-f40170e76473)


– O primeiro byte é um código de tipo da mensagem.  
– O segundo campo (10 bytes seguintes) é o nome (para esse tipo).  
– O terceiro campo (12 últimos bytes) é o tipo de usuário.  

## Campos separados por delimitadores

Formato pode variar na quantidade e tamanho dos campos.

### Vantagens
Pode se adaptar a diferentes situações de demanda.  
Exemplo: aplicação de transferência de arquivos.  
- Inicialmente envia o nome e o tamanho do arquivo, e a operação desejada.  
- Em seguida, o conteúdo do arquivo.  

### Desvantagem
Pior desempenho para interpretação das mensagens.

Ex.: 1;José;Professor

### Maior problema
Caractere delimitador pode aparecer no conteúdo de um campo (principalmente em conteúdos binários).

### Solução
Byte stuffing

## Pares de parâmetro x valor

Carrega, junto ao valor, o nome do parâmetro.  
Padrão adotado por protocolos orientados a texto da Internet (HTTP, SMTP, etc).

### Vantagens
Permite adaptação de conteúdo e extensões.  
A aplicação pode consumir somente parte dos campos.  

### Desvantagem
Pior desempenho para interpretação das mensagens.  
Ex.: codigo=1;nome=José;tipo=Professor  

### Problema
Caracteres delimitadores podem aparecer no conteúdo de um campo (principalmente em conteúdos binários).

### Solução
Byte stuffing

## Comportamento do cliente e do servidor

Em um protocolo define a funcionalidade esperada para as duas entidades, cliente e servidor.  

Especifica também em quais situações que tipo de mensagem será recebida ou enviada  
Formas de especificação.  
- Descrição textual: as possíveis funções, pré-condições e possíveis resultados são cuidadosamente enumerados
- Diagramas de estados, de atividades, ou pseudocódigo
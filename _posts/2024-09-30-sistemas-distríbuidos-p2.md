---
title: "Sistemas Distribuídos - Resumão para P2"
excerpt: "Resumo Sistemas Distribuídos"
categories:
  - Sistemas Distribuídos
tags:
  - Sistemas Distribuídos
  - Resumo
  - Teoria

toc: true
---

# Aula VII

## Por que sistemas distribuídos usam resolução de nomes?

Porque oferecem:  
- Compartilhamento de recursos  
- Identificação única de entidades  
- Referência de localidades  

## O que é resolução de nomes?

Processo de identificação de uma entidade através de seu nome.

Geralmente realizada através da consulta a um servidor de nomes.

## O que são nomes?

Descrevem entidades: computadores, usuários, impressoras…

Referenciam endereços: endereço é um tipo especial de nome que se refere a um ponto de acesso de uma entidade.

Identificador: referência única de uma entidade.

Fornecem transparência de localização:
- um ponto de acesso pode ser modificado, mas seu nome mantido para o sistema.
- o servidor de nomes deve manter a referência atual dos pontos de acesso.

## O que são Names Spaces

Forma como os nomes estão organizados (grafos).

![image](https://github.com/user-attachments/assets/a45f09dd-59cd-44a9-9f5b-7b5d749ce273)

## Explique a organização hierárquica

Existem 3 níveis.

### Nível global

Nós de mais alto nível (nó raiz e seus filhos diretos).  
Estrutura normalmente estável (modifica-se muito pouco).  
Descrevem organizações ou grupos de organizações.  

### Nível administrativo

Abaixo do nível global.  
Alteram-se com pouca frequência.  
Referenciam grupos de entidades de uma mesma organização ou unidade administrativa (exemplo: departamentos de uma organização).  

### Nível gerencial
 
Alteram-se com maior frequência.  
Representam entidades, como hosts ou sistemas de arquivos.  

## DNS

Domain Name System - serviço de nomes da Internet.

![image](https://github.com/user-attachments/assets/68a17f1e-e736-48c7-970b-72b70fb2b206)

## Resolução de nomes

### Resolução iterativa

O nome é resolvido através de diversas iterações de consulta, partindo do nível global ao nível gerencial.

Ex:

![image](https://github.com/user-attachments/assets/fe600bae-f92d-4970-a203-45df41c6ec2b)

ftp:// -> name space -> porta aplicação.  
ftp.cs.vu.nl -> DNS host (IP).  
/pub/globe/index.txt -> caminho FS.  

## Servidores de nomes

As implementações mais difundidas são:

- DNS (Domain Name System): instituído pela RFC 1034, é o serviço de nomes padrão para a Internet.
- LDAP (Lightweight Directory Access Protocol): implementação aberta inspirada no modelo de serviço de diretórios X.500 DAP para uso na Internet.
- NDS (Novell Directory Services): implementação do serviço de diretórios da Novell, baseada no X.500 DAP.
- Active Directory: implementação padrão do LDAP pela Microsoft.

## X.500 DAP ( Directory Access Protocol)

Padrão da ISO/ITU que define um modelo independente de plataforma para o serviço de diretórios.

Diretório: banco de dados com informações sobre objetos e entidades, baseadas em atributos e organizadas em forma de árvore.

- DIB (Directory Information Base)  
Banco de dados com os registros do serviço de diretório.  

- DIT (Directory Information Tree)  
Define a organização hierárquica dos objetos  

- Objetos  
Descritos pelas entradas no diretório e possuem atributos  

## Hierarquia X.500

Diferentes classes para objetos, para cada nível  

(Root)  
DC Domain Component  
C Country  
L Locality  
O Organization  
OU Organizational Unit  
CN Common Name  

Regras de acesso (ACL – access control lists)  
São definidas entre objetos, através de seus atributos

## O que é LDAP?

Lightweight Directory Access Protocol.

Desenvolvido inicialmente para ser cliente do X.500.  

O X.500 impunha uma implementação complexa de protocolo, para
operar sobre a pilha ISO/OSI.

O LDAP foi adaptado para operar sobre a pilha TCP/IP e tornou-se um
padrão de fato para a Internet.

Sua versão 3 é descrita pela RFC 2251

## Exemplo de entrada LDAP

![image](https://github.com/user-attachments/assets/6e46416d-f0d2-4b97-b8ff-489560bd91d7)

## Exemplo de hierarquia LDAP

![image](https://github.com/user-attachments/assets/8894736f-1469-44d3-a55b-2183ef29bf80)

## O que é LDIF?

LDAP Data Interchange Format (RFC 2849).

Formato de intercâmbio de informações para o LDAP.

Descreve o diretório e suas entradas em formato texto.

Sintaxe:

![image](https://github.com/user-attachments/assets/6b3b56af-9581-436e-bd57-f2cc5c1c7f30)

## Exemplo LDIF com 2 entradas

![image](https://github.com/user-attachments/assets/3902b9b4-00c9-4f4d-a19e-b260bbb274ed)

# Aula VIII

## O que é transação distribuída?

É uma sequência bem definida de operações e eventos que podem fazer uso de diversos recursos compartilhados.

- Protege o acesso simultâneo a recursos compartilhados entre processos concorrentes.

- Permite o processo acessar e modificar múltiplos itens de dados como uma operação atômica

- Se um processo desistir no meio da transação tudo deve ser reestabelecido ao ponto inicial antes da transação.

## Como funciona o modelo de transações?

Abstraído do mundo dos negócios.

Qualquer processos pode anunciar o início de uma transação.

O processo que iniciou a transação pode:

- Solicitar que todos se comprometam com o trabalho (commit).

- Situação revetida caso um processo discorde (rollback).

## Quais são as primitivas de transações

![image](https://github.com/user-attachments/assets/d17a19c9-686e-4d8a-a868-86a68853fa5a)

Escopo da transação:
- BEGIN_TRANSACTION e END_TRANSACTION
- Operações entre elas formam o corpo da transação

Todas as operações do corpo da transação devem ser executadas, ou
nenhuma deve ser executada

## Explique rapidamente as propriedades de transações

"tudo ou nada" -> principal propriedade, que possui quatro qualidades (ACID).

- Atômica: transações são indivisíveis.
- Consistente: o sistema deve ser mantido em estado consistente.
- Isolada: uma transação não pode interferir em outra transação.
- Durável: os efeitos de uma transação são permanentes.

## Classificação de transações

### Flat Transactions

Uma série de operações que satisfazem as propriedades ACID.

Sua limitação é não permitir que resultados parcias sejam "commited" ou mesmo "abortados".

### Transações aninhadas

Podem ser aninhadas através da definição de sub-transações (mais altas podem criar foks novos para os filhos rodarem).

Quando uma transação inicia-se:

- recebe uma cópia privada de todos os dados de todo o sistema para manipular como quiser.

- Se a transação é abortad seu universo privado é descartado
- Se ela chega ao commit seu universo privado sobrescreve o do pai.

### Transações distribuídas

Vista como uma transação flat e indivisível que opera dados distribuídos.

Principal problema é definir algoritmos separados para manipular o controle de acesso aos dados e realizar (commit) a transação.

![image](https://github.com/user-attachments/assets/5302590a-aea2-4655-bc9a-0de30782dc69)

## Explique a implementação de transações

### Espaço privado

Quando um processo inicia uma transação, recebe um espaço privado de trabalho.

- Se prever o acesso a diversos arquivos, copiar tudo para seu espaço privado pode ser impossível ou pouco aconselhável.
- Se o processo apenas fará leitura em um arquivo (sem alterá-lo), não precisará de uma cópia privada.
- Se necessitar escrever em um arquivo, o processo pode manter em sua área privada apenas o mapeamento (índice) dos blocos do arquivo.
- Dessa forma, fará a leitura dos blocos e, se alterar algum deles, somente estes serão alterados no disco.

### Writeahead log

Alterações a serem realizadas em um arquivo são anotadas em um registro histórico.

Somente depois de confirmada a gravação do log que a alteração pode ser realizada no arquivo.

Ex:

![image](https://github.com/user-attachments/assets/442cdd8d-e3e4-4ab2-b5b0-a82efe02cc02)

- Todas as alterações sofridas em estruturas de dados (ou outros recursos) do sistema são armazenadas no registro histórico.

- Se uma transação tiver que ser abortada antes de seu fim, todas as alterações registradas (efetuadas por suas operações) podem ser desfeitas e o estado inicial das estruturas (e recursos) restabelecido (rollback)

## Controle de concorrência

Trata dos requisitos de consistência e isolação.

### Consistência

Permitir que diversas transações executem simultaneamente acessos a uma coleção de itens de dados, mantendo-os em estado consistente.

Execução sequencial das transações sobre o conjunto de dados.

### Escalonador (scheduler)

Responsável pelo controle da concorrência.

Determina qual transação tem permissão para passar operações de leitura ou escrita ao gerenciador de dados (data manager) a cada momento.

### Isolação e Consistência

Podem ser garantidas pelas operações individuais de leitura e escrita realizadas pelo gerenciador.

### Gerenciador de transações (transaction manager)

Responsável por garantir a atomicidade das transações

Processa as primitivas das transações, transformando-as em chamadas ao escalonador.

![image](https://github.com/user-attachments/assets/7fe172fc-edc1-4019-a7c6-72fba1008ef6)

Pode ser utilizado para acessar diversos escalonadores em um ambiente distribuído.

![image](https://github.com/user-attachments/assets/e6ce33c1-e10c-4bdd-8ad6-dbb066c91238)

## Serialização

Impõe uma ordem de execução, isolando transações da execução simultânea e garantindo a execução sequencial de transações (só inicia se outra encerrar).

Duas abordagens p/ solução

Pessimista é mais utilizada e admite que problemas de concorrência irão ocorrer

Utiliza o bloqueio dos recursos (locking) como forma preventiva de evitá-los.

Ex:

![image](https://github.com/user-attachments/assets/5aa8d65d-6756-48cd-912f-0170c8bbf26c)

## Bloqueio em duas fases

Two-phases locking

- Quando um processo necessita de um recurso solicita o bloqueio do mesmo.

- Quando prevê não mais utilizá-lo, realiza sua liberação.

Sendo assim, o algoritmo prevê duas fases distintas:

- growing phase: fase onde ocorre o bloqueio de recursos pelo  processo.

- shrinking phase: fase na qual os recursos são liberados pelo  processo.

![image](https://github.com/user-attachments/assets/375bcd93-34c1-4efe-a11b-b7a95a631560)

![image](https://github.com/user-attachments/assets/5096924a-1fb8-4534-8cbe-468beb11c593)

## Gerenciamento de transações em EJB

Controle de transações resumi-se à demarcação de transações (quando será iniciada e concluída).

Várias formas de demarcar transações (cliente - comuns, servlets, beans - ou servidor - no container, declarações no DD, ou no bean, APIs como JTA, JDBC ou JMS).

## Estailo de demarcação

### BMT (Bean-Managed Transactions)

Total controle sobre o início e o fim das transações.

Nas outras modalidades é necessário ter todo o bean dentro (ou fora) de uma transação.

### CMT (Container-Managed Transactions)

Maior simplicidade.

Mais seguro: evita a introdução de código que pode provocar deadlock e outros problemas similares.

Tunnig de transações sem alterar uma linha de código.

### Demarcadas pelo cliente

Vantagem: controle em relação a falhas de rede.

Desvantagem: transação muito longa - ineficiente.

## CMT – Container Managed Transactions

Controle de transações totalmente gerenciado pelo container.

Não permite o uso de métodos commit() e rollback() de java.sql.Connection ou javax.jms.Session dentro do código.

Única forma de controlar transações em Entity Beans.

## Políticas transacionais - atributos

Os vetores suportados são:

NotSupported
- Indica que o método não suporta transações.

Supports
- Indica que o método suporta transações.

Required
- Indica que o escopo de uma transação é requerido pelo método.

RequiresNew
- Indica que o método requer uma nova transação.

Mandatory
- Indica que o método só pode ser chamado no escopo de uma transação do cliente.

Never
- Indica que o método nunca pode estar dentro de uma transação.

## Serviço de transações

Servidores J2EE oferecem serviço de transações distribuídas
CORBA: Object Transaction Service (OTS).

– Pode ser obtido através do serviço de nomes (via JNDI ou COS Naming).

Clientes também podem obter o serviço de transações do recurso que estão utilizando (se houver).

– Bancos de dados (através de JDBC).
– Sistemas de messaging (através de JMS).

Para ter acesso a esses serviços, existem APIs.

– JDBC ou JMS, para serviços do recurso utilizado.
– JTS ou JTA, para acesso ao OTS (distribuído).

Beans também podem realizar controle declarativo.

## JTS e JTA

JTS - Java Transaction Service  
é um mapeamento java-CORBA da especificação Object Transaction Service.

- Usado por fabricantes de containers.

JTA - Java Transaction API  
é uma especificação de interfaces para o sistema de transações.

- Suporte por parte do container é obrigatório.

## Tipos de Beans 

### Transientes (session beans)

- Fornecem suporte à sessões de clientes, durante transações com servidores de aplicação Java EE.

### Mensagens (message-driven beans)

- Realizam a comunicação via troca de mensagens entre cada parte que compõe o sistema distribuído

### Persistentes (entity beans)

- Representam os dados armazenados (persistidos) em servidores de
bancos de dados

## Session Beans

Encapsulam a lógica do negócio.

O session bean realiza o trabalho para o cliente, escondendo a complexidade de executar as tarefas de negócio no lado servidor

Tipos de session beans

### Stateful Session Beans

- As variáveis de instância representam uma única sessão do cliente
- São transientes, ou seja, são descartados quando a sessão terminar

### Stateless Session Beans
- O estado (valores de instância) não é retido depois de uma  chamada.
- Estado descartado assim que o método termina

### Singleton Session Beans
- São instanciados um por aplicação e existem enquanto ela executar.
- Podem ser compartilhados entre diversas sessões de clientes.

## Message-drive Beans

Um message-driven bean é um EJB que permite aplicações Java EE processarem mensagens assíncronas.

- Geralmente atua como um JMS message listener (Como um event listener, mas recebe mensagens no lugar de eventos).

- Podem também processar outros tipos de mensagens, além de JMS.

- Diferem-se dos session beans pois não são acessados via interfaces.

- Operam transações de múltiplos clientes e não retêm estados (stateless).

# Aula IX

## Requisitos de dependabilidade em SD

Disponibilidade: mede quanto o SD está pronto para ser usado imediatamente, probabilidade de um SD estar opertante.

Confiabilidade: mede quanto tempo um SD pode operar continuamente, sem a ocorrência de falha.

Segurança: capacidade de um SD nçao gerar algo catastrófico quando falhar na operação.

Manutenabilidade: facilidade de se reparar um SD ao apresentar falha. Boa manutenabilidade implica em maior disponibilidade.

## Exemplo disponibilidade VS confiabilidade

Se um sistema parar por um milissegundo a cada hora -> disponibilidade será alta e confiabilidade baixa.

Se um sistema nunca falha, mas fica desligado por duas semanas todo mês de agosto -> sua confiabilidade será alta e disponibilidade de apenas 96%.

## Defeito VS Erro VS falha

Defeito: consequência de um estado de erro do SD (não cumpre promessa).

Erro: constitui parte do estadp de um SD originado por uma falha.

Falha: trata-se da causa que originou o erro.

## Tipos de falhas

Transientes: falhas que ocorrem apenas uma vez e então desaparecem.

Intermitentes: não definem um padrão exato de ocorrência e são imprevisíveis.

Permanentes: não podem ser consertadas e normalmente implicam em danos irreparáveis em componentes.

## Modelos de falhas

Falha por quebra (crash): abrupta, normalmente associadas ao hardware e nada pode ser feito senão reiniciada.

Falha por omissão: quando um servidor falha ao responder uma requisição.

- Omissão da requisição: o servidor nem chega a receber a solicitação do cliente (perdida).

- Omissão da resposta: a resposta já foi perdida ou nem ter sido encaminhada à rede (servidor acha que enviou).

Falha de sincronismo: resposta em ritmo alterado pelo servidor (responder cedo ou tarde demais).

Falha na resposta: resposta errado do servidor, pode ser por valor incorreto ou falha de transição de estados (reação inesperada).

Falha arbitrária: servidor produz resposta que nunca deveria ser produzida, geralmente gerado por código malicioso e pode ser confundida com outras falhas.

## Redundância e resiliência de processos

Redundância de informação: uso de informação extra para recuperar erros em dados (código Hamming).

Redundância de corrência: ação pode ser repetida durante a execução de uma transação, caso necessário.

Redundância física (hardware ou software): adição de equipamento ou processos extras que permitem o sistema suportar o mau funcionamento de algum componente individual.

## Agrupamento de processos

Processos idênticos são agrupados e podem receber mensagems multicast - podem ser dinâmicos e um processo pode participar de mais de um grupo.

Estrutura de um grupo

- Grupo plano: processos têm papéis iguais e decisões são tomadas coletivamente.

- Grupo hierárquico: um dos processos é considerado coordenador e fará uma papel diferente dos outros.

![image](https://github.com/user-attachments/assets/6153cdeb-591f-4dcc-879e-235ecfc1bd94)

## Controle de grupo

Modelo centralizado: servidor de grupos administra os grupos (ponto único de falha do SD) e a replicação é baseada em um principal (primary-based - estruturação hierárquica - coordenador representa a comunicação com outros processos).

Modelo distribuído: todos os processos do grupo mantém informações sobre ele (pedidos devem ser enviados a todos e é 'k fault tolerant') e possui replicação de escrita.

## comunicação confiável

Permite enviar/tratar falhas por quebra, omissão, sincronismo ou arbitrária.

Comunicação ponto-a-ponto com TCP, protocolo de transporte confiável e mascara falhas (retransmite falhas perdidas).

Problemas com TCP: a conexão pode se encerrar abruptamente

## SRM

Scalable Reliable Multicasting

Só são comunicadas as mensagens faltantes, o que já reduz a demanda de tráfego na rede e evita que mais de um membro do grupo reclame a mesma mensagem.

![image](https://github.com/user-attachments/assets/812c54ed-573d-4545-85c6-7ee6e2e21712)

## Estratégia hierárquica

O coordenador de cada subgrupo é responsável por comunicar eventuais mensagens não recebidas pelos membros do grupo.

![image](https://github.com/user-attachments/assets/4efb4179-d224-4be5-ac8b-ebc152614ea1)

## Comunicação multicast

### Multicast atômico

Todos devem receber a mensagem.

Sincronismo virtual

- A camada de comunicação do SD deve segurar a mensagem até que todas as suas parceiras notifiquem o recebimento.

- A partir daí, todas as entidades podem passar a mensagem para a camada superior (aplicação).

![image](https://github.com/user-attachments/assets/5e44c26a-34a9-49b2-9885-df0259ae4db6)

### Ordenação de mensagens multicast

4 abordagens.

- Multicast desordenado confiável: garante-se que as mensagens cheguem, mas não garante a ordem.

- Multicast ordenado em filas (FIFO) confiável: a camada de comunicação é obrigada a entregar as mensagens na mesma ordem que forem enviadas.

- Multicast ordenado por causalidade e confiável: a entrega das mensagens mantém a relação de causalidade entre as diferentes operações do sistema.

- Multicast totalmente ordenado: independentemente da estratégia utilizada para encaminhamento, exige que as mensagens sejam entregues a todos os membros na mesma ordem.

## Commit distribuído

Um problema para commit em SD é garantir que uma operação seja realizada por cada membro do grupo, ou nenhum deles.

A solução é eleger um coordenador que ordena que os processos realizem, ou não, as operações em questão.

## Commit em duas fases

### Fase 1 - Votação

- O coordenador envia uma mensagem 'VOTE_REQUEST' para todos os participantes.

- Quando o participante recebe a mensagem, responde:

  'VOTE_COMMIT' – se estiver preparado para fazer o commit local da
  transação.  
  'VOTE_ABORT' – caso contrário

### Fase 2 - Decisão

- O coordenador obtém os votos e responde a todos.
  
  'GLOBAL_COMMIT' – se todos votarem favoráveis ao commit.  
  'GLOBAL_ABORT' – se apenas um deles votar por abortar.

- Cada participante espera a resposta.

  Se 'GLOBAL_COMMIT', executará localmente o commit da transação.  
  Se a for um 'GLOBAL_ABORT', a transação local é abortada.

![image](https://github.com/user-attachments/assets/98b2bdcb-ba77-4376-874f-8246e0d21399)

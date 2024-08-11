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

# Sistemas Distribuídos

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
    
    Vários usuários podem querer acesso a um mesmo serviço ou sistema.
    
    Diferentes threads do mesmo aplicativo concorrerão pelos recursos da máquina.
    
    Muitos usuários acessando pode comprometer a disponibilidade do sistema.
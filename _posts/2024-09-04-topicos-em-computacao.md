---
title: "Tópicos em computação - grupos e seus temas"
excerpt: "Resumo dos tópicos abordados pelos grupos"
categories:
  - Tópicos em computação
tags:
  - Tópicos em computação
  - Blockchain

toc: true
---

# Blockchain e Criptomoedas

Apresentação Berna e Aranha - 04/09

## Blockchain

- é um sistema de banco de dados avançado
- permite o compartilhamento transparente e seguro de informações de uma rede
- dados armazenados em blocos interligados que formam uma cadeia cronológica imutável (informações não podem ser alteradas nem excluídas)
- tal mecanismo é usado para monitorar transações (pedidos, pagamentos e contas)

## Origem

- origem nos anos 90
- ideia de criar uma rede de blocos protegidos por meio de criptografia, onde ninguém pudesse adulterar
- atualizado com árvores Merkle para aumentar efetividade -> acúmulo de documentos em um só bloco
- a partir de 2008 começou a ganhar popularidade

## Apartir de 2008

Satoshi Nakamoto -> não sabe se é pessoa ou organização de fato
aplicou o conceito digital no bitcoin

## Principais características

### Descentralização

- Distribui o controle e a tomada de decisão por toda a rede
- Reduz a dependencia de autoridades centrais
- Aumenta transparencia e resistencia a falhas

### Imutabilidade

- Transações não pode ser alteradores e excluídas
- Garante integridade e confiabilidade

### Consenso

- Transações só são validades e registradas após a concordância da - Maioria dos participantes da rede
- Assegura legitimidade e concordância coletiva sobre os dados

## Tipos de Blockchain

Publicas -> acesso aberto, qualqer pessoa pode participar e validar transações (bitcoin)

Privadas -> controlada por uma organização com acesso restrito

Híbridas -> combinação do público e privado, quais dados são públicos e quais não

Consórcio -> gerenciadas por organizações que colaboram e compartilham a manutenção da rede

## Impotância

- operação de forma descentralizada
- elimina a necessidade de intermediários confiáveis, reduzindo riscos de fraude e pontos únicos de falha.
- torna transações mais transparentes, seguras e eficientes -> aplicável em diversos setores da economia

Hyperledger Fabric: Framework modular e flexível para soluções empresariais privadas, foco em escalabilidade e segurança.

Ethereum: Plataforma descentralizada popular para a criação de aplicações públicas e contratos inteligentes.

Corda: Projetada para o setor financeiro, facilita transações diretas com altos níveis de privacidade.

Quorum: Variante do Ethereum adaptada para ambientes privados e consórcios empresariais, com melhorias em desempenho e privacidade.

## Aplicações em diferentes setores

### Energia

facilita a comercialização de energia entre pares
permite que proprietários de placas solares vendam excedentes diretamente a consumidores próximos através de plataformas automatizadas e seguras

### Financeiro

aprimorar processos de pagamentos e liquidações, tornando-os mais rápidos e confiáveis
otimização de transações e redução de processos manuais complexos

### Mídia e entretenimento

gerencia e protege direitos autorais, assegurando competência justa dos artistas
simplifica processo de verificação e transferência de direitos através de registros imutáveis

### Varejo

monitoramento e autenticação de produtos ao longa da cadeira de suprimentos
autentiicdade das mercadorias e aumento da confiança dos consumidores por meio de rastreabilidade transparente

## Conclusão

blockchain representa uma revolução na forma como transações e dados são gerenciados
oferecem segurança, transparência e eficiência
suas diversas aplicações mostram o seu potencial transformador
impulsiona inovação e confiança em processos digitais globalmente

# Bioinformática

Apresentação Matheus Gomes e Ivo - 11/09

## O que é

Campo interdisciplinar que combina biologia, ciência da computação e matemática para analisar e interpretar dados biológicos.

Sua história começa na segunda metada do século XX, impulsionada pelo avanço das tecnologias computacionais e pela necessidade de gerenciar grandes volumes de dados biológicos.

## Breve história

Pioneiros como Margare Dayhoff (1950 - 1960) começaram a aplicar métodos computacionais para comparar sequências para comparar sequências de proteínas.

Com o avanço dos computadores e dos métodos de sequenciamento de DNA (1970 - 1980), a bioinformática focou na análise de sequências biológicas.

Projeto Genoma Humano (1990) impulsionou o campo ao gerar grandes volumes de dados genômicos, necessitando de novas ferramentas de análise.

Com a chegada das tecnologias de sequecimaneto da nova geração nos anos 2000 a bioinformática se expandiu para outras "ômicas" como transcriptômica e proteômica, sendo hoje essencial para a biologia, medicina personalizada e desenvolvimento de novas terapias.

> marcos importantes: Projeto Genoma Humano, desenvolvimento de algoritmos para comparação de sequências.

## Aplicações

### Genômica e medicina personalizada

Análise do genoma individual para identificar predisposições genéticas a doenças e personalizar tratamentos.

Ex: Testes genéticos para prever resposta a medicamentos (farmacogenômica), tratamentos direcionados para câncer com base em mutações específicas.

### Agricultura e biotecnologia

Aplicação de técnicas de bioinformática para melhoramento genético de plantas e animais.

Ex: Identificação de genes para resistência a doenças em plantas e desenvolvimento de culturas geneticamente modificadas.

Benefícios: Aumento da produtividade agrícola, resistência a pragas e condições climáticas adversas.

### Descoberta e desenvolvimento de medicamentos:

uso de simulações e modelagem molecular para identificar e otimizar compostos candidatos a medicamentos.

Ex: Modelagem de proteínas para encontrar sítios de ligação de drogas e prever interações moleculares.

benefícios: Aceleração do desenvolvimento de medicamentos, redução de custos com ensaios laboratoriais.

## NCBI

O NCBI (National Center for Biotechnology Information) e é um dos principais repositórios globais de informações biológicas e genômicas

Fundado em 1988, o NCBI fornece acesso a uma vasta coleção de bancos de dados, como o GenBank para sequências de DNA e RNA, e o PubMed para literatura científica.

Oferece o BLAST (Basic Local Alignment Search Tool) que permite a comparação de sequências biológicas para identificar similaridades funcionais e evolutivas.

NCBI é essencial para pesquisadores e profissionais da área, pois facilita o acesso a dados genômicos e ferramentas de análise, impulsionando descobertas científicas, avanços em biotecnologia, e o desenvolvimento de novas terapias na medicina personalizada.

## Ferramentas e tecnologias

### Específicas

BLAST: Comparação de sequências para encontrar similaridades (identificação de genes, análise de homologia).
ClustalW: Alinhamento múltiplo de sequências (estudos filogenéticos, análise evolutiva).
Bowtie: Alinhamento rápido de sequências de DNA (análise de dados de sequenciamento, mapeamento de reads).

### Programação

Conjuntos de ferramentas de software desenvolvidas em diferentes linguagens de programação (Python, Java, Perl) para manipulação e análise de dados biológicos.
Servem para automação de processos bioinformáticos, manipulação de sequências de DNA, RNA, e proteínas, acesso a bancos de dados biológicos...

## Desafios atuais na bioinformática

Volume crescente de dados biológicos, exigindo infraestrutura avançada para armazenamento e análise.

Integração de dados heterogêneos e a falta de interoperabilidade entre ferramentas dificultam a análise e interpretação precisas.

Necessidade crítica de garantir a segurança e privacidade de dados genéticos, especialmente em contextos colaborativos.

## Futuro

Tedências que incluem o uso crescente de inteligênica artificiall e machine learning para análise de big data, impulsionando a medicina personalizada com tratamentos individualizados baseados em perfis genômicos.

Tecnologias de sequenciamento de terceira geração, como o sequeciameto por nanopore, oferecem leituras longas e em tempo real, com potencial de reduzir custps e expandir o uso clínico.

Dispositivos portátiveis estão possibilitando análises genômicas em campo, ampliando as aplicações da bioinformática em áreas como agricultura, conservação e saúde pública.
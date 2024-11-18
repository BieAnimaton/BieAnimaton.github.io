---
title: "Robótica P2 Perguntas Filtradas"
excerpt: "Robótica P2 Perguntas Filtradas"
categories:
  - Robótica
tags:
  - Robótica
  - Perguntas
  - Respostas

toc: true
---

# Aula 9 e 10

## Defina: medir, mensurando, indicação e indicação direta.

- Medir: procedimento experimental através do qual o valor momentâneo de uma grandeza física é determinada como um múltiplo ou fração de uma unidade.

- Mensurando: é o fenômeno sobreo  qual se deseja expressar a medição, no caso, é temperatura (ex 1.a).

- Indicação: é a quantidade/unidade do mensurando, no caso, ºC (ex 1.b).

- Indicação direta: é a medidade indicada (unidade) pelo sensor, no caso, mV (ex a.c).

## O que é range?

É a faixa de variação do mensurando à qual o sensor se aplica, no caso, para o sensor N é -270ºC a 1300ºC e K é -270ºC a 1372ºC (ex 1.d).

## O que é sensibilidade constante?

É a relação direta entre a resposta e o estímulo de um sensor, para uma determinada faixa (ex 1.e).

![image](https://github.com/user-attachments/assets/ae999b3d-50ff-40df-b3dc-d96db817ca54)

![image](https://github.com/user-attachments/assets/b9a6b88e-8a6b-4659-9199-52aa8802c417)

![image](https://github.com/user-attachments/assets/bfe6a82c-95ff-4dcc-8562-af764048d71a)

## Explique o funcionamento dos termopares para a medição de temperatura. Apresente um esboço.

Quando dois metais diferentes são unidos em uma junção, a diferença de temperatura entre o ponto da união e a outra extremidade dos condutores faz surgir uma tensão decorrente da força eletromotriz. Cria-se o ponto de medição e o ponto de referência.

![image](https://github.com/user-attachments/assets/c2c8767e-c890-4688-8f8f-34e6c41cbae1)

## Que vantagem a ligação a 3 fios apresenta em relação à ligação a 2 fios no uso de Pt-100? Explique.

A vantagem é a menor influência da temperatura ambiente nos condutores e maior precisão em grandes distâncias entre o elemento sensor e o circuito de medição.

## O que são e para que são utilizados os cabos de extensão e de compensação em termopares?

Cabos de extensão e de compensação em termopares servem para conectar o termopar ao sistema de medição sem alterar a precisão da leitura de temperatura.

O cabo de extensão é feito dos mesmos materiais do termopar para mantr as mesmas propriedades térmicas até o ponto de medição. Já o cabo de compensação utiliza materiais de composição semelhante para reduzir custos sendo eficaz dentro de uma faixa de temperatura.

## Explique, em linhas gerais, os princípios de Seebeck sobre termopares.

Elétrons livres trafegam entre metais diferentes dependendo da temperatura. A extremidade mais quente excita os elétrons dessa região fazendo com que se desloquem para o lado frio, gerando uma DDP entre as extremidades e isso fornece as medidas de temperatura.

## Explique, em linhas gerais, o efeito de Peltier sobre termopares.

Se uma corrente elétrica I flui na junção entre dois metais diferentes, o calor é gerado ou absorvido nesse local em quantidade proporcional à corrente.

## Um potenciômetro linear apresenta resistência máxima de 100k Ω e tem 12 cm de comprimento. Calcule quanto a tensão de saída varia a cada 1 cm de deslocamento da haste deslizante, para uma tensão de entrada de 15 v.

E = 15 V  
D = 12 cm  
d = 1 cm  

![image](https://github.com/user-attachments/assets/61acd6ae-d8b3-4f78-a103-0361d4b267e4)

## Um encoder possui um único canal, com 100 estrias, no qual realiza leituras a uma frequência de 2 kHz. Qual é a velocidade angular do rotor, em RPM, para esses valores?

N = 100 estrias.  
f = 2kHz = 2000 Hz.  

![image](https://github.com/user-attachments/assets/30d84bfb-374b-4098-8e02-69a11be7dea0)


## Explique como um tacogerador consegue registrar a velocidade angular de um rotor.

O tacogerador (dínamo taquimétrico) registra a velocidade angular de um rotor ao gerar um sinal diretamente proporcional à rotação. Um imã permanente cria um campo magnético fixo no estator, e, conforme o rotor gira com suas espiras, ele corta esse campo magnético. A rotação do rotor é então captada pelo movimento relativo entre o campo magnético e as espiras, permitindo que o sistema registre a velocidade de rotação e depois pode ser convertida para tensão.

## Um acelerômetro pode ser utilizado para medições de velocidade e de posição de um objeto? Como?

Sim, consiste de um transdutor que transforma aceleração (energia mecânica) em uma tensão elétrica analógica (energia elétrica).

## Qual é o princípio de funcionamento de um acelerômetro de deslocamento? Forneça um esboço para ilustrar.

É um tipo de acelerômetro mecânico que mede a alteração da inércia sobre uma massa (possui uma parte mecânico em seu interior) e como a aceleração é proporcional a essa força, pode ser obtida e fornecida pelo sensor.

Quando o corpo acelera, a força -m.a se opõe à força de restauração elástica e a massa m adota uma nova posição, sendo medida. Acompanha também um liquído para estabilizar oscilações.

## Em um acelerômetro de deslocamento, a massa de 1,5g do corpo de referência deslocou-se 0,5 cm. Sabendo-se que a constante de mola é de 0,3 dynas/cm, calcule a aceleração registrada pelo sensor.

m = 1,5 g.  
X = 0,5 cm.  
K = 0,3 dynas/cm.  

![image](https://github.com/user-attachments/assets/a825da84-dc71-45a9-a9d5-125c20fa882b)

![image](https://github.com/user-attachments/assets/01c4de27-eb93-44a6-845a-d511ef3129a9)

# Aula 11

## Explique os conceitos básicos

- Planta: itens de máquina que funcionam em conjunto para realizar operação.

- Processo: operação ou sequência de operações que implicam em mudança de estado.

- Sistema: combinação de componentes que atuam em conjunto para realizar um objetivo.

---

- Variável Controlada: quantidade medida para efetuar indicação ou controle do processo.

- Variável Manipulada: grandeza operada para manter a variável controlada no valor desejado.

- Set Point: valor desejado que serve como referência da variável controlada.

---

- Distúrbio: sinal que afeta a variável controlada.

- Desvio: diferença entre valor desejado e variável controlada.

- Ganho: quociente entre a taxa de mudança na saída e na entrada.

## O que é controle?

Manutenção de uma variável com um valor (fixo ou variante) para o  valor desejado (set point).

## Diferencie malha aberta e malha fechada

- Aberta: somente a entrada (comando) define o comportamento do controlador, responde com atuação, sem sensor e sem realimentação.

- Fechada: controlador considera a entrada e desvios, sensor monitora a saída e fornece um sinal de realimentação.

## Diferencie ação direta e indireta.

- Direta: ou normal, aumento da variável de processo provoca um aumento no sinal de saída. Ex: acelerar carro, aumenta velocidade.

- Indireta: ou reversa, aumento da variável de processo provoca um decréscimo no sinal de saída. Ex: frear carro, reduz velocidade.

## Explique os tipos de controle

- liga-desliga: dois estados para atuar, aberto e fechado.
- proporcional: ganho proporcional ao erro medido.
- integral: sinal de correção integrado no tempo e reação se baseia na acumulação de erros recentes.
- derivativo: fornece uma correção antecipada do desvio e diminiu tempo de resposta.

## Diferencie os dois tipos de sensores

### Medida

- Proprioceptivos: medem valores internos do robô (velocidade, carga, tensão).
- Exteroceptivos: medem valores externos (distância, luminosidade).

### Energia

- Passivo: energia vem do ambiente (sensor de temperatura, microfone).
- Ativo: emitem energia para o ambiente e mudem sua reação (sensor ultra-som).

# Aula 13

## Defina os tipos de controles adaptativos.

Contexto local: percepção local do ambiente (obstáculos, inclinação) e cada robô móvel tem a sua visão local (limitada) de mundo.

Contexto global: relacionado à missão, o objetivo geral da tarefa e pode ser uma visão compartilhada com grupos de robôs móveis.

## Explique o controle tradicional

Abordagem tradicional para controle de robôs móveis.

- Sense: obtém dados do ambiente por sensores.
- Plan: planeja a ação (deliberação ou reação).
- Act: gera uma resposta, através de seus atuadores.

![image](https://github.com/user-attachments/assets/2388e384-e969-4f52-a502-59dafda24fb5)

## Quais são as características do modelo de controle baseado em comportamentos, proposto por Brooks em sua Arquitetura de Subsunção?

Deu origam ao Behaviorismo.

Comportamento deliberativo (capacidades cognitivas) + reativo (reflexivo) e vários níveis 'plan' reagem ao mesmo estímulo sentido (sense) e interferem o sinal de saída (act).

## Diferencie comportamento deliberativo e reativo.

- Deliberativo: associado a capacidades cognitivas superiores, simbólico e apresenta tempo de resposta alto.

- Reativo: associado a capacidades instintivas, reflexivo e apresenta tempo de resposta baixo.

## Defina GGT, GLT e CL.

- GGT: nível superior, decide as coordenadas do ponto de destino e intermediários através de mapas do entorno e se detectar obstrução deve redefinir a trajetória.

- GLT: nível intermediário, faz o papel do piloto do robô (evita obstáculos, realiza correções da trajetória), atualiza o GGT sobre os resultados e comunia-se com snesores.

- CL: nível inferior, interpreta referências enviadas pelo GLT e gera ações de controle para atuação e controle dos motores de tração e direção.

## Diferencie ambientes estruturados e não estruturados.

- Ambiente estrururado: é aquele em que os objetos são estáticos e possuem características físicas particulares que permitem associá-los a formas geométricas conhecidos.

- Ambiente não estruturado: apresenta uma redondeza dinâmica ou a associação do entrono e características físicas não é viável.

## Descreva o Método do Campo Potencial aplicado à navegação de robôs móveis.

Cria forças imaginárias que atuam sobre o robô:

- Obstáculos aplica força repulsiva e destino aplica força atrativa.

- Para cada interação, calcular a resultanta 'r' (soma das forças), e a partir dela, a aceleração e a próxima posição.

## O que é Virtual Force Field?

Primeiro método que permite evitar obstáculos em tempo real para veículos autônomos rápidos.

Fazem parte do Método do Campo de Forças Virtuais, junto com outros componentes.

Componentes: grade histograma cartesiana bidimensional para representar obstáculos e campo potencial é criado com a informação probabilística.

# Aula 14

## Explique resumidamente o que cada nível da pirâmide da automação faz.

Estação (nível 1): Comando de Máquinas, Sequências e Movimentos através de Controladores Numéricos.

Célula (nível 2): supervisionar e controlar as atividades produtivas e serviços de suporte à produção no chão de fábrica.

Área (nível 3): coordenar a produção, suportar as atividades produtivas e cuidar da obtenção e alocação de recursos.

Planta (nível 4): planejar e programar a produção total.

Empresa (nível 5): define a missão da empresa e gerenciamento de corporação.

## O que é CAM (Computer Aided Manufacturing)? E CIM (Computer Integrated Manufacture)?

- CAM: ou Manufatura Auxiliada por Computador, representa a automação de uma indústria no nível de "Chão-de-Fábrica" através de Células e Sistemas Flexíveis de Manufatura, originada do desenvolvimento do processamento de informações (controle de máquinas e ferramentas).

- CIM: ou Manufatura Integrada por Computador, liga todas as funções relacionadas à manufatura de um produto e é definido como um sistema de informação e controle de manufatura.

## Quais são os principais benefícios da aplicação de CIM em um ambiente de manufatura?

Mudanças na estrutura de custos, aumento da repetibilidade dos processos, redução de inventários, aumento da flexibilidade e redução do tempo de trânsito entre estações de processamento.

## Explique o agrupamento de atividades ligadas à manufatura, de acordo com uma visão em níveis hierárquicos CIM.

Nível 1: hardware padrão, normalmente controlado por computadores
existentes nas máquinas ou por controladores programáveis.

Nível 2: grupos de equipamentos e materiais para a produção de famílias de peças através de um elevado grau de integração e
comunicação.

Nível 3: conexão de diversas Células do nível 2, formando ilhas, através da utilização de Redes de Comunicação - flexibilidade.

Nível 4: representa a integração total, grandes redes de informações interligam todas as funções de manufatura, este nível de integração representa o conceito de CIM.


## O que são células flexíveis de manufatura e de que forma são integradas em um sistema flexível de manufatura?

As células flexíveis de manufatura produzem peças individuais ou pequenos lotes, executando todas as etapas do processo e adaptando-se facilmente a diferentes tipos de peças por meio da reprogramação dos seus componentes.

São interligadas em um sistema flexível por sistemas automatizados de manipulação e de carga/descarga de materiais.

## Quais são os papéis dos robôs em um ambiente flexível de manufatura?

...

## O que é IoT? Quais são as contribuições dos robôs colaborativos nesse cenário?

IoT ou Internet das Coisas disponibiliza dados em tempo real por meio de dispositivos móveis através de conexões a grandes bancos de dados, identificando a alteração na capacidade física das coisas (sensores inteligentes) e interagindo/conectando com diversos objetos. Com isso, os robôs colaborativos interagem entre si e trabalham de forma segura junto as pessoas e também aprendem com elas.

# Aula 15

...
---
title: "Computação Gráfica - Resumão para P2"
excerpt: "Resumo Computação Gráfica"
categories:
  - Computação Gráfica
tags:
  - Computação Gráfica
  - Resumo
  - Teoria
  - Transformações Geométricas

toc: true
---

# Aula VI

Transformações mais simples: escala e translação.

## Escala

A Figura abaixo mostra a transformação de escala de quatro pontos: (2,1), (3,1), (2,2), (3,2). A escala aplicada foi de três vezes, no eixo x, e quatro vezes, no eixo y: (sx,sy)=(3,4).

![image](https://github.com/user-attachments/assets/aa02c3df-102b-4954-b856-ae7e341fbeb7)

### 2D

Forma direta:

x2 = sx * x1  
y2 = sy * y1  

Forma de matriz:  

![image](https://github.com/user-attachments/assets/a531beee-3b10-49b5-be06-5142561e8051)

### 3D

Forma direta:

x2 = sx * x1  
y2 = sy * y1  
z2 = z1

Forma de matriz:

![image](https://github.com/user-attachments/assets/1473971f-1e44-45e7-a77a-a97c4f13c474)

## Translação

A Figura abaixo representa por uma seta a translação do ponto (x1,y1)=(3,2) de (tx, ty) = (3,6), levando-o para o ponto (x2,y2)=(6,8).

![image](https://github.com/user-attachments/assets/00a459c5-2250-4b56-a3d2-fc19f022ae5c)

### 2D

Forma direta:

x2 = tx + x1  
y2 = ty + y1  

### 3D

Forma direta:

x2 = tx + x1  
y2 = ty + y1  
z2 = tz + z1

Forma de matriz:

![image](https://github.com/user-attachments/assets/c461bea7-2787-4b73-8126-4a29e5e94c05)

## Matrizes resultantes - escala e translação:

![image](https://github.com/user-attachments/assets/a70db3e1-6be8-4b24-aa40-63fac7cc0376)

## Rotação

A rotação de um ponto bidimensional (x1 ,x2) por um ângulo α em torno da origem é representada na figura abaixo.

![image](https://github.com/user-attachments/assets/00f7de29-0e09-488e-8b52-470edc29d881)

### 2D

Matriz de rotação

![image](https://github.com/user-attachments/assets/a77e62b0-7e52-48eb-abb5-9dc53b65c932)

### 3D

A matriz R pode ser facilmente estendida para três dimensões para as rotações em torno de um dos três eixos. Por ser uma rotação em torno do eixo Z, a coordenada Z não é alterada. A matriz de rotação é igual à matriz 2D, apenas acrescida da dimensão Z.

![image](https://github.com/user-attachments/assets/1f6eee19-54b6-4ebc-94ef-9748df11e74c)

Da qual podemos derivar Rxα e Ryα de rotação em torno dos eixos X e Y, respectivamente.

![image](https://github.com/user-attachments/assets/d1cf729c-bdc2-4f5a-b2c4-288f052396c4)

## Rotação no próprio eixo (centro fora da origem)

A rotação bidimensional em torno de um centro fora da origem pode ser obtida pela composição de transformações. A figura abaixo ilustra a rotação em torno do ponto c=(xc,yc).

![image](https://github.com/user-attachments/assets/28f6736a-2420-41f7-84ef-416e479aa53d)

- Fazer a translação de –c, de forma que o ponto c fique coincidente com a origem;
- Fazer a rotação pela matriz Rα , em torno da origem;
- Fazer a translação de c, de forma que o ponto c volte ao lugar correto.

![image](https://github.com/user-attachments/assets/7c0a4de0-43e7-433f-a706-dbdbf7026854)

![image](https://github.com/user-attachments/assets/c0b21151-385e-4edd-929d-da47493d9e7d)

# Aula VII

## Síntese de imagem

Recebe dados como entrada (da análise de imagem).

A imagem apresentada pelo processo de síntese é diferente da imagem que entrou no processo (amostragem, digitalização).

Na síntese os mesmo pontos da imagem podem originar outros objetos.

A ideia da imagem gerada da síntese é uma imagem descrita por um conjunto de informações (diz ao sistema como vai criar a outra imagem).

## Onde é aplicada?

Aplicações de síntese em CG são muito pesquisadas e aprimoradas.

Isso pois recebem muita grana e existem muitas industriais que se desenvolvem a partir da síntese.

Duas áreas/aplicações proeminentes são:

- Jogos
- Animações

Ex 1 - Jogo Tomb Raider:

![image](https://github.com/user-attachments/assets/b914dac8-2a9a-41e3-bd18-9f0f14a84cd3)

Ex 2 - Filme Toy Story:

![image](https://github.com/user-attachments/assets/ad8ac53c-dec2-4b2e-ab6b-66de55d5a87d)

Estas imagens também servem para mostrar como a área de síntese foi rapidamente aprimorada com o passar do tempo.

Jogos antigos possuíam poucos conjuntos de vértices, resultando em esferas mais "quadradas" -> menos polígonos (dados inseridos no ambiente).

Quanto mais quantidades de faces (dado), mais realista o jogo fica (Tomb Raider 2023).

A evolução também é graças à capacidade de processamento melhorada -> o computador consegue entender grande quantidade de vértices e depois renderizar imagens mais complexas.

Além disso, consigo fazer outras coisas nesta mesma área.  
Ex: produção de arquitetura, modelar em 2D ou 3D, etc...

Ex 3 - Blender:

![image](https://github.com/user-attachments/assets/010c9678-5271-44b9-a3bd-898a06c8346b)

## Síntese para jogos VS síntese para animações

Filmes/Animações -> elementos não interativos -> tendem a ser mais fotorrealismo do que os elementos interativos (elementos estáticos e sem mudanças são melhores para a renderização).

Jogos -> elementos interativos -> menos realista que os filmes (a renderização precisa ser calculada dependendo da escolha do jogador).

Observação: Muitos algoritmos para a renderização são aplicados nas Engines de jogos na tentativa de deixar o jogo o mais realista possível.

Ex 4 - Unity

![image](https://github.com/user-attachments/assets/608b0b66-416f-461d-801c-a133be261e6e)

Ex 5 - Unreal

![image](https://github.com/user-attachments/assets/1025536b-890f-4d67-80a0-d9f3429d51b8)

A indústria de jogos também vai se inspirar nos algoritmos realistas de filmes/animações.  
Os filmes também vão se inspiram nos melhores algoritmos de jogos.  
Um ajuda o outro.

## Artefatos da síntese de imagem

![image](https://github.com/user-attachments/assets/f60bc24d-c1f9-437d-85ed-ad8a220d9158)

Mundo real -> representado pelo modelo matemático (descreve mundo real) -> pode passar direto para a digitalização (sem alterar nada).  

Dados passam por descritores e descritores de imagem.  

Transformações podem ser aplicadas nesses modelos matemáticos.  

Saindo dos descritores, podem seguir dois caminhos:  

- Serialização é a área onde estes dados podem ser armazenados em um arquivo (arquivo descrito de imagem).

- Digitalização (essa é diferente da digitalização já estudada, melhor chamada de renderização).

Gera imagem digital (.png, .jpg).

Pronto para ser exibida em tela (abrir uma imagem e analisar resultado).

## O que é Pipeline Tradicional de Visualização?

Também chamado de pipeline de renderização, é o processo de vários estágios em que a saída de um estágio é a entrada de outrao estágio na sequência

![image](https://github.com/user-attachments/assets/2f03ff6f-a4d4-4717-aed1-288c76850aad)

## Explique a composição da aplicação

Modelo matemático composto por 5 elementos

- Dados de textura
- Malhas poligonais
- Vértices das malhas poligonais
- Pontos de vista
- Dados de iluminação

## Explique as partes do pipeline

## Transformações geométricas

Aplicadas aos vértices das próprias malhas.

 Para representar translações e rotações de um único objeto, são aplicadas transformações  eométricas sobre os vértices damalha desse objeto.
 
Para representar o reposicionamento e redirecionamento de uma câmera virtual (ponto de vista), são aplicadas transformações geométricas sobre todos os vértices de todas as malhas que compõem a cena.

São aplicadas todas as transformações de um modelo de câmera, exceto a transformação de perspectiva, que será feita no estágio de digitalização.

Por essa razão, os vértices e o ponto de vista são os elementos de entrada do estágio de transformações geométricas.

### Digitalização

Projeção perspectiva de pontos e leva em consideração a existência de oclusões.

Gera diversos fragmentos de imagem digital que são a entrada do último estágio do pipeline: a montagem da imagem final.

## Para que serve a entrada de usuário no pipeline?

Permite a interação com o modelo 3D, modificando cenas ou alterando a posição e direcionamento de câmeras virtuais (pontos de vistas).

A entrada de usuário junto com a realimentação de informações de estágios do pipeline permite a criação de animações interativas.

## O que OpenGL e Direct3D?

São APIs (Application Programming Interfaces) de desenvolvimento que implementam tarefas e até mesmo todo o pipeline gráfico, podendo utilizar recursos disponíveis em hardware nas unidades de processamento gráfico (GPUs).

OpenGL é a versão multiplataforma e Direct3D é específica para Windows.

## O que o estágio de digitalização faz?

No pipeline, p estágio de transformações geométricas processa dados definidos no espaço contínuo para gerar dados ainda no espaço contínuo.

Também, converte o espaço contínuo para o espaço discreto e envolve cálculos geométricos

## Defina o estágio de renderização

# Aula VIII

## Como projetar recursos 3D na tela do computador/celucar?

Síntese de imagem -> pipeline de visualização -> ray casting / tay tracing.

## O que é Ray Casting?

É a etapa onde a imagem do campo de visão da cãmera (FOV) será renderizada e apresentada ao espectador.

É o algoritmo mais clássico e mais interessante que foi descoberto, usado para a construção de imagens 2D.

Não tem a interpretação de objetos transparentes.

Limita a quantidade de processamento do número de pixels da imagem (objetos complexos), tornando a renderização viável a computação.

PROBLEMA: caso a imagem seja bem realista -> o tamanho de armazenamento vai ser grande.

## Seria possível a câmera caputurar ao infinito?

A cãmera não vai captura ao infinito graças ao campo de visão.

![image](https://github.com/user-attachments/assets/d2e98f3b-d221-4c94-b70c-13001d62f9e4)

## Para que servem as Normais?

A normal serve para o algoritmo de Ray Casting saber o que renderizar e exibir para o apresentador, economizando recursos e tempo.

![image](https://github.com/user-attachments/assets/18f174c5-5213-407b-a23d-4d59a61b75bd)

Geralmente em jogos, as normais dos mapas estão apenas para cima, tanto que se você entrar no mapa, não verá nada.

Sem as normais, eu precisaria considerar a outra face durante a renderização.

## O que é uma face difusa?

É uma face ou material que não é muito reflexibo, como o couro.

## Qual é a diferença para Ray Tracing?

Ray Casting: não considera a interação dos objetos em cena e não considera a composição de cores misturada com a luz (que pode gerar uma nova cor).

Ray Tracing: Considera as fontes de luz com os pixels vizinhos, e com isso, há a combinação de cores, devolvendo um aspecto mais real.
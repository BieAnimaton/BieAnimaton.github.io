---
title: "Computação Gráfica - Resumão para P1"
excerpt: "Resumo Computação Gráfica"
categories:
  - Computação Gráfica
tags:
  - Computação Gráfica
  - Resumo
  - Teoria
  - Processamento de Imagem
  - Análise de Imagem
  - Síntse de Imagem

toc: true
---

# Abertura da matéria

Computação Gráfica → 3 grandes áreas

![image](https://github.com/user-attachments/assets/00d10566-a32e-475a-bce9-3af59d072f75)

## Processamento de imagem

Área mais pesquisada e evoluída.  
Imagem que entra é alguma foto e precisa ser complexa → digitalização.  
Ajuda a preparar as imagens que serão analisadas (imagem mais critica).  

- Procura o tratamento e alterações de imagens digitais.  
- O objetivo é fazer modificações em imagens digitais para se obterem outras imagens digitais.  
- Engloba qualquer aplicação de edição de imagens com processamentos de filtragem, - segmentação e reconstrução.  

## Análise de imagem

Imagem processada entra aqui.  
Questões mais simples.  
Resulta em dados para a síntese.  

- Conjunto de artefatos e processamentos para extrair informação digital da imagem digital.  
- O objetivo é a extração de características e análise de dados extraídos da imagem.  
- Para isso, a imagem digital pode passar por pré-processamento, visando facilitar a extração de características.  
- Pode ser uma filtragem, com o objetivo de realçar características, ou uma segmentação, com o objetivo de separar objetos de interesse.

## Síntese de imagem

Área mais antiga e conhecida.  
Desenhar alguma coisa com os dados recebidos.  
Gerar uma imagem e retorna ao processamento de imagem  → renderização.  

- Procura à produção de imagens sintéticas a partir de modelos matemáticos e transformações do modelo.  
- Também trata da criação de interfaces gráficas de usuário e animações.  
- A imagem digital é o produto final resultante de processamentos realizados sobre modelos e descritores de imagem.

## Observações

- Imagem externa para processamento → digitalização.
- Imagem da síntese para processamento → renderização.

Ex: Entrar com dados (foto de uma casa - digitalização), processar (filtros), analisar (obter a posição das janelas) e devolver uma imagem (janelas em 3D pelo Blender, por exemplo- renderização).

## Por fim

Imagem que entra do mundo externo - digitalizada.  
Imagem sintetizado - sintética / vetorial.  

# Aula I

![image](https://github.com/user-attachments/assets/e4ec7326-15a3-41a1-b04d-54b86ea6d558)

## Realidade concreta:
É o que vivemos, o que podemos tocar.  
Ex: placa, ler o que está escrito no livro, copo de vidro...  

Consguimos extrair informação (conjunto) de algo que existe.  

## Realidade virtual
Substitui as infos que a realidade concreta (real) estaria dando.  
Eu sei que não é concreta.  
Ex: Óculos para enxergar, fone de ouvido para ouvir, esteira para andar
equipamentos para traduzir sentidos reais no virtual e vice-versa.  

## Realidade misturada
No meio dos dois - não é nem virtual e nem concreta.  

### Elementos mais proximos do real - realidade aumentada
Aumento as informações da realidade concreta (real).  
Ex: ao pesquisa um cachorro no google, você consegue "criar" um cachorro na vida real usando a câmera, simular na superfie plana.  

Mistura de coisas que existem no ambiente real (móvel, iluminação) acrescidas da info virtual (cachorro).  
Junção entre elementos reais e elementos virtuais - predominância de elementos reais.  

Ex 2: Pokemon Go
![image](https://github.com/user-attachments/assets/7f2c7991-1879-4ab5-86bc-8084e8715655)

### Elementos mais proximos do virtual - virtualidade aumentada
Também é uma junção do real e virtual.  
Muito mais elementos virtuais do que reais.  

Ex: filme ou jornal, apresentador e fundo verde com outra imagem, da impressão que está em outro lugar.

## Resumindo

Enquanto realidade virtual precisa de muitos equipamentos/periférics, a realidade aumentada só precisa de webcam e computador.

## Hoje em dia
Realidade aumentada de forma muito simples - próprio google.  

Realidade virtual - ainda que seja uma tecnologia evoluída, principalmente no mundo do entretenimento (compra de alguns dos periféricos), os equipamento são um pouquinho mais restritos (caros, necesistam mais processamento).

## Linha crescente

Da realidade concreta para realidade virtual.  
Aumentando a quantidade de elementos virtuais apresentadas ao observador.  

Obs: A observação das diferentes realidades pode ser continua.  

> A realidade virtual da década de 90 é a realidade virtual imersiva hoje em dia.  

## Realidade virtual imersiva
Para que a pçessoa experimentar, é necessário equipamentos que traduzam todos os sentidos para o ambiente virtual - tato, olfato, visão, audição, rosto - traduziods de alguma maneira.  
Objetivo de simular sensações que soa como se fossem provenientes da realidade concreta.

## Realidade virtual não imersiva
Muito presente em jogos - vai te transportar para uma outra realidade.  
Imersivo de maneira contemporânea sem todos os aparelhos.  
Não considera os outros sentidos - como tato e olfato.

Ex: Beat Saber
![image](https://github.com/user-attachments/assets/40ac7c36-236b-4554-9dd5-a50295aa8227)

## Fundamentos de imagem - Cap II

Imagem - resultado do processo de digitalização - é uma matriz de valores chamados pixels.  
Imagem matricial - resultado do processo de digitalização.  

Possuem 3 canais para armazenar as cores R, G e B.

![image](https://github.com/user-attachments/assets/99f93269-f378-4c12-8222-6d0898cbcfc1)

A imagem representada por uma matriz é chamada de imagem matricial, bitmap ou, simplesmente, imagem digital.

![image](https://github.com/user-attachments/assets/7dc00ddc-5cc9-4c28-8661-e9c0933de5c0)

## Digitalização

![image](https://github.com/user-attachments/assets/32a6714c-da24-4de3-bb1a-8f8f4052ec4e)

Etapas de digitalização

### Sinal original
Fótons da realidade concreta saindo da lâmpada, refletindo no objeto e as informações luminosas chegando no meu olho (cones e bastonetes).  

### Filro analógico
Relacionados com qualidade da máquina fotografia.  
Os sensores vão perceber a quantidade de fótons chegando (sensores mais precisos conseguem perceber uma maior quantidade de luz e vice-versa).  
Imagem capturada pela câmera gera o sinal filtrado.  

### Sinal filtrado
Já é menor que o original, possui menos informações.  

### Amostragem
Em quantos quadradrihos eu vou subdiviir esses sinal filtrado.  
Representa os pixels no final da minha imagem.  
Quanto mais amostras melhor a resolução.  
Resulta sinal amostrado.  

Ex: 2 mega pixels = 2 milhões de quadradrihos que "olham" o sinal filtrado e tentam representar o comportamento do mesmo.  
Diretamente relacionado com a quantidade de pixels que eu vou ter lá no final da minha imagem.  
Quanto mais amostragem, melhor a resolução da imagem.  

### Sinal amostrado
A quantidade elementos q eu vou escolher para representar o sinal original a partir do sinal filtrado.  

### Quantização
Atribuição de valores a cada uma dessas amostras.  
Recebe 3 valores, 256 tonalidades de R G e B.  
Para representar 1 cores 1 bit só.  
Quanto menos bits, mais informações perdidas.  
Quanto mais eu aumentar, mais bits na grade de quantização, maior a capacidade de representação da imagem.  
8 bits para cada um dos canais.  
Resulta no sinal digital.  

![image](https://github.com/user-attachments/assets/d2e84ba8-9141-45d1-940e-c8d80a0ded88)

### Sinal digital
Sinal já digitalizado.  

### Sistema digital
Faz o armazenamento da imagem digital (sinal digital) no sistema para uso futuro.  

### Sinal digital
Disponivel para os todos dispositivos.  

## Pontos positivos e negativos da digitalização

Positivos  
- Manipulação,
- Armazenamento,
- Distribuição.

negativos  
- Nível de detable (menos informações).

## Bitmap e imagens vetoriais

Uma imagem pode ser totalmente descrita por equações vetoriais, ou, melhor dizendo, por meio de descritores de imagens, para ser desenhada apenas quando necessário. Imagens
descritas com base neste princípio são chamadas imagens vetoriais

Bitmap é diferente de vetorial

Vetorial -> função matematica
Depois de ser digitalizada -> matrizes bitmap (.bmp)

## RGB e CMY

O modelo RGB surgiu a partir de estudos de composição de luzes, que demonstraram que a partir de apenas três cores primárias é possível obter todas as outras cores do espectro da luz visível.

Os estudos também mostraram que as três cores primárias que apresentam as melhores combinações para gerar outras cores são as cores vermelho (Red), verde (Green) e azul (Blue), o que deu origem ao modelo RGB.

![image](https://github.com/user-attachments/assets/698ded06-a315-4b77-946d-e4ab4c7bb19c)

O modelo RGB é um modelo de cor aditivo. A combinação das cores primárias gera as cores secundárias. Com r = 0, não há contribuição da cor vermelha, e com r = 255, há o máximo de contribuição da cor vermelha. O mesmo vale para as cores verde (g) e azul (b).  

Uma cor é, portanto, um ponto no interior do cubo de cores, cujos vértices representam as cores primárias (R, G e B), as cores secundárias (C, M e Y), a ausência de cor (K) e a composição de todas as cores (W).  

![image](https://github.com/user-attachments/assets/84872c5e-448e-41c7-b6e1-1f3c92eaa927)

O modelo HSL representa a cor pelos componentes de cromaticidade matiz (H - hue) e saturação (S - saturation), e pela componente de luminância (L - luminance). É um modelo bastante utilizado no processamento de imagens, isso porque alguns algoritmos de processamento de imagens requerem uma relação de ordem entre os elementos do contradomínio.

O contradomínio da componente luminância (L) do HSL contém todos os contornos da imagem (como uma fotografia monocromática) e
possui a relação de ordem (número inteiro). 

![image](https://github.com/user-attachments/assets/174ae2e8-cd1f-4516-b582-cfafbf13f4e1)


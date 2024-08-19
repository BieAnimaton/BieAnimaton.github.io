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
Imagem que entra é alguma foto e precisa ser complexa.  
Ajuda a preparar as imagens que serão analisadas (imagem mais critica).  

É a subárea da computação gráfica que visa o tratamento e alterações de imagens digitais. O objetivo do processamento de imagens é fazer modificações em imagens digitais para se obterem outras imagens digitais. Engloba qualquer aplicação de edição de imagens e o processamento mais comum é a filtragem, mas a segmentação e a reconstrução também são usadas no processamento.

## Análise de imagem

Imagem processada entra aqui.  
Questões mais simples.  
Resulta em dados para a síntese.  

A análise de imagens é o conjunto de artefatos e processamentos para extrair informação digital da imagem digital. O objetivo é a extração de características e análise de dados extraídos da imagem. Para isso, a imagem digital pode passar por pré-processamento, visando facilitar a extração de características. Pode ser uma filtragem, com o objetivo de realçar características, ou uma segmentação, com o objetivo de separar objetos de interesse.

## Síntese de imagem

Área mais antiga e conhecida.  
Desenhar alguma coisa com os dados recebidos.  
Gerar uma imagem e retorna ao processamento de imagem.  

A síntese de imagens é a subárea da computação gráfica que visa à produção de imagens sintéticas a partir de modelos matemáticos e transformações do modelo. É também a subárea que trata da criação de interfaces gráficas de usuário e animações. A imagem digital é o produto final resultante de processamentos realizados sobre modelos e descritores de imagem.

## Observações

- Imagem externa para processamento → digitalização.
- Imagem da síntese para processamento → renderização.

Entrar com dados (foto de uma casa - digitalização), processar (filtros), analisar (obter a posição das janelas) e devolver uma imagem (janelas em 3D pelo Blender, por exemplo- renderização).

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

Ex2:Pokemon Go
![image](https://github.com/user-attachments/assets/3fa40baa-598a-4cf6-a5d9-5272f4158f4c)

### Elementos mais proximos do virtual - virtualidade aumentada
Também é uma junção do real e virtual.
Muito mais elementos virtuais do que reais.
Ex: filme ou jornal, apresentador e fundo verde com outra imagem, da impressão que está em outro lugar.

## Resumindo

Enquanto realidade virtual precisava de muitos equipamentos/periférics, realidae aumentada só precisa de webcam e computador.

hj em dia - realidade aumentada de forma muit simples - proprio google
realidade virtual - ainda que seja uma tecnologia evoluida - evolução no mundo do entretenimento (comprar alguns dos periféricos) - equipamento um pouquinho mais restritos - caros - mais processamento

## Linha crescente

Da realidade concreta para realidade virtual.  
Aumentando a quantidade de elementos virtuais apresentadas ao observador.  

Obs: A observação das diferentes realidades pode ser continua.  

> A realidade virtual da década de 90 é a realidade virtual imersiva hoje em dia.  

## Realidade virtual imersiva
Para que a pçessoa experimentar, é necessário equipamentos que traduzam todos os sentidos para o ambiente virtual - tato, olfato, visao, audicao, rosto - traduziods de alguma maneira.  
Objetivo de simular sensações que soa como se fossem provenientes da realidade concreta.

## Realidade virtual não imersiva - jogo - vai te transportar para uma outra realidade
Imersivo de maneira contemporânea sem todos os aparelhos.  
Não considera os outros sentidos - como tato.

Ex: Beat Saber
![image](https://github.com/user-attachments/assets/40ac7c36-236b-4554-9dd5-a50295aa8227)

## Fundamentos de imagem - Cap II

A imagem - resultado do processo de digitalização - é uma matriz de valores chamados pixels.

Possuem 3 canais para armazenar as cores R, G e B.

![image](https://github.com/user-attachments/assets/99f93269-f378-4c12-8222-6d0898cbcfc1)

A imagem representada por uma matriz é chamada de imagem matricial, bitmap ou, simplesmente, imagem digital.

![image](https://github.com/user-attachments/assets/7dc00ddc-5cc9-4c28-8661-e9c0933de5c0)

## Digitalização

![image](https://github.com/user-attachments/assets/32a6714c-da24-4de3-bb1a-8f8f4052ec4e)

Etapas de digitalização
- Sinal original - fótons saindo da lâmpada, relfetindo no objeto e chegando no meu olho (cones e bastonetes).
- Filro analógico (qualidade da máquina fotografia) sensores q vao perceber a quantidade de fotons chegando - imagem capturada pela câmera.
- Sinal filtrado - possui menos informações.
- Amostragem : em quantos quadradrihos eu vou diviir esses sinal filtrado - pixels no final da minha imagem - quantos mais amostras melhor a resolução - resulta sinal amostrado.
- Sinal amostrado - elementos q eu vou escolher.
- Quantização atribuição de valores a cada uma dessas amostras - 256 tonalidades de R G e B - quanto mais eu aumentar, mais bits na grade de quantização, maior a capacidade de representação da img - 8 bits para cada um dos canais.
- Sinal digital - saída da quantização.
- Sistema digital - faz o storage da imagem digital.
- Sinal digital - disponivel para os dispositivos eletrônicos.

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


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

O modelo RGB surgiu através de estudos de composição de luzes e demonstraram que a partir de apenas três cores primárias é possível obter todas as outras cores do espectro da luz visível.

As três cores primárias que apresentam as melhores combinações para gerar outras cores são as cores vermelho (Red), verde (Green) e azul (Blue), dando origem ao modelo RGB.

![image](https://github.com/user-attachments/assets/698ded06-a315-4b77-946d-e4ab4c7bb19c)

O modelo RGB é um modelo de cor aditivo e a combinação das cores primárias gera as cores secundárias.  

Com r = 0, não há contribuição da cor vermelha, e com r = 255, há o máximo de contribuição da cor vermelha. O mesmo vale para as cores verde (g) e azul (b).  

Uma cor é, portanto, um ponto no interior do cubo de cores, cujos vértices representam:  

- as cores primárias (R, G e B),
- as cores secundárias (C, M e Y),
- a ausência de cor (K),
- a composição de todas as cores (W).  

![image](https://github.com/user-attachments/assets/84872c5e-448e-41c7-b6e1-1f3c92eaa927)

HSL (Hue, Saturation, Lightness) é um modelo de cores que representa as cores de forma mais próxima à percepção humana, onde a matiz define a tonalidade (como vermelho ou azul), a saturação define a intensidade da cor, e a luminosidade define a quantidade de luz. Diferente do RGB (Red, Green, Blue), que mistura as três cores primárias em diferentes intensidades para criar outras cores, o HSL separa a cor em aspectos que são mais intuitivos para manipulação, como ajustar a intensidade ou a claridade de uma cor específica.

Ex: clarear uma cor em HSL envolve simplesmente aumentar o valor da luminosidade, enquanto no RGB é necessário um cálculo mais complexo, podendo alterar inadvertidamente a tonalidade da cor.

Obs:
O contradomínio da componente luminância (L) do HSL contém todos os contornos da imagem (como uma fotografia monocromática) e possui a relação de ordem (número inteiro). 

![image](https://github.com/user-attachments/assets/174ae2e8-cd1f-4516-b582-cfafbf13f4e1)

# Aula II

## Representação de imagems

Área mais essencial da imagem (juntamente com os fundamentos - aula passada).

Com a maior capacidade de processamento, houve a evolução e o aumentado da representação do objeto - se aproximando da realidade (comparação dos gráficos de ps1 com ps5).

Vértices ligados 2 a 2 formam arestas.  
Arestas ligadas 3 a 3 formam faces.  

2 algorítmos em especial.  

## Criando imagem com Opencv no Python

Criar uma imagem com 3 canais (canais de cores)

```
color=np.ones((200,200,3))*155
```

Preenchidas com 1 - multiplicou por 155

## Criando retas com Opencv no Python

parâmetros: (matriz, inicio, final, cor, espessura)

```
color=cv2.line(color,(0,0),(200,200),(17,200,180),4)
```

![image](https://github.com/user-attachments/assets/9a826ffa-cf2a-4ace-ab65-eccaad06c39a)


## Criando círculos com Opencv no Python

```
image2 = np.zeros((200, 200, 3))
```

Desenhando um círculo vermelho com o centro em (100, 100) e raio 50, cor e espessura são os outros dois parametros

```
image2 = cv2.circle(image2, (100, 100), 50, (5, 0, 200), 2)
```

![image](https://github.com/user-attachments/assets/1c5a1029-ba67-479c-aaaf-2c988969e6c9)


## Exercíco 1
Criar uma paisagem com as funções de retas e círculos.

Utilize as funções de linhas e de círculos para desenvolver uma composição (em uma imagem matricial) que apresente um cenário no qual se observam:

- um gramado
- uma árvore
- montanhas
- o céu
- o por-do-sol

```
paisagem = np.zeros((200, 200, 3))

paisagem = cv2.line(paisagem,(0,0),(200,0),(120, 80, 0), 320) #ceu

for i in range(0, 25):
  paisagem = cv2.circle(paisagem, (200, 160), i, (0, 255, 255), 2) # sol

paisagem = cv2.line(paisagem,(2,180),(200,180),(120, 220, 120), 35) # grama

paisagem = cv2.line(paisagem,(50,140),(50,170),(0, 120, 200), 9) # arvore
for i in range(0, 25):
    paisagem = cv2.circle(paisagem, (50, 120), i, (0, 255, 0), 2) # folha

# montanha 1
paisagem = cv2.line(paisagem,(90,170),(110,130),(42, 77, 107), 2)
paisagem = cv2.line(paisagem,(130,170),(110,130),(42, 77, 107), 2)
paisagem = cv2.line(paisagem,(90,170),(130,170),(42, 77, 107), 2)

pts = np.array([[90, 170], [110, 130], [130, 170]], np.int32)
pts = pts.reshape((-1, 1, 2))

cv2.fillPoly(paisagem, [pts], (42, 77, 107))

# montanha 2
paisagem = cv2.line(paisagem,(130,170),(140,90),(42, 77, 107), 2)
paisagem = cv2.line(paisagem,(140,90),(170,170),(42, 77, 107), 2)
paisagem = cv2.line(paisagem,(90,170),(170,170),(42, 77, 107), 2)

pts = np.array([[130,170], [140,90], [170,170]], np.int32)
pts = pts.reshape((-1, 1, 2))

cv2.fillPoly(paisagem, [pts], (42, 77, 107))

# nuvem 1 e 2
for i in range(0, 15):
    paisagem = cv2.circle(paisagem, (50, 30), i, (255, 255, 255), 2) # folha
    paisagem = cv2.circle(paisagem, (60, 30), i, (255, 255, 255), 2) # folha
    paisagem = cv2.circle(paisagem, (70, 30), i, (255, 255, 255), 2) # folha

    paisagem = cv2.circle(paisagem, (140, 40), i, (255, 255, 255), 2) # folha
    paisagem = cv2.circle(paisagem, (150, 40), i, (255, 255, 255), 2) # folha
    paisagem = cv2.circle(paisagem, (160, 40), i, (255, 255, 255), 2) # folha

cv2_imshow(paisagem)
```

![image](https://github.com/user-attachments/assets/ac52e58b-a722-4883-8fe7-7bf09dd1978a)

## Algoritmos

## Algoritmo DDA

Desenha retas muitos bem feitas, porém utiliza elementos que vão fazer com que perca um pouco de tempo (divisões e arredondamentos).  
A dificuldade maior para realizar desenho em tempo real - quando precisa interagir com objetos.  
Ex: jogo - entrando com informações em tempo real - DDA demora muito (principalmente quando usar funções externas).  

```
#algoritmo DDA

#definindo a função DDA
def dda(x1, y1, x2, y2):
  #calculando a diferença entre os pontos
  dx = x2 - x1
  dy = y2 - y1

  #calculando os passos
  if abs(dx) > abs(dy):
    steps = abs(dx)
  else:
    steps = abs(dy)

  #calculando o incremento
  x_increment = dx / steps
  y_increment = dy / steps

  x = x1
  y = y1

  pixels = []

  #percorrendo os passos
  for _ in range(steps):
    #adicionando o pixel na lista
    pixels.append((round(x), round(y)))
    #calculando o próximo pixel
    x += x_increment
    y += y_increment

  #retornando a lista de pixels
  return pixels
```

## Exercício 2

Obter entradas do usuário e criar um triângulo com o algoritmo DDA.

```
triangulo = np.zeros((200, 200))

x1 = int(input("Valor X1: "))
y1 = int(input("Valor Y1: "))
x2 = int(input("Valor X2: "))
y2 = int(input("Valor Y2: "))
x3 = int(input("Valor X3: "))
y3 = int(input("Valor Y3: "))

a = dda(x1, y1, x2, y2)
b = dda(x3, y3, x2, y2)
c = dda(x1, y1, x3, y3)

vertices = a + b + c
for pixel in vertices:
  x, y = pixel
  triangulo[y, x] = 255

cv2_imshow(triangulo)
```

![image](https://github.com/user-attachments/assets/650b385b-cd83-4b75-a5d7-17fd7b3e83fc)

## Observação

Hoje em dia com o poder de processamento avançado - são feitas várias chamdas em pontos próximos para maior definição.  
Ex: várias chamdas de Bresenham para o desenho de um círculo. 

## Algoritmo Bresenham

Evolução do DDA - para desenhar mais rápido.  
Evita fazer contas de dividir e arredondamento.  
Verifica se pixel proximo é um pixel à direta ou um pixel na diagonal subindo.

```
#algoritmo de Bresenham

def bresenham(x1, y1, x2, y2):
    dx = abs(x2 - x1)
    dy = abs(y2 - y1)
    sx = 1 if x1 < x2 else -1
    sy = 1 if y1 < y2 else -1
    err = dx - dy

    pixels = []
    while True:
        pixels.append((x1, y1))
        if x1 == x2 and y1 == y2:
            break
        e2 = 2 * err
        if e2 > -dy:
            err -= dy
            x1 += sx
        if e2 < dx:
            err += dx
            y1 += sy

    return pixels
```

# Exercício 3

Demonstre na prática que o algoritmo Bresenham é mais rápido que o algoritmo DDA.

```
import time

image3 = np.zeros((200, 200))

x1 = int(input("Valor X1: "))
y1 = int(input("Valor Y1: "))
x2 = int(input("Valor X2: "))
y2 = int(input("Valor Y2: "))

start_time = time.time()

dda_pix = dda(x1, y1, x2, y2)
for pixel in dda_pix:
    x, y = pixel
    image3[y, x] = 255

end_time = time.time()

execution_time = end_time - start_time

cv2_imshow(image3)
print(f"DDA: {execution_time:.5f} segundos")

start_time = time.time()

bre_pix = bresenham(x1, y1, x2, y2)
for pixel in bre_pix:
    x, y = pixel
    image3[y, x] = 255

end_time = time.time()

execution_time = end_time - start_time

cv2_imshow(image3)
print(f"Bresenham: {execution_time:.5f} segundos")
```

![image](https://github.com/user-attachments/assets/e6fedc7e-a51b-4366-b529-1031613fd8ec)
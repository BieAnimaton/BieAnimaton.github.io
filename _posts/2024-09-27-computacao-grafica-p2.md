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
1

Forma de matriz:

![image](https://github.com/user-attachments/assets/c461bea7-2787-4b73-8126-4a29e5e94c05)

## Matrizes resultantes - escala de translação:

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

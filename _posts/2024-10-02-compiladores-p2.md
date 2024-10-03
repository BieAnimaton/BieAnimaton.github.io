---
title: "Compiladores - Resumão para P2"
excerpt: "Resumo Compiladores"
categories:
  - Compiladores
tags:
  - Compiladores
  - Resumo
  - Teoria
  - Análise Sintática

toc: true
---

# Aula VI

## Dervivação

Sequência de substituições de não-terminais por uma escolha das regras de produção gramaticais.  

Método utilizado para a construção de uma cadeia específica de terminais, partindo de uma não-terminal inicial.  

Existem várias derivações para a construção da mesma cadeia de não-terminais.  

Verificar se a sequência de tokens é aceita:
- Inicia-se com um símbolo não-terminal chamado raiz.
- Aplica-se produções, substituindo não-terminais, até somente restarem terminais.
- Uma derivação substitui um não-terminal pelo lado direito de uma de suas produções.
- O símbolo -> denota um passo de derivação.

## Exemplo

![image](https://github.com/user-attachments/assets/96c6dd11-c73d-495c-8c7a-c64c62fa0401)

### Solução

![image](https://github.com/user-attachments/assets/197ac9c3-b56a-43f0-9fa5-6c3a99ff1b7e)

## À esquerda e à dirieta

Derivação mais à esquerda:  
é a sequência de formas sentenciais que se obtém derivando sempre o símbolo não-terminal mais à esquerda.  

Derivação mais à direita:  
é a sequência de formas sentenciais que se obtém derivando sempre o símbolo não-terminal mais à direita.  

### À esquerda

![image](https://github.com/user-attachments/assets/6d030460-fb58-4c75-8166-554ee58dcd0a)

### À direita

![image](https://github.com/user-attachments/assets/47a890f6-d203-4dcc-846e-a5c6d946a461)

Observe que o código final é o mesmo nos dois casos.

## Exercício 1

![image](https://github.com/user-attachments/assets/908bddb5-8a1c-4f4d-b5ad-c42cadc0149c)

### Solução

Apenas a 3

Por que 1 não está na gramática?  
Pois é impossível ter apenas 1 C após usar o Y.

Por que 2 não está na gramática?  
Pois é impossível ter 2 Cs sem B.

Por que 4 não está na gramática?  
Pois é impossível ter 3 Bs com apenas 2 Cs.

## Propriedades

A recursividade em uma GLC é importante, pois a possibilita a
construção da repetição.  

As produções vazias (ℇ - produções) são úteis para definir
estruturas opcionais da linguagem.  

## Ambiguidade

Quando existe mais de uma árvore de derivação para a mesma sentença.

Isso representa um problema para o analisador sintático, pois
ele não especifica com precisão a estrutura sintática do programa.

O problema pode ser comparado aos autômatos não determinísticos, onde dois caminhos podem aceitar a mesma cadeia

> Isso pode mudar todo o entendimento do comando -> mudar o if e else.

Porém, a eliminação de ambiguidade de uma gramática não é tão simples como a eliminação de não-determinismo em autômatos.

O que deve ser feito:
- Estabelecer uma regra que especifique para cada caso ambíguo qual é o caminho correto.

## Exemplo

![image](https://github.com/user-attachments/assets/9dcbae98-0c26-46cb-9201-44a9ef9f8497)

A ordenação das operações matemáticas está errada.

## Eliminação da ambiguidade

Eliminação de ambiguidade:
- Tratar conceitos de precedência e associatividade.
- Especificar uma ordem na avaliação dos operadores.
- Operadores com maior precedência são avaliados primeiro.
- Operadores de igual precedência são avaliados de acordo com a associatividade (esquerda-direita, vice-versa).

### Precedência
Agrupamentos dos operadores de igual precedência.

Para cada nível de precedência introduz-se um não terminal e uma regra gramatical.

### Associatividade

Cria-se regras gramaticais recursivas à esquerda ou à direita.

## Correção

![image](https://github.com/user-attachments/assets/38c221e0-3abe-4499-bf94-a88273c4ec1b)

## Exemplo 2

![image](https://github.com/user-attachments/assets/05e54e94-4335-4f96-b267-5e0808238e9b)

![image](https://github.com/user-attachments/assets/dde07ea9-2d6d-4fbe-a48d-cd16fb1d7a1c)

### Solução

A eliminação da ambiguidade pode ser feita a seguinte forma:

Associar cada ‘else' ao ‘if' mais próximo que ainda não tenha sido associado.

![image](https://github.com/user-attachments/assets/9bbea1c9-b5d8-4c73-b0bd-a6e939e58ca5)

## Exercício 2

![image](https://github.com/user-attachments/assets/59e1da8e-1e05-4f07-a75f-635b8f2a7fd0)

![image](https://github.com/user-attachments/assets/d32e2524-dbe3-4209-8769-e2332327bce4)

### Solução

É ambígua, pois não tem níveis diferentes, ou seja, a soma e a multiplicação possuem o mesmo nível de prioridade.

![image](https://github.com/user-attachments/assets/8408604d-7551-482d-8bc1-677b1e939574)

Primeira representação -> ambíguo.  
Segunda representação -> não ambíguo.  

## Exercício 3

![image](https://github.com/user-attachments/assets/9c636aa7-ea11-4f17-be38-0cacb2885b1c)

### Solução

![image](https://github.com/user-attachments/assets/ebdca84c-cfdb-46b4-a201-b02214031bff)

## Exercício 4

![image](https://github.com/user-attachments/assets/c0b6651f-3d10-44ae-9c62-08b3d57b626d)

### Solução

![image](https://github.com/user-attachments/assets/12111771-67b5-4608-bf94-91a8aba85582)

## Exercício 5

![image](https://github.com/user-attachments/assets/d93afc37-df75-4db5-a6f6-0a9c7846840f)

### Solução

G1 e G3 são ambíguas, pois possuem dois símbolos não-terminais (S) do lado direito.

G2 apresente apenas 1, por isso não é.
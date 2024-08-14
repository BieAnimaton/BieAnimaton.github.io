---
title: "Compiladores - Resumão para P1"
excerpt: "Resumo Compiladores"
categories:
  - Compiladores
tags:
  - Compiladores
  - Resumo
  - Teoria
  - Análise Léxica
  - Análise Sintática
  - Análise semântica
  - Gerador de código

toc: true
---

# Aula I

## Compilar

Traduzir algo escrito em uma determinada linguagem para uma linguagem de máquina.

Traduz um código fonte (alto nível) para um código objeto binário (baixo nível).

Código fonte -> compilador -> código executável

## História

no inicio programas eram escritos em ling de maq

o primeiro compilador foi criado por Grace Hooper em 1952, A-0 System (Univac I)

compilador completo em 1957, FORTAN - John Backus

## Componentes

- Análise léxica
- Análise sintática
- Análise semântica
- Geração e otimização de código

### Analise léxica

Vai executar os autômatos.

Identificar os elementos do textos, caractere por caractere.

Verificar se a palavra é reservada, constante, variável.

Ignora comentários.

### Analise sintática

Identifica as construções válidas da linguagem com base nos elementos léxicos.

### Analise semântica

Garante que as construções identificadas façam sentido de acordo com as regras da linguagem.

Verifica se as variáveis usadas foram devidamente declaradas

### Gerador de código

Criação de código de baixo nível que reflete os comandos do código fonte.

Otimização dos comandos gerados para uma determinada arquitetura.

## Exemplo

soma := soma + 35

### Análise léxica

(valor)	(classe)

SOMA	identificador

:=		comando de atribuição

SOMA	identificador

+		operador numérico de adição

35		constante numérica inteira

### Análise sintática

Árvore de execução (desenho).

Caso a análise léxica esteja certa, constrói a árvore e código está certo.

Distribui as expressões, sequencias e operações

Em linguagens formais e autômatos → processo de derivação na linguagem → procurava derivar.

Criava a árvore de derivação → aqui é árvore sintática.

Linguagens formais não seguiam nenhum algoritmo específico → tentava e erro.

![analisador sintatioc](https://github.com/user-attachments/assets/ba88ab9b-9808-48f5-b784-49ade1dd71fc)

### Análise semântica

SOMA foi declarada?

SOMA é variável?

Qual o escopo de SOMA?

Qual o tipo de SOMA?

Coloca informações adicionais na árvore

### Geração de código

Movimentação de registradores

Código dentro do processador (assembly).

```nasm
MOV AX, [soma]
ADD AX, 35
MOV [soma], AX
```

## Componentes em detalhes

![componentes em detalhes](https://github.com/user-attachments/assets/2b13cdb6-d29f-4d6f-99b8-3801f90ef3d8)

## Compiladores vs Interpretadores

Existência das três analises (léxica, sintática e semântica).

Compilador faz trabalho rápido.

Interpretadores geram código objeto durante a execução.

Interpretadores são mais lentos, porem alterações no código são mais rápidas de serem realizadas.

## Bytecode

Presente no Java.

Ao invés de gerar comandos em linguagens de maquina, os comandos são armazenados na forma de códigos binários.

Este código será então interpretado por uma maquina virtual.

Compila até uma parte, depois manda para a máquina virtual.

Bom para rodar em arquitetura diferentes (um código Java feito no Linux pode rodar no Linux, Windows e Mac sem problemas).

# Alula 2

## O que é gramática?
Gramática é uma ferramenta para descrever uma linguagem.  
É a base do analisador léxico e sintático.

## Obs
Autômatos finitos são utilizados na análise lexicográfica para reconhecimento dos programas e na definição de suas estrutras.

## O que é um compilador?
É um tradutor entre duas linguagens (L1 e L2) de programação.  
Neste caso L1 representa o código fonte e L2 o código de máquina.

## Relembrando
Alfabeto: conjunto finito não vazio de símbolos.  
Palavra: sequência finita de símbolos do alfabeto.  
Comprimento da palavra: número de símbolos que compõem a palavra.  
Concatenação ou produto de palavras.  

Uma linguagem sobre um alfabeto Σ é um subconjunto de Σ*.  

## Qual é a regra geral da gramática?
Gramática G=(V,T,P,S), onde:  
– V: conjunto de símbolos não terminais  
– T: conjunto de símbolos disjuntos de V  
– P: conjunto de regras de produção  
– S: elemento de V denominado inicial  

## Exercício 1

![image](https://github.com/user-attachments/assets/95ab7a54-aeb1-4b40-a929-4c4f5dfa21ba)

![image](https://github.com/user-attachments/assets/d49bee0b-8b81-4ee7-b602-484953de031a)


## Exemplo 2

Obs: fere regra de produção - símbolos não terminais não podem estar nos dois lados (EOE).

![image](https://github.com/user-attachments/assets/7f75468b-c8aa-4685-93b3-88c0d093270e)

![image](https://github.com/user-attachments/assets/657c1152-311b-471d-a0b3-53c9d12a137d)

## Detecção de erros

### Dinâmicos
São erros originados em tempo de execução
Ex: input não esperado do usuárui

### Estáticos
São erros encontrados durante a compilação
- identificadores ma contruidos (analise lexica).  
	Verifica se reconhece os elementos.  
  Ex: na seguiu as regras de variaveis

- Desrespeito a gramatica - "syntaxa error" (analise sintatica).  
 - Desrespeita a política de tipos, visibilidade de identificadores, passagem de parâmetros, etc (análisesemântica).  

![image](https://github.com/user-attachments/assets/2e467e89-2b16-4cbb-8b51-38c660fd7ecb)

## Qual a função da análise léxica?
Sua função é ler o arquivo fonte e "etiquetar" os elementos significativos.  
Estes elementos significativos são chamados de **tokens**

## O que são tokens?
Tokens são os significados dos padrões de caracteres em um código fonte.

O processo de varredura é um caso especial de casamento de padrões.  
Métodos utilizados: Expressão regular (ER) e autômatos finitos.  
A velocidade do processamento é um ponto crítico.  

## O que é lexema?
Lexema é a sequência de caracteres na fonte que se associa a um padrão e então a um token - instância do token.  

## Simplificando
Lexema -> variavel / operação encontrado no codigo (if, sum, ...)  
Token -> como é representada |(numero, literal, ...)

![image](https://github.com/user-attachments/assets/b067dee1-2f27-4dbb-bab7-e2976704ada1)

A palavra léxico faz referencia ao conjunto teoricamente infinito de todas as palavras já realizadas e potenciais de uma língua  
Em linguagem de programação, palavras são objetos como nomes de variáveis, números, keywords.  
Estas palavras são chamadas de tokens.  

![image](https://github.com/user-attachments/assets/394ead41-865c-4001-aea5-862ee95775e4)

Entenda VALOR como Lexema e CLASSE como Token.

Input: letras individuais das palavras.  
Output: strings divididas em tokens.  
Descarta espaços em branco (espaços, quebra de linha e etc) e comentários.  

## Qual o objetivo da análise léxica?
Facilitar o trabalho do analisador sintático.

## Por que separar o analisador léxico do analisador sintático?
Pois é mais eficiente, modular e tradicional.

## O que faz um gerador léxico?
Transforma especificações de tokens e espaços em branco (em linguagem humana compreensível) em programas eficientes.  

Especificações léxicas são geralmente escritas usando expressões regulares.  
ER: notação algébrica para descrever um conjunto de caracteres.  
Assim, os gerados léxicos são descritos como autômatos finitos.  

## Análise léxica - ER

![image](https://github.com/user-attachments/assets/90d05d27-7126-4c17-8b14-cac72591d56b)

![image](https://github.com/user-attachments/assets/cbfaed32-8d95-4e22-bff3-d69ea0ccae50)

## Estrutura léxica - MiniJava

![image](https://github.com/user-attachments/assets/b92c03a4-6cf2-469c-8871-0ac7279a345f)

## Análise léxica - ER (continuação)

![image](https://github.com/user-attachments/assets/70b6b57a-be8a-4681-857e-632f9896fe68)

## Exercício 1

![image](https://github.com/user-attachments/assets/9a80776c-8ba7-4476-a870-a7924c3c18e1)

## Respostas  
a)  0*  
    42  

b)  0∗  
    ([0−9] |  
    [1−3][0−9] |  
    4[0−1] |  
    4[3−9] |  
    [5−9][0−9] |  
    [1−9][0−9][0−9]+)  

c)  0∗
    (4[3−9] |  
    [5−9][0−9] |  
    [1−9][0−9][0−9]+)  

## Qual é o melhor autômato para reconhecer as palavras?
É p autômato finito deterministico com o minimo de estados.  

## Vamos estudar 3 etapas
- ER para Autômato Finito Não Deterministico (AFN).
- Autômato Finito Não Deterministico (AFN) para Autômato Finito Deterministico (AFD).
- Minimização de estado do Deterministico (AFD).

## Análise léxica - ER para AFN
Utilização de fragmentos.  
Colar os diversos fragmentos para construir o autômato completo.  

![image](https://github.com/user-attachments/assets/5e5fb453-9807-4e6e-9158-f4b9eaabe593)

![image](https://github.com/user-attachments/assets/5cdb7425-ee5f-4c4c-926b-2f5949881603)

## Exercício 1
(a|b)*ac  
Qual é o AFN?

![image](https://github.com/user-attachments/assets/83795735-8c0a-44f2-83c5-91d65f946e59)

![image](https://github.com/user-attachments/assets/cb107a40-a390-47f1-a3c1-113836ba5282)
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

## Analise léxica

Vai executar os autômatos.

Identificar os elementos do textos, caractere por caractere.

Verificar se a palavra é reservada, constante, variável.

Ignora comentários.

## Analise sintática

Identifica as construções válidas da linguagem com base nos elementos léxicos.

## Analise semântica

Garante que as construções identificadas façam sentido de acordo com as regras da linguagem.

Verifica se as variáveis usadas foram devidamente declaradas

## Gerador de código

Criação de código de baixo nível que reflete os comandos do código fonte.

Otimização dos comandos gerados para uma determinada arquitetura.

## Exemplo.

soma := soma + 35

## Análise léxica

(valor)	(classe)

SOMA	identificador

:=		comando de atribuição

SOMA	identificador

+		operador numérico de adição

35		constante numérica inteira

## Análise sintática

Árvore de execução (desenho).

Caso a análise léxica esteja certa, constrói a árvore e código está certo.

Distribui as expressões, sequencias e operações

Em linguagens formais e autômatos → processo de derivação na linguagem → procurava derivar.

Criava a árvore de derivação → aqui é árvore sintática.

Linguagens formais não seguiam nenhum algoritmo específico → tentava e erro.

![analisador sintatioc](https://github.com/user-attachments/assets/ba88ab9b-9808-48f5-b784-49ade1dd71fc)

## Análise semântica

SOMA foi declarada?

SOMA é variável?

Qual o escopo de SOMA?

Qual o tipo de SOMA?

Coloca informações adicionais na árvore

## Geração de código

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
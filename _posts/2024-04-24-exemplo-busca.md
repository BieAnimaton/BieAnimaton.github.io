---
title: "Exemplos de Exercícios de Busca"
excerpt: "Alguns exemplos de exercícios de Busca para praticar."
categories:
  - IA
tags:
  - IA
  - Inteligência Artificial
  - Busca
  - Exercícios Busca
  - P1

toc: true
---

## Exercícios de Busca
Estado inicia (estado do começo do problema).  
Teste de objetivo (o que quero alcançar).  
Função sucessor (função para avançar o estado).  
Função de custo (o que custou mudar de estado).  

### Exercício 1
Você deve colorir um mapa plano utilizando apenas quatro cores de tal modo que não haja duas regiões adjacentes com a mesma cor.  

        Estado inicial: nenhuma região colorida no mapa.
		Teste de objetivo: todas as regiões coloridas e nenhuma região adjacente com a mesma cor.
		Função sucessor: atribuir uma cor a uma região que esteja sem cor.
		Função de custo: número total de atribuições.

### Exercício 2
Um macaco com um metro de altura está em uma sala em que algumas bananas estão suspensas no teto a 2,5 metros de altura. Ajude o macaco a alcançar as bananas. A sala contém dois engradados empilháveis e móveis com um metro de altura cada.  

        Estado inicial: como descrito no enunciado.
		Teste de objetivo: macaco alcançou as bananas.
		Função sucessor: subir no engradado, descer do engradado, mudar o engradado de lugar, andar de um lugar a  outro, agarrar bananas
		Função de custo: número total de ações.

### Exercício 3
Considere um programa que emite a seguinte mensagem: “registro de entrada inválido” quando alimentado com um certo arquivo de registros de entrada. Sabendo que cada registro é independente, como descobrir qual registro é inválido?  

        Estado inicial: programa não emite nenhuma mensagem.
		Teste de objetivo: receber a mensagem "registro de entrada inválido".
		Função sucessor: escolher o próximo arquivo para alimentar o sistema.
		Função de custo: número total de escolhas.
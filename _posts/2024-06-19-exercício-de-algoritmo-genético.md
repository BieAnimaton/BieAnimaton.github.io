---
title: "Exercícios de Algoritmo Genético"
excerpt: "Dois Exemplos de Exercícios de Algoritmo Genético."
categories:
  - IA
tags:
  - Inteligência Artificial
  - IA
  - Algoritmo Genético
  - GA
  - Exercícios

toc: true
---

# Problema 1

![image](https://github.com/BieAnimaton/BieAnimaton/assets/52220244/11aacf88-569a-407c-addf-192aab7ac36d)

Este é mais tranquilo, pois não impõe nenhum limite e você já pode perceber que o máximo é 31.  
A função f(x) também é fácil.  
Usaremos quantas gerações precisar e apenas 1 ponto de corte.  
	
00 = 00000  
31 = 11111  
Cromossomo de 5 bits.  
Avaliação é a própria função.  

## Iniciando
### 1ª Geração

- **Seleção do melhor indivíduo (maior avaliação):**  
indivíduos....x....f(x)	Pedaço da roleta (%)  
a1 = 10000  16	256		22,63%  
a2 = 11001  25	625		55,26%  
a3 = 01101  13	169		14,94%  
a4 = 01001  9   81		7,16%  

TOTAL f(x)		1131

**OBS: para calcular o pedaço da roleta:**

a1 = (256 / 1131) * 100 = 22,63%  
a2 = (625 / 1131) * 100 = 55,26%  
a3 = (169 / 1131) * 100 = 14,94%  
a4 = (81 / 1131) * 100 = 7,16%  

- **Melhores em ordem:**

11001, 10000, 01101 e 01001

- **Crossover (1 ponto) + mutação:**

110|01 -> 11000  
100|00 -> 10001 -> mutação -> 11001  

01|101 -> 01001 -> mutação -> 11001  
01|001 -> 01101

- **RESULTADO:**

11001 + 10000  =  11000 e 11001  
01101 + 01001  =  11001 e 01101

### 2ª Geração

- **Seleção do melhor indivíduo (maior avaliação):**

indivíduos....x....f(x)	Pedaço da roleta (%)  
a1 = 11000	24	576		28,87%  
a2 = 11001	25	625		31,32%  
a3 = 11001	25	625		31,32%  
a4 = 01101	13	169		8,47%  

TOTAL f(x)			1995  

- **Melhores em ordem:**

11001, 11001, 11000 e 01101  

- **Crossover (1 ponto) + mutação:**

11|001 -> 11001 -> mutação -> 11101  
11|001 -> 11001  

1100|0 -> 11001  
0110|1 -> 01100 -> mutação -> 11100  

- **RESULTADO:**

11001 + 11001  =  11101 e 11001  
11000 + 01101  =  11001 e 11100  

### 3ª Geração

- **Seleção do melhor indivíduo (maior avaliação):**

indivíduos....x....f(x)	Pedaço da roleta (%)  
a1 = 11101	29	841		29,25%  
a2 = 11001	25	625		21,73%  
a3 = 11001	25	625		21,73%  
a4 = 11100	28	784		27,26%  

TOTAL f(x)			2875

- **Melhores em ordem:**

11101, 11100, 11001 e 11001

- **Crossover (1 ponto) + mutação:**

1110|1 -> 11100  
1110|0 -> 11101 -> mutação -> 11111 (primeiro bom)  

11|001 -> 11001 -> mutação -> 11101  
11|001 -> 11001

- **RESULTADO:**

11101 + 11100  =  11100 e 11111   
11001 + 11001  =  11101 e 11001  

### 4ª Geração

- **Seleção do melhor indivíduo (maior avaliação):**

indivíduos....x....f(x)	Pedaço da roleta (%)  
a1 = 11100	28	784		26,17%  
a2 = 11111	31	961		32,08%  
a3 = 11001	25	625		20,86%  
a4 = 11001	25	625		20,86%  

TOTAL f(x)			2995

- **Melhores em ordem:**

11111, 11100, 11001 e 11001

- **Crossover (1 ponto) + mutação:**

1111|1 -> 11110 -> mutação -> 11111 (primeiro bom)  
1110|0 -> 11101  

1|1001 -> 11001  
1|1001 -> 11001 -> mutação -> 11101  

- **RESULTADO:**

11111 + 11100  =  11111 e 11101  
11001 + 11001  =  11001 e 11101  

### 5ª Geração

- **Seleção do melhor indivíduo (maior avaliação):**

indivíduos....x....f(x)	Pedaço da roleta (%)  
a1 = 11111	31	961		29,40%  
a2 = 11101	29	841		25,73%  
a3 = 11001	25	625		19,12%  
a4 = 11101	29	841		25,73%  

TOTAL f(x)			3268  

- **Melhores em ordem:**

11111, 11101, 11101 e 11001

- **Crossover (1 ponto) + mutação:**

1111|1 -> 11111 (primeiro bom)  
1110|1 -> 11101 -> mutação -> 11111 (segundo bom)  

1|1101 -> 11001  
1|1001 -> 11101 -> mutação -> 11111 (terceiro bom)  

- **RESULTADO:**
11111 + 11101  =  11111 e 11111  
11101 + 11001  =  11001 e 11111  

# Problema 2
![image](https://github.com/BieAnimaton/BieAnimaton/assets/52220244/3c618a13-b236-43f2-b6d6-483064850bdc)
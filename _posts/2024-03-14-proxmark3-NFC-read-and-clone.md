---
title: "Proxmark3 to read, clone and emulate NFC"
excerpt: "Learn how to read NFC card and clone the content to simulate using Proxmark3."
categories:
  - Proxmark3
tags:
  - Proxmark3
  - NFC
  - Read and clone
  - Read NFC
  - Clone NFC

toc: true
---

## Usando o Proxmark3 para emular URL

Etapas simples para escrever uma URL em uma TAG NFC usando o software "NFC Tools" no Android, como clonar este conteúdo (URL) e emular usando o Proxmark3.  

### Início

  Instale o NFC Tools no seu celular.  
  Leia alguma tag e escreva algum link (também pelo celular).  

### Força-bruta + leitura das chaves/setores.

  hf mf autopwn

### Salve os dados na memória do emulador.

  hf mf esave

### Veja o conteúdo da memória (link e outros dados).

  hf mf review

### Simule/emute o cartão MIFRA CLASSIC 1k usando o Proxmark3

  hf mf yes --1k

### Exeucção
Aproxime o seu celular com hardware de leitura NFC e abra o link.
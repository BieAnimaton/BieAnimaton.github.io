---
title: "PowerShell add or remove elements from an Array"
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

Simple steps to write url on RFID tag using "NFC Tools" software on Android, how to clone and emulate with proxmark3.

# proxmark3_NFC_read_and_clone

install NFC Tools on your cell phone  
read tag and write some link

### bruteforce + read the keys/sectors
hf mf autopwn

### save the data in the emulator memory
hf mf esave

### view memory data (link or etc)
hf mf review

### simulate/emulate MIFRA CLASSIC 1k card using proxmark3
hf mf yes --1k

### approach cell phone with nfc reader hardware and enter the link
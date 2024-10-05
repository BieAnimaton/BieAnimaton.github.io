---
title: "Sistemas Distribuídos - Resumão para P2"
excerpt: "Resumo Sistemas Distribuídos"
categories:
  - Sistemas Distribuídos
tags:
  - Sistemas Distribuídos
  - Resumo
  - Teoria

toc: true
---

# Aula VI

## Por que sistemas distribuídos usam resolução de nomes?

- Compartilhamento de recursos  
- Identificação única de entidades  
- Referência de localidades  

## O que é resolução de nomes?

Processo de identificação de uma entidade através de seu nome.

Geralmente realizada através da consulta a um servidor de nomes.

## O que são nomes?

Descrevem entidades: computadores, usuários, impressoras…

Referenciam endereços: endereço é um tipo especial de nome que se refere a um ponto de acesso de uma entidade.

Identificador: referência única de uma entidade.

Fornecem transparência de localização:
- um ponto de acesso pode ser modificado, mas seu nome mantido para o sistema.
- o servidor de nomes deve manter a referência atual dos pontos de acesso.

## O que são Names Spaces

Forma como os nomes estão organizados (grafos).

![image](https://github.com/user-attachments/assets/a45f09dd-59cd-44a9-9f5b-7b5d749ce273)

## Explique a organização hierárquica

Existem 3 níveis.

### Nível global

Nós de mais alto nível (nó raiz e seus filhos diretos).  
Estrutura normalmente estável (modifica-se muito pouco).  
Descrevem organizações ou grupos de organizações.  

### Nível administrativo

Abaixo do nível global.  
Alteram-se com pouca frequência.  
Referenciam grupos de entidades de uma mesma organização ou unidade administrativa (exemplo: departamentos de uma organização).  

### Nível gerencial
 
Alteram-se com maior frequência.  
Representam entidades, como hosts ou sistemas de arquivos.  

## DNS

Domain Name System - serviço de nomes da Internet.

![image](https://github.com/user-attachments/assets/68a17f1e-e736-48c7-970b-72b70fb2b206)

## Resolução de nomes

### Resolução iterativa

O nome é resolvido através de diversas iterações de consulta, partindo do nível global ao nível gerencial.

Ex:

![image](https://github.com/user-attachments/assets/fe600bae-f92d-4970-a203-45df41c6ec2b)

ftp:// -> name space -> porta aplicação.  
ftp.cs.vu.nl -> DNS host (IP).  
/pub/globe/index.txt -> caminho FS.  

## Servidores de nomes

As implementações mais difundidas são:

- DNS (Domain Name System): instituído pela RFC 1034, é o serviço de nomes padrão para a Internet.
- LDAP (Lightweight Directory Access Protocol): implementação aberta inspirada no modelo de serviço de diretórios X.500 DAP para uso na Internet.
- NDS (Novell Directory Services): implementação do serviço de diretórios da Novell, baseada no X.500 DAP.
- Active Directory: implementação padrão do LDAP pela Microsoft.

## X.500 DAP ( Directory Access Protocol)

Padrão da ISO/ITU que define um modelo independente de plataforma para o serviço de diretórios.

Diretório: banco de dados com informações sobre objetos e entidades, baseadas em atributos e organizadas em forma de árvore.

- DIB (Directory Information Base)  
Banco de dados com os registros do serviço de diretório.  

- DIT (Directory Information Tree)  
Define a organização hierárquica dos objetos  

- Objetos  
Descritos pelas entradas no diretório e possuem atributos  

## Hierarquia X.500

Diferentes classes para objetos, para cada nível  

(Root)  
DC Domain Component  
C Country  
L Locality  
O Organization  
OU Organizational Unit  
CN Common Name  

Regras de acesso (ACL – access control lists)  
São definidas entre objetos, através de seus atributos

## O que é LDAP?

Lightweight Directory Access Protocol.

Desenvolvido inicialmente para ser cliente do X.500.  

O X.500 impunha uma implementação complexa de protocolo, para
operar sobre a pilha ISO/OSI.

O LDAP foi adaptado para operar sobre a pilha TCP/IP e tornou-se um
padrão de fato para a Internet.

Sua versão 3 é descrita pela RFC 2251

## Exemplo de entrada LDAP

![image](https://github.com/user-attachments/assets/6e46416d-f0d2-4b97-b8ff-489560bd91d7)

## Exemplo de hierarquia LDAP

![image](https://github.com/user-attachments/assets/8894736f-1469-44d3-a55b-2183ef29bf80)

## O que é LDIF?

LDAP Data Interchange Format (RFC 2849).

Formato de intercâmbio de informações para o LDAP.

Descreve o diretório e suas entradas em formato texto.

Sintaxe:

![image](https://github.com/user-attachments/assets/6b3b56af-9581-436e-bd57-f2cc5c1c7f30)

## Exemplo LDIF com 2 entradas

![image](https://github.com/user-attachments/assets/3902b9b4-00c9-4f4d-a19e-b260bbb274ed)
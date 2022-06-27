---
layout: post
title: Fastify + gRPC 
subtitle: Sviluppare API REST super veloci con gRPC e Fastify con NodeJS
thumbnail-img: /assets/img/fastify_gRPC_thumb.jpg
share-img: /assets/img/fastify_gRPC_thumb.jpg
tags: [gRPC, API, REST, Fastify, NodeJS]
---

Spesso ci siamo trovati difronte al problema di come rendere performati i nostri progetti API REST, soprattutto quando le applicazioni client richiedono una mole di dati notevole, come nel caso di grossi gestionali, con query SQL complesse eseguite su un database remoto.

Per risolvere questo problema possiamo considerare le elevate prestazioni di _protocol buffer (Protobuf)_ sviluppato e utilizzato da Google per la comunicazione interna dei propri server per diminuire il tempo di latenza nella risposta dei numerosi microservizi collegati tra di loro.

In particolare cerchiamo di integrare [gRPC](https://grpc.io) con [Fastify](https://www.fastify.io), un server molto efficiente, decisamente uno dei più veloci framework web.

![gRPC+Fastify](/assets/img/posts/gRPC.jpg)

**gRPC** è un framework RPC ad utilizzo universale compatibile con diversi linguaggi di programmazione e pensato per ottenere elevate prestazioni grazie al [_protocol buffer_](https://developers.google.com/protocol-buffers)_ sul HTTP/2 sviluppato da Google che serializza i dati strutturati, come JSON o XML, tranne per il fatto che è più piccolo e più veloce e genera collegamenti in lingua nativa.

_protocol buffer_ è indipendente dal linguaggio di programmazione ed è definito da un linguaggio di definizione creato nei file _.proto_.

<iframe width="100%" height="480" src="https://www.youtube.com/embed/72mPlAfHIjs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Creazione progetto Fastify 
Utilizziamo fastify-cli per creare il nostro primo progetto API REST per la gestione di un planning dei dipendenti di un cantiere:

```bash
npm install --global fastify-cli
fastify generate planning
```
![Fastify 1](/assets/img/posts/fastify1.png)

  
una volta creato il progetto installiamo i componenti cominciamo a configurare gRPC:
```
cd planning
npm install
```

L'obiettivo finale del nostro progetto sarà la seguente struttura di cartelle:
![Fastify 2](/assets/img/posts/fastify2.png)
 
## gRPC  
 
Nella cartella gRPC scriveremo tutti gli script del nostro server gRPC compreso il file .proto di definizione.

Il file _gRPC/planning.proto_ conterrà la definizione dei messaggi di input _Request_ e la risposta dei servizi _ListEmployees_ per la lista dei dipendenti e _ListBuildings_ per la lista dei cantieri da microservizi remoti. La risposta attesa sarà un array _data_ di messaggi _Employee_ e _Buildings_ chiamato Employee_Response e Building_response.



Risposta CRUD dal database

```javascript
syntax = "proto3";

package timereport;

service TimeReport {
    rpc ListEmployee(Request) returns (Employee_Response) {}
    rpc ListBuildings(Request) returns (Building_Response) {}

}

message Request {
    string token = 1;
    int32 page = 2;
    int32 rows = 3;
}

message Employee {
    int32 id = 1;
    string name = 2;
    string username = 3;
    string role = 4;
}

message Building {
    int32 id = 1;
    string name = 2;
    string description = 3;
}

message Employee_Response {
    repeated Employee data = 1;
}

message Building_Response {
    repeated Employee data = 1;
}

```

Libreria in comune per client/server
server gRPC
client gRPC

configurazioni variabili ambiente Fastify
Hooks di avvio con avvio server gRPC
EndPoint API
Performance 



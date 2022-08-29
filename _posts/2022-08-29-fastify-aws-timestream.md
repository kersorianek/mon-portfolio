---
layout: post
title: fastify-aws-timestream
subtitle: gestione di database, tabelle e creazione di query pianificate con AWS Timestream
gh-repo: gzileni/fastify-aws-timestream
gh-badge: [star, fork, follow]
cover-img: /assets/img/fastify-aws-timestream.jpg
thumbnail-img: /assets/img/fastify-aws-timestream_thumb.jpg
share-img: /assets/img/fastify-aws-timestream.jpg
tags: [Fastify, AWS]
---

[Fastify-AWS-TimeStream](https://github.com/gzileni/fastify-aws-timestream) è un plugin per [Fastify](https://www.fastify.io/) per la gestione di database, tabelle e creazione di query pianificate con [AWS Timestream](https://aws.amazon.com/it/timestream/).

AWS Timestream è un database di serie temporali veloce, scalabile, serverless, che semplifica l'archiviazione e l'analisi di trilioni di punti dati di serie temporali al giorno.

Ad esempio con AWS Timestream è possibile gestire progetti per il monitoraggio delle metriche per migliorare le prestazioni e la disponibilità delle applicazioni, archiviare e analizzare telemetria industriale per ottimizzare, gestione e manutenzione delle apparecchiature, oppure archiviare e analizzare dati dei sensori #IoT.

## Storage

*fastify-aws-timestream* permette di creare il Database, il livello-0 dei dati, con le sue tabelle e serie temporali. I dati archiviati in Timestream sono in ordine temporale e in base agli attributi di contesto, e vengono scritti in tabelle che possono essere in due modalità: in-memory e magnetic.

Le scritture di dati vengono fatte a velocità elevata nella memoria in cui i dati sono ottimizzati per le scritture. Quando è trascorso un periodo di tempo configurato per le esigenze di scrittura, i dati possono fluire automaticamente dall'archivio di memoria all'archivio magnetico per ottimizzare i costi.

*fastify-aws-timestream* permette di impostare in Timestream un criterio di conservazione dei dati nell'archivio di memoria. Una volta che i dati sono disponibili nell'archivio magnetico, vengono riorganizzati in un formato altamente ottimizzato per letture di dati di grandi dimensioni. L'archivio magnetico ha anche una politica di conservazione dei dati che può essere configurata se esiste una soglia di tempo in cui i dati sopravvivono alla loro utilità. Quando i dati superano l'intervallo di tempo definito per il criterio di conservazione dell'archivio magnetico, vengono rimossi automaticamente.

AWS Timestream offre la possibilità di scrivere dati utilizzando due tipi di record, ovvero **single-measure**, una riga di tabella per record e **multi-measure**, più misure in una singola riga della tabella, molto utili per migrare i dati esistenti dai database relazionali ad Amazon Timestream con modifiche minime.

**fastify-aws-timestream scrive record nella tabella del database timestream utilizzando multi-measure.**

La scritture del record per multi-measure ha alcuni vantaggi nell'utilizzo:

- **Prestazioni e costi**: i record di più misure consentono di scrivere più misure di serie temporali in un'unica richiesta di scrittura, aumentando la portata di scrittura e riducendone i costi;
- **Semplicità delle query**: con record di più misure, non è necessario scrivere quei complesse perché le misure vengono archiviate come colonne in una singola riga della tabella.
- **Flessibilità nella modellazione dei dati**: Un record multi-measure può avere più attributi del tipo di dati TIMESTAMP, oltre al campo dell'ora in un record.

## Query

Per le query con AWS Timestream è facile perché si usa SQL con estensioni per il supporto specifico per serie temporali (tipi di dati e funzioni specifici per serie temporali).

**Con fastify-aws-timestream è possibile configurare AWS Timestream con query pianificate.**

Le query pianificate sono una funzionalità di AWS Timestream, è serverless e scalabile per il calcolo e l'archiviazione di aggregati, roll-up e altre forme di dati pre-laborati generalmente utilizzati per alimentare dashboard operativi, report aziendali, analisi ad hoc e altre applicazioni. Le query pianificate rendono l'analisi in tempo reale più efficiente e conveniente, così è possibile ricavare informazioni aggiuntive dai tuoi dati e continuare a prendere decisioni aziendali migliori. Con le query pianificate eseguite periodicamente e automaticamente si scrivono in modo affidabile i risultati della query in una tabella separata entro pochi minuti.

I vantaggi sono:

- **Facilità operativa**: le query pianificate sono serverless e completamente gestite. Bisogna solo definire la quei SQL e AWS Timestream si occuperà del resto.
- **Prestazioni e costi**: poiché le query pianificate precalcolano gli aggregati, i rollup e altre operazioni di analisi in tempo reale per i dati e archiviano i risultati in una tabella, le query che accedono alle tabelle popolate da query pianificate contengono meno dati rispetto alle tabelle di origine. Pertanto, le query eseguite su queste tabelle sono più veloci ed economiche. È inoltre possibile conservare questi dati per una durata maggiore nell'archivio di memoria a una frazione del costo di conservazione dei dati di origine nell'archivio di memoria.
- **Interoperabilità**: le tabelle popolate da query pianificate offrono tutte le funzionalità esistenti delle tabelle Timestream e possono essere utilizzate con tutti i servizi e gli strumenti che funzionano con Timestream

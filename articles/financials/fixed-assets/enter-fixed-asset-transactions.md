---
title: Alternativer for anleggsmiddeltransaksjon
description: Denne artikkelen beskriver de ulike metodene som er tilgjengelige for oppretting av anleggsmiddeltransaksjoner.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3d16b43eda0157e63a0d30fe806dac9a359d5fa4
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="fixed-asset-transaction-options"></a>Alternativer for anleggsmiddeltransaksjon

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver de ulike metodene som er tilgjengelige for oppretting av anleggsmiddeltransaksjoner.

Du kan definere anleggsmidler for integrasjon med Leverandører, Kunder, Innkjøp og leverandører og Økonomimodul. Du kan også overføre varer i Lagerstyring til Anleggsmidler hvis du vil bruke disse elementene internt.

## <a name="accounts-payable"></a>Leverandører
Du kan registrere anleggsmiddeltransaksjoner på Journalbilag-siden. Denne siden kan åpnes fra Fakturajournal-siden. Du kan også åpne siden Journalbilag fra Fakturagodkjenningsjournal-siden. I feltet Motkontotype velger du Anleggsmiddel. Deretter velger du et anleggmiddelnummer i Motkonto-feltet. I kategorien Anleggsmidler angir du verdier i feltene Transaksjonstype og Tablå.

## <a name="accounts-receivable"></a>Kundereskontro
Du kan registrere anleggsmiddeltransaksjoner på Fritekstfaktura-siden.  På siden Fritekstfakturaer, i rutenettet Fakturalinjer, velger du en linjevare. Klikk hurtigfanen Linjedetaljer. Angi nummeret og tablået for anleggsmiddelet i avhendingstransaksjonen. Når det gjelder fritekstfakturaer, er anleggsmiddeltransaksjoner alltid av typen Avhendingssalg.

## <a name="procurement-and-sourcing"></a>Innkjøp og leverandører
Du kan registrere anleggsmiddeltransaksjoner på Bestilling-siden. Angi nødvendig informasjon for å opprette en salgsordre, og klikk deretter OK. Klikk hurtigfanen Linjedetaljer på siden Bestilling. Deretter angir du informasjon om anleggsmiddelet i kategorien Anleggsmidler. 

Hvis du vil postere en anskaffelsestransaksjon for et eksisterende anleggsmiddel, må du angi anleggsmiddelets nummer, tablå og transaksjonstype. Anlegsmidlet kan ikke posteres hvis noe av denne informasjonen mangler. Hvis du vil postere en anskaffelsestransaksjon for et nytt anleggsmiddel, merker du av for Nytt anleggsmiddel og velger anleggsmiddelgruppen som det nye anleggsmiddelet skal tilordnes. Ingen anleggsmiddelfelt er imidlertid tilgjengelige for en linje hvis varen er en lagermodellgruppe som bruker en lagermodell med standard kostpris. I tillegg avgjør alternativene som er definert på siden Parametere for anleggsmidler, om du kan postere anskaffelsestransaksjoner fra innkjøpsmodulene. 

Når en bestilling eller Lager til anleggsmidler-journalen brukes til anskaffelse av anleggsmidler, påvirkes lagerverdien.

## <a name="general-ledger"></a>Økonomimodul
Alle typer anleggsmiddeltransaksjoner kan posteres på siden Økonomijournal. Du kan også bruke journaler i Anleggsmidler til å postere anleggsmiddeltransaksjoner.

## <a name="options-for-entering-fixed-asset-transaction-types"></a>Alternativer for å angi anleggsmiddeltransaksjonstyper


| transaksjonstype                    | Modul                   | Opsjoner                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Anskaffelse, Anskaffelsesjustering | Anleggsmidler             | Anleggsmidler, Beholdning til anleggsmidler   |
|                                     | Økonomimodul           | Økonomijournal                           |
|                                     | Leverandører         | Fakturajournal, Fakturagodkjenningsjournal |
|                                     | Innkjøp og leverandører | Bestilling                            |
| Avskrivning                        | Anleggsmidler             | Anleggsmidler                              |
|                                     | Økonomimodul           | Økonomijournal                           |
| Avhending                            | Anleggsmidler             | Anleggsmidler                              |
| ** **                               | Økonomimodul           | Økonomijournal                           |
| ** **                               | Kundereskontro      | Fritekstfaktura                         |



Hvis du vil ha mer informasjon, se [Integrering av anleggsmidler](fixed-asset-integration.md).





---
title: Alternativer for transaksjon av anleggsmiddel
description: Dette emnet beskriver de ulike metodene som er tilgjengelige for oppretting av anleggsmiddeltransaksjoner.
author: ShylaThompson
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: roschlom
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f9cd8846688e6b70f3ac2034caa1a9e3015355e
ms.sourcegitcommit: f9b40df70a77136529fbc790325ed657eb203731
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/20/2021
ms.locfileid: "6645378"
---
# <a name="fixed-asset-transaction-options"></a>Alternativer for transaksjon av anleggsmiddel

[!include [banner](../includes/banner.md)]

Dette emnet beskriver de ulike metodene som er tilgjengelige for oppretting av anleggsmiddeltransaksjoner.

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

### <a name="options-for-entering-fixed-asset-transaction-types"></a>Alternativer for å angi anleggsmiddeltransaksjonstyper


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

Den gjenværende verdien for nedskrivningsperioder for anleggsmiddelet oppdateres ikke når en journallinje for avskrivningstransaksjonstype opprettes manuelt eller importeres via en dataenhet. Denne verdien oppdateres når avskrivningsforslagsprosessen brukes til å opprette journallinjen.

Hvis du vil ha mer informasjon, se [Integrering av anleggsmidler](fixed-asset-integration.md).

### <a name="transactions-that-require-different-voucher-numbers"></a>Transaksjoner som krever ulike bilagsnumre

Følgende anleggsmiddeltransaksjoner bruker forskjellige bilagsnumre:

- En ekstra anskaffelse gjøres på et anleggsmiddel og "oppsamlingsavskrivning" beregnes.
- Et anleggsmiddel er delt.
- En parameter for å beregne avskrivning ved avhending aktiveres, og deretter avhendes anleggsmiddelet.
- Servicedatoen for et anleggsmiddel er før anskaffelsesdatoen. Derfor posteres en avskrivningsjustering.

> [!NOTE]
> Når du angir transaksjoner, må du kontrollere at alle transaksjonene gjelder det samme anleggsmidlet. Bilaget blir ikke postert hvis det inneholder mer enn ett anleggsmiddel, selv om **Nytt bilag**-feltet er satt til **Bare ett bilagsnummer** på **Journalnavn**-siden i økonomimodulen. Hvis du tar med flere anleggsmidler i bilaget, vises meldingen "Det kan bare være én anleggsmiddeltransaksjon per bilag", og du vil ikke kunne postere bilaget.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

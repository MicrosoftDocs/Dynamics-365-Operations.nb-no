---
title: "Lageropptelling på et lager"
description: "Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageropptellingsjournal for å telle en bestemt vare på en lokasjon i lageret."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 1d2ecf1cd80e05b59f206fb5f684d6a86fa5733e
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="count-inventory-in-a-warehouse"></a>Lageropptelling på et lager

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageropptellingsjournal for å telle en bestemt vare på en lokasjon i lageret. Fremgangsmåten gjelder for "grunnleggende lageraktiviteter"-funksjoner, tilgjengelige i lagerstyringsmodulen, ikke for lagerstyringsfunksjonaliteten som er tilgjengelig i lagerstyringsmodulen. Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Hvis du bruker dine egne data, må du kontrollere at du har produkter og lokasjoner definert, og at du har opprettet et beholdningsjournalnavn for opptellingsjournaler. Beholdningsopptelling utføres vanligvis av en lageransatt.


## <a name="create-an-inventory-counting-journal"></a>Opprette en lageropptellingsjournal
1. Gå til Lagerstyring > Loggoppføringer > Vareopptelling > Opptelling.
2. Klikk Ny.
3. Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.
4. Klikk journalnavnet for beholdningsopptelling som du vil bruke, i listen
    * Noen andre felt fylles ut basert på oppsettet av standardnavn for lageropptellingsjournal som du velger.  
5. Klikk rullegardinknappen i feltet Arbeider for å åpne oppslaget.
6. Velg arbeideren du vil bruke, i listen.
7. Klikk Velg.
8. Klikk OK.

## <a name="create-journal-lines"></a>Opprette journallinjer
1. Klikk Ny.
2. Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
3. Finn og velg ønsket post i listen.
    * Hvis du bruker demonstrasjonsdataselskapet USMF, velger du "A0001".  
4. Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.
5. Finn og velg ønsket post i listen.
    * Hvis du bruker demonstrasjonsdataselskapet USMF, velger du område 2.  
6. Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.
7. Finn og velg ønsket post i listen.
    * Hvis du bruker demonstrasjonsdataselskapet USMF, velger du lager 24.  
8. Klikk rullegardinknappen i Lokasjon-feltet for å åpne oppslaget.
9. Finn og velg ønsket post i listen.
    * Hvis du bruker demonstrasjonsdataselskapet USMF, velger du lokasjon BULK-001.  
10. Angi et tall i feltet Opptelt.
    * Hvis du angir et opptelt nummer som er forskjellig fra nummeret som vises i feltet Beholdning, oppdateres feltet Antall for å vise avviket.  
11. Klikk Lagre.

## <a name="post-the-inventory-counting-journal"></a>Postere lageropptellingsjournalen
1. Klikk Poster.
    * Når du posterer en lageropptellingsjournal, og hvis det opptelte beløpet er forskjellig fra beløpet som rapporteres i feltet Beholdning, blir det postert et lagermottak eller en lageravgang, lagernivå og lagerverdi endres og finanstransaksjoner blir generert.  
2. Klikk OK.

## <a name="view-inventory-transactions"></a>Vis lagertransaksjoner
1. Klikk Lager.
2. Klikk Transaksjoner.
    * Her kan du se relaterte transaksjoner som opprettes når du posterer lageropptellingsjournalen.   


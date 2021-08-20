---
title: Justere lagernivåer i lageret (grunnleggende lageraktiviteter)
description: Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en beholdningsjusteringsjournal for å justere lagernivåer for produkter i lageret.
author: MarkusFogelberg
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee20fdcb1a0b28500f85cfe50eb942ac565a2960e5bceed7d4d4427bc9bd7218
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765520"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a>Justere lagernivåer i lageret (grunnleggende lageraktiviteter)

[!include [banner](../../includes/banner.md)]

Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en beholdningsjusteringsjournal for å justere lagernivåer for produkter i lageret. Du må ha en lagerjournalnavn definert for lagerjusteringer før du starter dette. Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Disse oppgavene vil vanligvis utføres av en lageransatt.


## <a name="create-an-inventory-adjustment-journal"></a>Opprette en beholdningsjusteringsjournal
1. Gå til Lagerstyring > Journaloppføringer > Varer > Beholdningsjustering.
2. Klikk på Ny.
3. Klikk på rullegardinknappen i Navn-feltet for å åpne oppslaget.
4. Klikk på journalnavnet for beholdningsjustering som du vil bruke, i listen.
    * Noen andre felt fylles ut basert på oppsettet av navnet på lagerjusteringsjournal som du velger.  
5. Klikk på OK.

## <a name="create-journal-lines"></a>Opprette journallinjer
1. Klikk på Ny.
2. Merk varenummerfeltet i listen.
3. Velg en vare i Varenummer-feltet. Hvis du bruker demonstrasjonsdataselskapet USMF, skriver du inn "D0001".
4. Klikk på rullegardinknappen i Område-feltet for å åpne oppslaget.
5. Velg et område i listen.
6. Klikk på rullegardinknappen i Lager-feltet for å åpne oppslaget.
7. Velg et lager i listen.
    * Hvis du har valgt en vare med Lokasjon som en obligatorisk dimensjon, må du angi lokasjonen her.  
8. Angi et tall i feltet Antall.
    * Kostprisfeltet angir kostnaden per enhet for lagertilganger. Hvis kostnaden ikke er angitt for varenummeret, eller hvis du vil endre den manuelt, gjør du det her.  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a>Validere og postere beholdningsjusteringsjournalen
1. Klikk på Valider.
2. Klikk på OK.
3. Klikk på Poster.
    * Når du posterer denne typen journal, blir det postert et lagermottak eller en lageravgang, lagernivå og lagerverdi endres og finanstransaksjoner blir generert.  
4. Klikk på OK.
5. Lukk skjemaet.
6. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
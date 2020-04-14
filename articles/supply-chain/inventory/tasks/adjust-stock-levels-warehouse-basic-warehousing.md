---
title: Justere lagernivåer i lageret (grunnleggende lageraktiviteter)
description: Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en beholdningsjusteringsjournal for å justere lagernivåer for produkter i lageret.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c617517109146b96075d03b6f3549639a99d7d1c
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146083"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a>Justere lagernivåer i lageret (grunnleggende lageraktiviteter)

[!include [banner](../../includes/banner.md)]

Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en beholdningsjusteringsjournal for å justere lagernivåer for produkter i lageret. Du må ha en lagerjournalnavn definert for lagerjusteringer før du starter dette. Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Disse oppgavene vil vanligvis utføres av en lageransatt.


## <a name="create-an-inventory-adjustment-journal"></a>Opprette en beholdningsjusteringsjournal
1. Gå til Lagerstyring > Journaloppføringer > Varer > Beholdningsjustering.
2. Klikk Ny.
3. Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.
4. Klikk journalnavnet for beholdningsjustering som du vil bruke, i listen.
    * Noen andre felt fylles ut basert på oppsettet av navnet på lagerjusteringsjournal som du velger.  
5. Klikk OK.

## <a name="create-journal-lines"></a>Opprette journallinjer
1. Klikk Ny.
2. Merk varenummerfeltet i listen.
3. Velg en vare i Varenummer-feltet. Hvis du bruker demonstrasjonsdataselskapet USMF, skriver du inn "D0001".
4. Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.
5. Velg et område i listen.
6. Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.
7. Velg et lager i listen.
    * Hvis du har valgt en vare med Lokasjon som en obligatorisk dimensjon, må du angi lokasjonen her.  
8. Angi et tall i feltet Antall.
    * Kostprisfeltet angir kostnaden per enhet for lagertilganger. Hvis kostnaden ikke er angitt for varenummeret, eller hvis du vil endre den manuelt, gjør du det her.  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a>Validere og postere beholdningsjusteringsjournalen
1. Klikk Valider.
2. Klikk OK.
3. Klikk Poster.
    * Når du posterer denne typen journal, blir det postert et lagermottak eller en lageravgang, lagernivå og lagerverdi endres og finanstransaksjoner blir generert.  
4. Klikk OK.
5. Lukk skjemaet.
6. Lukk siden.


---
title: Riktig lagersporingsinformasjon
description: "Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for å korrigere lagersporingsinformasjon."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e28d10646f01604098de8cedc30c8c7a7c89866b
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="correct-inventory-tracking-information"></a>Riktig lagersporingsinformasjon

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for å korrigere lagersporingsinformasjon. I dette eksemplet vil vi oppdatere informasjonen for en partikontrollert vare ved å endre et feilregistrert parti til et annet parti. Du kan gå gjennom denne prosedyren i demonstrasjonsselskapet USPI eller ved hjelp av dine egne data. Hvis du bruker dine egne data, må du ha en vare som er partiaktivert, og den må ikke være lokasjonskontrollert. Du må også ha et lagerjournalnavn definert for lageroverføringer. Disse oppgavene vil vanligvis utføres av en lageransatt.


## <a name="create-an-inventory-transfer-journal"></a>Opprette en beholdningsoverføringsjournal
1. Gå til Overføring.
2. Klikk Ny.
3. Angi eller velg en verdi i Navn-feltet.
4. Klikk OK.

## <a name="create-journal-lines"></a>Opprette journallinjer
1. Klikk Ny.
2. Angi eller velg en verdi i Varenummer-feltet.
    * Hvis du bruker USPI, velger du varen M5003.  
3. Angi et tall i feltet Antall.
4. Klikk kategorien Lagerdimensjoner.
5. Angi eller velg en verdi i Partinummer-feltet.
6. Angi eller velg en verdi i Område-feltet.
7. Angi eller velg en verdi i feltet Lager.
8. Angi eller velg en verdi i Partinummer-feltet.

## <a name="post-the-journal"></a>Poster journalen
1. Klikk Poster.
2. Klikk OK.

## <a name="check-tracing-information"></a>Kontrollere sporingsinformasjon
1. Klikk Lager.
2. Klikk Spor.
3. Klikk OK.
    * Hvis du bruker denne sporingsinformasjonen, kan du spore tilbake til partiet du korrigerte lageret fra.  Du kan også bruke siden Varesporing for å se denne informasjonen.  
4. Lukk siden.

## <a name="check-inventory-transactions"></a>Kontrollere lagertransaksjoner
1. Klikk Lager.
2. Klikk Transaksjoner.
    * Her kan du se transaksjonene som ble opprettet da du posterte journalen.   


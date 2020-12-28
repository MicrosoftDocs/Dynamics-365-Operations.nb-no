---
title: Riktig lagersporingsinformasjon
description: Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for å korrigere lagersporingsinformasjon.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8a488d4c30923445b3ebc2626a79b8fa45012c7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434676"
---
# <a name="correct-inventory-tracking-information"></a>Riktig lagersporingsinformasjon

[!include [banner](../../includes/banner.md)]

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


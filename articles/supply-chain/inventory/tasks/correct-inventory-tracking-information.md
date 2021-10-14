---
title: Riktig lagersporingsinformasjon
description: Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for å korrigere lagersporingsinformasjon.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69921651ecd0969e9cdd3cdd3740db212a1953e1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573807"
---
# <a name="correct-inventory-tracking-information"></a>Riktig lagersporingsinformasjon

[!include [banner](../../includes/banner.md)]

Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for å korrigere lagersporingsinformasjon. I dette eksemplet vil vi oppdatere informasjonen for en partikontrollert vare ved å endre et feilregistrert parti til et annet parti. Du kan gå gjennom denne prosedyren i demonstrasjonsselskapet USPI eller ved hjelp av dine egne data. Hvis du bruker dine egne data, må du ha en vare som er partiaktivert, og den må ikke være lokasjonskontrollert. Du må også ha et lagerjournalnavn definert for lageroverføringer. Disse oppgavene vil vanligvis utføres av en lageransatt.


## <a name="create-an-inventory-transfer-journal"></a>Opprette en beholdningsoverføringsjournal
1. Gå til Overføring.
2. Klikk på Ny.
3. Angi eller velg en verdi i Navn-feltet.
4. Klikk på OK.

## <a name="create-journal-lines"></a>Opprette journallinjer
1. Klikk på Ny.
2. Angi eller velg en verdi i Varenummer-feltet.
    * Hvis du bruker USPI, velger du varen M5003.  
3. Angi et tall i feltet Antall.
4. Klikk på fanen Lagerdimensjoner.
5. Angi eller velg en verdi i Partinummer-feltet.
6. Angi eller velg en verdi i Område-feltet.
7. Angi eller velg en verdi i feltet Lager.
8. Angi eller velg en verdi i Partinummer-feltet.

## <a name="post-the-journal"></a>Poster journalen
1. Klikk på Poster.
2. Klikk på OK.

## <a name="check-tracing-information"></a>Kontrollere sporingsinformasjon
1. Klikk på Lager.
2. Klikk på Spor.
3. Klikk på OK.
    * Hvis du bruker denne sporingsinformasjonen, kan du spore tilbake til partiet du korrigerte lageret fra.  Du kan også bruke siden Varesporing for å se denne informasjonen.  
4. Lukk siden.

## <a name="check-inventory-transactions"></a>Kontrollere lagertransaksjoner
1. Klikk på Lager.
2. Klikk på Transaksjoner.
    * Her kan du se transaksjonene som ble opprettet da du posterte journalen.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
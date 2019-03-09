---
title: Dele et anleggsmiddel
description: Denne oppgaveveiledningen vil dele en prosent av ett anleggsmiddeltablå til et nytt anleggsmiddeltablå.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6be9de64265a4d7b5c91af3ee8acfce80c78e0f1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "333375"
---
# <a name="split-a-fixed-asset"></a>Dele et anleggsmiddel

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaveveiledningen vil dele en prosent av ett anleggsmiddeltablå til et nytt anleggsmiddeltablå.  Den bruker regnskapsførerrollen og USMF-demonstrasjonsdataene.


## <a name="create-a-new-fixed-asset"></a>Opprett et nytt anleggsmiddel
1. Gå til Anleggsmidler > Anleggsmidler > Anleggsmidler.
2. Klikk Ny.
3. Angi eller velg en verdi i feltet Anleggsmiddelgruppe.
4. Noter anleggsmiddelnummeret for senere bruk i prosessen for deling.
5. Skriv inn en verdi i Navn-feltet.
6. Lukk skjemaet.

## <a name="split-a-fixed-asset"></a>Dele et anleggsmiddel
1. I listen finner og merker du anleggsmidlet som skal deles.
2. Klikk koblingen i den valgte raden i listen.
3. Klikk Tablåer.
    * Velg tablået som skal deles til det nye anleggsmiddelet.  
4. Klikk Funksjoner.
5. Klikk Del anleggsmiddel.
6. Angi eller velg en verdi i feltet Til anleggsmiddel.
7. Klikk rullegardinknappen i feltet Til tablå for å åpne oppslaget.
8. Angi en dato i feltet Transaksjonsdato.
9. Angi et tall i Prosent-feltet.
10. Angi eller velg en verdi i feltet Journalnavn.
11. Klikk OK.

## <a name="post-the-journal-transaction"></a>Postere journaltransaksjonen
1. Gå til Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal.
2. Velg journalen som ble opprettet med prosessen for deling, fra listen.
3. Klikk Linjer.
    * Kontroller journallinjene som er opprettet.  En anskaffelsesjusteringstransaksjon opprettes for det originale anleggsmiddelet for å redusere verdien av prosenten som er angitt under prosessen med deling.  En anskaffelsestransaksjon er opprettet for det nye anleggsmiddelet for det samme beløpet.  
4. Klikk Poster.


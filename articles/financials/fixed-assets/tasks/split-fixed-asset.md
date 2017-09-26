--- 
title: Dele et anleggsmiddel
description: "Denne oppgaveveiledningen vil dele en prosent av ett anleggsmiddeltablå til et nytt anleggsmiddeltablå."
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5aea1aab9f6b084bd0c5bd2119639bff3555bb8a
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="split-a-fixed-asset"></a>Dele et anleggsmiddel

[!include[task guide banner](../../includes/task-guide-banner.md)]

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



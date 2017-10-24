--- 
title: "Definere avskrivningstablåer "
description: "Denne oppgaveveiledningen oppretter et nytt avskrivningstablå og knytter den til en anleggsmiddelgruppe."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d06d5f92e91e33dc752bf45ab890c37dfea3888d
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-depreciation-books"></a>Definere avskrivningstablåer  

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaveveiledningen oppretter et nytt avskrivningstablå og knytter den til en anleggsmiddelgruppe.  Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.


## <a name="create-a-depreciation-book"></a>Opprette et avskrivningstablå
1. Gå til Anleggsmidler > Oppsett > Avskrivningstablåer.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Avskrivningstablå.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Merk av eller fjern merket i boksen Beregn avskrivning.
6. Klikk rullegardinknappen i feltet Avskrivningsprofil for å åpne oppslaget.
7. Finn og velg ønsket avskrivningsprofil i listen.
8. Klikk koblingen i den valgte raden i listen.
9. Klikk rullegardinknappen i feltet Alternativ avskrivningsprofil for å åpne oppslaget.
10. Velg ønsket avskrivningsprofil i listen.
11. Klikk koblingen i den valgte raden i listen.
    * Den ekstraordinære avskrivningsprofilen brukes til ytterligere avskrivning av et aktiva i uvanlige omstendigheter. Du kan for eksempel bruke denne til å registrere avskrivning som skyldes en naturkatastrofe.  
12. Merk av eller fjern merket i boksen Opprett avskrivningsjusteringer med basisjusteringer.
13. Klikk rullegardinknappen i Kalender-feltet for å åpne oppslaget.
14. Klikk koblingen i den valgte raden i listen.

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a>Knytte avskrivningstablået til en anleggsmiddelgruppe
1. Klikk Anleggsmiddelgrupper.
2. Klikk rullegardinknappen i feltet Anleggsmiddelgruppe for å åpne oppslaget.
3. Finn og velg ønsket post i listen.
4. Klikk koblingen i den valgte raden i listen.
5. Velg et alternativ i feltet Avskrivningskonvensjon.
6. Angi et tall i Levetid-feltet.
    * Legg merke til at verdien i feltet Avskrivningsperioder beregnes etter at levetiden er angitt.  



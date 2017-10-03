--- 
title: "Definere leverandørbetalingsbetingelser"
description: "Konfigurer betalingsbetingelser for leverandørfakturaer."
author: abruer
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
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: cbac3b27c25377abff341c4bf259e553c14a4ae8
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="define-vendor-payment-terms"></a>Definere leverandørbetalingsbetingelser

[!include[task guide banner](../../includes/task-guide-banner.md)]

Konfigurer betalingsbetingelser for leverandørfakturaer. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. Gå til Leverandører > Betalingsoppsett > Betalingsbetingelser.
2. Klikk Ny.
    * Siden Betalingsbetingelser brukes til å definere hvordan forfallsdatoen beregnes. Den brukes ikke til å definere hvordan kontantrabatten skal beregnes.  
3. Skriv inn en verdi i Betalingsbetingelser-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Angi et tall i Dager-feltet.
    * Tallet som er angitt her, brukes til å legge til forfallsdatoen, eller til slutten av perioden angitt i betalingsmåten. Hvis du for eksempel velger Netto, legges tallet til forfallsdatoen. Hvis du velger Inneværende måned, legges nummeret til den siste dagen i gjeldende måned for å beregne forfallsdatoen.  
6. Klikk Lagre.
7. Lukk siden.
8. Gå til Leverandører > Betalingsoppsett > Kontantrabatt.
9. Klikk Ny.
10. Angi en ID i Kontantrabatt-feltet.
11. Skriv inn en verdi i feltet Beskrivelse.
12. Hvis leverandøren tilbyr en trinnvis rabatt, velger du neste kontantrabatt etter at den gjeldende er utløpt.
13. Lukk siden.
14. Angi et tall i Dager-feltet.
    * Antallet som er angitt i Dager-feltet, brukes til å beregne kontantrabattdatoen, avhengig av hvilket alternativ som er valgt i feltet Netto/løpende. Hvis Netto er valgt, legges antallet til fakturadatoen for å bestemme kontantrabattdatoen. Hvis Gjeldende måned valgt, legges antallet til på slutten av gjeldende måned for å bestemme kontantrabattdatoen.  
15. Angi prosenten av kontantrabatten i Rabatt-feltet. 
16. Angi hovedkontoen som kontantrabatten skal posteres til for kundefakturaer.
17. Angi hovedkontoen som kontantrabatten skal posteres til for leverandørfakturaer.
    * Hvis "Motkontoer for rabatt" er satt til Bruk hovedkonto for leverandørrabatt, brukes hovedkontoen.  Hvis alternativet er satt til Kontoer på fakturalinjene, posteres kontantrabatten til anleggsmiddel/utgiftshovedkontoene på fakturalinjene.  
18. Klikk Lagre.



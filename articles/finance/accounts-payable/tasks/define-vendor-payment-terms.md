---
title: Definere leverandørbetalingsbetingelser
description: Dette emnet forklarer hvordan du konfigurerer betalingsbetingelser for leverandørfakturaer.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b69b505996b5536088578885c11a7e8c27f4975
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971859"
---
# <a name="define-vendor-payment-terms"></a>Definere leverandørbetalingsbetingelser

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer betalingsbetingelser for leverandørfakturaer. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. Gå til **Navigasjonsrute > Moduler > Leverandører > Betalingsoppsett > Betalingsbetingelser**.
2. Velg **Ny**. Siden Betalingsbetingelser brukes til å definere hvordan forfallsdatoen beregnes. Den brukes ikke til å definere hvordan kontantrabatten skal beregnes.  
3. Skriv inn en verdi i **Betalingsbetingelser**-feltet.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Angi et tall i **Dager**-feltet. Tallet som er angitt her, brukes til å legge til forfallsdatoen, eller til slutten av perioden angitt i betalingsmåten. Hvis du for eksempel velger **Netto**, legges tallet til forfallsdatoen. Hvis du velger **Inneværende måned**, legges nummeret til den siste dagen i gjeldende måned for å beregne forfallsdatoen.  
6. Velg **Lagre**.
7. Lukk siden.
8. Gå til **Leverandører > Betalingsoppsett > Kontantrabatt**.
9. Velg **Ny**.
10. Angi en ID i **Kontantrabatt**-feltet.
11. Skriv inn en verdi i **Beskrivelse**-feltet.
12. Hvis leverandøren tilbyr en trinnvis rabatt, velger du neste kontantrabatt etter at den gjeldende er utløpt.
13. Lukk siden.
14. Angi et tall i **Dager**-feltet. Antallet som er angitt i **Dager**-feltet, brukes til å beregne kontantrabattdatoen, avhengig av hvilket alternativ som er valgt i feltet **Netto/løpende**. Hvis **Netto** er valgt, legges antallet til fakturadatoen for å bestemme kontantrabattdatoen. Hvis **Gjeldende måned** er valgt, legges antallet til på slutten av gjeldende måned for å bestemme kontantrabattdatoen.  
15. Angi prosenten av kontantrabatten i **Rabatt**-feltet. 
16. Angi hovedkontoen som kontantrabatten skal bokføres på for kundefakturaer, og angi deretter hovedkontoen som kontantrabatten skal bokføres på for leverandørfakturaer. Hvis **Motkontoer for rabatt** er satt til **Bruk hovedkonto for leverandørrabatt**, brukes hovedkontoen. Hvis alternativet er satt til **Kontoer på fakturalinjene**, posteres kontantrabatten til anleggsmiddel/utgiftshovedkontoene på fakturalinjene.  
17. Velg **Lagre**.


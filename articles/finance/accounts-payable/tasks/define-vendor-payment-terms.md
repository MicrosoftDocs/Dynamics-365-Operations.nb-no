---
title: Definere leverandørbetalingsbetingelser
description: Denne artikkelen forklarer hvordan du konfigurerer betalingsbetingelser for leverandørfakturaer.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a676856ed43bf1b78684eac0682e0fdef9c84083
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906478"
---
# <a name="define-vendor-payment-terms"></a>Definere leverandørbetalingsbetingelser

[!include [banner](../../includes/banner.md)]

Denne artikkelen forklarer hvordan du konfigurerer betalingsbetingelser for leverandørfakturaer. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. Gå til **Navigasjonsrute > Moduler > Leverandører > Betalingsoppsett > Betalingsbetingelser**.
2. Velg **Ny**. Siden **Betalingsbetingelser** brukes til å definere hvordan forfallsdatoen beregnes. Den brukes ikke til å definere hvordan kontantrabatten skal beregnes.  
3. Skriv inn en verdi i **Betalingsbetingelser**-feltet.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Angi et tall i **Dager**-feltet. Tallet som er angitt her, brukes til å legge til forfallsdatoen, eller til slutten av perioden angitt i **Betalingsmetode**. Hvis du for eksempel velger **Netto**, legges tallet til forfallsdatoen. Hvis du velger **Inneværende måned**, legges nummeret til den siste dagen i gjeldende måned for å beregne forfallsdatoen.  
6. Velg **Lagre**.
7. Lukk siden.
8. Gå til **Leverandører > Betalingsoppsett > Kontantrabatt**.
9. Velg **Ny**.
10. Angi en ID i **Kontantrabatt**-feltet.
11. Skriv inn en verdi i **Beskrivelse**-feltet.
12. Hvis leverandøren tilbyr en trinnvis rabatt, velger du neste kontantrabatt etter at den gjeldende er utløpt.
13. Lukk siden.
14. Angi et tall i **Dager**-feltet. Antallet som er angitt i **Dager**-feltet, brukes til å beregne **Kontantrabattdato**, avhengig av hvilket alternativ som er valgt i feltet **Netto/løpende**. Hvis **Netto** er valgt, legges antallet til fakturadatoen for å bestemme kontantrabattdatoen. Hvis **Gjeldende måned** er valgt, legges antallet til på slutten av gjeldende måned for å bestemme kontantrabattdatoen.  
15. Angi prosenten av kontantrabatten i **Rabatt**-feltet. 
16. Angi hovedkontoen som kontantrabatten skal bokføres på for kundefakturaer, og angi deretter hovedkontoen som kontantrabatten skal bokføres på for leverandørfakturaer. Hvis **Motkontoer for rabatt** er satt til **Bruk hovedkonto for leverandørrabatt**, brukes hovedkontoen. Hvis alternativet er satt til **Kontoer på fakturalinjene**, posteres kontantrabatten til anleggsmiddel/utgiftshovedkontoene på fakturalinjene.  
17. Velg **Lagre**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

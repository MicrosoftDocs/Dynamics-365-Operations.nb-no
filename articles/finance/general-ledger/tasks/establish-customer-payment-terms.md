---
title: Opprette kundebetalingsbetingelser
description: Dette definerer et oppsett for kontantrabatt og forfallsdato.
author: aprilolson
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9b2ae5e63a2efb4bc913efa4d88c65a70133a2d9
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752783"
---
# <a name="establish-customer-payment-terms"></a>Opprette kundebetalingsbetingelser

[!include [banner](../../includes/banner.md)]

Dette definerer et oppsett for kontantrabatt og forfallsdato. Denne oppgaveveiledningen bruker USMF demo firmaet.

1. Gå til **Navigasjonsrute > Moduler > Kunder > Betalingsoppsett > Betalingsdager**. Oppsettet for **betalingsbetingelsene** er delt for **kunder** og **leverandører**. Hvis du definerer det i modulen, vil det være tilgjengelig i den andre modulen også. Når det gjelder denne oppgaveveiledningen, er alle betalingsbetingelsene under **Kunder** definert.
2. Klikk på **Ny**. Opprett en betalingsdag hvis betalingsbetingelsene krever en bestemt dag i uken (mandag, tirsdag osv) eller en bestemt dato i måneden (5., 10. osv). 
3. Angi en ID i **Betalingsdag**-feltet.
4. I **Beskrivelse**-feltet angir du en beskrivelse av betalingsdagen.
5. I **Uke/måned**-feltet velger du Uke eller Måned. Hvis du vil angi en dag i uken, for eksempel mandag, velger du Uke. Hvis du vil angi en dato i måneden, for eksempel den 10., velger du Måned. Velg Måned for dette eksemplet. 
6. Angi en dato i **Dato**-feltet. Datoen må angis som et tall, for eksempel "10", og ikke som "10.". 
7. Klikk **Lagre**.
8. Lukk siden.
9. Gå til **Navigasjonsrute > Moduler > Kunder > Betalingsoppsett > Betalingsbetingelser**. 

>[!NOTE] 
>Hvis **Betalingsbetingelser** er **Kontanter**, må **Kontantbetaling**-feltet på siden **Betalingsbetingelser** inneholde **Nei**.

10. Klikk på **Ny**. **Betalingsbetingelsene** brukes til å definere hvordan forfallsdatoene beregnes. Dato for oppsett av kontantrabatten er definert i en egen side. 
11. Angi en ID i **Betalingsbetingelser**-feltet.
12. Angi en beskrivelse i **Beskrivelse**-feltet.
13. Velg en **betalingsmåte**, for eksempel **oppkrav**, **netto**, **gjeldende måned** og så videre. **Betalingsmåten** brukes til å definere starten for beregning av forfall. **Netto** brukes for eksempel hvis forfallsdatoen alltid er et angitt antall måneder eller dager etter fakturadato. **Oppkrav** kan brukes når betaling kreves ved faktura, slik at en forfallsdato ikke blir beregnet. Velg **Gjeldende måned** for denne oppgaveveiledningen.  
14. Velg en **Betalingsdag** hvis en bestemt dag i uken eller dato skal tas med i beregningen. Avhengig av betalingsbetingelsene, kan du angi et antall i måneder eller dager. Eller du bruke **Betalingsplan** eller **Betalingsdag** for å legge til på slutten av **betalingsmåten**. Hvis forfallsdatoen alltid skal være den 10. i neste måned, velger du **Betalingsdag** på den 10. Hvis du bruker en **betalingskalender**, kan du definere hvordan forfallsdatoen skal bestemmes når den beregnede datoen lander på en ikke-arbeidsdag. Den innledende forfallsdatoen beregnes ved hjelp av kalenderdager. Hvis den beregnede datoen lander på en ikke-arbeidsdag, kan du justere den beregnede forfallsdatoen til enten neste arbeidsdato eller en tidligere arbeidsdag.
15. Klikk på **Lagre**.
16. Lukk siden.
17. Gå til **Kunder > Betalingsoppsett > Kontantrabatt**.
18. Klikk på **Ny**. Denne siden brukes til å definere hvordan kontantrabatten skal beregnes. 
19. Angi en ID i **Kontantrabatt**-feltet.
20. Angi en beskrivelse i **Beskrivelse**-feltet.
21. Hvis en trinnvis kontantrabatt er tilgjengelig, velger du **Neste rabattkode** som er relevant etter denne nye kontantrabatten.
22. I **Dager**-feltet angir du hvor mange dager som brukes til å beregne kontantrabattdatoen. Hvis **Netto**-prinsippet er valgt, legges antallet dager til fakturadatoen for å beregne kontantrabattdatoen.  
23. Angi prosenten av kontantrabatten i **Rabattprosent**-feltet.
24. I feltet **Hovedkonto for kunderabatter** angir du hovedkontoen som kontantrabatten skal posteres til for kundefakturaer.
25. Velg et alternativ i feltet **Motkontoer for rabatt**. Hvis du velger "Kontoer på fakturalinjene", posteres kontantrabatten til samme anleggsmiddel/utgiftshovedkontoen på linjene i leverandørfakturaen. Hvis du velger **Bruk hovedkontoen for leverandørfakturaer**, posteres kontantrabatten til hovedkontoen du definerer i **Hovedkonto for leverandørfakturaer**. I dette eksemplet velger du **Bruk hovedkontoen for leverandørfakturaer**. 
26. I feltet **Hovedkonto for leverandørrabatter** angir du hovedkontoen som kontantrabatten skal posteres til for kundefakturaer.
27. Klikk **Lagre**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

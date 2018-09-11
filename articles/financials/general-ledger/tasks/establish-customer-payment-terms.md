--- 
title: Opprette kundebetalingsbetingelser
description: Dette definerer et oppsett for kontantrabatt og forfallsdato.
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4e0e43962bea3ff1c3adafa73da4ce3862963a51
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="establish-customer-payment-terms"></a>Opprette kundebetalingsbetingelser

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette definerer et oppsett for kontantrabatt og forfallsdato. Denne oppgaveveiledningen bruker USMF demo firmaet.

1. Gå til Kunder > Betalingsoppsett > Betalingsdager.
    * Oppsettet for betalingsbetingelsene er delt for kunder og leverandører. Hvis du definerer det i modulen, vil det være tilgjengelig i den andre modulen også. For denne veiledningen har jeg definert alle betalingsbetingelsene under Kunder.  
2. Klikk Ny.
    * Opprett en betalingsdag hvis betalingsbetingelsene krever en bestemt dag i uken (mandag, tirsdag osv) eller en bestemt dato i måneden (5., 10. osv).  
3. I feltet Betalingsdag angir du en ID for betalingsdagen i feltet Betalingsdag.
4. I Beskrivelse-feltet angir du en beskrivelse av betalingsdagen.
5. I Uke/måned-feltet velger du enten Uke eller Måned.
    * Hvis du vil angi en dag i uken, for eksempel mandag, velger du Uke. Hvis du vil angi en dato i måneden, for eksempel den 10., velger du Måned. Velg Måned for dette eksemplet.  
6. Angi en dato i Dato-feltet.
    * Datoen må angis som et tall, for eksempel "10", og ikke som "10.".  
7. Klikk Lagre.
8. Lukk siden.
9. Gå til Kunder > Betalingsoppsett > Betalingsbetingelser.
10. Klikk Ny.
    * Betalingsbetingelsene brukes til å definere hvordan forfallsdatoene beregnes. Dato for oppsett av kontantrabatten er definert i en egen side.  
11. Angi en ID i feltet Betalingsbetingelser.
12. Angi en beskrivelse i Beskrivelse-feltet.
13. Velg en betalingsmåte, for eksempel Oppkrav, Netto, Gjeldende måned og så videre.
    * Betalingsmåten brukes til å definere starten på hvordan forfallsdatoene beregnes.  Netto brukes for eksempel hvis forfallsdatoen alltid er et angitt antall måneder eller dager etter fakturadato. Oppkrav kan brukes når betaling kreves ved faktura, slik at en forfallsdato ikke blir beregnet. Velg Gjeldende måned for denne oppgaveveiledningen.  
14. Velg en betalingsdag hvis en bestemt dag i uken eller dato skal tas med i beregningen.
    * Avhengig av betalingsbetingelsene, kan du angi et antall i måneder eller dager. Eller du bruke betalingsplanen eller betalingsdagen for å legge til på slutten av betalingsmåten. Hvis forfallsdatoen alltid skal være den 10. i neste måned, velger du en betalingsdag på den 10.  
15. Klikk Lagre.
16. Lukk siden.
17. Gå til Kunder > Betalingsoppsett > Kontantrabatt.
18. Klikk Ny.
    * Denne siden brukes til å definere hvordan kontantrabatten skal beregnes.  
19. Angi en ID i feltet Kontantrabatt i feltet Kontantrabatt.
20. Angi en beskrivelse i Beskrivelse-feltet.
21. Hvis en trinnvis kontantrabatt er tilgjengelig, velger du den neste rabattkoden som er relevant etter denne nye kontantrabatten.
22. Angi hvor mange dager som brukes til å beregne kontantrabattdatoen.
    * Hvis nettoprinsippet er valgt, legges antallet dager til fakturadatoen for å beregne kontantrabattdatoen.  
23. Angi prosenten for kontantrabatten.
24. Angi hovedkontoen som kontantrabatten skal posteres til for kundefakturaer.
25. Velg et alternativ i feltet Motkontoer for rabatt.
    * Hvis du velger "Kontoer på fakturalinjene", posteres kontantrabatten til samme anleggsmiddel/utgiftshovedkontoen på linjene i leverandørfakturaen. Hvis du velger "Bruk hovedkontoen for leverandørfakturaer", posteres kontantrabatten til hovedkontoen du definerer i "Hovedkonto for leverandørfakturaer". I dette eksemplet velger du "Bruk hovedkontoen for leverandørfakturaer".  
26. Angi hovedkontoen som kontantrabatten skal posteres til for leverandørfakturaer.
27. Klikk Lagre.



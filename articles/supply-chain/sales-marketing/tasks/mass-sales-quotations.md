--- 
title: Masseopprett salgstilbud
description: "Denne fremgangsmåten beskriver hvordan du effektivt oppretter tilbud som tilbyr et sett av produkter eller tjenester som skal sendes til flere kunder."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1fcb2c4d47f0c8e701be025e0554ed476693d732
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="mass-create-sales-quotations"></a>Masseopprett salgstilbud

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten beskriver hvordan du effektivt oppretter tilbud som tilbyr et sett av produkter eller tjenester som skal sendes til flere kunder. Denne massetilbudsopprettelsen er basert på tilbudsmaler. Du kan kjøre denne fremgangsmåten med dine egne data eller i demonstrasjonsdataselskapet USMF.


## <a name="create-a-quotation-template"></a>Opprette en tilbudsmal
1. Gå til Salg og markedsføring > Oppsett > Tilbud > Malgrupper.
2. Klikk Ny.
3. Skriv inn en ID som du velger, i Gruppe-ID-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk Lagre.
6. Lukk siden.
7. Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.
8. Klikk Ny.
9. Velg Kunde i feltet Kontotype.
10. Angi eller velg en verdi i Kundekonto-feltet.
11. Klikk OK.
    * Du må utføre trinnene for oppsettet i tilbudshodet for at et tilbud skal bli en mal. Dette må gjøres før du kan legge til linjer i tilbudet.   
12. Klikk Alternativer i handlingsruten.
13. Klikk Bytt visning.
14. Klikk Hodevisning.
15. Utvid Oppsett-delen.
16. Angi eller velg en verdi i feltet Gruppe-ID.
17. Angi en verdi i Malnavn-feltet.
18. Velg Ja i Aktiv-feltet.
    * Bare aktive maler kan brukes når du bruker en mal på et nytt salgstilbud.  
19. Klikk Alternativer i handlingsruten.
20. Klikk Bytt visning.
21. Klikk Linjevisning.
22. Angi eller velg en verdi i feltet Vare.
23. Skriv inn en verdi i feltet Vare.
24. Lukk siden.
25. Angi et tall i feltet Rabattprosent.
26. Klikk Legg til linje.
27. Angi eller velg en verdi i feltet Vare.
28. Skriv inn en verdi i feltet Vare.
29. Lukk siden.
30. I Enhetspris-feltet angir du en ny pris eller endrer den gjeldende.
31. Klikk Legg til linje.
32. Angi eller velg en verdi i feltet Vare.
33. Skriv inn en verdi i feltet Vare.
34. Lukk siden.
35. Angi et tall i feltet Antall.
36. Angi et tall i feltet Rabatt.
37. Klikk Lagre.

## <a name="apply-the-template-to-create-a-single-quotation"></a>Bruke malen for å opprette ett enkelt tilbud
1. Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.
    * Legg merke til at tilbudet du nettopp opprettet, merkes som mal.  
2. Klikk Ny.
3. Velg Kunde i feltet Kontotype.
4. Angi eller velg en verdi i Kundekonto-feltet.
5. Utvid delen Mal.
6. Angi eller velg en verdi i feltet Gruppe-ID.
7. Angi eller velg en verdi i Malnavn-feltet.
8. Velg Basert på malverdier i feltet Beregningsmåte.
9. Klikk OK.
    * Det nye tilbudet er nå opprettet, basert på data og vilkår for malen.  
10. Lukk siden.
11. Lukk siden.

## <a name="apply-the-template-to-mass-create-quotations"></a>Bruke malen for å masseopprette tilbud
1. Gå til Salg og markedsføring > Salgstilbud > Tilbudsoppdatering > Masseopprett tilbud.
2. Velg Kunde i feltet Kontotype.
3. Angi eller velg en verdi i feltet Gruppe-ID.
4. Angi eller velg en verdi i Malnavn-feltet.
5. Velg Basert på malverdier i feltet Beregningsmåte.
6. Utvid delen Poster som skal inkluderes.
7. Klikk Filter.
8. Angi filteret til å dekke et valgt område av kunder du vil ha med i denne opprettelsen av massetilbud i Kriterier-feltet. Bruk følgende format Kunde1..KundeN.
    * Du kan for eksempel sette filteret til: US-001..US-004  
9. Klikk OK.
10. Klikk OK.
11. Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.
    * Kontroller at tilbud er opprettet for alle kunder som er angitt i rutinen Masseoppdatering, basert på den valgte malen.  



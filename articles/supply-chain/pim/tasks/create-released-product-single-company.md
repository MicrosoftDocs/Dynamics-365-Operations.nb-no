--- 
title: Opprette et frigitt produkt for ett firma
description: "Denne prosedyren viser hvordan du oppretter ett enkelt frigitt produkt i konteksten for én enkelt juridisk enhet."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 042eafc29e377e0ad6fb8dc1499daf8eb105b7ed
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-released-product-for-a-single-company"></a>Opprette et frigitt produkt for ett firma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren viser hvordan du oppretter ett enkelt frigitt produkt i konteksten for én enkelt juridisk enhet. Når det frigitte produktet er opprettet, er det umiddelbart tilgjengelig bare i denne enheten. Du kan gå gjennom denne prosedyren i demonstrasjonsdataselskapet USMF. Denne oppgaven utføres vanligvis av en produktdesigner.


## <a name="create-a-released-product"></a>Opprett et frigitt produkt
1. Gå til Frigitte produkter.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Produktnummer.
    * Hvis et produktnummer ikke angis automatisk i feltet produkt, skriver du inn et unikt produktnummer. Dette trinnet er bare nødvendig hvis ingen nummerserie er definert for produktnumre.  
4. Skriv inn en verdi i feltet Produktnavn.
    * Produktnavnet hentes som standard til et søkenavn. Hvis du trenger, kan du velge for å endre søkenavnet.  
5. Klikk rullegardinknappen i feltet Varemodellgruppe for å åpne oppslaget.
    * Varemodellgrupper inneholder innstillinger som bestemmer hvordan varer styres og behandles ved varemottak og vareavganger. Innstillingene bestemmer også hvordan forbruk av varer skal beregnes.  
6. Finn og velg ønsket post i listen.
7. Klikk koblingen i den valgte raden i listen.
8. Klikk rullegardinknappen i feltet Varegruppe for å åpne oppslaget.
    * Varegrupper brukes til å styre lager ved å dele inn lagervarer i grupper basert på vareegenskaper. Hvis du fore eksempel vil styre hvordan informasjon er postert til hovedkontoer, kan du opprette en serie med forskjellige varegrupper som er knyttet til bestemte hovedkontoer. Dette gjør det mulig for deg å spore lagerverdien for varer på forskjellige stadier.  
9. Finn og velg ønsket post i listen.
10. Klikk koblingen i den valgte raden i listen.
11. Klikk rullegardinknappen i Lagringsdimensjonsgruppe-feltet for å åpne oppslaget.
    * Lagringsdimensjoner hjelper deg styre hvordan varer lagres og hentes fra lageret. En lagringsdimensjon kan for eksempel være Område og lager.  
12. Finn og velg ønsket post i listen.
13. Klikk koblingen i den valgte raden i listen.
14. Klikk rullegardinknappen i Sporingsdimensjonsgruppe-feltet for å åpne oppslaget.
    * Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner du kan legge til et produkt. Parti- eller serienummer brukes for eksempel til å spore varer på lager.  
15. Finn og velg ønsket post i listen.
16. Klikk koblingen i den valgte raden i listen.
17. Klikk rullegardinknappen i feltet Lagerenhet for å åpne oppslaget.
    * Lagerenheten bestemmer hvordan produktet er bestemmes mengdemessig når de lagres på lageret.  
18. Finn og velg ønsket post i listen.
19. Klikk koblingen i den valgte raden i listen.
20. Klikk rullegardinknappen i feltet Innkjøpsenhet for å åpne oppslaget.
    * Innkjøpsenheten bestemmer hvordan produktet er bestemmes mengdemessig når det er kjøpt fra en leverandør.  
21. Finn og velg ønsket post i listen.
22. Klikk koblingen i den valgte raden i listen.
23. Klikk rullegardinknappen i feltet Salgsenhet for å åpne oppslaget.
    * Salgsenheten bestemmer hvordan produktet er bestemmes mengdemessig når den selges til en kunde.  
24. Finn og velg ønsket post i listen.
25. Klikk koblingen i den valgte raden i listen.
26. Klikk rullegardinknappen i feltet Stykklisteenhet for å åpne oppslaget.
    * Stykklisteenheten bestemmer hvordan produktet er bestemmes mengdemessig når du bruker den i en stykkliste (BOM).  
27. Finn og velg ønsket post i listen.
28. Klikk koblingen i den valgte raden i listen.
29. Klikk rullegardinknappen i feltet Merverdiavgiftsgruppe for vare: for å åpne oppslaget.
    * Mva-gruppen for vare i Salgsavgift-gruppen bestemmer hvordan mva beregnes for hver vare.  
30. Finn og velg ønsket post i listen.
31. Klikk koblingen i den valgte raden i listen.
32. Klikk rullegardinknappen i feltet Merverdiavgiftsgruppe for vare: for å åpne oppslaget.
    * Mva-gruppen for vare i Kjøpsavgift-gruppen bestemmer hvordan innkjøpsavgift beregnes for hver vare.  
33. Finn og velg ønsket post i listen.
34. Klikk koblingen i den valgte raden i listen.
35. Klikk OK.

## <a name="add-product-characteristics"></a>Legg til produktegenskaper
1. Vis eller skjul delen Administrer lager.
2. Angi et tall i feltet Nettovekt.
3. Angi et tall i feltet Taravekt.
4. Angi et nummer i Bruttodybde-feltet.
5. Angi et nummer i Bruttobredde-feltet.
6. Angi et tall i Bruttohøyde-feltet.
7. Angi et tall i feltet Volum.

## <a name="add-financial-dimensions"></a>Legg til finansdimensjoner
1. Vis eller skjul delen Finansdimensjoner.
2. Klikk rullegardinknappen i feltet BusinessUnit for å åpne oppslaget.
3. Finn og velg ønsket post i listen.
4. Klikk koblingen i den valgte raden i listen.
5. Klikk rullegardinknappen i feltet CostCenter for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
7. Klikk koblingen i den valgte raden i listen.
8. Klikk rullegardinknappen i Avdeling-feltet for å åpne oppslaget.
9. Finn og velg ønsket post i listen.
10. Klikk koblingen i den valgte raden i listen.
11. Klikk rullegardinknappen i feltet ItemGroup for å åpne oppslaget.
12. Finn og velg ønsket post i listen.
13. Klikk koblingen i den valgte raden i listen.



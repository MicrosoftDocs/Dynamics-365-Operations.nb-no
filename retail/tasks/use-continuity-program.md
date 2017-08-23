--- 
title: " Bruke et kontinuitetsprogram"
description: "Denne fremgangsmåten hjelper med å selge et kontinuitetsprogram og behandle tilknyttede salgsordrer."
author: scott-tucker
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: bd584bbb49ea83c4debf11ad0169c346ef0f9637
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="use-a-continuity-program"></a> Bruke et kontinuitetsprogram

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne fremgangsmåten hjelper med å selge et kontinuitetsprogram og behandle tilknyttede salgsordrer. For å fullføre denne prosedyren, må brukeren være definert som telefonsenterbruker. Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.

1. Gå til Detaljhandel og handel > Kunder > Kundestøtte.
2. I Søketekst-feltet skriver du inn Karin og trykker deretter Tab-tasten.
    * Avansert søk-dialogboksen skal vises. Hvis ikke, klikker du Søk til høyre for dette feltet.  
3. Merk den valgte raden i listen.
    * Det skal bare være én rad som vises med Karen Berg. Merk raden ved å klikke på avmerkingskolonnen helt til venstre i rutenettet.  
4. Klikk Velg.
5. Klikk Ny salgsordre.
    * Det er lurt å notere seg salgsordrenummeret. Du vil trenge det senere i prosedyren.  
6. I Varenummer-feltet skriver du inn 88000 og trykker deretter Tab-tasten.
    * Dette er en kontinuitetsvare i demonstrasjonsdataene for USRT.  
7. Klikk Fullført.
8. Angi Visa i Betalingsmetode-feltet.
9. Klikk Legg til kredittkort.
    * Angi den nødvendige kredittkortinformasjonen på denne siden.  
10. Klikk OK.
11. Vid delen Betaling.
    * Hvis du vil sende en telefonsenterordre, må betalinger angis for ordren.  
12. Klikk OK.
13. Klikk Send.
    * Du er ferdig med å opprette en ny kontinuitetsordre. Nå skal du kjøre to satsvise prosesser som brukes til å behandle kontinuitetsordrene.  
14. Lukk siden.
15. Gå til Detaljhandel og handel > Kontinuitet > Behandle kontinuitetsbetalinger.
16. I Kontinuitetsvare-feltet skriver du inn 88000 og trykker deretter Tab-tasten.
17. Klikk OK.
18. Gå til Detaljhandel og handel > Kontinuitet > Opprett underordnede kontinuitetsordrer.
    * Denne prosessen oppretter nye salgsordrer basert på innstillingene for kontinuitetsprogrammene dine.  
19. I Kontinuitetsvare-feltet skriver du inn 88000 og trykker deretter Tab-tasten.
    * Vare 88000 er en kontinuitetsvare i demonstrasjonsdataene for USRT.  
20. Angi eller velg en verdi i feltet Salgsordre.
    * Angi salgsordrenummeret du noterte deg tidligere i denne fremgangsmåten. Dette vil holde behandlingstiden nede på et minimum for denne prosedyren. Salgsordre-feltet er valgfritt – du kan behandle alle ordrer for et hvilken som helst program.  
21. Klikk OK.


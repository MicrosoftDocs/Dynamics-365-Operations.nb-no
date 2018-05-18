--- 
title: "Konfigurere bølgebehandling"
description: "Denne veiledningen beskriver hvordan du definerer vilkår som bestemmer hvilket arbeid som genereres for et lager når en bølge behandles, og om bølger behandles manuelt eller automatisk."
author: YuyuScheller
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f7a6db585468c235e07c4a0117a83995ec93f4b0
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="configure-wave-processing"></a>Konfigurere bølgebehandling

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne veiledningen beskriver hvordan du definerer vilkår som bestemmer hvilket arbeid som genereres for et lager når en bølge behandles, og om bølger behandles manuelt eller automatisk. Du angir vilkårene ved å definere bølgemaler og spørringer som samsvarer med en bølge med frigitte linjer i bestillinger, produksjonsordrer eller Kanban-ordrer. Bølgebehandling brukes i lagre som bruker funksjonaliteten i lagerstyringsmodulen, og ikke de som bruker funksjonaliteten i lagerstyringsmodulen. Du kan kjøre denne prosedyren i demonstrasjonsdataselskapet USMF.

1. Gå til Lagerstyring > Oppsett > Bølger > Bølgemaler.
2. Klikk Ny.
3. Angi en verdi i feltet Navn på bølgemal.
    * Når du definerer en bølgemal, kan du angi rekkefølgen for hvordan malene samsvares med frigitte linjene i salgsordrer, produksjonsordrer eller Kanbaner. Når en linje er frigitt til lageret eller til produksjon, brukes den første bølgemalen som den oppfyller kriteriene for. Vi anbefaler at du flytter malene med de mest spesifikke kriteriene øverst i listen. Jo bredere kriterier, desto mer sannsynlig er det at en linje oppfyller kriteriene, og dette kan føre til at linjer tilordnes til feil bølge.  
4. Skriv inn en verdi i feltet Beskrivelse av bølgemal.
5. Angi eller velg en verdi i Område-feltet.
    * Hvis du bruker USMF, kan du velge område 2.  
6. Angi eller velg en verdi i feltet Lager.
    * Hvis du bruker USMF, kan du velge lager 24.  
7. Sett feltet Automatisk oppretting av bølge til Ja.
    * Velg dette alternativet for å opprette en bølge automatisk når en salgsordre, produksjonsordre eller kanban frigis til lageret.  
8. Sett alternativet Behandle bølge ved frigivelse til lager til Ja. 
    * Velg dette alternativet for å behandle bølgen og opprette arbeid automatisk når en linje frigis til lageret.  
9. Sett alternativet Frigi bølge automatisk til Ja. 
    * Velg dette alternativet for å frigi bølgen automatisk. Plukkarbeidet opprettes og gjøres tilgjengelig på mobilenheter.  
10. Angi alternativet Tilordne til åpne bølger til Ja. 
    * Linjer tilordnes bølger basert på spørringsfilteret for bølgemalen.  
11. Sett alternativet Behandle bølge automatisk ved terskel til Ja. 
    * Velg dette alternativet for å behandle bølgen automatisk når verdiene når tersklene for vekt, forsendelse og linjer som er angitt i Bølgeterskler-feltgruppen. Dette alternativet er bare tilgjengelig hvis Forsendelse er valgt i Bølgemaltype-feltet.  
12. Sett alternativet Automatiser frigivelse av etterfyllingsarbeid til Ja. 
    * Velg dette alternativet for å opprette behovsbasert etterfyllingarbeid og frigi det automatisk. Du må legge til etterfyllingsbølgemetoden i bølgemalen og opprette en mal for etterfylling av typen Bølgebehov.  
13. Vis delen Metoder.
    * Bølgemalmetodene lar deg kontrollere rekkefølgen for aktiviteter som hver bølgen går gjennom når den behandles. Du kan for eksempel ha en metode for etterfylling for bølge. Når du legger til en metode, vises den automatisk på riktig sted i trinnrekkefølgen. Hvis du har angitt Ja for alternativet Automatiser frigivelse av etterfyllingsarbeid, må du legge til etterfyllingsmetoden her.  
    * Bølgeattributter fungerer som filtre for å begrense hva slags varer som kan bruke bølgen. Du kan for eksempel angir en varegruppe.  
14. Klikk Lagre.
15. Lukk siden.
16. Gå til Lagerstyring > Oppsett > Lagerstyringsparametere.
17. Vis delen Bølgebehandling.
18. Angi eller velg en verdi i feltet Satsvis gruppe for bølgebehandling.
19. Sett alternativet Behandle bølger satsvis til Ja.
20. Angi et tall i feltet Vent på lås (ms).
    * Angi tiden, i millisekunder, som et tildelingstrinn skal vente på en systemressurs som er låst av et annet tildelingstrinn. Når denne tiden overskrides, behandles ikke på bølgen, og det vises en feilmelding.  
21. Klikk Lagre.
22. Lukk siden.
23. Gå til Produksjonskontroll > Oppsett > Parametere for produksjonskontroll.
24. Velg et alternativ i feltet Frigi til lager.
    * Når det gjelder salgsordrer og Kanban-bestillinger, må beholdning reserveres før ordren frigis til lageret. Hvis ikke, varer eller tildelingslinjer kan ikke behandles i en Bølge. For produksjonsordrer kan du også velge Tillat delvis reservasjon. Dette er for eksempel nyttig hvis du har materialene du trenger for å starte produksjon, og du kan deretter vente til tilleggsmaterialene bli tilgjengelige for å fullføre prosessen. Hvis du velger dette alternativet, må du gjenta prosessen med frigivelse til lager manuelt når tilleggsmaterialene flere blir tilgjengelige.  
25. Lukk siden.



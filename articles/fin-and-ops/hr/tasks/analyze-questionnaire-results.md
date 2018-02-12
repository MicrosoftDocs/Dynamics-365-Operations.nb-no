--- 
title: "Analysere resultater av spørreskjema"
description: "Spørreskjemastatistikk kan brukes til å beregne gjennomsnitt, totaler og prosenter basert på et sett med demografiske data."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c243a84b63215ab44e2929c64dbc4aced7061474
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="analyze-questionnaire-results"></a>Analysere resultater av spørreskjema

[!include[task guide banner](../../includes/task-guide-banner.md)]

Spørreskjemastatistikk kan brukes til å beregne gjennomsnitt, totaler og prosenter basert på et sett med demografiske data. Hvis du vil gjør dette, kan du gå til Spørreskjema > Vis og analyser resultater > Spørreskjemastatistikk. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-a-questionnaire-statistics-record"></a>Opprette en post for spørreskjemastatistikk
1. Gå til Spørreskjemastatisitikk.
2. Klikk Ny.
3. Merk den valgte raden i listen.
4. Skriv inn en verdi i Statistikk-feltet.
5. Skriv inn en verdi i Beskrivelse-feltet.
6. Klikk rullegardinknappen i Spørreskjema-feltet for å åpne oppslaget.
7. Klikk koblingen i den valgte raden i listen.
8. Klikk kategorien Generelt.
    * Velg om du vil ta med anonyme resultater eller resultater fra ansatte, kontaktpersoner og søkere.  
9. Merk av eller fjern merket i avmerkingsboksen Arbeider.
    * Hvis du vil vise resultatene etter ansiennitet eller alder, angir du intervallene du vil bruke til å gruppere resultatene.  
    * Hvis du angir 5 for alderintervallet, grupperes resultatene etter fem års alderintervaller.  
10. Angi et tall i Alder-feltet.
    * Velg om du vil kjøre beregningen mot hele spørreskjemaet, for hver resultatgruppe, for hvert spørsmål eller for hver spørsmålsrad.  
    * Velg hvordan du vil gruppere resultatene.  
    * Hvis du for eksempel beregner gjennomsnittlige poeng per spørsmål, vil du kanskje se spørsmålene gruppert etter resultatgruppe.  
    * Velg dataene som skal basere beregningen på.  
    * Hvis du for eksempel vil vise gjennomsnittlig prosent mottatt på spørreskjemaet på tvers av ansatte kontra gjennomsnittlig antall poeng som er oppnådd på tvers av ansatte.  
11. Klikk kategorien Område.
    * Bruk områder til å begrense resultatsettet til bare de som oppfyller områdekriteriene.  
12. Klikk kategorien Gruppering av.
    * Bruk Grupperinger til å bestemme hvordan resultatene skal vises.  
    * Du kan for eksempel gruppere resultatene først etter kjønn, deretter etter alder.  
13. Finn og velg ønsket post i listen.
    * Flytt grupperingene til Valgt-siden og plasser dem i ønsket rekkefølge.  

## <a name="execute-the-statistics-calculation"></a>Utføre statistikkberegningen
1. Klikk Utfør.
    * Velg hvilken beregningsfunksjon du vil utføre på resultatene.  
    * Du kan for eksempel beregne gjennomsnittsprosentene på tvers av spørreskjemaet for de valgte grupperingene eller summere punktene på tvers av resultatgruppene for de valgte grupperingene.  
2. Merk av for eller fjern merkingen i avmerkingsboksen Slett tidligere søk.
3. Klikk OK.

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a>Vis resultatene av spørreskjemastatistikken.
1. Klikk Resultat.
2. Klikk Resultat.
3. Lukk siden.



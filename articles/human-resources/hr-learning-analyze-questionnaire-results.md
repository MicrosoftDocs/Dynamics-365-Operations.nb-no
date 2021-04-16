---
title: Analysere resultat av spørreskjema
description: Spørreskjemastatistikk kan brukes til å beregne gjennomsnitt, totaler og prosenter basert på et sett med demografiske data.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c7f6767b900ede0112e972149c271d53c36296f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794763"
---
# <a name="analyzing-questionnaire-results"></a>Analysere resultat av spørreskjema

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
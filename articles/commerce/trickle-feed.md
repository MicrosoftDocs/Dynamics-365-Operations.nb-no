---
title: Fordel feedbasert ordreoppretting for detaljhandelstransaksjoner
description: Dette emnet beskriver den fordelte, feedbaserte ordreopprettingen for butikktransaksjoner i Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 12/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3a7fd8698d7123403cf9092a4a4bf810595d795b
ms.sourcegitcommit: f82372b1e9bf67d055fd265b68ee6d0d2f10d533
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/14/2021
ms.locfileid: "7921251"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Fordel feedbasert ordreoppretting for detaljhandelstransaksjoner

[!include [banner](includes/banner.md)]

I Microsoft Dynamics 365 Commerce, versjon 10.0.5 og nyere anbefaler vi at du går over alle utdragsposteringsprosesser til prosessene for å fordele feedbasert utdragspostering. Betydelige ytelses- og forretningsfordeler knyttes til bruk av funksjonen for fordelingsfeed. Salgstransaksjoner behandles gjennom hele dagen. Transaksjoner for betalingsmiddel og kontantstyring behandles i regnskapsoppgjøret på slutten av dagen. Funksjonalitet for fordelingsfeed gjør det mulig å behandle salgsordrer, fakturaer og betalinger fortløpende. Derfor kan beholdning, inntekt og betalinger oppdateres og gjenkjennes med minimal forsinkelse.

## <a name="use-trickle-feed-based-posting"></a>Bruk postering basert på fordelingsfeed

> [!IMPORTANT]
> Før du aktiverer postering basert på fordelingsfeed, må du sørge for at det ikke finnes beregnede og uposterte utdrag. Poster alle utdrag før du aktiverer funksjonen. Du kan se etter åpne utdrag i arbeidsområdet **Finans for handelsbutikk**.

Hvis du vil aktivere postering basert på fordelingsfeed av detaljhandelstransaksjoner, aktiverer du funksjonen **Detaljhandelsoppgaver – fordelingsfeed** ved hjelp av arbeidsområdet **Funksjonsbehandling**. Utdrag blir delt inn i to typer: transaksjonsutdrag og regnskapsoppgjør.

### <a name="transactional-statements"></a>Transaksjonsutdrag

Behandling av transaksjonsutdrag er beregnet på å kjøres med høy frekvens, slik at dokumenter opprettes når transaksjonene lastes opp til Commerce Headquarters. Transaksjoner lastes fra butikkene til Commerce Headquarters når du kjører **P-jobben**. Du må også kjøre jobben **Valider butikktransaksjoner** for å validere transaksjoner slik at transaksjonsutdraget plukker dem opp.

Planlegg følgende jobber for å kjøre med høy frekvens:

- Hvis du vil beregne et transaksjonsutdrag, kjører du jobben **Beregn transaksjonsutdrag satsvis** (**Retail og Commerce \> IT for Retail og Commerce \> Salgsstedspostering \> Beregn transaksjonsutdrag satsvis**). Denne jobben plukker opp alle uposterte og validerte transaksjoner og legger dem til i et nytt transaksjonsutdrag.
- Hvis du vil postere transaksjonsutdrag satsvis, kjører du jobben **Poster transaksjonsutdrag satsvis** (**Retail og Commerce \> IT for Retail og Commerce \> Salgsstedspostering \> Poster transaksjonsutdrag satsvis**). Denne jobben kjører posteringsprosessen og oppretter salgsordrer, salgsfakturaer, betalingsjournaler, rabattjournaler og inntekt-/utgiftstransaksjoner for uposterte utdrag som ikke inneholder noen feil. 

### <a name="financial-statements"></a>Regnskapsoppgjør

Behandling av regnskapsoppgjør er ment å være en dagsoppgjørsprosess. Denne typen utdragsbehandling støtter bare **Skift**-lukkingsmetoden og plukker bare opp lukkede skift. Utdrag er begrenset til økonomisk avstemming. De oppretter bare journaler for de ulike beholdningsbeløpene mellom telt beløp og transaksjonsbeløp for betalingsmidlene og journaler for andre kontantstyringstransaksjoner.

Planlegg start- og sluttidspunktene for følgende regnskapsoppgjørsjobber basert på forventet dagsoppgjør:

- Hvis du vil beregne et regnskapsoppgjør, kjører du jobben **Beregn regnskapsoppgjør satsvis** (**Retail og Commerce \> IT for Retail og Commerce \> Salgsstedspostering \> Beregn regnskapsoppgjør satsvis**). Denne jobben samler alle uposterte økonomiske transaksjoner og legger dem til i et nytt regnskapsoppgjør.
- Hvis du vil postere regnskapsoppgjør satsvis, kjører du jobben **Poster regnskapsoppgjør satsvis** (**Retail og Commerce \> IT for Retail og Commerce \> Salgsstedspostering \> Poster regnskapsoppgjør satsvis**).

### <a name="manually-create-statements"></a>Opprett kontoutdrag manuelt

Du kan også opprette typer transaksjons- og regnskapsoppgjør manuelt. 

1. Gå til **Retail og Commerce \> Kanaler \> Butikker** og velg **Utdrag**. 
2. Velg **Nytt** og velg deretter utdragstypen du vil opprette. Felter på siden **Utdrag** viser data som er relevante for den valgte utdragstypen, og handlinger under **Utdragsgruppe** viser relevante handlinger.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Når skal et data mart tilbakestilles
description: Dette emnet viser en oversikt over forhold som kan forbedres ved å tilbakestille et data mart, og forhold der det er usannsynlig at tilbakestilling av data mart hjelper.
author: jinniew
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c88994a336528650bf8ab6e239c873fa6cd36c46
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754150"
---
# <a name="when-to-reset-a-data-mart"></a>Når skal et data mart tilbakestilles

Det kan være tidkrevende å tilbakestille et data mart. Denne handlingen er kanskje ikke løsningen som trengs, avhengig av forholdene. Dette emnet viser en oversikt over forhold som kan forbedres ved å tilbakestille et data mart, og forhold der det er usannsynlig at tilbakestilling av data mart hjelper.  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a>Når må du tilbakestille et data mart?
Vurder følgende spørsmål før du tilbakestiller et data mart. Hvis du svarer ja på ett eller flere spørsmål, kan det bety at organisasjonen kan dra nytte av å tilbakestille data mart.

- Programdatabasen ble gjenopprettet, men data mart-databasen ble ikke gjenopprettet.
- Du ser uriktige data for en regnskapsperiode, som ikke er resultatet av et problem med rapportutformingen.
- Du ser uriktige data for en regnskapsperiode, og postene vises under Integreringsforsøk på siden **Integreringsstatus** i Rapportutforming (start Rapportutforming og velg **Verktøy > Integreringsstatus**).
- Du har åpnet en støttehendelse, og en kundestøttetekniker har bedt deg om å tilbakestille data mart som en del av et feilsøkingstrinn.
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a>Når passer det ikke å tilbakestille et data mart?
Det finnes visse omstendigheter der vi anbefaler at du ikke tilbakestiller et data mart. Disse omfatter følgende. 

- Hver gang årsaken ikke er oppført i dette emnet.
- Du har ytelsesproblemer som er knyttet til en datasynkronisering. I slike omstendigheter hjelper det sannsynligvis ikke å tilbakestille data mart.
- Hvis du har et gjentakende tilbakestillingsmønster av en av følgende årsaker: 
  - **Manglende data** – Først eliminerer du for eksempel problemer med rapportutforming og tidsberegning av synkronisering som du ser at faktatilordningen ikke har kjørt siden manglende data ble postert.
  - **Fastlåst integreringstilstand** – Hvis integreringen går tregt eller ser ut til å ha låst seg, kan du sannsynligvis ikke løse problemet ved å tilbakestille data mart.
  - **Forsøk på å tilbakestille har vært mislykket** – Hvis det er gjort en rekke forsøk på å fullføre en tilbakestilling, og alle forsøkene mislyktes på grunn av manglende data, anbefaler vi at du åpner en støttehendelse og arbeider med en kundestøttetekniker for å analysere situasjonen, før du prøver å tilbakestille data mart på nytt.
  - **Foreldede poster** – Foreldede poster alene gir ikke nødvendigvis en god grunn til å tilbakestille data mart. Hvis du har et stort datasett, tar det litt tid å kjøre tilbakestillingsprosessen, men den fører sannsynligvis ikke til forbedringer.
 
## <a name="what-a-data-mart-reset-does-not-do"></a>Hva en tilbakestilling av data mart ikke gjør  
- En tilbakestilling starter bare når eksisterende oppgaver er fullført. Dette sikrer at gamle data ikke settes inn. På dette tidspunktet kan du for eksempel få meldingen «Tilbakestillingen av data mart kan ikke behandles på grunn av en aktiv oppgave. Prøv på nytt senere.»
- Tilbakestillingen deaktiverer integreringsoppgavene og sletter alle data mart-data. Integreringen aktiveres på nytt.

> [!NOTE]
> Følgende punkter angir to ting som tilbakestilling av et data mart *ikke* gjør. <br>
> - Tilbakestillinger fjerner ikke rapportutforminger. <br>
> - Tilbakestillinger fjerner ikke firmadata eller brukerdata med mindre dette velges.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
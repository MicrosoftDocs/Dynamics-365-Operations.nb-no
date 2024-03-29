---
title: Kjør og Overvåk et eksperiment
description: Denne artikkelen beskriver hvordan du kjører og overvåker et eksperiment i en tredjepartstjeneste. Det beskriver også hvordan du endrer variasjoner etter at eksperimentet er startet.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c9f62c97b46fa00791de52b2804dad5edde7f625
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909589"
---
# <a name="run-and-monitor-an-experiment"></a>Kjør og Overvåk et eksperiment

Denne artikkelen beskriver hvordan du kjører og overvåker eksperimentet i en tredjepartsapp, og om nødvendig endre variasjoner. Før du fullfører trinnene i denne artikkelen, må du først [publisere](experimentation-preview-publish.md) eksperimentet i Commerce. 

Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce. Flere trinn er beskrevet i separate artikler.

[ ![Brukerreise for eksperimentering – kjøre og overvåke.](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)

Når du har publisert variasjonene, fullføres alle trinnene du må gjøre i Commerce for å kjøre eksperimentet. Neste trinn avgjør hvilken variasjon som skal vises for hver bruker når de ber om en side. Tredjepartstjenesten avgjør dette, men først må du aktivere eksperimentet i tjenesten. Siden trinnene for aktivering av et eksperiment varierer fra tjeneste til tjeneste, må du følge instruksjonene som er inkludert i tjenesten eller fra leverandøren. Hvis eksperimentet ikke er aktivert, vil brukere bare se standardversjonen av siden (ingen variasjoner vil bli vist).

Du må kjøre eksperimentet lenge nok til å samle inn data for statistisk gyldige resultater. Bruk tredjepartstjenesten til å overvåke eksperimentrelaterte data og analyser mens eksperimentet kjører.

## <a name="adjust-your-variations"></a>Justere variasjonene
Hvis du av en eller annen grunn må endre variasjonene, følger du fremgangsmåten nedenfor.

> [!IMPORTANT]
> Hvis du utfører endringer i et liveeksperiment i Commerce eller en tredjepartstjeneste, kan resultatene bli betydelig påvirket. Vurder å la eksperimentet kjøre ferdig og deretter opprette et nytt eksperimenter for store endringer.

1. Velg **Eksperimenter** i den venstre navigasjonsruten i Commerce-områdebyggeren, og velg deretter eksperimentet. 
1. Velg variasjonen du vil oppdatere fra rullegardinmenyen.
1. Utfør nødvendige endringer, og forhåndsvis og publiser deretter variasjonene. Hvis du vil ha mer informasjon, kan du se [Forhåndsvise og publisere et eksperiment](experimentation-preview-publish.md).
1. Gå til tredjepartstjenesten for å gjøre endringer som er knyttet til eksperimentoppsettet.
    
## <a name="previous-step"></a>Forrige trinn
[Forhåndsvise og publisere et eksperiment](experimentation-preview-publish.md)

## <a name="next-step"></a>Neste trinn
[Fremme en variasjon og fullføre et eksperiment](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
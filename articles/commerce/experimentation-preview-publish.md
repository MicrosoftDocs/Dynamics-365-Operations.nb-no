---
title: Forhåndsvise og publisere et eksperiment
description: Denne artikkelen beskriver hvordan du forhåndsviser og publiserer et eksperiment fra Dynamics 365 Commerce.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 5da7a4e3c17057278d02ebd45702d1de404f0dc6
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946148"
---
# <a name="preview-and-publish-an-experiment"></a>Forhåndsvise og publisere et eksperiment

Denne artikkelen beskriver hvordan du forhåndsviser og publiserer eksperimentet i Dynamics 365 Commerce etter at du har [koblet til eksperimentet og redigert variasjonene](experimentation-connect-edit.md). Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce. Flere trinn er beskrevet i separate artikler.

[ ![Brukerreise for eksperimentering – forhåndsvise og publisere.](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>Forhåndsvise eksperimentvariasjonene
Du kan forhåndsvise variasjonene og fortsette å redigere dem til de ser ut slik du ønsker.

Følg denne fremgangsmåten for å forhåndsvise eksperimentvariasjonene i Commerce-områdebyggeren.

1. Fra rullegardinmenyen for variasjoner nedenfor kommandolinjen velger du innholdet du vil forhåndsvise. 
1. På kommandolinjen velger du **Forhåndsvis**. En forhåndsvisning av hvordan innholdet vil se ut når det publiseres.
1. Hvis du vil forhåndsvise en annen variasjon, velger du den fra rullegardinlisten for variasjon og velger **Forhåndsvisning** på nytt.

## <a name="publish-your-experiment"></a>Publisere eksperimentet
Hvis du ikke bruker en publiseringsgruppe til å planlegge når eksperimentet er aktivt og du vil publisere umiddelbart, velger du **Publiser** på kommandolinjen. Alle variasjoner som hører til eksperimentet, blir publisert.
    
> [!IMPORTANT]
> Hvis siden ikke har en publisert URL-adresse, må du først publisere URL-adressen eller den vil ikke være synlig for brukerne av nettstedet. Hvis du vil ha mer informasjon, kan du se [Lagre, forhåndsvise og publisere en side](save-preview-publish-page.md).
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>Bruke publiseringsgrupper til å planlegge når eksperimentet aktiveres
Varianter som er opprettet i områdebygger, kan planlegges for publisering ved hjelp av en publiseringsgruppe. I en publiseringsgruppe kan du koble en side eller et fragment til eksperimentet ved å velge **Eksperimenter** i den venstre navigasjonsruten. Du kan også gjøre dette ved å velge **Sider** eller **Fragmenter** og følge instruksjonene i [Koble til et eksperiment og redigere variasjoner](experimentation-connect-edit.md). Hvis du vil ha informasjon om publiseringsgrupper, kan du se [Arbeide med publiseringsgrupper](publish-groups.md).

Når du bruker publiseringsgrupper med eksperimenter, er det noen viktige hensyn du må være oppmerksom på.
- Når du legger til en side eller et fragment som kjører på den i en publiseringsgruppe, blir eksperimentet fjernet fra siden eller fragmentet i publiseringsgruppen.
- Eksperimenter som er koblet til sider på et aktivt område, er ikke tilgjengelige for sider i publiseringsgrupper og omvendt. Sider der eksperimenter kjører på dem i et aktivt område, er på samme måte ikke tilgjengelige for andre eksperimenter i publiseringsgrupper og omvendt.
- Når du publiserer eller planlegger en publiseringsgruppe, blir alt innholdet i publiseringsgruppen publisert, uansett om det finnes et eksperiment som er knyttet til publiseringsgruppen.
- Fordi en publiseringsgruppe beholdes etter at den er publisert på et aktivt område, vil eksperimenter i publiseringsgruppen også beholdes. Derfor kan du ikke knytte andre eksperimenter til samme side eller fragment. Du kan unngå denne begrensningen ved å slette alle publiseringsgrupper med eksperimenter som beholdes. Hvis du vil slette et eksperiment i et aktivt område som også finnes i en publiseringsgruppe, må du først slette det fra publiseringsgruppen.

### <a name="force-variations-for-testing"></a>Tving variasjoner for testing

Når eksperimentet er utført, kan du legge til forsøks-ID-en og variasjons-ID-en på standardsiden for å tvinge frem en variant for testing eller automatisering. Hvis for eksempel URL-adressen til standardsiden er `https://fabrikam.com/modern/homepage`, kan du tvinge frem en variant med en URL-adresse som denne: `https://fabrikam.com/modern/homepage?exp=18012910471|18024360464`. Du kan få eksperiment-ID-en og variasjons-ID-en for eksperimentvariasjonen din fra den forhåndsviste URL-adressen i **Forhåndsvis**-opplevelsen, som er forklart ovenfor.

## <a name="previous-step"></a>Forrige trinn
[Koble til og redigere et eksperiment](experimentation-connect-edit.md)

## <a name="next-step"></a>Neste trinn
[Kjøre og overvåke et eksperiment](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

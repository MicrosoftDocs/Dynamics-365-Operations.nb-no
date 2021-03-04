---
title: Forhåndsvise og publisere et eksperiment
description: Dette emnet beskriver hvordan du forhåndsviser og publiserer et eksperiment fra Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: f1a565917ab7a048d4d455bc0a0fbd9316237aeb
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/22/2020
ms.locfileid: "4414782"
---
# <a name="preview-and-publish-an-experiment"></a>Forhåndsvise og publisere et eksperiment

Dette emnet beskriver hvordan du forhåndsviser og publiserer eksperimentet i Dynamics 365 Commerce etter at du har [koblet til eksperimentet og redigert variasjonene](experimentation-connect-edit.md). Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce. Flere trinn er beskrevet i separate emner.

[ ![Brukerreise for eksperimentering – forhåndsvise og publisere](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

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

## <a name="previous-step"></a>Forrige trinn
[Koble til og redigere et eksperiment](experimentation-connect-edit.md)

## <a name="next-step"></a>Neste trinn
[Kjør og Overvåk et eksperiment](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
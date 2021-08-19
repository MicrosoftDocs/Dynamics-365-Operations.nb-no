---
title: Eksempel på konfigurering av bølgebehandling
description: Dette emnet gir et eksempel på hvordan du definerer vilkår som bestemmer hvilket arbeid som genereres for et lager når en bølge behandles, og om bølger behandles manuelt eller automatisk.
author: Mirzaab
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d462427b85e12a45058a2fdea7901a83d9e85e5a562376dd438c69dec1ee8948
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769377"
---
# <a name="configure-wave-processing-example"></a>Eksempel på konfigurering av bølgebehandling

[!include [banner](../../includes/banner.md)]

Dette emnet gir et eksempel på hvordan du definerer vilkår som bestemmer hvilket arbeid som genereres for et lager når en bølge behandles, og om bølger behandles manuelt eller automatisk. Du angir vilkårene ved å definere bølgemaler og spørringer som samsvarer med en bølge med frigitte linjer i bestillinger, produksjonsordrer eller Kanban-ordrer.

## <a name="enable-sample-data"></a>Aktivere eksempeldata

For å arbeide deg gjennom dette scenariet ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du bruke et system der standard demodata er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

## <a name="example-scenario-configure-wave-processing"></a>Eksempelscenario: konfigurering av bølgebehandling

Dette eksempelscenariet går gjennom mange av de forskjellige innstillingene som påvirker hvordan bølger opprettes, fylles ut, behandles og frigis.

1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Bølger > Bølgemaler**.
1. Velg **Ny**.
1. Angi en verdi i feltet **Navn på bølgemal**. Når du definerer en bølgemal, kan du angi rekkefølgen for hvordan malene samsvares med frigitte linjene i salgsordrer, produksjonsordrer eller Kanbaner. Når en linje er frigitt til lageret eller til produksjon, brukes den første bølgemalen som den oppfyller kriteriene for. Det anbefales at du flytter malene med de mest spesifikke kriteriene øverst i listen. Jo bredere kriterier, desto mer sannsynlig er det at en linje oppfyller kriteriene, og dette kan føre til at linjer tilordnes til feil bølge.  
1. Skriv inn en verdi i feltet **Beskrivelse av bølgemal**.
1. Angi eller velg en verdi i **Område**-feltet. Hvis du bruker USMF, kan du velge område 2.  
1. Angi eller velg en verdi i feltet **Lager**. Hvis du bruker USMF, kan du velge lager 24.  
1. Sett feltet **Automatisk oppretting av bølge** til **Ja**. Velg dette alternativet for å opprette en bølge automatisk når en salgsordre, produksjonsordre eller kanban frigis til lageret.  
1. Sett alternativet **Behandle bølge ved frigivelse til lager** til **Ja**. Velg dette alternativet for å behandle bølgen og opprette arbeid automatisk når en linje frigis til lageret.  
1. Sett alternativet **Frigi bølge automatisk** til **Ja**. Velg dette alternativet for å frigi bølgen automatisk. Plukkarbeidet opprettes og gjøres tilgjengelig på mobilenheter.  
1. Angi alternativet **Tilordne til åpne bølger** til **Ja**. Linjer tilordnes bølger basert på spørringsfilteret for bølgemalen.  
1. Sett alternativet **Behandle bølge automatisk ved terskel** til **Ja**. Velg dette alternativet for å behandle bølgen automatisk når verdiene når tersklene for vekt, forsendelse og linjer som er angitt i **Bølgeterskler**-feltgruppen. Dette alternativet er bare tilgjengelig hvis **Forsendelse** er valgt i **Bølgemaltype**-feltet.  
1. Sett alternativet **Automatiser frigivelse av etterfyllingsarbeid** til **Ja**. Velg dette alternativet for å opprette behovsbasert etterfyllingarbeid og frigi det automatisk. Du må legge til etterfyllingsbølgemetoden i bølgemalen og opprette en mal for etterfylling ved å bruke typen **Bølgebehov**.  
1. Bruk innstillinger i den arkiverte gruppen **Standardverdier** for å tilordne bølgeattributter. Bølgeattributter fungerer som filtre for å begrense hva slags varer som kan bruke bølgen. Du kan for eksempel angir en varegruppe.  
1. Utvid **Metoder**-delen og angi handlingene som utføres av bølgemalen. Bølgemalmetodene lar deg kontrollere rekkefølgen for aktiviteter som hver bølge går gjennom når den behandles. Du kan for eksempel ha en metode for etterfylling for bølge. Når du legger til en metode, vises den automatisk på riktig sted i trinnrekkefølgen. Hvis du har angitt **Ja** for alternativet **Automatiser frigivelse av etterfyllingsarbeid**, må du legge til etterfyllingsmetoden her.  
1. Velg **Lagre**.
1. Lukk siden.
1. Gå til **Lagerstyring > Oppsett > Lagerstyringsparametere**.
1. Vis delen **Bølgebehandling**.
1. Angi eller velg en verdi i feltet **Satsvis gruppe for bølgebehandling**.
1. Sett alternativet **Behandle bølger satsvis** til **Ja**.
1. Angi et tall i feltet **Vent på lås (ms)**. Angi tiden, i millisekunder, som et tildelingstrinn skal vente på en systemressurs som er låst av et annet tildelingstrinn. Når denne tiden overskrides, behandles ikke på bølgen, og det vises en feilmelding.  
1. Velg **Lagre**.
1. Lukk siden.
1. Gå til **Navigasjonsrute > Moduler > Produksjonskontroll > Oppsett > Parametere for produksjonskontroll**.
1. Velg et alternativ i feltet **Frigi til lager**.

    Når det gjelder salgsordrer og Kanban-bestillinger, må beholdning reserveres før ordren frigis til lageret. Hvis ikke, varer eller tildelingslinjer kan ikke behandles i en Bølge. For produksjonsordrer kan du også velge **Tillat delvis reservasjon**. Dette er for eksempel nyttig hvis du har materialene du trenger for å starte produksjon, og du kan deretter vente til tilleggsmaterialene bli tilgjengelige for å fullføre prosessen. Hvis du velger dette alternativet, må du gjenta prosessen med frigivelse til lager manuelt når tilleggsmaterialene flere blir tilgjengelige.
1. Lukk siden.

## <a name="additional-resources"></a>Tilleggsressurser

- [Bølgeoppretting og -behandling](../wave-processing.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

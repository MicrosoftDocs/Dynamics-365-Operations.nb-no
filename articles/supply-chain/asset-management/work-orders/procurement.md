---
title: Innkjøp
description: Denne artikkelen beskriver innkjøp i Aktivastyring.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderPurchaseListPagePreviewPane, EntAssetWorkOrderPurchaseListPage, EntAssetWorkOrderPurchaseLineAmountInfoPart, EntAssetWorkOrderPurchReqListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6e41a28ec922924b0ef86858a881280fd44bfe63
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014959"
---
# <a name="procurement"></a>Innkjøp

[!include [banner](../../includes/banner.md)]

I Aktivastyring kan du få en oversikt over innkjøpsrekvisisjoner og bestillinger som er knyttet til arbeidsordrer. Du kan også opprette en bestilling eller en innkjøpsrekvisisjon fra en arbeidsordre.

Listesiden **Innkjøpsrekvisisjon for arbeidsordre** (**Aktivastyring** > **Innkjøp** > **Innkjøpsrekvisisjon for arbeidsordre**) viser en liste over innkjøpsrekvisisjoner som er knyttet til arbeidsordrer. Når du velger en arbeidsordrejobb på denne siden, kan du bruke knappene i gruppen **Vis** i handlingsrutefanen **Innkjøpsrekvisisjon for arbeidsordre** til å utføre forskjellige handlinger:

- Hvis du vil åpne den tilknyttede innkjøpsrekvisisjonen, velger du **Innkjøpsrekvisisjon**. 
- Velg **Arbeidsordre** for å åpne er relatert arbeidsordre.
- Hvis du vil ha en oversikt som viser hvor varen på den valgte linjen brukes i forhold til aktiva, vedlikeholdjobbtypestandarder, reservedeler og arbeidsordrer i Aktivastyring, velger du **Vare der brukt**. Hvis du vil ha mer informasjon om denne oversikten, kan du se [Brukssted for vare](../controlling-and-reporting/item-where-used.md).

Illustrasjonen nedenfor viser et eksempel på listesiden **Innkjøpsrekvisisjon for arbeidsordre**.

![Figur 1.](media/08-work-orders.png)


Listesiden **Innkjøp for arbeidsordre** (**Aktivastyring** > **Innkjøp** > **Innkjøp for arbeidsordre**) viser en liste over innkjøpsordrer som er knyttet til arbeidsordrer. Når du velger en arbeidsordrejobb på denne siden, kan du bruke knappene i gruppen **Vis** i fanen **Innkjøp for arbeidsordre** i handlingsrutefanen til å utføre forskjellige handlinger:

- Velg **Bestilling** for å åpne den relaterte bestillingen. 
- Velg **Arbeidsordre** for å åpne er relatert arbeidsordre.
- Hvis du vil ha en oversikt som viser hvor varen på den valgte linjen brukes i forhold til aktiva, vedlikeholdjobbtypestandarder, reservedeler og arbeidsordrer i Aktivastyring, velger du **Vare der brukt**. Hvis du vil ha mer informasjon om denne oversikten, kan du se [Brukssted for vare](../controlling-and-reporting/item-where-used.md).

Illustrasjonen nedenfor viser et eksempel på listesiden **Innkjøp for arbeidsordre**.

![Figur 2.](media/09-work-orders.png)


På listesiden **Innkjøp for arbeidsordre** og listesiden **Innkjøpsrekvisisjon for arbeidsordre** vises et symbol som er knyttet til leveringsdatokontroll på høyre side av hver linje. Hvis symbolet er et utropstegn i en rød sirkel, betyr det at levering av den tilknyttede bestillingen eller innkjøpsrekvisisjonen kan bli forsinket.

For en bestilling blir datoen som er knyttet til bestillingslinjen, brukt til å beregne en mulig forsinkelse. Hvis du vil vise denne datoen, velger du bestillingslinjen på siden **Bestilling**. Datoen vises i feltet **Bekreftet leveringsdato** i fanen **Oppsett** på hurtigfanen **Linjedetaljer**. Hvis feltet **Bekreftet leveringsdato** ikke er angitt, brukes datoen i feltet **Leveringsdato** på hurtigmenyen **Bestillingshode** til beregning. Én av disse datoene sammenlignes med den tilgjengelige datoen i arbeidsordren eller arbeidsordrejobben i følgende rekkefølge:

1. Faktisk startdato i arbeidsordren  

2. Planlagt startdato i den tilknyttede arbeidsordrejobben 

3. Planlagt startdato i arbeidsordren 

4. Forventet startdato i arbeidsordren 

I en innkjøpsrekvisisjon brukes datoen i feltet **Ønsket dato** på hurtigfanen **Innkjøpsrekvisisjonshode** på siden **Innkjøpsrekvisisjoner** til å beregne en mulig forsinkelse. Datoen i feltet sammenlignes med den tilgjengelige datoen i arbeidsordren eller arbeidsordrejobben, i samme rekkefølge som brukes til en bestilling.


## <a name="create-a-purchase-order-from-a-work-order"></a>Opprette en bestilling fra en arbeidsordre

På listesiden **Alle arbeidsordrer** kan du velge en arbeidsordrejobb og deretter opprette en tilknyttet bestilling eller innkjøpsrekvisisjon. På den måten sikrer du at det finnes prosjektrelasjoner mellom bestillingen eller innkjøpsrekvisisjonen og arbeidsordren.

1. Velg **Aktivastyring** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg arbeidsordren du vil opprette en bestilling for, og velg deretter **Rediger**.

3. I hurtigfanen **Vedlikeholdsjobber for arbeidsordre** velger du arbeidsordrejobben du vil opprette bestillingen for.

4. Velg **Vareoppgaver** > **Bestilling fra arbeidsordrejobb**.

5. Velg **Ny** på listesiden **Prosjektbestillinger**.

6. Opprett bestillingen.

>[!NOTE]
>Hvis du vil opprette en relatert innkjøpsrekvisisjon, kan du bruke de samme trinnene. Du må imidlertid velge **Vareoppgaver** > **Innkjøpsrekvisisjon fra arbeidsordrejobb** i trinn 4.


## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Prosjektrelasjon mellom arbeidsordre og bestilling eller innkjøpsrekvisisjon

En bestillingslinje eller innkjøpsrekvisisjonslinje er knyttet til en arbeidsordrejobb via arbeidsordreprosjektet og det tilknyttede prosjektaktivitetsnummeret. Når du oppretter en bestilling eller en innkjøpsrekvisisjon fra en arbeidsordrejobb, er det tilknyttede prosjektaktivitetsnummeret obligatorisk. Prosjektaktivitetsnummeret settes automatisk inn på en bestilling eller innkjøpsrekvisisjon hvis alle arbeidsordrejobber i den tilknyttede arbeidsordren har samme vedlikeholdsjobbtype. Hvis arbeidsordrejobbene har ulike vedlikeholdsjobbtyper, må du angi prosjektaktivitetsnummeret på bestillingen eller innkjøpsrekvisisjonen manuelt.

Hvis du vil vise eller angi aktivitetsnummeret som er knyttet til en bestillingslinje, velger du bestillingsposten på listesiden **Innkjøp for arbeidsordre**, og deretter velger du koblingen for bestillingen i kolonnen **Bestilling**. Du finner feltet **Aktivitetsnummer** i fanen **Prosjekt** på hurtigfanen **Linjedetaljer**.

Illustrasjonen nedenfor viser et eksempel på siden **Bestilling**, med fokus på **Aktivitetsnummer**.

![Figur 3.](media/10-work-orders.png)

Hvis du vil vise eller angi aktivitetsnummeret som er knyttet til en linje for arbeidsordreinnkjøpsrekvisisjon, velger du innkjøpsrekvisisjonsposten på listesiden **Innkjøpsrekvisisjon for arbeidsordre**, og deretter velger du koblingen for innkjøpsrekvisisjonen i kolonnen **Innkjøpsrekvisisjon**. Du finner feltet **Aktivitetsnummer** i fanen **Prosjekt** på hurtigfanen **Linjedetaljer**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
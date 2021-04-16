---
title: Overstyre standard reserveringsprinsipp for materialer i produksjon
description: Dette emnet beskriver hvordan du angir et standard reserveringsprinsipp for hver varemodellgruppe, slik at forskjellige reserveringsprinsipper kan brukes automatisk for hver vare som er del av en produksjonsstykkliste eller partiordreformel.
author: johanhoffmann
ms.date: 12/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-10
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a1b2dd204c9a507dba387b0295f3021253e02dc4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814808"
---
# <a name="override-the-default-reservation-principle-for-materials-in-production"></a>Overstyre standard reserveringsprinsipp for materialer i produksjon

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Med funksjonen *Overstyr standard produksjonsreservering* kan du angi et standard reserveringsprinsipp for hver varemodellgruppe. De ulike reserveringsprinsippene kan derfor automatisk brukes for hver vare som er del av en produksjonsstykkliste eller partiordreformel. Du kan velge om hver varemodellgruppe skal overstyre standard reserveringsprinsipp som er angitt for en ordre, og hvilket reserveringsprinsipp som skal brukes i stedet (*manuell*, *anslag*, *planlegging*, *frigivelse* eller *start*).

Når du oppretter en ny produksjonsordre eller partiordre, blir du bedt om å velge reserveringsprinsippet som skal brukes på denne ordren, og alle stykklistelinjene eller formellinjene. Når funksjonen *Overstyr standard produksjonsreservering* brukes, kan noen eller alle stykkliste- eller formellinjene overstyre dette reserveringsprinsippet og i stedet bruke reserveringsprinsippet som er angitt for den aktuelle varemodellgruppen.

Hvis du for eksempel har råvarer eller ingredienser som krever plukkarbeid, må stykkliste- eller formellinjer som opprettes for disse produktene, reserveres fysisk siden fysisk reservering er en forutsetning for generering av lagerarbeid. Hvis du vil at reserveringen skal skje automatisk, kan du vanligvis velge et av følgende reserveringsprinsipper: *anslag*, *planlegging*, *frigivelse* eller *start*. Hvis du på den annen side har materialer eller ingredienser som ikke krever plukkarbeid, fordi de forbrukes direkte fra en lokasjon, velger du vanligvis det *manuelle* reserveringsprinsippet, som ikke foretar noen fysiske reserveringer eller genererer noe plukkingsarbeid.

## <a name="turn-on-the-feature"></a>Aktivere funksjonen

Før du kan bruke funksjonen må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Produksjonskontroll*
- **Funksjonsnavn:** *(Forhåndsversjon) Overstyr standard produksjonsreservering*

## <a name="assign-a-production-reservation-policy-to-an-item-model-group"></a>Tilordne en policy for produksjonsreservering til en varemodellgruppe

1. Gå til **Kostnadsstyring \> Oppsett for regnskapspolicyer for beholdning \> Varemodellgrupper**.
1. Opprett eller velg en varemodellgruppe.
1. Merk av for **Overstyr reservering for vareproduksjon** i hurtigfanen **Beholdningspolicyer**.
1. I **Reservering**-feltet velger du reserveringsprinsippet for varer som hører til i den valgte modellgruppen. (Disse varene omfatter varer som er på en stykkliste- eller formellinje.)

    - **Manuell** – Varer i modellgruppen reserveres ikke fysisk for produksjon automatisk. De kan imidlertid likevel reserveres manuelt etter behov.
    - **Anslag** – Varer i modellgruppen blir fysisk reservert under beregning av produksjonsordren.
    - **Planlegging** – Varer i modellgruppen blir fysisk reservert under planlegging av produksjonsordren.
    - **Frigivelse** – Varer i modellgruppen blir fysisk reservert når produksjonsordren frigis.
    - **Start** – Varer i modellgruppen blir fysisk reservert ved starten av produksjonsordren.

## <a name="example-using-reservation-principles-in-a-bulkpack-scenario"></a>Eksempel: Bruke reserveringsprinsipper i et bulk-/pakkescenario

Et bulksmøremiddel produseres i en 1000-liters mikser. Når bulkmaterialet er klart, pumpes det ut til flere fyllestasjoner der flasker av ulike størrelser fylles. Når fyllingen er fullført, pakkes flaskene inn i esker. Disse eskene blir deretter pakket på paller.

I dette scenarioet opprettes det en partiordre for å lage 1000 liter bulkmateriale. (Denne ordren er bulkordren.) Når denne partiordren er fullført, blir den ferdigmeldt til innleveringsstedet for materiale ved fyllestasjonene. Det blir deretter opprettet en partiordre for å fylle og pakke hver flaskestørrelse. (Disse ordrene er pakkeordrer.) Pakkeordrene har en formel som består av bulkmaterialet, en tom flaske, en etikett og andre emballasjematerialer. Siden bulkmaterialet flyter direkte fra miksertanken til fyllestasjonene, kreves det ikke noe lagerarbeid for å plukke denne ingrediensen, og bulkmaterialet forbrukes direkte fra innleveringsstedet. Reserveringsprinsippet er derfor satt til *manuell*. De andre materialene klargjøres for fyllestasjonen i faser med plukkarbeid. Reserveringsprinsippet for disse linjene er derfor for eksempel satt til å *frigivelse*, slik at reserveringen skjer automatisk når pakkeordren frigis.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
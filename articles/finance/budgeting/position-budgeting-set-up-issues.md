---
title: Feilsøke stillingsbudsjettering
description: Denne artikkelen inneholder svar på spørsmål du kan ha når du konfigurerer stillingsbudsjettering. Det tar for seg vanlige spørsmål om hvordan du oppretter budsjettetkostnadselementer, kompensasjonsgrupper og kompensasjonsrutenett.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: kfend
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d09aa8528eeccb214aea02b333ebd6353314984
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722974"
---
# <a name="position-budgeting-troubleshooting"></a>Feilsøke stillingsbudsjettering

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder svar på spørsmål du kan ha når du konfigurerer stillingsbudsjettering. Det tar for seg vanlige spørsmål om hvordan du oppretter budsjettetkostnadselementer, kompensasjonsgrupper og kompensasjonsrutenett. 

## <a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a>Hvorfor finner jeg ikke siden med prognosestillinger under Personale?

Prognosestillinger er flyttet til Budsjettering.

## <a name="why-cant-i-delete-a-budget-cost-element"></a>Hvorfor kan jeg ikke slette et budsjettkostnadselement?
Du kan ikke slette et budsjettkostnadselement som er tilordnet til en prognosestilling. Før du kan slette et budsjettkostnadselement, må du fjerne det fra alle prognosestillinger. **Tips:** For å finne alle stillinger som et budsjettert kostnadselement er tilordnet til, må du velge kostnadselementer å¨sioden **Budsjettkostnadselementer** og klikk deretter **Oppdater stillinger**. Stillinger som bruker kostnadselementet, vises i det øvre rutenettet.

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a>Hvordan kan jeg fjerne et kostnadselement fra flere prognosestillinger uten å åpne dem?
Du kan ikke fjerne et kostnadselement. Hvis du imidlertid endrer start- og sluttdatoene slik at de faller utenfor datoene for budsjettplanleggingssyklusen, blir kostnadselementert ikke lenger tilordnet til prognosestillingene i budsjettplanleggingssyklusen. Til å gjøre denne endringen åpner du det budsjetterte kostnadselementet, og deretter i hurtigkategorien **Kostnadsberegning** klikker du **Endre datoer** og endre gjeldende dato eller utløpsdatoen. Velg **OK** for å oppdatere automatisk alle prognosestillingene som kostnadelementet er tilordnet til. **Tips!** Hvis du bruker denne metoden, må du være oppmerksom på at budsjettkostnadselementet dermed fjernes fra **alle** prognosestillinger der start- og sluttdatoene ikke lenger er i det aktuelle området. Hvis dette ikke er det vil skal skje, må du åpne hver prognosestilling du vil fjerne budsjettkostnadselementet fra, og foreta endringen manuelt.

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a>Hvorfor kan jeg ikke angi et årlig beløp i hurtigkategorien Kostnadsberegning for budsjettkostnadselementet?
Du kan ikke angi et årlig beløp hvis det finnes budsjettkostnadselementer i hurtigkategorien **Beregningsgrunnlag**, fordi systemet krever en prosent for å beregne verdien. Fjern alle budsjettkostnadselementer fra hurtigkategorien **Beregningsgrunnlag** for å endre denne verdien.

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a>Hvorfor kan jeg ikke endre budsjettkostnadstypen fra inntekt til en annen budsjettkostnadstype?
Noen budsjettkostnadselementer bruker kostnadselementet inntekt som beregningsgrunnlag. Hvis du vil endre feltet **Budsjettkostnadstype**, må du fjerne kostnadselementet inntekt fra hurtigkategorien **Beregningsgrunnlag** for alle budsjettkostnadselementer.

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a>Hvorfor kan jeg ikke endre datoen på linjer for budsjettkostnadselement for et budsjettkostnadselement?
Du kan ikke endre datoen på linjen for budsjettkostnadselementet når et budsjettskostnadselement brukes av en prognosestilling. Denne begreningein sikrer at prognosestillingene alltid er innenfor retningslinjene for budsjettkostnadselementet. Hvis duvil endre datoen i hurtigkategorien **Kostnadsberegning**, klikker du **Endre datoer** og angir de nye datoene. Klikk deretter **OK** for å oppdatere prognosestillingene som kostnadelementet er tilordnet til.

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a>Hvorfor kan jeg ikke endre kostnadene for et budsjettkostnadselement på siden Kompensasjonsgruppe?
Du kan bare opprette og endre budsjettkostnadselementer på siden **Budsjettkostnadselementer**.

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a>Hvorfor får jeg en feilmelding når jeg endrer datoene for et kostnadselement i en prognosestilling?
Datoene på prognosestillingens linje for kostnadselement må være innenfor følgende områder:

-   Aktiverings- og pensjonavgangsdatoene for stillingen.
-   Aktiverings- og utløpsdatoene for budsjettkostnadselementet.
-   Start- og sluttdatoene for budsjettsyklusen som er knyttet til budsjettplanleggingsprosessen for prognosestillingen.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]

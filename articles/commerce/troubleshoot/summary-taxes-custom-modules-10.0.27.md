---
title: Delsummering av bestillinger omfatter ikke avgifter på tillegg ved bruk av moduler for tilpassede ordresammendrag
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når du bruker tilpassede samlemoduler for ordrer, og delsummen for ordren inkluderer ikke avgifter på gebyrer i scenariet Pris inkluderer merverdiavgift.
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 1a47561a3ac984bc554b5b93546592237c16cf18
ms.sourcegitcommit: 48d094d083c1bd45c3d72f8b666926b48ec7ae35
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2022
ms.locfileid: "8767962"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>Delsummering av bestillinger omfatter ikke avgifter på tillegg ved bruk av moduler for tilpassede ordresammendrag

Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når du bruker tilpassede samlemoduler for ordrer, og delsummen for ordren inkluderer ikke avgifter på gebyrer i scenariet Pris inkluderer merverdiavgift.

## <a name="description"></a>Beskrivelse

Fra og med Microsoft Dynamics 365 Commerce versjon 10.0.27 er det gjort følgende endringer i scenariet "Pris inkluderer mva", for å gi en konsekvent erfaring i ordresammendragsmoduler på tvers av e-handelssider.

- To nye felt er lagt til: **TaxOnShippingCharge** og **TaxOnNonShippingCharges**.
- APIene **GetSalesOrderBySalesId** og **GetSalesOrderByTransactionId** har nøyaktige verdier for følgende felt i scenariet "pris inkluderer merverdiavgift":

    - SubtotalSalesAmount
    - SubtotalAmountWithoutTax
    - SubtotalAmount
    - ShippingChargeAmount
    - OtherChargeAmount

Hvis du imidlertid bruker tilpassede moduler for ordresammendrag, kan disse endringene påvirke delsumverdiene for ordresammendrag ved ikke å inkludere avgifter på tillegg.

## <a name="resolution"></a>Oppløsning

Hvis du bruker moduler for tilpasset ordresammendrag, og ikke vil arve endringene som er gjort i scenariet "Pris inkluderer merverdiavgift" i Commerce versjon 10.0.27 og senere, følger du instruksjonene i denne delen.

Ved å gå tilbake til den forrige (før versjon 10.0.27) ordresammendragsatferden for feltene **salesTransaction.SubtotalAmount** og **salesTransaction.SubtotalAmountWithoutTax**-feltene, gjenoppretter du inkluderingen av totalt gebyr-avgiftsbeløpet(**TaxOnShippingCharge** og **TaxOnNonShippingCharges**) i delsummene (**SubtotalAmount** og **SubtotalAmountWithoutTax**).

Følg denne fremgangsmåten for å gå tilbake til det forrige sammendragsvirkemåten for ordre.

1. I Commerce headquarters åpner Handelsparametere-siden (**Detaljhandel og forretningsdrift \> Hovedkvarteroppsett \> Parametere \> Handelsparametere**).
1. I den venstre navigasjonsruten velger du **Konfigurasjonsparametre**.
1. Legg til følgende konfigurasjonsparametere, og sett verdien for hver til **sann**:

    - IsLegacyTaxOnChargeInSubtotalAmountIncludedInTaxIncusiveEnabled
    - IsLegacyOrderSummaryHydrationEnabled

> [!NOTE]
> Hvis du tidligere har brukt konfigurasjonsparameteren **IsUpdatedPriceIncludesTaxSubtotalCalculationEnabled**, og vil beholde samme virkemåte for egenskapen **order.NetAmountWithoutTax**, må du også legge til konfigurasjonsparameteren **IsLegacyPriceIncludesTaxNetAmountWithoutTaxCalculationEnabled** og sette verdien til **sann**.

## <a name="additional-resources"></a>Tilleggsressurser

[Skjul informasjon om avgiftsoppbrudd i ordresammendrag](../hide-taxes-breakup.md)

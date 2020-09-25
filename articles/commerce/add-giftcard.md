---
title: Gavekortmodul
description: Dette emnet dekker gavekortmoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761087"
---
# <a name="gift-card-module"></a>Gavekortmodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet dekker gavekortmoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Gavekortmoduler kan brukes i betalingsmoduler til å godta gavekort, som er en vanlig betalingsform som brukes i e-handelstransaksjoner. Gavekortmodulen støtter Dynamics 365-, SVS- og Givex-gavekort. SVS- og Givex-gavekort løses inn via betalingsleverandøren Adyen. Hvis du vil ha mer informasjon om støtte for eksterne gavekort som SVS og Givex, kan du se [Støtte for eksterne gavekort](./dev-itpro/gift-card.md).

Det finnes to tilgjengelige gavekortmoduler:

- **Gavekort** – Denne modulen kan brukes på en betalingsside til å løse ut et gavekort som et betalingsmiddel. 
- **Kontroll av gavekortsaldo** – Denne modulen kan brukes på alle sider til å kontrollere saldoen på et gavekort. Denne modulen er tilgjengelig i Commerce versjon 10.0.14 og nyere.

Bildet nedenfor viser et eksempel på en gavekortmodul på en kasseside.

![Eksempel på en gavekortmodul](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Modulegenskaper

- **Vis flere felt** – Denne egenskapen definerer hvilke felt som skal vises for gavekort i tillegg til gavekortnummeret, som alltid vises som standard. Noen gavekort støtter for eksempel visning av et personlig identifikasjonsnummer (PIN), og andre støtter visning av en PIN-kode og en utløpsdato. Alternativt kan denne egenskapen settes til "Ingen", som bare vil vise gavekortnummeret og ingen flere felt.

Verdier som støttes:
-   PIN-kode
-   Utløpsdato
-   PIN-kode og utløpsdato 
-   None

## <a name="site-settings-for-gift-card-modules"></a>Områdeinnstillinger for gavekortmoduler

I Commerce-områdebygger under **Områdeinnstillinger \> Tillegg** er det en innstilling for gavekortmodulen kalt **Støttet gavekorttype**. Denne innstillingen støtter tre verdier:
- **Dynamics 365-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen bare innløsning av Dynamics 365-gavekort. Denne innstillingen støttes bare for påloggede brukere på e-handelsområdet.
- **SVS- og Givex-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen bare innløsning av Givex- og SVS-gavekort. Denne innstillingen støttes for påloggede og anonyme brukere på e-handelsområdet.
- **Dynamics 365-, SVS- og Givex-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen innløsning av Dynamics 365-, Givex- og SVS-gavekort. Denne innstillingen støttes bare for påloggede brukere på e-handelsområdet.

## <a name="add-a-gift-card-module-to-a-page"></a>Legge til en gavekortmodul på en side

Hvis du vil ha informasjon om hvordan du legger til en gavekortmodul på en kasseside og angir de nødvendige egenskapene, kan du se [Kassemodul](add-checkout-module.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Handlekurvmodul](add-cart-module.md)

[Handlekurvikonmodul](cart-icon-module.md)

[Kassemodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Modul for leveringsalternativer](delivery-options-module.md)

[Ordredetaljermodul](order-confirmation-module.md)

[Støtte for eksterne gavekort](./dev-itpro/gift-card.md)

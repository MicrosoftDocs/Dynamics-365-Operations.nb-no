---
title: Gavekortmodul
description: Dette emnet dekker gavekortmoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 41f808d671bf5e7425390484ea30470e044899d8
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661248"
---
# <a name="gift-card-module"></a>Gavekortmodul

[!include [banner](includes/banner.md)]

Dette emnet dekker gavekortmoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Gavekort er en vanlig betalingsmåte, og gavekortmodulen kan brukes i en kassemodul for å godta gavekort. Gavekortmodulen støtter Dynamics 365-, SVS- og Givex-gavekort. SVS- og Givex-gavekort løses inn via betalingsleverandøren Adyen.

Hvis du vil ha mer informasjon om støtte for eksterne gavekort som SVS og Givex, kan du se [Støtte for eksterne gavekort](./dev-itpro/gift-card.md)

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

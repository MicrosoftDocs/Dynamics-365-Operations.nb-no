---
title: Importer og eksporter vurderinger og omtaler
description: Dette emnet beskriver hvordan du importerer og eksporterer produktvurderinger og -omtaler i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 3ae85f21f7a78d56621aed60527207badcee9c75
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968529"
---
# <a name="import-and-export-ratings-and-reviews"></a>Importer og eksporter vurderinger og omtaler

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du importerer og eksporterer produktvurderinger og -omtaler i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce tilbyr [vurderinger og omtaler](ratings-reviews-overview.md) som en omnikanalløsning. Når du bytter til Dynamics 365 Commerce-løsningen for vurderinger og omtaler, kan det hende at du vil flytte de eksisterende vurderings- og omtaledataene til Commerce-plattformen. Det kan også være at du ønsker å eksportere vurderings- og omtaledata fra Commerce, basert på forretningskravene. Med en Power Automate-kobling kan du importere vurderinger og omtaler til Commerce og eksportere dem fra Commerce.

> [!NOTE]
> Hvis du vil ha informasjon om hvordan du kommer i gang med logiske flyter i Power Automate, kan du se [Opprett en skyflyt i Power Automate](/power-automate/get-started-logic-flow).

## <a name="prerequisites"></a>Forutsetninger

Før du kan importere og eksportere vurderinger og omtaler, må du oppfylle følgende forutsetninger:

- Løsningen for vurderinger og omtaler må være aktivert for e-handelsområdet på Commerce-plattformen. Hvis du vil ha mer informasjon, kan du se [Velg å bruke vurderinger og omtaler](opt-in-ratings-reviews.md).
- Dynamics 365 Ratings and Reviews Power App Connector må være konfigurert til å muliggjøre innsending av vurderinger eller eksport av vurderinger i Power Automate. Hvis du vil ha mer informasjon, kan du se [Dynamics 365 Commerce – vurderinger og omtaler (forhåndsversjon)](/connectors/dynamics365ratingsre/).
- Service-to-Service-godkjenning (S2S) må konfigureres til å kalle API-en for vurderinger og omtaler fra utenfor Commerce på en sikker måte. Hvis du vil ha mer informasjon, kan du se [Konfigurer tjeneste-til-tjeneste-godkjenning](service-to-service-auth.md).

## <a name="import-ratings-and-reviews"></a>Importer vurderinger og omtaler

Hvis du vil importere vurderings- og omtaleav data fra det eksisterende systemet til Commerce, må du legge til Dynamics 365 Ratings and Review Power Automate-koblingen til en eksisterende Power Automate-flyt eller en ny flyt. Hvis du vil ha mer informasjon, kan du se [Dynamics 365 Commerce – vurderinger og omtaler (forhåndsversjon)](/connectors/dynamics365ratingsre/).

> [!IMPORTANT]
> Før du kan fullføre denne prosedyren, må du [konfigurere S2S-godkjenning](service-to-service-auth.md).

Hvis du vil importere vurderinger og omtaler i Commerce ved å bruke Dynamics 365 Ratings and Reviews Power Automate-koblingen, følger du trinnene nedenfor.

1. Velg handlingen **Send inn brukeromtale**.
1. Opprett en tilkobling ved å bruke Azure Active Directory-appinformasjonen (Azure AD) som ble opprettet da du konfigurerte S2S-godkjenningen. Hvis du vil ha mer informasjon, kan du se [Konfigurer tjeneste-til-tjeneste-godkjenning](service-to-service-auth.md).
1. Handlingen **Send inn brukeromtale** tar én omtale om gangen. Gjenta derfor handlingen. Bruk kildeomtalene som en liste for å sende masseomtaler.
    
## <a name="export-ratings-and-reviews"></a>Eksporter vurderinger og omtaler

Hvis du vil eksportere vurderings- og omtaledata fra Commerce, må du legge til Dynamics 365 Ratings and Review Power Automate-koblingen til en eksisterende Power Automate-flyt eller en ny flyt. Hvis du vil ha mer informasjon, kan du se [Dynamics 365 Commerce – vurderinger og omtaler (forhåndsversjon)](/connectors/dynamics365ratingsre/).

Hvis du vil eksportere vurderinger og omtaler fra Commerce ved å bruke Dynamics 365 Ratings and Reviews Power Automate-koblingen, følger du trinnene nedenfor.

1. Velg handlingen **Eksporter alle omtaler**.
1. Fullfør handlingen. 

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Velge å bruke vurderinger og anmeldelser](opt-in-ratings-reviews.md)

[Administrere vurderinger og anmeldelser](manage-reviews.md)

[Konfigurere vurderinger og anmeldelser](configure-ratings-reviews.md)

[Synkronisere produktvurderinger](sync-product-ratings.md)

[Aktivere manuell publisering av vurderinger og vurderinger av en moderator](manual-publish-rating-reviews.md)

[Konfigurer tjeneste-til-tjeneste-godkjenning](service-to-service-auth.md)

[Vanlige spørsmål om rangeringer og anmeldelser](ratings-reviews-faq.md)

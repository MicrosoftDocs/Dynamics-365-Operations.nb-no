---
title: Livssyklus for modelladministrasjon (forhåndsversjon)
description: Dette emnet beskriver måter å vedlikeholde organisasjonens maskinopplæringsmodeller på for å optimalisere prognosene de genererer.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: d5566bde97a2e60d050f4a7b499b554df4848bf9
ms.sourcegitcommit: f6050b444e636ba662c00d0443c94a99f8ea0b0d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/28/2021
ms.locfileid: "6309796"
---
# <a name="model-management-lifecycle-preview"></a>Livssyklus for modelladministrasjon (forhåndsversjon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver måter å vedlikeholde organisasjonens maskinopplæringsmodeller på for å optimalisere prognosene de genererer.

Vi anbefaler at du lærer opp AI-modellen i et sandkassemiljø og deretter bruker administrerte løsninger for å distribuere den til et produksjonsmiljø. Denne fremgangsmåten sikrer at de riktige kontrollene er på plass for administrasjon av modell-livssyklusen.

Siden AI-modellen er basert på de tilgjengelige faktura- og kundedataene, er det viktig at sandkassemiljøet har en ny kopi av produksjonsdataene. Du kan begynne å lære opp modellen ved å følge trinnene i [Bruke kundebetalingsforutsigelser](use-customer-payment-predictions.md). Når modellen er blitt lært opp på nytt, kan du evaluere resultatene slik det beskrives under [Evaluere den opprinnelige forutsigelsesmodellen for kundebetaling](evaluate-payment-prediction.md). Bruk informasjonen i [Forbedre forutsigelsesmodellen](improve-model.md) til å eksperimentere med funksjons- og filterkombinasjoner som kan bidra til å forbedre modellen.

Når du er fornøyd med opplæringsresultatene, følger du trinnene i [Distribuere AI-modellen](https://docs.microsoft.com/ai-builder/distribute-model) for å overføre modellen til produksjonsmiljøet.

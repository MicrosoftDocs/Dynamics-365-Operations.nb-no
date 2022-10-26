---
title: Vanlige spørsmål om asynkron kundeopprettingsmodus
description: Denne artikkelen gir svar på vanlige spørsmål om asynkron kundeopprettingsmodus i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 64c895fb9f3e55f7680759fa72626be6660aa67c
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690209"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>Vanlige spørsmål om asynkron kundeopprettingsmodus

[!include [banner](includes/banner.md)]

Denne artikkelen gir svar på vanlige spørsmål om asynkron kundeopprettingsmodus (asynk) i Microsoft Dynamics 365 Commerce.

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>Hvorfor kan jeg ikke aktivere funksjonen Aktiver redigering av kunder i asynkron modus?

Du må aktivere følgende funksjoner før du aktiverer funksjonen **Aktiver redigering av kunder i asynkron modus**:

- Ytelsesforbedringer for kundeordrer og kundetransaksjoner
- Aktiver forbedret asynkron kundeopprettelse
- Aktiver asynkron oppretting for kundeadresser

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>Hvorfor ser jeg fremdeles serviceanrop i sanntid som er gjort i Commerce headquarters etter at funksjonen Aktiver redigering av kunder i asynkron modus er aktivert?

Dette problemet oppstår når Commerce Data Exchange-jobber (CDX) ikke har blitt kjørt for å sikre at funksjonsstatusen og andre kanalmetadata er synkronisert med kanalen. Før du prøver scenarioet på nytt, må du kontrollere at følgende CDX-jobber kjøres i Commerce headquarters:

- 1110 (Global konfigurasjon)
- 1010 (Kunder)
- 1070 (Kanalkonfigurasjon)

Data som hurtigbufres i Commerce Scale Unit (CSU), gjenspeiles kanskje ikke umiddelbart i Commerce headquarters etter at CDX-jobbene er kjørt.

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>Hvorfor viser ikke Commerce headquarters kundeopprettelse eller oppdateringer fra salgsstedet eller netthandelskanalen?

Kontroller at følgende handlinger er utført i den rekkefølgen de er oppført her.

1. Kjør CDX P-jobben i Commerce headquarters for å sikre at asynkrone kundedata som er lagret i tabellen **RETAILASYNCCUSTOMERV2**, **RETAILASYNCADDRESSV2**, **RETAILASYNCCUSTOMERCONTACT**, **RETAILASYNCCUSTOMERAFFILIATION** og **RETAILASYNCCUSTOMERATTRIBUTEV2**.
1. Kjør den satsvise jobben **Synkroniser kunder og kanalforespørsler** i Commerce headquarters. Når den satsvise jobben er utført, vil alle poster som er behandlet fra tabellene ovenfor, ha feltet **OnlineOperationCompleted** satt til **1**.

### <a name="how-do-i-know-which-customer-management-in-asynchronous-mode-operation-has-failed-and-how-do-i-make-changes-if-they-are-required"></a>Hvordan vet jeg hvilken kundebehandling i asynkron modus som har mislyktes, og hvordan kan jeg foreta endringer hvis de er nødvendige?

Hvis du vil vise alle asynkrone modusoperatsjoner og synkroniseringsstatusen, går du til Commerce headquarters og **Commerce and Retail \> Kunder \> Kundesynkroniseringsstatus**. Hvis du vil foreta endringer, redigerer du en bestemt operasjon, oppdaterer feltene, velger **Lagre** og deretter **Synkroniser** for å synkronisere endringene.


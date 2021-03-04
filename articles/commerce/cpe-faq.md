---
title: Vanlige spørsmål om evalueringsmiljø for Dynamics 365 Commerce
description: Dette emnet gir svar på vanlige spørsmål om Microsoft Dynamics 365 Commerce-evalueringsmiljøet.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 637714e28b9f8f4aa66e251e709d8f78bff2739d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414542"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Vanlige spørsmål om evalueringsmiljø for Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Dette emnet gir svar på vanlige spørsmål om Microsoft Dynamics 365 Commerce-evalueringsmiljøet.

**Kan vi bruke Commerce-evalueringsmiljøet som en e-handel-butikkfasade for kunder som for tiden implementerer Retail?**

Nr. Evalueringsmiljøet for Commerce er bare for evaluering. Hvis du trenger et miljø for en kunde som implementerer Retail, kan du kontakte Microsoft.

**Kan evalueringsmiljøet for Commerce brukes til å klargjøre e-handelsfunksjonene oppå et eksisterende program/miljø som implementerer Retail?**

Nei (for det meste). Komponentene for Commerce-evaluering er bare tilgjengelige for miljøer som samsvarer med konfigurasjonene som er angitt i veiledningen for forhåndskrav og klargjøring. I tillegg vil de nødvendige grunndemodataene ikke være tilgjengelige i miljøer som ble distribuert med en første versjon som er eldre enn 10.0.8. 

**Hvilke kostnader er involvert i distribusjon av evalueringsmiljøet for Commerce på Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**

Et tradisjonelt Dynamics 365 Finance/Dynamics 365 Supply Chain Management-/Dynamics 365 Commerce-hovedkvarterdemomiljø (virtuell maskin\[VM\]) vil være vert for Azure-abonnementet. Du kan bruke [Azure prising-kalkulatoren](https://azure.microsoft.com/pricing/calculator/) til å estimere denne kostnaden.

Andre komponenter som for eksempel Commerce Scale Unit, Commerce-områdebygger og ditt e-handelsområde vil være tilgjengelig som en tjeneste (SaaS) og være vertsbasert hos Microsoft.

**Hvilke Azure-områder støttes for øyeblikket for evalueringsmiljøet i Commerce?**

Evalueringsmiljøet for Commerce kan bare distribueres i Nord-Amerika-området.

**Finnes det en nedlastbar virtuell harddisk (VHD) som har det komplette alternativet for OneBox virtuell maskin (VM)?**

Dynamics 365 Commerce og Commerce Scale Unit er fullstendig programvare som en tjeneste (SaaS) og må være skybasert.

**Hvor lenge kan evalueringsmiljøet for Commerce brukes?**

Commerce-evalueringsmiljøet har en 30-dagers tidsgrense fra datoen SaaS-komponenter som for eksempel Commerce Scale Unit, Commerce-områdebygger og ditt e-handelsområde klargjøres.

**Kan jeg forlenge tidsbegrensningen for evalueringsmiljøet i Commerce?**

Utvidelsen av tidsgrensen er et unntak fra normen og vurderes for hvert tilfelle. Du må kontakte din Microsoft-partnerkontakten for hjelp.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over Dynamics 365 Commerce-evalueringsmiljø](cpe-overview.md)

[Klargjøre et evalueringsmiljø for Dynamics 365 Commerce](provisioning-guide.md)

[Konfigurere et Dynamics 365 Commerce-evalueringsmiljø](cpe-post-provisioning.md)

[Konfigurere BOPIS i et evalueringsmiljø for Dynamics 365 Commerce](cpe-bopis.md)

[Konfigurere valgfrie funksjoner for et evalueringsmiljø for Dynamics 365 Commerce](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
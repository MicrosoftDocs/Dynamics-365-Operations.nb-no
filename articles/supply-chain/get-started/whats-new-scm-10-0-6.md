---
title: Hva er nytt eller endret i Dynamics 365 Supply Chain Management 10.0.6. (november 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Supply Chain Management 10.0.6.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9ee25036488d2f7f24c1691d36239f3f34caf0cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434457"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a>Hva er nytt eller endret i Dynamics 365 Supply Chain Management 10.0.6. (november 2019)

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management 10.0.6. Denne versjonen har et Build-nummer for 10.0.234. Når den generelle tilgjengelighetsdatoen er i november, er de nye funksjonene tilgjengelige for tidlig frigivelse i oktober. Hvis du vil ha mer informasjon om versjon 10.0.6, se [Tilleggsressurser](whats-new-scm-10-0-6.md#additional-resources).

## <a name="product-configuration-models-v2-data-entity"></a>V2-dataenheten produktkonfigurasjonsmodeller

En ny versjon for dataenheten "produktkonfigurasjonsmodeller" frigis (kalt "produktkonfigurasjonsmodeller V2"). Standardmalen "418-produktkonfigurasjonsmodeller" må også være slik at den bruker den nye "produktkonfigurasjonsmodeller V2"-dataenheten i malene for rammeverk for import/eksport. Malen blir ikke automatisk oppdatert, slik at du må laste malen inn fra standarden manuelt. V2-enheten eksporterer én rad som separat fil i et vedlegg i stedet for innebygd, og kan løse størrelsesbegrensningene for V1-enheten. 
 
Hva trenger du for å gjøre denne endringen?
-    Siden V1-enheten er avskrevet, bør du begynne å overføre fra V1 til V2. Hvis du bruker malen "418-produktkonfigurasjonsmodeller", kan du klikke knappen "last inn standardmaler" og laste malen "418 – produktkonfigurasjonsmodeller" på nytt.
-    Hvis du må beholde kompatibilitet med eksisterende systemer, kan du nå fortsette å bruke den eksisterende malen og (avskrevet) V1-enheten til du flytter integreringene til den nye malen. 

## <a name="feature-management-enhancements"></a>Forbedringer av funksjonsbehandling
Med funksjonsbehandling kan du nå aktivere alle nye funksjoner som standard, kreve bekreftelse for å aktivere en funksjon og aktivere alle funksjoner som ikke allerede er aktivert. 


## <a name="purchase-agreement-responsible-party"></a>Ansvarlig part for kjøpsavtale
Du kan nå definere primære og sekundære ansvarlige parter i skjemaet Kjøpsavtaleklassifisering og resulterende kjøpsavtaler.  Dette gir brukeren tilgang til hvem som overser avtalene.

## <a name="rfq-link-on-the-purchase-order-line"></a>Tilbudsforespørsel-kobling på kjøpsordrelinjen
Du kan legge til en referansekobling fra bestillingslinjene tilbake til de tilsvarende tilbudsforespørselslinjene de stammer fra, slik at brukeren enkelt kan få det støttende dokumentet for tilbudsforespørsel.

## <a name="additional-resources"></a>Tilleggsressurser

### <a name="bug-fixes"></a>Feilrettinger
Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av 10.0.6, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).

### <a name="platform-update-30"></a>Plattform update 30
Microsoft Dynamics 365 Supply Chain Management 10.0.6 inkluderer Platform update 30. Hvis du vil vite mer om plattformoppdatering 30, se [Hva er nytt eller endret i plattformoppdatering 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: 2019-frigivelsesbølge 2-planen
Er du spent på kommende og nylig utgitte tilleggspakkefunksjoner i våre bedriftsprogrammer eller -plattform?

Se [Dynamics 365: 2019-frigivelsesbølge 2-planen](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/). Vi har registrert alle detaljene, ende til ende, øverst til nederst, i et enkelt dokument som du kan bruke i planleggingen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og avskrevne funksjoner i Supply Chain Management

Emnet [Fjernede eller avskrevne funksjonene i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver funksjoner som er eller er planlagt å bli fjernet eller avskrevet for Supply Chain Management.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Før en funksjon fjernes fra produktet, vil avskrivningsvarselet bli kunngjort i emnet [Fjernede eller avskrevne funksjoner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder før fjerningen.

For oppdelingsendringer som bare påvirker kompileringstiden, men som er binære kompatible med sandkasse- og produksjonsmiljøer, vil avskrivningstiden være mindre enn 12 måneder. Dette er vanligvis funksjonelle oppdateringer som må gjøres på kompilatoren.

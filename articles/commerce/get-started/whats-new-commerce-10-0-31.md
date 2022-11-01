---
title: Forhåndsvisning av Dynamics 365 Commerce 10.0.31 (februar 2023)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Commerce 10.0.31.
author: josaw1
ms.date: 10/18/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-10-01
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 05ccd9794ffeba6a09d6fec0a57ffad2b59707ad
ms.sourcegitcommit: 87e75aa6af2c3280316d7d73eafa14a52353a5e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/21/2022
ms.locfileid: "9709862"
---
# <a name="preview-of-dynamics-365-commerce-10031-february-2023"></a>Forhåndsvisning av Dynamics 365 Commerce 10.0.31 (februar 2023)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Commerce, forhåndsversjon 10.0.31. Denne versjonen har et build-nummer 10.0.1406, og er tilgjengelig på følgende tidsplan:

- **Forhåndsversjon:** oktober 2022
- **Allmenn tilgjengelighet for versjon (selvoppdatering):** januar 2023
- **Allmenn tilgjengelighet for versjon (automatisk oppdatering):** februar 2023

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. Denne artikkelen kan være oppdatert for å inkludere funksjoner som ble lagt til i builden etter at denne artikkelen opprinnelig ble publisert.

| Funksjonsområde | Funksjon | Mer informasjon | Aktivert av   |
|---|---|---|---|
| Feilkoder | Commerce har innført standardiserte feilreferanser som inkluderes i elektroniske kanalkontrollfeil som presenteres for online-kunder.| [Feilkoder for kassemodul](../checkout-module-error-codes.md)  | Aktivert som standard |
| Betalinger | [Aktivere Apple Pay med Dynamics 365 Payment Connector for Adyen](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-apple-pay-dynamics-365-payment-connector-adyen)  | E-commerce-kunder kan bruke Apple Pay på handlekurv- og betalingssider når de bruker enheter eller nettlesere som støttes. | Valg for utvikler |
| Betalinger  |  Commerce har muligheten til å begrense hvordan brukere samhandler med regelmessige betalingstokenter i brukergrensesnittet for Commerce Headquarters. Betalingsskjemaer, for eksempel siden **Telefonsenter-salgsordrer**, viser ikke lenger kundens tidligere brukte regelmessige betalingstoken for bruke i en ny transaksjon. Bare fastslått kort i fil-inndata på Commerce-skjermen **Kundebetalinger**, eller med avtale med en kunde under betaling via en salgsordre, vil bli presentert for samtalesentret eller Commerce headquarters-brukerne når de behandler en betaling for en ny transaksjon. | [Begrense bruk av betalingstoken](../dev-itpro/limit-token-usage.md)  |  Funksjonsbehandling<p>*Begrens bruk av betalingstoken til ordrekontekst*  |
| Salgssted | [Opprette fra bestillinger fra salgssenter](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/create-purchase-orders-pos)  |  Med Forbedret inngående lageroperasjon på salgssted kan brukere opprette, redigere og bekrefte bestillingsforespørsler. |  Funksjonsbehandling<p>*Mulighet til å opprette bestillingsforespørsel på salgsstedet*   |



## <a name="additional-resources"></a>Tilleggsressurser

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformoppdateringer for økonomi- og driftsapper

Microsoft Dynamics 365 Commerce 10.0.31 inkluderer plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.31 av økonomi- og driftsapper (februar 2023)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-31.md). 
  

### <a name="bug-fixes"></a>Feilrettinger

Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av versjon 10.0.31, logger du på Microsoft Dynamics Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=758525).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 og bransjeskyer: plan for lanseringsbølge 2 for 2022

Er du spent på kommende og nylig utgitte tilleggspakkefunksjoner i våre bedriftsprogrammer eller -plattform?

Sjekk ut [Dynamics 365 og bransjeskyer: plan for lanseringsbølge 2 for 2022](/dynamics365-release-plan/2022wave2/). Vi har registrert alle detaljene, ende til ende, øverst til nederst, i et enkelt dokument som du kan bruke i planleggingen.

### <a name="removed-and-deprecated-commerce-features"></a>Fjernede og utskrevete Commerce-funksjoner

Artikkelen [Funksjoner som er fjernet eller avskrevet i Dynamics 365 Commerce](removed-deprecated-features-commerce.md) beskriver funksjoner som er fjernet eller avskrevet for Commerce.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Før en funksjon fjernes fra produktet, vil avskrivningsvarselet bli kunngjort i artikkelen [Fjernede eller avskrevne funksjoner i Dynamics 365 Commerce](removed-deprecated-features-commerce.md) 12 måneder før fjerningen.


For oppdelingsendringer som bare påvirker kompileringstiden, men som er binære kompatible med sandkasse- og produksjonsmiljøer, vil avskrivningstiden være mindre enn 12 måneder. Dette er vanligvis funksjonelle oppdateringer som må gjøres på kompilatoren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

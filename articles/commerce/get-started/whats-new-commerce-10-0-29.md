---
title: Forhåndsversjon av Dynamics 365 Commerce 10.0.29 (oktober 2022)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Commerce 10.0.29.
author: josaw1
ms.date: 08/02/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: c1f85fcd8f79106a3af93489d3bef608b9840bf3
ms.sourcegitcommit: 91f58a9863f4e8f30ac787c2a9771c1ff6a05f72
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/03/2022
ms.locfileid: "9224245"
---
# <a name="preview-of-dynamics-365-commerce-10029-october-2022"></a>Forhåndsversjon av Dynamics 365 Commerce 10.0.29 (oktober 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Commerce, forhåndsversjon 10.0.29. Denne versjonen har et build-nummer 10.0.1326, og er tilgjengelig på følgende tidsplan:

- **Forhåndsversjon:** august 2022
- **Allmenn tilgjengelighet for versjon (selvoppdatering):** september 2022
- **Allmenn tilgjengelighet for versjon (automatisk oppdatering):** oktober 2022

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. Denne artikkelen kan være oppdatert for å inkludere funksjoner som ble lagt til i builden etter at denne artikkelen opprinnelig ble publisert.

| Funksjonsområde | Funksjon | Mer informasjon | Aktivert av   |
|---------|------------------|----------------|--------------| 
| B2B | [Aktiver støtte for salgsavtaler på tvers av kanaler](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-b2b-sales-agreement-contract-based-pricing) | Ved hjelp av denne funksjonen kan selgerorganisasjoner (B2B) bruke salgsavtaler i Commerce headquarters til å definere kontraktbasert prissetting for kjøperne. Når et B2B-kjøperbutikker på nettstedet for netthandel, brukes den kontraktbaserte prissettingen som er konfigurert for B2B-kjøperorganisasjonen, automatisk for hele produktoppdagelses-, innkjøps- og betalingserfaringen. | Funksjonsbehandling<p>*Støtte for salgsavtaler på tvers av handelskanaler* |
| Customer Service | [Aktiver Customer Service med Dynamics 365 Omnikanal for Customer Service](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/chat-dynamics-365-commerce-omnichannel-customer-service) | En førsteklasses kundestøtteerfaring er nøkkelen for å gi en personlig og trivelig handelsopplevelse for kunder. Det finnes flere kontaktpunkter for handel, for eksempel fysiske butikker, nettkanaler og sosiale kanaler. Kunder forventer en tilpasset støtteopplevelse i alle disse kontaktpunktene. Ved hjelp av denne funksjonen kan du øke handlekurvkonverteringen til salg, øke personlig kontakt med forbrukere og forbedre kundeservicen ved å integrere med Dynamics 365 Omnikanal for Customer Service. | Aktivert av administratorer/utviklere |
| E-handel | Støtte for produktsammenligning i netthandel | Gjør det mulig for kunder å sammenligne produkter i en rekke kategorier slik at de kan ta riktige kjøpsbeslutninger for seg selv. Denne funksjonen er tilgjengelig for både bedrift-til-kunde-områder (B2C) og B2B-områder. | Områdebygger | 
| Gavekort | Støtte for handelsgavekorttabeller for deling av data på tvers av firmaer | Dynamics headquarters støtter muligheten til å aktivere datadeling på tvers av firmaer for bestemte tabeller i Dynamics-arkitekturen. I denne funksjonen legger Dynamics 365 Commerce til støtte for deling av data på tvers av firmaer for handelsgavekorttabeller. Derfor kan et gavekort i ett firma nå duplisere dataene til et annet firma i miljøet. Endringer som gjøres i den opprinnelige firmagavekorttabellen, vil bli delt til den dupliserte firmagavekorttabellen. | Utviklere |
| Ytelse | Fjern RTS-avhengighet for scenarioer med rediger kunde | Høy tilgjengelighet og høy ytelse er standardforventninger for salgssteds- og netthandelskanaler. For å oppfylle disse forventningene trenger ikke Dynamics 365 Commerce-kanaler lenger å være avhengig av kommunikasjon i sanntid med Commerce headquarters når kundeinformasjonen redigeres. Muligheten til å redigere kundeinformasjon asynkron for asynkrone og ikke-asynkrone kunder kan bidra til å redusere samtaler i sanntid til Commerce headquarters. | Aktivert av administratorer/utviklere |

## <a name="feature-state-changes-in-this-release"></a>Endringer av funksjonstilstand i denne versjonen

Denne tabellen viser funksjoner som er blitt obligatoriske eller som er aktivert som standard, i versjon 10.0.29. Alle disse funksjonene aktiveres automatisk for systemet så snart du oppdaterer til versjon 10.0.29. Obligatoriske funksjoner kan ikke slås av, men funksjoner som er på som standard, kan fremdeles slås av ved hjelp av [Funksjonsadministrasjon](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tabellen viser også funksjoner som tidligere var i forhåndsversjon, men som er endret til å bli generelt tilgjengelig i versjon 10.0.29. Denne endringen angir at funksjonene nå anbefales for bruk i produksjonsmiljøer. Disse funksjonene er deaktivert som standard med mindre annet er nevnt. Derfor må du bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) for å aktivere dem hvis du vil bruke dem.

| Funksjon | Tittel | Ny funksjonstilstand |
| --- | --- | --- |
| BrazilRetailLocalizationFeature_BR |(Brasil) Handelsfunksjonalitet som er spesifikk for Brasil | Aktivert som standard |
| RetailAdvancedGTETaxAdjustmentFeature | (India) Bruk merverdiavgift beregnet for detaljhandelstransaksjoner i Retail POS til detaljhandelsoppgaver | Aktivert som standard |
| RetailChronologicalInvoicePostingFeature_IT | (Italia) Aktiver detaljhandelsfakturaer som er postert uten kronologisk rekkefølge | Aktivert som standard |
| RetailDiscountWithoutTaxAdjustingFeature_MX | (Mexico) Rabattjustering i global CFDI for detaljhandel | Aktivert som standard |
| RetailFiscalIntegrationConfigurationEnhancementFeature | Overstyringer av tekniske profiler for regnskapsintegrering | Aktivert som standard |
| RetailFiscalIntegrationConnectorLocationFeature | Direkte regnskapsintegrering fra kasser på salgssted | Aktivert som standard |
| RetailFiscalIntegrationLocalStorageBackupEnableFeature | Sikkerhetskopi av lokalt lager for regnskapsintegrering | Aktivert som standard |
| RetailFiscalIntegrationPostponeFiscalRegistrationFeature | Utsatt registrering av dokumenter | Aktivert som standard |
| RetailFiscalIntegrationRegistrationProcessTerminalExceptionFeature | Regnskapsregistreringstilstand for kasser på salgssted | Aktivert som standard |
| RetailGSTInvoiceAddressTaxCalculationFeature_IN | (India) Beregn GST basert på fakturaadresse for e-handelsordrer | Aktivert som standard |
| RetailInvoicesDefaultSalesDocumentStatusFeature_PL | (Polen) Standard salgsdokumentstatus for detaljhandelsfakturaer | Aktivert som standard |
| RetailRecalculateRoundingOfTaxBaseAmountsFeature_MX | (Mexico) Avrundingsomberegning for avgiftsgrunnlagsbeløp i global CFDI for Retail. | Aktivert som standard |
| RetailSupplementaryInvoiceFeature | Aktiver tilleggsfakturaer for hentesalgstransaksjoner fullført i detaljhandelsbutikker | Aktivert som standard |
| RetailInventoryBufferAndInventoryLevelEnableFeature   |  Aktiver lagerbuffere og lagernivåer    |  Aktivert som standard|
|RetailInboundOutboundInventoryValidationFeature|   Aktiver validering i innkommende og utgående lageroperasjoner for salgssted   |   Aktivert som standard   |
|  RetailInventoryChannelCalculationConsolidationFeature    |  Forbedret lagerberegningslogikk for netthandelkanalsiden |   Aktivert som standard   |
|RetailInventoryAdjustmentsInPointOfSaleFeature|    Lagerjusteringer på salgssted   |  Aktivert som standard  |
| RetailMultiplePickupDeliveryModeFeature |  Støtte for flere henteleveringsmåter     |   Obligatorisk    |
|  RetailProductAvailabilityOptimizationFeature |   Optimalisert beregning av produkttilgjengelighet  |  Obligatorisk |
|   RetailPricingDataManagerV2Feature   |   Forbedre ytelsen for Commerce-prismotor |   Obligatorisk |
|  RetailPricingPreventUnintendedRecalculationFeature   | Forhindre utilsiktet prisberegning for handelsordrer    |  Obligatorisk  |
| RetailTeamsIntegration    |   Aktiver Microsoft Teams-integrering| Obligatorisk   |  
| ConsumerEFDSyncProcessFeature_BR | (Brasil) Synkron behandling av NFC-e | Aktivert som standard |
| RetailFiscalIntegrationInternalAndExternalServicesEnableFeature | Støtte for interne og eksterne koblinger i rammeverket for regnskapsintegrering | Obligatorisk |
| RetailTaxRegistrationIdEnableFeature_BR | (Brasil) Søk etter kunder i Retail POS etter avgiftsregistreringsnumre | Obligatorisk |
| RetailTaxRegistrationIdEnableFeature_IN | (India) Søk etter kunder i Retail POS etter avgiftsregistreringsnumre | Obligatorisk |
| RetailTaxRegistrationIdEnableFeature_IT | (Italia) Behandling av kundeopplysninger i Retail POS | Obligatorisk |
| RetailTaxRegistrationIdEnableFeature_PL | (Polen) Behandling av kundeopplysninger i Retail POS | Obligatorisk |
| RetailUpdateReturnOriginalTransactionIdGlobalEnableFeature_IN | (Merverdiavgift for detaljhandel for India) Oppdater kreditnotaer med referanser til opprinnelige fakturaer | Obligatorisk |
| RetailUserDefinedCertificateProfileFeature | Brukerdefinerte sertifikatprofiler for detaljhandelsbutikker | Obligatorisk |
  

## <a name="additional-resources"></a>Tilleggsressurser

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformoppdateringer for økonomi- og driftsapper

Microsoft Dynamics 365 Commerce 10.0.29 inkluderer plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.29 av økonomi- og driftsapper (oktober 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md). 

### <a name="bug-fixes"></a>Feilrettinger

Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av versjon 10.0.29, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559&dbType=3&qc=ec3e3846199f5d3a27a0c4949e3902ffdbc87560f0cf928c4838b3bdd421633c). 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 og bransjeskyer: plan for lanseringsbølge 2 for 2022

Er du spent på kommende og nylig utgitte tilleggspakkefunksjoner i våre bedriftsprogrammer eller -plattform?

Sjekk ut [Dynamics 365 og bransjeskyer: plan for lanseringsbølge 2 for 2022](/dynamics365-release-plan/2022wave2/). Vi har registrert alle detaljene, ende til ende, øverst til nederst, i et enkelt dokument som du kan bruke i planleggingen.

### <a name="removed-and-deprecated-features"></a>Funksjoner som er fjernet og avskrevet

Artikkelen [Funksjoner som er fjernet eller avskrevet i Dynamics 365 Commerce](removed-deprecated-features-commerce.md) beskriver funksjoner som er fjernet eller avskrevet for Commerce.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Før en funksjon fjernes fra produktet, vil avskrivningsvarselet bli kunngjort i artikkelen [Fjernede eller avskrevne funksjoner i Dynamics 365 Commerce](removed-deprecated-features-commerce.md) 12 måneder før fjerningen.

For oppdelingsendringer som bare påvirker kompileringstiden, men som er binære kompatible med sandkasse- og produksjonsmiljøer, vil avskrivningstiden være mindre enn 12 måneder. Dette er vanligvis funksjonelle oppdateringer som må gjøres på kompilatoren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Forhåndsversjon av Dynamics 365 Supply Chain Management 10.0.17 (april 2021)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Supply Chain Management 10.0.17.
author: kamaybac
manager: annbe
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 985879ef765bf3074387a909d508f0f93a4771ed
ms.sourcegitcommit: d7c18228256daeefbf6518c3ef82fed4f7dbc161
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571818"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10017-april-2021"></a>Forhåndsversjon av Dynamics 365 Supply Chain Management 10.0.17 (april 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management-forhåndsversjonen 10.0.17. Denne versjonen har et build-nummer 10.0.761, og er tilgjengelig som følger:

- **Forhåndsversjon:** februar 2021
- **Allmenn tilgjengelighet av versjon (selvoppdatering):** mars 2021
- **Allmenn tilgjengelighet av versjon (automatisk oppdatering):** april 2021

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne versjonen inneholder følgende funksjoner: Noen av funksjonene i listen er fortsatt i forhåndsversjon, mens andre kanskje allerede er allment tilgjengelige. Følg koblingene til [frigivelsesplanen](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) for å se de offisielle frigivelsesdatoene for hver funksjon.

De fleste av disse funksjonene må aktiveres ved hjelp av [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) før du kan bruke dem.

### <a name="asset-management"></a>Ressursbehandling

- [Bruk regler for gruppering av arbeidsordrer mens en vedlikeholdsplan kjører](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/apply-rules-grouping-work-orders-while-running-maintenance-plan)<br> - Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsordrer](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md).

- [Fakturere kunder for vedlikeholdsarbeid](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/bill-customers-maintenance-work)<br> - Hvis du vil ha mer informasjon, kan du se [Fakturere for vedlikehold av aktiva som eies av kunden](../asset-management/integration-to-project-management-and-accounting/customer-billing.md).

- [Planlegge vedlikehold basert på akkumulerte aktivatellerverdier](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/plan-maintenance-based-accumulated-asset-counter-values)<br> - Hvis du vil ha mer informasjon, kan du se [Vedlikeholdsplaner](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md).

### <a name="inventory-and-logistics"></a>Lager og logistikk

- [Integreringsrammeverk for materialhåndteringsutstyr for automatiserte lagerprosesser (tidligere MHAX)](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/integration-framework-material-handling-equipment-automated-warehouse-processes-previously-mhax)<br> - Hvis du vil ha mer informasjon, kan du se [Grensesnitt for materialhåndteringsutstyr (MHAX)](../warehousing/mhax.md).

- [Landingskostnad](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/landed-cost)<br> - Hvis du vil ha mer informasjon, kan du se [Modulen Netto innkjøpspris](../landed-cost/landed-cost-overview.md).

- [Pakking i forhold til lagringsdimensjoner](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/packing-vs.-storage-dimensions)<br> - Hvis du vil ha mer informasjon, kan du se [Angi ulike dimensjoner for pakking og lagring](../warehousing/packing-vs-storage-dimensions.md).

- [Lagrede visninger for lager og logistikk](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-inventory-logistics)<br> - Hvis du vil ha mer informasjon, kan du se [Standard lagrede visninger for Supply Chain Management](saved-views-scm.md).

- [Planlegge opprettelse av lagerarbeid](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-warehouse-work-creation)<br> - Hvis du vil ha mer informasjon, kan du se [Planlegge arbeidsopprettelse under bølge](../warehousing/configure-wave-schedule-work-creation.md).

- [Angi standard finansdimensjoner for revalueringsbilag for standardkostnad for lager](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/set-default-financial-dimensions-inventory-standard-cost-revaluation-vouchers)<br> - Hvis du vil ha mer informasjon, kan du se [Behandle oppdateringer av standardkostnad](../cost-management/manage-standard-cost-updates.md).

- [Forsendelse av småpakker](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/small-parcel-shipping-sps)<br> - Hvis du vil ha mer informasjon, kan du se [Forsendelse av småpakker](../warehousing/small-parcel-shipping.md).

- [Lagerkjøring med skalaenheter i skyen](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-scale-units-cloud)<br> - Hvis du vil ha mer informasjon, kan du se [Arbeidsbelastninger for lagerstyring for sky- og kantskalaenheter](../cloud-edge/cloud-edge-workload-warehousing.md) og [Lagerordrer for sky- og kantskalaenheter](../cloud-edge/cloud-edge-warehouse-order.md).

- [Mobilappen Lagerstyring](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application)<br> - Hvis du vil ha mer informasjon, kan du se [Installere og koble til brukerinnstillingene for lagerstyring](../warehousing/install-configure-warehouse-management-app.md) og [Brukerinnstillinger for mobil enhet](../warehousing/mobile-device-user-settings.md).

### <a name="manufacturing"></a>Produksjon

- [Funksjoner for aktivastyring i grensesnittet for produksjonsutførelse](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/asset-management-capabilities-production-floor-execution-interface)<br> - Hvis du vil ha mer informasjon, kan du se [Hvordan arbeidere bruker grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-use.md).

- [Overstyre standard reserveringsprinsipp for materialer i produksjon](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/override-default-reservation-principle-materials-production)<br> - Hvis du vil ha mer informasjon, kan du se [Overstyre standard reserveringsprinsipp for materialer i produksjon](../production-control/override-default-reservation-principle.md).

- [Lagrede visninger for produksjonskontroll](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-production-control)<br> - Hvis du vil ha mer informasjon, kan du se [Standard lagrede visninger for Supply Chain Management](saved-views-scm.md).

- [Produksjonsutførelse med skalaenheter i skyen](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-scale-units-cloud)<br> - Hvis du vil ha mer informasjon, kan du se [Arbeidsbelastninger for produksjonsutførelse for sky- og kantskalaenheter](../cloud-edge/cloud-edge-workload-manufacturing.md).

### <a name="planning"></a>Planlegging

- [Støtte for dekningshorisont for planleggingsoptimalisering](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/coverage-time-fence-support-planning-optimization)<br> - Hvis du vil ha mer informasjon, kan du se [Dekningshorisonter](../master-planning/planning-optimization/coverage-time-fence.md).

- [Støtte for prognoseundermodell for Planleggingsoptimalisering](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/forecast-submodel-support-planning-optimization)<br> - Hvis du vil ha mer informasjon, kan du se [Hovedplanlegging med behovsprognoser](../master-planning/planning-optimization/demand-forecast.md).

- [Støtte for innkjøpsrekvisisjon for planleggingsoptimalisering](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/purchase-requisition-support-planning-optimization)<br> - Hvis du vil ha mer informasjon, kan du se [Innkjøpsrekvisisjoner](../master-planning/planning-optimization/purchase-requisitions.md).

- [Lagrede visninger for planlagte bestillinger](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-planned-orders)<br> - Hvis du vil ha mer informasjon, kan du se [Standard lagrede visninger for Supply Chain Management](saved-views-scm.md).

### <a name="product-information-management"></a>Behandling av produktinformasjon

- [Aktiver endringsstyring på eksisterende produkter](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enable-change-management-existing-products)<br> - Hvis du vil ha mer informasjon, kan du se [Aktiver endringsstyring på eksisterende produkter](../engineering-change-management/change-management-existing-products.md).

## <a name="new-and-updated-documentation-resources"></a>Nye og oppdaterte dokumentasjonsressurser

Vi har nylig lagt til eller betydelig oppdatert følgende hjelpeemner. De er ikke nødvendigvis knyttet til de nye funksjonene som er lagt til for denne versjonen, som oppført i den forrige delen, men de kan hjelpe deg med å få mer ut av eksisterende funksjoner.

### <a name="cost-management"></a>Kostnadsstyring

- [Feilsøke kostnadsstyring](../cost-management/troubleshoot-costmanagement.md)

### <a name="asset-management"></a>Ressursbehandling

- [Konfigurere mobilt arbeidsområde for aktivabehandling](../asset-management/set-up-asset-management-mobile.md)

### <a name="inventory-and-logistics"></a>Lager og logistikk

- [Konfigurere produktfiltre for lagertransaksjoner](../warehousing/filters-and-filter-codes.md)

- [Delvis lokasjonssyklustelling](../warehousing/partial-location-cycle-counting.md)

- [Plukklinjegruppering](../warehousing/pick-line-grouping.md)

- [Feilsøke lageroperasjoner](../inventory/troubleshoot-inventory-operations.md)

- [Lagersporing](../warehousing/warehouse-slotting.md)

### <a name="manufacturing"></a>Produksjon

- [Utforme grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-tabs.md)

### <a name="planning"></a>Planlegging

- [Konsernintern planlegging](../master-planning/planning-optimization/Intercompany-planning.md)

- [Lagermerking med planleggingsoptimalisering](../master-planning/planning-optimization/marking.md)

- [Produksjonsplanlegging](../master-planning/planning-optimization/production-planning.md)

- [Innkjøpsrekvisisjoner i hovedplanlegging](../master-planning/planning-optimization/purchase-requisitions.md)

## <a name="additional-resources"></a>Tilleggsressurser

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattformoppdateringer for Finance and Operations-apper

Microsoft Dynamics 365 Supply Chain Management 10.0.17 inkluderer plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.17 av Finance and Operations-apper (april 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md).

### <a name="bug-fixes"></a>Feilrettinger

Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av 10.0.17, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=551039&dbType=3&qc=91219e7c3fc585acb17b810c915c3cbea499403538520c40e54de43a53aea6a8).

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021-frigivelsesbølge 1-planen

Er du spent på kommende og nylig utgitte tilleggspakkefunksjoner i våre bedriftsprogrammer eller -plattform?

Se [Dynamics 365: 2021-frigivelsesbølge 1-planen](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/). Vi har registrert alle detaljene, ende til ende, øverst til nederst, i et enkelt dokument som du kan bruke i planleggingen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og avskrevne funksjoner i Supply Chain Management

Emnet [Fjernede eller avskrevne funksjonene i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver funksjoner som er eller er planlagt å bli fjernet eller avskrevet for Supply Chain Management.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Før en funksjon fjernes fra produktet, vil avskrivningsvarselet bli kunngjort i emnet [Fjernede eller avskrevne funksjoner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder før fjerningen.

For oppdelingsendringer som bare påvirker kompileringstiden, men som er binære kompatible med sandkasse- og produksjonsmiljøer, vil avskrivningstiden være mindre enn 12 måneder. Dette er vanligvis funksjonelle oppdateringer som må gjøres på kompilatoren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
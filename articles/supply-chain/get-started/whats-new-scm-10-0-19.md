---
title: Forhåndsvisning av Dynamics 365 Supply Chain Management 10.0.19 (juli 2021)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Supply Chain Management 10.0.19.
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8bb4a7c8085b40ab3eca72675dbe7a3be412d8c1
ms.sourcegitcommit: 2eb7a9ae544f504155657c5c584cbac66c21dba4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2021
ms.locfileid: "5961687"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10019-july-2021"></a>Forhåndsvisning av Dynamics 365 Supply Chain Management 10.0.19 (juli 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management-forhåndsversjonen 10.0.19. Denne versjonen har et build-nummer 10.0.837, og er tilgjengelig som følger:

- **Forhåndsversjon:** april 2021
- **Allmenn tilgjengelighet av versjon (selvoppdatering):** Juni 2021
- **Allmenn tilgjengelighet av versjon (automatisk oppdatering):** Juli 2021

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. *Funksjon*-kolonnen gir koblinger til [frigivelsesplanen](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), der du kan se de offisielle frigivelsesdatoene for hver funksjon. Kolonnen *Mer informasjon* inneholder koblinger til tilknyttet dokumentasjon.

De fleste av disse funksjonene må aktiveres ved hjelp av [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) før du kan bruke dem. Noen av funksjonene i listen er fortsatt i forhåndsversjon, mens andre kanskje allerede er allment tilgjengelige.

| Funksjonsområde | Funksjon | Mer informasjon |
|---|---|---|
| Lager og logistikk | [Eksportoptimalisering av dataenhet for kontaktperson](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | *Ikke tilgjengelig* |
| Lager og logistikk | [Inkrementelle forbedringer for lagerutførelsesfunksjoner med vektenheter](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[Meldinger for meldingsprosessor](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[Lagerbeholdningsjustering](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[Skalaenheter for sky og kant for arbeidsbelastninger for lagerstyring](../cloud-edge/cloud-edge-workload-warehousing.md) |
| Lager og logistikk | [Oppslagsfunksjonalitet for Dokumentinnledning- og Dokumentkonklusjon-felt på salgstilbudsside](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | *Ikke tilgjengelig* |
| Lager og logistikk | [Lagerutførelse med skalenheter for kant på den egendefinerte maskinvaren](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [Distribuere skalenheter for kant på egendefinert maskinvare ved hjelp av LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Produksjon | [Produksjonsutførelse med skalenheter for kant på den egendefinerte maskinvaren](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [Distribuere skalenheter for kant på egendefinert maskinvare ved hjelp av LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Planlegging | Spørringsbasert autorisering av planlagt bestilling | [Autoriser planlagte ordrer](../master-planning/planning-optimization/planned-order-firming.md) |
| Behandling av produktinformasjon | [Sideforbedringer for variantforslag](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [Opprette forhåndsdefinerte produktvarianter](../pim/tasks/create-predefined-product-variants.md) |

## <a name="new-and-updated-documentation-resources"></a>Nye og oppdaterte dokumentasjonsressurser

Vi har nylig lagt til eller betydelig oppdatert følgende hjelpeemner. De er ikke nødvendigvis knyttet til de nye funksjonene som er lagt til for denne versjonen, som oppført i den forrige delen, men de kan hjelpe deg med å få mer ut av eksisterende funksjoner.

| Funksjonsområde | Nye eller oppdaterte emner |
|---|---|
| Styring av teknisk endring | [Vanlige spørsmål for styring av teknisk endring](../engineering-change-management/change-management-faq.md) |
| Innkjøp og leverandører | [Kategoriforespørsler fra leverandører](../procurement/category-requests-from-vendors.md) |
| Behandling av produktinformasjon | [Administrere måleenhet](../pim/tasks/manage-unit-measure.md)<br><br>[Beregninger for produktkonfigurasjonsmodell](../pim/config-model-calculations.md) |
| Produksjonskontroll | [Enhetlig nummerserie for jobb-ID-er](../production-control/unified-job-ids.md) |
| Transportstyring | [LTL-klasser](../transportation/ltl-class.md)<br><br>[NMFC-koder](../transportation/nmfc-codes.md) |
| Lagerstyring | [Feilsøke lagerparti- og seriereserveringshierarkier](../warehousing/troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md) |
| Lagerstyring, bølgeoppretting og -behandling | [Bølgeoppretting og -behandling](../warehousing/wave-processing.md)<br><br>[Lagerparametere for bølgebehandling](../warehousing/wave-warehouse-parameters.md)<br><br>[Bølgemaler](../warehousing/wave-templates.md)<br><br>[Bølgetildeling](../warehousing/wave-allocation-method.md)<br><br>[Planlegge oppretting av arbeidstid under bølge](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[Containerbruk](../warehousing/wave-containerization.md)<br><br>[Varslinger for bølgekjøring](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>Tilleggsressurser

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattformoppdateringer for Finance and Operations-apper

Microsoft Dynamics 365 Supply Chain Management 10.0.19 inkluderer plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Platformoppdateringer for versjon 10.0.19 av Finance and Operations-apper (juli 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md).

### <a name="bug-fixes"></a>Feilrettinger

Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av 10.0.19, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415).

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021-frigivelsesbølge 1-planen

Er du spent på kommende og nylig utgitte tilleggspakkefunksjoner i våre bedriftsprogrammer eller -plattform?

Se [Dynamics 365: 2021-frigivelsesbølge 1-planen](/dynamics365-release-plan/2021wave1/). Vi har registrert alle detaljene, ende til ende, øverst til nederst, i et enkelt dokument som du kan bruke i planleggingen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og avskrevne funksjoner i Supply Chain Management

Emnet [Fjernede eller avskrevne funksjonene i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver funksjoner som er eller er planlagt å bli fjernet eller avskrevet for Supply Chain Management.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Før en funksjon fjernes fra produktet, vil avskrivningsvarselet bli kunngjort i emnet [Fjernede eller avskrevne funksjoner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder før fjerningen.

For oppdelingsendringer som bare påvirker kompileringstiden, men som er binære kompatible med sandkasse- og produksjonsmiljøer, vil avskrivningstiden være mindre enn 12 måneder. Dette er vanligvis funksjonelle oppdateringer som må gjøres på kompilatoren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

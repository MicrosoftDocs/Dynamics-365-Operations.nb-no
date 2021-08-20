---
title: Hva er nytt eller endret i Dynamics 365 Supply Chain Management versjon 10.0.19 (juni 2021)
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
ms.openlocfilehash: c1930a47bc133c411a0e6054aa766322a261064a06ac4cec8dcdd12c126dc7cd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773543"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10019-june-2021"></a>Hva er nytt eller endret i Dynamics 365 Supply Chain Management versjon 10.0.19 (juni 2021)

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management, versjon 10.0.19. Denne versjonen har et build-nummer 10.0.837, og er tilgjengelig som følger:

- **Forhåndsversjon:** april 2021
- **Allmenn tilgjengelighet av versjon (selvoppdatering):** Juni 2021
- **Allmenn tilgjengelighet av versjon (automatisk oppdatering):** Juni 2021

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. *Funksjon*-kolonnen gir koblinger til [frigivelsesplanen](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), der du kan se de offisielle frigivelsesdatoene for hver funksjon. Kolonnen *Mer informasjon* inneholder mer informasjon og/eller koblinger til tilknyttet dokumentasjon.

De fleste av disse funksjonene må aktiveres ved hjelp av [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) før du kan bruke dem.

| Funksjonsområde | Funksjon | Mer informasjon |
|---|---|---|
| Lager&nbsp;og&nbsp;logistikk | [Godkjenn og lagre bankdetaljer sendt av en leverandør](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/approve-save-vendor-submitted-bank-details) | [Vedlikehold bankkontoinformasjon for leverandør](../../finance/accounts-payable/maintain-vendor-bank-info.md) |
| Lager og logistikk | [Eksportoptimalisering av dataenhet for kontaktperson](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | Når denne funksjonen er aktivert, vil ikke endringer i dem føre til at tilknyttede kontakter inkluderes i den neste trinnvise eksporten. Når denne funksjonen er deaktivert, vil endringer i dem føre til at tilknyttede kontakter inkluderes i den neste trinnvise eksporten. |
| Lager og logistikk | [Inkrementelle forbedringer for lagerutførelsesfunksjoner med vektenheter](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[Meldinger for meldingsprosessor](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[Lagerbeholdningsjustering](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[Skalaenheter for sky og kant for arbeidsbelastninger for lagerstyring](../cloud-edge/cloud-edge-workload-warehousing.md) |
| Lager og logistikk | [Oppslagsfunksjonalitet for Dokumentinnledning- og Dokumentkonklusjon-felt på salgstilbudsside](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Denne funksjonen legger til oppslagsfunksjonalitet for **Dokumentinnledning**- og **Dokumentkonklusjon**-feltene på **Salgstilbud**-siden.<br><br>Denne funksjonen er aktivert som standard. |
| Lager og logistikk | [Lagerutførelse med skalenheter for kant på den egendefinerte maskinvaren](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [Distribuere skalenheter for kant på egendefinert maskinvare ved hjelp av LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Produksjon | [Produksjonsutførelse med skalenheter for kant på den egendefinerte maskinvaren](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [Distribuer kantskalaenheter på egendefinert maskinvare ved hjelp av LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Planlegging | [Uendelig kapasitetsplanlegging for Planleggingsoptimalisering](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-infinite-capacity-support-planning-optimization) | Denne funksjonen aktiverer kapasitetsplanlegging med ubegrenset kapasitet for Planleggingsoptimalisering. Uten denne funksjonen får planlagte produksjonsordrer leveringstid fra leveringstiden for frigitte produkter, uansett planleggingshorisonten. |
| Planlegging | Spørringsbasert autorisering av planlagt bestilling | [Autoriser planlagte ordrer](../master-planning/planning-optimization/planned-order-firming.md) |
| Behandling av produktinformasjon | [Sideforbedringer for variantforslag](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [Opprett forhåndsdefinerte produktvarianter](../pim/tasks/create-predefined-product-variants.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Funksjonsforbedringer inkludert i denne versjonen

Denne tabellen viser funksjonsforbedringer i denne versjonen. Hvert av disse gir en trinnvis forbedring av en eksisterende funksjon. Siden de bare er forbedringer vises de ikke i [frigivelsesplanen](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). For å sikre at disse forbedringene ikke kommer i konflikt med eksisterende tilpasninger eller innstillinger, er imidlertid hver av dem slått av som standard (med mindre annet er angitt). Hvis du vil bruke noen av disse funksjonene, må du uttrykkelig aktivere dem i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funksjonsområde | Funksjons&nbsp;navn&nbsp; i funksjons&nbsp;behandling | Mer informasjon |
|---|---|---|
| Salg og markedsføring | Ytelsesforbedringer for salgshistorikkopprydding | Opprydding i salgshistorikk kan ta lang tid hvis det kjøres sjelden i miljøer med høyt volum på salgsoppdateringer. For å redusere varigheten og forbedre påliteligheten deler denne funksjonen opprydding i satsvis behandling som kjører i en begrenset varighet. Der det er mulig, vil databasefunksjoner utnyttes for å minimere låsing og unngå å slå sammen transaksjonstabeller under opprydding. |
| Salg og markedsføring | Oppdater Ønsket leveringsdato med Bekreftet dato for konserninterne ordrer | Ved hjelp av denne funksjonen kan du styre hva som skjer med feltverdiene for salgs- og innkjøpsdato ved bruk av konsernintern direktelevering. Du kan velge om systemet skal oppdatere ønskede datoer eller hoppe over oppdatering av dem. Hvis du hopper over oppdateringen, vil de ønskede datoene representere det kunden har bedt om. Hvis du aktiverer oppdatering, representerer de ønskede datoene (ved bruk av leveringsdatokontroll) bare i utgangspunktet hva kunden har bedt om. Leveringsdatokontroll, når en annen enn *Ingen*, vil overstyre det som opprinnelig ble forespurt. Du kan angi dette alternativet ved å bruke den nye innstillingen **Oppdater ønsket mottaksdato med Bekreftet dato** i innstillingene for den konserninterne leverandøren eller kunden.<br><br>Hvis funksjonen er deaktivert, overskrives den ønskede mottaksdatoen på opprinnelige salgsordrer basert på regelen for leveringsdatokontroll, men den ønskede forsendelsesdatoen vil bli værende som den er. |
| Lagerstyring | Rund antall ned til nærmeste salgsenhet ved frigivelse til lager | Denne funksjonen legger til et alternativ som kan begrense ordreantall ved frigivelse til lager. Når dette er aktivert, blir ordreantallet rundet ned til nærmeste hele salgsenhet, og ordrer som omfatter antall for mindre enn én salgsenhet, vil bli avvist for frigivelse. |
| Lagerstyring | Bølgemetoden Planlegg arbeidsopprettelse i hele organisasjonen | Når denne funksjonen aktiveres, vil bølgemetoden *Planlegg arbeidsoppretting* konfigureres til å kjøre parallelt på tvers av alle juridiske enheter. Flere tilleggsinnstillinger vil også bli påvirket. Hvis du vil ha all informasjon, kan du se [Planlegge arbeidsopprettelse under bølge](../warehousing/configure-wave-schedule-work-creation.md). |

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

Microsoft Dynamics 365 Supply Chain Management 10.0.19 inkluderer plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Platformoppdateringer for versjon 10.0.19 av Finance and Operations-apper (juni 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md).

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

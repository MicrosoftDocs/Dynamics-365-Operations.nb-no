---
title: Nyheter eller endringer i Dynamics 365 Supply Chain Management 10.0.21 (oktober 2021)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Supply Chain Management 10.0.21.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3f586a00943e23b458ede1470b353d7c018ba923
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500561"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10021-october-2021"></a>Nyheter eller endringer i Dynamics 365 Supply Chain Management 10.0.21 (oktober 2021)

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management, versjon 10.0.21. Denne versjonen har et build-nummer 10.0.960, og er tilgjengelig som følger:

- **Forhåndsversjon:** august 2021
- **Allmenn tilgjengelighet for versjon (selvoppdatering):** september 2021
- **Allmenn tilgjengelighet for versjon (automatisk oppdatering):** oktober 2021

## <a name="known-deployment-issue"></a>Kjent distribusjonsproblem

Når du distribuerer versjon 10.0.21 på IaaS, kan du få følgende distribusjonsvarsel:

**Advarselskode:** 95017

**Advarselsmelding:** Skript \[SetupDiagnostics\] mislyktes i utførelsen mot VM

Distribusjonen vil fungere med advarselen. Følgende kjente problemer kan imidlertid forekomme i Lifecycle Services (LCS):

- På siden **Miljøovervåking** vises ikke koblingen **Vis detaljert versjonsinformasjon**, så du kan ikke se de spesifikke versjonene av modulene som er installert i miljøet ditt. Uten disse dataene kan hurtigreparasjoner mislykkes fordi prosessen som gjelder disse metodene, bruker disse dataene til å kontrollere at forutsetningene for modulversjonen er oppfylt. Siden det ikke er mulig å bruke PEAP/Forhåndsversjon-build i produksjon eller ta i bruk hurtigreparasjoner, bør virkningen være minimal.
- Fanene **Ytelsesmåledata** og **Indeksanalyse** på siden **Miljøovervåking** under SQL Insights viser ingen data. Alle andre funksjoner for **Miljøovervåking** vil fungere etter hensikten.
- Siden **Fullstendig systemdiagnose** vil ikke være tilgjengelig. De tilknyttede dataene om statusen til nattlig innkrever kjører og problemer som oppdages av reglene, vises heller ikke.

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. *Funksjon*-kolonnen gir koblinger til [frigivelsesplanen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), der du kan se de offisielle frigivelsesdatoene for hver funksjon. Kolonnen *Mer informasjon* inneholder mer informasjon og/eller koblinger til tilknyttet dokumentasjon.

De fleste av disse funksjonene må aktiveres ved hjelp av [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) før du kan bruke dem.

| Funksjonsområde | Funksjon | Mer informasjon |
|---|---|---|
| Lager&nbsp;og&nbsp;logistikk | [Tillegget Globalt lagerregnskap for Dynamics 365 Supply Chain Management](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [Startside for globalt lagerregnskap](../global-inventory-accounting/global-inventory-accounting-home.md) |
| Lager&nbsp;og&nbsp;logistikk | [Poster lagerbeholdninger ved hjelp av koder som er koblet til motkontoer](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [Årsakskoder for lagertelling](../warehousing/reason-codes-for-counting-journals.md) |
| Lager&nbsp;og&nbsp;logistikk | [Eksportpolicy for data som salgstilbud henviser til](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | Velg om endringer i data som refereres av tilbud, vil føre til at disse tilbudene (eller linjene) skal inkluderes i den neste trinnvise eksporten. De trinnvise eksportene vil gå raskere hvis du velger ikke å ta med slike tilbud eller linjer.<br><br>Denne funksjonen legger til en innstilling kalt **Hopp over referansedata for salgstilbud under endringssporing** til siden **Kundeparametere**. |
| Lager&nbsp;og&nbsp;logistikk | Forseglet bud <!-- KFM: Add RP link when available --> | [Forseglede bud for tilbudsforespørsler](../procurement/sealed-bidding.md) |
| Lager&nbsp;og&nbsp;logistikk | [Skann strekkoder i lageret ved hjelp av standardene i GS1-format](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1-strekkoder og QR-koder](../warehousing/gs1-barcodes.md) |
| Lager&nbsp;og&nbsp;logistikk | [Ikke-forpliktende reservasjon for tillegget Lagersynlighet](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [Lagersynlighetsreservasjoner](../inventory/inventory-visibility-reservations.md) |
| Lager&nbsp;og&nbsp;logistikk | [Forbedringer i fradrag og faktisk vekt for Rabattbehandling](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Behandle fradrag med arbeidsområdet for fradrag](../rebate-management/deduction-workbench.md )<br><br>[Behandle, gjennomgå og postere rabatter](../rebate-management/process-review-post.md)<br><br>[Rabattbehandlingsavtaler](../rebate-management/rebate-management-deals.md) |
| Lager&nbsp;og&nbsp;logistikk | [Trinninstruksjoner for lagerapp](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Tilpass trinntitler og instruksjoner for mobilappen Warehouse Management](../warehousing/mobile-app-titles-instructions.md) |
| Lager&nbsp;og&nbsp;logistikk | [Arbeidspauser og sporingsoppdateringer for netto innkjøpspris](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Oppdateringssporing for plassering](../landed-cost/update-tracking-putaway.md )<br><br>[Behandling av varer i transitt](../landed-cost/in-transit-processing.md) |
| Hovedplanlegging | [Negative dager for Planleggingsoptimalisering](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Forsinkelsestoleranse (negative dager)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Funksjonsforbedringer inkludert i denne versjonen

Denne tabellen viser funksjonsforbedringer i denne versjonen. Hvert av disse gir en trinnvis forbedring av en eksisterende funksjon. Siden de bare er forbedringer vises de ikke i [frigivelsesplanen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). For å sikre at disse forbedringene ikke kommer i konflikt med eksisterende tilpasninger eller innstillinger, er imidlertid hver av dem slått av som standard (med mindre annet er angitt). Hvis du vil bruke noen av disse funksjonene, må du uttrykkelig aktivere dem i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funksjonsområde | Funksjons&nbsp;navn&nbsp; i funksjons&nbsp;behandling | Mer informasjon |
|---|---|---|
| Kostnadsstyring | Fremdriftsdetaljer for lagerlukking | Denne forhåndsversjonsfunksjonen gir en detaljert visning av fremdrift for lagerlukking. |
| Innkjøp og leverandører | Forhindre overforbruk av generelle budsjettreservasjoner når flere innkjøpsrekvisisjoner er i arbeidsflyt | Denne forhåndsversjonsfunksjonen forbedrer feilkontroll når brukere sender og godkjenner innkjøpsrekvisisjoner som overskrider den gjenværende saldoen til en generell budsjettreservasjonslinje. Dette forhindrer overforbruk av generelle budsjettreservasjoner når flere innkjøpsrekvisisjoner er i arbeidsflyten. |
| Produksjonskontroll | Vis fullstendige serie-, parti- og skiltnumre i grensesnittet for produksjonsutførelse | Denne funksjonen gir en forbedret erfaring for visning av lister over serie-, parti- og lisensnumre i grensesnittet for produksjonsutførelse. Visningsendringene fra en kortvisning med et begrenset antall tegn til en listevisning som gir nok plass til å vise de fullstendige verdiene. Listen gir også muligheten til å søke etter bestemte numre. |
| Salg og markedsføring | Begrens antall salgsordrer som kan velges for postering | Ved hjelp av denne funksjonen kan du definere maksimalt antall salgsordrer som kan velges ved postering av bekreftelser, plukklister, følgesedler og fakturaer fra listesiden for salgsordrer. Den aktiveres automatisk. Funksjonen legger til en innstilling kalt **Maks. antall salgsordrer for postering** på siden **Kundeparametere**. Den nye innstillingen har verdien *100* som standard. Funksjonen bidrar til å forbedre ytelsen på listesiden for salgsordrer når et betydelig antall salgsordrer velges. Den har ingen innvirkning på antall salgsordrer som kan behandles av en periodisk oppgave. |
| Lagerstyring | Koble plasseringsarbeid fra ASN-er | Denne funksjonen er nødvendig for å sende og forhåndsvarsler for forsendelse (ASN-er) når du kjører en lagerstyringsarbeidsbelastning på en skaleringsenhet (som en del av en distribuert hybridtopologi). Den legger til en ny databasetabell som er dedikert til å lagre informasjon om plasseringsarbeid. Tidligere ble denne informasjonen lagret i tabeller som også ble brukt for ASN-ene. |
| Lagerstyring | Blandede enheter for spor | Tillater at systemet sporer varer på lokasjoner som inneholder blandede enheter (for eksempel både bokser og kasser). For hver sporingsmallinje kan du bruke denne funksjonen til å velge om linjen skal lage varer i mellomenhets- eller enkeltenhetslokasjoner. |
| Lagerstyring | Bruk raskere API for containere som lukkes / åpnes på nytt på pakkestasjon | Når denne forhåndsversjonsfunksjonen er aktivert, opprettes det lagertransaksjoner relatert til containere ved hjelp av en ny lettvektsprosess som forbedrer ytelsen ved lukking eller åpning av containere på nytt under manuell behandling av emballasjematerialer. |

## <a name="new-and-updated-documentation-resources"></a>Nye og oppdaterte dokumentasjonsressurser

Vi har nylig lagt til eller betydelig oppdatert følgende hjelpeemner. De er ikke nødvendigvis knyttet til de nye funksjonene som er lagt til for denne versjonen, som oppført i den forrige delen, men de kan hjelpe deg med å få mer ut av eksisterende funksjoner.

| Funksjonsområde | Nye eller oppdaterte emner |
|---|---|
| Hovedplanlegging | [Lagerprognoser](../master-planning/inventory-forecast.md) |
| Hovedplanlegging | [Parametere som ikke brukes av planleggingsoptimalisering](../master-planning/planning-optimization/not-used-parameters.md) |
| Hovedplanlegging | [Etterfyllingsmetoder og antallsendring](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| Hovedplanlegging | [Planlegging med ubegrenset kapasitet](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Hovedplanlegging | [Vis planhistorikk og planleggingslogger](../master-planning/planning-optimization/plan-history-logs.md) |
| Lagerstyring | [Containerpakkestrategier](../warehousing/container-packing-strategy-overview.md) |
| Lagerstyring | [Eksempelscenarier for syklustelling](../warehousing/cycle-counting-scenarios.md) |
| Lagerstyring | [Importer innkommende forhåndsvarsler for forsendelse via V2-dataenheten](../warehousing/import-asn-v2-data-entity.md) |
| Lagerstyring | [Overplukking for salgs- og overføringsordrer](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| Lagerstyring | [Planlegg utskrift av bølgeetiketter under bølge](../warehousing/configure-task-based-wave-label-printing.md) |
| Lagerstyring | [Hva er nytt eller endret i mobilappen Warehouse Management](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>Tilleggsressurser

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattformoppdateringer for Finance and Operations-apper

Microsoft Dynamics 365 Supply Chain Management 10.0.21 inkluderer plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Platformoppdateringer for versjon 10.0.21 av Finance and Operations-apper (oktober 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

### <a name="bug-fixes"></a>Feilrettinger

Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av 10.0.21, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 og bransjeskyer: plan for lanseringsbølge 2 for 2021

Er du spent på kommende og nylig utgitte tilleggspakkefunksjoner i våre bedriftsprogrammer eller -plattform?

Sjekk ut [Dynamics 365 og bransjeskyer: plan for lanseringsbølge 2 for 2021](/dynamics365-release-plan/2021wave2/). Vi har registrert alle detaljene, ende til ende, øverst til nederst, i et enkelt dokument som du kan bruke i planleggingen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og avskrevne funksjoner i Supply Chain Management

Emnet [Fjernede eller avskrevne funksjonene i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver funksjoner som er eller er planlagt å bli fjernet eller avskrevet for Supply Chain Management.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Før en funksjon fjernes fra produktet, vil avskrivningsvarselet bli kunngjort i emnet [Fjernede eller avskrevne funksjoner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder før fjerningen.

For oppdelingsendringer som bare påvirker kompileringstiden, men som er binære kompatible med sandkasse- og produksjonsmiljøer, vil avskrivningstiden være mindre enn 12 måneder. Dette er vanligvis funksjonelle oppdateringer som må gjøres på kompilatoren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

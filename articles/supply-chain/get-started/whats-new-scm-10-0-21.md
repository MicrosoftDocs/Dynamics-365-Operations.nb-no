---
title: Nyheter eller endringer i Dynamics 365 Supply Chain Management 10.0.21 (oktober 2021)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Supply Chain Management 10.0.21.
author: kamaybac
ms.date: 10/28/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3b5f0c6947944ec875c30fa912f830f245b5a48e
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777943"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10021-october-2021"></a>Nyheter eller endringer i Dynamics 365 Supply Chain Management 10.0.21 (oktober 2021)

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management, versjon 10.0.21. Denne versjonen har et build-nummer 10.0.960, og er tilgjengelig som følger:

- **Forhåndsversjon:** august 2021
- **Allmenn tilgjengelighet for versjon (selvoppdatering):** september 2021
- **Allmenn tilgjengelighet for versjon (automatisk oppdatering):** oktober 2021

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. *Funksjon*-kolonnen gir koblinger til [frigivelsesplanen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), der du kan se de offisielle frigivelsesdatoene for hver funksjon. Kolonnen *Mer informasjon* inneholder mer informasjon og/eller koblinger til tilknyttet dokumentasjon.

De fleste av disse funksjonene må aktiveres ved hjelp av [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) før du kan bruke dem.

| Funksjonsområde | Funksjon | Mer informasjon |
|---|---|---|
| Lager&nbsp;og&nbsp;logistikk | [Tillegget Globalt lagerregnskap for Dynamics 365 Supply Chain Management](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [Startside for globalt lagerregnskap](../global-inventory-accounting/global-inventory-accounting-home.md) |
| Lager&nbsp;og&nbsp;logistikk | [Poster lagerbeholdninger ved hjelp av koder som er koblet til motkontoer](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [Årsakskoder for lagertelling](../warehousing/reason-codes-for-counting-journals.md) |
| Lager&nbsp;og&nbsp;logistikk | [Eksportpolicy for data som salgstilbud henviser til](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | Velg om endringer i data som refereres av tilbud, vil føre til at disse tilbudene (eller linjene) skal inkluderes i den neste trinnvise eksporten. De trinnvise eksportene vil gå raskere hvis du velger ikke å ta med slike tilbud eller linjer.<br><br>Denne funksjonen legger til en innstilling kalt **Hopp over referansedata for salgstilbud under endringssporing** til siden **Kundeparametere**. |
| Lager&nbsp;og&nbsp;logistikk | [Forseglet bud](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sealed-bidding) | [Forseglede bud for tilbudsforespørsler](../procurement/sealed-bidding.md) |
| Lager&nbsp;og&nbsp;logistikk | [Skann strekkoder i lageret ved hjelp av standardene i GS1-format](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1-strekkoder og QR-koder](../warehousing/gs1-barcodes.md) |
| Lager&nbsp;og&nbsp;logistikk | [Ikke-forpliktende reservasjon for tillegget Lagersynlighet](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [Lagersynlighetsreservasjoner](../inventory/inventory-visibility-reservations.md) |
| Lager&nbsp;og&nbsp;logistikk | [Forbedringer i fradrag og faktisk vekt for Rabattbehandling](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Behandle fradrag med arbeidsområdet for fradrag](../rebate-management/deduction-workbench.md )<br><br>[Behandle, gjennomgå og postere rabatter](../rebate-management/process-review-post.md)<br><br>[Rabattbehandlingsavtaler](../rebate-management/rebate-management-deals.md) |
| Lager&nbsp;og&nbsp;logistikk | [Trinninstruksjoner for lagerapp](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Tilpass trinntitler og instruksjoner for mobilappen Warehouse Management](../warehousing/mobile-app-titles-instructions.md) |
| Lager&nbsp;og&nbsp;logistikk | [Arbeidspauser og sporingsoppdateringer for netto innkjøpspris](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Oppdateringssporing for plassering](../landed-cost/update-tracking-putaway.md )<br><br>[Behandling av varer i transitt](../landed-cost/in-transit-processing.md) |
| Hovedplanlegging | [Negative dager for Planleggingsoptimalisering](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Forsinkelsestoleranse (negative dager)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Funksjonsforbedringer inkludert i denne versjonen

Denne tabellen viser funksjonsforbedringer i denne versjonen. Hvert av disse gir en trinnvis forbedring av en eksisterende funksjon. Siden de bare er forbedringer vises de ikke i [frigivelsesplanen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). For å sikre at disse forbedringene ikke kommer i konflikt med eksisterende tilpasninger eller innstillinger, er imidlertid hver av dem slått av som standard (med mindre annet er angitt). Hvis du vil bruke noen av disse funksjonene, må du uttrykkelig aktivere dem i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funksjons&nbsp;navn&nbsp; i funksjons&nbsp;behandling | Mer informasjon |
|---|---|---|
| Kostnadsstyring | Fremdriftsdetaljer for lagerlukking | Denne forhåndsversjonsfunksjonen gir en detaljert visning av fremdrift for lagerlukking. |
| Innkjøp og leverandører | Forhindre overforbruk av generelle budsjettreservasjoner når flere innkjøpsrekvisisjoner er i arbeidsflyt | Denne forhåndsversjonsfunksjonen forbedrer feilkontroll når brukere sender og godkjenner innkjøpsrekvisisjoner som overskrider den gjenværende saldoen til en generell budsjettreservasjonslinje. Dette forhindrer overforbruk av generelle budsjettreservasjoner når flere innkjøpsrekvisisjoner er i arbeidsflyten. |
| Produksjonskontroll | Vis fullstendige serie-, parti- og skiltnumre i grensesnittet for produksjonsutførelse | Denne funksjonen gir en forbedret erfaring for visning av lister over serie-, parti- og lisensnumre i grensesnittet for produksjonsutførelse. Visningsendringene fra en kortvisning med et begrenset antall tegn til en listevisning som gir nok plass til å vise de fullstendige verdiene. Listen gir også muligheten til å søke etter bestemte numre. |
| Salg og markedsføring | Begrens antall salgsordrer som kan velges for postering | Ved hjelp av denne funksjonen kan du definere maksimalt antall salgsordrer som kan velges ved postering av bekreftelser, plukklister, følgesedler og fakturaer fra listesiden for salgsordrer. Den aktiveres automatisk. Funksjonen legger til en innstilling kalt **Maks. antall salgsordrer for postering** på siden **Kundeparametere**. Den nye innstillingen har verdien *100* som standard. Funksjonen bidrar til å forbedre ytelsen på listesiden for salgsordrer når et betydelig antall salgsordrer velges. Den har ingen innvirkning på antall salgsordrer som kan behandles av en periodisk oppgave. |
| Lagerstyring | Koble plasseringsarbeid fra ASN-er | Denne funksjonen er nødvendig for å sende og forhåndsvarsler for forsendelse (ASN-er) når du kjører en lagerstyringsarbeidsbelastning på en skaleringsenhet (som en del av en distribuert hybridtopologi). Den legger til en ny databasetabell som er dedikert til å lagre informasjon om plasseringsarbeid. Tidligere ble denne informasjonen lagret i tabeller som også ble brukt for ASN-ene. |
| Lagerstyring | Blandede enheter for spor | Tillater at systemet sporer varer på lokasjoner som inneholder blandede enheter (for eksempel både bokser og kasser). For hver sporingsmallinje kan du bruke denne funksjonen til å velge om linjen skal lage varer i mellomenhets- eller enkeltenhetslokasjoner. |
| Lagerstyring | Bruk raskere API for containere som lukkes / åpnes på nytt på pakkestasjon | Når denne forhåndsversjonsfunksjonen er aktivert, opprettes det lagertransaksjoner relatert til containere ved hjelp av en ny lettvektsprosess som forbedrer ytelsen ved lukking eller åpning av containere på nytt under manuell behandling av emballasjematerialer. |

## <a name="features-turned-on-by-default-in-this-release"></a>Funksjoner som er aktivert som standard i denne versjonen

Denne tabellen viser funksjonene som er aktivert som standard i 10.0.21. De fleste funksjoner som er aktivert automatisk, kan slås av i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funksjonsnavn | Aktiveringsdato | Funksjon lagt til | Funksjonstilstand | Modul |
| :--- | :--- | :--- | :--- | :--- |
| Lagring av rapport for lagerbeholdning | 01.09.2021 | 01.04.2020 | Aktivert som standard | Lagerstyring |
| Annullering av overføringsordre | 01.09.2021 | 13.07.2020 | Aktivert som standard | Lagerstyring |
| Lås opp lagerjournal | 01.09.2021 | 17.08.2020 | Aktivert som standard | Lagerstyring |
| Lagrede visninger for lagerstyring | 01.09.2021 | 30.09.2020 | Aktivert som standard | Lagerstyring |
| Navigasjon til stykklisteversjon fra stykklistelinjer | 01.09.2021 | 11.11.2019 | Aktivert som standard | Lagerstyring |
| Bruker måleenhet og enhetsantall i lagerjournaler | 01.09.2021 | 11.11.2019 | Aktivert som standard | Lagerstyring |
| Tillat tomme verdier for partiattributter | 01.09.2021 | 11.11.2019 | Aktivert som standard | Lagerstyring |
| Øk linjenumre automatisk for ordrelinjer for lageroverføring | 01.09.2021 | 11.10.2019 | Aktivert som standard | Lagerstyring |
| Beholdningsjournal - godkjenn - arbeidsflyt | 01.09.2021 | 06.01.2020 | Aktivert som standard | Lagerstyring |
| Aktiver funksjon for advarsel om parametere for lagerkvalitetsstyring | 01.09.2021 | 07.10.2019 | Aktivert som standard | Lagerstyring |
| Opprett overføringsordre fra salgslinje | 01.09.2021 | 31.08.2019 | Aktivert som standard | Lagerstyring |
| Valg av prognosemodell i Detaljer om behovsprognose | 01.09.2021 | 11.10.2019 | Aktivert som standard | Hovedplanlegging |
| Visualisering av fremdrift for hovedplanlegging | 01.09.2021 | 07.10.2019 | Aktivert som standard | Hovedplanlegging |
| Automatisk autorisasjon for Planleggingsoptimalisering | 01.09.2021 | 11.10.2019 | Aktivert som standard | Hovedplanlegging |
| Parallell autorisasjon av planlagte ordrer | 01.09.2021 | 31.08.2019 | Aktivert som standard | Hovedplanlegging |
| Melding om vellykket sending av bud | 01.09.2021 | 15.05.2019 | Aktivert som standard | Innkjøp og leverandører |
| Referanse kobling for tilbudsforespørsel lagt til i bestilling | 01.09.2021 | 31.08.2019 | Aktivert som standard | Innkjøp og leverandører |
| Mulighet til satsvis bekreftelse av godkjente bestillinger fra leverandørsamarbeid | 01.09.2021 | 10.09.2019 | Aktivert som standard | Innkjøp og leverandører |
| Kjøp av cXML-forbedringer | 01.09.2021 | 11.11.2019 | Aktivert som standard | Innkjøp og leverandører |
| Vis koblingen &quot;Åpne publiserte tilbudsforespørsler&quot; som en flis | 01.09.2021 | 30.09.2020 | Aktivert som standard | Innkjøp og leverandører |
| Tilbudsforespørsel - spørsmål og svar | 01.09.2021 | 19.02.2020 | Aktivert som standard | Innkjøp og leverandører |
| Produktinformasjon og forsendelsesdokumentasjon for farlige materialer | 01.09.2021 | 14.06.2020 | Aktivert som standard | Behandling av produktinformasjon |
| Streng validering av standard ordreantall | 01.09.2021 | 24.06.2020 | Aktivert som standard | Behandling av produktinformasjon |
| Administrasjon av opprinnelsesland - funksjon | 01.09.2021 | 13.07.2020 | Aktivert som standard | Behandling av produktinformasjon |
| Lagrede visninger for frigitte produkter | 01.09.2021 | 30.09.2020 | Aktivert som standard | Behandling av produktinformasjon |
| Forbedringer i dialogboksene Godkjenn og Overfør jobber | 01.09.2021 | 11.10.2019 | Aktivert som standard | Produksjonskontroll |
| Nummerskilt for ferdigmelding lagt til i jobbkortenheten | 01.09.2021 | 31.08.2019 | Aktivert som standard | Produksjonskontroll |
| Den nye knappen Stopp pause er lagt til på siden Jobbkortterminal | 01.09.2021 | 19.02.2020 | Aktivert som standard | Produksjonskontroll |
| Aktiver delvis mottak av underleveransevarer, og rett opp et problem med beregning av svinn for stykklistelinjer av typen Leverandør. | 01.09.2021 | 11.11.2019 | Aktivert som standard | Produksjonskontroll |
| Lagrede visninger for produksjonskontroll | 01.09.2021 | 17.08.2020 | Aktivert som standard | Produksjonskontroll |
| Dynamics 365 Guides for Produksjon | 01.09.2021 | 13.07.2020 | Aktivert som standard | Produksjonskontroll |
| Produksjonsutførelse | 01.09.2021 | 30.09.2020 | Aktivert som standard | Produksjonskontroll |
| Funksjon for låsing av jobbkortenheten og jobbkortterminal slik at de kan rengjøres | 01.09.2021 | 10.05.2020 | Aktivert som standard | Produksjonskontroll |
| Gebyrtildeling i en salgsordre | 01.09.2021 | 30.09.2020 | Aktivert som standard | Salg og markedsføring |
| Begrens antall salgsordrer som kan velges for postering | 01.09.2021 | 01.09.2021 | Aktivert som standard | Salg og markedsføring |
| Rydd opp i oppdateringshistorikk for salgsordre | 01.09.2021 | 01.09.2021 | Aktivert som standard | Salg og markedsføring |
| Endre nummerserien for syklustellingsarbeid | 01.09.2021 | 07.10.2019 | Aktivert som standard | Lagerstyring |
| Etterfylling av oppgavebasert bølgebehov | 01.09.2021 | 07.10.2019 | Obligatorisk | Lagerstyring |
| Skjul feltet Total verdi på &quot;Alle laster&quot; og &quot;Lastdetaljer&quot;-sidene | 01.09.2021 | 07.10.2019 | Aktivert som standard | Lagerstyring |
| Bølgeetikettutskrift | 01.09.2021 | 19.02.2020 | Obligatorisk | Lagerstyring |
| Knytt bestillingsbeholdningstransaksjoner til belastning | 01.09.2021 | 06.01.2020 | Obligatorisk | Lagerstyring |
| Forbedrede oppsett for nummerskiltetikett | 01.09.2021 | 19.02.2020 | Aktivert som standard | Lagerstyring |
| Organisasjonsomfattende arbeidsblokkering | 01.09.2021 | 19.02.2020 | Obligatorisk | Lagerstyring |
| Detaljer for arbeidslinje | 01.09.2021 | 11.10.2019 | Aktivert som standard | Lagerstyring |
| Gjør lagerstatusfeltet for den mobile enhetsbeholdningen redigerbart | 01.09.2021 | 16.10.2019 | Aktivert som standard | Lagerstyring |
| Bekreft utgående forsendelser fra satsvise jobber | 01.09.2021 | 13.07.2020 | Aktivert som standard | Lagerstyring |
| Kontroller om en sammendragsside for mottak skal vises på mobilenheter | 01.09.2021 | 01.04.2020 | Aktivert som standard | Lagerstyring |
| Spør om å løse tvetydige &#39;Lok./nr.skilt&#39; navn | 01.09.2021 | 01.04.2020 | Aktivert som standard | Lagerstyring |
| Registrer produktvarianter og sporingsdimensjoner i lagerappen under mottak av lastvare | 01.09.2021 | 10.05.2020 | Aktivert som standard | Lagerstyring |
| Ikke tillat oppretting av laster som ikke oppfyller kravene i malen for lastplanbygging for bølge. | 01.09.2021 | 17.08.2020 | Aktivert som standard | Lagerstyring |
| Evaluer alle handlinger for lokasjonsdirektiver med flere SKU-er | 01.09.2021 | 30.09.2020 | Aktivert som standard | Lagerstyring |

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

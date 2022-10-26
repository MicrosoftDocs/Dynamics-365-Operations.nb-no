---
title: Forhåndsversjon av Dynamics 365 Supply Chain Management 10.0.29 (oktober 2022)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management 10.0.29.
author: kamaybac
ms.date: 08/12/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 62e06f2348ca3524beaaef5d8879c199db56696f
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689290"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10029-october-2022"></a>Nyheter eller endringer i Dynamics 365 Supply Chain Management 10.0.29 (oktober 2022)

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management, versjon 10.0.29. Denne versjonen har et build-nummer 10.0.1326, og er tilgjengelig på følgende tidsplan:

- **Forhåndsversjon:** august 2022
- **Allmenn tilgjengelighet for versjon (selvoppdatering):** september 2022
- **Allmenn tilgjengelighet for versjon (automatisk oppdatering):** oktober 2022

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. Denne artikkelen kan være oppdatert for å inkludere funksjoner som ble lagt til i builden etter at denne artikkelen opprinnelig ble publisert.

| Funksjonsområde | Funksjon | Mer informasjon | Aktivert av   |
|---|---|---|---|
| Lager og logistikk | [Tildel og reserver WMS-varer i lagersynlighet](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/allocate-reserve-whs-items-inventory-visibility) | Kommer snart | Aktivert som standard |
| Lager og logistikk | [Forhåndslast effektive lagerbeholdningslister](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/query-inventory-visibility-summary-entity) | [Bruk Inventory Visibility-appen](../inventory/inventory-visibility-power-platform.md) | Aktivert av tjenestekonfigurasjon |
| Forsyningsautomatisering for produser til ordre | [Automatisering av produksjon etter ordre](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-to-order-supply-automation) | [Automatisering av produksjon etter ordre](../master-planning/make-to-order-supply-automation.md) | Funksjonsbehandling:<br>*Automatisering av produksjon etter ordre* |
| Planlegging | [Vis og bruk detaljerte innsikter for etterspørselsdrevet planlegging av materialkrav](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/view-apply-detailed-insights-ddmrp) | [Oversikt over etterspørselsdrevet planlegging av materialkrav](../master-planning/planning-optimization/ddmrp-overview.md) | Funksjonsbehandling:<br>*(Forhåndsversjon) DDMRP for planleggingsoptimalisering* |
| Produksjonskontroll | [Gjør ferdigvarer fysisk tilgjengelige før postering til journaler](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-finished-goods-physically-before-posting) | [Gjør ferdigvarer fysisk tilgjengelige før postering til journaler](../production-control/deferred-posting.md) | Funksjonsbehandling:<br>*(Forhåndsversjon) Gjør ferdigvarer fysisk tilgjengelige før postering til journaler* |
| Lagerstyring | [Slå opp relevante data i Warehouse Mobile App](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/look-up-relevant-data-within-warehouse-mobile-app) | [Spør data med Warehouse Management-mobilappomveier](../warehousing/warehouse-app-data-inquiry.md) | Funksjonsbehandling:<br>*Dataforespørselsflyt i Warehouse Management-appen* |

## <a name="feature-enhancements-included-in-this-release"></a>Funksjonsforbedringer inkludert i denne versjonen

Denne tabellen viser funksjonsforbedringer i denne versjonen. Hvert av disse forbedringene gir en trinnvis forbedring av en eksisterende funksjon. Siden de bare er forbedringer vises de ikke i [frigivelsesplanen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). For å sikre at disse forbedringene ikke kommer i konflikt med eksisterende tilpasninger eller innstillinger, er imidlertid hver av dem slått av som standard (med mindre annet er angitt).

Hvis du vil slå noen av disse funksjonene på eller av, må du gjøre dette i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funksjonsnavn i funksjonsbehandling | Mer informasjon |
|---|---|---|
| Kostnadsstyring | Optimalisering av beregning av pris for koprodukt som venter | Denne funksjonen retter opp en konflikt som noen ganger kan oppstå når koproduktpriser beregnes ved å bruke flere tråder. Det fører til at systemet kontrollerer at hver koproduktpris beregnes bare én gang. Resultatet av denne beregningen brukes deretter som inndata for alle andre beregninger. Hvis det allerede finnes en ventende pris, brukes denne prisen. |
| Hovedplanlegging | Grupper transaksjoner i planleggingsoptimalisering | Denne funksjonen kan bidra til å redusere antall planlagte bestillinger som genereres for å forsyne en enkelt salgsordrelinje når du bruker planleggingsoptimalisering. Når denne funksjonen er aktivert, grupperer planleggingsoptimalisering alle lagertransaksjoner for en ordrelinje i ett enkelt behov for hele antallet. (Denne virkemåten samsvarer med den innebygde planleggingsmotorvirkemåten.) Tilbud og etterspørsel grupperes separat. Funksjonen bidrar derfor til å redusere transaksjonsvolumet når du har delte transaksjoner, og når du bruker dimensjoner (f.eks. partinumre eller serienumre) som ikke har dekningsdimensjoner. |
| Innkjøp og leverandører | Sett leverandør på vent for bestillinger | Ved hjelp av denne funksjonen kan du sette en leverandør på vent for bestillinger. Den legger til en ny sperretype *bestilling* som merker en leverandør som på vent for bestillinger. Du kan ikke opprette nye bestillinger for leverandører som er på vent for bestillinger, men du kan likevel gå videre med eventuelle åpne fakturaer eller betalinger for disse leverandørene. |
| Salg og markedsføring | Beregn linjenettobeløp ved import | Ved hjelp av denne funksjonen kan du styre om systemet skal beregne linjetotaler på nytt når du importerer data via enhetene *Salgsordrelinjer*, *Salgstilbudslinjer* eller *Returordrelinjer* ved hjelp av OData eller dobbel skriving. Den har bare effekt når du også har policyer for forretningsavtaleevaluering på plass som begrenser endringer i **Nettobeløp**-feltet for salgsordrelinjer, salgstilbudslinjer eller returordrelinjer. Det legger til en innstilling som kalles **Beregnnettobeløp på linjen**, til siden **Kunder > Oppsett > Kundeparametere**. Når denne innstillingen er satt til *Ja*, omberegner systemet alltid linjebeløpene når det er nødvendig (og dermed ignorerer alle evalueringspolicyer for forretningsavtaler for nettobeløpet på linjen). Når innstillingen er satt til *Nei*, vil systemet aldri automatisk beregne nettobeløpet på linjen, selv om innkommende endringer i linjepris, antall eller rabatt vil angi at nettobeløpet på linjen skal omberegnes. Denne funksjonen er aktivert som standard, og setter opprinnelig **Beregn nettobeløp for linje** til *Ja*. Innstillingen *Nei* samsvarer med systemvirkemåten før versjon 10.0.23, og angis vanligvis for å støtte eldre integreringsscenarioer.<br><br>Hvis du vil ha mer informasjon , kan du se [Beregne nettobeløp på nytt når du importerer salgsordrer, tilbud og returer](../sales-marketing/calc-line-net-amounts-import.md). |
| Salg og markedsføring | Beregn salgstotaler ved hjelp av flere tråder | Denne funksjonen bidrar til å forbedre ytelsen ved å aktivere systemet for bruk av parallell behandling når det beregner salgstotaler i et parti. Funksjonen legger til et nytt **Antall tråder**-felt i dialogboksen **Beregn salgstotaler**. Hvis du velger å kjøre beregningen i et parti, kan du bruke dette feltet til å angi maksimalt antall tråder. Hvis du angir verdien til *0* (null) eller *1*, brukes en enkelt tråd. Verdier over 1 aktiverer flertråding. |
| Salg og markedsføring | Oppdater priser og rabatter som er angitt manuelt for konsernintern | Denne funksjonen legger til støtte for manuelle endringspolicyer for konserninterne ordrer. Den inneholder støtte for overføring av manuelle endringspolicyer mellom konserninterne salgsordrer og bestillinger. Tidligere ble manuelle endringspolicyer bare støttet for ikke-konserninterne ordrer. Når denne funksjonen er aktivert, gir systemet deg muligheten til å oppdatere priser og rabatter etter at du har lagret endringer i en konsernintern ordre. Med dette alternativet kan du velge om du vil bruke de nye prisene og rabattdetaljene i den konserninterne ordren, eller la ordren stå uendret. |

## <a name="new-and-updated-documentation-resources"></a>Nye og oppdaterte dokumentasjonsressurser

Vi har nylig lagt til eller betydelig oppdatert følgende hjelpeartikler. Disse artiklene er ikke nødvendigvis knyttet til de nye funksjonene som ble lagt til i denne versjonen, som vist i de forrige delene. De kan imidlertid hjelpe deg med å få mer ut av eksisterende funksjoner.

| Funksjonsområde | Nye eller oppdaterte artikler |
|---|---|
| Hovedplanlegging, CTP | [Beregn leveringsdatoer for salgsordrer ved hjelp av CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) |
| Hovedplanlegging, etterspørselsdrevet planlegging av materialkrav | [Oversikt over etterspørselsdrevet planlegging av materialkrav](../master-planning/planning-optimization/ddmrp-overview.md)<br>[Aktiver DDMRP-funksjonen for systemet](../master-planning/planning-optimization/ddmrp-enable.md)<br>[Lagerplassering](../master-planning/planning-optimization/ddmrp-inventory-positioning.md)<br>[Bufferprofil og -nivåer](../master-planning/planning-optimization/ddmrp-buffer-profile-and-levels.md)<br>[Etterspørselsdrevet planlegging](../master-planning/planning-optimization/ddmrp-planning.md)<br>[Visuell og samarbeidsbasert kjøring](../master-planning/planning-optimization/ddmrp-visual-and-collaborative-execution.md) |
| Lagerstyring | [Pakkebeholdere til forsendelse](../warehousing/packing-containers.md)<br>[Pakkearbeid for pakking av utgående beholdere og behandling av forsendelser](../warehousing/packing-work.md) |

## <a name="feature-state-changes-in-this-release"></a>Endringer av funksjonstilstand i denne versjonen

Denne tabellen viser funksjoner som er blitt obligatoriske eller som er aktivert som standard, i versjon 10.0.29. Alle disse funksjonene aktiveres automatisk for systemet så snart du oppdaterer til versjon 10.0.29. Obligatoriske funksjoner kan ikke slås av, men funksjoner som er på som standard, kan fremdeles slås av ved hjelp av [Funksjonsadministrasjon](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tabellen viser også funksjoner som tidligere var i forhåndsversjon, men som er endret til å bli generelt tilgjengelig i versjon 10.0.29. Denne endringen angir at funksjonene nå anbefales for bruk i produksjonsmiljøer. Disse funksjonene er deaktivert som standard med mindre annet er nevnt. Derfor må du bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) for å aktivere dem hvis du vil bruke dem.

| Modul | Funksjonsnavn | Ny funksjonstilstand |
| --- | --- | --- |
| Ressursbehandling | [Funksjonalitet for anleggsmiddelstyring for grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-configure.md) | Obligatorisk |
| Kostnadsstyring | [Endre etiketten for annullering i Lukking og justering for å tilbakeføre](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse) | Obligatorisk |
| Kostnadsstyring | Rydd opp detaljer for stykklisteberegning | Obligatorisk |
| Kostnadsstyring | [Sammenlign varepriser - lagring](../cost-management/compare-item-price.md) | Obligatorisk |
| Kostnadsstyring | [Kostnadsberegningsnivå](../cost-management/cost-calculation-level.md) | Aktivert som standard |
| Kostnadsstyring | Aktiver brukerdefinert partinummeroppsett for tilbakeføring av lagerlukking | Aktivert som standard |
| Kostnadsstyring | [Fremdriftsdetaljer for lagerlukking](whats-new-scm-10-0-21.md) | Aktivert som standard |
| Kostnadsstyring | [Lagring av lagerverdirapport](../cost-management/inventory-value-report-storage.md) | Obligatorisk |
| Kostnadsstyring | Opprydding av rapportdata for lagerverdi | Obligatorisk |
| Kostnadsstyring | Glidende gjennomsnitt, reserve-kostnadssekvens | Obligatorisk |
| Kostnadsstyring | Vis lagerlukkingslogg i rutenett | Obligatorisk |
| Kostnadsstyring | Vis varene med ikke fullstendig utlignede transaksjoner i sammendragsformat | Obligatorisk |
| Lagerstyring | Tillat tomme verdier for partiattributter | Obligatorisk |
| Lagerstyring | Øk linjenumre automatisk for ordrelinjer for lageroverføring | Obligatorisk |
| Lagerstyring | Opprett overføringsordre fra salgslinje | Obligatorisk |
| Lagerstyring | Deaktiver feltet Lagerjournallinjer i arbeidsflyt | Obligatorisk |
| Lagerstyring | Aktiver funksjon for advarsel om parametere for lagerkvalitetsstyring | Obligatorisk |
| Lagerstyring | (Kina) Utelat fysiske mottaks- og utstedelseskostnader fra månedlig gjennomsnittskostnad | Aktivert som standard |
| Lagerstyring | [Beholdningsjournal - godkjenn - arbeidsflyt](../inventory/inventory-journal-workflow.md) | Obligatorisk |
| Lagerstyring | [Lagring av rapport for lagerbeholdning](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/inventory-on-hand-report-storage) | Obligatorisk |
| Lagerstyring | [Lagrede visninger for lagerstyring](saved-views-scm.md) | Obligatorisk |
| Lagerstyring | Annullering av overføringsordre | Obligatorisk |
| Lagerstyring | Bruker måleenhet og enhetsantall i lagerjournaler | Obligatorisk |
| Lagerstyring | Lås opp lagerjournal | Obligatorisk |
| Produksjon | [Automatisk plukking av lageraktiverte materialer for automatisk posterte plukklister](whats-new-scm-10-0-23.md) | Generelt tilgjengelig |
| Produksjon | Aktiver visning av lagerdimensjoner i materiallisten for produksjonsruteoperasjoner | Obligatorisk |
| Produksjon | [Aktiver angivelse av parti- og serienumre under ferdigrapportering fra jobbkortenheten](../production-control/report-finished-job-device.md) | Aktivert som standard |
| Produksjon | Forbedret plukking av et antall for faktisk vekt for produksjon | Aktivert som standard |
| Produksjon | [Jobbsøk for grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-configure.md) | Obligatorisk |
| Produksjon | [Integrering av produksjonsutførelsessystem](../production-control/mes-integration.md) | Aktivert som standard |
| Produksjon | [Visningen Min dag for grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-configure.md) | Aktivert som standard |
| Produksjon | [Kontroll av materialtilgjengelighet etter behov for produksjonsordrer](whats-new-scm-10-0-24.md) | Aktivert som standard |
| Produksjon | [Overstyr standard produksjonsreservasjon](../production-control/override-default-reservation-principle.md) | Obligatorisk |
| Produksjon | [Registrer materialforbruk i grensesnittet for produksjonsutførelse (ikke lagerstyring)](../production-control/production-floor-execution-configure.md) | Generelt tilgjengelig |
| Produksjon | [Rapport om faktisk vekt-varer fra grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-configure.md) | Generelt tilgjengelig |
| Produksjon | [Rapport om ko- og biprodukter fra grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-configure.md) | Aktivert som standard |
| Produksjon | [Rapport om planleggingsvarer i grensesnittet for produksjonsutførelse](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | Aktivert som standard |
| Produksjon | [Lagrede visninger for produksjonskontroll](saved-views-scm.md) | Obligatorisk |
| Produksjon | [Vis fullstendige serie-, parti- og skiltnumre i grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-configure.md) | Obligatorisk |
| Produksjon | [Valider utløp av råvarer mot dato for planlagt forbruk](whats-new-scm-10-0-23.md) | Aktivert som standard |
| Hovedplanlegging | [Automatisk autorisasjon for Planleggingsoptimalisering](../master-planning/planning-optimization/planned-order-firming.md) | Obligatorisk |
| Hovedplanlegging | [Autorisasjon og konsolidering av planlagte masse- og pakkepartiordrer](whats-new-scm-10-0-20.md) | Aktivert som standard |
| Hovedplanlegging | [Inkluder varer med beholdning når filtre for forhåndsbehandling er aktivert](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/master-planning-include-items-on-hand-when-pre-processing-filters-are-enabled) | Aktivert som standard |
| Hovedplanlegging | [Uendelig kapasitetsplanlegging for Planleggingsoptimalisering](../master-planning/planning-optimization/infinite-capacity-planning.md) | Aktivert som standard |
| Hovedplanlegging | [Marginer for planleggingsoptimalisering](../master-planning/planning-optimization/safety-margins.md) | Obligatorisk |
| Hovedplanlegging | [Negative dager for Planleggingsoptimalisering](../master-planning/planning-optimization/delay-tolerance.md) | Obligatorisk |
| Hovedplanlegging | [Parallell autorisasjon av justert behovsprognose](whats-new-scm-10-0-20.md) | Obligatorisk |
| Hovedplanlegging | [Autorisering av planlagt bestilling med filtrering](../master-planning/planning-optimization/planned-order-firming.md) | Obligatorisk |
| Hovedplanlegging | [Planlagte produksjonsordrer for planleggingsoptimalisering](../master-planning/planning-optimization/production-planning.md) | Obligatorisk |
| Hovedplanlegging | [Forretningsavtaler for innkjøp for planleggingsoptimalisering](../master-planning/planning-optimization/purchase-trade-agreement.md) | Obligatorisk |
| Hovedplanlegging | [Lagrede visninger for planlagte bestillinger](saved-views-scm.md) | Obligatorisk |
| Innkjøp og leverandører | Beløp fra og til for tillegg i bestillinger | Obligatorisk |
| Innkjøp og leverandører | Deaktiver tilbakestillingsknapp for distribusjon av innkjøpsrekvisisjon | Aktivert som standard |
| Innkjøp og leverandører | [Aktiver tilbakestilling av innkjøpsrelaterte arbeidsflyter](whats-new-scm-10-0-20.md) | Aktivert som standard |
| Innkjøp og leverandører | [Begrens antall bestillingslinjer per partioppgave](whats-new-scm-10-0-27.md) | Aktivert som standard |
| Innkjøp og leverandører | [Slå sammen finansdimensjoner fra leverandøren med aktiv finansdimensjon for dimensjonskobling på bestillingen](whats-new-scm-10-0-25.md) | Obligatorisk |
| Innkjøp og leverandører | [Poster registrerte antall lagerførte produkter og rester av ikke-lagerførte produkter for kvitteringer og leverandørfakturaer](whats-new-scm-10-0-26.md) | Generelt tilgjengelig |
| Innkjøp og leverandører | [Forhindre overforbruk av generelle budsjettreservasjoner når flere innkjøpsrekvisisjoner er i arbeidsflyt](whats-new-scm-10-0-21.md) | Aktivert som standard |
| Innkjøp og leverandører | [Ansvarlig part for kjøpsavtale](../procurement/purchase-agreements.md) | Obligatorisk |
| Innkjøp og leverandører | [Lagrede visninger for bestillinger](saved-views-scm.md) | Obligatorisk |
| Behandling av produktinformasjon | Forhåndsbehandling for stykklisterapport for å unngå tidsavbrudd | Obligatorisk |
| Behandling av produktinformasjon | Separer finansdimensjoner som standard ved bruk av varemaler | Obligatorisk |
| Behandling av produktinformasjon | Aktiver produktdimensjonsgrupper for varemaler | Obligatorisk |
| Behandling av produktinformasjon | Enhetsforbedringer for vare – strekkode | Obligatorisk |
| Behandling av produktinformasjon | Generer navn på produktvarianter på nytt basert på terminologi | Obligatorisk |
| Behandling av produktinformasjon | [Lagrede visninger for frigitte produkter](saved-views-scm.md) | Obligatorisk |
| Behandling av produktinformasjon | [Sideforbedringer for variantforslag](../pim/tasks/create-predefined-product-variants.md) | Obligatorisk |
| Salg og markedsføring | [Gebyrtildeling i en salgsordre](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/miscellaneous-charges-enhancements) | Obligatorisk |
| Salg og markedsføring | Rydd opp i oppdateringshistorikk for salgsordre | Obligatorisk |
| Salg og markedsføring | [Rydd opp i salgsoppdateringshistorikk basert på alder](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) | Obligatorisk |
| Salg og markedsføring | [Eksportoptimalisering av dataenhet for kontaktperson](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Obligatorisk |
| Salg og markedsføring | Kopier sluttrabattgruppe for salgskreditnota | Obligatorisk |
| Salg og markedsføring | [Aktiver oppslag for dokumentinnledning for salgstilbud og dokumentkonklusjonsfelt](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Obligatorisk |
| Salg og markedsføring | [Forbedre ytelsen til rapport om Topp 100-kunder](whats-new-scm-10-0-23.md) | Obligatorisk |
| Salg og markedsføring | Inkluder ventende poster i historikkoppryddingsoppgaver | Obligatorisk |
| Salg og markedsføring | Begrens antall salgsordrelinjer per partioppgave | Aktivert som standard |
| Salg og markedsføring | [Begrens antall salgsordrer som kan velges for postering](whats-new-scm-10-0-21.md) | Obligatorisk |
| Salg og markedsføring | Beregn beregnet kundesaldo på nytt | Obligatorisk |
| Salg og markedsføring | [Registrering av ordrereturlinje med desimalpresisjon med og uten faktisk vekt](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Obligatorisk |
| Salg og markedsføring | [Lagrede visninger for salg og markedsføring](saved-views-scm.md) | Obligatorisk |
| Salg og markedsføring | [Salgsordrebekreftelse med ett klikk](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation) | Obligatorisk |
| Transportstyring | Tillat oppheving av samsvar for fraktbrev fra fraktfakturalinjer uten en postert leverandørfakturajournal | Aktivert som standard |
| Transportstyring | [Aktiver oppretting av en leverandørfakturajournal når du forkaster et fraktbrev](whats-new-scm-10-0-20.md) | Aktivert som standard |
| Transportstyring | [Forsendelse av småpakker](../warehousing/small-parcel-shipping.md) | Obligatorisk |
| Transportstyring | [USMCA-sertifisering av opprinnelig dokument](../transportation/usmca-certification-of-origin.md) | Aktivert som standard |
| Lagerstyring | [Ekstra lokasjonssone](../warehousing/additional-location-zones.md) | Obligatorisk |
| Lagerstyring | [Avbryt arbeid](../warehousing/cancel-warehouse-work.md) | Obligatorisk |
| Lagerstyring | [Konsolider forsendelse](../warehousing/configure-shipment-consolidation-policies.md) | Obligatorisk |
| Lagerstyring | [Opprett og behandle overføringsordrer fra lagerappen](../warehousing/create-transfer-order-from-warehouse-app.md) | Obligatorisk |
| Lagerstyring | Kryssoverføringsmaler med lokasjonsdirektiver | Aktivert som standard |
| Lagerstyring | [Koble plasseringsarbeid fra ASN-er](whats-new-scm-10-0-21.md) | Obligatorisk |
| Lagerstyring | [Utsatte plasseringsoperasjoner](../warehousing/deferred-processing-manual-inventory-movement.md) | Obligatorisk |
| Lagerstyring | Utsatt plassering – container | Aktivert som standard |
| Lagerstyring | Behandling av utsatt plassering - aktiver for revisjonsmalfunksjon med utløserhendelse satt til Forrige | Obligatorisk |
| Lagerstyring | [Deaktiver forventede mottak fra kvalitetsordrer som eksempler blokkert beholdning](../inventory/inventory-blocking.md) | Aktivert som standard |
| Lagerstyring | Aktiver hurtigvalidering for lagermobilenheter | Obligatorisk |
| Lagerstyring | [Forbedret analyse for GS1-strekkoder](../warehousing/gs1-barcodes.md) | Generelt tilgjengelig |
| Lagerstyring | [Fleksibel, ordreforpliktet reservasjon av nummerskilt](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Obligatorisk |
| Lagerstyring | [Fleksibel dimensjonsreservasjon for lagernivå](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Obligatorisk |
| Lagerstyring | [Bruk av lokasjon for varekonsolidering](../warehousing/item-consolidation-location-utilization.md) | Aktivert som standard |
| Lagerstyring | Mottakshistorikk for nummerskilt | Aktivert som standard |
| Lagerstyring | [Manuell forsendelseskonsolidering](../warehousing/consolidate-shipments-manual-workbench.md) | Aktivert som standard |
| Lagerstyring | [Plukktjeneste for manuell overføringslinje for administrator eller lignende klarerte brukere](whats-new-scm-10-0-28.md) | Generelt tilgjengelig |
| Lagerstyring | [Grensesnitt for materialhåndteringsutstyr](../warehousing/mhax.md) | Obligatorisk |
| Lagerstyring | [Nye sider for arbeidsområde for lastplanlegging](whats-new-scm-10-0-24.md) | Generelt tilgjengelig |
| Lagerstyring | [Visualisering av utgående arbeidsmengde](../warehousing/outbound-workload-visualization.md) | Obligatorisk |
| Lagerstyring | [Planlagt direkteoverføring](../warehousing/planned-cross-docking.md) | Obligatorisk |
| Lagerstyring | [Behandle lagerapphendelser](../warehousing/warehouse-app-events.md) | Obligatorisk |
| Lagerstyring | Spørringsforbedring i arbeidsmalen for plassering av koprodukt og biprodukt | Obligatorisk |
| Lagerstyring | [Rund antall ned til nærmeste salgsenhet ved frigivelse til lager](whats-new-scm-10-0-19.md) | Obligatorisk |
| Lagerstyring | [Lagret visning for arbeidsområdet for lastplanlegging](saved-views-scm.md) | Obligatorisk |
| Lagerstyring | [Lagret visning for arbeidsdetaljsiden](saved-views-scm.md) | Obligatorisk |
| Lagerstyring | [Lagret visning for bølgebehandling](saved-views-scm.md) | Obligatorisk |
| Lagerstyring | [Lagrede visninger for lastbehandling](saved-views-scm.md) | Obligatorisk |
| Lagerstyring | [Lagrede visninger for forsendelsesbehandling](saved-views-scm.md) | Obligatorisk |
| Lagerstyring | [Skann GS1-strekkoder](../warehousing/gs1-barcodes.md) | Generelt tilgjengelig |
| Lagerstyring | Detaljer for forsendelsesbølgeetikett | Obligatorisk |
| Lagerstyring | [Blandede enheter for spor](whats-new-scm-10-0-21.md) | Obligatorisk |
| Lagerstyring | [Bruk raskere API for containere som lukkes / åpnes på nytt på pakkestasjon](whats-new-scm-10-0-21.md) | Aktivert som standard |
| Lagerstyring | [Valider maler som er valgt for etterfyllingsjobber](whats-new-scm-10-0-20.md) | Aktivert som standard |
| Lagerstyring | [Forfremmede felter for lagerapp](../warehousing/warehouse-app-promoted-fields.md) | Obligatorisk |
| Lagerstyring | [Trinninstruksjoner for lagerapp](../warehousing/mobile-app-titles-instructions.md) | Obligatorisk |
| Lagerstyring | [Status for lagerlokasjon](../warehousing/warehouse-location-status.md) | Obligatorisk |
| Lagerstyring | [Omveier i Warehouse Management-appen](../warehousing/warehouse-app-detours.md) | Aktivert som standard |
| Lagerstyring | [Detaljer om satsvis bølgejobb](../warehousing/wave-processing.md) | Obligatorisk |
| Lagerstyring | [Varslinger for bølgekjøring](../warehousing/wave-execution-notifications.md) | Obligatorisk |

## <a name="additional-resources"></a>Tilleggsressurser

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformoppdateringer for økonomi- og driftsapper

Microsoft Dynamics 365 Supply Chain Management 10.0.29 inkluderer plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.29 av økonomi- og driftsapper (oktober 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md).

### <a name="bug-fixes"></a>Feilrettinger

Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av versjon 10.0.29, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 og bransjeskyer: plan for lanseringsbølge 1 for 2022

Er du spent på kommende og nylig utgitte tilleggspakkefunksjoner i våre bedriftsprogrammer eller -plattform?

Sjekk ut [Dynamics 365 og bransjeskyer: plan for lanseringsbølge 2 for 2022](/dynamics365-release-plan/2022wave2/). Vi har registrert alle detaljene, ende til ende, øverst til nederst, i et enkelt dokument som du kan bruke i planleggingen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og avskrevne funksjoner i Supply Chain Management

Artikkelen [Fjernede eller avskrevne funksjoner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver funksjoner som er eller er planlagt å bli fjernet eller avskrevet for Supply Chain Management.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Før en funksjon fjernes fra produktet, vil avskrivningsvarselet bli kunngjort i artikkelen [Fjernede eller avskrevne funksjoner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder før fjerningen.

For oppdelingsendringer som bare påvirker kompileringstiden, men som er binære kompatible med sandkasse- og produksjonsmiljøer, vil avskrivningstiden være mindre enn 12 måneder. Dette er vanligvis funksjonelle oppdateringer som må gjøres på kompilatoren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

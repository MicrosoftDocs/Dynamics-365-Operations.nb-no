---
title: Forhåndsversjon av Dynamics 365 Supply Chain Management 10.0.25 (april 2022)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management 10.0.25.
author: kamaybac
ms.date: 02/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 8a9b873b7b4bba43b7b3e6e83c389ac35b4e223e
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103002"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10025-april-2022"></a>Forhåndsversjon av Dynamics 365 Supply Chain Management 10.0.25 (april 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management-forhåndsversjonen 10.0.25. Denne versjonen har et build-nummer 10.0.1149, og er tilgjengelig som følger:

- **Forhåndsversjon:** februar 2022
- **Allmenn tilgjengelighet av versjon (selvoppdatering):** mars 2022
- **Allmenn tilgjengelighet av versjon (automatisk oppdatering):** april 2022

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. Dette emnet kan være oppdatert for å inkludere funksjoner som ble tatt med i builden etter at dette emnet ble publisert.

| Funksjonsområde | Funksjon | Mer informasjon | Aktivert av   |
|---|---|---|---|
| Lager&nbsp;og&nbsp;logistikk | Forbedringer for farlige materialer | Disse forbedringene bygger på eksisterende funksjonalitet for farlige materialer for å hjelpe firmaene med å holde seg i samsvar med lokale bestemmelser ved transport av farlige materialer på tvers av forskjellige geografiske områder. <!-- KFM: Update to 2022w1 link when published -->| Funksjonsbehandling:<br>*Forbedringer for farlige materialer* |
| Lager&nbsp;og&nbsp;logistikk | Pakkearbeid for pakkestasjoner | Denne funksjonen gir betydelig bedre fleksibilitet og smidighet i pakke- og forsendelsesoperasjonene. Under pakkeprosessen kan lagerarbeidere nå pakke og sende individuelle pakker som er knyttet til samme forsendelse og belastning. Ordrelinjer som inngår i den samme forsendelsen, behøver ikke nødvendigvis å sendes sammen hvis noen varer er klare for forsendelse med en gang. En enkelt ordre kan pakkes og sendes i flere pakker til ulike forsendelsestider, noe som reduserer ventetidene og legger til fleksibilitet.<!-- KFM: Update to 2022w1 link when published --> | Funksjonsbehandling:<br>*Pakkearbeid for pakkestasjoner* |
| Lager&nbsp;og&nbsp;logistikk | [Skann strekkoder i lageret ved hjelp av standardene i GS1-format](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) <!-- KFM: Update to 2022w1 link when published --> | [GS1-strekkoder og QR-koder](../warehousing/gs1-barcodes.md) | Funksjonsbehandling:<br>*Skann GS1-strekkoder* |
| Produksjon | [Materialforbruk og reservasjoner i grensesnittet for produksjonsutførelse](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [Hvordan arbeidere bruker grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-use.md) | Funksjonsbehandling:<br>*(Forhåndsversjon) Registrer materialforbruk i grensesnittet for produksjonsutførelse (WMS-aktivert)* |
| Produksjon | [Registrer materialforbruk på storskalaenheter](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/register-material-consumption-scale-units) | [Skalaenheter for sky og kant for arbeidsbelastninger for produksjonsutførelse](../cloud-edge/cloud-edge-workload-manufacturing.md) | Funksjonsbehandling:<br>*Registrer materialforbruk i mobilappen på en skalaenhet* |
| Planlegging | [Forslag fra Planleggingsoptimalisering for å optimalisere eksisterende forsyning](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [Handlingsmeldinger](../master-planning/action-messages.md) | Aktivert som standard |
| Planlegging | Planlagte ordrer forenklet | [Planlagte ordrer forenklet](../master-planning/planning-optimization/planned-orders-simplified.md ) | Funksjonsbehandling:<br>*Planlagte ordrer forenklet* |

## <a name="feature-enhancements-included-in-this-release"></a>Funksjonsforbedringer inkludert i denne versjonen

Denne tabellen viser funksjonsforbedringer i denne versjonen. Hvert av disse forbedringene gir en trinnvis forbedring av en eksisterende funksjon. Siden de bare er forbedringer vises de ikke i [frigivelsesplanen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). For å sikre at disse forbedringene ikke kommer i konflikt med eksisterende tilpasninger eller innstillinger, er imidlertid hver av dem slått av som standard (med mindre annet er angitt).

Hvis du vil slå noen av disse funksjonene på eller av, må du gjøre dette i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funksjonsnavn i funksjonsbehandling | Mer informasjon |
|---|---|---|
| Lagerstyring | (Polen) Tillat å koble flere SAD-fakturaer til én bestillingslinje i én SAD | Ved hjelp av denne funksjonen kan du dele bestillingslinjer og koble dem til ett enkelt administrativt dokument (SAD) når disse bestillingslinjene ble postert for flere forskjellige fakturaer (for eksempel for forskjellige forsendelser). |
| Innkjøp og leverandører | Konsolider flere innkjøpsrekvisisjoner til én bestilling etter regnskapsdato | Ved hjelp av denne funksjonen kan flere innkjøpsrekvisisjoner konsolideres til én bestilling hvis de ulike innkjøpsrekvisisjonene har ulike regnskapsdatoer. Oppretting og etterspørselskonsolidering av innkjøpspolicyregler for bestillinger kan konfigureres til å automatisere beslutningen for gruppering av rekvisisjonslinjer etter regnskapsdato på bestillingsnivå. Bestillingskonsolidering etter regnskapsdato støttes ikke hvis budsjettkontroll er aktivert, fordi regnskapsdatoen brukes til budsjettreservasjoner og disposisjon. Derfor bør den beholdes i løpet av overgangen fra innkjøpsrekvisisjon til bestilling. |
| Innkjøp og leverandører | Vis eldre innstillinger for standard svarfelt i tilbudsforespørsel | Denne funksjonen gjeninnfører de eldre svarfeltinnstillingene for tilbudsforespørsler (RFQ), som tidligere ble fjernet fra brukergrensesnittet. Disse innstillingene inneholder ingen funksjonalitet ut av boksen, men kan tilpasses for å angi den etter behov. Aktiver denne funksjonen hvis organisasjonen allerede har lagt til funksjonalitet for standardinnstillingene for svarfeltene for tilbudsforespørsler eller planlegger å gjøre det. Når denne funksjonen er aktivert, kan du få tilgang til innstillingene ved å gå til siden **Parametere for innkjøp og leverandører**, åpne fanen **Tilbudsforespørsel** og velge **Standard svarfelt i tilbudsforespørsel**. |
| Innkjøp og leverandører | Slå sammen finansdimensjoner fra leverandøren med aktiv finansdimensjon for dimensjonskobling på bestillingen | Ved hjelp av denne funksjonen kan du flette finansdimensjoner fra leverandører med aktive finansdimensjoner for dimensjonskoblingetter godkjenning av innkjøpsrekvisisjonen hvis du definerer en kobling mellom en finansdimensjon og områdelagerdimensjonen. Oppretting og behovskonsolidering av innkjøpspolicyregler for bestillinger kan defineres til å kjøre beslutningen om å flette finansdimensjoner fra leverandører med finansdimensjonen for aktiv dimensjonskobling på bestillingshodenivå. |
| Produksjonskontroll | (Russland) Aktiver standard lokasjonsoppsett for produksjonsformel/stykkliste og automatisk GTD-reservasjon/-forbruk i produksjon | Funksjonen aktiverer flere alternativer for produksjon fra importerte råmaterialer (kun russisk oversettelse):<ul><li>Alternativ for å angi automatisk standardlokasjon for produksjonsformler og stykklister i både ressursgrupper og lagre.</li><li>Automatisk reservering av råvarer av dimensjonen *GTD-nummer* ved WMS-aktiverte lagre i henhold til algoritmen for ikke-WMS-reservasjon. Dette gjelder i tilfeller der det finnes en arbeidspolicy for *Råvareplukking* med **Arbeidsopprettelsesmetode** angitt til *Aldri*, og der oppsettet av lager, lokasjon og varenummer samsvarer med beholdningstransaksjonene for produksjonsordren (bunkeordren).</li><li>Automatisk forbruk av råvarer etter dimensjonen *GTD-nummer* ved plukklistepostering, i henhold til den oppnådde reserveringen som er beskrevet tidligere.</li></ul> |
| Lagerstyring | (Forhåndsversjon) Støtte for skalaenhet for innkommende og utgående lagerordrer | Denne funksjonen fører til at systemet oppretter utgående lagerordrer i løpet av frigivelse-til-lager-prosessen, og til å opprette innkommende lagerordrer når overføringsordrer posteres som sendte. Systemet synkroniserer deretter hver innkommende eller utgående lagerordre til storskalaenheten som er ansvarlig for forsendelse eller mottak av ordren. Legg merke til at når denne funksjonen er aktivert, må arbeidsmengdene for lagerutførelse oppgraderes. Hvis du vil ha mer informasjon, kan du se [Arbeidsbelastninger for lagerstyring for sky- og kantskalaenheter](../cloud-edge/cloud-edge-workload-warehousing.md).<br><br>Denne funksjonen krever funksjonen *Koble plasseringsarbeid fra ASN-er*, og vil gjøre det mulig å motta overføringsordrer ved hjelp av lisensmottaksprosessen i Warehouse Management-mobilappen. |

## <a name="feature-state-changes-in-this-release"></a>Endringer av funksjonstilstand i denne versjonen

Denne tabellen viser funksjoner som er blitt obligatoriske eller som er aktivert som standard, fra og med 10.0.25. Alle disse funksjonene aktiveres automatisk for systemet så snart du oppdaterer til 10.0.25. Obligatoriske funksjoner kan ikke slås av, men funksjoner som er på som standard, kan fremdeles slås av ved hjelp av [Funksjonsadministrasjon](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tabellen viser også funksjoner som tidligere var i offentlig forhåndsversjon, men som er endret til å bli generelt tilgjengelig i 10.0.25, som betyr at de nå anbefales for bruk i produksjonsmiljøer. Disse funksjonene er slått av som standard, med mindre annet er angitt, så du må bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) for å aktivere dem hvis du vil bruke dem.

| Modul | Funksjonsnavn | Funksjonstilstand |
| --- | --- | --- |
| Ressursbehandling | [Bruk regler for gruppering av arbeidsordrer når en vedlikeholdsplan kjøres](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md) | Generelt tilgjengelig |
| Ressursbehandling | [Tellerbaserte vedlikeholdsforbedringer](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md) | Generelt tilgjengelig |
| Kostnadsstyring | [Kostnadsberegningsnivå](../cost-management/cost-calculation-level.md) | Generelt tilgjengelig |
| Kostnadsstyring | Aktiver brukerdefinert partinummeroppsett for tilbakeføring av lagerlukking | Generelt tilgjengelig |
| Kostnadsstyring | [Fremdriftsdetaljer for lagerlukking](whats-new-scm-10-0-21.md) | Generelt tilgjengelig |
| Kostnadsstyring | [Alternativer for standardverdier for finansdimensjoner for kostnadsrevaluering av lagerstandard](../cost-management/manage-standard-cost-updates.md) | Generelt tilgjengelig |
| Kostnadsstyring | Opprydding av rapportdata for lagerverdi | Aktivert som standard |
| Kostnadsstyring | [Lagring av lagerverdirapport](../cost-management/inventory-value-report-storage.md) | Aktivert som standard |
| Kostnadsstyring | Vis lagerlukkingslogg i rutenett | Aktivert som standard |
| Styring av teknisk endring | [Aktiver endringsstyring på eksisterende produkter](../engineering-change-management/change-management-existing-products.md) | Aktivert som standard |
| Styring av teknisk endring | [Styring av teknisk endring](../engineering-change-management/product-engineering-overview.md) | Aktivert som standard |
| Styring av teknisk endring | [Tekniske varslinger for produksjon](../engineering-change-management/engineering-change-management.md) | Aktivert som standard |
| Styring av teknisk endring | [Forbedret attributtarv for Styring av teknisk endring](../engineering-change-management/engineering-attributes-and-search.md) | Aktivert som standard |
| Styring av teknisk endring | [Administrer endringer i formler og ingredienser](../engineering-change-management/manage-formula-changes.md) | Aktivert som standard |
| Styring av teknisk endring | [Produktklargjøringskontroller](../engineering-change-management/product-readiness.md) | Aktivert som standard |
| Styring av teknisk endring | [Variantgenerering for tekniske produkter](../engineering-change-management/engineering-variants.md) | Aktivert som standard |
| Lagerstyring | Navigasjon til stykklisteversjon fra stykklistelinjer | Obligatorisk |
| Hovedplanlegging | [Autorisasjon og konsolidering av planlagte masse- og pakkepartiordrer](whats-new-scm-10-0-20.md) | Generelt tilgjengelig |
| Hovedplanlegging | Ressursplanlegging med vedlikehold | Generelt tilgjengelig |
| Hovedplanlegging | Aktiver funksjoner i konfigurasjonsveiviseren for hovedplan | Obligatorisk |
| Hovedplanlegging | [Valg av prognosemodell i Detaljer om behovsprognose](../master-planning/manual-adjustments-baseline-forecast.md) | Obligatorisk |
| Hovedplanlegging | [Visualisering av fremdrift for hovedplanlegging](../master-planning/tasks/monitor-master-planning-run.md) | Obligatorisk |
| Hovedplanlegging | [Parallell autorisasjon av planlagte ordrer](../master-planning/planning-optimization/planned-order-firming.md) | Obligatorisk |
| Hovedplanlegging | [Autorisering av planlagt bestilling med filtrering](../master-planning/planning-optimization/planned-order-firming.md) | Aktivert som standard |
| Hovedplanlegging | [Lagrede visninger for planlagte bestillinger](saved-views-scm.md) | Aktivert som standard |
| Innkjøp og leverandører | Deaktiver tilbakestillingsknapp for distribusjon av innkjøpsrekvisisjon | Generelt tilgjengelig |
| Innkjøp og leverandører | [Aktiver tilbakestilling av innkjøpsrelaterte arbeidsflyter](whats-new-scm-10-0-20.md) | Generelt tilgjengelig |
| Innkjøp og leverandører | Mulighet til satsvis bekreftelse av godkjente bestillinger fra leverandørsamarbeid | Obligatorisk |
| Innkjøp og leverandører | Statusen Forseglet for kjøpsavtale | Obligatorisk |
| Innkjøp og leverandører | Legg til linjer i bestillingsfakturaer som er knyttet til en kjøpsavtale | Aktivert som standard |
| Innkjøp og leverandører | Legg til feltet Bestilt antall på siden Postere produktkvittering | Aktivert som standard |
| Innkjøp og leverandører | [Tillat leverandører å søke om innkjøpskategorier gjennom leverandørsamarbeid](../procurement/category-requests-from-vendors.md) | Aktivert som standard |
| Innkjøp og leverandører | Beløp fra og til for tillegg i bestillinger | Aktivert som standard |
| Innkjøp og leverandører | Oppsett for tillegg med område og lager | Aktivert som standard |
| Innkjøp og leverandører | Aktiver beregning av innkjøpsavgift basert på årlig tariff | Aktivert som standard |
| Innkjøp og leverandører | [Ansvarlig part for kjøpsavtale](../procurement/purchase-agreements.md) | Aktivert som standard |
| Innkjøp og leverandører | [Lagrede visninger for bestillinger](saved-views-scm.md) | Aktivert som standard |
| Behandling av produktinformasjon | [Streng validering av standard ordreantall](../production-control/default-order-settings.md) | Obligatorisk |
| Behandling av produktinformasjon | Forhåndsbehandling for stykklisterapport for å unngå tidsavbrudd | Aktivert som standard |
| Behandling av produktinformasjon | Separer finansdimensjoner som standard ved bruk av varemaler | Aktivert som standard |
| Behandling av produktinformasjon | Aktiver produktdimensjonsgrupper for varemaler | Aktivert som standard |
| Behandling av produktinformasjon | Generer navn på produktvarianter på nytt basert på terminologi | Aktivert som standard |
| Behandling av produktinformasjon | [Sideforbedringer for variantforslag](../pim/tasks/create-predefined-product-variants.md) | Aktivert som standard |
| Produksjonskontroll | Forbedret plukking av et antall for faktisk vekt for produksjon | Generelt tilgjengelig |
| Produksjonskontroll | Den nye knappen Stopp pause er lagt til på siden Jobbkortterminal | Obligatorisk |
| Produksjonskontroll | [Aktiver automatisk generering av nummerskiltnummer ved ferdigrapportering i jobbkortenheten](../production-control/production-floor-execution-configure.md) | Obligatorisk |
| Produksjonskontroll | Aktiver delvis mottak av underleveransevarer, og rett opp et problem med beregning av svinn for stykklistelinjer av typen Leverandør | Obligatorisk |
| Produksjonskontroll | [Funksjon for låsing av jobbkortenheten og jobbkortterminal slik at de kan rengjøres](../production-control/production-floor-execution-configure.md) | Obligatorisk |
| Produksjonskontroll | Forbedringer i dialogboksene Godkjenn og Overfør jobber | Obligatorisk |
| Produksjonskontroll | [Nummerskilt for ferdigmelding lagt til i jobbkortenheten](../production-control/production-floor-execution-configure.md) | Obligatorisk |
| Produksjonskontroll | [Skriv ut etikett fra jobbkortenhet](../production-control/production-floor-execution-configure.md) | Obligatorisk |
| Produksjonskontroll | [Produksjonsutførelse](../production-control/production-floor-execution-configure.md) | Obligatorisk |
| Produksjonskontroll | [Funksjonalitet for anleggsmiddelstyring for grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-configure.md) | Aktivert som standard |
| Produksjonskontroll | [Jobbsøk for grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-configure.md) | Aktivert som standard |
| Produksjonskontroll | [Overstyr standard produksjonsreservasjon](../production-control/override-default-reservation-principle.md) | Aktivert som standard |
| Produksjonskontroll | [Vis fullstendige serie-, parti- og skiltnumre i grensesnittet for produksjonsutførelse](whats-new-scm-10-0-21.md) | Aktivert som standard |
| Salg og markedsføring | [Ytelsesforbedring for salgsordredetaljer](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Generelt tilgjengelig |
| Salg og markedsføring | Ytelsesforbedring for salgstilbudsdetaljer | Generelt tilgjengelig |
| Salg og markedsføring | Eksportpolicy for data som salgsordre henviser til | Obligatorisk |
| Salg og markedsføring | [Policy for sletting av salgsordre til bestillingslinje](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-purchase-order-line-deletion-policy) | Obligatorisk |
| Salg og markedsføring | [Eksportpolicy for data som salgstilbud henviser til](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy)| Obligatorisk |
| Salg og markedsføring | [Eksportoptimalisering av dataenhet for kontaktperson](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Aktivert som standard |
| Salg og markedsføring | Aktiver oppslag for dokumentinnledning for salgstilbud og dokumentkonklusjonsfelt | Aktivert som standard |
| Salg og markedsføring | [Forbedre ytelsen til rapport om Topp 100-kunder](whats-new-scm-10-0-23.md) | Aktivert som standard |
| Salg og markedsføring | Beregn beregnet kundesaldo på nytt | Aktivert som standard |
| Salg og markedsføring | [Registrering av ordrereturlinje med desimalpresisjon med og uten faktisk vekt](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Aktivert som standard |
| Salg og markedsføring | [Lagrede visninger for salg og markedsføring](saved-views-scm.md) | Aktivert som standard |
| Salg og markedsføring | Salgsordrebekreftelse med ett klikk | Aktivert som standard |
| Lagerstyring | [Kryssoverføringsmaler med lokasjonsdirektiver](../warehousing/planned-cross-docking.md) | Generelt tilgjengelig |
| Lagerstyring | [Deaktiver forventede mottak fra kvalitetsordrer som eksempler blokkert beholdning](../inventory/inventory-blocking.md) | Generelt tilgjengelig |
| Lagerstyring | Mottakshistorikk for nummerskilt | Generelt tilgjengelig |
| Lagerstyring | [Grensesnitt for materialhåndteringsutstyr](../warehousing/mhax.md) | Generelt tilgjengelig |
| Lagerstyring | [Rund antall ned til nærmeste salgsenhet ved frigivelse til lager](whats-new-scm-10-0-19.md) | Generelt tilgjengelig |
| Lagerstyring | Skalaenhetsstøtte for arbeidslister for lagerapp | Generelt tilgjengelig |
| Lagerstyring | Detaljer for forsendelsesbølgeetikett | Generelt tilgjengelig |
| Lagerstyring | [Bruk raskere API for containere som lukkes / åpnes på nytt på pakkestasjon](whats-new-scm-10-0-21.md) | Generelt tilgjengelig |
| Lagerstyring | [Valider maler som er valgt for etterfyllingsjobber](whats-new-scm-10-0-20.md) | Generelt tilgjengelig |
| Lagerstyring | Tillat at etterfyllingsmalen bruker eksisterende umiddelbart etterfyllingsarbeid (på tvers av enheter) | Obligatorisk |
| Lagerstyring | Automatisk tilordning av GUID-er i WHS-brukeroppretting | Obligatorisk |
| Lagerstyring | Registrer produktvarianter og sporingsdimensjoner i lagerappen under mottak av lastvare | Obligatorisk |
| Lagerstyring | [Endre beholdningsstatusen for varer som kontrolleres av sporingsdimensjoner](../inventory/inventory-statuses.md) | Obligatorisk |
| Lagerstyring | [Endre arbeidspulje i arbeid](../warehousing/change-work-pool-on-work.md) | Obligatorisk |
| Lagerstyring | [Gruppestilling full](../warehousing/cluster-position-full.md) | Obligatorisk |
| Lagerstyring | [Funksjon for gruppeplassering](../warehousing/putaway-clusters.md) | Obligatorisk |
| Lagerstyring | [Bekreft og overfør](../warehousing/confirm-and-transfer.md) | Obligatorisk |
| Lagerstyring | [Bekreft utgående forsendelser fra satsvise jobber](../warehousing/confirm-outbound-shipments-from-batch-jobs.md) | Obligatorisk |
| Lagerstyring | [Kontroller om en sammendragsside for mottak skal vises på mobilenheter](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Obligatorisk |
| Lagerstyring | [Utsatt behandling av manuell lagerbevegelsesoperasjon](../warehousing/deferred-processing-manual-inventory-movement.md) | Obligatorisk |
| Lagerstyring | Ikke tillat oppretting av laster som ikke oppfyller kravene i malen for lastplanbygging for bølge | Obligatorisk |
| Lagerstyring | [Forbedrede oppsett for nummerskiltetikett](../warehousing/document-routing-layout-for-license-plates.md) | Obligatorisk |
| Lagerstyring | [Evaluer alle handlinger for lokasjonsdirektiver med flere SKU-er](../troubleshooting/warehousing/evaluate-multiple-location-directive-actions.md) | Obligatorisk |
| Lagerstyring | Skjul feltet Total verdi på sidene Alle laster og Lastdetaljer | Obligatorisk |
| Lagerstyring | Konfigurasjon av etikettversjon for nummerskilt | Obligatorisk |
| Lagerstyring | Manuell korrigering av lastlinje for administrator eller lignende klarerte brukere | Obligatorisk |
| Lagerstyring | [Nummerskiltposisjonering for lokasjon](../warehousing/location-license-plate-positioning.md) | Obligatorisk |
| Lagerstyring | [Kombinasjon av produktdimensjoner for lokasjon](../warehousing/location-product-dimension-mixing.md) | Obligatorisk |
| Lagerstyring | Gjør lagerstatusfeltet for den mobile enhetsbeholdningen redigerbart | Obligatorisk |
| Lagerstyring | Plukktjeneste for manuell salgslinje for administrator eller lignende klarerte brukere | Obligatorisk |
| Lagerstyring | [Hindre at nummerskilt som er sendt med overføringsordrer, brukes i andre lagre enn mållageret](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Obligatorisk |
| Lagerstyring | Spør om å løse tvetydige Lok./nr.skilt-navn | Obligatorisk |
| Lagerstyring | [Kvalitetskontroll](../warehousing/quality-check.md) | Obligatorisk |
| Lagerstyring | [Brukerinnstillinger, ikoner og trinntitler for den nye lagerappen](../warehousing/install-configure-warehouse-management-app.md) | Obligatorisk |
| Lagerstyring | [Ekstra lokasjonssone](../warehousing/additional-location-zones.md) | Aktivert som standard |
| Lagerstyring | [Opprett og behandle overføringsordrer fra lagerappen](../warehousing/create-transfer-order-from-warehouse-app.md) | Aktivert som standard |
| Lagerstyring | Aktiver hurtigvalidering for lagermobilenheter | Aktivert som standard |
| Lagerstyring | [Maksimal kjøringstid for jobben Opprydding i beholdningsoppføringer for lagerstyring](../warehousing/onhand-cleanup.md) | Aktivert som standard |
| Lagerstyring | [Visualisering av utgående arbeidsmengde](../warehousing/outbound-workload-visualization.md) | Aktivert som standard |
| Lagerstyring | [Behandle lagerapphendelser](../warehousing/warehouse-app-events.md) | Aktivert som standard |
| Lagerstyring | [Lagret visning for arbeidsområdet for lastplanlegging](saved-views-scm.md) | Aktivert som standard |
| Lagerstyring | [Lagret visning for arbeidsdetaljsiden](saved-views-scm.md) | Aktivert som standard |
| Lagerstyring | [Lagret visning for bølgebehandling](saved-views-scm.md) | Aktivert som standard |
| Lagerstyring | [Lagrede visninger for lastbehandling](saved-views-scm.md) | Aktivert som standard |
| Lagerstyring | [Lagrede visninger for forsendelsesbehandling](saved-views-scm.md) | Aktivert som standard |
| Lagerstyring | [Detaljer om satsvis bølgejobb](../warehousing/wave-processing.md) | Aktivert som standard |
| Lagerstyring | [Varslinger for bølgekjøring](../warehousing/wave-execution-notifications.md) | Aktivert som standard |

## <a name="additional-resources"></a>Tilleggsressurser

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformoppdateringer for økonomi- og driftsapper

Microsoft Dynamics 365 Supply Chain Management 10.0.25 inkluderer plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.25 av økonomi- og driftsapper (april 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md).

### <a name="bug-fixes"></a>Feilrettinger

Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av 10.0.25, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 og bransjeskyer: plan for lanseringsbølge 1 for 2022

Er du spent på kommende og nylig utgitte tilleggspakkefunksjoner i våre bedriftsprogrammer eller -plattform?

Sjekk ut [Dynamics 365 og bransjeskyer: plan for lanseringsbølge 1 for 2022](/dynamics365-release-plan/2022wave1/). Vi har registrert alle detaljene, ende til ende, øverst til nederst, i et enkelt dokument som du kan bruke i planleggingen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og avskrevne funksjoner i Supply Chain Management

Emnet [Fjernede eller avskrevne funksjonene i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver funksjoner som er eller er planlagt å bli fjernet eller avskrevet for Supply Chain Management.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Før en funksjon fjernes fra produktet, vil avskrivningsvarselet bli kunngjort i emnet [Fjernede eller avskrevne funksjoner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder før fjerningen.

For oppdelingsendringer som bare påvirker kompileringstiden, men som er binære kompatible med sandkasse- og produksjonsmiljøer, vil avskrivningstiden være mindre enn 12 måneder. Dette er vanligvis funksjonelle oppdateringer som må gjøres på kompilatoren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

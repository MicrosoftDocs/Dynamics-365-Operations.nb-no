---
title: Parametere som ikke brukes av planleggingsoptimalisering
description: Dette emnet viser parametrene som Planleggingsoptimalisering ikke vurderer under operasjonen.
author: crytt
ms.date: 6/29/2021
ms.topic: article
ms.search.form: ReqParameters, ReqGroup, ReqItemTable, ReqPlanSched, EcoResProductDetailsExtended, InventItemOrderSetup, WorkCalendarTable, PdsDispositionMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-29
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4d459f4de67f26f36aabcbde015988132e957601
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361352"
---
# <a name="parameters-not-used-by-planning-optimization"></a>Parametere som ikke brukes av planleggingsoptimalisering

[!include [banner](../../includes/banner.md)]

Dette emnet viser parametrene som Planleggingsoptimalisering ikke vurderer under operasjonen. Planleggingstjenesten kan hoppe over en parameter fordi for eksempel relatert funksjonalitet ikke er støttet ennå. Parameteren kan eventuelt ha blitt foreldet på grunn av funksjonsendringer.

I delene nedenfor finner du en oversikt over parametere som planleggingsoptimalisering ikke bruker på bestemte sider. De forklarer også hvorfor hver parameter ikke brukes.

## <a name="master-planning-parameters-page"></a>Hovedplanleggingsparametere-side

Planleggingsoptimalisering bruker ikke følgende parametere eller alternativer på siden **Hovedplanleggingsparametere**:

- **Generelt**-fanen:

    - **Gjeldende prognoseplan** – Venter på *prognose*-støtte.
    - **Gjeldende statisk hovedplan** – Venter på *Kopier statisk til dynamisk plan*-støtte.
    - **Gjeldende dynamisk hovedplan** – Venter på *Kopier statisk til dynamisk plan*-støtte.
    - **Kopier den fullstendige og oppdaterte statiske hovedplanen til den dynamiske hovedplanen** – Venter på *Kopier statisk til dynamisk plan*-støtte.
    - **Starttid for beregnede forsinkelser** – Venter på støtte for *Beregnede forsinkelser*.
    - **Bruk dynamiske negative dager** – Planleggingsoptimalisering bruker alltid metoden *Dynamiske negative dager*.
    - **Dagens datokalender** – Venter på støtte for *Planlegging*.
    - **Bruk av hurtigminne** – Konfigurasjonen av abonnementet på Microsoft Azure håndterer ytelsespunkt.
    - **Antall oppgaver i oppgavebunt for hjelper** – Azure-abonnementskonfigurasjonen håndterer ytelsespoeng.
    - **Forhåndsbehandling: Filtrer automatisk etter varer med direkte behov** – Azure-abonnementskonfigurasjonen håndterer ytelsespunkt.
    - **Etterbehandling: Filtrer automatisk etter varer med direkte behov** – Azure-abonnementskonfigurasjonen håndterer ytelsespunkt.
    - **Antall ordrer i autoriseringsbunt** – Azure-abonnementskonfigurasjonen håndterer ytelsespoeng.
    - **Antall tråder** – Azure-abonnementskonfigurasjonen håndterer ytelsespoeng.
    - **Tidsavbrudd for planleggingsprosess i minutter** – Azure-abonnementskonfigurasjonen håndterer ytelsespoeng.
    - **Planleggingens starttid** – Venter på støtte for *Planlegging*.

- Fanen **Planlagte bestillinger**:

    - **Mottakstidspunkt** – Venter på støtte for *Planlegging*.
    - **Produksjon** – Venter på støtte for *Planlegging*.
    - Felt i **Prosjekt**-delen – Venter på støtte for *Planlegging*.

- Fanen **Standardoppdatering**:

    - **Oppdater merking** – Venter på *Autorisasjon*-støtte.
    - **Avbryt autorisasjon ved feil** – Venter på *Autorisasjon*-støtte.
    - **Grupper etter leverandør** – Venter på *Autorisasjon*-støtte.
    - **Grupper etter innkjøpergruppe** – Venter på *Autorisasjon*-støtte.
    - **Grupper etter innkjøpsavtale** – Venter på *Autorisasjon*-støtte.
    - **Grupper etter periode** – Venter på *Autorisasjon*-støtte.
    - **Søk etter kjøpsavtaler** – Venter på *Autorisasjon*-støtte.
    - **Grupper etter planleggingsprioritet** – Venter på *Autorisasjon*-støtte.
    - **Grupper etter periode** – Venter på *Autorisasjon*-støtte.

## <a name="coverage-groups-page"></a>Dekningsgrupper-siden

Planleggingsoptimalisering bruker ikke følgende parametere eller alternativer på siden **Dekningsgrupper**:

- Hurtigfanen **Generelt**:

    - **Positive dager** – Venter på *Positive dager*-støtte.
    - **Bruk lagerbeholdning** – Venter på støtte for *Bruk av lagerbeholdning*.
    - **Bruk den angitte stykklisten eller formelversjonen** – Venter på støtte for *Formelversjoner med ko-/biprodukt*.
    - **Bruk den angitte ruteversjonen** – Venter på støtte for *Behov med angitt stykkliste eller definerte rutekrav*.

- **Handling**-hurtigfanen:

    - **Handlingsmelding** – Venter på *Handlinger*-støtte.
    - **Handlingshorisont bakover** – Venter på *Handlinger*-støtte.
    - **Utsettelsesmargin** – Venter på *Handlinger*-støtte.
    - **Fremskyndingsmargin** – Venter på *Handlinger*-støtte.
    - **Basisdato** – Venter på *Handlinger*-støtte.
    - **Fremskynd** – Venter på *Handlinger*-støtte.
    - **Utsett** – Venter på *Handlinger*-støtte.
    - **Nedskriv** – Venter på *Handlinger*-støtte.
    - **Oppskriv** – Venter på *Handlinger*-støtte.
    - **Avledede handlinger** – Venter på *Handlinger*-støtte.

- **Annet**-hurtigfanen:

    - **Låsningshorisont (dager)** – *Låsningshorisont*-støtte er ikke planlagt i Planleggingsoptimalisering.
    - **Nedbrytningshorisont for stykkliste (dager)** – Venter på *Planlegging*-støtte.
    - **Kapasitetsplanleggingshorisont (dager)** – Venter på *Planlegging*-støtte.
    - **Godkjent rekvisisjonshorisont (dager)** – Venter på *Rekvisisjon*-støtte.
    - **Tidshorisont for prognoseplan** – Venter på *prognose*-støtte.

- **Forsinkelser**-hurtigfanen:

    - **Beregnede forsinkelser** – Venter på støtte for *Beregnede forsinkelser*.
    - **Tidshorisont for beregnede forsinkelser** – Venter på støtte for *Beregnede forsinkelser*.

## <a name="item-coverage-page"></a>Siden Varedekning

Planleggingsoptimalisering bruker ikke følgende parametere eller alternativer på siden **Varedekning**:

- **Generelt**-fanen:

    - **Type planlagt bestilling** – Planleggingsoptimalisering støtter ikke *Kanban*-alternativet, venter på *Kanban*-støtte.
    - **Låsningshorisont (dager)** – *Låsningshorisont*-støtte er ikke planlagt i Planleggingsoptimalisering.
    - **Nedbrytningshorisont for stykkliste (dager)** – Venter på *Planlegging*-støtte.
    - **Kapasitetsplanleggingshorisont (dager)** – Venter på *Planlegging*-støtte.
    - **Godkjent rekvisisjonshorisont (dager)** – Venter på *Rekvisisjon*-støtte.
    - **Fyll opp minimum** – Planleggingsoptimalisering støtter ikke alternativene *Dagens dato*, *Første avgang* og *Dekningshorisont*. Den bruker alltid alternativet *Dagens dato + leveringstid*.
    - **Minimumsperioder** – Venter på støtte for *Minimumslagernivå*.
    - **Planleggingsformel** – Venter på støtte for *Formelversjoner med ko-/biprodukter*.
    - **Standardprioritet** – Venter på støtte for *Formelversjoner med ko-/biprodukter*.
    - **Gjeldende prioritet** – Venter på støtte for *Formelversjoner med ko-/biprodukter*.
    - **Endret data** – Venter på støtte for *Formelversjoner med ko-/biprodukter*.
    - **Bruk lagerbeholdning** – Venter på støtte for *Bruk av lagerbeholdning*.

## <a name="master-plans-page"></a>Hovedplaner-siden

Planleggingsoptimalisering bruker ikke følgende parametere eller alternativer på siden **Hovedplaner**:

- Hurtigfanen **Generelt**:

    - **Ta med lagerbeholdninger** – Venter på støtte for *Bruk av lagerbeholdning*.
    - **Overstyr lagerbeholdning** – Venter på støtte for *Bruk av lagerbeholdning*.
    - **Bruk lagerbeholdning** – Venter på støtte for *Bruk av lagerbeholdning*.
    - **Ta med lagertransaksjoner** – Venter på støtte for *Bruk av lagerbeholdning*.
    - **Ta med salgstilbud** – Venter på *Salgstilbud*-støtte.
    - **Inkluder tilbudsforespørsler** – Venter på støtte for *Tilbudsforespørsel*.
    - **Bruk holdbarhetsdatoer** – Venter på *Holdbarhet*-støtte.
    - **Inkluder kontinuitetsplan** – Venter på støtte for *Kontinuitetsplanlegging*.
    - **Planleggingsmetode** – Venter på støtte for *Planlegging*.
    - **Begrenset egenskap** – Venter på *Planlegging*-støtte.
    - **Horisont for kapasitet for planlegging bakover** – Venter på *Planlegging*-støtte.
    - **Begrenset kapasitet** – Venter på *Planlegging*-støtte.
    - **Horisont for begrenset kapasitet** – Venter på *Planlegging*-støtte.
    - **Begrenset kapasitet for flaskehalsressurser** – Venter på *Planlegging*-støtte.
    - **Kapasitetshorisont for flaskehalsressurser** – Venter på *Planlegging*-støtte.
    - **Planlagte bestillinger** – Planleggingsoptimalisering bruker faste nummerserier.
    - **Økt** – Planleggingsoptimalisering bruker faste nummerserier.
    - **Kontinuitetsplan** – Planleggingsoptimalisering bruker faste nummerserier.

- Hurtigfanen **Horisonter i dager**:

    - **Låsning** – *Låsningshorisont*-støtte er ikke planlagt i Planleggingsoptimalisering.
    - **Nedbryting** – Venter på støtte for *Planlegging*.
    - **Prognoseplan** – Venter på ekstra *prognose*-støtte.
    - **Kapasitet** – Venter på *Planlegging*-støtte.
    - **Kontinuitetsplan** – Venter på støtte for *Kontinuitetsplanlegging*.
    - **Handlingsmelding** – Venter på *Handlinger*-støtte.
    - **Beregnede forsinkelser** – Venter på ekstra støtte for *Beregnede forsinkelser*.
    - **Sekvensering** – Venter på støtte for *Produksjon*.

- **Beregnede forsinkelser**-hurtigfanen:

    - **Kontroller at de planlagte ordrene ikke opprettes før kjøredatoen for hovedplanlegging** – Venter på *Beregnede forsinkelser*.
    - **Legg til den beregnede forsinkelsen i behovsdatoen** (i delen **Planlagte bestillinger**) – Venter på *Beregnede forsinkelser*.
    - **Legg til den beregnede forsinkelsen i behovsdatoen** (i delen **Planlagte produksjonsordrer**) – Venter på *Beregnede forsinkelser*.
    - **Legg til den beregnede forsinkelsen i behovsdatoen** (i delen **Planlagt overføring**) – Venter på *Beregnede forsinkelser*.
    - **Legg til den beregnede forsinkelsen i behovsdatoen** (i delen **Planlagt Kanban**) – Venter på *Beregnede forsinkelser*.

- **Sekvensiering**-hurtigfanen:

    - **Sekvens for planlagte ordrer etter hovedplanlegging** – Venter på støtte for *Sekvensiering*.
    - **Samlingstype** – Venter på *Sekvensiering*-støtte.
    - **Periodetype** – Venter på *Sekvensiering*-støtte.
    - **Antall perioder i kampanjesyklusen** – Venter på støtte for *Sekvensiering*.

## <a name="released-product-details-page"></a>Siden Detaljer om frigitt produkt

Planleggingsoptimalisering bruker ikke følgende parameteralternativ på siden **Detaljer om frigitt produkt**:

- **Utvikle**-hurtigfanen:

    - **Produksjonstype** – Planleggingsoptimalisering støtter ikke alternativet *Planleggingselement*, venter på støtte for *Planleggingselementer*.

## <a name="default-order-settings-page"></a>Siden Standard ordreinnstillinger

Planleggingsoptimalisering bruker ikke følgende parameteralternativ på siden **Standard ordreinnstillinger**:

- **Beholdning**-hurtigfanen:

    - **Leveringsdatokontroll** – Planleggingsoptimalisering støtter ikke *CTP*-alternativet, venter på *CTP*-støtte.

## <a name="working-time-calendars-page"></a>Siden Arbeidstidskalendere

Planleggingsoptimalisering bruker ikke følgende parameter på siden **Arbeidstidskalendere**:

- **Basiskalender** – Venter på støtte for *Basiskalendere*.

## <a name="batch-disposition-master-page"></a>Siden Partidisposisjonsstandard

Planleggingsoptimalisering bruker ikke følgende parameter på siden **Partidisposisjonsstandard**:

- **Oppsett**-hurtigfanen:

    - **Nettbar** – Venter på støtte for *Partidisposisjonskoder*.
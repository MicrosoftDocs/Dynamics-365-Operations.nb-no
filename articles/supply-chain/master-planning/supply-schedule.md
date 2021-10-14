---
title: Forsyningsplan
description: Dette emnet inneholder informasjon om forsyningsplansiden og de tilhørende funksjonene.
author: ChristianRytt
ms.date: 9/3/2021
ms.topic: article
ms.search.form: ReqSupplyDemandSchedule, ReqSupplyDemandScheduleFilters, ReqSupplyDemandItemDetails, ReqTransFuturesActionsPart, ReqSupplyDemandOverviewLegendPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0d2f0f38d86ae307ef80bd02901e19a08d5e30ae
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578374"
---
# <a name="supply-schedule"></a>Forsyningsplan

[!include [banner](../includes/banner.md)]

**Forsyningsplan**-siden viser en omfattende oversikt over tilbud og etterspørsel etter et produkt eller en produktserie. Informasjonen filtreres etter lokasjon, hovedplan og perioder. Du kan også bruke siden til å opprette nye ordrer, endre eksisterende planlagte ordrer og kjøre hovedplanlegging.

## <a name="open-the-supply-schedule-page"></a>Åpne Forsyningsplan-siden

Du kan åpne siden **Forsyningsplan** på en av følgende måter:

- Gå til **Hovedplanlegging \> Hovedplanlegging \> Forsyningsplan**. Angi planen og produktet du vil bruke, i dialogboksen **Endre filter**, ved å angi filterverdier i feltene som vises. (I resten av dette emnet kalles samlingen med filterverdier du angi, "filteret" eller "det gjeldende filteret".) Velg **OK** når du er ferdig.
- Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**. Velg eller åpne et produkt. I handlingsruten, i **Plan**-fanen og **Visning**-gruppen, velger du **Forsyningsplan**.
- Gå til **Hovedplanlegging \> Oppsett \> Behovsprognose \> Varefordelingsnøkler**. Velg en varetildelingsnøkkel som brukes som en produktserie. Velg deretter **Forsyningsplan** i handlingsruten.
- Gå til **Hovedplanlegging \> Hovedplanlegging \> Planlagte ordrer**. Velg eller åpne en planlagt ordre. I handlingsruten, i **Visning**-fanen og **Visning**-gruppen, velger du **Forsyningsplan**.

> [!NOTE]
> Når du åpner **Forsyningsplan**-siden fra et produkt, en produktserie eller en planlagt bestilling, trenger du ikke angi filterverdier. Systemet vil bruke standard periodemalen.

## <a name="use-the-supply-schedule-page"></a>Bruke Forsyningsplan-siden

**Forsyningsplan**-siden består av en øvre del, hurtigfanen **Beholdning ved periodeslutt**, en ekstra hurtigfane som blir synlig basert på linjen som er valgt i den øvre delen, og Faktaboks-ruten. (Hvis du vil åpne Faktaboks-ruten og vise en Faktaboks, velger du **Beslektet informasjon** til høyre på siden.)

### <a name="upper-section"></a>Øvre del

Den øvre delen av **Forsyningsplan**-siden inneholder et rutenett som viser følgende data for et produkt eller en produktserie. Disse dataene deles inn etter perioder som er definert av **Periodemal**-verdien fra filteret.

- **Beholdning for periodestart** – Denne linjen viser den forventede lagersaldoen ved begynnelsen av perioden hvis alle ordrene i systemet forekommer.
- **Beholdning for periodeslutt** – Denne linjen viser den forventede lagersaldoen ved slutten av perioden hvis alle ordrene i systemet forekommer.
- **Tilsluttet lager ved periodeslutt** – Denne linjen viser lagermengden på slutten av perioden som er utligning mot fremtidig behov.
- **Nettoforsyning for periode** – Denne linjen viser forskjellen mellom tilbud og etterspørsel i perioden.
- **Minimumslager** – Denne noden viser sikkerhetslager for et produkt eller en produktserie. Hvis du vil utvide eller trekke sammen denne noden, merker du den og velger **Vis** eller **Skjul** på verktøylinjen. Denne noden vises bare når det finnes sikkerhetslager for produktet eller produktserien.
- **Etterspørsel** – Denne noden viser etterspørsel etter et produkt eller en produktserie. Behovet grupperes etter transaksjonstype. Hvis du vil utvide eller trekke sammen denne noden, merker du den og velger **Vis** eller **Skjul** på verktøylinjen. Behovstransaksjonstyper omfatter salg, overføringer og lagerjournaler. Denne noden vises bare når det finnes etterspørsel etter produktet eller produktserien.
- **Forsyning** – Denne noden viser forsyning for et produkt eller en produktserie. Forsyningen grupperes etter transaksjonstype. Hvis du vil utvide eller trekke sammen denne noden, merker du den og velger **Vis** eller **Skjul** på verktøylinjen. Forsyningstransaksjonstyper omfatter produksjon, innkjøp og overføringer. Denne noden vises bare når det finnes forsyning for produktet eller produktserien.

Mange av de tilgjengelige verktøylinjeknappene, Faktaboks-visningene og hurtigfanevisningene avhenger av hva du har valgt i den øvre delen. Vanligvis vil du velge en transaksjonstype ved å merke én av radene under **Forsyning**- eller **Behov**-noden. Deretter velger du en periode ved å velge en bestemt kolonne for den valgte raden.

Verktøylinjen over rutenettet i den øvre delen av **Forsyningsplan**-siden inneholder følgende knapper:

- **Vis/skjul** – Utvid eller skjul en valgt node, for eksempel **Behov**-noden, **Forsyning**-noden og deres undernoder. (Noder viser et **\[+\]**- eller **\[-\]**-prefiks for å angi om de er skjult eller utvidet.)
- **Ny** – Åpne en meny der hver kommando igjen åpner en dialogboks eller en side der du kan legge til en bestemt type vare for valget. Tilgjengelige kommandoer omfatter **Prognoseforsyning**, **Planlagt bestilling**, **Planlagt kanban**, **Ny produksjonsordre**, **Bestilling** og **Overføringsordre**.
- **Hovedplanlegging** – Kjør hovedplanlegging. Det vises en dialogboks der du kan angi planen som skal kjøres. Som standard settes feltet **Hovedplan** for å samsvare med gjeldende filter.
- **Ferdigmeldingsmaks** – Åpne siden **Ferdigmeldingsmaks** for produktet som er definert i det gjeldende filteret.
- **Oppdater planlagte bestillinger** – Åpne siden **Planlagte bestillinger**, som viser planlagte bestillinger for produktet eller produktserien som er definert i det gjeldende filteret.
- **Nivå** – Fordel planlagte ordrer i henhold til innstillingene fra dialogboksen som vises.
- **Materialplanpolicy etter lokasjon** – Åpne **Varedekning** for siden for produktet som er definert i det gjeldende filteret.
- **Kanban-regel** – Åpne **Kanban-regel**-siden for produktet som er definert i det gjeldende filteret.

### <a name="fasttabs"></a>Hurtigfaner

**Forsyningsplan**-siden kan inneholde følgende hurtigfaner:

- **Beholdning for periodeslutt** – Denne hurtigfanen viser periodesluttlagerdataene i et grafisk format.
- **Forsyningsprofil** – Denne hurtigfanen viser forsyningsdataene i et grafisk format. Den blir synlig når du velger en **Forsyning**-node eller en linje under den i den øvre delen.
- **Sammendrag** – Denne hurtigfanen viser sammendragsdetaljer som er knyttet til transaksjonstypen du har valgt i den øvre delen. Hvis du for eksempel velger **Salg** under **Behov**-noden, viser denne hurtigfanen felt som er knyttet til salgsordrer, for eksempel **Ønskede salgsordrelinjer** eller **Totalbeløp**. Hvis du velger **Produksjonsordrer** under undernoden **Produksjon** i noden **Forsyning**, viser denne hurtigfanen felt som er knyttet til produksjonsordrer, for eksempel **Planlagte produksjonsordrer** eller **Totaltplanlagt**. Feltverdier avhenger av perioden du har valgt i den øvre delen. 
- **\[Transaksjonstype\] - \[Periode\]** – Denne hurtigfanen viser ordrer for transaksjonstypen og perioden du valgte i den øvre delen. Navnet på hurtigfanen gjenspeiler de valgene. Den kan for eksempel ha navnet **Salgsordrer – Restanse** eller **Produksjonsordrer – uke 37**.

### <a name="action-pane"></a>Handlingsrute

Følgende knapper er tilgjengelige i handlingsruten:

- **Endre filter** – Åpne dialogboksen **Endre filter**, der du kan oppdatere filterverdier og deretter åpne **Forsyningsplan**-siden på nytt, som inneholder de oppdaterte filterinnstillingene.
- **Vis forsinkelser** – Uthev de relevante linjene i den øvre delen hvis det er en forsinket ordre av denne transaksjonstypen.

### <a name="factbox-pane"></a>Faktaboksrute

Hvis du vil åpne Faktaboks-ruten og vise en Faktaboks, velger du **Beslektet informasjon** til høyre på siden. Følgende faktabokser er tilgjengelige på **Forsyningsplan**-siden:

- **Varedetaljer** – Denne faktaboksen viser grunnleggende informasjon om produktet som er definert i det gjeldende filteret. Den er tom hvis du har definert en produktserie i filteret.
- **Handlinger** – Denne faktaboksen viser handlinger for bestillinger av transaksjonstypen som du valgte i øvre del.
- **Forsinkelser** – Denne faktaboksen viser forsinkelser for bestillinger av transaksjonstypen som du valgte i øvre del.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

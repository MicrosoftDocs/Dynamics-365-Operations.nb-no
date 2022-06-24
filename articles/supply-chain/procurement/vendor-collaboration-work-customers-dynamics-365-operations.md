---
title: Leverandørsamarbeid med kunder
description: Denne artikkelen beskriver hvordan du kan bruke leverandørsamarbeid for å arbeide med bestillinger og overvåke forsendelseslager.
author: GalynaFedorova
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart, VendVendorProfileCard, PurchVendorPortalAllResponse, PurchVendorPortalPendingResponsesPart, PurchVendorPortalResponses, PurchVendorPortalConfirmedOpenOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4e5748f2368376ee03f280f1487d1de65250d3a4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859176"
---
# <a name="vendor-collaboration-with-customers"></a>Leverandørsamarbeid med kunder

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du kan bruke leverandørsamarbeid for å arbeide med kunder i Microsoft Dynamics 365 Supply Chain Management. Leverandører kan utføre en rekke forretningsprosesser fra følgende arbeidsområder:

- **Bestillingsbekreftelse** – overvåke og svare på bestillinger (POs).
- **Leverandørbud** – vise tilbudsforespørsler (RFQ-er), og svare på dem ved å legge inn bud.
- **Leverandørinformasjon** – vise og oppdatere hoveddata for leverandør.
- **Fakturering** – arbeide med fakturaer. Denne artikkelen dekker ikke arbeidsområdet **Fakturering**. Hvis du vil ha mer informasjon om dette arbeidsområdet, kan du se [Arbeidsområde for leverandørsamarbeidsfakturering](../../finance/accounts-payable/vendor-portal-invoicing-workspace.md).

Leverandører kan også overvåke informasjon om forsendelseslager.

## <a name="working-with-pos-in-the-purchase-order-confirmation-workspace"></a>Arbeide med bestillinger i arbeidsområdet Bestillingsbekreftelse

I arbeidsområdet **Bestillingsbekreftelse** kan du svare på bestillingene som er sendt til deg for gjennomgang. Du kan også vise informasjon om bestillinger som venter på handling fra kunden og bestillinger som er bekreftet, men fremdeles er åpne.

Det er tre lister i arbeidsområdet **Bestillingsbekreftelsen**:

- **Bestillinger for vurdering** – Denne listen viser bestillinger som er sendt til deg og venter på svar fra deg. Når du har svart, forsvinner bestillingen fra listen. Hvis kunden sender deg en ny versjon av bestillingen før du har svart på den forrige versjonen, vises bare den nyeste versjonen.
- **Venter på kundehandling** – Denne listen inneholder alle bestillinger som du har svart på, men som kunden ennå ikke har bekreftet. Hvis du godtar en bestilling, kan du overvåke den i denne listen til statusen er endret til **Bekreftet**. Hvis du avviser en bestilling eller godtar den med endringer, kan du overvåke den her til kunden sender en ny versjon.
- **Åpne bekreftede bestillinger** – Denne listen inneholder alle bestillingene for kontoen som har statusen **Bekreftet**. Når produkter eller tjenester er fullstendig mottatt mot bestillingen, forsvinner bestillingen fra listen.

Du kan bruke følgende sider til å arbeide med bestillinger:

- **Bestillinger for vurdering** – Denne siden inneholder samme informasjon som listen **Bestillinger for vurdering** i arbeidsområdet. Se beskrivelsen tidligere i denne artikkelen.
- **Logg for leverandørbekreftelse for bestilling** – Denne siden inneholder alle bestillinger og alle versjoner av bestillinger som er sendt til leverandøren. Den inneholder også alle svarene som er returnert fra leverandøren.
- **Åpne bekreftede bestillinger** – Denne siden inneholder samme informasjon som listen **Åpne bekreftede bestillinger** i arbeidsområdet. Se beskrivelsen tidligere i denne artikkelen.
- **Alle bekreftede bestillinger** – Denne siden inneholder alle bestillinger som er bekreftet. Bestillingene som vises på denne siden, omfatter bestillinger der produkter eller tjenester er mottatt. Du kan bruke denne listen til å overvåke bestillinger som du kan sende fakturaer for.

### <a name="responding-to-pos"></a>Svare på bestillinger

Bestillingene som kunden sender til deg for gjennomgang, vises i arbeidsområdet **Bestillingsbekreftelse** og på siden **Bestillinger for vurdering**. Når du har åpnet en bestilling, kan du godta den, avvise den eller godta den med endringer. Det kan være vedlegg i bestillingshodet eller på de enkelte linjene. Du kan også legge til informasjon i svaret på bestillingshodet eller enkeltlinjer. Du kan for eksempel foreslå en erstatningsvare for én av linjene.

Du kan forhåndsvise og skrive ut bestillingen som en PDF-fil ved hjelp av alternativet **Forhåndsvis/Skriv ut**. Du kan bruke handlingen **Visningsdimensjoner** til å vise eller skjule følgende dimensjonskolonner: **Område**, **Lager**, **Farge**, **Størrelse**, **Stil** og **Konfigurasjon**. 

Hvis du bruker alternativet **Godta med endringer**, kan du godta eller avvise enkeltlinjer. Du kan også foreta følgende endringer i linjer:

- Endre datoer eller antall. Hvis du vil oppdatere den bekreftede leveringsdatoen på alle linjene, kan du bruke alternativet **Oppdater leveringsdato** i bestillingshodet.
- Dele linjer for ulike leveringsdatoer eller antall.
- Erstatte en vare. Under **Linjedetaljer** angir du en varebeskrivelse og varenummeret i **Ekstern**-feltet.

Du kan ikke endre prisinformasjon eller gebyrer, men du kan bruke merknader til å komme med forslag for disse endringene.

Hvis kunden sender deg en ny versjon av en bestilling, vil denne ha et versjonssuffiks for å angi at det er en endret versjon av en bestilling som tidligere ble sendt. På siden **Logg for leverandørbekreftelse for bestilling** kan du spore historikken for hver ordre.

## <a name="monitoring-consignment-inventory"></a>Overvåke forsendelseslager

Hvis du bruker forsendelseslager, kan du bruke grensesnittet for leverandørsamarbeid til å vise informasjon på følgende sider:

- **Bruk av forsendelseslager for bestillinger** – Bestillinger for forsendelseslager genereres når kunden blir eier av lageret. Disse bestillingene for forsendelse vises bare på denne siden. De er ikke inkludert på siden **Alle bekreftede bestillinger**.
- **Produkter mottatt fra forsendelseslager** – Denne siden viser alle transaksjoner der eierskapet for produkter er blitt overført til firmaet som bruker lageret. Du kan bruke denne informasjonen for fakturere kunden.
- **Forsendelseslager for beholdning** – Denne siden viser forsendelseslageret for beholdning som eies av firmaet, men som er på lager på kundens lager.

## <a name="working-with-rfqs-in-the-vendor-bidding-workspace"></a>Arbeide med tilbudsforespørsler i arbeidsområdet Leverandørbud

I arbeidsområdet **Leverandørbud** kan du vise tilbudsforespørsler som firmaet ditt har blitt invitert til å svare på. Du kan også svare på tilbudsforespørsler.

Arbeidsområdet viser også alle tilbudsforespørsler som du har tapt eller vunnet. Hvis systemet er konfigurert for offentlig sektor, vises dessuten tilbudsforespørsler som er offentlig tilgjengelige, i arbeidsområdet.

### <a name="viewing-rfqs"></a>Vise tilbudsforespørsler

Åpne arbeidsområdet **Leverandørbud** for å få tilgang til følgende informasjon:

- Velg **Invitasjoner til nytt bud** for å se tilbudsforespørsler som firmaet ditt har blitt invitert til å svare på. Herfra kan du vise en tilbudsforespørsel og starte budgivningsprosessen. Du kan også se endrede tilbudsforespørsler som et nytt bud må sendes inn for.
- Velg **Returnerte bud** for å se tilbudsforespørsler som kunden har returnert til deg, slik at du kan oppgi mer informasjon eller oppdatere budet.
- Velg **Bud som utføres** for å se tilbudsforespørsler som du eller en kontaktperson som representerer firmaet ditt, har arbeidet med, men ennå ikke sendt.
- Velg **Tildelte bud** for å se når kunden har vunnet minst ett linjeelement i budet.
- Velg **Tapte bud** for å se bud der alle linjer er avvist.
- Velg koblingen **Tilbudsforespørsler** koblingen for å se en liste over alle invitasjoner til tilbudsforespørsler fra leverandøren og alle bud som er sendt. På siden **Tilbudsforespørsler** vises alle tilbudsforespørsler som en leverandør har vært involvert i. Du kan søke etter status.
- Velg koblingen **Avslåtte bud** for å se en liste over alle tilbudsforespørsler der en leverandørs kontakt har avslått å by.

### <a name="working-with-rfqs-that-are-publicly-available"></a>Arbeide med tilbudsforespørsler som er offentlig tilgjengelig

Personer som arbeider i offentlig sektor, kan se åpne og utløpte tilbudsforespørsler som er gjort tilgjengelig for offentligheten.

- Velg koblingen **Åpne publiserte tilbudsforespørsler** for å se en liste over åpne tilbudsforespørsler som er tilgjengelige for offentligheten. En åpen tilbudsforespørsel er en tilbudsforespørsel som ennå ikke er utløpt. Du kan finne utløpsdatoen og -klokkeslettet i hodet i tilbudsforespørselen.

    Hvis du er invitert til å by, finner du den samme tilbudsforespørselen på siden **Invitasjoner til nytt bud**. Noen ganger vil du kanskje by på en åpen tilbudsforespørsel, men du har ikke blitt invitert til å by. Du kan i så fall kanskje invitere deg selv, forutsatt at kunden har aktivert personlig invitasjon for tilbudsforespørselssaken. 

    Siden **Invitasjoner til nytt bud** kan ha et filter som lar deg vise de åpne tilbudsforespørslene, og identifisere de som inneholder linjer som samsvarer med de godkjente innkjøpskategoriene. For å gjøre dette filteret tilgjengelig må du aktivere funksjonen *La leverandører søke etter tilbudsforespørsler etter innkjøpskategori* i systemet. Administratorer kan bruke **Funksjonsbehandling**-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:

    - **Modul:** *Leverandører*
    - **Funksjonsnavn:** *La leverandører søke etter tilbudsforespørsler etter innkjøpskategori* <!-- KFM: I don't see this here, is this right? -->

    Du kan forbedre tilgjengeligheten til koblingen **Åpne publiserte tilbudsforespørsler** ved å aktivere funksjonen *Vis Åpne publiserte tilbudsforespørsler-koblingen som en flis*. Denne funksjonen konverterer koblingen til en flis og flytter den til en fremtredende plassering, slik at den er lett å finne. Administratorer kan bruke **Funksjonsbehandling**-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. (Per Supply Chain Management versjon 10.0.21 er funksjonen aktivert som standard.) Der vises funksjonen på følgende måte:

    - **Modul:** *Innkjøp og leverandører*
    - **Funksjonsnavn:** *Vis koblingen Åpne publiserte tilbudsforespørsler som en flis*

- Velg koblingen **Lukkede publiserte tilbudsforespørsler** for å se en liste over lukkede tilbudsforespørsler som er tilgjengelige for offentligheten. En lukket tilbudsforespørsel er en tilbudsforespørsel som er utløpt. Du kan finne utløpsdatoen og -klokkeslettet i hodet i tilbudsforespørselen.

    En lukket tilbudsforespørsel viser alle leverandørbudene ned til linjenivå. Når bud er tildelt eller avvist, vises denne informasjonen i den lukkede tilbudsforespørselen. Vedlegg som er inkludert i budet, er også tilgjengelige.

> [!NOTE]
> Denne funksjonaliteten er bare tilgjengelig hvis konfigurasjon for offentlig sektor er aktivert.

### <a name="bidding"></a>Legge inn bud

- Velg **Bud** for å by på en tilbudsforespørsel.

    Når redigering er aktivert for budfelt i hodene og linjene i en tilbudsforespørsel, kan du angi budet direkte i rutenettet. Du må også vurdere ekstra budinformasjon som skal legges til i linjedetaljene.

    Når du begynner å arbeide med et bud, vises det i delen **Bud som utføres**.

    Du kan lagre et bud når som helst før utløpsdatoen. Du kan deretter gå tilbake senere for å fullføre og avgi budet. Når du har sendt et bud, kan du kalle det tilbake og oppdatere det frem til utløpsdatoen.

- Velg **Tilbakestill fra tilbudsforespørsel** for å tilbakestille dataene du angav for et bud og gå tilbake til den opprinnelige tilbudsforespørselen. Du kan tilbakestille hodet eller linjen.
- Velg **Legg til alternativ** eller **Fjern alternativ** i rutenettet for å arbeide med alternativer.

    Noen tilbudsforespørsler tillater alternative bud. Du kan angi alternative bud bare for linjer av typen **Kategori**, fordi enkelte varer ikke kan legges til som alternativer. 

- Velg **Vedlegg for tilbudsforespørsel** eller **Vedlegg for linjer i tilbudsforespørsel** for å åpne vedlegg som kunden har lagt til i en tilbudsforespørsel. Velg **Vedlegg i bud** eller **Vedlegg på budlinje** for å laste opp vedlegg sammen med budet.

    Det kan være spørreskjemaer som du må svare før du kan sende et bud.

- Velg **Avslå** hvis du ikke vil by. Når du har valgt **Avslå**, kan du ikke kalle tilbake handlingen og angi et bud.

Hvis en tilbudsforespørsel er endret, må du angi et nytt bud. Du finner informasjon om endringen på fanen **Endringer** på siden for tilbudsforespørselen. Endrede tilbudsforespørsler vises på siden **Invitasjoner til nytt bud**.

## <a name="accessing-vendor-master-data-in-the-vendor-information-workspace"></a>Tilgang til hoveddata for leverandør i arbeidsområdet Leverandørinformasjon

Som en leverandør kan du få tilgang til deler av informasjonen som kunden opprettholder, i den hovedoppføringen for leverandøren. Derfor kan du holde informasjonen oppdatert. Hvis du vil oppdatere informasjonen, må en rolle som leverandøradministrator (ekstern).

Tilgjengelig informasjon er leverandørnavnet, adresser, kontaktinformasjon, kontaktpersoner og deres kontaktinformasjon, ID-numre, mva-numre, innkjøpskategorier som leverandøren er godkjent for å selge til kunden, og informasjon om sertifisering.

## <a name="additional-resources"></a>Tilleggsressurser

[Administrere brukere av leverandørsamarbeid](manage-vendor-collaboration-users.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

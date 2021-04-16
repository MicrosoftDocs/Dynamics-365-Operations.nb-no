---
title: Forskuddsbetalte fakturaer i forhold til forskuddsbetalinger
description: Dette emnet inneholder beskriver og viser forskjellene mellom de to metodene som organisasjoner kan bruke for forskuddsbetaling.
author: abruer
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64301ac540ce2e6e914b6b23668fddeb295ef84c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827992"
---
# <a name="prepayment-invoices-vs-prepayments"></a>Forskuddsbetalte fakturaer i forhold til forskuddsbetalinger

[!include [banner](../includes/banner.md)]

Dette emnet inneholder beskriver og viser forskjellene mellom de to metodene som organisasjoner kan bruke for forskuddsbetaling. Den ene metoden oppretter en forskuddsbetalt faktura som er knyttet til en bestilling. Den andre metoden oppretter journalbilag for forskuddsbetaling ved å lage journaloppføringer og merke dem som journalbilag for forskuddsbetaling.

Organisasjoner kan utstede forskuddsbetalinger til leverandører for varer eller tjenester før varene eller tjenestene er oppfylt. To metoder kan brukes til å utstede forskuddsbetalinger til leverandører. Hvis du vil redusere risikoen, kan du spore forskuddsbetalinger ved å definere forskuddsbetalingen på en bestilling. For denne metoden må du opprette en forskuddsbetalt faktura som er knyttet til en bestilling. Denne metoden kalles forskuddsfakturering. Organisasjoner som ikke vil følge opp forskuddsbetalinger så tett, eller ikke mottar en forskuddsbetalt faktura fra leverandøren, kan bruke journalbilag for forskuddsbetaling i stedet for faktureringsmåten forskuddsbetaling. Du kan opprette journalbilag for forskuddsbetaling ved å lage journaloppføringer og merke dem som journalbilag for forskuddsbetaling. Du kan ikke spore hvilke forskuddsbetalinger til en leverandør som gjøres mot hvilke bestillinger for denne metoden. Du kan imidlertid merke en postert forskuddsbetaling for utligning mot en bestilling.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Når du bruker forskuddsfakturering i forhold til forskuddsbetalinger

| Forskuddsfakturering                                                                | Forskuddsbetalinger                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Definer en verdi for forskuddsbetaling på bestillingen.                                    | Ingen verdi for forskuddsbetaling er definert på bestillingen.                    |
| En forskuddsfaktura og en sluttfaktura må posteres.                       | Ingen forskuddsfaktura må posteres.                                    |
| Ansvar for forskuddsbetalingen holdes på kontoen for forskuddsbetaling, ikke AP-kontoen. | Ansvar for forskuddsbetalingen holdes på AP-kontoen.                  |
| Leverandørsaldoen gjenspeiler ikke verdien forskuddsbetaling gjennom hele prosessen.     | Leverandørsaldoen gjenspeiler verdien forskuddsbetaling gjennom hele prosessen. |
| Forskuddsfakturering er bare tilgjengelig på leverandører.                         | Forskuddsbetalinger er tilgjengelig i Leverandører og Kunder.    |

## <a name="overview-of-the-prepayment-process"></a>Oversikt over forhåndsbetalingsprosessen
Regnskapspraksis i mange land/regioner krever at forskuddsbetaling fra en kunde eller til en leverandør ikke posteres til de vanlige samlekontoene for kunden eller leverandøren. I stedet posteres disse forskuddbetalingene til spesielle økonomikontoer for forskuddsbetalinger. Når en salgsordre eller en bestilling opprettes, utstedes en faktura til kunden eller fra leverandøren. Når fakturaen betales, tilbakeføres forskuddbetalinger og forskuddbetalingsbilag av mva i finanskontoene for forskuddbetaling, og fakturabeløpene posteres automatisk til de vanlige samlekontoene. Hvis du vil opprette en forskuddsbetaling, gjør du følgende:

1.  Definer en posteringsprofil for forskuddsbetalinger.
2.  I Kundeparametere og Leverandørparametere, under **Finans og merverdiavgift**, velger du den nye posteringsprofilen ved hjelp av parameteren **Posteringsprofil for betalingsjournal med forskuddsbetaling**.
3.  Opprett en betalingsjournal, og opprett deretter den nye betalingen.
4.  Du kan flagge betalingen som en forskuddsbetaling. Hvis en betaling er flagget som en forskuddsbetaling, posteres betalingen til finanskontoer som er definert i posteringsprofilen som du definerer i trinn 1 og 2. Hvis betalingen er flagget som en forskuddsbetaling, beregnes også skatt. Noen myndigheter krever at avgiftene betales når det registreres en forskuddsbetaling, selv om det ikke er en faktura.
5.  Poster forskuddsbetalingen.
6.  Valgfritt: Du kan utligne forskuddsbetalingen mot bestillingen eller salgsordren før du oppretter fakturaen. I handlingsruten på salgsordre- eller bestillingssiden bruker du **Utlign transaksjoner**.
7.  Når leverandøren leverer varene eller tjenestene, kan du registrere fakturaen. Hvis du har utlignet forskuddsbetalingen mot bestillingen eller salgsordren i trinn 6, utlignes automatisk forskuddsbetalingen mot fakturaen som du opprettet. Hvis du ikke utlignet forskuddsbetalingen mot bestillingen eller salgsordren, kan du manuelt utligne den mot fakturaen ved hjelp av **Utlign transaksjoner** på kunde- eller leverandørsiden. Forskuddsbetalingsbeløpet tilbakeføres deretter ut fra den midlertidig AP/AR-finanskontoen. I tillegg, hvis merverdiavgift er beregnet, tilbakestilles de fordi fakturaen har de faktiske mva-beløpene.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Oversikt over forskuddsfaktureringsprosessen
Forskuddsbetalte fakturaer er vanlig forretningspraksis. En leverandør sender forskuddsbetalte fakturaer for å kreve et innskudd på innkjøpet før bestillingen er oppfylt. Noen leverandører krever for eksempel en forskuddsbetaling for tilpassede varer eller tjenester. Hvis en leverandør sender en faktura som ber om forskuddsbetaling, kan du bruke funksjonen for forskuddsfakturering. En verdi for forskuddsbetaling kan defineres i bestillingen, en forskuddsbetalt faktura registreres og betales, og deretter brukes forskuddsfakturaen på den endelige fakturaen. Hvis du vil opprette en forskuddsbetaling, gjør du følgende:

1.  Innkjøpsagenten oppretter, bekrefter og sender deretter en bestilling som leverandøren har bedt om forskuddsbetaling for. Verdien for forskuddsbetaling defineres i bestillingen som en del av avtalen.
2.  Leverandøren sender en forskuddsbetalt faktura.
3.  Leverandørkoordinatoren registrerer den forskuddsbetalte fakturaen mot bestillingen, og deretter betales den forskuddsbetalte fakturaen.
4.  Leverandøren sender en forespørsel om betaling, som kalles en standard leverandørfaktura. Når leverandøren har levert varene eller tjenestene, og de tilknyttede standard leverandørfakturaene er mottatt, bruker leverandørkoordinatoren forskuddsbetalingsbeløpet som allerede er betalt mot standardfakturaen.
5.  Leverandørkoordinatoren betaler og utligner det gjenstående beløpet på standardfakturaen.

## <a name="set-up-parameters-to-enable-the-prepayment-invoicing-process"></a>Definer parametere for å aktivere fakturering av forskuddsbetaling
En forskuddsbetalingskonto må defineres i kategorien **Bestilling** på siden **Lagerpostering** (**Lagerstyring \> Oppsett \> Postering \> Postering**). Forskuddsbetalingskontoen blir oppdatert, vanligvis debitert, når forskuddsbetalingsfakturaen posteres. Saldoen på forskuddsbetalingskontoen tilbakeføres når standardfakturaen som brukes på forskuddsbetalingsfakturaen, posteres. Hvis du ikke utligner forskuddsbetalingsfakturaen mot en betaling før forskuddsbetalingsfakturaen brukes på standardfakturaen, tilbakeføres regnskapsoppføringene fra den posterte forskuddsbetalingsfakturaen når standardfakturaen posteres.

Motpostering av samlekonto for leverandører defineres i **Leverandørpostering**-profilen. Hvis du vil definere standard posteringsprofil, klikker du på **Leverandører \>Oppsett \> Leverandørparametere \>Finans og merverdiavgift-fanen \> Posteringsprofil med forskuddsfaktura for leverandør**.

**Policy for bruk av forskuddsbetaling** indikerer om systemet automatisk bruker oppgjorte forskuddsfakturaer på den endelige fakturaen som ble opprettet manuelt. Fakturaer som opprettes ved hjelp av en dataenhet, refererer ikke til **Policy for bruk av forskuddsbetaling**. Du må bruke manuelt utlignede forskuddsbetalingsfakturaer på fakturaer som ble opprettet ved hjelp av en dataenhet. Hvis du vil definere policyen, kan du gå til **Leverandør \>Oppsett \> Leverandørparametere \> Finans og merverdiavgift-fanen \> Policy for bruk av forskuddsbetaling**. Hvis feltet **Policy for bruk av forskuddsbetaling** er satt til **Automatisk**, blir forskuddsbetalingsfakturaen automatisk merket for oppgjør med sluttfakturaen. Hvis feltet er satt til **Varsling**, vises en visuell indikasjon på at en forskuddsbetalingsfaktura er tilgjengelig for bruk når sluttfakturaen opprettes.

## <a name="create-a-purchase-order-that-contains-prepayment-invoice-information"></a>Opprett en bestilling som inneholder informasjon om forskuddsbetalingsfaktura
Når en leverandør forteller deg at de krever forskuddsbetaling for varer og tjenester i en bestilling, må du definere forskuddsbetalingsverdien for den tilknyttede bestillingen. Gå til **Leverandører \> Felles \> Bestillinger \> Alle bestillinger**, og finn leverandørens bestilling. I handlingsruten velger du kategorien **Innkjøpp** og deretter **Forskuddsbetaling**. Angi informasjon for forskuddsbetalingen, inkludert en beskrivelse, verdien av forskuddsbetalingen, om forskuddsbetalingen er et fast beløp eller en prosent, og en forskuddskategori-ID. 

Legg merke til at flere definisjoner av forskuddsbetalinger på en bestilling ikke er tillatt. Hvis du må tillate flere forskuddsbetalinger på en bestilling, posterer du betalingene ved hjelp av betalingsjournalen i stedet for en forskuddsbetalingsfaktura.

Forskuddsbetalingen kan bli fjernet fra bestillingen med mindre du allerede har utlignet en betaling mot den posterte forskuddsbetalingsfakturaen eller postert standardfakturaen. Hvis du vil fjerne informasjon om forskuddsbetaling fra bestillingen, velger du **Leverandører \> Felles \> Bestillinger \> Alle bestillinger** og finner leverandørens bestilling. I handlingsruten velger du kategorien **Innkjøp** og deretter **Fjern forskuddsbetaling**.

## <a name="create-and-post-a-prepayment-invoice"></a>Opprett og poster en forskuddsbetalingsfaktura
Hvis du vil registrere leverandørens forskuddsbetalingsfaktura, kan du gå til siden **Leverandørfaktura** ved å velge **Forskuddsbetalt faktura** på **Bestillinger**-siden (**Leverandører \> Felles \> Bestillinger \> Alle bestillinger \> Faktura-fanen \> Forskuddsbetalt faktura**). Angi informasjonen for den forskuddsbetalte fakturaen, inkludert fakturanummeret. Du kan ikke endre antallet for en forskuddsfaktura. Hvis leverandøren har fakturert et delvis beløp av forskuddsbetalingsverdien som er definert i bestillingen, kan du oppdatere enhetsprisen for å gjenspeile den delvise verdien.

Når forskuddsbetalingsfakturaen posteres, blir leverandørsaldoen og forskuddsbetalingskontoen oppdatert. Verdien av **Bruk av forskuddsbetaling** i forskuddsbetalingsdefinisjonen i bestillingen blir også oppdatert. Standard finansdimensjonsoppføringer for det posterte forskuddsbetalingsbilaget tas fra hodeinformasjonen i bestillingen.

## <a name="post-and-settle-payments-for-the-prepayment-invoice"></a>Postere og utligne betalinger for forskuddsbetalingsfakturaen
Deretter betales forskuddsbetalingsfakturaen fra siden **Betalingsjournal**. Du kan få tilgang til betalingsjournaler ved å klikke på **Leverandører \> Journaler \> Betalinger \> Betalingsjournal**. Når du har postert utligningen av betalingen til forskuddsbetalingsfakturaen, oppdateres bestillingens verdi for **Gjenværende forskuddsbetalingsplassering**.

Før du posterer standardfakturaen for forskuddsbetalingsfakturaen, kan du tilbakeføre utligningen av betalingen fra forskuddsbetalingsfakturaen. Når en standardfaktura er brukt på forskuddsbetalingsfakturaen, kan imidlertid ikke betalingsutligningen tilbakeføres fra forskuddsbetalingsfakturaen.

## <a name="post-the-standard-vendor-invoice-for-the-purchase-order-and-apply-the-prepayment-invoice-to-the-standard-invoice"></a>Poster standard leverandørfaktura for bestillingen, og bruk forskuddsbetalingsfakturaen på standardfakturaen
Registrer standardfakturaen som mottas fra leverandøren. Som en del av denne prosessen kan du bruke den utlignede forskuddsbetalingsfakturaen på leverandørfakturaen, slik at verdien av fakturaen reduseres med beløpet som allerede er betalt. Bruk av forskuddsbetalingsfakturaen på leverandørfakturaen vil sikre at regnskapsoppføringer fra forskuddsbetalingsfakturaen blir tilbakeført.

## <a name="application-of-the-prepayment-invoice-after-posting-the-standard-invoice"></a>Bruk av forskuddsbetalingsfaktura etter postering av standardfakturaen
Hvis du glemmer å bruke forskuddsbetalingen på standard leverandørfaktura når leverandørfakturaen blir postert, vil den utlignede forskuddsbetalingen være tilgjengelig for bruk på andre fakturaer fra denne leverandøren fra **Leverandører**-siden (**Leverandører \> Felles \> Leverandører \> Alle leverandører \> Faktura-fanen \> Bruk**).

## <a name="reversal-of-the-prepayment-application-process"></a>Tilbakeføring av bruk av forskuddsbetaling
Hvis du må oppheve eller tilbakeføre bruken av en forskuddsbetalingsfaktura fra en standardfaktura, velger du **Tilbakefør**-handlingen fra **Leverandører**-siden (**Leverandører \> Felles \> Leverandører \> Alle leverandører \> Faktura-fanen \> Tilbakefør**). Når bruken av forskuddsbetaling er tilbakeført, kan du bruke forskuddsbetalingen på en annen standardfaktura. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
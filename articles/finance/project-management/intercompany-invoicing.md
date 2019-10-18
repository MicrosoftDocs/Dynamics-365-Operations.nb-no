---
title: Konsernintern fakturering
description: Denne artikkelen inneholder informasjon om og eksempler på konserninterne fakturering for prosjekter.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0385c796ca1ac02d6b8f66c04dad21bafe15ef8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174976"
---
# <a name="intercompany-invoicing"></a>Konsernintern fakturering

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om og eksempler på konserninterne fakturering for prosjekter.

Organisasjonen kan ha flere avdelinger, datterselskaper og andre juridiske enheter som overfører produkter og tjenester til hverandre for prosjekter. Den juridiske enheten som tilbyr tjenestene eller produktene, *den juridiske enheten som låner ut*, og den juridiske enheten som mottar tjenestene eller produktene, kalles *den juridiske enheten som låner*. 

Illustrasjonen nedenfor viser et vanlig scenario der to juridiske enheter, SI FR (den juridiske enheten som låner) og SI USA (den juridiske enheten som låner ut), deler ressurser for å levere et prosjekt til kunde A. I dette scenariet avtales det at SI FR levere arbeidet til kunde A. 

[![Eksempel på konsernintern fakturering](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Målet er å gjøre kostnadskontroll, inntektsføring, avgifter og overføringspris for konserninterne prosjekttransaksjoner mer fleksibel og kraftig. I tillegg finnes følgende funksjoner:

-   Opprette kundefakturaer mot et prosjekt i en juridisk enhet som låner, ved hjelp av konserninterne timeregistreringer, utgifter og leverandørfakturaer i en juridisk enhet som låner ut.
-   Støtte for avgiftsberegninger og indirekte kostnader.
-   Utsette inntektsføring i en juridisk enhet som låner ut, og når en juridisk enhet som låner skal gjenkjenne kostnadene.
-   Avsette omsetning for varer i arbeid (VIA) i den juridisk enheten som låner ut.
-   Angi overføringspriser som kan være basert på forskjellige prismodeller. Her er noen eksempler:
    -   **Antall** – Beløpet du angir i feltet **Prissetting** er de faktiske kostnadene per antall eller enhet.
    -   **Gebyrbeløp** – Prisen/kostnaden per transaksjon pluss tilleggsbeløpet som du angir i feltet **Prissetting**.
    -   **Gebyrprosent** – Overføringsprisen er prisen/kostnaden per transaksjon multiplisert med tilleggsprosenten som du angir i feltet **Prissetting**.
    -   **Prosent av salgspris** – Prosenten av salgsprisen som overføres til den juridiske enheten som låner ut.
    -   **Beløp under salgspris** – Beløpet som den juridiske enheten som låner holder tilbake fra salgsprisen før overføring til den juridiske enheten som låner ut.
    -   **Dekningsgrad** – Nummeret du skriver inn i feltet **Prissetting** er dekningsgraden som er uttrykt som en prosentandel av salgsprisen.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Eksempel 1: Definere parametere for konserninterne fakturering
I dette eksemplet er USSI en juridisk enhet for utlån, og ressursene rapporterer tid mot den juridiske enheten som låner, FRSI, som eier kontrakten med sluttkunden. Timer og utgifter som USSI-ansatte rapporterer, kan inkluderes i prosjektfakturaen som FRSI genererer. I tillegg er det en tredje kilde for transaksjoner som kan komme fra den juridiske enheten som låner ut (USSI i dette eksemplet), når den inneholder delte leverandørtjenester til datterselskaper (for eksempel FRSI) og deretter sender disse kostnadene til prosjekter i datterselskapene. Alle samsvarende fakturadokumenter og avgiftsberegninger utføres av Finance. 

For dette eksemplet må FRSI være en kunde i den juridiske enheten for USSI, og USSI må være en leverandør i den juridiske enheten for FRSI. Du kan definere en konsernintern relasjon mellom de to juridiske enhetene. Fremgangsmåten nedenfor viser hvordan du definerer parameterne, slik at begge juridiske enheter kan delta i konsernintern fakturering.

1. Definer FRSI som en kunde i den juridiske enheten for USSI, og definer USSI som en leverandør i den juridiske enheten for FRSI. Det finnes tre inngangspunkter for trinnene som kreves for denne oppgaven.

   | Trinn |                                                       Inngangspunkt                                                        |                                                                                                                                                                                               beskrivelse                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | Gå til USSI, og klikk <strong>Kunder</strong> &gt; <strong>Kunder</strong> &gt; <strong>Alle kunder</strong>. |                                                                                                                                                                  Opprett en ny kundepost for FRSI, og velg kundegruppen.                                                                                                                                                                  |
   |  B   |    Gå til FRSI, og klikk <strong>Leverandører</strong> &gt; <strong>Leverandører</strong> &gt; <strong>Alle leverandører</strong>.     |                                                                                                                                                                    Opprett en ny leverandørpost for USSI, og velg leverandørgruppe.                                                                                                                                                                    |
   |  K   |                                  I FRSI åpner du leverandørposten som du nettopp opprettet.                                  | I handlingsruten i kategorien <strong>Generelt</strong> i <strong>Oppsett</strong>-gruppen, klikker du <strong>Konsernintern</strong>. På siden <strong>Konserninterne</strong> i kategorien <strong>Handelsforbindelse</strong>, setter du glidebryteren <strong>Aktiv</strong> til <strong>Ja</strong>. I feltet <strong>Kundefirma</strong> velger du kundeposten som du opprettet i trinn A. |


2. Klikk **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Kontoparametere for prosjektstyring**, og klikk deretter kategorien **Konsernintern**. Måten du oppretter parametrene avhenger av om du er den lånende juridiske enheten eller den som låner ut den juridiske enheten.
   -   Hvis du er den juridiske enheten som låner, velger du innkjøpskategorien som skal brukes til å samsvare med leverandørfakturaer, som genereres automatisk.
   -   Hvis du er den juridiske enheten som låner ut, velger du en standard prosjektkategori for hver transaksjonstype for hver enhet som låner. Prosjektkategorier brukes for mva-konfigurasjon når den fakturerte kategorien i konserninterne transaksjoner bare finnes i den juridiske enheten som låner. Du kan velge å avsette inntekt for konserninterne transaksjoner. Denne avsetningen gjøres når transaksjonene posteres og tilbakeføres deretter når den konserninterne fakturaen bokføres.

3. Klikk **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Priser** &gt; **Overføringspris**.
4. Velg valuta, transaksjonstype og overføringsprismodell. Valutaen som brukes på fakturaen er valutaen som er konfigurert i kundeposten for den juridiske enheten som låner i den juridiske enheten som låner ut. Valutaen som brukes til å samsvare med postene i tabellen for overføringspris.
5. Klikk **Økonomimodul** &gt; **Posteringsoppsett** &gt; **Konserninternt regnskap**, og definere en relasjon for USSI og FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Eksempel 2: Opprette og postere en konsernintern timeregistrering
USSI, den juridiske enheten som låner ut, må opprette og postere timeregistreringen for et prosjekt fra FRSI, den juridiske enheten som låner. Det finnes to inngangspunkter for trinnene som kreves for denne oppgaven.

| Trinn | Inngangspunkt                                                                       | beskrivelse                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Prosjektstyring og regnskap** &gt; **Timeregistreringer** &gt; **Alle timeregistreringer** | Opprett en ny timeregistrering. På timeregistreringslinjen i feltet **Juridisk enhet**, velger du **FRSI**. I feltet **Prosjekt-ID** velger du prosjektet i FRSI. Angi timer for hver ukedag. |
| B    | Siden **Timeregistrering**                                                                | Når arbeidsflyten kjøres, posterer du timeregistreringen og noterer bilagsnummeret.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Eksempel 3: Opprette og postere en konsernintern leverandørfaktura
USSI, den juridiske enheten som låner ut, må opprette den konserninterne leverandørfakturaen for et prosjekt fra FRSI, den juridiske enheten som låner. Denne leverandørfakturaen representerer utsatt arbeid og utgifter som ble utført av leverandører som betales av USSI. Det finnes to inngangspunkter for trinnene som kreves for denne oppgaven.

| Trinn | Inngangspunkt                                                                                      | beskrivelse                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Leverandører** &gt; **Fakturaer** &gt; **Åpne leverandørfakturaer** &gt; **Ny leverandørfaktura**. | Opprette en ny leverandørfaktura, og angi tjenestene som ble innkjøpt på vegne av FRSIs prosjekt.                                                                                                                                                                                  |
| B    | Siden **Leverandørfaktura**                                                                      | Angi linjer som representerer utsatte tjenester på vegne av FRSI. I hurtigfanen **Linjedetaljer** i kategorien **Prosjekt** for fakturalinjen, i feltet **Prosjektselskap**, angir du **FRSI**. Angi prosjekt og tilhørende informasjon. Poster deretter leverandørfakturaen. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Eksempel 4: Opprette og postere den konsernintern fakturaen
USSI, den juridiske enheten som låner ut, må opprette og postere den konserninterne fakturaen. Det finnes to inngangspunkter for trinnene som kreves for denne oppgaven.

| Trinn | Inngangspunkt                                                                                             | beskrivelse                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Prosjektstyring og regnskap** &gt; **Prosjektfakturaer** &gt; **Konsernintern kundefaktura**  | Klikk **Ny** for å åpne siden **Opprett konsernintern faktura**.                                                                                  |
| B    | **Prosjektstyring og regnskap** &gt; **Prosjektfakturaer** &gt; **Konserninterne kundefakturaer** | På siden **Opprett konsernintern faktura** angir du den juridiske enheten, angir transaksjonen som skal tas med, og klikker deretter **Søk**. |
| K    | **Prosjektstyring og regnskap** &gt; **Prosjektfakturaer** &gt; **Konserninterne kundefakturaer** | Velg transaksjoner som skal faktureres, eller klikk **Velg alt** for å fakturere alle transaksjonene i listen, og klikk deretter **OK**.                  |
| D    | Siden **Konsernintern faktura**                                                                       | Forslaget til konsernintern kundefaktura vises.                                                                                             |
| E    | Siden **Konsernintern faktura**                                                                       | Klikk **Poster**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Eksempel 5: Postere leverandørfakturaen og fakturere kunden
Når den juridiske enheten som låner ut, USSI, posterer den konsernintern kundefakturaen, opprettes en tilsvarende ventende leverandørfaktura opprettet i den juridiske enheten som låner, FRSI. Når denne leverandørfakturaen posteres, fakturerer FRSI også prosjektkunden for timene som USSI har angitt. Det finnes tre inngangspunkter for trinnene som kreves for denne oppgaven.

| Trinn | Inngangspunkt                                                                                        | beskrivelse                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Leverandører** &gt; **Fakturaer** &gt; **Ventende leverandørfakturaer**                            | Se gjennom fakturaen for å kontrollere at verdiene for timeregistreringen er inkludert, og poster deretter leverandørfakturaen.                  |
| B    | **Prosjektstyring og regnskap** &gt; **Prosjektfakturaer** &gt; **Fakturaforslag for prosjekt** | Opprett en ny prosjektfaktura for prosjektet, og kontroller at timetransaksjonene som er bokført vises.            |
| K    | Siden **Prosjektfaktura**.                                                                       | Velg prosjektfakturaen, og klikk deretter **Vis detaljer** for å gå gjennom kost- og salgsbeløp. Postere deretter fakturaen. |


Hvis du vil ha mer informasjon, se [Konfigurere konsernintern prosjektfakturering](tasks/configure-intercompany-project-invoicing.md).



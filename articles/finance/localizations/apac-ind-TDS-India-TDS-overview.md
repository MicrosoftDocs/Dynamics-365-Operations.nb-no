---
title: Oversikt over indisk TDS (Tax Deducted at Source)
description: Dette emnet inneholder detaljert informasjon om indisk TDS (Tax Deducted at Source). TDS-dokumentasjonen omhandler funksjonaliteten til denne funksjonen.
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 8064f10978712fc474dd72a5b5bdd9a445606d7a
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/03/2021
ms.locfileid: "6337727"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a>Oversikt over indisk TDS (Tax Deducted at Source)

[!include [banner](../includes/banner.md)]

Dette emnet inneholder detaljert informasjon om indisk TDS (Tax Deducted at Source).

TDS-dokumentasjonen omhandler funksjonaliteten til denne funksjonen. Den forklarer også hvordan du foretar den grunnleggende konfigurasjonen for TDS, beregner TDS for transaksjoner, fullfører TDS-utligningsprosessen, registrerer TDS-sertifikatnumre og genererer TDS-forespørsler, TDS-oppgaver og TDS-sertifikater. Dokumentasjonen inneholder følgende emner:

- [Grunnleggende konfigurasjon for TDS](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [Formeldesigner og terskelgrensefunksjonalitet som brukes til TDS-beregning](apac-ind-TDS-Formula-designer.md)
- [Beregning av TDS for fakturaer, betalinger, egenveksler og konserninterne transaksjoner](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [Periodisk TDS-utligningsprosess og utligning av TDS-beløp mot TDS-myndighetsleverandører](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [Registrere og oppdatere TDS-sertifikatnumre og -datoer](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a>Innføring i TDS

I henhold til loven om avskriving per inntektsskatt fra 1961 blir inntektsskatt trukket fra ved kilden av mottakeren av tjenesten på tidspunktet for forskuddsbetaling eller regnskapsføring av kredit, avhengig av hva som kommer først. Personen som foretar betalingen, må trekke fra avgiftsbeløpet og bare betale nettosaldoen til leverandøren av tjenesten. TDS brukes på tjenester angitt av myndighetene, og avgiften trekkes fra ved hjelp av satsene som myndighetene angir for en periode. Fradragssatsen er basert på statusen for enheten som mottar betalingen, eller som tilbyr tjenesten. Statuser omfatter **Enkeltperson**, **HUF** (**Hindu Undivided Family**), **Selskap**, **Firma**, **AOP** (**Association of Persons**), **BOI** (**Body of Individuals**) og **Lokale myndigheter**.

Følgende deler viser tjenestene som TDS brukes på, som angitt av myndighetene i India.

**Beboere**

- Inntekt fra lønn (i paragraf 192)
- Inntekter fra rente på verdipapirer (i paragraf 193)
- Inntekt fra aksjeutbytte (i paragraf 194)
- Inntekt fra rente (i paragraf 194A)
- Inntekt fra lotterier eller spill (i paragraf 194B)
- Gevinst fra hesteveddeløp og så videre (i paragraf 194BB)
- Oppdragstakere og underleverandører (i paragraf 194C)
- Forsikringsprovisjon (i paragraf 194D)
- Inntekt fra innbetaling i samsvar med nasjonal spareordning (i paragraf 194EE)
- Inntekt fra aksjefond eller UTI (i paragraf 194F)
- Provisjon, godtgjørelse, pris og så videre for salg eller lotteri (i paragraf 194G)
- Betaling av provisjon eller meglerprovisjon (i paragraf 194H)
- Leie (i paragraf 194I)
- Profesjonell tjeneste (i paragraf 194J)
- Inntekt fra aksjefondsenheter (i paragraf 194K)
- Betaling av kompensasjon ved anskaffelse av visse faste eiendommer (i paragraf 194LA)

**Utlending**

- Betalinger til utenlandske idrettsutøvere eller idrettslag (i paragraf 194E)
- Andre summer (i paragraf 195)
- Inntekt med hensyn til enheter av utlendinger (i paragraf 196A)

    - Inntekt fra utenlandske valutaobligasjoner eller aksjer i indisk selskap (i paragraf 196C)
    - Inntekter til utenlandske investorinstitusjoner fra verdipapirer (i paragraf 196D)
    - Lønn og alle andre positive inntekter under enhver inntektskilde (paragraf 192)
    - Renter på verdipapirer (paragraf 193)
    - Andre renter enn rente på verdipapirer (paragraf 194A)
    - Betalinger til oppdragstakere og underleverandører (paragraf 194C)
    - Gevinster fra lotteri eller kryssord (paragraf 194B)
    - Gevinster fra hesteveddeløp (paragraf 194BB)
    - Forsikringsprovisjon som dekker alle betalinger for anskaffelse av forsikringsvirksomhet (paragraf 194D)
    - Andre renter enn rente på verdipapirer som skal utstedes til utlendinger som ikke er et selskap, eller til et utenlandsk selskap (paragraf 195)
    - Betaling til utenlandsk idrettsutøver, inkludert idrettslag eller -institusjon. Når det gjelder utenlandsk idrettsutøver, er betalinger med hensyn til annonser og artikler om alle kamper/idretter i India i aviser, tidsskrifter og så videre. inkludert (paragraf 194E)
    - Betaling med hensyn til innbetalinger i samsvar med NSS \[National Savings Scheme\] (paragraf 194EE)
    - Betaling på grunn av tilbakekjøp av enheter ved aksjefond eller UTI (paragraf 194F)
    - Betaling for provisjon eller meglerprovisjon (paragraf 194H)
    - Betaling av leie (paragraf 194I)
    - Betaling av gebyrer for profesjonelle eller tekniske tjenester (paragraf 194J)
    - Provisjon til forhandlere, distributører, kjøpere og selgere av loddsedler, inkludert godtgjørelse eller pris på slike sedler (paragraf 194G)
    - Inntekt fra enheter som er kjøpt i utenlandsk valuta, eller langsiktig kapitalgevinst som skyldes overføring av slike enheter kjøpt i utenlandsk valuta (paragraf 196B)
    - Betaling av inntekter til utlendinger med hensyn til rente eller utbytte på verdipapirer og aksjer (paragraf 196C)

TDS beregnes for innkjøp, salg, salgsreturer, kreditnotaer, anleggsmiddelanskaffelser, forskuddsbetalinger, egenveksler, verksskatt og konserninterne transaksjoner.

> [!NOTE]
> I det gjeldende indiske skattescenarioet beregnes ikke TDS på salgstransaksjoner. Systemet omfatter imidlertid et tiltak for å beregne TDS som kan tilbakebetales på salgstransaksjoner, spesielt for konserninterne transaksjoner.

Beregningen av TDS tar alltid hensyn til terskelen og unntaksterskelen som er definert for TDS-komponenten.

Den periodiske TDS-utligningsprosessen må kjøres, og TDS-betalingene må utlignes mot TDS-myndighetsleverandører.

Sertifikatnumrene og -datoene for TDS-sertifikater som mottas fra leverandører eller kunder, kan registreres og oppdateres. De kvartalsvise oppgavene Form 26Q og Form 27Q samt sertifikatet Form 16A for TDS kan genereres i Finance.

## <a name="setting-up-and-working-with-tds"></a>Konfigurere og arbeide med TDS

Her er en oversikt over fremgangsmåten for å konfigurere og arbeide med TDS:

1. **TDS-konfigurasjon:**

    - Parameterkonfigurasjon:

        - Aktiver parametere som er knyttet til TDS, i Parametere for økonomimodul.
        - Konfigurer nummerserien for kildeskattbetalinger i Parametere for økonomimodul.
        - Konfigurer parametere i Leverandører og Kunder.

    - Grunnleggende konfigurasjon:

        - Konfigurer TDS-registreringsnumre for et selskap, kunder og leverandører.
        - Konfigurer TDS-komponentgrupper.
        - Konfigurer TDS-komponenter, knytt TDS-komponentgrupper til dem, og definer terskelen og unntaksterskelen for dem.
        - Konfigurer TDS-myndigheter.
        - Konfigurer TDS-utligningsperioder.
        - Konfigurer TDS-avgiftskoder, og knytt TDS-komponenter til dem.
        - Konfigurer TDS-avgiftsgrupper, og knytt TDS-avgiftskoder til dem.
        - I formeldesigneren definerer du en formel for å beregne TDS for en TDS-gruppe.
        - Registrer TDS-konsesjonssertifikatnumre.

    - Finanskontoer og selskapskonfigurasjon:

        - Konfigurer leverandør- og kundefinanskontoer for TDS.
        - Konfigurer et kontonummer for avgiftsfradrag og -innkreving (TAN) og en kategori av typen deductor for selskapet.

    - Annen konfigurasjon:

        - Konfigurer en betalingsplan som omfatter TDS-tildeling.
        - Konfigurer en betalingsgebyrtype for betalinger til TCS-myndigheten.
        - Konfigurer informasjon om TDS-grupper, permanente kontonumre (PAN) og TAN-numre for leverandører og kunder.

2. **Beregning av TDS i transaksjoner:**

    - Fakturaer og betalinger
    - Egenveksler
    - Forskuddsbetalinger
    - Forskuddsbetalinger

3. **TDS-utligning:**

    - Periodisk TDS-utligningsprosess
    - Utligning av TDS-betalinger mot TDS-myndighetsleverandører og generering av TDS-challan

4. **TDS-forespørsler, -oppgaver og -sertifikat:**

    - Registrer og oppdater TDS-sertifikatnumre og -datoer.
    - Generer en TDS-forespørsel og en postert TDS-forespørsel.
    - Generer de kvartalsvise oppgavene Form 27A, Form 26Q og Form 27Q for TDS og e-TDS.
    - Generere et TDS-sertifikat for Form 16A.

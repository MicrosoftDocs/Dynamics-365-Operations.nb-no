---
title: Leverandørrabatter
description: Dette emnet gir en oversikt over de vanligste oppgavene du kanskje vil utføre når du jobber med leverandørrabatter. Leverandørrabatter hjelper bedrifter bedre å håndtere sine leverandørrabattprogrammer ved å automatisere oppgaver som kreves for å administrere, spore og kreve rabatter som er opptjent.
author: omulvad
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMVendRebateAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 2012
ms.openlocfilehash: 7c0f98ffc6ede74f93523b9fa9800e7b6617d9b6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434623"
---
# <a name="vendor-rebates"></a>Leverandørrabatter

[!include [banner](../includes/banner.md)]

Leverandørrabatter hjelper bedrifter bedre å håndtere sine leverandørrabattprogrammer ved å automatisere oppgaver som kreves for å administrere, spore og kreve rabatter som er opptjent.

Dette emnet gir en oversikt over de vanligste oppgavene du kanskje vil utføre når du jobber med leverandørrabatter. Oversikten dekker følgende oppgaver:

- Gjennomgå detaljer om en rabattavtale.
- Identifiser bestillinger som kvalifiserer for rabatter, og generer rabattkrav.
- Gjennomgå og godkjenne krav.

## <a name="audience-and-purpose"></a>Målgruppe og formål

Informasjonen i dette emnet er ment for forretningsmessige beslutningstakere i bedriftsselskaper, i stillinger som innkjøpssjef, finansdirektør og regnskapsfører, som har følgende ansvar:

- Forhandle forhandlerpris, rabatt og rabattavtaler.
- Administrer ansatte som behandler rabattkrav og samler inn betalinger.
- Bestill varer til best mulig pris.

Folk i disse stillingene ser etter måter å oppnå ulike mål. Her er noen eksempler:

- Fleksibelt imøtekomme ulike typer leverandørprogrammer og rabattbetingelser.
- Reduser administrasjonsbelastningen og feilene som er knyttet til overvåking av kampanjeresultater og behandlingskrav.
- Forbedre kontantstrømsprognosene ved å tilføre fremtidige fordringer.
- Ha et kvantifisert grunnlag for løpende og fremtidige forhandlinger med leverandører om rabatter.

## <a name="review-details-of-a-vendor-rebate-agreement"></a>Se gjennom detaljer om en leverandørrabattavtale

En leverandørrabattavtale er en oversikt over en kontrakt med en leverandør som spesifiserer de forhandlede vilkårene hvor selskapet kvalifiserer for en pengepremie, i motsetning til å oppnå forhåndsdefinerte kjøpsmål. Leverandørrabattavtaler er registrert på siden **Rabattavtaler**.

Hvis du vil åpne siden **Leverandørrabattavtaler**, velg **Anskaffelse og innkjøp** &gt; **Leverandørrabatter** &gt; **Rabattavtaler**.

![Kjøpsavtale](media/purchase-agreement.PNG)

På siden **Leverandørrabattavtaler** kan du se informasjon om de forhandlede betingelsene for en leverandøravtale.

Avtalens topptekst spesifiserer de generelle vilkårene som kvalifiserer et selskap for rabatter. I utgangspunktet spesifiserer topptekstinformasjonen at en leverandør gir en rabatt når et bestemt produkt er kjøpt i en bestemt mengde. I toppteksten kan du også spesifisere enheten for målerabattalternativ og beregningsdatatypen.

- I kategorien **Oversikt**, hvis du har linjer med **Varekode** satt til *tabell* for å angi varen, er avtalen for den bestemte varen. Hvis du har linjer med **Varekode** satt til *Gruppe* eller *Alle* for å angi varene, vil leverandørrabattavtalen behandles individuelt per vare som er kvalifisert for varekoden, ikke på tvers av alle varer som kvalifiserer for varekoden.

- I kategorien **Generelt**, i feltet **Rabattalternativ for måleenhet**, kan du definere om en måleenhet bør være en betingelse for innkjøpsordre, for å kvalifisere for rabattkrav.

    - **Konvertere** – et innkjøpsordrelinje kvalifiserer for leverandørrabatt per rabattargument. Du vil motta en rabatt uavhengig av måleenheten som brukes på linjen.
    - **Eksakt treff** – for å kvalifisere for en rabatt må en innkjøpslinje ha samme målenhet som er spesifisert i avtalen.

- I kategorien **Generelt** i **Kalkulering av datatyper**-feltet, velg datoen som brukes for å fastsette om kjøpet skjer i gyldig periode for rabattavtalen.

    - **Opprettet** – bruk opprettelsesdato for kjøpsordre.
    - **Ønsket leveringsdato** – bruk ønsket leveringsdato

På avtalelinjene kan du spesifisere leverandørrabattavtalen nærmere.

- I feltet **Kumulere kjøp av**, kan du angi beregningen av rabattkravet. Beløpet kan settes avhengig av en periode (i uke, måned, år, levetid eller en tilpasset periode). Verdien **Faktura** indikerer at et rabattkrav vil bli bestemt hver gang en innkjøpsordrelinje faktureres.
- I feltet **Tatt fra** kan du spesifisere grunnlaget for rabattberegning.

    - **Brutto** – rabatten er beregnet basert på bruttopris for elementet.
    - **Netto** – rabatten er beregnet basert på nettopris for elementet (som er, prisen etter at andre rabatter er trukket fra).

- Feltene **Rabatprogramopptjeningskonto** og **Rabattprogramutgiftskonto** angir kontonumre som vil motta påløpte rabattbeløp i mellomstadiet mellom godkjenning og behandling.
- Når alternativet **Godkjenning nødvendig** er satt til **Ja**, vil rabattkravet måtte godkjennes før det påløpes eller betales.
- Feltet **Bruddtype for rabattlinje** spesifiserer grunnlaget for rabatter.

    - **Mengde** – rabatter er volumbasert.
    - **Beløp** – rabatter er beløpsbasert.

- I hurtigkategorien **Linjer** kan du se hvordan ulike kvantitetsnivåer kan settes opp for å gi ulike rabatter. For eksempel, i den forrige illustrasjonen, indikerer feltene **Fra-verdien** og **Til-verdien** at en produktmengde mellom 10 og 19 enheter vil kvalifisere til rabatt på USD 15 per enhet.

    > [!NOTE]
    > Verdien **Fra-verdien** er inklusiv, mens verdien **Til-verdien** er eksklusiv. For eksempel er feltet **Bruddtype for rabattlinje** satt til **Mengde** og du kan skrive inn **1** i feltet **Fra-verdi** og **3** i feltet **Til-verdi**. I dette tilfellet gjelder rabattbeløpet når du kjøper ett eller to elementer, men ikke når du kjøper tre varer.

- I feltet **Godkjenningsstatus for arbeidsflyt**, vil **Godkjent**-verdien indikere at avtalen kan brukes på innkjøpsordrer som oppfyller avtalens betingelser.

## <a name="identify-orders-that-qualify-for-rebates-and-generate-rebate-claims"></a>Identifiser bestillinger som kvalifiserer for rabatter, og generer rabattkrav

Når kjøpsordrer er plassert hos en leverandør som selskapet har en rabattavtale med, identifiserer programmet eventuelle fremtidige leverandørkredittbetalinger. Hvis kjøpsordrene kvalifiserer for rabatt, genereres et rabattkrav for hver ordrelinje så snart en innkjøpsfaktura er lagt ut. Denne prosessen skjer automatisk. Senere kan du gjennomgå forventede rabatter og se effekten av disse rabattene på produktets kostnads- og fortjenestemargin.

### <a name="view-details-of-rebates-that-are-applied-to-a-purchase-order-line-per-the-vendor-rebate-agreement"></a>Se detaljer om rabatter som brukes på en bestillingslinje per leverandørrabattavtale

1. På **Innkjøpsordre**-siden, velg en ordrelinje og deretter vel **Innkjøpsordrelinje** &gt; **Visning** &gt; **Prisinformasjon**.
2. På siden **Prisinformasjon**, velg hurtigkategorien **Rabatter**.

Rabattinformasjonen vises også i feltet **Leverandørrabat** i delen **Marginestimat** for siden **Prisinformasjon**.

> [!NOTE]
> På siden **Innkjøp og innkjøpsparametere**, i kategorien **Priser**, bekreft at alternativet **Aktiver prisinformasjon** er satt til **Ja**. Hvis dette alternativet er satt til **Nei**, vil du ikke kunne se rabatten.

## <a name="review-and-approve-claims"></a>Gjennomgå og godkjenne krav

Rabatkrav som genereres representerer fremtidige betalinger som kan forventes fra leverandøren. Før en kreditnota utstedes til leverandøren, vil avtalens eier typisk vurdere kravene og godkjenne dem. Vær imidlertid oppmerksom på at statusen for et krav bestemmer om kravet er klart for å gå gjennom godkjenningsprosessen.

### <a name="the-status-of-claims-and-the-effect-on-the-approval-process"></a>Status på krav og effekten på godkjenningsprosessen

Når et krav er generert statusen satt til **Til beregning** hvis rabatten er gitt på kumulativt basis, eller **Kalkulert** hvis rabatten er gitt per faktura. Hvis statusen for et krav er **Til beregning**, vil kravet måtte gå gjennom en beregningsprosess som håndteres av funksjonen Kumulativ. Kun krav som har statusen **Beregnet** kan inkluderes i godkjennelsesprosessen.

> [!NOTE]
> Hvis alternativet **Godkjennelse kreves** på en leverandørrabattavtale er satt til **Nei**, vil alle krav som genereres få statusen **Godkjent**. Godkjennelsen er obligatorisk for krav som er gitt på kumulativt basis.

### <a name="approve-claims-and-view-postings-and-invoice-details"></a>Godkjenn krav og se posteringer og fakturadetaljer

Når krav er godkjent kan de behandles som leverandørgjeld. En kreditnota (leverandørfaktura) for rabattkravbeløpet genereres automatisk. Kreditten kan legges til leverandørsaldoen, og teamet som skal behandle leverandørgjelden kan inkluderes i den ordinære oppgjørsprosessen.

1. Velg **Anskaffelse og innkjøp** &gt; **Leverandørrabatter** &gt; **Rabattkrav** for å åpne et rabattkrav.
2. Lukk rabattkravet.
3. Marker kravet, og velg deretter **Godkjenn** i Handlingsvinduet.
4. På forespørselssiden, i **Leverandør**-feltet, velg leverandøren du er autorisert til å motta en rabatt fra, og velg deretter **OK**.

    En rabattopptjeningsjournal er oppført for kravsbeløpet. Denne posteringen debiterer den opptjente leverandørrabatt-mottakskontoen for forventet leverandørkreditt og krediterer den midlertidige opptjente leverandørrabatter-mottakskontoen for forventet gevinst.

    ![Melding](media/message.png)

5. I rabattlisten velger du linjen, og deretter velger du **Rabatt-transaksjoner** i Handlingsvinduet for å se og navigere til journalbatchnummer for denne rabattopptjeningsposten.

    For å flytte kravene til ordinær leverandørgjeld-prosess, må ansvarlig for leverandørgjeld fullføre rabattkravhandlingen ved å kjøre Behandle-funksjonen.

6. I Handlingsvinduet, velg **Prosesser**, og velg deretter **Filter**. I feltet **Kriterier** for **Leverandørkonto**-feltet, velg leverandøren å behandle rabattkravet for, velg andre relevante filtre, og velg deretter **OK**.

    Meldingsfeltene og det faktum at statusen er endret til **Fullført**, tyder på at følgende hendelser har oppstått:

    - En journalpostering for rabattopptjening har reversert de tidligere foreløpige beløpene på periodiseringsfordelings- og kostnadsregnskapet.
    - En leverandørfaktura (kreditnota) for rabattbeløpet er opprettet.

        > [!NOTE]
        > Innstillingen for alternativet **Manuel fakturapostering** i kategorien **Rabattprogram** for siden **Parametere for anskaffelse og innkjøp** fastsetter om en leverandørfaktura skal legges inn manuelt eller automatisk som en del av kravbehandlingen.

    - Når leverandørfakturaen er oppført, enten automatisk eller manuelt, har leverandørens Betalbare konto blitt belastet, og mottakskonto for rabatter og tillatelser har blitt kreditert.

        > [!NOTE] 
        > Kontonummer for rabatter og motta tillatelser er spesifisert for anskaffelseskategorien som brukes på kjøpsfakturalinjen for rabatten. Anskaffelseskategorien er i sin tur satt i kategorien **Rabattprogram** for siden **Parametere for anskaffelse og innkjøp**.

7. I rabattlisten velger du linjen, og deretter velger du **Rabatt-transaksjoner** i Handlingsvinduet for å se og navigere til journalbatchnummer for denne rabattopptjeningsposten, og også leverandørfakturanummer.
8. Velg linjen for leverandørfaktura-transaksjonen, og velg deretter **Leverandørfaktura** i handlingsruten. Hvis leverandørfakturaen er postert, vil du se fakturajournalen. Hvis ikke, vil du se leverandørfakturaen som en ventende leverandørfaktura som krever manuell postering.

    Fakturalinjen spesifiserer detaljene for leverandørfakturaen for anskaffelseskategorien **Kommisjoner og rabatter**.

9. På siden **Alle leverandører**, velg en leverandør som du mottar en rabatt fra, og deretter i Handlingsvinduet, velg **Transaksjoner**. Finn linjen for fakturaen. Rabattbeløpet er nå lagt til leverandørsaldoen.

## <a name="summary"></a>Sammendrag

Prosessen for å håndtere leverandørrabatter innebærer flere manuelle sporingsoppgaver som ofte er kjedelige. Ved å automatisere disse oppgaver kan funksjonen for leverandørrabattadministrasjon hjelpe deg med å bevege deg gjennom følgende prosesser:

- Genererer nøyaktige rabattkrav
- Å påløpe forventet fordring og foreløpig gevinst i hovedboken
- Oppdaterer leverandørbalansen og resultatregnskapet med godtgjørelse som er forfalt


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
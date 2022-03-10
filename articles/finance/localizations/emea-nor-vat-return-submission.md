---
title: Sende en mva-retur til webtjeneste Altinn
description: Dette emnet beskriver hvordan du sender en mva-retur til Altinn-webtjenesten i Norge.
author: liza-golub
ms.date: 12/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Norway
ms.author: elgolu
ms.search.validFrom: 2021-11-18
ms.dyn365.ops.version: AX 10.0.22
ms.openlocfilehash: fd201ed282f6277f11d50c10f7e1e743d1e87ea3
ms.sourcegitcommit: b1c758ec4abfcf3bf9e50f18c1102d4a9c1316d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922401"
---
# <a name="submit-a-vat-return-to-the-altinn-web-service"></a>Sende en mva-retur til webtjeneste Altinn

[!include [banner](../includes/banner.md)]

Når du har fått tilgang til et tilgangstoken for Altinn, er Microsoft Dynamics 365 Finance-miljøet klart til å fungere sammen med webtjenesten Altinn for å sende inn mva-returer.

Behandlingen for en mva-retur som sendes til Altinn, består av mange trinn. Hvis du vil ha en fullstendig beskrivelse av innsendingsprosessen, kan du gå til [API](https://skatteetaten.github.io/mva-meldingen/english/api/)-siden.

[Elektroniske meldinger](../general-ledger/electronic-messaging.md)-funksjonaliteten (EM) brukes til å støtte prosessen med å generere en mva-retur og sende den direkte til Altinn fra Finance. Når du [importerer en pakke med dataenheter som inneholder et forhåndsdefinert EM-oppsett](emea-nor-vat-return-setup.md#em-setup) til den juridiske enheten, importeres alle handlingene som kreves for å sende mva-returer til Altinn. Illustrasjonen nedenfor viser et forenklet skjema for EM-behandlingen som leveres med oppsettfilen **NO MVA-retur – Altinn**.

![Skjema for EM-behandlingen som leveres med oppsettfilen NO MVA-retur – Altinn.](media/emea-nor-vat-return-em-processing.png)

Ikke alle relasjonene mellom handlingene som er definert i **NO MVA-retur** blir tatt med i diagrammet.

For å forenkle prosessen med å sende inn MVA-returer, samles de fleste handlingene i uatskillelige sekvenser. Når den første handlingen i en sekvens startes, kjører systemet automatisk alle handlingene i den rekkefølgen. Derfor er prosessen betydelig forenklet, og de nødvendige trinnene reduseres til følgende liste:

1. [Opprett en melding](#create-message).
2. [Samle inn mva-betalinger](#collect-sales-tax-payments).
3. [Merk meldingen som klar til å generere mva-returen](#ready-to-generate).
4. [Forhåndsvis mva-returen i Microsoft Excel](#preview-vat-return).
5. [Generer mva-returen](#generate-vat-return).
6. [Valider mva-returen i webtjenesten for skatteadministrasjon](#validate-vat-return).
7. [Send inn mva-returen](#submit-vat-return).
8. [Last ned vedlegg](#download-attachments).

## <a name="create-a-message"></a><a id="create-message"></a>Opprett en melding

Følg denne fremgangsmåten for å utføre handlingen **NO MVA Opprett melding**.

1. Gå til **Avgift** \> **Forespørsler og rapporter** \> **Elektroniske meldinger** \> **Elektroniske meldinger**, og velg **NO mva-retur**-EM-behandlingen i listen til venstre.
2. Velg **Ny** i hurtigfanen **Meldinger**.

    Handlingen **NO MVA Opprett melding** er forhåndsdefinert i dialogboksen **Kjør behandling**.

3. Velg **OK**. Den nye elektroniske meldingen opprettes.
4. I feltene **Fra dato** og **Til dato** for meldingen definerer du perioden du vil sende mva-retur for.
5. Valgfritt: Skriv inn en beskrivelse i **Beskrivelse**-feltet. Denne teksten inkluderes ikke i rapporten.

![Opprette en melding.](media/emea-nor-vat-return-create-message.png)

## <a name="collect-sales-tax-payments"></a><a id="collect-sales-tax-payments"></a>Samle inn mva-betalinger

Følg denne fremgangsmåten for å utføre handlingen **NO MVA Samle inn mva-betaling**.

1. Gå til **Avgift** \> **Forespørsler og rapporter** \> **Elektroniske meldinger** \> **Elektroniske meldinger**, og velg meldingen som ble opprettet i **NO mva-retur**-EM-behandlingen.
2. På hurtigfanen **Meldinger** velger du **Samle inn data**.

    Handlingen **NO MVA Samle inn mva-betaling** er forhåndsdefinert i dialogboksen **Kjør behandling**.

3. Velg **OK**.
4. Betalingslinjene for mva posteres i løpet av perioden som ble angitt for meldingen som vises i hurtigkategorien **Meldingselementer** i forbindelse med den valgte meldingen.

![Samle inn mva-betalinger.](media/emea-nor-vat-return-collect-sales-tax-payments.png)

I henhold til XSD-skjemaet (XML Schema Definition) for mva-returer kan en mva-retur inneholde en merknad som bruker en verdi fra en opplistingsliste med verdier eller en fritekstnota som er begrenset til 4 000 tegn. 

Følg denne fremgangsmåten for å legge til en merknad som bruker en verdi fra en opplistingsliste.

1. Velg den elektroniske meldingen på hurtigfanen **Meldinger** som det skal angis en merknad for.
2. I hurtigfanen **Tilleggsfelt for melding** velger du tilleggsfeltet **NO mva-notat for mva-retur**.
3. I kolonnen **Feltverdi** velger du en verdi i oppslagsfeltet.

Følg denne fremgangsmåten for å legge til en fritekstnota som er begrenset til 4 000 tegn.

1. Velg den elektroniske meldingen på hurtigfanen **Meldinger** som det skal angis en merknad for.
2. I hurtigfanen **Tilleggsfelt for melding** velger du tilleggsfeltet **NO mva-notat for mva-retur**.
3. I kolonnen **Feltverdi** velger du en **fritekstnota** i oppslagsfeltet.
4. Velg **Vedlegg**, og velg deretter **Ny** \> **Notat** i handlingsruten.
5. I **Notat**-feltet angir du notatet din. Dette notatet blir inkludert i mva-returen i XML-format når det genereres.

Følg denne fremgangsmåten for å inkludere en betalings-ID, eller et KID-nummer, i den digitale mva-returen. Dette KID-nummeret kan bare brukes når verdien `<fastsattMerverdiavgift>` (total merverdiavgift \[mva\] for rapporteringsperioden) er negativ.

1. Velg den elektroniske meldingen på hurtigfanen **Meldinger** som det skal angis KID-nummer for.
2. I hurtigfanen **Tilleggsfelt for melding** velger du tilleggsfeltet **NO mva-betalings-ID**.
3. Angi KID-nummeret i **Feltverdi**-kolonnen.

## <a name="mark-the-message-as-ready-to-generate-the-vat-return"></a><a id="ready-to-generate"></a>Merk meldingen som klar til å generere mva-returen

Følg denne fremgangsmåten for å utføre handlingen **NO MVA Klar til å generere mva**.

1. Gå til **Avgift** \> **Forespørsler og rapporter** \> **Elektroniske meldinger** \> **Elektroniske meldinger**, og velg meldingen som ble opprettet i **NO mva-retur**-EM-behandlingen.
2. På hurtigfanen **Meldinger** velger du **Oppdater status**.

    Handlingen **NO MVA Klar til å generere mva** og statusen **NO MVA Klar til å generere mva** er forhåndsdefinert i dialogboksen **Kjør behandling**.

3. Velg **OK**. Statusen for meldingen oppdateres til **NO MVA Klar til å generere mva** og knappen **Generer rapport** blir tilgjengelig.

![Merk en melding som klar til å generere en mva-retur.](media/emea-nor-vat-return-ready-to-generate.png)

Hvis du vil fortsette å samle inn data for rapporten, velger du **Oppdater status** og endrer status for meldingen tilbake til **NO MVA Ny elektronisk melding opprettet**.

## <a name="preview-the-vat-return-in-microsoft-excel"></a><a id="preview-vat-return"></a>Forhåndsvis mva-returen i Microsoft Excel

Følg denne fremgangsmåten for å utføre handlingen **NO MVA Forhåndsvisning av mva-retur i Excel**.

1. Gå til **Avgift** \> **Forespørsler og rapporter** \> **Elektroniske meldinger** \> **Elektroniske meldinger**, og velg meldingen som ble opprettet i **NO mva-retur**-EM-behandlingen.
2. Velg **Generer rapport** i kategorien **Melding**.
3. Velg **NO MVA Forhåndsvisning av mva-retur i Excel** i dialogboksen **Kjør behandling**.
4. For rapporteringsperioder som inneholder et stort volum av avgiftstransaksjoner, anbefaler vi at du kjører rapporten i satsvis modus. På hurtigfanen **Kjør i bakgrunnen** velger du avmerkingsboksen **Satsvis behandling**. Deretter angir du feltet **Oppgavebeskrivelse** og andre parametere for partiet.
5. Velg **OK**. Det legges ved en ny fil til meldingen, men status for meldingsstatusen er ikke endret.
6. Velg **Vedlegg**, og velg deretter **Forhåndsvis MVA-retur.xls**.
7. Velg **Åpne** i handlingsruten for å forhåndsvise mva-returen i Excel-format.

## <a name="generate-the-vat-return"></a><a id="generate-vat-return"></a>Generer mva-returen

Følg denne fremgangsmåten for å utføre handlingen **NO MVA Generer MVA-retur**.

1. Gå til **Avgift** \> **Forespørsler og rapporter** \> **Elektroniske meldinger** \> **Elektroniske meldinger**, og velg meldingen som ble opprettet i **NO mva-retur**-EM-behandlingen.
2. Velg **Generer rapport** i hurtigfanen **Meldinger**.
3. Velg **NO MVA Generer MVA-retur** i dialogboksen **Kjør behandling**.
4. For rapporteringsperioder som inneholder et stort volum av avgiftstransaksjoner, anbefaler vi at du kjører rapporten i satsvis modus. På hurtigfanen **Kjør i bakgrunnen** velger du avmerkingsboksen **Satsvis behandling**. Deretter angir du feltet **Oppgavebeskrivelse** og andre parametere for partiet.
5. Velg **OK**.

    ![Generere en mva-retur.](media/emea-nor-vat-return-generate-vat-return.png)

    Meldingens status oppdateres til **NO MVA XML-generert mva-retur er vellykket**, og en ny `mvamelding.xml`-fil legges ved i meldingen.

7. Velg **Vedlegg**, og velg deretter **mvamelding.xml**.
8. Velg **Åpne** i handlingsruten for å forhåndsvise mva-returen i XML-format.

## <a name="validate-the-vat-return-in-the-tax-administration-web-service"></a><a id="validate-vat-return"></a>Valider mva-returen i webtjenesten for skatteadministrasjon

Dette trinnet består av **NO MVA Validering**-sekvensen, som inneholder følgende handlinger:

- **NO MVA Send forespørsel om validering** – Denne handlingen overfører `mvamelding.xml`-filen til API for skatteetaten, mottar `valideringsresultat.xml`-filen som inneholder resultatene av forretningsvalideringen som utføres på `mvamelding.xml`-filen, og knytter `valideringsresultat.xml`-filen til den elektroniske meldingen.
- **NNO MVA Importer valideringssvar** – Denne handlingen analyserer informasjon fra `valideringsresultat.xml`-filen og oppdaterer statusen til den elektroniske meldingen. Hvis forretningsvalideringen som skatteadministrasjonen utfører, blir bestått, oppdaterer denne handlingen statusen til **NO MVA-returvalidering bestått**. Hvis det blir funnet feil under forretningsvalideringen, oppdaterer denne handlingen statusen til **NO MVA Mva-returvalideringsfeil**, knytter en XSLT-transformasjon (Extensible Stylesheet Language Transformations) til `valideringsresultat.xml`-filen, og knytter den transformerte filen til handlingsloggen for posten. Du kan deretter se nærmere på den som `valideringsresultat_transformed.html`-filen som er knyttet til handlingsloggen for handlingen **NO MVA Importer valideringssvar**.
- **NO MVA Generer forespørsel om forekomst** – Denne handlingen forbereder en forespørsel om neste trinn i prosessen, [Send inn mva-returen](#submit-vat-return).

Følg disse trinnene for å validere mva-returen i webtjenesten for skatteadministrasjon.

1. Gå til **Avgift** \> **Forespørsler og rapporter** \> **Elektroniske meldinger** \> **Elektroniske meldinger**, og velg meldingen som ble opprettet i **NO mva-retur**-EM-behandlingen.
2. Velg **Send rapport** i hurtigfanen **Meldinger**.

    Handlingen **NO MVA Send forespørsel om validering** er forhåndsdefinert i dialogboksen **Kjør behandling**.

4. Velg **OK**.

    Systemet kjører automatisk handlingene **NO MVA Send forespørsel om validering**, **NO MVA Importer valideringssvar** og **NO MVA Generer forespørsel om forekomst** én om gangen. Hvis forretningsvalideringen som skatteadministrasjonen utfører, blir bestått, oppdateres statusen for den elektroniske meldingen til **NO MVA-returvalidering bestått**. Hvis feil blir identifisert under forretningsvalideringen, oppdateres statusen til **NO MVA Mva-returvalideringsfeil**.

5. Hvis du vil se gjennom informasjonen om eventuelle feil som ble funnet under forretningsvalideringen som skatteetaten utfører, velger du linjen for **NO MVA Importer valideringssvar** i hurtigfanen **Handlingslogg**.
6. Velg **Vedlegg**, og velg deretter den vedlagte HTML-filen.
7. Velg **Åpne** i handlingsruten. Filen åpnes i et webleservindu, og du kan se gjennom innholdet i en tabell. Når du har brukt rettelser, kan du gå tilbake til trinnet [Generer mva-returen](#generate-vat-return) for å generere XML-filen på nytt.

## <a name="submit-the-vat-return"></a><a id="submit-vat-return"></a>Send inn mva-returen

Når `mvamelding.xml`-filen er validert av skatteetaten, har den elektroniske meldingen statusen **NO MVA-returvalidering bestått**, og du kan sende `mvamelding.xml`-filen til Altinn.

Prosessen med å sende en mva-retur omfatter følgende handlinger:

- **NO MVA Send forespørsel om å opprette forekomst** – Denne handlingen sender en forespørsel til Altinn3-App API for å opprette en forekomst for ytterligere mva-returinnsending. Deretter mottas svaret, og det knyttes til den elektroniske meldingen.
- **NO MVA Importer opprettelsessvar for forekomst** – Denne handlingen importerer den nødvendige informasjonen fra svaret til systemet for ytterligere innsending.
- **NO MVA Generer innsending av mva** – Denne handlingen oppretter en spesiell teknisk `konvolutt.xml`-fil som må sendes til Altinn3-App-API før `mvamelding.xml`-filen.
- **NO MVA Last opp innsending av mva** – Denne handlingen sender den tekniske `konvolutt.xml`-filen til Altinn3-App API.
- **NO MVA Last opp mva-retur** – Denne handlingen sender den `mvamelding.xml`-filen til Altinn3-App API.
- **NO MVA Fullstendig datafylling** – Denne handlingen sender en forespørsel om å fullføre overføringen av mva-returen til Altinn3-App-API.
- **NO MVA Fullfør innsending av MVA-retur** – Denne handlingen sender en forespørsel om å fullføre overføringsprosessen til Altinn3-App-API.
- **NO MVA Send statusforespørsel om tilbakemelding** – Denne handlingen ber om statusen til valideringsprosessen for den innsendte mva-returen.
- **NO MVA Importer tilbakemeldingsstatusrespons** – Denne handlingen importerer valideringsstatusen for mva-retur til systemet.
- **NO MVA Send forespørsel om tilbakemelding** – Denne handlingen ber om statusen til valideringen for den innsendte mva-returen.
- **NO MVA Importer tilbakemeldingssvar** – Denne handlingen importerer den nødvendige informasjonen fra svaret som inneholder valideringsresultatene for mva-returen.
- **NO VAT Last ned valideringsresultat** – Denne handlingen laster ned valideringsdetaljene for mva-returen.
- **NO MVA Importer endelig valideringsresultat** – Denne handlingen importerer informasjon om valideringsdetaljene for mva-retur til systemet, og oppdaterer statusen til den elektroniske meldingen. Hvis ingen feil ble identifisert i den sendte mva-returen, oppdateres statusen til **NO MVA MVA-meldingen lastet opp til Skatteetaten ble validert**. Hvis feil ble identifisert i den sendte mva-returen, oppdateres statusen til **NO mva Feilvalidering av opplastet MVA-retur**.

Følg denne fremgangsmåten for å sende inn mva-returen.

1. Gå til **Avgift** \> **Forespørsler og rapporter** \> **Elektroniske meldinger** \> **Elektroniske meldinger**, og velg meldingen som ble opprettet i **NO mva-retur**-EM-behandlingen.
2. Velg **Send rapport** i hurtigfanen **Meldinger**.

    Handlingen **NO MVA Send forespørsel om å opprette forekomst** er forhåndsdefinert i dialogboksen **Kjør behandling**.

3. Velg **OK**.

    Systemet kjører alle handlingene i den forrige listen én om gangen. Det kan ta flere minutter før tilbakemeldingen om mva-returen er klar på skatteetatsiden. I dette tilfellet stoppes **Send mva-retur**, og statusen oppdateres til **NO MVA Tilbakemelding tilbys ikke**. Vent i fem til ti minutter, og velg deretter **Send rapport** i hurtigfanen **Melding**.

    Handlingen **NO MVA Send statusforespørsel om tilbakemelding** er forhåndsdefinert i dialogboksen **Kjør behandling**.

4. Velg **OK**. Mva-returinnsendingen er fullført når den elektroniske meldingen har statusen **NO MVA MVA-meldingen lastet opp til Skatteetaten ble validert**.

## <a name="download-attachments"></a><a id="download-attachments"></a>Last ned vedlegg

Når en mva-retur er sendt, kan du laste ned betalingsinformasjonen i XML-format og kvitteringen i PDF-format.

1. Gå til **Avgift** \> **Forespørsler og rapporter** \> **Elektroniske meldinger** \> **Elektroniske meldinger**, og velg meldingen som ble opprettet i **NO mva-retur**-EM-behandlingen.
2. Velg **Send rapport** i hurtigfanen **Meldinger**.
3. Velg **NO MVA Last ned kvittering** eller **NO MVA Last ned betalingsinformasjon** i dialogboksen **Kjør behandling**.
4. Velg **OK**. Filen `betalingsinformasjon.xml` ("NO MVA Last ned betalingsinformasjon") eller `kvittering.pdf` ("NO MVA Last ned kvittering") er knyttet til den elektroniske meldingen.
5. Velg **Vedlegg**, og velg deretter **betalingsinformasjon.xml** eller **kvittering.pdf**.
6. Velg **Åpne** i handlingsruten.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

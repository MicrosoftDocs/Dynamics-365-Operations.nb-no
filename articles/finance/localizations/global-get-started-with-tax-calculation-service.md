---
title: Kom i gang med avgiftsberegning
description: Dette emnet forklarer hvordan du konfigurerer avgiftsberegning.
author: wangchen
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 454608c2c3a86b71cf181129c762c837c5165902
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336662"
---
# <a name="get-started-with-the-tax-calculation-preview"></a>Kom i gang med avgiftsberegning (forhåndsversjon)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dette emnet gir informasjon om hvordan du kommer i gang med avgiftsberegning. Først veileder den deg gjennom konfigurasjonstrinnene i Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS) og Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Deretter gjennomgås de vanlige prosessen for bruk av funksjonene for avgiftsberegning i Finance- og Supply Chain Management-transaksjoner.

Oppsettet består av fire hovedtrinn:

1. I LCS installerer du avgiftsberegning.
2. I RCS konfigurerer du funksjonen for avgiftsberegning. Dette oppsettet er ikke spesifikt for en juridisk enhet. Det kan deles på tvers av juridiske enheter i Finance og Supply Chain Management.
3. I Finance og Supply Chain Management definerer du parametere for avgiftsberegning etter juridisk enhet.
4. I Finance og Supply Chain Management oppretter du transaksjoner, for eksempel salgsordrer, og bruker avgiftsberegning til å bestemme og beregne avgifter.

## <a name="prerequisites"></a>Forutsetninger

Før du kan fullføre trinnene i dette emnet må følgende forutsetninger være på plass:

- Du har tilgang til LCS-kontoen din, og du har distribuert et LCS-prosjekt med et nivå 2-miljø (eller over) som kjører Dynamics 365 versjon 10.0.18 med [KB4616360](https://fix.lcs.dynamics.com/Issue/Details?kb=4616360&bugId=568738&dbType=3&qc=1f1c04ff39adad74ef871f539e8d73e14c1893ef7cc4b6e3f7d5c5864ec2781a) eller senere.
- Du har tilgang til RCS-kontoen din.
- Du har kontaktet Microsoft for å aktivere testversjonering i det distribuerte Finance- eller Supply Chain Management-miljøet.

## <a name="set-up-tax-calculation-in-lcs"></a>Konfigurer avgiftsberegning i LCS

1. Logg på [LCS](https://lcs.dynamics.com)
2. Fullfør oppsettet for Microsoft Power Platform-integrering. Hvis du vil ha mer informasjon, kan du se [Oversikt over tillegg](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Velg ett av de distribuerte ikke-produksjonsmiljøene, og velg deretter **Installer et nytt tillegg**.
4. Velg **Avgiftsberegning (forhåndsversjon)**.
5. Les og godta betingelsene, og velg deretter **Installer**.

## <a name="set-up-tax-calculation-in-rcs"></a>Konfigurer avgiftsberegning i RCS

Trinnene i denne delen er ikke knyttet til en bestemt juridisk enhet. Du må bare fullføre denne fremgangsmåten én gang, og du kan fullføre den i en hvilken som helst juridisk enhet i RCS.

1. Logg på [RCS](https://marketing.configure.global.dynamics.com/).
2. I arbeidsområdet **Elektronisk rapportering** legger du til en ny konfigurasjonsleverandør. Bruk firmanavnet som navn på leverandøren. Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Velg konfigurasjonsleverandøren du akkurat opprettet, og velg deretter **Angi som aktiv**.
4. Velg **Microsoft**-konfigurasjonsleverandøren, og velg deretter **Repositorier**.
5. Velg **Global** i **Type**-feltet.
6. Velg **Åpne**.
7. Gå til **Avgiftsdatamodell**, utvid filtreet, og velg deretter **Avgiftskonfigurasjon**.
8. Velg den siste versjonen, og velg deretter **Importer**.
9. Gå tilbake til arbeidsområdet **Globaliseringsfunksjoner (forhåndsversjon)**, velg **Funksjoner**, velg flisen **Avgiftsberegning**, og velg deretter **Legg til**.
10. Velg en av følgende funksjonstyper:

    - **Ny funksjon** – Opprett et funksjonsoppsett som har tomt innhold.
    - **Basert på eksisterende funksjon** – Opprett en funksjon fra en eksisterende funksjon, og kopier innholdet fra det eksisterende funksjonsoppsettet.

11. Angi et navn på og en beskrivelse av den nye funksjonen, og velg deretter **Opprett funksjon**.

    Når funksjonen er opprettet, opprettes det automatisk en utkastversjon.

12. Velg utkastversjonen av funksjonen, og velg deretter **Rediger**. Siden **Oppsett for avgiftsberegning** fylles ut.
13. Velg **Konfigurasjonsversjon**. Du skal se konfigurasjonsversjonen du importerte i trinn 8.

    Microsoft oppgir en standard mva-konfigurasjon for tillegget for avgiftsberegning. Denne konfigurasjonen dekker det meste av kravene til mva-beregningsvirkemåte. Den vil bli oppdatert basert på tilbakemeldinger fra markedet. Hvis du må utvide konfigurasjonen for å oppfylle bestemte krav, kan du se [Slik bygger du utvidelse i avgiftstjeneste](./tax-service-add-data-fields-tax-integration-by-extension.md) for informasjon om hvordan du genererer og velger din egen avgiftskonfigurasjon.

    Når du har valgt **Konfigurasjonsversjon**, vises flere ekstra faner:

    - **Avgiftskoder** – Denne kategorien er obligatorisk. Den brukes til å vedlikeholde hoveddata for avgiftskoder. Alle avgiftskoder som opprettes på denne fanen, synkroniseres automatisk med Finance når du aktiverer gjeldende versjon av mva-funksjonsoppsettet i den juridiske enheten.
    - **Relevans for avgiftskoder** – Denne kategorien er obligatorisk. Den brukes til å definere en matrise som bestemmer mva-koden, mva-gruppen og mva-gruppen for varen. Mva-koden som bestemmes, brukes til å beregne mva-beløpet. Verdiene i feltene **Mva-kode**, **Mva-gruppe** og **Mva-gruppe for vare** returneres til Finance.
    - **Relevans for mva-registreringsnummer for kunde** – Denne fanen er valgfri. Hvis du har flere avgiftsregistreringsnumre for én kunde, kan avgiftsberegning automatisk fastsette riktig avgiftsregistreringsnummer. I matrisen i denne kategorien definerer du reglene som tillegget bruker til å avgjøre. Ellers vil Finance og Supply Chain Management fortsette å bruke standard avgiftsregistreringsnummer på avgiftspliktige dokumenter for salgstransaksjoner.
    - **Relevans for mva-registreringsnummer for leverandør** – Denne fanen er valgfri. Hvis du har flere avgiftsregistreringsnumre for én leverandør, kan avgiftsberegning automatisk fastsette riktig avgiftsregistreringsnummer. I matrisen i denne kategorien definerer du reglene som tillegget bruker til å avgjøre. Ellers vil Finance og Supply Chain Management fortsette å bruke standard avgiftsregistreringsnummer på avgiftspliktige dokumenter for kjøpstransaksjoner.
    - **Relevans for listekode** – Denne fanen er valgfri. Den kan hjelpe deg med å fastslå verdien i **Listekode**-feltet automatisk ved hjelp av mer fleksible og konfigurerbare regler. I matrisen i denne kategorien kan du definere reglene som tillegget bruker til å avgjøre. Ellers vil Finance og Supply Chain Management fortsette å bruke standardkoden på avgiftspliktige dokumenter.

14. På **Avgiftskoder**-fanen velger du **Legg til** og angir deretter avgiftskoden og en beskrivelse.
15. Velg **Avgiftskomponent**. Avgiftskomponenten er en gruppe med metoder som ble definert i den forrige versjonen av den valgte avgiftskonfigurasjonen. Følgende avgiftskomponenter er tilgjengelige:

    - Etter nettobeløp
    - Etter bruttobeløp
    - Etter antall
    - Etter margin
    - Avgift på avgift

16. Velg **Lagre**. Flere felter blir tilgjengelige, basert på avgiftskomponenten du valgte.
17. Bruk følgende alternativer til å identifisere avgiftskodens natur:

    - Er Fritak
    - Er Bruk avgift
    - Er Snudd avregning
    - Ekskluder fra grunnlagsbeløpsberegning

    For et use tax-scenario definerer du en enkelt mva-kode som har en positiv mva-sats, og merker den som **Er Use tax**.

    For et scenario for snudd avregning definerer du to avgiftskoder, en som har en positiv mva-sats, og den andre har en negativ mva-sats, men samme satsverdi. Merk den negative avgiftskoden som **Er snudd avgift**. Hvis du vil ha mer informasjon om løsningen for snudd avregning i Finance, kan du se [Mekanisme for snudd avregning for MVA/GST-skjema](emea-reverse-charge.md).
    
    For enkelte avgiftstyper som skal utelates i beregningen av avgiftsgrunnlagsbeløpet for pris inklusive transaksjoner, for eksempel egendefinert avgift i noen land, merker du av for **Ekskluder fra grunnlagsbeløpsberegning**.

    Vedlikehold mva-satser og mva-beløpsgrensene for denne avgiftskoden.

18. Gjenta trinn 14 til og med 17 for å legge til alle andre avgiftskoder som kreves.
19. På fanen **Relevans for avgiftskoder** velger du kolonnene som kreves for å bestemme riktig avgiftskode, og deretter velger du **Legg til**.
20. Angi eller velg verdier for hver kolonne. Feltene **Mva-kode**, **Mva-gruppe** og **Mva-gruppe for vare** blir utdataene for denne matrisen.
21. Gjenta trinn 19 til og med 20 for å definere bruk av registreringsnumre for kundeavgift, leverandøravgiftsnumre og listekoder.
22. Velg **Lagre**, og lukk deretter siden.
23. Velg **Endre status** \> **Fullført**. Når statusen er endret til **Fullført**, kan du ikke lenger redigere versjonen.
24. Velg **Endre status** \> **Publiser**. Denne versjonen av oppsettet av avgiftsfunksjonen blir skjøvet til det globale repositoriet, og vil være synlig for hver juridiske enhet i Finance.

## <a name="dynamics-365-setup"></a>Dynamics 365-oppsett

Når du har fullført oppsettet i RCS, som beskrevet i den forrige delen, vil du ha en publisert versjon av mva-funksjonen. Følg denne fremgangsmåten for å konfigurere avgiftsberegning i Finance.

Oppsettet i denne delen utføres av en juridisk enhet. Du må konfigurere det for hver juridiske enhet du vil aktivere avgiftsberegning for i Finance.

1. I Finance går du til **Avgift** \> **Oppsett** \> **Avgiftskonfigurasjon** \> **Oppsett av avgiftsberegning (forhåndsversjon)**.
2. Angi følgende felt i fanen **Generelt**:

    - **Aktiver avgiftsberegning** – Merk av i denne boksen for å aktivere avgiftsberegning for den juridiske enheten. Hvis det ikke er aktivert for gjeldende juridisk enhet, vil den juridiske enheten fortsette å bruke den eksisterende avgiftsmotoren til å bestemme og beregne avgift.
    - **Funksjonsoppsett** – Velg et oppsett og en versjon for den juridiske enheten. Hvis du vil ha mer informasjon om hvordan du setter opp og fullfører en publisert avgiftsfunksjon, kan du se den forrige delen av dette emnet.
    - **Forretningsprosess** – Velg forretningsprosessene som skal aktiveres.
    - **Aktiver avgiftskodejustering** – Sett dette alternativet til **Ja** for å aktivere avgiftskodejusteringer på mva-siden.

3. I kategorien **Beregning** definerer du den forventede avrundingsregelen for den juridiske enheten.
4. I kategorien **Feilbehandling** definerer du den forventede metoden for feilbehandling for den juridiske enheten. Tre alternativer er tilgjengelige for hver resultatkode:

    - Ingen
    - Advarsel
    - Feil

5. Lagre oppsettet.
6. Gjenta trinn 1 til og med 5 for hver ekstra juridiske enhet.

## <a name="transaction-processing"></a>Transaksjonsbehandling

Når du har fullført alle oppsettprosedyrene, kan du bruke avgiftsberegning til å bestemme og beregne avgifter i Finance. Fremgangsmåten for å behandle transaksjoner forblir de samme. Følgende transaksjoner støttes i Finance versjon 10.0.18:

- Salgsprosess

    - Salgstilbud
    - Salgsordre
    - Bekreftelse
    - Plukkliste
    - Følgeseddel
    - Salgsfaktura
    - Kreditnota
    - Returordre
    - Hodegebyr
    - Linjetillegg

- Innkjøpsprosess

    - Bestilling
    - Bekreftelse
    - Tilgangsliste
    - Produktkvittering
    - Innkjøpsfaktura
    - Hodegebyr
    - Linjetillegg
    - Kreditnota
    - Returordre
    - Innkjøpsrekvisisjon
    - Belastning på innkjøpsrekvisisjonslinje
    - Tilbudsforespørsel
    - Belastning på tilbudsforespørselshode
    - Belastning på tilbudsforespørselslinje

- Beholdningsprosess

    - Overføringsordre – send
    - Overføringsordre – motta

---
title: Kom i gang med avgiftsberegning
description: Dette emnet forklarer hvordan du konfigurerer avgiftsberegning.
author: wangchen
ms.date: 03/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 61ee15901a091ee733b83c8cbaa5b84801fa8e5d
ms.sourcegitcommit: 4afd1e0b325d27cd7c4e0d9a198400b038262ac7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/09/2022
ms.locfileid: "8558320"
---
# <a name="get-started-with-tax-calculation"></a>Kom i gang med avgiftsberegning

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om hvordan du kommer i gang med avgiftsberegning. Delene i dette emnet veileder deg gjennom utforming på høyt nivå og konfigurasjonstrinnene i Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS), Dynamics 365 Finance og Dynamics 365 Supply Chain Management. 

Oppsettet består av tre hovedtrinn.

1. I LCS installerer du tillegget for avgiftsberegning.
2. I RCS konfigurerer du funksjonen for avgiftsberegning. Dette oppsettet er ikke spesifikt for en juridisk enhet. Det kan deles på tvers av juridiske enheter i Finance og Supply Chain Management.
3. I Finance og Supply Chain Management definerer du parametere for avgiftsberegning etter juridisk enhet.

## <a name="high-level-design"></a>Utforming på høyt nivå

### <a name="runtime-design"></a><a name="runtime"></a> Kjøretidsutforming

Illustrasjonen nedenfor viser kjøretidsutforming på høyt nivå av avgiftsberegning. Fordi avgiftsberegning kan integreres med flere Dynamics 365-apper, bruker illustrasjonen integreringen med Finance som et eksempel.

1. En transaksjon, for eksempel en salgsordre eller en bestilling, opprettes i Finance.
2. Finance bruker automatisk standardverdiene for mva-gruppen og mva-gruppen for vare.
3. Når **Utgående merverdiavgift**-knappen er valgt for transaksjonen, utløses avgiftsberegningen. Finance sender deretter nyttelasten til avgiftsberegningstjenesten.
4. Avgiftsberegningstjenesten samsvarer med nyttelasten med forhåndsdefinerte regler i avgiftsfunksjonen for å finne en mer nøyaktig mva-gruppe og mva-gruppe for vare samtidig.

    - Hvis nyttelasten kan samsvares med matrisen for **Anvendelse av avgiftsgruppe**, overstyrer den mva-gruppeverdien med verdien i mva-gruppen som samsvarer i relevansregelen. Ellers fortsetter den å bruke mva-gruppeverdien fra Finance.
    - Hvis nyttelasten kan samsvares med matrisen for **Anvendelse av vareavgiftsgruppe**, overstyrer den varens mva-gruppeverdi med den samsvarende mva-gruppen for vare i relevansregelen. Ellers fortsetter den å bruke mva-gruppeverdien for vare fra Finance.

5. Avgiftsberegningstjenesten fastsetter endelige avgiftskoder ved å bruke skjæringspunktet mellom mva-gruppen og varens mva-gruppe.
6. Avgiftsberegningstjenesten beregner avgift basert på de endelige avgiftskodene som er bestemt.
7. Avgiftsberegningstjeneste returnerer resultatet av avgiftsberegningen til Finance.

![Kjøretidsutforming for avgiftsberegning.](media/tax-calculation-runtime-logic.png)

### <a name="high-level-configuration"></a>Konfigurasjon på høyt nivå

Følgende trinn gir en oversikt på høyt nivå over konfigurasjonsprosessen for avgiftsberegningstjenesten.

1. I LCS installerer du tillegget **Avgiftsberegning** i LCS-prosjekt.
2. I RCS oppretter du funksjonen for **Avgiftsberegning**.
3. I RCS konfigurerer du funksjonen for **Avgiftsberegning**:

    1. Velg avgiftskonfigurasjonsversjonen.
    2. Opprett avgiftskoder.
    3. Opprett en avgiftsgruppe.
    4. Opprett en vareavgiftgruppe.
    5. Valgfritt: Opprett avgiftsgrupperelevans hvis du vil overstyre standard mva-gruppe som angis fra hoveddataene for kunde eller leverandør.
    6. Valgfritt: Opprett varegrupperelevans hvis du vil overstyre standard mva-gruppe for vare som angis fra hoveddataene for vare.

4. I RCS fullfører og publiserer du funksjonen **Avgiftsberegning**.
5. Velg den publiserte funksjonen **Avgiftsberegning** i Finance.

Når du har fullført disse trinnene, blir følgende oppsett automatisk synkronisert fra RCS til Finance.

- Mva-koder
- Mva-grupper
- Vare, mva-grupper

De gjenværende delene i dette emnet gir mer detaljerte konfigurasjonstrinn.

## <a name="prerequisites"></a>Forutsetninger

Før du kan fullføre de gjenværende trinnene i dette emnet må følgende forutsetninger være på plass:<!--TO HERE-->

- Du må ha tilgang til LCS-kontoen din, og du må ha distribuert et LCS-prosjekt som har et nivå 2-miljø (eller over) som kjører Dynamics 365 versjon 10.0.21 eller senere.
- Du må opprette et RCS-miljø for din organisasjon, og du må ha tilgang til kontoen. Hvis du vil ha mer informasjon om hvordan du oppretter et RCS-miljø, kan du se [Oversikt over Regulatory Configuration Service](rcs-overview.md).
- Følgende funksjoner må være aktivert i arbeidsområdet **Funksjonsbehandling** i det distribuerte Finance- eller Supply Chain Management-miljøet, basert på dine forretningsbehov:

    - Avgiftsberegningstjeneste
    - Støtte for flere mva-registreringsnumre
    - Avgift i overføringsordre

- Følgende funksjoner må være aktivert i arbeidsområdet **Funksjonsbehandling** i det distribuerte RCS-miljøet.

    - Globaliseringsfunksjoner

- Følgende roller bør tilordnes brukerne i RCS-miljøet etter behov:

    - Utvikler av elektronisk rapportering
    - Utvikler for globaliseringsfunksjon
    - Avgiftsmotorutvikler
    - Funksjonell konsulent for avgiftsmotor
    - Avgiftstjenesteutvikler

## <a name="set-up-tax-calculation-in-lcs"></a>Konfigurer avgiftsberegning i LCS

1. Logg på [LCS](https://lcs.dynamics.com)
2. Fullfør oppsettet for Microsoft Power Platform-integrering. Hvis du vil ha mer informasjon, kan du se [Oversikt over tillegg](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Velg ett av de distribuerte miljøene, og velg deretter **Installer et nytt tillegg**.
4. Velg **Avgiftsberegning**.
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
8. Velg riktig [versjon av avgiftskonfigurasjonen](global-tax-calcuation-service-overview.md#versions) basert på Finance-versjonen, og velg deretter **Importer**.
9. I arbeidsområdet **Globaliseringsfunksjoner** velger du **Funksjoner**, flisen **Avgiftsberegning** og deretter **Legg til**.
10. Velg en av følgende funksjonstyper:

    - **Ny funksjon** – Opprett et funksjonsoppsett som har tomt innhold.
    - **Basert på eksisterende funksjon** – Opprett en funksjon fra en eksisterende funksjon, og kopier innholdet fra det eksisterende funksjonsoppsettet.

11. Angi et navn på og en beskrivelse av den nye funksjonen, og velg deretter **Opprett funksjon**.

    Når funksjonen er opprettet, opprettes det automatisk en utkastversjon. Du kan velge **Hent denne versjonen** for å basere utkastversjonen på nytt for en hvilken som helst fullført versjon.

12. Velg utkastversjonen av funksjonen, og velg deretter **Rediger**. Siden **Oppsett for avgiftsberegning** fylles ut.
13. Velg **Konfigurasjonsversjon**. Du skal se konfigurasjonsversjonen du importerte i trinn 8.

    Microsoft oppgir en standard mva-konfigurasjon for avgiftsberegning. Denne konfigurasjonen dekker det meste av kravene til mva-beregningsvirkemåte. Den vil bli oppdatert basert på tilbakemeldinger fra markedet. Hvis du må utvide konfigurasjonen for å oppfylle bestemte krav, kan du se [Slik bygger du utvidelse i avgiftstjeneste](./tax-service-add-data-fields-tax-integration-by-extension.md) for informasjon om hvordan du genererer og velger din egen avgiftskonfigurasjon.

14. Når du har valgt **Konfigurasjonsversjon**, vises flere ekstra faner. Følg rekkefølgen som vises her, for å fullføre det obligatoriske faneoppsettet.

    **Obligatorisk oppsett**

    - **Avgiftskoder** – Vedlikehold hoveddata for avgiftskoder. Alle avgiftskoder som opprettes på denne fanen, synkroniseres automatisk med Finance når du aktiverer gjeldende versjon.
    - **Avgiftsgruppe** – Definer hoveddataene for avgiftsgruppen og avgiftskodene under gruppen.
    - **Vareavgiftsgruppe** – Definer hoveddataene for vareavgiftsgruppen og avgiftskodene under gruppen.

    **Valgfritt oppsett**

    - **Anvendelse av avgiftsgruppe** – Definer en matrise som bestemmer avgiftsgruppen. Hvis ingen anvendelsesregler i denne matrisen samsvarer med det avgiftspliktige dokumentet fra Dynamics 365, bruker Avgiftsberegning standardverdien på den avgiftspliktige dokumentlinjen.
    - **Anvendelse av vareavgiftsgruppe** – Definer en matrise som bestemmer vareavgiftsgruppen. Hvis ingen anvendelsesregler i denne matrisen samsvarer med det avgiftspliktige dokumentet fra Dynamics 365, bruker Avgiftsberegning standardverdien på den avgiftspliktige dokumentlinjen.
    - **Relevans for mva-registreringsnummer for kunde** – Hvis du har flere avgiftsregistreringsnumre for én kunde, kan Avgiftsberegning automatisk fastsette riktig avgiftsregistreringsnummer. I matrisen i denne kategorien definerer du reglene som skal brukes til å avgjøre. Ellers vil Finance og Supply Chain Management fortsette å bruke standard avgiftsregistreringsnummer på avgiftspliktige dokumenter for salgstransaksjoner.
    - **Relevans for mva-registreringsnummer for leverandør** – Hvis du har flere avgiftsregistreringsnumre for én leverandør, kan Avgiftsberegning automatisk fastsette riktig avgiftsregistreringsnummer. I matrisen i denne kategorien definerer du reglene som skal brukes til å avgjøre. Ellers vil Finance og Supply Chain Management fortsette å bruke standard avgiftsregistreringsnummer på avgiftspliktige dokumenter for kjøpstransaksjoner.
    - **Relevans for listekode** – Fastslå verdien i **Listekode**-feltet automatisk ved hjelp av mer fleksible og konfigurerbare regler. I matrisen i denne kategorien definerer du reglene som skal brukes til å avgjøre. Ellers vil Finance og Supply Chain Management fortsette å bruke standardkoden på avgiftspliktige dokumenter.

14. På **Avgiftskoder**-fanen velger du **Legg til** og angir deretter avgiftskoden og en beskrivelse.
15. Velg **Avgiftskomponent**. Avgiftskomponenten er en gruppe med metoder som ble definert i den forrige versjonen av den valgte avgiftskonfigurasjonen. Følgende avgiftskomponenter er tilgjengelige:

    - Etter nettobeløp
    - Etter bruttobeløp
    - Etter antall
    - Etter margin
    - Avgift på avgift

16. Velg **Lagre**. Flere felter blir tilgjengelige, basert på avgiftskomponenten du valgte.
17. Bruk følgende alternativer til å identifisere avgiftskodens natur:

    - Er fritak
    - Er bruk avgift
    - Er snudd avregning
    - Ekskluder fra grunnlagsbeløpsberegning

    For et use tax-scenario definerer du en enkelt mva-kode som har en positiv mva-sats, og merker den som **Er bruk avgift**.

    For et scenario for snudd avregning definerer du to avgiftskoder, en som har en positiv mva-sats, og den andre har en negativ mva-sats, men samme satsverdi. Merk den negative avgiftskoden som **Er snudd avgift**. Hvis du vil ha mer informasjon om løsningen for snudd avregning i Finance, kan du se [Mekanisme for snudd avregning for MVA/GST-skjema](emea-reverse-charge.md).

    For enkelte avgiftstyper som skal utelates fra beregningen av avgiftsgrunnlagsbeløpet for pris inklusive transaksjoner, (for eksempel egendefinert avgift i noen land eller områder), merker du av for **Ekskluder fra grunnlagsbeløpsberegning**. Hvis du vil ha mer informasjon om denne parameteren, kan du se [Beregning av avgift på toppen av prisen når Priser inkluderer mva. er aktivert](global-exclude-from-tax-base-amount-calculation.md).

    Vedlikehold mva-satser og mva-beløpsgrensene for denne avgiftskoden.

18. Gjenta trinn 14 til og med 17 for å legge til alle andre avgiftskoder som kreves.
19. På fanen **Avgiftsgruppe** velger du kolonnen **Avgiftsgruppe**, legger den til i matrisen som inndatabetingelsen og legger deretter til linjer for å vedlikeholde hoveddataene for avgiftsgruppen.

    Her er et eksempel:

    | Avgiftsgruppe    | Mva-koder           |
    | ------------ | ------------------- |
    | DEU_Domestic | DEU_VAT19; DEU_VAT7 |
    | DEU_EU       | DEU_Exempt          |
    | BEL_Domestic | BEL_VAT21; BEL_VAT6 |
    | BEL_EU       | BEL_Exempt          |

20. På fanen **Vareavgiftsgruppe** velger du kolonnen **Vareavgiftsgruppe**, legger den til i matrisen som inndatabetingelsen og legger deretter til linjer for å vedlikeholde hoveddataene for vareavgiftsgruppen.

    Her er et eksempel:

    | Vareavgiftsgruppe | Mva-koder                                    |
    | -------------- | -------------------------------------------- |
    | Full           | DEU_VAT19; BEL_VAT21; DEU_Exempt; BEL_Exempt |
    | Redusert        | DEU_VAT7; BEL_VAT6; DEU_Exempt; BEL_Exempt   |

21. På fanen **Relevans for avgiftsgruppe** velger du kolonnene som kreves for å bestemme riktig avgiftsgruppe, og deretter velger du **Legg til**. Angi eller velg verdier for hver kolonne. Feltet **Avgiftsgruppe** blir utdataene fra denne matrisen. Hvis denne fanen ikke er konfigurert, brukes avgiftsgruppen på transaksjonslinjen.

    Her er et eksempel:

    | Forretningsprosess | Send fra | Send til | Avgiftsgruppe    |
    | ---------------- | --------- | ------- | ------------ |
    | Salg            | DEU       | DEU     | DEU_Domestic |
    | Salg            | DEU       | FRA     | DEU_EU       |
    | Salg            | BEL       | BEL     | BEL_Domestic |
    | Salg            | BEL       | FRA     | BEL_EU       |
    
    > [!NOTE]
    > Hvis standard mva-gruppe på de avgiftspliktige dokumentlinjene er riktig, lar du denne matrisen stå tom. Hvis du vil ha mer informasjon, kan du se delen [Kjøretidsutforming](#runtime) i dette emnet.

22. På fanen **Relevans for vareavgiftsgruppe** velger du kolonnene som kreves for å bestemme riktig avgiftskode, og deretter velger du **Legg til**. Angi eller velg verdier for hver kolonne. Feltet **Vareavgiftsgruppe** blir utdataene fra denne matrisen. Hvis denne fanen ikke er konfigurert, brukes vareavgiftsgruppen på transaksjonslinjen.

    Her er et eksempel:

    | Varekode | Avgiftsgruppe for vare |
    | --------- | -------------- |
    | D0001     | Full           |
    | D0003     | Redusert        |

    > [!NOTE]
    > Hvis standard mva-varegruppe på de avgiftspliktige dokumentlinjene er riktig, lar du denne matrisen stå tom. Hvis du vil ha mer informasjon, kan du se delen [Kjøretidsutforming](#runtime) i dette emnet.

    Hvis du vil ha mer informasjon om hvordan avgiftskoder bestemmes i Avgiftsberegning, kan du se [Logikk for fastsettelse av avgiftsgruppe og vareavgiftsgruppe](global-sales-tax-group-determination.md).

23. Angi relevansen for registreringsnumre for kundeavgift, leverandøravgiftsnumre og listekoder, basert på forretningsbehovene.
24. Velg **Lagre**, og lukk deretter siden.
25. Velg **Endre status** \> **Fullført**. Når statusen er endret til **Fullført**, kan du ikke lenger redigere versjonen.
26. Velg **Endre status** \> **Publiser**. Denne versjonen av oppsettet av avgiftsfunksjonen blir skjøvet til det globale repositoriet, og vil være synlig for hver juridiske enhet i Finance.

## <a name="set-up-tax-calculation-in-dynamics-365"></a>Konfigurer avgiftsberegning i Dynamics 365

Når du har fullført oppsettet i RCS, vil du ha en publisert versjon av mva-funksjonen. Følg denne fremgangsmåten for å konfigurere avgiftsberegning i Finance.

Oppsettet i denne delen utføres av en juridisk enhet. Du må konfigurere det for hver juridiske enhet du vil aktivere avgiftsberegning for i Finance.

1. I Finance går du til **Avgift** \> **Oppsett** \> **Avgiftskonfigurasjon** \> **Parametere for avgiftsberegning**.
2. Angi følgende felt i fanen **Generelt**:

    - **Aktiver tjeneste for avgiftsberegning** – Merk av i denne boksen for å aktivere avgiftsberegning for den juridiske enheten. Hvis det ikke er aktivert for gjeldende juridisk enhet, vil den juridiske enheten fortsette å bruke den eksisterende avgiftsmotoren til å bestemme og beregne avgift.
    - **Funksjonsoppsett** – Velg et oppsett og en versjon for den juridiske enheten. Hvis du vil ha mer informasjon om hvordan du setter opp og fullfører en publisert avgiftsfunksjon, kan du se den forrige delen av dette emnet.
    - **Forretningsprosess** – Velg forretningsprosessene som skal aktiveres.

3. I kategorien **Beregning** definerer du den forventede avrundingsregelen for den juridiske enheten. Hvis du vil ha mer informasjon om avrundingslogikken, kan du se [Avrundingsregler for avgiftsberegning](https://go.microsoft.com/fwlink/?linkid=2166988).
4. I kategorien **Feilbehandling** definerer du den forventede metoden for feilbehandling for den juridiske enheten. Tre alternativer er tilgjengelige:

    - Ingen
    - Advarsel
    - Feil

    Du kan definere en metode for feilhåndtering for hver resultatkode i **Detaljer**-delen. Hvis enkelte resultatkoder ikke er synkronisert fra avgiftsberegningstjenesten, kan du imidlertid definere en standardmetode i **Generelt**-delen.

5. På fanen **Flere mva-registreringer** kan du aktivere mva-deklarering, EU-salgsliste og Intrastat separat for å fungere i et scenario med flere mva-registreringer. Hvis du vil ha mer informasjon om mva-rapportering for flere mva-registreringer, kan du se [Rapportering for flere mva-registreringer](emea-reporting-for-multiple-vat-registrations.md).
6. Lagre oppsettet, og gjenta de forrige trinnene for hver juridiske enhet. Når en ny versjon blir publisert, og du vil at den skal brukes, angir du feltet **Funksjonsoppsett** på **Generelt**-fanen på siden **Parametere for avgiftsberegning** (se trinn 2).

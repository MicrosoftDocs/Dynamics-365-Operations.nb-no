---
title: Definere økonomisk integrering for detaljhandelskanaler
description: Dette emnet gir retningslinjer for hvordan du konfigurerer regnskapsintegreringsfunksjonaliteten for detaljhandelskanaler.
author: josaw
manager: annbe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: a987e75834ddde486421a425a621e66f0b6e063f
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811171"
---
# <a name="set-up-the-fiscal-integration-for-retail-channels"></a>Definere økonomisk integrering for detaljhandelskanaler

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Innledning

Dette emnet gir retningslinjer for hvordan du konfigurerer regnskapsintegreringsfunksjonaliteten for detaljhandelskanaler. Hvis du vil ha mer informasjon om regnskapsintegrering, kan du se [Oversikt over regnskapsintegrering for detaljhandelskanaler](fiscal-integration-for-retail-channel.md).

Fremgangsmåten for å definere regnskapsintegreringen omfatter følgende hovedoppgaver:

1. Konfigurer regnskapskoblinger som representerer regnskapsenheter eller -tjenester som brukes til regnskapsregistreringformål, for eksempel regnskapsskrivere.
2. Konfigurer dokumentleverandører som genererer regnskapsdokumenter som skal registreres i regnskapsenheter eller -tjenester av regnskapskoblinger.
3. Konfigurer regnskapsregistreringsprosessen som definerer en sekvens med bilagsregistreringstrinn og regnskapskoblingene og leverandørene av regnskapsdokument som skal brukes for hvert trinn.
4. Tilordne bilagsregistreringsprosessen til funksjonalitetsprofiler for salgssted (POS).
5. Tilordne tekniske profiler for kobling til maskinvareprofiler.

## <a name="set-up-a-fiscal-registration-process"></a>Definere en bilagsregistreringsprosess

Før du bruker regnskapsintegreringsfunksjonaliteten, bør du konfigurere følgende innstillinger:

1. Oppdater detaljhandelsparametere.

    1. På **Delte parametere for detaljhandel**-siden, i **Generelt**-fanen angi **Aktiver regnskapsintegrering** til **Ja**. I kategorien **Nummerserier** definerer du nummersekvenser for følgende referanser:

        - Nummer for teknisk profil for regnskap
        - Gruppenummer for regnskapskobling
        - Nummer for registreringsprosess

    2. På **Detaljhandelsparametere**-siden definer nummersekvensen for nummer for funksjonell profil for regnskap.

    > [!NOTE]
    > Nummerserier er valgfrie. Numre for alle regnskapsintegrasjonsenheter kan genereres fra nummerserier eller manuelt.

2. Last opp konfigurasjoner av regnskapskoblinger og leverandører av regnskapsdokument.

    En leverandør for regnskapsdokumentet er ansvarlig for å generere regnskapsdokumenter som representerer detaljhandelstransaksjoner og hendelser som er registrert på salgsstedet i et format som også brukes for samhandlingen med en regnskapsenhet eller -tjeneste. For eksempel kan en regnskapsdokumentleverandør generere en representasjon av en bilagskvittering i XML-format.

    En regnskapskobling er ansvarlig for kommunikasjonen med en regnskapsenhet eller -tjeneste. En regnskapskobling kan for eksempel sende en bilagskvittering som en regnskapsdokumentleverandør opprettet i et XML-format til en bilagsskriver. Hvis du vil ha mer informasjon om regnskapsintegreringskomponentene, se [Bilagsregistreringsprosess og regnskapsintegreringeseksempler for regnskapsenheter](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

    1. På siden **Regnskapskoblinger** (**Detaljhandel \> Kanaloppsett \> Regnskapsintegrering \> Regnskapskoblinger**) laster du opp en XML-konfigurasjon for hver enhet eller tjeneste du planlegger å bruke for regnskapsintegreringsformål.

        > [!TIP]
        > Ved å velge **Vis** kan du vise alle funksjonelle og tekniske profiler som er knyttet til gjeldende regnskapskobling.

    2. På siden **Leverandører for regnskapsdokument** (**Detaljhandel \> Kanaloppsett \> Regnskapsintegrering \> Leverandører for regnskapsdokument**) laster du opp en XML-konfigurasjon for hver enhet eller tjeneste du planlegger å bruke.

        > [!TIP]
        > Ved å velge **Vis** kan du vise alle funksjonelle profiler som er knyttet til gjeldende finansdokumentleverandør.

    For eksempler på konfigurasjoner av regnskapskoblinger og regnskapsdokumentleverandører, se [Eksempler på regnskapsintegrering i SDK for detaljhandel](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-retail-sdk).

    > [!NOTE]
    > Datatilordning regnes som en del av en regnskapsdokumentleverandør. Hvis du vil definere forskjellige datatilordninger for samme tilkobling (for eksempel tilstandsspesifikke reguleringer), bør du opprette forskjellige regnskapsdokumentleverandører.

3. Opprett funksjonelle profiler for kobling og tekniske profiler for kobling.

    1. På siden **Funksjonelle profiler for kobling** (**Detaljhandel \> Kanaloppsett \> Regnskapsintegrering \> Funksjonelle profiler for kobling**), opprett en funksjonell profil for kobling for hver kombinasjon av regnskapskobling og finansdokumentleverandør som er knyttet til denne regnskapskoblingen.

        1. Velg et tilkoblingsnavn.
        2. Velg en dokumentleverandør.

        Du kan endre datatilordningparametrene i en funksjonell profil for kobling. Hvis du vil gjenopprette standardparameterne som er definert i konfigurasjon av regnskapsdokumentleverandør, velger du **Oppdater**.

        **Eksempler**

        |   | Formater | Eksempel |
        |---|--------|---------|
        | **Mva-satsinnstillinger** | verdi: VATrate | 1 : 2000, 2 : 1800 |
        | **Tilordning av mva-koder** | VATcode : verdi | vat20: 1, vat18: 2 |
        | **Tilordning av betalingsmiddeltyper** | TenderType: verdi | Kontant: 1, kort: 2 |

        > [!NOTE]
        > Funksjonelle profiler for kobling er firmaspesifikke. Hvis du planlegger å bruke samme kombinasjon av regnskapskobling og finansdokumentleverandør i forskjellige firmaer, bør du opprette en funksjonell profil for kobling for hvert firma.

    2. På siden **Tekniske profiler for kobling** (**Detaljhandel \> Kanaloppsett \> Regnskapsintegrering \> Tekniske profiler for kobling**) oppretter du en teknisk profil for kobling for hver regnskapskobling.

        1. Velg et tilkoblingsnavn.
        2. Velg en tilkoblingstype. For enheter som er koblet til en maskinvarestasjon, velger du **Lokal**.

            > [!NOTE]
            > Bare lokale koblinger støttes.

        Parameterne i kategoriene **Enhet** og **Innstillinger** i en teknisk profil for kobling kan endres. Hvis du vil gjenopprette standardparameterne som er definert i konfigurasjon for regnskapskobling, velger du **Oppdater**. Når en ny versjon av en XML-konfigurasjon er lastet inn, får du en melding om at gjeldende regnskapskobling eller regnskapsdokumentleverandør allerede er i bruk. Denne prosedyren overstyre ikke manuelle endringer som tidligere ble gjort i funksjonelle profiler for kobling og tekniske profiler for kobling. For å bruke standardsettet med parametere fra en ny konfigurasjon klikker du på siden **Funksjonelle profiler for kobling** eller siden **Tekniske profiler for kobling** og velger **Oppdater**.

4. Opprett grupper for regnskapskobling.

    En gruppe for regnskapskobling kombinerer funksjonelle profiler for regnskapskoblinger som utfører identiske funksjoner, og brukes på samme trinn i en regnskapsregistreringsprosess. Hvis for eksempel flere bilagsskrivermodeller kan brukes i en detaljhandel, kan regnskapskoblinger for disse bilagsskriverne kombineres i en gruppe for regnskapskobling.

    1. På siden **Gruppe for regnskapskobling** (**Detaljhandel \> Kanaloppsett \> Regnskapsintegrering \> Grupper for regnskapskobling**) oppretter du en ny gruppe for regnskapskobling.
    2. Legg til funksjonelle profiler i koblingsgruppen. I kategorien **Funksjonelle profiler** velger du **Legg til** og velger et profilnummer. Hver regnskapskobling i en koblingsgruppe kan bare ha én funksjonsprofil.
    3. Hvis du vil avbryte bruken av den funksjonelle profilen, må du sette **Deaktiver** til **Ja**. Denne endringen påvirker bare den gjeldende koblingsgruppen. Du kan fortsette å bruke den samme funksjonsprofilen i andre tilkoblingsgrupper.

5. Opprett en bilagsregistreringsprosess.

    En bilagsregistreringsprosess er definert av rekkefølgen på registreringstrinnene og koblingsgruppen som brukes for hvert trinn.

    1. På siden **Bilagsregistreringsprosess** (**Detaljhandel \> Kanaloppsett \> Regnskapsintegrering \> Bilagsregistreringsprosesser**) oppretter du en ny post for hver unike prosess i bilagsregistreringen.
    2. Legg til registreringstrinn i prosessen:

        1. Velg **Legg til**.
        2. Velg en regnskapskoblingstype.
        3. I feltet **Gruppenummer** velger du riktig gruppe for regnskapskobling.

6. Tilordne enheter av bilagsregistreringsprosessen til POS-profiler.

    1. På siden **Funksjonalitetsprofiler for salgssted** (**Detaljhandel \> Kanaloppsett \> POS-oppsett \> POS-profiler \> Funksjonalitetsprofiler**) tilordnes bilagsregistreringsprosessen til en funksjonalitetsprofil for salgssted. Velg **Rediger** og deretter i kategorien **Bilagsregistreringsprosess** i feltet **Prosessnummer** velger du en prosess.
    2. På siden **Maskinvareprofil for salgssted** (**Detaljhandel \> Kanaloppsett \> POS-oppsett \> POS-profiler \> Maskinvareprofiler**) tilordner du tekniske profiler for kobling til en maskinvareprofil. Velg **Rediger**, legg til en linje i kategorien **Eksterne regnskapsenheter** og deretter, i feltet **Profilnummer**, velger du en teknisk profil for kobling.

    > [!NOTE]
    > Du kan legge til flere tekniske profiler i den samme maskinvareprofilen. En maskinvareprofil eller funksjonalitetsprofil for salgssted skal imidlertid bare ha ett skjæringspunkt med en gruppe for regnskapskobling.

    Bilagsregistreringsflyten er definert av renskapsregistreringsprosessen og også av noen parametere for regnskapsintegreringskomponenter: Commerce Runtime-utvidelsen for regnskapsdokumentleverandøren og Maskinvarestasjon-utvidelsen for regnskapskoblingen.

    - Abonnementet for hendelser og transaksjoner til regnskapsregistrering er forhåndsdefinert i regnskapsdokumentleverandøren.
    - Regnskapsdokumentleverandøren er også ansvarlig for å identifisere regnskapskoblingen som brukes til regnskapsregistrering. Den samsvarer med de funksjonelle profilene for kobling som er inkludert i gruppen for regnskapskobling som er angitt for gjeldende trinn i regnskapsregistreringsprosessen for teknisk profil for kobling som er tilordnet til maskinvareprofilen for maskinvarestasjonen som salgsstedet er koblet til.
    - Regnskapsdokumentleverandøren bruker innstillingene for datatilordning fra regnskapsdokumentleverandørkonfigurasjonen for å transformere transaksjons-/hendelsesdata som for eksempel avgifter og betalinger når det genereres et regnskapsdokument.
    - Når regnskapsdokumentleverandøren genererer et regnskapsdokument, kan regnskapskoblingen enten sende det til regnskapsenheten som den er, eller analysere det og gjøre det om til en sekvens med kommandoer for API-enheten, avhengig av hvordan kommunikasjonen håndteres.

7. På siden **Bilagsregistreringsprosess** (**Detaljhandel \> Kanaloppsett \> Regnskapsintegrering \> Bilagsregistreringsprosesser**) velger du **Valider** for å validere regnskapsregistreringsprosessen.

    Vi anbefaler at du kjører denne typen validering i følgende tilfeller:

    - Når du har fullført alle innstillinger for en ny registreringsprosess, inkludert når du tilordner registreringsprosesser til salgsstedsfunksjonalitetsprofiler og maskinvareprofiler.
    - Når du endrer en eksisterende regnskapsregistreringsprosess, og disse endringene kan føre til at en annen registreringskobling velges ved kjøretid (for eksempel hvis du endrer koblingsgruppen for et trinn i regnskapsregistreringsprosessen, aktiverer en funksjonell profil for kobling i en tilkoblingsgruppe eller legger til en ny funksjonell profil for kobling i en koblingsgruppe).
    - Når du gjør endringer i tilordningen av tekniske profiler for kobling til maskinvareprofiler.

8. På siden **Distribusjonsplan** kjører du **1070**- og **1090**-jobber for å overføre data til kanaldatabasen.

## <a name="set-up-fiscal-texts-for-discounts"></a>Konfigurere bilagstekster for rabatter

I noen tilfeller må en spesiell tekst skrives ut på en bilagskvittering hvis en rabatt brukes. Du kan konfigurere bilagstekster for rabatter på siden **Gruppe for regnskapskobling** (**Detaljhandel \> Kanaloppsett \> Regnskapsintegrering \> Grupper for regnskapskobling**).

- For manuelle rabatter som brukes på salgsstedet, konfigurerer du en bilagstekst for informasjonskoden eller informasjonskodegruppen som er angitt som **Produktrabatt**-informasjonskoden i funksjonsprofilen for salgssted.

    1. På siden **Gruppe for regnskapskobling** velger du **Tekst for bilagskvittering**.
    2. I kategorien **Infokoder** velger du **Legg til** og velger en informasjonskode eller informasjonskodegruppe.
    3. I **Informasjonskodenummer** velger du en verdi.
    4. I feltet **Underkodenummer** velger en verdi hvis det kreves en delkode for den valgte informasjonskoden.
    5. I feltet **Tekst for bilagskvittering** angir du en bilagstekst som skal skrives ut på en bilagskvittering.
    6. Sett alternativet **Skriv ut brukerinndata på bilagskvittering** til **Ja** for å overstyre teksten på en bilagskvittering med informasjon som brukeren angir manuelt på salgsstedet. Dette alternativet gjelder bare for informasjonskoder som har inndatatypen **Tekst**.

    > [!NOTE]
    > Du kan angi en bilagstekst for flere informasjonskoder for å støtte scenarioer der informasjonskodegrupper, koblede infokoder og utløste infokoder brukes. I disse scenarioene inneholder bilagskvitteringene bilagstekstene fra alle infokoder som er koblet til transaksjonslinjen der rabatten ble brukt.

- Du bør definere en regnskapstekst for rabatt-ID-en for kanalspesifikke rabatter.

    1. På siden **Gruppe for regnskapskobling** velger du **Tekst for bilagskvittering**.
    2. I kategorien **Rabatter** velger du **Legg til**, og deretter velger du rabatt-ID.
    3. I feltet **Tekst for bilagskvittering** angir du en bilagstekst som skal skrives ut på en bilagskvittering.

    > [!NOTE]
    > Hvis flere rabatter brukes på samme transaksjonslinje, vil bilagskvitteringen inneholde bilagstekster fra alle rabatter som er koblet til denne transaksjonslinjen.

## <a name="set-error-handling-settings"></a>Angi innstillinger for feilbehandling

Feilbehandlingsalternativene som er tilgjengelige i regnskapsintegrasjonen, defineres i bilagsregistreringsprosessen. Hvis du vil ha mer informasjon om feilbehandling i regnskapsintegreringen, kan du se [Feilbehandling](fiscal-integration-for-retail-channel.md#error-handling).

1. På siden **Bilagsregistreringsprosess** (**Detaljhandel \> Kanaloppsett \> Regnskapsintegrering \> Bilagsregistreringsprosesser**) kan du angi følgende parametere for hvert trinn i bilagsregistreringsprosessen.

    - **Tillat overhopping** – Denne parameteren aktiverer **Hopp over**-alternativet i dialogboksen for feilbehandling.
    - **Tillat Merk som registrert** – Denne parameteren aktiverer **Merk som registrert**-alternativer i dialogboksen for feilbehandling.
    - **Fortsett ved feil** – Hvis denne parameteren er aktivert, vil bilagsregistreringsprosessen fortsette på salgsstedskassen hvis bilagsregistrering av en transaksjon eller hendelsen mislykkes. Hvis ikke, for å kjøre bilagsregistrering av neste transaksjon eller hendelse, må operatøren prøve å kjøre den mislykkede bilagsregistreringen på nytt, hoppe over den eller merke transaksjonen eller hendelsen som registrert. Hvis du vil ha mer informasjon, se [Valgfri bilagsregistrering](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Hvis parameteren **Fortsett ved feil** er aktivert, deaktiveres parameteren **Tillat overhopping** og **Tillat Merk som registrert** automatisk.

2. Alternativene **Hopp over** og **Merk som registrert** i dialogboksen for feilbehandling krever tillatelsen **Tillat å hoppe over registrering eller merke som registrert**. Derfor må du på siden **Tillatelsesgrupper** (**Detaljhandel \> Ansatte \> Tillatelsesgrupper**) aktivere tillatelsen **Tillat å hoppe over registrering eller merke som registrert**.
3. Alternativene **Hopp over** og **Merk som registrert** lar operatorer angi tilleggsinformasjon når bilagsregistreringen mislykkes. Hvis du vil gjøre denne funksjonaliteten tilgjengelig, må du angi infokodene **Hopp over** og **Merk som registrert** i en gruppe for regnskapskobling. Informasjonen som operatorene angir, lagres deretter som en infokodetransaksjon som er knyttet til regnskapstransaksjon. Hvis du vil ha mer informasjon om infokoder, kan du se [Informasjonskoder og informasjonskodegrupper](../info-codes-retail.md).

    > [!NOTE]
    > **Produkt**-utløserfunksjonen støttes ikke for informasjonskodene som brukes til **Hopp over** og **Merk som registrert** i grupper for regnskapskobling.

    - På siden **Gruppe for regnskapskobling** i fanen **Infokoder** velger du infokoder eller informasjonskodegrupper i feltene **Hopp over** og **Merk som registrert**.

    > [!NOTE]
    > Ett regnskapsdokument og ett ikke-regnskapsdokument kan genereres på et hvilket som helst trinn i bilagsregistreringsprosessen. En finansdokumentleverandørutvidelse identifiserer hver type transaksjon eller hendelse som er relatert til regnskapsdokumenter eller ikke-regnskapsdokumenter. Feilhåndteringsfunksjonen gjelder bare for regnskapsdokumenter.
    >
    > - **Regnskapsdokument** – Et obligatorisk dokument som må registreres med suksess (for eksempel en bilagskvittering).
    > - **Ikke-regnskapsdokument** – Et ekstra dokument for transaksjonen eller hendelsen (for eksempel en gavekortseddel).

4. Hvis operatøren må være i stand til å fortsette å behandle den aktuelle operasjonen (for eksempel oppretting eller avslutning av en transaksjon) etter at en tilstandskontrollfeil oppstår, bør du aktivere tillatelsen **Tillat å hoppe over tilstandskontrollfeil** på siden **Tillatelsesgrupper** (**Detaljhandel \> Ansatte \> Tillatelsesgrupper**). Hvis du vil ha mer informasjon om tilstandskontrollprosedyren, se [Tilstandskontroll for bilagsregistrering](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Konfigurere X-/Z-regnskapsrapporter fra salgsstedet

For å aktivere X-/Z-regnskapsrapporter fra salgsstedet bør du legge til nye knapper i et salgsstedsoppsett.

- På siden **Knappegrupper** følger du instruksjonene i [Legge til salgsstedsoperasjoner i salgsstedsoppsett ved hjelp av utforming for knappegruppe](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) for å installere utformingen og oppdatere et salgsstedsoppsett.

    1. Velg oppsettet som skal oppdateres. 
    2. Legg til en ny knapp, og angi **Skriv ut regnskapsår X**-knappeegenskapen.
    3. Legg til en ny knapp, og angi **Skriv ut regnskapsår Z**-knappeegenskapen.
    4. På siden **Distribusjonsplan** kjører du **1090**-jobben for å overføre endringer til kanaldatabasen.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Aktivere manuell kjøring av utsatt bilagsregistrering

For å aktivere manuell utføring av en utsatt bilagsregistrering bør du legge til en ny knapp i et POS-oppsett.

- På siden **Knappegrupper** følger du instruksjonene i [Legge til salgsstedsoperasjoner i salgsstedsoppsett ved hjelp av utforming for knappegruppe](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) for å installere utformingen og oppdatere et salgsstedsoppsett.

    1. Velg oppsettet som skal oppdateres.
    2. Legg til en ny knapp, og angi **Fullfør bilagsregistreringsprosess**-knappeegenskapen.
    3. På siden **Distribusjonsplan** kjører du **1090**-jobben for å overføre endringene dine til kanaldatabasen.

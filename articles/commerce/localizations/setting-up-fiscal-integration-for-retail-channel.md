---
title: Definere økonomisk integrering for handelskanaler
description: Dette emnet gir retningslinjer for hvordan du konfigurerer regnskapsintegreringsfunksjonaliteten for handelskanaler.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c15104e0f34c1f6cb6a599d506dad741be3e5e9e
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388396"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Definere økonomisk integrering for handelskanaler

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dette emnet gir retningslinjer for hvordan du konfigurerer regnskapsintegreringsfunksjonaliteten for handelskanaler. Hvis du vil ha mer informasjon om regnskapsintegrering, kan du se [Oversikt over regnskapsintegrering for handelskanaler](fiscal-integration-for-retail-channel.md).

## <a name="set-up-commerce-parameters"></a>Konfigurer handelsparametere

1. På siden **Delte handelsparametere**, i **Generelt**-fanen, angir du **Aktiver regnskapsintegrering** til **Ja**.
1. I kategorien **Nummerserier** definerer du nummersekvenser for følgende referanser:

    - Nummer for teknisk profil for regnskap
    - Gruppenummer for regnskapskobling
    - Nummer for registreringsprosess

1. På **Handelsparametere**-siden definerer du nummersekvensen for nummer for funksjonell profil for regnskap.

    > [!NOTE]
    > Nummerserier er valgfrie. Numre for alle regnskapsintegrasjonsenheter kan genereres fra nummerserier eller manuelt.

## <a name="set-up-a-fiscal-registration-process"></a>Definere en bilagsregistreringsprosess

Fremgangsmåten for å definere regnskapsintegreringen omfatter følgende hovedoppgaver:

- Konfigurer regnskapskoblinger som representerer regnskapsenheter eller -tjenester som brukes til regnskapsregistreringformål, for eksempel regnskapsskrivere.
- Konfigurer dokumentleverandører som genererer regnskapsdokumenter som skal registreres i regnskapsenheter eller -tjenester av regnskapskoblinger.
- Konfigurer regnskapsregistreringsprosessen som definerer en sekvens med bilagsregistreringstrinn og regnskapskoblingene og leverandørene av regnskapsdokument som skal brukes for hvert trinn.
- Tilordne bilagsregistreringsprosessen til funksjonalitetsprofiler for salgssted (POS).
- Tilordne tekniske profiler for kobling til maskinvareprofiler.
- Tilordne tekniske profiler for kobling til profiler for maskinvare eller funksjonalitet for salgssted.

### <a name="upload-configurations-of-fiscal-document-providers"></a>Last opp konfigurasjoner av leverandører av regnskapsdokumenter

En leverandør for regnskapsdokumentet er ansvarlig for å generere regnskapsdokumenter som representerer transaksjoner og hendelser som er registrert på salgsstedet i et format som også brukes for samhandlingen med en regnskapsenhet eller -tjeneste. For eksempel kan en regnskapsdokumentleverandør generere en representasjon av en bilagskvittering i XML-format.

Følg trinnene nedenfor for å laste opp konfigurasjoner av leverandører av regnskapsdokumenter.

1. I Commerce-hovedkvarteret går du til siden **Leverandører for regnskapsdokument** (**Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Leverandører for regnskapsdokument**).
1. Last opp en XML-konfigurasjon for hver enhet eller tjeneste du planlegger å bruke.

> [!TIP]
> Ved å velge **Vis** kan du vise alle funksjonelle profiler som er knyttet til gjeldende finansdokumentleverandør.

> [!NOTE]
> Datatilordning regnes som en del av en regnskapsdokumentleverandør. Hvis du vil definere forskjellige datatilordninger for samme tilkobling (for eksempel tilstandsspesifikke reguleringer), bør du opprette forskjellige regnskapsdokumentleverandører.

### <a name="upload-configurations-of-fiscal-connectors"></a>Last opp konfigurasjoner av regnskapskontakter

En regnskapskobling er ansvarlig for kommunikasjonen med en regnskapsenhet eller -tjeneste. En regnskapskobling kan for eksempel sende en bilagskvittering som en regnskapsdokumentleverandør opprettet i et XML-format til en bilagsskriver. Hvis du vil ha mer informasjon om regnskapsintegreringskomponentene, se [Bilagsregistreringsprosess og regnskapsintegreringeseksempler for regnskapsenheter og -tjenester](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

Følg trinnene nedenfor for å laste opp konfigurasjoner av regnskapskoblinger.

1. I Commerce-hovedkvarteret går du til siden **Regnskapskoblinger** (**Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Regnskapskoblinger**).
1. Last opp en XML-konfigurasjon for hver enhet eller tjeneste du planlegger å bruke til regnskapsintegreringsformål.

> [!TIP]
> Ved å velge **Vis** kan du vise alle funksjonelle og tekniske profiler som er knyttet til gjeldende regnskapskobling.

For eksempler på konfigurasjoner av regnskapskoblinger og regnskapsdokumentleverandører, se [Eksempler på regnskapsintegrering i SDK for Commerce](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-commerce-sdk).

### <a name="create-connector-functional-profiles"></a>Opprett funksjonsprofiler for kobling

Hvis du vil opprette funksjonsprofiler for koblinger, gjør du følgende.

1. I Commerce-hovedkvarteret går du til siden **Funksjonsprofiler for kobling** (**Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Funksjonsprofiler for kobling**).
1. Opprett en funksjonsprofil for kobling for hver kombinasjon av en regnskapskobling og en finansdokumentleverandør som er relatert til denne regnskapskoblingen, ved å følge trinnene nedenfor:

    1. Velg et tilkoblingsnavn.
    1. Velg en dokumentleverandør.

#### <a name="change-data-mapping-parameters-in-a-connector-functional-profile"></a>Endre datatilordningparametrene i en funksjonell profil for kobling

Du kan endre datatilordningparametrene i en funksjonell profil for kobling. Følgende tabell gir noen eksempler på datatilordningsparametere i en funksjonsprofil for kobling.

| Parameter | Format | Eksempel |
|-----------|--------|---------|
| Mva-satsinnstillinger | verdi: VATrate | 1 : 2000, 2 : 1800 |
| Tilordning av mva-koder | VATcode : verdi | vat20: 1, vat18: 2 |
| Tilordning av betalingsmiddeltyper | TenderType: verdi | Kontant: 1, kort: 2 |

Hvis du vil gjenopprette standardparameterne som er definert i konfigurasjon av regnskapsdokumentleverandør, velger du **Oppdater** på siden **Funksjonsprofiler for kobling**.

> [!NOTE]
> Funksjonelle profiler for kobling er firmaspesifikke. Hvis du planlegger å bruke samme kombinasjon av regnskapskobling og finansdokumentleverandør for forskjellige firmaer, bør du opprette en funksjonell profil for kobling for hvert firma.

### <a name="create-connector-technical-profiles"></a>Opprett tekniske profiler for kobling

Hvis du vil opprette tekniske profiler for koblinger, gjør du følgende.

1. I Commerce-hovedkvarteret går du til siden **Tekniske profiler for kobling** (**Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Tekniske profiler for kobling**).
1. Opprett en teknisk profil for kobling for hver regnskapskobling ved å følge denne fremgangsmåten:

    1. Velg et tilkoblingsnavn.
    1. Velg en tilkoblingstype:

        - Velg **Lokal** for enheter eller tjenester som er koblet til en maskinvarestasjon, eller som finnes i det lokale nettverket.
        - Velg **Ekstern** for eksterne tjenester.
        - For interne koblinger i Commerce Runtime (CRT) velger du **Intern**. 

    1. Velg en koblingsplassering:

        - Hvis koblingen befinner seg på maskinvarestasjonen, velger du **Maskinvarestasjon**.
        - Hvis koblingen finnes i kassen på salgsstedet, velger du **Kasse**.

Parameterne i kategoriene **Enhet** og **Innstillinger** i en teknisk profil for kobling kan endres. Hvis du vil gjenopprette standardparameterne som er definert i konfigurasjon for regnskapskobling, velger du **Oppdater**. Når en ny versjon av en XML-konfigurasjon lastes inn, får du en melding om at gjeldende regnskapskobling eller regnskapsdokumentleverandør allerede er i bruk. Denne prosedyren overstyre ikke manuelle endringer som tidligere ble gjort i funksjonelle profiler for kobling og tekniske profiler for kobling. For å bruke standardsettet med parametere fra en ny konfigurasjon velger du **Oppdater** på siden **Funksjonelle profiler for kobling** eller siden **Tekniske profiler for kobling**.

Følg denne fremgangsmåten hvis du må definere spesifikke parametere for en individuell POS-kasse eller -butikk.

1. Velg menyelementet **Overstyr**.
1. Opprett en ny post på **Overstyr**-siden.
1. Velg en butikk eller en POS-kasse. Du kan overstyre parametere for den valgte tekniske profilen for en enkelt POS-kasse eller alle POS-kasser i en enkelt butikk.
1. Angi parametere for den valgte POS-kassen eller butikken på **Enhet**-fanen.

### <a name="create-fiscal-connector-groups"></a>Opprett grupper for regnskapskobling

En gruppe for regnskapskobling kombinerer funksjonelle profiler for regnskapskoblinger som utfører identiske funksjoner, og brukes på samme trinn i en regnskapsregistreringsprosess. Hvis for eksempel flere bilagsskrivermodeller kan brukes i en butikk, kan regnskapskoblinger for disse bilagsskriverne kombineres i en gruppe for regnskapskobling.

Hvis du vil opprette en regnskapskobling, gjør du følgende.

1. Gå til siden **Gruppe for regnskapskobling** (**Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Grupper for regnskapskobling**).
1. Opprett en ny gruppe for regnskapskobling.
1. Legg til funksjonelle profiler i koblingsgruppen. I kategorien **Funksjonelle profiler** velger du **Legg til** og velger et profilnummer. Hver regnskapskobling i en koblingsgruppe kan bare ha én funksjonsprofil.
1. Hvis du vil avbryte bruken av den funksjonelle profilen, må du sette **Deaktiver** til **Ja**. Denne endringen påvirker bare den gjeldende koblingsgruppen. Du kan fortsette å bruke den samme funksjonsprofilen i andre tilkoblingsgrupper.

### <a name="create-a-fiscal-registration-process"></a>Opprett en bilagsregistreringsprosess

En bilagsregistreringsprosess er definert av rekkefølgen på registreringstrinnene og koblingsgruppen som brukes for hvert trinn.

Følg denne fremgangsmåten for å opprette en bilagsregistreringsprosess.

1. I Commerce-hovedkvarteret går du til siden **Bilagsregistreringsprosess** (**Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Bilagsregistreringsprosess**).
1. Opprett en ny post for hver unike bilagsregistreringsprosess.
1. Bruk denne fremgangsmåten til å legge til registreringstrinn i prosessen:

    1. Velg **Legg til**.
    1. Velg en regnskapskoblingstype.
    1. I feltet **Gruppenummer** velger du riktig gruppe for regnskapskobling.

### <a name="assign-entities-of-the-fiscal-registration-process-to-pos-profiles"></a>Tilordne enheter av bilagsregistreringsprosessen til POS-profiler

Gjør følgende for å tilordne enheter av bilagsregistreringsprosessen til POS-profiler.

1. I Commerce-hovedkvarteret går du til siden **Funksjonalitetsprofiler for salgssted** (**Detaljhandel og handel \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonalitetsprofiler**). 
1. Tilordne bilagsregistreringsprosessen til en funksjonalitetsprofil for salgssted.
1. Velg **Rediger** og deretter i kategorien **Bilagsregistreringsprosess** i feltet **Prosessnummer** velger du en prosess.
1. Velg tekniske profiler for kobling med koblingsplasseringen **Kasse** i fanen **Regnskapstjenester**.
1. Gå til siden **Maskinvareprofil for salgssted** (**Detaljhandel og handel \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Maskinvareprofiler**).
1. Tilordne tekniske profiler for kobling til en maskinvareprofil. 
1. Velg **Rediger**, og legg deretter til en linje på fanen **Eksterne regnskapsenheter**. 
1. Velg en teknisk profil for kobling i feltet **Profilnummer**.
1. Velg tekniske profiler for kobling med koblingsplasseringen **Maskinvarestasjon** i fanen **Eksterne regnskapsenheter**.

> [!NOTE]
> Du kan legge til flere tekniske profiler i den samme maskinvareprofilen. En maskinvareprofil eller funksjonalitetsprofil for salgssted skal imidlertid bare ha ett skjæringspunkt med en gruppe for regnskapskobling.

Bilagsregistreringsflyten er definert av renskapsregistreringsprosessen og også av noen parametere for regnskapsintegreringskomponenter: CRT-utvidelsen for regnskapsdokumentleverandøren og Maskinvarestasjon-utvidelsen for regnskapskoblingen.

- Abonnementet for hendelser og transaksjoner til regnskapsregistrering er forhåndsdefinert i regnskapsdokumentleverandøren.
- Regnskapsdokumentleverandøren er også ansvarlig for å identifisere regnskapskoblingen som brukes til regnskapsregistrering. Den samsvarer med de funksjonelle profilene for kobling som er inkludert i gruppen for regnskapskobling som er angitt for gjeldende trinn i regnskapsregistreringsprosessen for teknisk profil for kobling som er tilordnet til maskinvareprofilen for maskinvarestasjonen som salgsstedet er koblet til.
- Regnskapsdokumentleverandøren bruker innstillingene for datatilordning fra regnskapsdokumentleverandørkonfigurasjonen for å transformere transaksjons-/hendelsesdata som for eksempel avgifter og betalinger når det genereres et regnskapsdokument.
- Når regnskapsdokumentleverandøren genererer et regnskapsdokument, kan regnskapskoblingen enten sende det til regnskapsenheten som den er, eller analysere det og gjøre det om til en sekvens med kommandoer for API-enheten, avhengig av hvordan kommunikasjonen håndteres.

### <a name="set-up-registers-with-fiscal-registration-restrictions"></a>Konfigurere kasser med begrensninger for regnskapsregistrering

Du kan velge kasser der regnskapsregistrering skal være forbudt, for eksempel når du bare trenger å tilby ikke-regnskapsoperasjoner, for eksempel søk i produktkatalog, kundeoppslag eller opprettelse av transaksjonsutkast på disse enhetene.

Følg denne fremgangsmåten for å konfigurere kasser med begrensninger for regnskapsregistrering.

1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Regnskapsregistreringsprosesser** i Commerce Headquarters.
1. Velg prosessen som kreves.
1. Velg fanen **Kasser på salgssted med begrensninger for regnskapsprosess**.
1. Legg til kasser med begrensninger for regnskapsprosess etter behov.

### <a name="validate-the-fiscal-registration-process"></a>Valider regnskapsregistreringsprosessen

Det anbefales at du validerer bilagsregistreringsprosessen i følgende tilfeller:

- Du har fullført alle innstillingene for en ny registreringsprosess. Disse innstillingene omfatter tilordning av registreringsprosesser til POS-funksjonalitetsprofiler og maskinvareprofiler.
- Du har foretatt endringer i en eksisterende bilagsregistreringsprosess, og disse endringene kan føre til at en annen regnskapskobling blir valgt ved kjøretid. (Du har for eksempel endret koblingsgruppen for et trinn i bilagsregistreringsprosessen, aktivert en koblingsfunksjonsprofil i en koblingsgruppe eller lagt til en ny koblingsfunksjonsprofil i en koblingsgruppe.)
- Du har foretatt endringer i tilordningen av tekniske profiler for kobling til maskinvareprofiler.

Følg denne fremgangsmåten for å validere bilagsregistreringsprosessen.

1. I Commerce-hovedkvarteret går du til siden **Bilagsregistreringsprosess** (**Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Bilagsregistreringsprosess**).
1. Velg **Valider** for å validere bilagsregistreringsprosessen.
1. På siden **Distribusjonsplan** kjører du **1070**- og **1090**-jobber for å overføre data til kanaldatabasen.

## <a name="set-up-fiscal-texts-for-discounts"></a>Konfigurere bilagstekster for rabatter

I noen tilfeller må en spesiell tekst skrives ut på en bilagskvittering hvis en rabatt brukes. Du kan konfigurere bilagstekster for rabatter på siden **Gruppe for regnskapskobling** (**Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Grupper for regnskapskobling**).

- For manuelle rabatter som brukes på salgsstedet, konfigurerer du en bilagstekst for informasjonskoden eller informasjonskodegruppen som er angitt som **Produktrabatt**-informasjonskoden i funksjonsprofilen for salgssted.

    1. På siden **Gruppe for regnskapskobling** velger du **Tekst for bilagskvittering**.
    1. I kategorien **Infokoder** velger du **Legg til** og velger en informasjonskode eller informasjonskodegruppe.
    1. I feltet **Informasjonskodenummer** velger du en verdi.
    1. I feltet **Underkodenummer** velger en verdi hvis det kreves en delkode for den valgte informasjonskoden.
    1. I feltet **Tekst for bilagskvittering** angir du en bilagstekst som skal skrives ut på en bilagskvittering.
    1. Sett alternativet **Skriv ut brukerinndata på bilagskvittering** til **Ja** for å overstyre teksten på en bilagskvittering med informasjon som brukeren angir manuelt på salgsstedet. Dette alternativet gjelder bare for informasjonskoder som har inndatatypen **Tekst**.

    > [!NOTE]
    > Du kan angi en bilagstekst for flere informasjonskoder for å støtte scenarioer der informasjonskodegrupper, koblede infokoder og utløste infokoder brukes. I disse scenarioene inneholder bilagskvitteringene bilagstekstene fra alle infokoder som er koblet til transaksjonslinjen der rabatten ble brukt.

- Du bør definere en regnskapstekst for rabatt-ID-en for kanalspesifikke rabatter.

    1. På siden **Gruppe for regnskapskobling** velger du **Tekst for bilagskvittering**.
    1. I kategorien **Rabatter** velger du **Legg til**, og deretter velger du rabatt-ID.
    1. I feltet **Tekst for bilagskvittering** angir du en bilagstekst som skal skrives ut på en bilagskvittering.

    > [!NOTE]
    > Hvis flere rabatter brukes på samme transaksjonslinje, vil bilagskvitteringen inneholde bilagstekster fra alle rabatter som er koblet til denne transaksjonslinjen.

## <a name="set-error-handling-settings"></a>Angi innstillinger for feilbehandling

Feilbehandlingsalternativene som er tilgjengelige i regnskapsintegrasjonen, defineres i bilagsregistreringsprosessen. Hvis du vil ha mer informasjon om feilbehandling i regnskapsintegreringen, kan du se [Feilbehandling](fiscal-integration-for-retail-channel.md#error-handling).

Følg denne fremgangsmåten for å angi innstillinger for feilhåndtering.

1. På siden **Bilagsregistreringsprosess** (**Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Bilagsregistreringsprosesser**) kan du angi følgende parametere for hvert trinn i bilagsregistreringsprosessen.

    - **Tillat overhopping** – Denne parameteren aktiverer **Hopp over**-alternativet i dialogboksen for feilbehandling.
    - **Tillat Merk som registrert** – Denne parameteren aktiverer **Merk som registrert**-alternativer i dialogboksen for feilbehandling.
    - **Tillat utsettelse** – Denne parameteren aktiverer **Utsett**-alternativet i dialogboksen for feilbehandling.
    - **Fortsett ved feil** – Hvis denne parameteren er aktivert, vil bilagsregistreringsprosessen fortsette på salgsstedskassen hvis bilagsregistrering av en transaksjon eller hendelsen mislykkes. Hvis ikke, for å kjøre bilagsregistrering av neste transaksjon eller hendelse, må operatøren prøve å kjøre den mislykkede bilagsregistreringen på nytt, hoppe over den eller merke transaksjonen eller hendelsen som registrert. Hvis du vil ha mer informasjon, se [Valgfri bilagsregistrering](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Hvis parameteren **Fortsett ved feil** er aktivert, deaktiveres parameteren **Tillat overhopping** og **Tillat Merk som registrert** automatisk.

1. Alternativene **Hopp over** og **Merk som registrert** i dialogboksen for feilbehandling krever at tillatelsen **Tillat å hoppe over registrering eller merke som registrert** er aktivert. Du kan aktivere denne tillatelsen ved å gå til siden **Tillatelsesgrupper** (**Detaljhandel og handel \> Ansatte \> Tillatelsesgrupper**), og angi alternativet **Tillat å hoppe over registrering eller merke som registrert** til **Ja**.
1. **Utsette**-alternativet i dialogboksen for feilbehandling krever at tillatelsen **Tillat utsettelse** er aktivert. Du kan aktivere tillatelsen ved å gå til siden **Tillatelsesgrupper** (**Detaljhandel og handel \> Ansatte \> Tillatelsesgrupper**), og angi alternativet **Tillat utsettelse** til **Ja**.
1. Alternativene **Hopp over**, **Merk som registrert** og **Utsett** lar operatorer angi tilleggsinformasjon når bilagsregistreringen mislykkes. Hvis du vil gjøre denne funksjonaliteten tilgjengelig, må du angi infokodene **Hopp over**, **Merk som registrert** og **Utsett** i en gruppe for regnskapskobling. Informasjonen som operatorene angir, lagres deretter som en infokodetransaksjon som er knyttet til regnskapstransaksjon. Hvis du vil ha mer informasjon om infokoder, kan du se [Informasjonskoder og informasjonskodegrupper](../info-codes-retail.md).

    > [!NOTE]
    > **Produkt**-utløserfunksjonen støttes ikke for informasjonskodene som brukes til **Hopp over** og **Merk som registrert** i grupper for regnskapskobling.

    - På siden **Gruppe for regnskapskobling** på fanen **Infokoder** velger du infokoder eller informasjonskodegrupper i feltene **Hopp over**, **Merk som registrert** og **Utsett**.

    > [!NOTE]
    > Ett regnskapsdokument og ett ikke-regnskapsdokument kan genereres på et hvilket som helst trinn i bilagsregistreringsprosessen. En finansdokumentleverandørutvidelse identifiserer hver type transaksjon eller hendelse som er relatert til regnskapsdokumenter eller ikke-regnskapsdokumenter. Feilhåndteringsfunksjonen gjelder bare for regnskapsdokumenter.
    >
    > - **Regnskapsdokument** – Et obligatorisk dokument som må registreres med suksess (for eksempel en bilagskvittering).
    > - **Ikke-regnskapsdokument** – Et ekstra dokument for transaksjonen eller hendelsen (for eksempel en gavekortseddel).

1. Hvis operatøren må være i stand til å fortsette å behandle den aktuelle operasjonen (for eksempel oppretting eller avslutning av en transaksjon) etter at en tilstandskontrollfeil oppstår, bør du aktivere tillatelsen **Tillat å hoppe over tilstandskontrollfeil** på siden **Tillatelsesgrupper** (**Retail og Commerce \> Ansatte \> Tillatelsesgrupper**). Hvis du vil ha mer informasjon om tilstandskontrollprosedyren, se [Tilstandskontroll for bilagsregistrering](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Konfigurere X-/Z-regnskapsrapporter fra salgsstedet

For å aktivere X-/Z-regnskapsrapporter fra salgsstedet bør du legge til nye knapper i et salgsstedsoppsett.

- På siden **Knappegrupper** følger du instruksjonene i [Legge til salgsstedsoperasjoner i salgsstedsoppsett ved hjelp av utforming for knappegruppe](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) for å installere utformingen og oppdatere et salgsstedsoppsett.

    1. Velg oppsettet som skal oppdateres. 
    1. Legg til en ny knapp, og angi **Skriv ut regnskapsår X**-knappeegenskapen.
    1. Legg til en ny knapp, og angi **Skriv ut regnskapsår Z**-knappeegenskapen.
    1. På siden **Distribusjonsplan** kjører du **1090**-jobben for å overføre endringer til kanaldatabasen.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Aktivere manuell kjøring av utsatt bilagsregistrering

For å aktivere manuell utføring av en utsatt bilagsregistrering bør du legge til en ny knapp i et POS-oppsett.

- På siden **Knappegrupper** følger du instruksjonene i [Legge til salgsstedsoperasjoner i salgsstedsoppsett ved hjelp av utforming for knappegruppe](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) for å installere utformingen og oppdatere et salgsstedsoppsett.

    1. Velg oppsettet som skal oppdateres.
    1. Legg til en ny knapp, og angi **Fullfør bilagsregistreringsprosess**-knappeegenskapen.
    1. På siden **Distribusjonsplan** kjører du **1090**-jobben for å overføre endringene dine til kanaldatabasen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

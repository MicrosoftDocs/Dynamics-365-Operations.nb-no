---
title: Oversikt over kundeaktiviteter
description: Dette emnet gir en oversikt over funksjonene for kundeaktiviteter som er tilgjengelige i butikkprogrammet.
author: bebeale
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom:
- "260624"
- intro-internal
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: 48e3b93b7e53a47673f824d35ac95b65d8566bce
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594809"
---
# <a name="clienteling-overview"></a>Oversikt over kundeaktiviteter

[!include [banner](includes/banner.md)]


Mange forhandlere, spesielt avanserte spesialleverandører, vil at deres salgsmedarbeidere skal skape langsiktige forhold med deres nøkkelkunder. Medarbeiderne forventes å vite hva disse kundenes liker og ikke liker, kjøpshistorikk, produktpreferanser og viktige datoer, for eksempel merkedager og fødselsdager. Medarbeidere trenger en plass der de kan hente denne informasjonen og finne den på en enkel måte når det er nødvendig. Hvis denne informasjonen er tilgjengelig i en enkelt visning, kan medarbeiderne enkelt målrette kunder som oppfyller bestemte kriterier. De kan for eksempel finne alle kunder som foretrekker å handle håndvesker, eller kunder som har en viktig hendelse som nærmer seg, for eksempel en fødselsdag eller jubileum.

## <a name="client-book"></a>Klientbok

I Microsoft Dynamics 365 Commerce kan forhandlere bruke klientbokfunksjonaliteten til å hjelpe butikkmedarbeidere med å skape langsiktige forbindelser med viktige kunder.

Klientboken inneholder kundekort som viser kontaktinformasjon for hver kunde, sammen med tre flere egenskaper som er definert av forhandleren og konfigurert i Hovedkontor. Forhandlere kan bestemme de tre viktigste tingene som salgsmedarbeidere bør vite om kunder. En smykkeforhandler kan for eksempel inkludere viktige datoer som jubileer eller fødselsdager, fordi disse datoene er anledninger da folk kjøper flere smykker. På samme måte kan en moteforhandler ta med kundens foretrukne handleinteresser og merker.

Klientboken lar også salgsmedarbeidere filtrere listen slik at den bare viser kunder som oppfyller bestemte kriterier. En ny skokolleksjon har for eksempel kommet i butikken, og en medarbeider vil informere kunder som ønsker å kjøpe sko. I dette tilfellet kan medarbeideren filtrere klientboken for å finne relevante kunder, og deretter foreta mer handling.

Hvis kunder ikke lenger anses som nøkkelkunder av en eller annen grunn, og bør derfor ikke være tett administrert, kan salgsmedarbeidere fjerne dem fra sin klientbok.

Noen forhandlere vil ikke administrere kunder på salgsmedarbeidernivå. De vil i stedet behandle en liste over nøkkelkunder på butikknivå. Disse detaljistene kan vise kunder fra butikklientbøker. Ved hjelp av dette alternativet kan forhandlere vise kundene fra klientbøkene for alle salgsmedarbeider med adressebok som samsvarer med adresseboken til den gjeldende butikken. Hvis en medarbeider arbeider i flere butikker for den juridiske enheten, viser klientboken kundene fra alle butikkene. Denne funksjonaliteten støtter flere funksjoner. Kunder kan for eksempel tilordnes på nytt fra en medarbeider til en annen medarbeider. Denne funksjonen er nyttig når medarbeidere overføres eller forlater firmaet.

Hver salgsmedarbeider kan ha én klientbok per juridisk enhet, og medarbeidere kan legge til én eller flere kunder i sin klientbok. I Commerce kan hver kunde for øyeblikket bare legges til i én klientbok. Microsoft planlegger imidlertid å legge til funksjonalitet som gjør at en enkelt kunde kan legges til flere klientbøker.

> [!NOTE]
> Til forskjell fra kundesøk filtrerer ikke klientboken kundeposter basert på butikkens adressebøker.

## <a name="activities-and-notes"></a>Aktiviteter og merknader

Ved hjelp av Internett-kanaler kan forhandlere lære om kundepreferanser uten å kreve at kundene eksplisitt oppgir denne informasjonen. Når kunder samhandler med salgsmedarbeidere i butikken, kan de eksplisitt dele informasjon om deres preferanser. Denne informasjonen kan dessverre gå tapt etter at salget er over. Hvis denne informasjonen er registrert, kan den imidlertid hjelpe forhandlere å forstå kundene bedre og dermed hjelpe dem med å gi bedre anbefalinger og en bedre generell handleopplevelse.

For å hente den kritiske informasjonen som kunder deler, kan salgsmedarbeidere ikke bare bruke klientbokattributtene, men også bruke funksjonaliteten aktiviteter og merknader. Forhandlere kan konfigurere aktivitetstypene, for eksempel informasjon om butikkbesøk, e-postadresse, telefonnummer og avtaler. Aktiviteter som medarbeidere oppretter, kan vises i et tids linjeformat på salgsstedet. De kan også vises i kategorien **Aktiviteter** på siden **Alle kunder \> Generelt** i Hovedkontor.

Salgsmedarbeidere kan du også bruke merknader til å registrere generell kundeinformasjon som det kan refereres til før alle typer samhandlinger. Disse merknadene lagres i Hovedkontor og kan vises i kundeprofilen eller på siden for kundedetaljer i telefonsenteret.

> [!NOTE]
> For øyeblikket kan alle notater og aktiviteter vises av alle salgsmedarbeidere som arbeider for den juridiske enheten, og som kan vise kundedetaljsider. Merknader og aktiviteter er ikke begrenset til medarbeideren som la til en kunde i klientboken.

## <a name="integration-with-dynamics-365-customer-insights"></a>Integrering med Dynamics 365 Customer Insights

Ved å bruke Dynamics 365 Customer Insights-programmet kan forhandlere samle data fra de ulike systemene som kundene bruker til å arbeide interaktivt med forhandlerens merke. De kan deretter bruke disse dataene til å generere en enkelt visning av kunden og ha avledet innsikt. Integrering av Customer Insights med Commerce lar forhandlerne velge ett eller flere mål som skal vises på kundekortet i klientboken. Forhandlere kan for eksempel bruke dataene i Customer Insights til å beregne "frafallssannsynlighet" for en kunde og definere "neste beste handling". Hvis disse verdiene er definert som mål, kan de vises på kundekortet, og de kan gi viktig informasjon til salgsmedarbeidere. Hvis du vil ha mer informasjon om Customer Insights, se dokumentasjonen for [Dynamics 365 Customer Insights](/dynamics365/ai/customer-insights/overview). Hvis du vil ha mer informasjon om mål, se [Mål](/dynamics365/ai/customer-insights/pm-measures).

## <a name="set-up-clienteling"></a>Definere kundeaktiviteter

Følg denne fremgangsmåten for å aktivere kundeaktiviteter-funksjonaliteten i miljøet.

1. I arbeidsområdet **funksjonsbehandling** filtrerer du funksjonene etter modulen **Detaljhandel og handel**.

    ![Kundeaktiviteter i listen over funksjoner i modulen Commerce.](./media/Enable_clienteling.png "Kundeaktiviteter i listen over funksjoner i modulen Detaljhandel og handel")

2. Aktiver **Kundeaktiviteter**-funksjonen ved å velge **Aktiver nå**.
3. På siden **Parametere for Commerce**, i kategorien **Nummerserie**, velger du raden **Klientbokidentifikator**. Deretter velger du en nummerserie i feltet **Nummerseriekode**. Systemet vil bruke denne nummerserien til å tilordne en ID til klientbøker.
4. Velg **Lagre**.
5. Opprett en ny attributtgruppe som inneholder attributtene du vil registrere for kunder som administreres i klientbøker. Du finner instruksjonene i [Attributter og attributtgrupper](./attribute-attributegroups-lifecycle.md).

    - Definer de nødvendige attributtene som **Kan justeres**. Salgsmedarbeidere kan deretter bruke disse attributtene til å filtrere sin klientbok.
    - Angi visningsrekkefølgen for disse attributtene. Denne visningsrekkefølgen bestemmer hvilke attributter som skal vises på kundekortet i klientboken. En visningsrekkefølge på 1 anses som høyere enn visningsrekkefølgen på 2. Derfor vises attributtet som har en visningsrekkefølge på 1, før attributtet som har en visningsrekkefølge på 2.

    > [!NOTE]
    > Du kan gjøre Customer Insights tilgjengelig fra samme side. En ID og hemmelighet for Azure-app må opprettes for godkjenningsformål. (Hvis du vil ha informasjon om kravene, se delen [Aktivere integrering av Customer Insights med Commerce](#turn-on-the-integration-of-customer-insights-with-commerce) senere i dette emnet.) Hvis Customer Insights er aktivert, og du velger ett eller flere mål som skal vises på kundekortet, vil disse målene vises først. Deretter vises attributtgrupper for klientbok, basert på visningsrekkefølgen. Hvis du for eksempel velger to mål fra Customer Insights, vil disse to målene og ett klientbokattributt vises på kundekortet. (Klientbokattributtet som vises, vil være attributtet som har høyest visningsrekkefølge.)

6. Velg attributtgruppen du nettopp opprettet, på siden **Parametere for Commerce** i kategorien **Kundeaktiviteter** i feltet **Attributtgruppe for klientbok**.

    ![Attributtgruppe for klientbok valgt.](./media/Client%20book%20attributes.png "Attributtgruppe for klientbok valgt")

7. Hvis du vil registrere aktiviteter som forekommer på salgsstedet, definerer du aktivitetstypene på **Aktivitetstyper**-siden (**Retail og Commerce \> Kunder \> Aktivitetstyper**).

    > [!NOTE]
    > Aktivitetstyper hentes av Commerce Scale Unit når den foretar et sanntidskall for første gang. Når aktivitetene hentes, hurtigbufres de i et par timer. Hvis du endrer aktivitetstypene, må du vente til hurtigbufferen ikke lenger er gyldig. Du kan også starte Commerce Scale Unit-tjenesten for ikke-produktive miljøer på nytt.

8. Legg til to knapper i det aktuelle oppsettet for salgssted-skjermen, slik at selgere kan vise sine egne klientbøker og butikkklientboken. (Butikkens klientbøker omfatter klienter fra alle klientbøker til alle medarbeidere som deler en adressebok med butikken.) De tilsvarende operasjonene kalles **Vis kunder i klientbok** og **Vis kunder fra butikkens klientbøker**. Det finnes tre tilleggsoperasjoner som er relatert til klientbøker. Disse operasjonene bestemmer hvilke medarbeidere som kan legge til, fjerne og tilordne kunder på nytt fra en klientbok. De heter **Legg til kunde i klientbok**, **Fjern kunder fra klientboken** og **Tilordne kunder på nytt til en klientliste**.
9. Kjør følgende jobber for distribusjonsplan: 1040, 1150, 1110 og 1090.

Etter at du har fullført denne fremgangsmåten, kan salgsmedarbeidere åpne siden kundedetaljer på salgsstedet, og legge kunder til i sin klientbok, vise og registrere aktiviteter og merknader for kunder, og målrette mot kunder ved hjelp av kunde- og klientbok-attributter til å filtrere klientboken. Illustrasjonen nedenfor viser et eksempel på en klientbok.

![Eksempel på en klientbok.](./media/client_book.png "Eksempel på en klientbok")

## <a name="turn-on-the-integration-of-customer-insights-with-commerce"></a>Slå på integrering av Customer Insights med Commerce

Hvis du vil slå på integreringen av Customer Insights med Commerce, må du kontrollere at du har en aktiv forekomst av Customer Insights i leieren der Commerce er klargjort. Du må også ha en Azure Active Directory (Azure AD)-brukerkonto som har et Azure-abonnement.

Gjør følgende for å konfigurere integrasjonen:

1. Registrer et nytt program i Azure Portal, og noter deg programnavnet, program-IDen og hemmeligheten. Denne informasjonen brukes til tjeneste-til-tjeneste-godkjenning mellom Commerce og Customer Insights. Registrer hemmeligheten på en sikker måte, fordi den må lagres i Key Vault. I eksemplet nedenfor bruker du CI_Access_name, CI_Access_AppID, CI_Access_Secret for henholdsvis programnavn, program-ID og hemmelighet. Du finner mer informasjon i [Hurtigstart: Registrere en app med Microsoft-identitetsplattformen](/azure/active-directory/develop/quickstart-register-app).

    > [!IMPORTANT]
    > Utfør tiltak slik at du husker å endre hemmeligheten før den utløper. Hvis ikke vil integreringen stoppes uventet.

2. Gå til Customer Insights-forekomsten, og søk etter navnet på programmet som ble opprettet ovenfor (i dette eksemplet "CI_Access_name").
3. Opprett et Azure Key Vault, og noter deg navnet og URL-adressen (i dette eksemplet "KeyVaultName", "KeyVaultURL"). Hvis du vil ha instruksjoner, kan du se [Hurtigstart: Angi og hente en hemmelighet fra Azure Key Vault ved hjelp Azure-portalen](/azure/key-vault/quick-create-portal).
4. Lagre navnet (i dette eksemplet "CI_Access_Secret") i Key Vault. Når denne hemmeligheten lagres i Key Vault, får den et navn. Merk deg det hemmelige navnet (i dette eksempelet SecretName).
5. For å få tilgang til hemmeligheten fra Azure Key Vault må du opprette et annet program med program-ID og hemmelighet (i dette eksemplet "KeyVault_Access_AppID" og "KeyVault_Access_Secret"). Registrer hemmeligheten på en trygg måte, fordi den blir ikke vist igjen.
6. Deretter må du gi programmet tillatelser for å få tilgang til Key Vault fra Commerce ved hjelp av APIer. Gå til programsiden i Azure Portal. Velg **API-tillatelser** under delen **Behandle**. Legg til tillatelser for å få tilgang **Azure key vault**. Velg **Tilgangspolicy** for denne tillatelsen. Velg malen som **Hemmelig administrasjon**, og velg alternativene **Hent**, **Liste**, **Dekrypter** og **Krypter**. 
5. Gå til **Systemadministrasjon \> Oppsett \> Key Vault-parametere** i Commerce Headquarters, og angi den nødvendige informasjonen for key vault. I feltet **Key Vault-klient** angir du deretter program-IDen du brukte i trinn 4, slik at Commerce kan få tilgang til hemmelighetene i nøkkelhvelvet.
6. Hvis du vil legge til programmet du opprettet i trinn 1, i listen over sikre programmer (noen ganger kalt en hviteliste), kan du gå til Customer Insights og velge **Visning**-tilgang til programmet. Hvis du vil ha instruksjoner, kan du se [Tillatelser](/dynamics365/ai/customer-insights/pm-permissions).
7. På siden **Systemadministrasjon > Oppsett > Key Vault-parametere** i Commerce HQ oppdateres feltene som beskrevet nedenfor: 

- **Key Vault-URL**: "KeyVaultURL" (fra trinn 3 ovenfor).
- **Key Vault-klient**: "KeyVault_Access_AppID" (fra trinn 5 ovenfor).
- **Hemmelig Key Vault-nøkkel** "KeyVault_Access_Secret" (fra trinn 5 ovenfor).
- I **Hemmeligheter**-delen:
    - **Navn:** Et hvilket som helst navn, for eksempel "CIHemmelighet".
    - **Beskrivelse**: En hvilken som helst verdi.
    - **Hemmelig**: **hvelv**:`//<Name of key vault>/<name of secret>>` I dette eksemplet vil det være `vault://KeyVaultName/SecretName`.

Når du har oppdatert feltene, velger du **Valider** for å sikre at Commerce-programmet får tilgang til hemmeligheten.

8. I Commerce, på siden **Commerce-parametere**, i kategorien **Kundeaktiviteter**, i hurtigkategorien **Dynamics 365 Customer Insights** angir du **Program-ID** til "CI_Access_AppID" (fra trinn 1 over). For **Hemmelig navn** velger du navnet på hemmeligheten som ble angitt i trinn 7 ovenfor ("CIHemmelighet"). Sett alternativet **Aktiver Customer Insights** til **Ja**. Hvis oppsettet av en eller annen grunn ikke er vellykket, vil du få en feilmelding, og dette alternativet vil bli satt til **Nei**. 

Du kan ha flere miljøer i Customer Insights, for eksempel test- og produksjonsmiljøer. I feltet **ID for miljøforekomst** angir du det aktuelle miljøet. I feltet **Alternativ kunde-ID** angir du egenskapen i Customer Insights som er tilordnet kundekontonummeret. (I Commerce er kundekontonummeret kunde-IDen.) De gjenværende tre egenskapene er målene som vil bli vist på kundekortet i klientboken. Du kan velge opptil tre mål som skal vises på kundekortet. Du trenger imidlertid ikke å velge noen mål. Som tidligere nevnt viser systemet disse verdiene først, og deretter viser det verdiene for klientbokattributtgruppen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
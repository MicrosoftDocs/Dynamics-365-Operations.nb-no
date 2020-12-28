---
title: Oversikt over kundeaktiviteter
description: Dette emnet gir en oversikt over funksjonene for kundeaktiviteter som er tilgjengelige i butikkprogrammet.
author: bebeale
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: d76668fa16a7634e7fbd953afaa6c89eed5457a2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414639"
---
# <a name="clienteling-overview"></a>Oversikt over kundeaktiviteter

[!include [banner](includes/banner.md)]


Mange forhandlere, spesielt avanserte spesialleverandører, vil at deres salgsmedarbeidere skal skape langsiktige forhold med deres nøkkelkunder. Medarbeiderne forventes å vite hva disse kundenes liker og ikke liker, kjøpshistorikk, produktpreferanser og viktige datoer, for eksempel merkedager og fødselsdager. Medarbeidere trenger en plass der de kan hente denne informasjonen og finne den på en enkel måte når det er nødvendig. Hvis denne informasjonen er tilgjengelig i en enkelt visning, kan medarbeiderne enkelt målrette kunder som oppfyller bestemte kriterier. De kan for eksempel finne alle kunder som foretrekker å handle håndvesker, eller kunder som har en viktig hendelse som nærmer seg, for eksempel en fødselsdag eller jubileum.

## <a name="client-book"></a>Klientbok

I Microsoft Dynamics 365 Commerce kan forhandlere bruke klientbokfunksjonaliteten til å hjelpe butikkmedarbeidere med å skape langsiktige forbindelser med viktige kunder.

Klientboken inneholder kundekort som viser kontaktinformasjon for hver kunde, sammen med tre ekstra egenskaper som er definert av forhandleren og konfigurert i Hovedkontor. Forhandlere kan bestemme de tre viktigste tingene som salgsmedarbeidere bør vite om kunder. En smykkeforhandler kan for eksempel inkludere viktige datoer som jubileer eller fødselsdager, fordi disse datoene er anledninger da folk kjøper flere smykker. På samme måte kan en moteforhandler ta med kundens foretrukne handleinteresser og merker.

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

Ved å bruke Dynamics 365 Customer Insights-programmet kan forhandlere samle data fra de ulike systemene som kundene bruker til å arbeide interaktivt med forhandlerens merke. De kan deretter bruke disse dataene til å generere en enkelt visning av kunden og ha avledet innsikt. Integrering av Customer Insights med Commerce lar forhandlerne velge ett eller flere mål som skal vises på kundekortet i klientboken. Forhandlere kan for eksempel bruke dataene i Customer Insights til å beregne "frafallssannsynlighet" for en kunde og definere "neste beste handling". Hvis disse verdiene er definert som mål, kan de vises på kundekortet, og de kan gi viktig informasjon til salgsmedarbeidere. Hvis du vil ha mer informasjon om Customer Insights, se dokumentasjonen for [Dynamics 365 Customer Insights](https://docs.microsoft.com/dynamics365/ai/customer-insights/overview). Hvis du vil ha mer informasjon om mål, se [Mål](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).

## <a name="set-up-clienteling"></a>Definere kundeaktiviteter

Følg denne fremgangsmåten for å aktivere kundeaktiviteter-funksjonaliteten i miljøet.

1. I arbeidsområdet **funksjonsbehandling** filtrerer du funksjonene etter modulen **Detaljhandel og handel**.

    ![Kundeaktiviteter i listen over funksjoner i modulen Commerce](./media/Enable_clienteling.png "Kundeaktiviteter i listen over funksjoner i modulen Detaljhandel og handel")

2. Aktiver **Kundeaktiviteter**-funksjonen ved å velge **Aktiver nå**.
3. På siden **Parametere for Commerce**, i kategorien **Nummerserie**, velger du raden **Klientbokidentifikator**. Deretter velger du en nummerserie i feltet **Nummerseriekode**. Systemet vil bruke denne nummerserien til å tilordne en ID til klientbøker.
4. Velg **Lagre**.
5. Opprett en ny attributtgruppe som inneholder attributtene du vil registrere for kunder som administreres i klientbøker. Du finner instruksjonene i [Attributter og attributtgrupper](https://docs.microsoft.com/dynamics365/retail/attribute-attributegroups-lifecycle).

    - Definer de nødvendige attributtene som **Kan justeres**. Salgsmedarbeidere kan deretter bruke disse attributtene til å filtrere sin klientbok.
    - Angi visningsrekkefølgen for disse attributtene. Denne visningsrekkefølgen bestemmer hvilke attributter som skal vises på kundekortet i klientboken. En visningsrekkefølge på 1 anses som høyere enn visningsrekkefølgen på 2. Derfor vises attributtet som har en visningsrekkefølge på 1, før attributtet som har en visningsrekkefølge på 2.

    > [!NOTE]
    > Du kan gjøre Customer Insights tilgjengelig fra samme side. En ID og hemmelighet for Azure-app må opprettes for godkjenningsformål. (Hvis du vil ha informasjon om kravene, se delen [Aktivere integrering av Customer Insights med Commerce](#turn-on-the-integration-of-customer-insights-with-commerce) senere i dette emnet.) Hvis Customer Insights er aktivert, og du velger ett eller flere mål som skal vises på kundekortet, vil disse målene vises først. Deretter vises attributtgrupper for klientbok, basert på visningsrekkefølgen. Hvis du for eksempel velger to mål fra Customer Insights, vil disse to målene og ett klientbokattributt vises på kundekortet. (Klientbokattributtet som vises, vil være attributtet som har høyest visningsrekkefølge.)

6. Velg attributtgruppen du nettopp opprettet, på siden **Parametere for Commerce** i kategorien **Kundeaktiviteter** i feltet **Attributtgruppe for klientbok**.

    ![Attributtgruppe for klientbok valgt](./media/Client%20book%20attributes.png "Attributtgruppe for klientbok valgt")

7. Hvis du vil registrere aktiviteter som forekommer på salgsstedet, definerer du aktivitetstypene på **Aktivitetstyper**-siden (**Retail og Commerce \> Kunder \> Aktivitetstyper**).

    > [!NOTE]
    > Aktivitetstyper hentes av Commerce Scale Unit når den foretar et sanntidskall for første gang. Når aktivitetene hentes, hurtigbufres de i et par timer. Hvis du endrer aktivitetstypene, må du vente til hurtigbufferen ikke lenger er gyldig. Du kan også starte Commerce Scale Unit-tjenesten for ikke-produktive miljøer på nytt.

8. Legg til to knapper i det aktuelle oppsettet for salgssted-skjermen, slik at selgere kan vise sine egne klientbøker og butikkklientboken. (Butikkens klientbøker omfatter klienter fra alle klientbøker til alle medarbeidere som deler en adressebok med butikken.) De tilsvarende operasjonene kalles **Vis kunder i klientbok** og **Vis kunder fra butikkens klientbøker**. Det finnes tre tilleggsoperasjoner som er relatert til klientbøker. Disse operasjonene bestemmer hvilke medarbeidere som kan legge til, fjerne og tilordne kunder på nytt fra en klientbok. De heter **Legg til kunde i klientbok**, **Fjern kunder fra klientboken** og **Tilordne kunder på nytt til en klientliste**.
9. Kjør følgende jobber for distribusjonsplan: 1040, 1150, 1110 og 1090.

Etter at du har fullført denne fremgangsmåten, kan salgsmedarbeidere åpne siden kundedetaljer på salgsstedet, og legge kunder til i sin klientbok, vise og registrere aktiviteter og merknader for kunder, og målrette mot kunder ved hjelp av kunde- og klientbok-attributter til å filtrere klientboken. Illustrasjonen nedenfor viser et eksempel på en klientbok.

![Eksempel på en klientbok](./media/client_book.png "Eksempel på en klientbok")

## <a name="turn-on-the-integration-of-customer-insights-with-commerce"></a>Slå på integrering av Customer Insights med Commerce

Hvis du vil slå på integreringen av Customer Insights med Commerce, må du kontrollere at du har en aktiv forekomst av Customer Insights i leieren der Commerce er klargjort. Du må også ha en Azure Active Directory (Azure AD)-brukerkonto som har et Azure-abonnement.

Gjør følgende for å konfigurere integrasjonen:

1. Registrer et program i Azure-portalen. Dette programmet vil bli brukt til godkjenning med Customer Insights. Du finner instruksjoner under [Hurtigstart: Registrer et program med Microsoft-identitetsplattformen](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).
2. Opprett en hemmelighet for programmet. Noter deg hemmeligheten, og oppbevar den på et trygt sted, fordi du vil trenge den senere. Velg også utløpsvarighet for hemmeligheten.

    > [!IMPORTANT]
    > Utfør tiltak slik at du husker å endre hemmeligheten før den utløper. Hvis ikke vil integreringen stoppes uventet.

3. Opprett et Azure Key Vault, og lagre programhemmeligheten. Hvis du vil ha instruksjoner, kan du se [Hurtigstart: Angi og hente en hemmelighet fra Azure Key Vault ved hjelp Azure-portalen](https://docs.microsoft.com/azure/key-vault/quick-create-portal).
4. Slå på tilgang til Azure Key Vault fra Commerce. Du må ha en program-ID og hemmelig for å kunne fullføre dette trinnet. Programmet kan være det samme programmet som du opprettet i trinn 1, eller det kan være et nytt program. (Med andre ord kan du bruke programmet du opprettet i trinn 1, for både Key Vault-tilgang og Customer Insights-tjenestetilgang, eller du kan opprette et unikt program for hver tilgangs type.) Hvis du vil ha instruksjoner, kan du se [Lagre tjenestelegitimasjoner i Azure Stack Key Vault](https://docs.microsoft.com/azure-stack/user/azure-stack-key-vault-store-credentials?view=azs-1908#create-a-service-principal).
5. Gå til **Systemadministrasjon \> Oppsett \> Key Vault-parametere** i Hovedkvarter, og angi den nødvendige informasjonen for nøkkelhvelvet. I feltet **Key Vault-klient** angir du deretter program-IDen du brukte i trinn 4, slik at Commerce kan få tilgang til hemmelighetene i nøkkelhvelvet.
6. Hvis du vil legge til programmet du opprettet i trinn 1, i listen over sikre programmer (noen ganger kalt en hviteliste), kan du gå til Customer Insights og gi **Visning**-tilgang til programmet. Hvis du vil ha instruksjoner, kan du se [Tillatelser](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-permissions).
7. Følg denne fremgangsmåten i Commerce på siden **Parametere for Commerce** i kategorien **Kundeaktiviteter** i **Dynamics 365 Customer Insights**-hurtigfanen:

    1. I feltet **Program-ID** angir du den program-IDen du brukte i trinn 1.
    2. I feltet **Hemmelig navn** angir du navnet på Key Vault-hemmeligheten som du opprettet i trinn 5.
    3. Sett alternativet **Aktiver Customer Insights** til **Ja**. Hvis oppsettet av en eller annen grunn ikke er vellykket, vil du få en feilmelding, og dette alternativet vil bli satt til **Nei**.
    4. Du kan ha flere miljøer i Customer Insights, for eksempel test- og produksjonsmiljøer. I feltet **ID for miljøforekomst** angir du det aktuelle miljøet.
    5. I feltet **Alternativ kunde-ID** angir du egenskapen i Customer Insights som er tilordnet kundekontonummeret. (I Commerce er kundens kontonummer kunde-IDen.)
    6. De gjenværende tre egenskapene er målene som vil vises på kundekortet i klientboken. Du kan velge opptil tre mål som skal vises på kundekortet. (Du trenger imidlertid ikke å velge noen mål.) Som nevnt tidligere, viser systemet disse verdiene først, og deretter vises verdiene for attributtgruppen for klientbok.

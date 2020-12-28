---
title: Oversikt over betalinger for omnikanal
description: Dette emnet gir en oversikt over omnikanalinnbetalinger i Dynamics 365 Commerce.
author: rubendel
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 8.1.3
ms.openlocfilehash: 80eaf36fb382e0ebe0a66383ea17ab76faa07dfa
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414765"
---
# <a name="omni-channel-payments-overview"></a>Oversikt over betalinger for omnikanal

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over omnikanalinnbetalinger i Dynamics 365 Commerce. Det inneholder en omfattende liste over støttede scenarioer, informasjon om funksjonalitet, oppsett og feilsøking, og beskrivelser av enkelte vanlige problemer.

## <a name="key-terms"></a>Viktige termer

| Semester | Beskrivelse |
|---|---|
| Token  | En streng med data som en betalingsprosessor gir som en referanse. Tokener kan representere betalingskortnumre, betalingsautoriseringer og tidligere betalingsregistreringer. Tokener er viktige, fordi de bidrar til å holde sensitive data utenfor salgsstedssystemet. De kalles noen ganger også for *referanser*. |
| Korttoken | Et token som en betalingsprosessor gir for lagring i POS-systemet. Et korttoken kan bare brukes av forretningsenheten som mottar det. Korttoken kalles noen ganger også for *kortreferanser*. |
| Token for autorisasjon | En unik ID som en betalingsprosess gir som en del av svaret den sender til et POS-system etter at POS-systemet har gjort en godkjenningsforespørsel. Et autorisasjonssymbol kan brukes senere hvis prosessoren kalles for å utføre handlinger som tilbakeføring eller annullering av autorisasjonen. Det brukes imidlertid oftes til å fange opp midler når en ordre er fullført eller en transaksjon er sluttført. Autorisasjonstoken kalles noen ganger også for *autorisasjonsreferanser*. |
| Registreringstoken | En referanse som en betalingsprosessor leverer til et POS-system når en betaling sluttføres eller registreres. Registreringssymbolet kan deretter brukes til å referere til betalingsregistreringen i etterfølgende operasjoner, for eksempel refunderingsforespørsler. | 
| Kort finnes ikke | En betegnelse som refererer til betalingstransaksjoner der et fysisk kort ikke blir presentert. Disse transaksjonene kan for eksempel forekomme i scenarier med e-handel eller telefonsenter. For disse transaksjonene angis den betalingsrelaterte informasjonen manuelt på et webområde for e-handel, i en telefonsenterflyt eller på salgsstedet eller betalingsterminalen. |
| Kort finnes | En betegnelse som refererer til betalingstransaksjoner der et fysisk kort presenteres og brukes på en betalingsterminal som er koblet til Microsoft Dynamics 365-salgsstedssystemet. |

## <a name="overview"></a>Oversikt

Vanligvis beskriver begrepet *omnikanalbetalinger* muligheten til å opprette en ordre i én kanal og fylle den ut i en annen kanal. Nøkkelen til omnikanalbetalingsstøtte er å bevare betalingsdetaljer sammen med resten av ordredetaljene, og deretter bruke betalingsdetaljene når ordren tilbakekalles eller behandles i en annen kanal. Et klassisk eksempel er scenarioet "Kjøp på nett, hent i butikk". I dette scenarioet legges betalingsdetaljene til når ordren opprettes på nettet. De kalles deretter tilbake på salgsstedet for å belaste kundens betalingskort på hentetidspunktet. 

Alle scenarioene som beskrives i dette emnet, kan implementeres ved hjelp av standard SDK for betalinger som leveres med Commerce. [Dynamics 365 Payment Connector for Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) gir en enkel implementering av alle scenarioer som er beskrevet her. 

### <a name="prerequisites"></a>Forutsetninger

Alle scenarioer som beskrives i dette emnet, krever en betalingskobling som støtter omnikanalbetalinger. Den medfølgende Adyen-tilkoblingen kan også brukes, fordi den støtter scenarioene som er tilgjengelige via betalings-SDK-en. Hvis du vil ha mer informasjon om hvordan du implementerer betalingskoblinger og Retail-SDK-en generelt, kan du gå til [Startside for detaljhandel for IT-teknikere og utviklere](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors).

#### <a name="supported-versions"></a>Støttede versjoner

Omnikanalbetalingsfunksjonene som beskrives i dette emnet, er utgitt som en del av Microsoft Dynamics 365 for Retail versjon 8.1.3. 

#### <a name="card-present-and-card-not-present-connectors"></a>"Kort finnes"- og "Kort finnes ikke"-koblinger

Betalings-SDK-en er avhengig av to sett med APIer (Application Programming Interface) for betalinger. Det første settet med APIer heter **iPaymentProcessor**. Den brukes til å implementere "kort finnes ikke"-betalingskoblinger som kan brukes i telefonsentre og med e-handelsplattformen til Microsoft Dynamics. Hvis du vil ha mer informasjon om **iPaymentProcessor**-grensesnittet, kan du se hvitboken [Implementere en betalingskobling og betalingsenhet](https://download.microsoft.com/download/e/2/7/e2735c65-1e66-4b8d-8a3c-e6ef3a319137/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device_update.pdf), som dekker betalinger. 

Det andre settet med APIer heter **iNamedRequestHandler**. Det støtter implementering av "kort finnes"-betalingsintegreringer som bruker en betalingsterminal. Hvis du vil ha mer informasjon om **iNamedRequestHandler**-grensesnittet, kan du se [Opprette en betalingsintegrering for en betalingsterminal](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension). 

### <a name="setup-and-configuration"></a>Oppsett og konfigurasjon

Følgende komponenter og oppsettrinn kreves:

- **eCommerce-integrering:** En integrering med Commerce er nødvendig for å støtte scenarier der en ordre kommer fra en nettbutikkfasade. Hvis du vil ha mer informasjon om Retail e-Commerce-SDK-en, kan du se [SDK for e-Commerce-plattformen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk). I et demonstrasjonsmiljø støtter referansebutikkfasaden omnikanalbetalingsscenarioer. 
- **Konfigurasjon av onlinebetalinger:** Oppsettet for Internett-kanalen må inkludere en betalingskobling som er oppdatert for å støtte omnikanalbetalinger. Alternativt kan en medfølgende betalingskobling brukes. Hvis du vil ha informasjon om hvordan du konfigurerer Adyen-betalingskoblingen for nettbutikker, se [Adyen-betalingskobling](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce). I tillegg til eCommerce-oppsettrinnene som beskrives i dette emnet, må parameteren **Tillat lagring av betalingsinformasjon i e-handel** settes til **sann** i innstillingene for Adyen-koblingen. 
- **Omnikanalbetalingskonfigurasjon:** I back office gå til **Retail og Commerce \> Hovedkvarteroppsett \> Parametere \> Delte handelsparametere**. I kategorien **Omnikanal-betalinger** setter du alternativet **Bruk betalinger for omnikanal** til **Ja**. I Commerce versjon 10.0.12 og senere er denne innstillingen i arbeidsområdet **Funksjonsbehandling**. Velg funksjonen **Omnikanal-betalinger**, og klikk på **Aktiver nå**. 
- **Betalingstjenester:** Telefonsenteret bruker standard betalingskobling på **Betalingstjenester**-siden for å behandle betalinger. Hvis du vil ha støtte for scenarioer som "Bestille på telefonsenter og hente i butikk", må denne standard betalingskoblingen være Adyen-betalingskoblingen eller en betalingskobling som oppfyller implementeringskravene for omnikanalbetalinger.
- **EFT-tjeneste:** Betalinger via en betalingsterminal må defineres i hurtigfanen **EFT-tjeneste** i maskinvareprofilen. Adyen-koblingen støtter standard omnikanalbetalingsscenarier. Andre betalingskoblinger som støtter **iNamedRequestHandler**-grensesnittet, kan også brukes hvis de støtter omnikanalbetalinger.
- **Betalingskoblingstilgjengelighet:** Når en ordre kalles tilbake, vil betalingsbeløplinjene som tilbakekalles sammen med ordren, inkludere navnet på betalingskoblingen som ble brukt til å opprette godkjenningene som er knyttet til ordren. Når ordren er oppfylt, prøver betalings-SDKen å bruke den samme koblingen som ble brukt til å opprette den opprinnelige autorisasjonen. Derfor må en betalingskobling som har samme forhandleregenskaper, være tilgjengelige for henting. 
- **Korttyper:** For at omnikanalscenarioer skal fungere skikkelig, må hver kanal ha samme oppsett for betalingsmiddeltyper som kan brukes for omnikanalen. Dette oppsettet omfatter betalingsmåte-IDer og korttype-IDer. Hvis for eksempel betalingsmiddeltypen **Kort** har IDen **2** i nettbutikkoppsettet, må den ha samme ID i oppsettet for detaljhandelsbutikken. Det samme kravet gjelder for korttype-IDer. Hvis kortnummer **12** er satt til **Visa** i nettbutikken, skal den samme IDen defineres for detaljhandelsbutikken. 
- Retail Modern POS for Windows eller Android med innebygd maskinvarestasjon -eller-
- Modern POS for iOS eller Cloud POS med tilkoblet, delt maskinvarestasjon. 

### <a name="basic-principle-supporting-omni-channel-payments"></a>Grunnleggende prinsipp som støtter omnikanalbetalinger

Betalingskoblinger og betalingsprosessorer bruker tokener, eller referanser, til å referere til samhandlinger som er knyttet til kortbetalinger. Når det for eksempel bes om en betalingsautorisering, gis det en referanse til denne autorisasjonen. Autorisasjonen kan derfor refereres til senere når det registreres midler på tidspunktet for oppfyllelse. Denne autorisasjonen er unik for forretningsenheten, betalingskontakten og prosessoren. 

Hvis en ordre som ble opprettet elektronisk, blir hentet i butikken, må de samme betalingsdetaljene for denne ordren kalles tilbake og brukes. Når de opprinnelige detaljene leveres som en del av forespørselen om å registrere en betaling mot den opprinnelige autorisasjonen, vil betalingsbehandleren kunne behandle forespørselen og registrere betalingen. 

Hvis det skal refereres til den elektroniske bestillingen på riktig måte, må også "kort finnes ikke"-betalingskontakten som støtter den samme prosessoren, være tilgjengelig. På denne måten kan POS-systemet ha én prosessor for "kort finnes" -betalinger, men den kan også ha tilgang til andre betalingskontakter, slik at de kan oppfylle ordrer som er opprettet i andre kanaler, ved å bruke ulike betalingsprosessorer. 

## <a name="supported-scenarios"></a>Scenarier som støttes

Følgende omnikanalbetalingsscenarioer støttes:

- Kjøpe på Internett og hente i butikk
- Bestille på telefonsenter og hente i butikk
- Kjøpe i butikk A og hente i butikk B
- Kjøpe i butikk A, sende til kunde

    > [!NOTE]
    > Betalinger som er gjort i telefonsenteret som er tilordnet "Normal"-betalingsfunksjonen, må merkes med **Forskuddbetaling** = **Ja** for å bli reflektert i beløpet som forfaller ved tilbakekalling av ordren på salgsstedet. Ikke-forskuddsbetalinger av typen Normal gjenkjennes ikke når ordren kalles på nytt i POS. 

Det er også støtte for variasjoner av disse scenariene. En elektronisk ordre kan for eksempel inneholde både linjer som skal sendes til kunden, og linjer som skal plukkes opp i en butikk. Alle ordreoppfyllingsalternativer støttes via omnikanalbetalinger. 

Følgende deler beskriver fremgangsmåten for hvert scenario og viser hvordan du kjører scenariet ved hjelp av demonstrasjonsdata. 

### <a name="buy-online-pick-up-in-store"></a>Kjøpe på Internett og hente i butikk

Før du starter må du kontrollere at følgende forutsetninger er oppfylt:

- Du har en referansebutikkfasade der Adyen-koblingen er konfigurert.
- Alternativet **Omnikanal-betalinger** på siden **Delte handelsparametere** er satt til **Sann**. I senere versjoner er denne innstillingen flyttet til arbeidsområdet **Funksjonsbehandling**, der du kan velge funksjonen **Omnikanal-betalinger** og klikke på **Aktiver nå**. 
- Adyen-betalingskoblingen er konfigurert for Houston-salgsstedskassene.
- Retail Modern POS for Windows eller Android med innebygd maskinvarestasjon -eller-
- Modern POS for iOS eller Cloud POS med tilkoblet, delt maskinvarestasjon. 

Følg disse trinnene for å kjøre scenarioet.

1. I referansebutikkfasaden oppretter du en ordre for plukking i butikk. Pass på at du velger **Houston**-butikken. 
2. Gå gjennom utsjekkingstrinnene, og betal ved hjelp av et testkredittkortnummer. Du kan finne testkredittkortnumre på siden for [Adyen-testkortnumre](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description).
3. I Commerce bruker du den satsvise jobben **Synkroniser ordrer** og **P-001**-distribusjonsplanen for å opprette ordrene i back office.
4. På velkomstsiden for salgsstedet velger du **Ordrer som skal plukkes**-operasjonen for å se ordrene som skal hentes i butikken. 
5. Velg én eller flere linjer fra ordren som ble opprettet i referansebutikkfasaden, og velg deretter **Plukk**.

    Ordren hentes fra back office. 

6. Når ordrelinjedetaljene hentes fra back office, og en kortbetaling som kan brukes for omnikanalen, oppdages, blir du informert om at en betalingsmåte er tilgjengelig.
7. Velg **Bruk tilgjengelige betalingsmåte** for å fullføre transaksjonen ved hjelp av kortopplysningene som ble angitt i referansebutikkfasaden.

    Ordrelinjene lastes på transaksjonssiden, og forfalt saldo er 0 (null). 

8. Velg kategorien **Betalinger** for å vise betalingsmiddellinjen som ble trukket fra nettordren. 
9. Velg en hvilken som helst betalingsmåte for å fullføre transaksjonen. 

### <a name="buy-in-call-center-pick-up-in-store"></a>Bestille på telefonsenter og hente i butikk

1. I Commerce, på siden **Kundeservice**, angir du **Karin Berg** i søkefeltet, og deretter velger **Søk**. 
3. Velg **Karin Berg** i søkeresultatene.
4. Etter Karin er lastet inn på **Kundeservice**-siden, velger **Ny salgsordre**.
5. Velg **Hode** på den nye salgsordresiden for å vise ordrehodet. 
6. På **Ordrehode**-siden setter du området til **Sentralt** og lageret til **Houston**.
7. I kategorien **Lever** setter du **Leveringsmiddel**-feltet til **60** for kundehenting.
8. Velg **Linjer**, og legg deretter til én eller flere linjer i ordren. 
9. Velg **Fullført** for å angi flyten for fullføring av ordren.
10. Rull ned til betalingsdelen, velg **Legg til**, og velg deretter en linje der betalingsmåtetypen er satt til **Kort**. 
11. Velg plusstegnet (**+**) for å legge til en kortbetaling. 
12. Angi detaljene for et testkredittkortnummer som du fant på siden for [Adyen-testkortnumre](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description), og velg deretter **OK**.

    > [!NOTE]
    > Hvis kortmerket for kortnummeret du har angitt, er forskjellig fra merket som ble valgt da betalingen ble initiert, vil betalingen fremdeles gå gjennom. Den posteres imidlertid til kontoene som er tilordnet til kortmerket du valgte i trinn 10.

12. Velg **OK** på nytt for å lukke dialogboksen **Ordrefullføringsbetalinger**.
13. Velg **Send** på siden **Salgsordresammendrag**.
14. På velkomstsiden for salgsstedet velger du **Ordrer som skal plukkes**-operasjonen for å se ordrene som skal hentes i butikken. 
15. Velg én eller flere linjer fra ordren som ble opprettet i referansebutikkfasaden, og velg deretter **Plukk**.

    Ordren hentes fra back office. 

16. Når ordrelinjedetaljene hentes fra back office, og en kortbetaling som kan brukes for omnikanalen, oppdages, blir du informert om at en betalingsmåte er tilgjengelig.
17. Velg **Bruk tilgjengelige betalingsmåte** for å fullføre transaksjonen ved hjelp av kortopplysningene som ble angitt i referansebutikkfasaden.

    Ordrelinjene lastes på transaksjonssiden, og forfalt saldo er 0 (null).

18. Velg kategorien **Betalinger** for å vise betalingsmiddellinjen som ble trukket fra nettordren. 
19. Velg en hvilken som helst betalingsmåte for å fullføre transaksjonen. 

### <a name="buy-in-store-a-pick-up-in-store-b"></a>Kjøpe i butikk A og hente i butikk B

1. Start salgsstedet for Houston-butikken.
2. På **Transaksjon**-siden legger du til Karin Berg i transaksjonen ved å bruke det numeriske tastaturet for å angi **2001**.
3. Legg til én eller flere linjer i transaksjonen.
4. Velg **Ordrer** for å se ordrealternativene.
5. Velg **Plukk alle**, og deretter, når du blir bedt om det, velger du **Kundeordre**.
6. I søkefeltet angir du **Seattle**, og deretter velger du **Seattle**-butikken for plukking. 
7. Velg **OK** for å godta gjeldende dato som hentedato.
9. Velg **Betal med kort** for å starte betalingen.
10. Tilby kortbetalingen for beløpet som forfaller for innbetalingen. 
11. Fullfør innbetalingen på betalingsterminalen. 
12. Når betalingen er utført, velger du alternativet for å bruke det samme kortet for oppfyllelsen, og vent til ordren er fullført. 
13. Start salgsstedet for Seattle-butikken.
14. På velkomstsiden for salgsstedet velger du **Ordrer som skal plukkes**-operasjonen for å se ordrene som skal hentes i butikken. 
15. Velg én eller flere linjer fra ordren som ble opprettet i referansebutikkfasaden, og velg deretter **Plukk**.

    Ordren hentes fra back office. 

16. Når ordrelinjedetaljene hentes fra back office, og en kortbetaling som kan brukes for omnikanalen, oppdages, blir du informert om at en betalingsmåte er tilgjengelig.
17. Velg **Bruk tilgjengelige betalingsmåte** for å fullføre transaksjonen ved hjelp av kortopplysningene som ble angitt i referansebutikkfasaden.

    Ordrelinjene lastes på transaksjonssiden, og forfalt saldo er 0 (null).

18. Velg kategorien **Betalinger** for å vise betalingsmiddellinjen som ble trukket fra nettordren. 
19. Velg en hvilken som helst betalingsmåte for å fullføre transaksjonen. 

### <a name="buy-in-store-a-ship-to-customer"></a>Kjøpe i butikk A, sende til kunde

1. Start salgsstedet for Houston-butikken.
2. På **Transaksjon**-siden legger du til Karin Berg i transaksjonen ved å bruke det numeriske tastaturet for å angi **2001**.
3. Legg til én eller flere linjer i transaksjonen.
4. Velg **Ordrer** for å se ordrealternativene.
5. Velg **Send alle**, og deretter, når du blir bedt om det, velger du **Kundeordre**.
6. På leveringsmåtesiden velger du **Standard over natten**, og deretter **OK** for å godta dagens dato som forsendelsesdato. 
7. Velg **OK** for å godta gjeldende dato som hentedato.
8. Velg **Betal med kort** for å starte betalingen.
9. Tilby kortbetalingen for beløpet som forfaller for innbetalingen. 
10. Fullfør innbetalingen på betalingsterminalen. 
11. Når betalingen er utført, velger du alternativet for å bruke det samme kortet for oppfyllelsen, og vent til ordren er fullført.

Når ordren plukkes, pakkes og faktureres i back office, vil betalingsdetaljene som gis på salgsstedet, bli brukt til å registrere midlene for varene som sendes til kunden. 

## <a name="scenario-details"></a>Scenariodetaljer

I tillegg til de grunnleggende scenariene som akkurat ble beskrevet, er det gjort flere forbedringer i betalings-SDKen for å støtte omnikanalbetalinger. 

### <a name="pos"></a>Salgssted

#### <a name="single-swipedip-for-customer-orders"></a>Enkelt sveip/innsetting for kundeordrer

Før omnikanalfunksjonen ble implementert, da kundeordrer som inkluderte innskudd, ble opprettet på salgsstedet, måtte kundene dra (eller sette inn) kortet to ganger: én gang for å betale og én gang for å tokenisere kortet for etterfølgende ordreoppfyllelse. Når funksjonen for omnikanaltokenisering er aktivert, må kundene bare dra kort kortet én gang for å både å utføre betalingen og autorisere beløpet som er skyldig for varer som skal oppfylles senere. På tidspunktet for oppfyllelse registreres de autoriserte midlene. Før funksjonen for omnikanaltokenisering ble implementert, ble bare et gjentakende korttoken opprettet for etterfølgende ordreoppfyllelse. Derfor ble ikke midlene for den ventende oppfyllelsen godkjent, og fordi disse midlene ikke ble holdt for det bestemte kjøpet, var det mindre sannsynlig at de ble registrert senere.

> [!NOTE]
> Enkelt sveip støttes ikke i Retail versjon 8.1.3. Kundeordrer i versjon 8.1.3 bruker samme flyt som ble brukt før funksjonen for omnikanaltokenisering ble implementert. 

### <a name="cards-that-cant-issue-recurring-card-tokens"></a>Kort som ikke kan utstede gjentakende korttokener

Enkelte kort kan ikke brukes til omnikanalbetalinger fordi de ikke støtter utstedelse av regelmessige korttokener. Når en ordre opprettes på salgsstedet, brukes den forrige korttokeniseringsflyten hvis innbetalingen betales ved hjelp av et kort som ikke støtter gjentakende korttokener. Derfor må en kunde som ønsker å oppgi en betaling som skal brukes til etterfølgende ordreoppfyllelse, presentere et ekstra kort. Hvis det andre kortet ikke støtter gjentakende korttokener, vil tokeniseringshandlingen bli avslått, og kassereren blir bedt om å be kunden oppgi et annet kort. 

### <a name="using-a-different-card"></a>Bruke et annet kort

En kunde som kommer til butikken for ordreplukking, har muligheten til å bruke et annet kort. Når kassereren mottar meldingen **Bruk tilgjengelig betalingsmåte** når ordren plukkes, kan han eller hun spørre om kunden ønsker å bruke det samme kortet. Hvis kunden har mistet kortet som ble brukt til å opprette ordren, og vil betale for ordren ved å bruke et annet kort, kan kassereren velge **Bruk en annen betalingsmåte**. Hvis kunden senere kommer tilbake for å hente flere varer for den samme ordren, og hvis den opprinnelige kortautorisasjonen fremdeles er gyldig, kan kassereren på nytt spørre om kunden ønsker å bruke dette kortet.

### <a name="invalid-authorizations"></a>Ugyldige godkjenninger

Hvis kortet som ble brukt til å opprette en ordre, ikke lenger er gyldig når produktene velges for plukking, vil betalingsregistreringsforespørselen mislykkes. Salgsstedbetalingskoblingen vil deretter prøve å opprette en ny autorisasjon og registrere ved hjelp av samme kortdetaljer. Hvis den nye godkjenningen eller registreringen mislykkes, vil kassereren bli informert om at betalingen ikke kan behandles. Kassereren må deretter få en ny betaling fra kunden. 

### <a name="multiple-available-payments"></a>Flere tilgjengelige betalinger

Når en ordre som har flere betalingsmidler og flere linjer, blir plukket, mottar kassereren meldingen **Bruk tilgjengelig betalingsmåte**. Hvis det finnes flere kort når kassereren velger **Bruk tilgjengelige betalingsmåte**, vil de eksisterende betalingsmiddellinjene registreres til saldoen er oppfylt for varene som blir plukket for øyeblikket. Kassereren har ikke mulighet til å velge kortet som skal brukes for varene som blir plukket. 

## <a name="related-topics"></a>Relaterte emner

- [Vanlige spørsmål om betalinger](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [Dynamics 365 Payment Connector for Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3)
- [Konfigurere BOPIS i et evalueringsmiljø for Dynamics 365 Commerce](https://docs.microsoft.com/dynamics365/commerce/cpe-bopis)


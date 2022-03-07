---
title: Produkt- og kundesøk på salgssted
description: Dette emnet gir en oversikt over forbedringer som har blitt gjort for produkt- og kundesøkfunksjonalitet i Dynamics 365 Commerce.
author: ShalabhjainMSFT
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 022dcaca9bb3c9e7e749ee143702325367e5149b
ms.sourcegitcommit: f8b597b09157d934b62bd5fb9a4d05b8f82b5a0e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/26/2021
ms.locfileid: "7700095"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Produkt- og kundesøk på salgssted

[!include [banner](includes/banner.md)]

Modern Point of Sale (MPOS) og Cloud Point of Sale (CPOS) gir søkefunksjonalitet som er enkel å bruke for produkter og kunder. Ettersom søkefeltet alltid er til stede på toppen av MPOS- og CPOS-vinduene, kan ansatte raskt søke etter produkter og kunder.

Ansatte kan søke etter produkter i sortimentene og katalogene som er knyttet til det gjeldende lageret. De kan også søke i sortimentene og katalogene som er knyttet til andre lager i firmaet. Derfor kan kasserere selge og returnere produkter utenfor butikkens sortiment. På samme måte kan ansatte søke etter kunder som er knyttet til nåværende butikk eller annen butikk i selskapet. I tillegg kan ansatte søke etter kunder som er tilknyttet et annet selskap i morselskapet.

## <a name="product-search"></a>Produktsøk

Som standard gjøres produktsøk i butikkens sortiment. Denne typen søk er også kjent som et *lokalt produktsøk*. Men ansatte kan enkelt bytte til hvilken som helst katalog som er knyttet til gjeldende butikk, eller de kan søke i en annen butikk. Denne typen søk er også kjent som et *eksternt produktsøk*. For å endre katalogen, velg **Kategorier**-knappen på venstre side av siden. Velg knappen **Endre katalog** i toppen av ruten som dukker opp, og velg deretter en av de tilgjengelige katalogene for å bla gjennom den. Systemet vil søke i den valgte katalogen for produkter.

På siden **Endre katalog** kan ansatte enkelt søke en hvilken som helst butikk, eller de kan søke etter produkter på tvers av alle butikker.

![Endre katalogen.](./media/Changecatalog.png "Endre katalogen")

Et lokalt produktsøk søker i følgende produktegenskaper:

- Produktnummer
- Produktnavn
- beskrivelse
- Dimensjoner
- Strekkode
- Søkenavn

### <a name="additional-local-product-search-capabilities-conventional-sql-full-text-search"></a>Flere funksjoner for lokalt produktsøk (vanlig SQL-fulltekstsøk) 

- For søk med flere søkeord kan forhandlere konfigurere om søkeresultatene skal inneholde resultater som samsvarer med et *hvilket som helst* søkeord, eller bare resultater som samsvarer med *alle* søkeordene. Innstillingen for denne funksjonaliteten er tilgjengelig i POS-funksjonalitetsprofilen, i en ny gruppe kalt **Produktsøk**. Standardinnstillingen er **Match et hvilket som helst søkeord**. Dette er også den anbefalte innstillingen. Når **Samsvar alle søkeord**-innstillingen brukes, returneres alle produkter som helt eller delvis samsvarer med ett eller flere søkeord. Disse resultatene sorteres automatisk i stigende rekkefølge for produkter som har de fleste nøkkelordtreffene (fullstendig eller delvis).

    Innstillingen **Match alle søkeord** gir bare produkter som matcher alle søkeordene (helt eller delvis). Denne innstillingen er nyttig når produktnavnene er lange, og ansatte vil bare se begrensede produkter i søkeresultatene. Denne typen søk har imidlertid to begrensninger:

    - Søket er gjort på individuelle produktegenskaper. For eksempel returneres kun produkter som har alle søkte søkeord i minst én produktegenskap.
    - Det søkes ikke i dimensjoner.
> [!NOTE]
> Følgende konfigurasjoner av **Samsvar alle søkeord**/**Match alle søkeord** i POS-funksjonalitetsprofiler gjelder bare for **lokale** produktsøk (vanlig SQL-fulltekstsøk). Denne konfigurasjonen har ingen innvirkning på den skydrevne søkefunksjonen. Den nye søkemotoren har sin egen avanserte algoritme som gir en relevans av søk etter produktsøkeresultater. 

- Forhandlere kan konfigurere produktsøk for å vise søkeforslag når brukere skriver inn produktnavn. En ny innstilling for denne funksjonaliteten er tilgjengelig i POS-funksjonalitetsprofilen, i en gruppe som heter **Produktsøk**. Innstillingen heter **Vis søkeforslag under skriving**. Denne funksjonaliteten kan hjelpe ansatte å raskt å finne produktet de søker etter, fordi de ikke trenger å skrive hele navnet manuelt.
- Produktsøkalgoritmen søker nå også etter de søkevilkårene i **Søkenavn**-egenskapen for produktet.

![Produktforslag.](./media/Productsuggestions.png "Produktforslag")

## <a name="customer-search"></a>Kundesøk

Kundesøk brukes til å finne kunder til ulike formål. For eksempel kan kasserere vise kundens ønskeliste eller kjøpshistorikk, eller knytte kunden til en transaksjon. Søkealgoritmen samsvarer søkeordene mot verdiene i følgende kundeegenskaper:

- Navn
- E-postadresse
- Telefonnummer
- Fordelskortnummer
- Adresse
- Kontonummer

Blant disse egenskapene gir navnet størst fleksibilitet når det gjelder søk med flere søkeord, fordi algoritmen returnerer alle kunder som oppfyller et hvilket som helst av søkeordene. Kundene som samsvarer med flest søkeord, vises øverst i resultatene. Denne virkemåten gjør det enklere for kasserere i situasjoner der de søker ved å skrive inn fullt navn, men der for- og etternavn ble ombyttet i den første dataregistreringen. Av hensyn til ytelsen beholder imidlertid alle de andre egenskapene rekkefølgen til søkeordene. Derfor returneres ingen resultater hvis rekkefølgen til søkeordene ikke samsvarer med rekkefølgen som dataene er lagret i.

Som standard gjøres et kundesøk på kundeadresseboken som er knyttet til butikken. Denne typen søk er kjent som et *lokalt kundesøk*. Men ansatte kan også søke etter kunder globalt. Med andre ord kan de søke på tvers av butikkene i selskapet og på tvers av alle andre juridiske enheter. Denne typen søk er også kjent som et *eksternt kundesøk*.

For å søke globalt, kan medarbeidere velge knappen **Filterresultater** nederst på siden, og deretter velge alternativet **Søk alle butikker** som vist i illustrasjonen som følger. I dette tilfellet returneres ikke bare kunder. Alle typer parter som er en del av en adressebok hos hovedkontoret, returneres også. Disse partene inkluderer arbeidstakere, leverandører, kontakter og konkurrenter.

> [!NOTE]
> Du må angi minst fire tegn for et eksternt kundesøk for å returnere resultater.

Kunde-ID-en vises ikke for kunder som ble spurt fra andre juridiske enheter, fordi det ikke er opprettet noen kunde-ID for disse partene i det nåværende selskapet. Men hvis en medarbeider åpner kundedetaljersiden, genererer systemet automatisk en kunde-ID for denne parten, og forbinder også butikkens kundeadressebøker med kunden. Derfor vil kunden være synlig i lokale butiksøk som gjøres senere.

![Globalt kundesøk.](./media/Globalcustomersearch.png "Globalt kundesøk")

### <a name="additional-local-customer-search-capabilities"></a>Flere funksjoner for lokalt kundesøk

Når brukeren søker etter et telefonnummer, ignorerer systemet spesialtegn (for eksempel mellomrom, bindestreker og parenteser) som kan ha blitt lagt til da kunden ble opprettet. Kasserere trenger derfor ikke tenke på telefonnummerformatet når de søker. For eksempel, hvis en kundes telefonnummer ble oppgitt som **123-456-7890**, kan en kasserere søke etter kunden ved å skrive **1234567890** eller ved å skrive inn de første tallene i telefonnummeret.

> [!NOTE]
> En kunde kan ha flere telefonnumre og flere e-postadresser. Algoritmen for kundesøk søker også gjennom disse sekundære e-postadressene og telefonnumrene, men siden med kundesøkresultatene viser bare primær e-postadresse og telefonnummer. Dette kan føre til litt forvirring når de returnerte kunderesultatene ikke viser e-postadressen eller telefonnummeret du har søkt etter. I en fremtidig utgivelse har vi tenkt å forbedre skjermen for kundesøkresultater for å vise denne informasjonen.

Det vanlige kundesøket kan være tidkrevende fordi det søker i flere felt. I stedet kan kasserere søke i en enkelt kundeegenskap, for eksempel navn, e-postadresse eller telefonnummer. Egenskapene som kundesøkealgoritmen bruker, kalles *kundesøkekriterier*. Systemadministratoren kan lett konfigurere ett eller flere kriterier som snarveier som vises i POS. Ettersom søket er begrenset til ett kriterium, vises bare de relevante søkeresultatene, og ytelsen er mye bedre ut enn ytelsen til et standard kundesøk. Illustrasjonen nedenfor viser kundesøksnarveiene i POS.

![Snarveier for kundesøk.](./media/SearchShortcutsPOS.png "Snarveier for kundesøk")

Når du skal angi søkekriterier som snarveier, må administratoren åpne **Handelsparametre**-siden i Commerce, og deretter i **POS-søkekriterier**-kategorien velge alle kriteriene som skal vises som snarveier.

![Konfigurere søkesnarveier.](./media/ConfigureShortcutsAX.png "Konfigurere søkesnarveier")

> [!NOTE]
> Hvis du legger til for mange snarveier, vil rullegardinmenyen i søkefeltet i POS bli uoversiktlig, og den ansattes søkeopplevelse kan bli påvirket. Vi anbefaler at du bare legger til så mange snarveier som du trenger.

**Visningsrekkefølge**-feltet fastsetter rekkefølgen som snarveier vises i, i POS. Kriteriene som vises, er standardegenskapene som kundesøkealgoritmen bruker for kundesøk. Partnere kan imidlertid legge til egendefinerte egenskaper som snarveier for søk. Hvis du vil legge til egendefinerte egenskaper som søkesnarveier, må systemadministratoren utvide den utvidbare opplistingen som brukes for kundesøkekriteriene og deretter merke partnerens egendefinerte egenskaper som snarveier. Partnere er ansvarlig for å skrive koden for å finne resultater når de egendefinerte snarveiene brukes for søk.

> [!NOTE]
> En egendefinert egenskap som legges til opplistingen, påvirker ikke standard kundesøkalgoritme. Med andre ord kundesøkalgoritmen søker ikke i den egendefinerte egenskapen. Brukere kan bare bruke en egendefinert egenskap for søk hvis den egendefinerte egenskapen legges til som snarvei, eller hvis standard søkealgoritme overstyres.

Forhandlere kan også sette standard kundesøkemodus i POS til **Søk i alle butikker**. Denne konfigurasjonen kan være nyttig i scenarier der kunder som ble opprettet utenfor Salgssted, umiddelbart må søkes etter (for eksempel til og med før datadistribusjonsjobben kjøres). Hvis du vil gjøre dette, må forhandleren aktivere alternativet **Standard kundesøkemodus** i POS-funksjonalitetsprofilen. Når alternativet er satt til **Ja**, vil hvert forsøk på kundesøk deretter foreta et sanntidskall til hovedkvarteret.

For å unngå uventede ytelsesproblemer er denne konfigurasjonen skjult bak et testversjoneringsflagg kalt **CUSTOMERSEARCH_ENABLE_DEFAULTSEARCH_FLIGHTING**. For å vise innstillingen **Standard kundesøkemodus** i brukergrensesnittet må forhandleren opprette en støtteforespørsel for dets testemiljø for brukeraksept (UAT) og produksjonsmiljø. Etter at forespørselen er mottatt, samarbeider teknikerteamet med forhandleren for å sikre at forhandleren foretar testing i ikke-produksjonsmiljøene for å vurdere ytelsen og implementere eventuelle optimaliseringer som trengs.

## <a name="cloud-powered-customer-search"></a>Skybasert kundesøk

Offentlig forhåndsvisning av funksjonen for kundesøk ved hjelp av tjenesten Azure Cognitive Search er frigitt som en del av Commerce 10.0.18-versjonen. I tillegg til ytelsesforbedringer drar også brukere av tjenesten nytte av omfattende justeringer og forbedrede relevansfunksjoner. Ytelsesforbedringene er spesielt innlysende når den globale søkefunksjonen (Søk i alle butikker) av POS-en brukes. Dette skyldes at søkeresultater hentes fra søkeindeksen for Azure i stedet for spørringer fra dataene i Commerce Headquarters. 

### <a name="enable-the-cloud-powered-search-feature"></a>Aktivere den skydrevne søkefunksjonen

> [!NOTE]
> Det kreves at både Commerce Headquarters og Commerce Scale Unit oppdateres til versjon 10.0.18. Det er ikke nødvendig å oppdatere POS-et.

Hvis du vil aktivere funksjonen for skybasert søk i Commerce Headquarters, gjør du følgende.

1. Gå til **Systemadministrasjon \> Arbeidsområder \> Funksjonsbehandling**.
1. Finn og velg funksjonen **(Forhåndsversjon) Skybasert kundesøk**, og deretter velger du **Aktiver nå**.
1. Gå til **Detaljhandel og handel > Hovedkvarteroppsett > Handelsplanlegger > Initialiser handelsplanlegger** og velg **OK** for å vise den nye jobben **1010_CustomerSearch** i skjemaet **Distribusjonsplan**.
1. Gå til **Detaljhandel og handel > IT for Detaljhandel og handel > Distribusjonsplan**.
1. Kjør jobben **1010_CustomerSearch**. Denne jobben publiserer datoen til søkeindeksen i Azure. Når publiseringen av indeksen er fullført, settes statusen for jobben til **Brukt**.
1. Etter at statusen for jobben **1010_CustomerSearch** er satt til **Brukt**, kjører du jobben **1110 – Global konfigurasjon** for å oppdatere POS-kanaler for den nylig aktiverte funksjonen i **Funksjonsstyring**.
1. Deretter kjører du jobben **1010_CustomerSearch** med regelmessige intervaller for å sende kundeoppdateringer til søkeindeksen.

> [!NOTE]
> Når det gjelder publisering av den innledende indeksen, kan det hende jobben **1010_CustomerSearch** tar noen timer å fullføre, ettersom den vil sende alle kundepostene til søkeindeksen for Azure. Etterfølgende oppdateringer tar et par minutter. Når den skydrevne søkefunksjonen er aktivert, men indekspubliseringen ennå ikke er fullført, vil kundesøket fra POS som standard bruke det eksisterende SQL-baserte søket. Dette sikrer at det ikke er noen avbrytelser i butikkoperasjonene.

### <a name="functional-differences-from-the-existing-search"></a>Funksjonelle forskjeller fra det eksisterende søket

Listen nedenfor viser hvordan funksjonaliteten for skybasert kundesøk er forskjellig fra den eksisterende søkefunksjonaliteten. 

- Kunder som opprettes og redigeres i Commerce Headquarters, sendes til søkeindeksen for Azure når jobben **1010_CustomerSearch** kjøres. Det tar minst 15 til 20 minutter å oppdatere indeksen. POS-brukere kan søke etter nye kunder (eller søke basert på oppdatert informasjon) omtrent 15 til 20 minutter etter at oppdateringene skjer i Commerce Headquarters. Hvis forretningsprosessen krever at kunder som opprettes i Commerce Headquarters, umiddelbart kan søke i POS, er dette kanskje ikke den riktige tjenesten for deg.
- Nye kunder som opprettes i POS, sendes til søkeindeksen for Azure fra Commerce Scale Unit, og kan umiddelbart søkes i alle butikker. Hvis funksjonen for oppretting av Async-kunde imidlertid er aktivert, vil ikke nye kundeposter bli publisert til søkeindeksen for Azure fra Commerce Scale Unit, og de vil ikke være søkbare fra POS før kundeinformasjonen er synkronisert med Commerce Headquarters og kunde-ID-er er generert for Async-kunder. Jobben **1010_CustomerSearch** vil da kunne sende Async-kundepostene til søkeindeksen for Azure. I gjennomsnitt går det ca. 30 minutter før du kan søke etter nyopprettede Async-kunder i POS. Dette estimatet forutsetter at jobbene **1010_CustomerSearch**, **P-job** og **Synkroniser kunder og forretningspartnere fra asynkron modus** blir planlangt til å kjøre hvert 15. minutt.
- Skydrevne søk søker også etter de sekundære e-postene og telefonnumrene til kundene, men kundenes søkeresultater vises i øyeblikket bare det primære telefonnummeret og den primære e-postadressen til kundene. Ved første blikk kan det bekrefte at det er returnert relevante søkeresultater, men hvis du kontrollerer den sekundære e-postmeldingen og telefonnummeret til en kunde i søkeresultater, kan du bekrefte om du har søkt etter nøkkelord som føres i en kundesvar. For å unngå slik forvirring har vi planer om å forbedre søkeresultatsiden for å gjøre det enkelt for brukerne å forstå hvorfor et søkeresultat ble returnert.
- Kravet om å søke med minst fire tegn i et globalt søk ("Søk i alle butikker") gjelder ikke for denne tjenesten.

> [!NOTE]
> Funksjoner for kundesøk ved hjelp av tjenesten Azure Cognitive Search, er tilgjengelig i begrensede områder for forhåndsvisning. Funksjonen for kundesøk er *ikke* tilgjengelig i følgende områder:
> - Brasil
> - India

[!INCLUDE[footer-include](../includes/footer-banner.md)]

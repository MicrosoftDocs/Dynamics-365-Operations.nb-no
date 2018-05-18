---
title: "Produktsøk og kundesøk i POS"
description: "Dette emnet gir en oversikt over forbedringer som har blitt gjort for produkt- og kundesøkfunksjonalitet i Microsoft Dynamics 365 for Retail."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b055ae09e87434f9e43c558e2a43d0467d70aaed
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="overview-of-product-and-customer-search-in-point-of-sale"></a>Oversikt over produkt- og kundesøk i Point of Sale

[!include [banner](includes/banner.md)]

Modern Point of Sale (MPOS) og Cloud Point of Sale (CPOS) gir søkefunksjonalitet som er enkel å bruke for produkter og kunder. Ettersom søkefeltet alltid er til stede på toppen av MPOS- og CPOS-vinduene, kan ansatte raskt søke etter produkter og kunder.

Ansatte kan søke etter produkter i sortimentene og katalogene som er knyttet til det gjeldende lageret. De kan også søke i sortimentene og katalogene som er knyttet til andre lager i firmaet. Derfor kan kasserere selge og returnere produkter utenfor butikkens sortiment. På samme måte kan ansatte søke etter kunder som er knyttet til nåværende butikk eller annen butikk i selskapet. I tillegg kan ansatte søke etter kunder som er tilknyttet et annet selskap i morselskapet.

## <a name="product-search"></a>Produktsøk

Som standard gjøres produktsøk i butikkens sortiment. Denne typen søk er også kjent som et *lokalt produktsøk*. Men ansatte kan enkelt bytte til hvilken som helst katalog som er knyttet til gjeldende butikk, eller de kan søke i en annen butikk. Denne typen søk er også kjent som et *eksternt produktsøk*. For å endre katalogen, velg **Kategorier**-knappen på venstre side av siden. Velg knappen **Endre katalog** i toppen av ruten som dukker opp, og velg deretter en av de tilgjengelige katalogene for å bla gjennom den. Systemet vil søke i den valgte katalogen for produkter.

På siden **Endre katalog** kan ansatte enkelt søke en hvilken som helst butikk, eller de kan søke etter produkter på tvers av alle butikker.

![Endring av katalogen](./media/Changecatalog.png "Endring av katalogen")
 
Et lokalt produktsøk søker i følgende produktegenskaper:

- Produktnummer
- Produktnavn
- beskrivelse
- Dimensjoner
- Strekkode
- Søkenavn

### <a name="enhancements-to-local-product-searches"></a>Forbedringer til lokalt produktsøk

Opplevelsen for lokale produktsøk er nå mer brukervennlig. Følgende forbedringer er gjort:

- Rullegardinmenyer for produkt og kunde er lagt til i søkefeltet, slik at ansatte kan velge enten **Produkt** eller **Kunde** før de gjør søket. Som standard er **Produkt** valgt, som vist i følgende illustrasjon.
- For søk med flere søkeord kan forhandlere konfigurere om søkeresultatene skal inneholde resultater som samsvarer med et *hvilket som helst* søkeord, eller bare resultater som samsvarer med *alle* søkeordene. Denne innstillingen er tilgjengelig i POS-funksjonalitetsprofilen, i en ny gruppe som heter **Produktsøk**. Standardinnstillingen er **Match et hvilket som helst søkeord**. Dette er også den anbefalte innstillingen. Når **Samsvar alle søkeord**-innstillingen brukes, returneres alle produkter som helt eller delvis samsvarer med ett eller flere søkeord. Disse resultatene sorteres automatisk i stigende rekkefølge for produkter som har de fleste nøkkelordtreffene (fullstendig eller delvis).

    Innstillingen **Match alle søkeord** gir bare produkter som matcher alle søkeordene (helt eller delvis). Denne innstillingen er nyttig når produktnavnene er lange, og ansatte vil bare se begrensede produkter i søkeresultatene. Denne typen søk har imidlertid to begrensninger:

    - Søket er gjort på individuelle produktegenskaper. For eksempel returneres kun produkter som har alle søkte søkeord i minst én produktegenskap.
    - Det søkes ikke i dimensjoner.

- Forhandlere kan nå konfigurere produktsøk for å vise søkeforslag når brukere skriver inn produktnavn. En ny innstilling for denne funksjonaliteten er tilgjengelig i POS-funksjonalitetsprofilen, i en gruppe som heter **Produktsøk**. Innstillingen heter **Vis søkeforslag under skriving**. Denne funksjonaliteten kan hjelpe ansatte å raskt å finne produktet de søker etter, fordi de ikke trenger å skrive hele navnet manuelt.
- Produktsøkalgoritmen søker nå også etter de søkevilkårene i **Søkenavn**-egenskapen for produktet.

![Produktforslag](./media/Productsuggestions.png "Produktforslag")

## <a name="customer-search"></a>Kundesøk

Kundesøk brukes til å finne kunder til ulike formål. For eksempel kan kasserere vise kundens ønskeliste eller kjøpshistorikk, eller knytte kunden til en transaksjon. Ved søk med flere søkeord returnerer kundesøkalgoritmen alle kunder som samsvarer med noen av de søkte søkeordene. Kunder som samsvarer med de fleste søkeord vises imidlertid øverst i resultatene. Denne oppførselen er sammenlignbar med måten andre søkemotorer viser resultater på. De viser først resultatene som samsvarer med de mest søkte vilkårene, og viser deretter resultatene som delvis samsvarer med søkeordene. Denne oppførselen hjelper kasserere i situasjoner der de bruker flere søkeord for søket, men et av søkeordene har stavefeil.

Som standard gjøres et kundesøk på kundeadresseboken som er knyttet til butikken. Denne typen søk er kjent som et *lokalt kundesøk*. Men ansatte kan også søke etter kunder globalt. Med andre ord kan de søke på tvers av butikkene i selskapet og på tvers av alle andre juridiske enheter. Denne typen søk er også kjent som et *eksternt kundesøk*.

For å søke globalt, kan medarbeidere velge knappen **Filterresultater** nederst på siden, og deretter velge alternativet **Søk alle butikker** som vist i illustrasjonen som følger. I dette tilfellet returneres ikke bare kunder. Alle typer parter som er en del av en adressebok hos hovedkontoret, returneres også. Disse partene inkluderer arbeidstakere, leverandører, kontakter og konkurrenter.

> [!NOTE]
> Du må angi minst fire tegn for et eksternt kundesøk for å returnere resultater.

I et eksternt kundesøk vises ikke kunde-ID for kunder fra de andre juridiske enhetene, fordi det ikke er opprettet noen kunde-ID for disse partene i det nåværende selskapet. Men hvis en medarbeider åpner kundedetaljersiden, genererer systemet automatisk en kunde-ID for denne parten, og forbinder også butikkens kundeadressebøker med kunden. Derfor vil kunden være synlig i lokale butiksøk som gjøres senere.

![Globalt kundesøk](./media/Globalcustomersearch.png "Globalt kundesøk")

### <a name="enhancements-to-local-customer-search"></a>Forbedringer for lokalt kundesøk

Søk som er basert på telefonnummeret, er forenklet. Disse søkene ignorerer nå spesialtegn, for eksempel mellomrom, bindestreker og parenteser, som kan ha blitt lagt til da kunden ble opprettet. Kasserere trenger derfor ikke tenke på telefonnummerformatet når de søker. De kan også søke etter kunder ved å skrive inn et delvis telefonnummer. Hvis et telefonnummer inneholder spesialtegn, kan det også bli funnet ved å søke etter numrene som vises etter spesialtegnene. For eksempel, hvis en kundes telefonnummer ble oppgitt som **123-456-7890,** kan en kasserere søke etter kunden ved å skrive **123**, **456**, **7890** eller **1234567890**, eller ved å skrive inn de første tallene i telefonnummeret.

Det vanlige kundesøket kan være tidkrevende fordi det søker i flere felt. I stedet kan kasserere nå søke i en enkelt egendefinert egenskap, for eksempel navn, e-postadresse eller telefonnummer. Egenskapene som kundesøkealgoritmen bruker, kalles *kundesøkekriterier*. Systemadministratoren kan lett konfigurere ett eller flere kriterier som snarveier som vises i POS. Ettersom søket er begrenset til ett kriterium, vises bare de relevante søkeresultatene, og ytelsen er mye bedre ut enn ytelsen til et standard kundesøk. Illustrasjonen nedenfor viser kundesøksnarveiene i POS.

![Kundesøksnarveier](./media/SearchShortcutsPOS.png "Kundesøksnarveier")

Når du skal angi søkekriterier som snarveier, må administratoren åpne **Detaljhandelsparametre**-siden i Microsoft Dynamics 365 for Finance and Operations, og deretter i **POS-søkekriterier**-kategorien velge alle kriteriene som skal vises som snarveier.

![Konfigurere snarveier for søk](./media/ConfigureShortcutsAX.png "Konfigurere snarveier for søk")

> [!NOTE]
> Hvis du legger til for mange snarveier, vil rullegardinmenyen i søkefeltet i POS bli uoversiktlig, og den ansattes søkeopplevelse kan bli påvirket. Vi anbefaler at du bare legger til så mange snarveier som du trenger.

**Visningsrekkefølge**-feltet fastsetter rekkefølgen som snarveier vises i, i POS. Kriteriene som vises, er standardegenskapene som kundesøkealgoritmen bruker for kundesøk. Partnere kan imidlertid legge til egendefinerte egenskaper som snarveier for søk. Hvis du vil legge til egendefinerte egenskaper som søkesnarveier, må systemadministratoren utvide den utvidbare opplistingen som brukes for kundesøkekriteriene og deretter merke partnerens egendefinerte egenskaper som snarveier. Partnere er ansvarlig for å skrive koden for å finne resultater når de egendefinerte snarveiene brukes for søk.

> [!NOTE]
> En egendefinert egenskap som legges til opplistingen, påvirker ikke standard kundesøkalgoritme. Med andre ord kundesøkalgoritmen søker ikke i den egendefinerte egenskapen. Brukere kan bare bruke en egendefinert egenskap for søk hvis den egendefinerte egenskapen legges til som snarvei, eller hvis standard søkealgoritme overstyres.


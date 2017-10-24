---
title: "Produktsøk og kundesøk i POS"
description: "Dette emnet gir en oversikt over forbedringer som har blitt gjort for produkt- og kundesøkfunksjonalitet i Dynamics 365 for Retail."
author: shalabhjain
manager: AnnBe
ms.date: 08/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 66859535ee118ffc04a847dfe6e8e0bae1cd9d6c
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="overview-of-product-and-customer-search-in-point-of-sale"></a>Oversikt over produkt- og kundesøk i Point of Sale

Modern Point of Sale (MPOS) og Cloud Point of Sale (CPOS) gir søkefunksjonalitet som er enkel å bruke, og som gjør at ansatte raskt kan søke etter produkter og kunder. Søkefeltet er alltid til stede på toppen av MPOS og CPOS, slik at ansatte raskt kan finne produkter og kunder.

Ansatte kan søke etter produkter i utvalgene og katalogene som er knyttet til gjeldende butikk, og i utvalgene og katalogene som er knyttet til enhver annen butikk i selskapet. Derfor kan kasserere selge og returnere produkter utenfor butikkens sortiment. På samme måte kan ansatte søke etter kunder som er knyttet til nåværende butikk eller annen butikk i selskapet. I tillegg kan ansatte søke etter kunder som er tilknyttet et annet selskap i morselskapet.

## <a name="product-search"></a>Produktsøk 

Som standard gjøres et produktsøk i butikkens sortiment. Denne typen søk er også kjent som et *lokalt produktsøk*. Men ansatte kan enkelt bytte til hvilken som helst katalog som er knyttet til gjeldende butikk, eller de kan søke i en annen butikk. Denne typen søk er også kjent som et *eksternt produktsøk*. For å endre katalogen, velg **Kategorier**-knappen på venstre side av siden. Velg knappen **Endre katalog** i toppen av ruten som dukker opp, og velg deretter en av de tilgjengelige katalogene for å bla gjennom den. Systemet vil søke i den valgte katalogen for produkter.

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

Opplevelsen for lokale produktsøk har blitt gjort mer brukervennlig. Følgende forbedringer er gjort:

- Rullegardinmenyer for produkt og kunde er lagt til i søkefeltet, slik at ansatte kan velge enten **Produkt** eller **Kunde** før de gjør søket. Som standard er **Produkt** valgt, som vist i følgende illustrasjon.
- For søk med flere søkeord kan forhandlere konfigurere om søkeresultatene skal inneholde resultater som samsvarer med et hvilket som helst søkeord, eller bare resultater som samsvarer med alle søkeordene. Denne innstillingen er tilgjengelig i POS-funksjonalitetsprofilen, under en ny gruppe som heter **Produktsøk**. Standardinnstillingen er **Match et hvilket som helst søkeord**. Dette er også den anbefalte innstillingen. Når **Match et hvilket som helst søkeord** er satt vil alle produkter som helt eller delvis samsvarer med ett eller flere søkeord returneres som resultater, og resultatene sorteres automatisk i stigende rekkefølge av produkter som har de fleste søkeordmatch (helt eller delvis).

    Innstillingen **Match alle søkeord** gir bare produkter som matcher alle søkeordene (helt eller delvis). Denne innstillingen er nyttig når produktnavnene er lange, og ansatte vil bare se begrensede produkter i søkeresultatene. Denne typen søk har imidlertid to begrensninger:

    - Søket er gjort på individuelle produktegenskaper. For eksempel returneres kun produkter som har alle søkte søkeord i minst én produktegenskap.
    - Det søkes ikke i dimensjoner.

- Forhandlere kan nå konfigurere produktsøk for å vise søkeforslag når brukere skriver inn produktnavn. En ny innstlling for denne funksjonaliteten er tilgjengelig i POS-funksjonalitetsprofilen, under en gruppe som heter **Produktsøk**. Innstillingen heter **Vis søkeforslag under skriving**. Denne funksjonaliteten kan hjelpe ansatte å raskt å finne produktet de søker etter, fordi de ikke trenger å skrive hele navnet manuelt.
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

### <a name="enhancements-to-local-customer-searches"></a>Forbedringer for lokalt produktsøk

Lokale kundesøk hjelper ansatte å raskt finne kunder ved telefonnummer. Ansatte trenger ikke skrive noen spesialtegn som er lagt til kundens telefonnummer, for eksempel mellomrom, bindestreker eller parentes. Selv om kasserere kan lagre telefonnumre i et hvilket som helst format (for eksempel kan de inneholde parentes, bindestreker, symboler osv.), kan de søke etter kunder ved å skrive et delvis telefonnummer. Hvis en kassereren inkluderte spesialtegn når han eller hun skrev inn et telefonnummer, kan andre kasserere finne kunden ved å skrive inn tallene som vises etter spesialtegnene. For eksempel, hvis en kundes telefonnummer ble oppgitt som **123-456-7890,** kan en kasserere søke etter kunden ved å skrive **123**, **456**, **7890** eller **1234567890**, eller ved å delvis skrive inn de første tallene i telefonnummeret.


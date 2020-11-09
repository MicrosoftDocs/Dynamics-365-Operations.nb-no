---
title: Skrive ut og kansellere bølgeetiketter
description: Dette emnet beskriver hvordan du annullerer og skriver ut eksisterende bølgeetiketter på nytt.
author: GarmMSFT
manager: PJacobse
ms.date: 07/09/2020
ms.topic: reprint-and-void-wave-labels
ms.service: dynamics-ax-applications
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSWaveTableListPage, WHSWorkException, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelLayout, WHSWaveLabelType, WHSWaveLabelTemplateGroup
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: af92334af28824b3fcebde5f046bd7c6da459885
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016660"
---
# <a name="reprint-and-void-wave-labels"></a>Skrive ut og kansellere bølgeetiketter

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du behandler etiketter som genereres av bølgebehandling. (Hvis du vil ha en detaljert beskrivelse og og konfigurasjonsinstruksjoner, kan du se [Konfigurere bølgeetikettutskrift](../warehousing/configure-wave-label-printing.md).)

Du kan når som helst skrive ut bølgeetiketter på nytt. Det kan for eksempel hende at du må skrive ut en enkelt etikett hvis en eksisterende etikett gikk tapt eller ble skadet. Alternativt kan en lagerarbeider eller leder skrive ut en hel rull med etikett på nytt hvis tallet og/eller sammensetningen av en hel serie med bølgeetiketter har blitt endret (for eksempel på grunn av lagermangel eller andre årsaker). Selv om bare antallet kartonger er endret, må hele rullen ofte skrives ut på nytt for å holde det totale antallet nøyaktig i delen om "Kartong X av Y" i hver etikett.

Funksjonen for ny utskrift av bølgeetiketter støtter følgende funksjonalitet:

- Skriv ut etiketter på nytt både fra lagerappen og den rike klienten.
- Kanseller etiketter og skrive dem ut på nytt samtidig. (Muligheten til å annullere etiketter er eksempelvis innebygget i scenarioer med plukk med mangler.)
- Rydde opp i bølgeetikettloggen.

Dette emnet viser en samling scenarier som viser, gjennom eksempler, hvordan du arbeider med funksjonen for å skrive ut bølgeetiketter på nytt.

> [!IMPORTANT]
> Hvis du vil arbeide gjennom scenariene som presenteres i dette emnet, må du først aktivere og konfigurere de aktuelle funksjonene for bølgeutskriftsfunksjoner, som beskrevet i [Konfigurere bølgeetikettutskrift](../warehousing/configure-wave-label-printing.md). Flere av scenariene i dette emnet krever også at du først arbeider gjennom scenariene i dette emnet for å generere nødvendige eksempeldata.

## <a name="scenario-1-reprint-labels-from-the-web-client"></a>Scenario 1: Skrive ut etiketter på nytt fra webklienten

Du kan vise og skrive ut bølgeetiketter på nytt fra følgende sider. På handlingsruten for hver side, i kategorien **Forsendelser** i gruppen **Beslektet informasjon** , velger du **Bølgeetiketter**.

- Alle forsendelser \> Forsendelsesdetaljer
- Alle laster \> Lastdetaljer
- Alle bølger
- Bølgeetiketter
- Historikk for bølgeetikett

Følg denne fremgangsmåten for å skrive ut en bølgeetikett på nytt fra webklienten.

1. Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Velg bølgen det skal skrives ut etiketter på nytt fra.
1. I handlingsruten, i kategorien **Bølge** i **Skriv ut** -gruppen, velger du **Bølgeetiketter**.
1. Følg én av eller begge av disse trinnene:

    - For å skrive ut etiketten velger du en skriver i feltet **Skrivernavn**. (La dette feltet stå tomt hvis du bare vil oppdatere bølgeetikettdetaljene uten å skrive ut etiketten på nytt.)
    - Hvis du vil oppdatere etiketten, merker du av for **Oppdater bølgeetikettdetaljer**. (La avmerkingsboksen være tom hvis du bare vil skrive ut den forrige etiketten på nytt.)

    > [!NOTE]
    > Hver gang en bølgeetikett skrives ut eller skrives ut på nytt, konverteres dataene ved hjelp av det aktuelle oppsettet for bølgeetiketter, og alle plassholdere erstattes med faktiske verdier. Den resulterende strengen lagres som en post i bølgeetikettloggen. Hvis merket er fjernet for **Oppdater bølgeetikettdetaljer** , brukes de lagrede ZPL- dataene (Zebra Programming Language) når en etikett skrives ut på nytt. Hvis det er merket av for **Oppdater bølgeetikettdetaljer** genereres en ny streng. De eksisterende bølgeetikettene omberegnes også, og eventuelle ekstra etiketter (for eksempel hvis de tilknyttede arbeidslinjene er annullert eller endret) er merket som **Annullert** og skrives ikke ut på nytt.

1. Velg **OK** for å bekrefte valget.

## <a name="scenario-2-reprint-labels-from-the-warehousing-app"></a>Scenario 2: Skrive ut etiketter på nytt fra lagerappen

Dette scenariet gjelder vanligvis hvis en etikettrull har gått tapt eller er skadet. Den inneholder et eksempel som viser hvordan du oppretter menyelementer for mobilenheter som lar arbeidere skrive ut enkle og flere etiketter på nytt. Deretter vises det hvordan du bruker disse nye menyelementene mens du arbeider med en mobilenhet.

### <a name="set-up-the-required-menu-items-and-menu-for-the-mobile-device"></a>Konfigurere de nødvendige menyelementene og menyen for den mobile enheten

Før arbeidere kan skrive ut etiketter på nytt fra en mobil enhet, må du angi menyelementer for å tilby denne funksjonaliteten og deretter legge til disse varene på lagerappmenyen.

#### <a name="create-new-mobile-device-menu-items"></a>Opprette nye menyelementer for mobilenhet

Følg disse trinnene for å opprette en ny samling av menyelementer for å skrive ut etiketter på nytt fra lagerstyringsappen.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Opprett et menyelement, og angi følgende verdier for det:

    - **Menyelementnavn:** *Skriv ut enkel bølgeetikett på nytt*
    - **Tittel:** *Skriv ut enkel bølgeetikett på nytt*
    - **Modus:** *Indirekte*
    - **Aktivitetskode:** *Skriv ut enkel bølgeetikett på nytt*

1. Opprett et menyelement nummer to, og angi følgende verdier for det:

    - **Menyelementnavn:** *Skriv ut etiketter på nytt (vare)*
    - **Tittel:** *Skriv ut bølgeetiketter på nytt (vare)*
    - **Modus:** *Indirekte*
    - **Aktivitetskode:** *Skriv ut flere bølgeetiketter på nytt*
    - **Vis filter for arbeidslistegruppering:** *Ja*
    - **Systemgrupperingsfelt:** *ShipmentID*
    - **Systemgrupperingsetikett:** *ShipmentID*
    - **Utskriftsmodus:** *Produkt*

1. I handlingsruten velger du **Feltliste** for å åpne en side der du kan velge feltene som skal vises for å hjelpe arbeiderne med å identifisere den riktige etikettrullen.
1. Du kan vise opptil sju felt. Bruk rullegardinlisten til å velge feltet som vises i hver tilgjengelige posisjon. La feltene du ikke trenger, være tomme. 

    Her er et eksempel:

    - **Visningsfelt:** *LabelItemId*
    - **Visningsfelt 2:** *LabelItemName*
    - **Visningsfelt 3:** *InventQty*
    - **Visningsfelt 4:** *LabelUnitId*

1. Lukk siden.
1. Opprett et menyelement nummer tre, og angi følgende verdier for det:

    - **Menyelementnavn:** *Skriv ut etiketter på nytt (Opplisting)*
    - **Tittel:** *Skriv ut bølgeetiketter på nytt (Opplisting)*
    - **Modus:** *Indirekte**
    - **Aktivitetskode:** *Skriv ut flere bølgeetiketter på nytt*
    - **Vis filter for arbeidslistegruppering:** *Ja*
    - **Systemgrupperingsfelt:** *ShipmentID*
    - **Systemgrupperingsetikett:** *ShipmentID*
    - **Utskriftsmodus:** *Opplisting*

1. I handlingsruten velger du **Feltliste** , og deretter bruker du rullegardinlistene til å velge feltene som skal vises for å hjelpe arbeiderne med å identifisere den riktige etikettrullen (for eksempel *LabelItemId* , *LabelItemName* , *InventQty* , *LabelUnitId* og *NumberOfLabels* ).
1. Lukk siden.
1. Opprett et menyelement nummer fire, og angi følgende verdier for det:

    - **Menyelementnavn:** *Skriv ut etiketter på nytt (etter siste)*
    - **Tittel:** *Skriv ut bølgeetiketter på nytt (etter siste)*
    - **Modus:** *Indirekte*
    - **Aktivitetskode:** *Skriv ut flere bølgeetiketter på nytt*
    - **Vis filter for arbeidslistegruppering:** *Ja*
    - **Systemgrupperingsfelt:** *ShipmentID*
    - **Systemgrupperingsetikett:** *ShipmentID*
    - **Utskriftsmodus:** *Siste gode bølgeetikett-ID*

1. I handlingsruten velger du **Feltliste** , og deretter bruker du rullegardinlistene til å velge feltene som skal vises for å hjelpe arbeiderne med å identifisere den riktige etikettrullen (for eksempel *LabelItemId* , *LabelItemName* , *InventQty* , *LabelUnitId* og *NumberOfLabels* ).
1. Lukk siden.

#### <a name="set-up-the-mobile-device-menu"></a>Definere mobilenhetsmeny

Følg disse trinnene for å legge til de nye menyelementene på lagerappmenyen.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.
1. Velg en eksisterende **Utgående** -meny.
1. I listen til venstre finner du menyelementene for ny utskrift som du nettopp opprettet, og deretter bruker du høyre pilknapp for å legge dem til i listen til høyre.
1. Lukk siden.

### <a name="use-cases"></a>Brukstilfeller

Brukstilfellene som finnes her, gir eksempler som viser hvordan du kan bruke de ulike mobilenhetsmenyelementene du konfigurerer, til å aktivere arbeidere til å skrive ut bølgeetiketter på nytt.

Før du arbeider med disse brukstilfellene må følgende forutsetninger være på plass:

- Du må installere demonstrasjonsdata, og du må velge den juridiske enheten **USMF**.
- Utskrift av bølgeetiketter må konfigureres, og enkelte etiketter må genereres, som beskrevet i [Konfigurere bølgeetikettutskrift](../warehousing/configure-wave-label-printing.md).

#### <a name="use-case-21-a-single-wave-label-is-scratched-and-must-be-reprinted"></a>Brukstilfelle 2.1: En enkelt bølgeetikett er kassert og må skrives ut på nytt.

1. Logg på lagerappen som en bruker som har tilgang til lager *62*. (I standard demodata kan du logge deg på ved å bruke *62* som bruker-ID og *1* som passord.)
1. Gå til **Utgående \> Skriv ut enkel bølgeetikett på nytt**.
1. Angi eller skann bølgeetikett-IDen.
1. Velg skriveren du vil skrive ut på.
1. Velg **OK** for å bekrefte handlingen.

#### <a name="use-case-22-several-labels-for-boxes-of-the-same-item-were-damaged-and-must-be-reprinted-each-label-has-a-product-bar-code-but-no-enumeration-or-sscc-number"></a>Bruks tilfelle 2.2: Flere etiketter for bokser for samme vare er skadet og må skrives ut på nytt. Hver etikett har en produktstrekkode, men ikke opplistings- eller SSCC-nummer.

1. Logg på lagerappen som en bruker som har tilgang til lager *62*. (I standard demodata kan du logge deg på ved å bruke *62* som bruker-ID og *1* som passord.)
1. Gå til **Utgående \> Skriv ut etiketter på nytt (vare)**.
1. Angi eller skann forsendelses-IDen.
1. Velg flisen som har riktig etikettrull å skrive ut på nytt fra.
1. Skann produktstrekkoden fra en eksisterende etikett for å bekrefte at riktig linje er valgt.
1. Angi antallet etiketter som skal skrives ut på nytt.
1. Velg skriveren du vil skrive ut på.
1. Velg **OK** for å bekrefte handlingen.

#### <a name="use-case-23-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-because-the-labels-have-enumeration-you-can-define-the-carton-range-to-reprint"></a>Bruks tilfelle 2.3: Det ble ikke skrevet ut flere etiketter for bokser på grunn av papirproblemer i skriveren. Siden etikettene har opplisting, kan du definere kartongområdet som skal skrives ut på nytt.

1. Logg på lagerappen som en bruker som har tilgang til lager *62*. (I standard demodata kan du logge deg på ved å bruke *62* som bruker-ID og *1* som passord.)
1. Gå til **Utgående \> Skriv ut etiketter på nytt (Opplisting)**.
1. Angi eller skann forsendelses-IDen.
1. Velg flisen som har riktig etikettrull å skrive ut på nytt fra.
1. Angi den første kartongen som du vil skrive ut en etikett for.
1. Angi den siste kartongen som du vil skrive ut en etikett for. Du kan også la dette feltet stå tomt hvis du vil skrive ut etiketter på nytt for alle kartonger etter den angitte første kartongen.
1. Velg skriveren du vil skrive ut på.
1. Velg **OK** for å bekrefte handlingen.

#### <a name="use-case-24-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-the-last-good-label-has-a-wave-label-id-that-is-printed-as-a-bar-code"></a>Bruks tilfelle 2.4: Det ble ikke skrevet ut flere etiketter for boser på grunn av papirproblemer i skriveren. Den siste gode etiketten har en bølgeetikett-ID som skrives ut som en strekkode.

1. Logg på lagerappen som en bruker som har tilgang til lager *62*. (I standard demodata kan du logge deg på ved å bruke *62* som bruker-ID og *1* som passord.)
1. Gå til **Utgående \> Skriv ut etiketter på nytt (etter siste)**.
1. Angi eller skann forsendelses-IDen.
1. Velg flisen som har riktig etikettrull å skrive ut på nytt fra.
1. Angi eller skann bølgeetikett-ID-en til den siste gode bølgeetiketten. Appen identifiserer den neste etiketten i sekvensen som den første kartongen som en etikett vil bli skrevet ut på nytt for.
1. Angi den siste kartongen som du vil skrive ut en etikett for. Du kan også la dette feltet stå tomt hvis du vil skrive ut etiketter på nytt for alle kartonger etter den angitte første kartongen.
1. Velg skriveren du vil skrive ut på.
1. Velg **OK** for å bekrefte handlingen.

## <a name="scenario-3-short-pick-and-reprint"></a>Scenario 3: Plukk med mangler og ny utskrift

Før du arbeider gjennom dette scenarioet må følgende forutsetninger være på plass:

- Du må installere demonstrasjonsdata, og du må velge den juridiske enheten **USMF**.
- Utskrift av bølgeetiketter må konfigureres, og enkelte etiketter må genereres, som beskrevet i [Konfigurere bølgeetikettutskrift](../warehousing/configure-wave-label-printing.md).

### <a name="set-up-work-exceptions"></a>Konfigurer arbeidsunntak

Arbeidsunntak kontrollerer virkemåten til plukking med mangler. Følg disse trinnene for å angi et arbeidsunntak.

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsunntak**.
1. Opprett en post som har følgende innstillinger:

    - **Kode for arbeidsunntak:** *Plukk med mangler og utskrift*
    - **Unntakstype:** *Plukk med mangler*
    - **Foreslå ny utskrift av bølgeetiketter:** *Ja*

### <a name="void-and-reprint-after-a-short-pick"></a>Annuller og skriv ut på nytt etter plukk med mangler

1. Logg på lagerappen som en bruker som har tilgang til lager *62*. (I standard demodata kan du logge deg på ved å bruke *62* som bruker-ID og *1* som passord.)
1. Åpne en arbeidsbehandlingsflyt for salgsordrearbeidet som ble opprettet når bølgeetiketter opprinnelig ble skrevet ut.
1. Velg **Plukk med mangler**.
1. Velg arbeidsunntakskoden du opprettet for dette scenariet.
1. Hvis du valgte det riktige unntaket, vil avmerkingsboksen **Annuller og skriv ut på nytt** være tilgjengelig. Merk av i denne boksen og bekreft. Ved bekreftelse blir etikettrullsekvensen som identifiseres av feltet **Etikettversjons-ID** , beregnet på nytt basert på det endrede arbeidslinjeantallet. Den skrives deretter ut på nytt på den angitte skriveren.

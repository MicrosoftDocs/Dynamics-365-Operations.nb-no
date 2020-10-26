---
title: Attributtbaserte salgspriser for begrensningsbasert produktkonfigurasjon
description: Dette emnet beskriver hvordan du bygger salgsprismodeller med salgspriser som er basert på komponenter og attributter, i stedet for på den fysiske stykklisten og ruten.
author: sorenva
manager: tfehr
ms.date: 10/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2020-08-17
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: c0f9c1bb94b4dcc3c3c1e7656868ef6e6bd903db
ms.sourcegitcommit: 9ca63cbc6bc6d6baed9d45bce30d0b32e156301c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/12/2020
ms.locfileid: "3988328"
---
# <a name="attribute-based-sales-prices-for-constraint-based-product-configuration"></a>Attributtbaserte salgspriser for begrensningsbasert produktkonfigurasjon

Dette emnet beskriver hvordan du bygger salgsprismodeller med salgspriser som er basert på komponenter og attributter, i stedet for på den fysiske stykklisten og ruten. Du kan bygge flere salgsprismodeller for hver produktkonfigurasjonsmodell.

## <a name="set-relevant-product-information-management-parameters"></a>Angi relevante parametere for produktinformasjonsbehandling

Før du begynner å bygge prismodellene må du definere en standardvaluta som brukes når du bygger opp salgsprismodellene. Du kan også velge om du vil tilknytte en Microsoft Excel-fil med prisoppdeling for alle ordre- eller tilbudslinjer. Prisoppdeling lar deg dele detaljer med kunder om hvordan du kom frem til en bestemt salgspris for et konfigurert produkt.

Slik angir du standardvalutaen:

1. Gå til **Behandling av produktinformasjon \> Oppsett \> Parametere for produktinformasjonsbehandling** .
1. Åpne kategorien **Begrensningsbaserte produktkonfigurasjonsmodeller** .
1. Åpne rullegardinlisten **Standardvaluta** , og velg valuta.

    ![Angi standardvaluta for begrensningsbasert produktkonfigurasjon](media/prod-config-currency.png "Angi standardvaluta for begrensningsbasert produktkonfigurasjon")

1. Hvis du vil tilknytte en Excel-fil med prisoppdeling for alle ordre- eller tilbudslinjer, går du til delen **Prismodell** og setter **Legg ved** til *Ja* .

## <a name="build-your-sales-price-models"></a><a name="build-price-model"></a>Lage salgsprismodeller

Slik lager du salgsprismodeller:

1. Gå til **Behandling av produktinformasjon \> Produkter \> Produktkonfigurasjonsmodeller** .
1. Velg målproduktkonfigurasjonsmodellen.
1. Åpne kategorien **Modell** i handlingsruten, og gå til **Oppsett** -gruppen og velg **Prismodeller** .
1. Siden **Prismodeller** åpnes.
1. Velg en prismodell, eller legg til en ny i rutenettet.
1. Velg **Rediger** for å åpne redigeringssiden for den valgte modellen, som inneholder følgende funksjoner:
    - Toppteksten i skjemaet viser standardvalutaen, og lar deg legge til nye valutaer for prisoppsettet.
    - Ruten til venstre viser alle komponentene og brukerkravene for produktmodellen. Hver node i produktmodelltreet kan ha ett basisprisuttrykk og et valgfritt antall uttrykksregler. En uttrykksregel består av en betingelse og et uttrykk, og hver uttrykksregel dekker et produktalternativ som hjelper med å styre prisen på produktet.
    - Når du lager betingelser og uttrykk, har du de samme operatorene tilgjengelige som for beregninger i en produktmodell. Uttrykksredigering støtter også både betingelser og uttrykk.
1. Velg en node i venstre kolonne, og bruk deretter funksjonene som er beskrevet i det forrige trinnet til å etablere prisregler for den (se også eksemplet etter denne prosedyren). Gjenta dette trinnet for hver node etter behov.

Følgende eksempel viser en basispris for et statisk antall på 899,95 EUR, som kan endres av én eller flere av følgende fem uttrykksregler, avhengig av konfigurasjonen som er valgt av kunden:

- Trekk fra 59,95 EUR for hvit kabinettfinish.
- Legg til 35,95 EUR for hjørnebeskyttelse.
- Legg til 89,95 EUR for frontgrill i metall.
- Legg til 119,95 EUR for skak i rosewood-finish.
- Legg til 12,95 EUR for hver høyttalerhøyde.

![Eksempel på prismodell](media/prod-config-rules-example.png "Eksempel på prismodell")

## <a name="add-support-for-multiple-currencies"></a>Legge til støtte for flere valutaer

Når et konfigurerbart produkt selges, kontrollerer systemet om prisene er angitt eksplisitt i valutaen til kunden. I så fall brukes de eksplisitte verdiene. Hvis ikke bruker systemet valutakursene som er opprettet for salgsfirmaet, til å konvertere standard valutaverdi til kundens valuta.

Slik legger du til eksplisitte priser i tilleggsvaluta:

1. Åpne redigeringssiden for prismodellen, som beskrevet i [Lage salgsprismodeller](#build-price-model).
1. Velg **Legg til** -knappen i toppteksten for prismodellen for å åpne dialogboksen for rullegardinlisten **Valutaer** , som viser de tilgjengelige valutaene.
1. Velg valutaen du vil legge til i dialogboksen for rullegardinlisten **Valutaer** , og velg deretter **OK** .
1. Rullegardinlisten **Gjeldende valuta** inneholder nå valutaen du nettopp la til, pluss eventuelle andre valutaer som kan ha blitt lagt til tidligere. Velg den nye valutaen, og legg merke til at rutenettet i delen **Uttrykksregler** nå inneholder to uttrykksfelt:
    - **Uttrykk** – Viser uttrykket (eller konstant verdi) for å finne prisen ved hjelp av valutaen som er valgt for **Gjeldende valuta** .
    - **Standarduttrykk** – Viser uttrykket (eller konstant verdi) for å finne prisen ved hjelp av gjeldende standard (vises i feltet **Gjeldende valuta** ).

    > [!NOTE]
    > **Betingelse** -feltet for uttrykksreglene "eies" av standardvalutaen, og det betyr at du ikke kan endre betingelsen for andre valutaer. Du kan heller ikke legge til nye uttrykksregler mens en annen valuta enn standardvalutaen er valgt som **Gjeldende valuta** .
1. Rediger verdiene i **Uttrykk** -kolonnen etter behov for gjeldende valuta.

I eksemplet nedenfor er _EUR_ standardvalutaen, og _USD_ er lagt til som en tilleggsvaluta.

![Eksempel på en modell med flere valutaer](media/prod-config-rules-currency-example.png "Eksempel på en modell med flere valutaer")

> [!NOTE]
> Du kan ikke legge til uttrykksregler som er unike for en valuta som ikke er standard. Hvis du vil opprette uttrykksregler som bare gjelder for en annen valuta enn standardvalutaen, kan du sette prisuttrykket for standardvalutaen til null. Deretter angir du det aktuelle uttrykket for valutaen som ikke er standard.

## <a name="test-your-price-model"></a>Teste prismodellen

Hvis du vil teste hvordan salgsprisene fungerer i en konfigurasjonsøkt, åpner du redigeringssiden for prismodellen, som beskrevet under [Lage salgsprismodeller](#build-price-model), og deretter velger du **Test** i handlingsruten. Dialogboksen **Test produktmodell** åpnes, der du kan gjøre følgende:

- Bruk konfigurasjonsinnstillingene her til å velge produktalternativer, og se deretter hvordan de påvirker verdien som vises for **Pris og forsendelsesdato** .
- Velg **Vis prisoppdeling** for å laste ned et Excel-dokument som viser detaljert informasjon om hvordan prisen ble beregnet.

![Teste produktmodellen](media/prod-config-test.png "Teste produktmodellen")

Det nedlastede regnearket viser både absolutt verdi og dekning som en prosent for hvert aktive priselement. Hvis du har angitt alternativet **Legg ved** for prismodellen på siden **Parametere for produktinformasjonsbehandling** , blir dette Excel-arket lagt ved ordre- eller tilbudslinjen.

![Excel-regneark som viser prisoppdeling](media/prod-config-excel-example.png "Excel-regneark som viser prisoppdeling")

## <a name="set-up-selection-criteria-for-price-models"></a>Konfigurere utvalgskriterier for prismodeller

Når prismodellene er på plass, må du opprette minst ett utvalgskriterium for å hente prismodellen når du konfigurerer til tilbud eller ordre. Du gjør dette ved å konfigurere én eller flere spørringer. I en kombinasjon med samsvarende salgsprismodeller gir spørringene stor fleksibilitet for målretting av salgspriser for bestemte kunder, områder, perioder og andre kriterier.

Slik konfigurerer du utvalgskriterier for prismodeller:

1. Gå til **Behandling av produktinformasjon \> Produkter \> Produktkonfigurasjonsmodeller** .
1. Velg målproduktkonfigurasjonsmodellen.
1. Åpne kategorien **Modell** i handlingsruten, og gå til **Oppsett** -gruppen og velg **Prismodellkriterier** . Siden **Prismodellkriterier** åpnes.
1. Hvis spørringsraden du trenger, ikke finnes ennå, velger du **Ny** i handlingsruten for å legge til en ny rad i rutenettet og angi følgende innstillinger for den:
    - **Navn** – Angi et navn for raden.
    - **Beskrivelse** – Beskriv kort spørringen og hva den gjelder for.
    - **Prismodell** – Velg en [prismodell](#build-price-model) (fra den gjeldende konfigurasjonsmodell) som spørringen skal bruke når den utløses.
    - **Ordretype** – Velg ordretypen forespørselen skal gjelde for.
    - **Gyldig fra** – Angi den første dagen spørringen skal gjelde.
    - **Utløp innen** – Angi den siste datoen spørringen skal gjelde.

    ![Prismodellkriterier](media/prod-config-price-model-criteria.png "Prismodellkriterier")

1. Velg raden for spørringen du vil definere, og velg deretter **Rediger** i **handlingsruten** . Dialogboksen for spørringsutforming åpnes. Det fungerer som de fleste spørringsutformere i Supply Chain Management. Bruk dette til å definere vilkårene for bruk av prismodellen for den valgte raden.

1. Gjenta trinn 4–5 for hver spørring du trenger.
    > [!TIP]
    > Du kan spare tid ved å kopiere en eksisterende rad som allerede ligner på en ny, som du må legge til. Dette gjør du ved å velge en målrad og deretter velge **Duplikat** i handlingsruten.

1. Når du er ferdig med å definere kriteriene, kan du ordne dem i riktig rekkefølge i listen **Prismodellkriterier** . Hvis du vil flytte en rad, merker du raden og velger **Opp** eller **Ned** i handlingsruten.

    > [!IMPORTANT]
    > På konfigurasjonstidspunktet starter systemet å søke fra toppen av listen og bruker den første spørringen som samsvarer med dataene i tilbuds- eller ordrelinjen. Du må derfor plassere de mest spesifikke spørringene øverst. Hvis du plasserer en generell spørring øverst på listen, brukes denne selv om det kan være en spørring i listen som er rettet mot den nøyaktige kunden eller kundeemnet for konfigurasjonen.

## <a name="set-attribute-based-sales-prices-for-the-product-model-version"></a>Angi attributtbaserte salgspriser for produktmodellversjonen

Det siste trinnet er å angi attributtbaserte salgspriser for produktmodellversjonen. Slik gjør du det:

1. Gå til **Behandling av produktinformasjon \> Produkter \> Produktkonfigurasjonsmodeller** .
1. Velg målproduktkonfigurasjonsmodellen.
1. Åpne kategorien **Modell** i handlingsruten, og gå til **Produktmodelldetaljer** -gruppen og velg **Versjoner** .
1. **Versjoner** -siden åpnes. Kontroller at **Prismetode** er satt til **Attributtbasert** .
    ![Sette prismetode til attributtbasert](media/prod-config-versions.png "Sette prismetode til attributtbasert")

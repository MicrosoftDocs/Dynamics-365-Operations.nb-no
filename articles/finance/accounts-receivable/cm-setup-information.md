---
title: Oppsett for kredittbehandling
description: Dette emnet beskriver oppsettet som kreves for kredittbehandling.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5cd6d2f23a68ad3d7308d40a2638866dde7a7a81
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224771"
---
# <a name="credit-management-setup"></a>Oppsett for kredittbehandling 

[!include [banner](../includes/banner.md)]

## <a name="credit-management-workflows"></a>Arbeidsflyter for kredittbehandling

Gå til **Kreditt og innkreving \> Oppsett \> Arbeidsflyter for kredittbehandling** for å definere arbeidsflytene som brukes til å behandle kredittgrensejusteringer.

- Du kan opprette en arbeidsflyt som lar deg godkjenne et parti med kredittgrensejusteringer gjennom én enkelt godkjenning.
- Du kan legge til en arbeidsflyt på linjenivå, slik at kredittgrensejusteringer kan godkjennes individuelt.
- Du kan opprette en arbeidsflyt for frigivelse som automatisk ruter sperringer til en arbeidsflytprosess.

## <a name="blocking-rules"></a>Sperreregler

### <a name="ranking-payment-terms"></a>Rangere betalingsbetingelser

Du kan sette en salgsordre på vent hvis betalingsbetingelsene for ordren ikke samsvarer med standard betalingsbetingelsene for kunden. Noen ganger er betalingsbetingelsene imidlertid forskjellige, men ligner nok til at du ikke vil sette ordren på vent. Du kan rangere betalingsbetingelser slik at noen av dem har samme rangering, mens andre har en høyere eller lavere rangering.

Hvis rangeringene for betalingsbetingelsene er aktive, og hvis betalingsbetingelsene i ordren har høyere rangering enn standard betalingsvilkår for kunden, blir salgsordren satt på vent.

Du kan definere rangeringer av betalingsbetingelser ved å gå til **Kreditt og innkreving \> Oppsett \> Kredittbehandlingsoppsett \>Ranger betalingsbetingelser**  

### <a name="ranking-settlement-discounts"></a>Rangere utligningsrabatter

Du kan sette en salgsordre på vent hvis kontantrabatten for ordren ikke samsvarer med standard kontantrabatt for kunden. Noen ganger er kontantrabattene imidlertid forskjellige, men ligner nok til at du ikke vil sette ordren på vent. Du kan rangere kontantrabatter slik at noen av dem har samme rangering, mens andre har en høyere eller lavere rangering.

Hvis rangeringene for utligningsrabattene er aktive, vil salgsordren bli satt på vent hvis kontantrabatten i ordren har høyere rangering enn standard kontantrabatt for kunden.

Du kan definere rangeringer av betalingsbetingelser ved å gå til **Kreditt og innkreving \> Oppsett \> Kredittbehandlingsoppsett \>Ranger utligningsrabatter**  

## <a name="reasons"></a>Årsaker

Det brukes flere typer årsaker i kredittbehandling:

- Sperreårsaker angir hvorfor en salgsordre ble satt på vent.
- Frigivelsesårsaker tilordnes en ordre når den frigis fra sperring.
- Statusårsaker angir hvorfor en kontostatus ble tilordnet til en kunde.

Du kan definere årsaker på siden **Kredittbehandlingsårsaker** (**Kreditt og innkreving \> Oppsett \> Kredittbehandlingsoppsett \> Kredittbehandlingsårsaker**).

1. Velg årsakstypen i **Årsakstype**-feltet: **Sperre**, **Frigivelse** eller **Status**.
2. I **Årsak**-feltet angir du et navn på årsaken.
3. I **Beskrivelse**-feltet angir du en beskrivelse av årsakskoden.

## <a name="credit-management-groups"></a>Kredittbehandlingsgrupper

Kredittbehandlingsgrupper brukes til å identifisere kunder eller grupper med kunder som har samme kredittbehandlingsegenskaper. For eksempel kan kredittbehandlingsgrupper brukes til å bestemme kredittbehandlingsregler for blokkering og ekskludering for kunder.

Du kan opprette kredittbehandlingsgrupper på siden **Kredittbehandlingsgrupper** (**Kreditt og innkreving \> Oppsett > Kredittbehandlingsoppsett \> Kredittbehandlingsgrupper**).

1. Velg **Ny** for å opprette en linje.
2. Angi en ID for gruppen. ID-en kan inneholde opptil 10 tegn.
3. Skriv inn et navn for gruppen i feltet **Beskrivelse**. Navnet kan inneholde opptil 60 tegn.

Kredittbehandlingsgruppen tilordnes til en kunde i hurtigfanen **Kreditt og innkreving** på **Alle kunder**-siden (**Kunder \> Kunder \> Alle kunder**).

## <a name="account-statuses"></a>Kontostatuser

Du kan opprette kontostatuser som identifiserer kredittstatusen til en kundekonto. Du kan definere en status og virkningen på prosessene for fakturering og levering på vent. Kontostatuser kan også brukes til å bestemme blokkeringsregler for en kunde.

Du kan opprette kontostatuser på **Kontostatuser**-siden (**Credit and collections \> Oppsett > Kredittbehandlingsoppsett \> Kontostatuser**).

1. Legg til en kontostatus, og angi en beskrivelse som representerer kredittstatusen for en kunde. Du kan for eksempel bruke **Normal** til å angi at en kunde er solid og åpne ordrer er underlagt standard kredittbehandling.
2. I feltene **Fakturering** og **Levering på vent** velger du type sperring som skal forekomme for kunder som har denne kontostatusen. Du kan sperre all behandling, bare fakturabehandling eller ingen behandling når kredittgrensereglene brukes.

## <a name="scoring-groups"></a>Poengberegningsgrupper

Du kan definere poengberegningsgrupper for å definere risikofaktorer og kriteriene som brukes til å måle dem. Når informasjon om en kunde brukes på en poengberegningsgruppe, beregnes en poengsum for hver risikofaktor og brukes til å plassere kunden i en risikogruppe. Risikogruppen kan brukes til å identifisere kredittverdighet og beregne automatiske kredittgrenser.

Du kan opprette poengberegningsgrupper på siden **Poengberegningsgrupper** (**Kreditt og innkreving \> Oppsett \> Kredittbehandlingsoppsett \> Risiko \> Poengberegningsgrupper**).

1. Opprett en poengberegningsgruppe og angi et navn for den.
2. Angi en beskrivelse for å beskrive poengberegningsgruppen ytterligere.
3. Velg en gruppetype. Det finnes åtte forhåndsdefinerte typer. Du kan også velge **Brukerdefinert** for å definere en gruppetype som er bedre egnet for organisasjonen.
4. Velg en poengsumtype for å definere hvordan poengberegningsgruppen skal beregne risikopoengene. Følgende alternativer er tilgjengelige:

    - **Område** – Bruk dette alternativet til å definere et verdiområde som skal brukes til å beregne en poengsum.
    - **Brukerdefinert** – Bruk dette alternativet til manuelt å definere en liste over verdier som skal brukes for poengsummen.

5. Hvis du valgte **Område** som poengsumtype, legger du til linjer for å definere verdiområdet og de tilsvarende poengsummene.

    1. I **Fra verdi**-feltet angir du den laveste verdien i området.
    2. I **Til verdi**-feltet angir du den høyeste verdien i området.
    3. I **Poengsum**-feltet angir du poengsummen som skal tilordnes når verdien som er oppgitt, er i fra/til-området.

    Hvis du valgte **Brukerdefinert** som poengsumtype, legger du til linjer for å definere de brukerdefinerte verdiene og de tilsvarende poengsummene.

    1. I **Verdi**-feltet angir du den brukerdefinerte verdien som skal oppgis fra kundeinformasjonen.
    2. I **Poengsum**-feltet angir du poengsummen som skal tilordnes når verdien som er oppgitt, er i fra/til-området.

## <a name="risk-classification"></a>Risikoklassifisering

Du kan definere risikovurderinger som kan tilordnes til kunder, basert på risikopoengene deres. En risikopoengsum beregnes ved å sammenligne kundeinformasjon med hver poengberegningsgruppe. Poengene summeres, og den totale poengsummen sammenlignes med verdiene i risikogruppeoppsettet for å identifisere risikogruppen som kunden tilhører. Risikogruppepoengsummen brukes deretter til å definere blokkerings- og ekskluderingsregler for kredittbehandling for kunden.

Du kan definere risikogrupper på siden **Risikovurderinger** (**Kreditt og innkreving \> Oppsett \> Kredittbehandlingsoppsett \> Risiko \> Risikoklassifisering**).

1. Angi en risikogruppe-ID.
2. Angi en beskrivelse for å forklare risikogruppen ytterligere.
3. Angi et område med poeng som brukes til å bestemme hvilke kunder som tilhører risikogruppen.
4. Velg en risikogruppeindikator for å angi symbolet som representerer risikogruppen.

## <a name="guaranteeinsurance-types"></a>Garanti-/forsikringstyper

Du kan definere garanti-/forsikringstyper på siden **Garanti-/forsikringstyper** (**Kreditt og innkreving \> Oppsett \> Kredittbehandlingsoppsett \> Forsikring og garantier \> Forsikrings- og garantiertyper**).

1. Angi en garanti- eller forsikringstype som identifiserer navnet på garantisten eller forsikringsgiveren.
2. Angi en beskrivelse for å beskrive garantisten/forsikringsgiveren.

## <a name="coverage-types"></a>Dekningstyper

Dekningstyper kan brukes til å klassifisere forsikringspoliser ytterligere. De kan ikke brukes med garantier.

Du kan legge til dekningstyper på **Dekningstyper**-siden (**Kreditt og innkreving \> Oppsett \> Kredittbehandlingsoppsett \> Forsikring og garantier \> Dekningstyper**).

1. Angi en dekningstype for å identifisere typen dekning som skal legges til som forsikring eller garanti.
2. Angi en beskrivelse for å beskrive dekningstypen.

## <a name="automatic-credit-limits"></a>Automatiske kredittgrenser

Du kan opprette kriterier for automatiske kredittgrenser på siden **Automatiske kredittgrenser** (**Kreditt og innkreving \> Oppsett \> Kredittbehandlingsoppsett \> Risiko \> Automatiske kredittgrenser**).

1. Velg en risikogruppe som den automatiske kredittgrensen skal tilordnes til.
2. Velg valutaen for den automatiske kredittgrensen. Du kan opprette flere automatiske kredittgrenser i forskjellige valutaer for samme risikogruppe.
3. Angi inntektsbeløpet som representerer maksimal firmainntekt som kan brukes for denne automatiske kredittgrensen. Når kredittgrenser opprettes, sammenlignes inntektsbeløpet med en inntektsverdi som finnes på **Finans**-siden (**Kunder \> Alle kunder \> Velg en kunde \> Generelt \> Statistikk \> Finans**). Systemet bruker den siste verdien i **Oversikt**-delen.

Følg disse trinnene for å legge til linjer som representerer kredittgrensen som genereres basert på de valgte kriteriene.

1. Velg poengberegningsgruppen som definerer kundeinformasjonen som skal brukes til å beregne kredittgrensen.
2. Velg sammenligningsoperatoren som definerer hvordan informasjonen om poengberegningsgruppen skal evalueres.
3. Angi verdien som skal sammenlignes med verdien som angis for poengberegningsgruppen.
4. Angi kredittgrensen som skal tilordnes hvis kundeinformasjonen samsvarer med verdien som er angitt for poengberegningsgruppen. Du oppretter for eksempel en automatisk kredittgrense for den **lave** poengberegningsgruppen. Hvis årene i virksomhet er en av poengberegningsgruppene, kan du definere en linje som tilordner en 100 000 kredittgrense hvis kunden har drevet virksomheten i fem år, og en annen linje som tilordner en 200 000 kredittgrense hvis kunden har drevet virksomheten i 10 år.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Endre celler for raddefinisjon
description: Denne artikkelen beskriver informasjonen som kreves for hver celle i en raddefinisjon i en finansrapport, og beskriver hvordan du registrerer denne informasjonen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations, Core
ms.custom: 58881
ms.assetid: 0af492df-a84e-450c-8045-78ef1211abaf
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: eb09c0bb28c2ba8e7b890854c444cec80fe8277c
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="modify-row-definition-cells"></a>Endre celler for raddefinisjon

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver informasjonen som kreves for hver celle i en raddefinisjon i en finansrapport, og beskriver hvordan du registrerer denne informasjonen. 

# <a name="specify-a-row-code-in-a-row-definition"></a>Angi en radkode i en raddefinisjon

I raddefinisjoner identifiserer tall eller etiketter **Radkode**-cellen hver linje i raddefinisjonen. Du kan angi radkoden for å referere til data i beregninger og totaler.

### <a name="row-code-requirements"></a>Krav til radkode

En radkode kreves for alle rader. Du kan blande numeriske koder, alfanumeriske koder og ikke-angitte (tom) radkoder i en raddefinisjon. Radkoden kan være positive heltall (mindre enn 100 000 000) eller beskrivende etiketter som identifiserer raden. En beskrivende etiketten må følge disse reglene:

-   Etiketten må begynne med et alfabetisk tegn (a til z eller A til Z), og kan være en kombinasjon av tall og bokstaver på opptil 16 tegn. 
    > [!NOTE]
    > En etikett kan inneholde understrekingstegnet (\_), men ingen andre spesialtegn er tillatt.
-   Etiketten kan ikke bruke noen av følgende reserverte ord: AND, OR, IF, THEN, ELSE, PERIODS, TO, BASEROW, UNIT, NULL, CPO, eller RPO.

Eksemplene nedenfor er gyldige rad oder:

-   320
-   TL\_NET\_INCOME
-   TL\_NET\_94

### <a name="change-a-row-code-in-a-row-definition"></a>Endre en radkode i en raddefinisjon

1.  I Rapportutforming klikker du **Raddefinisjoner**, og deretter åpner du raddefinisjonen som skal endres.
2.  Angi den nye verdien i cellen i **Radkode**-kolonnen i den aktuelle raden.

### <a name="reset-numeric-row-codes"></a>Tilbakestille numeriske radkoder

1.  I Rapportutforming klikker du **Raddefinisjoner**, og deretter åpner du raddefinisjonen som skal endres.
2.  På **Rediger**-menyen klikker du **Nummerer rader**.
3.  I dialogboksen **Nummerer rader** angir du nye verdier for den første radkoden og radkodeintervallet. Du kan tilbakestille de numeriske radkodene til verdier med lik avstand. Rapportutforming nummererer imidlertid bare radkoder som begynner med tall (for eksempel 130 eller 246). Den nummerere ikke radkoder som begynner med bokstaver (for eksempel INCOME\_93 eller TP0693). 
> [!NOTE]
> Når du nummererer radkoder, oppdaterer rapportutforming automatisk **TOT**- og **CAL**-referanser. Hvis en **TOT**-rad for eksempel refererer til et intervall som starter med radkoden 100, og du nummererer radene på nytt fra og med 90, endres startreferansen **TOT** fra 100 til 90.

## <a name="add-a-description"></a>Legge til en beskrivelse
Beskrivelsescellen inneholder beskrivelsen av de økonomiske dataen i raden i rapporten, for eksempel "Inntekt" eller "Nettoinntekt". Teksten i **Beskrivelse**-cellen vises i rapporten nøyaktig slik du skriver den inn i raddefinisjonen. 
> [!NOTE]
> Bredden til beskrivelseskolonnen i rapporten angis i kolonnedefinisjonen. Hvis teksten i **Beskrivelse**-kolonnen i raddefinisjonen er lang, kontrollerer du bredden på **DESC**-kolonnen. Når du bruker dialogboksen **Sett inn rader fra**, er verdiene i **Beskrivelse**-kolonnen segmentverdiene eller dimensjonsverdiene fra de økonomiske dataene. Du kan sette inn rader for å legge til beskrivelsestekst, for eksempel en avsnittsoverskrift eller en avsnittssum, og for å legge til formatering, for eksempel en linje før en radsum. Hvis rapporten inneholder et rapporteringstre, kan du inkludere mer tekst som er definert for rapporteringsenhetene i rapporteringstreet. Du kan også begrense tilleggsteksten til en bestemt rapporteringsenhet.

### <a name="add-the-description-for-a-line-on-a-report"></a>Legge til beskrivelsen for en linje i en rapport

1.  I Rapportutforming klikker du **Raddefinisjoner**, og deretter åpner du raddefinisjonen som skal endres.
2.  Velg **Beskrivelse**-cellen, og skriv deretter inn navnet på rapportraden.
3.  Bruke formatering.

### <a name="add-additional-text-from-a-reporting-tree-in-the-description"></a>Legge til tilleggstekst fra et rapporteringstre i beskrivelsen

1.  I Rapportutforming klikker du **Raddefinisjoner**, og deretter åpner du raddefinisjonen som skal endres.
2.  Angi koden for tilleggsteksten og eventuell annen tekst i det aktuelle **Beskrivelse**-cellen.
3.  Bruke formatering.

### <a name="limit-the-additional-text-to-a-specific-reporting-unit"></a>Begrense tilleggsteksten til en bestemt rapporteringsenhet

1.  I Rapportutforming klikker du **Raddefinisjoner**, og deretter åpner du raddefinisjonen som skal endres.
2.  Finn raden der resten av teksten skal opprettes, og dobbeltklikk deretter cellen i Kolonnen **Relaterte formler/rader/enheter**.
3.  I dialogboksen **Valg av rapporteringsenhet**, i **Rapporteringstre**-feltet, velger du et rapporteringstre.
4.  Vis eller skjul rapporteringstreet i feltet **Velg rapporteringsenhet for begrensning**, og velg deretter en rapporteringsenhet.

## <a name="add-a-format-code"></a>Legge til en formatkode
**Formatkode**-celle tilbyr et utvalg av forhåndsformaterte valg for innholdet i denne raden. Hvis **Formatkode**-cellen er tom, tolkes raden som en detaljrad for økonomiske data. 
> [!NOTE]
> Hvis en rapport inneholder formateringsrader for nullantall som er knyttet til beløpsrader som er skjulte (for eksempel på grunn av nullsaldo), kan du bruke kolonnen **Relaterte formler/rader/enheter** for å hindre at tittel- og formatrader skrives ut.

### <a name="add-a-format-code-to-a-report-row"></a>Legge til en formatkode i en rapportrad

1.  I Rapportutforming klikker du **Raddefinisjoner**, og deretter velger du raddefinisjonen som skal endres.
2.  Dobbeltklikk **Formatkode**-cellen.
3.  Velg en formatkode i listen. Tabellen nedenfor beskriver formatkodene og handlingene.
    | Formatkode                   | Tolkning av formatkoden | Handling|
    |---|---|---|
    | (Ingen)                        |                                    | Tømmer **Formatkode**-cellen.                                                                                                                                                                               |
    | TOT                           | Sum                              | Identifiserer en rad som bruker matematiske operatorer i kolonnen **Relaterte formler/rader/enheter**. Totaler inneholder enkle operatorer, for eksempel **+** eller **-**.                                                      |
    | CAL                           | Beregning                        | Identifiserer en rad som bruker matematiske operatorer i kolonnen **Relaterte formler/rader/enheter**. Beregninger inneholder komplekse operatorer, for eksempel **+**, **-**, **\***, **/** og **IF/THEN/ELSE**-setninger. |
    | DES                           | beskrivelse                        | Identifiserer en overskriftslinje eller en tom linje i en rapport.                                                                                                                                                        |
    | LFT RGT CEN                   | Venstre Høyre Midt                  | Justerer den radbeskrivelsen på rapportsiden uavhengig av tekstens plassering i kolonnedefinisjonen.                                                                                               |
    | CBR                           | Endre basisrad                    | Identifiserer en rad som angir basisraden for kolonneberegninger.                                                                                                                                               |
    | COLUMN                        | Kolonneskift                       | Starter en ny kolonne i rapporten.                                                                                                                                                                             |
    | PAGE                          | Sideskift                         | Starter en ny side i rapporten.                                                                                                                                                                               |
    | ---                           | Enkel understreking                   | Setter en enkel strek under alle kolonnene i rapporten.                                                                                                                                                     |
    | ===                           | Dobbel understreking                   | Setter en dobbel strek under alle kolonnene i rapporten.                                                                                                                                                     |
    | LINE1                         | Tynn linje                          | Tegner en enkel tynn linje på tvers av siden.                                                                                                                                                                      |
    | LINJE2                         | Tykk linje                         | Tegner en enkelt tykk linje over siden.                                                                                                                                                                     |
    | LINJE3                         | Prikket linje                        | Tegner en enkel prikket linje på tvers av siden.                                                                                                                                                                    |
    | LINE4                         | Tykk linje og tynn linje           | Tegner en dobbel tynn linje på tvers av siden. Den øverste linjen er tykk, og den nederste er tynn.                                                                                                                       |
    | LINE5                         | Tynn linje og tykk linje           | Tegner en dobbel tynn linje på tvers av siden. Den øverste linjen er tynn, og den nederste er tykk.                                                                                                                       |
    | BXB BXC                       | Innrammet rad                          | Tegner en ramme rundt rapportradene som begynner med **BXB**-raden og slutter med **BXC**-raden.                                                                                                               |
    | KOM                           | Kommentar                             | Identifiserer en rad som er en kommentarrad, og som ikke skal skrives ut på rapporten. En kommentarrad kan for eksempel forklare formateringsteknikkene du bruker.                                                            |
    | SORT ASORT SORTDESC ASORTDESC | Sorter                               | Sorterer utgifter eller inntekter, sorterer en faktisk rapport eller avviksrapport for budsjett etter største avviket eller sorterer radbeskrivelsene alfabetisk.                                                                   |

## <a name="specify-related-formulasrowsunits"></a>Angi relaterte formler/rader/enheter
Cellen **Relaterte formler/rader/enheter** har mange funksjoner. Avhengig av hvilken type rad, kan en **Relaterte formler/rader/enheter**-celle utføre én av følgende funksjoner:

-   Definer radene du vil ta med i en beregning når du bruker **TOT**-formatkode eller en **CAL**-formatkode.
-   Koble en formateringsrad til et radbeløp, slik at formateringen bare skrives ut når det tilknyttede beløpet skrives ut.
-   Begrense en rad til en bestemt rapporteringsenhet.
-   Definer basisraden for beregninger når du bruker **BASEROW**-formatkoden.
-   Definer radene som skal sorteres når du bruker formatkoder for sortering.

### <a name="use-a-row-total-in-a-row-definition"></a>Bruke en radtotal i en raddefinisjon

Bruk en radtotalformel for å legge til eller trekke fra beløp i andre rader. En formel for å opprette en radtotal kan inneholde operatorene + og - for å kombinere enkeltradkoder og områder. Områder er angitt med et kolon (:). Formelen kan inneholde opptil 1 024 tegn. Her er et eksempel på en standard totalformelen: 400+420+430+450+460GJELD+EGENKAPITAL520:546520:546-GJELD

### <a name="components-of-a-row-total-formula"></a>Komponenter i en radsumformel

Når du oppretter en radtotalformel, må du bruke radkoder til å angi hvilke rader som leges til eller trekkes fra i gjeldende raddefinisjonen, og du må bruke operatorer for å angi hvordan rader kombineres. Totalrader og beløpsrader kan brukes i en hvilken som helst kombinasjon. **Obs!**  Alle totalrader som er i et område blir utelatt. Hvis du vil beregne en totalsum, kan du angi radområde. Hvis den første raden i et område er en totalrad, vil denne raden inkluderes i den nye totalen. Tabellen nedenfor beskriver hvordan operatorer brukes i radtotalformler.

| Operatør | Eksempelformel | beskrivelse                                                 |
|----------|-----------------|-------------------------------------------------------------|
| +        | 100+330         | Legger beløpet i rad 100 til beløpet i rad 330.        |
| :        | 100:330         | Legger sammen totalene for alle rader mellom rad 100 og rad 330.    |
| -        | 100-330         | Trekker beløpet i rad 100 fra beløpet i rad 330. |

### <a name="create-a-row-total"></a>Opprette en radsum

1.  Klikk **Raddefinisjoner** i Rapportutforming, og åpne deretter raddefinisjonen som skal endres.
2.  Dobbeltklikk **Formatkode**-cellen i raddefinisjonen, og velg **TOT**.
3.  I cellen **Relaterte formler/rader/enheter** skriver du inn totalformelen.

### <a name="relate-a-format-row-to-an-amount-row"></a>Knytte en formatrad til en beløpsrad

I **Formatkode**-kolonnen i en raddefinisjon, angir formatkodene **DES**, **LFT**, **RGT**, **CEN**, **---** og **===** formatering for nullbeløpsrader. Hvis du vil unngå at dette formatering blir skrevet ut når de tilknyttede beløpsradene skjules (for eksempel fordi beløpsradene inneholder nullverdier eller ingen periodeaktivitet), må du relatere formatradene til de tilsvarende beløpsradene. Denne funksjonen er nyttig når du vil hindre at overskrifter eller formatering som er knyttet til delsummer, blir skrevet ut når det ikke finnes detaljer å skrive ut for perioden. 
    > [!NOTE]
    >  You can also prevent the detailed amount rows from being printed by clearing the option to display rows without amounts. This option is located on the **Settings** tab of the report definition. By default, transaction detail accounts that have a zero balance or no period activity are suppressed in reports. To show these transaction detail accounts, select the **Display rows without an amounts** check box on the **Settings** tab of the report definition.

### <a name="relate-a-format-row-to-an-amount-row"></a>Knytte en formatrad til en beløpsrad

1.  I Rapportutforming klikker du **Raddefinisjoner**, og deretter velger du raddefinisjonen som skal endres.
2.  I formateringsraden i cellen **Relaterte formler/rader/enheter**, skriver du inn radkoden for beløpsraden som skal skjules. **Obs!**  Hvis du vil skjule en beløpsrad, må saldoen for raden være 0 (null). En beløpsrad som har en saldo som ikke er skjult.
3.  Klikk **Lagre** på **Fil**-menyen.

### <a name="example-of-preventing-printing-of-rows"></a>Eksempel på å hindre utskrift av rader

I eksemplet nedenfor vil Jenny hindre utskrift av overskriften og understrekinger i **Kontanter totalt** i rapporten, fordi det ikke var aktivitet i noen av kontantkontoene. I rad 220 (som formatkoden **---** angir, er en formateringsrad) i cellen **Relaterte formler/rader/enheter**, skriver hun derfor inn **250**, som er radkoden til beløpsraden hun vil skjule. [![RelatedRowsRowDefinition](./media/relatedrowsrowdefinition-1024x144.png)](./media/relatedrowsrowdefinition.png)

## <a name="select-the-base-row-for-a-column-calculation"></a>Velge basisraden for en kolonneberegning
I tilhørende rapportering tilordner du én eller flere basisrader i raddefinisjonen ved hjelp av formatkoden **CBR** (endre basisrad). En basisrad refereres deretter av en beregning i kolonnedefinisjonen. Her er noen vanlige eksempler CBR-beregninger:

-   Prosent av total omsetning som er knyttet til individuelle omsetningselementer
-   Prosent av totale utgifter som er knyttet til individuelle utgiftselementer
-   Prosent av bruttofortjeneste som er knyttet til divisjons- eller avdelingsdetaljer.

Én eller flere basisrader defineres i raddefinisjonen, og deretter bestemmer kolonnedefinisjonen relasjonene som basisraden rapporteres for. Koden som brukes i kolonneformelen er **BASEROW**. Følgende grunnleggende matematiske operasjoner brukes med **BASEROW**: divisjon, multiplikasjon, addisjon eller subtraksjon. Operasjonen som brukes oftest deles på **BASEROW**, der resultatet vises som en prosent. Kolonneberegninger som bruker **BASEROW** i formelen bruker raddefinisjonen for de relaterte basisradkodene. **CBR**-rader har følgende egenskaper:

-   **CBR**-rader skrives ikke ut på den fullførte rapporten.
-   **CBR**-formatkoden og den tilknyttede radkoden plasseres over raden eller inndelingen som viser tilknyttede beregninger.

I en kolonnedefinisjon indikerer kolonnetypen **BRGN** en kolonne som angir en formel i **Formel**-raden. Denne formelen brukes på dataene for denne kolonnen i rapporten, og bruker nøkkelordet Baserow for å basere beregninger på **CBR**-formatkodene i raden. I raddefinisjon definerer **CBR**-formatkode basisraden for kolonnene som beregner en prosentdel av eller multiplum av basisraden for hver rad i rapporten. Du kan ha flere **CBR**-formatkoder i et radformat, for eksempel én for nettosalg, én for bruttosalg og én for totale utgifter. Vanligvis brukes **CBR**-formatkoden til å opprette en prosent for kontoer som sammenlignes med en totallinjen. En basisrad brukes for alle beregninger til en annen basisrad er definert. Du må definere en **CBR**-formatkode for start og en **CBR**-formatkode for slutt. Hvis du for eksempel vil finne utgifter som en prosentandel av nettosalg, kan du dividere verdien i hver utgiftsrad med verdien i nettosalgraden. I dette tilfellet er nettosalgsraden basisraden. Du kan definere en kolonnedefinisjon som rapporterer gjeldende resultat og resultat hittil i år, sammen med en basisprosent for hvert resultat, som vist i eksemplet nedenfor. Start med et detaljert resultatregnskap.

### <a name="select-the-base-row-in-a-row-definition-for-a-column-calculation"></a>Velge basisraden i en raddefinisjon for en kolonneberegning

1.  I Rapportutforming klikker du **Kolonnedefinisjoner**, og deretter åpner du kolonnedefinisjonen for er resultatregnskap.
2.  Legg til en ny kolonne i kolonnedefinisjonen, og sett kolonnetypen til **CALC**.
3.  I **Formel**-cellen for den nye kolonnen skriver du inn formelen **X/BASEROW**, der **X** **FD**-kolonnetypen å se en prosent av.
4.  Dobbeltklikk cellen **Format/valutaoverstyring**.
5.  I dialogboksen **Overstyr format** i **Formatkategori**-listen, velger du **Prosent** og klikker deretter **OK**.
6.  På **Fil**-menyen klikker du **Lagre som** for å lagre kolonnedefinisjonen med et nytt navn. Legg til **CBR** i gjeldende filnavn (for eksempel **CUR\_YTD\_CBR**). Kolonnedefinisjonen er basisraddefinisjonen for kolonnen.
7.  I Rapportutforming klikker du **Raddefinisjoner**, og deretter åpner du raddefinisjonen som skal endres, ved å bruke basisradberegningen.
8.  Sette inn en ny rad over raden der basisradberegningen skal starte.
9.  Dobbeltklikk **Formatkode**-cellen i raddefinisjonen, og velg deretter **CBR**.
10. I cellen **Relaterte formler/rader/enheter** skriver du inn radkodenummer for basisraden.

### <a name="example-of-base-row-calculation"></a>Eksempel på basisradberegning

I følgende eksempel på en raddefinisjon viser rad 100 at basisraden for beregninger er rad 280. [![Eksempel på basisradberegning.](./media/cbrrowdefinition.png)](./media/cbrrowdefinition.png) I eksemplet nedenfor av en kolonnedefinisjon, bruker beregningene **CBR**-formatkoden. Beregningen i kolonne C dividerer verdien i kolonne B for rapporten med verdien i rad 280 i kolonne B. Formatoverstyringen i kolonne B skriver ut resultatet av beregningen i prosent. På samme måte er hver beløp i kolonne E i kolonne D som en prosentandel av nettosalg. [![Eksempel på kolonnedefinisjon.](./media/cbrcolumndefinition2.png)](./media/cbrcolumndefinition2.png) Eksemplet nedenfor viser en rapport som kan bli generert basert på de forrige beregningene. [![Eksempelrapport basert på tidligere eksempelberegninger.](./media/cbrreport-1024x272.png)](./media/cbrreport.png)

## <a name="select-a-sorting-code-for-a-row-definition"></a>Velge en sorteringskode for en raddefinisjon
Sorteringskoder sorterer kontoer eller verdier, sorterer en faktisk rapport eller avviksrapport for budsjett etter største avviket eller sorterer radbeskrivelsene alfabetisk. Følgende sorteringskoder er tilgjengelige:

-   **SORT** – Sorterer rapporten i stigende rekkefølge basert på verdiene i den angitte kolonnen.
-   **ASORT** – Sorterer rapporten i stigende rekkefølge basert på den absolutte verdien for verdiene i den angitte kolonnen. Symbolet for hver verdi ignoreres altså når verdiene sorteres. Denne formatkoden sorterer verdiene av størrelsen på avviket, uavhengig av om avviket er positivt eller negativt.
-   **SORTDESC** – Sorterer rapporten i synkende rekkefølge basert på verdiene i den angitte kolonnen.
-   **ASORTDESC** – Sorterer rapporten i synkende rekkefølge basert på den absolutte verdien for verdiene i den angitte kolonnen

### <a name="select-a-sorting-code"></a>Velge en sorteringskode

1.  I Rapportutforming klikker du **Raddefinisjoner**, og deretter åpner du raddefinisjonen som skal endres.
2.  Dobbeltklikk **Formatkode**-cellen, og velg deretter en sorteringskode.
3.  I cellen **Relaterte formler/rader/enheter** angir du området for radkodene som skal sorteres. Hvis du vil angi et område, angir du den første radkoden, et kolon (:) og den siste radkoden. Skriv for eksempel **160:490** for å angi at område er rad 160 til rad 490.
4.  I **Kolonnebegrensning**-cellen skriver du inn bokstaven på rapportkolonnen som skal brukes for sorteringen. 
    > [!NOTE]
    > Inkluder bare beløpsrader i en sorteringsberegning.

### <a name="examples-of-ascending-and-descending-column-values"></a>Eksempler på stigende og synkende kolonneverdier

I eksemplet nedenfor, vil verdiene i kolonne D for rapporten sorteres i stigende rekkefølge for radene 160 gjennom 490. I tillegg vil de absolutte verdiene i kolonne G for rapporten sorteres i synkende rekkefølge for radene 610 til 940.

| Radkode | Beskrivelse                                         | Formatkode | Relaterte formler/rader/enheter | Vanlig saldo | Kolonnebegrensning | Kobling til finansdimensjoner |
|----------|-----------------------------------------------------|-------------|-----------------------------|----------------|--------------------|------------------------------|
| 100      | Sortert etter månedlige avvik i stigende rekkefølge       | DES         |                             |                |                    |                              |
| 130      |                                                     | SORT        | 160:490                     |                | D                  |                              |
| 160      | Salg                                               |             |                             | C              |                    | 4100                         |
| 190      | Salgsreturer                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 490      | Renteinntekter                                     |             |                             | C              |                    | 7000                         |
| 520      |                                                     | DES         |                             |                |                    |                              |
| 550      | Sortert etter absolutt avvik hittil i år i synkende rekkefølge | DES         |                             |                |                    |                              |
| 580      |                                                     | ASORTDESC   | 610:940                     |                | G                  |                              |
| 610      | Salg                                               |             |                             | C              |                    | 4100                         |
| 640      | Salgsreturer                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 940      | Renteinntekter                                     |             |                             | C              |                    | 7000                         |

Her er et eksempel på rapporten som genereres.

|||||||||
|---|---|---|---|---|---|---|
|**Avviksanalyse (sortert etter avvik)**|||||||

|**Beijing- og Atlanta-området**|||||||

|**For de sju månedene som avsluttes 31. juli 2013**|||||||

||**Juli**|**Hittil i år**|||||

||**Faktisk**|**Budsjett**|**Avvik**|**Faktisk**|**Budsjett**|**Avvik**|

|**Sortert etter månedlige avvik i stigende rekkefølge**|||||||

|Vareforbruk|873 872|236 144|(637 728)|4 864 274|1 590 315|(3 273 959)|

Lønn|97 624|65 573|(32 051)|653 884|441 664|(212 220)| |Salgsrabatter|36 383|24 152|(12 231)|241 562|162 670|(78 892)| |Salgsreturer|10 917|7 246|(3 671)|62 809|48 803|(14 006)| |Leieutgifter|12 052|9 019|(3 033)|80 444|60 748|(19 696)| |Kontorutgifter|5 023|3 291|(1 732)|33 420|22 098|(11 322)| |Reiseutgifter|7 656|7 641|(15)|51 062|51 469|407| |Salg|1 240 119|410 389|829 730|7 139 288|2 764 549|4 374 739| |**Sortert etter absolutt avvik hittil i år i synkende rekkefølge**||||||| |Salg|1 240 119|410 389|829 730|7 139 288|2 764 549|4 374 739| |Reiseutgifter|7 656|7 641|(15)|51 062|51 469|407| |Kontorutgifter|5 023|3 291|(1 732)|33 420|22 098|(11 322)| |Salgsreturer|10 917|7 246|(3 671)|62 809|48 803|(14 006)| |Leieutgifter|12 052|9 019|(3 033)|80 444|60 748|(19 696)| |Salgsrabatter|36 383|24 152|(12 231)|241 562|162 670|(78 892)| |Lønn|97 624|65 573|(32 051)|653 884|441 664|(212 220)| |Vareforbruk|873 872|236 144|(637 728)|4 864 274|1 590 315|(3 273 959)|

## <a name="specify-a-format-override-cell"></a>Angi en celle for formatoverstyring
**Overstyr format**-cellen angir formateringen som brukes for raden når rapporten skrives ut. Denne formateringen overstyrer formateringen som er angitt i kolonnedefinisjonen og rapportdefinisjonen. Formateringen som er angitt i disse definisjonene er som standard valutaen. Hvis én rad av rapporten viser antall aktiva, for eksempel antall bygninger, og en annen rad viser pengeverdien for disse aktivaene, kan du overstyre valutaformateringen og angi numerisk formatering for raden som angir antall bygninger. Du kan angi denne informasjonen i dialogboksen **Overstyre format**. De tilgjengelige alternativene avhenger av formatkategorien du velger. **Eksempel**-området i dialogboksen viser eksempelformater. Følgende formatkategorier er tilgjengelige:

-   Valutaformatering
-   Numerisk formatering
-   Prosentformatering
-   Egendefinert formatering

### <a name="override-cell-formatting"></a>Overstyr celleformatering

1.  Åpne raddefinisjonen som skal endres i Rapportutforming.
2.  I raden som formatet skal overstyres for, dobbeltklikker du i cellen i **Overstyr format**-kolonnen.
3.  I dialogboksen **Overstyr format** velger du formateringsalternativet som skal brukes for denne raden i rapporten.
4.  Klikk **OK**.

### <a name="currency-formatting"></a>Valutaformatering

Valutaformatering gjelder for et regnskapsbeløp, og den inneholder valutasymbolet. Følgende alternativer er tilgjengelige:

-   **Valutasymbol** – Valutasymbolet for rapporten. Denne verdien overstyrer innstillingen **Regionale innstillinger** for firmainformasjonen.
-   **Negative tall** – Negative tall kan ha et minustegn (-), de kan vises i parentes eller de kan ha en trekant (∆).
-   **Desimaler** – Antall sifre som skal vises etter desimaltegnet.
-   **Tekst for nullverdioverstyring** – Teksten som skal inkluderes i rapporten når beløpet er 0 (null). Denne teksten vises som den siste linjen i **Eksempel**-området. 
    > [!NOTE]
    >  Hvis utskrift er skjult for nullverdier eller ingen periodeaktivitet, skjules denne teksten.

### <a name="numeric-formatting"></a>Numerisk formatering

Numerisk formatering gjelder for alle beløp, og den inneholder ikke valutasymbolet. Følgende alternativer er tilgjengelige:

-   **Negative tall** – Negative tall kan ha et minustegn (-), de kan vises i parentes eller de kan ha en trekant (∆).
-   **Desimaler** – Antall sifre som skal vises etter desimaltegnet.
-   **Tekst for nullverdioverstyring** – Teksten som skal inkluderes i rapporten når beløpet er 0 (null). Denne teksten vises som den siste linjen i **Eksempel**-området. 
    > [!NOTE]
    >  Hvis utskrift er skjult for nullverdier eller ingen periodeaktivitet, skjules denne teksten.

### <a name="percentage-formatting"></a>Prosentformatering

Prosentformatering inkluderer prosenttegnet (%). Følgende alternativer er tilgjengelige:

-   **Negative tall** – Negative tall kan ha et minustegn (-), de kan vises i parentes eller de kan ha en trekant (∆).
-   **Desimaler** – Antall sifre som skal vises etter desimaltegnet.
-   **Tekst for nullverdioverstyring** – Teksten som skal inkluderes i rapporten når beløpet er 0 (null). Denne teksten vises som den siste linjen i **Eksempel**-området. 
    > [!NOTE]
    >  Hvis utskrift er skjult for nullverdier eller ingen periodeaktivitet, skjules denne teksten.

### <a name="custom-formatting"></a>Egendefinert formatering

Bruk kategorien for egendefinert formatering for å opprette en egendefinert formatoverstyring. Følgende alternativer er tilgjengelige:

-   **Type** – Det tilpassede formatet.
-   **Tekst for nullverdioverstyring** – Teksten som skal inkluderes i rapporten når beløpet er 0 (null). Denne teksten vises som den siste linjen i **Eksempel**-området. 
    > [!NOTE]
    >  Hvis utskrift er skjult for nullverdier eller ingen periodeaktivitet, skjules denne teksten.

Typen skal representere den positive verdien og den negative verdien. Vanligvis angir du et lignende format som skiller positive og negative verdier. Hvis du vil for eksempel vil angi at både positive og negative verdier har to desimaler, men negative skal vises i parenteser, kan du skrive inn **0,00;(0,00)**. Tabellen nedenfor viser egendefinerte formater som du kan bruke til å styre formatet for verdier. Alle eksemplene start fra verdien 1234,56.

| Formater                         | Positiv   | Negativ     | Null    |
|--------------------------------|------------|--------------|---------|
| 0                              | 1235       | -1235        | 0       |
| 0;0                            | 1235       | 1235         | 0       |
| 0;(0);-                        | 1235       | 1235         | -       |
| \#,\#\#\#;(\#,\#\#\#);“”       | 1,235      | (1,235)      | (Tom) |
| \#,\#\#0,00;(\#,\#\#0,00);null | 1,234.56   | (1,234.56)   | null    |
| 0.00%;(0.00%)                  | 123456.00% | (123456.00%) | 0,00 %   |

## <a name="specify-a-normal-balance-cell"></a>Angi en Normal balanse-celle
Cellen **Normal balanse** i en raddefinisjon bestemmer fortegnet for beløpene i en rad. Hvis du vil snu fortegnet for en rad, eller hvis den normale saldoen for en konto er et kreditbeløp, kan du skrive inn en **C** i **Normal balanse**-cellen for denne raden. Rapportutformingen snur fortegnet for alle kreditbalansekontoer i denne raden. Når rapportutforming konverterer disse kontoene, fjernes debet/kreditegenskapen fra alle beløp, og gjør derfor summering enkel. Hvis du for eksempel vil beregne nettoinntekt, trekker du utgifter fra inntekt. Vanligvis påvirkes ikke totalrader og beregnede rader av en **C**-kode. **XCR**-uskriftskontrollen i kolonnedefinisjonen tilbakestiller imidlertid fortegnet for alle rader som inneholder en **C** i **Normal balanse**-kolonnen. Denne formateringen er spesielt viktig når du vil vise alle ugunstige avvik som negative beløp. Hvis en total eller beregnet beløp har feil fortegn, angir du en **C** i **Normal balanse**-cellen for raden å snu fortegnet.

## <a name="specify-a-row-modifier-cell"></a>Angi en celle for radmodifikator
Innholdet i **Radmodifikator**-cellen i en raddefinisjon, overstyrer regnskapsårene, periodene og annen informasjon som er angitt i kolonnedefinisjon for denne raden. Den valgte modifikatoren gjelder for alle kontoer i raden. Du kan endre hver rad ved hjelp av én eller flere av følgende typer modifikatorer:

-   Kontomodifikatorer
-   Registerkodemodifikatorer
-   Konto-og transaksjonsattributter

### <a name="override-a-column-definition"></a>Overstyre en kolonnedefinisjon

1.  Åpne raddefinisjonen som skal endres i Rapportutforming.
2.  I raden der du vil overstyre kolonnedefinisjonen, dobbeltklikker du **Radmodifikator**-cellen.
3.  I dialogboksen **Radmodifikator** velger du et alternativ i **Kontomodifikator**-feltet. Hvis du vil se en beskrivelse av alternativene, kan du se avsnittet "Kontomodifikatorer".
4.  I **Registerkodemodifikator**-feltet velger du registerkoden som skal brukes for raden.
5.  Under **Attributter** følger du denne fremgangsmåten for å legge til en oppføring for hver attributt som skal tas med i radkoden:
    1.  Dobbeltklikk **Attributt**-cellen, og velg et attributtnavn. **Advarsel!** Erstatt nummertegn (\#) med en numerisk verdi.
    2.  Dobbeltklikk **Fra**-cellen, og angi den første verdien for området.
    3.  Dobbeltklikk **Til**-cellen, og angi den siste verdien for området.

6.  Klikk **OK**.

### <a name="account-modifiers"></a>Kontomodifikatorer

Når du velger en bestemt konto, kombinerer rapportutforming vanligvis kontoen og regnskapsårene, periodene og annen informasjon du angir i kolonnedefinisjonen. Du kan bruke forskjellig informasjon, for eksempel forskjellige regnskapsperioder, for bestemte rader. Tabellen nedenfor viser kontomodifikatorene som er tilgjengelige. Erstatt nummertegnet (\#) med en verdi som er lik eller mindre enn antall perioder i regnskapsåret.

| Kontomodifikator | Hva skrives ut?                                                                           |
|------------------|-------------------------------------------------------------------------------------------|
| /BB              | Åpningssaldoen for en konto.                                                     |
| /\#              | Saldoen for en bestemt periode.                                                     |
| /-\#             | Saldoen for perioden som er \# perioder før gjeldende periode.                  |
| /+\#             | Saldoen for perioden som er \# perioder etter gjeldende periode.                   |
| /C               | Saldoen for gjeldende periode.                                                       |
| /C-\#            | Saldoen for perioden som er \# perioder før gjeldende periode.                  |
| /C+\#            | Saldoen for perioden som er \# perioder etter gjeldende periode.                   |
| /Y               | Saldoen hittil i år til gjeldende periode.                                      |
| /Y-\#            | Saldoen hittil i år til perioden som er \# perioder før gjeldende periode. |
| /Y+\#            | Saldoen hittil i år til perioden som er \# perioder etter gjeldende periode.  |

### <a name="book-code-modifiers"></a>Registerkodemodifikatorer

Du kan begrense en rad til en eksisterende registerkode. Kolonnedefinisjonen må inneholde minst én **FD**-kolonne som inneholder en registerkode. 
> [!NOTE]
> Registerkodebegrensningen for en rad overstyrer registerkodebegrensningene i kolonnedefinisjon for denne raden.

### <a name="account-and-transaction-attributes"></a>Konto- og transaksjonsattributter

Noen regnskapssystemer støtter kontoattributter og transaksjonsattributter i de økonomiske dataen. Disse attributtene fungerer som virtuelle kontosegmenter, og kan inneholde tilleggsinformasjon om konto eller transaksjon. Denne tilleggsinformasjonen kan være konto-ID-er, parti-ID-er, postnumre eller andre attributter. Hvis regnskapssystemet støtter attributter, kan du bruke kontoattributter eller transaksjonsattributter som radmodifikatorer i raddefinisjonen. Hvis du vil ha informasjon om hvordan du overstyrer radinformasjon, kan du se avsnittet "Overstyre en kolonnedefinisjon" tidligere i denne artikkelen.

## <a name="specify-a-link-to-financial-dimensions-cell"></a>Angi en celle for kobling til finansdimensjoner
Cellen **Kobling til finansdimensjoner** inneholder koblinger til de økonomiske dataene som skal tas med i hver rad i en rapport. Denne cellen inneholder dimensjonsverdier, men du kan angi celler i et Microsoft Excel-regneark i stedet for eller i tillegg til segmentverdiene eller dimensjonsverdier. Åpne dialogboksen **Dimensjoner**, og dobbeltklikk cellen **Kobling til finansdimensjoner**. 
> [!NOTE]
> Rapportutforming kan ikke velge kontoer, dimensjoner eller felt fra Microsoft Dynamics ERP-systemet som inneholder ett av følgende reserverte tegn: &, \*, \[, \], { eller }. Hvis du vil angi informasjon for en rad som allerede finnes i raddefinisjonen, kan du legge til informasjonen i cellen **Kobling til finansdimensjoner**. Hvis du vil legge til nye rader som er koblet til de økonomiske dataen, kan du bruke dialogboksen **Sett inn rader fra** for å opprette nye rader i rapportdefinisjonen. Kolonnetittelen endres, avhengig av hvordan kolonnen er konfigurert, som vist i tabellen nedenfor.

| Koblingstype som er valgt       | Beskrivelsen av koblingskolonnen endres til dette |
|----------------------------------|----------------------------------------------------|
| Finansdimensjoner             | Kobling til finansdimensjoner                       |
| Eksternt regneark               | Kobling til regneark                                  |
| Finansdimensjoner + regneark | Kobling til finansdimensjoner + regneark           |
| Management Reporter-rapport       | Management Reporter-rapport                         |

### <a name="specify-a-dimension-or-range"></a>Angi en dimensjon eller et område

1.  Åpne raddefinisjonen som skal endres, i Rapportutforming.
2.  Dobbeltklikk en celle i kolonnen **Kobling til finansdimensjoner**.
3.  Dobbeltklikk en celle under dimensjonsnavnet i dialogboksen **Dimensjoner**.
4.  I dialogboksen for dimensjonen velger du **Enkeltvis eller område**.
5.  I **Fra**-feltet angir du startdimensjonen eller klikker ![Bla gjennom](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "Bla gjennom") for å søke etter tilgjengelige dimensjoner. Hvis du vil angi et intervall av dimensjoner, kan du angi sluttdimensjonen i **Til**-feltet.
6.  Klikk **OK** for å lukke dialogboksen for dimensjonen. Dialogboksen **Dimensjoner** viser oppdatert dimensjon eller område.
7.  Klikk **OK** for å lukke dialogboksen **Dimensjoner**..

## <a name="display-zero-balance-accounts-in-a-row-definition"></a>Vise nullsaldokontoer i en raddefinisjon
Rapportutforming skriver som standard ikke ut rader som ikke har en tilsvarende saldo i de økonomiske dataen. Du kan derfor opprette én raddefinisjonen som inneholder alle naturlige segmentverdier eller alle dimensjonsverdier, og deretter bruke denne raddefinisjonen alle avdelingene.

### <a name="modify-zero-balance-settings"></a>Endre innstillinger for nullsaldo

1.  Åpne rapportdefinisjonen som skal endres i Rapportutforming.
2.  I kategorien **Innstillinger** under **Annen formatering**, velger du alternativer for raddefinisjonen som skal brukes i rapportdefinisjonen.
3.  Klikk **Lagre** på **Fil**-menyen for å lagre endringene.

## <a name="use-wildcard-characters-and-ranges-in-a-row-definition"></a>Bruke jokertegn og områder i en raddefinisjon
Når du angir en naturlige segmentverdi i dialogboksen **Dimensjoner**, kan du plassere et jokertegn (? eller \*) i en hvilken som helst posisjon i et segment. Rapportutformingen trekker ut alle verdiene for de definerte posisjonene uten å ta hensyn til jokertegnene. Raddefinisjonen inneholder bare for eksempel naturlige segmentverdier og naturlige segmenter har fire tegn. Ved å angi **6???** i en rad angir du at rapportutformningen skal å ta med alle kontoene som har en naturlig segmentverdien som begynner med en 6. Hvis du skriver inn **6\***, de samme resultater returneres, men resultatene inkluderer også verdier med variabel bredd , som **60** og **600000**. Rapportutforming erstatter hvert jokertegn (?) med et fullstendig utvalg av mulige verdier, blant annet bokstaver og spesialtegn. I området fra **12?0** til **12?4**, vil for eksempel jokertegnet i **12?0** erstattes med den laveste verdien i tegnsettet, og jokertegn i **12?4** erstattes med den høyeste verdien i tegnsettet. 
> [!NOTE]
> Du bør unngå å bruke jokertegn for start- og sluttkontoer i områder. Hvis du bruker jokertegn i startkontoen eller sluttkontoen, kan du få uventede resultater.

### <a name="single-segment-or-single-dimension-ranges"></a>Enkeltsegment- eller enkeltdimensjonsområder

Du kan angi en rekke segmentverdiene eller dimensjonsverdier. Fordelen med å angi et område er at du ikke trenger å oppdatere raddefinisjonen hver gang en ny verdi for segment- eller dimensjonsverdien legges til de økonomiske dataen. Området **+Konto=\[6100:6900\]** henter for eksempel verdiene fra kontoene 6100 til og med 6900 inn i radbeløpet. Når et område inneholder et jokertegn (?), evaluerer ikke rapportutforming området tegn for tegn. I stedet bestemmes den lave og høye enden av området, og deretter inkluderes sluttverdiene og alle verdier mellom dem. 
> [!NOTE]
> Rapportutforming kan ikke velge kontoer, dimensjoner eller felt fra Microsoft Dynamics ERP-systemet som inneholder ett av følgende reserverte tegn: &, \*, \[, \], { eller }. Du kan legge til et &-tegn bare når du bygger raddefinisjoner automatisk ved hjelp av dialogboksen **Sett inn rader fra dimensjoner**.

### <a name="multiple-segment-or-multiple-dimension-ranges"></a>Flersegments- eller fleredimensjonsområder

Når du angir et område ved hjelp av kombinasjoner av flere dimensjonsverdier, gjøres områdesammenligningen på en ..\financial-dimensions\dimension-by-dimension basis. Områdesammenligningen kan ikke utføres tegn for tegn eller for delsegment. Området **+Konto=\[5000:6000\], Avdeling=\[1000:2000\], Kostsenter=\[00\]** omfatter bare kontoer som samsvarer med hvert segment. I dette scenariet den første dimensjonen må være i området fra 5000 gjennom 6000, den andre dimensjonen må være i området fra 1000 til 2000, og den siste dimensjonen må være 00. For eksempel **+Konto=\[5100\], Avdeling=\[1100\], Kostsenter=\[01\]** er ikke inkludert i rapporten, fordi det siste segmentet er utenfor det angitte området. Hvis en segmentverdi inneholder mellomrom, setter du verdien i hakeparenteser (\[ \]). Følgende verdier er gyldige for et segment med fire tegn: **\[ 234\], \[123 \], \[1 34\]**. Dimensjonsverdier som skal stå i hakeparentes (\[ \]), og rapportutforming legger til disse parentesene for deg. Når et område med flere segmenter eller flere dimensjoner inneholder jokertegn (? eller \*), bestemmes den lave og høye enden av hele flersegmenters- eller flerdimensjonsområdet og deretter inkluderes sluttverdiene og alle verdier mellom dem. Hvis du har et stort område, for eksempel hele rekken med kontoene fra 40 000 til 99 999, må du angi en gyldig start- og sluttkonto når det er mulig. 
> [!NOTE]
> Rapportutforming kan ikke velge kontoer, dimensjoner eller felt fra Microsoft Dynamics ERP-systemet som inneholder ett av følgende reserverte tegn: &, \*, \[, \], { eller }. Du kan legge til et &-tegn bare når du bygger raddefinisjoner automatisk ved hjelp av dialogboksen **Sett inn rader fra dimensjoner**.

## <a name="add-or-subtract-from-other-accounts-in-a-row-definition"></a>Legge til eller trekke fra andre kontoer i en raddefinisjon
Hvis du vil legge til eller trekke fra pengebeløp i én konto fra pengebeløp i en annen konto, kan du bruke plusstegnet (+) og minustegnet (-) i cellen **Kobling til finansdimensjoner**. Tabellen nedenfor viser akseptable formater for å legge til og trekke fra koblinger til økonomiske data.

| Operasjon  | Bruk dette formatet  |
|------------|-----------------|
| Legg til to fullstendig kvalifiserte kontoer.                                                       | +Divisjon=\[000\], Konto=\[1205\], Avdeling=\[00\]+Divisjon=\[100\], Konto=\[1205\], Avdeling=\[00\] |
| Legg til to segmentverdier.                                                                 | +Konto=\[1205\]+Konto=\[1210\]                                                                           |
| Legg til segmenteverdier som inneholder jokertegn.                                    | +Konto=\[120?+Konto=\[11??\]                                                                             |
| Legg til et område med fullstendig kvalifiserte kontoer.                                                | +Divisjon=\[000:100\], Konto=\[1205\], Avdeling=\[00\]                                                   |
| Legg til et område med segmentverdier.                                                          | +Konto=\[1200:1205\]                                                                                       |
| Legg til et område med segmenteverdier som inneholder jokertegn.                         | +Konto=\[120?:130\]                                                                                       |
| Trekk én fullstendig kvalifisert konto fra en annen fullstendig kvalifisert konto.              | +Divisjon=\[000\], Konto=\[1205\], Avdeling=\[00\]-Divisjon=\[100\], Konto=\[1205\], Avdeling=\[00\] |
| Trekk én segmentverdi fra en annen segmentverdi.                                  | +Konto=\[1205\]-Konto=\[1210\]                                                                           |
| Trekk en segmentverdi som inneholder et jokertegn fra en annen segmentverdi. | +Konto=\[1200\]-Konto=\[11??\]                                                                           |
| Trekk fra et område med fullstendig kvalifiserte kontoer.                                           | -Divisjon=\[000:100\], Konto=\[1200:1205\], Avdeling=\[00:01\]                                           |
| Trekk fra et område med segmentverdier.                                                     | -Konto=\[1200:1205\]                                                                                       |
| Trekk fra et område med segmenteverdier som inneholder jokertegn.                    | -Konto=\[120?:130?\]                                                                                       |

Selv om du kan endre kontoene direkte, kan du også bruke dialogboksen **Dimensjoner** for å angi riktig formatering på koblingene for de økonomiske dataene. Alle verdiene kan inneholde jokertegn (? eller \*). Rapportutforming kan imidlertid ikke velge kontoer, dimensjoner eller felt fra Microsoft Dynamics ERP-systemet som inneholder ett av følgende reserverte tegn: &, \*, \[, \], { eller }. 
> [!NOTE]
> Hvis du vil trekke fra verdier, må du sette parenteser rundt verdiene. Hvis du for eksempel angir **450?-(4509)**, vises dette som **+Konto=\[4509\]-Konto=\[450?\]**, og du angir for rapportutforming å trekke beløpet for kontosegment 4509 fra beløpet for kontosegmenter som begynner med 450.

### <a name="add-or-subtract-accounts-from-other-accounts"></a>Legge til eller trekke fra kontoer fra andre kontoer

1.  Åpne raddefinisjonen som skal endres i Rapportutforming.
2.  Dobbeltklikk celle i kolonnen **Kobling til finansdimensjoner** i den aktuelle raden.
3.  I den første raden i dialogboksen **Dimensjoner**, følger du denne fremgangsmåten:
    1.  I det første feltet velger du alle dimensjoner (standard) eller klikker for å åpne dialogboksen **Behandle dimensjonssett**, der du kan opprette, endre, kopiere eller slette et sett.
    2.  Dobbeltklikk cellen **Operator +/-**, og velg pluss- (**+**) eller minusoperatoren (**-**) som gjelder for én eller flere dimensjonsverdier eller sett i raden.
    3.  I den aktuelle dimensjonsverdikolonnen dobbeltklikker du cellen for å åpne dialogboksen **Dimensjoner**, og velger om denne dimensjonsverdien gjelder enkeltvis eller for et område, et dimensjonsverdisettet eller totalkontoer. Hvis du vil se beskrivelse for feltene i dialogboksen **Dimensjoner**, kan du se avsnittet "Beskrivelse for dimensjonsdialogboksen".
    4.  Angi segmentverdier i **Fra**-kolonnen og **Til**-kolonnen.

4.  Gjenta trinn 2 til og med 3 hvis du vil legge til flere operasjoner.

> [!NOTE]
> Operatoren gjelder for alle dimensjoner i raden.

## <a name="description-of-the-dimensions-dialog-box"></a>Beskrivelse for dimensjonsdialogboksen
Tabellen nedenfor beskriver feltene i dialogboksen **Dimensjoner**.

| Vare                | Beskrivelse                                                                                                                                                                                                                                                                                             |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enkeltvis eller område | I **Fra**-feltet angir du navnet på en konto eller klikker **Bla gjennom**-knappen ![Bla gjennom](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "Bla gjennom") for å bla gjennom etter kontoen. Hvis du vil merke et område, kan du angi eller bla gjennom etter en verdi i **Til**-feltet.                                             |
| Dimensjonsverdisett | I **Navn**-feltet angir du navnet på et dimensjonsverdisett. Hvis du vil opprette, endre, kopiere, eller slette et sett, klikker du **Behandle dimensjonsverdisett**. **Formel**-feltet fylles ut med formelen fra cellen **Kobling til finansdimensjoner** for dette dimensjonsverdisettet i raddefinisjonen. |
| Totalkontoer   | I **Navn**-feltet angir eller blar du gjennom etter en dimensjon for totalkontoer. **Formel**-feltet fylles ut med formelen i cellen **Kobling til finansdimensjoner** for denne totalkontoen i rapportdefinisjonen.                                                                       |

## <a name="add-dimension-value-sets-in-a-row-definition"></a>Legge til dimensjonsverdisett i en raddefinisjon
Et dimensjonsverdisett er en navngitt gruppe med dimensjonsverdier. Et dimensjonsverdisettet kan inneholde verdier i bare én enkelt dimensjon, men du kan bruke et dimensjonsverdisett i flere raddefinisjoner, kolonnedefinisjoner, rapporteringstredefinisjoner og rapportdefinisjoner. Du kan også kombinere dimensjonsverdisett i en rapportdefinisjon. Når en endring i de økonomiske dataen krever at du endrer dimensjonsverdisettet, kan du oppdatere definisjonen for dimensjonsverdisettet, og denne oppdateringen gjelder for alle områder som bruker dimensjonsverdisettet. Hvis du for eksempel ofte viser et område med verdier som skal kobles til de økonomiske dataene, for eksempel verdiene fra 5 100 til 5 600, kan du tilordne dette området til et kontosett med navnet Salg. Når du har opprettet et sett med dimensjonsverdier, kan du velge dette settet som koblingen til finansdataene. Et annet eksempel: Hvis du har verdiområdet 5100 til 5600 tilordnet til Salg og 4175 tilordnet til Rabatter, kan du finne det totale salget ved å trekke Rabatter fra Salg. Denne operasjonen er angitt som **(5100:5600)-4175**.

### <a name="create-a-set-of-dimension-values"></a>Opprette er sett med dimensjonsverdier

1.  Åpne rad-, kolonne eller tredefinisjonen som skal endres i Rapportutforming.
2.  Klikk **Behandle dimensjonsverdisett** på **Rediger**-menyen.
3.  I dialogboksen **Behandle dimensjonsverdisett** i **Dimensjon**-feltet, velger du hvilken type dimensjonsverdisettet som skal opprettes, og deretter klikker du **Ny**.
4.  Skriv inn et navn og en beskrivelse for settet i dialogboksen **Ny**.
5.  Dobbeltklikk en celle i **Fra**-kolonnen.
6.  I dialogboksen **Konto** velger du kontonavnet i listen, eller søker etter posten i **Søk**-feltet. Klikk deretter **OK**.
7.  Gjenta trinn 5 til 6 i **Til**-kolonnen for å utforme en formel for denne operatoren.
8.  Når formelen er fullført, klikker du **OK**.
9.  Klikk **Lukk** i dialogboksen **Behandle dimensjonssett**.

### <a name="update-a-set-of-dimension-values"></a>Oppdatere et sett med dimensjonsverdier

1.  Åpne rad-, kolonne- eller tredefinisjonen som skal endres, i Rapportutforming.
2.  Klikk **Behandle dimensjonsverdisett** på **Rediger**-menyen.
3.  Velg dimensjonstype i dialogboksen **Behandle dimensjonsverdisett** i **Dimensjon**-feltet.
4.  Velg dimensjonsverdisettet i listen som skal oppdateres, og klikk deretter **Endre**.
5.  I dialogboksen **Endre** endrer du formelverdiene som skal inkluderes i settet. 
    > [!NOTE]
    >  Hvis du legger til nye kontoer eller dimensjoner, må du passe på at du endrer eksisterende dimensjonsverdisett til å ta med endringene.
6.  Dobbeltklikk cellen, og velg den aktuelle operatoren, **Fra**-konto og **Til**-konto.
7.  Klikk **OK** for å lukke dialogboksen **Endre** og lagre endringene.

### <a name="copy-a-dimension-set"></a>Kopiere et dimensjonssett

1.  Åpne rad-, kolonne eller tredefinisjonen som skal endres i Rapportutforming.
2.  Klikk **Behandle dimensjonsverdisett** på **Rediger**-menyen.
3.  Velg dimensjonstype i dialogboksen **Behandle dimensjonsverdisett** i **Dimensjon**-feltet.
4.  Velg settet som skal kopieres i listen, og klikk deretter **Lagre som**.
5.  Skriv inn et nytt navn på det kopierte settet, og klikk deretter **OK**.

### <a name="delete-a-dimension-set"></a>Slette et dimensjonssett

1.  Åpne rad-, kolonne- eller tredefinisjonen som skal endres, i Rapportutforming.
2.  Klikk **Behandle dimensjonsverdisett** på **Rediger**-menyen.
3.  Velg dimensjonstype i dialogboksen **Behandle dimensjonsverdisett** i **Dimensjon**-feltet.
4.  Velg settet som skal slettes, og klikk deretter **Slett**. Klikk **Ja** for å slette dimensjonsverdisettet permanent.


<a name="see-also"></a>Se også
--------

[Finansrapportering](financial-reporting-intro.md)





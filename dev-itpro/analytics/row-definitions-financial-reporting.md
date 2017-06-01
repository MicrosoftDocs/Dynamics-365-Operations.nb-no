---
title: Raddefinisjoner i Utforming av finansrapport
description: "En raddefinisjon er en rapportkomponent eller byggeblokk som angir innholdet i hver rad i finansrapport. En raddefinisjon kan kombineres med kolonnedefinisjoner, definisjoner av rapporttre og rapportdefinisjoner for å opprette en blokkgruppe som kan brukes av flere firmaer."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter, Core
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: cf0886725e2d8d4031e19810e75755f4306b7c49
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="row-definitions-in-financial-report-designer"></a>Raddefinisjoner i Utforming av finansrapport

[!include[banner](../includes/banner.md)]


En raddefinisjon er en rapportkomponent eller byggeblokk som angir innholdet i hver rad i finansrapport. En raddefinisjon kan kombineres med kolonnedefinisjoner, definisjoner av rapporttre og rapportdefinisjoner for å opprette en blokkgruppe som kan brukes av flere firmaer.

<a name="create-a-row-definition"></a>Opprett en raddefinisjon
-----------------------

1.  I navigasjonsruten i Rapportutforming klikker du **Raddefinisjoner**.
2.  Klikk **Ny** på **Fil**-menyen, og klikk deretter **Raddefinisjon**. Hvis du vil ha mer informasjon om innholdet i hver celle, kan du se [Endre celler for raddefinisjon](modify-row-definition-cells-financial-reporting.md).

## <a name="open-a-row-definition"></a>Åpne en raddefinisjon
1.  I navigasjonsruten i Rapportutforming klikker du **Raddefinisjoner**.
2.  Dobbeltklikk navnet på raddefinisjonen du vil åpne.
3.  Hvis du vil vise alle byggeblokker som er knyttet til raddefinisjonen, høyreklikker du raddefinisjonen og velger deretter **Tilknytninger**.

## <a name="contents-of-a-row-definition"></a> Innholdet i en raddefinisjon
En raddefinisjon kan inneholde opptil 20 000 finansdimensjonsrader og kan inneholder følgende informasjon:

-   Beskrivende tekst som gir mening i rapporten ved å opprette inndelingsoverskrifter, linjer og mellomrom, for eksempel **Kontanter** eller **Totalomsetning**
-   Koblinger til økonomiske data, som kan inneholde dimensjonsverdier i Microsoft Dynamics 365 for Operations. **Obs!** Du kan definere en raddefinisjon for å hente ut data fra finansdimensjonssystemet hver gang rapporten blir generert.
-   Totaler og formler for rader som er basert på de økonomiske dataen som er koblet

Hver rad i en raddefinisjon inneholder vanligvis én av følgende typer informasjon:

-   Referanser til finansdimensjonssystemet
-   Totaler eller beregninger som er basert på dataene
-   Formatering

Det finnes to metoder for å skrive inn informasjon i en raddefinisjon:

-   Angi radinformasjon manuelt i en ny raddefinisjon. Hvis du vil ha mer informasjon, kan du se [Endre celler for raddefinisjon](modify-row-definition-cells-financial-reporting.md).
-   Bruk rapportutforming til å hente radinformasjon direkte fra finansdimensjonene. Hvis du vil ha mer informasjon, kan du se delen Relaterte formler/rader/enheter i [Endre celler for raddefinisjon](modify-row-definition-cells-financial-reporting.md).

## <a name="add-dimensions-in-a-row-definition"></a> Legge til dimensjoner i en raddefinisjon
En dimensjon er en overlapping av data og verdier. Du kan gruppere data og verdier i rapportutforming. Du kan deretter klassifisere og analysere transaksjoner mer detaljert. Du kan bruke dialogboksen **Sett inn rader fra dimensjoner** for å legge til flere rader i en raddefinisjon samtidig. Dialogboksen viser én kolonne for hver dimensjon. Tabellen nedenfor beskriver informasjonen du kan angi i hver dimensjon.

| Alternativ                | Beskrivelse                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dimensjon             | Mønsteret som identifiserer dimensjonen som skal legges til raddefinisjonen. Dette mønsteret inneholder ett &-tegn eller nummertegn (\#) for hver posisjon i dimensjonene. Bruk vanligvis bare &-tegn for hovedkontodimensjonen og bare nummertegn (#) for andre dimensjoner. |
| Start på dimensjonsområde | Den første verdien for denne dimensjonen som skal legges til raddefinisjonen.                                                                                                                                                                                                                 |
| Slutt på dimensjonsområde   | Den siste verdien for denne dimensjonen som skal legges til raddefinisjonen.                                                                                                                                                                                                                  |

Følg fremgangsmåten nedenfor for å legge til dimensjoner i en raddefinisjon.

1.  I Rapportutforming klikker du **Raddefinisjoner**, og deretter åpner du raddefinisjonen som skal endres.
2.  På **Rediger**-menyen klikker du **Sett inn rader fra dimensjoner**.
3.  I dialogboksen **Sett inn rader fra dimensjoner**, i **Dimensjoner**-raden, velger du cellen for dimensjonen som skal overføres til raddefinisjonen, og deretter klikker du **Bare &&&**.
4.  Hvis du vil begrense raddefinisjonen for et bestemt områder dimensjonsverdier, angir du startverdien for dimensjonen i cellen **Start på dimensjonsområde**, og deretter angir du sluttverdien for dimensjonen i cellen **Slutt på dimensjonsområde**. Hvis du vil ta med alle verdier for den valgte dimensjonen, lar du disse cellene være tomme. **Obs!** Jokertegn (\* eller?) i dimensjonsområder kan ikke returnere alle resultatene som du vil ha, avhengig av hvordan ERP-databasen sorterer data.
5.  I feltet **Kode for startrad** angir du radkoden for den første dimensjonsverdien som skal legges til raddefinisjonen.
6.  I feltet **Øk hver rad med** angir du avstanden mellom etterfølgende radkoder. Hvis den første radkoden for eksempel er 100 og økningsverdien er 30, har de første nye radene kodene 100, 130, 160, 190 og 220. Bruk en inkrementell verdi som gir nok plass til å sette inn nye format- og formelrader.
7.  Klikk **OK**. Én linje for hver valgte dimensjonsverdi legges til raddefinisjonen.

## <a name="adjust-rounding-in-a-row-definition"></a> Justere avrunding i en raddefinisjon
Hvis du har en balanse der beløpene er avrundet, kan det hende totalene ikke er i balanse. Dette problemet kan oppstå hvis du for eksempel bruker alternativet for avrunding på en balanserapport og rapportdefinisjonen også angir avrunding. Du kan bruke alternativet **Avrundingsjustering** i raddefinisjonen for å balansere beløpene i balansen. Du kan deaktivere eller endre avrunding i kategorien **Innstillinger** i rapportdefinisjonen. Tabellen nedenfor viser hvordan beløp avrundes. I denne tabellen er totalene forskjellige for rad 100 og 200 når avrunding er aktivert.

| Radkode | Beløp uten avrunding | Beløp med avrunde til hele tusener |
|----------|--------------------------|-----------------------------------------|
| 100      | 3,600                    | 4                                       |
| 200      | 3,700                    | 4                                       |
| Sum    | 7,300                    | 8                                       |

Følg fremgangsmåten nedenfor hvis du vil justere avrunding i en balanse.

1.  I Rapportutforming klikker du **Raddefinisjoner**, og deretter åpner du raddefinisjonen som skal endres.
2.  På **Rediger**-menyen klikker du **Avrundingsjustering**.
3.  Skriv inn følgende verdier i dialogboksen **Avrundingsjusteringer**:
    -   **Raden Avrundingsjustering** – Radkoden for raden som skal justeres for å balansere balansen.
    -   **Raden Sum aktiva** – Radkoden for raden i balansen som inneholder de samlede aktivaene.
    -   **Raden Samlet gjeld og egenkapital** – Radkoden for raden i balansen som inneholder samlet gjeld og egenkapital.
    -   **Grense for justeringsbeløp** – Et positivt heltall som angir grensen for automatiske justeringer. Dette beløpe blir sammenlignet med den absolutte verdien av den faktiske avrundingsdifferansen.

    **Obs!** Disse radkodene må være koblet til de økonomiske dataen. Raden må med andre ord ha en dimensjonsverdi i cellen **Kobling til finansdimensjoner**. **Ikke** refererer til raden for beskrivelse (**DESC**), beregnet (**CALC**) eller summert (**TOT**).

Beløpene i balansen vil nå være i balanse når avrunding er aktivert. **Obs!** Grensen for justering brukes basert på alternativet **Avrundingspresisjon**, som er angitt for rapportdefinisjonen. Hvis du for eksempel velger å runde av rapporten til tusener og angi **2** i feltet **Grense for justeringsbeløp**, vises en advarsel når verdien som identifiseres i feltet **Raden Avrundingsjustering**, økes eller reduseres med mer enn 2 000.

## <a name="format-row-and-column-text"></a>Formatere rad- og kolonnetekst
Du kan tilpasse utseendet på rapportene ved å endre skrifter og formatere tekst. Avsnittene nedenfor beskriver hvordan du kan formatere utseendet på rader og kolonner i rapporter.

### <a name="manage-font-styles"></a>Behandle skriftstiler

Du kan opprette og endre skriftstiler for rapporten. Du kan deretter bruke disse stilene i dokumentet, eller på en bestemt rad eller kolonne i en rapport.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Opprette en skriftstil</td>
<td><ol>
<li>På <strong>Format</strong>-menyen i Rapportutforming klikker du <strong>Stiler og formatering</strong>.</li>
<li>Klikk <strong>Ny</strong> i dialogboksen <strong>Stiler og formatering</strong>, og skriv deretter inn et unikt navn for den nye stilen.</li>
<li>Velg skriftene du vil bruke, og klikk deretter <strong>OK</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Endre en skriftstil</td>
<td><ol>
<li>På <strong>Format</strong>-menyen i Rapportutforming klikker du <strong>Stiler og formatering</strong>.</li>
<li>Velg en stil å endre i dialogboksen <strong>Stiler og formatering</strong>, og klikk deretter <strong>Endre</strong>.</li>
<li>Velg skriftene du vil bruke, og klikk deretter <strong>OK</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Bruke en skriftstil</td>
<td><ol>
<li>I en definisjon eller kolonnedefinisjon, eller i topptekst og bunntekst, velger du én eller flere celler i Rapportutforming.</li>
<li>Velg en skriftstil i <strong>Stil</strong>-listen.</li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>Formatere radtekst

Formateringen som er angitt i raddefinisjonen, overstyrer all formatering som er angitt i kolonnedefinisjonen og rapportdefinisjonen. Du kan endre tekstformatet ved hjelp av kontrollene på formateringsverktøylinjen. Disse kontrollene er standardkontroller for Microsoft Windows.

1.  Åpne raddefinisjonen som skal endres i Rapportutforming.
2.  Velg cellene som skal formateres. Hvis du vil velge flere celler, holder du nede CTRL-tasten når du velger cellen.
3.  Klikk verktøylinjeknappen for formatet som skal brukes. Hvis du for eksempel vil rykke inn en rad, velger du raden og klikk deretter på **Øk innrykk** ![Øk innrykk](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Øk innrykk") på verktøylinjen.

### <a name="adjust-columns-while-you-design-reports"></a>Justere kolonner mens du utformer rapporter

Hvis du vil gjøre det enklere å vise kolonnene som du arbeider med i raddefinisjonen, kan du justere bredden på en kolonne og skjul (minimere) eller vise kolonner i visningsruten. Endringene du gjør, påvirker bare utseendet til kolonnene på skjermen. De påvirker ikke kolonneformatering i rapporter.

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>Endre bredden på en kolonne i visningruten

1.  Åpne raddefinisjonen som skal endres i Rapportutforming.
2.  Velg **Kolonnebredde** på **Format**-menyen.
3.  Angi en verdi, og klikk deretter **OK** i dialogboksen **Kolonnebredde**. Du kan også dra den høyre kanten av en kolonneoverskriftscelle for å endre bredden på kolonnen.

### <a name="hide-columns-in-the-view-pane"></a>Skjule kolonner i visningsruten

1.  Åpne raddefinisjonen som skal endres i Rapportutforming.
2.  Velg kolonnen eller kolonnene du vil minimere.
3.  Høyreklikk og klikk deretter **Skjul**.

### <a name="show-all-hidden-columns-in-the-view-pane"></a>Vise alle skjulte kolonner i visningsruten

1.  Åpne raddefinisjonen som skal endres i Rapportutforming.
2.  Høyreklikk den minimerte kolonnen som skal vises, og klikk deretter **Vis**.


<a name="see-also"></a>Se også
--------

[Finansrapportering](financial-reporting-intro.md)





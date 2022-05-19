---
title: Ny tildeling av inntektsføring
description: Dette emnet gir informasjon om ny tildeling, noe som gjør det mulig for organisasjoner å beregne inntektspriser på nytt når betingelsene for et kontraktsmessig salg endres. Emnet inneholder koblinger til andre emner som beskriver hvordan du fører inntekt i flere scenarioer.
author: kweekley
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7528202ed140dc2c0a7fc8c595178f155c3c1f75
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726134"
---
# <a name="revenue-recognition-reallocation"></a>Ny tildeling av inntektsføring

[!include [banner](../includes/banner.md)]

Ny tildeling gjør det mulig for organisasjoner å beregne inntektspriser på nytt når betingelsene for et kontraktsmessig salg endres. Når det gjelder inntektsføring, anses salgsordredokumentene som kontrakten.

Organisasjonen må selv bestemme om det kreves ny tildeling. Det kan hende at tillegget av en ny linje i en salgsordre, eller at en ny salgsordre for en kunde er tilføyd, ikke utgjør en endring i kontrakten. Følgende scenarioer kan kreve ny tildeling:

- En kunde som legger til varer i en salgsordre, eller fjernet varer fra salgsordren, etter at ordren ble fullstendig eller delvis fakturert.
- Flere salgsordrer, enten i bekreftet eller fakturert stat, ble angitt for den samme forhandlede kontrakten.
- En kunde returnerte eller mottok kreditt for en vare etter at den opprinnelige salgsordren ble fullstendig eller delvis fakturert.

Det er noen viktige begrensninger på prosessen for ny tildeling:

- Prosessen kan bare kjøres én gang. Det er derfor viktig at du kjører den først når alle endringene er ferdigstilt.

    - Denne begrensningen fjernes i versjon 10.0.17 og senere.

- Prosessen kan ikke kjøres på prosjektsalgsordrer.

    - Denne begrensningen fjernes i versjon 10.0.17 og senere.

- Hvis det gjelder flere salgsordrer, må de være for samme kundekonto.
- Alle salgsordrer som er tildelt på nytt, må ha samme transaksjonsvaluta.
- Prosessen kan ikke tilbakeføres eller angres etter at den er kjørt.

    - Denne begrensningen fjernes i versjon 10.0.17 og senere.

- Tildeling på nytt kan bare utføres for enten salgsordrer eller prosjektsalgsordrer. Det kan ikke gjøres for en kombinasjon av salgsordrer og prosjektsalgsordrer.

    - Denne begrensningen fjernes i versjon 10.0.17 og senere.

## <a name="set-up-reallocation"></a>Oppsett av ny tildeling

Én parameter påvirker prosessen for ny tildeling.

Ettersom ny tildeling kan utføres på en salgsordre som er delvis eller fullstendig fakturert, må alle tidligere regnskapsoppføringer for fakturaen rettes opp ved hjelp av de nye inntektsprisene som er tildelt på nytt. Denne rettelsen gjøres ved å tilbakeføre den opprinnelige fakturaens regnskapsoppføring og postere en ny regnskapsoppføring som er basert på inntektsprisene som er omforhandlet.

Hver organisasjon må bestemme om rettelsen bare skal oppdateres i økonomimodulen, eller om den også skal oppdatere Kunder. Beslutningen som tas, fastslår den forskriftsmessige innstillingen for alternativet **Poster fakturakorrigeringer til Kunder** på fanen **Inntektsføring** på siden **Parametere for økonomimodul** (**Inntektsføring \> Oppsett \> Parametere for økonomimodul**). Innstillingen som velges, avhenger av det bestemte scenarioet. Hvis du vil ha mer informasjon om mulige scenarioer, kan du bruke koblingene i [Scenarioer for ny tildeling](#scenarios-for-reallocation) senere i dette emnet.

[![Fanen Inntektsføring på siden Parametere for økonomimodul.](./media/01_RevRecScenarios.png)](./media/01_RevRecScenarios.png)

Hvis alternativet **Poster fakturakorrigeringer til Kunder** er satt til **Ja**, gir prosessen for ny tildeling følgende resultat:

- Et kredittdokument opprettes i Kunder for å tilbakeføre fakturaen som krever rettelse.

    - Kredittdokumentet bruker det opprinnelige fakturanummeret på nytt, men "-1" føyes til.
    - Kredittdokumentet utlignes automatisk mot den opprinnelige fakturaen. Hvis den opprinnelige fakturaen allerede er utlignet med et annet kreditdokument eller en annen betaling, tilbakeføres denne utligningen automatisk.
    - Kredittdokumentet posteres til økonomimodulen for å tilbakeføre regnskapsoppføringen som ble postert på den opprinnelige fakturaen. Oppføringer i transaksjonen Lager og Solgte varers kost (COGS) tilbakeføres imidlertid ikke.

- En ny faktura som er basert på de nye prisbeløpene som er tildelt på nytt, opprettes i Kunder.

    - Den nye fakturaen bruker det opprinnelige fakturanummeret på nytt, men "-2" føyes til.
    - Den nye fakturaen utlignes automatisk mot eventuelle kredittdokumenter eller betalinger som tidligere er utlignet mot den opprinnelige fakturaen.
    - Den nye fakturaen posteres til økonomimodulen ved hjelp av de nye inntektsprisbeløpene som er tildelt på nytt. Fakturaen vil ikke bli postert i kontoene Lager og Solgte varers kost igjen, ettersom disse oppføringene vedlikeholdes på den opprinnelige fakturaens regnskapsoppføring.

Hvis alternativet **Poster fakturakorrigeringer til Kunder** er satt til **Nei**, gir prosessen for ny tildeling følgende resultat:

- En tilbakeføringsregnskapsoppføring posteres bare til økonomimodulen. All regnskapsføring fra den opprinnelige fakturaen tilbakeføres, bortsett fra oppføringer for kontoen Lager og Solgte varers kost.
- En ny regnskapsoppføring posteres bare til økonomimodulen, basert på de nye inntektsprisene som er tildelt på nytt. Fakturaen vil ikke bli postert i kontoene Lager og Solgte varers kost igjen, ettersom disse oppføringene vedlikeholdes på den opprinnelige fakturaens regnskapsoppføring.
- Fakturaen på siden **Kundetransaksjoner** påvirkes eller endres ikke, men gjenspeiler likevel den opprinnelige regnskapsoppføringen. Det er ingen referanse til tilbakeførings- eller nye regnskapsoppføringer.

Som nevnt kan du bare oppdatere økonomimodulen, eller du kan oppdatere både Økonomimodul og Kunder. Begge metodene har fordeler og ulemper. Det anbefales at du evaluerer organisasjonens krav for å bestemme hvilket alternativ du skal bruke. Hvis du oppdaterer både Økonomimodul og Kunder, vises de riktige regnskapsoppføringene på den nye fakturaen, og de kan vises fra dokumentet på siden **Kundetransaksjoner**. I tillegg vil utligningsprosessen bruke de oppdaterte regnskapsoppføringene til å postere kontantrabatter og forsterkninger eller tap. På den annen side vises kredittdokumentet og den nye fakturaen på kundeutdrag og aldersfordelingsrapporter, på samme måte som andre kredittdokumenter og kundefakturaer. Beskrivelsen av disse dokumentene viser at de ble opprettet ved hjelp av en regnskapsrettelse.

## <a name="run-the-reallocation-process"></a>Kjøre prosessen for ny tildeling

Hvis du vil starte prosessen for ny tildeling, velger du **Tildeling av pris på nytt med nye ordrelinjer** i en salgsordre som du må tildele på nytt. Du kan eventuelt gå til **Inntektsføring \> Periodiske oppgaver \> Tildel pris på nytt med nye ordrelinjer**, og deretter angir du de riktige filtrene, for eksempel kundekontoen.

[![Siden Tildel pris på nytt med nye ordrelinjer.](./media/02_RevRecScenarios.png)](./media/02_RevRecScenarios.png)

Det øvre rutenettet på siden **Tildel pris på nytt med nye ordrelinjer** kalles **Salg**. Det viser en liste over salgsordrene for kunden. Velg salgsordrene som må tildeles på nytt. Hvis en salgsordre har en ID for ny tildeling, er den allerede merket for ny tildeling av en annen bruker. Hvis én eller flere salgsordrer tidligere ble tildelt på nytt, og må inkluderes i en annen ny tildeling, må du først angre den nye tildelingen av disse salgsordrene. Deretter kan den tas med i en ny tildeling. Hvis du vil ha mer informasjon, kan du se delene [Angre en ny tildeling](#undo-a-reallocation) og [Ny tildeling flere ganger](#reallocate-multiple-times) senere i dette emnet.

Det nederste rutenettet på siden kalles **Linjer**. Når du har valgt én eller flere salgsordrer i rutenettet **Salg**, viser rutenettet **Linjer** salgsordrelinjene. Velg salgsordrelinjene som må tildeles på nytt. Hvis du bare har valgt én salgsordre, må linjer i den samme salgsordren tildeles på nytt. Denne situasjonen kan oppstå når en av salgsordrelinjene tidligere er fakturert, og deretter ble en ny linje lagt til, eller en eksisterende linje ble fjernet eller avbrutt. Hvis en linje er fjernet, vises den ikke i rutenettet. Derfor kan den ikke velges. Den vil imidlertid fortsatt bli tatt hensyn til når prosessen for ny tildeling kjøres.

Når du er ferdig med å velge de nødvendige salgsordrelinjene, bruker du knappene i handlingsruten, som beskrevet her:

- **Oppdater ny tildeling** – Beregn de nye inntektsprisbeløpene for de valgte salgsordrelinjene. Hvis en linje blir fjernet eller avbrutt, blir den nye tildelingen bare utført for de eksisterende linjene du har valgt. Illustrasjonen nedenfor viser et eksempel på salgsordrelinjer før ny tildeling oppdateres.

    [![Salgsordrelinjer før ny tildeling oppdateres.](./media/03_RevRecScenarios.png)](./media/03_RevRecScenarios.png)

    De nye inntektsprisbeløpene vises i kolonnen **Beløp tildelt på nytt** i rutenettet **Linjer**. På dette tidspunktet er den nye tildelingen behandlet, men den er ennå ikke beregnet. Illustrasjonen nedenfor viser et eksempel på salgsordrelinjer etter at den nye tildelingen er oppdatert.

    [![Salgsordrelinjer etter at den nye tildelingen er oppdatert.](./media/04_RevRecScenarios.png)](./media/04_RevRecScenarios.png)

- **Behandle** – Behandle eller poster inntektspriser på nytt. Etter at du har valgt denne knappen, er det ingen måte å tilbakeføre den nye tildelingen på. Hvis du ikke valgte **Oppdater ny tildeling** før du velger **Behandle**, blir den nye tildelingen kjørt automatisk.

    - Hvis ingen salgsordrelinjer er fakturert, oppdateres inntektsprisbeløpene på alle salgsordrer som er valgt for ny tildeling.
    - Hvis én eller flere salgsordrelinjer er fakturert, posteres korrigeringen av regnskapsoppføringene, og eventuelle inntektsplandetaljer som ble opprettet for den fakturerte salgsordrelinjen, blir rettet opp.

- **Forventet bilag** – Vis en forhåndsvisning av regnskapsoppføringene som er opprettet for alle salgsordrelinjer som er fakturert. Hvis ingen linjer er fakturert, vises ingenting. Hvis du ikke valgte **Oppdater ny tildeling** før du velger **Forventet bilag**, blir den nye tildelingen kjørt automatisk.
- **Ny tildeling for inntekt** – Åpne en side som viser inntektsspristildelingen for alle de valgte linjene. Du kan ikke endre informasjonen på siden. Siden viser linjebeløpene som ble brukt til å utføre den nye tildelingen.

    [![Linjebeløp som ble brukt for ny tildeling.](./media/05_RevRecScenarios.png)](./media/05_RevRecScenarios.png)

- **Tilbakestill data for valgt kunde** – Hvis prosessen for ny tildeling ble startet, men du ikke har fullført prosessen, fjerner du dataene i tabellen for ny tildeling for den valgte kunden. Hvis du for eksempel merker flere salgsordrelinjer for ny tildeling, lar du siden være åpen uten å velge **Behandle**, og deretter blir siden tidsavbrutt. I dette tilfellet vil salgsordrelinjene forbli markert, og de vil ikke være tilgjengelige før en annen bruker kan fullføre prosessen for ny tildeling. Siden kan til og med være tom når den åpnes. I slike situasjoner kan knappen **Tilbakestill data for valgt kunde** brukes til å fjerne ubehandlede salgsordrer, slik at en annen bruker kan fullføre prosessen for ny tildeling.

## <a name="undo-a-reallocation"></a>Angre en ny tildeling

Du angrer en ny tildeling ved å kjøre en annen ny tildeling. Ny tildeling blir utført på nytt, og brukeren velger ulike salgsordrelinjer som skal tas med i den andre tildelingsprosessen.

Hvis en ny tildeling blir utført på tvers av to eller flere atskilte salgsordrer, kan den omgjøres ved å velge **Tildel pris på nytt med nye ordrelinjer** fra en hvilken som helst salgsordre som er inkludert i den nye tildelingen. Du kan ikke gå til **Inntektsføring \> Periodiske oppgaver \> Tildel pris på nytt med nye ordrelinjer** for å angre den nye tildelingen, ettersom siden som åpnes på denne måten, viser bare salgsordrer som ikke har noen ID for ny tildeling. ID-en for ny tildeling tilordnes etter at dokumentet er tildelt på nytt.

Fjern merket for alle salgsordrer som skal utelates fra kontraktsavtalen, på siden **Ny tildeling av pris med nye ordrelinjer**. Bruk de aktuelle knappene i handlingsruten, for eksempel **Oppdater ny tildeling** og **Prosess** til å behandle den nye tildelingen. Hvis alle salgsordrer, bortsett fra den aktive salgsordren, ikke er merket, fjernes ID-en for ny tildeling når endringen behandles.

Hvis en ny tildeling er utført ved å legge til en ny linje i en fullstendig eller delvis fakturert salgsordre, kan du bare omgjøre den nye tildelingen ved å fjerne denne linjen fra salgsordren, og deretter kjøre ny tildeling på nytt. Salgsordrelinjen må fjernes, fordi alle linjer i en salgsordre antas å være del av den samme kontrakten. Du kan ikke fjerne merket for en salgsordrelinje når du er på siden **Tildel pris på nytt med nye ordrelinjer**.

## <a name="reallocate-multiple-times"></a>Tildel på nytt flere ganger

Du kan gjøre flere nye tildelinger mot den samme salgsordren hvis det er gjort flere endringer i kontrakten. Hver nye tildeling utløser tilordningen av en ID for ny tildeling til salgsordren eller gruppen av salgsordrer, for å gruppere endringene. Hvis flere nye tildelinger er utført, bruker hver nye tildeling samme ID for ny tildeling som den første nye tildelingen.

Salgsordre 00045 registreres for eksempel, og har flere linjer. Når salgsordren er ferdigfakturert, legges det til en ny salgsordrelinje. Den nye tildelingen kjøres deretter ved å åpne siden **Tildel pris på nytt med nye ordrelinjer** fra salgsordre 00045 eller ved å gå til **Inntektsføring \> Periodiske oppgaver \> Tildel pris på nytt med nye ordrelinjer**. ID-en for ny tildeling, **Reall000001**, blir tilordnet til salgsordren.

En sekundær salgsordre, 00052, blir opprettet for den samme kontrakten. Du kan kjøre den nye tildelingen en gang til ved å åpne siden **Tildel pris på nytt med nye ordrelinjer** fra salgsordre 00045, men ikke fra salgsordre 00052. Hvis du åpner siden **Tildel pris på nytt med nye ordrelinjer** fra salgsordre 00052, vil ikke salgsordre 00045 vises, fordi en ID for ny tildeling er tilordnet til den. Siden viser bare salgsordrer som ikke har noen ID for ny tildeling.

Det er to måter å gjøre den andre nye tildelingen på. Du kan angre den nye tildelingen av salgsordre 00045. I dette tilfellet fjernes ID-en for ny plassering, og du kan deretter flytte på nytt fra salgsordre 00045 eller salgsordre 00052. Du kan eventuelt åpne siden **Tildel pris på nytt med nye ordrelinjer** fra salgsordre 00045 og legge til den andre salgsordren. Når tildelingen på nytt blir behandlet, blir ID-en **Reall000001** for ny tildeling tilordnet til både salgsordre 00045 og salgsordre 00052.

## <a name="scenarios-for-reallocation"></a>Scenarioer for ny tildeling

Følgende emner går gjennom ulike scenarioer for inntektsføring:

- [Ny tildeling av inntektsføring – scenario 1](rev-rec-reallocation-scenario-1.md) – To salgsordrer angis, men de blir bare bekreftet. Det samme scenarioet vil gi like resultater hvis mer enn to salgsordrer har bekreftet status.
- [Ny tildeling av inntektsføring – scenario 2](rev-rec-reallocation-scenario-2.md) – To salgsordrer blir angitt, og deretter legger kunden til en vare i kontrakten etter at den første salgsordren er fakturert.
- [Ny tildeling av inntektsføring – scenario 3](rev-rec-reallocation-scenario-3.md) – En ny linje legges til i en eksisterende, fakturert salgsordre.
- [Ny tildeling av inntektsføring – scenario 4](rev-rec-reallocation-scenario-4.md) – En linje fjernes fra en eksisterende, delvis fakturert salgsordre.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

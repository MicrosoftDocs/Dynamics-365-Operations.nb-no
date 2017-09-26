---
title: Prosjektstyring og regnskap
description: "Prosjektstyrings- og regnskapsfunksjonaliteten kan brukes i flere bransjer for å tilby en tjeneste, produsere et produkt eller oppnå et resultat."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 12afcde947463b3abf58dea6138653a32dcda6f1
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017

---

# <a name="project-management-and-accounting"></a>Prosjektstyring og regnskap

[!include[banner](../includes/banner.md)]


Prosjektstyrings- og regnskapsfunksjonaliteten kan brukes i flere bransjer for å tilby en tjeneste, produsere et produkt eller oppnå et resultat.  

Et prosjekt er en gruppe aktiviteter som er utformet for å tilby en tjeneste, produsere et produkt eller oppnå et resultat. Prosjekter forbruker ressurser og genererer økonomiske resultater i form av inntekter eller aktiva.

## <a name="projects-across-industries"></a>Prosjekter på tvers av bransjer
Funksjonaliteten for prosjektstyring og regnskap kan brukes i flere bransjer, som vist i illustrasjonen nedenfor. [![Prosjekter på tvers av bransjer](./media/projects-accross-industries.jpg)](./media/projects-accross-industries.jpg) 

I et telefonsenter kan en henvendelse om kundestøtte brukes til å beskrive et sett med handlinger som kreves for å løse problemet til kunden. Konsulentfirmaer, for eksempel administrasjon eller teknisk rådgivning organisasjoner eller reklamebyråer, refererer til sine aktiviteter som prosjekter. I markedsføring representerer en kampanje et sett med arbeid som skal leveres. I prosjektbasert produksjon angir en produksjonsordre det ulike arbeidet som må gjøres for å produsere ferdige varer. Uansett hvilket navn du bruker for dem, omfatter disse prosjektene ressurser, tidsplaner og kostnader, og funksjonaliteten for prosjektstyring og regnskap i Enterprise-utgaven av Microsoft Dynamics 365 for Finance and Operations kan bidra i planleggingen, utførelsen og analysen av disse prosjektene.

## <a name="project-phases"></a>Prosjektfaser
Selv om denne prosessflyten er rettet mot eksterne prosjekter eller prosjekter som fullføres for én eller flere kunder, gjelder også funksjonaliteten for interne prosjekter som bare består av kostnader. 

![Tre stadier i et prosjekt](./media/3-stages-of-a-project.png) 

Som vist i illustrasjonen ovenfor kan prosjektstyring og regnskap deles inn i tre faser:

1.  Start
2.  Utfør
3.  Analyser

## <a name="initiate-the-project"></a>Starte prosjektet
Under prosjektstart oppstår flere viktige prosesser. Du kan bruke et prosjekttilbud til å kommunisere anslått arbeidskraft, utgifter og materialer til kunden. Du kan registrere faktureringvilkårene, grenser og avtaler i en prosjektkontrakt. Du kan bruke en prosjektstrukturplan (WBS) til å planlegge og beregne arbeidet. Du kan definere prognoser og budsjetter for å lede prosjektkjøringen. Illustrasjonen nedenfor viser strukturen til et prosjekt.[![prosjektstruktur](./media/project-structure1.jpg)](./media/project-structure1.jpg)  

### <a name="create-project-quotations"></a>Opprett prosjekttilbud

I den første salgsfasen av et prosjekt kan du bruke et prosjekttilbud til å gi kunden et ikke-bindende tilbud. Et tilbud kan inneholde elementer, som varene og tjenestene som tilbudet er gitt for, grunnleggende kontaktinformasjon, spesielle forretningsavtaler og rabatter, og mulige avgifter og tillegg.

Du kan også utstede et garantibrev for en prosjekttilbudstransaksjon mellom organisasjonen og kunden. Når prosjekttilbudet er opprettet, kan du opprette garantibrevforespørselen for kunden og sende den inn til banken. Når banken har godkjent forespørselen, utstedes garantibrevet til kunden. 

Hvis du vil ha mer informasjon, kan du se [Prosjekttilbud](project-quotations.md).

### <a name="create-project-contracts"></a>Opprett prosjektkontrakter

Når du inngår en avtale med en kunde eller en annen finansieringskilde for å fullføre et prosjekt, må du først opprette en prosjektkontrakt. Når du har opprettet prosjektet, må du deretter tilordne det til den tilsvarende kontrakten. Prosjekttypen du oppretter for en prosjektkontrakt, fastsetter metoden som brukes til å fakturere prosjektkundene. Du kan endre en prosjektkontrakt og det tilknyttede prosjektet, men du kan ikke endre prosjekttypen. Hvis du vil ha mer informasjon om prosjekttyper, kan du se delen «Opprette prosjekter».

Hvis du vil ha mer informasjon om prosjektkontrakter, kan du se [Prosjektkontrakter](project-contracts.md).

### <a name="create-work-breakdown-structures"></a>Opprette arbeidsnedbrytningsstrukturer

Detaljnivået i en arbeidsnedbrytningsstruktur avhenger av nøyaktighetsnivået som kreves i estimater, og sporingsnivået som er nødvendig mot disse estimatene. Prosjekter som har svært lite slingringsmonn i tidsplan eller kostnader, krever vanligvis en mer detaljert arbeidsnedbrytningsstruktur samt grundig sporing av arbeidsfremdriften og kostnadene mot arbeidsnedbrytningsstrukturen. 

Hvis du vil ha mer informasjon, kan du se [Arbeidsnedbrytningsstrukturer](work-breakdown-structures.md).

### <a name="create-project-forecasts-and-budgets"></a>Opprette prosjektprognoser og -budsjetter

Du kan bruke prognose hvis organisasjonen har et driftsperspektiv og fokuserer på inntekter og kostnader som er avledet fra bestemte transaksjoner. Hvis organisasjonen imidlertid fokuserer mer på økonomiske beløp, kan du bruke budsjettering. Hver metode har sine fordeler. Hvis du vil ha mer informasjon, kan du se [Prosjektprognoser og -budsjetter](project-forecasts-budgets.md).

### <a name="create-projects"></a>Opprett prosjekter

Du kan opprette seks typer prosjekter i Microsoft Finance and Operations. Hver prosjekttype er satt opp forskjellig for kostnader og inntektsføring. Prosjekttypen du velger er avhengig av formålet med prosjektet. Tabellen nedenfor beskriver den vanlige bruken av hver prosjekttype.

                                                                                                                                                                         |
| Prosjekttype      | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tid og materialer | I Etter regning-prosjekter faktureres kunden for alle kostnader som er påløpt i et prosjekt. Disse kostnadene omfatter kostnader for timer, utgifter, varer og gebyrer.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Fast pris       | I fastprisprosjekter består fakturaene av a konto-transaksjoner. Et fastprisprosjekt faktureres i samsvar med en faktureringstidsplan som er basert på en prosjektkontrakt. Omsetning for et fastprisprosjekt kan beregnes og posteres overalt i prosjektet ved hjelp av metoden for fullføringsprosent. Alternativt kan inntekt beregnes og posteres når prosjektet er fullført, ved hjelp av metoden for fullført kontrakt. Firmaer kan ofte dra nytte av å bruke verdien for varer i arbeid (VIA) til å beregne fullføringsgraden til et prosjekt eller en gruppe prosjekter.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Investering        | Investeringsprosjekter er prosjekter som ikke gir umiddelbare inntekter. De brukes vanligvis til langsiktige interne prosjekter der kostnadene må kapitaliseres. Bare kostnader for varer, timer og utgifter kan registreres for et investeringsprosjekt. Kostnader i et investeringsprosjekt spores og styres ved hjelp av estimatfunksjonaliteten. Investeringsprosjekter kan defineres med en valgfri maksimal kapitalisering. Etter hvert som et investeringsprosjekt skrider fremover, registrerer du kostnadene for det i VIA-kontoer, der kostnadene holdes til prosjektet er fullført. Når prosjektet er eliminert, overfører du VIA-verdien til et anleggsmiddel, en finanskonto eller til et nytt prosjekt. Obs!  Transaksjoner på investeringsprosjekter blir ikke vist på siden **Poster kostnader**, **Avsett inntekt** eller **Opprett fakturaforslag**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Kostnadsprosjekt      | Kostnadsprosjekter brukes vanligvis til å spore interne prosjekter, slik som investeringsprosjekter, og bare timer, utgifter og varer kan registreres for dem. Kostnadsprosjekter er imidlertid vanligvis kortere enn investeringsprosjekter. I motsetning til investeringsprosjekter kan kostnadsprosjekter i tillegg ikke kapitaliseres til balansekontoer. I stedet posteres bare prosjekttransaksjonene til resultatkontoer. **OBS!** Transaksjoner på kostnadsprosjekter gjenspeiles ikke på siden **Poster kostnader**, **Avsett inntekt** eller **Opprett fakturaforslag**. Siden kostnadsprosjekter vanligvis brukes til å spore interne prosjekter, trenger de vanligvis ikke å være knyttet til en kundekonto. Hvis definisjonen imidlertid krever at varebehov opprettes for bestillinger, må du knytte kostnadsprosjekt til en kunde. Denne tilknytningen er nødvendig fordi varebehov behandles som salgsordrelinjer, og systemet krever at det angis en kunde. Dette oppsettet fører imidlertid ikke til at varebehov opprettes automatisk fra en bestilling. Når det gjelder kostnadsprosjekter, ignoreres innstillingen **Opprett varebehov**. Hvis du trenger et varebehov i et kostnadsprosjekt, kan du opprette det manuelt, gitt at en kunde er knyttet til prosjektet. |
| Intern          | Interne prosjekter brukes til å spore kostnader på et prosjekt som er internt i organisasjonen. Interne prosjekter kan gi et planleggingsverktøy for å styre ressursforbruk. **Obs!**  Transaksjoner på kostnadsprosjekter gjenspeiles ikke på siden **Avsett inntekt** eller **Opprett fakturaforslag**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Klokkeslett              | Tidsprosjekter brukes til å spore tid som er knyttet til ikke-belastbare og ikke-produktive aktiviteter, for eksempel et prosjekt for å spore sykefravær for arbeidere. Transaksjoner i tidsprosjekter posteres ikke i finans. I stedet tas de med i arbeider rapporter for utnyttelse av arbeider. Bare timetransaksjoner kan registreres i tidsprosjekter. Du bruker en timejournal eller timeregistrering til å registrere timene i prosjektet. Når timene registrert, vises de som prosjekttransaksjoner, men uten tilsvarende bilagstransaksjoner. **Obs!** Transaksjoner på tidsprosjekter gjenspeiles ikke på siden **Poster kostnader**, **Avsett inntekt** eller **Opprett fakturaforslag**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |


### <a name="assign-workers-categories-and-resources"></a>Tilordne arbeidere, kategorier og ressurser

Du kan planlegge arbeiderressurser basert på kravene og tidsplanen for et prosjekt eller på kompetansen og tilgjengeligheten til arbeidere. Når du bruker funksjonene for ressursplanlegging, kan du effektivt distribuere organisasjonens arbeidere. Du kan raskt finne de best kvalifiserte arbeiderne som har anledning til å arbeide på prosjektet. Du kan også enkelt se hvordan du kan bruke disse arbeiderne bedre i løpet av prosjektet. 

Her er noen av måtene du kan bruke funksjonaliteten for ressursplanlegging på:

-   Bruk informasjon om attributter for en arbeider, for eksempel utdannelse, ferdigheter, sertifiseringer og prosjekterfaring, for å samsvare arbeideren med kravene til et prosjekt.
-   Bruk informasjon om en arbeiders kalenderen og tilgjengelighet for å samsvare arbeiderens tidsplanen med prosjektkalenderen.
-   Vurder kapasiteten til hver arbeider, og finn ut hvordan denne kapasiteten brukes. Hvis en arbeider for eksempel brukes for lite, kan arbeideren tilordnes til et prosjekt som passer hans eller hennes tilgjengelighet og attributter.
-   Gå gjennom en arbeiders tilgjengelighet for å være sikker på at det ikke finnes kalenderkonflikter med arbeiderens tilordninger.
-   Se gjennom informasjon om bruk av arbeider i en sammendragsvisning (for eksempel etter avdeling eller etter arbeider) eller i en detaljert visning (for eksempel etter arbeidere i en avdeling eller etter ukentlige detaljer for hver arbeider).
-   Endre ressurstildelinger for ulike tidsenheter, for eksempel dag, uke eller måned, for å optimalisere hvordan arbeiderne brukes.

## <a name="execute-the-project"></a>Utføre prosjektet
Under prosjektutførelse registrerer teammedlemmer eller ledere arbeid og utgifter som er påløpt, ved å bruke timeregistreringer, utgiftsrapporter og andre forretningsdokumenter. Prosjektledere har verktøy de kan bruke til å overvåke forbruk av budsjettbeløp for prosjektet. Prosjektledere kan også bestille, plukke eller levere materialer til prosjekter ved hjelp av bestillinger og andre forretningsdokumenter. Fakturaer klargjøres og godkjennes, slik at kunder kan faktureres for pågående arbeid. Til slutt gjenkjennes omsetning i denne prosessen som påvirkning i organisasjonens økonomi.

### <a name="manage-work-breakdown-structures"></a>Styre arbeidsnedbrytningsstrukturer

En arbeidsnedbrytningsstruktur er en beskrivelse av arbeid som skal fullføres for et prosjekt. En arbeidsnedbrytningsstruktur er et hierarki av oppgaver. Den representerer ikke bare arbeidet for hver oppgave, men også størrelsen, kostnaden og varigheten til oppgaven. 

Hvis du vil ha mer informasjon, kan du se [Arbeidsnedbrytningsstrukturer](work-breakdown-structures.md).

### <a name="manage-project-forecasts-and-budgets"></a>Behandle prosjektprognoser og -budsjetter

Du kan styre og kontrollere prosjekter på to måter: prosjektprognoser og prosjektbudsjetter. Du kan bruke prognose hvis organisasjonen har et driftsperspektiv og fokuserer på inntekter og kostnader som er avledet fra bestemte transaksjoner. Hvis organisasjonen imidlertid fokuserer mer på økonomiske beløp, kan du bruke budsjettering.

Hvis du vil ha mer informasjon, kan du se [Prosjektprognoser og -budsjetter](project-forecasts-budgets.md).

### <a name="create-production-orders"></a>Opprette produksjonsordrer

En prosjektrelatert produksjonsordre kan kobles til en salgsordre eller et varebehov ved hjelp av metoden for ferdig vare eller metoden for forbrukt vare. Hvis produksjonsordren ble opprettet manuelt, er det i tillegg ingen kobling mellom produksjonsordren og salgsordren eller et varebehovet (ingen kobling til ordre). Hvis produksjonsordren imidlertid ble opprettet automatisk for å oppfylle en salgsordre eller et varebehov, er det en kobling mellom produksjonsordren og salgsordren eller varebehovet (kobling til ordre). 

Bruk én av følgende metoder avhengig av kombinasjonene av disse faktorene:

-   **Ferdig vare/kobling til ordre** – Koble prosjektet til en salgsordre eller et varebehov. Når du bruker denne metoden, posteres de faktiske kostnadene når salgsordren blir fakturert, eller når følgeseddelen blir oppdatert for varebehovet. Kostnaden blir postert som en ferdig vare.
-   **Ferdig vare/ingen kobling til ordre** – Faktiske kostnader kan ikke posteres før produksjonssyklusen for en vare har statusen **Avsluttet**. Kostnaden for den ferdige varen blir postert som én transaksjon.
-   **Forbrukt vare/kobling til ordre** – Koble prosjektet til et varebehov. Hvis du bruker denne metoden, kan du vise de faktiske prosjektkostnadene når produksjonen har statusen **Startet** eller rapporteres som fullført. Kostnadene blir postert som flere varetransaksjoner i prosjekt for råvarer og brukte timer for produksjon. Når følgeseddelen blir oppdatert etter varebehovet, blir det ikke postert noen kostnader. Du kan også definere nivået i stykklistehierarkiet der prosjektene i produksjonen spores.
-   ****Forbrukt vare/ingen kobling til ordre**** – Koble prosjektet til et varebehov. Hvis du bruker denne metoden, kan du vise de faktiske prosjektkostnadene når produksjonen har statusen **Startet** eller rapporteres som fullført. Kostnadene blir postert som flere varetransaksjoner i prosjekt for råvarer og brukte timer for produksjonen. Du kan også definere nivået i stykklistehierarkiet der prosjektene i produksjonen spores.

### <a name="procure-products-and-services"></a>Anskaffe produkter og tjenester

Kjøp og salg av varer er utbredte aktiviteter i mange bedrifter med fokus på prosjekter.

#### <a name="purchase-orders-for-projects"></a>Bestillinger for prosjekter

Formålet med bestillingen fastsetter når bestillingen skal forbrukes, og derfor når varene skal belastes på et prosjekt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metode</th>
<th>Formål</th>
<th>Forbruk av varer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Opprett en bestilling direkte.</td>
<td>Kjøp varer fra en ekstern leverandør for forbruk på et prosjekt. Du kan opprette bestillingen på følgende måter:
<ul>
<li>Fra selve prosjektet. I dette tilfellet er prosjekt allerede definert for bestillingen.</li>
<li>Ved å navigere til prosjektbestillingen. Du må velge både leverandøren og prosjektet som bestillingen skal opprettes for.</li>
</ul></td>
<td>Varene forbrukes når leverandørfakturaen oppdateres.</td>
</tr>
<tr class="even">
<td>Opprett en bestilling fra en salgsordre.</td>
<td>Kjøp varer når du oppretter en salgsordre fra et prosjekt.</td>
<td>Varene forbrukes når salgsordren faktureres kunden.</td>
</tr>
<tr class="odd">
<td>Opprett en bestilling fra et varebehov.</td>
<td>Kjøp varer når du oppretter et varebehov fra et prosjekt.</td>
<td>Varene forbrukes når følgeseddelen for varebehov oppdateres.</td>
</tr>
</tbody>
</table>

#### <a name="sales-orders-for-projects"></a>Salgsordrer for prosjekter

I Prosjektstyring og regnskap kan du registrere vareforbruk på flere ulike måter. Du kan selge eller kjøpe varer fra et prosjekt, eller reservere varer for et prosjekt. 

Du kan bestille varer fra firmaets lager for forbruk på et prosjekt. Du kan også kjøpe varer fra en ekstern leverandør. Varer kan brukes i alle typer prosjekter, bortsett fra i tidsprosjekter. 

Måten du bestiller varer på, er avhengig av hvor du bestiller dem fra:

-   Hvis du vil bestille varer fra firmaets lager, må du registrere ordren som et varebehovet. Hvis du bruker siden **Varebehov**, kan du definere behovet slik at du mottar varer som delleveringer. Derfor kan du utsette forbruk av et antall av varene inntil det er behov for varene.
-   Hvis du vil bestille varer fra en ekstern leverandør, må du opprette ordren som en bestilling på **Bestilling**-siden.

> [!NOTE] 
> Følgeseddelen for en prosjektrelatert salgsordre kan ikke annulleres hvis varene allerede er merket for pakking. 

Tabellen nedenfor viser bestillingsmetodene for varer og beskriver hvordan varene forbrukes.

| Metode            | Formål                                                                                                                                                        | Forbruk av varetransaksjoner                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Salgsordre       | Legg inn en transaksjon direkte i et Etter regning-prosjekt.                                                                                                   | Varetransaksjoner forbrukes når leverandørfakturaen posteres.                                                                               |
| Lagerjournal | Angi og vedlikehold vareposter raskt. Hvis du for eksempel vil legge inn et varebehov basert på en utskrevet liste, kan du bruke lagerjournalen. | Varetransaksjoner forbrukes når journalen posteres.                                                                                        |
| Varebehov  | Angi varer som ikke skal brukes umiddelbart. Denne metoden gjør at du kan spore hvor mange varer som er brukt i én varebehovspost.    | Varetransaksjoner forbrukes når følgeseddelen oppdateres. Varebehovet blir med andre ord opprettet når følgeseddelen posteres. |
| Bestillinger   | Legg inn transaksjoner på ett av tre steder, avhengig av kjøpsmetoden.                                                                              | Varetransaksjoner brukes når følgeseddelen oppdateres, eller når kunden eller leverandøren faktureres.                                      |

### <a name="process-project-invoices"></a>Behandle prosjektfakturaer

Prosjekttypen avgjør hvilken faktureringsprosess som skal brukes. Det er bare de to eksterne prosjekttyper (Etter regning og Fastpris) som kan faktureres. Etter regning-prosjekter og fastprisprosjekter er alltid knyttet til prosjektkontrakt. 

Før du oppretter en kundefaktura for et prosjekt, kan du opprette en foreløpig faktura, eller et fakturaforslag. Du kan velge prosjekttransaksjoner som skal tas med i en prosjektfaktura, i et fakturaforslag. Deretter kan du se gjennom fakturadetaljene før du posterer prosjektfakturaen og sende den til kunden eller en annen finansieringskilde. 


Hvis du vil ha mer informasjon om hvordan du behandler prosjektfakturaer, kan du se [Prosjektfakturering](../accounts-payable/project-invoicing.md).


### <a name="calculate-the-cost-to-complete-a-project"></a>Beregne kostnaden for å fullføre et prosjekt

Når du oppretter et estimat, kan du velge metoden som brukes til å beregne kostnaden for å fullføre prosjektet. Du velger en metode i feltet **Metode for kostnad som skal fylles ut** på siden **Opprett estimat**. Metoden du velger, brukes separat på hver kostnadslinje i kostnadsestimatet. Når en linje har statusen **Opprettet**, kan du endre metoden som brukes for den, på siden **Kostnadsestimat**-siden. 

Tabellen nedenfor beskriver metodene for beregning av kostnaden for å fullføre et prosjekt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Metode</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Total kostnad – faktisk</td>
<td>Estimerte kostnader må angis manuelt. Når kolonnen <strong>Total kostnad</strong> eller <strong>Totalt antall</strong> på siden <strong>Kostnadsestimat </strong>er fylt ut, trekkes de faktiske kostnadene fra de brukerregistrerte totalene. Resultatet er kostnaden for å fullføre prosjektet. Kostnadsutviklingen spores for eksempel vanligvis ikke basert på hvor mange hotellopphold og måltider som registreres i hver periode. I stedet baseres sporing vanligvis på en sammenligning med totalt antall estimerte timer. Denne fremgangsmåten krever ikke en prognosemodell, og den totale kostnaden eller totale antallet kan endres manuelt. Når det angis en verdi i kolonnen <strong>Total kostnad</strong> eller <strong>Totalt antall</strong>, sammenlignes verdien mot de faktiske transaksjonene som er postert i perioden, og deretter reduseres verdien i kolonnen <strong>Antall som skal fullføres</strong> eller <strong>Kostnad som skal fylles ut</strong>.</td>
</tr>
<tr class="even">
<td>Totalt budsjett – faktisk</td>
<td>Faktiske kostnader sammenlignes med prognosemodellen du velger for å fastslå kostnadene. Denne metoden bruker en total budsjettmodell som omfatter prognoseberegnede transaksjoner. Hvis du vil ha en nøyaktigere visning av prosjektet, kan du justere budsjettmodellen når prosjektet pågår. Hvis du må justere prognosen, følger du denne generelle fremgangsmåten:
<ol>
<li>Kopier prognosetransaksjoner til en annen prognosemodell.</li>
<li>Sammenlign prognosetransaksjoner med faktiske transaksjoner.</li>
<li>Oppretthold, reduser eller øk estimatene for neste periode.</li>
</ol>
Finance and Operations reduserer ikke prognoseberegnede estimater automatisk. Det er derfor en god idé å opprettholde en original prognosemodell i fastprisprosjektet for å opprette et utgangspunkt for sammenligning når prosjektet er fullført. 
> [!NOTE] Bruk minst to prognosemodeller når du velger denne metoden. Én modell må inneholde den opprinnelige prognosen. Når det gjelder den andre modellen, må du kopiere prognosetransaksjoner fra en annen modell. Denne metoden er bare gyldig for fastprisprosjekter og investeringsprosjekter.</td>
> </tr>
<tr class="odd">
<td>Gjenstående budsjett</td>
<td>Denne metoden bruker en modell for gjenstående budsjett til å beregne kostnaden for å fullføre prosjektet. Når du bruker denne metoden, summeres de faktiske kostnadene og de prognoseberegnede beløpene i modellen for gjenstående budsjett. Resultatet er en totalkostnad. Før du bruker denne metoden, må en modell for gjenstående budsjett defineres for å trekke fra transaksjoner basert på faktiske transaksjoner som er registrert i systemet. På <strong>Prognosemodeller</strong>-siden må du kontrollere at det er merket av for feltene i gruppen <strong>Automatisk prognosereduksjon</strong>. Vanligvis kopieres et gjenstående budsjett fra et opprinnelig budsjett. Når transaksjoner registreres, reduseres transaksjonene på det gjenstående budsjettet. Hvis du finner ut at du må justere det gjenstående budsjettet etter hvert som prosjektet går fremover, belaster du det gjenstående budsjettet med prognosetransaksjoner. <strong>Obs! </strong> Denne metoden kan bare brukes hvis en prognosemodell er knyttet til estimatet.</td>
</tr>
<tr class="even">
<td>Som forrige estimat</td>
<td>Den samme estimeringsmetoden som ble brukt i forrige periode, brukes. Denne metoden krever en prognosemodell hvis den forrige perioden krevde en prognosemodell.</td>
</tr>
<tr class="odd">
<td>Sett kostnaden som skal fullføres, til null</td>
<td>Denne metoden brukes vanligvis før estimatprosjektet er eliminert. Denne metoden avstemmer de totale estimatene med de faktiske transaksjonene som er postert, og tømmer kolonnen <strong>Kostnad som skal fylles ut</strong>. Den resulterende fullføringsprosenten er alltid 100 prosent. <strong>Prognose</strong>-feltet velges ikke for hver kostnadslinje du oppretter, og det totale estimatet kopieres fra det forrige kostnadsestimatet. Det faktiske forbruket for estimatperioden trekkes fra kostnaden for å fullføre prosjektet. Denne metoden krever ikke en prognosemodell.</td>
</tr>
<tr class="even">
<td>Fra kostnadsmal</td>
<td>Metoden for kostnad som skal fylles ut som er definert i kostnadsmalen som er knyttet til det valgte estimatprosjektet, brukes.</td>
</tr>
</tbody>
</table>

## <a name="analyze-the-project"></a>Analysere prosjektet
På det mest grunnleggende nivået brukes et prosjekt til å gruppere transaksjoner der kostnader registreres, og deretter til å postere disse kostnadene i økonomimodulen. 

Disse transaksjonene er vanligvis et resultat av forretningsdokumenter, for eksempel timeregistreringer, utgiftsrapporter, leverandørfakturaer eller lagertransaksjoner. Livssyklusen til et prosjekt starter vanligvis med estimater, prognoser og budsjetter som bidrar til å planlegge og forutse arbeidsmengden i og den økonomiske innvirkningen på prosjektet. Når du analyserer et prosjekt, kan du evaluere ikke bare transaksjonene som ble utført i løpet av prosjektet, men også nøyaktigheten til beregningene og prognosene, utnyttelsesraten for prosjektgruppemedlemmene og hvor vellykket prosjektet var totalt sett.

### <a name="analyze-cash-flow"></a>Analysere kontantstrøm

Bruk kontantstrømovervåking til å gå gjennom prognoseberegnede kontantstrømmer og faktiske kontantstrømmer for et prosjekt. Du kan gå gjennom kontantstrømmer mens et prosjekt pågår, eller du kan velge å vise kontantstrømmene for et fullført prosjekt. 

Når du overvåker kontantstrømmer, kan du evaluere ett enkelt prosjekt, bruke rapportene til å vise flere prosjekter og overføre kontantstrømmer for prosjekt til kontantstrømprognosene i økonomimodulen.

#### <a name="cash-inflow-forecasting"></a>Prognoser for kontant innflyt

Du kan lage en prognose for kontant innflyt for et valgt prosjekt basert på oppsettet. Hvis prosjektdatoen for eksempel er 5. mars 2012 og du fakturerer 31. mars 2012, kan du lage en prognose for forfallsdatoen og den forventede salgsbetalingsdatoen slik:

-   **Prosjektdato:** 5. mars 2012.
-   **Fakturadato:** 31. mars 2012. Denne datoen fastsettes basert på fakturafrekvensen. I dette eksemplet setter du fakturafrekvensen til gjeldende måned. Derfor blir alle transaksjoner som er postert i mars, fakturert på den siste dagen i måneden.
-   **Forfallsdato:** 14. April 2012. Denne datoen fastsettes basert på betalingsbetingelsene som er angitt for prosjektet. I dette eksemplet valgte du betalingsbetingelser på 14 dager. Derfor blir 14 dager lagt til fakturadatoen, noe som gir forfallsdatoen 14. april 2012.
-   **Forventet salgsbetalingsdato:** 27. april 2012. Denne datoen beregnes ved å legge sammen antall dager i feltet **Generelle bufferdager** på siden **Parametere for prosjektstyring og regnskap** med antall dager i feltet **Individuelle bufferdager** på **Prosjektkontrakter**-siden og deretter legge sammen totalen med antall dager i **Forfallsdato**-feltet. I dette eksemplet angav du **3** i feltet **Generelle bufferdager** og **10** i feltet **Individuelle bufferdager**. Derfor blir 13 dager lagt til forfallsdatoen, noe som gir den forventede salgsbetalingsdatoen 27. april 2012.

De generelle bufferdagene kan enten erstatte de individuelle bufferdagene eller legges til de individuelle bufferdagene:

-   Hvis du vil bruke de generelle bufferdagene som erstatning for de individuelle bufferdagene, kan du angi gjennomsnittlig antall dager mellom forfallsdatoen og faktisk betalingsdato for kunder.
-   Hvis du vil legge de generelle bufferdagene til de individuelle bufferdagene, angir du estimatet for antall dager mellom dagen kunden sender betalingen og dagen organisasjonen mottar betalingen, i feltet **Generelle bufferdager**.

Definer individuelle bufferdager i kontrakten for prosjektet. Dagene beregnes på grunnlag av både forfallsdatoen for salgsfaktura og organisasjonens erfaring med en kundes betalingsmønster.

#### <a name="actual-cash-inflow"></a>Faktisk kontant innflyt

Faktisk kontant innflyt ligner på prognosen, men du kan begynne beregningene fra første fakturadato. Her er et eksempel:

-   **Fakturadato:** 2. mars 2012.
-   **Forfallsdato:** 16. mars 2012. Betalingsbetingelsene er satt til 14 dager.
-   **Forventet salgsbetalingsdato:** 29. mars 2012. Beregningen omfatter tre generelle bufferdager og 10 individuelle bufferdager.

#### <a name="cost-forecasting"></a>Kostnadsprognose

Basert på dagene som er definert, kan kostnadsbetalingsdatoen være forskjellig fra prosjektdatoen. I så fall beregnes kostnadsbetalingsdatoen ved å legge sammen antall dager fra prosjektdatoen med antall dager i betalingsbetingelsene. 

La oss si at prosjektdatoen for transaksjonen er 5. mars 2012 og følgende betalingsbetingelser er angitt:

-   **Timer:** Gjeldende måned (**M**)
-   **Utgifter:** 14 dager (**D14**)
-   **Varer:** 30 dager (**D30**)

Basert på disse innstillingene er kostnadsbetalingsdatoen for hver transaksjonstype følgende:

-   **Timer:** 31. mars 2012, som er den siste dagen i den valgte måneden.
-   **Utgifter:** 19. mars 2012, som er 14 dager etter transaksjonsdatoen.
-   **Varer:** 4. april 2012, som er 30 dager etter transaksjonsdatoen.

> [!NOTE] 
> Forfallsdatoen for bestillingen er basert på leverandørtransaksjonen når prosjektbestillingen opprettes. Forfallsdatoen fastsettes ikke av noen standardinnstillinger. 

Kostnadsbetalingsdatoen beregnes ikke på bufferdager. Når et prosjekt er fullført og all etterkalkulering og fakturering er fullført, posteres både kostnaden og salget til resultatkontoene. 

Når alle salgs- og leverandørfakturaer er fullført, kan du vise relasjonen mellom feltene på **Kontantstrøm**-siden og feltene på **Prosjektoppgaver**-siden.

| Kontantstrøm-siden | Prosjektoppgaver-siden |
|----------------|-------------------------|
| Kontant innflyt   | Omsetning                 |
| Kontant utflyt  | Total kostnad              |
| Netto kontantstrøm | Bruttofortjeneste            |

### <a name="review-costs"></a>Gå gjennom kostnader

Du kan overvåke de påløpte kostnadene for organisasjonen i løpet av et prosjekt på **Kostnadskontroll**-siden. Når du sammenligner de opprinnelige budsjetterte kostnadene for prosjektet med gjeldende faktiske kostnader og igangsatt kost, kan du finne ut om prosjektet er i rute eller over eller under budsjettet. 

> [!NOTE] 
> Når du bruker **Kostnadskontroll**-siden til å vise gjeldende status for prosjektkostnader, bruker du prognosemodellene som ble valgt for det opprinnelige og gjenstående budsjettet. Hvis du velger andre prognosemodeller når du beregner kostnader, blir ikke resultatene av beregningen nøyaktige.

#### <a name="viewing-the-remaining-budgeted-amounts"></a>Vise gjenstående budsjettbeløp

Hvis **Gjenstående budsjett** er valgt som metode for kostnadskontroll på siden **Parametere for prosjektstyring og regnskap**, beregner **Kostnadskontroll**-siden kostnader som ikke har blitt postert som faktiske kostnader eller merket som igangsatt. Beløpene i **Generelt**-fanen i den nedre ruten på **Kostnadskontroll**-siden beregnes slik:

-   **Faktiske kostnader** – Det totale beløpet som er brukt i prosjektet for den valgte kostnadslinjen. Det faktiske kostnadsbeløpet beregnes på siden **Finansoppdateringer**.
-   **Igangsatt kost** – Det ekstra utgiftsbeløpet som den juridiske enheten har avtalt å betale. De bestemte igangsatte kostbeløpene beregnes på siden **Igangsatt kost**.
-   **Gjenstående budsjett** – Hvor mye av det opprinnelige budsjetterte beløpet som fortsatt er tilgjengelig for den valgte kostnadslinjen. Det gjenstående budsjettbeløpet beregnes på siden **Forhåndsvisning av økonomimodul**.
-   **Total kostnad** – Summen av faktiske kostnader, igangsatt kost og gjenstående budsjettbeløp.

Du kan vise en sammenligning av de totale forventede kostnadene og det opprinnelige budsjettet i **Avvik**-fanen på **Kostnadskontroll**-siden. Denne sammenligningen viser forskjeller mellom disse beløpene. Derfor kan du se hvor dataene ikke stemmer overens. Avviksbeløpene beregnes på følgende måter:

-   **Opprinnelig budsjett** – Beløpet som opprinnelig ble budsjettert for den valgte kostnadslinjen. Det opprinnelige budsjettbeløpet beregnes på siden **Forhåndsvisning av økonomimodul**.
-   **Total kostnad** – Summen av faktiske kostnader, igangsatt kost og gjenstående budsjett, som rapportert i **Generelt**-fanen.
-   **Avvik** – Forskjellen mellom den totale kostnaden og det opprinnelige budsjettet.
-   **Avvik basert på antallet** – Den totale differansen mellom den opprinnelige prognosen og samlet prognose. Denne forskjellen kan uttrykkes matematisk som (totalt prognoseantall) × (opprinnelig gjennomsnittpris – total gjennomsnittpris). Denne beregningen gjelder bare prosjekttimer.
-   **Avvik basert på pris** – Den totale differansen mellom den opprinnelige prognosen og samlet prognose. Denne forskjellen kan uttrykkes matematisk som (opprinnelig prognosepris) × (opprinnelig prognoseantall – totalt prognoseantall). Denne beregningen gjelder bare prosjekttimer.

#### <a name="viewing-the-total-budgeted-amounts"></a>Vise totale budsjettbeløp

Hvis **Totalt budsjett** er valgt som metode for kostnadskontroll på siden **Parametere for prosjektstyring og regnskap**, beregner **Kostnadskontroll**-siden de faktiske kostnadene og de totale kostnadene for prosjektet for å hjelpe deg å oppdage en eventuell differanse mellom dem. Beløpene i kolonnene i den nedre ruten i **Generelt**-fanen på **Kostnadskontroll**-siden beregnes slik:

-   **Samlede budsjetterte kostnader** – Hele det budsjetterte beløpet for den valgte kostnadslinjen.
-   **Faktiske kostnader** – Det totale kostnadsbeløpet som er påløpt i prosjektet hittil for de valgte kostnadslinjene.
-   **Igangsatt kost** – Det totale beløpet som er igangsatt for den valgte kostnadslinjen.
-   **Avvik** – Differansen mellom summen av faktiske kostnader pluss igangsatt kost og den totale kostnaden. Avviket viser om ekstra kostnader må være angitt for det totale budsjettet.

Du kan vise differansen mellom det totale budsjettet og det opprinnelige budsjettet i **Avvik**-fanen på **Kostnadskontroll**-siden ved å se i følgende felt:

-   **Opprinnelig budsjett** – Beløpet som opprinnelig ble budsjettert for kostnadslinjen. Det opprinnelige budsjettet beregnes på siden **Forhåndsvisning av økonomimodul**.
-   **Samlede budsjetterte kostnader** – Den totale kostnaden som opprinnelig ble budsjettert for kostnadslinjen. De samlede budsjetterte kostnadene beregnes på siden **Forhåndsvisning av økonomimodul**.
-   **Avvik** – Avviket for kostnadslinjen. Dette beløpet beregnes ved å trekke totalkostnaden fra det opprinnelige budsjettet.
-   **Avvik basert på antallet** – Den totale differansen mellom det opprinnelige budsjettet og det totale budsjettet. Dette beløpet beregnes ved å trekke det totale antallet timer i budsjettet fra antallet timer i det opprinnelige budsjettet, og deretter multiplisere differansen med kostprisen i det opprinnelige budsjettet. Denne differansen kan uttrykkes matematisk som (kostpris i opprinnelig budsjett) × (antall timer i opprinnelig budsjett – totalt antall timer i budsjett). Denne beregningen gjelder bare prosjekttimer.
-   **Avvik basert på pris** – Dette beløpet beregnes ved å trekke det totale antallet timer i budsjettet fra antallet timer i det opprinnelige budsjettet, og deretter multiplisere differansen med det totale timeforbruket. Denne differansen kan uttrykkes matematisk som (antall timer brukt totalt) × (antall timer i opprinnelig budsjett – totalt antall timer i budsjett). Denne beregningen gjelder bare prosjekttimer.

### <a name="analyze-utilization"></a>Analysere utnyttelse

Utnyttelsesraten er prosentandelen av tid en arbeider bruker på fakturerbart eller produktivt arbeid i en bestemt arbeidsperiode. Fakturerbare timer er arbeiderens timer som en bestemt kunde kan belastes for. 

En arbeiders utnyttelsesrate beregnes ved å dele antall fakturerbare timer på antall arbeidstimer i en bestemt periode. Hvis en arbeider for eksempel har 30 fakturerbare timer i en periode, og antallet arbeidstimer i samme periode er 40, er arbeiderens utnyttelsesrate 75 prosent. 

Når du beregner utnyttelsesrate for en arbeider, kan du beregne fakturerbar rate eller effektivitetsrate:

-   **Fakturerbar rate** – Forskjellen mellom fakturerbare timer og ikke-fakturerbare timer eller normtimer.
-   **Effektivitetsrate** – Forskjellen mellom produktive timer og ikke-produktive timer eller normtimer. Produktive timer utgjør timene arbeideren bruker på å bidra til et bestemt prosjekt. Produktive timer faktureres vanligvis kunder, bortsett fra når det gjelder interne prosjekter. Ikke-produktive timer faktureres aldri en kunde.

Du beregner utnyttelsesraten på **Timebruk**-siden. Beregningene er basert på standardinnstillinger. Disse innstillingene angir også hvordan timer beregnes, ved å tilordne **Utnyttelse** eller **Belastning** for hver prosjekttype. Dette gjelder for beregninger av fakturerbar rate og effektivitetsrate.

-   **Utnyttelse** – Timer som rapporteres for den valgte prosjekttypen, vurderes alltid for fakturerbart forbruk eller effektivitetsforbruk.
-   **Belastning** – Timer som rapporteres for den valgte prosjekttypen, vurderes alltid for ikke-fakturerbart forbruk eller ikke-effektivitetsforbruk.
-   **I henhold til egenskap for linje** – Linjeegenskapene for en bestemt timetransaksjon avgjør om timene vurderes for fakturerbart forbruk eller effektivitetsforbruk.
-   **Tas ikke med** – Timer tas ikke med i beregningen av fakturerbart forbruk eller effektivitetsforbruk.

På **Timebruk**-siden kan du vise den samlede utnyttelsesraten i prosent for en arbeider eller et prosjekt, og du kan vise hvor mange timer som ble brukt på beregningene av utnyttelsesraten for hver av følgende timetyper:

-   **Ikke inkluderte timer** – Disse timene tas ikke med i timebruksraten.
-   **Inkluderte timer** – Disse timene beregnes ved å legge sammen brukstimene og belastningstimene. Disse timene tas med i beregningen av utnyttelsesraten.
-   **Belastningstimer** – Hvis du beregner en fakturerbar rate, er disse timene de samme som ikke-belastbare timer. Når du beregner en effektivitetsrate, er disse timene de samme som ikke-produktive timer.
-   **Utnyttelsestimer** – Hvis du beregner en fakturerbar rate, er disse timene de samme som ikke-belastbare timer. Når du beregner en effektivitetsrate, er disse timene de samme som produktive timer.

Når du beregner utnyttelsesrate for en arbeider, kan du bruke normtimene eller inkluderte timer. Hvis du bruker inkluderte timer, må du kontrollere at arbeidere registrerer all arbeidstid for timeregistreringsperiodene, fordi beregningen uttrykkes som en prosent av timer som oppgis. Når du beregner timebruksraten for et prosjekt, en prosjektkontrakt, en kundepost eller en kategori, må du bruke inkluderte timer i beregningen.

### <a name="review-project-statements"></a>Gå gjennom prosjektoppgaver

Du kan opprette en prosjektoppgave for å få en rask oversikt over fremdriften til et prosjekt. Når du kjører en prosjektoppgave, kan du angi kriteriene som brukes til å beregne oppgaven, ved å foreta valg i **Generelt**-fanen på **Prosjektoppgaver**-siden. Du kan velge om du vil inkludere eller ekskludere følgende informasjon:

-   Prosjekttyper
-   Transaksjonstyper
-   Prosjektdato/finansdato
-   Data

Når oppgaven beregnes, kan du vise følgende informasjon i de ulike fanene på **Prosjektoppgaver**-siden:

-   **Generelt** – Generell informasjon om den grunnleggende resultatstrukturen for prosjektet.
-   **Resultat** – Informasjon om påløpt omsetning.
-   **VIA** – Informasjon om VIA-kontosaldoer.
-   **Forbruk** – Informasjon om forbruket av timer, varer, utgifter og lønnstransaksjoner.
-   **Faktura** – Informasjon om fakturaer og a konto-fakturering.
-   **Timepris** – Timepriser for timer som posteres til inntekts- og utgiftskontoer.






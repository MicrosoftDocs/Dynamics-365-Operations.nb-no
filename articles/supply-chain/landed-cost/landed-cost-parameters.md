---
title: Oppsett for parametere for netto innkjøpspris
description: Dette emnet beskriver hvordan du definerer generell informasjon og konfigurasjonsinnstillinger som brukes i hele modulen Netto innkjøpspris for postering, statusoppdateringer, nummerserier og virkemåte.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 834a8cc5b50e02afb1ecf7f53d2c4fa661764219
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571791"
---
# <a name="landed-cost-parameters-setup"></a>Oppsett for parametere for netto innkjøpspris

[!include [banner](../../includes/banner.md)]

Du bruker siden **Parametere for netto innkjøpspris** til å definere generell informasjon og konfigurasjonsinnstillinger som brukes i hele modulen **Netto innkjøpspris** for postering, statusoppdateringer, nummerserier og virkemåte. Parameteroppsettet deles på tvers av juridiske enheter og kan endres av en administrator.

## <a name="open-the-landed-cost-parameters-page"></a>Åpne siden Parametere for netto innkjøpspris

Hvis du vil arbeide med parameterne, kan du gå til **Netto innkjøpspris \> Oppsett \> Parametere for netto innkjøpspris**, og deretter angir du feltene slik som beskrevet i følgende underdeler.

![Siden Parametere for netto innkjøpspris.](media/landed-cost-parameters.png "Siden Parametere for netto innkjøpspris")

## <a name="general-tab"></a>Fanen Generelt

### <a name="general-fasttab"></a>Hurtigfanen Generelt

Følgende tabell beskriver feltene som er tilgjengelige i hurtigfanen **Generelt** i fanen **Generelt** på siden **Parametere for netto innkjøpspris**.

| Innstilling | beskrivelse |
|---|---|
| Bruk forsendelsessats | En forsendelsessats er definert for en definert periode, og brukes til å estimere kostnader for varer som bruker flere valutaer. Sett dette alternativet til *Ja* for å bruke en forsendelsessats. |
| Valutakurstype | Standard samling valutakurser som brukes til flervalutaberegninger for en sjøreise og sjøreisekostnader. |
| Oppdater bestillingsantall | Velg hva som skal skjer hvis en bruker endrer antallet på en bestillingslinje:<ul><li>**Godta** – Sjøreiseantallet justeres automatisk.</li><li>**Advarsel** – Hvis linjen er knyttet til en sjøreise, vises det en advarsel, men sjøreiseantallet oppdateres.</li><li>**Feil** – Hvis linjen er knyttet til en sjøreise, vises det en feilmelding, og bestillingen kan ikke oppdateres. Ordrelinjen må derfor først fjernes fra sjøreisen.</li></ul> |
| Oppdater antall kartonger automatisk | Når dette alternativet er satt til *Ja*, legges alle kartongene sammen og vises på sjøreise- og containernivåene. Når feltet er satt til *Nei*, settes antall kartonger i utgangspunktet til 0 (null) og kan redigeres manuelt etter behov. |

### <a name="costing-fasttab"></a>Hurtigfanen Etterkalkulering

Følgende tabell beskriver feltene som er tilgjengelige i hurtigfanen **Etterkalkulering** i fanen **Generelt** på siden **Parametere for netto innkjøpspris**.

| Innstilling | beskrivelse |
|---|---|
| Posteringsspesifikasjon | Velg verdijusteringen i finans:<ul><li>**Totalsum** – En totalsum posteres til finans.</li><li>**Varegruppe** – Justeringen er angitt per varegruppe.</li><li>**Varenummer** – Justeringen er angitt per vare. Denne verdien gir flest detaljer.</li></ul> |
| Tillat nullkostnader | Sett dette alternativet til *Nei* hvis det skal vises en feil hvis en bruker prøver å postere et kostnadsestimat for en sjøreisefaktura eller en bestilling som ikke inneholder en verdi for den forventede sjøreisekostnaden. Feilmeldingen angir at en kostnad på 0 (null) ikke kan fordeles, og fakturapostering vil mislykkes. I dette tilfellet kan brukeren manuelt oppdatere estimatet (eller konfigurere den automatiske kostnaden på nytt), og deretter enten trekke inn den oppdaterte verdien eller slette kostnaden hvis den ikke gjelder.<p>Sett dette alternativet til *Ja* for å tillate at sjøreisekostnaden kan være tom. I dette tilfellet blir en pris på 0 (null) tildelt i henhold til kostnadsområdet. En leverandørkostnadsfaktura kan deretter behandles mot nullpriskostnaden når sjøreisen mottas.</p><p>Det anbefales at du konfigurerer estimatet for automatisk kostnadspost for å hindre at en nullprispris vises. Selv om denne forhåndsberegningen ikke er fullstendig nøyaktig, skal den fremdeles være mer nøyaktig enn en antatt null kostnad.</p> |
| Posteringsdato for justering | Når du posterer en sjøreisekostnadsfaktura for leverandører, oppdateres også utligningstabellen (lagerjusteringer). Velg datoen som er definert som standard på siden **Velg sjøreisekostnader** når du er i fakturajournalen:<ul><li>**Transaksjonsdato** – Bruk datoen for journalen (posteringsdato):</li><li>**Fakturadato for bestilling** – Bruk den økonomiske posteringsdatoen for lagerfakturaen (bestilling).</li><li>**Valgt dato** – Brukeren kan angi en posteringsdato. Selv om datoen kan stå tom, vil brukeren få en feilmelding hvis den fremdeles er tom når kostnadsfakturaen posteres.</li></ul> |
| Bruk innkjøpsfakturabilag | Når du setter alternativet til *Ja*, bruker kostnadsavsetningstransaksjoner det samme bilagsnummeret som brukes for innkjøpsfakturaen. Når den er satt til *Nei*, bruker systemet det neste tilgjengelige nummeret for nummerserien **Bilag for kostnadsavsetning** som er definert i fanen **Nummerserier** på siden **Parametere for netto innkjøpspris**.<p>Dette alternativet har bare effekt når alternativet **Poster til belastningskonto i finans** er satt til *Ja* i fanen **Faktura** på siden **Leverandørparametere**.</p> |
| Blokker manuell postering til avregningskonto | Sett dette alternativet til *Ja* for å hindre postering til avklaringskontoer der transaksjonen ikke er knyttet til en sjøreise ved å velge **Funksjoner \> Velg sjøreisekostnader** i handlingsruten for leverandørfakturajournalen. Det anbefales at du setter dette alternativet til *Ja*, slik at sjøreise- og avsetningskontoen kan utlignes på riktig måte. |
| Bruk tilleggsavsetningskonto for kostnadstype | Når dette alternativet er satt til *Ja*, brukes avsetningskontoen som er konfigurert for den relevante kosttypekoden på siden **Kosttypekoder** til å avsette kostnader som en utgift.<p>Dette alternativet har bare effekt når alternativet **Poster til belastningskonto i finans** er satt til *Ja* i fanen **Faktura** på siden **Leverandørparametere**. |
| Poster justeringer som avvik | Når du setter alternativet til *Ja*, overstyrer det standardfunksjonaliteten og tvinger lagerjusteringstransaksjonene som er knyttet til avvik mellom estimerte kostnader og faktiske kostnader som skal posteres til en avvikskonto.<p>Når du setter dette alternativet til *Nei*, håndteres lagerjusteringstransaksjonene som er relatert til avvik, basert på konfigurasjonen til etterkalkuleringsmetoden og kostnadstypekoden. For standardkost vil avvikene likevel bli postert til avvikskontoen. Når det kommer til avveid gjennomsnitt (WMA), blir avvik postert enten til avvikskontoen eller til lageret.</p><p>Dette alternativet har bare effekt når alternativet **Poster til belastningskonto i finans** er satt til *Ja* i fanen **Faktura** på siden **Leverandørparametere**.</p> |

### <a name="validation-fasttab"></a>Hurtigfanen Validering

Følgende tabell beskriver feltene som er tilgjengelige i hurtigfanen **Validering** i fanen **Generelt** på siden **Parametere for netto innkjøpspris**.

| Innstilling | beskrivelse |
|---|---|
| Flere kostnadsfakturaer | Velg hva som skal skje hvis mer enn én faktura behandles mot en sjøreise, folio eller container for samme tillegg.<ul><li>**Godta** – Systemet bør tillate flere kostnadsfakturaer.</li><li>**Advarsel** – Det vises en advarsel.</li><li>**Feil** – Det vises en feilmelding.</li></ul> |
| Flere leverandører per folio | Velg hva som skal skje hvis me renn én leverandørs bestillinger blir lagt til en folio.<ul><li>**Godta** – Systemet bør tillate handlingen.</li><li>**Advarsel** – Det vises en advarsel, men handlingen kan fremdeles utføres.</li><li>**Feil** – Det vises en feilmelding, og handlingen hindres.</li></ul><p>Tollmekleren eller lokale lover kan gjøre en bestemt verdi obligatorisk for dette feltet.</p> |
| Toleranse for flere leveringsmåter | Velg hva som skal skje hvis varer fra en bestilling som bruker en annen leveringsmåte enn sjøreisen, blir lagt til for den sjøreisen.<ul><li>**Godta** – Systemet bør tillate handlingen.</li><li>**Advarsel** – Det vises en advarsel, men handlingen kan fremdeles utføres.</li><li>**Feil** – Det vises en feilmelding, og handlingen hindres.</li></ul> |
| Toleranse for flere lagre | Velg hva som skal skje hvis en sjøreise inkluderer flere ordrelinjer som må leveres til forskjellige lagre. Disse ordrelinjene kan være spredt på tvers av én eller flere bestillinger.<ul><li>**Godta** – Systemet bør tillate handlingen.</li><li>**Advarsel** – Det vises en advarsel.</li><li>**Feil** – Det vises en feilmelding.</li></ul> |
| Mangler volum | Velg hva som skal skje hvis en bruker legger til en vare uten volum i en sjøreise.<ul><li>**Godta** – Systemet bør godta varen.</li><li>**Advarsel** – Det vises en advarsel.</li><li>**Feil** – Det vises en feilmelding.</li></ul><p>Hvis volumer brukes til å beregne og fordelingskostnader, anbefales det at du velger enten *Advarsel* eller *Feil*.</p> |
| Leverandør av tjenester uten sjøreisekostnad | Velg hva som skal skje hvis en bruker prøver å behandle en faktura for en leverandør som ikke er knyttet til tilknytning til en sjøreise. <ul><li>**Godta** – Systemet bør tillate handlingen.</li><li>**Advarsel** – Det vises en advarsel.</li><li>**Feil** – Det vises en feilmelding.</li></ul><p>Det anbefales at du velger *Advarsel*.</p> |

### <a name="defaults-fasttab"></a>Hurtigfanen Standarder

Følgende tabell beskriver feltene som er tilgjengelige i hurtigfanen **Standarder** i fanen **Generelt** på siden **Parametere for netto innkjøpspris**.

| Innstilling | beskrivelse |
|---|---|
| Journalnavn | Velg standardjournalen som funksjonen *Opprett ankomstjournal* skal bruke. |
| Sjøreisestatus | Velg statusen en sjøreise må ha før brukere kan sette opp en forsendelsescontainer for levering i systemet. Denne handlingen skjer vanligvis når varene er i transitt eller ved kaien. |
| Reisemal | Velg standard reisemal som skal brukes for nye forsendelsescontainere for leie. Du vil vanligvis velge en reisemal som inkluderer leiekostnader. |
| Bevegelse | Hvis over-/underantallet for en levering er innenfor den definerte toleransen, behandles en bevegelsesjournal automatisk. Velg standard bevegelsesjournal som skal brukes. Feltet **Motkonto** for det valgte navnet på bevegelsesjournalen må ha en verdi. |
| Overfør | Når en underlevering behandles, blir kortmottaksantallet overført til et underleveringslager. Velg standard overføringsjournal som skal brukes. |
| Deaktiver bestillinger som ikke gjelder sjøreise | Deaktiver funksjonaliteten for over-/underlevering av netto innkjøpspris for bestillinger som ikke er knyttet til en sjøreise. |
| Deaktiver bestillinger som ikke gjelder varer i transitt | Deaktiver funksjonaliteten for over-/underlevering av netto innkjøpspris for bestillinger som ikke bruker funksjonen for varer i transitt. |
| Respittperiode for varer i transitt-overmottak | Angi antall dager etter første mottak av en forsendelsescontainer som flere overmottak fremdeles kan fullføres for den forsendelsescontaineren. |

## <a name="status-updates-tab"></a>Fanen Statusoppdateringer

Systemet bruker statusverdier til å angi statusen til hver sjøreise. Verdier for sjøreisestatus kan automatisk brukes for sjøreiser via sjøreisesporing eller periodiske satsvise jobber. Du kan eventuelt bruke dem manuelt ved å åpne reisen og deretter velge en status i gruppen **Sjøreiseoppdatering** i fanen **Behandle** i handlingsruten. 

Du kan opprette så mange verdier for sjøreisestatus du vil. Fire av dem må imidlertid defineres som brukt for et spesielt formål i fanen **Statusoppdateringer** på siden **Parametere for netto innkjøpspris**. Følgende tabell beskriver feltene som er tilgjengelige der.

| Innstilling | beskrivelse |
|---|---|
| Kalkulert | Velg sjøreisestatusen som identifiserer at en sjøreise er gjennomført. |
| I transitt | Velg sjøreisestatusen som identifiserer at en sjøreise er i transitt. |
| Klar for etterkalkulering | Velg sjøreisestatusen som identifiserer at en sjøreise er klar for etterkalkulering. Denne statusen brukes når alle lagerinnkjøpsfakturaer og sjøreisekostfakturaer for kostpriser i feltet **Krediter på reisekostnad** som er satt til *Leverandør*, er behandlet for sjøreisen. Sjøreiser som ikke fullfører den kostnadsførte prosessen, får statusen *Klar til etterkalkulering*.|
| Forhåndskalkulert | Velg sjøreisestatusen som identifiserer at en sjøreise kjørgjøres for etterkalkulering. Denne statusen brukes når en ny kostnadstransaksjon legges til en sjøreise etter at den allerede er kostnadsført. Nye kostnadstransaksjoner kan bli lagt til en tidligere kostnadsført sjøreise når en ny fraktfaktura eller uventet kostnad for overliggetid mottas. Denne statusen brukes automatisk når det legges til en ny sjøreisekostnad for en kostnadsført sjøreise. |

## <a name="voyage-creator-tab"></a>Fanen Sjøreiseoppretter

I tabellen nedenfor beskrives delene i fanen **Sjøreiseoppretter** på siden **Parametere for netto innkjøpspris**.

| Del | beskrivelse |
|---|---|
| Toleranser | Feltene **Utenfor volumtoleranse** og **Utenfor vekttoleranse** definerer terskler som gjør at varer regnes som overvolum og overvekt hvis terskelverdien overskrides. Når en bruker legger til varer på siden **Sjøreiseredigering**, vises det en advarsel hvis volumet eller vekten overskrider verdien du angir her. Verdien til hvert felt uttrykkes som en prosent av maksimalt volum eller vekt som er angitt for den relevante forsendelsescontainertypen. Det anbefales at verdien er mellom 5 og 10 prosent av maksimalt volum eller vekt. |
| Oppsett for foliooppretting | Systemet kan opprette flere folioer i løpet av prosessen for sjøreiseoppretting. Bruk denne delen til å definere når det skal opprettes en ny folio. For hver rad i denne delen kontrollerer systemet den angitte tabellen og det angitte feltet, og det opprettes en folio for hver unike feltverdi. |

## <a name="cost-estimates-tab"></a>Fanen Kostnadsestimater

Fanen **Kostnadsestimater** på siden **Parametere for netto innkjøpspris** har bare ett felt: **Standard etterkalkuleringsversjon**. Dette feltet gjelder bare når etterkalkuleringsmetoden er *Standard etterkalkulering*. Velg standard etterkalkuleringsversjon som skal brukes for den periodiske oppgaven *Oppdatering av varekostpris*. Det kan hende at du må endre denne innstillingen hver gang et nytt finansår begynner.

## <a name="inventory-dimensions-tab"></a>Fanen Lagerdimensjoner

Du bruker fanen **Lagerdimensjoner** på siden **Parametere for netto innkjøpspris** til å kontrollere hvilke tilgjengelige lagerdimensjoner som skal vises som standard på hver side for netto innkjøpspris der dimensjoner brukes.

Velg en dimensjon, og sett deretter alternativet **Sjøreiselinjer**, **Varer i transitt** og/eller alternativet **Kostnadsestimater** til *Ja* for hver side der denne dimensjonen skal vises som standard. Gjenta dette trinnet for andre dimensjoner etter behov.

Innstillingene i denne fanen fastsetter standarddimensjonene for hver angitte side på tvers av juridiske enheter. Brukere som arbeider på en av de angitte sidene, kan imidlertid overstyre standarddimensjonene ved å velge **Lager \> Visningsdimensjoner** i handlingsruten.

## <a name="number-sequences-tab"></a>Fanen Nummerserier

Fanen **Nummerserier** på siden **Parametere for netto innkjøpspris** viser hver type referansenummerserie som Netto innkjøpspris krever, men som ikke deles på tvers av juridiske enheter. For hver referanse i listen velger du en nummerseriekode.

> [!NOTE]
> I en konfigurasjon for flere firmaer må det opprettes ulike nummerserier for hvert firma (juridisk enhet).

## <a name="shared-number-sequences-tab"></a>Fanen Delte nummerserier

Fanen **Delte nummerserier** på siden **Parametere for netto innkjøpspris** viser hver type referansenummerserie som er delt på tvers av juridiske enheter for Netto innkjøpspris. Det er for øyeblikket bare én nummerserie i listen. Denne nummerserien brukes for sjøreise-ID-en.

Brukere kan vise alle sjøreisene på tvers av alle juridiske enheter på siden **Alle sjøreiser**. Brukere må imidlertid være i den juridiske enheten for den valgte posten for at brukerne skal kunne redigere og behandle sjøreisen.

## <a name="feature-visibility-tab"></a>Fanen Funksjonssynlighet

Netto innkjøpspris tilfører funksjonalitet (felt og funksjoner) til flere ofte brukte sider i Microsoft Dynamics 365 Supply Chain Management. Disse sidene inneholder undersider som er knyttet til hoveddata for leverandører, frigitte produkter, bestillinger, overføringsordrer og lageroppsett. Hvis du bruker Netto innkjøpspris, må du gjøre disse funksjonene synlige overalt før du kan dra nytte av dem. Hvis du ikke bruker Netto innkjøpspris, kan du skjule funksjonene slik at de holdes utenfor.

I fanen **Funksjonssynlighet** på siden **Parametere for netto innkjøpspris** setter du alternativet **Aktiver** til *Ja* for å gjøre funksjonene for Netto innkjøpspris synlige der de er tilgjengelige. Sett den til *Nei* for å skjule funksjonene på vanlige sider utenfor Netto innkjøpspris. Selv om alternativet er angitt til *Nei*, vil imidlertid selve modulen, inkludert siden **Parametere for netto innkjøpspris**, være tilgjengelig for brukere som har de riktige tillatelsene til å få tilgang til den.

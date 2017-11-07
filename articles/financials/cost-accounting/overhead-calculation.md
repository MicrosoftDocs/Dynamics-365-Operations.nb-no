---
title: Beregning av indirekte kostnader
description: Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0ea6f7428cd5c7618d2d69f1fb66fd9539ad1073
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="overhead-calculation"></a>Beregning av indirekte kostnader

[!include[banner](../includes/banner.md)]


Dette emnet beskriver de vanlige prosessene for beregning og tildeling av indirekte kostnader.

<a name="term-definition"></a>Termdefinisjon
---------------

Indirekte kostnader er kostnadene som påløper for å drive en virksomhet, men som ikke kan direkte tilskrives en bestemt forretningsaktivitet, et produkt eller en tjeneste. Indirekte kostnader gir viktig støtte for generering av fortjenesteskapende aktiviteter. Her er noen eksempler på indirekte kostnader:

-   Leie
-   Elektrisitet
-   Administrative lønninger

## <a name="overhead-calculation-overview"></a>Oversikt over indirekte kostnader
Beregning av indirekte kostnader kjører policyene for kostnadsregnskap i riktig rekkefølge. Du kan kjøre beregning av indirekte kostnader flere ganger for samme regnskapsperiode hvis policyer for kostnadsregnskap er endret eller bestemte feil er oppdaget. Hver kjøring av beregningen av indirekte kostnader lagres og mottar en unik versjons-ID som lar deg sammenligne beregningene i forskjellige versjoner. Kostnadsoppføringene som de indirekte kostnadene genererer mottar en regnskapsdato. Denne regnskapsdatoen samsvarer med sluttdatoen for regnskapsperioden som skal brukes i beregningen. Den unike versjons-ID-en består av følgende elementer:

-   Versjonstype
-   Dato og klokkeslett
-   Kostnadsregnskapsfinans
-   Regnskapsår
-   Regnskapsperiode

Beregning av indirekte kostnader kjøres uavhengig av versjonen. Derfor kan du beregne budsjettversjonen før den faktiske versjonen. Beregning av indirekte kostnader består av fire trinn, som vist i illustrasjonen nedenfor. I hvert trinn opprettes et journalhode med journaloppføringer. Dette journalhodet inneholder inndataene for hvert beregningstrinn. Policyer og regler som brukes på hver journallinje, og kostposter, genereres som utdata. Derfor må du alltid full sporbarhet. 

[![Beregning av indirekte kostnader](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a>Beregne og tildele den indirekte kostnaden for strøm
I finansbokføring registreres noen kostnader, for eksempel strøm, som et engangsbeløp. Derfor finnes ikke detaljert lederinnsikt for kostnadsregnskap. For å gi riktig lederinnsikt på tvers av alle organisasjonsenheter og nivåer i kostnadsregnskap, må kostnader flyte gjennom organisasjonsenhetene. Denne flyten må være basert på en nøyaktig oversikt over forbruk eller en virkelig vurdering. I økonomimodulen kan en strømkostnad posteres som vist i tabellen nedenfor.

<table>
<thead>
<tr>
<th>Regnskapsdato</th>
<th colspan="2">Kostsenter</th>
<th colspan="2">Hovedkonto</th>
<th>Beløp i regnskapsvalutaen</th>
</tr>
</thead>
<tbody>
<tr>
<td>3. januar 2017</td>
<td>CC099</td>
<td>Standard kostsenter</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>10 000,00</td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a>Trinn 1: Behandle beregning av kostnadsatferd

Når kostnadsoppføringer importeres fra kildedataene, mottar de som standard klassifiseringen **Uklassifisert** for kostnadsatferd i kostnadsregnskap. Ved å bruke policyregler for kostnadsatferd, kan du klassifisere kostnadsoppføringer som **Faste kostnader** eller **Variable kostnader**.

#### <a name="define-the-cost-behavior-rule"></a>Definere regelen for kostnadsatferd

I noen tilfeller er deler av kostnaden et fast gebyr, og restkostnadene er basert på forbruk. Strømregninger samsvarer ofte med denne definisjonen. Når du betaler en bestemt fast gebyr, betaler du for forbruk per kilowattime (kWt). Hvis det faste gebyret for eksempel er 1 000,00, defineres regelen for kostnadsatferd slik:

-   Fast beløp 1 000,00
    -   0 &lt;= 1 000,00 = Fast
    -   1000,01 &lt; N = Variabel

##### <a name="journal"></a>Journalen

<table>
<thead>
<tr>
<th>Journalen</th>
<th>Journaltype</th>
<th colspan="3">Økonomisk kalenderperiode</th>
<th>Versjon</th>
</tr>
</thead>
<tbody>
<tr>
<td>00001</td>
<td>Journal for beregning av kostnadsatferd</td>
<td>Skattemessig</td>
<td>2017</td>
<td>Periode 1</td>
<td>Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)

<table>
<thead>
<tr>
<th>Regnskapsdato</th>
<th colspan="2">Kostnadsobjekt</th>
<th colspan="2">Kostnadselement</th>
<th>Kostnadsatferd</th>
<th>Beløp</th>
</tr>
</thead>
<tbody>
<tr>
<td>3. januar 2017</td>
<td>CC099</td>
<td>Standard kostsenter</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Uklassifisert</td>
<td>10 000,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kostnadsoppføringer

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th colspan="2">Kostnadselement</th>
<th>Kostnadsatferd</th>
<th>Beløp</th>
<th>Regnskapsdato</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Standard kostsenter</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Uklassifisert</td>
<td>10 000,00</td>
<td>3. januar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Standard kostsenter</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Uklassifisert</td>
<td>-10 000,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Standard kostsenter</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>1 000,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Standard kostsenter</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>9,000.00</td>
<td>31. januar 2017</td>
</tr>
</tbody>
</table>

Hvis du vil ha detaljert informasjon om kostnadsatferd, kan du se Policy for kostnadsatferd. (Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.)

### <a name="step-2-process-the-cost-distribution-calculation"></a>Trinn 2: Behandle beregning av kostnadsdistribusjon

Kostnadsdistribusjon brukes til å omfordele kostnadene fra ett kostnadsobjekt til ett eller flere kostnadsobjekter ved å bruke et relevant tildelingsgrunnlag. Forskjellen mellom kostnadsdistribusjon og kostnadsfordeling er at kostnadsdistribusjon alltid skjer på nivået for primærkostnadselementet for den opprinnelige kostnaden.

#### <a name="define-the-cost-distribution-rule"></a>Definere regelen for kostnadsdistribusjon

I finansbokføring registreres ofte strømkostnader som et engangsbeløp. I kostnadsregnskap er ikke denne tilnærmingen detaljert nok. Variable kostnader skal fordeles rettferdig til de individuelle kostnadsobjektene. Det mest logiske tildelingsgrunnlaget er strømforbruket (kWt). Det opprettes et statistisk dimensjonsmedlem med navnet Strøm, og strømforbruket registreres. Som standard blir alle statistiske dimensjonsmedlemmer tilgjengelige som tildelingsgrunnlag.

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th>kWt</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>1 000</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>6,000</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>0</td>
</tr>
</tbody>
</table>

Tabellen nedenfor viser resultatet når strømforbruk brukes som tildelingsgrunnlag for variable kostnader.

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th>Størrelse</th>
<th>Tildelingsfaktor</th>
<th>Beløp</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>1 000</td>
<td>(1 000 ÷ 7 000) × 9 000,00</td>
<td>1,285.71</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>6,000</td>
<td>(6 000 ÷ 7 000) × 9 000,00</td>
<td>7,714.29</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>0</td>
<td>(0 ÷ 7 000) × 9 000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

De faste kostnadene skal fordeles likt på de individuelle kostnadsobjektene som har brukt strøm. Du kan oppnå dette resultatet ved hjelp av det statistiske dimensjonsmedlemmet Strøm i et formeltildelingsgrunnlag: (Strøm &gt; 0,00) Tabellen nedenfor viser resultatet når elektrisitetsforbruk brukes som tildelingsgrunnlag for variable kostnader.

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th>Formel</th>
<th>Størrelse</th>
<th>Tildelingsfaktor</th>
<th>Beløp</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>(1 000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1 000,00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>(6 000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1 000,00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>(0 &gt; 0,00)</td>
<td>0</td>
<td>(0 ÷ 2) × 1 000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Journalen

<table>
<thead>
<tr>
<th>Journalen</th>
<th>Journaltype</th>
<th colspan="3">Økonomisk kalenderperiode</th>
<th>Versjon</th>
</tr>
</thead>
<tbody>
<tr>
<td>00002</td>
<td>Beregningsjournal for kostnadsdistribusjon</td>
<td>Skattemessig</td>
<td>2017</td>
<td>Periode 1</td>
<td>Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)

<table>
<thead>
<tr>
<th>Regnskapsdato</th>
<th colspan="2">Kostnadsobjekt</th>
<th colspan="2">Kostnadselement</th>
<th>Kostnadsatferd</th>
<th>Beløp</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. januar 2017</td>
<td>CC099</td>
<td>Standard kostsenter</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>1 000,00</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>CC099</td>
<td>Standard kostsenter</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>9,000.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kostnadsoppføringer

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th colspan="2">Kostnadselement</th>
<th>Kostnadsatferd</th>
<th>Beløp</th>
<th>Regnskapsdato</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Standard kostsenter</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>-1 000,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>500,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>500,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Standard kostsenter</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>-9 000,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>1,285.71</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>7,714.29</td>
<td>31. januar 2017</td>
</tr>
</tbody>
</table>

Hvis du vil ha detaljert informasjon om kostnadsdistribusjon og tildelingsgrunnlag, kan du se Kostnadsdistribusjonspolicy og Tildelingsgrunnlag. (Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.)

### <a name="step-3-process-the-overhead-rate-calculation"></a>Trinn 3: Behandle beregningen av indirekte kostnader

Satsen for indirekte kostnader brukes til å belaste ett eller flere spesifikke kostnadsobjekter. Tillegget er basert på en forhåndsdefinert kostnadssats og størrelsen fra det tilordnede tildelingsgrunnlaget. 

#### <a name="define-the-overhead-rate"></a>Definer satsen for indirekte kostnader

Kostnadsobjekt CC001 Personale bidrar til et sett med interne prosjekter. Et statistisk dimensjonsmedlem med navnet Personaleprosjekter opprettes for å måle den brukte størrelsen.

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th>Timeantall</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prosj 1</td>
<td>Prosjekt 1</td>
<td>3</td>
</tr>
<tr>
<td>Prosj 2</td>
<td>Prosjekt 2</td>
<td>1</td>
</tr>
</tbody>
</table>

En forhåndsbestemt kostnadssatsen er definert for kostnadsprosjektbidrag.

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th>Kostnadselement</th>
<th>Kostnadsatferd</th>
<th>Enheter</th>
<th>Sats</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>10001</td>
<td>Variabel kostnad</td>
<td>1</td>
<td>10</td>
</tr>
</tbody>
</table>

Tabellen nedenfor viser resultatet når personaleprosjektene brukes som tildelingsgrunnlag.

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th>Størrelse</th>
<th>Kostnadselement</th>
<th>Tildelingsfaktor</th>
<th>Beløp</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prosj 1</td>
<td>Prosjekt 1</td>
<td>3</td>
<td>10001</td>
<td>(3 ÷ 1) × 10,00</td>
<td>30,00</td>
</tr>
<tr>
<td>Prosj 2</td>
<td>Prosjekt 2</td>
<td>1</td>
<td>10001</td>
<td>(1 ÷ 1) × 10,00</td>
<td>10,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Journalen

<table>
<thead>
<tr>
<th>Journalen</th>
<th>Journaltype</th>
<th colspan="3">Økonomisk kalenderperiode</th>
<th>Versjon</th>
</tr>
</thead>
<tbody>
<tr>
<td>00003</td>
<td>Journal for beregning av sats for indirekte kostnader</td>
<td>Skattemessig</td>
<td>2017</td>
<td>Periode 1</td>
<td>Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a>Journaloppføringer (journaloppføringer for beregning av sats for indirekte kostnader)

<table>
<thead>
<tr>
<th>Regnskapsdato</th>
<th colspan="2">Kostnadsobjekt</th>
<th>Størrelse</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. januar 2017</td>
<td>Prosj 1</td>
<td>internt prosj 1</td>
<td>3,00</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>Prosj 2</td>
<td>internt prosj 2</td>
<td>1,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kostnadsoppføringer

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th colspan="2">Kostnadselement</th>
<th>Kostnadsatferd</th>
<th>Beløp</th>
<th>Regnskapsdato</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC0001</td>
<td>Personale</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>-30,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prosj 1</td>
<td>internt prosj 1</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>30,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>-10,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prosj 2</td>
<td>internt prosj 2</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>10,00</td>
<td>31. januar 2017</td>
</tr>
</tbody>
</table>

Hvis du vil ha mer informasjon om policyen for sats for indirekte kostnader, kan du se Policy for sats for indirekte kostnader og Tildelingsgrunnlag. (Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.)

### <a name="step-4-process-the-cost-allocation-calculation"></a>Trinn 4: Behandle beregning av kostnadstildeling

Tildelinger brukes til å tildele saldoen på et kostnadsobjekt til andre kostnadsobjekter ved å bruke et tildelingsgrunnlag. Finance and Operations støtter gjensidig tildelingsmetode. I den gjensidige tildelingsmetoden gjenkjennes fullstendig de gjensidige tjenestene som hjelpekostnadsobjekter utveksler. Systemet fastslår automatisk riktig rekkefølge for tildelingene. Saldoen på et kostnadsobjekt tildeles av ett enkelt tildelingsgrunnlag. Tildelinger på tvers av dimensjoner for kostnadsobjekter og deres respektive medlemmer, støttes. Tildelingsrekkefølgen styres av kostnadskontrollenheten. 

[![Gjensidig metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)

#### <a name="define-the-cost-allocation"></a>Definere kostnadstildelingen

Her er et enkelt eksempel som forklarer hvordan du kan spore kostnadsflyten. Kostnadsobjekt CC001 Personale bidrar til flere kostnadsobjekter. Et statistisk dimensjonsmedlem med navnet Personaletjenester opprettes for å måle den brukte størrelsen.

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th>Personaletjenester</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>35</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>55</td>
</tr>
<tr>
<td>CC004</td>
<td>Innpakning</td>
<td>10</td>
</tr>
</tbody>
</table>

Kostnadsobjekt CC002 Finans bidrar til flere kostnadsobjekter. Et statistisk dimensjonsmedlem med navnet Finanstjenester opprettes for å måle den brukte størrelsen.

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th>Finanstjenester</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>65</td>
</tr>
<tr>
<td>CC004</td>
<td>Innpakning</td>
<td>35</td>
</tr>
</tbody>
</table>

Kostnadsobjekt CC003 Montering bidrar til flere kostnadsobjekter. Et statistisk dimensjonsmedlem med navnet Monteringstjenester opprettes for å måle den brukte størrelsen.

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th>Monteringstjenester (timer)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>60</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>20</td>
</tr>
</tbody>
</table>

Kostnadsobjekt CC004 Emballasje bidrar til flere kostnadsobjekter. Et statistisk dimensjonsmedlem med navnet Emballasjetjenester opprettes for å måle den brukte størrelsen.

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th>Emballasjetjenester (timer)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Produkt 1</td>
<td>Produkt 1</td>
<td>80</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>15</td>
</tr>
</tbody>
</table>

**Obs!** I Finance and Operations kan statistiske målinger, som produksjonstimer som produktet bruker, avledes fra kildedataene. Hvis du vil ha mer informasjon om statistiske målleverandører, kan du se Maler for leverandør av statistisk måling. (Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.) Tabellen nedenfor viser resultatet når personaletjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th>Størrelse</th>
<th>Tildelingsfaktor</th>
<th>Beløp</th>
<th>Kostnadsatferd</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>35</td>
<td>(35 ÷ 100) × 500,00</td>
<td>175.00</td>
<td>Fast kostnad</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>55</td>
<td>(55 ÷ 100) × 500,00</td>
<td>275.00</td>
<td>Fast kostnad</td>
</tr>
<tr>
<td>CC004</td>
<td>Innpakning</td>
<td>10</td>
<td>(10 ÷ 100) × 500,00</td>
<td>50,00</td>
<td>Fast kostnad</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>35</td>
<td>(35 ÷ 100) × 1 245,71</td>
<td>436.00</td>
<td>Variabel kostnad</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>55</td>
<td>(55 ÷ 100) × 1 245,71</td>
<td>685.14</td>
<td>Variabel kostnad</td>
</tr>
<tr>
<td>CC004</td>
<td>Innpakning</td>
<td>10</td>
<td>(10 ÷ 100) × 1 245,71</td>
<td>124.57</td>
<td>Variabel kostnad</td>
</tr>
</tbody>
</table>

Tabellen nedenfor viser resultatet når finanstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th>Størrelse</th>
<th>Tildelingsfaktor</th>
<th>Beløp</th>
<th>Kostnadsatferd</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>65</td>
<td>(65 ÷ 100) × (500,00 + 175,00)</td>
<td>438.75</td>
<td>Fast kostnad</td>
</tr>
<tr>
<td>CC004</td>
<td>Innpakning</td>
<td>35</td>
<td>(35 ÷ 100) × (500,00 + 175,00)</td>
<td>236.25</td>
<td>Fast kostnad</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>65</td>
<td>(65 ÷ 100) × (7 714,29 + 436,00)</td>
<td>5,297.69</td>
<td>Variabel kostnad</td>
</tr>
<tr>
<td>CC004</td>
<td>Innpakning</td>
<td>35</td>
<td>(35 ÷ 100) × (7 714,29 + 436,00)</td>
<td>2,852.60</td>
<td>Variabel kostnad</td>
</tr>
</tbody>
</table>

Tabellen nedenfor viser resultatet når monteringstjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th>Størrelse</th>
<th>Tildelingsfaktor</th>
<th>Beløp</th>
<th>Kostnadsatferd</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>60</td>
<td>(60 ÷ 80) × (275,00 + 438,75)</td>
<td>535.31</td>
<td>Fast kostnad</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>20</td>
<td>(20 ÷ 80) × (275,00 + 438,75)</td>
<td>178.44</td>
<td>Fast kostnad</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>60</td>
<td>(60 ÷ 80) × (5 297,69 + 685,14)</td>
<td>4,487.12</td>
<td>Variabel kostnad</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>20</td>
<td>(20 ÷ 80) × (5 297,69 + 685,14)</td>
<td>1,495.71</td>
<td>Variabel kostnad</td>
</tr>
</tbody>
</table>

Tabellen nedenfor viser resultatet når emballasjetjenestene brukes som tildelingsgrunnlag for totale kostnader (faste kostnader og variable kostnader).

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th>Størrelse</th>
<th>Tildelingsfaktor</th>
<th>Beløp</th>
<th>Kostnadsatferd</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>80</td>
<td>(80 ÷ 95) × (50,00 + 236,25)</td>
<td>241.05</td>
<td>Fast kostnad</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>15</td>
<td>(15 ÷ 95) × (50,00 + 236,25)</td>
<td>45.20</td>
<td>Fast kostnad</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>80</td>
<td>(80 ÷ 95) × (2 852,60 + 124,57)</td>
<td>2,507.09</td>
<td>Variabel kostnad</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>15</td>
<td>(15 ÷ 95) × (2 852,60 + 124,57)</td>
<td>470.08</td>
<td>Variabel kostnad</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Journaloppføringer (journaloppføringer for saldo for kostnadsobjekt)

<table>
<thead>
<tr>
<th>Journalen</th>
<th>Journaltype</th>
<th colspan="3">Økonomisk kalenderperiode</th>
<th>Versjon</th>
</tr>
</thead>
<tbody>
<tr>
<td>00004</td>
<td>Kostfordelingsjournal</td>
<td>Skattemessig</td>
<td>2017</td>
<td>Periode 1</td>
<td>Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a>Journallinjer

<table>
<thead>
<tr>
<th>Regnskapsdato</th>
<th colspan="2">Kostnadsobjekt</th>
<th colspan="2">Kostnadselement</th>
<th>Kostnadsatferd</th>
<th>Beløp</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. januar 2017</td>
<td>CC001</td>
<td>Personale</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>500,00</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>CC001</td>
<td>Personale</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>1,245.71</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>675.00</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>8,150.29</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>713.75</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>5,982.83</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>CC003</td>
<td>Innpakning</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>286.25</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>CC003</td>
<td>Innpakning</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>2,977.17</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>776.36</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>6,994.21</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>Prod 2</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>223.64</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>Prod 2</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>1,965.79</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kostnadsoppføringer

<table>
<thead>
<tr>
<th colspan="2">Kostnadsobjekt</th>
<th colspan="2">Kostnadselement</th>
<th>Kostnadsatferd</th>
<th>Beløp</th>
<th>Regnskapsdato</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>-500,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>175.00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>275.00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Innpakning</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>50,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>-1 245,71</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>436.00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>685.14</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Innpakning</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>124.57</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>-675,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>438.75</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Innpakning</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>236.25</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>-8 150,29</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>5,297.69</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Innpakning</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>2,852.60</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>-713,75</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>535.31</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>178.44</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>-5 982,83</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>4,487.12</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>1,495.71</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>-286,25</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>241.05</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Fast kostnad</td>
<td>45.20</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>-2 977,17</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Produkt 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>2,507.09</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>10001</td>
<td>Elektrisitet</td>
<td>Variabel kostnad</td>
<td>470.08</td>
<td>31. januar 2017</td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a>Konklusjon
I finansbokføring blir en kostnad på 10 000,00 for strøm postert til en midlertidig kostnadssenter-ID. Derfor vet regnskapsførere at denne kostnaden må tildeles. I kostnadsregnskap flyter kostnadene på tvers av organisasjonsenheter og -nivåer, basert på policyene og reglene som brukes. Hver kostnad er tilknyttet et tildelingsgrunnlag som gir best mulig vurdering for kostnadsfordelingen.

<table>
<thead>
<tr>
<th colspan="2" rowspan="2">Kostnadselement</th>
<th colspan="9">Kostnadsobjekt</th>
<th rowspan="2">Sum</th>
</tr>
<tr>
<th>CC099</th>
<th>CC001</th>
<th>CC002</th>
<th>CC003</th>
<th>CC004</th>
<th>Prosj 1</th>
<th>Prosj 2</th>
<th>Prod 1</th>
<th>Prod 2</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">10001 Strøm</td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><strong>30,00</strong></td>
<td style="text-align: right;"><strong>10,00</strong></td>
<td style="text-align: right;"><strong>7.770,57</strong></td>
<td style="text-align: right;"><strong>2.189,43</strong></td>
<td style="text-align: right;"><strong>10.000,00</strong></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;">Uklassifisert</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">Fast kostnad</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;">776.36</td>
<td style="text-align: right;">223.64</td>
<td style="text-align: right;"><strong>1.000,00</strong></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">Variabel kostnad</td>
<td style="text-align: right;">000</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">30,00</td>
<td style="text-align: right;">10,00</td>
<td style="text-align: right;">6,994.21</td>
<td style="text-align: right;">1,965.79</td>
<td style="text-align: right;"><strong>9.000,00</strong></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Dette emnet beskriver hvordan et primærkostnadselementet, 10001 Strøm, flyter gjennom kostnadsobjektene. Denne indirekte kostnaden tildeles derfor til det laveste nivået i organisasjonen. Med andre ord vil kostnadsobjektene på laveste nivå bære kostnaden. Hvis du trenger en visuell flyt for kostnaden mellom kostnadsobjektene, kan du bruke policyreglene for kostnadsakkumulering til å visualisere kostnadsflyten. Hvis du vil ha mer informasjon, kan du se policyen for kostnadsakkumulering. (Vær oppmerksom på at dette emnet er ikke fullføre ennå, men kommer snart.)





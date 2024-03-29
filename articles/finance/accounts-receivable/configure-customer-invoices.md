---
title: Opprette en kundefaktura
description: En kundefaktura for en salgsordre er en regning som er knyttet til et salg, og som en organisasjon gir til en kunde.
author: ShivamPandey-msft
ms.date: 03/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0d1221e07f6dc4a5a99aa205c4a7f6fb367f000
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780502"
---
# <a name="create-a-customer-invoice"></a>Opprette en kundefaktura

[!include [banner](../includes/banner.md)]

En **Kundefaktura for en salgsordre** er en regning som er knyttet til et salg, og som en organisasjon gir til en kunde. Denne typen kundefaktura opprettes basert på en salgsordre, som inneholder ordrelinjer og varenumre. Varenumrene er spesifisert og postert i finans. Underfinansjournaloppføringer er ikke tilgjengelig for en kundefaktura for en salgsordre. Hvis du vil ha mer informasjon, kan du se [Opprette salgsordrefakturaer](tasks/create-sales-order-invoices.md).

En **Fritekstfaktura** er ikke relatert til en salgsordre. Den inneholder ordrelinjer som omfatter finanskontoer, fritekstbeskrivelser og et salgsbeløp som du angir. Du kan ikke legge inn et varenummer i denne fakturatypen. Du må legge inn riktige mva-opplysninger. En hovedkonto for salg er angitt i hver fakturalinje, som du kan distribuere til flere finanskontoer ved å klikke **Fordel beløp** på siden **Fritekstfaktura**. I tillegg posteres kundesaldoen til samlekontoen fra posteringsprofilen som brukes for fritekstfakturaen.

Hvis du vil ha mer informasjon, kan du se:
 - [Opprett fritekstfakturaer](../accounts-receivable/create-free-text-invoice-new.md)
 - [Opprette en mal for fritekstfaktura](../accounts-receivable/create-free-text-invoice-template-new.md)
 - [Tilordne mal for fritekstfaktura til en kunde](tasks/assign-free-text-invoice-template-customer.md)
 - [Generere og postere gjentakende fritekstfakturaer](tasks/post-recurring-free-text-invoices.md)


En **Proformafaktura** er en faktura som er klargjort som et estimat av de faktiske fakturabeløpene før fakturaen posteres. Du kan skrive ut en **Proformafaktura** for en kundefaktura for en salgsordre eller for en fritekstfaktura. 

>[!NOTE]
> Hvis det oppstår et systemavbrudd i salgsprosessen med en proformafaktura, kan proformafakturaen bli frittstående. Du kan slette en frittstående proformafaktura ved å kjøre den periodiske jobben **Slett proformafakturaer manuelt**. Gå til **Salg og markedsføring > Periodiske oppgaver > Rydd opp > Slett proformafakturaer manuelt**.

## <a name="using-sales-order-customer-invoice-data-entities"></a>Bruke kundefakturadataenheter for salgsordre
Du kan bruke dataenheter til å importere og eksportere informasjon om en kundefaktura for en salgsordre. Det er forskjellige enheter for informasjonen i salgsfakturahodet og salgsfakturalinjene.

Følgende enheter er tilgjengelige for informasjonen i salgsfakturahodet:

- Enheten **Journalhode for salgsfaktura** (SalesInvoiceJournalHeaderEntity)
- Enheten **Salgsfakturahoder V2** (SalesInvoiceHeaderV2Entity)

Vi anbefaler at du bruker enheten **Journalhode for salgsfaktura**, fordi dette gir en mer gjennomførbar opplevelse for import og eksport av salgshode. Denne enheten inneholder ikke kolonnen **Mva-beløp** (INVOICEHEADERTAXAMOUNT), som representerer mva-verdien i salgsfakturahodet. Hvis forretningsscenarioet krever denne informasjonen, bruker du enheten **Salgsfakturahoder V2** til å importere og eksportere informasjon om salgsfakturahodet.

Følgende enheter er tilgjengelige for informasjonen i salgsfakturalinjer:

- Enheten **Kundefakturalinjer** (BusinessDocumentSalesInvoiceLineItemEntity)
- Enheten **Salgsfakturalinjer V3** (SalesInvoiceLineV3Entity)

Når du skal avgjøre hvilken linjeenhet som skal brukes til eksportering, må du vurdere om det skal brukes en fullstendig fremskyvning eller en trinnvis fremskyvning. I tillegg må du vurdere datasammensetningen. Enheten **Salgsfakturalinjer V3** støtter mer komplekse scenarioer (for eksempel tilordning til beholdningsfeltene). Det støtter også eksportscenarioer med fullstendig fremskyvning. For trinnvise fremskyvninger anbefaler vi at du bruker enheten **Kundefakturalinjer**. Denne enheten inneholder en mye enklere datasammensetning enn enheten **Salgsfakturalinjer V3**, og er foretrukket, spesielt hvis integrering av lagerfelt ikke er nødvendig. På grunn av forskjeller i tilordningsstøtte mellom linjeenhetene har enheten **Kundefakturalinjer** vanligvis raskere ytelse enn enheten **Salgsfakturalinjer V3**.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Postere og skrive ut individuelle kundefakturaer som er basert på salgsordrer
Bruk denne fremgangsmåten til å opprette en faktura som er basert på en salgsordre. Du kan gjøre dette hvis du beslutter å fakturere kunden før du leverer varene eller tjenestene. 

Når du posterer en faktura, oppdateres **Fakturarest**-antallet for hver vare med totalantallet som er fakturert fra den valgte salgsordren. Hvis både **Fakturarest**-antallet og **Gjenstående levering**-antallet for alle varer på salgsorden er 0 (null), endres statusen for salgsorden til **Fakturert**. Hvis **Fakturarest**-antallet ikke er 0 (null), endres ikke statusen for salgsordren, og flere fakturaer kan registreres på den.

Du kan vise statusen for salgsordrene på listesiden **Alle salgsordrer**. Bruk listesiden **Åpne kundefakturaer** til å vise fakturaene du har postert.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Postere og skrive ut individuelle kundefakturaer som er basert på følgesedler og datoen
Bruk denne fremgangsmåten når én eller flere følgesedler er postert for salgsordren. Kundefakturaen er basert på disse følgesedlene og gjenspeiler antallet i dem. Finansinformasjonen for fakturaen er basert på informasjonen du angir når du posterer fakturaen. 

Du kan opprette en kundefaktura som er basert på følgeseddellinjevarene som er levert til nå, selv om ikke alle varene i en bestemt salgsordre er levert. Du kan for eksempel gjøre dette hvis den juridiske enheten din sender ut én faktura per kunde per måned som dekker alle forsendelser du sender i løpet av den måneden. Hver følgeseddel representerer en delvis eller komplett forsendelse av varene i salgsordren. 

Når du posterer fakturaen, oppdateres **Fakturarest**-antallet for hver vare med totalantallet som er levert for de valgte følgesedlene. Hvis både **Fakturarest**-antallet og **Gjenstående levering**-antallet for alle varer på salgsorden er 0 (null), endres statusen for salgsorden til **Fakturert**. Hvis **Fakturarest**-antallet ikke er 0 (null), endres ikke statusen for salgsordren, og flere fakturaer kan registreres på den. 

Lagertransaksjoner oppdateres med fakturanummeret, og statusen i **Linjestatus**-feltet på salgsordren endres til **Fakturert**. 

Vis statusen for salgsordrene på listesiden **Alle salgsordrer**.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Konsolidere salgsordrer eller følgesedler for postering
Bruk denne fremgangsmåten når én eller flere salgsordrer er klare til fakturering, og du vil konsolidere dem i én enkelt faktura. 

Du kan velge flere fakturaer på **Salgsordre**-listesiden og deretter bruke **Generer fakturaer** for å konsolidere dem. På siden **Postering av faktura** kan du endre innstillingen **Samleordre** for å summere etter ordrenummer (der det finnes flere følgesedler for én enkelt ordre) eller etter fakturakonto (der det er flere salgsordrer for én enkelt fakturakonto). Bruk knappen **Ordne** for å konsolidere salgsordrer til enkeltfakturaer basert på **Samleordre**-innstillingene.

## <a name="split-sales-order-invoices-by-site-and-delivery-information"></a>Dele salgsordrefakturaer etter område og leveringsinformasjon
Du kan konfigurere delingen av salgsordrekundefakturaer etter område eller leveringsadresse i fanen **Samleoppdatering** på siden **Parametere for kundereskontro**. 
 - Velg alternativet **Deling basert på fakturaområde** for å opprette én faktura per område når du posterer. 
 - Velg alternativet **Deling basert på leveringsinformasjon for faktura** for å opprette én faktura per leveringsadresse for salgsordrelinje ved postering. 

## <a name="post-to-revenue-account-for-sales-order-lines-that-have-no-price-and-no-cost"></a>Poster til inntektskonto for salgsordrefakturalinjer som ikke har en pris og ingen kostnad
Du kan oppdatere **Inntekt**-kontoen i **Økonomimodul** for salgsordrelinjer som ikke har noen pris og ingen kostnad. 

Slik definerer eller viser du denne informasjonen:
1. Gå til parameteren **Poster til inntektskonto for salgsordrefakturalinjer med nullpris og nullkostnad** i fanen **Finans og merverdiavgift** på siden **Kundeparametere**. (**Kunder > Oppsett > Kundeparametere**). 
2. Velg **Ja** for å oppdatere **Inntekt**-kontoen for salgsordrefakturalinjer som ikke har noen pris og ingen kosntad. 
 - Hvis du velger dette alternativet, vil bilaget inneholde 0,00 oppføringstypene **Kundesaldo** og **Inntekt**. En inntektskonto er definert på parametersiden **Lagerpostering** i fanen for definisjon av **Salgsordre**-kontoen. 
 - Hvis dette alternativet ikke er valgt, posteres ikke linjer som ikke har pris- eller kostnadsinformasjon, til **Inntekt**-kontoen. I stedet vil bilaget inneholde en oppføring på 0,00 for posteringstypen **Kundesaldo**.

## <a name="line-creation-sequence-number-information"></a>Informasjon om sekvensnummer for linjeoppretting
Når du posterer kundefakturalinjer, har du muligheten til å opprette sekvensielle linjeopprettingsserienumre. Linjeopprettingssekvensnumre tilordnes under posteringsprosessen. Ved å tillate ikke-sekvensiell nummerering kan du få hjelp til å forbedre ytelsen til kundefakturapostering. Linjeopprettingsserienumre kan brukes av tredjepartsintegrering som forventer sekvensiell bestilling. Forhør deg med IT-avdelingen om eventuelle utvidelser som kan integreres med sekvensnumre for linjeoppretting.

Hvis du vil definere eller vise denne informasjonen, går du til siden **Parametere for kundereskontro**, **Oppdateringer**-fanen, og angir alternativet **Tildel sekvensielle linjenumre ved postering av kundefakturalinjer**:

- Sett alternativet til **Nei** hvis du vil bruke ikke-sekvensiell nummerering for serienumre for linjeoppretting.
- Sett alternativet til **Ja** for å bruke sekvensiell nummerering. Du må velge **Ja** for juridiske enheter som har hovedadresse i Italia. Du må også sette det til **Ja** hvis testversjonen **CustInvoiceTransRandLineCreationSeqNumFlight** er deaktivert.

## <a name="additional-settings-that-change-the-posting-behavior"></a>Tilleggsinnstillinger som endrer posteringsvirkemåten
Følgende felt endrer virkemåten for posteringsprosessen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Felt</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Antall</td>
<td>Velg antallsinformasjonen som dokumentposteringen skal baseres på. Alternativene som er tilgjengelige, varierer avhengig av typen dokument du posterer, for eksempel en følgeseddel eller en faktura.
<ul>
<li><strong>Lever nå</strong> – Velg alle antall som er angitt i feltet <strong>Lever nå</strong>. Bruk dette alternativet til å bekrefte eller levere en delordre.</li>
<li><strong>Plukket</strong> – Velg alle antall som er plukket.</li>
<li><strong>Alle</strong> – Velg alle antall på salgsordren som ennå ikke er oppdatert med den gjeldende dokumenttypen.</li>
<li><strong>Følgeseddel</strong> – Velg alle antall som er blitt oppdatert av en følgeseddel.</li>
<li><strong>Plukket antall og ikke-lagerførte produkter</strong> – Velg alle antall som er plukket og alle produktantall som ikke er lagerført.</li>
</ul></td>
</tr>
<tr class="even">
<td>Posterer</td>
<td><ul>
<li>Velg dette alternativet for å journalføre salgsordren.</li>
<li>Fjern merket for å skrive ut en proformasalgsordre. <strong>Obs!</strong> Hvis du har gjort en avtale for en betalingsplan, blir ikke betalingsplanen vist på proformasalgsordren. Betalingsplaner vises bare på faktiske salgsordrer.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Senere valg</td>
<td>Velg dette alternativet hvis du vil bruke spørringen senere. Dette alternativet brukes for satsvise jobber. Spørringen kjøres når den satsvise jobben kjøres.</td>
</tr>
<tr class="even">
<td>Reduser antall</td>
<td>Velg dette alternativet for å automatisk redusere det leverte antallet når dokumentet posteres, slik at det leverte antallet er lik det tilgjengelige lageret.</td>
</tr>
<tr class="odd">
<td>Skriv ut</td>
<td>Velg når dokumenter skal skrives ut:
<ul>
<li><strong>Gjeldende</strong> – Skriv ut dokumenter etter at hver faktura er oppdatert.</li>
<li><strong>Etter</strong> – Skriv ut dokumenter når alle fakturaene er oppdatert.</li>
</ul>
<strong>Obs!</strong> <strong>Skriv ut</strong>-feltet er bare tilgjengelig hvis du velger <strong>Skriv ut faktura</strong>, <strong>Skriv ut bekreftelse</strong>, <strong>Skriv ut plukkliste</strong> eller <strong>Skriv ut følgeseddel</strong>. På siden <strong>Skjemasortering</strong> definerer du at informasjonen skal sorteres etter fakturakonto i systemet. Du kan deretter velge <strong>Etter</strong> for å skrive ut dokumentene i en bunke som sorteres etter fakturakonto. Hvis ikke skrives dokumentene ut før behandlingen er fullført, og dokumentene sorteres ikke i rekkefølgen som er angitt på siden <strong>Skjemasortering</strong>.</td>
</tr>
<tr class="even">
<td>Skriv ut faktura</td>
<td>Merk av i denne boksen for å skrive ut fakturaen. Hvis dette alternativet er deaktivert, kan du postere en faktura uten å skrive ut den.</td>
</tr>
<tr class="odd">
<td>Send e-post</td>
<td>Velg dette alternativet for å sende fakturaen for en salgsordre til kunden som et e-postvedlegg når fakturaen er postert. Vedlegg sendes som PDF- og XML-filer. Dette alternativet er bare tilgjengelig hvis du velger alternativet <strong>Aktiver CFD (elektroniske fakturaer)</strong> på siden <strong>Parametere for elektroniske fakturaer</strong>. <strong>Obs!</strong> (MEX) Denne kontrollen er bare tilgjengelig for juridiske enheter med primæradresse i Mexico.</td>
</tr>
<tr class="even">
<td>Bruk utskriftsbehandlingsmål</td>
<td>Velg dette alternativet for å bruke utskriftsinnstillingene som er angitt for transaksjonen, dokumentet eller modulen på siden <strong>Oppsett for utskriftsbehandling</strong>.</td>
</tr>
<tr class="odd">
<td>Kontroller kredittgrense</td>
<td>Velg informasjonen som skal analyseres når en kredittgrensekontroll utføres.
<ul>
<li><strong>Ingen</strong> – Det finnes ingen krav til kontroll av kredittgrense.</li>
<li><strong>Saldo</strong> - Kredittgrensen kontrolleres mot kundesaldoen.</li>
<li><strong>Saldo + følgeseddel eller produktkvittering</strong> – Kredittgrensen kontrolleres mot kundesaldoen og leveranser.</li>
<li><strong>Saldo+Alt</strong> - Kredittgrensen kontrolleres mot kundesaldoen, leveranser og åpne ordrer.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kreditrettelse</td>
<td>Velg dette alternativet for å vise kreditnotaen som debet i bilagstransaksjonene.</td>
</tr>
<tr class="odd">
<td>Kreditrestantall</td>
<td>Hvis du posterer en kreditnota, velger du dette alternativet for å beholde det resterende antallet på ordren. Hvis dette alternativet ikke er valgt, settes det gjenstående antallet til 0 (null).</td>
</tr>
<tr class="even">
<td>Samleoppdatering for</td>
<td>Velg hvordan flere salgsordrer skal summeres:
<ul>
<li><strong>Ingen</strong> – Ikke oppsummer salgsordrer. En egen faktura opprettes eksempelvis for hver salgsordre.</li>
<li><strong>Fakturakonto</strong> – Oppsummer alle valgte ordrer i henhold til kriteriene som er angitt på siden <strong>Parametere for samleoppdatering</strong>.</li>
<li><strong>Ordre</strong> – Summer et valgt intervall av ordrer, i én angitt ordre. Ordrene oppsummeres i henhold til kriteriene som er angitt på siden <strong>Parametere for samleoppdatering</strong>. Hvis du velger dette alternativet, må du velge en verdi i feltet <strong>Salgsordre</strong>.</li>
<li><strong>Automatisk oppsummering</strong> – Hvis samleoppdateringer er angitt på siden <strong>Samleoppdatering</strong>, oppsummeres alle valgte ordrer basert på kriteriene som er angitt på siden <strong>Parametere for samleoppdatering</strong>. Hvis det ikke er angitt samleoppdateringer, posteres ordren separat.</li>
<li><strong>Følgeseddel</strong> – Summer et valgt intervall av ordrer i én faktura per følgeseddel. Dette alternativet er bare tilgjengelig hvis <strong>Følgeseddel</strong> er valgt i <strong>Antall</strong>-feltet.</li>
</ul></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

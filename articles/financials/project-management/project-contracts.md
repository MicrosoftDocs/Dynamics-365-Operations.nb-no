---
title: Prosjektkontrakter
description: "Dette emnet beskriver og gir eksempler på prosjektkontrakter som du kan opprette for forskjellige typer prosjekter og finansieringskilder, og hvordan du kan behandle kontrakter og fakturere prosjektkunder i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3a1bfd4bd5f396c05277159ac112eaa8197d5818
ms.openlocfilehash: c8328bd2d93bbe763e629248edc1b7b4576005ae
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="project-contracts"></a>Prosjektkontrakter

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver og gir eksempler på prosjektkontrakter som du kan opprette for forskjellige typer prosjekter og finansieringskilder, og hvordan du kan behandle kontrakter og fakturere prosjektkunder i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

Prosjekttypen du oppretter for en prosjektkontrakt, fastsetter metoden som brukes til å fakturere prosjektkunder. Du kan endre en prosjektkontrakt og det tilknyttede prosjektet, men du kan ikke endre prosjekttypen. 

Ved å bruke en prosjektkontrakt kan du fakturere ett eller flere prosjekter samtidig. Prosjektkontrakten bidrar også til å sikre en enhetlig faktureringsprosedyre på hvert underprosjekt i en prosjektstruktur. 

Hvert prosjekt som faktureres, må være tilknyttet en prosjektkontrakt. Innstillingene for en prosjektkontrakt gjelder alle prosjekter og underprosjekter som er tilknyttet prosjektkontrakten. 

En prosjektkontrakt kan angi en eller flere kilder for finansiering. Derfor kan du dele fakturering mellom flere kapitalinnskytere, definere finansieringsgrenser slik at finansieringskilder ikke faktureres mer enn et bestemt beløp, og konfigurere finansieringsregler for belastning av utgifter.

## <a name="funding-for-project-contracts"></a>Finansiering for prosjektkontrakter
Noen prosjektkontrakter angir at flere parter deler ansvaret for finansiering av prosjektkostnadene. Her er noen eksempler:

-   En stor kunde som har flere avdelinger, ber om at finansiering for et prosjekt deles opp etter avdeling.
-   Firmaet ditt deler kostnadene for et stort prosjekt med en ekstern organisasjon.
-   Et veiprosjekt er delfinansiert av to kommuner.
-   Et broprosjekt finansieres av offentlige tilskudd og et privat selskap.

I Finance and Operations kan du dele faktureringen for en enkelt transaksjon eller et helt prosjekt blant flere kunder, tilskudd eller organisasjoner. 

I prosjekter som har flere kapitalinnskytere, kalles alle parter som bidrar til finansieringen av et avansert finansieringsprosjekt, finansieringskilder. Når en kunde, en organisasjon eller et tilskudd er definert som en finansieringskilde, kan den/det tilordnes til én eller flere finansieringsregler. Finansieringsregler inneholder kriteriene som bestemmer hvordan tillegg tilordnes de forskjellige finansieringskildene for et prosjekt. 

Fordi lagerførte varer, blant annet de som vises på innkjøpsrekvisisjoner og bestillinger, ikke kan deles, kan ikke kostnadsbeløpet deles mellom flere finansieringskilder ved distribusjon. Finansieringskildeverdien forblir derfor 0 (null) helt til lageravgangen er postert. Når lageravgangen er postert, fordeles kostnadsbeløpet i henhold til reglene for kontodistribusjon for prosjektet.

Her er noen fremgangsmåter du kan bruke for å gjøre det enklere å dele faktureringen mellom flere finansieringskilder:

-   Angi at alle transaksjoner som er angitt for et prosjekt, bruker den samme salgsvalutaen som prosjektkontrakten.
-   Sett opp finansieringsgrenser slik at en finansieringskilde ikke faktureres mer enn et angitt beløp mot et prosjekt.
-   Konfigurer finansieringsregler og finansieringsgrenser for hver arbeider, vare, kategori, kategorigruppe og transaksjonstype (eller for alle transaksjonstyper).
-   Velg valgfrie start- og sluttdatoer for å definere perioden når hver finansieringsregel er gyldig.
-   Angi prosentdelen som hver finansieringskilde er ansvarlig for.
-   Angi hvilken finansieringskilde som er ansvarlig for avrundingsdifferanser som skyldes finansieringstildelingsberegninger.
-   Definer regler som bestemmer hvordan prosjektkostnader faktureres til eksterne kunder og belastes interne organisasjoner.
-   Registrer transaksjoner på finansieringskonto på vent til ytterligere finansiering kan anskaffes, eller til du beslutter å bære kostnadene internt.

For å fastsette hvilken avgiftsgruppe som skal knyttes til en transaksjon, søkes det etter en mva-gruppetilordning i prosjektet. Hvis ingen mva-gruppetilordning er gjort på prosjektnivå, søkes det i prosjektkontrakten.

### <a name="example-multiple-funding-sources-simple"></a>Eksempel: Flere finansieringskilder (enkel)

Tabellen nedenfor gir scenarier for behandling av finansieringskildetilordning mellom flere finansieringskilder. Disse scenariene er basert på følgende forutsetninger:

-   Prioritetsinnstillingene tas med i tildelingen av midler før andre finansieringsregelkriterier brukes.
-   Ingen datointervall er angitt for å definere perioden d når finansieringsregelen gjelder.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenario</strong></td>
<td><strong>Finansieringskilde </strong></td>
<td><strong>Tildelingsprosent </strong></td>
<td><strong>Tildelingsprioritet </strong></td>
</tr>
<tr class="even">
<td>Du vil tildele kostnader til én finansieringskilde før midlene er oppbrukt, tildele kostnader til en finansieringskilde nummer to før midlene er oppbrukt, og til slutt tildele de gjenstående kostnadene til en tredje finansieringskilde.</td>
<td><ul>
<li>Finansierinskilde 1</li>
<li>Finansieringskilde 2</li>
<li>Finansieringskilde 3</li>
</ul></td>
<td><ul>
<li>100 %</li>
<li>100 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Du ønsker å tildele 75 prosent av kostnadene til én finansieringskilde og 25 prosent til en annen finansieringskilde. Når disse finansieringskildene er oppbrukt, vil du betale de gjenstående kostnadene fra en tredje finansieringskilde.</td>
<td><ul>
<li>Finansierinskilde 1</li>
<li>Finansieringskilde 2</li>
<li>Finansieringskilde 3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Du ønsker å tildele 75 prosent av kostnadene til én finansieringskilde og 25 prosent til en annen finansieringskilde. Når disse finansieringskildene er oppbrukt, ønsker du å dele de gjenstående kostnadene mellom en tredje finansieringskilde og en fjerde finansieringskilde.</td>
<td><ul>
<li>Finansierinskilde 1</li>
<li>Finansieringskilde 2</li>
<li>Finansieringskilde 3</li>
<li>Finansieringskilde 4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Du ønsker å tildele de første 25 prosentene av kostnadene til én finansieringskilde og resten til en finansieringskilde nummer to.</td>
<td><ul>
<li>Finansierinskilde 1</li>
<li>Finansieringskilde 2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Eksempel: Flere finansieringskilder (kompleks)

Du har tre finansieringskilder som du vil bruke i følgende rekkefølge:

1.  Bruk finansieringskilde 2 og finansieringskilde 3 likt helt til finansieringskilde 2 er oppbrukt.
2.  Fortsett å bruke finansieringskilde 3 helt til den er oppbrukt.
3.  Bruk finansieringskilde 1 når finansieringskilde 3 er oppbrukt.

For å nå dette målet må du gjøre følgende:

-   Definere finansieringsgrenser for finansieringskilde 2 og finansieringskilde 3 for de respektive beløpene.
-   Opprette følgende finansieringsregler:
    -   Regel 1 (prioritet 1): Tildele 50 prosent av transaksjoner til finansieringskilde 2 og 50 prosent til finansieringskilde 3.
    -   Regel 2 (prioritet 2): Fordele 100 prosent av transaksjoner til finansieringskilde 3.
    -   Regel 3 (prioritet 3): Fordele 100 prosent av transaksjoner til finansieringskilde 1.

Dette oppsettet fungerer fordi transaksjoner er kontrollert mot reglene og begrensningene for å finne ut om noen av dem gjelder for transaksjonen. Hvis ingen bestemte regler eller begrensninger gjelder for transaksjonen, gjelder Alle transaksjoner-regelen. Alle transaksjoner-regelen samsvarer med alle transaksjoner. 

Hvis det finnes en regel som samsvarer med en transaksjon, brukes prosenten som er tildelt regelen, først, men bare etter at treffene er kontrollert mot eventuelle begrensninger som er angitt. Hvis en grense er nådd og en finansieringskildes midler er oppbrukt, ignoreres finansieringsregelen som er tilknyttet finansieringsgrensen, og det søkes automatisk etter den neste regelen som gjelder. 

I noen tilfeller kan du fordele bare en del av en transaksjon under en regel. Dette kan skje fordi en grense nås når transaksjonen er tildelt. I så fall tildeles bare et bestemt beløp i henhold til denne regelen, for eksempel 50 prosent til hver finansieringskilde. Dette er tilfelle i regelen 1, som er beskrevet tidligere i denne delen. Resten tildeles i henhold til den neste regelen i sekvensen. 

Tabellen nedenfor illustrerer dette scenarioet mer detaljert.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fokus </strong></td>
<td><strong>Detaljer</strong></td>
</tr>
<tr class="even">
<td>Finansieringsregler</td>
<td><ul>
<li>Regel 1 (prioritet 1): Alle transaksjoner. Tildel finansieringskilde 2 med 50 % og finansieringskilde 3 med 50 %.</li>
<li>Regel 2 (prioritet 2): Alle transaksjoner. Tildel finansieringskilde 3 med 100 %.</li>
<li>Regel 3 (prioritet 2): Alle transaksjoner. Tildel finansieringskilde 1 med 100 %.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Finansieringsgrenser</td>
<td><ul>
<li>Finansieringskilde 1-grense = 10 000,00</li>
<li>Finansieringskilde 2-grense = 500,00</li>
<li>Finansieringskilde 3-grense = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transaksjon 1</td>
<td><strong>Transaksjonsbeløp:</strong> 100,00<strong>Finansiering:</strong> Transaksjonen betales bare i henhold til regel 1, fordi transaksjonen betales i sin helhet når regel 1 er brukt. Transaksjonen finansieres likt mellom finansieringskilde 2 og finansieringskilde 3.
<ul>
<li>Finansieringskilde 2: 50,00</li>
<li>Finansieringskilde 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transaksjon 2</td>
<td><strong>Transaksjonsbeløp</strong>: 5 000,00<strong>Finansiering</strong>: Transaksjonen betales i henhold til alle tre regler. <strong>Regel 1</strong>
<ul>
<li>Finansieringskilde 2: 450,00</li>
<li>Finansieringskilde 3: 450,00</li>
</ul>
<strong>Regel 2</strong>
<ul>
<li>Finansieringskilde 3: 250,00 (= 750,00 - 50,00 - 450,00)</li>
</ul>
<strong>Regel 3</strong>
<ul>
<li>Finansieringskilde 1: 3 850,00 (= 5 000,00 - 450,00 - 450,00 - 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Totale midler som fordeles for hver finansieringskilde</td>
<td><ul>
<li>Finansieringskilde 1: 3 850,00</li>
<li>Finansieringskilde 2: 500,00</li>
<li>Finansieringskilde 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Faktureringsregler
Når du forhandler med en kunde om en prosjektkontrakt, definerer du hvordan og når kan du fakturere kunden for arbeid på et prosjekt. Når du har definert prosjektkontrakten og prosjektet, kan du definere faktureringsregler for prosjektet. Faktureringsregler er basert på prosjektvilkårene som er angitt i prosjektkontrakten. Faktureringsreglene du kan opprette avhenger av betingelsene i prosjektkontrakten og av prosjekttypen, for eksempel Etter regning eller Fastpris som du knytter til faktureringsregelen. Du kan opprette mer enn n faktureringsregel for en prosjektkontrakt. Du kan også tilordne en faktureringsregel til flere prosjekter som er knyttet til samme prosjektkontrakt og har lignende faktureringsvilkår. 

Du kan definere følgende typer faktureringsregler:

-   **Leveringsenhet** – Fakturer en kunde når du fullfører en leveringsenhet. Du definerer leveringsenhetene i kontrakten.
-   **Fremdrift** – Fakturer en kunde når du fullfører en bestemt prosentandel av prosjektet. Du kan definere en faktureringsregel for å beregne en prosentandel av fullført arbeid automatisk, eller du kan manuelt beregne prosentandelen av fullført arbeid og beløpet som skal faktureres kunden.
-   **Milepæl** – Fakturer en kunde for hele beløpet for en prosjektmilepæl når milepælen er nådd.
-   **Gebyr** – Fakturer en kunde for tjenestene dine i tillegg til et behandlingsgebyr, som vanligvis er en prosentandel av tjenestenes kostnad.
-   **Tid og materialer** – Fakturer en kunde for verdien av tid og materialer som brukes på et prosjekt.

For alle typer faktureringsregler kan du angi en bevaringsprosent som trekkes fra kundefakturaer helt til et prosjekt når et avtalt stadium. Prosenten for betalingsbevaring er angitt i prosjektkontrakten. Beløpet beregnes basert på, og trekkes fra, den totale verdien av linjene i en kundefaktura. 

For **Tid og materialer**- og **Fremdrift**-faktureringsregler kan du tilordne belastbare kategorier. Belastbare kategorier angir transaksjonene som skal inkluderes i kundefakturaer. 

Når du er klar til å fakturere en kunden, beregnes beløpet som skal faktureres for prosjektet, basert på faktureringsreglene, og det genereres et prosjektfakturaforslag. 

Delene nedenfor innholder eksempler som viser hvordan du definerer og administrerer en faktureringsregler for et prosjekt.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Eksempel: Opprett en fakturaregel som er basert på antall leverte enheter

Organisasjonen din inngår en avtale om å levere totalt fem opplæringsøkter til en kundes ansatte til en kostnad på 10 000 per opplæringsøkt. Du fakturerer kunden etter hver opplæringsøkt. 

Når du definerer faktureringsregler for kontrakten, bruker du følgende verdier:

-   Leveringsenheten er én opplæringsøkt.
-   Enhetsprisen er 10 000 per opplæringsøkt.
-   Totalt antall enheter er fem opplæringsøkter.

Når du har fullført én opplæringsøkt, kan du opprette en faktura på 10 000 for den første enheten som ble levert, og sende fakturaen til kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Eksempel: Opprett en fakturaregel som er basert på en angitt fullføringsprosent av prosjektet (beregnes manuelt)

Organisasjonen din er et programvarekonsulentfirma som inngår en avtale med en kunde om å utvikle en del av et produkt som kunden utvikler. Organisasjonen godtar å levere programvarekode over en periode på seks måneder. Kunden godtar å betale organisasjonen totalt 100 000 for arbeidet. Du oppretter en faktureringsregel for å fakturere kunden basert på prosenten av fullført arbeid på prosjektet, som angitt i kontrakten.

-   På slutten av den første måneden møter du kunden for å finne ut hvor stor prosentandel av arbeidet er fullført. Når du og kunden går gjennom prosjektet, fastsetter dere at prosjektet er 15 prosent fullført.
-   Du oppretter en faktura på 15 000 (15 prosent av 100 000) og sender den til kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Eksempel: Opprett en fakturaregel som er basert på en angitt fullføringsprosent av prosjektet (beregnes automatisk)

Organisasjonen din, et programvareutviklingsfirma, avtaler å utvikle en lønnsregnskapspakke for en kunde for 30 000. Kunden godtar å betale organisasjonen på grunnlag av prosenten av fullført arbeid. Du beregner prosjektkostnadene til 20 000. Prosjektkontrakten angir arbeidskategoriene du bruker i faktureringsprosessen. Du definerer faktureringsregler som automatisk beregner fakturabeløpene for arbeidsprosenten som er fullført for hver kategori. Du definerer et budsjett for hver kategori:

-   **Utvikling** – Kostnad på 15 000 og omsetning på 20 000
-   **Installasjon** – Kostnad på 5 000 og omsetning på 10 000

Når du oppretter en kundefaktura for første gang, beregnes fakturabeløpet automatisk basert på følgende informasjon:

-   Etter en måned sender arbeideren på prosjektet en timeregistrering for prosjektet. Kostnaden til arbeiderens timer er 5000 for utvikling og 1000 for installasjon. Utviklingsarbeidet er 33 prosent fullført (5 000 i faktiske kostnader / 15 000 i budsjettkostnader), og installasjonsarbeidet er 20 prosent fullført (1 000 i faktiske kostnader / 5 000 i budsjettkostnader).
-   Fakturabeløpet på 8 667 beregnes automatisk (33 prosent av 20 000 + 20 prosent av 10 000).
-   Du oppretter en faktura på 8 667 og sender den til kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Eksempel: Opprett en fakturaregel som er basert på avtalte milepæler

Organisasjonen din er et rådgivningsfirma og avtaler å utføre markedsundersøkelser for et forbrukerprodukt som kunden planlegger å selge. Kunden godtar å bruke dine tjenester over en periode på tre måneder med start i mars, og godtar å betale organisasjonen 50 000. Prosjektet har tre milepæler:

-   Milepæl 1: Samle inn forbrukerdata – 31. mars
-   Milepæl 2: Analysere forbrukerdata – 30. april
-   Milepæl 3: Presentere et forslag for levedyktighet for produktet – 31. mai

Kunden godtar å betale organisasjonen 10 000 for den første milepælen, 20 000 for milepæl nummer to og 20 000 for tredje milepæl. 

Når du definerer prosjektkontrakten, godtar du å fakturere kunden basert på milepælen som er fullført. Faktureringsregeloppsettet omfatter følgende trinn:

-   Definer milepælene i prosjektet.
-   Angi beløpet som skal faktureres kunden når hver milepæl er fullført.

Når den første milepælen fullføres 31. mars, merker du milepælen som fullført, og deretter oppretter du en faktura på 10 000 og sender den til kunden. Du kan ikke opprette en faktura for en milepæl før du har merket milepælen som fullført.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Eksempel: Opprett en faktureringsregel som er basert på tjenester i tillegg til et gebyr for administrasjon

Organisasjonen din, som er et rådgivningsfirma, avtaler å utføre markedsundersøkelser for å evaluere gjennomføringen av et produkt som kunden, et detaljhandelsfirma, utvikler. Vilkårene i avtalen angir at tjenestene skal utføres av de tre beste konsulentene, som skal utføre undersøkelsen på grunnlag av tid og materialer. Kunden godtar å betale 100 per time pluss et administrasjonsgebyr på ti prosent for konsultasjonstimene som faktureres til prosjektet. 

Når du definerer prosjektkontrakten, oppretter du en faktureringsregel for å legge til et administrasjonsgebyr på 10 prosent for konsultasjonstimene som prosjektet belastes med. 

Når du oppretter en faktura for kunden, faktureres kunden et administrasjonsgebyr på 10 prosent samt kostnadene for konsultasjonstimene. Hvis de tre konsulentene for eksempel arbeidet totalt 200 timer på prosjektet, opprettes en faktura på 22 000 basert på følgende beregning:

-   200 timer til 100 per time = 20 000
-   10 prosent administrasjonsgebyr = 2000
-   Totalt fakturabeløp = 22 000

Hvis gebyrer er avgiftspliktige for en kunde og du velger en mva-gruppe i prosjektkontrakten, registreres mva-gruppen automatisk i en faktureringsregel for gebyrer.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Eksempel: Opprett en faktureringsregel for verdien av tid og materialer

Organisasjonen din, som er et programvarekonsulentfirma, avtaler å stille med fem tekniske konsulenter som skal jobbe på et programvareutviklingsprosjekt for en kunde over de neste seks månedene. Kunden godtar å betale 150 for hver konsulenttime i tillegg til kostnaden for kontorutstyr. Organisasjonen din sender en faktura til kunden på slutten av hver måned. 

Når du definerer prosjektkontrakten, godtar du å fakturere kunden månedlig for tid og materialer på prosjektet. Du oppretter en faktueringsregel som inkluderer følgende informasjon:

-   Kontraktperioden er seks måneder.
-   Rådgivningstid beregnes med en sats på 150 per time.
-   Kontorutstyr faktureres til kostpris, og totalkostnad for prosjektet kan ikke overskride 10 000.
-   Du oppretter en kundefaktura på slutten av hver kalendermåned i løpet av prosjektet.

I løpet av den første måneden registrerer konsulentene totalt 800 timer på prosjektet. Kostnaden for kontorutstyr som belastes prosjektet, er 2000. På slutten av måneden kan du derfor opprette en faktura på 122 000, som beregnes til 800 timer til 150 per time, pluss 2 000 for kontorrekvisita.





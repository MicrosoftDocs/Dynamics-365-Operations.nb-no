---
title: Tilordne kanaler til e-handelsområder
description: Denne artikkelen beskriver noen av de vanligere scenarioene for kanaltilordning i Microsoft Dynamics 365 Commerce som kan ekstrapoleres for de fleste andre forretningsbehov.
author: samjarawan
ms.date: 05/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 94c43df26e8d6e55a5b6d459b65066d5873e1063
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902769"
---
# <a name="map-channels-to-e-commerce-sites"></a>Tilordne kanaler til e-handelsområder

Denne artikkelen beskriver noen av de vanligere scenarioene for kanaltilordning i Microsoft Dynamics 365 Commerce som kan ekstrapoleres for de fleste andre forretningsbehov.

Dynamics 365 Commerce støtter mange forretningsscenarioer for tilordning av [Internett-kanaler](#channels) som har et konfigurert sett med produkter, priser og rabatter, til kundeopplevelser på [e-handelsområder](#e-commerce-sites).

Denne artikkelen dekker følgende scenarioer:

- **En enkeltspråklig kanal med én e-handelsområdeopplevelse.** Dette scenarioet kan for eksempel gjelde ett varemerkeområde som er konfigurert for et amerikansk engelsk marked.
- **En flerspråklig kanal med én lokalisert områdeopplevelse.** Dette scenarioet kan for eksempel gjelde ett varemerkeområde som er konfigurert for Canada med støtte for fransk og engelsk. Brukere som velger ulike språk i dette scenarioet, får samme områdeopplevelse, men det er lokalisert til språket brukeren velger.
- **En flerspråklig kanal med en egen områdeopplevelse for hvert språk.** Dette scenarioet kan for eksempel gjelde ett varemerkeområde som er konfigurert for Canada med støtte for fransk og engelsk. Dette scenarioet byr på en egen områdeopplevelse for hvert språk.
- **Flere kanaler (enkeltspråklige og/eller flerspråklige) med én lokalisert områdeopplevelse.** Dette scenarioet kan for eksempel gjelde ett varemerkeområde som er konfigurert for Australia og New Zealand. I dette scenarioet deler begge land samme områdeopplevelse på engelsk, men hvert land er konfigurert med ulike produkter, valuta, priser, rabatter og leveringsmåter.
- **Flere kanaler (enkeltspråklige og/eller flerspråklige) med en egen områdeopplevelse for hver kanal.** Dette scenarioet kan for eksempel gjelde ett varemerkeområde som er konfigurert for Australia, Canada og Tyskland på flere språk. I dette scenarioet har hvert land en unik områdeopplevelse som er konfigurert med ulike produkter, valuta, priser, rabatter og leveringsmåter.

## <a name="channels"></a>Kanaler

En kanal (som også kan kalles en nettbutikk eller en Internett-kanal) representerer en nettbutikk som brukes til å tilordne produkter, priser, rabatter, språk, betalingsmåter, leveringsmåter, oppfyllelsessentre og andre aspekter ved nettopplevelsen som skal være tilgjengelig for e-handelskundene. Kanaler opprettes og administreres i Commerce headquarters, og tilordnes til én [juridisk enhet](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json#legal-entities). Den juridiske enheten er vanligvis basert i ett land som krever avgiftsrapportering for kanalen, og kan konfigureres med bare én valuta.

Hvis du vil ha mer informasjon om kanaler, kan du se [kanaloversikten](channels-overview.md). Hvis du vil ha mer informasjon om hvordan du oppretter en nettkanal, kan du se [Konfigurer en nettkanal](channel-setup-online.md).

Eksemplet med Commerce headquarters nedenfor viser standard Internett-kanaler som distribueres med Dynamics 365 Commerce, hvis alternativet for demodata velges.

![Standard demodatakanaler i Commerce headquarters.](media/channel-mapping-1.png)

## <a name="e-commerce-sites"></a>E-handelsområder

Et e-handelsområde inneholder et sett med områdesider som kunder blar gjennom og bruker til å handle. E-handelsområder administreres i Commerce-områdebygger.

Hvis du vil ha mer informasjon om hvordan du oppretter og administrerer områder i områdebygger, kan du se [Oversikt over e-handelsområde](online-store-overview.md).

## <a name="common-channel-mapping-scenarios"></a>Vanlige scenarioer for kanaltilordning

Dynamics 365 Commerce støtter en lang rekke scenarioer for kanaltilordning. Scenarioene for kanaltilordning som følger nedenfor, er bare et delsett av alle de mulige scenarioene. De er ment å være veiledende i planleggingen for eventuelle unike forretningsscenarioer du har. Den fiktive sportsbutikken Adventure Works. som følger med demodataene for Dynamics 365 Commerce, brukes som et eksempel i hvert scenario.

### <a name="single-language-channel-that-has-a-single-e-commerce-site-experience"></a>En enkeltspråklig kanal med én e-handelsområdeopplevelse

I det enkleste scenarioet har én kanal ett språk for salg i ett marked. Nettbutikken Adventure Works, som bare er konfigurert for det amerikansk engelske markedet, er et eksempel på dette scenarioet.

Eksemplet nedenfor viser en kanalkonfigurasjon i Commerce headquarters. I denne konfigurasjonen støtter Internett-kanalen bare ett språk (**en-us**), én valuta (**USD**) og én forretningsenhet (**usrt**) som brukes til avgiftsrapportering.

![Verdiene for juridisk enhet, valuta og språk for nettbutikken Adventure Works er uthevet i Commerce headquarters.](media/channel-mapping-3.png)

Denne ene Internett-kanalen kan tilordnes til ett e-handelsområde i områdebygger. Hvis du vil ha informasjon om hvordan du oppretter et nytt område og tilordner det til en kanal, kan du se delen [Tilordne en kanal til et område i områdebygger](#map-a-channel-to-a-site-in-site-builder) i denne artikkelen.

### <a name="multi-language-channel-that-has-a-single-localized-site-experience"></a>En flerspråklig kanal med én lokalisert områdeopplevelse

I dette scenarioet støtter én kanal flere språk. Produktnavn, beskrivelser og attributter kan derfor lokaliseres i Commerce headquarters. Hvis du vil gi en fullstendig, lokalisert områdeopplevelse, kan markedsføringsinnhold på området også lokaliseres i Commerce-områdebygger.

Begrensningen ved dette scenarioet er at én kanal bare kan konfigureres med én valuta, én juridisk enhet og ett sett med produkter og priser. Denne konfigurasjonen fungerer best for land som har én valuta og flere språk (for eksempel Canada, som har engelsk og fransk ), én juridisk enhet og ett sett med produkter og priser.

Hvert språk i en kanal kan konfigureres med et eget domenenavn. Domenet `www.adventure-works.ca` kan for eksempel konfigureres for den engelske versjonen i Canada, og domenet `www.adventure-works-fr.ca` kan konfigureres for den franske versjonen i Canada. Alternativt kan ulike språk i en kanal konfigureres i ett domene, og deretter kan en egen bane brukes for hvert språk. Domenet `www.adventure-works.ca` kan for eksempel konfigureres for den engelske versjonen i Canada, og så kan domenet `www.adventure-works.ca/fr` brukes for den franske versjonen i Canada. [Registrering av geografisk område](geo-detection-redirection.md) kan også brukes til å omdirigere en bruker automatisk til riktig område basert på hvor brukeren er.

Hvis du vil ha informasjon om hvordan du gjør at kunder kan bytte mellom språk manuelt, kan du se delen [Legge til og konfigurere områdevelgermodulen](#add-and-configure-the-site-picker-module) i denne artikkelen. Hvis du vil ha informasjon om hvordan du tilpasser lokaliserte sider og fragmenter, kan du se [Administrere områdeinnhold med flere kanaler og språk](#manage-site-content-that-has-multiple-channels-and-languages).

### <a name="multi-language-channel-that-has-a-different-site-experience-per-language"></a>En flerspråklig kanal med en egen områdeopplevelse for hvert språk

Det kan hende at du foretrekker et scenario der én kanal støtter flere språk, men en helt egen områdeopplevelse for hvert språk. Den anbefalte metoden for implementering av dette scenarioet er å bruke [sidevarianter](#implement-page-variants-for-each-language) på ett område.

En annen metode er å opprette et nytt e-handelsområde for hvert språk i områdebygger og deretter tilordne hvert område til én Internett-kanal og ett språk. Resultatet blir én Internett-kanal som er tilordnet til flere e-handelsområder, ett for hvert språk. Denne metoden for flere områder krever ekstra administrasjonsressurser fordi det blir flere områder å administrere i områdebygger.

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-single-localized-site-experience"></a>Flere kanaler (enkeltspråklige og/eller flerspråklige) med én lokalisert områdeopplevelse

Et varemerkeområde krever kanskje flere Internett-kanaler per geografiske område for å støtte ulike valutaer, sett med produkter og sett med priser for hver kanal på ett område. Området Adventure Works kan for eksempel ha en Internett-kanal for det kanadiske markedet med flere språk, en kanal for det amerikanske markedet med ett språk, og en kanal for det tyske markedet med ett språk. I dette scenarioet konfigureres hver Internett-kanal for en områdespesifikk juridisk enhet, og den kan ha samme sett med produkter som andre kanaler har, et delsett av disse produktene eller et annet sett med produkter. Hver kanal har også egne priser i den regionale valutaen samt egne avgifter, rabatter og leveringsmåter.

I dette scenarioet kan hvert marked konfigureres med egne domenenavn. Domenet `www.adventure-works.com` kan for eksempel konfigureres for det amerikanske markedet, og domenet `www.adventure-works.de` kan konfigureres for det tyske markedet. Hvert marked kan alternativt konfigureres slik at det bruker en egen bane. Domenet `www.adventure-works.com` kan for eksempel konfigureres for det amerikanske markedet, og så kan banen `www.adventure-works.com/de` brukes for det tyske markedet. [Registrering av geografisk område](geo-detection-redirection.md) kan også brukes til å omdirigere brukere automatisk til riktig område basert på det geografiske området de er i.

Du vil kanskje også at området skal ha en rullegardinliste der brukere kan bytte manuelt til et bestemt marked. Hvis du vil ha mer informasjon, kan du se delen [Legge til og konfigurere områdevelgermodulen](#add-and-configure-the-site-picker-module) senere i denne artikkelen.

Hvis du vil ha informasjon om hvordan du konfigurerer flere kanaler på ett område, kan du se delen [Konfigurere flere kanaler på et e-handelsområde](#configure-multiple-channels-on-an-e-commerce-site).

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-different-site-experience-per-channel"></a>Flere kanaler (enkeltspråklige og/eller flerspråklige) med en egen områdeopplevelse for hver kanal

Du vil kanskje ha flere kanaler for ett varemerke i ulike geografiske områder, og du vil kanskje at hvert geografiske område skal ha en egen områdeopplevelse. Det finnes to metoder for å implementere dette scenarioet:

- Bruk [sidevarianter](#implement-page-variants-for-each-language).
- Konfigurer et eget område for hver Internett-kanal i områdebygger, og tilordne deretter hvert område til en egen Internett-kanal og et annet språk. Denne metoden krever ekstra administrasjonsressurser fordi det blir flere områder å administrere i områdebygger.

## <a name="cross-channel-sharing"></a>Deling på tvers av kanal

Deling på tvers av kanal er nyttig når flere kanaler på ett enkelt område kan dele innhold. En forhandler som har flere merker og butikkfasader som er gruppert under ett enkelt område, kan for eksempel dele noe av innholdet blant noen av eller alle butikkfasader. Delt innhold kan omfatte sider for vilkår og betingelser, betalingsbetingelser, leveringsmåter og vanlige spørsmål. Hvis du vil ha mer informasjon, kan du se [Aktivere og bruke krysskanaldeling](cross-channel-sharing.md).

## <a name="map-a-channel-to-a-site-in-site-builder"></a>Tilordne en kanal til et område i områdebygger

Det finnes flere metoder for opprettelse og konfigurasjon av områder som bruker egne Internett-kanaler.

### <a name="create-a-new-site"></a>Opprette et nytt område

Du kan opprette et helt nytt område i områdebygger ved å gå til **Områder**-listesiden og velge **Nytt område**. Du kan deretter velge standard Internett-kanal og språk for området i dialogboksen **Nytt område** som vises, som vist i illustrasjonen nedenfor.

![Opprett en ny kanal i områdebygger.](media/channel-mapping-4.png)

Området du oppretter på denne måten, er tomt og inneholder ingen områdesider (for eksempel en hjemmeside, kategorisider eller produktsider).

Hvis du vil ha mer informasjon, kan du se [Opprette et e-handelsområde](create-ecommerce-site.md).

### <a name="create-a-new-site-by-using-the-site-copy-operation"></a>Opprette et nytt område ved hjelp av områdekopiering

I stedet for å opprette et helt nytt, tomt område som beskrevet i forrige del, er det bedre å begynne med en kopi av et av startområdene i Commerce-modulbiblioteket, for eksempel området Fabrikam eller Adventure Works.

Hvis du vil kopiere et eksisterende område, går du til **Områder**-listesiden i områdebygger og velger **Kopier område**. Du kan deretter velge kildeområdet i dialogboksen **Kopier område** som vises, og angi navnet på målområdet.

Du kan foreløpig ikke velge standard Internett-kanal og språk for området. Du kan imidlertid konfigurere disse egenskapene etter at områdekopieringen er fullført. Når du først velger området på **Områder**-listesiden i områdebygger, vises dialogboksen **Konfigurer området**, der du kan velge standardkanal og språk.

Hvis du vil ha mer informasjon om områdekopieringen, kan du se [Kopiere et e-handelsområde](copy-ecommerce-site.md).

### <a name="manage-an-existing-site-channel"></a>Administrere en eksisterende områdekanal

Etter at et område er konfigurert med en kanal, kan du administrere og oppdatere kanalen fra det valgte området i områdebygger i **Områdeinnstillinger \> Kanaler**, som vist i illustrasjonen nedenfor.

![Administrere kanaltilordningen i områdebygger.](media/channel-mapping-7.png)

## <a name="support-multiple-sites-in-a-single-tenant"></a>Støtte flere områder i én leier

Mange varemerkeområder kan eksistere sammen i én leier. Illustrasjonen nedenfor viser tre forskjellige varemerkeområder (Adventure Works, Adventure Works Business og Fabrikam) der hvert område er tilordnet til en egen Internett-kanal.

![Områdeliste i områdebygger.](media/channel-mapping-8.png)

## <a name="configure-a-single-domain-name-with-paths-for-multiple-sites"></a>Konfigurere ett domenenavn med baner for flere områder

Ett domenenavn kan brukes for flere områder, og baner kan deretter brukes til å skille områder eller språk. Domenet `www.mycompany.com` er for eksempel konfigurert for to ulike e-handelsområder: ett for Fabrikam og ett for Adventure Works. I dette tilfellet kan standardbanen (`www.mycompany.com`), som også kan kalles en tom bane, brukes for området Fabrikam, og en annen bane (for eksempel `www.mycompany.com/adventureworks`) kan brukes for området Adventure Works. Et annet alternativ er å bruke en egendefinert bane (for eksempel `www.mycompany.com/fabrikam`) i stedet for standardbanen for området Fabrikam også.

Alternativt kan et annet domenenavn brukes for hvert område (for eksempel `www.adventure-works.com` og `www.fabrikam.com`). Baner kan deretter brukes for ulike språk eller områder (for eksempel `www.adventure-works.com/fr-ca` for fransk i Canada).

## <a name="configure-multiple-languages-on-a-site"></a>Konfigurere flere språk på et område

Språk kan konfigureres for e-handelsområdet i områdebygger i **Områdeinnstillinger \> Kanaler**. I eksemplet nedenfor er hvert språk konfigurert ved hjelp av de nasjonale innstillingene for banen, slik at hvert språk har en egen nettadresse.

![Flere språk konfigurert på et område.](media/channel-mapping-10.png)

Hvis du vil legge til et nytt kanalspråk, går du til **Områdeinnstillinger \> Kanaler** og velger kanalkoblingen. Velg **Legg til en nasjonal innstilling** i ruten som vises til høyre, for å velge kanalen og den nasjonale innstillingen du vil legge til. Angi deretter banen som skal brukes for den valgte kanalen.

### <a name="add-and-configure-the-site-picker-module"></a>Legge til og konfigurere områdevelgermodulen

Etter at du har konfigurert et område med flere språk og/eller kanaler, vil du kanskje legge til en språkvelger i toppteksten på områdesiden, slik at brukere kan velge språk eller land manuelt. [Topptekstmodulen](author-header-module.md) i modulbiblioteket har innebygd støtte for at brukere kan velge et språk ved hjelp av [områdevelgermodulen](site-selector.md). Områdevelgermodulen kan legges til i topptekstmodulen i topptekstfragmentet.

Hvis du vil ha mer informasjon om hvordan du legger til og konfigurerer områdevelgermodulen, kan du se delen [Områdevelgermodul](site-selector.md).

### <a name="implement-page-variants-for-each-language"></a>Implementere sidevarianter for hvert språk

I dette scenarioet finnes det bare én kanal, men det finnes flere språk. Du kan endre utseendet på en side basert på det valgte språket, ved å opprette en sidevariant for det. Du kan deretter legge til lokalisert innhold i varianten.

Når du har en side åpen i områdebygger og velger koblingen i øvre høyre hjørne som viser gjeldende kanal og språk, vises en kanal- og språkvelger, som vist i illustrasjonen nedenfor. Hvis du vil overstyre siden for gjeldende språk, velger du en annen nasjonal innstilling og deretter **Endre**. Du kan også endre kanalen hvis du [administrerer et område med flere kanaler og språk](#manage-site-content-that has-multiple-channels-and-languages).

![Endre språket for en side i områdebygger.](media/channel-mapping-14.png)

Hvis varianten for den valgte siden eller fragmentet ikke er opprettet ennå, får du en advarsel, som vist i illustrasjonen nedenfor. I dette tilfellet velger du koblingen **Opprett sidevariant** i meldingsteksten. Dialogboksen som vises, inneholder alternativer du kan bruke til å begynne med en kopi av en eksisterende variant eller opprette en helt ny side fra en mal.

![Melding for opprettelse av en sidevariant i områdebygger](media/channel-mapping-16.png)

Hvis du ikke oppretter en variant, gjengis den opprinnelige siden, og riktig språk vises for modulstrenger og produktinformasjon fra Commerce headquarters. Hvis det imidlertid er angitt tekst, for eksempel en sidetittel eller annet markedsføringsinnhold, direkte i standard sidemoduler, forblir strengene for denne teksten i det opprinnelige språket.

I stedet for å opprette hver side og hvert fragment manuelt kan du eksportere hver side og hvert fragment til en XLM XLIFF-fil (Localization Interchange File Format) som deretter kan sendes til lokalisering. Etter at hver XLIFF-fil er lokalisert, kan den importeres som en lokal sidevariant. Hvis du vil eksportere en XLIFF-fil fra en side eller et fragment i områdebygger eller importere en XLIFF-fil til en side eller et fragment, velger du **Lokalisering** på kommandolinjen. Velg deretter enten **Eksporter XLIFF** eller **Importer XLIFF**, som vist i illustrasjonen nedenfor.

![Importere eller eksportere en side eller et fragment i XLIFF-format.](media/channel-mapping-18.png)

## <a name="manage-site-content-that-has-multiple-channels-and-languages"></a>Administrere områdeinnhold med flere kanaler og språk

Et område med flere kanaler og/eller språk lagrer en unik variant av hver side og hvert fragment for hver kombinasjon av en kanal og et språk. Denne funksjonaliteten gjør at sidevarianter kan inneholde lokaliserte data, men også gi deg fleksibiliteten til å endre utseende og funksjonalitet på en side for en bestemt variant.

Hvis du vil ha informasjon om hvordan du arbeider med sidevarianter, kan du se [Implementere sidevarianter for hvert språk](#implement-page-variants-for-each-language) i denne artikkelen.

## <a name="configure-multiple-channels-on-an-e-commerce-site"></a>Konfigurere flere kanaler på et e-handelsområde

Du kan legge til kanaler på et e-handelsområde i områdebygger ved å gå til **Områdeinnstillinger \> Kanaler** og velge **Legg til en kanal**. Du kan deretter velge Internett-kanalen og standard nasjonal innstilling i dialogboksen **Legg til en kanal** som vises.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over kanaler](channels-overview.md)

[Konfigurere en nettkanal](channel-setup-online.md)

[Oversikt over organisasjoner og organisasjonshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md)

[Konfigurere registrering og omadressering av georeplikering](geo-detection-redirection.md)

[Aktivere og bruke deling på tvers av kanal](cross-channel-sharing.md)

[Opprette et e-handelsområde](create-ecommerce-site.md)

[Kopiere et e-handelsområde](copy-ecommerce-site.md)

[Områdevelgermodul](site-selector.md)

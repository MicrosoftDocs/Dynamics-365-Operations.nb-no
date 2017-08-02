---
title: Definere og vedlikeholde kanalklienter, kasser og maskinvarestasjoner
description: Dette emnet beskriver hvordan du kobler eksterne enheter til salgsstedet for detaljhandel.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 5c5a6cc45ad65c7581dbfb9a4441fdddbbc19242
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017



---

# <a name="define-and-maintain-channel-clients-registers-and-hardware-stations"></a>Definere og vedlikeholde kanalklienter, kasser og maskinvarestasjoner

[!include[banner](includes/banner.md)]


Dette emnet beskriver hvordan du kobler eksterne enheter til salgsstedet for detaljhandel.

**Obs!** For spesifikke installasjonsinstruksjoner, kan du se [Konfigurasjon og installasjon av Maskinvarestasjon for detaljhandel](retail-hardware-station-configuration-installation.md) og [Nedlasting og installasjon av moderne salgssted for enhetsaktivering av Moderne salgssted og skysalgssted](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Nøkkelkomponenter
Flere komponenter brukes til å definere relasjonene mellom en butikk, kasser på salgsstedet eller kanaler i butikken, og de eksterne detaljhandelsenhetene som disse kassene eller kanalene bruker for å behandle transaksjoner. Dette avsnittet beskriver hver komponent og forklarer hvordan den skal brukes i en distribusjon av detaljhandelsbutikk.

### <a name="pos-registers"></a>Kasser på salgssted

Navigering: Klikk **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Kasser**. Kassen på salgsstedet er en enhet som brukes til å definere egenskapene til en bestemt forekomst av salgsstedet. Disse egenskapene inkluderer maskinvareprofilen eller oppsettet for detaljhandelsenheter som skal brukes i kassen, butikken som kassen er tilordnet og den visuelle opplevelsen for brukeren som logger på kassen.

### <a name="devices"></a>Enheter

Navigering: Klikk **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Enheter**. En enhet er en enhet som representerer en fysisk forekomst av en enhet som er tilordnet en kasse på salgsstedet. Når en enhet opprettes, tilordnes den til en kasse på salgsstedet. Enhetsenheten registrerer informasjon om når en kasse på salgsstedet aktiveres, klienttypen som brukes og programpakken som er distribuert til en bestemt enhet. Enheter kan være av to typer: **Moderne salgssted for detaljhandel** (MPOS) eller **Skybasert salgssted** (Cloud POS).

#### <a name="mpos"></a>MPOS

MPOS er et klientprogram for salgssted som er installert på Windows 8.1 eller nyere PC-basert operativsystem. Hvis programtypen **Moderne salgssted for detaljhandel** er tilordnet til en enhet, kan nedlastingspakken angis for en bestemt enhet. Nedlastingspakken kan tilpasses slik at den inkludere ulike versjoner av installasjonspakken. Muligheten til å distribuere forskjellige pakker gir fleksibilitet i tilfeller der ulike kasser på salgssted må ha ulike integreringer. MPOS distribueres sammen med en innebygd maskinvarestasjon.

#### <a name="cloud-pos"></a>Skybasert salgssted

Skysalgssted er et nettleserbasert salgssted. Siden det kjører i nettleseren, krever ikke det skybaserte salgsstedet Windows 8.1 eller et nyere PC-basert operativsystem. Hvis programtypen **Skybasert salgssted for detaljhandel** er tilordnet til en bestemt enhet på hovedkontoret for detaljhandel, kan denne enheten brukes i nettleseren uten behov for å laste ned eller installere en pakke. Skybasert salgssted krever en maskinvarestasjonen for å bruke maskinvare utover tastatur, kortbasert strekkodeskanning.

### <a name="hardware-profile"></a>Maskinvareprofil

Navigering: Klikk **Handel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofiler** &gt; **Maskinvareprofiler**. En maskinvareprofil identifiserer maskinvaren som er koblet til en kasse på salgssted eller en maskinvarestasjon. Maskinvareprofilen brukes også til å angi parametere for betalingsprosessor som skal brukes under kommunikasjon med SDK for betaling (Software Development Kit). (SDK for betaling distribueres som en del av maskinvarestasjonen).

### <a name="hardware-station"></a>Maskinvarestasjon

Navigering: Klikk **Detaljhandel** &gt; **Kanaler** &gt; **Detaljhandelbutikker** &gt; **Alle detaljhandelsbutikker**. Velg en butikk, og klikk deretter hurtigfanen **Maskinvarestasjoner**. En maskinvarestasjon er en forekomst av forretningslogikk som styrer tilbehør for salgssted. EN maskinvarestasjon installeres automatisk sammen med MPOS. Maskinvarestasjonen kan eventuelt installeres som en frittstående komponent, og deretter brukes av MPOS eller Cloud POS via en webtjeneste. Maskinvarestasjonen må være definert på kanalnivå.

### <a name="hardware-station-profile"></a>Profil for maskinvarestasjon

Navigering: Klikk **Handel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofiler** &gt; **Profiler for maskinvarestasjon**. Mens selve maskinvarestasjonen er angitt på kanalnivå og inkluderer forekomstspesifikk informasjon, for eksempel URL-adressen for maskinvarestasjonen, inneholder profilen for maskinvarestasjon informasjon som kan være statisk eller delt på tvers av flere maskinvarestasjoner. Den statiske informasjon inkluderer porten som skal brukes, pakken for maskinvarestasjonen og maskinvareprofilen. Den statiske informasjon inneholder også en beskrivelse av hvilken type maskinvarestasjon som distribueres, for eksempel **Gå til kassen** eller **Returer**, avhengig av maskinvaren som kreves for hver bestemte maskinvarestasjon.

## <a name="scenarios"></a>Scenarier
### <a name="mpos-with-connected-peripheral-devices"></a>MPOS med tilkoblede eksterne enheter

[![Tradisjonelt fast salgssted](./media/traditional-300x279.png)](./media/traditional.png) 

Hvis du vil koble MPOS til enheter på salgssted i et tradisjonelt scenario for fast salgssted, må du først gå til kassen og tilordne en maskinvareprofil til den. Du kan finne kassen på salgsstedet under **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Kasser**. Når du har tilordnet maskinvareprofilen, synkroniserer du endringer til kanaldatabasen ved hjelp av distribusjonsplanen "Kasser". Du finner distribusjonsplanene under **Detaljhandel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplan**. Deretter definerer du en "lokal" maskinvarestasjon på kanalen. Klikk **Detaljhandel** &gt; **Kanaler** &gt; **Detaljhandelbutikker** &gt; **Alle detaljhandelsbutikker**, og velg butikk. I hurtigfanen **Maskinvarestasjoner** klikker du **Legg til** for å legge til en maskinvarestasjon. Skriv inn en beskrivelse, skriv inn **localhost** som vertsnavnet, og synkroniser deretter endringene til kanalen ved hjelp av distribusjonsplan "Kanalkonfigurasjon". Du finner distribusjonsplanene under **Detaljhandel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplan**. Til slutt går du til MPOS og bruker operasjonen **Velg maskinvarestasjon** for å velge maskinvarestasjonen **localhost**. Sett maskinvarestasjonen til **Aktive**. Maskinvareprofilen som brukes i dette scenariet skal komme fra kassen på salgsstedet. En profil for maskinvarestasjon er ikke nødvendig for dette scenariet. **Obs!** Noen endringer i maskinvareprofil, for eksempel endringer i kassaskuffer, krever at det åpnes et nytt skift etter at endringene er synkronisert til kanalen. **Obs!** Skybasert salgssted må bruke den frittstående maskinvarestasjonen for å kommunisere med eksterne detaljhandelsenheter.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS eller Cloud POS en frittstående maskinvarestasjon
[![Delte eksterne enheter](./media/shared-300x254.png)](./media/shared.png)

I dette scenariet er en frittstående maskinvarestasjon delt mellom MPOS- og Cloud POS-klienter. Dette scenariet krever at du oppretter en profil for maskinvarestasjon for å angi nedlastingspakken, port og maskinvareprofil som maskinvarestasjonen bruker. Du kan finne profilen for maskinvarestasjon på **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofiler** &gt; **Profiler for maskinvarestasjon**. Når du har opprettet profilen for maskinvarestasjon, kan du gå til den spesifikke detaljhandelskanalen (**Detaljhandel** &gt; **Kanaler** &gt; **Detaljhandelbutikker** &gt; **Alle detaljhandelbutikker**), og legge til en ny maskinvarestasjon. Tilordne denne nye maskinvarestasjonen til profilen for maskinvarestasjon som ble opprettet tidligere. Deretter angir du en beskrivelse som hjelper kassereren med å identifisere maskinvarestasjonen. I feltet **Vertsnavn** angir du URL-adressen for vertsmaskinen i følgende format: **https://&lt;Maskinnavn:Port&gt;/Maskinvarestasjon**. (Erstatt **&lt;Maskinnavn:Port&gt;** med det faktiske maskinnavnet på maskinvarestasjonen og porten som er angitt i profilen for maskinvarestasjonen.) For en frittstående maskinvarestasjon må du også angi terminal-ID-en for elektronisk pengeoverføring (EFT). Denne verdien identifiserer EFT-terminalen som er koblet til maskinvarestasjonen når betalingstilkoblingen kommuniserer med betalingsleverandøren. Deretter, fra selve maskinvarestasjonen, går du til kanalen og velg maskinvarestasjonen. Klikk deretter **Last ned** og installer maskinvarestasjonen. Deretter, fra MPOS eller Cloud POS, bruker du operasjonen **Velg maskinvarestasjon** for å velge maskinvarestasjonen som ble installert tidligere. Velg **Par** for å opprette en sikker relasjon mellom salgsstedet og maskinvarestasjonen. Dette trinnet må fullføres én gang for hver kombinasjon av salgssted og en maskinvarestasjon. Når maskinvarestasjonen er sammenkoblet, brukes den samme operasjonen for å aktivere maskinvarestasjonen når den er i bruk. I dette scenariet skal maskinvareprofilen tilordnes profilen for maskinvarestasjon i stedet for kassen. Hvis maskinvarestasjonen en eller annen grunn ikke har en maskinvareprofil direkte tilordnet, brukes i stedet maskinvareprofilen som er tilordnet kassen.

## <a name="client-maintenance"></a>Klientvedlikehold
### <a name="registers"></a>Kasser

Kasser på salgssted behandles hovedsakelig gjennom kassen, og også gjennom profiler som er tilordnet til kasser. Attributter som er spesifikke for én enkelt kasse administreres på kassenivå. Disse attributtene omfatter butikken der kassen brukes, kassenummeret, beskrivelsen og EFT-terminal-ID-en som er spesifikk for kassen.

### <a name="pos-profiles"></a>Salgsstedsprofiler

Du kan finner salgsstedsprofilene under **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofiler**. Det er nyttig å administrere mange deler av en kasse gjennom profiler, fordi profilene kan deles av mange kasser. Profiler kan tilordnes én enkelt kasse eller, hvis en profil er effektiv på hele butikken, til detaljhandelbutikken. Avsnittene nedenfor beskriver salgsstedsprofiler og hvordan de brukes.

#### <a name="offline-profile"></a>Frakoblet profil

Den frakoblede profilen angis på lagernivå. Den brukes til å angi innstillingene for opplasting for transaksjoner som utføres en kasse for salgssted når kassen ikke er tilkoblet kanaldatabasen.

#### <a name="functionality-profile"></a>Funksjonalitetsprofil

Funksjonsprofilen angis på butikknivå. Den brukes til å angi innstillinger for hele butikken om funksjoner som kan utføres på salgsstedet. Funksjonene nedenfor administreres gjennom funksjonsprofilen. Disse funksjonene er ordnet etter hurtigfane.

-   Hurtigfanen **Generelt**:
    -   International Organization for Standardization (ISO).
    -   Opprette en kunde i frakoblet modus.
    -   Kvitteringsprofil for e-post.
    -   Påloggingsgodkjenning for sentralstab.
-   Hurtigfanen **Funksjoner**:
    -   Behandling av pålogging og utvidet pålogging.
    -   Økonomiske og valutarelaterte deler av salgsstedet, for eksempel muligheten til registrere priser og om desimaler er nødvendig for mindre valuta.
    -   Aktivere tidsregistrering gjennom salgsstedet.
    -   Hvordan produktene og betalinger vises på salgsstedet og på kvitteringer.
    -   Administrasjon av sagsoppgjør.
    -   Parametere for transaksjonsbevaring for kanaldatabase.
    -   Hvordan kunder slås opp og opprettes fra salgsstedet.
    -   Hvordan rabatter beregnes.
-   Hurtigfanen **Beløp**:
    -   Maksimums- og minimumspriser som er tillatt.
    -   Rabattprogram og -beregning.
-   Hurtigfanen **Informasjonskoder**:
    -   Alle aspekter av hvordan informasjonskoder behandles på salgsstedet. Hvis du vil ha mer informasjon, kan du se [Infokoder](info-codes-retail.md).
-   Hurtigfanen **Kvitteringsnummerering**:
    -   Angi masker for kvitteringsnummerering, som kan omfatte segmenter for butikknummer, terminalnummer, konstanter og om salg, returer, salgsordrer og tilbud skal skrives ut i separate serier, eller om alle følger samme sekvens.

#### <a name="receipt-profiles"></a>Kvitteringsprofiler

Kvitteringsprofiler tilordnes direkte til skrivere i maskinvareprofilen. De brukes til å angi hvilke kvitteringstyper som skrives ut på en bestemt skriver. Profilene omfatter innstillinger for kvitteringsformater og innstillinger som bestemmer om kvitteringer alltid skrives alltid, eller om kassereren blir bedt om å bestemme om kvitteringen skal skrives ut. Ulike skrivere kan også bruke ulike kvitteringsprofiler. Skriver 1 er for eksempel en standard termisk kritteringsskriver og har derfor mindre kvitteringsformater. Skriveren 2 er imidlertid en skriver for kvitteringer i full størrelse som brukes til å skrive ut kvitteringer for kundebestillinger, som krever mer plass.

#### <a name="hardware-profiles"></a>Maskinvareprofiler

Maskinvareprofiler er forklart som en komponent for klientoppsett tidligere i denne artikkelen. Maskinvareprofiler tilordnes direkte til kassen på salgsstedet eller til en profil for maskinvarestasjon. De brukes til å angi hvilke typer enheter en bestemt kasse på salgssted eller maskinvarestasjon bruker. Maskinvareprofiler kan også brukes til å angi EFT-innstillinger som brukes til å kommunisere med SDK for betaling.

#### <a name="visual-profiles"></a>Visuelle profiler

Visuelle profiler tilordnes på kassenivå. De brukes til å angi temaet for en bestemt kasse. Profilene omfatter innstillinger for programtypen som brukes (MPOS eller Cloud POS), uthevingsfarge og tema, skriftutvalget, påloggingsbakgrunnen og bakgrunn for salgssted.

### <a name="custom-fields"></a>Egendefinerte felt

Du kan opprette egendefinerte felt for å legge til felt som ikke følger med som standard, for salgsstedet. Hvis du vil ha mer informasjon om hvordan du bruker egendefinerte felt, kan du se [blogginnlegget om å arbeide med egendefinerte felt](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Språktekst

Ved overstyre standardstrenger på salgsstedet ved hjelp av tekstoppføringer for språket. Hvis du vil overstyre en streng på salgsstedet, legge til en ny språktekstlinje. Angi deretter en ID, standardstrengen som skal overstyres og teksten som skal vises på salgsstedet i stedet for standardstrengen.

### <a name="hardware-station-profiles"></a>Profiler for maskinvarestasjon

Profiler for maskinvarestasjon er beskrevet tidligere i denne artikkelen. De brukes for å tilordne informasjon som ikke er forekomstspesifikk for maskinvarestasjoner.

### <a name="channel-reports-configuration"></a>Konfigurasjon av kanalrapporter

Du definere rapportene som er tilgjengelige for detaljhandelskanalen på siden **Konfigurasjon av detaljhandelskanalrapporter**. Du kan opprette nye rapporter ved å angi XML-definisjonen for rapporten, og tilordne rapporten til en bestemt tillatelsesgruppe på salgsstedet.

### <a name="devices"></a>Enheter

Enheter er beskrevet tidligere i denne artikkelen. De brukes til å administrere aktiveringen av en bestemt kasse på salgsstedet. Enheter brukes også for å angi programmet som brukes for en bestemte kasse, og installasjonspakken som skal brukes for å installere MPOS-klienten. Her er statusene for enhetsaktivering:

-   **Venter** – Enheten er klar til å bli aktivert.
-   **Aktivert** – Enheten er aktivert.
-   **Deaktivert** – Enheten er deaktivert i for hovedkontoret for detaljhandel eller gjennom salgsstedet.
-   **Deaktivert** – Enheten er deaktivert.

Aktiveringsrelatert tilleggsinformasjon inkluderer arbeideren som endret aktiveringsstatus for enheten, og et tidsstempel for aktiveringen og om enhetskonfigurasjonen er godkjent.

### <a name="client-data-synchronization"></a>Klientdatasynkronisering

Alle endringer i en klient på salgsstedet, unntatt endringer i statusen for enhetsaktivering, må synkroniseres til kanaldatabasen for å tre i kraft. Hvis du vil synkronisere endringer til kanaldatabasen, går du til **Detaljhandel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplan**, og kjører den nødvendige distribusjonsplan. For klientendringer må du kjøre distribusjonsplanene "Kasser" og "Kanalkonfigurasjon".





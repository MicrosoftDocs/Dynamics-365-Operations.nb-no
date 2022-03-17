---
title: Koble eksterne enheter til salgsstedet
description: Dette emnet beskriver hvordan du kobler eksterne enheter til salgsstedet for detaljhandel.
author: BrianShook
ms.date: 03/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice
audience: Application User
ms.reviewer: josaw
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f1c53c7215d3a5a182f345d5e040274ae06f9b12
ms.sourcegitcommit: 116898def829c0f78bda8a117242aa308793465d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/01/2022
ms.locfileid: "8370957"
---
# <a name="connect-peripherals-to-the-point-of-sale-pos"></a>Koble eksterne enheter til salgsstedet

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du kobler eksterne enheter til salgsstedet for detaljhandel.

> [!NOTE]
> Hvis du vil ha bestemte installasjonsinstruksjoner, kan du se [Konfigurere og installere Retail Hardware Station](retail-hardware-station-configuration-installation.md) og [Konfigurere, installere og aktivere Moderne salgssted (MPOS)](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Nøkkelkomponenter

Flere komponenter brukes til å definere relasjonene mellom en butikk, kasser på salgsstedet eller kanaler i butikken, og de eksterne handelsenhetene som disse kassene eller kanalene bruker for å behandle transaksjoner. Dette avsnittet beskriver hver komponent og forklarer hvordan den skal brukes i en distribusjon av butikk.

### <a name="pos-registers"></a>Kasser på salgssted

Navigasjon: Klikk på **Detaljhandel og handel** &gt; **Kanaloppsett** &gt; **Oppsett av salgssted** &gt; **Kasser**.

Kassen på salgsstedet er en enhet som brukes til å definere egenskapene til en bestemt forekomst av salgsstedet. Disse egenskapene inkluderer maskinvareprofilen eller oppsettet for eksterne enheter som skal brukes i kassen, butikken som kassen er tilordnet og den visuelle opplevelsen for brukeren som logger på kassen.

### <a name="devices"></a>Enheter

Navigasjon: Klikk på **Detaljhandel og handel** &gt; **Kanaloppsett** &gt; **Oppsett av salgssted** &gt; **Enheter**.

En enhet er en enhet som representerer en fysisk forekomst av en enhet som er tilordnet en kasse på salgsstedet. Når en enhet opprettes, tilordnes den til en kasse på salgsstedet. Enhetsenheten registrerer informasjon om når en kasse på salgsstedet aktiveres, klienttypen som brukes og programpakken som er distribuert til en bestemt enhet. Enheter kan være av to typer: **Moderne salgssted for detaljhandel** (MPOS) eller **Skybasert salgssted** (Cloud POS).

#### <a name="mpos"></a>MPOS

MPOS er et klientprogram for salgssted som er installert på Windows 8.1 eller nyere PC-basert operativsystem. Hvis programtypen **Moderne salgssted for detaljhandel** er tilordnet til en enhet, kan nedlastingspakken angis for en bestemt enhet. Nedlastingspakken kan tilpasses slik at den inkludere ulike versjoner av installasjonspakken. Muligheten til å distribuere forskjellige pakker gir fleksibilitet i tilfeller der ulike kasser på salgssted må ha ulike integreringer. MPOS distribueres sammen med en innebygd maskinvarestasjon.

#### <a name="cloud-pos"></a>Skybasert salgssted

Skysalgssted er et nettleserbasert salgssted. Siden det kjører i nettleseren, krever ikke det skybaserte salgsstedet Windows 8.1 eller et nyere PC-basert operativsystem. Hvis programtypen **Skybasert salgssted for detaljhandel** er tilordnet til en bestemt enhet på hovedkontoret, kan denne enheten brukes i nettleseren uten behov for å laste ned eller installere en pakke. Skybasert salgssted krever en maskinvarestasjonen for å bruke maskinvare utover tastatur, kortbasert strekkodeskanning.

### <a name="hardware-profile"></a>Maskinvareprofil

Navigasjon: Gå til **Detaljhandel og handel \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Maskinvareprofiler**.

En maskinvareprofil identifiserer maskinvaren som er koblet til en kasse på salgsstedet via en integrert eller delt maskinvarestasjon. Maskinvareprofilen brukes også til å angi parametere for betalingsprosessor som skal brukes under kommunikasjon med SDK for betaling (Software Development Kit). SDK for betaling distribueres som en del av maskinvarestasjonen.

### <a name="hardware-station"></a>Maskinvarestasjon

Navigasjon: Gå til **Detaljhandel og handel \> Kanaler \> Butikker \> Alle butikker**, velg en butikk, og velg deretter hurtigfanen **Maskinvarestasjoner**.

En maskinvarestasjon er en forekomst av forretningslogikk som styrer tilbehør for salgssted. EN maskinvarestasjon installeres automatisk sammen med MPOS. Maskinvarestasjonen kan eventuelt installeres som en frittstående komponent, og deretter brukes av MPOS eller Cloud POS via en webtjeneste. Maskinvarestasjonen må være definert på kanalnivå.

## <a name="scenarios"></a>Scenarier

### <a name="mpos-with-connected-peripheral-devices"></a>MPOS med tilkoblede eksterne enheter

[![Tradisjonelt fast salgssted.](./media/traditional-300x279.png)](./media/traditional.png)

Hvis du vil koble MPOS til enheter på salgssted i et tradisjonelt scenario for fast salgssted, må du først gå til kassen og tilordne en maskinvareprofil til den. Du kan finne kassen på salgsstedet under **Detaljhandel og handel** &gt; **Kanaloppsett** &gt; **Oppsett av salgssted** &gt; **Kasser**. 

Når du har tilordnet maskinvareprofilen, synkroniserer du endringer til kanaldatabasen ved hjelp av distribusjonsplanen **Kasser**. Du finner distribusjonsplanene under **Detaljhandel og handel** &gt; **IT for handel og detaljhandel** &gt; **Distribusjonsplan**. 

Konfigurer deretter en dedikert maskinvarestasjon for kanalen. Gå til **Detaljhandel og handel \> Kanaler \> Butikker \> Alle butikker**, og velg en butikk. 

I hurtigfanen **Maskinvarestasjoner** velger du **Legg til** for å legge til en maskinvarestasjon. Velg **Dedikert** som maskinvarestasjonstype, og skriv deretter inn en beskrivelse. Feltet **Maskinvareprofil** kan stå tomt, fordi maskinvareprofilen som brukes i dette scenarioet, kommer fra selve kassen på salgsstedet. Synkroniser deretter endringene med kanalen ved å bruke distribusjonsplanen **Kanalkonfigurasjon**. Du finner distribusjonsplanene under **Detaljhandel og handel \> IT for handel og detaljhandel \> Distribusjonsplan**. 

I MPOS bruker du operasjonen **Velg maskinvarestasjon** til å velge maskinvarestasjonen som samsvarer med verdien du tidligere angav for beskrivelsen, og deretter angir du **Aktiv** for maskinvarestasjonen. 

> [!NOTE]
> - Noen endringer i maskinvareprofil, for eksempel endringer i kassaskuffer, krever at det åpnes et nytt skift etter at endringene er synkronisert til kanalen.
> - Skybasert salgssted må bruke den frittstående maskinvarestasjonen for å kommunisere med eksterne handelsenheter.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS eller Cloud POS med en frittstående maskinvarestasjon

[![Delte eksterne enheter.](./media/shared-300x254.png)](./media/shared.png)

I dette scenarioet er en frittstående maskinvarestasjon delt mellom MPOS- og Cloud POS-klienter. Dette scenarioet krever at du oppretter en delt maskinvarestasjon og angir nedlastingspakken, porten og maskinvareprofilen som maskinvarestasjonen bruker. Du definerer en ny maskinvarestasjon ved å velge hurtigfanen **Maskinvarestasjoner** i den bestemte kanalen (**Detaljhandel og handel \> Kanaler \> Butikker \> Alle butikker**) og legge til en ny maskinvarestasjon av typen **Delt**. 

Deretter angir du en beskrivelse som hjelper kassereren med å identifisere maskinvarestasjonen. I feltet **Vertsnavn** angir du URL-adressen for vertsmaskinen i følgende format: `https://<MachineName:Port>/HardwareStation`. (Erstatt **&lt;Maskinnavn:Port&gt;** med det faktiske maskinnavnet på maskinvarestasjonen.) For en frittstående maskinvarestasjon må du også angi terminal-ID-en for elektronisk pengeoverføring (EFT). Denne verdien identifiserer EFT-terminalen som er koblet til maskinvarestasjonen når betalingstilkoblingen kommuniserer med betalingsleverandøren. 

Gå deretter fra maskinen som er vert for maskinvarestasjonen, til kanalen i Headquarters, og velg maskinvarestasjonen. Velg deretter **Last ned** for å laste ned installasjonsprogrammet for maskinvarestasjonen, og installer maskinvarestasjonen. Hvis du vil ha mer informasjon om hvordan du installerer maskinvarestasjonen, kan du se [Konfigurere og installere Retail Hardware Station](retail-hardware-station-configuration-installation.md). 

Deretter, fra MPOS eller Cloud POS, bruker du operasjonen **Velg maskinvarestasjon** for å velge maskinvarestasjonen som ble installert tidligere. Velg **Par** for å opprette en sikker relasjon mellom salgsstedet og maskinvarestasjonen. Dette trinnet må fullføres én gang for hver kombinasjon av salgssted og en maskinvarestasjon. 

Når maskinvarestasjonen er sammenkoblet, brukes den samme operasjonen for å aktivere maskinvarestasjonen når den er i bruk. I dette scenarioet skal maskinvareprofilen tilordnes profilen for den delte maskinvarestasjonen i stedet for selve kassen. Hvis ingen maskinvareprofil er tilordnet direkte til maskinvarestasjonen av en eller annen grunn, brukes maskinvareprofilen som er tilordnet til kassen.

## <a name="client-maintenance"></a>Klientvedlikehold

### <a name="registers"></a>Kasser

Kasser på salgssted behandles hovedsakelig gjennom kassen, og også gjennom profiler som er tilordnet til kasser. Attributter som er spesifikke for én enkelt kasse administreres på kassenivå. Disse attributtene omfatter butikken der kassen brukes, kassenummeret, beskrivelsen og EFT-terminal-ID-en som er spesifikk for kassen.

### <a name="pos-profiles"></a>Salgsstedsprofiler

Du kan finner salgsstedsprofilene under **Detaljhandel og handel** &gt; **Kanaloppsett** &gt; **Oppsett av salgssted** &gt; **Salgsstedsprofiler**. Det er nyttig å administrere mange deler av en kasse gjennom profiler, fordi profilene kan deles av mange kasser. Profiler kan tilordnes én enkelt kasse eller, hvis en profil er effektiv på hele butikken, til butikken. Avsnittene nedenfor beskriver salgsstedsprofiler og hvordan de brukes.

#### <a name="offline-profile"></a>Frakoblet profil

Den frakoblede profilen angis på lagernivå. Den brukes til å angi innstillingene for opplasting for transaksjoner som utføres en kasse for salgssted når kassen ikke er tilkoblet kanaldatabasen.

#### <a name="functionality-profile"></a>Funksjonalitetsprofil

Funksjonsprofilen angis på butikknivå. Den brukes til å angi innstillinger for hele butikken om funksjoner som kan utføres på salgsstedet. Funksjonene nedenfor administreres gjennom funksjonsprofilen. Disse funksjonene er ordnet etter hurtigfane.

- Hurtigfanen **Generelt**:

    - International Organization for Standardization (ISO).
    - Opprette en kunde i frakoblet modus.
    - Kvitteringsprofil for e-post.
    - Påloggingsgodkjenning for sentralstab.

- Hurtigfanen **Funksjoner**:

    - Behandling av pålogging og utvidet pålogging.
    - Økonomiske og valutarelaterte deler av salgsstedet, for eksempel muligheten til registrere priser og om desimaler er nødvendig for mindre valuta.
    - Aktivere tidsregistrering gjennom salgsstedet.
    - Hvordan produktene og betalinger vises på salgsstedet og på kvitteringer.
    - Administrasjon av sagsoppgjør.
    - Parametere for transaksjonsbevaring for kanaldatabase.
    - Hvordan kunder slås opp og opprettes fra salgsstedet.
    - Hvordan rabatter beregnes.

- Hurtigfanen **Beløp**:

    - Maksimums- og minimumspriser som er tillatt.
    - Rabattprogram og -beregning.

- Hurtigfanen **Informasjonskoder**:

    - Alle aspekter av hvordan informasjonskoder behandles på salgsstedet. Hvis du vil ha mer informasjon, kan du se [Informasjonskoder og informasjonskodegrupper](info-codes-retail.md).

- Hurtigfanen **Kvitteringsnummerering**:

    - Angi masker for kvitteringsnummerering, som kan omfatte segmenter for butikknummer, terminalnummer, konstanter og om salg, returer, salgsordrer og tilbud skal skrives ut i separate serier, eller om alle skal følge samme sekvens.

#### <a name="receipt-profiles"></a>Kvitteringsprofiler

Kvitteringsprofiler tilordnes direkte til skrivere i maskinvareprofilen. De brukes til å angi hvilke kvitteringstyper som skrives ut på en bestemt skriver. Profilene omfatter innstillinger for kvitteringsformater og innstillinger som bestemmer om kvitteringer alltid skrives alltid, eller om kassereren blir bedt om å bestemme om kvitteringen skal skrives ut. Ulike skrivere kan også bruke ulike kvitteringsprofiler. Skriver 1 er for eksempel en standard termisk kritteringsskriver og har derfor mindre kvitteringsformater. Skriveren 2 er imidlertid en skriver for kvitteringer i full størrelse som brukes til å skrive ut kvitteringer for kundebestillinger, som krever mer plass. Hvis du vil ha mer informasjon, kan du se [Konfigurere en kvitteringsprofil](configure-emailed-receipt-formats.md#configure-a-receipt-profile).

#### <a name="hardware-profiles"></a>Maskinvareprofiler

Maskinvareprofiler er forklart som en komponent for klientoppsett tidligere i dette emnet. Maskinvareprofiler tilordnes direkte til kassen på salgsstedet eller til en delt maskinvareprofil og brukes til å angi typene enheter som en bestemt kasse på salgsstedet eller maskinvareprofil bruker. Maskinvareprofiler kan også brukes til å angi EFT-innstillinger som brukes til å kommunisere med SDK for betaling.

#### <a name="visual-profiles"></a>Visuelle profiler

Visuelle profiler brukes til å angi temaet for en bestemt kasse og tilordnes på kassenivå. Profilene omfatter innstillinger for programtypen som brukes (MPOS eller Cloud POS), uthevingsfarge og tema, skriftutvalget, bakgrunnen på påloggingssiden og bakgrunnen for salgsstedet. Hvis du vil ha mer informasjon, kan du se [Opprette visuelle profiler for salgssted](tasks/create-pos-visual-profile-2016-02.md). 

### <a name="custom-fields"></a>Tilpassede felter

Du kan opprette egendefinerte felt for å legge til felt som ikke følger med som standard, for salgsstedet. Hvis du vil ha mer informasjon om hvordan du bruker egendefinerte felt, kan du se [blogginnlegget om å arbeide med egendefinerte felt](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Språktekst

Ved overstyre standardstrenger på salgsstedet ved hjelp av tekstoppføringer for språket. Hvis du vil overstyre en streng på salgsstedet, legge til en ny språktekstlinje. Angi deretter en ID, standardstrengen som skal overstyres og teksten som skal vises på salgsstedet i stedet for standardstrengen.

### <a name="channel-reports-configuration"></a>Konfigurasjon av kanalrapporter

Du definere rapportene som er tilgjengelige for kanalen på siden **Konfigurasjon av kanalrapporter**. Du kan opprette nye rapporter ved å angi XML-definisjonen for rapporten, og tilordne rapporten til en bestemt tillatelsesgruppe på salgsstedet.

### <a name="devices"></a>Enheter

Enheter er beskrevet tidligere i denne artikkelen. De brukes til å administrere aktiveringen av en bestemt kasse på salgsstedet. Enheter brukes også for å angi programmet som brukes for en bestemte kasse, og installasjonspakken som skal brukes for å installere MPOS-klienten. Her er statusene for enhetsaktivering:

- **Venter** – Enheten er klar til å bli aktivert.
- **Aktivert** – Enheten er aktivert.
- **Deaktivert** – Enheten er deaktivert i for hovedkontoret eller gjennom salgsstedet.
- **Deaktivert** – Enheten er deaktivert.

Aktiveringsrelatert tilleggsinformasjon inkluderer arbeideren som endret aktiveringsstatus for enheten, og et tidsstempel for aktiveringen og om enhetskonfigurasjonen er godkjent.

### <a name="client-data-synchronization"></a>Klientdatasynkronisering

Alle endringer i en klient på salgsstedet, unntatt endringer i statusen for enhetsaktivering, må synkroniseres til kanaldatabasen for å tre i kraft. Hvis du vil synkronisere endringer til kanaldatabasen, går du til **Detaljhandel og handel** &gt; **IT for detaljhandel og handel** &gt; **Distribusjonsplan**, og kjører den påkrevde distribusjonsplanen. For klientendringer må du kjøre distribusjonsplanene **Kasser** og **Kanalkonfigurasjon**.

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere og installere Retail Hardware Station](retail-hardware-station-configuration-installation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

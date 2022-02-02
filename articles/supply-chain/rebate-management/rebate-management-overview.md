---
title: Oversikt over rabattbehandlingsmodul
description: Dette emnet gir en oversikt over rabattbehandlingsmodulen for Microsoft Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 75311e137df522c476b938f660b8305004396137
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985513"
---
# <a name="rebate-management-module-overview"></a>Oversikt over rabattbehandlingsmodul

[!include [banner](../includes/banner.md)]

Du kan bruke **Rabattbehandling**-modulen til å opprette kontrakter eller avtaler mellom forretningen og kundene eller leverandørene, slik at du kan beregne rabatter, fradrag og royalty. Rabattbehandling sporer og vedlikeholder transaksjoner for rabatt og fradrag på et sentralt sted der brukere effektivt kan opprette, gjennomgå og behandle dem.

Rabattbehandling støtter oppretting, vedlikehold og behandling av *rabatter*. En rabatt er tilbakebetaling av en del av innkjøpsprisen av en selger eller kjøper. Rabatter er vanligvis basert på kjøp av et bestemt antall eller verdien av varer i en bestemt periode. I motsetning til avslag blir rabatter utført etter at innkjøpsbeløpet er fullt fakturert.

Rabattbehandling støtter også *fradrag*. Et fradrag er kompensasjon, en vurdering eller et gebyr som betales enten for lisens eller rettighetene som brukes av immaterielle rettigheter som merke, opphavsrett eller patent, eller for privilegiet å bruke en naturressurs til et formål som for eksempel opphavsrett, opphavsrett eller utvinning. Fradrag beregnes vanligvis som en prosent av omsetningen eller fortjeneste fra realisert bruk. Jo mer immaterielle rettigheter eller ressurser som brukes, desto større er fratrekket som blir realisert.

I tillegg støtter rabattbehandling *kunderoyalty*. Royalty er betalinger som en part foretar til lisenstakeren eller franchisetakeren for rett til å bruke et anleggsmiddel.

Med rabattbehandling kan du definere posteringsprofiler for avsetninger, rabatter og avskrivinger. Posteringer kan også defineres for en bestemt kunde eller leverandør. På denne måten kan avtaler som ikke gjelder alle kunde- eller leverandørscenarier, spores via posteringer.

Rabattransaksjoner genereres automatisk, basert på beregningsmetoden som er valgt og planlagt i satsvise jobber. I tillegg kan du definere arbeidsflyter for å administrere, se gjennom og godkjenne avtaler.

## <a name="basis-calculation"></a>Grunnlagsberegning

Kunderabatter, kunderoyalty og leverandørrabatter kan bruke forskjellige grunnlag, avhengig av dine forretningskrav:

- Kunderabatter kan være basert på salgsordrer, følgesedler eller fakturaer.
- Kunderoyalty kan være basert på salgsordrer, følgesedler eller betalte fakturaer.
- Leverandørrabatter kan være basert på enten bestillinger eller salgsordrer. De kan beregnes på grunnlag av produkter som kjøpes fra rabattleverandøren, og selges til kunder via salgsfakturaer.

## <a name="flexible-calculations"></a>Fleksible beregninger

Perioder for rabattberegning er tilgjengelige for både kundeavtaler og leverandøravtaler. En beregningsperiode definerer lengden på avtalen, beregningsfrekvensen og beregningsperioden. Rabattene kan avsettes basert på salgsordreantallene eller -beløpene for kvalifiserte produkter i løpet av rabattperioden.

For hver avtaleberegning kan en av følgende perioder angis:

- Faktura
- Dag
- Uke
- Måned
- Kvartal
- År
- Tilpasset periode
- Ethvert multiplum av enhver av periodene som er oppført tidligere

Beregningen kan brukes på enkeltkunder og -produkter, grupper av kunder og produkter eller alle kunder og produkter. Rabatter som har flere detaljlinjer, kan ha ulike kvalifiserende datoområder. Avsetnings- og kravperiodene kan være forskjellige. Avsetningene kan for eksempel behandles hver dag, mens krav behandles én gang per måned.

Rabatter kan konfigureres basert på mange forskjellige parametere. De kan for eksempel konfigureres som en prosent, en sats eller et fast beløp. Det finnes fire beregningsmetoder:

- Trinnvis
- Kumulativ
- Rullende
- Total verdi

Resultatene av rabattberegning kan også reduseres av andre rabatter, avhengig av om rabatten er satt opp til å beregne på grunnlag av nettobeløpet.

På leverandørsiden kan rabatter som er basert på salgsordrer, beregne prisen basert på en FIFO-regel (først-inn-først-ut), siste innkjøpspris, gjennomsnittlig innkjøpspris eller salgspris.

## <a name="rebate-target-transactions"></a>Rabattmåltransaksjoner

Utdataene som rabattavtalen eller avtalen genererer, kan være finans eller varer.

Finansutdata bestemmes av betalingstypen som er tilordnet avtalen fra posteringsprofilen. Disse utdataene kan omfatte kundefradragsjournaler, fritekstfakturaer og leverandørfakturaer. Av revisjonshensyn inneholder transaksjoner for økonomiske rabattmål en referanse til den opprinnelige rabattavtalen.

Vareutdata oppretter en gratis varesalgsordre for kunderabatter og en bestilling for leverandørfakturaer. Transaksjoner for varerabattmål inneholder alternativer for å bestemme hvilken rabattreferanse som skal angis på gratisvaresalgsordren eller bestillingen.

## <a name="accurate-rebate-calculations"></a>Nøyaktige rabattberegninger

Kombinasjonen av de tilknyttede avtalene, frekvensen av beregningene, beregningsgrunnlaget og beregningsmetoden som er valgt, bestemmer nøyaktigheten og presisjonen i rabattberegningene. Rabattavsetningene kan brukes til å avsette posterte verdier og verdier det er gjort krav på.

Avsetningene kan administreres daglig, ukentlig, månedlig eller i henhold til en egendefinert periode. Funksjonaliteten kan imidlertid tildele eller betale rabatten, eller motta betaling av den, til en hvilken som helst definert frekvens som er den samme som eller lengre enn avsetningsfrekvensen. Avskriving bruker samme frekvens som rabatten. Brukere kan enkelt justere en plan eller betalingsbeløp når som helst i løpet av utbetalingen.

Brukerne trenger ikke lenger å håndtere avtaler eller avsetninger i to trinn. Avsetninger og avskrivinger posteres direkte til finans. Kreditnotaer kan også opprettes automatisk. Derfor er det fullstendig integrasjon med leverandører og kunder. Under behandlingen vurderer beregningene utligningsrabatter, betalte fakturaer, forhandlerrabatter og eksisterende kreditnotaer for å sikre at beløp og verdier beregnes nøyaktig.

Når rabatter beregnes, oppretter prosessen transaksjoner som kan gjennomgås før postering skjer. En separat prosess posterer rabattbehandlingstransaksjoner. En journal, kreditnota eller debettransaksjon kan deretter opprettes under postering til foreslåtte transaksjoner. Rapporteringskontoutdrag og transaksjonsoversikter kan hentes for å sikre samsvar, effektivitet og gjennomsiktighet.

## <a name="guaranteed-royalty-payments"></a>Garanterte royalty-betalinger

I Rabattbehandling gjør automatisk betalingsgenerering det mulig å håndtere royalty på en rask og enkel måte, selv om minimumskravene er gjeldende.

## <a name="maximizing-spend-versus-rebates"></a>Maksimer forbruk kontra rabatter

Leverandører og produkter kan grupperes etter territorium, og du kan få forskjellige tilbud, avhengig av landet eller regionen for transaksjonen. Når brukere velger produkter, kan de definere varene som er inkludert, og antallet varer som skal brukes i rabattutligingen.

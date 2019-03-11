---
title: Detaljhandelsutdrag
description: Dette emnet beskriver hvordan utdrag opprettes og posteres.
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 9e88a8b22b73aca5c2cee6984ecad3c62e597102
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "347704"
---
# <a name="retail-statements"></a>Detaljhandelsutdrag

[!include [banner](includes/banner.md)]

I Microsoft Dynamics 365 for Retail brukes posteringsprosessen for utdraget til å ta hensyn til transaksjoner som forekommer i sky-salgsstedet eller Modern POS (MPOS). Posteringsprosessen for utdrag bruker distribusjonstidsplanen til å hente et sett med salgsstedstransaksjoner til klienten på hovedkontoret. Parameterne som er definert på sidene **Detaljhandelsparametere** og **Lagre**, brukes til å velge transaksjonene som hentes til enkeltstående utdrag.

Illustrasjonen nedenfor viser utdragposteringsprosessen. I denne prosessen vil transaksjoner som registreres i salgsstedet, overføres til klienten ved hjelp av Detaljhandel Planlegger. Når klienten mottar transaksjonene, kan du opprette, beregne og bokføre transaksjonskontoutdraget for butikken.

[![Utdragsposteringsprosess](./media/retail-statements.png)](./media/retail-statements.png)

## <a name="creating-and-posting-statements"></a>Opprette og postere utdrag

Du kan opprette et utdrag manuelt eller ved hjelp av satsvise prosesser du konfigurerer for å kjøre regelmessig i løpet av dagen. I begge tilfeller brukes fremgangsmåten nedenfor til å opprette og postere utdrag.

### <a name="create-the-statement"></a>Opprett utdraget

Dette trinnet identifiserer butikken som utdraget opprettes manuelt for. Hvis du konfigurerer en satsvis prosess, kan du opprette utdrag for alle butikker automatisk, basert på en tidsplan du definerer.

### <a name="calculate-the-statement"></a>Beregne utdraget

I dette trinnet velges transaksjonslinjene basert på kriterier som er definert for hver butikk på sidene **Detaljhandelsparametere** og **Lagre**. På disse sidene kan du definere kriteriene og angi hvordan transaksjonene skal beregnes. Hvis du vil vise en liste over transaksjonene som er inkludert i utdraget før du kan beregne utdraget, bruker du siden **Transaksjoner**.

Utdragsberegningen bruker kasseoppgjør fra kassene som opptelt beløp. Du kan eventuelt angi det opptelte beløpet manuelt. Utdraget viser differansen mellom salgsbeløpet for transaksjonene og det faktiske, opptelte beløpet i alle betalingsmåter. Utdraget posteres bare hvis denne differansen er mindre enn maksimal posteringsdifferanse som er angitt for butikken.

> [!NOTE]
> Utdragsberegningsprosessen bruker den globale nummerserien.

Når du beregner et utdrag, omfatter beregningen følgende oppgaver:

- For det valgte datoområdet kan du merke transaksjoner som ikke ble inkludert i forrige utdragsberegning.
- Beregn det totale beløpet som ble betalt i de valgte transaksjonene. Resultatene vises i utdragslinjene, avhengig av utdragsmetoden:

    - Hvis utdragsmetoden er **Total**, opprettes en linje for hver betalingsmåte i de valgte transaksjonene.
    - Hvis utdragsmetoden er **Stab**, opprettes en linje for hver betalingsmåte i transaksjonene som ble foretatt av det valgte stabsmedlemmet.
    - Hvis utdragsmetoden er **Salgsstedsterminal**, opprettes en linje for hver betalingsmåte i transaksjoner som ble utført for den valgte kassen.
    - Hvis utdragsmetoden er **Skift**, opprettes en linje for hver betalingsmåte i transaksjoner som ble utført under et skift.

Hvis det er merket av for **Del etter utdragsmetode** på siden **Lagre**, et separat utdrag opprettes basert på verdien som er valgt i feltet **Utdragsmetode**.

Hvis arbeidstiden i butikken overskrider midnatt, kan du konfigurere postering av utdrag slik at det er basert på endt arbeidsdag i stedet for endt kalenderdag.

På **Lagre**-siden, i hurtigkategorien **Utdrag/avslutning** i feltet **Slutt på arbeidsdag** angir du tidspunktet som den siste transaksjonen må registreres innen, for å bli inkludert i utdraget for denne arbeidsdagen. Merk av for **Poster som arbeidsdag** for å postere transaksjonene i løpet av samme arbeidsdag. Når utdraget er postert, kan transaksjoner som er registrert på samme arbeidsdag, inkluderes i den samme salgsordren, selv om enkelte transaksjoner skjer før midnatt og andre transaksjoner skjer etter midnatt.

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a>Eksempel: Postere et utdrag for en arbeidsdag som strekker seg over to dager i kalenderen

Et lager er åpent mellom 08:00 og 03:00, og **Poster som arbeidsdag** er merket av i butikkens konfigurasjon. 31. mai registrerer lageret transaksjoner mellom 08:00 og midnatt. Lageret registrerer også transaksjoner mellom 12:01 og 03:00 1. juni.

Når butikken posterer oppgaven for avslutning av arbeidsdagen, vil salgsordren genereres, inkludere alle transaksjoner som ble registrert i arbeidstiden mellom 08:00 og 03:00, selv om transaksjonene fant sted i løpet av to dager, 31. mai og 1. juni.

Hvis merket for **Poster som arbeidsdag** fjernes for den samme butikken, genereres separate salgsordrer når butikken posterer oppgaven for avslutning av arbeidsdagen. Én salgsordre inneholder transaksjoner som ble registrert mellom arbeidstiden 08:00 og midnatt den 31. mai, og den andre salgsordren inneholder transaksjoner som ble registrert mellom virketimene 12:01 og 03:00. den 1. juni.

> [!NOTE]
> Før du kan opprette utdrag, må du lukke skiftene i utdragsperioden.

### <a name="post-the-statement"></a>Postere utdraget

Når du posterer et utdrag, opprettes salgsordrer og fakturaer for detaljhandelssalgene i utdraget.

- Hentesalg aggregeres i én salgsordre og faktureres til standardkunden som er tilordnet butikken.
- Detaljhandelsalg der en kunde ble lagt til for transaksjonen i Microsoft Dynamics 365 for Retail POS, genererer separate salgsordrer og fakturaer, én for hver unike kunde.

Betalingsjournaler opprettes automatisk for betalingene i utdraget, og lageret oppdateres for salgsstedsbutikken.

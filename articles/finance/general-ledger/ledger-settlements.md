---
title: Utligninger
description: Denne artikkelen forklarer hvordan du bruker siden Utligninger til å utligne finanstransaksjoner og tilbakeføre utligninger.
author: kweekley
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 6357629f83873437eb62a4839fafd8efd98fffc1
ms.sourcegitcommit: 9041fa6e00ecbdf1a1880659d9bdfff4d888f20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/22/2022
ms.locfileid: "9800638"
---
# <a name="ledger-settlements"></a>Utligninger

[!include [banner](../includes/banner.md)]

Utligning er prosessen ved å samsvare debet- og kredittransaksjoner i økonomimodulen. Utligningen av debet- og kreditbeløpene brukes til å avstemme saldoen i finanskontoen med de detaljerte transaksjonene som utgjør denne saldoen.

Utlignede transaksjoner kan utelates fra forespørsler og rapporter. På denne måten er det enklere å analysere de åpne finanstransaksjonene som utgjør saldoen for finanskontoen.

> [!IMPORTANT] 
> Modulene Leverandører (AP) og Kunder (AR) har også utligning av fakturaer og betalinger. Når utligning skjer i AR- og AP-underhovedbøkene, utlignes ikke de tilsvarende hovedbokoppføringene automatisk.

## <a name="ledger-settlement-features"></a>Funksjoner for hovedbokutligning
I Microsoft Dynamics 365 Finance versjon 10.0.21 ble alternativet **Aktiver avanserte utligninger** fjernet fra siden **Parametere for økonomimodul**. Avansert utligning er nå alltid aktivert.
I Finance versjon 10.0.25 ble funksjonen **Forståelse av finansutligning og årsavslutning** innført. Denne funksjonen endrer den grunnleggende funksjonaliteten både i utligning og årsavslutning for økonomimodulen. Før du aktiverer denne funksjonen i arbeidsområdet **Funksjonsbehandling**, kan du se [Forståelse av finansutligning og årsavslutning](awareness-between-ledger-settlement-year-end-close.md).

## <a name="set-up-ledger-settlement"></a>Konfigurerer utligning i hovedbok
Du må velge hovedkontoene du vil utføre hovedbokutligning for. Det er to måter å velge disse hovedkontoene på.

1. Gå til **Økonomimodul** > **Finansoppsett** > **Parametere for økonomimodul**.
2. På **Utligninger**-fanen velger du kontoplanene du vil velge hovedkontoene fra.
3. Velg hovedkontoene du vil utføre hovedbokutligning for. Fordi kontoplaner er globale, vil alle firmaer som de valgte kontoplanene er tilordnet til, ha de samme hovedkontoene valgt for hovedbokutligning.

  - eller -

1. Gå til **Økonomimodul** > **Periodiske oppgaver** > **Utligninger**.
2. Velg **Utligningskontoer**.
3. I dialogboksen velger du kontoplanene og hovedkontoene du vil utføre hovedbokutligning for. Denne dialogboksen er en snarvei. Eventuelle hovedkontoer du legger til her, gjenspeiles også på siden **Parametere for økonomimodul**.

Du kan bruke de samme grunnleggende fremgangsmåtene for å fjerne hovedkontoer fra finansutligning når som helst. Fjerning av en hovedkonto har ingen innvirkning på tidligere finansutligninger. Hovedkontoen og transaksjonene vil imidlertid ikke lenger vises på siden **Utligning**.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Utlign transaksjoner
Hvis du vil utligne finanstransaksjoner, følger du disse trinnene.

1. Gå til **Økonomimodul** > **Periodiske oppgaver** > **Utligninger**.
2. Definer filtrene øverst på siden:

    - Velg et datoområde. Du kan også velge en datointervallkode for å automatisk fylle ut datoområdet. Vi anbefaler ikke at du utligner transaksjoner som på går over flere regnskapsår.
    - Endre posteringslaget etter behov. Du kan ikke utligne transaksjoner som er i forskjellige posteringslag.
    - Velg et finansdimensjonsett for å vise hovedkontoen og dimensjonene separat.

3. Velg **Vis transaksjoner** for å vise alle transaksjonene som samsvarer med filtrene du angav, og listen over kontoer som du angav da du konfigurerte kontoplanen i den forrige delen.

    - Hvis du endrer noen av filtrene eller dimensjonssettene, må du velge **Vis transaksjoner** på nytt.
    - Hvis du vil filtrere transaksjonene til en enkelt hovedkonto, bruker du filteret i feltet **Finanskonto**. Vi anbefaler ikke at du utfører hovedbokutligning for transaksjoner som posteres til ulike hovedkontoer.

4. Velg linjer for utligning. Verdien i feltet **Valgt beløp** øverst på siden økes eller reduseres for å gjenspeile det totale beløpet på de valgte linjene.
5. Når du er ferdig med å velge transaksjoner, velger du **Merk som valgt**. For hver valgte transaksjon vises det en hake i **Merket**-kolonnen. I tillegg økes eller reduseres verdien i feltet **Merket beløp** over rutenettet for å gjenspeile det totale beløpet på de merkede linjene.
6. Når verdien i feltet **Merket beløp** er **0** (null), velger du **Utligne merkede transaksjoner**. Statusen for de merkede transaksjonene oppdateres til **Utlignet**.

    > [!IMPORTANT]
    > Alle transaksjoner du har merket for utligning for den aktive juridiske enheten, blir utlignet, selv om de ikke vises i øyeblikket på Utligning-siden fordi du brukte et filter.

## <a name="make-transactions-easier-to-find"></a>Gjøre det enklere å finne transaksjoner
Siden **Utligninger** inkluderer funksjoner som gjør det enklere å vise transaksjoner som er nødvendige for utligning.

- Bruk filteret **Merket** til å filtrere transaksjoner basert på om **Merket**-avmerkingsboksen for transaksjonene er merket av.
- Bruk **Status**-filteret til å filtrere transaksjoner basert på statusen.
- Velg **Sorter etter absolutt beløp** for å sortere beløpene etter absolutt verdi. På denne måten kan du gruppere debet- og kreditoppføringer som har samme beløp.

## <a name="reverse-a-settlement"></a>Tilbakeføre en utligning
Du kan tilbakeføre en utligning som ble gjort ved en feiltakelse.

1. Følg trinn 1 til 3 i delen [Utligne transaksjoner](#settle-transactions) for å vise transaksjonene du er interessert i.
2. Velg **Utlignet** i **Status**-filteret.
3. Velg linjer for tilbakeføring.
4. Velg **Tilbakefør merkede transaksjoner**. Statusen for alle transaksjoner som har samme utlignings-ID, oppdateres til **Ikke utlignet**.

    > [!IMPORTANT]
    > Alle transaksjoner som har samme utlignings-ID, blir tilbakeført, selv om de ikke er merket. Fire linjer ble for eksempel merket og utlignet. Alle de fire linjene har samme utlignings-ID. Hvis du merker én av disse fire linjene og deretter velger **Tilbakefør merkede transaksjoner**, tilbakeføres alle de fire linjene.

## <a name="unmark-for-selected-users"></a>Fjern markering for valgte brukere
Velg **Fjern markering for valgte brukere** for å fjerne merket for utlignede transaksjoner for alle juridiske enheter etter bruker-ID. Dette gjør for eksempel at en regnskapsansvarlig kan fjerne merket for transaksjoner for en bruker som dro på ferie før han eller hun er ferdig med utligningen, eller for en bruker som har forlatt organisasjonen. Handlingen gjør det mulig for en annen bruker å merke for utligning.


## <a name="unmark-all-transactions"></a>Fjern merket for alle transaksjoner
Velg **Fjern merket for alle transaksjoner** for å fjerne merket for alle utlignede transaksjoner for alle brukere og alle juridiske enheter. Denne handlingen er tilgjengelig for administratorrollen.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

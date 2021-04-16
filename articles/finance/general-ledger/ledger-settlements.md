---
title: Utligninger
description: Dette emnet forklarer hvordan du bruker siden Utligninger til å utligne finanstransaksjoner og tilbakeføre utligninger.
author: mikefalkner
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: b9279c264294d95c2a06f9614189b26ce8f78566
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826528"
---
# <a name="ledger-settlements"></a>Utligninger

[!include [banner](../includes/banner.md)]

Med utligninger kan du samsvare debet- og kredittransaksjoner i økonomimodulen og merke dem som utlignet. På denne måten kan du kontrollere at relaterte transaksjoner er fjernet. Du kan også tilbakeføre utligninger hvis de ble opprettet ved en feiltakelse.

## <a name="enable-advanced-ledger-settlements"></a>Aktivere avanserte utligninger

Siden for avanserte utligninger gir flere muligheter for filtrering og valg av transaksjoner. Gjør følgende for å aktivere siden for avanserte utligninger.

1. Velg **Økonomimodul** \> **Finansoppsett** \> **Parametere for økonomimodul**. 
2. I fanen **Finansutligninger** setter du alternativet **Avanserte utligninget** til **Ja** for å aktivere funksjonen for avansert utligning. Siden **Finansutligninger** vil bli brukt når du velger **Utligninger** i **Periodiske oppgaver**. 
3. Du må angi listen over kontoer som skal brukes for utligninger for hver kontoplan. Denne listen brukes til å filtrere listen over transaksjoner som vises på siden **Utligninger**. I listen **Kontoplan** velger du en kontoplan, og deretter velger du **Ny** for å legge til nye kontoer i listen.

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a>Utlign transaksjoner ved hjelp av siden for avanserte utligninger

Hvis du vil utligne finanstransaksjoner, følger du disse trinnene.

1. Velg **Økonomimodul** \> **Periodiske oppgaver** \> **Utligninger**.
2. Definer filtrene øverst på siden:

    - Velg et datointervall, eller velg **Datointervallkode** for å automatisk fylle ut datointervallet.
    - Endre posteringslaget etter behov.
    - Velg et finansdimensjonsett for å vise finanskontoen og dimensjonene separat.

3. Velg **Vis transaksjoner** for å vise alle transaksjonene som samsvarer med filtrene du angav, og listen over kontoer som du angav da du konfigurerte kontoplanen i den forrige delen. Hvis du endrer noen av filtrene eller dimensjonssettene, må du velge **Vis transaksjoner** på nytt.
4. Velg én eller flere linjer som du vurderer for utligning. Verdien for feltet **Valgt beløp** øverst på siden økes eller reduseres med det totale beløpet på linjene som du har valgt.
5. Når du er ferdig med å velge transaksjoner, velger du **Merk som valgt**. Det vises en hake i **Merket**-kolonnen for hver transaksjon du har valgt. I tillegg økes eller reduseres verdien for feltet **Merket beløp** over rutenettet med det totale beløpet på linjene du merket.
6. Når **Merket beløp**-verdien er **0** (null), velger du **Utligne merkede transaksjoner**. Statusen for de merkede transaksjonene oppdateres til **Utlignet**.

## <a name="make-transactions-easier-to-find"></a>Gjøre det enklere å finne transaksjoner

Siden **Finansutligninger** inkluderer funksjoner som gjør det enklere å vise transaksjoner som er nødvendige for utligning.

- Knappen **Fjern merket** sletter feltet **Merket** for alle linjer som er valgt.
- Filteret **Merket** lar deg filtrere transaksjoner basert på om **Merket**-feltet for transaksjonene er merket eller fjernet.
- Filteret **Status** lar deg filtrere transaksjoner basert på om den tilhørende statusen er **Utlignet** eller **Ikke utlignet**.
- Knappen **Sorter etter absolutt beløp** lar deg sortere beløpene etter absoluttverdi, slik at du kan gruppere debet og kreditt som har samme beløp.

## <a name="reverse-a-settlement"></a>Tilbakeføre en utligning

Du kan tilbakeføre en utligning som ble gjort ved en feiltakelse.

1. Følg trinn 1 til 3 i delen "Utlign transaksjoner ved hjelp av siden for avanserte utligninger" for å vise transaksjonene du leter etter.
2. Velg **Utlignet** i **Status**-filteret.
3. Velg én eller flere linjer som du vurderer for tilbakeføring. Verdien for feltet **Valgt beløp** øverst på siden økes eller reduseres med det totale beløpet på linjene som du har valgt.
4. Når du er ferdig med å velge transaksjoner, velger du **Merk som valgt**. Det vises en hake i **Merket**-kolonnen for hver transaksjon du har valgt. I tillegg økes eller reduseres verdien for feltet **Merket beløp** øverst på siden med det totale beløpet på linjene du merket.
5. Når **Merket beløp**-verdien er **0** (null), velger du **Tilbakefør merkede transaksjoner**. Statusen for de merkede transaksjonene oppdateres til **Ikke utlignet**.

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a>Oppdater listen over kontoer som er inkludert i listen over transaksjoner

Velg **Utligningskontoer** for å åpne en dialogboks der du kan redigere kontoene som er inkludert i listen over transaksjoner. Velg **Ny** for å legge til nye kontoer i listen. Denne listen brukes til å filtrere listen over transaksjoner som vises på siden **Utligninger**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
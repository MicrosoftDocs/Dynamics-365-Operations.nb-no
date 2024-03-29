---
title: Finansdimensjonssett
description: Denne artikkelen beskriver finansdimensjonssett og gir noen tips for optimalisering av bruken.
author: yukonpeegs
ms.date: 03/07/2022
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 3d4c15504b2ad128493e1bafa36aed271c2ab6dc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864288"
---
# <a name="financial-dimension-sets"></a>Finansdimensjonssett

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver finansdimensjonssett og gir noen tips for optimalisering av bruken.

Et dimensjonssett er en sortert liste over finansdimensjoner som kan brukes til å oppsummere økonomimoduldata på en brukerdefinert måte. En primær bruk av dimensjonssett er å definere en råbalanse.

Det eneste standard dimensjonssettet er dimensjonssettet som bare inneholder hovedkontoen.

Du bruker siden **Finansdimensjonssett** til å opprette og behandle finansdimensjonssett.

## <a name="dimension-set-balances"></a>Dimensjonssettsaldoer

Et dimensjonssett kan ha saldoer som er basert på finansdimensjonene. Saldoene finnes i økonomimodulen og er basert på dimensjonssettdefinisjonen. Saldoene oppsummeres fra økonomimoduldataene for å forbedre ytelsen når de hentes (for eksempel når det genereres en råbalanse).

## <a name="create-balances"></a>Opprett saldoer

Bruk knappen **Opprett saldoer** til å initialisere saldoene for et dimensjonssett som ikke har saldoer for øyeblikket.

> [!NOTE]
> Vi anbefaler at du begrenser antall dimensjonssett som har saldoer, fordi saldooppdateringer påvirker alle posteringsaktiviteter i økonomimodulen.

## <a name="update-balances"></a>Oppdater saldoer

Bruk **Oppdater saldoer**-knappen til å inkludere den siste posteringsaktiviteten for økonomimodulen i saldoene. Saldooppdateringer er enkle operasjoner. De må bare behandle posteringsaktiviteten for økonomimodulen som har inntruffet siden forrige oppdatering.

> [!NOTE]
> Visning av råbalansen tvinger en oppdatering for å sikre at saldoene som vises, er gjeldende. Vurder å bruke en gjentakende satsvis jobb, slik at oppdateringer av de mest brukte dimensjonssettene går raskt. På denne måten kan du redusere tiden som råbalansebrukere må vente.

## <a name="rebuild-balances"></a>Bygg saldoer på nytt

Bruk knappen **Bygg saldoer på nytt** til å opprette saldoene på nytt fra begynnelsen. På denne måten kan du sikre at de samsvarer med dataene i økonomimodulen. En gjenoppbygging av saldoer krever masse behandling, og bør vanligvis ikke være nødvendig.

> [!NOTE]
> Hvis du har et scenario som regelmessig krever en gjenoppbygging av saldoer, anbefaler vi at du kontakter kundestøtte. Kundestøtte kan hjelpe deg med å finne ut hvorfor saldoer ikke samsvarer med dataene i økonomimodulen.

## <a name="clear-balances"></a>Avstem saldoer

Bruk **Tøm saldoer**-knappen til å tømme saldoene og stoppe flere oppdateringer. Dimensjonssettet vil ikke lenger påvirke posteringsaktiviteter i økonomimodulen.

## <a name="delete-a-dimension-set"></a>Slette et dimensjonssett

Ikke **slett og opprett dimensjonssett på nytt** som noen form for omgåelse for å løse potensielle problemer med saldodataene for et bestemt dimensjonssett. Det er kostbart å opprette et dimensjonssett på nytt. Hvis du vil ha mer hjelp med problemer, kan du kontakte kundestøtte. 


Hvis du vil ha mer informasjon, kan du se [Finansdimensjoner](financial-dimensions.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Sømløs bryter for frakoblet modus for gavekort- og kreditnotaoperasjoner
description: Denne artikkelen gir en oversikt over forbedringer som gir en sømløs bryter i frakoblet modus for bestemte betalingstyper.
author: BrianShook
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: e0416a61bd5fd3b875b427ad8a6313d0e9936f0d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869167"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a>Sømløs bryter for frakoblet modus for gavekort- og kreditnotaoperasjoner

[!include [banner](../includes/banner.md)]

Hvis en salgsstedsenhet (POS) mister tilkoblingen til kanaldatabasen, kan de fleste de fleste POS-operasjoner og -transaksjoner som var i gang, fortsette etter at kassereren får en advarsel om tap av tilkobling. I noen tilfeller har transaksjoner imidlertid elementer som er avhengige av service i sanntid, og disse elementene støttes ikke når POS er frakoblet. Denne artikkelen beskriver noe funksjonalitet som bidrar til å redusere virkningen av tapt tilkobling i disse scenariene.

## <a name="completing-gift-card-transactions-in-offline-mode"></a>Fullføring av gavekorttransaksjoner i frakoblet modus

Interne gavekort er avhengige av service i sanntid, fordi saldoen for gavekortene må vedlikeholdes sentralt i Microsoft Dynamics 365 Commerce Headquarters. For å hindre svindel eller andre synkroniseringsproblemer låses gavekort så snart de er lagt til i en transaksjon. Låsefunksjonen sikrer at et gavekort ikke kan brukes på flere terminaler samtidig. Når en transaksjon er fullført, blir gavekortet oppdatert og låst opp.

Hvis tilkoblingen til salgsstedet forsvinner etter at et gavekort er lagt til i en transaksjon, kan gavekortet imidlertid bli ubrukelig. For å hindre denne situasjonen har Dynamics 365 Commerce en parameter som gjør det mulig å fullføre transaksjoner som inneholder en gavekortlinje mens POS er frakoblet. Når denne parameteren er aktivert, vil gavekorttransaksjoner som fremtvinges frakoblet, lagres sammen med frakoblede transaksjoner, og de blir synkronisert til Commerce Headquarters når de frakoblede transaksjonene er synkronisert. Synkroniseringen vil også låse opp gavekortet slik at det kan brukes ved en annen terminal.

Hvis du vil aktivere funksjonaliteten for å fullføre gavekorttransaksjoner etter at du har byttet til frakoblet modus, kan du gå til kategorien **Postering** på siden **Parametere for Commerce**. I denne kategorien finner du hurtigfanen **Gavekort**, og angi **Tillat avslutning av gavekorttransaksjoner i frakoblet modus** til **Ja**.

![Frakoblet innstilling for gavekort.](../media/gift.png)

Commerce-parametere bufres vanligvis. Etter at innstillingen for denne parameteren er oppdatert og distribusjonsplanen startes for å synkronisere endringen til kanalen, kan det derfor ta opptil 24 timer før endringen trer i kraft. Hvis du vil gjøre endringene gjeldende umiddelbart, tilbakestiller du Microsoft Internet Information Services (IIS).

## <a name="completing-credit-memo-transactions-in-offline-mode"></a>Fullføring av kreditnotatransaksjoner i frakoblet modus

På samme måte som interne gavekort vedlikeholdes kreditnotaer sentralt i Commerce Headquarters. Commerce har en parameter som gjør at kreditnotatransaksjoner kan fullføres mens salgsstedet er frakoblet. Denne parameteren fungerer som gavekortparameteren som ble nevnt i forrige del. Når parameteren er aktivert, vil kreditnotatransaksjoner som fremtvinges frakoblet, synkroniseres tilbake til kanaldatabasen sammen med andre transaksjoner som ble utført mens salgsstedet var frakoblet.

Hvis du vil aktivere funksjonaliteten for å fullføre kreditnotatransaksjoner etter at du har byttet til frakoblet modus, kan du gå til kategorien **Postering** på siden **Parametere for Commerce**. I denne kategorien finner du hurtigfanen **Kreditnota**, og angi **Tillat avslutning av kreditnotatransaksjoner i frakoblet modus** til **Ja**.

![Frakoblet innstilling for kreditnota.](../media/creditmemo.png)

Commerce-parametere bufres vanligvis. Etter at innstillingen for denne parameteren er oppdatert og distribusjonsplanen startes for å synkronisere endringen til kanalen, kan det derfor ta opptil 24 timer før endringen trer i kraft. Hvis du vil gjøre endringene gjeldende umiddelbart, tilbakestiller du IIS.

## <a name="related-articles"></a>Relaterte artikler

- [Frakoblet salgsstedsfunksjonalitet](../pos-offline-functionality.md)
- [Tilkoblede og frakoblede salgsstedsoperasjoner (POS)](../pos-operations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
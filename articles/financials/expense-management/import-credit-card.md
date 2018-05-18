---
title: Importere og opprettholde kredittkorttransaksjoner
description: Dette emnet forklarer hvordan importere og vedlikeholde kostnadsrelaterte kredittkorttransaksjoner. Disse transaksjonene kan konfigureres slik at de importeres automatisk i en gjentatt tidsplan, eller de kan importeres manuelt etter behov.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e640c9e44add5599be4a2e381b4ffd81f212889c
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="import-and-maintain-credit-card-transactions"></a>Importere og opprettholde kredittkorttransaksjoner

[!include [banner](../includes/banner.md)]

Utgiftsrelaterte kredittkorttransaksjoner kan konfigureres slik at de automatisk importeres på en gjentatt tidsplan. Alternativt kan transaksjonene importeres manuelt etter behov. Kredittkorttransaksjonene blir importert via dataenheten Kredittkorttransaksjon.

Hvis du vil ha mer informasjon om datatyper, kan du se [Dataenheter](../../dev-itpro/data-entities/data-entities.md).

## <a name="import-credit-card-transactions"></a>Importer kredittkorttransaksjoner

1. På siden **kredittkorttransaksjoner**, velg **Importer transaksjoner**. Hvis du åpner databehandling for første gang, må systemet oppdatere listen over dataenheter før du kan fortsette.
2. Skriv inn en unik beskrivelse av importjobben i feltet **Navn**.
3. I feltet **Kildedataformat**, velg formatet for filen som inneholder kredittkorttransaksjonene som skal importeres.
4. Velg **Last opp** og finn og velg filen som skal importeres.
5. Etter at filen er lastet opp, valider tilordning av filen med kredittkorttransaksjonene og kolonnene for dataenhet for Kredittkorttransaksjoner ved å velge **Se kartlegging**-koblingen på flisen. Hvis det er tilordningsfeil, eller du må endre tilordningen, gjør tilordningsendringene fra enten kategorien **Mappevisualisering** eller kategorien **Mappedetaljer**.
6. For å automatisere kredittkorttransaksjoner, velg **Opprett gjentakende datajobb**. Du kan deretter angi gjentakelsen som definerer hvor ofte kredittkorttransaksjoner skal importeres. Når du er ferdig, velg **OK**.
7. For å importere den valgte filen nå, velg **Importer**.
8. Hvis det oppstår feil under importen, kan du se utførelsesloggen eller lagringsdata for å se feilene du må fikse for å garantere en vellykket import.

> [!NOTE]
> Hvis du må importere flere enn ett filformat, må du opprette separate importjobber for hver formattype.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Tilordne kredittkorttransaksjonene for ansatte som har sluttet

Etter at en ansatts oppføringer er terminert, vil den ansattes Active Directory Domain Services (AD DS)-konto deaktiveres. Det kan imidlertid være aktive kredittkorttransaksjoner som fortsatt må kostnadsføres og refunderes. Fra siden **Kredittkorttransaksjoner** kan du tilordne medarbeiderne for eventuelle kredittkorttransaksjoner for ansatte som har sluttet.

Velg én eller flere kredittkorttransaksjoner, og velg deretter **Tilordne transaksjoner**. Du kan velge en annen ansatt å tildele kredittkorttransaksjoner til. Etter at kredittkorttransaksjonene er tildelt kan de velges for en utgiftsrapport og betales gjennom de vanlige prosesser for refusjon av utgifter.


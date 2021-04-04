---
title: Innkjøps- og leverandørparametere for Netto innkjøpspris
description: Dette emnet beskriver hvordan du definerer de relevante innkjøps- og leverandørparameterne når du bruker modulen Netto innkjøpspris.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 49e046a1437917cfa866f690511789496fac2c53
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500748"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a>Innkjøps- og leverandørparametere for Netto innkjøpspris

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Siden **Innkjøps- og leverandørparametere** har et par innstillinger som er spesielt relevante når du bruker modulen **Netto innkjøpspris**. Bruk dialogboksen **Oppdater ordrelinjer** som åpnes fra siden **Innkjøps- og leverandørparametere** til å angi om bestillingslinjer automatisk skal oppdateres når det gjøres endringer i bestillingshodet.

Følg fremgangsmåten nedenfor for å fullføre dette oppsettet.

1. Gå til **Innkjøp og leverandører** \> Oppsett \> Parametere for innkjøp og leverandører.
1. Velg koblingen **Oppdater ordrelinjer** i fanen **Generelt**.
1. Dialogboksen **Oppdater ordrelinjer** viser feltene på ordrehodet, som også kan bruke automatiske oppdateringer for relaterte felt på ordrelinjene. Sett hvert felt i listen til en av følgende verdier:

    - **Alltid** – Ordrelinjene blir oppdatert automatisk når ordrehodet oppdateres.
    - **Aldri** – Ordrelinjene blir aldri oppdatert automatisk når ordrehodet oppdateres.
    - **Ledetekst** – Brukeren blir bedt om å velge om ordrelinjene skal oppdateres.

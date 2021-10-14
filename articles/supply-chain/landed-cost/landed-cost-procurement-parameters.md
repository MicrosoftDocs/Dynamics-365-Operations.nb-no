---
title: Innkjøps- og leverandørparametere for Netto innkjøpspris
description: Dette emnet beskriver hvordan du definerer de relevante innkjøps- og leverandørparameterne når du bruker modulen Netto innkjøpspris.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: cb41fc6477acb005912c735a691de6d1a659c020
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569847"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a>Innkjøps- og leverandørparametere for Netto innkjøpspris

[!include [banner](../../includes/banner.md)]

Siden **Innkjøps- og leverandørparametere** har et par innstillinger som er spesielt relevante når du bruker modulen **Netto innkjøpspris**. Bruk dialogboksen **Oppdater ordrelinjer** som åpnes fra siden **Innkjøps- og leverandørparametere** til å angi om bestillingslinjer automatisk skal oppdateres når det gjøres endringer i bestillingshodet.

Følg fremgangsmåten nedenfor for å fullføre dette oppsettet.

1. Gå til **Innkjøp og leverandører** \> Oppsett \> Parametere for innkjøp og leverandører.
1. Velg koblingen **Oppdater ordrelinjer** i fanen **Generelt**.
1. Dialogboksen **Oppdater ordrelinjer** viser feltene på ordrehodet, som også kan bruke automatiske oppdateringer for relaterte felt på ordrelinjene. Sett hvert felt i listen til en av følgende verdier:

    - **Alltid** – Ordrelinjene blir oppdatert automatisk når ordrehodet oppdateres.
    - **Aldri** – Ordrelinjene blir aldri oppdatert automatisk når ordrehodet oppdateres.
    - **Ledetekst** – Brukeren blir bedt om å velge om ordrelinjene skal oppdateres.

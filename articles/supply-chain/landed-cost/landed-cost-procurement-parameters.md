---
title: Innkjøps- og leverandørparametere for Netto innkjøpspris
description: Denne artikkelen beskriver hvordan du definerer de relevante innkjøps- og leverandørparameterne når du bruker modulen Netto innkjøpspris.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 92ce3e3d09bed15970375735f680b1b8348bbca8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905986"
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

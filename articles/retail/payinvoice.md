---
title: Definere scenarier for betaling av faktura
description: Dette emnet beskriver hvordan du konfigurerer Dynamics 365 for Retail til å støtte ulike scenarier for fakturabetalinger.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b7132dc9b3c78fa04fcfc38ea72b5678ad08deb2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564976"
---
# <a name="set-up-pay-invoice-scenarios"></a>Definere scenarier for betaling av faktura

[!include [banner](includes/banner.md)]

Funksjonen Betal faktura i Dynamics 365 for Retail er utvidet for å støtte:

- Betaling av flere salgsordrefakturaer i én salgsstedstransaksjon.
- Betaling for ulike typer kundefakturaer, inkludert fritekstfakturaer, prosjektbaserte fakturaer og kreditnotaer.

Hvis du vil aktivere disse scenariene, må funksjonsprofilen for butikker konfigureres som beskrevet nedenfor.

1. Gå til **Detaljhandel \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonsprofiler** og velg en profil som er knyttet til butikkene du vil gjøre endringene for.
2. Konfigurer følgende parametere etter behov, i kategorien **Funksjoner**.

    - **Salgsordrefaktura** – Velg **Ja** slik at brukere kan betale én eller flere salgsordrebaserte fakturaer i én salgsstedstransaksjon.
    - **Fritekstfaktura** – Velg **Ja** slik at brukere kan betale én eller flere fritekstbaserte fakturaer i én salgsstedstransaksjon.
    - **Prosjektfaktura** – Velg **Ja** slik at brukere kan betale én eller flere prosjektbaserte fakturaer i én salgsstedstransaksjon.
    - **Salgsordre – kreditnota** – Velg **Ja** slik at brukere kan utligne flere salgsordrebaserte kreditnotaer mot åpne fakturaer, eller betale pengene tilbake til kunden for en åpen kreditnota.

> [!NOTE]
> Betaling eller utligning delvise beløper støttes ikke ennå.

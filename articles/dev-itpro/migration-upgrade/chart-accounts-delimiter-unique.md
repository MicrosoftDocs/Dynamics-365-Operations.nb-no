---
title: "Gjøre skilletegn for kontoplan unik"
description: "Du kan ikke ha samme skilletegn for kontoplan og dimensjonsverdier i Dynamics 365 for Finance and Operations,. Du må endre skilletegnverdier etter oppgraderingen."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---

# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Gjøre skilletegn for kontoplan unik

[!include [banner](../includes/banner.md)]

Du kunne bruke samme skilletegn for kontoplanene og dimensjonsverdiene i Microsoft Dynamics AX 2012. Du kan ikke ha samme skilletegn for kontoplan og dimensjonsverdier i Dynamics 365 for Finance and Operations,. Hvis det finnes dupliserte skilletegn, kan du endre dem etter oppgraderingen. 

Denne funksjonen er tilgjengelig i:
- Dynamics 365 for Finance and Operations versjon 8.0
- Dynamics 365 for Finance and Operations versjon 7.1, KB 4094701 Kan ikke angi finansdimensjonene når dimensjonsverdiene inneholder skilletegn for kontoplan
- Dynamics 365 for Finance and Operations versjon 7.2, KB 4092967 Kan ikke velge underprosjektet som dimensjon når underprosjektformatet inneholder skilletegn for dimensjon

## <a name="update-delimiter"></a>Oppdatere skilletegn
Hvis det er en konflikt med kontoplanen, kan skilletegn for kontoplanen og formatet for prosjekt/underprosjekt-ID endres. Ingen andre dimensjonsskilletegn kan endres. 
- Du kan endre skilletegn for kontoplanen etter oppgradering til Finance and Operations i **Parametere for økonomimodul** > **Kontoplan og dimensjoner** > **Endre skilletegn**. 
- Hvis den eneste konflikten er med formatet for prosjekt/underprosjekt-ID, kan du endre verdien i **Parametere for prosjektstyring og regnskap** > **Generell** > **Endre format for delprosjekt**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Slik fastslår du om miljøet ditt krever oppdaterte skilletegn 
Hvis skilletegn i det oppgraderte miljøet er i konflikt, kan du oppleve ustabilitet når du angir verdier i en segmentert angivelseskontroll eller dimensjonsangivelseskontroll. Dette betyr at du alltid må bruke oppslag eller en undermeny når du angir kombinasjoner av konto og dimensjon.


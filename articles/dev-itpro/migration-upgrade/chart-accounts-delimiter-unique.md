---
title: "Skilletegn for kontoplan må være unik"
description: "Du kan ikke ha samme skilletegn for kontoplan og dimensjonsverdier i Dynamics 365 for Finance and Operations,. Du må endre skilletegnverdier etter oppgraderingen."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c9728714944b54f3bff1e2a8b43c7adcf5200f08
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="chart-of-accounts-delimiter-must-be-unique"></a>Skilletegn for kontoplan må være unik

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


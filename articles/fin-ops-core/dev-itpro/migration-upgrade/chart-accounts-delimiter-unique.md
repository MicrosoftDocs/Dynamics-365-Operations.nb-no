---
title: Gjøre skilletegnet for kontoplan unikt
description: Dette emnet beskriver hvordan du ikke kan ha samme skilletegn for kontoplanen og dimensjonsverdier. Du må endre skilletegnverdier etter oppgraderingen.
author: panolte
ms.date: 03/23/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 433e9f8a7b0a9f476c74096a4bd7fef03c87dee1
ms.sourcegitcommit: 0d5ee97670bdeb1986aaea880f32962b5e374751
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468056"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Gjøre skilletegnet for kontoplan unikt

[!include [banner](../includes/banner.md)]

Du kunne bruke samme skilletegn for kontoplanene og dimensjonsverdiene i Microsoft Dynamics AX 2012. Du kan ikke ha samme skilletegn for kontoplan og dimensjonsverdier i gjeldende versjon av Finance and Operations. Hvis det finnes dupliserte skilletegn, kan du endre dem etter oppgraderingen. 

## <a name="update-delimiter"></a>Oppdatere skilletegn
Hvis det er en konflikt med kontoplanen, kan skilletegn for kontoplanen og formatet for prosjekt/underprosjekt-ID endres. Ingen andre dimensjonsskilletegn kan endres. 
- Du kan endre skilletegn for kontoplanen etter oppgradering i **Parametere for økonomimodul** > **Kontoplan og dimensjoner** > **Endre skilletegn**. 
- Hvis den eneste konflikten er med formatet for prosjekt/underprosjekt-ID, kan du endre verdien i **Parametere for prosjektstyring og regnskap** > **Generell** > **Endre format for delprosjekt**. 

### <a name="other-considerations"></a>Andre hensyn
På samme måte som ID for prosjekt/underprosjekt bør ikke andre hoveddataposter som brukes som finansdimensjoner, for eksempel leverandører eller kunder, ha konto-ID-verdier som bruker samme tegn som kontoplanskilletegnet. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Slik fastslår du om miljøet ditt krever oppdaterte skilletegn 
Hvis skilletegn i det oppgraderte miljøet er i konflikt, kan du oppleve ustabilitet når du angir verdier i en segmentert angivelseskontroll eller dimensjonsangivelseskontroll. Dette betyr at du alltid må bruke oppslag eller en undermeny når du angir kombinasjoner av konto og dimensjon.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

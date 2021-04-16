---
title: Gjøre skilletegnet for kontoplan unikt
description: Dette emnet beskriver hvordan du ikke kan ha samme skilletegn for kontoplanen og dimensjonsverdier. Du må endre skilletegnverdier etter oppgraderingen.
author: panolte
ms.date: 03/30/2018
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
ms.openlocfilehash: f4f89772dedb5433c3da3f0f7bf02106641f59a8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748113"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Gjøre skilletegnet for kontoplan unikt

[!include [banner](../includes/banner.md)]

Du kunne bruke samme skilletegn for kontoplanene og dimensjonsverdiene i Microsoft Dynamics AX 2012. Du kan ikke ha samme skilletegn for kontoplan og dimensjonsverdier i gjeldende versjon av Finance and Operations. Hvis det finnes dupliserte skilletegn, kan du endre dem etter oppgraderingen. 

Denne funksjonen er ikke tilgjengelig i følgende versjoner:
- Finance and Operations versjon 8.0
- Finance and Operations versjon 7.1, KB 4094701 Kan ikke angi finansdimensjonene når dimensjonsverdiene inneholder skilletegn for kontoplan
- Finance and Operations versjon 7.2, KB 4092967 Kan ikke velge underprosjektet som dimensjon når underprosjektformatet inneholder skilletegn for dimensjon

## <a name="update-delimiter"></a>Oppdatere skilletegn
Hvis det er en konflikt med kontoplanen, kan skilletegn for kontoplanen og formatet for prosjekt/underprosjekt-ID endres. Ingen andre dimensjonsskilletegn kan endres. 
- Du kan endre skilletegn for kontoplanen etter oppgradering i **Parametere for økonomimodul** > **Kontoplan og dimensjoner** > **Endre skilletegn**. 
- Hvis den eneste konflikten er med formatet for prosjekt/underprosjekt-ID, kan du endre verdien i **Parametere for prosjektstyring og regnskap** > **Generell** > **Endre format for delprosjekt**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Slik fastslår du om miljøet ditt krever oppdaterte skilletegn 
Hvis skilletegn i det oppgraderte miljøet er i konflikt, kan du oppleve ustabilitet når du angir verdier i en segmentert angivelseskontroll eller dimensjonsangivelseskontroll. Dette betyr at du alltid må bruke oppslag eller en undermeny når du angir kombinasjoner av konto og dimensjon.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
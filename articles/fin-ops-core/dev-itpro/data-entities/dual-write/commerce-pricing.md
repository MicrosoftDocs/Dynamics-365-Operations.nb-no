---
title: Bruke prissettingsmotoren i Dynamics 365 Commerce med Dynamics 365 Sales
description: Dette emnet beskriver hvordan du bruker prissettingsmotoren i Microsoft Dynamics 365 Commerce til å opprette salgstilbud i Dynamics 365 Sales.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fa93b1262049d80148ff23b3d7223ec0f6c2fe68
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941172"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Bruke prissettingsmotoren i Dynamics 365 Commerce med Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du bruker prissettingsmotoren i Microsoft Dynamics 365 Commerce til å opprette salgstilbud i Dynamics 365 Sales.

Prissettingsmotoren i Dynamics 365 Commerce støtter de fleste prisscenarioene for bedrift-til-kunde (B2C), for eksempel priser på butikknivå, tilknytningsbasert og lojalitetsbasert prissetting, samlerabatter, kvantumsrabatter og terskelrabatter. Prissettingsmotoren bruker komplekse regler til å bestemme den beste prisen for et gitt tilbud eller ordre.

Når du bruker [dobbel skriving](./dual-write-overview.md), har du tre alternativer for prissettingsbehovene dine. Du kan bruke den statiske prissettingen som kommer fra prislisten i Dynamics 365 Sales, prissettingsmotoren i Dynamics 365 Supply Chain Management eller prissettingsmotoren i Dynamics 365 Commerce. Blant disse alternativene er prissettingsmotoren i Commerce best egnet i B2C-scenarioer.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>Bruk prissettingsmotoren i Commerce i Sales

> [!NOTE]
> For øyeblikket kan prissettingsmotoren i Commerce bare brukes til opprettelse av tilbud i Sales. Salgsordreintegrering med prissettingsmotoren i Commerce er ikke tilgjengelig ennå.

Når brukere starter et tilbud i Sales, kopierer rammeverket for dobbel skriving tilbudsdetaljene til Commerce. Endringer i eksisterende tilbudslinjer eller tilbudslinjer som nylig er lagt til i Sales, kopieres til Commerce. Når brukere vil bruke prissettingsmotoren i Commerce til å gi tilbudet en pris, kan de velge **Pristilbud** for å oppdatere prisene i tilbudet, basert på prissettingsmotoren i Commerce. Priser oppdateres deretter automatisk i både Sales og Commerce.

## <a name="prerequisites"></a>Forutsetninger

- Før du kan bruke prissettingsmotoren i Commerce i Sales, må du følge fremgangsmåten i [Kundeemne til kontanter i dobbel skriving](./dual-write-prospect-to-cash.md).
- Du må deaktivere evaluering av forretningsavtale for manuell registrering ved å følge disse trinnene:

    1. Gå til **Kunder \> Oppsett \> Kundeparametere** i Commerce-miljøet ditt.
    1. Fjern merket for **Manuell registrering** i hurtigfanen **Evaluering av handelsavtale** i **Priser**-fanen.

## <a name="additional-resources"></a>Tilleggsressurser

[Kundeemne til kontanter i dobbel skriving](./dual-write-prospect-to-cash.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
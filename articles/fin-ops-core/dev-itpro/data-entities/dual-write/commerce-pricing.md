---
title: Bruke prissettingsmotoren i Dynamics 365 Commerce med Dynamics 365 Sales
description: Denne artikkelen beskriver hvordan du bruker prissettingsmotoren i Microsoft Dynamics 365 Commerce til å opprette salgstilbud i Dynamics 365 Sales.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 11a164ec15c8b7a69172a153b961011a8b324712
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881401"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Bruke prissettingsmotoren i Dynamics 365 Commerce med Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

Denne artikkelen beskriver hvordan du bruker prissettingsmotoren i Microsoft Dynamics 365 Commerce til å opprette salgstilbud i Dynamics 365 Sales.

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
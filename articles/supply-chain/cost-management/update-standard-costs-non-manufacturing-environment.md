---
title: Oppdatere standardkostnader i et ikke-produksjonsmiljø
description: Denne artikkelen gir råd for å oppdatere standardkostnader i et ikke-produksjonsmiljø.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09dca3012952b739a75a6930908752fba73a4550
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434356"
---
# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a>Oppdatere standardkostnader i et ikke-produksjonsmiljø

[!include [banner](../includes/banner.md)]

Denne artikkelen gir råd for å oppdatere standardkostnader i et ikke-produksjonsmiljø.

Retningslinjene antar at du bruker en toversjons tilnærming til å oppdatere standardkostnad. I denne fremgangsmåten, inneholder én etterkalkuleringsversjon standardkostnader som opprinnelig ble definert for den frosne perioden, og den andre etterkalkuleringsversjonen inneholder de inkrementelle oppdateringene. Hver oppdatering angis som en kostnadspost som er vedlagt i den andre etterkalkuleringsversjonen, og til slutt den er aktivert. En alternativ fremgangsmåte med én versjon bruker settet med standardkostnader som opprinnelig var definert. Toversjonsmåten krever at du definerer enda en etterkalkuleringsversjon. Her følger retningslinjene for å definere denne etterkalkuleringsversjonen:

-   Tilordne en etterkalkuleringstype for **standardkostnader**.
-   Tilordne en meningsfull identifikator som identifiserer innholdet i etterkalkuleringsversjonen, for eksempel **2016-OPPDATERINGER**.
-   Kontroller at innholdet omfatter kostprisposter.
-   Tillat innlegging av kostnadsposter for alle områder. Hvis du angir et område, kan kostnadsposter angis bare for dette området.
-   Angi tilbakefallsprinsippet **Ingen**. Tilbakefallsprinsippet gjelder bare kostnadsberegninger for produserte varer.

Hvis du skal rette, justere eller oppdatere standardkostnader for mye varer, gjør du følgende.

1.  Bruk **Etterkalkuleringsversjon**-**oppsett** siden for å aktivere kostnadsdata som skal angis i den andre etterkalkuleringsversjonen. Alternativt kan du forhindre aktiveringen av uavsluttede kostpriser, slik at aktiveringen vil bli tillatt etter at de uavsluttede kostprisene er fullført og korrekt definert. Du kan også angi en dato i **Fra dato**-feltet. Som en generell retningslinje kan du bruke datoen når du planlegger å aktivere de inkrementelle oppdateringene. Du kan også la **Fra dato**-feltet være tomt for etterkalkuleringsversjonen og angi en dato i **Fra dato**-feltet for hver kostnadsoppføring.
2.  Bruk **Varepris**-siden for å angi oppdateringer som varekostnadsposter som er vedlagt i den andre etterkalkuleringsversjonen.
3.  Bruk **Varepriser**-rapporten for å bekrefte at varekostnadspostene som er vedlagt den andre etterkalkuleringsversjonen, er fullført og nøyaktige.
4.  Bruk siden **Vedlikehold av etterkalkuleringsversjon** for å endre blokkeringsflagget for å tillate aktivering av ventende kostnadsposter som er vedlagt den andre etterkalkuleringsversjonen.
5.  Bruk siden **Aktiver priser** (som du åpner fra siden **Vedlikehold av etterkalkuleringsversjon**) for å aktivere alle ventende varekostnadsposter som er vedlagt den andre etterkalkuleringsversjonen. Du kan også aktivere de ventende kostnadspostene for enkelte varer ved å klikke knappen **Aktiver ventende pris** på **Varepris**-siden.
6.  For å unngå ytterligere datavedlikehold kan du bruke siden **Oppsett av etterkalkuleringsversjon** til å endre blokkeringsflaggene som er vedlagt den andre etterkalkuleringsversjonen. Blokkeringspolicyene forhindrer innlegging av nye uavsluttede kostnader og aktivering av uavsluttede kostpriser.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
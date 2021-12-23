---
title: Konvertere asynkron-kunder til synkron-kunder
description: Dette emnet beskriver hvordan du konverterer asynkron-kunder til synkron-kunder i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: d8a386299f2c67c870fe0b8f779c9155405c1f1a
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913804"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Konvertere asynkron-kunder til synkron-kunder

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du konverterer asynkron-kunder til synkron-kunder i Microsoft Dynamics 365 Commerce.

Følg disse trinnene for å konvertere asynkron-kunder til synkron-kunder.

1. I Commerce Headquarters kjører du **P-jobb** for å sende asynkron-kunder til Commerce Headquarters.
1. Kjør jobben **Synkroniser kunder og forretningspartnere fra asynkron modus** for å opprette kundekonto-ID-er. (Denne jobben ble tidligere kalt **Synkroniser kunder og forretningspartnere fra asynkron modus**.)
1. Kjør jobben **1010** for å synkronisere de nye kundekonto-ID-ene til kanalene.

Hvis en ordre refererer til en asynkron-kunde eller -adresse som ennå ikke er synkronisert i Commerce Headquarters, synkroniseres kunden eller adressen som en del av den satsvise jobben **Synkroniser ordrer**. Hvis en hentesalgstransaksjon refererer til en asynkron-kunde eller -adresse, synkroniseres kunden eller adressen før EOD-postering (slutten av dagen).

## <a name="additional-resources"></a>Tilleggsressurser

[Kundebehandling i butikker](customer-mgmt-stores.md)

[Asynkron kundeopprettingsmodus](async-customer-mode.md)

[Kundeattributter](dev-itpro/customer-attributes.md)

[Utelatelse av frakoblede data](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)

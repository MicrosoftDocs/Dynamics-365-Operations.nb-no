---
title: Konvertere asynkron-kunder til synkron-kunder
description: Denne artikkelen beskriver hvordan du konverterer asynkron-kunder til synkron-kunder i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 0ce4906816deab8824b1079a34489e55651c0e03
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884397"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Konvertere asynkron-kunder til synkron-kunder

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du konverterer asynkron-kunder til synkron-kunder i Microsoft Dynamics 365 Commerce.

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

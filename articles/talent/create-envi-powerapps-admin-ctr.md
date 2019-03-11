---
title: Kan ikke opprette et miljø i PowerApps-administrasjonssenteret
description: Dette emnet forklarer hva du gjør hvis administratoren ikke kan opprette et miljø i Microsoft PowerApps-administrasjonssenteret.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "305687"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a>Kan ikke opprette et miljø i PowerApps-administrasjonssenteret

[!include [banner](includes/banner.md)]

**Utstede**

- Leier-/miljøadministratoren kan ikke opprette et miljø i Microsoft PowerApps-administrasjonssenteret.
- En lisens som gir brukerne rett til å utføre miljøopprettingstrinnet, er ikke tilordnet direkte til brukeren som utfører dette trinnet.

**Løsning**

Kontroller at leieradministratoren har tilordnet en gyldig lisens for PowerApps P2 direkte til brukeren som utfører miljøopprettingstrinnet. Her er Microsoft Dynamics-serviceplanene som gir denne rettigheten.

| Generell produktlagerenhet (SKU)       | PowerApps P2-serviceplan  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | PowerApps for Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | PowerApps for Dynamics 365 |

Legg merke til at ulike Microsoft Office-SKUer også gir rettighet, sammen med frittstående PowerApps Plan 2-SKUer. Det viktige er at én av disse SKU-ene er nødvendig.

1. Gå til [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Opprett miljøene ved å følge instruksjonene i [Klargjøre Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

---
title: Kan ikke opprette et miljø i administrasjonssenteret for Power Apps
description: Dette emnet forklarer hva du gjør hvis administratoren ikke kan opprette et miljø i Microsoft Power Apps-administrasjonssenteret.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7a66b7624655aaf976aaa63b2626f65c54d0ea38
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898826"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Kan ikke opprette et miljø i administrasjonssenteret for Power Apps

**Avgang**

- Leier-/miljøadministratoren kan ikke opprette et miljø i Microsoft Power Apps-administrasjonssenteret.
- En lisens som gir brukerne rett til å utføre miljøopprettingstrinnet, er ikke tilordnet direkte til brukeren som utfører dette trinnet.

**Løsning**

Kontroller at leieradministratoren har tilordnet en gyldig lisens for Power Apps P2 direkte til brukeren som utfører miljøopprettingstrinnet. Her er Microsoft Dynamics-serviceplanene som gir denne rettigheten.

| Generell produktlagerenhet (SKU)       | Power Apps P2-serviceplan  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps for Dynamics 365 |

Legg merke til at ulike Microsoft Office-SKUer også gir rettighet, sammen med frittstående Power Apps Plan 2-SKUer. Det viktige er at én av disse SKU-ene er nødvendig.

1. Gå til [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Opprett miljøene ved å følge instruksjonene i [Klargjøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

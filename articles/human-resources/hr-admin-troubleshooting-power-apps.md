---
title: Kan ikke opprette et miljø i administrasjonssenteret for Power Apps
description: Denne artikkelen forklarer hva du gjør hvis administratoren ikke kan opprette et miljø i Microsoft Power Apps-administrasjonssenteret.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 26a228229a09e74809a048675a3ff90025f2a26c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892233"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Kan ikke opprette et miljø i administrasjonssenteret for Power Apps

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Avgang**

- Leier-/miljøadministratoren kan ikke opprette et miljø i Microsoft Power Apps-administrasjonssenteret.
- Brukeren har ikke en lisens som gir rett til å opprette miljøer.

**Løsning**

Kontroller at leietakeradministratoren har tilordnet en gyldig Power Apps P2-lisens til brukeren som oppretter miljøet. Følgende Microsoft Dynamics-serviceplaner gir tillatelser til å opprette miljøer:

| Generell produktlagerenhet (SKU)       | Power Apps P2-serviceplan  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps for Dynamics 365 |

Legg merke til at ulike Microsoft Office-SKUer også gir rettighet, sammen med frittstående Power Apps Plan 2-SKUer. Det viktige er at én av disse SKU-ene er nødvendig.

1. Gå til [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Opprett miljøene ved å følge instruksjonene i [Klargjøre Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
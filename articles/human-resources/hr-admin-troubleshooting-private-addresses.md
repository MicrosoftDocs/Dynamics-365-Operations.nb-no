---
title: Tilgang til private adresser etter sikkerhetsrolle
description: Dette emnet forklarer hva du gjør hvis en kunde ikke får tilgang til private adresser.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 213aada51a477257df0b079c95e74610854b5a4f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689585"
---
# <a name="access-to-private-addresses-by-security-role"></a>Tilgang til private adresser etter sikkerhetsrolle


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Utstede**

Når en kunde dupliserer en sikkerhetsrolle og logger på som den nye rollen, kan ikke kunden se adresser som er merket som private.

**Oppløsning**

For å løse problemet må kunden følge denne fremgangsmåten for den dupliserte sikkerhetsrollen.

1. Gå til **Organisasjonsstyring \> Global adressebok \> Parametere for global adressebok**.
2. På fanen **Sikkerhet for privat lokasjon** flytter du den nye sikkerhetsrollen fra listen **Tilgjengelige roller** til listen **Valgte roller**.
3. Velg **Lagre**.

![Siden for parametere for global adressebok.](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

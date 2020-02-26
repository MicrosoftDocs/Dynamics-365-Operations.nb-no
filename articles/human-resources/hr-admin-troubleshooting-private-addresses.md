---
title: Tilgang til private adresser etter sikkerhetsrolle
description: Denne artikkelen forklarer hvordan du løser problemet der en kunde ikke får tilgang til private adresser.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: facfd17f007b2c9e6f068d0ec4c5ce45b85a1b78
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010094"
---
# <a name="access-to-private-addresses-by-security-role"></a>Tilgang til private adresser etter sikkerhetsrolle

**Utstede**

Når en kunde dupliserer en sikkerhetsrolle og logger på som den nye rollen, kan ikke kunden se adresser som er merket som private.

**Oppløsning**

For å løse problemet må kunden følge denne fremgangsmåten for den dupliserte sikkerhetsrollen.

1. Gå til **Organisasjonsstyring \> Global adressebok \> Parametere for global adressebok**.
2. På fanen **Sikkerhet for privat lokasjon** flytter du den nye sikkerhetsrollen fra listen **Tilgjengelige roller** til listen **Valgte roller**.
3. Velg **Lagre**.

![Siden for parametere for global adressebok](media/GAD-parameters.png)

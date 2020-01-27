---
title: Tilgang til private adresser etter sikkerhetsrolle
description: Dette emnet forklarer hvordan du løser problemet der en kunde ikke får tilgang til private adresser.
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
ms.openlocfilehash: 58f3322ad64f7de07e17d193ff665bd6536a4070
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897103"
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

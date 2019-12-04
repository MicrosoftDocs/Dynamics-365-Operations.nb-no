---
title: Brukeren har tilgang til Core HR, men ikke Onboard eller Attract
description: Dette emnet forklarer hvordan du løser problemet der en bruker får tilgang til Microsoft Dynamics 365 Talent – Core HR, men får tilgang til Attract eller Onboard.
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
ms.openlocfilehash: 1a86936d756d8375761ce50c9d9bf33dc638dfad
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772925"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a>Brukeren har tilgang til Core HR, men ikke Onboard eller Attract

[!include [banner](includes/banner.md)]

**Miljødetaljer**

- Microsoft Dynamics Lifecycle Services-distribusjonen (LCS) ble utført av bruker A.
- Bruker A la til bruker B som bruker i Microsoft Dynamics 365 Talent: Core HR.

**Avgang**

Bruker B har tilgang til Core HR, men har ikke tilgang til appene Talent: Attract eller Talent: Onboard. Når brukeren prøver å gå til **Opplev-appene**, kommer han eller hun til et prøvemiljø i stedet.

**Løsning**

Bruker B må tilordnes rettigheter til å vise Microsoft Power Apps-miljøet som bruker A opprettet under klargjøringsprosessen.

Hvis du vil ha informasjon, kan du se delen "Gi tilgang til utviklingsmiljøet" i [Klargjøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Langsiktig løsning**

Microsoft vurderer å tilordne de nødvendige rettighetene til Onboard og Attract automatisk når en bruker legges til i Core HR.

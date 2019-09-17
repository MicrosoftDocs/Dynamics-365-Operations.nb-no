---
title: Brukeren har tilgang til Core HR, men ikke appen Onboard eller Attract
description: Dette emnet forklarer hvordan du løser problemet der en bruker får tilgang til Microsoft Dynamics 365 for Talent Core HR, men får tilgang til appen Attract eller Onboard.
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
ms.openlocfilehash: 6fc27a4c137fef2f8d204d90366c316389da08e6
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741730"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>Brukeren har tilgang til Core HR, men ikke appen Onboard eller Attract

[!include [banner](includes/banner.md)]

**Miljødetaljer**

- Microsoft Dynamics Lifecycle Services-distribusjonen (LCS) ble utført av bruker A.
- Bruker A la til bruker B som bruker i Microsoft Dynamics 365 for Talent Core HR.

**Avgang**

Bruker B har tilgang til Core HR, men har ikke tilgang til appene Talent: Attract eller Talent: Onboard. Når brukeren prøver å gå til **Opplev-appene**, kommer han eller hun til et prøvemiljø i stedet.

**Løsning**

Bruker B må tilordnes rettigheter til å vise Microsoft PowerApps-miljøet som bruker A opprettet under klargjøringsprosessen.

Hvis du vil ha informasjon, kan du se delen "Gi tilgang til utviklingsmiljøet" i [Klargjøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Langsiktig løsning**

Microsoft vurderer å tilordne de nødvendige rettighetene til Onboard og Attract automatisk når en bruker legges til i Core HR.

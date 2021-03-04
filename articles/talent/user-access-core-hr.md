---
title: Brukeren har tilgang til Human Resources, men ikke Onboard eller Attract
description: Dette emnet forklarer hvordan du løser problemet der en bruker får tilgang til Microsoft Dynamics 365 Talent – Human Resources, men ikke får tilgang til Attract eller Onboard.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462097"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a>Brukeren har tilgang til Human Resources, men ikke Onboard eller Attract

[!include [banner](includes/banner.md)]

**Miljødetaljer**

- Microsoft Dynamics Lifecycle Services-distribusjonen (LCS) ble utført av bruker A.
- Bruker A la til bruker B som bruker i Microsoft Dynamics 365 Human Resources.

**Avgang**

Bruker B har tilgang til Human Resources, men har ikke tilgang til appene Talent: Attract eller Talent: Onboard. Når brukeren prøver å gå til **Opplev-appene**, kommer han eller hun til et prøvemiljø i stedet.

**Løsning**

Bruker B må tilordnes rettigheter til å vise Microsoft Power Apps-miljøet som bruker A opprettet under klargjøringsprosessen.

Hvis du vil ha informasjon, kan du se delen "Gi tilgang til utviklingsmiljøet" i [Klargjøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Langsiktig løsning**

Microsoft vurderer å tilordne de nødvendige rettighetene til Onboard og Attract automatisk når en bruker legges til i Human Resources.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
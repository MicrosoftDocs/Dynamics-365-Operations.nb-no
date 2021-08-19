---
title: Statuser for transportstyring
description: Dette emnet forklarer hvordan du oppretter en transportstatus og tilordner statusen til en transportørstatus.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 5a2b114be69d5e2e26f1fc7e82a4332f343adbaa71d7b7cf8c6df8ce09b08642
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753186"
---
# <a name="transportation-management-statuses"></a>Statuser for transportstyring

[!include [banner](../includes/banner.md)]

Definer primærkoder for transportstatuser for å tolke koder som leveres av transportørene. Dermed kan du integrere med transportører for å angi en status. Transportstatusen du angir for en primær kode for transportstatus, kan hjelpe deg med å spore status for en last, forsendelse eller container. Den bestemte transportstatusen for last, forsendelse eller container kan bare oppdateres gjennom dataintegrering, og ikke manuelt via brukergrensesnittet.

## <a name="create-a-transportation-status"></a>Opprette en transportstatus

Hvis du vil opprette en transportstatus, gjør du følgende:

1. Gå til **Transportstyring \> Oppsett \> Transportstatusmal**.
1. Velg **Ny** for å opprette en transportstatusmal.
1. I **Transportstatusmal**-feltet angir du inn en unik kode for transportstatusen.
1. I **Transporttype**-feltet velger du enten *Transportør* eller *Hub* som transporttype.
1. Angi et navn og en transportstatus.
1. Lukk siden.

## <a name="map-a-transportation-status-to-a-carrier-status"></a>Tilordne en transportstatus til en transportørstatus

Følg denne fremgangsmåten for å tilordne en transportstatus til en transportørstatus:

1. Gå til **Transportstyring \> Oppsett \> Transportører \> Transportstatus for transportør**.
1. Velg **Ny** for å tilordne en kode fra en transportør til en primær kode for transportstatus.
1. Velg den unike ID-en for transportøren og transportørtjenesten.
1. Velg transportstatuskoden som du vil tilordne til den valgte transportørkoden.
1. Angi den eksterne koden transportøren bruker.
1. Lukk siden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
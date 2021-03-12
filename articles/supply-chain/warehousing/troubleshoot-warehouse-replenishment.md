---
title: Feilsøke lageretterfylling
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lageretterfylling i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7748a18d2b6f612b3ac9ac1a75efb6ae5f13859a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993897"
---
# <a name="troubleshoot-warehouse-replenishment"></a>Feilsøke lageretterfylling

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lageretterfylling i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>Jeg får følgende feilmelding: Blokkeringen av arbeid %1 kan ikke oppheves, fordi den har ikke-fullført etterfyllingsarbeid.

### <a name="issue-description"></a>Problembeskrivelse

Plukkarbeid er blokkert på grunn av avhengig etterfyllingsarbeid.

### <a name="issue-resolution"></a>Problemløsning

Når du bruker etterfylling av bølgebehov, hvis en plukklokasjon må etterfylles for å opofylle kildeordrebehovet, vil systemet opprette både etter fyllingsarbeidet og plukkarbeidet. Det blokkerer imidlertid plukkarbeidet til etterfyllingsarbeidet er fullført. Denne virkemåten er med hensikt, fordi plukklokasjonen ikke har nok lager hvis ikke etterfyllingsarbeidet er fullført. Fullfør etterfyllingsarbeidet, og behandle deretter plukkarbeidet.

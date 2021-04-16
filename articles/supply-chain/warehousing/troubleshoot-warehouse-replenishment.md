---
title: Feilsøke lageretterfylling
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lageretterfylling i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8940f729e1115405e8d6e50eccc92d9fffe37f3e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828088"
---
# <a name="troubleshoot-warehouse-replenishment"></a>Feilsøke lageretterfylling

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lageretterfylling i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>Jeg får følgende feilmelding: Blokkeringen av arbeid %1 kan ikke oppheves, fordi den har ikke-fullført etterfyllingsarbeid.

### <a name="issue-description"></a>Problembeskrivelse

Plukkarbeid er blokkert på grunn av avhengig etterfyllingsarbeid.

### <a name="issue-resolution"></a>Problemløsning

Når du bruker etterfylling av bølgebehov, hvis en plukklokasjon må etterfylles for å opofylle kildeordrebehovet, vil systemet opprette både etter fyllingsarbeidet og plukkarbeidet. Det blokkerer imidlertid plukkarbeidet til etterfyllingsarbeidet er fullført. Denne virkemåten er med hensikt, fordi plukklokasjonen ikke har nok lager hvis ikke etterfyllingsarbeidet er fullført. Fullfør etterfyllingsarbeidet, og behandle deretter plukkarbeidet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
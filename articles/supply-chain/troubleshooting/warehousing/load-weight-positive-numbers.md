---
title: Belastningsvekt kan bare inneholde positive tall
description: Når du behandler arbeid mellom lokasjoner, kan du få en feilmelding om belastningsvekten og oppdateringen som blir annullert. Følg fremgangsmåten nedenfor for å løse problemet.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8ea1f6679a521e3e8683b8e5f18f509e98044414
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477188"
---
# <a name="load-weight-error-and-update-canceled-when-processing-work-between-locations"></a>Belastningsfeil og oppdater ble avbrutt under behandling av arbeid mellom lokasjoner

## <a name="symptoms"></a>Symptomer

Du får denne feilmeldingen hvis det er åpent arbeid når du behandler arbeid fra emballasjelokasjoner til oppsamlingslokasjoner, eller fra oppsamlingslokasjoner til forankringslokasjoner.

> Feltet "Lastvekt" (=-%1) kan bare inneholde positive tall. Oppdateringen er avbrutt.

## <a name="resolution"></a>Løsning

Hvis du vil løse dette problemet, går du til **Systemadministrasjon \> Periodiske oppgaver \> Database \> Konsekvenskontroll** og kjører prosessen for **Konsekvenskontroll av lagerlastvekt**.

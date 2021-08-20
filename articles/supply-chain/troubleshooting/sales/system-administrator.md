---
title: Systemadministratorer kan ikke fjerne bestillinger fordi de ikke har autorisasjon til dette
description: Systemadministratorer kan ikke fjerne bestillinger fordi de ikke har autorisasjon til dette.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0d0fbcc111d77ae1a362984033216f5973e2bc74f2ee95947b662ef60a13d83e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750912"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a>Systemadministratorer kan ikke fjerne bestillinger fordi de ikke har autorisasjon til dette

KB-nummer: 4614642

## <a name="symptoms"></a>Symptomer

Systemansvarlige kan ikke fjerne salgsordrer med mindre de har den bestemte rollen som er tilordnet i ordresperrekoden.

## <a name="resolution"></a>Oppløsning

Tilgang til enkelte operasjoner, for eksempel å fjerne salgsordrer, drives av oppsettet av en forretningspolicy. Systemadministratorer har vanligvis ikke tillatelse til å utføre operasjoner av denne typen. 

Oftere styres tilgangen til å utføre en bestemt oppgave av forretningspolicyer, og bare bestemte personer i en organisasjon godkjennes for å utføre denne oppgaven. Eksempler inkluderer godkjenninger som er resultatet av arbeidsflytgodkjenning og bestemte oppgaver som er resultatet av en arbeidsflytkonfigurasjon.

Selv om ingen arbeidsflyt er knyttet til ordresperrer, er prinsippet likt. En relevant rolle angir den bestemte gruppen av personer i en organisasjon som har rettighet til å fjerne ordresperringer. Denne rettigheten bør ikke nødvendigvis gis til alle administratorer, fordi denne tilnærmingen bryter den definerte forretningspolicyen.

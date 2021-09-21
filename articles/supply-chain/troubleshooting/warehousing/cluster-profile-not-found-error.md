---
title: Klyngeprofil blir ikke funnet
description: Når du arbeider med innkommende lageroperasjoner, kan du få en feilmelding som sier at klyngeprofilen ikke kan bli funnet. Kontroller at klyngeprofiler er satt opp riktig.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bbf9c5bc70c8f3ba1fa26db425249e65e82c0518
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477244"
---
# <a name="cluster-profile-cant-be-found"></a>Finner ikke gruppeprofil

## <a name="symptoms"></a>Symptomer

Du kan få følgende feilmelding når du arbeider med innkommende lageroperasjoner:

> "Kvalitetsordre %1 er generert. Finner ikke gruppeprofil. Kontroller konfigurasjonen."

Denne feilmeldingen er knyttet til en mottaksprosess der kvalitetsstyring (QMS) er aktivert. Avhengig av konfigurasjonene i miljøet ditt kan flere detaljer om transaksjonen som genererer feilmeldingen, hjelpe deg med å løse problemet.

## <a name="resolution"></a>Løsning

Først kontrollerer du konfigurasjonen for gruppeplukking og kontrollerer at gruppeprofilene er riktig konfigurert. Du kan ikke bruke et menyelement på mobilenheten for gruppeplukking med mindre gruppeprofiler er konfigurert. Avhengig av miljøet kan det være at du også må se gjennom andre tilknyttede konfigurasjoner.

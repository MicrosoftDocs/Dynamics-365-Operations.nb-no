---
title: Opprette en arbeidsklasse
description: Denne fremgangsmåten viser hvordan du setter opp en arbeidsklasse.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc0eb4c0a6397164d068b5dd44a0807dfdf65814
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979605"
---
# <a name="create-a-work-class"></a>Opprette en arbeidsklasse

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du setter opp en arbeidsklasse. Arbeidsklasser brukes til å styre og/eller begrense typen arbeidsordrelinjer som en lagermedarbeider kan behandle på en mobil enhet. Linjene som en arbeider kan behandle, bestemmes fra arbeidsklassene på menyelementene for mobilenhet som Lagermedarbeideren har tilgang til og arbeidsklassen som er angitt på arbeidslinjene. Arbeidsklasser kan også brukes til å validere plasseringslokasjon for en arbeidsordrelinje. Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Denne fremgangsmåten er ment for lagersjef.

1. Gå til Lagerstyring > Oppsett > Arbeid > Arbeidsklasser.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Arbeidsklasse-ID.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Velg et alternativ i feltet Arbeidsordretype.
6. Klikk Ny.
7. Skriv inn en verdi i feltet Lokasjonstype.
    * Hvis du velger en lokasjonstype, angir dette en begrensning på hvor varene kan plasseres når de har blitt plukket. Denne innstillingen brukes når et lokasjonsdirektiv forsøker å løse lokasjonen, eller hvis lagermedarbeider angir lokasjonen for menyelementet for mobil enhet manuelt.  
8. Lukk siden.


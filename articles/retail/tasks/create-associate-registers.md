---
title: " Opprette og tilknytte kasser"
description: Denne fremgangsmåten beskriver hvordan du oppretter en kasse for et salgssted (POS).
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07e4b9f32a3a74b273272bd0b759d35c2a963e2e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "360653"
---
# <a name="create-and-associate-registers"></a> Opprette og tilknytte kasser

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne fremgangsmåten beskriver hvordan du oppretter en kasse for et salgssted (POS). Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.

1. Gå til Detaljhandel og handel > Kanaloppsett > Salgsstedsoppsett > Kasser.
2. Klikk Ny.
3. I Kassenummer-feltet skriver du inn en ID for den nye kassen.
    * Kasse-ID-en inneholder vanligvis koder som bidrar til å tilordne kassen til butikken den tilhører, og plasseringen i butikken.  
4. I Navn-feltet skriver du inn et beskrivende navn på kassen.
5. Angi eller velg en verdi i Butikknummer-feltet.
6. Angi eller velg en verdi i Maskinvareprofil-feltet.
    * Maskinvareprofiler brukes til å angi eksterne detaljhandelsenheter som skal kobles til kassen, for eksempel kassaskuffen og kvitteringsskriveren.  
7. Angi eller velg en verdi i Visuell profil-feltet.
    * Visuelle profiler brukes til å angi bildene som brukes på bakgrunnen og påloggingssiden for salgsstedet, samt oppsett for salgsstedet.  
8. Skriv inn en verdi i feltet EFT-registreringsnummer for POS.
    * EFT-registreringsnummeret for POS brukes til å informere betalingprosessoren om hvilken betalingsterminal som sender forespørsler om godkjenning. Denne verdien kalles ofte Terminal-ID eller TID. TID finnes vanligvis på et klistremerke på betalingsenheten.  
9. Klikk Lagre.


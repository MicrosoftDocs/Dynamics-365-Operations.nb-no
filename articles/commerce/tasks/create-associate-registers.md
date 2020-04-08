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
ms.openlocfilehash: 001bdd61f9266798dadae2ac7c96a4f4c19dbb94
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141459"
---
# <a name="create-and-associate-registers"></a> Opprette og tilknytte kasser

[!include [banner](../includes/banner.md)]

Denne fremgangsmåten beskriver hvordan du oppretter en kasse for et salgssted (POS). Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.

1. Gå til Detaljhandel og handel > Kanaloppsett > Salgsstedsoppsett > Kasser.
2. Klikk Ny.
3. I Kassenummer-feltet skriver du inn en ID for den nye kassen.
    * Kasse-ID-en inneholder vanligvis koder som bidrar til å tilordne kassen til butikken den tilhører, og plasseringen i butikken.  
4. I Navn-feltet skriver du inn et beskrivende navn på kassen.
5. Angi eller velg en verdi i Butikknummer-feltet.
6. Angi eller velg en verdi i Maskinvareprofil-feltet.
    * Maskinvareprofiler brukes til å angi eksterne enheter som skal kobles til kassen, for eksempel kassaskuffen og kvitteringsskriveren.  
7. Angi eller velg en verdi i Visuell profil-feltet.
    * Visuelle profiler brukes til å angi bildene som brukes på bakgrunnen og påloggingssiden for salgsstedet, samt oppsett for salgsstedet.  
8. Skriv inn en verdi i feltet EFT-registreringsnummer for POS.
    * EFT-registreringsnummeret for POS brukes til å informere betalingprosessoren om hvilken betalingsterminal som sender forespørsler om godkjenning. Denne verdien kalles ofte Terminal-ID eller TID. TID finnes vanligvis på et klistremerke på betalingsenheten.  
9. Klikk Lagre.


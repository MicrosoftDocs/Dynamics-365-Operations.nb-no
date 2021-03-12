---
title: Konfigurere og kjøre jobben for å postere utdrag
description: Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å postere utdrag for en valgt butikk eller en gruppe med butikker.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bed4cfb4875231d11ad76e4403c7995519d56e73
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003684"
---
# <a name="configure-and-run-job-to-post-statements"></a>Konfigurere og kjøre jobben for å postere utdrag

[!include [banner](../includes/banner.md)]

Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å postere utdrag for en valgt butikk eller en gruppe med butikker. Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.

1. Gå til Alle arbeidsområder > .. > Finans for butikk.
2. Klikk på Poster utdrag satsvis.
    * Velg et organisasjonshierarki, og velg deretter en enkelt butikk eller node i organisasjonsnodetreet. Velg en node hvis du vil opprette den satsvise jobben for en gruppe med butikker.  
    * Klikk pilen for å legge til valget.  
3. Klikk på kategorien Kjør i bakgrunnen. ![Kjør i bakgrunnen](../dev-itpro/media/runbackground.png "Kjør i bakgrunnen") 
4. Merk av eller fjern merket for Satsvis behandling.
![Satsvis behandling](../dev-itpro/media/batchprocessing.png "Satsvis behandling og gjentakelse") 
5. Klikk Regelmessighet.
6. Angi en dato i Startdato-feltet.
7. Angi et tidspunkt i Starttidspunkt-feltet.
    * Velg om du vil avslutte gjentakelsen etter et bestemt antall kjøringer, på en bestemt dato eller aldri. Velg deretter de ulike alternativene for å definere hvor ofte du vil at jobben skal kjøres.  
8. Klikk OK.
9. Klikk OK.


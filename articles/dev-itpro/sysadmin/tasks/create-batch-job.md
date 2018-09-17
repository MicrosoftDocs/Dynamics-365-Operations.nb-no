--- 
title: Opprette en satsvis jobb
description: En satsvis jobb er en gruppe oppgaver som sendes til en AOS-forekomst (Application Object Server) for automatisk behandling.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 31c8e2ba87ef8c17a3147e1159104585258d4164
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-batch-job"></a>Opprette en satsvis jobb

[!include [task guide banner](../../includes/task-guide-banner.md)]

En satsvis jobb er en gruppe oppgaver som sendes til en AOS-forekomst (Application Object Server) for automatisk behandling. Satsvise jobber kjøres med samme sikkerhetslegitimasjon som brukeren som opprettet jobben. Bruk fremgangsmåten nedenfor til å opprette en satsvis jobb. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-the-batch-job"></a>Opprette den satsvise jobben
1. Gå til Systemadministrasjon > Forespørsler > Satsvise jobber.
2. Klikk Ny.
3. Skriv inn en verdi i Jobbeskrivelse-feltet.
4. Angi en dato og et klokkeslett i feltet Planlagt startdato/-klokkeslett.
5. Klikk Lagre.

## <a name="create-a-recurrence"></a>Opprette en gjentakelse
1. Klikk Satsvis jobb i handlingsruten.
2. Klikk Regelmessighet.
    * Bruk disse alternativene for å angi et område og mønster for regelmessighet.  
3. Klikk OK.

## <a name="add-alerts"></a>Legge til varsler
1. Klikk Satsvis jobb i handlingsruten.
2. Klikk Varsler.
    * Angi om du vil at det skal sendes varslingsmeldinger når den satsvise jobben avsluttes, har en feil eller avbrytes. Angi deretter om du vil at varslene skal vises som popup-meldinger.   
3. Klikk OK.



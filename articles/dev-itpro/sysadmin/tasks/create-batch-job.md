--- 
title: Opprett satsvise jobber
description: En satsvis jobb er en gruppe oppgaver som sendes til en AOS-forekomst (Application Object Server) for automatisk behandling.
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b32c16a0c0045e22128746f81c6e9fd03370ac1f
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---
# <a name="create-batch-jobs"></a>Opprett satsvise jobber

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



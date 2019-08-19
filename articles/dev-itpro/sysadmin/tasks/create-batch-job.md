---
title: Opprette en satsvis jobb
description: En satsvis jobb er en gruppe oppgaver som sendes til en AOS-forekomst (Application Object Server) for automatisk behandling.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27541c84a40fe9b7e7705162e06167ad4f7e4ed9
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851293"
---
# <a name="create-a-batch-job"></a>Opprette en satsvis jobb

[!include [task guide banner](../../includes/task-guide-banner.md)]

En satsvis jobb er en gruppe oppgaver som sendes til en AOS-forekomst (Application Object Server) for automatisk behandling. Satsvise jobber kjøres med samme sikkerhetslegitimasjon som brukeren som opprettet jobben. Bruk fremgangsmåten nedenfor til å opprette en satsvis jobb. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-the-batch-job"></a>Opprette den satsvise jobben
1. Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Forespørsler > Satsvise jobber**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i **Jobbeskrivelse**-feltet.
4. Angi en dato og et klokkeslett i feltet **Planlagt startdato/-klokkeslett**.
5. Klikk **Lagre**.

## <a name="create-a-recurrence"></a>Opprette en gjentakelse
1. Klikk på **Satsvis jobb** i handlingsruten.
2. Klikk på **Regelmessighet**. Bruk disse alternativene for å angi et område og mønster for regelmessighet.  
3. Klikk **OK**.

## <a name="add-alerts"></a>Legge til varsler
1. Klikk på **Satsvis jobb** i handlingsruten.
2. Klikk på **Varsler**. Angi om du vil at det skal sendes varslingsmeldinger når den satsvise jobben avsluttes, har en feil eller avbrytes. Angi deretter om du vil at varslene skal vises som popup-meldinger.   
3. Klikk **OK**.

## <a name="adjust-batch-job-status"></a>Justere status for satsvis jobb
1. Gå til **Systemadministrasjon > Forespørsler > Satsvise jobber**.
2. Velg den riktige satsvise jobben.
3. Klikk på **Satsvis jobb > Funksjoner > Endre status** i handlingsruten.
4. Velg den aktuelle statusen:
    - **Trekk tilbake**: Angi **tilbakeholdt** for den satsvise jobben, slik at den holdes tilbake fra planleggeren for satsvis jobb. Tilsvarer *stopp*.
    - **Venter**: Angi **venter** for den satsvise jobben, slik at den venter på å bli hentet av planleggeren for satsvis jobb. Tilsvarer *start*.
5. Klikk **OK**.

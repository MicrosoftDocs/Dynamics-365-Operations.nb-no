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
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4360cd7068658a170f5b44c2ce7c71c39c44fa8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679894"
---
# <a name="create-a-batch-job"></a>Opprette en satsvis jobb

[!include [banner](../../includes/banner.md)]

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

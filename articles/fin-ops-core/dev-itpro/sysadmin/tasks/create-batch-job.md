---
title: Opprette en satsvis jobb
description: En satsvis jobb er en gruppe oppgaver som sendes til en AOS-forekomst (Application Object Server) for automatisk behandling.
author: matapg007
ms.date: 11/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: matgupta
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
ms.openlocfilehash: 06fb9a18e70c316be97645ba76f9462cd3ccc729
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292458"
---
# <a name="create-a-batch-job"></a>Opprette en satsvis jobb

[!include [banner](../../includes/banner.md)]

En satsvis jobb er en gruppe oppgaver som sendes til en AOS-forekomst (Application Object Server) for automatisk behandling. Satsvise jobber kjøres med samme sikkerhetslegitimasjon som brukeren som opprettet jobben. Bruk fremgangsmåten nedenfor til å opprette en satsvis jobb. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-the-batch-job"></a>Opprette den satsvise jobben
1. Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Forespørsler > Satsvise jobber**.
2. Velg **Ny**.
3. I **Jobbeskrivelse**-feltet angir du en beskrivelse av den satsvise jobben.
4. Skriv inn dato og klokkeslett for kjøring av den satsvise jobben i feltet **Planlagt startdato/-klokkeslett**.
5. Velg **Lagre**.

## <a name="create-a-recurrence"></a>Opprette en gjentakelse
1. Velg **Satsvis jobb** i handlingsruten.
2. Velg **Regelmessighet**. Bruk disse alternativene for å angi et område og mønster for regelmessighet.  
3. Velg **OK**.

## <a name="add-alerts"></a>Legge til varsler
1. Velg **Satsvis jobb** i handlingsruten.
2. Velg **Varsler**. Angi om du vil at det skal sendes varslingsmeldinger når den satsvise jobben avsluttes, har en feil eller avbrytes. Angi deretter om du vil at varslene skal vises som popup-meldinger.   
3. Velg **OK**.

## <a name="add-a-task-to-a-batch-job"></a>Legge til en oppgave i en satsvis jobb
1.  På **Satsvise jobber**-siden velger du **Vis oppgaver**.
2.  Velg **Ctrl+N** for å opprette en oppgave.
3.  Angi en beskrivelse av den satsvise oppgaven.
4.  I **Firmakontoer**-feltet velger du firmadatabasen der oppgaven skal kjøres.
5.  I feltet **Klassenavn** velger du prosessen du vil at oppgaven skal kjøre. 
6.  Velg en satsvis gruppe for oppgaven etter behov.

    Klientoppgaver må tilordnes en satsvis gruppe. De tilordnes automatisk til standard satsvis gruppe (kalles også Tom satsvis gruppe).

7.  Velg **Ctrl+S** for å lagre oppgaven.
8.  Hvis du vil gjøre den valgte oppgaven avhengig av en annen oppgave i jobben, velger du **Har betingelser**-rutenettet, og følger deretter disse trinnene for hver betingelse du vil definere:

    1. Velg **Ctrl+N** for å opprette en betingelse.
    2. Velg oppgave-IDen til den overordnede oppgaven.
    3. Velg statusen den overordnede oppgaven må ha før den avhengige oppgaven kan kjøres.
    4. Velg **Ctrl+S** for å lagre betingelsen.

    Hvis du har angitt mer enn én betingelse, og hvis *alle* betingelsene må være oppfylt før den avhengige oppgaven kan kjøres, velger du betingelsestypen **Alle**. Hvis den avhengige oppgaven kan kjøres når *hvilken som helst* av betingelsene er oppfylt, velger du betingelsestypen **Vilkårlig**.

9.  Velg hvordan mislykkede oppgaver skal behandles. Hvis du vil ignorere en bestemt oppgave hvis den mislykkes, velger du alternativet **Ignorer oppgavefeil** for den aktuelle oppgaven i fanen **Generelt**. Hvis du merker av for dette alternativet, vil ikke hele jobben mislykkes hvis denne ene oppgaven mislykkes. Du kan også bruke feltet **Maksimalt antall nye forsøk** til å angi hvor mange nye forsøk på å fullføre oppgaven som skal gjøres før den regnes som mislykket. Det er en anbefalt fremgangsmåte å ikke sette feltet **Maksimalt antall nye forsøk** til en verdi som er mer enn **5**.

    Hvis du vil ha mer informasjon om satsvise nye forsøk, kan du se [Aktiver nye forsøk på satsvise jobber](../retryable-batch.md).

## <a name="adjust-batch-job-status"></a>Justere status for satsvis jobb
1. Gå til **Systemadministrasjon > Forespørsler > Satsvise jobber**.
2. Velg den riktige satsvise jobben.
3. Klikk på **Satsvis jobb > Funksjoner > Endre status** i handlingsruten.
4. Velg den aktuelle statusen:
    - **Trekk tilbake**: Angi **tilbakeholdt** for den satsvise jobben, slik at den holdes tilbake fra planleggeren for satsvis jobb. Tilsvarer *stopp*.
    - **Venter**: Angi **venter** for den satsvise jobben, slik at den venter på å bli hentet av planleggeren for satsvis jobb. Tilsvarer *start*.
5. Velg **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

---
title: Hva er nytt eller endret i Dynamics 365 for Talent Core HR (1. oktober 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: 97820cd25ece48dc0b8045d9ba509d0971ca5aad
ms.contentlocale: nb-no
ms.lasthandoff: 10/16/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-1-2018"></a>Hva er nytt eller endret i Dynamics 365 for Talent Core HR (1. oktober 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.1035.0**

Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.

## <a name="turn-off-electronic-payment-validation"></a>Slå av validering av elektroniske betalinger

Validering av elektroniske betalinger skjer hvis du setter opp leverandørbetalinger for direkteinnskudd, enten via arbeidsområdet **Ansattselvbetjening** eller direkte på ansattskjemaet. Dette alternativet gir deg fleksibilitet til å fjerne denne valideringen hvis du ikke trenger valideringskontrollerer for beløp og gjenværende verdier. Denne funksjonen er nyttig hvis du skal integrere med et eksternt lønnssystem som har forskjellige krav.

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a>Lederselvbetjening - Legg til mål for teammedlemmer via flisen Ytelsesmål for team

Før denne versjonen kan ledere legge til mål for ansatte individuelt via ytelsesmålene knyttet til hver ansatt. Med denne oppdateringen kan ledere få tilgang til flisen **Ytelsesmål for team** og opprette nye mål ved å velge en av de direkte rapportene.

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a>Lederselvbetjening - Legg til gjennomganger for teammedlemmer via flisen Gjennomganger av teamytelse

Før denne versjonen kan ledere legge til gjennomganger for ansatte individuelt via gjennomgangene knyttet til hver ansatt. Med denne oppdateringen kan ledere få tilgang til flisen **Gjennomgang av teamytelse** og opprette nye gjennomganger ved å velge en av de direkte rapportene.

## <a name="configure-proration-options-by-leave-plan"></a>Konfigurere fordelingsalternativer etter permisjonsplan

Organisasjoner belønner de ansatte med fritid på forskjellige måter, basert på når ansatte starter hos og forlater firmaet. I noen organisasjoner får de ansatte fullstendig tildeling på startdatoen mens andre fordeler bonusen. Du finner nye alternativer i denne versjonen som lar deg velge hvordan belønningene og avsetningene skal fordeles for ansatte som starter hos og forlater en organisasjon. Alternativene omfatter: Fordelt, Full avsetning og ingen avsetning.

## <a name="other-changes"></a>Andre endringer

-   Ansattenhet oppdatert – **Personlig**-flisen kan nå oppdateres ved hjelp av Excel-tillegg / dataadministrasjon.

-   Sikkerhetsendring for å tillate fjerning av knappene **Slett** og **Deaktiver** i ansattselvbetjening for betalingsinformasjon.

## <a name="known-issue"></a>Kjent problem

-   **Problem:** Når du legger til en ny tilknytning til en arbeider, er knappenei **Ny** og **Rediger** nedtonet. **Løsning:** Før du åpner vedleggssiden, må du kontrollere at faktaboksene på **Arbeider**-siden er lukket. Hvis faktaboksene er lukket når **Arbeider**-siden lastes, blir **Vedlegg**-knappene aktivert. (Dette problemet vil bli løst i neste plattformoppdatering.)


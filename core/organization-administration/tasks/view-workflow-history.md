--- 
title: Vis arbeidsflytlogg
description: "Bruk denne fremgangsmåten til å vise status for et dokument som er sendt til arbeidsflytsystemet for behandling og godkjenning."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a0e16467972596ad6d8b0d9785e68b487150781c
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="view-workflow-history"></a>Vis arbeidsflytlogg

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bruk denne fremgangsmåten til å vise status for et dokument som er sendt til arbeidsflytsystemet for behandling og godkjenning. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.

1. Gå til Felles > Forespørsler > Arbeidsflyt > Arbeidsflytlogg.
    * Bruk dette skjemaet til å vise status for et dokument som er sendt til arbeidsflytsystemet for behandling og godkjenning.  
    * Arbeidsflyt-IDen er identifikasjonskoden til arbeidsflytforekomsten som behandler, eller som har behandlet, dokumentet.  
    * Statusen er arbeidsflytstatusen for dokumentet.  
    * Arbeidsflyt-IDen er identifikasjonskoden til arbeidsflyten som behandler, eller som har behandlet, dokumentet.  
    * Dokumentet er identifikasjonskoden for dokumentet.  
    * Dokumenttypen er typen dokument som ble sendt til behandling.  
    * Arbeidsflyten er navnet på arbeidsflyten som behandler, eller som har behandlet, dokumentet.  
    * Versjonen er versjonsnummeret for arbeidsflyten som behandler, eller som har behandlet, dokumentet.  
    * Opprettingsdato og -klokkeslett er datoen og klokkeslettet da dokumentet ble sendt.  
    * Tidsforbruk er tiden som har gått siden dokumentet ble sendt.  
    * Med Fortsett-knappen kan du gjenoppta arbeidsflytprosessen for det valgte dokumentet.  
    * Med Tilbakekall-knappen kan du kalle tilbake til det valgte dokumentet slik at det ikke blir behandlet.   
2. Klikk koblingen i den valgte raden i listen.
    * Kontroller at delen Arbeidselementer er utvidet.    I denne delen kan du vise arbeidselementene som er tilknyttet det valgte dokumentet. Det kan for eksempel hende at en oppgave må fullføres, eller at dokumentet må godkjennes.  
    * Med knappen Tilordne på nytt åpner du en dialogboks der du kan tilordne et arbeidselement på nytt til en annen bruker.  
    * Kontroller at delen Sporingsdetaljer er utvidet.    I denne delen kan du vise arbeidsflytloggen for det valgte dokumentet.  



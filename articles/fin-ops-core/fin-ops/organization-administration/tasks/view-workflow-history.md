---
title: Vis arbeidsflytlogg
description: Denne artikkelen beskriver fremgangsmåten for å vise status for et dokument som er sendt til arbeidsflytsystemet for behandling og godkjenning.
author: jasongre
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a5810eaed5d2ff6cb5c98e1b21c098c70f24485
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868586"
---
# <a name="view-workflow-history"></a>Vis arbeidsflytlogg

[!include [banner](../../includes/banner.md)]


[!INCLUDE [PEAP](../../../../includes/peap-1.md)]

Denne artikkelen beskriver fremgangsmåten for å vise status for et dokument som er sendt til arbeidsflytsystemet for behandling og godkjenning. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.

1. Gå til **Navigasjonsrute > Moduler > Felles > Forespørsler > Arbeidsflyt > Arbeidsflytlogg**.
    - Bruk dette skjemaet til å vise status for et dokument som er sendt til arbeidsflytsystemet for behandling og godkjenning.  
    - **Arbeidsflyt-ID-en** er identifikasjonskoden til arbeidsflytforekomsten som behandler, eller som har behandlet, dokumentet.  
    - **Status** er arbeidsflytstatusen for dokumentet.  
    - **Arbeidsflyt-ID** er identifikasjonskoden til arbeidsflyten som behandler, eller som har behandlet, dokumentet.  
    - **Dokument** er identifikasjonskoden for dokumentet.  
    - **Dokumenttype** er typen dokument som ble sendt til behandling.  
    - **Arbeidsflyt** er navnet på arbeidsflyten som behandler, eller som har behandlet, dokumentet.  
    - **Versjon** er versjonsnummeret for arbeidsflyten som behandler, eller som har behandlet, dokumentet.  
    - **Opprettingsdato og -klokkeslett** er datoen og klokkeslettet da dokumentet ble sendt.  
    - **Tidsforbruk** er tiden som har gått siden dokumentet ble sendt.  
    - Med **Fortsett**-knappen kan du gjenoppta arbeidsflytprosessen for det valgte dokumentet.  
    - Med **Tilbakekall**-knappen kan du kalle tilbake til det valgte dokumentet slik at det ikke blir behandlet.   
2. Velg koblingen i den ønskede raden i listen.
    - Kontroller at delen **Arbeidselementer** er utvidet. I denne delen kan du vise arbeidselementene som er tilknyttet det valgte dokumentet. Det kan for eksempel hende at en oppgave må fullføres, eller at dokumentet må godkjennes.  
    - Med knappen **Tilordne på nytt** åpner du en dialogboks der du kan tilordne et arbeidselement på nytt til en annen bruker.  
    - Kontroller at delen **Sporingsdetaljer** er utvidet. I denne delen kan du vise arbeidsflytloggen for det valgte dokumentet.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
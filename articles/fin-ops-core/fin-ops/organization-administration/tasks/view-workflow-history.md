---
title: Vise arbeidsflytlogg
description: Dette emnet beskriver fremgangsmåten for å vise status for et dokument som er sendt til arbeidsflytsystemet for behandling og godkjenning.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d7118e85ff56f8c935c24a91dc84c6cc09641e0
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694317"
---
# <a name="view-workflow-history"></a>Vise arbeidsflytlogg

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver fremgangsmåten for å vise status for et dokument som er sendt til arbeidsflytsystemet for behandling og godkjenning. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.

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


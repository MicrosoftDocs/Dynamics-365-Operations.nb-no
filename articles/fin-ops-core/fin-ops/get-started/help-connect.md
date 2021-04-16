---
title: Konfigurere hjelpeopplevelsen for Finance and Operations-apper
description: Dette emnet inneholder informasjon om komponentene i hjelpesystemet for noen Microsoft Dynamics 365-apper.
author: margoc
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82bb9a09e6d302b0d453ceb5131da039769b58fb
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745695"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a>Konfigurere hjelpeopplevelsen for Finance and Operations-apper

[!include [banner](../includes/banner.md)]

I dette emnet vil du finne en oversikt over komponentene i hjelpesystemet for Finance and Operations-apper, for eksempel Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Human Resources. Emnet forklarer også hvordan du kobler disse komponentene og gir et sammendrag av prosessen med å opprette tilpasset hjelp.

## <a name="help-architecture"></a>Hjelpearkitektur

Finance and Operations-apper omfatter begrepsmessige oversikter og andre emner som publiseres til nettstedet for [https://docs.microsoft.com/dynamics365](/dynamics365/). Du får tilgang til dette innholdet fra **Hjelp**-ruten i produktet. Illustrasjonen nedenfor viser delene av hjelpesystemet.

[![Hjelpearkitektur](./media/help-architecture.png)](./media/help-architecture.png)

Hjelpesystemet i produktet trekker ut artikler fra docs.microsoft.com og andre tilkoblede nettsteder. Den henter også inn oppgaveveiledninger som er lagret i forretningsprosessmodelereren (BPM) i Microsoft Dynamics Lifecycle Services (LCS).

## <a name="adding-task-guides"></a>Legge til oppgaveveiledninger

> [!NOTE]
> fanen **Oppgaveveiledninger** er for øyeblikket ikke tilgjengelig i Human Resources eller Commerce. <!--We are currently working to enable this functionality in a future release.--> Oppgaveveiledningene i opplevelsen Komme i gang i Human Resources vil imidlertid fortsatt være tilgjengelige for å dekke grunnleggende funksjonalitet. For både Human Resources og Commerce er prosedyremessig hjelp tilgjengelig på nettstedet for [https://docs.microsoft.com/dynamics365](/dynamics365/).

På siden **Systemparametere** kan systemadministratorer konfigurere tilgang til de relevante oppgavelinjebibliotekene for en implementering.

> [!NOTE]
> - Hvis du vil konfigurere Hjelp, må du logge på med en konto i samme leier som leieren der appen er distribuert.
> - Et LCS-biblioteket kan ikke kobles til fra en forekomst av appen som kjører på en virtuell harddisk (VHD).

[![Skjemaet Systemparametere med innstillinger for hjelp](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Hvis du vil konfigurere oppgavelinjer for en løsning, følger du denne fremgangsmåten på siden **Systemparametere**.

> [!IMPORTANT]
> Første gang du åpner fanen **Hjelp**, må du koble til Lifecycle Services. Husk å velge koblingen i midten av skjemaet, vent på tilkoblingen, lukk dialogboksen og velg **OK** for å få tilgang til siden **Systemparametere**.
>
> [![Koble til LCS](./media/connect-to-lcs-crop-1024x365.png "Koble til LCS")](./media/connect-to-lcs-crop.png)

1. Velg Lifecycle Services-prosjektet du vil koble til.
2. Velg BPM-bibliotekene (i det valgte prosjektet) du vil hente oppgaveregistreringer fra.
3. Angi visningsrekkefølge for BPM-bibliotekene. Visningsrekkefølgen definerer hvilken rekkefølge oppgaveregistreringer fra bibliotekene skal vises i, i **Hjelp**-ruten.

Etter at du har fullført disse trinnene, kan du åpne **Hjelp**-ruten og velge fanen **Oppgaveveiledninger**. Du ser nå oppgaveveiledningene som gjelder for siden du er på i Finance and Operations-apper. Hvis det ikke finneds noen oppgaveveiledninger, kan du angi nøkkelord for å presisere søket.

### <a name="showing-translated-task-guides"></a>Vise oversatte oppgaveveiledninger

Oversatte oppgaveveiledninger ble først lansert i APQC Unified Library fra mai 2016 og i Komme i gang-biblioteket. Hvis du vil vise lokalisert hjelp for oppgaveveiledning, må du sørge for at Dynamics 365-løsningen er koblet til biblioteket for mai 2016. Brukere kan endre språket som en oppgaveveiledning vises i, ved å endre språkinnstillingene under **Alternativer** &gt; **Innstillinger**.

> [!NOTE]
> Selv om mange oppgaveveiledninger er oversatt, viser klienten for øyeblikket ikke de oversatte navnene på oppgaveveiledningene. I tillegg er oversettelser tilgjengelige i bibliotekte for mai 2016 bare for oppgaveveiledningene som ble lansert i februar 2016. Microsoft vil publisere et oppdatert bibliotek som inkluderer flere oversettelser.
>
> - Hvis en oppgaveveiledning er oversatt, vil all teksten i oppgaveveiledningen vises på det valgte språket når du åpner oppgaveveiledningen.
> - Hvis en oppgaveveiledning ikke er oversatt, vil bare noe av teksten (teksten til kontrollene) vises på det valgte språket når du åpner oppgaveveiledningen.

## <a name="adding-custom-help"></a>Legge til tilpasset Hjelp

Du kan bruke oppgaveveiledninger til å opprette tilpasset Hjelp, eller du kan koble et tilpasset nettsted til **Hjelp**-ruten.

### <a name="create-custom-help-by-using-task-guides"></a>Opprette tilpasset Hjelp ved hjelp av oppgaveveiledninger

Du kan opprette tilpasset Hjelp for de støttede appene ved å opprette oppgaveregistreringer som gjenspeiler implementeringen, og deretter kan du lagre dem i et forretningsprosessbibliotek i LCS. Du kan ikke opprette tilpassede oppgaveveiledninger for Human Resources.

Hvis du er partner og du hever nivået for et bibliotek til et firmabibliotek og inkludere det i en løsning, vil det være tilgjengelig for kundene dine. Du kan også lage en kopi av det APQC-enhetlige biblioteket og deretter åpne oppgaveregistreringene i kopien, redigere dem og lagre endringene. Hvis du vil ha mer informasjon, kan du se [Ressurser for Oppgaveregistrering](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-help-site"></a>Koble til et tilpasset hjelpeområde

Finance and Operations-apper blir sjelden brukt i sin bruksklare form. Løsningen er i stedet tilpasset og utvidet for å tilpasses organisasjonens behov. Du kan også tilpasse og utvide hjelpeopplevelsen. Du kan for eksempel legge til tilpasset hjelp i **Hjelp**-ruten i produktet.

Microsoft tilbyr et verktøysett som hjelper deg med å distribuere og koble til tilpasset i **Hjelp**-ruten. Hvis du vil ha informasjon om hvordan du kan sette opp en tilpasset hjelpløsning som er koblet til **Hjelp**-ruten, kan du se [Oversikt over tilpasset hjelp](../../dev-itpro/help/custom-help-overview.md).

Hvis du vil samarbeide med Microsoft om verktøy og prosesser for å tilpasse hjelp, fyller du ut skjemaet på [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).

## <a name="see-also"></a>Se også

[Hjelpesystem](help-overview.md)  
[Oversikt over tilpasset hjelp](../../dev-itpro/help/custom-help-overview.md)  
[Ressurser for Oppgaveregistrering](../../dev-itpro/user-interface/task-recorder.md)  
[Lage dokumentasjon eller opplæring med Oppgaveregistrering](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[Tilpasset hjelp for GitHub-repositorium](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
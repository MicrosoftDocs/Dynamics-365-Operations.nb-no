---
title: Koble til hjelpesystemet
description: Dette emnet beskriver komponentene i hjelpesystemet for Microsoft Dynamics 365 for Operations, og gir en oversikt over hvordan du kobler dem og et sammendrag over hvordan du oppretter egendefinert hjelp.
author: margoc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: f9af4de5f15125569d8f3e78f36e6a2b9c2a089b
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="connect-the-help-system"></a>Koble til hjelpesystemet

[!include[banner](../includes/banner.md)]


Dette emnet beskriver komponentene i hjelpesystemet for Microsoft Dynamics 365 for Operations. Det gir en oversikt over hvordan du kobler disse komponentene og et sammendrag av hvordan du oppretter egendefinert hjelp. 

<a name="help-architecture"></a>Hjelpearkitektur
-----------------

Illustrasjonen nedenfor viser delene av Dynamics 365 for Operations-hjelpesystemet. Det integrerte hjelpesystemet i produktet henter artikler fra Dynamics 365 for Operations-nettstedet https://docs.microsoft.com i tillegg til oppgaveveiledninger som er lagret i Forretningsprosessmodellereren i Lifecycle Services (LCS). 
**Merk:** Funksjonene som nevnes i diagrammet med en stjerne (\*), er planlagte, men er ennå ikke tilgjengelige. [![Hjelpearkitektur](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Koble til hjelpesystemet
Ved hjelp av siden **Systemparametere**, kobler systemadministratorer delene av hjelpesystemet for en implementering. [![Skjemaet Systemparametere med innstillinger for hjelp](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) På **Systemparametere**-siden følger du disse trinnene:

> [!IMPORTANT]
> Første gang du åpner kategorien **Hjelp**, må du koble til Lifecycle Services. Husk å klikke koblingen i midten av skjemaet, vent på tilkoblingen, lukk dialogboksen og klikk **OK** for å få tilgang til siden **Systemparametere**.[![Koble til LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)

1.  Velg Lifecycle Services-prosjektet du vil koble til.
2.  Velg BPM-bibliotekene (i det valgte prosjektet) du vil hente oppgaveregistreringer fra.
3.  Angi visningsrekkefølge for BPM-bibliotekene. Dette bestemmer hvilken rekkefølge oppgaveregistreringer fra bibliotekene skal vises i, i **Hjelp**-ruten.

Når du har fullført disse trinnene, kan du åpne **Hjelp**-ruten og klikke **Oppgaveveiledninger**-kategorien. Nå vil du se oppgaveveiledningene som gjelder for siden du er på i Dynamics 365 for Operations. Hvis det ikke finneds noen oppgaveveiledninger, kan du angi nøkkelord for å presisere søket.

### <a name="showing-translated-task-guides"></a>Vise oversatte oppgaveveiledninger

Oversatte oppgaveveiledninger ble først levert i APQC Unified Library fra mai 2016, og Komme i gang-biblioteket. Hvis du vil vise lokaliserte oppgaveveiledninger i Microsoft Dynamics 365 for Operations, kontroller at du er koblet til biblioteket fra mai. Språket som en oppgaveveiledning vises i, kontrolleres for hver bruker av språkinnstillingene under **Alternativer** &gt; **Innstillinger**. 

> [!NOTE]
> Selv om mange oppgaveveiledninger er oversatt, viser ikke Dynamics 365 for Operations-klienten de oversatte navnene på oppgaveveiledningene. Bare oppgaveveiledninger som ble utgitt i februar 2016, er også tilgjengelige i oversettelse i mai-biblioteket. Vi vil publisere et oppdatert bibliotek med flere oversettelser.
> -   Hvis en oppgaveveiledning er oversatt, vil all teksten i oppgaveveiledningen vises på det valgte språket når du åpner oppgaveveiledningen.
> -   Hvis en oppgaveveiledning ikke er oversatt, vil bare noe av teksten (teksten til kontrollene) vises på det valgte språket når du åpner oppgaveveiledningen.

## <a name="creating-custom-help"></a>Opprette egendefinert hjelp
Du kan opprette egendefinert hjelp for Dynamics 365 for Operations-implementeringen din ved å opprette oppgaveregistreringer som gjenspeiler implementeringen, og lagre dem i et bibliotek for LCS-forretningsprosess. For partnere, hvis du hever nivået for et bibliotek til et firmabibliotek og inkludere det i en løsning, vil det være tilgjengelig for kundene dine. Du kan også lage en kopi av det globale APQC-enhetlige biblioteket og deretter åpne kopien din, åpne oppgaveregistreringer fra den, endre dem og lagre registreringene sammen med endringene. Hvis du vil ha mer informasjon, se [Opprette en oppgaveregistrering som skal brukes som dokumentasjon eller opplæring](../user-interface/task-recorder.md).

<a name="see-also"></a>Se også
--------

[Hjelpeoversikt](help-overview.md)

[Oversikt over oppgaveopptaker](../user-interface/task-recorder.md)

[Opprette en oppgaveregistrering som skal brukes som dokumentasjon eller opplæring](../user-interface/task-recorder-training-docs.md)






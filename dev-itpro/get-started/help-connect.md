---
title: Koble til hjelpesystemet
description: Dette emnet beskriver komponentene i hjelpesystemet for Microsoft Dynamics 365 for Finance and Operations, og gir en oversikt over hvordan du kobler dem og et sammendrag over hvordan du oppretter egendefinert hjelp.
author: margoc
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
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
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 425e87f8b667b53fcc950730dc4ece6330503d66
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017


---

# Koble til hjelpesystemet
<a id="connect-the-help-system" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Dette emnet beskriver komponentene i hjelpesystemet for Microsoft Dynamics 365 for Finance and Operations. Det gir en oversikt over hvordan du kobler disse komponentene og et sammendrag av hvordan du oppretter egendefinert hjelp. 

## Hjelpearkitektur
<a id="help-architecture" class="xliff"></a>
Illustrasjonen nedenfor viser delene av Finance and Operations-hjelpesystemet. Det integrerte hjelpesystemet i produktet henter artikler fra Finance and Operations-nettstedet https://docs.microsoft.com i tillegg til oppgaveveiledninger som er lagret i Forretningsprosessmodellereren i Lifecycle Services (LCS). 
> [!NOTE]
> Funksjonene som nevnes i diagrammet med en stjerne (\*), er planlagte, men er ennå ikke tilgjengelige. [![Hjelpearkitektur](./media/help-architecture.png)](./media/help-architecture.png)


## Koble til hjelpesystemet
<a id="connecting-the-help-system" class="xliff"></a>
> [!NOTE]
> Kategorien **oppgaveveiledninger** er ikke tilgjengelig i Microsoft Dynamics 365 for Talent og Microsoft Dynamics 365 for Retail. Vi arbeider for å aktivere denne funksjonaliteten i fremtidige utgaver. Oppgaveveiledningene i Kom i gang-delen i Talene vil fortsatt være tilgjengelig for å dekke grunnleggende funksjonalitet. Prosedyrehjelp er også tilgjengelig på webområdet docs.microsoft.com ([docs.microsoft.com/dynamics365/operations](/dynamics365/#pivot=solutions&panel=solutions_operations)) for både Retail og Talent.
 

Ved hjelp av siden **Systemparametere**, kobler systemadministratorer delene av hjelpesystemet for en implementering. [![Skjemaet Systemparametere med innstillinger for hjelp](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) På **Systemparametere**-siden følger du disse trinnene:

> [!IMPORTANT]
> Første gang du åpner kategorien **Hjelp**, må du koble til Lifecycle Services. Husk å klikke koblingen i midten av skjemaet, vent på tilkoblingen, lukk dialogboksen og klikk **OK** for å få tilgang til siden **Systemparametere**.[![Koble til LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)

1.  Velg Lifecycle Services-prosjektet du vil koble til.
2.  Velg BPM-bibliotekene (i det valgte prosjektet) du vil hente oppgaveregistreringer fra.
    - For Finance and Operations, for Microsoft-innhold, velger du QPC Unified Library for Microsoft Dynamics 365 for Finance and Operations fra februar 2017. 
    - For Retail vil vi utgi et bibliotek i juli. 
    - Du trenger ikke velge et bibliotek for Talent – tilkoblingen til riktig biblioteket blir opprettet for deg. 

3.  Angi visningsrekkefølge for BPM-bibliotekene. Dette bestemmer hvilken rekkefølge oppgaveregistreringer fra bibliotekene skal vises i, i **Hjelp**-ruten.

Når du har fullført disse trinnene, kan du åpne **Hjelp**-ruten og klikke **Oppgaveveiledninger**-kategorien. Nå vil du se oppgaveveiledningene som gjelder for siden du er på i Finance and Operations. Hvis det ikke finneds noen oppgaveveiledninger, kan du angi nøkkelord for å presisere søket.

### Vise oversatte oppgaveveiledninger
<a id="showing-translated-task-guides" class="xliff"></a>

Oversatte oppgaveveiledninger ble først levert i APQC Unified Library fra mai 2016, og Komme i gang-biblioteket. Hvis du vil vise lokaliserte oppgaveveiledninger i Finance and Operations, kontroller at du er koblet til biblioteket fra mai. Språket som en oppgaveveiledning vises i, kontrolleres for hver bruker av språkinnstillingene under **Alternativer** &gt; **Innstillinger**. 

> [!NOTE]
> Selv om mange oppgaveveiledninger er oversatt, viser ikke Finance and Operations-klienten de oversatte navnene på oppgaveveiledningene. Bare oppgaveveiledninger som ble utgitt i februar 2016, er også tilgjengelige i oversettelse i mai-biblioteket. Vi vil publisere et oppdatert bibliotek med flere oversettelser.
> -   Hvis en oppgaveveiledning er oversatt, vil all teksten i oppgaveveiledningen vises på det valgte språket når du åpner oppgaveveiledningen.
> -   Hvis en oppgaveveiledning ikke er oversatt, vil bare noe av teksten (teksten til kontrollene) vises på det valgte språket når du åpner oppgaveveiledningen.

## Opprette egendefinert hjelp
<a id="creating-custom-help" class="xliff"></a>
Du kan opprette egendefinert hjelp for Finance and Operations og for Retail ved å opprette oppgaveregistreringer som gjenspeiler implementeringen, og lagre dem i et bibliotek for LCS-forretningsprosess. Du kan ikke opprette egendefinerte oppgaveveiledninger for Talent. 

For partnere, hvis du hever nivået for et bibliotek til et firmabibliotek og inkludere det i en løsning, vil det være tilgjengelig for kundene dine. Du kan også lage en kopi av det globale APQC-enhetlige biblioteket og deretter åpne kopien din, åpne oppgaveregistreringer fra den, endre dem og lagre registreringene sammen med endringene. Hvis du vil ha mer informasjon, se [Opprette en oppgaveregistrering som skal brukes som dokumentasjon eller opplæring](../user-interface/task-recorder.md).

Se også
<a id="see-also" class="xliff"></a>
--------

[Hjelpeoversikt](help-overview.md)

[Oversikt over oppgaveopptaker](../user-interface/task-recorder.md)

[Opprette en oppgaveregistrering som skal brukes som dokumentasjon eller opplæring](../user-interface/task-recorder-training-docs.md)






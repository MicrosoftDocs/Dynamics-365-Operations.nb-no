---
title: Koble til hjelpesystemet
description: Dette emnet beskriver komponentene i hjelpesystemet for Finance and Operations-apper, og gir en oversikt over hvordan du kobler dem og et sammendrag over hvordan du oppretter egendefinert hjelp.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 491024c9c3d6c7d20ef212e167ceab6abac8dac7
ms.sourcegitcommit: d554faca895609b8124bf2ea5aca5a55c407534a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2019
ms.locfileid: "2537861"
---
# <a name="connect-the-help-system"></a>Koble til hjelpesystemet

[!include [banner](../includes/banner.md)]

Dette emnet beskriver komponentene i hjelpesystemet for Finance and Operations-apper, for eksempel Dynamics 365 Finance, Supply Chain Management, Retail og Talent. Det gir en oversikt over hvordan du kobler disse komponentene og et sammendrag av hvordan du oppretter egendefinert hjelp.

## <a name="help-architecture"></a>Hjelpearkitektur

Illustrasjonen nedenfor viser delene av hjelpesystemet. Det integrerte hjelpesystemet i produktet henter artikler fra https://docs.microsoft.com i tillegg til oppgaveveiledninger som er lagret i Forretningsprosessmodellereren i Lifecycle Services (LCS).

> [!NOTE]
> Funksjonene som nevnes i diagrammet med en stjerne (\*), er planlagte, men er ennå ikke tilgjengelige.

[![Hjelpearkitektur](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Koble til hjelpesystemet

> [!NOTE]
> Kategorien **Oppgaveveiledninger** er ikke tilgjengelig for øyeblikket i Dynamics 365 Talent eller Retail. Vi arbeider for å aktivere denne funksjonaliteten i fremtidige utgaver. Oppgaveveiledningene i Kom i gang-delen i Talene vil fortsatt være tilgjengelig for å dekke grunnleggende funksjonalitet. Prosedyrehjelp er også tilgjengelig på nettstedet docs.microsoft.com for Retail og Talent.

Ved hjelp av siden **Systemparametere**, kobler systemadministratorer delene av hjelpesystemet for en implementering.

[![Skjemaet Systemparametere med innstillinger for hjelp](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Følge denne fremgangsmåten på siden **Systemparametere**:

> [!IMPORTANT]
> Første gang du åpner kategorien **Hjelp**, må du koble til Lifecycle Services. Husk å klikke koblingen i midten av skjemaet, vent på tilkoblingen, lukk dialogboksen og klikk **OK** for å få tilgang til **Systemparametere**-siden.
>
> [![Koble til LCS](./media/connect-to-lcs-crop-1024x365.png "Koble til LCS")](./media/connect-to-lcs-crop.png)

1. Velg Lifecycle Services-prosjektet du vil koble til.
2. Velg BPM-bibliotekene (i det valgte prosjektet) du vil hente oppgaveregistreringer fra.
3. Angi visningsrekkefølge for BPM-bibliotekene. Dette bestemmer hvilken rekkefølge oppgaveregistreringer fra bibliotekene skal vises i, i **Hjelp**-ruten.

Når du har fullført disse trinnene, kan du åpne **Hjelp**-vinduet og klikke på **Oppgaveveiledning**-fanen. Du ser nå oppgavelinjene som gjelder for siden du er på for øyeblikket i Finance and Operations-apper. Hvis det ikke finneds noen oppgaveveiledninger, kan du angi nøkkelord for å presisere søket.

### <a name="showing-translated-task-guides"></a>Vise oversatte oppgaveveiledninger

Oversatte oppgaveveiledninger ble først levert i APQC Unified Library fra mai 2016, og Komme i gang-biblioteket. Hvis du vil vise lokaliserte oppgaveveiledninger i Finance and Operations-apper, kontroller at du er koblet til biblioteket fra mai. Språket som en oppgaveveiledning vises i, kontrolleres for hver bruker av språkinnstillingene under **Alternativer** &gt; **Innstillinger**.

> [!NOTE]
> Selv om mange oppgaveveiledninger er oversatt, viser ikke klienten de oversatte navnene på oppgaveveiledningene. Bare oppgaveveiledninger som ble utgitt i februar 2016, er også tilgjengelige i oversettelse i mai-biblioteket. Vi vil publisere et oppdatert bibliotek med flere oversettelser.
>
> - Hvis en oppgaveveiledning er oversatt, vil all teksten i oppgaveveiledningen vises på det valgte språket når du åpner oppgaveveiledningen.
> - Hvis en oppgaveveiledning ikke er oversatt, vil bare noe av teksten (teksten til kontrollene) vises på det valgte språket når du åpner oppgaveveiledningen.

## <a name="creating-custom-help"></a>Opprette egendefinert hjelp

Du kan bruke støttelinjer for å opprette egendefinert hjelp, eller du kan koble et webområde til Hjelp-ruten.

### <a name="create-custom-help-with-task-guides"></a>Opprette egendefinert hjelp med oppgaveveiledninger

Du kan opprette egendefinert hjelp for Supply Chain Management og for Retail ved å opprette oppgaveregistreringer som gjenspeiler implementeringen, og lagre dem i et bibliotek for LCS-forretningsprosess. Du kan ikke opprette egendefinerte oppgaveveiledninger for Talent.

For partnere, hvis du hever nivået for et bibliotek til et firmabibliotek og inkludere det i en løsning, vil det være tilgjengelig for kundene dine. Du kan også lage en kopi av det globale APQC-enhetlige biblioteket og deretter åpne kopien din, åpne oppgaveregistreringer fra den, endre dem og lagre registreringene sammen med endringene. Hvis du vil ha mer informasjon, se [Opprette en oppgaveregistrering som skal brukes som dokumentasjon eller opplæring](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-site"></a>Koble til et tilpasset område

Microsoft har en hvitbok og eksempelkode som beskriver hvordan du kan opprette og koble et område med tilpasset hjelp til Hjelp-ruten. Hvis du vil ha mer informasjon,  kan du se:

- [Lage egendefinert hjelp for Finance and Operations-apper (hvitbok)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [Egendefinert hjelp for GitHub-repositoriet](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over Hjelp](help-overview.md)

[Oversikt over oppgaveopptaker](../../dev-itpro/user-interface/task-recorder.md)

[Opprette en oppgaveregistrering som skal brukes som dokumentasjon eller opplæring](../../dev-itpro/user-interface/task-recorder-training-docs.md)

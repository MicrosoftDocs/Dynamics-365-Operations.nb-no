---
title: Koble til hjelpesystemet
description: Dette emnet beskriver komponentene i hjelpesystemet for Microsoft Dynamics 365 for Operations, og gir en oversikt over hvordan du kobler dem og et sammendrag over hvordan du oppretter egendefinert hjelp.
author: margoc
manager: AnnBe
ms.date: 2017-04-04
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
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 5ac5e30cff2239f601778001368fa7aaba478f5c
ms.lasthandoff: 03/31/2017


---

# <a name="connect-the-help-system"></a>Koble til hjelpesystemet

Dette emnet beskriver komponentene i hjelpesystemet for Microsoft Dynamics-365 for operasjoner. Det gir en oversikt over hvordan du kobler disse komponentene og et sammendrag av hvordan du oppretter egendefinerte hjelp. 

<a name="help-architecture"></a>Hjelpearkitektur
-----------------

Illustrasjonen nedenfor viser delene i Dynamics-365 for hjelp for operasjoner. Hjelpesystemet i produktet trekker artikler fra Dynamics-365 for området operasjoner på https://docs.microsoft.com, i tillegg til aktivitet støttelinjer som er lagret i Business Process modell i livssyklusen tjenester (LCS). 
**Merk:** funksjoner som er oppført i diagrammet med en stjerne (\*) er planlagt, men ennå ikke er tilgjengelig. [![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Koble til hjelpesystemet
Ved hjelp av den **systemparametere** siden systemadministratorer koble delene av hjelpesystemet for implementering. [![Parametere-skjemaet for systemet med innstillinger for hjelp](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) på den **systemparametere** side, følger du denne fremgangsmåten:

1.  **Viktig:** første gang du åpner den **å** kategorien, må du koble til levetidstjenester. Husk å klikke koblingen i midten av skjemaet, venter på tilkoblingen, lukke dialogboksen, og klikk deretter **OK** å få tilgang til den **systemparametere** siden. [![Koble til LCS](./media/connect-to-lcs-crop-1024x365.png "koble til LCS")](./media/connect-to-lcs-crop.png)
2.  Velg Lifecycle Services-prosjektet du vil koble til.
3.  Velg BPM-bibliotekene (i det valgte prosjektet) du vil hente oppgaveregistreringer fra.
4.  Angi visningsrekkefølge for BPM-bibliotekene. Dette bestemmer hvilken rekkefølge oppgaveregistreringer fra bibliotekene skal vises i, i **Hjelp**-ruten.

Når du har fullført disse trinnene, kan du åpne **Hjelp**-ruten og klikke **Oppgaveveiledninger**-kategorien. Nå vil du se oppgaveveiledningene som gjelder for siden du er på i Dynamics 365 for Operations. Hvis det ikke finneds noen oppgaveveiledninger, kan du angi nøkkelord for å presisere søket.

### <a name="showing-translated-task-guides"></a>Vise oversatte oppgaveveiledninger

Oversatte aktivitet støttelinjer først ble levert i mai-2016 APQC Unified biblioteket, og komme i gang-biblioteket. Hvis du vil vise lokaliserte oppgaveveiledninger i Microsoft Dynamics 365 for Operations, kontroller at du er koblet til biblioteket fra mai. Språket som en veiledning for oppgaven vises i kontrolleres for hver bruker av språkinnstillingene under **alternativer**&gt;**innstillinger**. **Obs! ** Selv om mange oppgaveveiledninger er oversatt, viser ikke Dynamics 365 for Operations-klienten de oversatte navnene på oppgaveveiledningene. Bare oppgaven støttelinjene som ble utgitt i februar 2016 er også tilgjengelig i oversettelse i mai-biblioteket. Vi vil publisere et oppdatert bibliotek med flere oversettelser.

-   Hvis en oppgaveveiledning er oversatt, vil all teksten i oppgaveveiledningen vises på det valgte språket når du åpner oppgaveveiledningen.
-   Hvis en oppgaveveiledning ikke er oversatt, vil bare noe av teksten (teksten til kontrollene) vises på det valgte språket når du åpner oppgaveveiledningen.

## <a name="creating-custom-help"></a>Opprette egendefinert hjelp
Du kan opprette egendefinert hjelp for Dynamics 365 for Operations-implementeringen din ved å opprette oppgaveregistreringer som gjenspeiler implementeringen, og lagre dem i et bibliotek for LCS-forretningsprosess. For partnere, hvis du hever nivået for et bibliotek til et firmabibliotek og inkludere det i en løsning, vil det være tilgjengelig for kundene dine. Du kan også lage en kopi av det globale APQC-enhetlige biblioteket og deretter åpne kopien din, åpne oppgaveregistreringer fra den, endre dem og lagre registreringene sammen med endringene. Hvis du vil ha mer informasjon, se [hvordan du oppretter en oppgave registreringen som skal brukes som dokumentasjon eller opplæring](../user-interface/task-recorder.md).

<a name="see-also"></a>Se også
--------

[Help overview](help-overview.md)

[Oversikt over aktiviteten Lydinnspilling](../user-interface/task-recorder.md)

[Opprette en oppgaveregistrering som skal brukes som dokumentasjon eller opplæring](../user-interface/task-recorder-training-docs.md)

[Opprette nye biblioteker for opplæring for Dynamics 365 for operasjoner i levetidstjenester ved hjelp av Oppgaveregistrering (ekstern link)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)



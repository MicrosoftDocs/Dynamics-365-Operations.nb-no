---
title: Opprett nytt prosjekt
description: Dette emnet gir informasjon om hvordan du oppretter et nytt prosjekt.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760623"
---
# <a name="create-a-new-project"></a>Opprett nytt prosjekt

[!include [banner](../includes/banner.md)]

Fullfør fremgangsmåten nedenfor for å opprette et nytt prosjekt.

1. På siden **Prosjektledelse**, velg **Nytt prosjekt**, og skriv inn følgende verdier:

    - **Prosjekttype:** Tid og materialer
    - **Prosjektnavn:** XYZ-oppgraderingsfase 2
    - **Prosjektgruppe:** TM\_WIP
    - **Prosjektkontrakt-ID:** 00000002

2. Velg **Opprett prosjekt**.

## <a name="assign-a-resource-to-a-project"></a>Tilordne en ressurs til et prosjekt

1. På siden **Arbeidstakere** i listen **Arbeidstakere**, velg den oppføringen for den arbeidstakeren du tidligere har satt opp kompetanse for. Åpne deretter arbeidstakerens oppføring.
2. På Handling-panelet, i kategorien **Prosjekt**, i gruppen **Oppsett**, velg **Tilordne prosjekt**.
3. På siden **Oppgaver for ressursvalideringsprosjekt**, i kategorien **Prosjekter**, i **Legg til prosjektet til valgte prosjekter**-feltet, filtrer på **XYZ oppgraderingsfase 2**-prosjektet.
4. I vinduet **Gjenstående prosjekter**, velg ett prosjekt og velg deretter pilknappen for å legge det til vinduet **Valgte prosjekter**.

Du kan også tildele kategorier for en ressurs etter behov. Kategoritypen er enten **Kostnad** eller **Inntekt**. Kategoritypen bestemmes av organisasjonen. Hvis ingen kategorier er tildelt for en ressurs, finner Finance standardkategori på timepriser for kostnader og inntekter.

## <a name="set-up-project-resource-and-role-characteristics"></a>Definere egenskaper for prosjektressurs og rolle

En prosjektleder kan bruke prosjektetressursfunksjonaliteten til å opprette roller som kreves for prosjektet. Roller kan brukes hvis bekreftede ressurser er ukjente når ressursene blir reservert. Roller kan reserveres midlertidig som planlagte ressurser, slik at du kan fortsette prosjektetplanleggingsfasene.

[![Eksempel på en rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso ble ansatt for å fullføre et tid og materialer-prosjekt som har et godkjent prosjektdokument. Den underordnede prosjektlederen fullfører fremdeles omfanget av prosjektet. Ressursbehandleren identifiserer de bestemte ressursene som skal reserveres, for å arbeide med det nye prosjektet. På grunn av prosjektets kritiske karakter, forespurte prosjektsponsoren Senior prosjektleder som en av rollene. Den ressursansvarlige må anskaffe den nye ressursen og definere rollen i systemet dersom junior prosjektleder krever ressursinformasjon under prosjektplanlegging.

Følgende fremgangsmåte viser hvordan ressursbehandleren kan definere rollen som overordnet prosjektleder og tilknytte ressursegenskaper til den. Rollen kan senere brukes til å søke etter ressurser som samsvarer med de nødvendige ressurskompetansene.

1. På siden **Oppsett av roller**, velg **Ny** og skriv inn følgende verdier:

    - **Rolle-ID:** Overordnet prosjektleder
    - **Beskrivelse:** Overordnet prosjektleder

2. Velg **Opprett**.
3. Velg rollen **Senior prosjektleder**, og velg deretter **Konfigurer egenskaper**.
4. I feltet **Egenskapstype** velger du **Ferdighet**.
5. I feltet **Tilgjengelige egenskaper**, skriv inn ferdigheten det skal søkes etter.
6. I feltet **Egenskapstype** velger du **Sertifikat**.
7. I feltet **Tilgjengelige egenskaper** angir du sertifikattypen du skal søke etter.

## <a name="assign-a-project-resource-to-a-project"></a>Tilordne en prosjektressurs til et prosjekt

1. På siden **Alle prosjekter**, velg **XYZ Oppgrader fase 2**-prosjektet.
2. I kategorien **Prosjektteam og planlegging**, velg **Legg til**.
3. I **Rolle**-feltet velger du **Teammedlem**.
4. Velg **Bestill fra kalender**.
5. På siden **Ressurstilgjengelighet**, velg **Vis innstillinger**.
6. På siden **Juster visningsinnstillinger** angir du følgende verdier:

    - **Format for visning av datoområde:** Dag
    - **Vis tilgjengelighetsbeskrivelser:** Ja
    - **Vis gjenstående kapasitet:** Ja

7. Velg en ressurs i listen over ressurser.
8. Velg **Forpliktende bestilling** og **Full kapasitet**.

## <a name="assign-a-resource-to-a-default-role"></a>Tilordne en ressurs til en standardrolle

For å hjelpe prosjektledere eller ressursforvaltere å gå videre med ressursene som kan reserveres for et prosjekt. Du kan knytte en standardrolle til en eksisterende ressurs eller en nylig anskaffet ressurs. Eksempel: Da Daniel ble ansatt, hadde han erfaring og ferdigheter til å fylle rollen som forretningsanalytiker. Ressursbehandleren tilordnet denne rollen som Daniels standardrolle. Derfor la ressursbehandleren Daniel til i et utvalg av forretningsanalytikere som er tilgjengelige for å arbeide med prosjekter.

Under ressursreservering kan prosjektledere filtrere rolleressursene som er tilgjengelige for arbeid på prosjekter. De kan bruke denne informasjonen som én av betingelsene når de utfører analyse av beslutninger med flere kriterier under ressursoppfyllelse. De kan også legge til andre ressursegenskaper i filteret for å søke etter ressurser som har bestemte ferdigheter, utdanning og erfaring for et bestemt prosjekt.

**Scenario:** Et godkjent prosjekt er startet, og rollen Overordnet prosjektstyrer ble reservert som en planlagt ressurs i løpet av prosjektplanleggingsfasen. Ressurslederen har nå anskaffet seg en ressurs for å oppfylle rollen Overordnet prosjektleder.

1. På siden **Ressursliste**, velg **Daniel Goldschmidt**.
2. På siden **Ressursrolle**, velg **Ny** og skriv inn følgende verdier:

    - **Gjelder fra:** Skriv inn gjeldende dato.
    - **Utløper:** Skriv inn **Aldri**.
    - **Rolle:** Skriv inn **Senior prosjektleder**.

3. Velg **Lagre**, og lukk deretter siden.
4. I kategorien **Kompetanser** legger du til ferdigheten **ProjectMgmt** og **PMP**-sertifikatet.

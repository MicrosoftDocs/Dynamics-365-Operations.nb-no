---
title: Opprette et prosjektteam
description: Dette emnet gir informasjon om hvordan du oppretter og administrerer prosjektteam.
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
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760624"
---
# <a name="create-a-project-team"></a>Opprette et prosjektteam

[!include [banner](../includes/banner.md)]

Hvis du vil bruke rollene som tidligere ble angitt i et prosjekt, må en prosjektleder knytte rollene til prosjektet. Et prosjekt kan få tildelt flere roller. For å unngå forvirring merkes disse rollene automatisk under reservasjon. For eksempel, hvis prosjektlederen behøver tre programvareingeniører, genereres automatisk tre programvareingeniører som har **programvareingeniør 1**, **programvareingeniør 2** og **programvareingeniør 3** som etiketter. Hvis rolleegenskaper er angitt tidligere for rollen, brukes de som et filter ved søking etter en ressurs. Du kan legge flere egenskaper etter behov for å spesifisere søket ytterligere.

Visningsinnstillinger kan også tilpasses for å få en bedre oversikt over tilgjengelige ressurser. Det finnes alternativer for å vise tilgjengelighet for hver time, dag, uke, måned, kvartal og år. Det finnes også et alternativ for å vise tilgjengelig og gjenværende kapasitet i ressurser. Dette alternativet er nyttig for tidsstyring, når du estimerer tilgjengelig tid for aktiviteter eller ressurstilgjengelighet.

Prosjektlederen kan velge en rolle på siden, og hvis det finnes en tilgjengelig ressurs som passer til behovet, velge å reservere en ressurs til å fylle rollen. Vær oppmerksom på at ressursene ikke må reserveres på dette tidspunktet i planleggingsfasen. Når du oppretter en prosjektstrukturplan, kan du erstatte roller med bemannede ressurser for prosjektet. Hvis roller erstattes med bemannede ressurser i prosjektstrukturplanen, oppdaterer ressursoppsettet automatisk prosjektgruppeoversikten og -planleggingen.

[![Prosjektgruppeoversikt som inneholder både roller og faktiske ressurser](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Prosjektlederen har forskjellige alternativer for å bestille en ressurs for et prosjekt, for eksempel **Gjenværende kapasitet**, **Full kapasitet**, **Kapasitetsprosent** og **Angi timer**. Disse alternativene for bestilling kan annulleres når som helst hvis ressurstildelinger endres. To typer bestilling støttes:

- **Forpliktende bestilling** – Ressursreserveringen ble godkjent og bekreftet for å arbeide med prosjektet for den angitte varigheten.
- **Ikke-forpliktende bestilling** – Ressursreserveringen ble foreløpig angitt for å arbeide med prosjektet for den angitte varigheten.

Fremgangsmåten nedenfor forklarer hvordan du oppretter et prosjektteam.

## <a name="create-a-project-team"></a>Opprette et prosjektteam

1. Velg et prosjekt på listesiden **Alle prosjekter**, og velg deretter **Rediger**.
2. I kategorien **Prosjektteam og planlegging** i feltet **Planlegg sluttdato** angir du startdato for tidsplanen pluss én måned. Hvis for eksempel startdatoen for tidsplanen er 24. juni 2017 (24/06/2017), angir du **24/07/2017**.
3. Velg **Legg til**.
4. I ruten **Legg til roller i prosjektet** i **Rolle**-feltet velger du **Overordnet prosjektleder**.
5. Velg **Nødvendige kompetanser**.
6. På siden **Velg egenskaper** er egenskapene som du tidligere har angitt for rollen Overordnet prosjektleder, valgt som standard. Velg **OK**.
7. På siden **Legg til roller i prosjekt** i feltet **Antall ressurser** angir du **1**.
8. I **Ressurs**-feltet vil oppslaget vise alle ressurser som har de nødvendige kompetansene. Velg **Daniel Goldschmidt** og velg deretter **Opprett**.
9. På siden **Prosjekt**, velg **Legg till**.
10. I ruten **Legg til roller i prosjektet** i **Rolle**-feltet velger du **Teammedlem**. I feltet **Antall ressurser** angir du **5**.
11. Velg **Opprett**.
12. På siden **Prosjekt**, velg **Oppfyll ressurs**.

## <a name="monitor-project-teams"></a>Overvåke prosjektteam
1. På siden **Alle prosjekter**, velg koblingen **Prosjekt-ID** for prosjektet **XYZ opgraderingsfase 2**.
2. I hurtigkategorien **Prosjektteam og planlegging** kontrollerer du at prosjektressursene som er oppført, er riktige.

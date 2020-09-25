---
title: Synkronisere ressurskapasitet
description: Dette emnet inneholder informasjon om hvordan du synkroniserer kapasiteten til en ressurs på tvers av kalendere og prosjekter.
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
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760622"
---
# <a name="synchronize-resource-capacity"></a>Synkronisere ressurskapasitet

[!include [banner](../includes/banner.md)]

Prosessene for ressurssynkronisering sikrer at informasjon for kalenderen og grunnkalenderen slår ned i prosjektressursplanlegging. Hvis kalenderen er endret, vil prosessene foreta de nødvendige oppdateringene i planleggingen av prosjektressurser. Prosessene bidrar også til å forbedre ytelsen, fordi kalenderens ressursinformasjon er synkronisert på forhånd. Derfor opptrer oppdateringer til ressursplanleggingsinformasjon raskere. Vi anbefaler at du planlegger prosessene som en satsvis jobb i stedet for én om gangen. Ellers er det fare for at noen glemmer datoene da informasjonen ble sist synkronisert. Hvis inklusive datoer ikke brukes, kan det oppstå mellomrom under synkronisering av dato.

![Kalendersynkronisering](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Synkroniser opprullinger av ressurskapasitet

Synkroniseringsprosessen er utformet for å synkronisere all kalenderinformasjon for ressursen. Denne informasjonen inneholder grunnkalenderinformasjon om eventuelle endringer i prosjektets kapasitetstabell i ressurskalender. Hvis det legges til nye ressurser i prosjektet, synkronisering bidrar til å sikre at det finnes oppdatert kalenderinformasjonen. Denne synkroniseringen kan utføres når som helst.

Vi anbefaler at du bruker et parti. Alternativene er tilgjengelige under synkronisering av kapasitetsreservasjoner.

1. Velg **Prosjektstyring og regnskap** &gt; **Periodisk** &gt; **Kapasitetssynkronisering** &gt; **Synkroniser opprullinger av ressuskapasitet**.
2. Sett alternativene i følgende tabell.

    | Alternativ      | beskrivelse |
    |-------------|-------------|
    | Periodekode | Velg valgfritt intervallkoden for hovedboken for å angi start- og sluttdatoer for synkroniseringsprosessen for opprullinger av ressurskapasitet. |
    | Startdato  | Skriv inn startdato for synkroniseringsprosessen for opprullinger av ressurskapasitet. |
    | Sluttdato    | Skriv inn sluttdato for synkroniseringsprosessen for opprullinger av ressurskapasitet. |

[![Synkroniseringsprosess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

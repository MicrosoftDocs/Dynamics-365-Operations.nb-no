---
title: Opprette prognosemodeller for prosjektbudsjetter
description: Dette emnet beskriver hvordan du oppretter en prognosemodell for gjenstående budsjetter.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321785"
---
# <a name="create-forecast-models-for-project-budgets"></a>Opprette prognosemodeller for prosjektbudsjetter 

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter en prognosemodell for gjenstående budsjetter. Et prosjekt som skal gjennomgå budsjettkontroll, bruker to typer budsjetter: opprinnelig budsjett og gjenstående budsjett. Når du oppretter et prosjektbudsjett, må du angi prognosemodellene for opprinnelig og gjenstående budsjett som ble opprettet på siden **Prognosemodeller**. Prosjektbudsjetter som er basert på angitte modeller, opprettes når du igangsetter prosjektbudsjettet.

> [!NOTE]
> En prognosemodell som brukes til budsjettkontroll, kan ikke ha en undermodell og kan ikke brukes som en undermodell.

1. Velg **Prosjektstyring og regnskap** > **Oppsett** > **Prognoser**  > **Prognosemodeller**.
2. Velg **Ny** for å opprette en ny prognosemodell, og angi deretter et modell-ID-nummer og et navn for den nye modellen. 
3. Sett alternativet **Stoppet** til **Ja** for å hindre eventuelle endringer i prognoselinjer for prognosemodellen. 
4. Hvis prognoselinjene som modellen er tilknyttet, skal generere kontantstrømprognoser i økonomimodulen, setter du **Inkluder i kontantstrømprognoser** til **Ja**. 
5. Hvis du vil bruke prosjektdatoen som fakturadato, setter du valget for **prognosefakturadato** til **Ja**. 
6. I **Budgettype**-feltet velger du én av følgende modelltyper:

   - **Opprinnelig budsjett**: Bruk de opprinnelige budsjettbeløpene som igangsettes når det opprinnelige budsjettet opprettes og godkjennes.
   - **Gjenstående budsjett**: Bruk de gjenstående budsjettbeløpene mens prosjektet pågår. Saldoene i denne prognosemodellen reduseres av faktiske transaksjoner og økes eller reduseres av budsjettendringer.
   - **Overført budsjett**: Bruk de overførte budsjettbeløpene for prosjektet. Overføring er en valgfri prosess som kan kjøres for å overføre ubrukte budsjettbeløp fra ett regnskapsår til et annet.

7. Angi følgende alternativer etter behov:

   - Aktiver **Prognosefakturadato** for å bruke prosjektdatoen som fakturadato.
   - Aktiver **Prognose med VIA** for prognosebasert på varer i arbeid (VIA), og velg deretter typen VIA. 
   - Du kan beholde standard **Budsjettype** som **Ingen** eller angi en ny type. Budsjettypen kan ikke endres etter at du har endret en post.     
    > [!NOTE]
    > Hvis du endrer standard budsjettype, blir alle andre alternativer ikke tilgjengelig for oppdateringer, og du kan ikke bruke denne prognosemodellen på nytt. 
   


 


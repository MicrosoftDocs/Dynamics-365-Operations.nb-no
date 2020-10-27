---
title: Fremme en variasjon og fullføre et eksperiment
description: Dette emnet beskriver hvordan du fremmer en vellykket variasjon og fullfører et eksperiment i Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930256"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Fremme en variasjon og fullføre et eksperiment

Dette emnet beskriver hvordan du kan fremme variasjonen som produserte de best resultatene i eksperimentet, og hvordan du fullfører eksperimentet. Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce. Flere trinn er beskrevet i separate emner.

[ ![Brukerreise for eksperimentering – se gjennom og fullføre](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

Når du har [kjørt eksperimentet](experimentation-run-monitor.md) og samlet inn nok data til å avgjøre hvilken variasjon du vil bruke på det aktive området, kan du fremme variasjonen og avslutte eksperimentet.

## <a name="promote-a-variation"></a>Fremme en variasjon
Bruk dataene og analysen som er relatert til eksperimentet i tredjepartstjenesten, til å avgjøre hvilken variant som oppnådde det beste resultatet. Hvis du vil erstatte gjeldende innhold på det aktive området med den vinnende variasjonen, slik at det er tilgjengelig for alle som bruker nettstedet, gjør du følgende: 

1. Gå til kategorien **Eksperimenter** i områdebygger, og velg eksperimentet.
1. Velg **Fullfør eksperimente** på linjen øverst.
1. På dialogboksmenyen **Fullfør eksperiment** velger du **Se gjennom eksperimentdataene** . Det åpnes en tredjepartstjeneste der du kan validere måledataene og avgjøre hvilken variant som er fungerte best.
1. På dialogboksmenyen **Fullfør eksperiment** i områdebygger, velger du den vinnende variasjonen og velger deretter **Neste** .
1. Åpne tredjepartstjenesten, og stopp eksperimentet.
1. Velg **Fullfør** i områdebygger for å overskrive den opprinnelige aktive siden og publisere den vinnende variasjonen, slik at den er tilgjengelig for alle som bruker nettstedet. 

> [!NOTE]
> Hvis du velger å beholde gjeldende aktive side og ikke publisere en variasjon, velger du **Publiser den opprinnelige siden på nytt** .

## <a name="delete-your-experiment"></a>Slette eksperimentet
Selv om det ikke er nødvendig at du sletter et fullført eksperiment i Commerce, kan du velge å slette det for å spare plass eller rydde arbeidsområdet. Gjør følgende for å slette et eksperiment:

1. Gå til kategorien **Eksperimenter** i områdebygger, og velg eksperimentet. 
    > [!NOTE]
    > Hvis eksperimentet fortsatt er aktivt, stopper du eksperimentet i tredjepartstjenesten før du fortsetter.
1. Velg **Opphev publisering** på kommandolinjen for å fjerne variasjonsinnholdet fra det aktive området.
1. Velg **Slett** på kommandolinjen for å slette eksperimentet.

## <a name="previous-step"></a>Forrige trinn
[Kjør og Overvåk et eksperiment](experimentation-run-monitor.md)

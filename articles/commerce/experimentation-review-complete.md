---
title: Fremme en variasjon og fullføre et eksperiment
description: Denne artikkelen beskriver hvordan du fremmer en vellykket variasjon og fullfører et eksperiment i Dynamics 365 Commerce.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 3e9a978551622bbb14d9213f607d9dfabe42672a
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942749"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Fremme en variasjon og fullføre et eksperiment

Denne artikkelen beskriver hvordan du kan fremme variasjonen som produserte de best resultatene i eksperimentet, og hvordan du fullfører eksperimentet. Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce. Flere trinn er beskrevet i separate artikler.

[ ![Brukerreise for eksperimentering – se gjennom og fullføre.](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

Når du har [kjørt eksperimentet](experimentation-run-monitor.md) og samlet inn nok data til å avgjøre hvilken variasjon du vil bruke på det aktive området, kan du fremme variasjonen og avslutte eksperimentet.

## <a name="promote-a-variation"></a>Fremme en variasjon
Bruk dataene og analysen som er relatert til eksperimentet i tredjepartstjenesten, til å avgjøre hvilken variant som oppnådde det beste resultatet. Du kan deretter forfremme den ved å erstatte gjeldende innhold på det aktive området med den vinnende variasjonen, slik at det er tilgjengelig for alle som bruker nettstedet.

Følg denne fremgangsmåten for å forfremme den vinnende variasjonen. 

1. Velg **Eksperimenter** i den venstre navigasjonsruten i Commerce-områdebyggeren, og velg deretter eksperimentet.
1. Velg **Fullfør eksperiment** på kommandolinjen.
1. I dialogboksen **Fullfør eksperiment** velger du **Se gjennom eksperimentdataene**. Det åpnes en tredjepartstjeneste der du kan validere måledataene og avgjøre hvilken variant som er fungerte best.
1. I dialogboksen **Fullfør eksperiment** i områdebygger, velger du den vinnende variasjonen og velger deretter **Neste**.
1. Åpne tredjepartstjenesten, og stopp eksperimentet.
1. Velg **Fullfør** i områdebygger for å overskrive den opprinnelige aktive siden og publisere den vinnende variasjonen, slik at den er tilgjengelig for alle som bruker nettstedet. 

> [!NOTE]
> Hvis du velger å beholde gjeldende aktive side og ikke publisere en variasjon, velger du **Publiser den opprinnelige siden på nytt**.

## <a name="delete-your-experiment"></a>Slette eksperimentet
Selv om det ikke er nødvendig at du sletter et fullført eksperiment i Commerce, kan du velge å slette det for å spare plass eller rydde arbeidsområdet. 

Følg denne fremgangsmåten for å slette et fullført eksperiment i Commerce-områdebyggeren.

1. Velg **Eksperimenter** i den venstre navigasjonsruten, og velg deretter eksperimentet. 
    > [!NOTE]
    > Hvis eksperimentet fortsatt er aktivt, stopper du eksperimentet i tredjepartstjenesten før du fortsetter.
1. Velg **Opphev publisering** på kommandolinjen for å fjerne variasjonsinnholdet fra det aktive området.
1. Velg **Slett** for å slette eksperimentet.

## <a name="previous-step"></a>Forrige trinn
[Kjøre og overvåke et eksperiment](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Identifisere en hypotese og fastslå måledataene for et eksperiment
description: Dette emnet beskriver hvordan du identifiserer hypotesen og suksessmåledataene for et eksperiment som du kan kjøre på et nettsted for e-handel i Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 5594b81d09eade263487244a14c0305d589ff94e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010005"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>Identifisere en hypotese og fastslå suksessmåledataene for et eksperiment
Den første fasen i livssyklusen for eksperimentering omfatter å identifisere hypotesen for eksperimentet og fastslå måledataene du vil spore for å vurdere suksess. Diagrammet nedenfor viser alle trinnene for å [konfigurere og kjøre et eksperiment](experimentation-overview.md) på et nettsted for e-handel i Dynamics 365 Commerce. Flere trinn er beskrevet i separate emner. 

[ ![Brukerreise for eksperimentering – identifisere](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)

En hypotese er en erklæring der du forutser resultatet av eksperimentet. Mange faktorer inngår definisjonen av en hypotese, for eksempel undersøke brukerens atferd og nettstedsdata som du har samlet inn. Med hypotesen definerer du antakelsen eller teorien du vil validere med eksperimentet. Et eksempel på en hypotese for eksperimentet kan være *et bilde av en hvit t-skjorte på startsiden vil gi en høyere grad av gjennomklikking enn en blå genser i sommermånedene fordi brukerne vil gjerne ha på seg noe lett og lyst om sommeren*. I så fall kan du opprette variasjoner som inneholder en hvit t-skjorte og en blå genser og publisere begge samtidig.

For å validere en hypotese må et eksperiment som er en suksess eller er mislykket, være direkte knyttet til brukerhandlinger, for eksempel hvis nettstedsbrukeren klikker på en kobling eller knapp. Disse handlingene må samsvare med hendelser som vil bli rapportert til tredjepartstjenesten som sporer eksperimentet. Over tid blir prosentandelen av brukere som utfører handlingen, registrert som en måleverdi du kan bruke til å generere rapporter og utføre analyser. Se emnet [Hendelser for Commerce-komponent for diagnose og feilsøking](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) for å se gjennom alle tilgjengelige hendelser og attributter.

## <a name="previous-step"></a>Forrige trinn
[Eksperimentering i Dynamics 365 Commerce](experimentation-overview.md)


## <a name="next-step"></a>Neste trinn
[Definere et eksperiment](experimentation-setup.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
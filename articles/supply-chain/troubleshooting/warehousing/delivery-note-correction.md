---
title: Følgeseddelkorrigering kan ikke behandles
description: Hvis du prøver å rette en følgeseddel etter at den er postert, får du en feilmelding. Denne siden beskriver hvordan du retter posterte følgesedler for varer som er aktivert for WMS.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bb0d827adff8abd8762bf2de844cad5574628e4b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477226"
---
# <a name="delivery-note-correction-cant-be-processed"></a>Følgeseddelkorrigering kan ikke behandles

## <a name="symptoms"></a>Symptomer

Når du har postert en følgeseddel, kan du ikke avbryte den fordi **Avbryt**-knappen ikke er tilgjengelig. Du kan heller ikke korrigere følgeseddelen. Hvis du prøver, kan du få følgende feilmelding:

> Følgeseddelkorrigeringen kan ikke behandles. Følgeseddelen inneholder bare varer som er underlagt lagerstyringsprosesser, siden disse ikke støttes av følgeseddelkorrigering.

## <a name="resolution"></a>Løsning

Hvis du vil korrigere posterte følgesedler for varer som er aktivert for avansert lagerstyring (WMS), må du utføre posteringen fra lasten, ikke direkte fra ordren.

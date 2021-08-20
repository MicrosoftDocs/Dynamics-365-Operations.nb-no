---
title: Partinummer tømmes når en ny parti-ID velges
description: Når du gjennomgår en plukklistejournallinje, fjerner du merket for verdien i Partinummer-feltet hvis du velger en ny verdi i Parti-ID-feltet.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6d71720b1d3a34a31639db0f829dee300d6f96d53fd61c0a8740be9f2306d6dd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738825"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>Partinummer tømmes når en ny parti-ID velges

KB-nummer: 4613107

## <a name="symptoms"></a>Symptomer

Når du gjennomgår en plukklistejournallinje, fjerner du merket for verdien i **Partinummer**-feltet hvis du velger en ny verdi i **Parti-ID**-feltet.

## <a name="resolution"></a>Oppløsning

Systemet fungerer som tiltenkt. Hvis du endrer parti-IDen, endrer du varekonteksten. Derfor tilbakestilles partinummeret.

Hvis du vil knytte partinummeret til en parti-ID, må du angi parti-IDen først.

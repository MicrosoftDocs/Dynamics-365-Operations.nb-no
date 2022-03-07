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
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026764"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>Partinummer tømmes når en ny parti-ID velges

KB-nummer: 4613107

## <a name="symptoms"></a>Symptomer

Når du gjennomgår en plukklistejournallinje, fjerner du merket for verdien i **Partinummer**-feltet hvis du velger en ny verdi i **Parti-ID**-feltet.

## <a name="resolution"></a>Oppløsning

Systemet fungerer som tiltenkt. Hvis du endrer parti-IDen, endrer du varekonteksten. Derfor tilbakestilles partinummeret.

Hvis du vil knytte partinummeret til en parti-ID, må du angi parti-IDen først.

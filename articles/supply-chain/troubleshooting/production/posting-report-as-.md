---
title: Feil når Ferdigmeldingsjournalen er postert
description: Når du posterer ferdigmeldingsjournalen, får du en feilmelding som angir at det bestilte antallet ikke kan reduseres.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026768"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a>Feil når Ferdigmeldingsjournalen er postert

KB-nummer: 4612891

## <a name="symptoms"></a>Symptomer

Når du posterer **Ferdigmeld**-journalen, oppstår det en feil, og du får følgende feilmelding:

> Det bestilte antallet kan ikke settes ned siden det ikke finnes nok åpne lagertransaksjoner med status Bestilt. Varene er kjøpt, mottatt eller registrert.

Denne feilen oppstår bare når feltet **Antall feil** er angitt på den første linjen i **Ferdigmeld**-journalen og feltet **Antall korrekte** er angitt på den siste linjen. Hvis feltet **Antall feil** er angitt på den siste linjen, oppstår det ingen feil.

## <a name="resolution"></a>Oppløsning

Hvis du vil hindre denne feilen, åpner du siden **Parametere for produksjonskontroll**, og i kategorien **Generelt** angir du alternativet for **Øk gjenværende antall med feilantall** til *Ja*.

---
title: Valgt formelnummer er ikke godkjent for en partiordre
description: Når du prøver å autorisere en planlagt bestilling, får du en feilmelding som angir at det valgte formelnummeret ikke er godkjent for en partiordre.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a41cf955d151726348bea83e52a24bc8784352c2d07268ced944e4cc6bf35491
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712916"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a>Valgt formelnummer er ikke godkjent for en partiordre

Feilkode: PRO2614

## <a name="symptoms"></a>Symptomer

Når du prøver å autorisere en planlagt ordre, mottar du følgende feilmelding:

> Det valgte formelnummeret er ikke godkjent for en partiordre.

## <a name="cause"></a>Årsak

Systemet validerer autoriseringsoperasjonen for å sikre at en godkjent formel er tilgjengelig for den aktive varen. Du må sannsynligvis godkjenne formelen.

## <a name="resolution"></a>Løsning

For å godkjenne en formel, følg denne fremgangsmåten.

1. Gå til **Behandling av produktinformasjon \> Stykklister og formler \> Formler**.
1. Velg relevant formel.
1. I handlingsruten, i kategorien **Formel**, i **Oppretthold**-gruppen, velger du **Godkjenn formel**.
1. Velg dialogboksen **Godkjenn stykkliste eller formel**, og velg deretter **OK**.

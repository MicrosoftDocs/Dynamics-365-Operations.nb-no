---
title: Du kan legge til bare hovedkontoen som kreditkontoen av avstemmingsårsaker
description: Når du definerer en avstemmingsårsak i Transportstyring, kan du bare legge til hovedkontoen som kreditkontoen.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026765"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>Du kan legge til bare hovedkontoen som kreditkontoen av avstemmingsårsaker

KB-nummer: 4603538

## <a name="symptoms"></a>Symptomer

Når du definerer en avstemmingsårsak i Transportstyring, kan du bare legge til hovedkontoen som kreditkontoen. Du kan ikke legge til et kostsenter eller en annen dimensjon som kreditkonto. Du kan imidlertid bruke debetkontoen til å velge andre dimensjoner.

## <a name="resolution"></a>Oppløsning

Hvis avstemmingen ikke utføres for å betale leverandøren, men for å kreditere en bestemt hovedkonto, lar ikke systemet deg velge en finansdimensjon for kreditkontoen når du definerer avstemmingsårsaken.

Hvis kontostrukturen krever en bestemt finansdimensjonsverdi for hovedkontoen for kredit, kan ikke den resulterende leverandørjournalen posteres automatisk, fordi finansdimensjonsverdien mangler. Derfor må du først angi kreditkontoen manuelt ved hjelp av **Fakturajournal**-siden.

Fordi det kreves en dimensjonsverdi for kreditkontoen, kan ikke leverandørfakturajournalen posteres automatisk. Du må postere den manuelt etter at du manuelt har lagt til dimensjonsverdien i hovedkontoen for kreditlinjen.

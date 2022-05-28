---
title: Sende returnerte varer til inspeksjon
description: Når du registrerer en returnert vare, kan du beslutte at den bør sendes til inspeksjon før den returneres til lager eller avhendes på en annen måte.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 959df8e1ecbc493dc11e4793120f352b94b8b635
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676754"
---
# <a name="pass-returned-items-on-to-inspection"></a>Sende returnerte varer til inspeksjon 

[!include [banner](../includes/banner.md)]


Når du registrerer en returnert vare, kan du beslutte at den bør sendes til inspeksjon før den returneres til lager eller avhendes på en annen måte.

1.  Klikk på **Lagerstyring** \> **Journaler** \> **Vareankomst** \> **Vareankomst**.
    
    \-eller-
    
    Klikk på **Lagerstyring** \> **Journaler** \> **Vareankomst** \> **Produksjonsinnlevering**.

2.  I skjemaet **Lokasjonsjournal** registrerer du mottaket av varen på vanlig måte.
    

    > [!NOTE]
    > <P>Hvis du vil ha informasjon om hvordan du registrerer mottak av returnerte varer, kan du se <A href="register-the-receipt-of-returned-items.md">Registrere mottaket av returnerte varer</A>.</P>



3.  På fanen **Standardverdier** i området **Behandlingsmåte** merker du av for **Karantenestyring**.

Nå vil systemet opprette en karanteneordre, og personen eller avdelingen som utfører inspeksjoner, vil svare på denne ordren ved hjelp av **Karanteneordre**-skjemaet.

## <a name="see-also"></a>Se også

[Ta returnerte varer gjennom inspeksjon](take-returned-items-through-inspection.md)

[Angi hvordan du kvitter deg med returnerte varer](specify-how-to-dispose-of-returned-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
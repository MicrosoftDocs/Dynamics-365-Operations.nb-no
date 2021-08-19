---
title: Sende returnerte varer til inspeksjon
description: Når du registrerer en returnert vare, kan du beslutte at den bør sendes til inspeksjon før den returneres til lager eller avhendes på en annen måte.
author: ShylaThompson
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0aa5d15856b39dcfd948eeeeeabce1b57370acf901a1ff48b0d443bc13a25f1e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722277"
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
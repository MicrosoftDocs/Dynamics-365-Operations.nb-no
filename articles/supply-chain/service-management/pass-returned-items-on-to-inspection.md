---
title: Sende returnerte varer til inspeksjon
description: Når du registrerer en returnert vare, kan du beslutte at den bør sendes til inspeksjon før den returneres til lager eller avhendes på en annen måte.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e8205db277715f4f4f9c1ee589f264c0ded6617
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983825"
---
# <a name="pass-returned-items-on-to-inspection"></a>Sende returnerte varer til inspeksjon 

[!include [banner](../includes/banner.md)]


Når du registrerer en returnert vare, kan du beslutte at den bør sendes til inspeksjon før den returneres til lager eller avhendes på en annen måte.

1.  Klikk **Lagerstyring** \> **Journaler** \> **Vareankomst** \> **Vareankomst** .
    
    \-eller-
    
    Klikk **Lagerstyring** \> **Journaler** \> **Vareankomst** \> **Produksjonsinnlevering** .

2.  I skjemaet **Lokasjonsjournal** registrerer du mottaket av varen på vanlig måte.
    

    > [!NOTE]
    > <P>Hvis du vil ha informasjon om hvordan du registrerer mottak av returnerte varer, kan du se <A href="register-the-receipt-of-returned-items.md">Registrere mottaket av returnerte varer</A>.</P>



3.  På fanen **Standardverdier** i området **Behandlingsmåte** merker du av for **Karantenestyring** .

Nå vil systemet opprette en karanteneordre, og personen eller avdelingen som utfører inspeksjoner, vil svare på denne ordren ved hjelp av **Karanteneordre** -skjemaet.

## <a name="see-also"></a>Se også

[Ta returnerte varer gjennom inspeksjon](take-returned-items-through-inspection.md)

[Angi hvordan du kvitter deg med returnerte varer](specify-how-to-dispose-of-returned-items.md)


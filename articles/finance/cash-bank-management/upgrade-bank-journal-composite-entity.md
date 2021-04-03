---
title: Oppdatere sammensatt enhet for bankjournal
description: Fremgangsmåten nedenfor kreves for å legge til tilleggsfeltet BankTransactionType i den sammensatte BankJournalEntity.
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 18137ca8cecc43b4269f14b36df2eb8063192e52
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236353"
---
# <a name="update-the-bank-journal-composite-entity"></a>Oppdatere sammensatt enhet for bankjournal

[!include [banner](../includes/banner.md)]

Fremgangsmåten nedenfor kreves for å legge til tilleggsfeltet BankTransactionType i den sammensatte BankJournalEntity.

Bruk fremgangsmåten nedenfor for å legge til tilleggsfeltet BankTransactionType i den sammensatte BankJournalEntity.

1.  Kompiler og synkroniser følgende sammensatte enheter for bankjournalen, enheter og oppsamlingstabeller:
    -   Sammensatt Entity\\BankJournalEntity
    -   Entity\\BankJournalHeaderEntity
    -   Entity\\BankJournalLineEntity
    -   Table\\BankJournalHeaderStaging
    -   Table\\BankJournalLineStaging

2.  Databehandling\\dataprosjekter
    -   Viser **Banktransaksjon**-typen på **Kildedata**-oppsettet.
        -   Kildedataformat = XML-element
        -   Enhetsnavn = Bankjournal
        -   Last opp datafil = ny versjon SampleBankJournalCompositeEntity.xml
        -   Klikk **Ja** for å overskrive den eksisterende filen.
        -   Klikk **Ja** for å generere tilordningen fra bunnen av.
        -   Kontroller at Banktransaksjon-typen er tilordnet.
            -   Klikk **Vis tilordning** i linjeenhet.
            -   Kontroller at Banktransaksjon-typen er tilordnet fra Kilde til Oppsamling.

3.  Importer det nye utdraget.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
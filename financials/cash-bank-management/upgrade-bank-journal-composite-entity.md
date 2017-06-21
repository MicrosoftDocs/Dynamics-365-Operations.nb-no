---
title: Oppdatere sammensatt enhet for bankjournal
description: "Fremgangsmåten nedenfor kreves for å legge til tilleggsfeltet BankTransactionType i den sammensatte BankJournalEntity."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 43413aad9d537e518f7276ccab11ce01d23cf13f
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="update-the-bank-journal-composite-entity"></a>Oppdatere sammensatt enhet for bankjournal

[!include[banner](../includes/banner.md)]


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






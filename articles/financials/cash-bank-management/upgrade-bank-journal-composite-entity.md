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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a8b11df3b21f8d97986d934ff3c65931aa7ee0c6
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

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






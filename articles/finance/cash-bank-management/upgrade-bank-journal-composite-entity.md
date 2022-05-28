---
title: Oppdatere sammensatt enhet for bankjournal
description: Dette emnet viser fremgangsmåten som kreves for å legge til tilleggsfeltet BankTransactionType i den sammensatte BankJournalEntity.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 730e6bd10b0cdd1587c915bb9ec8d6a4792435d9
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727265"
---
# <a name="update-the-bank-journal-composite-entity"></a>Oppdatere sammensatt enhet for bankjournal

[!include [banner](../includes/banner.md)]

Dette emnet viser fremgangsmåten som kreves for å legge til tilleggsfeltet BankTransactionType i den sammensatte BankJournalEntity.

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

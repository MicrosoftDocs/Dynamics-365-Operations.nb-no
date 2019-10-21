---
title: Avansert bankavstemming MT940-import – oppgradering for sammensatt dataenhet
description: Et serienummer må legges til importenheten for bankkontoutdraget for å støtte MT940-formatet.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88eb5b3c408d36620ab550b29d2e5a3278d25d8a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188470"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Avansert bankavstemming MT940-import – oppgradering for sammensatt dataenhet

[!include [banner](../includes/banner.md)]

Et serienummer må legges til importenheten for bankkontoutdraget for å støtte MT940-formatet. 

Bruk fremgangsmåten nedenfor for å legge til importenheten for bankkontoutdrag for å støtte MT940-formatet.

1.  Kompiler og synkroniser følgende:
    -   Sammensatt Entity\\BankStatementImportEntity
    -   Entity\\BankStatementBalanceEntity
    -   Entity\\BankStatementDocumentEntity
    -   Entity\\BankStatementEntity
    -   Entity\\BankStatementLineEntity
    -   Tabeller\\BankStatementStaging

2.  Databehandling\\dataprosjekter.
    1.  Laste inn MT940-importprosjekter
        1.  Endre XSLT.
            -   Klikk **Vis tilordning**.
            -   Klikk **Vis tilordning** på dokumentet for bankkontoutdrag.
            -   Klikk **Transformasjoner**
            -   Slett filen BankReconiliation-to-Composite.xslt.
            -   Legg til den nye versjonen av BankReconiliation-to-Composite.xslt.

        2.  Vise **Serienummer** på **Kildedata**-oppsettet.
            1.  Kildedataformat = XML-element.
            2.  Enhetsnavn = Bankkontoutdrag.
            3.  Last opp datafil = ny versjon SampleBankCompositeEntity.xml.
            4.  Klikk **Ja** for å overskrive den eksisterende filen.
            5.  Klikk **Ja** for å generere en ny tilordning.
            6.  Kontroller at S**equenceNumber** er tilordnet.
                -   Klikk **Vis tilordning** på utdragsenheten.
                -   Kontroller at **SequenceNumber** er tilordnet fra Kilde til Oppsamling.

3.  Importer det nye utdraget.




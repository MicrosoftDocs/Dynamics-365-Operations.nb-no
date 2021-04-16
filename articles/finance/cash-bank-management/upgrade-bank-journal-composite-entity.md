---
title: Oppdatere sammensatt enhet for bankjournal
description: Fremgangsmåten nedenfor kreves for å legge til tilleggsfeltet BankTransactionType i den sammensatte BankJournalEntity.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7e265915cf3f53a8243788b50a9374d521efbbae
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819611"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="b97e4-103">Oppdatere sammensatt enhet for bankjournal</span><span class="sxs-lookup"><span data-stu-id="b97e4-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b97e4-104">Fremgangsmåten nedenfor kreves for å legge til tilleggsfeltet BankTransactionType i den sammensatte BankJournalEntity.</span><span class="sxs-lookup"><span data-stu-id="b97e4-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="b97e4-105">Bruk fremgangsmåten nedenfor for å legge til tilleggsfeltet BankTransactionType i den sammensatte BankJournalEntity.</span><span class="sxs-lookup"><span data-stu-id="b97e4-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="b97e4-106">Kompiler og synkroniser følgende sammensatte enheter for bankjournalen, enheter og oppsamlingstabeller:</span><span class="sxs-lookup"><span data-stu-id="b97e4-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="b97e4-107">Sammensatt Entity\\BankJournalEntity</span><span class="sxs-lookup"><span data-stu-id="b97e4-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="b97e4-108">Entity\\BankJournalHeaderEntity</span><span class="sxs-lookup"><span data-stu-id="b97e4-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="b97e4-109">Entity\\BankJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="b97e4-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="b97e4-110">Table\\BankJournalHeaderStaging</span><span class="sxs-lookup"><span data-stu-id="b97e4-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="b97e4-111">Table\\BankJournalLineStaging</span><span class="sxs-lookup"><span data-stu-id="b97e4-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="b97e4-112">Databehandling\\dataprosjekter</span><span class="sxs-lookup"><span data-stu-id="b97e4-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="b97e4-113">Viser **Banktransaksjon**-typen på **Kildedata**-oppsettet.</span><span class="sxs-lookup"><span data-stu-id="b97e4-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="b97e4-114">Kildedataformat = XML-element</span><span class="sxs-lookup"><span data-stu-id="b97e4-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="b97e4-115">Enhetsnavn = Bankjournal</span><span class="sxs-lookup"><span data-stu-id="b97e4-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="b97e4-116">Last opp datafil = ny versjon SampleBankJournalCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="b97e4-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="b97e4-117">Klikk **Ja** for å overskrive den eksisterende filen.</span><span class="sxs-lookup"><span data-stu-id="b97e4-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="b97e4-118">Klikk **Ja** for å generere tilordningen fra bunnen av.</span><span class="sxs-lookup"><span data-stu-id="b97e4-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="b97e4-119">Kontroller at Banktransaksjon-typen er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="b97e4-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="b97e4-120">Klikk **Vis tilordning** i linjeenhet.</span><span class="sxs-lookup"><span data-stu-id="b97e4-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="b97e4-121">Kontroller at Banktransaksjon-typen er tilordnet fra Kilde til Oppsamling.</span><span class="sxs-lookup"><span data-stu-id="b97e4-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="b97e4-122">Importer det nye utdraget.</span><span class="sxs-lookup"><span data-stu-id="b97e4-122">Import the new statement.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
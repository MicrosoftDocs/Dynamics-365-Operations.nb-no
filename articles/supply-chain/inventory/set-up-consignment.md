---
title: Definere forsendelse
description: Dette emnet forklarer hvordan du konfigurerer operasjoner for innkommende forsendelseslager.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 24500ff46cc77ca8fa59c0c16427d9f05f33a87e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550022"
---
# <a name="set-up-consignment"></a><span data-ttu-id="de3cc-103">Definere forsendelse</span><span class="sxs-lookup"><span data-stu-id="de3cc-103">Set up consignment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de3cc-104">Dette emnet forklarer hvordan du konfigurerer operasjoner for innkommende forsendelseslager.</span><span class="sxs-lookup"><span data-stu-id="de3cc-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="de3cc-105">Forsendeleslager er lager som eies av en leverandør, men lagres på ditt område.</span><span class="sxs-lookup"><span data-stu-id="de3cc-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="de3cc-106">Når du er klar til å forbruke eller bruke lageret, kan du ta over eierskapet for lageret.</span><span class="sxs-lookup"><span data-stu-id="de3cc-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="de3cc-107">Dette emnet beskriver oppsettet for å aktivere forsendelsesprosessene.</span><span class="sxs-lookup"><span data-stu-id="de3cc-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="de3cc-108">Hvis du vil ha mer informasjon om forsendelsesprosesser, kan du se [Forsendelse](consignment.md).</span><span class="sxs-lookup"><span data-stu-id="de3cc-108">For more information about consignment processes, see [Consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="de3cc-109">Beholdningseiere</span><span class="sxs-lookup"><span data-stu-id="de3cc-109">Inventory owners</span></span>
<span data-ttu-id="de3cc-110">Hvis du vil registrere fysisk forsendelse for innkommende lager, må du definere en leverandøreier.</span><span class="sxs-lookup"><span data-stu-id="de3cc-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="de3cc-111">Dette gjøres på siden **Lagereier**.</span><span class="sxs-lookup"><span data-stu-id="de3cc-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="de3cc-112">Når du velger en **leverandørkonto**, genereres det standardverdier for feltene **Navn** og **Eier**.</span><span class="sxs-lookup"><span data-stu-id="de3cc-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="de3cc-113">Verdien i **Eier**-feltet vil være synlig for leverandøren, slik at du kanskje vil endre dette hvis dine navn på leverandørkontoer ikke er enkle for eksterne brukere å gjenkjenne.</span><span class="sxs-lookup"><span data-stu-id="de3cc-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="de3cc-114">Det er mulig å redigere **Eier**-feltet, men bare frem til når du lagrer posten **Lagereier**.</span><span class="sxs-lookup"><span data-stu-id="de3cc-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="de3cc-115">**Navn**-feltet fylles ut med navnet på parten som leverandørkontoen som er knyttet til, og dette kan ikke endres.</span><span class="sxs-lookup"><span data-stu-id="de3cc-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="de3cc-116">[![Beholdningseiere](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="de3cc-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="de3cc-117">Sporingsdimensjonsgruppe</span><span class="sxs-lookup"><span data-stu-id="de3cc-117">Tracking dimension group</span></span>
<span data-ttu-id="de3cc-118">Varer som skal brukes i forsendelsesprosesser må være knyttet til en **sporingsdimensjonsgruppe** der **Eier**-dimensjonen er satt til **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="de3cc-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="de3cc-119">Alternativene **Fysisk beholdning** og **Økonomisk lager** er alltid valgt for eierdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="de3cc-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="de3cc-120">**Dekningsplanlegg etter dimensjon** er aldri er valgt.</span><span class="sxs-lookup"><span data-stu-id="de3cc-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="de3cc-121">[![Sporingsdimensjonsgruppe](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="de3cc-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="de3cc-122">Endringsjournal for lagereierskap</span><span class="sxs-lookup"><span data-stu-id="de3cc-122">Inventory ownership change journal</span></span>
<span data-ttu-id="de3cc-123">Journalen **Endring av lagereierskap** brukes til å registrere overføring av eierskap av forsendelseslageret fra leverandøren til den juridiske enheten som forbruker det.</span><span class="sxs-lookup"><span data-stu-id="de3cc-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="de3cc-124">Det må identifiseres med et lagerjournalnavn, på samme måte som en hvilken som helst annen lagerjournal.</span><span class="sxs-lookup"><span data-stu-id="de3cc-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="de3cc-125">Disse navnene opprettes på siden **Navn på lagerjournal**, og **Journaltype** må være satt til **Endring av eierskap**.</span><span class="sxs-lookup"><span data-stu-id="de3cc-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="de3cc-126">[![Endringsjournal for lagereierskap](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="de3cc-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="de3cc-127">Leverandørsamarbeid i forsendelsesprosesser</span><span class="sxs-lookup"><span data-stu-id="de3cc-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="de3cc-128">Hvis leverandørene bruker grensesnittet for leverandørsamarbeid, kan de bruke dette til å overvåke forbruket av beholdningen på området.</span><span class="sxs-lookup"><span data-stu-id="de3cc-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="de3cc-129">Hvis du vil ha mer informasjon om hvordan du definerer leverandører med leverandørsamarbeid, kan du se [Konfigurere sikkerhet for brukere av leverandørsamarbeid](../procurement/configure-security-vendor-portal-users.md).</span><span class="sxs-lookup"><span data-stu-id="de3cc-129">For more information about setting up vendors to use vendor collaboration, see [Configuration of security for vendor collaboration users](../procurement/configure-security-vendor-portal-users.md).</span></span>

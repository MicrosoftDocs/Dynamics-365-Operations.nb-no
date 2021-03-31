---
title: Opprette et anleggsmiddel
description: Dette emnet beskriver hvordan du oppretter en ny anleggsmiddelpost fra listesiden for anleggsmidler.
author: moaamer
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bbbafb1732a9628cb90ad284fce224e3d8172afd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227046"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="415bf-103">Opprette et anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="415bf-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="415bf-104">Dette emnet beskriver hvordan du oppretter en ny anleggsmiddelpost fra listesiden for **anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="415bf-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="415bf-105">Systemet tilordner anleggsmiddelnummeret basert på nummerserien som er tilordnet anleggsmiddelgruppen.</span><span class="sxs-lookup"><span data-stu-id="415bf-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="415bf-106">Hvis du bruker anleggsmiddelmalen til å importere anleggsmidler via Microsoft Excel-tillegget, eller hvis du bruker en annen importjobb, oppretter systemet automatisk anleggsmiddelposter og øker anleggsmiddelnummeret.</span><span class="sxs-lookup"><span data-stu-id="415bf-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="415bf-107">Hvis du vil opprette en anleggsmiddelpost manuelt, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="415bf-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="415bf-108">Gå til **Navigasjonsrute \> Moduler \> Anleggsmidler \> Anleggsmidler \> Anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="415bf-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="415bf-109">I **handlingsruten** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="415bf-109">On the **Action pane**, select **New**.</span></span>
3. <span data-ttu-id="415bf-110">Angi eller velg en verdi i feltet **Anleggsmiddelgruppe**.</span><span class="sxs-lookup"><span data-stu-id="415bf-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="415bf-111">**Nummer**-feltet hentes hvis du har aktivert funksjonaliteten **Automatisk nummerering av anleggsmidler** i **anleggsmiddelparameterne** og **anleggsmiddelgruppen**.</span><span class="sxs-lookup"><span data-stu-id="415bf-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="415bf-112">Hvis ikke må du skrive inn et unikt nummer for å identifisere anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="415bf-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="415bf-113">Angi en verdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="415bf-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="415bf-114">Angi tilleggsinformasjonen som forretningen trenger for dette aktivaet.</span><span class="sxs-lookup"><span data-stu-id="415bf-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="415bf-115">Velg **Tablåer** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="415bf-115">On the **Action pane**, select **Books**.</span></span>
6. <span data-ttu-id="415bf-116">Angi en dato i feltet **Anskaffelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="415bf-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="415bf-117">Angi et tall i feltet **Anskaffelsespris**.</span><span class="sxs-lookup"><span data-stu-id="415bf-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="415bf-118">Angi tilleggsinformasjonen som forretningen trenger for dette tablået.</span><span class="sxs-lookup"><span data-stu-id="415bf-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="415bf-119">Angi tilleggsinformasjonen som forretningen trenger for de gjenværende tablåene.</span><span class="sxs-lookup"><span data-stu-id="415bf-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="415bf-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="415bf-120">Close the page.</span></span>

<span data-ttu-id="415bf-121">Du kan også importere anleggsmidler ved hjelp av Excel-tillegget eller ved å kjøre en importjobb fra arbeidsområdet **Dataadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="415bf-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="415bf-122">Før du kjører importen, må du angi verdiene for de nødvendige feltene i malen.</span><span class="sxs-lookup"><span data-stu-id="415bf-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="415bf-123">Hvis du ikke har definert anleggsmiddelnummeret i malen for Excel-tillegget, eller i databehandling, oppretter systemet et anleggsmiddelnummer for hvert importerte anleggsmiddel, og øker automatisk nummerserien for hver.</span><span class="sxs-lookup"><span data-stu-id="415bf-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="415bf-124">Hvis du imidlertid importerer anleggsmidler og definerer anleggsmiddelnumre i malen, vil **ikke** systemet automatisk øke nummerserien.</span><span class="sxs-lookup"><span data-stu-id="415bf-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="415bf-125">I dette tilfellet kan det hende at en administrator må oppdatere nummerserien manuelt.</span><span class="sxs-lookup"><span data-stu-id="415bf-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="415bf-126">Hvis du har definert anleggsmiddelnummeret i malen for Excel-tillegget, bruker systemet det definerte anleggsmiddelnummeret og øker nummerserien.</span><span class="sxs-lookup"><span data-stu-id="415bf-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="415bf-127">Når avskrivningen er postert, låses feltene **Tatt i bruk** og **Startdato for avskrivning** på **Tablå**-siden.</span><span class="sxs-lookup"><span data-stu-id="415bf-127">After posting the depreciation, the **Placed in service** and **Depreciation run date** fields will be locked on the **Book** page.</span></span> <span data-ttu-id="415bf-128">Begge eller ingen av feltene blir i tillegg oppdatert fra dataenheten.</span><span class="sxs-lookup"><span data-stu-id="415bf-128">Also, both neither field will be updated from the data entity.</span></span>

> [!WARNING]
> <span data-ttu-id="415bf-129">Anleggsmiddelposten blir ikke slettet hvis transaksjonene ble postert i det tilknyttede tablået, eller hvis det nylig opprettede anleggsmidlet angis på en journallinje, men ikke posteres.</span><span class="sxs-lookup"><span data-stu-id="415bf-129">The fixed asset record won't be deleted if transactions were posted to the associated book, or if the newly created fixed asset is entered on a journal line but not posted.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
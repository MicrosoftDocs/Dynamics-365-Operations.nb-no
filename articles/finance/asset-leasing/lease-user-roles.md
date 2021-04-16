---
title: Tilordne leiebrukerroller
description: Dette emnet beskriver sikkerhetsrollene som brukes i aktivaleie. Det forklarer også hvordan du tilordner brukere til disse rollene.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 16719576dde73f096c0102a89c43cbc75594cc80
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819848"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="06391-104">Tilordne leiebrukerroller</span><span class="sxs-lookup"><span data-stu-id="06391-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06391-105">Dette emnet beskriver sikkerhetsrollene som brukes i aktivaleie.</span><span class="sxs-lookup"><span data-stu-id="06391-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="06391-106">Det forklarer også hvordan du tilordner brukere til disse rollene.</span><span class="sxs-lookup"><span data-stu-id="06391-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="06391-107">Tre brukerroller skiller adgang til aktivaleie.</span><span class="sxs-lookup"><span data-stu-id="06391-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="06391-108">Én rolle er velegnet til vedlikehold av leieavtaler, én er velegnet for visning av leieavtaler, og én er velegnet for å utføre leieassistentoppgaver.</span><span class="sxs-lookup"><span data-stu-id="06391-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="06391-109">Hver rolle har bestemte tillatelser for alle leiesider, og hver av dem gir brukere muligheten til å vise, opprette, redigere eller slette leieavtaler, i henhold til deres jobbplikter.</span><span class="sxs-lookup"><span data-stu-id="06391-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="06391-110">Rolle</span><span class="sxs-lookup"><span data-stu-id="06391-110">Role</span></span>           | <span data-ttu-id="06391-111">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="06391-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="06391-112">Vedlikeholde leieavtale</span><span class="sxs-lookup"><span data-stu-id="06391-112">Maintain Lease</span></span> | <span data-ttu-id="06391-113">Brukere i denne rollen kan legge til, redigere, slette og vise leieavtaler.</span><span class="sxs-lookup"><span data-stu-id="06391-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="06391-114">Denne rollen er utformet for daglige brukere som har oppgaver som omfatter oppretting og postering av månedlige journaloppføringer, og tillegging av nye leieavtaler.</span><span class="sxs-lookup"><span data-stu-id="06391-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="06391-115">Denne rollen gir tilgang til alle aktivaleiefunksjoner.</span><span class="sxs-lookup"><span data-stu-id="06391-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="06391-116">Vise leie</span><span class="sxs-lookup"><span data-stu-id="06391-116">View Lease</span></span>     | <span data-ttu-id="06391-117">Brukere i denne rollen kan bare vise leieposter, tidsplaner og kjøre rapporter.</span><span class="sxs-lookup"><span data-stu-id="06391-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="06391-118">De kan ikke opprette nye leieavtaler, redigere eksisterende leieavtaler eller opprette journaloppføringer mot leieavtaler.</span><span class="sxs-lookup"><span data-stu-id="06391-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="06391-119">Rollen er utformet for brukere som bare trenger å vise leieavtaler, leietidsplaner og transaksjonene som skjer mot disse leieavtalene.</span><span class="sxs-lookup"><span data-stu-id="06391-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="06391-120">Leieassistent</span><span class="sxs-lookup"><span data-stu-id="06391-120">Lease Clerk</span></span>    | <span data-ttu-id="06391-121">Brukere i denne rollen kan bare opprette nye leieavtaler.</span><span class="sxs-lookup"><span data-stu-id="06391-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="06391-122">De kan ikke redigere eller slette eksisterende leieavtaler, vise leieplaner eller postere leiejournaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="06391-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="06391-123">Denne rollen er utformet for brukere som arbeider i en dataregistreringskapasitet.</span><span class="sxs-lookup"><span data-stu-id="06391-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="06391-124">Følg disse trinnene for å tilordne brukere til rollene som brukes i aktivaleie.</span><span class="sxs-lookup"><span data-stu-id="06391-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="06391-125">Gå til **Systemadministrasjon \> Sikkerhet \> Tilordne brukere til roller**.</span><span class="sxs-lookup"><span data-stu-id="06391-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="06391-126">Velg rollen **Vedlikehold leieavtale**, **Leieassistent** eller **Vis leie**, og velg deretter **Tilordne/utelate brukere manuelt**.</span><span class="sxs-lookup"><span data-stu-id="06391-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="06391-127">Velg brukeren du vil tilordne til rollen, og velg deretter **Tilordne til rolle**.</span><span class="sxs-lookup"><span data-stu-id="06391-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
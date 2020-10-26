---
title: Sikkerhetsdiagnostikk for oppgaveregistreringer
description: Dette emnet inneholder informasjon om hvordan du analyserer og administrerer krav til sikkerhetstillatelse basert på et oppgaveopptak.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 4aecda7e0d604b70dec58a4f5bb2992fe7e0a5e2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982436"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="07f08-103">Sikkerhetsdiagnostikk for oppgaveregistreringer</span><span class="sxs-lookup"><span data-stu-id="07f08-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="07f08-104">Før du begynner</span><span class="sxs-lookup"><span data-stu-id="07f08-104">Before you begin</span></span>

<span data-ttu-id="07f08-105">Dette emnet inneholder informasjon om hvordan du analyserer og administrerer krav til sikkerhetstillatelse basert på et oppgaveopptak.</span><span class="sxs-lookup"><span data-stu-id="07f08-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="07f08-106">Før du fullfører trinnene i dette emnet må du ha en oppgaveregistrering for forretningsprosessen du vil analysere.</span><span class="sxs-lookup"><span data-stu-id="07f08-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="07f08-107">Hvis du vil registrere en forretningsprosess, se [Ressurser for Oppgaveregistrering](../../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="07f08-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="07f08-108">Behandle sikkerhet for et oppgaveopptak</span><span class="sxs-lookup"><span data-stu-id="07f08-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="07f08-109">Gå til **Systemadministrasjon** > **Sikkerhet** > **Sikkerhetsdiagnostikk for oppgaveopptak** .</span><span class="sxs-lookup"><span data-stu-id="07f08-109">Go to **System administration** > **Security** > **Security diagnostic for task recording** .</span></span>
2. <span data-ttu-id="07f08-110">Åpne oppgaveopptaket fra plasseringen.</span><span class="sxs-lookup"><span data-stu-id="07f08-110">Open the task recording from its location.</span></span> <span data-ttu-id="07f08-111">Velg **Åpne fra denne PC-en** eller **Åpne fra Lifecycle Services** , og velg deretter **Lukk** .</span><span class="sxs-lookup"><span data-stu-id="07f08-111">Select **Open from this PC** or **Open from Lifecycle Services** , and then select **Close** .</span></span>
3. <span data-ttu-id="07f08-112">Dette vil åpne siden for **elementdetaljer for sikkerhetsmeny** som viser sikkerhetsobjektene som kreves for prosessen.</span><span class="sxs-lookup"><span data-stu-id="07f08-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="07f08-113">Menyelementene **Handling** og **Utdata** er ikke inkludert i listen.</span><span class="sxs-lookup"><span data-stu-id="07f08-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="07f08-114">Velg en bruker i feltet **Bruker-ID** .</span><span class="sxs-lookup"><span data-stu-id="07f08-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="07f08-115">Hvis brukeren ikke har tillatelser for noen menyelementer, vil feltet **Manglende tillatelser** oppdateres til **Ja** .</span><span class="sxs-lookup"><span data-stu-id="07f08-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes** .</span></span>
  
  ![Side for elementdetaljer for sikkerhetsmeny](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="07f08-117">Velg **Legg til referanse** for å vise en liste over sikkerhetsobjektene, inkludert roller, plikter og rettigheter, som gir den manglende tillatelsen.</span><span class="sxs-lookup"><span data-stu-id="07f08-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="07f08-118">Velg et sikkerhetsobjekt fra listen:</span><span class="sxs-lookup"><span data-stu-id="07f08-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="07f08-119">Hvis **Rolle** er valgt, velger du **Legg til rolle for bruker** .</span><span class="sxs-lookup"><span data-stu-id="07f08-119">If **Role** is selected, select **Add role to user** .</span></span> <span data-ttu-id="07f08-120">Dette vil åpne siden **Tilordne brukere til roller** .</span><span class="sxs-lookup"><span data-stu-id="07f08-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="07f08-121">Hvis du vil ha mer informasjon, kan du se siden [Tilordne brukere til sikkerhetsroller](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="07f08-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="07f08-122">Hvis **Plikt** er valgt, velger du **Legg til plikt i rollen** , velger rollene som plikten skal legges til, og velg deretter **OK** .</span><span class="sxs-lookup"><span data-stu-id="07f08-122">If **Duty** is selected, select **Add duty to role** , select the roles that the duty should be added to, and then select **OK** .</span></span>
    - <span data-ttu-id="07f08-123">Hvis **Rettighet** er valgt, velger du **Legg til rettighet i plikter** , velger rollene som plikten skal legges til, og velg deretter **OK** .</span><span class="sxs-lookup"><span data-stu-id="07f08-123">If **Privilege** is selected, select **Add privilege to duties** , select the roles that the duty should be added to, and then select **OK** .</span></span>

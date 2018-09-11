--- 
title: Aktiver brukere for mottak av arbeidsflytrelaterte e-postmeldinger
description: "Du kan konfigurere systemet slik at det sendes e-postmeldinger til brukere når det oppstår arbeidsflytrelaterte hendelser."
author: jasongre
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 2ddad87b42915ddbd1632c805d6e57a67b6e9638
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2018

---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="48f53-103">Aktiver brukere for mottak av arbeidsflytrelaterte e-postmeldinger</span><span class="sxs-lookup"><span data-stu-id="48f53-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48f53-104">Du kan konfigurere systemet slik at det sendes e-postmeldinger til brukere når det oppstår arbeidsflytrelaterte hendelser.</span><span class="sxs-lookup"><span data-stu-id="48f53-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="48f53-105">E-postmeldinger kan for eksempel sendes til brukere når dokumentene er tilordnet til dem for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="48f53-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="48f53-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="48f53-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="48f53-107">Gå til Systemadministrasjon > Brukere > Brukere.</span><span class="sxs-lookup"><span data-stu-id="48f53-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="48f53-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="48f53-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="48f53-109">Klikk Brukeralternativer.</span><span class="sxs-lookup"><span data-stu-id="48f53-109">Click User options.</span></span>
4. <span data-ttu-id="48f53-110">Klikk Arbeidsflyt-kategorien.</span><span class="sxs-lookup"><span data-stu-id="48f53-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="48f53-111">Kontroller at delen Varslinger er utvidet.</span><span class="sxs-lookup"><span data-stu-id="48f53-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="48f53-112">I delen Varslinger kan du angi hvordan du vil at brukeren skal varsles om arbeidsflytrelaterte hendelser.</span><span class="sxs-lookup"><span data-stu-id="48f53-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="48f53-113">Velg et alternativ i feltet Varslingstype for arbeidsflyt for linjeelement.</span><span class="sxs-lookup"><span data-stu-id="48f53-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="48f53-114">Gruppert – Varslinger for linjeelementer grupperes i en enkelt e-postmelding.</span><span class="sxs-lookup"><span data-stu-id="48f53-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="48f53-115">Enkeltvis – En e-postmelding sendes for hvert linjeelement.</span><span class="sxs-lookup"><span data-stu-id="48f53-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="48f53-116">Hvis du vil at brukeren skal motta varslinger i klienten, merker du av for Send varslinger i e-post.</span><span class="sxs-lookup"><span data-stu-id="48f53-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="48f53-117">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="48f53-117">Click Save.</span></span>
7. <span data-ttu-id="48f53-118">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="48f53-118">Close the page.</span></span>



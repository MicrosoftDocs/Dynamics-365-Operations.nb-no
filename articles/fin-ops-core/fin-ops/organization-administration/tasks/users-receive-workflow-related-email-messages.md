---
title: Aktiver brukere for mottak av arbeidsflytrelaterte e-postmeldinger
description: Du kan konfigurere systemet slik at det sendes e-postmeldinger til brukere når det oppstår arbeidsflytrelaterte hendelser.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4c9f2f22bc4b5ca5b4351f7956ad2eb6d3b903d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140427"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="f1368-103">Aktiver brukere for mottak av arbeidsflytrelaterte e-postmeldinger</span><span class="sxs-lookup"><span data-stu-id="f1368-103">Enable users to receive workflow-related email messages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1368-104">Du kan konfigurere systemet slik at det sendes e-postmeldinger til brukere når det oppstår arbeidsflytrelaterte hendelser.</span><span class="sxs-lookup"><span data-stu-id="f1368-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="f1368-105">E-postmeldinger kan for eksempel sendes til brukere når dokumentene er tilordnet til dem for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="f1368-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="f1368-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="f1368-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="f1368-107">Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Brukere > Brukere**.</span><span class="sxs-lookup"><span data-stu-id="f1368-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="f1368-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f1368-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f1368-109">Klikk på **Brukeralternativer** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="f1368-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="f1368-110">Klikk på kategorien **Arbeidsflyt**. Kontroller at **Varslinger**-delen er utvidet.</span><span class="sxs-lookup"><span data-stu-id="f1368-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="f1368-111">I delen **Varslinger** kan du angi hvordan du vil at brukeren skal varsles om arbeidsflytrelaterte hendelser.</span><span class="sxs-lookup"><span data-stu-id="f1368-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="f1368-112">Velg et alternativ i feltet **Varslingstype for arbeidsflyt for linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="f1368-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="f1368-113">Gruppert – Varslinger for linjeelementer grupperes i en enkelt e-postmelding.</span><span class="sxs-lookup"><span data-stu-id="f1368-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="f1368-114">Enkeltvis – En e-postmelding sendes for hvert linjeelement.</span><span class="sxs-lookup"><span data-stu-id="f1368-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="f1368-115">Hvis du vil at brukeren skal motta varslinger i klienten, merker du av for **Send varslinger i e-post**.</span><span class="sxs-lookup"><span data-stu-id="f1368-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="f1368-116">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f1368-116">Click **Save**.</span></span>
7. <span data-ttu-id="f1368-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f1368-117">Close the page.</span></span>


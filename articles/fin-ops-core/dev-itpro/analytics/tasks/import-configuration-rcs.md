---
title: (ER) Importere konfigurasjoner fra RCS
description: Dette emnet inneholder informasjon om hvordan en bruker kan importere en ny versjon av en ER-konfigurasjon fra RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea2bfd2514be666d05165410ca27041a86464715
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143229"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="daa56-103">(ER) Importere konfigurasjoner fra RCS</span><span class="sxs-lookup"><span data-stu-id="daa56-103">(ER) Import configurations from RCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="daa56-104">De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan importere en ny versjon av en ER-konfigurasjon (elektronisk rapportering) fra Microsoft Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="daa56-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="daa56-105">I dette eksemplet skal du velge versjonen av ER-konfigurasjonen som er konfigurert i en RCS-forekomst, og importere den til gjeldende forekomst for eksempelfirma, Litware, Inc. Disse trinnene kan utføres i alle firmaer fordi ER-konfigurasjoner deles mellom firmaer.</span><span class="sxs-lookup"><span data-stu-id="daa56-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="daa56-106">For å fullføre disse trinnene må du først fullføre trinnene i emnet [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="daa56-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="daa56-107">For å kunne fullføre disse trinnene må du også ha tilgang til en RCS-forekomst som inneholder minst én ER-konfigurasjon med statusen **Fullført** eller **Delt**.</span><span class="sxs-lookup"><span data-stu-id="daa56-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="daa56-108">Gå til **Organisasjonsstyring** > **Arbeidsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="daa56-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="daa56-109">Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="daa56-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="daa56-110">Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i emnet [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="daa56-110">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="daa56-111">Hvis du ikke har noe RCS-miljø klargjort for firmaet, klikker du på den eksterne koblingen **Regulatory Services – Configuration** og følger instruksjonene for å klargjøre et RCS-miljø.</span><span class="sxs-lookup"><span data-stu-id="daa56-111">If you have no RCS environment provisioned to your company, click **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="daa56-112">Klikk på **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="daa56-112">Click **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="daa56-113">Klikk på **RCS**-fanen.</span><span class="sxs-lookup"><span data-stu-id="daa56-113">Click the **RCS** tab.</span></span> 
6. <span data-ttu-id="daa56-114">Hvis RCS-miljøet allerede er klargjort for firmaet ditt, kan du bruke URL-adressene på siden til å få tilgang til det.</span><span class="sxs-lookup"><span data-stu-id="daa56-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="daa56-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="daa56-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="daa56-116">Registrere et nytt ER-repositorium.</span><span class="sxs-lookup"><span data-stu-id="daa56-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="daa56-117">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="daa56-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="daa56-118">Velg leverandøren Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="daa56-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="daa56-119">Klikk Repositorier.</span><span class="sxs-lookup"><span data-stu-id="daa56-119">Click Repositories.</span></span> 
4. <span data-ttu-id="daa56-120">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="daa56-120">Click Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="daa56-121">Angi RCS i feltet Type konfigurasjonsrepositorium.</span><span class="sxs-lookup"><span data-stu-id="daa56-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="daa56-122">Klikk Opprett repositorium.</span><span class="sxs-lookup"><span data-stu-id="daa56-122">Click Create repository.</span></span> 
7. <span data-ttu-id="daa56-123">Angi eller velg en verdi i feltet for visningsnavn på RCS-miljø.</span><span class="sxs-lookup"><span data-stu-id="daa56-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="daa56-124">Velg ønsket RCS-forekomst.</span><span class="sxs-lookup"><span data-stu-id="daa56-124">Select the desired RCS instance.</span></span> <span data-ttu-id="daa56-125">Legg merke til at du kan ha flere av dem.</span><span class="sxs-lookup"><span data-stu-id="daa56-125">Note that you can have several of them.</span></span> 
9. <span data-ttu-id="daa56-126">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="daa56-126">Click OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="daa56-127">Importere ER-konfigurasjoner fra RCS-basert repositorium</span><span class="sxs-lookup"><span data-stu-id="daa56-127">Import ER configurations from RCS based repository</span></span>
1. <span data-ttu-id="daa56-128">Klikk på **Vis filtre**.</span><span class="sxs-lookup"><span data-stu-id="daa56-128">Click **Show filters**.</span></span> 
2. <span data-ttu-id="daa56-129">Angi filterverdien «RCS» i **Navn**-feltet ved hjelp av filteroperatoren **begynner med**.</span><span class="sxs-lookup"><span data-stu-id="daa56-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="daa56-130">Når du åpner det valgte repositoriet, klikker du på koblingen **Klikk her for å koble til Regulatory Configuration Service** på siden **Koble til Regulatory Configuration Services**.</span><span class="sxs-lookup"><span data-stu-id="daa56-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, click **Click here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="daa56-131">Klikk på **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="daa56-131">Click **Open**.</span></span> 
5. <span data-ttu-id="daa56-132">Klikk **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="daa56-132">Click **Close**.</span></span> 
6. <span data-ttu-id="daa56-133">Velg ønsket versjon av ER-konfigurasjon, og klikk på **Importer** for å hente den inn i gjeldende forekomst.</span><span class="sxs-lookup"><span data-stu-id="daa56-133">Select the desired version of ER configuration and click **Import** to bring it in the current instance.</span></span>


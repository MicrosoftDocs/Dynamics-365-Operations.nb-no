---
title: Konfigurere sikkerhet for SQL Server Reporting Services for lokale distribusjoner
description: Dette emnet inneholder informasjon om hvordan du konfigurerer SQL Server Reporting Services (SSRS) for en lokal distribusjon.
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: bb6e8a55c9bee4e60c3a627409d2fbe3b8915196
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174242"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a><span data-ttu-id="a7c57-103">Konfigurere sikkerhet for SQL Server Reporting Services for lokale distribusjoner</span><span class="sxs-lookup"><span data-stu-id="a7c57-103">Configure SQL Server Reporting Services for on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7c57-104">Bruk fremgangsmåten i dette emnet til å konfigurere SQL Server Reporting Services (SSRS) for din distribusjon av Microsoft Dynamics 365 Finance + Operations (lokal).</span><span class="sxs-lookup"><span data-stu-id="a7c57-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 Finance + Operations (on-premises) deployment.</span></span>

1. <span data-ttu-id="a7c57-105">Åpne programmet Reporting Services Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a7c57-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="a7c57-106">Lar standardnavnet **Servernavn** være, som skal være navnet på gjeldende datamaskin, og **Rapportserverforekomst**, **MSSQLSERVER**.</span><span class="sxs-lookup"><span data-stu-id="a7c57-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span>
3. <span data-ttu-id="a7c57-107">Klikk **Koble til**.</span><span class="sxs-lookup"><span data-stu-id="a7c57-107">Click **Connect**.</span></span>

    <span data-ttu-id="a7c57-108">[![Tilkobling til konfigurasjon av rapporteringstjenester](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="a7c57-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>

4. <span data-ttu-id="a7c57-109">Klikk kategorien **Tjenestekonto** og kontroller at innstillingene samsvarer med grafikken nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a7c57-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="a7c57-110">[![Kategorien Tjenestekonto](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="a7c57-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>

5. <span data-ttu-id="a7c57-111">Klikk kategorien **URL for webtjeneste** og kontroller at innstillingene samsvarer med grafikken nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a7c57-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="a7c57-112">[![Kategorien URL for webtjeneste](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="a7c57-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span>

6. <span data-ttu-id="a7c57-113">Klikk kategorien **Database** og kontroller at **Databasenavn** og **Legitimasjonsinnstillinger** samsvarer med grafikken nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a7c57-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a7c57-114">Du må opprette en ny database.</span><span class="sxs-lookup"><span data-stu-id="a7c57-114">You will need to create a new database.</span></span> <span data-ttu-id="a7c57-115">Dette gjør du ved å klikke **Endre Database** og deretter kontrollere at det nye databasenavnet er: **DynamicsAxReportServer**.</span><span class="sxs-lookup"><span data-stu-id="a7c57-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="a7c57-116">[![Kategorien Database](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="a7c57-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>

7. <span data-ttu-id="a7c57-117">Klikk kategorien **URL for webportal** og kontroller at innstillingene samsvarer med grafikken nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a7c57-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a7c57-118">Du må klikke **Bruk** for å opprette og konfigurere portalen.</span><span class="sxs-lookup"><span data-stu-id="a7c57-118">You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="a7c57-119">[![Kategorien URL for webportal](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="a7c57-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>

    <span data-ttu-id="a7c57-120">Når portalen er konfigurert, vil kategorien **Webportal** samsvarer med grafikken nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a7c57-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>

    <span data-ttu-id="a7c57-121">[![Kategorien webportal](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="a7c57-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>

8. <span data-ttu-id="a7c57-122">Klikk URL-adressene for rapportene for å vise SQL Server Reporting Services-webportalen.</span><span class="sxs-lookup"><span data-stu-id="a7c57-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span>
9. <span data-ttu-id="a7c57-123">Når du er i portalenområdet, oppretter du en ny mappe kalt **Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="a7c57-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="a7c57-124">[![Dynamics-mappe](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="a7c57-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>

10. <span data-ttu-id="a7c57-125">I **Reporting Services Configuration Manager** klikker du kategorien **E-postinnstillinger** og kontrollerer at innstillingene samsvarer med grafikken nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a7c57-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="a7c57-126">[![Kategorien E-postinnstillinger](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="a7c57-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>

11. <span data-ttu-id="a7c57-127">Klikk kategorien **Utførelseskonto** og kontroller at innstillingene samsvarer med grafikken nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a7c57-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="a7c57-128">[![Kategorien Utførelseskonto](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="a7c57-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>

    <span data-ttu-id="a7c57-129">Ikke endre standardinnstillingene i kategorien **Krypteringsnøkler**.</span><span class="sxs-lookup"><span data-stu-id="a7c57-129">Don't change the default settings on the **Encryption Keys** tab.</span></span>

    <span data-ttu-id="a7c57-130">[![Kategorien Krypteringsnøkler](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="a7c57-130">[![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>

12. <span data-ttu-id="a7c57-131">Klikk kategorien **Abonnementinnstillinger** og kontroller at innstillingene samsvarer med grafikken nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a7c57-131">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="a7c57-132">[![Kategorien Abonnementinnstillinger](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="a7c57-132">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>

    <span data-ttu-id="a7c57-133">Ikke endre standardinnstillingene i kategorien **Skaler ut distribusjon**.</span><span class="sxs-lookup"><span data-stu-id="a7c57-133">Don't change the default settings on the **Scale-out Deployment** tab.</span></span>

    <span data-ttu-id="a7c57-134">[![Kategorien Skaler ut distribusjon](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="a7c57-134">[![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>

    <span data-ttu-id="a7c57-135">Ikke endre standardinnstillingene i kategorien **Power BI-integrering**.</span><span class="sxs-lookup"><span data-stu-id="a7c57-135">Don't change the default settings on the **Power BI Integration** tab.</span></span>

    <span data-ttu-id="a7c57-136">[![Kategorien Power BI-integrering](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="a7c57-136">[![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span>

13. <span data-ttu-id="a7c57-137">Klikk **Avslutt** for å lukke **Reporting Services Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="a7c57-137">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="a7c57-138">[![Lukke Rreporting Services Configuration Manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="a7c57-138">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>

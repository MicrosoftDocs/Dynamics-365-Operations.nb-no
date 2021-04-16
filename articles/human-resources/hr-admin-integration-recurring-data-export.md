---
title: Opprette en app for gjentakende dataeksport
description: Denne artikkelen viser hvordan du oppretter en logisk Microsoft Azure-app som eksporterer data fra Microsoft Dynamics 365 Human Resources etter en gjentakende tidsplan.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3d7fc01906a017d4214d4794097a11b4a3416b95
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801125"
---
# <a name="create-a-recurring-data-export-app"></a><span data-ttu-id="a84d1-103">Opprette en app for gjentakende dataeksport</span><span class="sxs-lookup"><span data-stu-id="a84d1-103">Create a recurring data export app</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a84d1-104">Denne artikkelen viser hvordan du oppretter en logisk Microsoft Azure-app som eksporterer data fra Microsoft Dynamics 365 Human Resources etter en gjentakende tidsplan.</span><span class="sxs-lookup"><span data-stu-id="a84d1-104">This article shows how to create a Microsoft Azure logic app that exports data from Microsoft Dynamics 365 Human Resources on a recurring schedule.</span></span> <span data-ttu-id="a84d1-105">Opplæringsprogrammet drar nytte av REST-API for DMF-pakke i Human Resources for å eksportere dataene.</span><span class="sxs-lookup"><span data-stu-id="a84d1-105">The tutorial takes advantage of Human Resources' DMF package REST application programming interface (API) to export the data.</span></span> <span data-ttu-id="a84d1-106">Når dataene er eksportert, lagrer den logiske appen den eksporterte datapakken i en Microsoft OneDrive for Business-mappe.</span><span class="sxs-lookup"><span data-stu-id="a84d1-106">After the data has been exported, the logic app saves the exported data package to a Microsoft OneDrive for Business folder.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="a84d1-107">Forretningsscenario</span><span class="sxs-lookup"><span data-stu-id="a84d1-107">Business scenario</span></span>

<span data-ttu-id="a84d1-108">I et typisk forretningsscenario for Microsoft Dynamics 365-integreringer må data eksporteres til et nedstrøms system etter en regelmessig tidsplan.</span><span class="sxs-lookup"><span data-stu-id="a84d1-108">In one typical business scenario for Microsoft Dynamics 365 integrations, data must be exported to a downstream system on a recurring schedule.</span></span> <span data-ttu-id="a84d1-109">Denne opplæringen viser hvordan du eksporterer alle arbeiderposter fra Microsoft Dynamics 365 Human Resources og lagrer listen over arbeidere i en OneDrive for Business-mappe.</span><span class="sxs-lookup"><span data-stu-id="a84d1-109">This tutorial shows how to export all worker records from Microsoft Dynamics 365 Human Resources and save the list of workers in a OneDrive for Business folder.</span></span>

> [!TIP]
> <span data-ttu-id="a84d1-110">De spesifikke dataene som eksporteres i denne opplæringen og målet for de eksporterte dataene, er bare eksempler.</span><span class="sxs-lookup"><span data-stu-id="a84d1-110">The specific data that is exported in this tutorial and the destination of the exported data are only examples.</span></span> <span data-ttu-id="a84d1-111">Du kan enkelt endre dem slik at de oppfyller dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="a84d1-111">You can easily change them to meet your business needs.</span></span>

## <a name="technologies-used"></a><span data-ttu-id="a84d1-112">Teknologier som brukes</span><span class="sxs-lookup"><span data-stu-id="a84d1-112">Technologies used</span></span>

<span data-ttu-id="a84d1-113">Denne opplæringen bruker følgende teknologier:</span><span class="sxs-lookup"><span data-stu-id="a84d1-113">This tutorial uses the following technologies:</span></span>

- <span data-ttu-id="a84d1-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – Hoveddatakilden for arbeidere som skal eksporteres.</span><span class="sxs-lookup"><span data-stu-id="a84d1-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – The master data source for workers that will be exported.</span></span>
- <span data-ttu-id="a84d1-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – Teknologien som sørger for orkestrering og planlegging av den gjentakende eksporten.</span><span class="sxs-lookup"><span data-stu-id="a84d1-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – The technology that provides orchestration and scheduling of the recurring export.</span></span>

    - <span data-ttu-id="a84d1-116">**[Kontakter](https://docs.microsoft.com/azure/connectors/apis-list)** – Teknologien som brukes til å koble den logiske appen til de nødvendige endepunktene.</span><span class="sxs-lookup"><span data-stu-id="a84d1-116">**[Connectors](https://docs.microsoft.com/azure/connectors/apis-list)** – The technology that is used to connect the logic app to the required endpoints.</span></span>

        - <span data-ttu-id="a84d1-117">[HTTP med Azure AD](https://docs.microsoft.com/connectors/webcontents/)-kontakt</span><span class="sxs-lookup"><span data-stu-id="a84d1-117">[HTTP with Azure AD](https://docs.microsoft.com/connectors/webcontents/) connector</span></span>
        - <span data-ttu-id="a84d1-118">[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)-kontakt</span><span class="sxs-lookup"><span data-stu-id="a84d1-118">[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector</span></span>

- <span data-ttu-id="a84d1-119">**[REST-API for DMF-pakke](../dev-itpro/data-entities/data-management-api.md)** – Teknologien som brukes til å utløse eksporten og overvåke fremdriften.</span><span class="sxs-lookup"><span data-stu-id="a84d1-119">**[DMF package REST API](../dev-itpro/data-entities/data-management-api.md)** – The technology that is used to trigger the export and monitor its progress.</span></span>
- <span data-ttu-id="a84d1-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – Målet for de eksporterte arbeiderne.</span><span class="sxs-lookup"><span data-stu-id="a84d1-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – The destination for the exported workers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a84d1-121">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="a84d1-121">Prerequisites</span></span>

<span data-ttu-id="a84d1-122">Før du begynner øvelsen i denne opplæringen, må du ha følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="a84d1-122">Before you begin the exercise in this tutorial, you must have the following items:</span></span>

- <span data-ttu-id="a84d1-123">Et Human Resources-miljø med tillatelser på administratornivå i miljøet</span><span class="sxs-lookup"><span data-stu-id="a84d1-123">A Human Resources environment that has admin-level permissions in the environment</span></span>
- <span data-ttu-id="a84d1-124">Et [Azure-abonnement](https://azure.microsoft.com/free/) for å være vert for den logiske appen</span><span class="sxs-lookup"><span data-stu-id="a84d1-124">An [Azure subscription](https://azure.microsoft.com/free/) to host the logic app</span></span>

## <a name="the-exercise"></a><span data-ttu-id="a84d1-125">Øvelsen</span><span class="sxs-lookup"><span data-stu-id="a84d1-125">The exercise</span></span>

<span data-ttu-id="a84d1-126">På slutten av denne øvelsen vil du ha en logisk app som er koblet til Human Resources-miljøet og OneDrive for Business-kontoen din.</span><span class="sxs-lookup"><span data-stu-id="a84d1-126">At the end of this exercise, you will have a logic app that is connected to your Human Resources environment and your OneDrive for Business account.</span></span> <span data-ttu-id="a84d1-127">Den logiske appen eksporterer en datapakke fra Human Resources, venter på at eksporten skal fullføres, laster ned den eksporterte datapakken og lagrer datapakken i OneDrive for Business-mappen du har angitt.</span><span class="sxs-lookup"><span data-stu-id="a84d1-127">The logic app will export a data package from Human Resources, wait for the export to be completed, download the exported data package, and save the data package in the OneDrive for Business folder that you specified.</span></span>

<span data-ttu-id="a84d1-128">Den fullførte logiske appen ligner på den følgende illustrasjonen.</span><span class="sxs-lookup"><span data-stu-id="a84d1-128">The completed logic app will resemble the following illustration.</span></span>

![Oversikt over logisk app](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a><span data-ttu-id="a84d1-130">Trinn 1: Opprette et dataeksportprosjekt i Human Resources</span><span class="sxs-lookup"><span data-stu-id="a84d1-130">Step 1: Create a data export project in Human Resources</span></span>

<span data-ttu-id="a84d1-131">I Human Resources oppretter du et dataeksportprosjekt som eksporterer arbeidere.</span><span class="sxs-lookup"><span data-stu-id="a84d1-131">In Human Resources, create a data export project that exports workers.</span></span> <span data-ttu-id="a84d1-132">Gi prosjektet navnet **Eksporter arbeidere**, og kontroller at alternativet **Generer data pakke** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a84d1-132">Name the project **Export Workers**, and make sure that the **Generate data package** option is set to **Yes**.</span></span> <span data-ttu-id="a84d1-133">Legg til en enkelt enhet (**arbeider**) i prosjektet, og velg formatet du vil eksportere i.</span><span class="sxs-lookup"><span data-stu-id="a84d1-133">Add a single entity (**Worker**) to the project, and select the format to export in.</span></span> <span data-ttu-id="a84d1-134">(Microsoft Excel-formatet brukes i denne opplæringen.)</span><span class="sxs-lookup"><span data-stu-id="a84d1-134">(Microsoft Excel format is used in this tutorial.)</span></span>

![Dataprosjektet Eksporter arbeidere](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> <span data-ttu-id="a84d1-136">Husk navnet på dataeksportprosjektet.</span><span class="sxs-lookup"><span data-stu-id="a84d1-136">Remember the name of the data export project.</span></span> <span data-ttu-id="a84d1-137">Du kommer til å trenge det når du oppretter den logiske appen i neste trinn.</span><span class="sxs-lookup"><span data-stu-id="a84d1-137">You will need it when you create the logic app in the next step.</span></span>

### <a name="step-2-create-the-logic-app"></a><span data-ttu-id="a84d1-138">Trinn 2: Opprette den logiske appen</span><span class="sxs-lookup"><span data-stu-id="a84d1-138">Step 2: Create the logic app</span></span>

<span data-ttu-id="a84d1-139">Mesteparten av øvelsen omfatter oppretting av den logiske appen.</span><span class="sxs-lookup"><span data-stu-id="a84d1-139">The bulk of the exercise involves creating the logic app.</span></span>

1. <span data-ttu-id="a84d1-140">Opprett en logisk app i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="a84d1-140">In the Azure portal, create a logic app.</span></span>

    ![Side for å opprette logisk app](media/integration-logic-app-creation-1.png)

2. <span data-ttu-id="a84d1-142">Start med en tom logisk app i Logic Apps Designer.</span><span class="sxs-lookup"><span data-stu-id="a84d1-142">In the Logic Apps Designer, start with a blank logic app.</span></span>
3. <span data-ttu-id="a84d1-143">Legg til en [utløser for gjentakelsesplan](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) for å kjøre appen hvert døgn (eller etter en plan du velger selv).</span><span class="sxs-lookup"><span data-stu-id="a84d1-143">Add a [Recurrence Schedule trigger](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) to run the logic app every 24 hours (or according to a schedule of your choice).</span></span>

    ![Dialogboks for gjentakelse](media/integration-logic-app-recurrence-step.png)

4. <span data-ttu-id="a84d1-145">Kall DMF REST-API-en [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) for å planlegge eksporten av datapakken.</span><span class="sxs-lookup"><span data-stu-id="a84d1-145">Call the [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API to schedule the export of your data package.</span></span>

    1. <span data-ttu-id="a84d1-146">Bruk handlingen **Aktiver en HTTP-forespørsel** fra HTTP med Azure AD-kontakten.</span><span class="sxs-lookup"><span data-stu-id="a84d1-146">Use the **Invoke an HTTP request** action from the HTTP with Azure AD connector.</span></span>

        - <span data-ttu-id="a84d1-147">**URL-adresse for basisressurs:** URL-adressen til Human Resources-miljøet (ikke inkluder informasjon om bane/navneområde)</span><span class="sxs-lookup"><span data-stu-id="a84d1-147">**Base Resource URL:** The URL of your Human Resources environment (Don't include path/namespace information.)</span></span>
        - <span data-ttu-id="a84d1-148">**URI for Azure AD-ressurs:** `http://hr.talent.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="a84d1-148">**Azure AD Resource URI:** `http://hr.talent.dynamics.com`</span></span>

        > [!NOTE]
        > <span data-ttu-id="a84d1-149">Human Resources-tjenesten har enda ikke en kontakt som viser alle API-ene som utgjør REST-API-en for DMF-pakke, for eksempel **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="a84d1-149">The Human Resources service doesn't yet provide a connector that exposes all the APIs that make up the DMF package REST API, such as **ExportToPackage**.</span></span> <span data-ttu-id="a84d1-150">Du må i stedet kalle API-ene ved å bruke rå HTTPS-forespørsler via HTTP med Azure AD-koblingen.</span><span class="sxs-lookup"><span data-stu-id="a84d1-150">Instead, you must call the APIs by using raw HTTPS requests through the HTTP with Azure AD connector.</span></span> <span data-ttu-id="a84d1-151">Denne koblingen bruker Azure Active Directory (Azure AD) for godkjenning og autorisasjon til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a84d1-151">This connector uses Azure Active Directory (Azure AD) for authentication and authorization to Human Resources.</span></span>

        ![HTTP med Azure AD-kontakt](media/integration-logic-app-http-aad-connector-step.png)

    2. <span data-ttu-id="a84d1-153">Logg deg på Human Resources-miljøet via HTTP med Azure AD-kontakten.</span><span class="sxs-lookup"><span data-stu-id="a84d1-153">Sign in to your Human Resources environment through the HTTP with Azure AD connector.</span></span>
    3. <span data-ttu-id="a84d1-154">Konfigurer en HTTP **POST**-forespørsel for å kalle DMF REST-API-en **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="a84d1-154">Set up an HTTP **POST** request to call the **ExportToPackage** DMF REST API.</span></span>

        - <span data-ttu-id="a84d1-155">**Metode:** POST</span><span class="sxs-lookup"><span data-stu-id="a84d1-155">**Method:** POST</span></span>
        - <span data-ttu-id="a84d1-156">**URL-adresse til forespørselen:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="a84d1-156">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span></span>
        - <span data-ttu-id="a84d1-157">**Teksten i forespørselen:**</span><span class="sxs-lookup"><span data-stu-id="a84d1-157">**Body of the request:**</span></span>

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Aktivere en HTTP-forespørselshandling](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > <span data-ttu-id="a84d1-159">Du vil kanskje gi nytt navn til hvert trinn, slik at det blir mer meningsfylt enn standardnavnet, **Aktiver en HTTP-forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="a84d1-159">You might want to rename each step so that it's more meaningful than the default name, **Invoke an HTTP request**.</span></span> <span data-ttu-id="a84d1-160">Du kan for eksempel endre navnet på dette trinnet til **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="a84d1-160">For example, you can rename this step **ExportToPackage**.</span></span>

5. <span data-ttu-id="a84d1-161">[Initialiser en variabel](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) for å lagre kjørestatusen til **ExportToPackage**-forespørselen.</span><span class="sxs-lookup"><span data-stu-id="a84d1-161">[Initialize a variable](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) to store the execution status of the **ExportToPackage** request.</span></span>

    ![Handlingen Initialiser variabel](media/integration-logic-app-initialize-variable-step.png)

6. <span data-ttu-id="a84d1-163">Vent til kjørestatusen for dataeksporten er **Vellykket**.</span><span class="sxs-lookup"><span data-stu-id="a84d1-163">Wait until the execution status of the data export is **Succeeded**.</span></span>

    1. <span data-ttu-id="a84d1-164">Legg til en [Til-løkke](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) som gjentas til verdien av **ExecutionStatus**-variabelen er **Vellykket**.</span><span class="sxs-lookup"><span data-stu-id="a84d1-164">Add an [Until loop](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) that repeats until the value of the **ExecutionStatus** variable is **Succeeded**.</span></span>
    2. <span data-ttu-id="a84d1-165">Legg til en **Forsinkelse**-handling som venter fem sekunder før den spør etter gjeldende kjørestatus for eksporten.</span><span class="sxs-lookup"><span data-stu-id="a84d1-165">Add a **Delay** action that waits five seconds before it polls for the current execution status of the export.</span></span>

        ![Beholder for Til-løkke](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > <span data-ttu-id="a84d1-167">Sett grenseantallet til **15** for å vente i maksimalt 75 sekunder (15 gjentakelser x 5 sekunder) for at eksporten skal fullføres.</span><span class="sxs-lookup"><span data-stu-id="a84d1-167">Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="a84d1-168">Hvis eksporten tar mer tid, justerer du grenseantallet etter behov.</span><span class="sxs-lookup"><span data-stu-id="a84d1-168">If your export takes more time, adjust the limit count as appropriate.</span></span>        

    3. <span data-ttu-id="a84d1-169">Legg til handlinge **Aktiver HTTP-forespørsel** for å kalle DMF REST-API-en [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus), og sett variabelen **ExecutionStatus** til resultatet av **GetExecutionSummaryStatus**-svaret.</span><span class="sxs-lookup"><span data-stu-id="a84d1-169">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>

        > <span data-ttu-id="a84d1-170">Dette eksemplet sjekker ikke for feil.</span><span class="sxs-lookup"><span data-stu-id="a84d1-170">This sample doesn't do error checking.</span></span> <span data-ttu-id="a84d1-171">API-en **GetExecutionSummaryStatus** kan returnere ikke-vellykkede sluttilstander (det vil si andre tilstander enn **Vellykket**).</span><span class="sxs-lookup"><span data-stu-id="a84d1-171">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="a84d1-172">Hvis du vil ha mer informasjon, kan du se i [API-dokumentasjonen](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span><span class="sxs-lookup"><span data-stu-id="a84d1-172">For more information, see the [API documentation](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

        - <span data-ttu-id="a84d1-173">**Metode:** POST</span><span class="sxs-lookup"><span data-stu-id="a84d1-173">**Method:** POST</span></span>
        - <span data-ttu-id="a84d1-174">**URL-adresse til forespørselen:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="a84d1-174">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span></span>
        - <span data-ttu-id="a84d1-175">**Teksten i forespørselen:** body('Invoke\_an\_HTTP\_request')?['value']</span><span class="sxs-lookup"><span data-stu-id="a84d1-175">**Body of the request:** body('Invoke\_an\_HTTP\_request')?['value']</span></span>

            > [!NOTE]
            > <span data-ttu-id="a84d1-176">Du må kanskje angi verdien for **Teksten i forespørselen:** enten i kodevisning eller i funksjonsredigeringsprogrammet i utformingen.</span><span class="sxs-lookup"><span data-stu-id="a84d1-176">You might have to enter the **Body of the request** value either in code view or in the function editor in the designer.</span></span>

        ![Aktivere en HTTP-forespørselshandling 2](media/integration-logic-app-get-execution-status-step.png)

        ![Angi variabelhandling](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > <span data-ttu-id="a84d1-179">Verdien for handlingen **Angi variabel** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) er forskjellig fra verdien for teksten **Aktivere en HTTP-forespørsel 2**, selv om verdiene vises på samme måte i utformingen.</span><span class="sxs-lookup"><span data-stu-id="a84d1-179">The value for the **Set variable** action (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) will differ from the value for the **Invoke an HTTP request 2** body value, even though the designer will show the values in the same way.</span></span>

7. <span data-ttu-id="a84d1-180">Få tak i URL-adressen for nedlasting av den eksporterte pakken.</span><span class="sxs-lookup"><span data-stu-id="a84d1-180">Get the download URL of the exported package.</span></span>

    - <span data-ttu-id="a84d1-181">Legg til hendelsen **Aktiver HTTP-forespørsel** for å kalle DMF REST-API-en [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl).</span><span class="sxs-lookup"><span data-stu-id="a84d1-181">Add an **Invoke HTTP request** action to call the [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span></span>

        - <span data-ttu-id="a84d1-182">**Metode:** POST</span><span class="sxs-lookup"><span data-stu-id="a84d1-182">**Method:** POST</span></span>
        - <span data-ttu-id="a84d1-183">**URL-adresse til forespørselen:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="a84d1-183">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span></span>
        - <span data-ttu-id="a84d1-184">**Teksten i forespørselen:** {"executionId": body('GetExportedPackageURL')?['value']}</span><span class="sxs-lookup"><span data-stu-id="a84d1-184">**Body of the request:** {"executionId": body('GetExportedPackageURL')?['value']}</span></span>

        ![GetExportedPackageURL-handlingen](media/integration-logic-app-get-exported-package-step.png)

8. <span data-ttu-id="a84d1-186">Last ned den eksporterte pakken.</span><span class="sxs-lookup"><span data-stu-id="a84d1-186">Download the exported package.</span></span>

    - <span data-ttu-id="a84d1-187">Legg til en HTTP **GET**-forespørsel (en innebygd [HTTP-koblingshandling](https://docs.microsoft.com/azure/connectors/connectors-native-http)) for å laste ned pakken fra URL-adressen som ble returnert i forrige trinn.</span><span class="sxs-lookup"><span data-stu-id="a84d1-187">Add an HTTP **GET** request (a built-in [HTTP connector action](https://docs.microsoft.com/azure/connectors/connectors-native-http)) to download the package from the URL that was returned in the previous step.</span></span>

        - <span data-ttu-id="a84d1-188">**Metode:** GET</span><span class="sxs-lookup"><span data-stu-id="a84d1-188">**Method:** GET</span></span>
        - <span data-ttu-id="a84d1-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span><span class="sxs-lookup"><span data-stu-id="a84d1-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="a84d1-190">Du må kanskje angi verdien for **URI** enten i kodevisning eller i funksjonsredigeringsprogrammet i utformingen.</span><span class="sxs-lookup"><span data-stu-id="a84d1-190">You might have to enter the **URI** value either in code view or in the function editor in the designer.</span></span>

        ![HTTP GET-handling](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > <span data-ttu-id="a84d1-192">Denne forespørselen krever ingen ekstra godkjenning fordi URL-adressen som API-en **GetExportedPackageUrl** returnerer, inneholder et token for delte tilgangssignaturer som gir tilgang til å laste ned filen.</span><span class="sxs-lookup"><span data-stu-id="a84d1-192">This request doesn't require any additional authentication, because the URL that the **GetExportedPackageUrl** API returns includes a shared access signatures token that grants access to download the file.</span></span>

9. <span data-ttu-id="a84d1-193">Lagre den nedlastede pakken ved hjelp av [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)-koblingen.</span><span class="sxs-lookup"><span data-stu-id="a84d1-193">Save the downloaded package by using the [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector.</span></span>

    - <span data-ttu-id="a84d1-194">Legg til en OneDrive for Business-handling [Opprett fil](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file).</span><span class="sxs-lookup"><span data-stu-id="a84d1-194">Add a OneDrive for Business [Create File](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) action.</span></span>
    - <span data-ttu-id="a84d1-195">Koble til OneDrive for Business-kontoen etter behov.</span><span class="sxs-lookup"><span data-stu-id="a84d1-195">Connect to your OneDrive for Business account, as required.</span></span>

        - <span data-ttu-id="a84d1-196">**Mappebane:** En mappe du velger</span><span class="sxs-lookup"><span data-stu-id="a84d1-196">**Folder Path:** A folder of your choice</span></span>
        - <span data-ttu-id="a84d1-197">**Filenavn:** worker\_package.zip</span><span class="sxs-lookup"><span data-stu-id="a84d1-197">**File Name:** worker\_package.zip</span></span>
        - <span data-ttu-id="a84d1-198">**Filinnhold:** Teksten fra forrige trinn (dynamisk innhold)</span><span class="sxs-lookup"><span data-stu-id="a84d1-198">**File Content:** The body from the previous step (dynamic content)</span></span>

        ![Opprett fil-handling](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a><span data-ttu-id="a84d1-200">Trinn 3: Teste den logiske appen</span><span class="sxs-lookup"><span data-stu-id="a84d1-200">Step 3: Test the logic app</span></span>

<span data-ttu-id="a84d1-201">Hvis du vil teste den logiske appen, velger du **Kjør**-knappen i utformingsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="a84d1-201">To test your logic app, select the **Run** button in the designer.</span></span> <span data-ttu-id="a84d1-202">Du ser at trinnene i den logiske appen begynner å kjøre.</span><span class="sxs-lookup"><span data-stu-id="a84d1-202">You will see that the steps of the logic app start to run.</span></span> <span data-ttu-id="a84d1-203">Etter 30 til 40 sekunder, skal den logiske appen slutte å kjøre, og OneDrive for Business-mappen skal inneholde en ny pakkefil som inneholder de eksporterte arbeiderne.</span><span class="sxs-lookup"><span data-stu-id="a84d1-203">After 30 to 40 seconds, the logic app should finish running, and your OneDrive for Business folder should include a new package file that contains the exported workers.</span></span>

<span data-ttu-id="a84d1-204">Hvis det rapporteres en feil i et hvilket som helst trinn, velger du det mislykkede trinnet i utformingen og undersøker feltene **Inndata** og **Utdata** for den.</span><span class="sxs-lookup"><span data-stu-id="a84d1-204">If a failure is reported for any step, select the failed step in the designer, and examine the **Inputs** and **Outputs** fields for it.</span></span> <span data-ttu-id="a84d1-205">Feilsøk og rett opp trinnet etter behov for å korrigere feilene.</span><span class="sxs-lookup"><span data-stu-id="a84d1-205">Debug and adjust the step as required to correct the errors.</span></span>

<span data-ttu-id="a84d1-206">Illustrasjonen nedenfor viser hvordan Logic Apps Designer ser ut når alle trinnene i den logiske appen er kjørt vellykket.</span><span class="sxs-lookup"><span data-stu-id="a84d1-206">The following illustration shows what the Logic Apps Designer looks like when all the steps of the logic app run successfully.</span></span>

![Vellykket kjøring av logisk app](media/integration-logic-app-successful-run.png)

## <a name="summary"></a><span data-ttu-id="a84d1-208">Sammendrag</span><span class="sxs-lookup"><span data-stu-id="a84d1-208">Summary</span></span>

<span data-ttu-id="a84d1-209">I denne opplæringen lærte du hvordan du bruker en logisk app til å eksportere data fra Human Resources og lagre de eksporterte dataene i en OneDrive for Business-mappe.</span><span class="sxs-lookup"><span data-stu-id="a84d1-209">In this tutorial, you learned how to use a logic app to export data from Human Resources and save the exported data to a OneDrive for Business folder.</span></span> <span data-ttu-id="a84d1-210">Du kan endre trinnene i denne opplæringen etter behov for å dekke dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="a84d1-210">You can modify the steps of this tutorial as required to suit your business needs.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
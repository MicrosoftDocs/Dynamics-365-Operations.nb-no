---
title: Importere data fra Excel-dataenhetsmaler med flere regneark
description: Dette emnet beskriver hvordan du importerer data ved hjelp av Excel-dataenhetsmaler for Microsoft Dynamics 365 for Finance and Operations.
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: cfaf17a8279026bf9bc8b581afd07e4fdbd3f03a
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="excel-templates-with-multiple-worksheets"></a><span data-ttu-id="333d9-103">Excel-maler med flere regneark</span><span class="sxs-lookup"><span data-stu-id="333d9-103">Excel templates with multiple worksheets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="333d9-104">Databehandling i Microsoft Dynamics 365 for Finance and Operations støtter Microsoft Excel-baserte maler for dataenheter.</span><span class="sxs-lookup"><span data-stu-id="333d9-104">Data management in Microsoft Dynamics 365 for Finance and Operations supports Microsoft Excel-based templates for data entities.</span></span> <span data-ttu-id="333d9-105">Disse malene kan inneholde ett eller flere regneark.</span><span class="sxs-lookup"><span data-stu-id="333d9-105">These templates can contain one or more worksheets.</span></span> <span data-ttu-id="333d9-106">Maler med flere regneark brukes ofte når det passer å behandle data i en enkelt fil og importere den til flere dataenheter.</span><span class="sxs-lookup"><span data-stu-id="333d9-106">Templates with multiple worksheets are often used when it is convenient to manage data in a single file and import it to multiple data entities.</span></span> <span data-ttu-id="333d9-107">Et eksempel er områder og lagre.</span><span class="sxs-lookup"><span data-stu-id="333d9-107">An example would be sites and warehouses.</span></span>

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a><span data-ttu-id="333d9-108">Laste opp en fil én gang og tilordne den til alle enheter</span><span class="sxs-lookup"><span data-stu-id="333d9-108">Upload a file once and map it to all entities</span></span>
<span data-ttu-id="333d9-109">La oss et eksempel der det er én Excel-fil med regneark som heter **Områder** og **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="333d9-109">Let’s take an example where there is one Excel file with worksheets called **Sites** and **Warehouses**.</span></span> <span data-ttu-id="333d9-110">For å definere dataimportprosjektet ville du lagt til den første dataenheten, **Områder**, og deretter lastet opp filen.</span><span class="sxs-lookup"><span data-stu-id="333d9-110">To set up the data import project, you would add the first data entity, **Sites** and then upload the file.</span></span> <span data-ttu-id="333d9-111">Du vil kunne velge **Områder** som regnearket som skal brukes for denne enheten.</span><span class="sxs-lookup"><span data-stu-id="333d9-111">You will be able to select **Sites** as the worksheet to be used for this entity.</span></span>

<span data-ttu-id="333d9-112">Hvis du legger til den andre enheten, **Lagre**, uten å forlate **Legg til fil**-skjemaet, vil regnearkoppslaget la deg velge **Lagre**-regnearket uten at du må laste opp filen på nytt.</span><span class="sxs-lookup"><span data-stu-id="333d9-112">If you add the second entity **Warehouses** without leaving the **Add file** form, the worksheet lookup will let you select the **Warehouses** worksheet without having to upload the file again.</span></span> <span data-ttu-id="333d9-113">Den eneste grunnen til å laste opp en ny fil ville være hvis **Lagre**-dataene var i en annen fil.</span><span class="sxs-lookup"><span data-stu-id="333d9-113">The only reason to upload a new file would be if the **Warehouses** data was in a different file.</span></span>

![Flere regneark](./media/AddFileMultipleWorkSheets.png) 

## <a name="fix-worksheet-to-entity-mapping"></a><span data-ttu-id="333d9-115">Ordne tilordning av regneark til enhet</span><span class="sxs-lookup"><span data-stu-id="333d9-115">Fix worksheet to entity mapping</span></span>

<span data-ttu-id="333d9-116">Tilordningen av regnearket til en dataenhet i importjobben kan ordnes fra rutenettet.</span><span class="sxs-lookup"><span data-stu-id="333d9-116">The mapping of the worksheet to a data entity in the import job can be fixed from the grid.</span></span> <span data-ttu-id="333d9-117">**Regneark**-kolonnen i rutenettet viser regnearkene fra filen som ble tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="333d9-117">The **Worksheet** column in the grid shows the worksheets from the file that was mapped.</span></span> <span data-ttu-id="333d9-118">Du kan velge et annet regneark fra rullegardinlistemenyen.</span><span class="sxs-lookup"><span data-stu-id="333d9-118">You can choose a different worksheet from the drop-down menu.</span></span> <span data-ttu-id="333d9-119">Hvis det valgte regnearket allerede er tilordnet en enhet i dataprosjektet, ber systemet deg om å bekrefte endringen.</span><span class="sxs-lookup"><span data-stu-id="333d9-119">If the chosen worksheet is already mapped to an entity in the data project, the system asks you to confirm the change.</span></span> <span data-ttu-id="333d9-120">Vi anbefaler at du order alle tilordninger i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="333d9-120">We recommend that you fix all mappings in the grid.</span></span>

![Oppdatere regnearktilordning](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a><span data-ttu-id="333d9-122">Tilordne på nytt til en ny fil</span><span class="sxs-lookup"><span data-stu-id="333d9-122">Re-map to a new file</span></span>

<span data-ttu-id="333d9-123">I tilfeller der en ny versjon av samme fil eller en helt ny fil må lastes opp for eksisterende enheter i et dataprosjekt, må du bruke **Legg til fil**, og legge til enheter på nytt som om de ble lagt til for første gang.</span><span class="sxs-lookup"><span data-stu-id="333d9-123">In cases where a new version of the same file or a completely new file must be uploaded for existing entities in a data project, you must use the **Add file** experience, and add the entities again as if they were being added for the first time.</span></span> <span data-ttu-id="333d9-124">Systemet vil bekrefte at du vil overskrive eksisterende enheter i dataprosjektet før du fortsetter.</span><span class="sxs-lookup"><span data-stu-id="333d9-124">The system will confirm that you want to overwrite the existing entities in the data project before proceeding.</span></span> <span data-ttu-id="333d9-125">Enheter som ikke legges til på nytt (eller overskrives), vil fortsatt inneholde de tidligere tilordningene fra den forrige filen.</span><span class="sxs-lookup"><span data-stu-id="333d9-125">Entities that are not added again (or overwritten) will continue to hold the previous mappings from the previous file.</span></span>

## <a name="upload-a-file-using-run-project"></a><span data-ttu-id="333d9-126">Laste opp en fil ved hjelp av Kjør prosjekt</span><span class="sxs-lookup"><span data-stu-id="333d9-126">Upload a file using Run project</span></span>

<span data-ttu-id="333d9-127">Du kan laste opp en Excel-fil når du bruker **Kjør prosjekt**-alternativet for å kjøre et importprosjekt.</span><span class="sxs-lookup"><span data-stu-id="333d9-127">You can upload an Excel file while using the **Run project** option to execute an import project.</span></span> <span data-ttu-id="333d9-128">Du må være forsiktig og bare laste opp filer som har de samme regnearkene som de eksisterende tilordningene på dataenhetene i dataprosjektet.</span><span class="sxs-lookup"><span data-stu-id="333d9-128">You must be careful to upload only files that have the same worksheets as the existing mappings on the data entities in the data project.</span></span> <span data-ttu-id="333d9-129">Hvis et regneark ikke finnes i den nylig opplastede filen, vises en feilmelding og importen stoppes.</span><span class="sxs-lookup"><span data-stu-id="333d9-129">If a worksheet is not found in the newly uploaded file, the system displays an error and will stop the import.</span></span> <span data-ttu-id="333d9-130">Hvis tilordningen til regnearket må endres for en enhet, må tilordningene i dataprosjektet først oppdateres fra dataprosjektet før du kan bruke filen i **Kjør prosjekt**-opplevelsen.</span><span class="sxs-lookup"><span data-stu-id="333d9-130">If the mapping to the worksheet must be changed for an entity, then the mappings in the data project must be first updated from within the data project before using the file in the **Run project** experience.</span></span>



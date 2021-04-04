---
title: Nytt dokumentbrukergrensesnitt i forretningsdokumentbehandling
description: Dette emnet inneholder informasjon om hvordan du bruker det nye dokumentbrukergrensesnittet i funksjonen for administrasjon av forretningsdokument for elektronisk rapportering.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7f8099f2f6872c34c30de918a6fc5fd27bcde958
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565716"
---
# <a name="new-document-user-interface-in-business-document-management"></a><span data-ttu-id="b0763-103">Nytt dokumentbrukergrensesnitt i Forretningsdokumentbehandling</span><span class="sxs-lookup"><span data-stu-id="b0763-103">New document user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0763-104">Med forretningsdokumentadministrering kan forretningsbrukere redigere forretningsdokumentmaler ved å bruke en Microsoft 365-tjeneste eller den aktuelle Microsoft Office-skrivebordsapplikasjonen.</span><span class="sxs-lookup"><span data-stu-id="b0763-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="b0763-105">Redigeringer kan inneholde utformingsendringer eller nye distribusjoner, eller brukere kan legge til plassholdere for å inkludere ytterligere data uten å måtte endre kildekoden.</span><span class="sxs-lookup"><span data-stu-id="b0763-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="b0763-106">Hvis du vil ha mer informasjon om hvordan du arbeider med administrering av forretningsdokumenter, kan du se [Oversikt over administrering av forretningsdokumenter](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="b0763-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="b0763-107">Det nye dokumentbrukergrensesnittet (UI) er tydeligere og mer behagelig å bruke.</span><span class="sxs-lookup"><span data-stu-id="b0763-107">The new document user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="b0763-108">**Forretningsdokument**-området viser bare malene som er tilgjengelige for gjeldende leverandør.</span><span class="sxs-lookup"><span data-stu-id="b0763-108">The **Business document** area shows only the templates that are available for the current provider.</span></span>

<span data-ttu-id="b0763-109">Med **Nytt dokument**-knappen kan brukere opprette og redigere en mal i en formatkonfigurasjon for elektronisk rapportering (ER) som leveres av en annen leverandør.</span><span class="sxs-lookup"><span data-stu-id="b0763-109">The **New document** button lets users create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="b0763-110">I eksemplet i dette emnet er leverandøren Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b0763-110">In the example in this topic, the provider is Microsoft.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="b0763-111">Gjøre det nye dokumentbrukergrensesnittet i forretningsdokumentadministrering tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="b0763-111">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="b0763-112">Hvis du vil begynne å bruke det nye dokumentbrukergrensesnittet i forretningsdokumentadministrering, må du aktivere **Office-lignende brukergrensesnittopplevelse for forretningsdokumentadministrering**-funksjonen i **Funksjonsadministrering**-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="b0763-112">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="b0763-113">Følg disse trinnene for å aktivere denne funksjonen for alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="b0763-113">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="b0763-114">I **Funksjonsadministrering**-arbeidsområdet, i **Ny**-fanen velger du **Office-lignende brukergrensesnittopplevelse for forretningsdokumentadministrering**-funksjonen i listen.</span><span class="sxs-lookup"><span data-stu-id="b0763-114">In the **Feature management** workspace, on the **New** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="b0763-115">Velg **Aktiver nå** for å aktivere den valgte funksjonen.</span><span class="sxs-lookup"><span data-stu-id="b0763-115">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="b0763-116">Oppdater siden for å få tilgang til den nye funksjonen.</span><span class="sxs-lookup"><span data-stu-id="b0763-116">Refresh the page to access the new feature.</span></span>

### <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="b0763-117">Redigere maler som eies av andre leverandører</span><span class="sxs-lookup"><span data-stu-id="b0763-117">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="b0763-118">I **Forretningsdokumentadministrering**-arbeidsområdet velger du **Nytt dokument**.</span><span class="sxs-lookup"><span data-stu-id="b0763-118">In the **Business document management** workspace, select **New document**.</span></span>

    ![Arbeidsområdet Administrasjon av forretningsdokument](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="b0763-120">I dialogboksen velger du dokumentet som skal brukes som mal, og velger deretter **Opprett dokument**.</span><span class="sxs-lookup"><span data-stu-id="b0763-120">In the dialog box, select the document to use as a template, and then select **Create document**.</span></span>

    ![Forretningsdokumenter-dialogboksen](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="b0763-122">I den nye dialogboksen, i **Tittel**-feltet endrer du tittelen etter behov.</span><span class="sxs-lookup"><span data-stu-id="b0763-122">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="b0763-123">Tittelteksten brukes til å navngi den nye ER-formatkonfigurasjonen som opprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="b0763-123">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="b0763-124">Utkastversjonen av denne konfigurasjonen (**Kopi av FTI-kunderapport (GER)**) vil inneholde den redigerte malen og vil bli brukt til å kjøre dette ER-formatet for den gjeldende brukeren.</span><span class="sxs-lookup"><span data-stu-id="b0763-124">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="b0763-125">Den opprinnelige malen fra den grunnleggende ER-formatkonfigurasjonen vil bli brukt til å kjøre dette ER-formatet for alle andre brukere.</span><span class="sxs-lookup"><span data-stu-id="b0763-125">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="b0763-126">I **Navn** -feltet endrer du navnet på den første revisjonen av den redigerbare malen som skal opprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="b0763-126">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="b0763-127">I **Kommentar**-feltet oppdater du merknadene for revisjonen av den redigerbare malen som opprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="b0763-127">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="b0763-128">Velg **OK** for å bekrefte starten på redigeringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="b0763-128">Select **OK** to confirm the start of the editing process.</span></span>

    ![Dokumentopprettelse-dialogboksen](./media/BDM_overview_new_template3.png)

<span data-ttu-id="b0763-130">**Nytt dokument**-knappen brukes til å opprette og redigere en mal i en ER-formatkonfigurasjon som leveres av en annen leverandør.</span><span class="sxs-lookup"><span data-stu-id="b0763-130">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="b0763-131">I dette eksemplet er leverandøren Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b0763-131">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="b0763-132">Når du velger **Nytt dokument**, kan du vise alle malene som eies av gjeldende leverandør og andre leverandører.</span><span class="sxs-lookup"><span data-stu-id="b0763-132">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="b0763-133">Når du har valgt malen, åpnes den for redigering.</span><span class="sxs-lookup"><span data-stu-id="b0763-133">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="b0763-134">Den redigerte malen blir deretter lagret i en ny ER-formatkonfigurasjon som genereres automatisk.</span><span class="sxs-lookup"><span data-stu-id="b0763-134">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

<span data-ttu-id="b0763-135">Hvis du vil ha mer informasjon, kan du se [Oversikt over forretningsdokumentadministrering](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="b0763-135">For more information, see [Business document management overview](er-business-document-management.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
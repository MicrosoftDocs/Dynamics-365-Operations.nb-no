---
title: Legge til datafelt i avgiftskonfigurasjoner
description: Dette emnet beskriver hvordan du tilpasser avgiftskonfigurasjoner ved å legge til datafelt.
author: kailiang
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b9d9fce81151ad70d57c69e389e238a6f9137d56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819430"
---
# <a name="add-data-fields-in-tax-configurations"></a><span data-ttu-id="cbd98-103">Legge til datafelt i avgiftskonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="cbd98-103">Add data fields in tax configurations</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="cbd98-104">Dette emnet beskriver hvordan du tilpasser avgiftskonfigurasjoner ved hjelp av [datafelt som legges til i avgiftsintegrasjon](tax-service-add-data-fields-tax-integration-by-extension.md).</span><span class="sxs-lookup"><span data-stu-id="cbd98-104">This topic explains how to customize tax configurations by using [data fields that are added in the tax integration](tax-service-add-data-fields-tax-integration-by-extension.md).</span></span>

## <a name="customize-the-tax-data-model"></a><span data-ttu-id="cbd98-105">Tilpasse avgiftsdatamodellen</span><span class="sxs-lookup"><span data-stu-id="cbd98-105">Customize the tax data model</span></span>

1. <span data-ttu-id="cbd98-106">I Microsoft Dynamics 365 Finance går du til **Elektronisk rapportering** \> **Avgiftskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="cbd98-106">In Microsoft Dynamics 365 Finance, go to **Electronic Reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="cbd98-107">I konfigurasjonstreet velger du **Avgiftsdatamodell – Europa**.</span><span class="sxs-lookup"><span data-stu-id="cbd98-107">In the configuration tree, select **Tax Data Model - Europe**.</span></span> <span data-ttu-id="cbd98-108">Velg deretter **Opprett konfigurasjon** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="cbd98-108">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="cbd98-109">I rullegardinlisten velger du **Modell for avgiftsbelagte dokumenter utledet fra navnet: Avgiftsdatamobell – Europa, Microsoft**, skriver inn et navn på den nye avgiftsdatamodellen og velger deretter **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="cbd98-109">In the drop-down dialog box, select the **Taxable document model derived from Name: Tax Data Model -- Europe, Microsoft** option, enter a name for the new tax data model, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="cbd98-110">Velg avgiftsdatamodellen du akkurat opprettet, og velg deretter **Utforming** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="cbd98-110">Select the tax data model that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="cbd98-111">Utvid datamodelltreet, velg **Linjer**, og velg deretter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cbd98-111">Expand the data model tree, select **Lines**, and then select **New**.</span></span>
6. <span data-ttu-id="cbd98-112">I dialogboksen **Opprett node** angir du et navn, angir varetypen og velger **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="cbd98-112">In the **Create node** dialog box, enter a name, specify the item type, and then select **Add**.</span></span>
7. <span data-ttu-id="cbd98-113">Legg til eventuelle nødvendige kolonner.</span><span class="sxs-lookup"><span data-stu-id="cbd98-113">Add any required columns.</span></span>
8. <span data-ttu-id="cbd98-114">Velg **Lagre** i handlingsruten , og velg deretter **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="cbd98-114">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="cbd98-115">Lukk siden, og vis den fullførte versjonen av avgiftsdatamodellen.</span><span class="sxs-lookup"><span data-stu-id="cbd98-115">Close the page, and view the completed version of your tax data model.</span></span>

## <a name="customize-the-tax-configuration"></a><span data-ttu-id="cbd98-116">Tilpasse avgiftskonfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="cbd98-116">Customize the tax configuration</span></span>

1. <span data-ttu-id="cbd98-117">I Finance går du til **Elektronisk rapportering** \> **Avgiftskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="cbd98-117">In Finance, go to **Electronic reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="cbd98-118">I konfigurasjonstreet velger du **Avgiftskonfigurasjon – Europa**.</span><span class="sxs-lookup"><span data-stu-id="cbd98-118">In the configuration tree, select **Tax Configuration -- Europe**.</span></span> <span data-ttu-id="cbd98-119">Velg deretter **Opprett konfigurasjon** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="cbd98-119">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="cbd98-120">I rullegardinlisten velger du **Konfigurasjon av avgiftstjeneste utledet fra navnet: Avgiftskonfigurasjon – Europa, Microsoft**, skriver inn et navn på den nye avgiftskonfigurasjonen og velger deretter **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="cbd98-120">In the drop-down dialog box, select the **Tax service configuration derived from Name: Tax Configuration -- Europe, Microsoft** option, enter a name for the new tax configuration, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="cbd98-121">Velg avgiftskonfigurasjonen du akkurat opprettet, og velg deretter **Utforming** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="cbd98-121">Select the tax configuration that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="cbd98-122">I **Egenskaper**-delen i **Datamodell**-feltet velger du den tilpassede avgiftsdatamodellen du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="cbd98-122">In the **Properties** section, in the **Data model** field, select the customized tax data model that you created earlier.</span></span>
6. <span data-ttu-id="cbd98-123">I feltet **Datamodellversjon** velger du den fullførte versjonen av avgiftsdatamodellen.</span><span class="sxs-lookup"><span data-stu-id="cbd98-123">In the **Data model version** field, select the completed version of the tax data model.</span></span>
7. <span data-ttu-id="cbd98-124">Velg **Legg til**, og legg til de nødvendige avgiftsmålene.</span><span class="sxs-lookup"><span data-stu-id="cbd98-124">Select **Add**, and add the required tax measures.</span></span>
8. <span data-ttu-id="cbd98-125">Velg **Lagre** i handlingsruten , og velg deretter **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="cbd98-125">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="cbd98-126">Lukk siden, og vis den fullførte versjonen av avgiftskonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="cbd98-126">Close page, and view the completed version of your tax configuration.</span></span>

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a><span data-ttu-id="cbd98-127">Implementere avgiftsfunksjoner i den tilpassede avgiftskonfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="cbd98-127">Implement tax features in the customized tax configuration</span></span>

1. <span data-ttu-id="cbd98-128">I Regulatory Configuration Service (RCS) går du til **Globaliseringsfunksjoner** \> **Avgift**.</span><span class="sxs-lookup"><span data-stu-id="cbd98-128">In Regulatory Configuration Service (RCS), go to **Globalization Features** \> **Tax**.</span></span>
2. <span data-ttu-id="cbd98-129">Velg **Legg til**, angi informasjon om den nye funksjonen, og velg deretter **Opprett funksjon**.</span><span class="sxs-lookup"><span data-stu-id="cbd98-129">Select **Add**, enter information about the new feature, and then select **Create feature**.</span></span>
3. <span data-ttu-id="cbd98-130">Velg funksjonen på **Versjoner**-fanen, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="cbd98-130">On the **Versions** tab, select the feature, and then select **Edit**.</span></span>
4. <span data-ttu-id="cbd98-131">På **Generelt**-fanen i **Konfigurasjonsversjon**-feltet velger du den tilpassede avgiftskonfigurasjonen og versjonen.</span><span class="sxs-lookup"><span data-stu-id="cbd98-131">On the **General** tab, in the **Configuration version** field, select the customized tax configuration and version.</span></span>
5. <span data-ttu-id="cbd98-132">I dialogboksen **Administrer kolonner** velger du overskriften og linjekolonnene du vil inkludere i det tilpassede avgiftsmålet, og deretter velger du pil høyre for å legge dem til i listen **Valgte kolonner**.</span><span class="sxs-lookup"><span data-stu-id="cbd98-132">In the **Manage columns** dialog box, select the header and line columns that you want to include in your customized tax measure, and then select the right arrow button to add them to the **Selected columns** list.</span></span>

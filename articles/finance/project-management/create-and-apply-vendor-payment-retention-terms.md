---
title: Opprette og ta i bruk betingelser for tilbakeholdelse av leverandørbetaling
description: Dette emnet gir informasjon om hvordan du konfigurerer og opprettholder betingelser for tilbakeholdelse av leverandørbetalinger.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410253"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="0fafb-103">Opprette og ta i bruk betingelser for tilbakeholdelse av leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="0fafb-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="0fafb-104">Det er nyttig å definere tilbakeholdelsesbetingelser for leverandørbetalinger for et prosjekt når organisasjonen ønsker å tilbakeholde en del av betalingene til en leverandør.</span><span class="sxs-lookup"><span data-stu-id="0fafb-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="0fafb-105">Dette kan for eksempel være om du vil vente med å betale en leverandør til produktene de leverer, oppfyller forventningene dine.</span><span class="sxs-lookup"><span data-stu-id="0fafb-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="0fafb-106">Betingelser for tilbakeholdelse av leverandørbetalinger kan spesifiseres når du forhandler om en leverandørkontrakt.</span><span class="sxs-lookup"><span data-stu-id="0fafb-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="0fafb-107">Opprett betingelser for tilbakeholdelse av leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="0fafb-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="0fafb-108">Du kan prosenten av en leverandørbetaling som skal holdes tilbake, og prosenten av tidligere tilbakeholdte beløp som skal frigis.</span><span class="sxs-lookup"><span data-stu-id="0fafb-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="0fafb-109">Beløp tilbakeholdes automatisk på leverandørfakturaer til kontrakten når angitt fullføringstilstand.</span><span class="sxs-lookup"><span data-stu-id="0fafb-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="0fafb-110">Når du har definert betingelsene for tilbakeholdelse, kan du bruke dem på alle prosjekter for den aktuelle leverandøren.</span><span class="sxs-lookup"><span data-stu-id="0fafb-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="0fafb-111">Bruk følgende trinn for å konfigurere og vedlikeholde betingelser for tilbakeholdelse av leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="0fafb-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="0fafb-112">Gå til **Prosjektstyring og regnskap** > **Tilbakeholdelse** > **Betingelser for tilbakeholdelse av leverandørbetaling**.</span><span class="sxs-lookup"><span data-stu-id="0fafb-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="0fafb-113">Velg **Ny** for å legge til en ny betingelse for tilbakeholdelse av leverandørbetaling.</span><span class="sxs-lookup"><span data-stu-id="0fafb-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="0fafb-114">Verdien for **Regel-ID** for den nye betingelsen angis automatisk.</span><span class="sxs-lookup"><span data-stu-id="0fafb-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="0fafb-115">Skriv inn en kort beskrivelse i **Beskrivelse**-feltet, gå til **Betingelser**-hurtigkategorien og velg **Legg til linje** for å angi betingelsesverdier for følgende:</span><span class="sxs-lookup"><span data-stu-id="0fafb-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="0fafb-116">**Prosent av leverte enheter**: Angi en fullføringsprosent for betingelsen.</span><span class="sxs-lookup"><span data-stu-id="0fafb-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="0fafb-117">Beløp tilbakeholdes automatisk på leverandørfakturaer til fullføringsstadiet for prosjektet er lik den spesifiserte prosentdelen.</span><span class="sxs-lookup"><span data-stu-id="0fafb-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="0fafb-118">Hvis du for eksempel angir 50,00, tilbakebeholdes beløp til prosjektet er 50 prosent fullført.</span><span class="sxs-lookup"><span data-stu-id="0fafb-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="0fafb-119">**Prosent som skal tilbakeholdes**: Angi prosenten av et leverandørfakturabeløp som skal tilbakeholdes.</span><span class="sxs-lookup"><span data-stu-id="0fafb-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="0fafb-120">Hvis du for eksempel angir 10,00, tilbakeholdes 10 prosent av beløpet på en leverandørfaktura til prosjektet når fullføringsprosenten du valgte i feltet **Prosent av leverte enheter**.</span><span class="sxs-lookup"><span data-stu-id="0fafb-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="0fafb-121">**Prosent som skal frigis**: Velg **Legg til linje** for å angi prosenten av eventuelle tidligere tilbakeholdte beløp som skal frigis på det valgte nivået av prosjektfullføring.</span><span class="sxs-lookup"><span data-stu-id="0fafb-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="0fafb-122">Hvis du har flere milepæler for ulike nivåer av prosjektfullføring, angir du en egen linje med betingelse for tilbakeholdelse av leverandørbetaling for hver enkelt tilbakeholdelsesregel.</span><span class="sxs-lookup"><span data-stu-id="0fafb-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="0fafb-123">Hver linje kan ha en egen prosentdel for tilbakeholdelse, og en egen prosentdel som skal frigis, for hvert angitte nivå av prosjektfullføring.</span><span class="sxs-lookup"><span data-stu-id="0fafb-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="0fafb-124">Når du har definert betingelsene for tilbakeholdelse for en leverandør, kan du bruke dem i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="0fafb-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="0fafb-125">Ta i bruk betingelser for tilbakeholdelse av leverandørbetalinger i et prosjekt</span><span class="sxs-lookup"><span data-stu-id="0fafb-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="0fafb-126">Gå til **Prosjektstyring og regnskap** > **Prosjekter** > **Alle prosjekter**, og åpne et prosjekt fra prosjektlistesiden.</span><span class="sxs-lookup"><span data-stu-id="0fafb-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="0fafb-127">Klikk **Legg til linje** på hurtigfanen **Leverandøravtaler**.</span><span class="sxs-lookup"><span data-stu-id="0fafb-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="0fafb-128">Velg ett av følgende alternativer i **Kontokode**-feltet:</span><span class="sxs-lookup"><span data-stu-id="0fafb-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="0fafb-129">**Tabell**: Betingelsene for tilbakeholdelse av leverandørbetaling gjelder for én leverandør.</span><span class="sxs-lookup"><span data-stu-id="0fafb-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="0fafb-130">**Gruppe**: Betingelsene for tilbakeholdelse av leverandørbetaling gjelder alle leverandører i en leverandørgruppe.</span><span class="sxs-lookup"><span data-stu-id="0fafb-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="0fafb-131">**Alle**: Betingelsene for tilbakeholdelse av leverandørbetaling gjelder alle leverandører.</span><span class="sxs-lookup"><span data-stu-id="0fafb-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="0fafb-132">Velg leverandøren eller leverandørgruppen som betingelsene for tilbakeholdelse av leverandørbetaling gjelder for, i feltet **Leverandør/leverandørgruppe**.</span><span class="sxs-lookup"><span data-stu-id="0fafb-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="0fafb-133">Hvis du valgte **Alle** i forrige trinn, er dette feltet utilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="0fafb-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="0fafb-134">I **Betingelser for tilbakeholdelse for leverandør**-feltet velger du tilbakeholdelsesbetingelsene du opprettet i forrige prosedyre.</span><span class="sxs-lookup"><span data-stu-id="0fafb-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="0fafb-135">Hvis prosjektet også har etterbetalingsvilkår definert for leverandøren, angir du terskelprosenten for prosjektet i feltet **Terskelprosent for etterbetaling**.</span><span class="sxs-lookup"><span data-stu-id="0fafb-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="0fafb-136">Betingelsene for tilbakeholdelse av leverandørbetaling vises også på bestillinger du oppretter for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="0fafb-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>

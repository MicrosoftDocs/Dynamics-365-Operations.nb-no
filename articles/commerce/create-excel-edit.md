---
title: Opprette en Excel-arbeidsbok for å redigere detaljhandelstransaksjoner
description: Dette emnet beskriver hvordan du oppretter en Excel-arbeidsbok, slik at du kan redigere detaljhandelstransaksjoner i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b2b6e98db54e7747912aad26f4b8ae24b9ad5a6d
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/04/2020
ms.locfileid: "4459676"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="19787-103">Opprette en Excel-arbeidsbok for å redigere detaljhandelstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="19787-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19787-104">Dette emnet beskriver hvordan du oppretter en Excel-arbeidsbok, slik at du kan redigere detaljhandelstransaksjoner i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="19787-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="19787-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="19787-105">Overview</span></span>

<span data-ttu-id="19787-106">Det finnes en forhåndsdefinert Excel-mal som kunder kan få tilgang til fra forskjellige deler av systemet, og bruke den til å redigere og kontrollere detaljhandelstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="19787-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="19787-107">Kunder kan imidlertid også opprette en egendefinert Excel-arbeidsbok for dette formålet.</span><span class="sxs-lookup"><span data-stu-id="19787-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="19787-108">Opprette og konfigurere en Excel-arbeidsbok</span><span class="sxs-lookup"><span data-stu-id="19787-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="19787-109">Hvis du vil opprette og konfigurere en Excel-arbeidsbok slik at du kan redigere detaljhandelstransaksjoner, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="19787-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="19787-110">Åpne Excel og opprett en tom arbeidsbok.</span><span class="sxs-lookup"><span data-stu-id="19787-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="19787-111">Velg **Mine tillegg** i kategorien **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="19787-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="19787-112">I ruten til høyre velger du koblingen **Legg til serverinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="19787-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="19787-113">Angi serverens URL-adresse, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="19787-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="19787-114">Hvis du får feil meldingen "Fant ingen appletregistreringer", kan du følge denne fremgangsmåten for å løse problemet:</span><span class="sxs-lookup"><span data-stu-id="19787-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="19787-115">I Commerce kan du gå til **Systemadministrasjon \> Oppsett \> Parametere til Office-app**.</span><span class="sxs-lookup"><span data-stu-id="19787-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="19787-116">Velg **Initialiser app-parametere** i hurtigkategorien **App-parametere**.</span><span class="sxs-lookup"><span data-stu-id="19787-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="19787-117">I bekreftelsesboksen velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="19787-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="19787-118">I hurtigkategorien **Registrerte appleter** velger du **Initialiser appletregistrering**.</span><span class="sxs-lookup"><span data-stu-id="19787-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="19787-119">Gjenta de tre forrige trinnene etter behov.</span><span class="sxs-lookup"><span data-stu-id="19787-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="19787-120">Velg **Utforming**, og velg deretter **Legg til tabell**.</span><span class="sxs-lookup"><span data-stu-id="19787-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="19787-121">Basert på dataene som skal endres, velger du enhetene som må legges til i Excel-arbeidsboken for redigering.</span><span class="sxs-lookup"><span data-stu-id="19787-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="19787-122">Bruk tabellen nedenfor som referanse.</span><span class="sxs-lookup"><span data-stu-id="19787-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="19787-123">Transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="19787-123">Transaction type</span></span> | <span data-ttu-id="19787-124">Dataenheter som skal brukes</span><span class="sxs-lookup"><span data-stu-id="19787-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="19787-125">Hentesalgstransaksjoner, elektroniske ordrer, asynkrone kundeordrer, asynkrone kundetilbud</span><span class="sxs-lookup"><span data-stu-id="19787-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="19787-126">Transaksjon (kan overvåkes), salgstransaksjon (kan overvåkes), betalingstransaksjoner (kan overvåkes), mva-transaksjoner (kan overvåkes), rabattransaksjoner (kan overvåkes), gebyrtransaksjoner (kan overvåkes)</span><span class="sxs-lookup"><span data-stu-id="19787-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="19787-127">Deponering til bank</span><span class="sxs-lookup"><span data-stu-id="19787-127">Bank drop</span></span> | <span data-ttu-id="19787-128">Transaksjon (kan overvåkes), betalingsmiddeltransaksjoner til bank (kan overvåkes)</span><span class="sxs-lookup"><span data-stu-id="19787-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="19787-129">Deponering til safe</span><span class="sxs-lookup"><span data-stu-id="19787-129">Safe drop</span></span> | <span data-ttu-id="19787-130">Transaksjon (kan overvåkes), betalingsmiddeltransaksjoner til safe (kan overvåkes)</span><span class="sxs-lookup"><span data-stu-id="19787-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="19787-131">Kasseoppgjør</span><span class="sxs-lookup"><span data-stu-id="19787-131">Tender declaration</span></span> | <span data-ttu-id="19787-132">Transaksjon (kan overvåkes), kasseoppgjørtransaksjoner (kan overvåkes)</span><span class="sxs-lookup"><span data-stu-id="19787-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="19787-133">Inntekt, utgift</span><span class="sxs-lookup"><span data-stu-id="19787-133">Income, Expense</span></span> | <span data-ttu-id="19787-134">Transaksjon (kan overvåkes), inntekts-/utgiftstransaksjoner (kan overvåkes), betalingstransaksjoner (kan overvåkes)</span><span class="sxs-lookup"><span data-stu-id="19787-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="19787-135">Deklarer startbeløp, fjerning av betalingsmiddel, flytpost, endre betalingsmiddel, fakturabetaling, kundeinnskudd</span><span class="sxs-lookup"><span data-stu-id="19787-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="19787-136">Transaksjon (kan overvåkes), betalingstransaksjoner (kan overvåkes)</span><span class="sxs-lookup"><span data-stu-id="19787-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="19787-137">Det er viktig at du bare legger til én dataenhet i hver Excel-arbeidsbok.</span><span class="sxs-lookup"><span data-stu-id="19787-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="19787-138">I tillegg må alle felt som er merket med et nøkkelsymbol, legges til i den aktuelle arbeidsboken.</span><span class="sxs-lookup"><span data-stu-id="19787-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="19787-139">Når arbeidsboken er konfigurert, bruker du de nødvendige filtrene.</span><span class="sxs-lookup"><span data-stu-id="19787-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="19787-140">Sørg for at du bruker de samme filtrene i alle regnearkene i filen.</span><span class="sxs-lookup"><span data-stu-id="19787-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="19787-141">Unngå å laste inn svært store mengder data i Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="19787-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="19787-142">Ellers kan ytelsen bli påvirket, og Excel og systemet mister kanskje noe av hastigheten.</span><span class="sxs-lookup"><span data-stu-id="19787-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="19787-143">Det anbefales at du alltid bruker "Firma" og "Utdragsnummer" eller "Transaksjonsnummer" som filtre for filen.</span><span class="sxs-lookup"><span data-stu-id="19787-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="19787-144">Når filtrene er konfigurert, velger du **Oppdater** for å laste dataene.</span><span class="sxs-lookup"><span data-stu-id="19787-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="19787-145">Rediger de nødvendige dataene, og publiser dem deretter.</span><span class="sxs-lookup"><span data-stu-id="19787-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="19787-146">Hvis knappen **Publiser** ikke er tilgjengelig, er det sannsynlig at enkelte nøkkelfelt ikke ble lagt til i Excel-arbeidsboken.</span><span class="sxs-lookup"><span data-stu-id="19787-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19787-147">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="19787-147">Additional resources</span></span>

[<span data-ttu-id="19787-148">Redigere og overvåke hentesalgs- og kassastyringstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="19787-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="19787-149">Rediger og overvåk nettordretransaksjoner og asynkrone kundeordretransaksjoner</span><span class="sxs-lookup"><span data-stu-id="19787-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="19787-150">Redigere finansdimensjoner for detaljhandelstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="19787-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="19787-151">Legge til felt i en Excel-arbeidsbok for å redigere detaljhandelstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="19787-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)

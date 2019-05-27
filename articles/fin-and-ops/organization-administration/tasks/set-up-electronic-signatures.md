---
title: Opprette elektroniske signaturer
description: Bruk denne prosedyren for å definere elektroniske signaturer.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eb6bf529b1e94d598e219482f182140402f2928a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545528"
---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="5fdf1-103">Opprette elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="5fdf1-103">Set up electronic signatures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5fdf1-104">Bruk denne prosedyren for å definere elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="5fdf1-105">En elektronisk signatur bekrefter identiteten til en person som er i ferd med å starte eller godkjenne en dataprosess.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="5fdf1-106">Demonstrasjonsdatafirmaet DAT brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="5fdf1-107">Aktivere konfigurasjonsnøkkelen for elektronisk signatur</span><span class="sxs-lookup"><span data-stu-id="5fdf1-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="5fdf1-108">Gå til Systemadministrasjon > Oppsett > Lisenskonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="5fdf1-109">Utvid Administrasjon i treet.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="5fdf1-110">Verifiser at det er merket av for Elektronisk signatur.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="5fdf1-111">Hvis det ikke er merket av for Elektronisk signatur, må du aktivere vedlikeholdsmodus.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="5fdf1-112">Vedlikeholdsmodus kan aktiveres i dette miljøet ved å kjøre en vedlikeholdsjobb fra Lifecycle Services, eller ved hjelp av verktøyet Deployment.Setup lokalt.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="5fdf1-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="5fdf1-114">Definere parametere for elektronisk signatur</span><span class="sxs-lookup"><span data-stu-id="5fdf1-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="5fdf1-115">Gå til Organisasjonsstyring > Oppsett > Elektronisk signatur > Parametere for elektronisk signatur.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="5fdf1-116">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-116">Click Edit.</span></span>
3. <span data-ttu-id="5fdf1-117">Skriv inn en verdi i feltet Varsel.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="5fdf1-118">Angi varselet som signatarer vil motta når det bes om en signatur.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="5fdf1-119">Du kan skrive inn hvilken som helst tekst.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-119">You can enter any text.</span></span> <span data-ttu-id="5fdf1-120">Vanligvis forteller denne teksten brukeren hva det betyr å signere et dokument elektronisk.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="5fdf1-121">Hvis du vil angi varselteksten på flere språk, klikker du knappen Oversettelser.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="5fdf1-122">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-122">Click Save.</span></span>
5. <span data-ttu-id="5fdf1-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="5fdf1-124">Definere årsakskoder for elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="5fdf1-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="5fdf1-125">Gå til Organisasjonsstyring > Oppsett > Elektronisk signatur > Årsakskoder for elektronisk signatur.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="5fdf1-126">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-126">Click New.</span></span>
    * <span data-ttu-id="5fdf1-127">Du må definere årsakskoder før bruk av elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="5fdf1-128">Det kreves en gyldig årsakskode ved signering av et dokument.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="5fdf1-129">En signatar velger en årsakskode for å angi formålet med en elektronisk signatur.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="5fdf1-130">En årsakskode kan for eksempel brukes til å angi juridisk godkjenning.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="5fdf1-131">Skriv inn en verdi i feltet Årsakskode.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="5fdf1-132">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="5fdf1-133">Angi flere årsakskoder, om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="5fdf1-134">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-134">Click Save.</span></span>
6. <span data-ttu-id="5fdf1-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="5fdf1-136">Kreve elektroniske signaturer for eksisterende prosesser</span><span class="sxs-lookup"><span data-stu-id="5fdf1-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="5fdf1-137">Gå til Organisasjonsstyring > Oppsett > Elektronisk signatur > Krav til elektronisk signatur.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="5fdf1-138">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5fdf1-139">Velg en prosess som krever elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="5fdf1-140">Merk av eller fjern merket i avmerkingsboksen Signatur nødvendig.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="5fdf1-141">Gjenta disse trinnene for hver prosess som krever elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="5fdf1-142">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="5fdf1-143">Opprette et egendefinert krav til elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="5fdf1-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="5fdf1-144">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-144">Click New.</span></span>
2. <span data-ttu-id="5fdf1-145">Merk av eller fjern merket i avmerkingsboksen Signatur nødvendig.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="5fdf1-146">I Navn-feltet angir du et navn på prosessen som krever elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="5fdf1-147">Klikk rullegardinknappen i feltet Tabellnavn for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="5fdf1-148">Finn og velg tabellen der dataene må signeres og lagres, i listen.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="5fdf1-149">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="5fdf1-150">Klikk rullegardinknappen i feltet Feltnavn for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="5fdf1-151">Finn og velg feltet i tabellen som du vil overvåke, i listen.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="5fdf1-152">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5fdf1-153">Angi når det kreves en signatur.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-153">Specify when a signature is required.</span></span>     <span data-ttu-id="5fdf1-154">Velg Alltid hvis det kreves en signatur når dataene i feltet endres.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="5fdf1-155">Velg Bare hvis det bare kreves en signatur under bestemte vilkår.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="5fdf1-156">Hvis du velger Bare, må du også velge ett av følgende alternativer: Når en post settes inn, Når en post oppdateres eller Når en post slettes.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="5fdf1-157">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-157">Click Save.</span></span>
11. <span data-ttu-id="5fdf1-158">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5fdf1-158">Close the page.</span></span>


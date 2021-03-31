---
title: Tilstandsvurdering
description: Dette emnet forklarer hvordan du oppretter en mal for tilstandsvurdering og registrerer deg for et aktivum i Aktivumbehandling.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d84520413659db32713711ad5ac980f1e8b5519
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217179"
---
# <a name="condition-assessment"></a><span data-ttu-id="c22e8-103">Tilstandsvurdering</span><span class="sxs-lookup"><span data-stu-id="c22e8-103">Condition assessment</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c22e8-104">Dette emnet forklarer hvordan du oppretter en mal for tilstandsvurdering og registrerer deg for et aktivum i Aktivumbehandling.</span><span class="sxs-lookup"><span data-stu-id="c22e8-104">This topic explains how to create a condition assessment template and registration on an asset in Asset Management.</span></span> <span data-ttu-id="c22e8-105">Tilstandsvurdering utføres med jevne mellomrom, og det primære målet er å opprette og vedlikeholde tilstandsdata for aktiva.</span><span class="sxs-lookup"><span data-stu-id="c22e8-105">Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on assets.</span></span> <span data-ttu-id="c22e8-106">Sett fra et forebyggende vedlikeholdsperspektiv er det viktig å overvåke viktig informasjon som nåværende tilstand, og gjenværende levetid.</span><span class="sxs-lookup"><span data-stu-id="c22e8-106">Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span.</span></span> <span data-ttu-id="c22e8-107">Videre, hvis du utfører tilstandsvurdering med jevne mellomrom, vil du være i stand til å overvåke og sammenligne forholdene på maskineriet i fabrikken.</span><span class="sxs-lookup"><span data-stu-id="c22e8-107">Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.</span></span>

<span data-ttu-id="c22e8-108">Tilstandsvurdering kan brukes til å måle og overvåke mange forhold på utstyret ditt.</span><span class="sxs-lookup"><span data-stu-id="c22e8-108">Condition assessment can be used to measure and monitor many conditions on your equipment.</span></span> <span data-ttu-id="c22e8-109">Eksempel: Du kan måle vibrasjoner på maskineriet.</span><span class="sxs-lookup"><span data-stu-id="c22e8-109">Example: You could measure vibrations on your machinery.</span></span> <span data-ttu-id="c22e8-110">Etter at du har registrert vibrasjonsmålinger i Aktivumbehandling på ulike typer utstyr, kan du søke etter den siste registrerte vurderingen og vise vibrasjonsmålinger.</span><span class="sxs-lookup"><span data-stu-id="c22e8-110">After you have registered vibration measurements in Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.</span></span>

<span data-ttu-id="c22e8-111">Tilstandsvurderingen opprettes på aktiva.</span><span class="sxs-lookup"><span data-stu-id="c22e8-111">Condition assessment is created on assets.</span></span> <span data-ttu-id="c22e8-112">Du definerer en mal for tilstandsvurdering for en aktivatype før du utfører tilstandsvurderingsprosedyren.</span><span class="sxs-lookup"><span data-stu-id="c22e8-112">You set up a condition assessment template on an asset type before you carry out the condition assessment procedure.</span></span> <span data-ttu-id="c22e8-113">Grunnen til å bruke maler for tilstandsvurdering er å unngå variasjon av tilstandsdata for lignende aktiva.</span><span class="sxs-lookup"><span data-stu-id="c22e8-113">The reason for using templates for condition assessment is to avoid variation of condition data on similar assets.</span></span> <span data-ttu-id="c22e8-114">Sekvensen for å definere og bruke tilstandsvurdering i Aktivumbehandling er: Først oppretter du de nødvendige malene for tilstandsvurdering.</span><span class="sxs-lookup"><span data-stu-id="c22e8-114">The sequence for setting up and using condition assessment in Asset Management is: First you set up the required condition assessment templates.</span></span> <span data-ttu-id="c22e8-115">Deretter knytter du maler til ressurstyper i skjemaet **Aktivatyper**.</span><span class="sxs-lookup"><span data-stu-id="c22e8-115">Next, you associate templates with asset types in the **Asset types** form.</span></span> <span data-ttu-id="c22e8-116">Til slutt kan du opprette tilstandsvurderingsregistreringer for et aktivum i **Aktivum**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="c22e8-116">Finally, you can create condition assessment registrations on an asset in the **Asset** form.</span></span>

## <a name="create-a-condition-assessment-template"></a><span data-ttu-id="c22e8-117">Opprette en mal for tilstandsvurdering</span><span class="sxs-lookup"><span data-stu-id="c22e8-117">Create a condition assessment template</span></span>

1. <span data-ttu-id="c22e8-118">Velg **Aktivastyring** > **Oppsett** > **Aktivatyper** > **Tilstandsvurdering**.</span><span class="sxs-lookup"><span data-stu-id="c22e8-118">Select **Asset management** > **Setup** > **Asset types** > **Condition assessment**.</span></span>
2. <span data-ttu-id="c22e8-119">Velg **Ny** for å opprette en ny mal.</span><span class="sxs-lookup"><span data-stu-id="c22e8-119">Select **New** to create a new template.</span></span>
3. <span data-ttu-id="c22e8-120">Sett inn en ID for malen i **Mal**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c22e8-120">Insert and ID for the template in the **Template** field.</span></span>
4. <span data-ttu-id="c22e8-121">Sett inn et navn på malen i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c22e8-121">Insert a name for the template in the **Name** field.</span></span>
5. <span data-ttu-id="c22e8-122">På hurtigfanen **Tilstandsvurderingslinjer** legger du til linjene som kreves for tilstandsvurderingen, inkludert valg av riktig tilstandstype og målenhet.</span><span class="sxs-lookup"><span data-stu-id="c22e8-122">On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.</span></span>
6. <span data-ttu-id="c22e8-123">På hurtigfanen **Aktivatyper** legger du til aktivatypene som skal bruke malen for tilstandsvurdering.</span><span class="sxs-lookup"><span data-stu-id="c22e8-123">On the **Asset types** FastTab, add the asset types that should use the condition assessment template.</span></span>
7. <span data-ttu-id="c22e8-124">I feltene **Linjer** og **Aktivatyper** i **Detaljer**-gruppen øverst på skjermen ser du antallet tilstandslinjer og aktivatypene som er knyttet til den valgte malen for tilstandsvurdering.</span><span class="sxs-lookup"><span data-stu-id="c22e8-124">In the **Lines** and **Asset types** fields in the **Details** group at the top of the screen, you will see the number of assessment lines and asset types related to the selected condition assessment template.</span></span>


## <a name="create-condition-assessment-registration-on-an-asset"></a><span data-ttu-id="c22e8-125">Opprette tilstandsvurderingsregistrering på et aktivum</span><span class="sxs-lookup"><span data-stu-id="c22e8-125">Create condition assessment registration on an asset</span></span>

1. <span data-ttu-id="c22e8-126">Velg **Aktivastyring** > **Felles** > **Aktiva** > **Alle aktiva**.</span><span class="sxs-lookup"><span data-stu-id="c22e8-126">Select **Asset management** > **Common** > **Assets** > **All Assets**.</span></span>
2. <span data-ttu-id="c22e8-127">I listen velger du aktivumet du vil opprette en tilstandsvurderingsregistrering for.</span><span class="sxs-lookup"><span data-stu-id="c22e8-127">In the list, select the asset for which you want to create a condition assessment registration.</span></span>
3. <span data-ttu-id="c22e8-128">Gå til fanen **Generelt**, og klikk **Tilstandsvurdering**.</span><span class="sxs-lookup"><span data-stu-id="c22e8-128">On the **General** tab, click **Condition assessment**.</span></span>
4. <span data-ttu-id="c22e8-129">Klikk på **Ny** for å lage en ny registrering.</span><span class="sxs-lookup"><span data-stu-id="c22e8-129">Click **New** to make a new registration.</span></span>
5. <span data-ttu-id="c22e8-130">Velg datoen for tilstandsvurderingen i **Dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c22e8-130">Select the date for the condition assessment in the **Date** field.</span></span>
6. <span data-ttu-id="c22e8-131">Velg navnet på arbeideren som utførte tilstandsregistreringen, i **Arbeider**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c22e8-131">Select the name of the worker who carried out the assessment registration in the **Worker** field.</span></span>
7. <span data-ttu-id="c22e8-132">I **linjer**-feltet ser du antallet vurderingslinjer som er definert for tilstandsvurderingen.</span><span class="sxs-lookup"><span data-stu-id="c22e8-132">In the **Lines** field, you see the number of assessment lines set up on the condition assessment.</span></span>
8. <span data-ttu-id="c22e8-133">Velg en mal for tilstandsvurderingen i **Mal**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c22e8-133">Select a template for the condition assessment in the **Template** field.</span></span> <span data-ttu-id="c22e8-134">Navnet på malen settes inn automatisk inn i **Navn**-feltet, og de relaterte registreringslinjene settes inn på hurtigfanen **Tilstandsvurderingslinjer**.</span><span class="sxs-lookup"><span data-stu-id="c22e8-134">The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.</span></span>
9. <span data-ttu-id="c22e8-135">Du kan sette inn merknader knyttet til den valgte tilstandsvurderingen på hurtigfanen **Notater**.</span><span class="sxs-lookup"><span data-stu-id="c22e8-135">You can insert notes relating to the selected condition assessment on the **Notes** FastTab.</span></span>
10. <span data-ttu-id="c22e8-136">For hver tilstandsvurderingslinje setter du inn målingsdata i **Verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c22e8-136">For each condition assessment line, insert measurement data in the **Value** field.</span></span>
11. <span data-ttu-id="c22e8-137">Du kan sette inn en merknad knyttet til den valgte registreringslinjen på hurtigfanen **Tilstandsvurderingslinjer** > **Kommentarer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c22e8-137">You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** field.</span></span> <span data-ttu-id="c22e8-138">Hvis du legger til en kommentar på en linje, merkes det det automatisk av for **Kommentar**.</span><span class="sxs-lookup"><span data-stu-id="c22e8-138">If you add a comment on a line, the **Comment** check box is automatically selected.</span></span>

<span data-ttu-id="c22e8-139">Når du har foretatt en tilstandsvurderingsregistrering på et aktivum, kan du skrive ut en tilstandsvurderingsrapport.</span><span class="sxs-lookup"><span data-stu-id="c22e8-139">After you have made a condition assessment registration on an asset, you can print a condition assessment report.</span></span>

>[!NOTE]
><span data-ttu-id="c22e8-140">Du kan også registrere en tilsynsvurdering på en arbeidsordre (**Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** > **Tilstandsvurdering**-knappen.)</span><span class="sxs-lookup"><span data-stu-id="c22e8-140">You can also register condition assessment on a work order (**Asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
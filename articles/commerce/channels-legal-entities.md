---
title: Opprett juridiske enheter
description: Dette emnet beskriver hvordan du oppretter juridiske enheter i Microsoft Dynamics 365 Commerce, som må opprettes og konfigureres før du oppretter kanaler.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 28cbcc42505f1dc90c420adc812735841541c8e0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414608"
---
# <a name="create-legal-entities"></a><span data-ttu-id="c8e6d-103">Opprett juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="c8e6d-103">Create legal entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c8e6d-104">Dette emnet beskriver hvordan du oppretter juridiske enheter i Microsoft Dynamics 365 Commerce, som må opprettes og konfigureres før du oppretter kanaler.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

## <a name="overview"></a><span data-ttu-id="c8e6d-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="c8e6d-105">Overview</span></span>

<span data-ttu-id="c8e6d-106">En juridisk enhet er en organisasjon som har en registrert eller lovfestet juridisk struktur.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-106">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="c8e6d-107">Juridiske enheter kan inngå juridiske kontrakter og er påkrevd for å klargjøre oppgjør som rapporterer om prestasjonen.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-107">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="c8e6d-108">Et firma er en type juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-108">A company is a type of legal entity.</span></span> <span data-ttu-id="c8e6d-109">Firmaer er for øyeblikket den eneste typen juridisk enhet som du kan opprette, og hver juridisk enhet er tilknyttet en firma-IDen.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-109">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="c8e6d-110">Denne tilknytningen finnes fordi noen funksjonsområder i programmet bruker en firma-ID eller *dataområde-ID*, i sine datamodeller.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-110">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="c8e6d-111">I disse funksjonsområdene brukes firmaer som en grense for datasikkerhet.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-111">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="c8e6d-112">Brukere har bare tilgang til data for firmaet de er logget på.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-112">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="c8e6d-113">Når du oppretter en kanal, må du angi hvilken juridisk enhet kanalen tilhører.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-113">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="c8e6d-114">Opprette en ny juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="c8e6d-114">Create a new legal entity</span></span>

<span data-ttu-id="c8e6d-115">Hvis du vil opprette en ny juridisk enhet i Dynamics 365 Commerce, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="c8e6d-115">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="c8e6d-116">I navigasjonsruten går du til **Moduler \> Hovedkvarteroppsett \> Juridiske enheter**.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-116">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="c8e6d-117">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-117">On the action pane, select **New**.</span></span> <span data-ttu-id="c8e6d-118">Ruten **Ny juridisk enhet** vises til høyre.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-118">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="c8e6d-119">Angi en verdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="c8e6d-120">Angi en verdi i feltet **Firma**.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-120">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="c8e6d-121">Angi eller velg en verdi i **Land/område**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-121">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="c8e6d-122">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-122">Select **OK**.</span></span> 

   ![Opprette juridisk enhet](media/legal-entities.png)

1. <span data-ttu-id="c8e6d-124">I **Generelt**-seksjonen angir du følgende generelle informasjon om den juridiske enheten:</span><span class="sxs-lookup"><span data-stu-id="c8e6d-124">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="c8e6d-125">Angi et søkenavn hvis et søkenavn er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-125">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="c8e6d-126">Et søkenavn er et alternativt navn som kan brukes til å søke etter den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-126">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="c8e6d-127">Velg om den juridiske enheten brukes som et konsoliderte firma.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-127">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="c8e6d-128">Velg om den juridiske enheten brukes som et elimineringsfirma.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-128">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="c8e6d-129">Velg **standardspråket** for enheten.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-129">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="c8e6d-130">Velg **tidssonen** for enheten.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-130">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="c8e6d-131">I **Adresser**-delen velger du **Rediger** for å angi adresseinformasjon, for eksempel gatenavn og -nummer, postnummer og poststed.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-131">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="c8e6d-132">I delen **Kontaktinformasjon** angir du informasjon om kommunikasjonsmetoder, for eksempel e-postadresse, URL-adresser og telefonnumre.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-132">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="c8e6d-133">I delen **Lovbestemt rapportering** skriver du inn registreringsnumrene som brukes ved lovbestemt rapportering.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-133">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="c8e6d-134">I delen **Registreringsnumre** angir du eventuell informasjon som kreves av den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-134">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="c8e6d-135">I delen **Bankkontoinformasjon** angir du bankkontoer og registreringsnumre for den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-135">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="c8e6d-136">I delen **Utenrikshandel og logistikk** angir du forsendelsesinformasjon for den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-136">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="c8e6d-137">I delen **Nummerserier** kan du vise nummerseriene som er tilknyttet den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-137">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="c8e6d-138">Dette vil være tomt til å begynne med.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-138">This will be empty to start with.</span></span>
1. <span data-ttu-id="c8e6d-139">I delen **Instrumentbordbilde** viser eller endrer du logoen og instrumentbordbildet som er knyttet til den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-139">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="c8e6d-140">I delen **Avgiftsregistrering** skriver du inn registreringsnumrene som brukes til å rapportere til skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-140">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="c8e6d-141">I delen **1099-avgift** skriver du inn 1099-informasjon for den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-141">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="c8e6d-142">I delen **Skatteinformasjon** angir du skatteinformasjon for den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-142">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="c8e6d-143">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-143">Select **Save**.</span></span>

<span data-ttu-id="c8e6d-144">Bildet nedenfor viser et detaljer om et eksempel på en juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="c8e6d-144">The following image shows details of an example legal entity.</span></span>

![Generell del om juridisk enhet](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="c8e6d-146">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c8e6d-146">Additional resources</span></span>

[<span data-ttu-id="c8e6d-147">Oversikt over organisasjoner og organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="c8e6d-147">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c8e6d-148">Planlegge organisasjonshierarkiet</span><span class="sxs-lookup"><span data-stu-id="c8e6d-148">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c8e6d-149">Organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="c8e6d-149">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="c8e6d-150">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="c8e6d-150">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="c8e6d-151">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="c8e6d-151">Channel setup prerequisites</span></span>](channels-prerequisites.md)

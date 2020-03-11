---
title: Opprette en standardkunde
description: Dette emnet beskriver hvordan du oppretter en standardkunde som skal brukes ved opprettelse av en kanal i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: ba1d10a897f349703737068d772423f7d0292944
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057968"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="e5e7a-103">Opprette en standardkunde</span><span class="sxs-lookup"><span data-stu-id="e5e7a-103">Create a default customer</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e5e7a-104">Dette emnet beskriver hvordan du oppretter en standardkunde som skal brukes ved opprettelse av en kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e5e7a-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="e5e7a-105">Overview</span></span>

<span data-ttu-id="e5e7a-106">Når du oppretter en kanal, må du angi en standardkunde.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-106">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="e5e7a-107">En standardkunde kan enkelt opprettes etter at du først har opprettet kundegruppen og kundeadresseboken.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-107">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="e5e7a-108">Opprette en kundegruppe</span><span class="sxs-lookup"><span data-stu-id="e5e7a-108">Create a customer group</span></span>

<span data-ttu-id="e5e7a-109">Hvis det ikke finnes kundegrupper enda, kan du opprette én.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-109">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="e5e7a-110">Eksempler kan være grupper for å representere ulike kundegrupper, for eksempel engros, detaljhandel, Internett, ansatte osv.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-110">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="e5e7a-111">Hvis du vil opprette en kundegruppe, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-111">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="e5e7a-112">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kunder \> Kundegrupper**.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-112">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="e5e7a-113">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="e5e7a-114">I **Kundegruppe**-boksen angir du en kundegruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-114">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="e5e7a-115">I **Beskrivelse**-boksen angir du en passende beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-115">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="e5e7a-116">I **Betalingsvilkår**-boksen angir du en passende verdi.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-116">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="e5e7a-117">I **Tid mellom forfallsdato og betalingsdato for faktura**-boksen angir du en passende verdi.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-117">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="e5e7a-118">I **Standard avgiftsgruppe**-boksen angir du om aktuelt en avgiftsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-118">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="e5e7a-119">Merk om aktuelt av i **Prisene inkluderer salgsavgift**-avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-119">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="e5e7a-120">I **Standard avskrivingsgrunn**-boksen angir du om aktuelt en passende verdi.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-120">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="e5e7a-121">Følgende bilde viser flere konfigurerte kundegrupper.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-121">The following image shows several configured customer groups.</span></span>

![Kundegrupper](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="e5e7a-123">Opprette en kundeadressebok</span><span class="sxs-lookup"><span data-stu-id="e5e7a-123">Create a customer address book</span></span>

<span data-ttu-id="e5e7a-124">En kunde må være knyttet til en adressebok.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-124">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="e5e7a-125">Hvis dette ikke er opprettet enda, må du opprette én.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-125">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="e5e7a-126">Hvis du vil opprette en kundeadressebok, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-126">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="e5e7a-127">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Adressebøker**.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-127">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="e5e7a-128">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-128">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="e5e7a-129">I **Navn**-boksen angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-129">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="e5e7a-130">I **Beskrivelse**-boksen angir du en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-130">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="e5e7a-131">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-131">On the action pane, select **Save**.</span></span>

<span data-ttu-id="e5e7a-132">Bildet nedenfor viser et eksempel på en adressebok.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-132">The following image shows an example address book.</span></span>

![Adressebok](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="e5e7a-134">Opprette en standardkunde</span><span class="sxs-lookup"><span data-stu-id="e5e7a-134">Create a default customer</span></span>

<span data-ttu-id="e5e7a-135">Hvis du vil opprette en standardkunde, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-135">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="e5e7a-136">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kunder \> Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-136">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="e5e7a-137">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="e5e7a-138">I **Type**-rullegardinlisten velger du "Person".</span><span class="sxs-lookup"><span data-stu-id="e5e7a-138">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="e5e7a-139">I **Kundekonto**-rullegardinlisten velger du eller skriver inn et kontonummer (for eksempel "100001").</span><span class="sxs-lookup"><span data-stu-id="e5e7a-139">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="e5e7a-140">I **Fornavn**-rullegardinlisten velger du eller angir et navn (for eksempel "Standard").</span><span class="sxs-lookup"><span data-stu-id="e5e7a-140">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="e5e7a-141">I **Mellomnavn**-rullegardinlisten velger du eller angir et navn (for eksempel "Detaljhandel").</span><span class="sxs-lookup"><span data-stu-id="e5e7a-141">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="e5e7a-142">I **Etternavn**-rullegardinlisten velger du eller angir et navn (for eksempel "Kunde").</span><span class="sxs-lookup"><span data-stu-id="e5e7a-142">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="e5e7a-143">I **Valuta**-rullegardinlisten velger du eller angir en valuta (for eksempel "USD").</span><span class="sxs-lookup"><span data-stu-id="e5e7a-143">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="e5e7a-144">I **Valuta**-rullegardinlisten velger du kundegruppen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-144">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="e5e7a-145">I **Adressebøker**-rullegardinlisten velger du en eksisterende kundeadressebok.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-145">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="e5e7a-146">Velg **Lagre** for å lagre og gå tilbake til Kundedetaljer-skjermbildet for den nye kunden.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-146">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="e5e7a-147">Det er ikke nødvendig å legge til en adresse for en standardkunde.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-147">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="e5e7a-148">Bildet nedenfor viser et eksempel på kundeopprettelse.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-148">The following image shows an example of customer creation.</span></span>

![Standardkundeopprettelse](media/default-customer-creation.png)

<span data-ttu-id="e5e7a-150">Bildet nedenfor viser en standardkundekonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-150">The following image shows a default customer configuration.</span></span>

![Eksempel på kundekonfigurasjon](media/default-customer-configuration1.png)

<span data-ttu-id="e5e7a-152">De fleste standardverdiene på Kundedetaljer-skjermbildet kan bli slik de er, men to verdier må endres.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-152">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="e5e7a-153">På Kundedetaljer-skjermbildet utvider du **Standardverdier for salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-153">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="e5e7a-154">I **Område**-rullegardinlisten velger du eller angir et forhåndskonfigurert område.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-154">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="e5e7a-155">I **Lager**-rullegardinlisten velger du eller angir et forhåndskonfigurert lager.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-155">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="e5e7a-156">Bildet nedenfor viser et eksempel på kundekonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-156">The following image shows an example customer configuration.</span></span>

![Eksempel på kundekonfigurasjon](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="e5e7a-158">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e5e7a-158">Additional resources</span></span>

[<span data-ttu-id="e5e7a-159">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="e5e7a-159">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="e5e7a-160">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="e5e7a-160">Channel setup prerequisites</span></span>](channels-prerequisites.md)

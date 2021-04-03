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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: f988732549ce82919f02c87b320623d8d4218735
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477906"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="b8078-103">Opprette en standardkunde</span><span class="sxs-lookup"><span data-stu-id="b8078-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b8078-104">Dette emnet beskriver hvordan du oppretter en standardkunde som skal brukes ved opprettelse av en kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b8078-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b8078-105">Når du oppretter en kanal, må du angi en standardkunde.</span><span class="sxs-lookup"><span data-stu-id="b8078-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="b8078-106">En standardkunde kan enkelt opprettes etter at du først har opprettet kundegruppen og kundeadresseboken.</span><span class="sxs-lookup"><span data-stu-id="b8078-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="b8078-107">Opprette en kundegruppe</span><span class="sxs-lookup"><span data-stu-id="b8078-107">Create a customer group</span></span>

<span data-ttu-id="b8078-108">Hvis det ikke finnes kundegrupper enda, kan du opprette én.</span><span class="sxs-lookup"><span data-stu-id="b8078-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="b8078-109">Eksempler kan være grupper for å representere ulike kundegrupper, for eksempel engros, detaljhandel, Internett, ansatte osv.</span><span class="sxs-lookup"><span data-stu-id="b8078-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="b8078-110">Hvis du vil opprette en kundegruppe, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="b8078-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="b8078-111">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kunder \> Kundegrupper**.</span><span class="sxs-lookup"><span data-stu-id="b8078-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="b8078-112">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b8078-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="b8078-113">I **Kundegruppe**-boksen angir du en kundegruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="b8078-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="b8078-114">I **Beskrivelse**-boksen angir du en passende beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b8078-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="b8078-115">I **Betalingsvilkår**-boksen angir du en passende verdi.</span><span class="sxs-lookup"><span data-stu-id="b8078-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="b8078-116">I **Tid mellom forfallsdato og betalingsdato for faktura**-boksen angir du en passende verdi.</span><span class="sxs-lookup"><span data-stu-id="b8078-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="b8078-117">I **Standard avgiftsgruppe**-boksen angir du om aktuelt en avgiftsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b8078-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="b8078-118">Merk om aktuelt av i **Prisene inkluderer salgsavgift**-avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="b8078-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="b8078-119">I **Standard avskrivingsgrunn**-boksen angir du om aktuelt en passende verdi.</span><span class="sxs-lookup"><span data-stu-id="b8078-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="b8078-120">Følgende bilde viser flere konfigurerte kundegrupper.</span><span class="sxs-lookup"><span data-stu-id="b8078-120">The following image shows several configured customer groups.</span></span>

![Kundegrupper](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="b8078-122">Opprette en kundeadressebok</span><span class="sxs-lookup"><span data-stu-id="b8078-122">Create a customer address book</span></span>

<span data-ttu-id="b8078-123">En kunde må være knyttet til en adressebok.</span><span class="sxs-lookup"><span data-stu-id="b8078-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="b8078-124">Hvis dette ikke er opprettet enda, må du opprette én.</span><span class="sxs-lookup"><span data-stu-id="b8078-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="b8078-125">Hvis du vil opprette en kundeadressebok, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="b8078-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="b8078-126">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Adressebøker**.</span><span class="sxs-lookup"><span data-stu-id="b8078-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="b8078-127">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b8078-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="b8078-128">I **Navn**-boksen angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="b8078-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="b8078-129">I **Beskrivelse**-boksen angir du en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b8078-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="b8078-130">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b8078-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="b8078-131">Bildet nedenfor viser et eksempel på en adressebok.</span><span class="sxs-lookup"><span data-stu-id="b8078-131">The following image shows an example address book.</span></span>

![Adressebok](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="b8078-133">Opprette en standardkunde</span><span class="sxs-lookup"><span data-stu-id="b8078-133">Create a default customer</span></span>

<span data-ttu-id="b8078-134">Hvis du vil opprette en standardkunde, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="b8078-134">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="b8078-135">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kunder \> Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="b8078-135">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="b8078-136">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b8078-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="b8078-137">I **Type**-rullegardinlisten velger du "Person".</span><span class="sxs-lookup"><span data-stu-id="b8078-137">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="b8078-138">I **Kundekonto**-rullegardinlisten velger du eller skriver inn et kontonummer (for eksempel "100001").</span><span class="sxs-lookup"><span data-stu-id="b8078-138">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="b8078-139">I **Fornavn**-rullegardinlisten velger du eller angir et navn (for eksempel "Standard").</span><span class="sxs-lookup"><span data-stu-id="b8078-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="b8078-140">I **Mellomnavn**-rullegardinlisten velger du eller angir et navn (for eksempel "Detaljhandel").</span><span class="sxs-lookup"><span data-stu-id="b8078-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="b8078-141">I **Etternavn**-rullegardinlisten velger du eller angir et navn (for eksempel "Kunde").</span><span class="sxs-lookup"><span data-stu-id="b8078-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="b8078-142">I **Valuta**-rullegardinlisten velger du eller angir en valuta (for eksempel "USD").</span><span class="sxs-lookup"><span data-stu-id="b8078-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="b8078-143">I **Valuta**-rullegardinlisten velger du kundegruppen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="b8078-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="b8078-144">I **Adressebøker**-rullegardinlisten velger du en eksisterende kundeadressebok.</span><span class="sxs-lookup"><span data-stu-id="b8078-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="b8078-145">Velg **Lagre** for å lagre og gå tilbake til Kundedetaljer-skjermbildet for den nye kunden.</span><span class="sxs-lookup"><span data-stu-id="b8078-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="b8078-146">Det er ikke nødvendig å legge til en adresse for en standardkunde.</span><span class="sxs-lookup"><span data-stu-id="b8078-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="b8078-147">Bildet nedenfor viser et eksempel på kundeopprettelse.</span><span class="sxs-lookup"><span data-stu-id="b8078-147">The following image shows an example of customer creation.</span></span>

![Standardkundeopprettelse](media/default-customer-creation.png)

<span data-ttu-id="b8078-149">Bildet nedenfor viser en standardkundekonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="b8078-149">The following image shows a default customer configuration.</span></span>

![Eksempel på kundekonfigurasjon](media/default-customer-configuration1.png)

<span data-ttu-id="b8078-151">De fleste standardverdiene på Kundedetaljer-skjermbildet kan bli slik de er, men to verdier må endres.</span><span class="sxs-lookup"><span data-stu-id="b8078-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="b8078-152">På Kundedetaljer-skjermbildet utvider du **Standardverdier for salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="b8078-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="b8078-153">I **Område**-rullegardinlisten velger du eller angir et forhåndskonfigurert område.</span><span class="sxs-lookup"><span data-stu-id="b8078-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="b8078-154">I **Lager**-rullegardinlisten velger du eller angir et forhåndskonfigurert lager.</span><span class="sxs-lookup"><span data-stu-id="b8078-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="b8078-155">Bildet nedenfor viser et eksempel på kundekonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="b8078-155">The following image shows an example customer configuration.</span></span>

![Eksempel på kundekonfigurasjon](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="b8078-157">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b8078-157">Additional resources</span></span>

[<span data-ttu-id="b8078-158">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="b8078-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="b8078-159">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="b8078-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

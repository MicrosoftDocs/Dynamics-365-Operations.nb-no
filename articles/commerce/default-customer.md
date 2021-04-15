---
title: Opprette en standardkunde
description: Dette emnet beskriver hvordan du oppretter en standardkunde som skal brukes ved opprettelse av en kanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ecdf4e5618d3397527bf83977857fbe3f8dbb265
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799185"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="bb989-103">Opprette en standardkunde</span><span class="sxs-lookup"><span data-stu-id="bb989-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bb989-104">Dette emnet beskriver hvordan du oppretter en standardkunde som skal brukes ved opprettelse av en kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb989-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="bb989-105">Når du oppretter en kanal, må du angi en standardkunde.</span><span class="sxs-lookup"><span data-stu-id="bb989-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="bb989-106">En standardkunde kan enkelt opprettes etter at du først har opprettet kundegruppen og kundeadresseboken.</span><span class="sxs-lookup"><span data-stu-id="bb989-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="bb989-107">Opprette en kundegruppe</span><span class="sxs-lookup"><span data-stu-id="bb989-107">Create a customer group</span></span>

<span data-ttu-id="bb989-108">Hvis det ikke finnes kundegrupper enda, kan du opprette én.</span><span class="sxs-lookup"><span data-stu-id="bb989-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="bb989-109">Eksempler kan være grupper for å representere ulike kundegrupper, for eksempel engros, detaljhandel, Internett, ansatte osv.</span><span class="sxs-lookup"><span data-stu-id="bb989-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="bb989-110">Hvis du vil opprette en kundegruppe, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="bb989-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="bb989-111">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kunder \> Kundegrupper**.</span><span class="sxs-lookup"><span data-stu-id="bb989-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="bb989-112">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bb989-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="bb989-113">I **Kundegruppe**-boksen angir du en kundegruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="bb989-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="bb989-114">I **Beskrivelse**-boksen angir du en passende beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="bb989-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="bb989-115">I **Betalingsvilkår**-boksen angir du en passende verdi.</span><span class="sxs-lookup"><span data-stu-id="bb989-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="bb989-116">I **Tid mellom forfallsdato og betalingsdato for faktura**-boksen angir du en passende verdi.</span><span class="sxs-lookup"><span data-stu-id="bb989-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="bb989-117">I **Standard avgiftsgruppe**-boksen angir du om aktuelt en avgiftsgruppe.</span><span class="sxs-lookup"><span data-stu-id="bb989-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="bb989-118">Merk om aktuelt av i **Prisene inkluderer salgsavgift**-avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="bb989-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="bb989-119">I **Standard avskrivingsgrunn**-boksen angir du om aktuelt en passende verdi.</span><span class="sxs-lookup"><span data-stu-id="bb989-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="bb989-120">Følgende bilde viser flere konfigurerte kundegrupper.</span><span class="sxs-lookup"><span data-stu-id="bb989-120">The following image shows several configured customer groups.</span></span>

![Kundegrupper](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="bb989-122">Opprette en kundeadressebok</span><span class="sxs-lookup"><span data-stu-id="bb989-122">Create a customer address book</span></span>

<span data-ttu-id="bb989-123">En kunde må være knyttet til en adressebok.</span><span class="sxs-lookup"><span data-stu-id="bb989-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="bb989-124">Hvis dette ikke er opprettet enda, må du opprette én.</span><span class="sxs-lookup"><span data-stu-id="bb989-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="bb989-125">Hvis du vil opprette en kundeadressebok, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="bb989-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="bb989-126">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Adressebøker**.</span><span class="sxs-lookup"><span data-stu-id="bb989-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="bb989-127">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bb989-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="bb989-128">I **Navn**-boksen angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="bb989-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="bb989-129">I **Beskrivelse**-boksen angir du en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="bb989-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="bb989-130">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="bb989-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="bb989-131">Bildet nedenfor viser et eksempel på en adressebok.</span><span class="sxs-lookup"><span data-stu-id="bb989-131">The following image shows an example address book.</span></span>

![Adressebok](media/address-book.png)

## <a name="create-a-default-customer&quot;></a><span data-ttu-id=&quot;bb989-133&quot;>Opprette en standardkunde</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;bb989-133&quot;>Create a default customer</span></span>

<span data-ttu-id=&quot;bb989-134&quot;>Hvis du vil opprette en standardkunde, følger du disse trinnene.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;bb989-134&quot;>To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id=&quot;bb989-135&quot;>I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kunder \> Alle kunder**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;bb989-135&quot;>In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id=&quot;bb989-136&quot;>I handlingsruten velger du **Ny**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;bb989-136&quot;>On the action pane, select **New**.</span></span>
1. <span data-ttu-id=&quot;bb989-137&quot;>I **Type**-rullegardinlisten velger du &quot;Person&quot;.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;bb989-137&quot;>In the **Type** drop-down list, select &quot;Person&quot;.</span></span>
1. <span data-ttu-id=&quot;bb989-138&quot;>I **Kundekonto**-rullegardinlisten velger du eller skriver inn et kontonummer (for eksempel &quot;100001").</span><span class="sxs-lookup"><span data-stu-id="bb989-138">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="bb989-139">I **Fornavn**-rullegardinlisten velger du eller angir et navn (for eksempel "Standard").</span><span class="sxs-lookup"><span data-stu-id="bb989-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="bb989-140">I **Mellomnavn**-rullegardinlisten velger du eller angir et navn (for eksempel "Detaljhandel").</span><span class="sxs-lookup"><span data-stu-id="bb989-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="bb989-141">I **Etternavn**-rullegardinlisten velger du eller angir et navn (for eksempel "Kunde").</span><span class="sxs-lookup"><span data-stu-id="bb989-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="bb989-142">I **Valuta**-rullegardinlisten velger du eller angir en valuta (for eksempel "USD").</span><span class="sxs-lookup"><span data-stu-id="bb989-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="bb989-143">I **Valuta**-rullegardinlisten velger du kundegruppen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="bb989-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="bb989-144">I **Adressebøker**-rullegardinlisten velger du en eksisterende kundeadressebok.</span><span class="sxs-lookup"><span data-stu-id="bb989-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="bb989-145">Velg **Lagre** for å lagre og gå tilbake til Kundedetaljer-skjermbildet for den nye kunden.</span><span class="sxs-lookup"><span data-stu-id="bb989-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="bb989-146">Det er ikke nødvendig å legge til en adresse for en standardkunde.</span><span class="sxs-lookup"><span data-stu-id="bb989-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="bb989-147">Bildet nedenfor viser et eksempel på kundeopprettelse.</span><span class="sxs-lookup"><span data-stu-id="bb989-147">The following image shows an example of customer creation.</span></span>

![Standardkundeopprettelse](media/default-customer-creation.png)

<span data-ttu-id="bb989-149">Bildet nedenfor viser en standardkundekonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="bb989-149">The following image shows a default customer configuration.</span></span>

![Eksempel på kundekonfigurasjon](media/default-customer-configuration1.png)

<span data-ttu-id="bb989-151">De fleste standardverdiene på Kundedetaljer-skjermbildet kan bli slik de er, men to verdier må endres.</span><span class="sxs-lookup"><span data-stu-id="bb989-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="bb989-152">På Kundedetaljer-skjermbildet utvider du **Standardverdier for salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="bb989-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="bb989-153">I **Område**-rullegardinlisten velger du eller angir et forhåndskonfigurert område.</span><span class="sxs-lookup"><span data-stu-id="bb989-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="bb989-154">I **Lager**-rullegardinlisten velger du eller angir et forhåndskonfigurert lager.</span><span class="sxs-lookup"><span data-stu-id="bb989-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="bb989-155">Bildet nedenfor viser et eksempel på kundekonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="bb989-155">The following image shows an example customer configuration.</span></span>

![Eksempel på kundekonfigurasjon](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="bb989-157">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="bb989-157">Additional resources</span></span>

[<span data-ttu-id="bb989-158">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="bb989-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="bb989-159">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="bb989-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

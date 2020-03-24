---
title: Integrerte originalkunde
description: Dette emnet beskriver integreringen av kundedata mellom Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 269346d38eeb3812c352d16f9d50fbcd09307c12
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124595"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="7d64b-103">Integrert original for kunde</span><span class="sxs-lookup"><span data-stu-id="7d64b-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="7d64b-104">Det er vanlig at kundeposter mestres i mer enn ett program.</span><span class="sxs-lookup"><span data-stu-id="7d64b-104">It's typical for customer records to be mastered in more than one application.</span></span> <span data-ttu-id="7d64b-105">Salgsaktivitet kan for eksempel hente inn kommersielle kundeposter gjennom et salgsprogram, og e-handel eller detaljsalg kan hente inn kundeposter gjennom et Finance and Operations-program.</span><span class="sxs-lookup"><span data-stu-id="7d64b-105">For example, sales activity can bring in commercial customer records through a Sales application, and e-Commerce or retail sales can bring in customer records through a Finance and Operations application.</span></span> <span data-ttu-id="7d64b-106">Uansett hvor kundeposten kommer fra, er den integrert bak kulissene på tvers av applikasjonsgrenser og infrastrukturforskjeller.</span><span class="sxs-lookup"><span data-stu-id="7d64b-106">Regardless of where the customer record originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> <span data-ttu-id="7d64b-107">Integrert kundemestring hjelper håndtere multi-Mastering scenarier og gir en omfattende visning av kunden til Dynamics 365-programpakken.</span><span class="sxs-lookup"><span data-stu-id="7d64b-107">Integrated customer mastering helps handle multi-mastering scenarios and provides a comprehensive view of the customer to the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="7d64b-108">Kundedataflyt</span><span class="sxs-lookup"><span data-stu-id="7d64b-108">Customer data flow</span></span>

<span data-ttu-id="7d64b-109">*Kunde* er et veldefinert begrep i programmer.</span><span class="sxs-lookup"><span data-stu-id="7d64b-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="7d64b-110">Integreringen av kundedata innebærer derfor bare å harmonisere kundekonseptet mellom de to programmene.</span><span class="sxs-lookup"><span data-stu-id="7d64b-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="7d64b-111">Følgende illustrasjon viser kundedataflyten.</span><span class="sxs-lookup"><span data-stu-id="7d64b-111">The following illustration shows the customer data flow.</span></span>

![Kundedataflyt](media/dual-write-customer-data-flow.png)

<span data-ttu-id="7d64b-113">Kunder kan grovt klassifiseres i to typer: kommersielle/organisatoriske kunder og forbrukere/sluttbrukere.</span><span class="sxs-lookup"><span data-stu-id="7d64b-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="7d64b-114">Disse to kundetypene lagres og håndteres forskjellig i Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7d64b-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="7d64b-115">I Finance and Operations administreres både kommersielle/organisatoriske kunder og forbrukere/sluttbrukere i én enkelt tabell som heter **CustTable** (CustomerCustomerV3Entity), og de klassifiseres basert på **Type**-attributtet.</span><span class="sxs-lookup"><span data-stu-id="7d64b-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustomerCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="7d64b-116">(Hvis **Type** er satt til **Organisasjon**, er kunden en kommersiell/organisastorisk kunde, og hvis **Type** er satt til **Person**, er kunden en forbruker/sluttbruker.) Den primære kontaktpersoninformasjonen håndteres via SMMContactPersonEntity-enheten.</span><span class="sxs-lookup"><span data-stu-id="7d64b-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="7d64b-117">I Common Data Service, kommersielle/organisatoriske kunder er mastret i kontoenheten og identifiseres som kunder når **RelationshipType**-attributtet er satt til **Kunde**.</span><span class="sxs-lookup"><span data-stu-id="7d64b-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="7d64b-118">Både forbrukere/sluttbrukere og kontaktpersonen representeres av Kontakt-enheten.</span><span class="sxs-lookup"><span data-stu-id="7d64b-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="7d64b-119">Hvis du vil gi et klart skille mellom en forbruker/sluttbruker og en kontaktperson, har **Kontakt**-enheten et boolsk flagg som heter **Sellable**.</span><span class="sxs-lookup"><span data-stu-id="7d64b-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="7d64b-120">Når **Sellable** er **True**, er kontakten en forbruker/sluttbruker, og tilbud og ordrer kan opprettes for denne kontakten.</span><span class="sxs-lookup"><span data-stu-id="7d64b-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="7d64b-121">Når **Sellable** er **False**, er kontakten bare en primærkontaktperson for en kunde.</span><span class="sxs-lookup"><span data-stu-id="7d64b-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="7d64b-122">Når en ikke-salgbar kontakt deltar i en tilbuds- eller en ordreprosess er **Sellable** satt til **True** for å flagge kontakten som en salgbar kontakt.</span><span class="sxs-lookup"><span data-stu-id="7d64b-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="7d64b-123">En kontakt som har blitt en salgbar kontakt, forblir en salgbar kontakt.</span><span class="sxs-lookup"><span data-stu-id="7d64b-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="7d64b-124">Maler</span><span class="sxs-lookup"><span data-stu-id="7d64b-124">Templates</span></span>

<span data-ttu-id="7d64b-125">Kundedata inkluderer all informasjon om kunden, for eksempel kundegruppe, adresser, kontaktinformasjon, betalingsprofil, fakturaprofil og fordelsstatus.</span><span class="sxs-lookup"><span data-stu-id="7d64b-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="7d64b-126">En samling enhetstilordninger fungerer sammen under kundedatasamhandling, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="7d64b-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="7d64b-127">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="7d64b-127">Finance and Operations apps</span></span> | <span data-ttu-id="7d64b-128">Andre Dynamics 365-apper</span><span class="sxs-lookup"><span data-stu-id="7d64b-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="7d64b-129">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="7d64b-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="7d64b-130">CDS-kontakter V2</span><span class="sxs-lookup"><span data-stu-id="7d64b-130">CDS Contacts V2</span></span>             | <span data-ttu-id="7d64b-131">kontakter</span><span class="sxs-lookup"><span data-stu-id="7d64b-131">contacts</span></span>                        | <span data-ttu-id="7d64b-132">Denne malen synkroniserer all primær, sekundær og tertiær informasjon, både for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="7d64b-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="7d64b-133">Kundegrupper</span><span class="sxs-lookup"><span data-stu-id="7d64b-133">Customer groups</span></span>             | <span data-ttu-id="7d64b-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="7d64b-134">msdyn_customergroups</span></span>            | <span data-ttu-id="7d64b-135">Denne malen synkroniserer kundegruppeinformasjon.</span><span class="sxs-lookup"><span data-stu-id="7d64b-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="7d64b-136">Kundebetalingsmåte</span><span class="sxs-lookup"><span data-stu-id="7d64b-136">Customer payment method</span></span>     | <span data-ttu-id="7d64b-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="7d64b-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="7d64b-138">Denne malen synkroniserer informasjon om kundebetalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="7d64b-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="7d64b-139">Kunder V3</span><span class="sxs-lookup"><span data-stu-id="7d64b-139">Customers V3</span></span>                | <span data-ttu-id="7d64b-140">kontoer</span><span class="sxs-lookup"><span data-stu-id="7d64b-140">accounts</span></span>                        | <span data-ttu-id="7d64b-141">Denne malen synkroniserer kundens hoveddata for kommersielle og organisatoriske kunder.</span><span class="sxs-lookup"><span data-stu-id="7d64b-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="7d64b-142">Kunder V3</span><span class="sxs-lookup"><span data-stu-id="7d64b-142">Customers V3</span></span>                | <span data-ttu-id="7d64b-143">kontakter</span><span class="sxs-lookup"><span data-stu-id="7d64b-143">contacts</span></span>                        | <span data-ttu-id="7d64b-144">Denne malen synkroniserer hoveddata for kunder for forbrukere og sluttbrukere.</span><span class="sxs-lookup"><span data-stu-id="7d64b-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="7d64b-145">Fordelskort</span><span class="sxs-lookup"><span data-stu-id="7d64b-145">Loyalty card</span></span>                | <span data-ttu-id="7d64b-146">msdyn_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="7d64b-146">msdyn_loyaltycards</span></span>              | <span data-ttu-id="7d64b-147">Denne malen synkroniserer informasjon om fordelskort.</span><span class="sxs-lookup"><span data-stu-id="7d64b-147">This template synchronizes customer loyalty card information.</span></span>
<span data-ttu-id="7d64b-148">Navnevedlegg</span><span class="sxs-lookup"><span data-stu-id="7d64b-148">Name affixes</span></span>                | <span data-ttu-id="7d64b-149">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="7d64b-149">msdyn_nameaffixes</span></span>               | <span data-ttu-id="7d64b-150">Denne malen synkroniserer referansedata for navnevedlegg, både for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="7d64b-150">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="7d64b-151">Betalingsdagslinjer, CDS V2</span><span class="sxs-lookup"><span data-stu-id="7d64b-151">Payment day lines CDS V2</span></span>    | <span data-ttu-id="7d64b-152">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="7d64b-152">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="7d64b-153">Denne malen synkroniserer referansedata om betalingsdagslinjer, både for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="7d64b-153">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="7d64b-154">Betalingsdager, CDS</span><span class="sxs-lookup"><span data-stu-id="7d64b-154">Payment days CDS</span></span>            | <span data-ttu-id="7d64b-155">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="7d64b-155">msdyn_paymentdays</span></span>               | <span data-ttu-id="7d64b-156">Denne malen synkroniserer referansedata om betalingsdager, både for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="7d64b-156">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="7d64b-157">Linjer i betalingsplan</span><span class="sxs-lookup"><span data-stu-id="7d64b-157">Payment schedule lines</span></span>      | <span data-ttu-id="7d64b-158">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="7d64b-158">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="7d64b-159">Synkroniserer referansedata om betalingsplanlinjer, både for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="7d64b-159">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="7d64b-160">Betalingsplan</span><span class="sxs-lookup"><span data-stu-id="7d64b-160">Payment schedule</span></span>            | <span data-ttu-id="7d64b-161">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="7d64b-161">msdyn_paymentschedules</span></span>          | <span data-ttu-id="7d64b-162">Denne malen synkroniserer referansedata om betalingsplan, både for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="7d64b-162">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="7d64b-163">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="7d64b-163">Terms of payment</span></span>            | <span data-ttu-id="7d64b-164">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="7d64b-164">msdyn_paymentterms</span></span>              | <span data-ttu-id="7d64b-165">Denne malen synkroniserer referansedata om betalingsbetingelser, både for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="7d64b-165">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]

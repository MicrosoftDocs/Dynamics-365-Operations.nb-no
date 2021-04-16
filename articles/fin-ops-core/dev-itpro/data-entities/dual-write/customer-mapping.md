---
title: Integrerte originalkunde
description: Dette emnet beskriver integreringen av kundedata mellom Finance and Operations og Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 0015ca2ccbb0098a5a96bf56ff355fb2f9f8f626
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748929"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="fb39b-103">Integrert original for kunde</span><span class="sxs-lookup"><span data-stu-id="fb39b-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="fb39b-104">Kundedata kan styres i mer enn ett Dynamics 365-program.</span><span class="sxs-lookup"><span data-stu-id="fb39b-104">Customer data can be mastered in more than one Dynamics 365 application.</span></span> <span data-ttu-id="fb39b-105">En kunderad kan for eksempel komme fra salgsaktivitet i Dynamics 365 Sales (en modelldrevet app i Dynamics 365), eller en rad kan stamme fra detaljhandelsaktivitet i Dynamics 365 Commerce (en Finance and Operations-app).</span><span class="sxs-lookup"><span data-stu-id="fb39b-105">For example, a customer row can originate though sales activity in Dynamics 365 Sales (a model-driven app in Dynamics 365), or a row can originate through retail activity in Dynamics 365 Commerce (a Finance and Operations app).</span></span> <span data-ttu-id="fb39b-106">Uansett hvor kundedataene kommer fra, er de integrert bak kulissene.</span><span class="sxs-lookup"><span data-stu-id="fb39b-106">No matter where where the customer data originates, it is integrated behind the scenes.</span></span> <span data-ttu-id="fb39b-107">Integrert original for kunde gir deg fleksibilitet til å styre kundedata i alle Dynamics 365-programmer, og gir en omfattende visning av kunden på tvers av Dynamics 365-programserien.</span><span class="sxs-lookup"><span data-stu-id="fb39b-107">Integrated customer master gives you the flexibility to master customer data in any Dynamics 365 application and provides a comprehensive view of the customer across the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="fb39b-108">Kundedataflyt</span><span class="sxs-lookup"><span data-stu-id="fb39b-108">Customer data flow</span></span>

<span data-ttu-id="fb39b-109">*Kunde* er et veldefinert begrep i programmer.</span><span class="sxs-lookup"><span data-stu-id="fb39b-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="fb39b-110">Integreringen av kundedata innebærer derfor bare å harmonisere kundekonseptet mellom de to programmene.</span><span class="sxs-lookup"><span data-stu-id="fb39b-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="fb39b-111">Følgende illustrasjon viser kundedataflyten.</span><span class="sxs-lookup"><span data-stu-id="fb39b-111">The following illustration shows the customer data flow.</span></span>

![Kundedataflyt](media/dual-write-customer-data-flow.png)

<span data-ttu-id="fb39b-113">Kunder kan grovt klassifiseres i to typer: kommersielle/organisatoriske kunder og forbrukere/sluttbrukere.</span><span class="sxs-lookup"><span data-stu-id="fb39b-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="fb39b-114">Disse to kundetypene lagres og håndteres forskjellig i Finance and Operations og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="fb39b-114">These two types of customers are stored and handled differently in Finance and Operations and Dataverse.</span></span>

<span data-ttu-id="fb39b-115">I Finance and Operations administreres både kommersielle/organisatoriske kunder og forbrukere/sluttbrukere i én enkelt tabell som heter **CustTable** (CustCustomerV3Entity), og de klassifiseres basert på **Type**-attributtet.</span><span class="sxs-lookup"><span data-stu-id="fb39b-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="fb39b-116">(Hvis **Type** er satt til **Organisasjon**, er kunden en kommersiell/organisatorisk kunde, og hvis **Type** er satt til **Person**, er kunden en forbruker/sluttbruker.) Den primære kontaktpersoninformasjonen håndteres via SMMContactPersonEntity-tabellen.</span><span class="sxs-lookup"><span data-stu-id="fb39b-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity table.</span></span>

<span data-ttu-id="fb39b-117">I Dataverse styres kommersielle/organisatoriske kunder i kontotabellen og identifiseres som kunder når **RelationshipType**-attributtet er satt til **Kunde**.</span><span class="sxs-lookup"><span data-stu-id="fb39b-117">In Dataverse, commercial/organizational customers are mastered in the Account table and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="fb39b-118">Både forbrukere/sluttbrukere og kontaktpersonen representeres av Kontakt-tabellen.</span><span class="sxs-lookup"><span data-stu-id="fb39b-118">Both consumers/end users and the contact person are represented by the Contact table.</span></span> <span data-ttu-id="fb39b-119">Hvis du vil gi et klart skille mellom en forbruker/sluttbruker og en kontaktperson, har **Kontakt**-tabellen et boolsk flagg kalt **Kan selges**.</span><span class="sxs-lookup"><span data-stu-id="fb39b-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** table has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="fb39b-120">Når **Sellable** er **True**, er kontakten en forbruker/sluttbruker, og tilbud og ordrer kan opprettes for denne kontakten.</span><span class="sxs-lookup"><span data-stu-id="fb39b-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="fb39b-121">Når **Sellable** er **False**, er kontakten bare en primærkontaktperson for en kunde.</span><span class="sxs-lookup"><span data-stu-id="fb39b-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="fb39b-122">Når en ikke-salgbar kontakt deltar i en tilbuds- eller en ordreprosess er **Sellable** satt til **True** for å flagge kontakten som en salgbar kontakt.</span><span class="sxs-lookup"><span data-stu-id="fb39b-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="fb39b-123">En kontakt som har blitt en salgbar kontakt, forblir en salgbar kontakt.</span><span class="sxs-lookup"><span data-stu-id="fb39b-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="fb39b-124">Maler</span><span class="sxs-lookup"><span data-stu-id="fb39b-124">Templates</span></span>

<span data-ttu-id="fb39b-125">Kundedata inkluderer all informasjon om kunden, for eksempel kundegruppe, adresser, kontaktinformasjon, betalingsprofil, fakturaprofil og fordelsstatus.</span><span class="sxs-lookup"><span data-stu-id="fb39b-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="fb39b-126">En samling tabelltilordninger fungerer sammen under kundedatasamhandling, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="fb39b-126">A collection of table maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="fb39b-127">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="fb39b-127">Finance and Operations apps</span></span> | <span data-ttu-id="fb39b-128">Andre Dynamics 365-apper</span><span class="sxs-lookup"><span data-stu-id="fb39b-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="fb39b-129">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fb39b-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="fb39b-130">CDS-kontakter V2</span><span class="sxs-lookup"><span data-stu-id="fb39b-130">CDS Contacts V2</span></span>             | <span data-ttu-id="fb39b-131">kontakter</span><span class="sxs-lookup"><span data-stu-id="fb39b-131">contacts</span></span>                        | <span data-ttu-id="fb39b-132">Denne malen synkroniserer all primær, sekundær og tertiær informasjon, både for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="fb39b-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="fb39b-133">Kundegrupper</span><span class="sxs-lookup"><span data-stu-id="fb39b-133">Customer groups</span></span>             | <span data-ttu-id="fb39b-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="fb39b-134">msdyn_customergroups</span></span>            | <span data-ttu-id="fb39b-135">Denne malen synkroniserer kundegruppeinformasjon.</span><span class="sxs-lookup"><span data-stu-id="fb39b-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="fb39b-136">Kundebetalingsmåte</span><span class="sxs-lookup"><span data-stu-id="fb39b-136">Customer payment method</span></span>     | <span data-ttu-id="fb39b-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="fb39b-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="fb39b-138">Denne malen synkroniserer informasjon om kundebetalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="fb39b-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="fb39b-139">Kunder V3</span><span class="sxs-lookup"><span data-stu-id="fb39b-139">Customers V3</span></span>                | <span data-ttu-id="fb39b-140">kontoer</span><span class="sxs-lookup"><span data-stu-id="fb39b-140">accounts</span></span>                        | <span data-ttu-id="fb39b-141">Denne malen synkroniserer kundens hoveddata for kommersielle og organisatoriske kunder.</span><span class="sxs-lookup"><span data-stu-id="fb39b-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="fb39b-142">Kunder V3</span><span class="sxs-lookup"><span data-stu-id="fb39b-142">Customers V3</span></span>                | <span data-ttu-id="fb39b-143">kontakter</span><span class="sxs-lookup"><span data-stu-id="fb39b-143">contacts</span></span>                        | <span data-ttu-id="fb39b-144">Denne malen synkroniserer hoveddata for kunder for forbrukere og sluttbrukere.</span><span class="sxs-lookup"><span data-stu-id="fb39b-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="fb39b-145">Navnevedlegg</span><span class="sxs-lookup"><span data-stu-id="fb39b-145">Name affixes</span></span>                | <span data-ttu-id="fb39b-146">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="fb39b-146">msdyn_nameaffixes</span></span>               | <span data-ttu-id="fb39b-147">Denne malen synkroniserer referansedata for navnevedlegg, både for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="fb39b-147">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="fb39b-148">Betalingsdagslinjer, CDS V2</span><span class="sxs-lookup"><span data-stu-id="fb39b-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="fb39b-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="fb39b-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="fb39b-150">Denne malen synkroniserer referansedata om betalingsdagslinjer, både for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="fb39b-150">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="fb39b-151">Betalingsdager, CDS</span><span class="sxs-lookup"><span data-stu-id="fb39b-151">Payment days CDS</span></span>            | <span data-ttu-id="fb39b-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="fb39b-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="fb39b-153">Denne malen synkroniserer referansedata om betalingsdager, både for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="fb39b-153">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="fb39b-154">Linjer i betalingsplan</span><span class="sxs-lookup"><span data-stu-id="fb39b-154">Payment schedule lines</span></span>      | <span data-ttu-id="fb39b-155">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="fb39b-155">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="fb39b-156">Synkroniserer referansedata om betalingsplanlinjer, både for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="fb39b-156">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="fb39b-157">Betalingsplan</span><span class="sxs-lookup"><span data-stu-id="fb39b-157">Payment schedule</span></span>            | <span data-ttu-id="fb39b-158">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="fb39b-158">msdyn_paymentschedules</span></span>          | <span data-ttu-id="fb39b-159">Denne malen synkroniserer referansedata om betalingsplan, både for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="fb39b-159">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="fb39b-160">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="fb39b-160">Terms of payment</span></span>            | <span data-ttu-id="fb39b-161">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="fb39b-161">msdyn_paymentterms</span></span>              | <span data-ttu-id="fb39b-162">Denne malen synkroniserer referansedata om betalingsbetingelser, både for kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="fb39b-162">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
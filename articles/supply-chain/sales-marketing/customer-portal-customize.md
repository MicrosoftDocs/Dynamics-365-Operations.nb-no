---
title: Tilpasse og bruke kundeportalen
description: Dette emnet beskriver hvordan du tilpasser kundeportalen etter at den er lagt til i systemet.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 1e491100bc24718b8e5bc0f62de241835787f7ea
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980862"
---
# <a name="customize-and-use-the-customer-portal"></a><span data-ttu-id="f7f76-103">Tilpasse og bruke kundeportalen</span><span class="sxs-lookup"><span data-stu-id="f7f76-103">Customize and use the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f7f76-104">Dette emnet beskriver de ulike sidene som er tilgjengelige som standard i kundeportalen.</span><span class="sxs-lookup"><span data-stu-id="f7f76-104">This topic describes the different pages that available in the Customer portal out of the box.</span></span> <span data-ttu-id="f7f76-105">Den forklarer funksjonene til sidene samt hvordan du kan tilpasse dem.</span><span class="sxs-lookup"><span data-stu-id="f7f76-105">It explains what the pages do and how you can customize them.</span></span>

<span data-ttu-id="f7f76-106">Kundeportalen tilbyr enkelte nettsider og handlinger som standard.</span><span class="sxs-lookup"><span data-stu-id="f7f76-106">The Customer portal offers a few webpages and actions out of the box.</span></span> <span data-ttu-id="f7f76-107">Følgende områdekart gir en oversikt over disse nettsidene og handlingene, og rollene som kan utføre handlingene.</span><span class="sxs-lookup"><span data-stu-id="f7f76-107">The following site map provides an overview of those webpages and actions, and the roles that can perform the actions.</span></span>

<span data-ttu-id="f7f76-108">![Områdekart for kundeportal](media/customer-portal-site-map.png "Områdekart for kundeportal")</span><span class="sxs-lookup"><span data-stu-id="f7f76-108">![Customer portal site map](media/customer-portal-site-map.png "Customer portal site map")</span></span>

## <a name="typical-customizations"></a><span data-ttu-id="f7f76-109">Vanlige tilpasninger</span><span class="sxs-lookup"><span data-stu-id="f7f76-109">Typical customizations</span></span>

<span data-ttu-id="f7f76-110">Følgende emner hjelper deg å lære grunnleggende kunnskaper om Power Apps-portaler samt hvordan du kan tilpasse portaler:</span><span class="sxs-lookup"><span data-stu-id="f7f76-110">The following topics will help you learn the basics about Power Apps portals and how you can customize portals:</span></span>

- <span data-ttu-id="f7f76-111">[Arbeide med maler](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates) – dette emnet gir en generell oversikt over hvordan Power Apps-portaler fungerer, og hvordan du kan utføre enkle tilpasninger av portaler.</span><span class="sxs-lookup"><span data-stu-id="f7f76-111">[Work with templates](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates) – This topic provides a general overview of how Power Apps portals works and how you can do simple customizations of portals.</span></span>
- <span data-ttu-id="f7f76-112">[Behandle portalinnhold](https://docs.microsoft.com/dynamics365/portals/manage-portal-content) – dette emnet beskriver hvordan du kan administrere og tilpasse innholdet på portalen.</span><span class="sxs-lookup"><span data-stu-id="f7f76-112">[Manage portal content](https://docs.microsoft.com/dynamics365/portals/manage-portal-content) – This topic explains how you can manage and customize the content that you surface in your portal.</span></span>
- <span data-ttu-id="f7f76-113">[Rediger CSS](https://docs.microsoft.com/powerapps/maker/portals/edit-css) – dette emnet hjelper deg med å utføre mer avanserte tilpasninger i brukergrensesnittet til portalen.</span><span class="sxs-lookup"><span data-stu-id="f7f76-113">[Edit CSS](https://docs.microsoft.com/powerapps/maker/portals/edit-css) – This topic helps you make more complex customizations to the user interface (UI) of your portal.</span></span>
- <span data-ttu-id="f7f76-114">[Opprett et tema for portalen](https://docs.microsoft.com/dynamics365/portals/create-theme) – dette emnet hjelper deg med å opprette et brukergrensesnitt-tema for portalen.</span><span class="sxs-lookup"><span data-stu-id="f7f76-114">[Create a theme for your portal](https://docs.microsoft.com/dynamics365/portals/create-theme) – This topic helps you create a UI theme for your portal.</span></span>
- <span data-ttu-id="f7f76-115">[Opprette og vise portalinnhold enkelt](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content) – dette emnet hjelper deg med å styre de underliggende dataene og tabellene som du bruker for portalen.</span><span class="sxs-lookup"><span data-stu-id="f7f76-115">[Create and expose portal content easily](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content) – This topic helps you manage the underlying data and tables that you use for your portal.</span></span>
- <span data-ttu-id="f7f76-116">[Konfigurere en kontakt for bruk på en portal](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) – dette emnet forklarer hvordan du oppretter og tilpasser brukerroller, og hvordan sikkerhet og godkjenning fungerer i Power Apps-portaler.</span><span class="sxs-lookup"><span data-stu-id="f7f76-116">[Configure a contact for use on a portal](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) – This topic explains how to create and customize user roles, and how security and authentication work in Power Apps portals.</span></span>
- <span data-ttu-id="f7f76-117">[Konfigurere merknader for tabellskjemaer og nettskjemaer på portaler](https://docs.microsoft.com/powerapps/maker/portals/configure-notes) – dette emnet forklarer hvordan du legger til dokumenter og ekstra lagringsplass på portalen.</span><span class="sxs-lookup"><span data-stu-id="f7f76-117">[Configure notes for table forms and web forms on portals](https://docs.microsoft.com/powerapps/maker/portals/configure-notes) – This topic explains how to add documents and additional storage to your portal.</span></span>
- <span data-ttu-id="f7f76-118">[Feilhåndtering for portalnettstedet](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log) – dette emnet forklarer hvordan du viser feillogger for portaler og lagrer dem i Microsoft Azure Blob Storage-kontoen.</span><span class="sxs-lookup"><span data-stu-id="f7f76-118">[Error handling for portal website](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log) – This topic explains how to view portal error logs and store them in your Microsoft Azure Blob storage account.</span></span>

## <a name="customize-the-order-creation-process"></a><span data-ttu-id="f7f76-119">Tilpasse prosessen for ordreopprettelse</span><span class="sxs-lookup"><span data-stu-id="f7f76-119">Customize the order creation process</span></span>

<span data-ttu-id="f7f76-120">Når en bruker sender en ordre ved hjelp av kundeportalen, synkroniseres ordren automatisk til det tilsvarende Dynamics 365 Supply Chain Management-miljøet.</span><span class="sxs-lookup"><span data-stu-id="f7f76-120">When a user submits an order by using the Customer portal, the order is automatically synced to the corresponding Dynamics 365 Supply Chain Management environment.</span></span> <span data-ttu-id="f7f76-121">Siden brukeren er en ekstern kunde, blir noe påkrevd informasjon med hensikt skjult fra ham eller henne.</span><span class="sxs-lookup"><span data-stu-id="f7f76-121">Because the user is an external customer, some required information is intentionally hidden from him or her.</span></span> <span data-ttu-id="f7f76-122">Denne informasjonen fylles automatisk ut når skjemaet sendes inn.</span><span class="sxs-lookup"><span data-stu-id="f7f76-122">This information will automatically be filled in when the form is submitted.</span></span>

<span data-ttu-id="f7f76-123">Denne delen viser hvordan du bør konfigurere kontakter for å unngå feil.</span><span class="sxs-lookup"><span data-stu-id="f7f76-123">This section shows how you should set up contacts to avoid errors.</span></span> <span data-ttu-id="f7f76-124">Den forklarer felter som angis automatisk, og hvordan du kan endre verdien i disse feltene hvis du trenger det.</span><span class="sxs-lookup"><span data-stu-id="f7f76-124">It explains fields that are automatically set and how you can modify the value of those fields if you must.</span></span>

### <a name="the-out-of-box-order-creation-process"></a><span data-ttu-id="f7f76-125">Standardprosessen for ordreopprettelse</span><span class="sxs-lookup"><span data-stu-id="f7f76-125">The out-of-box order creation process</span></span>

<span data-ttu-id="f7f76-126">Her er standardtrinnene for å sende en ordre fra kundeportalen.</span><span class="sxs-lookup"><span data-stu-id="f7f76-126">Here are the standard steps for submitting an order from the Customer portal.</span></span>

1. <span data-ttu-id="f7f76-127">På hjemmesiden velger du **Opprett ordre**-flisen for å åpne **Opprett ordre**-veiviseren.</span><span class="sxs-lookup"><span data-stu-id="f7f76-127">On the home page, select the **Create order** tile to open the **Create Order** wizard.</span></span>
1. <span data-ttu-id="f7f76-128">På **Ordreinformasjon**-siden angir du følgende felter:</span><span class="sxs-lookup"><span data-stu-id="f7f76-128">On the **Order Information** page, set the following fields:</span></span>

    - <span data-ttu-id="f7f76-129">**Ønsket leveringsdato** – angi leveringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="f7f76-129">**Requested receipt date** – Specify the date of delivery.</span></span>
    - <span data-ttu-id="f7f76-130">**Leveringsadresse** – angi adressen som ordren skal leveres til.</span><span class="sxs-lookup"><span data-stu-id="f7f76-130">**Delivery address** – Enter the address that the order should be delivered to.</span></span>
    - <span data-ttu-id="f7f76-131">**Firma** – velg navnet på kundens firma.</span><span class="sxs-lookup"><span data-stu-id="f7f76-131">**Company** – Select the name of the customer company.</span></span> <span data-ttu-id="f7f76-132">Dette feltet angis automatisk for brukere som ikke er administratorer.</span><span class="sxs-lookup"><span data-stu-id="f7f76-132">This field is automatically set for non-admin users.</span></span>
    - <span data-ttu-id="f7f76-133">**Rekvisisjonsnummer** – angi rekvisisjonsnummeret for ordren.</span><span class="sxs-lookup"><span data-stu-id="f7f76-133">**Requisition number** – Enter the requisition number of the order.</span></span> <span data-ttu-id="f7f76-134">Dette feltet er ikke obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f7f76-134">This field isn't required.</span></span>
    - <span data-ttu-id="f7f76-135">**Leveringsland/-område** – angi landet eller området som varene skal leveres til.</span><span class="sxs-lookup"><span data-stu-id="f7f76-135">**Ship to country/region** – Enter the country or region that the items will be delivered to.</span></span> <span data-ttu-id="f7f76-136">Dette feltet angis automatisk for brukere som ikke er administratorer.</span><span class="sxs-lookup"><span data-stu-id="f7f76-136">This field is automatically set for non-admin users.</span></span>

    <span data-ttu-id="f7f76-137">![Ordreinformasjonsside](media/customer-portal-order-information.png "Ordreinformasjonsside")</span><span class="sxs-lookup"><span data-stu-id="f7f76-137">![Order Information page](media/customer-portal-order-information.png "Order Information page")</span></span>

1. <span data-ttu-id="f7f76-138">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="f7f76-138">Select **Next**.</span></span>
1. <span data-ttu-id="f7f76-139">På **Varer**-siden velger du **Legg til vare**.</span><span class="sxs-lookup"><span data-stu-id="f7f76-139">On the **Items** page, select **Add Item**.</span></span>

    <span data-ttu-id="f7f76-140">![Varer-side](media/customer-portal-items.png "Varer-side")</span><span class="sxs-lookup"><span data-stu-id="f7f76-140">![Items page](media/customer-portal-items.png "Items page")</span></span>

1. <span data-ttu-id="f7f76-141">I **Vareinformasjon**-dialogboksen angir du følgende felt:</span><span class="sxs-lookup"><span data-stu-id="f7f76-141">In the **Item Information** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="f7f76-142">**Produktnavn** – finn og velg et produkt som skal legges til i ordren.</span><span class="sxs-lookup"><span data-stu-id="f7f76-142">**Product Name** – Find and select a product to add to the order.</span></span>
    - <span data-ttu-id="f7f76-143">**Antall** – angi antallet for det valgte produktet.</span><span class="sxs-lookup"><span data-stu-id="f7f76-143">**Quantity** – Enter the quantity of the selected product.</span></span>
    - <span data-ttu-id="f7f76-144">**Enhet** – Angi måleenheten (f.eks. **per.**, **kg** eller **boks**).</span><span class="sxs-lookup"><span data-stu-id="f7f76-144">**Unit** – Specify the unit of measure (for example, **ea.**, **kgs**, or **box**).</span></span>
    - <span data-ttu-id="f7f76-145">**Estimert nettobeløp** – verdien beregnes som den estimerte prisen på varen × antallet for den valgte enheten.</span><span class="sxs-lookup"><span data-stu-id="f7f76-145">**Estimated net amount** – The value is calculated as the estimated price of the item × the quantity for the selected unit.</span></span>

    <span data-ttu-id="f7f76-146">![Dialogboksen Vareinformasjon](media/customer-portal-item-information.png "Dialogboksen Vareinformasjon")</span><span class="sxs-lookup"><span data-stu-id="f7f76-146">![Item Information dialog box](media/customer-portal-item-information.png "Item Information dialog box")</span></span>

1. <span data-ttu-id="f7f76-147">Velg **Send** for å legge til varen i ordren.</span><span class="sxs-lookup"><span data-stu-id="f7f76-147">Select **Submit** to add the item to the order.</span></span>
1. <span data-ttu-id="f7f76-148">Gjenta trinn 4 til 6 til du har lagt til alle varene du vil bestille.</span><span class="sxs-lookup"><span data-stu-id="f7f76-148">Repeat steps 4 through 6 until you've added all the items that you want to order.</span></span>
1. <span data-ttu-id="f7f76-149">Når du er ferdig med å legge til varer, velger du **Neste** på **Varer**-siden.</span><span class="sxs-lookup"><span data-stu-id="f7f76-149">When you've finished adding items, select **Next** on the **Items** page.</span></span>
1. <span data-ttu-id="f7f76-150">På **Ordre informasjon**-siden ser du et sammendrag av ordren.</span><span class="sxs-lookup"><span data-stu-id="f7f76-150">The **Order Information** page provides a summary of the order.</span></span> <span data-ttu-id="f7f76-151">Se gjennom ordreinnholdet og leveringsdetaljene.</span><span class="sxs-lookup"><span data-stu-id="f7f76-151">Review the order contents and delivery details.</span></span> <span data-ttu-id="f7f76-152">Hvis alt ser riktig ut, velger du **Send** for å sende ordren.</span><span class="sxs-lookup"><span data-stu-id="f7f76-152">If everything looks correct, select **Submit** to submit the order.</span></span>

    <span data-ttu-id="f7f76-153">![Ordreinformasjonsside](media/customer-portal-order-submit.png "Ordreinformasjonsside")</span><span class="sxs-lookup"><span data-stu-id="f7f76-153">![Order Information page](media/customer-portal-order-submit.png "Order Information page")</span></span>

### <a name="standard-data-setup"></a><span data-ttu-id="f7f76-154">Standard datakonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="f7f76-154">Standard data setup</span></span>

<span data-ttu-id="f7f76-155">For å bidra til en enklere brukeropplevelse fyller kundeportalen automatisk ut verdier for flere obligatoriske felt.</span><span class="sxs-lookup"><span data-stu-id="f7f76-155">To help ensure a smooth user experience, the Customer portal automatically fills in values for several required fields.</span></span> <span data-ttu-id="f7f76-156">Disse verdiene er basert på informasjon i kontaktposten for kunden som sender ordren.</span><span class="sxs-lookup"><span data-stu-id="f7f76-156">These values are based on information in the contact record of the customer who is submitting the order.</span></span>

<span data-ttu-id="f7f76-157">For hver [kontaktrad](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) som tilhører en kunde, og som skal bruke kundeportalen til å sende ordrer, må det angis verdier for følgende obligatoriske felt.</span><span class="sxs-lookup"><span data-stu-id="f7f76-157">For each [contact row](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) that belongs to a customer who will use the Customer portal to submit orders, values must be specified for the following required fields.</span></span> <span data-ttu-id="f7f76-158">Hvis ikke oppstår det feil.</span><span class="sxs-lookup"><span data-stu-id="f7f76-158">Otherwise, errors will occur.</span></span>

- <span data-ttu-id="f7f76-159">**Firma** – Den juridiske enheten som ordren tilhører.</span><span class="sxs-lookup"><span data-stu-id="f7f76-159">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="f7f76-160">**Potensiell kunde** – Kundekontoen som er knyttet til den valgte ordren</span><span class="sxs-lookup"><span data-stu-id="f7f76-160">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="f7f76-161">**Prisliste** – Den egendefinerte prislisten for kunden</span><span class="sxs-lookup"><span data-stu-id="f7f76-161">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="f7f76-162">**Valuta** – Valutaen prisen oppgis i</span><span class="sxs-lookup"><span data-stu-id="f7f76-162">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="f7f76-163">**Leveringsland/-område** – Landet eller området som varene skal leveres til</span><span class="sxs-lookup"><span data-stu-id="f7f76-163">**Ship to country/region** – The country or region that the items will be delivered to</span></span>

<span data-ttu-id="f7f76-164">Følgende felt angis automatisk for salgsordretabellen:</span><span class="sxs-lookup"><span data-stu-id="f7f76-164">The following fields are automatically set for the sales order table:</span></span>

- <span data-ttu-id="f7f76-165">**Språk** – Språket for ordren (som standard hentes verdien fra kontaktposten.)</span><span class="sxs-lookup"><span data-stu-id="f7f76-165">**Language** – The language of the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="f7f76-166">**Leveringsland/-område** – landet eller området som varene skal leveres til (som standard hentes verdien fra kontaktposten.)</span><span class="sxs-lookup"><span data-stu-id="f7f76-166">**Ship to country/region** – The country or region that the items will be delivered to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="f7f76-167">**Kontaktperson** – Brukeren som kan kontaktes for informasjon om ordren (som standard hentes verdien fra kontaktposten.)</span><span class="sxs-lookup"><span data-stu-id="f7f76-167">**Contact person** – The user who can be contacted for information about the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="f7f76-168">**Firma** – Den juridiske enheten som ordren tilhører (som standard hentes verdien fra kontaktposten.)</span><span class="sxs-lookup"><span data-stu-id="f7f76-168">**Company** – The legal entity that the order belongs to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="f7f76-169">**Potensiell kunde** – Kundekontoen som er knyttet til ordren (som standard hentes verdien fra kontaktposten.)</span><span class="sxs-lookup"><span data-stu-id="f7f76-169">**Potential customer** – The customer account that is associated with the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="f7f76-170">**Fakturakunde** – Faktureringskontoen for ordren (standardverdien er den potensielle kunden fra kontaktposten.)</span><span class="sxs-lookup"><span data-stu-id="f7f76-170">**Invoice customer** – The billing account of the order (The default value is the potential customer from the contact record.)</span></span>
- <span data-ttu-id="f7f76-171">**Salgsordrenavn** – navnet på salgsordren (standardverdien er **salgsordre**.)</span><span class="sxs-lookup"><span data-stu-id="f7f76-171">**Sales order name** – The name of the sales order (The default value is **sales order**.)</span></span>
- <span data-ttu-id="f7f76-172">**Valuta** – Valutaen prisen oppgis i (som standard hentes verdien fra kontaktposten.)</span><span class="sxs-lookup"><span data-stu-id="f7f76-172">**Currency** – The currency of the price (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="f7f76-173">**Prisliste** – Den egendefinerte prislisten for kunden (som standard hentes verdien fra kontaktposten.)</span><span class="sxs-lookup"><span data-stu-id="f7f76-173">**Price list** – The custom price list for the customer (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="f7f76-174">**Beskrivelse av leveringsadresse** – leveringsadressen for salgsordren (standardverdien er **beskrivelse av leveringsadresse**.)</span><span class="sxs-lookup"><span data-stu-id="f7f76-174">**Delivery address description** – The delivery address of the sales order (The default value is **delivery address description**.)</span></span>

### <a name="modify-the-order-creation-process"></a><span data-ttu-id="f7f76-175">Endre prosessen for ordreopprettelse</span><span class="sxs-lookup"><span data-stu-id="f7f76-175">Modify the order creation process</span></span>

<span data-ttu-id="f7f76-176">Du kan fritt endre utseendet og brukergrensesnittet til kundeportalen hvis du ikke endrer prosessen for grunnleggende ordreoppretting.</span><span class="sxs-lookup"><span data-stu-id="f7f76-176">You can freely modify the appearance and UI of the Customer portal if you don't change the basic order creation process.</span></span> <span data-ttu-id="f7f76-177">Hvis du vil endre prosessen for oppretting av ordrer, er det noen få ting du bør huske på.</span><span class="sxs-lookup"><span data-stu-id="f7f76-177">If you want to change the order creation process, there are a few points that you must keep in mind.</span></span>

<span data-ttu-id="f7f76-178">Ikke fjern følgende kolonner fra salgsordreenheten i Microsoft Dataverse, siden de kreves for å opprette en salgsordre med dobbel skriving:</span><span class="sxs-lookup"><span data-stu-id="f7f76-178">Don't remove the following columns from the sales order table in Microsoft Dataverse, because they are required to create a sales order in dual-write:</span></span>

- <span data-ttu-id="f7f76-179">**Firma** – Den juridiske enheten som ordren tilhører.</span><span class="sxs-lookup"><span data-stu-id="f7f76-179">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="f7f76-180">**Navn** – navnet på salgsordren</span><span class="sxs-lookup"><span data-stu-id="f7f76-180">**Name** – The name of the sales order</span></span>
- <span data-ttu-id="f7f76-181">**Valuta** – Valutaen prisen oppgis i</span><span class="sxs-lookup"><span data-stu-id="f7f76-181">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="f7f76-182">**Prisliste** – Den egendefinerte prislisten for kunden</span><span class="sxs-lookup"><span data-stu-id="f7f76-182">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="f7f76-183">**Leveringsland/-område** – Landet eller området som varene skal leveres til</span><span class="sxs-lookup"><span data-stu-id="f7f76-183">**Ship to country/region** – The country or region that the items will be delivered to</span></span>
- <span data-ttu-id="f7f76-184">**Potensiell kunde** – Kundekontoen som er knyttet til den valgte ordren</span><span class="sxs-lookup"><span data-stu-id="f7f76-184">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="f7f76-185">**Språk** – språket i ordren (dette språket er vanligvis språket til den potensielle kunden.)</span><span class="sxs-lookup"><span data-stu-id="f7f76-185">**Language** – The language of the order (Typically, this language is the language of the potential customer.)</span></span>
- <span data-ttu-id="f7f76-186">**Beskrivelse av leveringsadresse** – leveringsadressen for salgsordren</span><span class="sxs-lookup"><span data-stu-id="f7f76-186">**Delivery address description** – The delivery address of the sales order</span></span>

<span data-ttu-id="f7f76-187">Følgende kolonner er obligatoriske for varer:</span><span class="sxs-lookup"><span data-stu-id="f7f76-187">For items, the following columns are required:</span></span>

- <span data-ttu-id="f7f76-188">**Produkt** – produktet som skal bestilles</span><span class="sxs-lookup"><span data-stu-id="f7f76-188">**Product** – The product to order</span></span>
- <span data-ttu-id="f7f76-189">**Antall** – antallet av det valgte produktet</span><span class="sxs-lookup"><span data-stu-id="f7f76-189">**Quantity** – The quantity of the selected product</span></span>
- <span data-ttu-id="f7f76-190">**Enhet** – måleenheten (f.eks. **per.**, **kg** eller **boks**)</span><span class="sxs-lookup"><span data-stu-id="f7f76-190">**Unit** – The unit of measure (for example, **ea.**, **kgs**, or **box**)</span></span>
- <span data-ttu-id="f7f76-191">**Leveringsland/-område** – landet eller området det skal leveres til</span><span class="sxs-lookup"><span data-stu-id="f7f76-191">**Ship to country/region** – The country or region of delivery</span></span>
- <span data-ttu-id="f7f76-192">**Beskrivelse av leveringsadresse** – leveringsadressen for ordren</span><span class="sxs-lookup"><span data-stu-id="f7f76-192">**Delivery address description** – The delivery address of the order</span></span>

<span data-ttu-id="f7f76-193">Du må kontrollere at kundeportalen på en eller annen måte sender inn verdier for alle disse kolonnene.</span><span class="sxs-lookup"><span data-stu-id="f7f76-193">You must make sure that your Customer portal somehow submits values for all these columns.</span></span>

<span data-ttu-id="f7f76-194">Hvis du vil legge til kolonner på siden eller fjerne kolonner, kan du se [Opprette eller redigere hurtigopprettingsskjemaer for en strømlinjeformet dataregistreringsopplevelse](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span><span class="sxs-lookup"><span data-stu-id="f7f76-194">If you want to add columns to the page, or remove columns, see [Create or edit quick create forms for a streamlined data entry experience](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span></span>

<span data-ttu-id="f7f76-195">Hvis du vil endre hvordan kolonner forhåndsinnstilles og hvordan verdier angis når siden lagres, kan du se følgende informasjon i dokumentasjonen for Power Apps-portaler:</span><span class="sxs-lookup"><span data-stu-id="f7f76-195">If you want to change how columns are preset and how values are set when the page is saved, see the following information in the Power Apps portals documentation:</span></span>

- [<span data-ttu-id="f7f76-196">Forhåndsutfylle felt</span><span class="sxs-lookup"><span data-stu-id="f7f76-196">Prepopulate field</span></span>](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [<span data-ttu-id="f7f76-197">Angi verdi ved lagring</span><span class="sxs-lookup"><span data-stu-id="f7f76-197">Set Value On Save</span></span>](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a><span data-ttu-id="f7f76-198">Tilpasse startsiden</span><span class="sxs-lookup"><span data-stu-id="f7f76-198">Customize the home page</span></span>

<span data-ttu-id="f7f76-199">Alle kontrollene i kundeportalen er innebygde Power Apps-portalkontroller.</span><span class="sxs-lookup"><span data-stu-id="f7f76-199">All the controls in the Customer portal are built-in Power Apps portals controls.</span></span> <span data-ttu-id="f7f76-200">Du kan tilpasse dem ved å følge fremgangsmåten i [Opprette en side](https://docs.microsoft.com/powerapps/maker/portals/compose-page) i Power Apps-portaldokumentasjonen.</span><span class="sxs-lookup"><span data-stu-id="f7f76-200">You can customize them by following the steps in [Compose a page](https://docs.microsoft.com/powerapps/maker/portals/compose-page) in the Power Apps portals documentation.</span></span>

<span data-ttu-id="f7f76-201">Den eneste egendefinerte kontrollen som er inkludert i kundeportalmalen, brukes til å opprette flisene på startsiden.</span><span class="sxs-lookup"><span data-stu-id="f7f76-201">The only custom control that is included in the Customer portal template is used to create the tiles on the home page.</span></span>

<span data-ttu-id="f7f76-202">![Fliser på startsiden](media/customer-portal-home-page-tiles.png "Fliser på startsiden")</span><span class="sxs-lookup"><span data-stu-id="f7f76-202">![Tiles on the home page](media/customer-portal-home-page-tiles.png "Tiles on the home page")</span></span>

<span data-ttu-id="f7f76-203">Følg fremgangsmåten nedenfor for å endre flisene.</span><span class="sxs-lookup"><span data-stu-id="f7f76-203">To modify the tiles, follow these steps.</span></span>

1. <span data-ttu-id="f7f76-204">Åpne [Portal Management-appen](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal).</span><span class="sxs-lookup"><span data-stu-id="f7f76-204">Open the [Portal Management app](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal).</span></span>
1. <span data-ttu-id="f7f76-205">Velg **Sidemaler** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="f7f76-205">In the navigation pane on the left, select **Page Templates**.</span></span>

    <span data-ttu-id="f7f76-206">![Navigasjonsrute for Portal Management](media/customer-portal-nav.png "Navigasjonsrute for Portal Management")</span><span class="sxs-lookup"><span data-stu-id="f7f76-206">![Portal Management navigation pane](media/customer-portal-nav.png "Portal Management navigation pane")</span></span>

1. <span data-ttu-id="f7f76-207">Velg sidemalen som heter **Hjem**.</span><span class="sxs-lookup"><span data-stu-id="f7f76-207">Select the page template that is named **Home**.</span></span>
1. <span data-ttu-id="f7f76-208">I **Webmal**-feltet velger du **Hjem**-koblingen for å åpne kildekoden for denne siden.</span><span class="sxs-lookup"><span data-stu-id="f7f76-208">In the **Web Template** field, select the **Home** link to open the source code for that page.</span></span>

    <span data-ttu-id="f7f76-209">![Webmal-felt](media/customer-portal-web-template.png "Webmal-felt")</span><span class="sxs-lookup"><span data-stu-id="f7f76-209">![Web Template field](media/customer-portal-web-template.png "Web Template field")</span></span>

1. <span data-ttu-id="f7f76-210">Nå skal du kunne se alle kildekodene for hjemmesiden, og du kan endre dem slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="f7f76-210">You should now see all the source code for the home page and can modify it as you require.</span></span>

## <a name="resources"></a><span data-ttu-id="f7f76-211">Ressurser</span><span class="sxs-lookup"><span data-stu-id="f7f76-211">Resources</span></span>

<span data-ttu-id="f7f76-212">Hvis du vil ha mer informasjon om hvordan du kan definere og tilpasse kundeportalen, kan du se følgende ressurser:</span><span class="sxs-lookup"><span data-stu-id="f7f76-212">To learn more about how you can set up and customize the Customer portal, see the following resources:</span></span>

- [<span data-ttu-id="f7f76-213">Dokumentasjon for Power Apps-portaler</span><span class="sxs-lookup"><span data-stu-id="f7f76-213">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="f7f76-214">Dokumentasjon for dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="f7f76-214">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [<span data-ttu-id="f7f76-215">Om portalens livssyklus</span><span class="sxs-lookup"><span data-stu-id="f7f76-215">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="f7f76-216">Oppgradere en portal</span><span class="sxs-lookup"><span data-stu-id="f7f76-216">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="f7f76-217">Overføre en portalkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="f7f76-217">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="f7f76-218">Administrasjon livssyklus for løsning: Dynamics 365 for Customer Engagement-apper</span><span class="sxs-lookup"><span data-stu-id="f7f76-218">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)

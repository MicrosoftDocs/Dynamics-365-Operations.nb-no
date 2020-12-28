---
title: Malstykklister
description: En malstykkliste gir en standardisert liste over komponentene for serviceobjekter som blir vedlikeholdt regelmessig.
author: ShylaThompson
manager: tfehr
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88e732f64b389acafee23427594225dfacda71cc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434361"
---
# <a name="template-boms"></a><span data-ttu-id="12009-103">Malstykklister</span><span class="sxs-lookup"><span data-stu-id="12009-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="12009-104">En malstykkliste gir deg en standardisert liste over komponentene for serviceobjekter som blir vedlikeholdt regelmessig.</span><span class="sxs-lookup"><span data-stu-id="12009-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="12009-105">Komponentene som er oppført i malstykklisten, representerer de individuelle delkomponentene til serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="12009-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="12009-106">Ved å bruke en malstykkliste på et serviceobjekt, kan du holde oversikt over delkomponentene som er erstattet på serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="12009-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="12009-107">Du kan bruke en malstykkliste på en serviceavtale eller en serviceordre ved å knytte den til en serviceobjektforbindelse.</span><span class="sxs-lookup"><span data-stu-id="12009-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="12009-108">Du kan bare bruke én malstykkliste på et serviceobjekt.</span><span class="sxs-lookup"><span data-stu-id="12009-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="12009-109">Opprette en malstykkliste</span><span class="sxs-lookup"><span data-stu-id="12009-109">Create a template BOM</span></span>

<span data-ttu-id="12009-110">Tabellen nedenfor inneholder informasjon om de forskjellige metodene du kan bruke til å opprette en malstykkliste.</span><span class="sxs-lookup"><span data-stu-id="12009-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12009-111">Metode</span><span class="sxs-lookup"><span data-stu-id="12009-111">Method</span></span></p></th>
<th><p><span data-ttu-id="12009-112">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="12009-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12009-113">Produksjon</span><span class="sxs-lookup"><span data-stu-id="12009-113">Production</span></span></p></td>
<td><p><span data-ttu-id="12009-114">Malstykklisten er basert på en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="12009-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="12009-115">Dette alternativet er bare tilgjengelig hvis du jobber i et produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="12009-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="12009-116">Fordelen er at du har en aktuell, detaljert oppføring av komponentene som utgjør en vare.</span><span class="sxs-lookup"><span data-stu-id="12009-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12009-117">Vare BOM</span><span class="sxs-lookup"><span data-stu-id="12009-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="12009-118">Malstykklisten er basert på en varestykkliste.</span><span class="sxs-lookup"><span data-stu-id="12009-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="12009-119">Varestykklisten, i motsetning til produksjonsstykklisten, er en statisk liste over komponentene som utgjør en vare.</span><span class="sxs-lookup"><span data-stu-id="12009-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12009-120">Eksisterende mal</span><span class="sxs-lookup"><span data-stu-id="12009-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="12009-121">Malen er basert på en eksisterende malstykkliste.</span><span class="sxs-lookup"><span data-stu-id="12009-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12009-122">Manuell</span><span class="sxs-lookup"><span data-stu-id="12009-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="12009-123">Hvis du vet hvilke reservedeler som vanligvis erstattes på et serviceobjekt, kan du opprette malstykklisten manuelt.</span><span class="sxs-lookup"><span data-stu-id="12009-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="12009-124">Denne metoden bidrar til å sikre at komponentene som er inkludert i malen, gjenspeiler de faktiske kravene til arbeidsplassen.</span><span class="sxs-lookup"><span data-stu-id="12009-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="12009-125">Bruk malstykklisten på en serviceavtale eller en serviceordre</span><span class="sxs-lookup"><span data-stu-id="12009-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="12009-126">Du kan bruke en malstykkliste kan brukes for en serviceavtale og en serviceordre, eller begge deler.</span><span class="sxs-lookup"><span data-stu-id="12009-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="12009-127">Serviceavtalen dekker vanligvis et langsiktig forhold med en kunde.</span><span class="sxs-lookup"><span data-stu-id="12009-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="12009-128">Loggen for erstatninger som er registrert i servicestykkmalen, er nyttige data å ha for serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="12009-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="12009-129">Du kan også bruke en malstykkliste på en serviceordre for å registrere historikken for servicen som er utført på et serviceobjekt.</span><span class="sxs-lookup"><span data-stu-id="12009-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="12009-130">Kopiere loggen til en servicestykkliste</span><span class="sxs-lookup"><span data-stu-id="12009-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="12009-131">Du kan kopiere loggen til en servicestykklistelinje fra en serviceavtale til en annen serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="12009-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="12009-132">Når du kopierer serviceloggen mellom serviceavtaler, kan du beholde erstatningsoppføringen for en vare.</span><span class="sxs-lookup"><span data-stu-id="12009-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="12009-133">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="12009-133">**Example**</span></span>

<span data-ttu-id="12009-134">Du har angitt en serviceavtale på tre år for bilen til en kunde.</span><span class="sxs-lookup"><span data-stu-id="12009-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="12009-135">I den perioden blir kunden vant til firmaets gode service som firmaet tilbyr.</span><span class="sxs-lookup"><span data-stu-id="12009-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="12009-136">Derfor når avtalen utløper, ønsker kunden å sette opp en ny.</span><span class="sxs-lookup"><span data-stu-id="12009-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="12009-137">Du kan nå forhandle bedre betingelser for firmaet.</span><span class="sxs-lookup"><span data-stu-id="12009-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="12009-138">Ettersom oppføringen av erstattede komponenter kan være nyttig i fremtiden, kopierer du loggen for servicestykklisten til den nye avtalen.</span><span class="sxs-lookup"><span data-stu-id="12009-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="12009-139">Endre malstykklisten</span><span class="sxs-lookup"><span data-stu-id="12009-139">Modify the template BOM</span></span>

<span data-ttu-id="12009-140">Hvis en malstykkliste ikke er knyttet til et serviceobjekt, kan du endre eller slette linjer i den.</span><span class="sxs-lookup"><span data-stu-id="12009-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="12009-141">Når malstykklisten er knyttet til et serviceobjekt, kan du bare endre den lokale versjonen av stykklisten.</span><span class="sxs-lookup"><span data-stu-id="12009-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="12009-142">Hvis du vil duplisere oppsettet av en lokal versjon av malstykklisten, kan du opprette en ny malstykkliste basert på den lokale versjonen.</span><span class="sxs-lookup"><span data-stu-id="12009-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="12009-143">Hvis du vil ha mer informasjon, se [Endre en servicestykkliste](modify-service-bom.md).</span><span class="sxs-lookup"><span data-stu-id="12009-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="12009-144">Hvis du erstatter en vare i stykklisten, kan du registrere erstatningen på stykklistelinjen i stykklisteutformeren.</span><span class="sxs-lookup"><span data-stu-id="12009-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="12009-145">Du kan også opprette en serviceordrelinje for erstatningsobjektet.</span><span class="sxs-lookup"><span data-stu-id="12009-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="12009-146">Hvis du oppretter en serviceordrelinje, kan du fakturere erstatningsvaren.</span><span class="sxs-lookup"><span data-stu-id="12009-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="12009-147">Hvis du ikke oppretter en serviceordrelinje for en erstatning, beholdes erstatningsregistreringen slik at du kan spore loggen til serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="12009-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="12009-148">Endre hvordan informasjon på stykklistelinjen vises</span><span class="sxs-lookup"><span data-stu-id="12009-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="12009-149">Du kan endre hvordan informasjonen på stykklistelinjen vises for alle maler og servicestykklister.</span><span class="sxs-lookup"><span data-stu-id="12009-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="12009-150">Endringene brukes på alle malstykklister og servicestykklister.</span><span class="sxs-lookup"><span data-stu-id="12009-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="12009-151">Dette inkluderer de som er knyttet til serviceobjekter.</span><span class="sxs-lookup"><span data-stu-id="12009-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="12009-152">Angi nummerserier for malstykklister</span><span class="sxs-lookup"><span data-stu-id="12009-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="12009-153">Hvis du vil bruke malstykklister, må du angi to nummerserier.</span><span class="sxs-lookup"><span data-stu-id="12009-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="12009-154">Definer en nummerserie for malstykklisten og en for linjenummeret for stykklistelogg.</span><span class="sxs-lookup"><span data-stu-id="12009-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="12009-155">Nummerserier brukes til å tildele identifikatorer oppføringer som krever det.</span><span class="sxs-lookup"><span data-stu-id="12009-155">Number sequences are used to allocate identifiers to records that require them.</span></span> <span data-ttu-id="12009-156">Før du kan tilordne en nummerserie for en malstykkliste eller et linjenummer for stykklistelogg, må du definere nummerseriekoder.</span><span class="sxs-lookup"><span data-stu-id="12009-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="12009-157">Definer nummerserier</span><span class="sxs-lookup"><span data-stu-id="12009-157">Set up number sequences</span></span>

1.  <span data-ttu-id="12009-158">På listesiden **Nummerserier** oppretter du nummerserier for malstykklister og linjenummeret for stykklisteloggen.</span><span class="sxs-lookup"><span data-stu-id="12009-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="12009-159">Klikk **Servicestyring** \> **Oppsett** \> **Servicestyringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="12009-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="12009-160">Klikk **Nummerserier**, og velg en nummerseriekode for nummerseriereferansene du har opprettet i skjemaet **Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="12009-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="12009-161">Lukk skjemaet for å lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="12009-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="12009-162">Linjenummeret for stykklisteloggen brukes av systemet til å knytte transaksjonene i stykklisteloggen til en serviceavtale eller serviceordre.</span><span class="sxs-lookup"><span data-stu-id="12009-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="12009-163">Nummeret vises ikke i brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="12009-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="12009-164">Se også</span><span class="sxs-lookup"><span data-stu-id="12009-164">See also</span></span>

[<span data-ttu-id="12009-165">Opprette en malstykkliste</span><span class="sxs-lookup"><span data-stu-id="12009-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="12009-166">Behandle malstykklister på objektrelasjoner</span><span class="sxs-lookup"><span data-stu-id="12009-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="12009-167">Endre en servicestykkliste</span><span class="sxs-lookup"><span data-stu-id="12009-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 



---
title: Feilsøke produktinformasjon
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med produktinformasjon.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4c505ccfd1998acd40dbae715c7fa572e315af2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007522"
---
# <a name="troubleshoot-product-information"></a><span data-ttu-id="1cfbd-103">Feilsøke produktinformasjon</span><span class="sxs-lookup"><span data-stu-id="1cfbd-103">Troubleshoot product information</span></span>

<span data-ttu-id="1cfbd-104">Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med produktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-104">This topic describes how to fix issues that you might encounter while you work with product information.</span></span>

## <a name="i-cant-delete-a-released-product"></a><span data-ttu-id="1cfbd-105">Jeg kan ikke slette et frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-105">I can't delete a released product.</span></span>

### <a name="issue-description"></a><span data-ttu-id="1cfbd-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1cfbd-106">Issue description</span></span>

<span data-ttu-id="1cfbd-107">Du kan bare slette et frigitt produkt og alle variantene av det hvis det frigitte produktet ikke har noen tilknyttede transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-107">You can delete a released product and all its variants only if the released product doesn't have any related transactions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1cfbd-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1cfbd-108">Issue resolution</span></span>

<span data-ttu-id="1cfbd-109">Følg denne fremgangsmåten for å slette et frigitt produkt eller en frigitt produktstandard.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-109">Follow these steps to delete a released product or product master.</span></span>

1. <span data-ttu-id="1cfbd-110">Lukk alle åpne transaksjoner for varene.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-110">Close all open transactions for the items.</span></span>
1. <span data-ttu-id="1cfbd-111">Reduser lageret til 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1cfbd-111">Reduce the inventory to 0 (zero).</span></span>
1. <span data-ttu-id="1cfbd-112">Utfør lagerlukking.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-112">Perform inventory closing.</span></span>
1. <span data-ttu-id="1cfbd-113">Slett alle produktvarianter for produktstandarden du vil slette.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-113">Delete all product variants for the product master that you want to delete.</span></span>

## <a name="can-i-change-the-item-number-of-a-released-product"></a><span data-ttu-id="1cfbd-114">Kan jeg endre varenummeret til et frigitt produkt?</span><span class="sxs-lookup"><span data-stu-id="1cfbd-114">Can I change the item number of a released product?</span></span>

<span data-ttu-id="1cfbd-115">I de fleste tilfeller kan du ikke redigere varenumre for frigitte produkter, fordi denne endringen vil føre til at data blir ødelagt.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-115">In most cases, you can't edit item numbers for released products, because that change will cause data to become corrupted.</span></span> <span data-ttu-id="1cfbd-116">Du kan bare redigere varenummeret hvis du må reparere skadede data som ble forårsaket av en tidligere endring av navnet til primærnøkkelen for det frigitte produktet, som nevnt i listen over [fjernede eller avskrevne funksjoner for Finance and Operations 10.0.0 med Platform Update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="1cfbd-116">You can edit the item number only if you must repair data corruption that was caused by a previous rename of the primary key of that released product, as mentioned in the list of [removed or deprecated features for Finance and Operations 10.0.0 with Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span></span>

<span data-ttu-id="1cfbd-117">Hvis du vil ha muligheten til å redigere varenumre for frigitte produkter, må du [stemme på dette forslaget i Ideer-portalen](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span><span class="sxs-lookup"><span data-stu-id="1cfbd-117">If you want to be able to edit item numbers for released products, [vote for this idea in Ideas portal](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span></span>

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a><span data-ttu-id="1cfbd-118">Standard trekkprinsipp fra produktet blir ikke angitt i stykklistelinjen.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-118">The default flushing principle from the product isn't being entered on the bill of materials line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="1cfbd-119">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1cfbd-119">Issue description</span></span>

<span data-ttu-id="1cfbd-120">Når du legger til en vare i en stykklistelinje, bruker ikke systemet standardinformasjonen for trekkprinsippet som er definert for varen.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-120">When you add an item to a bill of materials (BOM) line, the system doesn't use the default flushing principle information that is set up for the item.</span></span> <span data-ttu-id="1cfbd-121">Med andre ord vises ikke trekkprinsippet fra varen på siden **Stykklistelinje**.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-121">In other words, the flushing principle from the item doesn't appear on the **BOM line** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1cfbd-122">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1cfbd-122">Issue resolution</span></span>

<span data-ttu-id="1cfbd-123">Hvis du angir et trekkprinsipp på en stykklistelinje, vil dette gjelde for denne stykklistelinjen.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-123">If you specify a flushing principle on a BOM line, it will apply to that BOM line.</span></span> <span data-ttu-id="1cfbd-124">Hvis trekkprinsippet for eksempel er tomt, eller hvis det ikke er angitt på en stykklistelinje, vil trekkprinsippet som er angitt på varen, fortsatt gjelde for denne stykklistelinjen, selv om det ikke vises på stykklistelinjen.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-124">However, if the flushing principle is blank, or if it isn't set on a BOM line, the flushing principle that is set on the item will still apply to that BOM line, even though it isn't shown on the BOM line.</span></span>

<span data-ttu-id="1cfbd-125">Standardlogikken for andre funksjoner i Microsoft Dynamics 365 Supply Chain Management fungerer vanligvis ikke på denne måten.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-125">The defaulting logic for other features in Microsoft Dynamics 365 Supply Chain Management doesn't usually work in this way.</span></span> <span data-ttu-id="1cfbd-126">Gjeldende virkemåte kan imidlertid ikke endres.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-126">However, the current behavior can't be changed.</span></span> <span data-ttu-id="1cfbd-127">Hvis ikke kan noen eksisterende tilpasninger som er avhengige av det, bli ødelagt.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-127">Otherwise, some existing customizations that rely on it might be broken.</span></span>

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a><span data-ttu-id="1cfbd-128">Systemet lar meg lagre duplikatstrekkoder for ulike varer eller for samme vare som har forskjellige dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-128">The system lets me save duplicate bar codes for different items or for the same item that has different dimensions.</span></span>

<span data-ttu-id="1cfbd-129">Systemet håndhever for øyeblikket ikke unike strekkoder, og tillegget av denne begrensningen vil være en oppdelingsendring.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-129">The system doesn't currently enforce unique bar codes, and the addition of this restriction would be a breaking change.</span></span> <span data-ttu-id="1cfbd-130">Microsoft har faktisk bevis på at noen eksisterende kundeinstallasjoner vil bli ødelagt av denne endringen.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-130">In fact, Microsoft has evidence that some existing customer installations would be broken by this change.</span></span> <span data-ttu-id="1cfbd-131">Vi vil imidlertid vurdere en større endring i utformingen for å aktivere denne funksjonen i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-131">However, we will consider a broader design change to enable this feature in the future.</span></span>

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a><span data-ttu-id="1cfbd-132">Jeg får følgende feilmelding når jeg redigerer maler for vareposter: Lagerlokasjonen kan ikke opprettes fordi varen ikke er lagerført.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-132">I receive the following error message when I edit item record templates: "The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="1cfbd-133">For lagerførte varer må Lagerført produkt-alternativet i den tilknyttede varemodellgruppen velges.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-133">To stock items, the Stocked product option on the associated item model group must be selected."</span></span>

### <a name="issue-description"></a><span data-ttu-id="1cfbd-134">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1cfbd-134">Issue description</span></span>

<span data-ttu-id="1cfbd-135">Dette problemet oppstår hvis du følger denne fremgangsmåte for å forsøke å opprette en mal for en vare som ikke er lagerført.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-135">This issue occurs if you follow these steps to try to create a template for an item that isn't stocked.</span></span>

1. <span data-ttu-id="1cfbd-136">Åpne et frigitt produkt som ikke er lagerført.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-136">Open a released product that isn't stocked.</span></span>
1. <span data-ttu-id="1cfbd-137">Velg **Portinformasjon** i fanen **Alternativer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-137">On the Action Pane, on the **Options** tab, select **Record info**.</span></span>
1. <span data-ttu-id="1cfbd-138">Velg **Firmakontomal** i dialogboksen **Postinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-138">In the **Record information** dialog box, select **Company accounts template**.</span></span>

<span data-ttu-id="1cfbd-139">I dette tilfellet får du følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="1cfbd-139">In this case, you receive the following error message:</span></span>

> <span data-ttu-id="1cfbd-140">Lagerlokasjonen kan ikke opprettes fordi varen ikke er lagerført.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-140">The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="1cfbd-141">For lagerførte varer må Lagerført produkt-alternativet i den tilknyttede varemodellgruppen velges.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-141">To stock items, the Stocked product option on the associated item model group must be selected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1cfbd-142">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1cfbd-142">Issue resolution</span></span>

<span data-ttu-id="1cfbd-143">Prosessen med å opprette produktmaler krever ekstra, produktspesifikk logikk.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-143">The process of creating product templates requires extra product-specific logic.</span></span> <span data-ttu-id="1cfbd-144">Derfor kan du ikke bruke den generelle knappen **Firmakontomal** til dette formålet.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-144">Therefore, you can't use the generic **Company accounts template** button for this purpose.</span></span> <span data-ttu-id="1cfbd-145">Følg i stedet denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-145">Instead, follow these steps.</span></span>

1. <span data-ttu-id="1cfbd-146">Åpne et frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-146">Open a released product.</span></span>
1. <span data-ttu-id="1cfbd-147">I handlingsruten, i **Produkt**-fanen og **Ny**-gruppen velger du **Mal \> Opprett delt mal**.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-147">On the Action Pane, on the **Product** tab, in the **New** group, select **Template \> Create shared template**.</span></span>

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a><span data-ttu-id="1cfbd-148">Standard hjelpetekst som legges til i produktattributter, er ikke angitt i et frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-148">Default Help text that is added in product attributes isn't entered in a released product.</span></span>

<span data-ttu-id="1cfbd-149">En beskrivelse og hjelpetekst som legges til i produktattributtene, vises ikke eller angis ikke som standard i de frigitte produktene.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-149">A description and Help text that are added in the product attributes aren't visible or entered by default in the released products.</span></span> <span data-ttu-id="1cfbd-150">Denne virkemåten er standard.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-150">This behavior is by design.</span></span>

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a><span data-ttu-id="1cfbd-151">Standardantallet som er angitt, er forskjellig når det er registrert fra en stykkliste, og når det er registrert fra en stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-151">The default quantity that is entered differs when it's registered from a BOM and when it's registered from a BOM version.</span></span>

### <a name="issue-description"></a><span data-ttu-id="1cfbd-152">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1cfbd-152">Issue description</span></span>

<span data-ttu-id="1cfbd-153">Når du legger til en vare i en stykkliste, settes antallet som standard til 1 i stedet for antallet som er definert i **Minimumsordre**-feltet på siden **Standard ordreinnstillinger** for et valgt produkt.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-153">By default, when you add an item to a BOM, the quantity is set to 1 instead of the quantity that is defined in the **Min. order quantity** field on the **Default order settings** page for a selected product.</span></span> <span data-ttu-id="1cfbd-154">Når du imidlertid legger til en vare fra en stykklisteversjon, og varen og varianten velges, tar antallet som er angitt som standard, hensyn til minimumsantallet som er angitt i standard ordreinnstillinger for de bestemte dimensjonene.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-154">However, when you add an item from a BOM version, and the item and variant are selected, the quantity that is entered by default takes into account the minimum quantity that is set in the default order settings for the specific dimensions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1cfbd-155">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1cfbd-155">Issue resolution</span></span>

<span data-ttu-id="1cfbd-156">Denne virkemåten er forventet.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-156">This behavior is expected.</span></span> <span data-ttu-id="1cfbd-157">Men det at logikken er forskjellig i stykklisten og stykklisteversjonen, er et kjent problem.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-157">However, the fact that the logic differs in the BOM and the BOM version is a known issue.</span></span> <span data-ttu-id="1cfbd-158">Denne virkemåten vil likevel ikke bli endret fordi en endring kan påvirke mange forskjellige kundescenarioer.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-158">Nevertheless, this behavior won't be changed, because a change could affect many different customer scenarios.</span></span>

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a><span data-ttu-id="1cfbd-159">I detaljene for det frigitte produktet kan jeg ikke endre de vedlagte bildene som ble lastet opp fra dataenheten for produktdokumentvedlegg.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-159">In the released product details, I can't change the attached images that were uploaded from the Product document attachments data entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="1cfbd-160">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1cfbd-160">Issue description</span></span>

<span data-ttu-id="1cfbd-161">Dette problemet kan oppstå når du knytter et bilde til en vare ved hjelp av dataenheten for *produktdokumentvedlegg* .</span><span class="sxs-lookup"><span data-stu-id="1cfbd-161">This issue can occur when you attach an image to an item by using the *Product document attachments* data entity.</span></span> <span data-ttu-id="1cfbd-162">I dette tilfellet vises varebildet for varen.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-162">In this case, the item image is shown for the item.</span></span> <span data-ttu-id="1cfbd-163">Hvis du imidlertid velger **Endre bilde**, vises ingenting i listen over opplastede bilder.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-163">However, if you select **Change image**, nothing is shown in the list of uploaded images.</span></span> <span data-ttu-id="1cfbd-164">Det vises heller ingen vedlegg for varen.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-164">Additionally, no attachments are shown for the item.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1cfbd-165">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1cfbd-165">Issue resolution</span></span>

<span data-ttu-id="1cfbd-166">Enheten *EcoResProductDocumentAttachmentEntity* (*produktdokumentvedlegg*) importerer dokumentvedlegg for *produkter*, men ikke for *frigitte produkter*.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-166">The *EcoResProductDocumentAttachmentEntity* entity (*Product document attachments*) imports document attachments for *products* but not for *released products*.</span></span> <span data-ttu-id="1cfbd-167">(Frigitte produkter er også kjent som *varer*). Hvis du vil vise vedleggene for en vare på siden **Detaljer om frigitt produkt**, må du bruke enheten *EcoResReleasedProductDocumentAttachmentEntity* (*dokumentvedlegg for frigitt produkt*) i stedet.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-167">(Released products are also known as *items*.) To view the attachments for an item on the **Released product details** page, you must use the *EcoResReleasedProductDocumentAttachmentEntity* entity (*Released product document attachments*) instead.</span></span>

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a><span data-ttu-id="1cfbd-168">Microsoft Flow-koblingen viser følgende feilmelding: Oppdatering ikke tillatt for feltet ProductNumber.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-168">The Microsoft Flow connector shows the following error message: "Update not allowed for field 'ProductNumber'."</span></span>

### <a name="issue-description"></a><span data-ttu-id="1cfbd-169">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1cfbd-169">Issue description</span></span>

<span data-ttu-id="1cfbd-170">Dette problemet oppstår hvis du prøver å oppdatere **Produktnummer**-feltet ved hjelp av enheten *Frigitte produkter* V2 og Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-170">This issue occurs if you try to update the **Product number** field by using the *Released products* entity V2 and Microsoft Flow.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1cfbd-171">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1cfbd-171">Issue resolution</span></span>

<span data-ttu-id="1cfbd-172">Denne virkemåten er forventet.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-172">This behavior is expected.</span></span> <span data-ttu-id="1cfbd-173">Muligheten til å redigere produktnummeret for et frigitt produkt ble fjernet i Dynamics 365 Finance and Operations 10.0.0 med Platform Update 24 for å bidra til å hindre ødelagte data.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-173">The ability to edit the product number for a released product was removed in Dynamics 365 Finance and Operations 10.0.0 with platform update 24 to help prevent data corruption.</span></span> <span data-ttu-id="1cfbd-174">I uvanlige tilfeller der du må reparere skadede data som var forårsaket av en tidligere endring av navnet til primærnøkkelen for et frigitt produkt, kan du be Microsoft Kundestøtte om å fjerne denne begrensningen midlertidig.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-174">In exceptional cases, where you must repair data corruption that was caused by a previous rename of the primary key of a released product, you can ask Microsoft Support to temporarily remove this restriction.</span></span>

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a><span data-ttu-id="1cfbd-175">Jeg kan ikke opprette en frigitt produktvariant i en annen juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-175">I can't create a released product variant in another legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="1cfbd-176">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1cfbd-176">Issue description</span></span>

<span data-ttu-id="1cfbd-177">Hvis du prøver å frigi en produktstandard uten varianter, og deretter oppretter variantene i hver juridiske enhet (firma) etter behov, kan du ikke frigi variantene ved hjelp av variantforslag.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-177">If you try to release a product master without variants, and then create the variants in each legal entity (company) as they are required, you won't be able to release the variants by using variant suggestions.</span></span> <span data-ttu-id="1cfbd-178">Du vil heller ikke kunne opprette variantene manuelt.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-178">You also won't be able to manually create the variants.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1cfbd-179">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1cfbd-179">Issue resolution</span></span>

<span data-ttu-id="1cfbd-180">Denne virkemåten er standard.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-180">This behavior is by design.</span></span> <span data-ttu-id="1cfbd-181">Relasjonene mellom en produktstandard og dimensjonene som standarden kan ta, beholdes på et delt nivå.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-181">The relations of a product master and the dimensions that the master can take are kept at a shared level.</span></span> <span data-ttu-id="1cfbd-182">Derfor kan du ikke opprette tilgjengelige dimensjoner for en delt produktstandard i den bestemte juridiske enheten der disse dimensjonene er frigitt, og deretter replikere prosessen i hver juridiske enhet der dimensjonene er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-182">Therefore, you can't create the available dimensions for a shared product master in the specific legal entity where those dimensions are released and then replicate the process in each legal entity where the dimensions are required.</span></span> <span data-ttu-id="1cfbd-183">I stedet må du endre frigivelsesprosessen for å tilpasse til den utformede prosessen.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-183">Instead, you must change your release process to adapt to the designed process.</span></span>

<span data-ttu-id="1cfbd-184">Her er prosessen for frigivelse av produkter.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-184">Here is the process for releasing products.</span></span>

1. <span data-ttu-id="1cfbd-185">Opprett den delte produktstandarden og dimensjonene som kan frigis til de juridiske enhetene.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-185">Create the shared product master and the dimensions that can be released to the legal entities.</span></span>
1. <span data-ttu-id="1cfbd-186">Frigi produktene til de juridiske enhetene enten ved å bruke variantforslag, eller ved å legge til kombinasjonene som skal frigis, manuelt.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-186">Release the products to the legal entities either by using variant suggestions or by manually adding the combinations that should be released.</span></span>

<span data-ttu-id="1cfbd-187">Du kan også opprette det frigitte produktet direkte.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-187">Alternatively, you can directly create the released product.</span></span>

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a><span data-ttu-id="1cfbd-188">Når jeg frigir en variant i et annet firma, får jeg følgende feilmelding: Produktvariant med angitte dimensjoner er allerede opprettet.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-188">When I release a variant in another company, I receive the following error message: "Product variant with specified dimensions has already been created."</span></span>

### <a name="issue-description"></a><span data-ttu-id="1cfbd-189">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1cfbd-189">Issue description</span></span>

<span data-ttu-id="1cfbd-190">Hvis en produktvariant allerede er frigitt i et firma A, og du prøver å frigi den i firma B ved hjelp av **Ny**-knappen på siden **Frigitte produktvarianter**, vil du få følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="1cfbd-190">If a product variant has already been released in a company A, and you try to release it in company B by using the **New** button on the **Released product variants** page, you will receive the following error message:</span></span>

> <span data-ttu-id="1cfbd-191">Produktvariant med angitte dimensjoner er allerede opprettet.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-191">Product variant with specified dimensions has already been created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1cfbd-192">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1cfbd-192">Issue resolution</span></span>

<span data-ttu-id="1cfbd-193">**Ny**-knappen på siden **Frigitte produktvarianter** oppretter varianten og frigir den i firmakonteksten.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-193">The **New** button on the **Released product variants** page creates the variant and releases it in the company context.</span></span> <span data-ttu-id="1cfbd-194">Hvis varianten allerede er opprettet, kan du ikke bruke **Ny**-knappen til å frigi den i et annet firma.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-194">If the variant has already been created, you can't use the **New** button to release it in another company.</span></span>

<span data-ttu-id="1cfbd-195">Du kan løse problemet ved å åpne siden **Produktstandard** og velge **Frigi produkt** for å frigi den eksisterende varianten i ønsket firma.</span><span class="sxs-lookup"><span data-stu-id="1cfbd-195">To fix the issue, open the **Product master** page, and select **Release product** to release the existing variant in the desired company.</span></span>

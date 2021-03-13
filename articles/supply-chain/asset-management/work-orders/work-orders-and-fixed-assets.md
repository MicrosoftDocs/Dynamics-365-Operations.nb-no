---
title: Arbeidsordrer og anleggsmidler
description: Dette emnet forklarer arbeidsordrer og anleggsmidler i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
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
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4eadbdc452a5b7d28adfa0f102a9a727faad3c07
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016709"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="3903d-103">Arbeidsordrer og anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="3903d-103">Work orders and fixed assets</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="3903d-104">I Aktivastyring kan aktiva relateres til anleggsmidler, og du kan opprette arbeidsordrer for disse aktivaene.</span><span class="sxs-lookup"><span data-stu-id="3903d-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="3903d-105">Hvis du bruker denne funksjonen, kan du få en fullstendig oversikt over anleggsmidler, tilknyttede investeringsprosjekter og kostnadene som er registrert på investeringsprosjektene, i **Prosjektstyring og regnskap** og **Anleggsmidler**-modulene i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3903d-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs that are registered on the investment projects in the **Project management and accounting** and **Fixed assets** modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="3903d-106">Feltet **Anleggsmidlets nummer** fylles bare ut på arbeidsordrejobbprosjektet hvis **Investering** er valgt som prosjekttype i arbeidsordrejobbprosjektet.</span><span class="sxs-lookup"><span data-stu-id="3903d-106">The **Fixed asset number** field on the work order job project is set only if **Investment** is selected as the project type on the work order job project.</span></span>

<span data-ttu-id="3903d-107">Illustrasjonen nedenfor viser forholdet mellom et investeringsprosjekt i modulen **Prosjektstyring og regnskap** og et arbeidsordrejobbprosjekt.</span><span class="sxs-lookup"><span data-stu-id="3903d-107">The illustration below shows the relation between an investment project in the **Project management and accounting** module and a work order job project.</span></span>

![Figur 1](media/24-work-orders.png)

<span data-ttu-id="3903d-109">Følgende fremgangsmåte beskriver forholdet mellom aktiva, arbeidsordrer, arbeidsordrejobbprosjekter og anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="3903d-109">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="3903d-110">Du oppretter et aktivum som du knytter til et anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="3903d-110">You create an asset that you relate to a fixed asset.</span></span>

![Figur 2](media/25-work-orders.png)

2. <span data-ttu-id="3903d-112">Når du definerer arbeidsordretyper på siden **Arbeidsordretyper** (**Aktivabehandling** > **Oppsett** > **Arbeidsordrer** > **Arbeidsordretyper**), oppretter du en arbeidsordretype for behandling av investeringer.</span><span class="sxs-lookup"><span data-stu-id="3903d-112">When you set up work order types on the **Work order types** page (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="3903d-113">Se også [Arbeidsordretyper](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="3903d-113">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Figur 3](media/26-work-orders.png)

3. <span data-ttu-id="3903d-115">Når du definerer prosjektgrupper for arbeidsordrer i fanen **Prosjektgruppe** på siden **Prosjektoppsett for arbeidsordre** (**Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Prosjektoppsett**), oppretter du en relasjon mellom arbeidsordretypen som brukes for investeringer, og prosjektgruppen som ble opprettet for investeringer på siden **Prosjektgrupper** i modulen **Prosjektstyring og regnskap** (**Prosjektstyring og regnskap** > **Oppsett** > **Postering** > **Prosjektgrupper**).</span><span class="sxs-lookup"><span data-stu-id="3903d-115">When you set up work order project groups on the **Project group** tab of the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**), you create a relation between the work order type that is used for investments and the project group that was created for investments on the **Project groups** page in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Figur 4](media/27-work-orders.png)

4. <span data-ttu-id="3903d-117">Når du oppretter en arbeidsordre som er relatert til et anleggsmiddel, velger du arbeidsordretypen som brukes til å behandle investeringer, for eksempel **Investering**.</span><span class="sxs-lookup"><span data-stu-id="3903d-117">When you create a work order that is related to a fixed asset, you select the work order type that is used to handle investments, such as **Investment**.</span></span>

5. <span data-ttu-id="3903d-118">Når arbeidsordren opprettes, vises den tilknyttede arbeidsordretypen på siden **Alle arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="3903d-118">When the work order is created, the related work order type is shown on the **All work orders** page.</span></span>

![Figur 5](media/28-work-orders.png)

6. <span data-ttu-id="3903d-120">Når arbeidsordren opprettes, opprettes prosjektet som er knyttet til arbeidsordren, på siden **Alle prosjekter** i modulen **Prosjektstyring og regnskap** (**Prosjektstyring og regnskap** > **Prosjekter** > **Alle prosjekter**).</span><span class="sxs-lookup"><span data-stu-id="3903d-120">When the work order is created, the project that is related to the work order is created on the **All projects** page in the **Project management and accounting** module (**Project management and accounting** > **Projects** > **All projects**).</span></span> <span data-ttu-id="3903d-121">Hvis du vil vise prosjektrelatert informasjon, velger du koblingen i feltet **Prosjekt-ID** i fanen **Generelt** i hurtigfanen **Linjedetaljer** i detaljvisningen på siden **Alle arbeidsordrer** i modulen **Aktivabehandling** (**Aktivabehandling** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer**).</span><span class="sxs-lookup"><span data-stu-id="3903d-121">To view project-related information, select the link in the **Project ID** field on the **General** tab on the **Line details** FastTab in the details view of the **All work orders** page in the **Asset management** module (**Asset management** > **Commom** > **Work orders** > **All work orders**).</span></span>

![Figur 6](media/29-work-orders.png)

7. <span data-ttu-id="3903d-123">Hvis du vil se en oversikt over prosjektene som er knyttet til et anleggsmiddel, velger du **Anleggsmidler** > **Anleggsmidler** > **Anleggsmidler** og deretter, i feltet **Anleggsmidlets nummer**, velger du koblingen til anleggsmidlet for å åpne detaljvisningen.</span><span class="sxs-lookup"><span data-stu-id="3903d-123">To see an overview of the projects associated with a fixed asset, select **Fixed assets** > **Fixed assets** > **Fixed assets**, and then, in the **Fixed asset number** field, select the link for the fixed asset to open the details view.</span></span> <span data-ttu-id="3903d-124">Utvid ruten **Beslektet informasjon** til høyre på siden, og velg hurtigfanen **Tilknyttede prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="3903d-124">Expand the **Related information** pane on the right side of the page, and select the **Associated projects** FastTab.</span></span>


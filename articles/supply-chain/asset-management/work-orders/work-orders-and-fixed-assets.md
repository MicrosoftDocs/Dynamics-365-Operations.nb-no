---
title: Arbeidsordrer og anleggsmidler
description: Dette emnet forklarer arbeidsordrer og anleggsmidler i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f03b7fa073c4e5338b7b5681ba7b8c9fe00a657b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875813"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="2f556-103">Arbeidsordrer og anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="2f556-103">Work orders and fixed assets</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="2f556-104">I Aktivastyring kan aktiva relateres til anleggsmidler, og du kan opprette arbeidsordrer for disse aktivaene.</span><span class="sxs-lookup"><span data-stu-id="2f556-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="2f556-105">Hvis du bruker denne funksjonen, kan du få en fullstendig oversikt over anleggsmidler, tilknyttede investeringsprosjekter og kostnadene som er registrert på investeringsprosjektene, i **Prosjektstyring og regnskap**-modulen og **Anleggsmidler**-modulen i Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2f556-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module in Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="2f556-106">**Anleggsmiddelnummer**-feltet fylles bare ut på arbeidsordrejobbprosjektet hvis typen Investering er valgt som prosjekttype i arbeidsordrejobbprosjektet.</span><span class="sxs-lookup"><span data-stu-id="2f556-106">The **Fixed asset number** field is only filled out on the work order job project if type "Investment" is selected as the project type on the work order job project.</span></span>

![Figur 1](media/24-work-orders.png)

<span data-ttu-id="2f556-108">Følgende fremgangsmåte beskriver forholdet mellom aktiva, arbeidsordrer, arbeidsordrejobbprosjekter og anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="2f556-108">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="2f556-109">Du oppretter et aktivum som du knytter til et anleggsmiddel, som vist i figuren nedenfor.</span><span class="sxs-lookup"><span data-stu-id="2f556-109">You create an asset that you relate to a fixed asset, as shown in the figure below.</span></span>

![Figur 2](media/25-work-orders.png)

2. <span data-ttu-id="2f556-111">Når du definerer arbeidsordretyper (**Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Arbeidsordretyper**), oppretter du en arbeidsordretype for behandling av investeringer.</span><span class="sxs-lookup"><span data-stu-id="2f556-111">When you set up work order types (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="2f556-112">Se også [Arbeidsordretyper](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="2f556-112">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Figur 3](media/26-work-orders.png)

3. <span data-ttu-id="2f556-114">Når du definerer prosjektgrupper for arbeidsordrer (**Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Prosjektoppsett** > **Prosjektgruppe**-koblingen), oppretter du en relasjon mellom arbeidsordretypen som brukes for investeringer, og prosjektgruppen opprettet for investeringer i **Prosjektstyring og regnskap**-modulen (**Prosjektstyring og regnskap** > **Oppsett** > **Postering** > **Prosjektgrupper**).</span><span class="sxs-lookup"><span data-stu-id="2f556-114">When you set up work order project groups (**Asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Figur 4](media/27-work-orders.png)

4. <span data-ttu-id="2f556-116">Når du oppretter en arbeidsordre som er knyttet til et anleggsmiddelobjekt, velger du arbeidsordretypen som brukes til å behandle investeringer, for eksempel Investering.</span><span class="sxs-lookup"><span data-stu-id="2f556-116">When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".</span></span>

5. <span data-ttu-id="2f556-117">Når arbeidsordren opprettes, vises den tilknyttede arbeidsordretypen i **Alle arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="2f556-117">When the work order is created, the related work order type is shown in **All work orders**.</span></span>

![Figur 5](media/28-work-orders.png)

6. <span data-ttu-id="2f556-119">Når arbeidsordren opprettes, opprettes prosjektet som er knyttet til arbeidsordren, i **Prosjektstyring og regnskap** > **Alle prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="2f556-119">When the work order is created, the project related to the work order is created in **Project management and accounting** > **All projects**.</span></span> <span data-ttu-id="2f556-120">Du kan vise prosjektrelatert informasjon ved å klikke på koblingen **Prosjekt-ID** i arbeidsordren (i **Aktivastyring** åpner du arbeidsordren i detaljvisningen > hurtigfanen **Linjedetaljer** > kategorien **Generelt** > feltet **Prosjekt-ID**).</span><span class="sxs-lookup"><span data-stu-id="2f556-120">You can see project-related information by clicking the **Project ID** link on the work order (in **Asset management**, open the work order in Details view > **Line details** FastTab > **General** tab > **Project ID** field).</span></span>

![Figur 6](media/29-work-orders.png)

7. <span data-ttu-id="2f556-122">I **Anleggsmidler** kan du se en oversikt over prosjektene som er knyttet til et anleggsmiddel (**Anleggsmidler** > **Anleggsmidler** > **Anleggsmidler**> klikk på anleggsmidlet i feltet **Anleggsmiddelnummer** > vis innholdet i **Relatert informasjon**-ruten > delen **Tilknyttede prosjekter**).</span><span class="sxs-lookup"><span data-stu-id="2f556-122">In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > view the contents in the **Related information** pane > **Associated projects** section).</span></span>


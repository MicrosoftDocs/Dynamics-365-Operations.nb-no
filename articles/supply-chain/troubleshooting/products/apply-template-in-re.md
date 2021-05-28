---
title: Du kan ikke bruke en mal på et frigitt produkt
description: Du kan ikke bruke en mal på et frigitt produkt.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026772"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a><span data-ttu-id="7df40-103">Du kan ikke bruke en mal for å opprette et frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="7df40-103">You can't apply a template to create a released product</span></span>

<span data-ttu-id="7df40-104">KB-nummer: 4612097</span><span class="sxs-lookup"><span data-stu-id="7df40-104">KB number: 4612097</span></span>

## <a name="symptoms"></a><span data-ttu-id="7df40-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="7df40-105">Symptoms</span></span>

<span data-ttu-id="7df40-106">Når du oppretter et nytt frigitt produkt ved hjelp av dialogboksen **Nytt frigitt produkt**, kan du velge en mal.</span><span class="sxs-lookup"><span data-stu-id="7df40-106">When you create a new released product by using the **New released product** dialog box, you can select a template.</span></span> <span data-ttu-id="7df40-107">Malen skal angi standardinnstillinger for mange felt i det nye frigitte produktet.</span><span class="sxs-lookup"><span data-stu-id="7df40-107">The template is supposed to provide default settings for many fields of the new released product.</span></span> <span data-ttu-id="7df40-108">Noen eller alle feltene velges imidlertid ikke etter at du har valgt malen.</span><span class="sxs-lookup"><span data-stu-id="7df40-108">However, some or all of the fields aren't set after you select the template.</span></span>

## <a name="cause"></a><span data-ttu-id="7df40-109">Årsak</span><span class="sxs-lookup"><span data-stu-id="7df40-109">Cause</span></span>

<span data-ttu-id="7df40-110">På mange sider i Microsoft Dynamics 365 Supply Chain Management kan du opprette en mal som oppretter innledende innstillinger for postene som vises på disse sidene.</span><span class="sxs-lookup"><span data-stu-id="7df40-110">Many pages in Microsoft Dynamics 365 Supply Chain Management let you create a template that establishes initial settings for the records that are shown on those pages.</span></span> <span data-ttu-id="7df40-111">Du kan opprette én av disse malene ved å velge **Postinformasjon** i kategorien **Alternativer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7df40-111">You can create one of these templates by selecting **Record info** on the **Options** tab of the Action Pane.</span></span> <span data-ttu-id="7df40-112">Frigitte produkter er imidlertid mye mer komplekse enn de fleste andre typer poster.</span><span class="sxs-lookup"><span data-stu-id="7df40-112">However, released products are much more complex than most other types of records.</span></span> <span data-ttu-id="7df40-113">Selv om du kan velge **Postinformasjon** på siden **Frigitte produkter** for å opprette en mal, og selv om du kan velge den malen når du oppretter et frigitt produkt, vil ikke malen gi de forventede feltverdiene for det nye frigitte produktet.</span><span class="sxs-lookup"><span data-stu-id="7df40-113">Although you can select **Record info** on the **Released products** page to create a template, and although you can select that template when you create a released product, the template won't provide the expected field values for the new released product.</span></span> <span data-ttu-id="7df40-114">Derfor kan du ikke bruke postinformasjon-maler for frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="7df40-114">Therefore, you can't use "record info" templates for released products.</span></span> <span data-ttu-id="7df40-115">I stedet må du opprette dedikerte produktmaler.</span><span class="sxs-lookup"><span data-stu-id="7df40-115">Instead, you must create dedicated product templates.</span></span>

## <a name="resolution"></a><span data-ttu-id="7df40-116">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="7df40-116">Resolution</span></span>

<span data-ttu-id="7df40-117">Hvis du vil opprette en produktmal, bruker du **Mal**-menyen i kategorien **Produkt** i handlingsruten, og ikke **Postinformasjon**-knappen i kategorien **Alternativer**.</span><span class="sxs-lookup"><span data-stu-id="7df40-117">To create a product template, use the **Template** menu on the **Product** tab of the Action Pane, not the **Record info** button on the **Options** tab.</span></span>

1. <span data-ttu-id="7df40-118">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="7df40-118">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="7df40-119">I handlingsruten i kategorien **Produkt** i gruppen **Ny**, velger du **Mal**, og velg deretter enten **Opprett personlig mal** eller **Opprett delt mal** etter behov.</span><span class="sxs-lookup"><span data-stu-id="7df40-119">On the Action Pane, on the **Product** tab, in the **New** group, select **Template**, and then select either **Create personal template** or **Create shared template**, as appropriate.</span></span>

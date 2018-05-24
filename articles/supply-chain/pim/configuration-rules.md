---
title: Konfigurasjonsregler
description: Denne artikkelen gir generell informasjon om konfigurasjonsregler. Konfigurasjonsregler definerer relasjoner mellom elementer i en stykkliste for produkter som bruker teknologi for dimensjonsbasert konfigurasjon.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8bbec5a0e6b6d9c3001fc36c7bdd053f92112fea
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="configuration-rules"></a><span data-ttu-id="caac9-104">Konfigurasjonsregler</span><span class="sxs-lookup"><span data-stu-id="caac9-104">Configuration rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="caac9-105">Denne artikkelen gir generell informasjon om konfigurasjonsregler.</span><span class="sxs-lookup"><span data-stu-id="caac9-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="caac9-106">Konfigurasjonsregler definerer relasjoner mellom elementer i en stykkliste for produkter som bruker teknologi for dimensjonsbasert konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="caac9-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="caac9-107">Konfigurasjonsregler er tilgjengelige når du definerer dimensjonsbaserte konfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="caac9-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="caac9-108">Konfigurasjonsregler brukes til å fremtvinge eller forby bestemte varekombinasjoner i en stykkliste.</span><span class="sxs-lookup"><span data-stu-id="caac9-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="caac9-109">Du kan definere én eller flere konfigurasjonsregler når en stykkliste har blitt opprettet og de aktuelle varene er tilordnet til de respektive konfigurasjonsgruppene.</span><span class="sxs-lookup"><span data-stu-id="caac9-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="caac9-110">Hvis to varer hører sammen, brukes operatoren **Velg** til å sikre inkludering.</span><span class="sxs-lookup"><span data-stu-id="caac9-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="caac9-111">Hvis to varer er gjensidig utelukkende, brukes operatoren **Fjern merking** til å sikre utelatelse.</span><span class="sxs-lookup"><span data-stu-id="caac9-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="caac9-112">**Obs!** Denne informasjonen gjelder bare for produktstandarder som bruker dimensjonsbasert konfigurasjonsteknologi.</span><span class="sxs-lookup"><span data-stu-id="caac9-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="caac9-113">Eksisterende konfigurasjoner påvirkes ikke av etterfølgende endringer i konfigurasjonsreglene.</span><span class="sxs-lookup"><span data-stu-id="caac9-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="caac9-114">Det er imidlertid viktig at du definerer reglene før du definerer en ny konfigurasjon, og at du kontrollerer reglene hvis du tror at de er endret.</span><span class="sxs-lookup"><span data-stu-id="caac9-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="caac9-115">**Obs!** For metoden **Velg** velges den avledede konfigurasjonsgruppen, det avledede varenummeret og den avledede konfigurasjonen automatisk.</span><span class="sxs-lookup"><span data-stu-id="caac9-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="caac9-116">For metoden **Fjern merking** kan ikke den avledede konfigurasjonsgruppen, det avledede varenummeret og den avledede konfigurasjonen velges.</span><span class="sxs-lookup"><span data-stu-id="caac9-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="additional-resources"></a><span data-ttu-id="caac9-117">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="caac9-117">Additional resources</span></span>
--------

[<span data-ttu-id="caac9-118">Dimensjonsbasert produktkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="caac9-118">Dimension-based product configuration</span></span>](dimension-based-product-configuration.md)





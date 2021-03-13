---
title: Vise tillegg for en produsert vare
description: De konstante kostnadene til en produsert vare viser oppstillingstider for operasjonene og komponentene som har et konstant antall eller et konstant svinnbeløp.
author: AndersGirke
manager: tfehr
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 2e181e6c933a4c360320e4539f8434c20d409358
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008272"
---
# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="1b762-103">Vise tillegg for en produsert vare</span><span class="sxs-lookup"><span data-stu-id="1b762-103">Display charges for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b762-104">De konstante kostnadene til en produsert vare viser oppstillingstider for operasjonene og komponentene som har et konstant antall eller et konstant svinnbeløp.</span><span class="sxs-lookup"><span data-stu-id="1b762-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="1b762-105">Det beregnede beløpet for en vares tillegg kan vises med varens enhetskostnader.</span><span class="sxs-lookup"><span data-stu-id="1b762-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="1b762-106">Tilleggene vises imidlertid noen ganger som separate felt, og de er ikke inkludert i varens enhetskostnader.</span><span class="sxs-lookup"><span data-stu-id="1b762-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="1b762-107">Når tilleggene vises som separate felt, viser ett felt det samlede tilleggsbeløpet, og det andre feltet viser kostnadspartistørrelsen (som kalles prisenheten) som ble brukt da beløpet ble nedbetalt.</span><span class="sxs-lookup"><span data-stu-id="1b762-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="1b762-108">Varepris-siden viser for eksempel tilleggene som to separate felt.</span><span class="sxs-lookup"><span data-stu-id="1b762-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="1b762-109">Siden Fullført viser imidlertid varens totale kostnad per enhet, og nedbetalte kostnader er inkludert i enhetskosten.</span><span class="sxs-lookup"><span data-stu-id="1b762-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>

<span data-ttu-id="1b762-110">Tilleggene for en produsert vare inkluderes alltid i varens enhetskostnad til standardkostformål.</span><span class="sxs-lookup"><span data-stu-id="1b762-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="1b762-111">De kan om ønskelig inkluderes også til planlagt kost-formål.</span><span class="sxs-lookup"><span data-stu-id="1b762-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="1b762-112">En policy i etterkalkuleringsversjonen implementerer beslutningen om å inkludere tillegg i en produsert vares kostnader.</span><span class="sxs-lookup"><span data-stu-id="1b762-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="1b762-113">Når du aktiverer en vares kostnadspost, oppdaterer du tilleggene for varens basiskostinformasjon, som vises på Varepris-siden.</span><span class="sxs-lookup"><span data-stu-id="1b762-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="1b762-114">Tilleggene vises som to separate felt, og de er ikke inkludert i varens enhetskostnader.</span><span class="sxs-lookup"><span data-stu-id="1b762-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="1b762-115">Hver aktivering oppdaterer varens basiskostinformasjon, selv om aktiveringen gjenspeiler forskjellige områder.</span><span class="sxs-lookup"><span data-stu-id="1b762-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="1b762-116">Du bør derfor vise basiskostinformasjonen som referanseinformasjon.</span><span class="sxs-lookup"><span data-stu-id="1b762-116">Therefore, you should view the base cost information as reference information.</span></span>






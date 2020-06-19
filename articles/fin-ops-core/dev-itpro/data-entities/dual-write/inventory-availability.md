---
title: Beholdningstilgjengelighet i dobbel skriving
description: Dette emnet inneholder informasjon om å sjekke beholdningstilgjengelighet i dobbel skriving.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
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
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426988"
---
# <a name="inventory-availability"></a><span data-ttu-id="c4f93-103">Beholdningstilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="c4f93-103">Inventory availability</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="c4f93-104">Ved å bruke beholdningstilgjengelighet kan du kontrollere beholdningen før du legger til et produkt i skjemaene **Tilbud**, **Ordre** eller **Fakturaer** i modelldrevne apper i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c4f93-104">Using inventory availability, you can check your inventory before you add a product into the **Quotes**, **Orders**, or **Invoices** forms in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="c4f93-105">Det å kontrollere beholdning og fastslå en fullføringsdato er for eksempel en nøkkeloppgave i [kundeemne-til-kontanter](dual-write-prospect-to-cash.md)-prosessen.</span><span class="sxs-lookup"><span data-stu-id="c4f93-105">For example, checking inventory and determining a fulfullment date is a key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span> <span data-ttu-id="c4f93-106">Hvis du ikke har nok beholdning, kan du beregne en leveringsdato basert på prosjekterte beholdningsmottak og -problemer.</span><span class="sxs-lookup"><span data-stu-id="c4f93-106">If you don't have enough inventory, you can estimate a delivery date based on projected inventory receipts and issues.</span></span> <span data-ttu-id="c4f93-107">Du kan også kontrollere produktets tilgjengelig for ordre (ATP)-informasjon, der du kan finne ATP-antallet i den forhåndsdefinerte tidshorisonten.</span><span class="sxs-lookup"><span data-stu-id="c4f93-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the pre-defined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="c4f93-108">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="c4f93-108">On-hand Inventory</span></span> 

<span data-ttu-id="c4f93-109">I toppteksten i skjemaene **Tilbud**, **Ordre** eller **Fakturaer** i Dynamics 365 Sales, legges det til en ny knapp for **Lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="c4f93-109">In the header of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **On-hand Inventory** is added.</span></span> <span data-ttu-id="c4f93-110">Når du klikker på knappen, vises det en dialogboks hvor du kan angi firmaet og produktet du vil kontrollere tilgjengelig beholdning for.</span><span class="sxs-lookup"><span data-stu-id="c4f93-110">When you click the button, a dialog box appears and you can specify the company and the product for which you want to check the on-hand inventory.</span></span> <span data-ttu-id="c4f93-111">Den returnerer beholdningsinformasjonen fra Dynamics 365 Supply Chain Management, og viser den samme informasjonen som [Tilgjengelig beholdning](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="c4f93-111">It returns the inventory information from Dynamics 365 Supply Chain Management, and shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span> <span data-ttu-id="c4f93-112">Informasjonen inkluderer disse antallene:</span><span class="sxs-lookup"><span data-stu-id="c4f93-112">The information includes these quantities:</span></span>

- <span data-ttu-id="c4f93-113">**Antall på lager**</span><span class="sxs-lookup"><span data-stu-id="c4f93-113">**On-hand Quantity**</span></span>
- <span data-ttu-id="c4f93-114">**Antall reservert på lager**</span><span class="sxs-lookup"><span data-stu-id="c4f93-114">**Reserved On-hand Quantity**</span></span>
- <span data-ttu-id="c4f93-115">**Antall tilgjengelig på lager**</span><span class="sxs-lookup"><span data-stu-id="c4f93-115">**Available On-hand Quantity**</span></span>
- <span data-ttu-id="c4f93-116">**Antall bestilt**</span><span class="sxs-lookup"><span data-stu-id="c4f93-116">**Orderd Quantity**</span></span>
- <span data-ttu-id="c4f93-117">**Antall i bestilling**</span><span class="sxs-lookup"><span data-stu-id="c4f93-117">**On-order Quantity**</span></span>
- <span data-ttu-id="c4f93-118">**Antall reservert og bestilt**</span><span class="sxs-lookup"><span data-stu-id="c4f93-118">**Reserved Ordered Quantity**</span></span>
- <span data-ttu-id="c4f93-119">**Totalt tilgjengelig antall**</span><span class="sxs-lookup"><span data-stu-id="c4f93-119">**Total Available Quantity**</span></span>

## <a name="atp-information"></a><span data-ttu-id="c4f93-120">ATP-informasjon</span><span class="sxs-lookup"><span data-stu-id="c4f93-120">ATP information</span></span>

<span data-ttu-id="c4f93-121">På linjeelementer i skjemaene **Tilbud**, **Ordre** eller **Fakturaer** i Dynamics 365 Sales, legges det til en ny knapp for **ATP-informasjon**.</span><span class="sxs-lookup"><span data-stu-id="c4f93-121">On line items of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **ATP Information** is added.</span></span> <span data-ttu-id="c4f93-122">Når du klikker på knappen, vises det en dialogboks hvor du kan angi firma, produkt, beholdningsnettsted, beholdningslager og ordreantall.</span><span class="sxs-lookup"><span data-stu-id="c4f93-122">When you click the button, a dialog box appears and you can specify the company, product, inventory Site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="c4f93-123">Den returnerer **ATP-informasjon** fra Supply Chain Management, og viser innstillingene som er beskrevet i [Ordrebekreftelse](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="c4f93-123">It returns the **ATP Information** from Supply Chain Management and shows the settings descrbed in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span> <span data-ttu-id="c4f93-124">Informasjonen omfatter **ATP-antall**, **Tilgangsantall**, **Avgangsantall** og **Beholdningsantall**.</span><span class="sxs-lookup"><span data-stu-id="c4f93-124">The information includes **ATP quantity**, **Receipt quantity**, **Issue quantity**, and **On-hand quantity**.</span></span>

---
title: Utføringsordre for innledende synkronisering av Finance and Operations og Common Data Service
description: Dette emnet angir rekkefølgen for synkroniseringen du må følge for å opprette de opprinnelige dataene.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797304"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="c5c45-103">Utføringsordre for innledende synkronisering av Finance and Operations og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c5c45-103">Execution order for initial sychronization of Finance and Operations and Common Data Service</span></span>

<span data-ttu-id="c5c45-104">Før du bruker dataintegrering, må du opprette de første dataene som kreves for kunder, leverandører og kontakter.</span><span class="sxs-lookup"><span data-stu-id="c5c45-104">Before you use data integration, you must create the initial data required for customers, vendors and contacts.</span></span> <span data-ttu-id="c5c45-105">Hvis du for eksempel vil opprette en ny **Leverandørgruppe**-vare og angi **betalingsbetingelsene** som **Net30**, før du prøver å opprette **Leverandørgruppe**-varen, må du kontrollere at **Net30** finnes både i Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c5c45-105">For example, if you want to create a new **Vendor group** item and set its **Terms of Payment** as **Net30**, then before you attempt to create the **Vendor group** item you need to make sure that **Net30** exists in both Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="c5c45-106">(I fremtiden vil vi gi ut en dobbel skrive plattform funksjonalitet kalt **Initial Sync**. Det vil gjøre en éngangs datasynkronisering mellom Finance and Operations og Common Data Service som en del av dual-Write-oppsettet.)</span><span class="sxs-lookup"><span data-stu-id="c5c45-106">(In the future, we will release a  dual-write platform functionality called **Initial Sync**. It will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

<span data-ttu-id="c5c45-107">Tips: Vi lanserer et dual-Write-kart for alle referansedata inkludert **betalingsbetingelser**.</span><span class="sxs-lookup"><span data-stu-id="c5c45-107">Tips: We are releasing a dual-write map for all reference data including **Terms of Payment** (Payment Terms).</span></span> <span data-ttu-id="c5c45-108">Hvis du allerede har de opprinnelige dataene i ett system, kan en liten oppdateringsoperasjon på en oppføring utløse dobbel skriving på denne oppføringen.</span><span class="sxs-lookup"><span data-stu-id="c5c45-108">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span> 

<span data-ttu-id="c5c45-109">Du må følge følgende prioritetsrekkefølge og kontrollere at de opprinnelige dataene er tilgjengelige både i Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c5c45-109">You must follow the following order of precedence and make sure that the initial data is available on both Finance and Operations and Common Data Service.</span></span>   

## <a name="vendor"></a><span data-ttu-id="c5c45-110">Leverandør</span><span class="sxs-lookup"><span data-stu-id="c5c45-110">Vendor</span></span>

<span data-ttu-id="c5c45-111">Rekkefølgen for utførelse av leverandør er:</span><span class="sxs-lookup"><span data-stu-id="c5c45-111">The order of execution for Vendor is:</span></span>

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a><span data-ttu-id="c5c45-112">Kunde (organisasjon)</span><span class="sxs-lookup"><span data-stu-id="c5c45-112">Customer (Organization)</span></span>

<span data-ttu-id="c5c45-113">Rekkefølgen for utførelse av kunde er:</span><span class="sxs-lookup"><span data-stu-id="c5c45-113">The order of execution for Customer is:</span></span>

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a><span data-ttu-id="c5c45-114">Kontakt (person)</span><span class="sxs-lookup"><span data-stu-id="c5c45-114">Contact (Person)</span></span>

<span data-ttu-id="c5c45-115">Rekkefølgen for utførelse av kontakt er:</span><span class="sxs-lookup"><span data-stu-id="c5c45-115">The order of execution for Contact is:</span></span>

```
Customer
Vendor               
```

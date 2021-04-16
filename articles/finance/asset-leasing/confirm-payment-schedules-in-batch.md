---
title: Bekrefte betalingsplaner for aktivaleie i en bunke
description: Dette emnet forklarer hvordan du bekrefter flere betalingsplaner i en bunke.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9a3bd7293fed4b8df5d7bd76edacbcae253aa1f5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816082"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="bdc21-103">Bekrefte betalingsplaner for aktivaleie i en bunke</span><span class="sxs-lookup"><span data-stu-id="bdc21-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bdc21-104">Dette emnet forklarer hvordan du bekrefter flere betalingsplaner i en bunke.</span><span class="sxs-lookup"><span data-stu-id="bdc21-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="bdc21-105">Betalingsplaner bekreftes enten på en leie-til-leie-basis eller gjennom bunkeprosessen for bekreftelse.</span><span class="sxs-lookup"><span data-stu-id="bdc21-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="bdc21-106">En journaloppføring kan bare posteres mot en leieavtale som har en bekreftet betalingsplan.</span><span class="sxs-lookup"><span data-stu-id="bdc21-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="bdc21-107">Bekreftelse av betalingsplanen fungerer som en endelig godkjenning av den økonomiske informasjonen for leieavtalen.</span><span class="sxs-lookup"><span data-stu-id="bdc21-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="bdc21-108">Alle fremtidige endringer i den økonomiske informasjonen for leieavtalen, for eksempel betalinger og leieperioden, utgjør en leiejustering og skal behandles på denne måten.</span><span class="sxs-lookup"><span data-stu-id="bdc21-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="bdc21-109">Hvis du vil bekrefte flere betalingsplaner, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="bdc21-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="bdc21-110">Gå til **Aktivaleie \> Periodisk \> Bekreftelsesbunke**.</span><span class="sxs-lookup"><span data-stu-id="bdc21-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="bdc21-111">På siden **Bekreftelsesbunke** velger du **Bekreftelsesbunke**.</span><span class="sxs-lookup"><span data-stu-id="bdc21-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="bdc21-112">I dialogboksen som vises, filtrerer du for tablåene du vil bekrefte.</span><span class="sxs-lookup"><span data-stu-id="bdc21-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="bdc21-113">Hvis du vil bekrefte alle tablåene i en bestemt leiegruppe, velger du gruppen i feltet **Leiegruppe**.</span><span class="sxs-lookup"><span data-stu-id="bdc21-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="bdc21-114">Hvis du vil bekrefte bestemte tablåer, velger du tablåene i feltet **Tablå-ID**.</span><span class="sxs-lookup"><span data-stu-id="bdc21-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="bdc21-115">Hvis du vil bekrefte alle tablåer, aktiverer du parameteren **For alle tablåer**.</span><span class="sxs-lookup"><span data-stu-id="bdc21-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="bdc21-116">Informasjon for de nylig bekreftede bøkene vises på siden **Bekreftede tablåer**.</span><span class="sxs-lookup"><span data-stu-id="bdc21-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="bdc21-117">Etter at betalingsplanene er bekreftet, kan journaloppføringene for opprinnelig føring posteres mot leieavtalen.</span><span class="sxs-lookup"><span data-stu-id="bdc21-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
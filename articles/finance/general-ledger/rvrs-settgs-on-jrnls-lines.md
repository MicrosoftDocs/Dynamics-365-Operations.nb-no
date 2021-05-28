---
title: Tilbakefør innstillinger for journaler og linjer
description: Dette emnet omhandler hvorfor en tilbakeføringsoppføring som ble angitt i en økonomijournal, kanskje ikke er tatt med i den posterte transaksjonen.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028578"
---
# <a name="reverse-settings-on-journals-and-lines"></a><span data-ttu-id="66348-103">Tilbakefør innstillinger for journaler og linjer</span><span class="sxs-lookup"><span data-stu-id="66348-103">Reverse settings on journals and lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66348-104">Dette emnet omhandler hvorfor en tilbakeføringsoppføring som ble angitt i en økonomijournal, kanskje ikke er tatt med i den posterte transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="66348-104">This topic addresses why a reversing entry that was entered on a general journal might not be included on the posted transaction.</span></span>  

## <a name="symptom"></a><span data-ttu-id="66348-105">Symptom</span><span class="sxs-lookup"><span data-stu-id="66348-105">Symptom</span></span>

<span data-ttu-id="66348-106">En økonomijournal inneholder en tilbakeføringsoppføring og tilbakeføringsdato i journalen.</span><span class="sxs-lookup"><span data-stu-id="66348-106">A general journal includes a reversing entry and reversing date on the journal.</span></span> <span data-ttu-id="66348-107">Når du posterer journalen, tilbakeføres ingen av bilagene.</span><span class="sxs-lookup"><span data-stu-id="66348-107">When you post the journal, none of the vouchers are reversed.</span></span> <span data-ttu-id="66348-108">Hvorfor skjer dette?</span><span class="sxs-lookup"><span data-stu-id="66348-108">Why does this happen?</span></span>

## <a name="resolution"></a><span data-ttu-id="66348-109">Løsning</span><span class="sxs-lookup"><span data-stu-id="66348-109">Resolution</span></span>

<span data-ttu-id="66348-110">Når journalen posteres, ser tilbakeføringsprosessen bare på innstillingene for **tilbakeføringsoppføring** og **tilbakeføringsdato** i delen **Linjer** på bilaget.</span><span class="sxs-lookup"><span data-stu-id="66348-110">When the journal is posted, the reversing process looks only at the **Revering entry** and **Reversing date** settings on the **Lines** section of the voucher.</span></span> <span data-ttu-id="66348-111">Ved hjelp av denne fremgangsmåten kan en journal omfatte noen bilag som er merket for tilbakeføring, mens andre som ikke er det.</span><span class="sxs-lookup"><span data-stu-id="66348-111">This approach allows a journal to include some vouchers that are marked for reversing, and others that are not.</span></span>

<span data-ttu-id="66348-112">Verdiene fra journalen brukes bare som standard når det legges til *nye* linjer.</span><span class="sxs-lookup"><span data-stu-id="66348-112">The values from the journal are only used as defaults when adding *new* lines.</span></span> <span data-ttu-id="66348-113">Endring av verdiene i journalen påvirker ikke eksisterende linjer.</span><span class="sxs-lookup"><span data-stu-id="66348-113">Changing the values on the journal doesn’t affect existing lines.</span></span> <span data-ttu-id="66348-114">I dette eksemplet ble bilagslinjene lagt inn først.</span><span class="sxs-lookup"><span data-stu-id="66348-114">In this example, the voucher lines were entered first.</span></span> <span data-ttu-id="66348-115">Når du angir linjedetaljene før du angir journalen som tilbakeføring, blir ikke betegnelsen som en tilbakeføringsoppføring og -dato brukt på noen eksisterende linjer.</span><span class="sxs-lookup"><span data-stu-id="66348-115">When you enter the line detail before designating the journal as reversing, the designation as a reversing entry and date won't be applied to any existing lines.</span></span>

<span data-ttu-id="66348-116">Endring av tilbakeføringsoppføringen eller tilbakeføringsdatoen på en eksisterende linje overfører den til andre linjer i det samme bilaget.</span><span class="sxs-lookup"><span data-stu-id="66348-116">Changing the reversing entry or reversing date on an existing line propagates that change to other lines in the same voucher.</span></span> <span data-ttu-id="66348-117">For å optimalisere ytelsen oppdateres ikke rutenettet etter at endringer er overført til andre linjer.</span><span class="sxs-lookup"><span data-stu-id="66348-117">To optimize performance, the grid is not refreshed after propagating changes to other Lines.</span></span> <span data-ttu-id="66348-118">Du kan vise de oppdaterte verdiene ved å oppdatere rutenettet.</span><span class="sxs-lookup"><span data-stu-id="66348-118">You can display the updated values by refreshing the grid.</span></span>



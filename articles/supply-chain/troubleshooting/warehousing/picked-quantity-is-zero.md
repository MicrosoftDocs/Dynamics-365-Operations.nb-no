---
title: Du kan ikke bekrefte en forsendelse fordi det er null antall
description: Du kan ikke bekrefte en forsendelse fordi det er null antall
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938524"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a><span data-ttu-id="a2ef0-103">Du kan ikke bekrefte en forsendelse fordi det er null antall</span><span class="sxs-lookup"><span data-stu-id="a2ef0-103">You can't confirm a shipment because there is zero quantity</span></span>

<span data-ttu-id="a2ef0-104">Feilkode: LoadLineOppdateringUpdatedToZero</span><span class="sxs-lookup"><span data-stu-id="a2ef0-104">Error code: LoadLineWarningUpdatedToZero</span></span>

## <a name="symptoms"></a><span data-ttu-id="a2ef0-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="a2ef0-105">Symptoms</span></span>

<span data-ttu-id="a2ef0-106">Når du prøver å bekrefte en forsendelse, viser systemet følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="a2ef0-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="a2ef0-107">Belastningslinjen for varen %1 og forsendelsen %2 er oppdatert til å ha nullantall på grunn av underleveringsoppsett, noe som gjør at du ikke kan levere noen antall for denne varen.</span><span class="sxs-lookup"><span data-stu-id="a2ef0-107">Load line for item %1 and shipment %2 has been updated to have zero quantity due to underdelivery setup allowing not to ship any quantities for this item.</span></span>

<span data-ttu-id="a2ef0-108">Derfor kan du ikke bekrefte forsendelsen for belastningen.</span><span class="sxs-lookup"><span data-stu-id="a2ef0-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="a2ef0-109">Årsak</span><span class="sxs-lookup"><span data-stu-id="a2ef0-109">Cause</span></span>

<span data-ttu-id="a2ef0-110">Systemet evaluerer om det plukkede antallet er innenfor de forventede grensene, basert på plukket antall, belastningslinjeantall og underleveringsprosent.</span><span class="sxs-lookup"><span data-stu-id="a2ef0-110">The system evaluates whether the picked quantity is within the expected limits, based on the picked quantity, load line quantity, and underdelivery percentage.</span></span> <span data-ttu-id="a2ef0-111">Hvis systemet finner ut at det plukkede antallet på belastningslinjen er 0 (null), kan du ikke bekrefte forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="a2ef0-111">If the system finds that the picked quantity on the load line is 0 (zero), you can't confirm the shipment.</span></span> <span data-ttu-id="a2ef0-112">Dette problemet kan for eksempel oppstå hvis arbeidet er avbrutt og underleveringsprosenten på belastningslinjen er 100 prosent.</span><span class="sxs-lookup"><span data-stu-id="a2ef0-112">For example, this issue might occur if work has been canceled, and the underdelivery percentage on the load line is 100 percent.</span></span>

## <a name="resolution"></a><span data-ttu-id="a2ef0-113">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="a2ef0-113">Resolution</span></span>

<span data-ttu-id="a2ef0-114">Kontroller belastningslinjene for å være sikker på at underleveringsprosenten og antallet samkjøres med det plukkede arbeidet.</span><span class="sxs-lookup"><span data-stu-id="a2ef0-114">Check your load lines to make sure that the underdelivery percentage and quantities are aligned with the picked work.</span></span>

1. <span data-ttu-id="a2ef0-115">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="a2ef0-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="a2ef0-116">Velg belastningen som forsendelsen ikke kan bekreftes for.</span><span class="sxs-lookup"><span data-stu-id="a2ef0-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="a2ef0-117">I hurtigfanen **Lastlinjer** velger du lastlinjen for varen som overskrider underleveringsprosenten.</span><span class="sxs-lookup"><span data-stu-id="a2ef0-117">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="a2ef0-118">Juster verdien i **Underlevering**-feltet eller **Antall**-feltet etter behov.</span><span class="sxs-lookup"><span data-stu-id="a2ef0-118">Adjust the value of the **Underdelivery** field or the **Quantity** field as required.</span></span>

> [!TIP]
> <span data-ttu-id="a2ef0-119">Hvis problemet fremdeles ikke er løst, kan det hende at du må fullføre mer plukkarbeid for de tilknyttede salgsordrene eller overføringsordrene til det tilgjengelige antallet er samkjørt med belastningen eller forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="a2ef0-119">If the issue still isn't fixed, you might have to complete more picking work for the related sales orders or transfer orders until the available quantity is aligned with the load or shipment.</span></span>

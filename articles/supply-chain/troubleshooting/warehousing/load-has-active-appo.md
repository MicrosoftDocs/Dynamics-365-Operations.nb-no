---
title: Du kan ikke bekrefte en forsendelse på grunn av et problem med kalenderen
description: Du kan ikke bekrefte en forsendelse på grunn av et problem med kalenderen
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
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938527"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a><span data-ttu-id="7db66-103">Du kan ikke bekrefte en forsendelse på grunn av et problem med kalenderen</span><span class="sxs-lookup"><span data-stu-id="7db66-103">You can't confirm a shipment because of an issue with the calendar</span></span>

<span data-ttu-id="7db66-104">Feilkode: TRX2716</span><span class="sxs-lookup"><span data-stu-id="7db66-104">Error code: TRX2716</span></span>

## <a name="symptoms"></a><span data-ttu-id="7db66-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="7db66-105">Symptoms</span></span>

<span data-ttu-id="7db66-106">Når du prøver å bekrefte en forsendelse, viser systemet følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="7db66-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="7db66-107">Kalendertype %1 krever at avtale %2 sjekkes inn og ut.</span><span class="sxs-lookup"><span data-stu-id="7db66-107">The calendar type %1 requires the appointment %2 to be checked in and out.</span></span>

<span data-ttu-id="7db66-108">Derfor kan du ikke bekrefte forsendelsen for belastningen.</span><span class="sxs-lookup"><span data-stu-id="7db66-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="7db66-109">Årsak</span><span class="sxs-lookup"><span data-stu-id="7db66-109">Cause</span></span>

<span data-ttu-id="7db66-110">Det finnes aktive avtaler for lasten.</span><span class="sxs-lookup"><span data-stu-id="7db66-110">Active appointments for the load exist.</span></span> <span data-ttu-id="7db66-111">Det finnes for eksempel en regel som krever sjåførinnsjekking.</span><span class="sxs-lookup"><span data-stu-id="7db66-111">For example, there is a rule that requires driver check-in.</span></span> <span data-ttu-id="7db66-112">Derfor er lasten for øyeblikket i en tilstand der forsendelsesbekreftelsen mislykkes.</span><span class="sxs-lookup"><span data-stu-id="7db66-112">Therefore, the load is currently in a state where shipment confirmation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="7db66-113">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="7db66-113">Resolution</span></span>

<span data-ttu-id="7db66-114">Du må undersøke og rette eventuelle problemer med de aktive avtalene som er koblet til lasten.</span><span class="sxs-lookup"><span data-stu-id="7db66-114">You must investigate and fix any issues with the active appointments that are linked to the load.</span></span>

1. <span data-ttu-id="7db66-115">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="7db66-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="7db66-116">Velg belastningen som forsendelsen ikke kan bekreftes for.</span><span class="sxs-lookup"><span data-stu-id="7db66-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="7db66-117">På handlingsruten i fanen **Transport** i **Avtaler**-gruppen velger du **Avtaleplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="7db66-117">On the Action Pane, on the **Transportation** tab, in the **Appointments** group, select **Appointment scheduling**.</span></span>
1. <span data-ttu-id="7db66-118">Følg ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="7db66-118">Follow one of these steps:</span></span>

    - <span data-ttu-id="7db66-119">Kontroller at sjåførinnsjekking/-utsjekkingen er fullført for avtalen.</span><span class="sxs-lookup"><span data-stu-id="7db66-119">Make sure that driver check-in/check-out is completed for the appointment.</span></span>
    - <span data-ttu-id="7db66-120">Fullfør eller avbryt avtalen.</span><span class="sxs-lookup"><span data-stu-id="7db66-120">Complete or cancel the appointment.</span></span>
    - <span data-ttu-id="7db66-121">Deaktiver alternativet **Krever sjåførinnsjekking** for den relaterte avtaleregelen.</span><span class="sxs-lookup"><span data-stu-id="7db66-121">Disable the **Driver check-in required** option for the related appointment rule.</span></span>

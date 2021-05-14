---
title: Vektfeltene på lastlinjene stemmer ikke overens med vektfeltene på lasten
description: Vektfeltene på lastlinjene stemmer ikke overens med vektfeltene på lasten
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924357"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a><span data-ttu-id="b264e-103">Vektfeltene på lastlinjene stemmer ikke overens med vektfeltene på lasten</span><span class="sxs-lookup"><span data-stu-id="b264e-103">The weight fields on load lines don't match the weight fields on the load</span></span>

<span data-ttu-id="b264e-104">Feilkoder: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span><span class="sxs-lookup"><span data-stu-id="b264e-104">Error codes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span></span>

## <a name="symptoms"></a><span data-ttu-id="b264e-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="b264e-105">Symptoms</span></span>

<span data-ttu-id="b264e-106">Systemet viser følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="b264e-106">The system shows the following error message:</span></span>

> <span data-ttu-id="b264e-107">Vektfeltene på lastlinjene stemmer ikke overens med vektfeltene på lasten %1.</span><span class="sxs-lookup"><span data-stu-id="b264e-107">The weight fields on load lines do not match the weight fields on load %1.</span></span> <span data-ttu-id="b264e-108">Kjør konsekvenskontroll av lagerlastvekt for å beregne vektfeltene på nytt.</span><span class="sxs-lookup"><span data-stu-id="b264e-108">Run the Warehouse load weight consistency check to recalculate the weight fields.</span></span>

## <a name="cause"></a><span data-ttu-id="b264e-109">Årsak</span><span class="sxs-lookup"><span data-stu-id="b264e-109">Cause</span></span>

<span data-ttu-id="b264e-110">Feltene **Nettovekt** og **Taravekt** settes til *0* (null) på lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="b264e-110">The **Net weight** and **Tara weight** fields are set to *0* (zero) on the load line.</span></span> <span data-ttu-id="b264e-111">Vektfeltene settes imidlertid ikke til *0* for vektmålinger på produktet.</span><span class="sxs-lookup"><span data-stu-id="b264e-111">However, the weight fields aren't set to *0* for the weight measurements on the product.</span></span> <span data-ttu-id="b264e-112">Når vektfeltene ikke er angitt på lastlinjen, kan alle rettelser av antallet på lastlinjene føre til feil vektberegning på lasten.</span><span class="sxs-lookup"><span data-stu-id="b264e-112">When weight fields aren't set on the load line, any corrections of the quantity on the load line might cause incorrect weight calculation on the load.</span></span> <span data-ttu-id="b264e-113">Dette problemet kan oppstå hvis vekten på produktet er endret siden lastlinjen ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="b264e-113">This issue might occur if the weights on the product have been changed since the load line was created.</span></span>

## <a name="resolution"></a><span data-ttu-id="b264e-114">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="b264e-114">Resolution</span></span>

<span data-ttu-id="b264e-115">Når det opprettes en lastlinje, angis vektfeltene fra produktet som standard på den.</span><span class="sxs-lookup"><span data-stu-id="b264e-115">By default, when a load line is created, the weight fields from the product are entered on it.</span></span> <span data-ttu-id="b264e-116">Hvis vekten er null, kan du omberegne den ved å bruke funksjonaliteten for *konsekvenskontroll av lagerlastvekt*.</span><span class="sxs-lookup"><span data-stu-id="b264e-116">If the weight is zero, you can recalculate it by using the *Warehouse load weight consistency check* functionality.</span></span>

1. <span data-ttu-id="b264e-117">Gå til **Systemadministrasjon \> Periodiske oppgaver \> Database \> Konsekvenskontroll**.</span><span class="sxs-lookup"><span data-stu-id="b264e-117">Go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="b264e-118">I dialogboksen **Konsekvenskontroll** setter du **Modul**-feltet til *Lagerstyring*.</span><span class="sxs-lookup"><span data-stu-id="b264e-118">In the **Consistency check** dialog box, set the **Module** field to *Warehouse management*.</span></span>
1. <span data-ttu-id="b264e-119">Sett feltet **Kontroller/korriger** til *Rett feil*.</span><span class="sxs-lookup"><span data-stu-id="b264e-119">Set the **Check/Fix** field to *Fix error*.</span></span>
1. <span data-ttu-id="b264e-120">Merk av for **Konsekvenskontroll av lagerlastvekt** i avmerkingslisteboksen, og kontroller at bare raden for denne avmerkingsboksen er uthvevet.</span><span class="sxs-lookup"><span data-stu-id="b264e-120">In the checkbox list, select the **Warehouse load weight consistency check** checkbox, and make sure that only the row for this checkbox is highlighted.</span></span>
1. <span data-ttu-id="b264e-121">Øverst i avmerkingsbokslisten velger du ellipseknappen (**...**), og deretter velger du **Dialogboks** på menyen.</span><span class="sxs-lookup"><span data-stu-id="b264e-121">At the top of the checkbox list, select the ellipsis button (**...**), and then select **Dialog** on the menu.</span></span>
1. <span data-ttu-id="b264e-122">I **Konsekvenskontroll av lagerlastvekt** definerer du følgende felt for å angi kriteriene som konsekvenskontrollen skal kjøres for:</span><span class="sxs-lookup"><span data-stu-id="b264e-122">In the **Warehouse load weight consistency check** dialog box, set the following fields to specify the criteria that the consistency check should run for:</span></span>

    - <span data-ttu-id="b264e-123">**Last-ID:** Angi en last-ID.</span><span class="sxs-lookup"><span data-stu-id="b264e-123">**Load ID:** Specify a load ID.</span></span> <span data-ttu-id="b264e-124">La denne stå tom for å kontrollere alle last-IDene.</span><span class="sxs-lookup"><span data-stu-id="b264e-124">Leave this blank to check all load IDs.</span></span>
    - <span data-ttu-id="b264e-125">**Varenummer:** Angi et varenummer.</span><span class="sxs-lookup"><span data-stu-id="b264e-125">**Item number:** Specify an item number.</span></span> <span data-ttu-id="b264e-126">La denne stå tom for å kontrollere alle elementer.</span><span class="sxs-lookup"><span data-stu-id="b264e-126">Leave this blank to check all items.</span></span>
    - <span data-ttu-id="b264e-127">**Omberegn alltid vekt på last:** Sett dette alternativet til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="b264e-127">**Always recalculate weight on loads:** Set this option to *Yes*.</span></span>
    - <span data-ttu-id="b264e-128">**Tillat overskriving av vekt på lastlinjer:** Sett dette alternativet til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="b264e-128">**Allow overwrite of weight on load lines:** Set this option to *Yes*.</span></span>

1. <span data-ttu-id="b264e-129">Velg **OK** for å lukke dialogboksen **Konsekvenskontroll av lagerlastvekt**.</span><span class="sxs-lookup"><span data-stu-id="b264e-129">Select **OK** to close the **Warehouse load weight consistency check** dialog box.</span></span>
1. <span data-ttu-id="b264e-130">Velg ellipseknappen, og velg deretter **Utfør** på menyen.</span><span class="sxs-lookup"><span data-stu-id="b264e-130">Select the ellipsis button, and then select **Execute** on the menu.</span></span>

<span data-ttu-id="b264e-131">Vekten beregnes på nytt basert på kriteriene du har angitt.</span><span class="sxs-lookup"><span data-stu-id="b264e-131">The weight is recalculated based on the criteria that you specified.</span></span> <span data-ttu-id="b264e-132">Velg koblingen **Meldingsdetaljer** for å vise resultatet av konsistenskontrollen.</span><span class="sxs-lookup"><span data-stu-id="b264e-132">Select the **Message details** link to view the result of the consistency check.</span></span>

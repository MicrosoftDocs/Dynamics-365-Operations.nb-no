---
title: Konfigurere TDS-parametere i Leverandører og Kunder
description: Dette emnet forklarer hvordan du angir parametere i Leverandører og Kunder for å støtte TDS-fradrag (Tax Deducted at Source).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023478"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="04e59-103">Konfigurere TDS-parametere i Leverandører og Kunder</span><span class="sxs-lookup"><span data-stu-id="04e59-103">Set TDS parameters in Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04e59-104">Dette emnet forklarer hvordan du angir parametere i Leverandører og Kunder for å støtte TDS-fradrag (Tax Deducted at Source).</span><span class="sxs-lookup"><span data-stu-id="04e59-104">This topic explains how to set parameters in Accounts payable and Accounts receivable to support Tax Deducted at Source (TDS) deductions.</span></span>

1. <span data-ttu-id="04e59-105">Gå til **Avgift \> Oppsett \> Parametere \> Kundeparametere**.</span><span class="sxs-lookup"><span data-stu-id="04e59-105">Go to **Tax \> Setup \> Parameters \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="04e59-106">Velg **Oppdater ordrelinjer** i **Oppdateringer**-fanen for å åpne dialogboksen **Oppdater ordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="04e59-106">On the **Updates** tab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
3. <span data-ttu-id="04e59-107">Angi metoden du vil bruke til å oppdatere TDS-gruppen på linjenivået, i feltet **Oppdatering av TDS-gruppe** i delen **TDS-gruppe**.</span><span class="sxs-lookup"><span data-stu-id="04e59-107">In the **TDS group** section, in the **Updating TDS group** field, specify the method to use to update the TDS group at the line level.</span></span> <span data-ttu-id="04e59-108">Denne innstillingen brukes når TDS-gruppen oppdateres i et ordrehode.</span><span class="sxs-lookup"><span data-stu-id="04e59-108">This setting is used when the TDS group is updated on an order header.</span></span> <span data-ttu-id="04e59-109">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="04e59-109">The following options are available:</span></span>

    - <span data-ttu-id="04e59-110">**Aldri** – TDS-gruppen oppdateres ikke på ordrelinjene når den oppdateres i ordrehodet.</span><span class="sxs-lookup"><span data-stu-id="04e59-110">**Never** – The TDS group isn't updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="04e59-111">**Alltid** – TDS-gruppen oppdateres automatisk på ordrelinjene når den oppdateres i ordrehodet.</span><span class="sxs-lookup"><span data-stu-id="04e59-111">**Always** – The TDS group is automatically updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="04e59-112">**Be om** – Brukere får en melding der de blir bedt om å oppdatere TDS-gruppen på ordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="04e59-112">**Prompt** – Users receive a message that prompts them to update the TDS group on the order lines.</span></span>
4. <span data-ttu-id="04e59-113">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="04e59-113">Select **OK**.</span></span>

    <span data-ttu-id="04e59-114">[![Dialogboksen Oppdater ordrelinjer](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span><span class="sxs-lookup"><span data-stu-id="04e59-114">[![Update order lines dialog box](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span></span>

5. <span data-ttu-id="04e59-115">Gå til **Avgift \> Oppsett \> Parametere \> Leverandørparametere**.</span><span class="sxs-lookup"><span data-stu-id="04e59-115">Go to **Tax \> Setup \> Parameters \> Accounts payable parameters**.</span></span>
6. <span data-ttu-id="04e59-116">Sett alternativet **Produktkvittering** til **Ja** i hurtigfanen **Del basert på leveringsinformasjon** i **Generelt**-fanen hvis du vil postere og dele en produktkvittering som har ulike leveringsadresser og TAN-numre.</span><span class="sxs-lookup"><span data-stu-id="04e59-116">On the **General** tab, on the **Split based on delivery information** FastTab, set the **Product receipt** option to **Yes** to post and split a product receipt that has different delivery addresses and tax account numbers (TANs).</span></span> <span data-ttu-id="04e59-117">Hvis du setter dette alternativet til **Nei**, kan du ikke postere en bestillingsfølgeseddel som har ulike leveringsadresser og TAN-numre.</span><span class="sxs-lookup"><span data-stu-id="04e59-117">If this option is set to **No**, you can't post a purchase packing slip that has different delivery addresses and TANs.</span></span>
7. <span data-ttu-id="04e59-118">Sett alternativet **Faktura** til **Ja** for å postere og dele en innkjøpsfaktura som har ulike leveringsadresser og TAN-numre.</span><span class="sxs-lookup"><span data-stu-id="04e59-118">Set the **Invoice** option to **Yes** to post and split a purchase invoice that has different delivery addresses and TANs.</span></span>

    <span data-ttu-id="04e59-119">[![Hurtigfanen Del basert på leveringsinformasjon](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span><span class="sxs-lookup"><span data-stu-id="04e59-119">[![Split based on delivery information FastTab](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span></span>

8. <span data-ttu-id="04e59-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="04e59-120">Close the page.</span></span>

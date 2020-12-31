---
title: Konfigurere parametere for leieavtale (forhåndsversjon)
description: Dette emnet beskriver konfigurasjonsinnstillingene for Aktivaleie, for eksempel sikkerhetsinformasjon og regnskapsinnstillinger.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f71006570cd8f2bdc0385388eae0800cd29d3ec8
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446597"
---
# <a name="configure-lease-parameters"></a><span data-ttu-id="88fcf-103">Konfigurere parametere for leieavtale</span><span class="sxs-lookup"><span data-stu-id="88fcf-103">Configure lease parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88fcf-104">Flere konfigurasjonsinnstillinger påvirker hvordan Aktivaleie fungerer.</span><span class="sxs-lookup"><span data-stu-id="88fcf-104">Several configuration settings affect how Asset leasing behaves.</span></span> <span data-ttu-id="88fcf-105">Disse innstillingene omfatter journalnavn, generelle parametere og postering av profilinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="88fcf-105">These settings include journal names, general parameters, and posting profile settings.</span></span>

1. <span data-ttu-id="88fcf-106">Gå til **Aktivaleie \> Oppsett \> Parametere for aktivaleie**.</span><span class="sxs-lookup"><span data-stu-id="88fcf-106">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="88fcf-107">Velg hurtigfanen **Generelt** i fanen **Leieavtaler**.</span><span class="sxs-lookup"><span data-stu-id="88fcf-107">On the **Leases** tab, select the **General** FastTab.</span></span>

    <span data-ttu-id="88fcf-108">Parameteren **Tillat manuell overstyring av klassifisering** avgjør om leieavtaleklassifiseringen kan overstyres før betalingsplanen er bekreftet.</span><span class="sxs-lookup"><span data-stu-id="88fcf-108">The **Allow manual classification override** parameter determines whether the lease classification can be overridden before the payment schedule is confirmed.</span></span>

    <span data-ttu-id="88fcf-109">Parameteren **Parti på tvers av enheter** fastsetter om du kan postere i andre juridiske enheter fra den gjeldende juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="88fcf-109">The **Cross-entity batch** parameter determines whether you can post to other legal entities from the current legal entity.</span></span> <span data-ttu-id="88fcf-110">Hvis denne parameteren er aktivert, kan du opprette journaloppføringer for de juridiske enhetene du har tilgang til.</span><span class="sxs-lookup"><span data-stu-id="88fcf-110">If this parameter is turned on, you can create journal entries for the legal entities that you have access to.</span></span>

3. <span data-ttu-id="88fcf-111">Sett alternativet **Tillat sletting av bekreftede leieavtaler** til **Ja** for å tillate at leieavtaler som har bekreftede betalingsplaner, slettes.</span><span class="sxs-lookup"><span data-stu-id="88fcf-111">Set the **Allow delete of confirmed leases** option to **Yes** to allow leases that have confirmed payment schedules to be deleted.</span></span> <span data-ttu-id="88fcf-112">Leieavtaler kan ikke slettes hvis det er knyttet posterte eller uposterte transaksjoner til dem, uavhengig av innstillingen for dette alternativet.</span><span class="sxs-lookup"><span data-stu-id="88fcf-112">Leases can't be deleted if posted or unposted transactions are associated with them, regardless of the setting of this option.</span></span> <span data-ttu-id="88fcf-113">Du kan ikke gjenopprette en leiepost etter at den er slettet.</span><span class="sxs-lookup"><span data-stu-id="88fcf-113">You can't restore a lease record after it's deleted.</span></span> <span data-ttu-id="88fcf-114">Hvis du laster opp poster for en slettet leieavtale, enten manuelt eller gjennom dataenheter, behandles den opplastede informasjonen som ny, ikke som en oppdatering for en eksisterende leieavtale.</span><span class="sxs-lookup"><span data-stu-id="88fcf-114">If you upload any records for a deleted lease, either manually or through data entities, the uploaded information is treated as new, not as an update to an existing lease.</span></span>

    <span data-ttu-id="88fcf-115">Hvis du setter dette alternativet til **Ja** og overgangstypen for tablået er **Kumulativt oppdateringsalternativ A eller B**, setter systemet feltet **Trinnvis lånerente** til verdien i feltet **Trinnvis lånerente ved overgang** på siden **Tablåoppsett**.</span><span class="sxs-lookup"><span data-stu-id="88fcf-115">If you set this option to **Yes**, and the transition type of the book is **Cumulative Catchup Option A or B**, the system sets the **Incremental borrowing rate** field to the value of the **Incremental borrowing rate at transition** field on the **Book setup** page.</span></span> <span data-ttu-id="88fcf-116">Hvis dette alternativet er satt til **Nei**, settes satsen for hodeleien til verdien i feltet **Trinnvis lånerente** på siden **Tablådetaljer**, uansett hva som er overgangstypen for tablået.</span><span class="sxs-lookup"><span data-stu-id="88fcf-116">If this option is set to **No**, the rate on the head lease is set to the value of the **Incremental borrowing rate** field on the **Book details** page, regardless of the transition type of the book.</span></span>

4. <span data-ttu-id="88fcf-117">Sett alternativet **Tillat tilbakeføring av avskrivning i en lukket tablåversjon** til **Ja** for å tillate at utgiftstransaksjoner for avskrivning tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="88fcf-117">Set the **Allow depreciation reversals on closed book version** option to **Yes** to allow depreciation expense transactions to be reversed.</span></span> <span data-ttu-id="88fcf-118">Utgiftstransaksjoner kan tilbakeføres selv om tablåversjonen er lukket.</span><span class="sxs-lookup"><span data-stu-id="88fcf-118">Expense transactions can be reversed even when the book version is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="88fcf-119">Vi anbefaler at du lar dette alternativet være satt til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="88fcf-119">We recommend that you keep this option set to **No**.</span></span> <span data-ttu-id="88fcf-120">Innstillingen for dette alternativet brukes som validering og kontroll til å forhindre at en lukket tablåversjon blir avskrevet ved et uhell.</span><span class="sxs-lookup"><span data-stu-id="88fcf-120">The setting of this option is used as a validation and control to prevent a closed book version from being accidently depreciated.</span></span> <span data-ttu-id="88fcf-121">Når du har alternativet satt til **Nei**, bidrar du til å holde netto bokført verdi og fremtidige avskrivningsberegninger nøyaktige.</span><span class="sxs-lookup"><span data-stu-id="88fcf-121">By keeping the option set to **No**, you help keep the net book value and future depreciation calculations accurate.</span></span>

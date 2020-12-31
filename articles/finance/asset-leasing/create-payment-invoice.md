---
title: Opprette betalingsfakturaer
description: Dette emnet forklarer hvordan du oppretter månedlige leiefakturaer. Du kan opprette fakturaer for individuelle leieavtaler, eller du kan bruke en satsvis prosess til å opprette dem for flere leieavtaler.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 32618814d00cb1e1f1082169a64b187cce1e76b4
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446583"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="c9325-104">Opprette betalingsfakturaer</span><span class="sxs-lookup"><span data-stu-id="c9325-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9325-105">Du kan opprette månedlige fakturaer for individuelle leieavtaler, eller du kan bruke en satsvis prosess til å opprette dem for flere leieavtaler.</span><span class="sxs-lookup"><span data-stu-id="c9325-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="c9325-106">Følgende fremgangsmåte viser hvordan du oppretter en individuell oppføring for leiebetaling når parameteren **Betal til leverandør** på siden **Oppsett av leietablå** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="c9325-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="c9325-107">På siden **Leiesammendrag** velger du en leieavtale, og deretter velger du **Tablåer \> Betalingsplan**.</span><span class="sxs-lookup"><span data-stu-id="c9325-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="c9325-108">Velg betalingen som må gjøres, og velg deretter **Opprett journal**.</span><span class="sxs-lookup"><span data-stu-id="c9325-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="c9325-109">Du får en melding om at det ble opprettet en journal mot den valgte betalingen.</span><span class="sxs-lookup"><span data-stu-id="c9325-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="c9325-110">Velg **Fakturajournaler**, og velg deretter fakturaen som må betales.</span><span class="sxs-lookup"><span data-stu-id="c9325-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="c9325-111">Se gjennom journaloppføringen på **Linjer**-siden før du posterer den i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="c9325-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c9325-112">Leverandørfakturalinjene som opprettes, bruer som standard leverandørposteringsprofilen fra siden **Leverandørparametere**.</span><span class="sxs-lookup"><span data-stu-id="c9325-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="c9325-113">Velg riktig journal, og velg deretter fakturaen som må betales.</span><span class="sxs-lookup"><span data-stu-id="c9325-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="c9325-114">I dette eksemplet er parameteren **Betal til leverandør** i leietablået aktivert.</span><span class="sxs-lookup"><span data-stu-id="c9325-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="c9325-115">Fakturaen kommer derfor til å være i fakturajournalen.</span><span class="sxs-lookup"><span data-stu-id="c9325-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="c9325-116">**Oversikt**-delen viser et sammendrag av journaloppføringen, og **Linjer**-delen viser detaljer om de faktiske journallinjene.</span><span class="sxs-lookup"><span data-stu-id="c9325-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c9325-117">Hvis parameteren **Betal til leverandør** er deaktivert, blir betalingsjournaloppføringer oppført på siden **Aktivaleie** for leietablået, og systemet oppretter en aktivaleieoppføring i stedet for en faktura.</span><span class="sxs-lookup"><span data-stu-id="c9325-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="c9325-118">Oppføringen for leiebetaling blir postert i journalnavnet som er angitt i feltet **Journal for månedlig leie**.</span><span class="sxs-lookup"><span data-stu-id="c9325-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="c9325-119">Etter at transaksjonen er postert, kan du vise transaksjonsinformasjonen og den bokførte verdien til leieforpliktelse ved å velge **Gjeldstransaksjoner** i leietablået.</span><span class="sxs-lookup"><span data-stu-id="c9325-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="c9325-120">Det merkes av for **Journal postert** i betalingsplanen, og linjen viser fakturajournalnummeret.</span><span class="sxs-lookup"><span data-stu-id="c9325-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="c9325-121">Etter at en betalingsjournal og en oppføring for denne journalen er opprettet, må du tilbakeføre oppføringen før den kan opprettes på nytt.</span><span class="sxs-lookup"><span data-stu-id="c9325-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>

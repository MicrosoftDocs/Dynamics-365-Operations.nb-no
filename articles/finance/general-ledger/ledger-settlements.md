---
title: Utligninger
description: Dette emnet forklarer hvordan du bruker siden Utligninger til å utligne finanstransaksjoner og tilbakeføre utligninger.
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 01764db27eb7061deeddc01997f16a43f9cb00c6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186446"
---
# <a name="ledger-settlements"></a><span data-ttu-id="08c83-103">Utligninger</span><span class="sxs-lookup"><span data-stu-id="08c83-103">Ledger settlements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08c83-104">Med utligninger kan du samsvare debet- og kredittransaksjoner i økonomimodulen og merke dem som utlignet.</span><span class="sxs-lookup"><span data-stu-id="08c83-104">Ledger settlements let you match debit and credit transactions in the general ledger, and mark them as settled.</span></span> <span data-ttu-id="08c83-105">På denne måten kan du kontrollere at relaterte transaksjoner er fjernet.</span><span class="sxs-lookup"><span data-stu-id="08c83-105">In this way, you can make sure that related transactions have been cleared.</span></span> <span data-ttu-id="08c83-106">Du kan også tilbakeføre utligninger hvis de ble opprettet ved en feiltakelse.</span><span class="sxs-lookup"><span data-stu-id="08c83-106">You can also reverse settlements if they were made by mistake.</span></span>

## <a name="enable-advanced-ledger-settlements"></a><span data-ttu-id="08c83-107">Aktivere avanserte utligninger</span><span class="sxs-lookup"><span data-stu-id="08c83-107">Enable advanced ledger settlements</span></span>

<span data-ttu-id="08c83-108">Siden for avanserte utligninger gir flere muligheter for filtrering og valg av transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="08c83-108">The advanced ledger settlements page provides additional capabilities for filtering and selecting transactions.</span></span> <span data-ttu-id="08c83-109">Gjør følgende for å aktivere siden for avanserte utligninger.</span><span class="sxs-lookup"><span data-stu-id="08c83-109">To enable advanced ledger settlements page, follow these steps.</span></span>

1. <span data-ttu-id="08c83-110">Velg **Økonomimodul** \> **Finansoppsett** \> **Parametere for økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="08c83-110">Select **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span> 
2. <span data-ttu-id="08c83-111">I fanen **Finansutligninger** setter du alternativet **Avanserte utligninget** til **Ja** for å aktivere funksjonen for avansert utligning.</span><span class="sxs-lookup"><span data-stu-id="08c83-111">On the **Ledger settlements** tab, set the **Advanced ledger settlement** option to **Yes** to turn on the advanced ledger settlement functionality.</span></span> <span data-ttu-id="08c83-112">Siden **Finansutligninger** vil bli brukt når du velger **Utligninger** i **Periodiske oppgaver**.</span><span class="sxs-lookup"><span data-stu-id="08c83-112">The advanced **Ledger settlements** page will be used when you select **Ledger settlements** in the **Periodic tasks**.</span></span> 
3. <span data-ttu-id="08c83-113">Du må angi listen over kontoer som skal brukes for utligninger for hver kontoplan.</span><span class="sxs-lookup"><span data-stu-id="08c83-113">You must enter the list of accounts to use for ledger settlements for each chart of accounts.</span></span> <span data-ttu-id="08c83-114">Denne listen brukes til å filtrere listen over transaksjoner som vises på siden **Utligninger**.</span><span class="sxs-lookup"><span data-stu-id="08c83-114">This list is used to filter the list of transactions that appears on the **Ledger settlements** page.</span></span> <span data-ttu-id="08c83-115">I listen **Kontoplan** velger du en kontoplan, og deretter velger du **Ny** for å legge til nye kontoer i listen.</span><span class="sxs-lookup"><span data-stu-id="08c83-115">In the **Chart of accounts** list, select a chart of accounts, and then select **New** to add new accounts to the list.</span></span>

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a><span data-ttu-id="08c83-116">Utlign transaksjoner ved hjelp av siden for avanserte utligninger</span><span class="sxs-lookup"><span data-stu-id="08c83-116">Settle transactions by using the advanced ledger settlements page</span></span>

<span data-ttu-id="08c83-117">Hvis du vil utligne finanstransaksjoner, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="08c83-117">To settle ledger transactions, follow these steps.</span></span>

1. <span data-ttu-id="08c83-118">Velg **Økonomimodul** \> **Periodiske oppgaver** \> **Utligninger**.</span><span class="sxs-lookup"><span data-stu-id="08c83-118">Select **General ledger** \> **Periodic tasks** \> **Ledger settlements**.</span></span>
2. <span data-ttu-id="08c83-119">Definer filtrene øverst på siden:</span><span class="sxs-lookup"><span data-stu-id="08c83-119">Set the filters at the top of the page:</span></span>

    - <span data-ttu-id="08c83-120">Velg et datointervall, eller velg **Datointervallkode** for å automatisk fylle ut datointervallet.</span><span class="sxs-lookup"><span data-stu-id="08c83-120">Select a date range, or select **Date interval code** to automatically fill in the date range.</span></span>
    - <span data-ttu-id="08c83-121">Endre posteringslaget etter behov.</span><span class="sxs-lookup"><span data-stu-id="08c83-121">Change the posting layer as you require.</span></span>
    - <span data-ttu-id="08c83-122">Velg et finansdimensjonsett for å vise finanskontoen og dimensjonene separat.</span><span class="sxs-lookup"><span data-stu-id="08c83-122">To show the ledger account and dimensions separately, select a financial dimension set.</span></span>

3. <span data-ttu-id="08c83-123">Velg **Vis transaksjoner** for å vise alle transaksjonene som samsvarer med filtrene du angav, og listen over kontoer som du angav da du konfigurerte kontoplanen i den forrige delen.</span><span class="sxs-lookup"><span data-stu-id="08c83-123">Select **Display transactions** to show all the transactions that match the filters that you set and the list of accounts that you specified when you set up the chart of accounts list in the previous section.</span></span> <span data-ttu-id="08c83-124">Hvis du endrer noen av filtrene eller dimensjonssettene, må du velge **Vis transaksjoner** på nytt.</span><span class="sxs-lookup"><span data-stu-id="08c83-124">If you change any of the filters or the dimension sets, you must select **Display transactions** again.</span></span>
4. <span data-ttu-id="08c83-125">Velg én eller flere linjer som du vurderer for utligning.</span><span class="sxs-lookup"><span data-stu-id="08c83-125">Select one or more lines that you're considering for settlement.</span></span> <span data-ttu-id="08c83-126">Verdien for feltet **Valgt beløp** øverst på siden økes eller reduseres med det totale beløpet på linjene som du har valgt.</span><span class="sxs-lookup"><span data-stu-id="08c83-126">The value of the **Selected amount** field at the top of the page increases or decreases by the total amount on the lines that you selected.</span></span>
5. <span data-ttu-id="08c83-127">Når du er ferdig med å velge transaksjoner, velger du **Merk som valgt**.</span><span class="sxs-lookup"><span data-stu-id="08c83-127">After you've finished selecting transactions, select **Mark selected**.</span></span> <span data-ttu-id="08c83-128">Det vises en hake i **Merket**-kolonnen for hver transaksjon du har valgt.</span><span class="sxs-lookup"><span data-stu-id="08c83-128">A check mark appears in the **Marked** column for each transaction that you selected.</span></span> <span data-ttu-id="08c83-129">I tillegg økes eller reduseres verdien for feltet **Merket beløp** over rutenettet med det totale beløpet på linjene du merket.</span><span class="sxs-lookup"><span data-stu-id="08c83-129">Additionally, the value of the **Marked amount** field above the grid increases or decreases by the total amount on the lines that you marked.</span></span>
6. <span data-ttu-id="08c83-130">Når **Merket beløp**-verdien er **0** (null), velger du **Utligne merkede transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="08c83-130">When the **Marked amount** value is **0** (zero), select **Settle marked transactions**.</span></span> <span data-ttu-id="08c83-131">Statusen for de merkede transaksjonene oppdateres til **Utlignet**.</span><span class="sxs-lookup"><span data-stu-id="08c83-131">The status of the marked transactions is updated to **Settled**.</span></span>

## <a name="make-transactions-easier-to-find"></a><span data-ttu-id="08c83-132">Gjøre det enklere å finne transaksjoner</span><span class="sxs-lookup"><span data-stu-id="08c83-132">Make transactions easier to find</span></span>

<span data-ttu-id="08c83-133">Siden **Finansutligninger** inkluderer funksjoner som gjør det enklere å vise transaksjoner som er nødvendige for utligning.</span><span class="sxs-lookup"><span data-stu-id="08c83-133">The **Ledger settlements** page includes capabilities that make it easier to see the transactions that you need for settlement.</span></span>

- <span data-ttu-id="08c83-134">Knappen **Fjern merket** sletter feltet **Merket** for alle linjer som er valgt.</span><span class="sxs-lookup"><span data-stu-id="08c83-134">The **Unmark selected** button clears the **Marked** field for all lines that are selected.</span></span>
- <span data-ttu-id="08c83-135">Filteret **Merket** lar deg filtrere transaksjoner basert på om **Merket**-feltet for transaksjonene er merket eller fjernet.</span><span class="sxs-lookup"><span data-stu-id="08c83-135">The **Marked** filter lets you filter transactions based on whether the **Marked** field for them is selected or cleared.</span></span>
- <span data-ttu-id="08c83-136">Filteret **Status** lar deg filtrere transaksjoner basert på om den tilhørende statusen er **Utlignet** eller **Ikke utlignet**.</span><span class="sxs-lookup"><span data-stu-id="08c83-136">The **Status** filter lets you filter transactions based on whether their status is **Settled** or **Not settled**.</span></span>
- <span data-ttu-id="08c83-137">Knappen **Sorter etter absolutt beløp** lar deg sortere beløpene etter absoluttverdi, slik at du kan gruppere debet og kreditt som har samme beløp.</span><span class="sxs-lookup"><span data-stu-id="08c83-137">The **Sort by absolute amount** button lets you sort the amounts by absolute value, so that you can group together debits and credits that have the same amount.</span></span>

## <a name="reverse-a-settlement"></a><span data-ttu-id="08c83-138">Tilbakeføre en utligning</span><span class="sxs-lookup"><span data-stu-id="08c83-138">Reverse a settlement</span></span>

<span data-ttu-id="08c83-139">Du kan tilbakeføre en utligning som ble gjort ved en feiltakelse.</span><span class="sxs-lookup"><span data-stu-id="08c83-139">You can reverse a settlement that was made by mistake.</span></span>

1. <span data-ttu-id="08c83-140">Følg trinn 1 til 3 i delen "Utlign transaksjoner ved hjelp av siden for avanserte utligninger" for å vise transaksjonene du leter etter.</span><span class="sxs-lookup"><span data-stu-id="08c83-140">Follow steps 1 through 3 in the "Settle transactions by using advanced ledger settlements page" section to show the transactions that you're looking for.</span></span>
2. <span data-ttu-id="08c83-141">Velg **Utlignet** i **Status**-filteret.</span><span class="sxs-lookup"><span data-stu-id="08c83-141">In the **Status** filter, select **Settled**.</span></span>
3. <span data-ttu-id="08c83-142">Velg én eller flere linjer som du vurderer for tilbakeføring.</span><span class="sxs-lookup"><span data-stu-id="08c83-142">Select one or more lines that you're considering for reversal.</span></span> <span data-ttu-id="08c83-143">Verdien for feltet **Valgt beløp** øverst på siden økes eller reduseres med det totale beløpet på linjene som du har valgt.</span><span class="sxs-lookup"><span data-stu-id="08c83-143">The value of the **Selected amount** field at the top of the page increases or decreases by the total amount on the lines that you selected.</span></span>
4. <span data-ttu-id="08c83-144">Når du er ferdig med å velge transaksjoner, velger du **Merk som valgt**.</span><span class="sxs-lookup"><span data-stu-id="08c83-144">After you've finished selecting transactions, select **Mark selected**.</span></span> <span data-ttu-id="08c83-145">Det vises en hake i **Merket**-kolonnen for hver transaksjon du har valgt.</span><span class="sxs-lookup"><span data-stu-id="08c83-145">A check mark appears in the **Marked** column for each transaction that you selected.</span></span> <span data-ttu-id="08c83-146">I tillegg økes eller reduseres verdien for feltet **Merket beløp** øverst på siden med det totale beløpet på linjene du merket.</span><span class="sxs-lookup"><span data-stu-id="08c83-146">Additionally, the value of the **Marked amount** field at the top of the page increases or decreases by the total amount on the lines that you marked.</span></span>
5. <span data-ttu-id="08c83-147">Når **Merket beløp**-verdien er **0** (null), velger du **Tilbakefør merkede transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="08c83-147">When the **Marked amount** value is **0** (zero), select **Reverse marked transactions**.</span></span> <span data-ttu-id="08c83-148">Statusen for de merkede transaksjonene oppdateres til **Ikke utlignet**.</span><span class="sxs-lookup"><span data-stu-id="08c83-148">The status of the marked transactions is updated to **Not settled**.</span></span>

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a><span data-ttu-id="08c83-149">Oppdater listen over kontoer som er inkludert i listen over transaksjoner</span><span class="sxs-lookup"><span data-stu-id="08c83-149">Update the list of accounts that are included in the list of transactions</span></span>

<span data-ttu-id="08c83-150">Velg **Utligningskontoer** for å åpne en dialogboks der du kan redigere kontoene som er inkludert i listen over transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="08c83-150">Select **Ledger settlement accounts** to open a dialog box where you can edit the accounts that are included in the list of transactions.</span></span> <span data-ttu-id="08c83-151">Velg **Ny** for å legge til nye kontoer i listen.</span><span class="sxs-lookup"><span data-stu-id="08c83-151">Select **New** to add new accounts to the list.</span></span> <span data-ttu-id="08c83-152">Denne listen brukes til å filtrere listen over transaksjoner som vises på siden **Utligninger**.</span><span class="sxs-lookup"><span data-stu-id="08c83-152">This list is used to filter the list of transactions that appears on the **Ledger settlements** page.</span></span>

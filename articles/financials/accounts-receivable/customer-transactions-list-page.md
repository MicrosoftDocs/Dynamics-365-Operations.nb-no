---
title: Listeside for kundetransaksjoner
description: Dette emnet gir informasjon om listesiden for kundetransaksjoner for Microsoft Dynamics 365 for Finance and Operations.
author: mikefalkner
manager: aolson
ms.date: 08/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e828cb292ad48bb4690117b41589b25edcdf28bc
ms.contentlocale: nb-no
ms.lasthandoff: 08/31/2018

---

# <a name="customer-transaction-list-page"></a><span data-ttu-id="fc719-103">Listeside for kundetransaksjoner</span><span class="sxs-lookup"><span data-stu-id="fc719-103">Customer transaction list page</span></span>

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a><span data-ttu-id="fc719-104">Vis utligninger</span><span class="sxs-lookup"><span data-stu-id="fc719-104">View settlements</span></span>

<span data-ttu-id="fc719-105">Kategorien **Vis utligninger** i handlingsruten gir rask tilgang til utligningshistorikken og mer informasjon om hele utligningstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="fc719-105">The **View settlements** tab on the action pane provides quick access to settlement history and more information about the whole settlement transaction.</span></span> <span data-ttu-id="fc719-106">Du kan også vise flere transaksjoner som er knyttet til den valgte transaksjonen, fordi de var en del av samme utligningen, eller fordi de er betalinger som ble opprettet i samme betalingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="fc719-106">You can also show additional transactions that are related to the selected transaction, either because they were part of the same settlement or because they are payments that were created in the same payment journal.</span></span>

1. <span data-ttu-id="fc719-107">Velg **Kunder \> Kunder**.</span><span class="sxs-lookup"><span data-stu-id="fc719-107">Select **Accounts receivable \> Customers**.</span></span>
2. <span data-ttu-id="fc719-108">Velg en kunde som har transaksjoner, og velg deretter **Kunde \> Transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="fc719-108">Select a customer that has transactions, and then select **Customer \> Transactions**.</span></span>
3. <span data-ttu-id="fc719-109">Velg en transaksjonen du vil undersøke.</span><span class="sxs-lookup"><span data-stu-id="fc719-109">Select a transaction to research.</span></span>
4. <span data-ttu-id="fc719-110">Velg kategorien **Vis utligninger** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="fc719-110">Select the **View settlements** tab on the action pane.</span></span>

    <span data-ttu-id="fc719-111">I dialogboksen **Vis utligninger** vises den valgte transaksjonen og alle dokumenter som er utlignet mot den.</span><span class="sxs-lookup"><span data-stu-id="fc719-111">The **View settlements** dialog box shows the selected transaction and all documents that have been settled against it.</span></span> <span data-ttu-id="fc719-112">Denne dialogboksen ligner på utligningsloggvisningen, men den inneholder alle relaterte dokumenter.</span><span class="sxs-lookup"><span data-stu-id="fc719-112">This dialog box resembles the settlement history view, but it includes all related documents.</span></span> 

5. <span data-ttu-id="fc719-113">Du kan utføre forskjellige oppgaver i denne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="fc719-113">You can perform various tasks from this dialog box.</span></span> <span data-ttu-id="fc719-114">Velg ett eller flere bilag, og velg deretter én av følgende menyer:</span><span class="sxs-lookup"><span data-stu-id="fc719-114">Select one or more vouchers, and then select one of the following menus:</span></span>

   - <span data-ttu-id="fc719-115">**Vis regnskap** – alle bilagene som er knyttet til de valgte dokumentene, vises.</span><span class="sxs-lookup"><span data-stu-id="fc719-115">**View accounting** – All vouchers that are related to the selected documents appear.</span></span> <span data-ttu-id="fc719-116">Velg **Lukk** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="fc719-116">Select **Close** to close the dialog box.</span></span>
   - <span data-ttu-id="fc719-117">**Eksporter** – eksporter de valgte bilagene til Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="fc719-117">**Export** – Export the selected vouchers to Microsoft Excel.</span></span>
   - <span data-ttu-id="fc719-118">**Vis relaterte betalinger** – alle journaltransaksjoner for betaling som ble opprettet i betalingsjournalen som er knyttet til det valgte dokumentet, vises.</span><span class="sxs-lookup"><span data-stu-id="fc719-118">**View related payments** – All the payment journal transactions that were created in the payment journal that is related to the selected document appear.</span></span> <span data-ttu-id="fc719-119">I tillegg vises alle utligninger som er knyttet til disse betalingene.</span><span class="sxs-lookup"><span data-stu-id="fc719-119">In addition, all the settlements that are related to those payments appear.</span></span> <span data-ttu-id="fc719-120">Etiketten for denne menyen også endres til **Vis utligninger**.</span><span class="sxs-lookup"><span data-stu-id="fc719-120">The label of this menu also changes to **View settlements**.</span></span> <span data-ttu-id="fc719-121">Velg **Vis utligninger** for å vise bare transaksjonene som ble vist da du åpnet dialogboksen **Vis utligninger** for første gang.</span><span class="sxs-lookup"><span data-stu-id="fc719-121">Select **View settlements** to show only the transactions that were shown when you first opened the  **View settlements** dialog box.</span></span>
    - <span data-ttu-id="fc719-122">**Utlign transaksjoner** – denne menyen vises hvis det opprinnelige dokumentet som ble valgt, ikke ble helt utlignet.</span><span class="sxs-lookup"><span data-stu-id="fc719-122">**Settle transactions** – This menu appears if the original document that was selected wasn't fully settled.</span></span> <span data-ttu-id="fc719-123">Når du velger dette, vises dialogboksen **Utlign transaksjoner**, der du kan velge transaksjoner for utligning.</span><span class="sxs-lookup"><span data-stu-id="fc719-123">When you select it, the **Settle transactions** dialog box appears, where you can select transactions for settlement.</span></span>
    - <span data-ttu-id="fc719-124">**Angre utligninger** – denne menyen vises hvis det opprinnelige dokumentet som ble valgt, ble helt utlignet.</span><span class="sxs-lookup"><span data-stu-id="fc719-124">**Undo settlements** – This menu appears if the original document that was selected was fully settled.</span></span> <span data-ttu-id="fc719-125">Når du velger dette, vises dialogboksen **Angre utligninger**, der du kan angre utligningene som er utført for dette dokumentet.</span><span class="sxs-lookup"><span data-stu-id="fc719-125">When you select it, the **Undo settlements** dialog box appears, where you can undo the settlements that were done for that document.</span></span>
    


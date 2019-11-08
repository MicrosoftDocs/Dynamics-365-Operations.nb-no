---
title: Suspendere og gjenoppta en transaksjon på salgsstedet
description: Dette emnet forklarer hvordan brukere kan avbryte pågående transaksjoner og deretter gjenoppta dem senere eller i en annen kasse ved hjelp av Dynamics 365 Retail.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 38011f094c1434e3cafe62629902b1556df73566
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552424"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a><span data-ttu-id="8ff83-103">Suspendere og gjenoppta en transaksjon på salgsstedet</span><span class="sxs-lookup"><span data-stu-id="8ff83-103">Suspend and resume a transaction in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="8ff83-104">Salgsstedsbrukere kan avbryte pågående transaksjoner og deretter gjenoppta dem senere eller i en annen kasse.</span><span class="sxs-lookup"><span data-stu-id="8ff83-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="8ff83-105">Transaksjoner suspenderes ofte for å frigjøre en kasse raskt til en annen oppgave uten å miste arbeidet i gjeldende transaksjon.</span><span class="sxs-lookup"><span data-stu-id="8ff83-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="8ff83-106">En butikkmedarbeider begynner for eksempel å behandle en kundetransaksjon på en mobil enhet, men må fullføre den i en kasse som har kassaskuffe.</span><span class="sxs-lookup"><span data-stu-id="8ff83-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="8ff83-107">I dette tilfellet kan butikkmedarbeideren avbryte transaksjonen på den mobile enheten, og deretter gjenoppta og fortsette den i en kasse.</span><span class="sxs-lookup"><span data-stu-id="8ff83-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="8ff83-108">Konfigurere suspenderings- og gjenopptagelsesfunksjonalitet</span><span class="sxs-lookup"><span data-stu-id="8ff83-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="8ff83-109">POS-operasjoner</span><span class="sxs-lookup"><span data-stu-id="8ff83-109">POS operations</span></span>

<span data-ttu-id="8ff83-110">To [salgsstedsoperasjoner](pos-operations.md) lar salgsstedet støtte suspenderings- og gjenopptagelsesscenarioer.</span><span class="sxs-lookup"><span data-stu-id="8ff83-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="8ff83-111">Du kan tilordne disse operasjonene til [knappegrupper](pos-screen-layouts.md) på transaksjonssiden eller velkomstsiden.</span><span class="sxs-lookup"><span data-stu-id="8ff83-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="8ff83-112">503: Suspender transaksjon</span><span class="sxs-lookup"><span data-stu-id="8ff83-112">503: Suspend transaction</span></span>
- <span data-ttu-id="8ff83-113">504: Tilbakekall transaksjon</span><span class="sxs-lookup"><span data-stu-id="8ff83-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="8ff83-114">Kvitteringsmal</span><span class="sxs-lookup"><span data-stu-id="8ff83-114">Receipt template</span></span>

<span data-ttu-id="8ff83-115">Salgsstedet kan konfigureres til å generere en utskrevet seddel når en transaksjon blir suspendert.</span><span class="sxs-lookup"><span data-stu-id="8ff83-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="8ff83-116">Denne seddelen kan brukes til å identifisere og tilbakekalle transaksjonen raskt senere.</span><span class="sxs-lookup"><span data-stu-id="8ff83-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="8ff83-117">Hvis du vil la salgsstedet kunne skrive ut en seddel, må du legge til **Suspendert transaksjon**-kvitteringsformatet i butikkens kvitteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="8ff83-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="8ff83-118">Du kan utforme kvitteringsformatet slik at det inkluderer eller utelukker spesifikke detaljer om transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="8ff83-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="8ff83-119">Formatet kan for eksempel inkludere en strekkode som støtter skanning.</span><span class="sxs-lookup"><span data-stu-id="8ff83-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="8ff83-120">Kvitteringsnummerering</span><span class="sxs-lookup"><span data-stu-id="8ff83-120">Receipt numbering</span></span>

<span data-ttu-id="8ff83-121">Som for andre salgsstedstransaksjonstyper som genererer en utskrevet kvittering, kan du definere en nummerserie for suspenderte transaksjoner i **Kvitteringsnummerering**-delen i butikkens funksjonalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="8ff83-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="8ff83-122">Annuller ved avslutning av skift</span><span class="sxs-lookup"><span data-stu-id="8ff83-122">Void when closing shift</span></span>

<span data-ttu-id="8ff83-123">Du kan bruke **Annuller ved avslutning av skift**-alternativet for å kreve at brukerne enten fullfører eller annullerer alle suspenderte transaksjoner før de avslutter skiftet.</span><span class="sxs-lookup"><span data-stu-id="8ff83-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="8ff83-124">Under **Lukk skift**-operasjonen vil salgsstedet be brukerne om å enten vise eller annullere utestående suspenderte transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="8ff83-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="8ff83-125">Suspendere og gjenoppta en transaksjon</span><span class="sxs-lookup"><span data-stu-id="8ff83-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="8ff83-126">Suspendere en transaksjon</span><span class="sxs-lookup"><span data-stu-id="8ff83-126">Suspend a transaction</span></span>

<span data-ttu-id="8ff83-127">Brukere som har tilstrekkelige rettigheter og som har et skjermoppsett som inneholder **Suspender transaksjon**-operasjonen, kan avbryte en transaksjon slik at den kan tilbakekalles senere eller i en annen kasse.</span><span class="sxs-lookup"><span data-stu-id="8ff83-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="8ff83-128">Transaksjoner kan bare suspenderes hvis de **ikke** inneholder følgende typer linjer:</span><span class="sxs-lookup"><span data-stu-id="8ff83-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="8ff83-129">Aktive betalingslinjer</span><span class="sxs-lookup"><span data-stu-id="8ff83-129">Active payment lines</span></span>
- <span data-ttu-id="8ff83-130">Gavekortlinjer (enten for å utstede et gavekort eller for å legge til på gavekortsaldoen)</span><span class="sxs-lookup"><span data-stu-id="8ff83-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="8ff83-131">En suspendert transaksjon påvirker ikke salgsinformasjon eller informasjon om lagertilgjengelighet for butikken.</span><span class="sxs-lookup"><span data-stu-id="8ff83-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="8ff83-132">Gjenoppta en suspendert transaksjon</span><span class="sxs-lookup"><span data-stu-id="8ff83-132">Resume a suspended transaction</span></span>

<span data-ttu-id="8ff83-133">Suspenderte transaksjoner kan tilbakekalles og gjenopptas i den samme butikken av alle brukere som har tilstrekkelige rettigheter, og som også har et oppsett som inneholder **Tilbakekall transaksjon**-operasjonen.</span><span class="sxs-lookup"><span data-stu-id="8ff83-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="8ff83-134">Skann strekkoden på den utskrevne seddelen hvis du vil tilbakekalle en suspendert transaksjon raskt og enkelt, mens du viser listen over transaksjoner fra **Tilbakekall transaksjon**-operasjonen.</span><span class="sxs-lookup"><span data-stu-id="8ff83-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="8ff83-135">Hensyn ved frakoblet modus</span><span class="sxs-lookup"><span data-stu-id="8ff83-135">Considerations for offline mode</span></span>

- <span data-ttu-id="8ff83-136">Transaksjoner som suspenderes når salgsstedet er i tilkoblet modus, kan ikke gjenopptas i frakoblet modus fordi dataene ikke er synkronisert til den frakoblede databasen.</span><span class="sxs-lookup"><span data-stu-id="8ff83-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="8ff83-137">Hvis du suspenderer en transaksjon når salgsstedet er i frakoblet modus, kan du tilbakekalle den i frakoblet modus, forutsatt at salgsstedet ikke ble satt tilbake til tilkoblet modus når som helst etter du suspenderte transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="8ff83-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="8ff83-138">Når salgsstedet settes tilbake til tilkoblet modus, flyttes data om suspenderte transaksjoner til den tilkoblede databasen og fjernes fra den frakoblede databasen.</span><span class="sxs-lookup"><span data-stu-id="8ff83-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="8ff83-139">Derfor kan du bare gjenoppta transaksjonene i tilkoblet modus.</span><span class="sxs-lookup"><span data-stu-id="8ff83-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="8ff83-140">Hvis du setter salgsstedet tilbake til frakoblet modus, kan du ikke gjenoppta disse suspenderte transaksjonene fordi de allerede har blitt fjernet fra den frakoblede databasen.</span><span class="sxs-lookup"><span data-stu-id="8ff83-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="8ff83-141">Annullere en suspendert transaksjon</span><span class="sxs-lookup"><span data-stu-id="8ff83-141">Void a suspended transaction</span></span>

<span data-ttu-id="8ff83-142">Du kan annullere suspenderte transaksjoner enten ved å tilbakekalle transaksjonen og deretter utføre **Annuller transaksjon**-operasjonen, eller ved å velge transaksjonen i **Tilbakekall transaksjon**-listen og velge **Annuller** i programfeltet.</span><span class="sxs-lookup"><span data-stu-id="8ff83-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="8ff83-143">Eventuelt kan butikken konfigureres til å be brukerne om å annullere suspenderte transaksjoner når de avslutter skiftet.</span><span class="sxs-lookup"><span data-stu-id="8ff83-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>

---
title: Endre leveringsmodus i POS
description: Dette emnet beskriver hvordan du konfigurerer og bruker endre leveringsmodus i POS.
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: eaffe7821b60dd787a7d8b7533c1b8599033ba68
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594143"
---
# <a name="change-mode-of-delivery-in-pos"></a><span data-ttu-id="6b16e-103">Endre leveringsmodus i POS</span><span class="sxs-lookup"><span data-stu-id="6b16e-103">Change mode of delivery in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6b16e-104">Dette emnet beskriver hvordan du konfigurerer og bruker funksjonen "endre leveringsmodus" i salgsstedsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="6b16e-104">This topic describes how to set up and use the "change mode of delivery" functionality in your point of sale (POS) environment.</span></span> 

<span data-ttu-id="6b16e-105">I Dynamics 365 Commerce versjon 10.0.10 og senere er **Endre leveringsmodus** (647) tilgjengelig for å legge til i skjermoppsett for POS.</span><span class="sxs-lookup"><span data-stu-id="6b16e-105">In Dynamics 365 Commerce versions 10.0.10 and later, the **Change mode of delivery** operation (647) is available to add to your POS screen layouts.</span></span>

<span data-ttu-id="6b16e-106">Med funksjonen for endring av leveringsmåte kan du endre leveringsmåten for én eller flere forsendelseskonfigurerte salgslinjer på POS-transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="6b16e-106">The change mode of delivery feature provides you with the option to change the mode of delivery for one or more shipment-configured sales lines on the POS transaction.</span></span> <span data-ttu-id="6b16e-107">I tidligere versjoner av Commerce måtte du gå gjennom de fullstendige konfigurasjonsflytene **Send alle** eller **Valgt for forsendelse** hvis du ville endre leveringsmåten for en eksisterende linje som ble konfigurert for forsendelse.</span><span class="sxs-lookup"><span data-stu-id="6b16e-107">In previous versions of Commerce, you had to go through the full **Ship all** or **Ship selected** configuration flows if you wanted to change the mode of delivery on an existing line that was configured for shipment.</span></span> <span data-ttu-id="6b16e-108">Denne prosessen var tidkrevende, og kunne føre til utilsiktede endringer i leveringsopprinnelsen eller leveringsdatoen for linjen.</span><span class="sxs-lookup"><span data-stu-id="6b16e-108">This process was time consuming and could result in accidental changes to the delivery origin or delivery dates for the line.</span></span> <span data-ttu-id="6b16e-109">De nye funksjonene gir en alternativ metode for effektiv oppdatering av leveringsmåten på disse salgslinjene.</span><span class="sxs-lookup"><span data-stu-id="6b16e-109">The new functionality provides an alternative method for efficiently updating the mode of delivery on these sales lines.</span></span>

<span data-ttu-id="6b16e-110">Hvis du vil ha mer informasjon om hvordan du legger til en operasjon på en knapp i POS-rutenettet, kan du se [Skjermoppsett for salgssted](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span><span class="sxs-lookup"><span data-stu-id="6b16e-110">For more information about how to add an operation to a button on your POS button grid, see [Screen layouts for the point of sale](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span></span>

<span data-ttu-id="6b16e-111">Når denne funksjonen er konfigurert i POS-feltet og du velger **Endre leveringsmåte**, åpnes en listeside som gir deg muligheten til å velge linjene i transaksjonen du vil endre leveringsmåten for.</span><span class="sxs-lookup"><span data-stu-id="6b16e-111">After this feature is configured in POS, when you select **Change mode of delivery**, you will be presented with a list page that allows you to choose the lines of the transaction that you want to change the mode of delivery for.</span></span> <span data-ttu-id="6b16e-112">Du kan velge noen av eller alle linjene, eller avslutte uten å gjøre noen endringer.</span><span class="sxs-lookup"><span data-stu-id="6b16e-112">You can choose some or all of the lines, or exit without making any changes.</span></span> <span data-ttu-id="6b16e-113">Salgslinjene som tidligere ble konfigurert for forsendelse, er de eneste linjene i listen som du kan endre.</span><span class="sxs-lookup"><span data-stu-id="6b16e-113">The sales lines that were previously configured for shipment are the only lines in the list that you can change.</span></span> <span data-ttu-id="6b16e-114">Hvis du vil endre en linje som er utpekt til plukking eller utlevering, må du bruke operasjonene **Send alle** eller **Valgt for forsendelse**.</span><span class="sxs-lookup"><span data-stu-id="6b16e-114">If you want to change a line designated for pickup or carryout to ship, you must use the **Ship all** or **Ship selected** operations.</span></span> <span data-ttu-id="6b16e-115">Hvis du derimot vil endre en linje som er utpekt som en forsendelse til en plukking eller utlevering, må du bruke operasjonene **Plukk alle**, **Plukk valgte produkter**, **Utlevering av alle** eller **Utlevering av valgte**.</span><span class="sxs-lookup"><span data-stu-id="6b16e-115">Conversely, if you want to change a line designated as a shipment to a pickup or carryout, you must use the  **Pickup all**, **Pickup selected**, **Carryout all**, or **Carryout selected** operations.</span></span>

<span data-ttu-id="6b16e-116">Når du har valgt linjene du vil endre, klikker du **Endre leveringsmåte** for å bli bedt om å velge alternativer for leveringmåte.</span><span class="sxs-lookup"><span data-stu-id="6b16e-116">After you select the lines that you want to change, click **Change mode of delivery** to be prompted to select the delivery mode options.</span></span> <span data-ttu-id="6b16e-117">Hvis du valgte flere linjer som skal endres, viser salgssted bare leveringsmåter som er konfigurert som tillatt for alle de valgte varene.</span><span class="sxs-lookup"><span data-stu-id="6b16e-117">If you selected multiple lines to change, POS will only display modes of delivery that have been configured as allowable for all of the selected products.</span></span> <span data-ttu-id="6b16e-118">Leveringsmåter kan konfigureres til å støtte bestemte produkter og leveringsadresser.</span><span class="sxs-lookup"><span data-stu-id="6b16e-118">Modes of delivery can be configured to support specific products and delivery addresses.</span></span> <span data-ttu-id="6b16e-119">Hvis det finnes en leveringsmåte som er akseptabel for én produkt- og adressekombinasjon, men ikke er akseptabel for en annen valgt produkt- og adressekombinasjon, er ikke leveringsmåten tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="6b16e-119">If there is a mode of delivery that is acceptable for one product and address combination but is not acceptable for another selected product and address combination, the mode of delivery is not available.</span></span> <span data-ttu-id="6b16e-120">Det kan hende at du må velge linjer én etter én og endre leveringsmåten for hver linje separat hvis du vil velge en leveringsmåte for ett produkt som ikke støttes av et annet produkt.</span><span class="sxs-lookup"><span data-stu-id="6b16e-120">You may need to select lines one by one and change the mode of delivery for each line separately if you want to select a mode of delivery for one product that is not supported by another product.</span></span>  

<span data-ttu-id="6b16e-121">Når du har valgt den nye leveringsmåten, vises transaksjonssiden.</span><span class="sxs-lookup"><span data-stu-id="6b16e-121">After you select the new mode of delivery, the transaction page is displayed.</span></span> <span data-ttu-id="6b16e-122">Hvis du vil se gjennom de nye valgene for leveringsmodus, velger du kategorien **Levering** i transaksjonslisten.</span><span class="sxs-lookup"><span data-stu-id="6b16e-122">To review your new delivery mode selections, select the **Delivery** tab on the transaction list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6b16e-123">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6b16e-123">Additional resources</span></span>

[<span data-ttu-id="6b16e-124">Opprette telefonsenterordrer</span><span class="sxs-lookup"><span data-stu-id="6b16e-124">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="6b16e-125">Tilpasse transaksjons-e-poster etter leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="6b16e-125">Customize transactional emails by mode of delivery</span></span>](customize-email-delivery-mode.md)

---
title: Returnere serienummerkontrollerte produkter i POS
description: Dette emnet beskriver funksjonene for validering av serialiserte varer som en del av returprosessen i Microsoft Dynamics 365 Commerce POS.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7a067994828f3df577c0dc4146d26ac81990d4ac
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129823"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a><span data-ttu-id="a8b61-103">Returnere serienummerkontrollerte produkter i POS</span><span class="sxs-lookup"><span data-stu-id="a8b61-103">Return serial number–controlled products in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="a8b61-104">Dette emnet beskriver funksjonene for validering av serialiserte varer som en del av returprosessen i Microsoft Dynamics 365 Commerce POS.</span><span class="sxs-lookup"><span data-stu-id="a8b61-104">This topic describes the capabilities for validating serialized items as part of the return process in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

> [!NOTE]
> <span data-ttu-id="a8b61-105">Det er en ny funksjon kalt **Enhetlig returbehandling i POS** tilgjengelig i Commerce versjon 10.0.20 og nyere.</span><span class="sxs-lookup"><span data-stu-id="a8b61-105">In the Commerce version 10.0.20 release and later, a new feature that is named **Unified return processing experience in POS** is available.</span></span> <span data-ttu-id="a8b61-106">Hvis du vil bruke serienummervalidering under returordrebehandling i POS, må du aktivere denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="a8b61-106">To use serial number validation during return order processing in POS, you must turn on this feature.</span></span> <span data-ttu-id="a8b61-107">Hvis du vil ha informasjon om andre funksjoner denne funksjonen gir når den er aktivert, kan du se [Opprette returer i POS](POS-returns.md).</span><span class="sxs-lookup"><span data-stu-id="a8b61-107">For information about others capabilities that this feature provides when it's turned on, see [Create returns in POS)](POS-returns.md).</span></span>
>
> <span data-ttu-id="a8b61-108">Når funksjonen er aktivert, kan den ikke deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="a8b61-108">After the feature is turned on, it can't be turned off.</span></span>

## <a name="options-for-validating-serialized-returns"></a><span data-ttu-id="a8b61-109">Alternativer for validering av serialiserte returer</span><span class="sxs-lookup"><span data-stu-id="a8b61-109">Options for validating serialized returns</span></span>

<span data-ttu-id="a8b61-110">Når funksjonen **Enhetlig returbehandling i POS** er aktivert, kan organisasjoner utføre en validering av returer av serienummerkontrollerte varer via POS.</span><span class="sxs-lookup"><span data-stu-id="a8b61-110">When the **Unified return processing experience in POS** feature is turned on, organizations can perform a validation on returns of serial number–controlled items through POS.</span></span> <span data-ttu-id="a8b61-111">Denne funksjonen kan advare brukere hvis serienummeret som returneres, er forskjellig fra det opprinnelige serienummeret som ble solgt.</span><span class="sxs-lookup"><span data-stu-id="a8b61-111">This capability can warn users if the serial number that is being returned differs from the original serial number that was sold.</span></span> <span data-ttu-id="a8b61-112">Meldingen som brukere mottar i Commerce versjon 10.0.20 og nyere, er bare en advarsel.</span><span class="sxs-lookup"><span data-stu-id="a8b61-112">In the Commerce version 10.0.20 release and later, the message that users receive is only a warning message.</span></span> <span data-ttu-id="a8b61-113">Brukere kan fortsette å behandle en retur mot et serienummer som er forskjellig fra serienummeret som opprinnelig ble solgt.</span><span class="sxs-lookup"><span data-stu-id="a8b61-113">Users can continue to process a return against a serial number that differs from the serial number that was originally sold.</span></span>

<span data-ttu-id="a8b61-114">Hvis du vil konfigurere serienummervalidering for en organisasjon etter at funksjonen **Enhetlig returbehandling i POS** er aktivert, går du til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Handelsparametere** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="a8b61-114">To configure serial number validation for an organization after the **Unified return processing experience in POS** feature is turned on, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters** in Commerce headquarters.</span></span> <span data-ttu-id="a8b61-115">Sett alternativet **Aktiver validering av serienumre for returer i POS** til **Ja** i hurtigfanen **Butikklageroperasjoner** i **Lager**-fanen.</span><span class="sxs-lookup"><span data-stu-id="a8b61-115">On the **Inventory** tab, on the **Store inventory operations** FastTab, set the **Enable validation of serial numbers on POS returns** option to **Yes**.</span></span>

## <a name="process-returns-for-serialized-items-in-pos"></a><span data-ttu-id="a8b61-116">Behandle returer for serialiserte varer i POS</span><span class="sxs-lookup"><span data-stu-id="a8b61-116">Process returns for serialized items in POS</span></span>

<span data-ttu-id="a8b61-117">Hvis alternativet **Aktiver validering av serienumre for returer i POS** er satt til **Ja** når en serienummerkontrollert vare returneres via POS, kan brukeren angi serienummeret for returlinjen i detaljruten på siden **Produkter som kan returneres**.</span><span class="sxs-lookup"><span data-stu-id="a8b61-117">If the **Enable validation of serial numbers on POS returns** option has been set to **Yes**, when a serial number–controlled item is returned through POS, the user can enter the serial number for the return line in the details pane on the **Returnable products** page.</span></span> <span data-ttu-id="a8b61-118">Hvis serienummeret som angis, ikke samsvarer med det opprinnelige serienummeret som ble solgt for salgstransaksjonen, får brukeren en advarsel.</span><span class="sxs-lookup"><span data-stu-id="a8b61-118">If the serial number that is entered doesn't match the original serial number that was sold for the sales transaction, the user receives a warning message.</span></span> <span data-ttu-id="a8b61-119">Programmet forhindrer imidlertid ikke brukeren fra å fortsette å postere returen.</span><span class="sxs-lookup"><span data-stu-id="a8b61-119">However, the application doesn't prevent the user from continuing to post the return.</span></span>

> [!NOTE]
> <span data-ttu-id="a8b61-120">POS støtter for øyeblikket validering av serienumre bare på returlinjer der det opprinnelig bestilte antallet ikke er større enn én.</span><span class="sxs-lookup"><span data-stu-id="a8b61-120">Currently, POS supports validation of serial numbers only on return lines where the original ordered quantity is no more than one.</span></span> <span data-ttu-id="a8b61-121">Hvis den opprinnelige salgsordrelinjen ble opprettet i en ikke-POS-kanal, og hvis antallet som ble bestilt for den serialiserte varen på en angitt salgslinje, er større enn én, kan ikke varen returneres riktig via POS.</span><span class="sxs-lookup"><span data-stu-id="a8b61-121">If the original sales order line was created in a non-POS channel, and if the quantity that was ordered for the serialized item on a given sales line is more than one, the item can't be correctly returned through POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a8b61-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a8b61-122">Additional resources</span></span>

[<span data-ttu-id="a8b61-123">Opprette returer i POS</span><span class="sxs-lookup"><span data-stu-id="a8b61-123">Create returns in POS</span></span>](POS-returns.md)

---
title: Avbryte lagerarbeid for unntaksbehandling
description: Dette emnet beskriver Avbryt arbeid-funksjonen som gjør det mulig for lagersjefer å håndtere blokkert arbeid.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: daa8f0d19de75e6c126fe7a5fe312bca24c89bdc
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434770"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a><span data-ttu-id="36910-103">Avbryte lagerarbeid for unntaksbehandling</span><span class="sxs-lookup"><span data-stu-id="36910-103">Cancel warehouse work for exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36910-104">Funksjonen Avbryt arbeid i Microsoft Dynamics 365 Supply Chain Management lar administratorbrukeren avbryte bestemt lagerarbeid som pågår, men som er blokkert av systemet eller ikke kan fullføres på grunn av eksepsjonelle omstendigheter.</span><span class="sxs-lookup"><span data-stu-id="36910-104">The Cancel work functionality in Microsoft Dynamics 365 Supply Chain Management lets the admin user cancel specific warehouse work that is currently in progress, but that is blocked by the system or can't be completed because of exceptional circumstances.</span></span> <span data-ttu-id="36910-105">Denne funksjonaliteten er et attraktivt og sikkert alternativ til SQL-korrigerte skript som retter opp inkonsekvente data.</span><span class="sxs-lookup"><span data-stu-id="36910-105">This functionality is an attractive and secure alternative to SQL corrective scripts that fix inconsistent data.</span></span> <span data-ttu-id="36910-106">Disse skriptene er som regel anmodet fra IT-medarbeidere, men kan også brukes av brukere i firmaet som har administratorrettigheter.</span><span class="sxs-lookup"><span data-stu-id="36910-106">However, whereas these scripts are typically requested from IT professionals, the Cancel work functionality can be used by users in the company who have admin rights.</span></span>

<span data-ttu-id="36910-107">Du kan få tilgang til Avbryt arbeid-funksjonen ved å gå til **Lagerstyring** \> **Periodiske oppgaver** \> **Opprydding \> Avbryt arbeid**.</span><span class="sxs-lookup"><span data-stu-id="36910-107">You can access the Cancel work functionality at **Warehouse management** \> **Periodic tasks** \> **Clean up \> Cancel work**.</span></span> <span data-ttu-id="36910-108">I dialogboksen **Avbryt arbeid** angir du arbeids-IDen for arbeidet som skal annulleres, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="36910-108">In the **Cancel work** dialog box, specify the work ID of the work to cancel, and then select **OK**.</span></span>

## <a name="warehouse-work-that-can-be-canceled"></a><span data-ttu-id="36910-109">Lagerarbeid som kan annulleres</span><span class="sxs-lookup"><span data-stu-id="36910-109">Warehouse work that can be canceled</span></span>

<span data-ttu-id="36910-110">Under lagerplukkinger, kan en arbeider støte på situasjoner der de har registrert antall som plukket fra en lagringslokasjon til brukerlokasjonen, men de kan ikke registrere plasseringsoperasjonen.</span><span class="sxs-lookup"><span data-stu-id="36910-110">During warehouse picking operations, a worker might encounter situations where they have registered quantities as picked from a storage location to their user location, but then they can't register the put operation.</span></span> <span data-ttu-id="36910-111">Inkonsekvente lagerdata er ofte, men ikke alltid, årsaken til at arbeidet er blokkert.</span><span class="sxs-lookup"><span data-stu-id="36910-111">Inconsistent warehouse data is often, but not always, the reason why work is blocked.</span></span>

<span data-ttu-id="36910-112">I motsetning til den vanlige Avbryt-funksjonaliteten som du får tilgang til ved å bruke **Avbryt**-knappen i arbeidshodet, krever ikke funksjonen Avbryt arbeid at den siste fullførte arbeidslinjen er en arbeidslinje av typen **Plasser**.</span><span class="sxs-lookup"><span data-stu-id="36910-112">Unlike the regular Cancel functionality that can be accessed by using the **Cancel** button on the work header, the Cancel work functionality doesn't require that the last completed work line be a work line of the **put** type.</span></span> <span data-ttu-id="36910-113">Med andre ord, for å avbryte Avbryt arbeid-funksjonen, kan annulleringslogikken kjøres selv om vareantallet på en arbeidslinje er på en brukerlokasjon.</span><span class="sxs-lookup"><span data-stu-id="36910-113">In other words, for the Cancel work functionality, cancellation logic can be run even if the item quantity on a work line is in a user location.</span></span>

> [!NOTE]
> <span data-ttu-id="36910-114">For arbeid som må avbrytes av hensyn til driften, må lagerbrukere fortsette å bruke den vanlige Avbryt-funksjonaliteten på arbeidssiden.</span><span class="sxs-lookup"><span data-stu-id="36910-114">For work that must be canceled for operational reasons, warehouse users must continue to use the regular Cancel functionality on the work page.</span></span>

<span data-ttu-id="36910-115">Bare arbeid av typen **Salg**, **Utstedelse for overføring**, **Råvareplukking** eller **Etterfylling** kan annulleres ved hjelp av funksjonen Avbryt arbeid.</span><span class="sxs-lookup"><span data-stu-id="36910-115">Only work of the **Sales**, **Transfer issue**, **Raw material picking**, or **Replenishment** type can be canceled by using the Cancel work functionality.</span></span> <span data-ttu-id="36910-116">Annulleringslogikk vil ikke kjøres for plukkarbeid av fryste råvarer eller arbeid som kan avbrytes ved å bruke den vanlige Avbryt-funksjonaliteten (se den foregående merknaden).</span><span class="sxs-lookup"><span data-stu-id="36910-116">Cancellation logic won't be run for frozen raw material picking work or work that can be canceled by using the regular Cancel functionality (see the preceding note).</span></span>

<span data-ttu-id="36910-117">Hvis du vil oppheve blokkeringen av arbeidet, avbryter systemet alle gjenværende arbeidslinjer og reparerer lagerdataene som er knyttet til arbeids-IDen som brukeren har angitt.</span><span class="sxs-lookup"><span data-stu-id="36910-117">To unblock the work, the system cancels any remaining work lines and fixes the warehouse data that is associated with the work ID that the user specified.</span></span> <span data-ttu-id="36910-118">Eventuelle vanlige lagerhåndteringsoperasjoner som involverer det berørte vareantallet, kan deretter fortsette.</span><span class="sxs-lookup"><span data-stu-id="36910-118">Any regular warehouse-handling operations that involve the affected item quantity can then resume.</span></span>

<span data-ttu-id="36910-119">Hvis du vil plassere den berørte varen på en bestemt lokasjon etter at arbeidet er annullert, må brukeren bruke en lagerbevegelse eller antallsjusteringsoperasjon på en mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="36910-119">To put the affected item in a specific location after the work is canceled, the user must use an inventory movement or quantity adjustment operation on a mobile device.</span></span>

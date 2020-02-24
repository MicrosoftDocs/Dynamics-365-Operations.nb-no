---
title: Skjule leveringsmåter som ikke er transportør, fra forsendelsesalternativene på salgssted
description: Dette emnet beskriver et konfigurasjonsalternativ som kan forhindre at leveringsmåter fra ikke-transportører vises for det merkede området når forsendelsesordrer opprettes i salgsstedsprogrammet (POS).
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 75e7e8f183982f7829db78eb75b8c29c9ab95e89
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023616"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a><span data-ttu-id="87b54-103">Skjule leveringsmåter som ikke er transportør, fra forsendelsesalternativene på salgssted</span><span class="sxs-lookup"><span data-stu-id="87b54-103">Hide non-carrier delivery modes from the shipping options in POS</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="87b54-104">Dette emnet beskriver et konfigurasjonsalternativ som er tilgjengelig for salgsstedsprogrammet (POS).</span><span class="sxs-lookup"><span data-stu-id="87b54-104">This topic describes a configuration option that is available for the point of sale (POS) application.</span></span> <span data-ttu-id="87b54-105">Dette konfigurasjonsalternativet endrer virkemåten for valg av en leveringsmåte når det opprettes forsendelsesordrer på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="87b54-105">This configuration option changes the behavior for the selection of a mode of delivery when shipment orders are created in POS.</span></span>

<span data-ttu-id="87b54-106">Når brukere oppretter leveringsordrer for kunde på salgsstedet, kan de velge en leveringsmåte for forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="87b54-106">When users create customer shipment orders in POS, they can select a mode of delivery for the shipment.</span></span> <span data-ttu-id="87b54-107">Denne funksjonaliteten er tilgjengelig uansett om hele ordren sendes eller bare valgte linjer.</span><span class="sxs-lookup"><span data-stu-id="87b54-107">This functionality is available regardless of whether the whole order is being shipped or only selected lines.</span></span>

<span data-ttu-id="87b54-108">Dialogboksen der en leveringsmåte er valgt, viser som standard alle de gyldige leveringsmåtene for kombinasjonen av en kanal, en vare og en leveringsadresse.</span><span class="sxs-lookup"><span data-stu-id="87b54-108">By default, the dialog box where a mode of delivery is selected shows all the valid modes of delivery for the combination of a channel, an item, and a delivery address.</span></span> <span data-ttu-id="87b54-109">Disse leveringsmåtene er definert på **Leveringsmåter**-siden i Hovedkontor (**Salg og markedsføring \> Oppsett \> Distribusjon \> Leveringsmåter**).</span><span class="sxs-lookup"><span data-stu-id="87b54-109">These modes of delivery are defined on the **Modes of delivery** page in Headquarters (**Sales and marketing \> Setup \> Distribution \> Modes of delivery**).</span></span> <span data-ttu-id="87b54-110">"Ikke-transportør"-modi for levering, for eksempel **Utlevering** eller **Henting**, kan også vises som valg i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="87b54-110">"Non-carrier" modes of delivery, such as **Carryout** or **Pickup**, might also appear for selection in the dialog box.</span></span>

<span data-ttu-id="87b54-111">Det er imidlertid lagt til en funksjon som lar deg skjule ikke-transportør-leveringsmåter i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="87b54-111">However, a feature has been added that lets you hide non-carrier modes of delivery in the dialog box.</span></span> <span data-ttu-id="87b54-112">Hvis du vil aktivere denne funksjonen, går du til siden **Handelsparametere**, kategorien **Kundeordrer** og angir alternativet for **Vis bare transportøralternativer for forsendelsesordrer** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="87b54-112">To turn on this feature, on the **Commerce parameters** page, on the **Customer orders** tab, set the **Show only carrier mode options for ship orders** option to **Yes**.</span></span> <span data-ttu-id="87b54-113">Når du har aktivert denne funksjonen og kjørt de aktuelle distribusjonsjobbene for å synkronisere informasjonen til kanaldatabasen, vil ikke leveringsmåter for ikke-transportør vises som valg under oppretting av forsendelsesordrer på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="87b54-113">After you turn on this feature and run the appropriate distribution jobs to sync the information to the channel database, non-carrier modes of delivery won't appear for selection during the process of creating shipment orders in POS.</span></span>

---
title: Feilsøke lagerarbeid
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lagerarbeid i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a00ae517ff583e4231099d8e9f5d5b5a696cf7f7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645799"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="87b43-103">Feilsøke lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="87b43-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87b43-104">Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lagerarbeid i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="87b43-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="87b43-105">Jeg kan ikke flytte nummerskilter som har serienummervarer når det er en tom avgang, og det er tillatt med tomt mottak på sporingsdimensjonsgruppen.</span><span class="sxs-lookup"><span data-stu-id="87b43-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="87b43-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="87b43-106">Issue description</span></span>

<span data-ttu-id="87b43-107">Du kan ikke flytte et nummerskilt ved hjelp av et **Flytting**-menyelement hvis serienummeret har innstillinger for *Tom avgang tillatt* og *Tomt mottak tillatt* på sporingsdimensjonsgruppen, og hvis det er flere nummerskilter på samme sted, kan noe av disse ha serienumre og noen av dem ikke ha det.</span><span class="sxs-lookup"><span data-stu-id="87b43-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="87b43-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="87b43-108">Issue resolution</span></span>

<span data-ttu-id="87b43-109">Dette problemet vil løses ved hjelp av endringer som er distribuert i [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span><span class="sxs-lookup"><span data-stu-id="87b43-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="87b43-110">Disse endringene gjør **Serienummer**-feltet valgfritt når det er tillatt med tomt mottak og tom avgang.</span><span class="sxs-lookup"><span data-stu-id="87b43-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="87b43-111">Jeg får følgende feilmelding i lagerappen når jeg behandler flyttinger: Lagereieren %1 er ikke tillatt i denne prosessen.</span><span class="sxs-lookup"><span data-stu-id="87b43-111">I receive the following error message in the warehouse app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="87b43-112">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="87b43-112">Issue description</span></span>

<span data-ttu-id="87b43-113">**Eier**-sporingsdimensjonen mangler når lagerappen brukes til å lage bevegelser.</span><span class="sxs-lookup"><span data-stu-id="87b43-113">The **Owner** tracking dimension is missing when the warehouse app is used to make movements.</span></span> <span data-ttu-id="87b43-114">En vanlig lageroverføringsjournal fra Supply Chain Management-klienten ser ut til å fungere som tiltenkt og kan bare posteres hvis **Eier**-dimensjonen er fylt ut.</span><span class="sxs-lookup"><span data-stu-id="87b43-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="87b43-115">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="87b43-115">Issue resolution</span></span>

<span data-ttu-id="87b43-116">Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning.</span><span class="sxs-lookup"><span data-stu-id="87b43-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="87b43-117">For øyeblikket støtter lagerstyringsprosesser bare lager som eies av den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="87b43-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>

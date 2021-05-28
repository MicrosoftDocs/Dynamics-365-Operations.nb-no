---
title: Systemadministratorer kan ikke fjerne bestillinger fordi de ikke har autorisasjon til dette
description: Systemadministratorer kan ikke fjerne bestillinger fordi de ikke har autorisasjon til dette.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026796"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a><span data-ttu-id="b7c1d-103">Systemadministratorer kan ikke fjerne bestillinger fordi de ikke har autorisasjon til dette</span><span class="sxs-lookup"><span data-stu-id="b7c1d-103">System administrators can't clear order holds because they aren't authorized</span></span>

<span data-ttu-id="b7c1d-104">KB-nummer: 4614642</span><span class="sxs-lookup"><span data-stu-id="b7c1d-104">KB number: 4614642</span></span>

## <a name="symptoms"></a><span data-ttu-id="b7c1d-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="b7c1d-105">Symptoms</span></span>

<span data-ttu-id="b7c1d-106">Systemansvarlige kan ikke fjerne salgsordrer med mindre de har den bestemte rollen som er tilordnet i ordresperrekoden.</span><span class="sxs-lookup"><span data-stu-id="b7c1d-106">System administrators can't clear sales order holds unless they have the specific role that is assigned in the order hold code.</span></span>

## <a name="resolution"></a><span data-ttu-id="b7c1d-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="b7c1d-107">Resolution</span></span>

<span data-ttu-id="b7c1d-108">Tilgang til enkelte operasjoner, for eksempel å fjerne salgsordrer, drives av oppsettet av en forretningspolicy.</span><span class="sxs-lookup"><span data-stu-id="b7c1d-108">Access to some operations, such as clearing sales order holds, is driven by the setup of a business policy.</span></span> <span data-ttu-id="b7c1d-109">Systemadministratorer har vanligvis ikke tillatelse til å utføre operasjoner av denne typen.</span><span class="sxs-lookup"><span data-stu-id="b7c1d-109">System administrators aren't typically allowed to perform operations of this type.</span></span> 

<span data-ttu-id="b7c1d-110">Oftere styres tilgangen til å utføre en bestemt oppgave av forretningspolicyer, og bare bestemte personer i en organisasjon godkjennes for å utføre denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="b7c1d-110">More often, access to perform a specific task is governed by business policies, and only specific persons in an organization are approved to perform that task.</span></span> <span data-ttu-id="b7c1d-111">Eksempler inkluderer godkjenninger som er resultatet av arbeidsflytgodkjenning og bestemte oppgaver som er resultatet av en arbeidsflytkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="b7c1d-111">Examples include approvals that are the result of workflow approvals and specific tasks that are the result of a workflow configuration.</span></span>

<span data-ttu-id="b7c1d-112">Selv om ingen arbeidsflyt er knyttet til ordresperrer, er prinsippet likt.</span><span class="sxs-lookup"><span data-stu-id="b7c1d-112">Although no workflow is associated with order holds, the principle is similar.</span></span> <span data-ttu-id="b7c1d-113">En relevant rolle angir den bestemte gruppen av personer i en organisasjon som har rettighet til å fjerne ordresperringer.</span><span class="sxs-lookup"><span data-stu-id="b7c1d-113">A relevant role designates the specific group of people in an organization who have the right to clear order holds.</span></span> <span data-ttu-id="b7c1d-114">Denne rettigheten bør ikke nødvendigvis gis til alle administratorer, fordi denne tilnærmingen bryter den definerte forretningspolicyen.</span><span class="sxs-lookup"><span data-stu-id="b7c1d-114">This right should not necessarily be granted to all administrators, because that approach violates the defined business policy.</span></span>

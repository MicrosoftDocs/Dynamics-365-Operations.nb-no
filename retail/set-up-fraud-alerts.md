---
title: Definere svindelvarsler
description: "Dette emnet forklarer hvordan du definerer regler for å varsle kundeservicerepresentanter om potensiell falsk informasjon når ordrer behandles. Du kan definere spesifikke sperrekoder som skal brukes automatisk eller manuelt til å sette mistenkelige ordrer på vent."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: nb-no
ms.lasthandoff: 06/29/2017



---

# <a name="set-up-fraud-alerts"></a><span data-ttu-id="07a0f-104">Definere svindelvarsler</span><span class="sxs-lookup"><span data-stu-id="07a0f-104">Set up fraud alerts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="07a0f-105">Dette emnet forklarer hvordan du definerer regler for å varsle kundeservicerepresentanter om potensiell falsk informasjon når ordrer behandles.</span><span class="sxs-lookup"><span data-stu-id="07a0f-105">This topic explains how to set up rules to alert customer service representatives of potentially fraudulent information when orders are processed.</span></span> <span data-ttu-id="07a0f-106">Du kan definere spesifikke sperrekoder som skal brukes automatisk eller manuelt til å sette mistenkelige ordrer på vent.</span><span class="sxs-lookup"><span data-stu-id="07a0f-106">You can define specific codes to use to automatically or manually put suspicious orders on hold.</span></span> 

<span data-ttu-id="07a0f-107">Før du definerer og bruker svindelkontrollregler, må du aktivere svindelkontroll og definere de grunnleggende verdiene for svindelkontroll i telefonsenterparameterne.</span><span class="sxs-lookup"><span data-stu-id="07a0f-107">Before you set up and use fraud checking rules, you must enable fraud checking and define the basic fraud checking values in the call center parameters.</span></span> <span data-ttu-id="07a0f-108">Det finnes to typer svindelregler:</span><span class="sxs-lookup"><span data-stu-id="07a0f-108">There are two types of fraud rules:</span></span>

-   <span data-ttu-id="07a0f-109">**Statiske regler** bruker en bestemt verdi, for eksempel et telefonnummer som har blitt svartelistet.</span><span class="sxs-lookup"><span data-stu-id="07a0f-109">**Static rules** use a specific value, such as a phone number that has been blacklisted.</span></span>
-   <span data-ttu-id="07a0f-110">**Dynamiske regler** kan bestå av variabler og betingelser.</span><span class="sxs-lookup"><span data-stu-id="07a0f-110">**Dynamic rules** can be composed from variables and conditions.</span></span>

<span data-ttu-id="07a0f-111">Før du oppretter en dynamisk regel, må du opprette variablene og betingelsene som definerer hvem regelen gjelder for, og når regelen skal brukes.</span><span class="sxs-lookup"><span data-stu-id="07a0f-111">Before you create a dynamic rule, you must create the variables and conditions that define who the rule applies to and when the rule should be applied.</span></span> <span data-ttu-id="07a0f-112">La oss si at du vil opprette en regel som krever at alle salgsordrer som kunde 1202 legger inn som er verdt 1 000,00 eller mer, må settes på vent til kundebetalingen kan bekreftes.</span><span class="sxs-lookup"><span data-stu-id="07a0f-112">For example, you want to create a rule to require that any sales order that customer 1202 places that is worth 1,000.00 or more be put on hold until the customer payment can be verified.</span></span> <span data-ttu-id="07a0f-113">I dette tilfellet er variablene kunde 1202 og en ordretotal på 1 000,00.</span><span class="sxs-lookup"><span data-stu-id="07a0f-113">In this case, the variables are customer 1202 and an order total of 1,000.00.</span></span> <span data-ttu-id="07a0f-114">Betingelsen angir at når kunde 1202 plasserer en ordre, og totalbeløpet for ordren er lik eller mer enn 1 000,00, må salgsordren settes på vent til kundebetalingen kan bekreftes.</span><span class="sxs-lookup"><span data-stu-id="07a0f-114">The condition specifies that if customer 1202 places an order, and the total amount of the order is equal to or more than 1,000.00, the sales order must be put on hold until the customer payment can be verified.</span></span>





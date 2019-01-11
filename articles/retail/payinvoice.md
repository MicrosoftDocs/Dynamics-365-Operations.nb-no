---
title: Definere scenarier for betaling av faktura
description: "Dette emnet beskriver hvordan du konfigurerer Dynamics 365 for Retail til å støtte ulike scenarier for fakturabetalinger."
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: b7132dc9b3c78fa04fcfc38ea72b5678ad08deb2
ms.contentlocale: nb-no
ms.lasthandoff: 01/04/2019

---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="4a326-103">Definere scenarier for betaling av faktura</span><span class="sxs-lookup"><span data-stu-id="4a326-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4a326-104">Funksjonen Betal faktura i Dynamics 365 for Retail er utvidet for å støtte:</span><span class="sxs-lookup"><span data-stu-id="4a326-104">The Pay invoice functionality in Dynamics 365 for Retail has been expanded to support:</span></span>

- <span data-ttu-id="4a326-105">Betaling av flere salgsordrefakturaer i én salgsstedstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="4a326-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="4a326-106">Betaling for ulike typer kundefakturaer, inkludert fritekstfakturaer, prosjektbaserte fakturaer og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="4a326-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="4a326-107">Hvis du vil aktivere disse scenariene, må funksjonsprofilen for butikker konfigureres som beskrevet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="4a326-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="4a326-108">Gå til **Detaljhandel \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonsprofiler** og velg en profil som er knyttet til butikkene du vil gjøre endringene for.</span><span class="sxs-lookup"><span data-stu-id="4a326-108">Go to **Retail \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="4a326-109">Konfigurer følgende parametere etter behov, i kategorien **Funksjoner**.</span><span class="sxs-lookup"><span data-stu-id="4a326-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="4a326-110">**Salgsordrefaktura** – Velg **Ja** slik at brukere kan betale én eller flere salgsordrebaserte fakturaer i én salgsstedstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="4a326-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="4a326-111">**Fritekstfaktura** – Velg **Ja** slik at brukere kan betale én eller flere fritekstbaserte fakturaer i én salgsstedstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="4a326-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="4a326-112">**Prosjektfaktura** – Velg **Ja** slik at brukere kan betale én eller flere prosjektbaserte fakturaer i én salgsstedstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="4a326-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="4a326-113">**Salgsordre – kreditnota** – Velg **Ja** slik at brukere kan utligne flere salgsordrebaserte kreditnotaer mot åpne fakturaer, eller betale pengene tilbake til kunden for en åpen kreditnota.</span><span class="sxs-lookup"><span data-stu-id="4a326-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="4a326-114">Betaling eller utligning delvise beløper støttes ikke ennå.</span><span class="sxs-lookup"><span data-stu-id="4a326-114">Payment or settlement of partial amounts is not yet supported.</span></span>


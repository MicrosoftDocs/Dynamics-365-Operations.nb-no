---
title: Definere scenarier for betaling av faktura
description: Dette emnet beskriver hvordan du konfigurerer Dynamics 365 Commerce til å støtte ulike scenarier for fakturabetalinger.
author: josaw1
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 08d3cf48c0bea6f0e13dda49e53b314a6037860d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804559"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="1904e-103">Definere scenarier for betaling av faktura</span><span class="sxs-lookup"><span data-stu-id="1904e-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1904e-104">Funksjonen Betal faktura i Dynamics 365 Commerce er utvidet for å støtte:</span><span class="sxs-lookup"><span data-stu-id="1904e-104">The Pay invoice functionality in Dynamics 365 Commerce has been expanded to support:</span></span>

- <span data-ttu-id="1904e-105">Betaling av flere salgsordrefakturaer i én salgsstedstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="1904e-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="1904e-106">Betaling for ulike typer kundefakturaer, inkludert fritekstfakturaer, prosjektbaserte fakturaer og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="1904e-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="1904e-107">Hvis du vil aktivere disse scenariene, må funksjonsprofilen for butikker konfigureres som beskrevet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="1904e-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="1904e-108">Gå til **Detaljhandel og handel \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonsprofiler** og velg en profil som er knyttet til butikkene du vil gjøre endringene for.</span><span class="sxs-lookup"><span data-stu-id="1904e-108">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="1904e-109">Konfigurer følgende parametere etter behov, i fanen **Funksjoner**.</span><span class="sxs-lookup"><span data-stu-id="1904e-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="1904e-110">**Salgsordrefaktura** – Velg **Ja** slik at brukere kan betale én eller flere salgsordrebaserte fakturaer i én salgsstedstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="1904e-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="1904e-111">**Fritekstfaktura** – Velg **Ja** slik at brukere kan betale én eller flere fritekstbaserte fakturaer i én salgsstedstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="1904e-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="1904e-112">**Prosjektfaktura** – Velg **Ja** slik at brukere kan betale én eller flere prosjektbaserte fakturaer i én salgsstedstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="1904e-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="1904e-113">**Salgsordre – kreditnota** – Velg **Ja** slik at brukere kan utligne flere salgsordrebaserte kreditnotaer mot åpne fakturaer, eller betale pengene tilbake til kunden for en åpen kreditnota.</span><span class="sxs-lookup"><span data-stu-id="1904e-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="1904e-114">Betaling eller utligning delvise beløper støttes ikke ennå.</span><span class="sxs-lookup"><span data-stu-id="1904e-114">Payment or settlement of partial amounts is not yet supported.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
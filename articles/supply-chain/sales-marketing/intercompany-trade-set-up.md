---
title: Definere konsernintern handel
description: Denne artikkelen forklarer hvordan du definerer konsernintern handel
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8d956c60db9f3acf2f1759dc3e1922da40d8a514
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905638"
---
# <a name="set-up-intercompany-trade"></a>Definere konsernintern handel

[!include [banner](../../includes/banner.md)]

Før du kan aktivere Microsoft Dynamics 365 Supply Chain Management for konsernintern handel, må du sette opp kunder og leverandører for konsernintern handel. Du må også definere Leverandører, Kunder, Innkjøp og leverandører og Salg og markedsføring.

## <a name="before-you-set-up-intercompany-trade"></a>Før du setter opp konsernintern handel

Før du setter opp konsernintern handel, må du definere hvilke kunder som er konserninterne kunder og hvilke leverandører som er konserninterne leverandører. For hver juridiske enhet i Microsoft Dynamics 365 Supply Chain Management må du ta stilling til hvilken policy som skal brukes i konsernintern handel med en bestemt konsernintern kunde eller leverandør.

Vi anbefaler særlig at du og organisasjonen gjør deg kjent med de konserninterne parameterne.

- Drøft oppsettets implikasjoner med lederne som er ansvarlige for konsernintern handel i hver juridiske enhet.
- Definer riktige verdier for hver juridiske enhet.

## <a name="set-up-trading-relations"></a>Definere handelsforbindelser

Følg denne fremgangsmåten for å definere leverandører, kunder og varer for konsernintern handel.

1. Gå til **Kunder \> Kunder \> Alle kunder**.
1. Velg en kundekonto.
1. Velg **Konsernintern** i fanen **Generelt** i handlingsruten.
1. Angi konserninterne oppsettparametere for kundekontoen. Disse parameterne omfatter den juridiske enheten som inneholder den tilsvarende leverandøren og leverandørkontoen. Parameterne omfatter også bestillingspolicyer, salgsordrepolicyer, verditilordning og policyer for salgsavtale og kjøpsavtaler. Du angir også om stamdataverdier skal brukes fra kundekontoen eller fra leverandørkontoen i den andre juridiske enheten.
1. Gjenta trinn 1 til og med 4 for de gjenværende konserninterne kundene i den juridiske enheten.
1. Gå til **Leverandører \> Leverandører \> Alle leverandører**.
1. Velg en leverandørkonto.
1. Velg **Konsernintern** i fanen **Generelt** i handlingsruten.
1. Angi konserninterne oppsettparametere for leverandørkontoen. Disse parameterne omfatter den juridiske enheten som inneholder den tilsvarende kunden og kundekontoen. Parameterne omfatter også salgsordrepolicyer, bestillingspolicyer, verditilordning og policyer for salgsavtale og kjøpsavtaler. Du angir også om stamdataverdier skal brukes fra leverandørkontoen eller fra kundekontoen i den andre juridiske enheten.
1. Gjenta trinn 6 til og med 9 for de gjenværende konserninterne leverandørene i den juridiske enheten.

## <a name="set-up-products"></a>Definere produkter

Følg denne fremgangsmåten for å definere leverandører, kunder og varer for konsernintern handel.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Alle produkter og produktstandarder**.
1. Definer produktene som er frigitt til de juridiske enhetene der du vil utføre konsernintern handel.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Definer kanalspesifikke rabatter
description: Forhandlere angir ofte ulike rabatter i forskjellige kanaler. Dette emnet beskriver begrepene du trenger å kjenne til for å opprette en rabatt for en bestemt kanal.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 539a6f2df46450c5e0fd18ba69501432d6f3fbdd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414654"
---
# <a name="define-channel-specific-discounts"></a>Definere kanalspesifikke rabatter

[!include [banner](includes/banner.md)]

Dette emnet beskriver begrepene du trenger å kjenne til for å opprette en rabatt for en bestemt kanal.

## <a name="channel-specific-discounts"></a>Kanalspesifikke rabatter

Forhandlere tilbyr ofte ulike rabatter i forskjellige kanaler. Det kan gjøres for å målrette lokale markedsforhold eller for å forholde seg til konkurrerende forhandlere.

Handel bruker prisgrupper til å definere kanalspesifikke rabatter. Prisgrupper kan tilordnes til én eller flere av følgende enheter: kanaler, kataloger, tilknytninger og fordelsprogrammer. Denne artikkelen inneholder informasjon om kanaler, men de samme konseptene gjelder for katalograbatter, tilknytningsrabatter og lojalitetsrabatter.

## <a name="price-groups"></a>Prisgrupper

[![Prisgrupper](./media/price-groups-1024x608.png)](./media/price-groups.png)

Diagrammet over illustrerer relasjonen mellom enheter som kan være på en transaksjon (kanal, katalog, tilknytning, kunde, fordelskort) og de ulike typene rabatter som kan konfigureres. Alle transaksjoner skjer i en kanal, slik at kanalen er garantert å finnes på en transaksjon. De gjenværende enhetene er valgfrie. Det er en kobling til en relatert prisgruppe på hver hoveddataside der du kan vise og legge til prisgrupper etter behov. En prisgruppe brukes til å relatere fire forskjellige typer enheter til rabatter, prisjusteringer og forretningsavtaler. Vi anbefaler at du planlegger en strategi for hvordan du navngir prisgrupper for å holde orden på dem. Ett alternativ er å bruke en bokstav eller tallprefiks eller suffiks til å skille mellom de ulike typene. For eksempel 1-xxxxx for kanalprisgrupper og 2-xxxxx i katalogprisgrupper. Det er fire forespørselssider som fokuserer på hver handelsenhet som kan ha rabatter som er knyttet til dem.

- **Prisgrupper for kanal** – Denne siden viser en liste over kanaler og rabatter som er koblet sammen for hver prisgruppe.
- **Katalogprisgrupper** – Denne siden viser en liste over kataloger og rabatter som er koblet sammen for hver prisgruppe.
- **Prisgrupper for fordelsprogram** – Denne siden viser en liste over fordelsprogrammer og rabatter som er koblet sammen for hver prisgruppe.
- **Prisgrupper for tilknytninger** – Denne siden viser en liste over tilknytninger og rabatter som er koblet sammen for hver prisgruppe.

## <a name="example-channel-discount-set-up"></a>Eksempel på kanalrabattoppsett

Følgende eksempel viser oppgavene med å konfigurere en kanalrabatt.

1. Du har for eksempel en kanal som kalles **Houston**, og du skal opprette en ny rabatt kalt **Tilbake til skolen**.
2. Fordi pris- og rabattstrategien inneholder muligheten for kanalrabatter, oppretter du alltid en kanalspesifikk prisgruppe når du oppretter en kanal.
3. Du har prisgruppen **Houston-PG**, og den er tilordnet til **Houston**-kanalen.
4. Når du har opprettet den nye **Tilbake til skolen**-rabatten, må du klikke **Prisgrupper** øverst på **Rabatt**-siden. **Rabattprisgrupper**-siden åpnes. Deretter klikker du **Ny** og velger **Houston-PG**-prisgruppen.
5. Nå kan du aktivere rabatten og overføre den til kanalen.

## <a name="additional-resources"></a>Tilleggsressurser

[Prisjusteringer og rabatter](price-adjustments-discounts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
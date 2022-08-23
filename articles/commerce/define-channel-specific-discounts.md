---
title: Definer kanalspesifikke rabatter
description: Forhandlere angir ofte ulike rabatter i forskjellige kanaler. Denne artikkelen beskriver begrepene du trenger å kjenne til for å opprette en rabatt for en bestemt kanal.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.industry: Retail
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
ms.openlocfilehash: f426503a6897a73010b77082f4277b65545bfcc3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273561"
---
# <a name="define-channel-specific-discounts"></a>Definere kanalspesifikke rabatter

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver begrepene du trenger å kjenne til for å opprette en rabatt for en bestemt kanal.

## <a name="channel-specific-discounts"></a>Kanalspesifikke rabatter

Forhandlere tilbyr ofte ulike rabatter i forskjellige kanaler. Det kan gjøres for å målrette lokale markedsforhold eller for å forholde seg til konkurrerende forhandlere.

Handel bruker prisgrupper til å definere kanalspesifikke rabatter. Prisgrupper kan tilordnes til én eller flere av følgende enheter: kanaler, kataloger, tilknytninger og fordelsprogrammer. Denne artikkelen inneholder informasjon om kanaler, men de samme konseptene gjelder for katalograbatter, tilknytningsrabatter og lojalitetsrabatter.

## <a name="price-groups"></a>Prisgrupper

[![Prisgrupper.](./media/price-groups-1024x608.png)](./media/price-groups.png)

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

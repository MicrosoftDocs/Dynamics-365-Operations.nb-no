---
title: Definer kanalspesifikke rabatter
description: "Forhandlere angir ofte ulike rabatter i forskjellige kanaler. Dette emnet beskriver begrepene du trenger å kjenne til for å opprette en rabatt for en bestemt kanal."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: b2f59db59ea49925c3bb5e1d75beee95191220d0
ms.lasthandoff: 03/31/2017


---

# <a name="define-channel-specific-discounts"></a>Definer kanalspesifikke rabatter

Forhandlere angir ofte ulike rabatter i forskjellige kanaler. Dette emnet beskriver begrepene du trenger å kjenne til for å opprette en rabatt for en bestemt kanal. 

<a name="channel-specific-discounts"></a>Kanalspesifikke rabatter
--------------------------

Forhandlere gir ofte ulike rabatter i forskjellige kanaler. Dette er kan gjøres til adresse lokal markedsforhold eller å forholde seg til konkurrerende forhandlere.

Handel og handel i Microsoft Dynamics 365 for operasjoner bruker prisgrupper for å definere kanal-spesifikke rabatter. Prisgrupper kan tilordnes til én eller flere av følgende enheter: kanaler, kataloger, tilknytninger og fordelsprogrammer. Denne artikkelen inneholder informasjon om kanaler, men de samme konseptene gjelder for katalograbatter, tilknytningsrabatter og lojalitetsrabatter.

## <a name="price-groups"></a>Prisgrupper
\[overskrifts-IDen = "vedlegg\_256084" align = "alignnone" width = "640"\][![pris grupper](./media/price-groups-1024x608.png)](./media/price-groups.png) pris gruppen koblinger for detaljhandel\[/bildetekst\]

Diagrammet ovenfor illustrerer forholdet mellom enheter som kan være på en transaksjon (kanal, katalog, ansettelsesforhold, kunde-, lojalitet kort) og ulike rabattyper som kan konfigureres. Alle transaksjoner skjer i en kanal, slik at kanalen er garantert å finnes på en transaksjon. De gjenværende enhetene er valgfrie. Det er en kobling til en relatert prisgruppe på hver hoveddataside der du kan vise og legge til prisgrupper etter behov. En prisgruppe brukes til å relatere fire forskjellige typer enheter til rabatter, prisjusteringer og forretningsavtaler. Vi anbefaler at du planlegge en strategi for hvordan du får navnet ditt prisgrupper for å holde orden på dem. Ett alternativ er å bruke en bokstav eller tall prefiks eller suffiks til å skille mellom de forskjellige typene. For eksempel 1-xxxxx for prisgrupper for kanalen og 2-xxxxx i katalogen prisgrupper. Det er fire forespørselssider som fokuserer på hver detaljhandelsenhet som kan ha rabatter som er knyttet til dem.

-   **Prisgrupper for detaljhandelskanal **– Denne siden viser en liste over kanaler og rabatter som er koblet sammen for hver prisgruppe.
-   **Katalogprisgrupper **– Denne siden viser en liste over kanaler og rabatter som er koblet sammen for hver prisgruppe.
-   **Prisgrupper for fordelsprogram **– Denne siden viser en liste over fordelsprogrammer og rabatter som er koblet sammen for hver prisgruppe.
-   **Prisgrupper for tilknytninger **– Denne siden viser en liste over tilknytninger og rabatter som er koblet sammen for hver prisgruppe.

## <a name="example-channel-discount-set-up"></a>Eksempel på kanalrabattoppsett
Følgende eksempel viser oppgavene med å konfigurere en kanalrabatt.

1.  Du har for eksempel en kanal som kalles **Houston**, og du skal opprette en ny rabatt kalt **Tilbake til skolen**.
2.  Fordi pris- og rabattstrategien inneholder muligheten for kanalrabatter, oppretter du alltid en kanalspesifikk prisgruppe når du oppretter en kanal.
3.  Du har prisgruppen **Houston-PG**, og den er tilordnet til **Houston**-kanalen.
4.  Når du har opprettet den nye **Tilbake til skolen**-rabatten, må du klikke **Prisgrupper** øverst på **Rabatt**-siden. **Rabattprisgrupper**-siden åpnes. Deretter klikker du **Ny** og velger **Houston-PG**-prisgruppen.
5.  Nå kan du aktivere rabatten og overføre den til kanalen.

 

<a name="see-also"></a>Se også
--------

[Price adjustments and discounts](price-adjustments-discounts.md)



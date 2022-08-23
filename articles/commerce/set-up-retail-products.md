---
title: Definere detaljhandelsprodukter
description: Denne artikkelen beskriver hvordan definerer produkter i Dynamics 365 Commerce.
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
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.industry: Retail
ms.search.form: RetailProductAndCategoryWorkspace, EcoResProductDetails
ms.openlocfilehash: 22a3ecb235b21e239b23e5450ca4a2f12f9a41ac
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276081"
---
# <a name="set-up-retail-products"></a>Definere detaljhandelsprodukter

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan definerer produkter i Dynamics 365 Commerce.

Før du kan tilby produkter for videresalg i handelskanalene, må du opprette og konfigurere produktene. Commerce oppretter produkter i hele organisasjonen i produktstandarden. Du kan opprette produktene, definere produktegenskaper og -attributter og tilordne produktene til handelskategorihierarkier. For å gjøre produktene tilgjengelige for kanalene og legge dem til i et aktivt utvalg må du deretter frigi produktene til de juridiske enhetene der de er tilgjengelige. Hvis du vil definere produktene som selges ved hjelp av kanaler, kan du utføre følgende oppgaver.

1. **Definer et produkthierarki.** Ved hjelp av kategorihierarkifunksjonene i Commerce kan du definere detaljhandelskategorihierarkier for å gruppere og kategorisere produktene som distribueres til kanaler. Brukerdefinerte attributter og systemattributter kan defineres på kategorinivå. Deretter arver alle produkter som er tilordnet til kategorien, disse attributtene. Du kan definere flere kategorihierarkier, og hvert produkt kan tilordnes flere hierarkier. Men i et enkelt hierarki kan hvert produkt tilordnes bare én kategori.
2. **Legg til produkter og produktvarianter i produktstandarden.** Produkter som er lagt til i produktstandarden, representerer en global liste over produkter. Du kan legge til produkter manuelt, ett om gangen, eller du kan importere produktdata fra leverandører.
3. **Frigi produktene til juridiske enheter.** Det er bare produkter som er frigitt til juridiske enheter som kan gjøres tilgjengelig for kanalene. Når du først definerer et produkt, kan du definere det på et nivå for hele organisasjonen. Du kan deretter velge én eller flere juridiske enheter som produktet skal frigis til. Produktet blir da tilgjengelig for flere kanaler på tvers av organisasjonen. Du kan bruke denne funksjonen til å opprette et produkt én gang, legge til og oppdatere produktattributter og -egenskaper på ett sted, og deretter distribuere produktet på tvers av organisasjonen, til kanalene hvor det er tilgjengelig.
4. **Legg til produkter i sortimenter.** Et sortiment representerer en samling produkter som du tilbyr i kanalene dine. Du kan definere ett eller flere sortimenter, og hvert produkt kan tilordnes til ett eller flere sortimenter. Du kan tilordne produkter til kanaler ved å tilordne sortimentene til disse kanalene. Når du oppretter et sortiment, kan du legge til produkter som ennå ikke er frigitt til en juridisk enhet. Du må imidlertid frigi produktene til en juridisk enhet før de kan gjøres tilgjengelige for kanalene.
5. **Legge til produkter i navigasjonshierarkier.** Før du kan bla gjennom produkter elektronisk eller på et salgssted, må de kategoriseres i et navigasjonshierarki for handel.
6. **Legg til produkter i kataloger.** Selv om dette trinnet er valgfritt for salgssted, krever Internett-butikker at produkter skal inkluderes i minst én katalog.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

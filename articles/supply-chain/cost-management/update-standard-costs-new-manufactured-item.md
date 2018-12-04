---
title: Oppdatere standardkostnader for en ny produsert vare
description: "Denne artikkelen gir råd for å oppdatere standardkostnader for en ny produsert vare."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79693
ms.assetid: ba64b70f-3f4c-4373-9a7d-8fd07c45a8cf
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1cfb04a98f7d01f7766bea97157ca3c44c51e326
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-for-a-new-manufactured-item"></a>Oppdatere standardkostnader for en ny produsert vare

[!include [banner](../includes/banner.md)]

Denne artikkelen gir råd for å oppdatere standardkostnader for en ny produsert vare. 

Retningslinjene antar at du bruker en toversjons tilnærming til å oppdatere standardkostnader. I denne fremgangsmåten, inneholder én etterkalkuleringsversjon standardkostnader som opprinnelig ble definert for den frosne perioden, og den andre etterkalkuleringsversjonen inneholder de inkrementelle oppdateringene som gjelder for de nye produserte varene. De inkrementelle oppdateringene blir lagt inn som kostnadsposter i den andre etterkalkuleringsversjonen, og til slutt aktivert. Toversjonsmåten krever at du definerer enda en etterkalkuleringsversjon. Her følger retningslinjene for å definere denne etterkalkuleringsversjonen:

-   Tilordne en etterkalkuleringstype for **standardkostnad**.
-   Tilordne en signifikant identifikator som identifiserer innholdet i etterkalkuleringsversjonen, for eksempel **2016-OPPDATERINGER**.
-   I feltgruppen **Tillat pristyper** må du kontrollere at **Kostpris** er satt til **Ja**.
-   Tillat at kostnadsposter kan angis for alle områder (det vil si, la **Område**-feltet stå tomt). Hvis du angir et område, kan kostnadsposter angis bare for dette området.
-   Bruk tilbakefallsprinsippet **Aktiv**.

Hvis du vi legge til nye produksjonsvarer i hele den frosne perioden, kan du gjøre følgende.

1.  Bruk **Etterkalkuleringsversjon**-oppsettsiden for å aktivere kostnadsposter som skal angis i den andre etterkalkuleringsversjonen, som inneholder de inkrementelle oppdateringene. Hindre aktiveringen av uavsluttede kostpriser, der aktiveringen vil bli tillatt etter at de uavsluttede kostprisene er fullført og korrekt definert. Angi en tom fra-dato som en policy i kostversjonen, og deretter angir du den fra-datoen når du legger inn hver kostprispost. Fra-datoen skal representere en dato før de nye varene blir innkjøpt eller produsert.
2.  Bruk **Varepris**-siden til å angi kostprisposter for nye innkjøpte varer. For hver kostnadspost angir du kostversjonen som inneholder inkrementelle oppdateringer, og bruker en fra-dato som kommer før den forventede produksjonsdatoen for nye produserte varer.
3.  Beregn kostprisen på nye produserte varer ved hjelp av **Beregning**-siden. Åpne **BNeregning**-siden fra siden **Vedlikehold av etterkalkuleringsversjon**, og velg deretter etterkalkuerlingsversjonen som inneholder de inkrementelle oppdateringene. Bruk utvalgskriteriene til å angi den nye produserte varen og eventuelle produserte komponenter. I en produktstrutkru på flere nivåer kan det også være nødvendig å identifisere alle overordnede varer som inneholder de nye produserte varene som en komponent. Angi en fra-dato for stykklisteberegningen som samsvarer med starten på produksjonen for de nye produserte varene. Fra-datoen må være innenfor de effektive datoene for varens stykklisteversjon og ruteversjon. **Obs!** En manglende kostnadspost kan angi en ny produsert vare. Stykklisteberegninger kan være begrenset til varer med manglende kostpriser.
4.  Kontroller at de beregnede kostprisene for nye produserte varer er fullført og nøyaktig. Bruk **Fullført**-siden til å se gjennom de beregnede kostnadene for hver varekostnadspostene, og eventuelle advarselsmeldinger i infologgen. Du kan også bruke **Beregning**-siden til å se gjennom en liste med de beregnede kostnadene.
5.  Bruk siden **Oppsett av etterkalkuleringsversjon** for å endre blokkeringsflagget for å tillate aktivering av ventende kostnadsposter i den andre etterkalkuleringsversjonen.
6.  Bruk siden **Aktiver priser** (som du åpner fra siden **Vedlikehold av etterkalkuleringsversjon**) for å aktivere alle ventende kostnadsposter i den andre etterkalkuleringsversjonen. Du kan også aktivere de ventende kostnadspostene for enkelte varer ved å klikke knappen **Aktiver** på **Varepris**-siden.
7.  For å unngå ytterligere datavedlikehold kan du bruke siden **Oppsett av etterkalkuleringsversjon** til å endre blokkeringsflaggene som er vedlagt den andre etterkalkuleringsversjonen. Blokkeringspolicyene forhindrer innlegging av nye uavsluttede kostnader og aktivering av uavsluttede kostpriser.






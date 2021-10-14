---
title: Endre konserninterne ordrer
description: Dette emnet forklarer hvordan du endringer konserninterne ordrer
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 1129794bf0ac6513770f8b2a0eeb7fb6154d7942
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548457"
---
# <a name="change-intercompany-orders"></a>Endre konserninterne ordrer

[!include [banner](../../includes/banner.md)]

Hvis du endrer en konsernintern salgsordre eller bestilling, vil den tilsvarende salgsordren eller bestillingen i det tilsvarende selskapet også gjenspeile endringen.

## <a name="adding-new-lines"></a>Legge til nye linjer

Du kan legge til nye linjer til en konsernintern salgsordre og bestilling hvis den opprinnelige salgsordren er en del av den konserninterne ordrekjeden. Du kan også legge til nye linjer hvis den opprinnelige salgsordren ikke er en direkte levering. Hvis den opprinnelige salgsordren er en direkte levering, kan du bare legge til nye ordrelinjer til den konserninterne salgsordren og bestillingen hvis feltet **Tillat indirekte oppretting** er valgt i hurtigfanen **Konserninterne innstillinger** i den opprinnelige salgsordren.

## <a name="changing-prices-and-discounts"></a>Endre priser og rabatter

Du kan endre prisene og rabattene hvis det er merket av for **Tillat prisredigering** og **Tillat rabattredigering** på **Konsernintern**-siden.

Hvis du endrer enhetsprisen til en av de eksisterende linjene på den konserninterne salgsordrelinjen, blir også enhetsprisen på den konserninterne bestillingen endret.

Hvis du endrer noen av rabattfeltene på den konserninterne salgsordelinjen, oppdateres de relevante rabattfeltene på den konserninterne bestillingen.

## <a name="changing-and-adding-new-charges"></a>Endre og legge til nye tillegg

Du kan endre tilleggene hvis det er merket av for **Tillat prisredigering** og **Tillat rabattredigering** på **Konsernintern**-siden.

Hvis du legger til et nytt tillegg i det konserninterne salgsordrehodet og et nytt tillegg til den konserninterne salgslinjen, kopieres begge tilleggene til den konserninterne bestillingen. Derfor har den konserninterne salgsordren og den konserninterne bestillingen det samme totalbeløpet. Tilleggene blir aldri kopiert til den opprinnelige salgsordren.

## <a name="copying-a-fee"></a>Kopiere et gebyr

Når du skal kopiere et gebyr til den opprinnelige salgsordren, oppretter du det som en ny salgslinje som har en vare av typen **Tjeneste**.

## <a name="changing-quantities-and-deleting-intercompany-purchases-and-sales-order-lines"></a>Endre antall og slette konserninterne bestillinger og salgsordrelinjer

Du kan bare endre antallet eller slette en konsernintern bestillings- eller salgsordrelinje hvis linjen ble opprettet direkte fra skjemaet **Salgsordre** eller **Bestilling**. Denne endringen fører til at enten den konserninterne bestillingen eller salgsordren/-linjen blir kilden.

## <a name="origins-of-orders-and-order-lines"></a>Opprinnelse til ordrer og ordrelinjer

Konserninterne ordrer og ordrelinjer kan ha én av to opprinnelser:

- **Avledet** – Ordren ble opprettet automatisk fra en konsernintern ordrekjede.
- **Kilde** – Ordren ble opprettet manuelt av en bruker.

Opprinnelsen er angitt i ordrehodet til de konserninterne bestillings- og salgsordrene i feltet **Opprinnelse**. Dette feltet finnes i hurtigfanen **Konserninterne innstillinger** i salgsordren og i **Oppsett**-hurtigfanen i bestillingen.

Opprinnelsen til **Avledet** og **Kilde** gjelder bare konserninterne ordrer. Feltet **Opprinnelse** er tomt for alle andre salgsordrer, bestillinger og ordrelinjer. Dette feltet er også tomt for den opprinnelige salgsordren.

## <a name="example-derived-origin"></a>Eksempel: Avledet opprinnelse

Du oppretter en opprinnelig salgsordre for en ekstern kunde. Denne salgsordren inneholder én ordrelinje. Denne opprinnelige salgsordren oppretter en konsernintern bestilling som inneholder én ordrelinje, som oppretter en konsernintern salgsordre som inneholder én ordrelinje. Det konserninterne bestillingshodet og den konserninterne ordrelinjen blir opprettet automatisk fra den opprinnelige salgsordren.

Verdien til **Opprinnelse**-feltet i hurtigfanen **Oppsett** for den konserninterne bestillingen, og hurtigfanen **Konsernintern innstilling** for i de konserninterne salgsordrehodene er **Avledet**. Verdien til **Opprinnelse**-feltet i kategorien **Linjedetaljer** i bestillings- og salgsordrelinjer er også **Avledet**.

Hvis en ordrelinje har opprinnelsen **Avledet**, kan du ikke slette ordrelinjen direkte. Du kan bare slette ordrelinjen fra kilden som opprettet ordrelinjen. Du kan også bare slette det bestilte antallet fra kilden som opprettet ordrelinjen.

Hvis en opprinnelig salgsordre og en opprinnelig salgsordrelinje er en del av den konserninterne ordrekjeden, kan du endre det bestilte antallet fra den opprinnelige salgsordren, og du kan slette ordrelinjer fra den opprinnelige salgsordren.

## <a name="example-source-origin"></a>Eksempel: Kildeopprinnelse

Du oppretter en bestilling for en konsernintern leverandør. Den konserninterne bestillingen og ordrelinjen får begge opprinnelsen **Kilde**. Derfor blir denne konserninterne bestillingen kontrolleren, og en konserninterne salgsordren som opprettes automatisk i leverandørfirmaet, har opprinnelsen **Avledet**.

I tillegg kan ikke det bestilte antallet i en ordrelinje som er opprettet i den konserninterne bestillingen, endres på den konserninterne salgsordren. Ordrelinjen kan bare slettes fra den konserninterne bestillingen. Hvis det legges til en ny linje i den konserninterne salgsordren, har den konserninterne salgsordrelinjen deretter opprinnelsen **Kilde**.

Når en opprinnelig salgsordre er en del av den konserninterne ordrekjeden, kan du alltid kontrollere de konserninterne ordrene og de konserninterne ordrelinjene fra den opprinnelige salgsordren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

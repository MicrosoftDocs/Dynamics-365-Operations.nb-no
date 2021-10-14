---
title: Endre eller slette en opprinnelig konsernintern salgsordre
description: Dette emnet beskriver hvordan du endrer og sletter en opprinnelig salgsordrefunksjonalitet
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
ms.openlocfilehash: 7bd6bdbf65499e9f18bf6bb5e160a5634bc37fba
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548444"
---
# <a name="change-or-delete-an-original-intercompany-sales-order"></a>Endre eller slette en opprinnelig konsernintern salgsordre

[!include [banner](../../includes/banner.md)]

Når du endrer en salgsordre, synkroniseres disse endringene automatisk med både den relevante konserninterne bestillingen og den konserninterne salgsordren.

> [!NOTE]
> Bestillinger for eksterne leverandører påvirkes ikke av endringer du gjør, og det gjør heller ikke de opprinnelige salgslinjene som er koblet til bestillingslinjene for eksterne leverandører.

Tabellen nedenfor summerer endringene du kan gjøre og de forventede resultatene.

| Operasjon | Resultat |
|---|---|
| Slett&nbsp;en&nbsp;opprinnelig&nbsp;salgs&nbsp;ordre. | Den relaterte konserninterne bestillingen og den konserninterne salgsordren slettes også. Hvis statusen for ordren er **Plukkliste** eller senere i prosessen, kan du ikke slette salgsordren. |
| Slett en opprinnelig salgsordrelinje. | Den relaterte konserninterne bestillingslinjen og den konserninterne salgsordrelinjen slettes. Hvis statusen for ordren er **Plukkliste** eller senere i prosessen, kan du ikke slette salgsordrelinjen. |
| Legg til en ny salgslinje i en opprinnelig salgsordre. | Den nye salgslinjen opprettes både i den konserninterne bestillingen og i den konserninterne salgsordren. |
| Endre antallet på en opprinnelig salgsordrelinje. | Antallet synkroniseres med både den konserninterne bestillingslinjen og den konserninterne salgsordelinjen. Nettobeløpet omberegnes i alle ordrene. |
| Deaktiver direkte levering for en opprinnelig salgsordre. | Du kan ikke endre **Direktelevering**-feltet i den opprinnelige salgsordren hvis den konserninterne salgsordrelinjen har nådd en minimum status på **Plukkliste**, **Utleveringsordre** eller **Plukklistejournal**. Leveringsadressen i den konserninterne bestillingen endres til standard leveringsadresse (standard leveringsadresse for bestilling). De konserninterne bestillingslinjene endres også til standard leveringsadresse for linjene. Begge synkroniseres med den konserninterne salgsordren og linjene. Leveringstypen på alle linjene i den opprinnelige salgsordren endres til **Ingen**, og feltet synkroniseres med de konserninterne bestillingslinjene. Bestillinger for eksterne leverandører påvirkes ikke, og det gjør heller ikke opprinnelige salgslinjer som er koblet til bestillingslinjer for eksterne leverandører. Leveringsdatoen for konserninterne bestillinger og linjer, og Ønsket leveringsdato / Ønsket forsendelsestid for konserninterne salgsordrer og linjer oppdateres. |
| Aktiver direkte levering for en opprinnelig salgsordre. | Du kan ikke endre **Direktelevering**-feltet i den opprinnelige salgsordren hvis den konserninterne salgsordrelinjen har nådd en minimum status på **Plukkliste**, **Utleveringsordre** eller **Plukklistejournal**. Leveringsadressen i den konserninterne bestillingen endres til leveringsadressen fra den opprinnelige salgsordren, og synkroniseres med den konserninterne salgsordren. Leveringstypen på alle linjene i den opprinnelige salgsordren endres til **Direktelevering**, og feltet synkroniseres med de konserninterne bestillingslinjene. Leveringsadressen på hver opprinnelige salgsordrelinje synkroniseres med både de konserninterne bestillingslinjen og de konserninterne salgsordrelinjene. Leveringsdatoen for konserninterne bestillinger og linjer, og Ønsket leveringsdato / Ønsket forsendelsestid for konserninterne salgsordrer og linjer oppdateres. |
| Legg til et notat i både et opprinnelig salgsordrehode og på linjene. | Notatet kopieres til den konserninterne bestillingen og den konserninterne salgsordren. |
| Endre eller slette et notat. | Hvis du endrer eller sletter et notat, endres og slettes tilsvarende notat i den konserninterne bestillingen og den konserninterne salgsordren i henhold til dette. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

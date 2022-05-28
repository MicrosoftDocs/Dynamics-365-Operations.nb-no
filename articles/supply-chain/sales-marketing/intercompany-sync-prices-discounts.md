---
title: Synkronisere konserninterne priser og rabatter
description: Dette emnet forklarer synkronisering av priser og rabatter for konserninterne salgsordrer og bestillinger
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 90fa2244b5947c37b8498d1c70cddf894979f931
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673641"
---
# <a name="synchronize-intercompany-prices-and-discounts"></a>Synkronisere konserninterne priser og rabatter

[!include [banner](../../includes/banner.md)]

Rabatter og priser synkroniseres alltid mellom den konserninterne salgsordren og den konserninterne bestillingen. Du kan også synkronisere prisen og rabattene til og fra den opprinnelige salgsordren, slik at alle ordrene har de samme prisene og rabattene. Du gjør dette fra **Konsernintern**-siden som du går til fra kategorien **Generelt** på listesiden **Alle kunder**, enten fra **Salg og markedsføring** eller fra **Innkjøp og leverandører**.

Feltet **Pris og rabatt** synkroniseres med den konserninterne salgsordrelinjen. Dette betyr at du ved å merke av for **Tillat prisredigering** og **Tillat rabattredigering** har gitt tillatelse til en endring mellom den konserninterne salgsordren og den konserninterne bestillingen. En endring i enhetsprisen, prisenheten eller salgstillegget i den konserninterne salgsordren bestemmer prisen på den konserninterne bestillingslinjen.

Hvis feltene **Tillat prisredigering** og **Tillat rabattredigering** er aktivert i den konserninterne salgsordren eller den konserninterne bestillingen, kan du endre prisen eller rabatten manuelt på begge ordrene. Hvis ikke kan du ikke det.

Hvis feltene **Tillat prisredigering** og **Tillat rabattredigering** ikke er aktivert i den konserninterne salgsordren, kan du ikke endre prisen (eller tillegg) eller rabatten manuelt på en konsernintern salgsordre.

Hvis feltene **Tillat prisredigering** og **Tillat rabattredigering** ikke er aktivert i den konserninterne bestillingen, kan du ikke endre prisen (eller tillegg) eller rabatten manuelt på en konsernintern bestilling.

Hvis feltene **Tillat prisredigering** og **Tillat rabattredigering** er aktivert i både den konserninterne bestillingen og salgsordren, kan du endre begge ordrene manuelt. Dette kan imidlertid forårsake en situasjon der oppdateringer som gjøres av én person, overstyres av oppdateringer som gjøres av en annen person i et annet firma i den samme ordren.

> [!NOTE]
> Hvis du har aktivert feltet **Pris og rabatt** i både den konserninterne salgsordren og den konserninterne bestillingen, har du ikke kontroll over prissettingen.

Hvis du vil unngå denne typen konflikter, er det best å tillate at priser og rabatter bare endres i den konserninterne salgsordren eller i den konserninterne bestillingen. Dette kan gjøres ved å aktivere feltene **Tillat prisredigering** og **Tillat rabattredigering** i én av disse ordrene.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

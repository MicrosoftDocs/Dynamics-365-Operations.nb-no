---
title: Servicemaler
description: Du kan definere en serviceavtale som en mal, og senere kopiere linjene i malen til andre serviceavtaler eller til en serviceordre.
author: sorenva
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7c99e56751230a7b8881dc55c1d460674cc6f0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850503"
---
# <a name="service-templates"></a>Servicemaler

[!include [banner](../includes/banner.md)]

Du kan definere en serviceavtale som en mal, og senere kopiere linjene i malen til andre serviceavtaler eller til en serviceordre.

## <a name="example"></a>Eksempel

En kunde som du tilbyr en tjeneste, har identiske heiser på fem forskjellige steder.

Du vil angi fem serviceavtaler for kunden, én for hvert sted.
For å begrense gjentakende oppsett og å sørge for at oppsettinformasjonen i serviceavtalene er identiske kan du opprette en serviceavtale og angi den som en mal for vedlikeholdsarbeid på heisene.

Du kan nå kopiere mallinjene til de fem nye serviceavtalene slik at hver serviceavtale fylles med linjer fra malen.

## <a name="create-a-template"></a>Opprett en mal

Når du oppretter en servicemal, oppretter du en serviceavtale, oppretter deretter de obligatoriske linjene og knytter en serviceavtale til en servicemalgruppe.

> [!NOTE]
> En serviceavtalen kan bare defineres som en mal hvis den ikke har en tilknyttet serviceordre. En serviceordre kan heller ikke genereres fra en serviceavtale som er definert som en mal.

## <a name="copy-template-lines"></a>Kopier mallinjer

Du kan kopiere mallinjer fra en servicemal til en annen serviceavtale eller til en serviceordre.

Når du kopierer mallinjer til serviceordrene eller serviceavtalene, vises malgruppene i en trevisning der hver gruppe kan utvides. I denne visningen kan du se hver mal og mallinje.

Det er enklere å bestemme servicemallinjene som du vil kopiere, hvis du har gruppert malene under navn som reflekterer bruken til malene.

## <a name="related-articles"></a>Relaterte artikler

[Kopiere servicemallinjer](copy-service-template-lines.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
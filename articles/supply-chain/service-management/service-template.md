---
title: Servicemaler
description: Du kan definere en serviceavtale som en mal, og senere kopiere linjene i malen til andre serviceavtaler eller til en serviceordre.
author: ShylaThompson
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 409c15ae9c8f5f3c9c72adf3313f4594ba3c1764
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819022"
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

## <a name="related-topics"></a>Relaterte emner

[Kopiere servicemallinjer](copy-service-template-lines.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
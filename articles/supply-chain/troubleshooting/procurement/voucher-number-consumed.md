---
title: Et bilagsnummer for produktmottak forbrukes selv om det ikke genereres et bilag
description: Et bilagsnummer for produktkvitteringen forbrukes selv om det ikke genereres et økonomisk bilag under produktkvitteringen
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0556969950c45e80d177a0e96096c4157d690ae3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477194"
---
# <a name="a-product-receipt-voucher-number-is-consumed-even-when-not-generating-a-voucher"></a>Et bilagsnummer for produktmottak forbrukes selv om det ikke genereres et bilag

## <a name="symptoms"></a>Symptomer

Et bilagsnummer for produktkvitteringen forbrukes selv om det ikke genereres et økonomisk bilag under produktkvitteringen.

## <a name="resolution"></a>Løsning

Hvis alternativet **Gjeldsavsetning på produktkvittering** er satt til *Nei* for varemodellgruppen, vil ingen posteringer til økonomimodulen forekomme. En fysisk hendelse vil imidlertid bli registrert for regnskapsformål i en underfinans, og denne hendelsen krever et bilagsnummer. Dette bilagsnummeret er bilagsnummeret som det refereres til i lagertransaksjonene.

Det anbefales at du setter alternativet **Gjeldsavsetning på produktkvittering** til *Ja*, som beskrevet i følgende blogginnlegg: [Poster tilleggskostnader på tidspunktet for produktkvitteringen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

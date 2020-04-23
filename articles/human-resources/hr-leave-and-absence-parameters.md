---
title: Konfigurere permisjons- og fraværsparametere
description: Du kan definere personalparametere for permisjon og fravær i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb992cbfbed33f88e125d3a8b721f8815414599a
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197987"
---
# <a name="configure-leave-and-absence-parameters"></a>Konfigurere permisjons- og fraværsparametere

Før du definerer permisjons- og fraværsplaner i Dynamics 365 Human Resources, kan det være lurt å kontrollere innstillingene for alle relaterte personaleparametere, inkludert:

- Nummerserie for permisjonsforespørsler
- Innstillinger for sykemelding og permisjon (FMLA)
- Innstillinger i Ansattselvbetjening for permisjons- og fraværsforespørsler
- Parametere for permisjon og fravær

## <a name="view-and-change-human-resources-parameters"></a>Vise og endre personaleparametere

1. På siden **Permisjon og fravær** velger du **Koblinger**-fanen.

2. Under **Oppsett** velger du **Personalparametere**.

3. I kategorien **Nummerserier** bekrefter du **Nummerseriekode** for **ID for permisjonsforespørsel** og endrer etter behov. Denne innstillingen bestemmer serien som skal brukes til å tilordne ID-er automatisk til permisjonsforespørsler.

4. I kategorien **FMLA** kontrollerer du FMLA-innstillingene og endrer etter behov.

5. I kategorien **Ansattselvbetjening** angir du om ledere kan angi permisjons- og fraværsforespørsler på vegne av de ansatte.

6. I kategorien **Permisjon og fravær** kontrollerer du innstillingene og endrer etter behov.

7. Velg **Lagre**.

## <a name="view-and-change-leave-and-absence-parameters"></a>Vise og endre permisjons- og fraværsparametere

1. På siden **Permisjon og fravær** velger du **Koblinger**-fanen.

2. Under **Oppsett**velger du **Permisjons- og fraværsparametere**.

3. Angi følgende parametere i kategorien **Generelt**:
 
    - Angi **Enhet for permisjon og fravær** til enten timer eller dager. Hvis dager, kan du velge **Aktiver halvdagsdefinisjon** for å la de ansatte velge enten den første eller andre halvparten av dagen i fritidsforespørsler. 

    - Velg **Gyldighetsdato for måneder med jobberfaring** for å angi når avsetningsratene trer i kraft for permisjonsplaner som bruker måneder med jobberfaring.

    - Velg **Saldoberegning** for å vise saldoer per dag eller per avsetningsperiode. Hvis du velger **Saldo per i dag**, viser saldoen summen av alle avsetningene, justeringene og forespørslene per i dag. Hvis du velger **Saldo per avsetningsperiode**, viser saldoen summen av alle avsetningene, justeringene og forespørslene fra avsetningsperioden som er definert av frekvensen i permisjonsplanen. 

## <a name="configure-calendar-parameters"></a>Konfigurere kalenderparametere

1. På siden **Permisjon og fravær** velger du **Koblinger**-fanen.

2. Under **Oppsett**velger du **Permisjons- og fraværsparametere**.

3. I kategorien **Kalender** endrer du kalenderinnstillinger etter behov.

4. Velg **Lagre**.

## <a name="see-also"></a>Se også

- [Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)

---
title: Konfigurer permisjons- og fraværsparametere
description: Denne artikkelen beskriver hvordan du definerer personalparametere for permisjon og fravær i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a39c74eef3865c03ccb9dd5aa2fece7f25e639a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891386"
---
# <a name="configure-leave-and-absence-parameters"></a>Konfigurer permisjons- og fraværsparametere

>[!Important]
>Funksjonaliteten som er nevnt i denne artikkelen, er for øyeblikket tilgjengelig for kunder i frittstående Dynamics 365 Human Resources. Noe av eller all funksjonaliteten vil være tilgjengelig som en del av en fremtidig versjon av Finance-infrastrukturen etter Finance versjon 10.0.26.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Før du definerer permisjons- og fraværsplaner i Dynamics 365 Human Resources, kan det være lurt å kontrollere innstillingene for alle relaterte **personaleparametere, inkludert**:

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

7. Velg **Lagre**.

>[!IMPORTANT]
>Visning av permisjon og fravær på tvers av firmaer er for øyeblikket i forhåndsversjon. Du må aktivere den i **sandkassemiljøet** for å vise alternativet for permisjon og fravær. Hvis du vil ha mer informasjon om aktivering av evalueringsfunksjonalitet, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

## <a name="view-and-change-human-resources-shared-parameters"></a>Vise og endre delte parametere for Human Resources

1. På siden **Personaladministrasjon** velger du **Koblinger**-fanen.

2. Under **Oppsett** velger du **delte parametere for Human Resources**.

3. I fanen **Avansert tilgang** velger du **Ja** for å **aktivere permisjonsvisning på tvers av firmaer** for å tillate at permisjon vises på tvers av firmaet.

4. Velg **Lagre**.

## <a name="view-and-change-leave-and-absence-parameters"></a>Vise og endre permisjons- og fraværsparametere

1. På siden **Permisjon og fravær** velger du **Koblinger**-fanen.

2. Under **Oppsett** velger du **Permisjons- og fraværsparametere**.

3. Angi følgende parametere i kategorien **Generelt**:
 
    - Angi **Enhet for permisjon og fravær** til enten timer eller dager. Hvis dager, kan du velge **Aktiver halvdagsdefinisjon** for å la de ansatte velge enten den første eller andre halvparten av dagen i fritidsforespørsler. 

    - Velg **Gyldighetsdato for måneder med jobberfaring** for å angi når avsetningsratene trer i kraft for permisjonsplaner som bruker måneder med jobberfaring.

    - Velg **Saldoberegning** for å vise saldoer per dag eller per avsetningsperiode. Hvis du velger **Saldo per i dag**, viser saldoen summen av alle avsetningene, justeringene og forespørslene per i dag. Hvis du velger **Saldo per avsetningsperiode**, viser saldoen summen av alle avsetningene, justeringene og forespørslene fra avsetningsperioden som er definert av frekvensen i permisjonsplanen. 

    - Angi **starttidspunktet** for den satsvise jobben for **utløpet av overføring**.  
    
    - Velg **Ja** for **Tillat ansatte å kjøpe permisjon** og **Tillat ansatte å selge permisjon**. Hvis du velger **Ja** for disse alternativene, kan du opprette policyer for kjøp og salg av permisjoner og gjøre det mulig for ansatte å sende inn og selge permisjonsforespørsler.

## <a name="configure-calendar-parameters"></a>Konfigurere kalenderparametere

1. På siden **Permisjon og fravær** velger du **Koblinger**-fanen.

2. Under **Oppsett** velger du **Permisjons- og fraværsparametere**.

3. I kategorien **Kalender** endrer du kalenderinnstillinger etter behov.

4. Velg **Lagre**.

## <a name="see-also"></a>Se også

- [Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

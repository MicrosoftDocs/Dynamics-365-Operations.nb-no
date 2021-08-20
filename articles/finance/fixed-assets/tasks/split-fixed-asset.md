---
title: Dele et anleggsmiddel
description: Dette emnet forklarer hvordan du deler en prosent av ett anleggsmiddeltablå til et nytt anleggsmiddeltablå.
author: saraschi2
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ac7bc9ae9040f9668c36c570be795ebeb7c6970049ff911b1caeadd06f31d0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778996"
---
# <a name="split-a-fixed-asset"></a>Dele et anleggsmiddel

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du deler en prosent av ett anleggsmiddeltablå til et nytt anleggsmiddeltablå. Den bruker regnskapsførerrollen og USMF-demonstrasjonsdataene.

## <a name="create-a-new-fixed-asset"></a>Opprett et nytt anleggsmiddel

1. I navigasjonsruten går du til **Moduler \> Anleggsmidler \> Anleggsmidler \> Anleggsmidler**.
2. Velg **Ny**.
3. Angi eller velg en verdi i feltet **Anleggsmiddelgruppe**. Noter anleggsmiddelnummeret for senere bruk i prosessen for deling.
4. Angi en verdi i feltet **Navn**.
5. Lukk skjemaet.

## <a name="split-a-fixed-asset"></a>Dele et anleggsmiddel

Før et ferdig avskrevet anleggsmiddel deles, skal anleggsmiddelstatusen endres manuelt fra **Lukket** til **Åpen**. Dette trinnet er nødvendig fordi den bokførte statusen må være **Åpen** hvis du må postere transaksjoner for anleggsmiddelet (for eksempel for et salg). Du må også aktivere parameteren **Tillat flere transaksjoner i ett bilag** i kategorien **Generelt** på siden **Parametere for økonomimodul**. Når statusen for anleggstablået er endret, og flere transaksjoner innenfor ett bilag er tillatt, fullfører du trinnene nedenfor for å dele opp aktivaet.

1. I listen finner og velger du koblingen for anleggsmidlet som skal deles.
2. Velg **Bøker**. Velg tablået som skal deles til det nye anleggsmiddelet.
3. Velg **Funksjoner**.
4. Velg **Del anleggsmiddel**.
5. Angi eller velg en verdi i feltet **Til anleggsmiddel**.
6. Velg rullegardinknappen i feltet **Til tablå** for å åpne oppslaget.
7. Angi en dato i feltet **Transaksjonsdato**.
8. Angi et tall i **Prosent**-feltet.
9. Angi eller velg en verdi i feltet **Journalnavn**.
10. Velg **OK**.

## <a name="post-the-journal-transaction"></a>Postere journaltransaksjonen

1. I navigasjonsruten går du til **Moduler \> Anleggsmidler \> Journaloppføringer \> Anleggsmiddeljournal**.
2. Velg journalen som ble opprettet med prosessen for deling, fra listen.
3. Velg **Linjer**.

    - Kontroller journallinjene som er opprettet.
    - En anskaffelsesjusteringstransaksjon opprettes for det originale anleggsmiddelet for å redusere verdien av prosenten som er angitt under prosessen med deling.
    - En anskaffelsestransaksjon er opprettet for det nye anleggsmiddelet for det samme beløpet.

4. Velg **Poster**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
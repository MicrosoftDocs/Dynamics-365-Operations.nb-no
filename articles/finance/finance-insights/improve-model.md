---
title: Forbedre forutsigelsesmodellen (forhåndsversjon)
description: Dette emnet beskriver funksjoner du kan bruke til å forbedre ytelsen til forutsigelsesmodeller.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 184a1cb5d3851e26b41340b711c51ef38e06eb53
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186648"
---
# <a name="improve-the-prediction-model-preview"></a>Forbedre forutsigelsesmodellen (forhåndsversjon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver funksjoner du kan bruke til å forbedre ytelsen til forutsigelsesmodeller. Du begynner å forbedre modellen i arbeidsområdet **Kundebetalingsforutsigelser** i Microsoft Dynamics 365 Finance. Forbedringstrinnene fullføres deretter i AI Builder.

## <a name="select-historical-outcomes"></a>Velge historiske resultater

Du velger først ett eller flere av de tre mulige resultatene for fakturaer: **Til planlagt tid**, **Forsinket** og **Svært sent**. Alle de tre resultatene bør velges. Hvis du fjerner merkingen av noen av resultatene, blir fakturaene filtrert ut av opplæringsprosessen, og nøyaktigheten til forutsigelsen blir redusert.

[![Bekrefte resultater](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

Hvis organisasjonen bare krever to resultater, endrer du de **Forsinket**- og **Svært sent**-terskelene til 0 (null) dager. På denne måten kan du effektivt skjule forutsigelsen til en binær tilstand **Til planlagt tid** eller **Forsinket**.

## <a name="select-fields"></a>Velg felter

Når du velger felt som skal tas med i modellen, må du være oppmerksom på at listen inneholder alle tilgjengelige felt i Microsoft Dataverse-tabellen som er tilordnet dataene i Azure Data Lake. Noen av disse feltene bør **ikke** velges. Feltene som ikke bør velges, faller inn i én av tre kategorier:

- Feltet er obligatorisk for Dataverse-tabellen, men det finnes ingen sikkerhetskopi av dataene i Data Lake.
- Feltet er en ID og gir derfor ingen mening for en maskinlæringsfunksjon.
- Feltet representerer informasjon som ikke vil være tilgjengelig under forutsigelse.

De følgende delene viser feltene som er tilgjengelige for faktura- og kundeenhetene, og viser feltene som **ikke** må velges for opplæring. Kategorien som er angitt for hvert av disse feltene, refererer til kategoriene i listen ovenfor.
 
### <a name="invoice-dataverse-table"></a>Dataverse-tabellen for faktura

Følgende illustrasjon viser feltene som er tilgjengelig for fakturatabellen.

[![Tilgjengelige felt for fakturatabellen](./media/available-fields.png)](./media/available-fields.png)

Følgende felt bør ikke velges for opplæring:

- **Fakturakonto** (kategori 2)
- **Er lukket** (kategori 3) – Dette feltet brukes til å filtrere fakturaer for læring (lukket) og forutsigelse (ikke lukket).
- **Navn** (kategori 1)
- **Kilde-ID** (kategori 2)
- **Kildepost** (kategori 2)
- **Kildetabell** (kategori 2)

### <a name="customer-dataverse-table"></a>Dataverse-tabell for kunde

Følgende illustrasjon viser feltene som er tilgjengelige for kundetabellen.

[![Tilgjengelige felt for kundetabellen](./media/related-entities.png)](./media/related-entities.png)

Følgende felt bør ikke velges for opplæring:

- **Unik nøkkel for rad** (kategori 2)

## <a name="filters"></a>Filtre

Filtrene støtter for øyeblikket ikke scenarioet med kundebetalingsforutsigelse. Velg derfor **Hopp over dette trinnet**, og fortsett til sammendragssiden.

[![Fokusmodell med filtre](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

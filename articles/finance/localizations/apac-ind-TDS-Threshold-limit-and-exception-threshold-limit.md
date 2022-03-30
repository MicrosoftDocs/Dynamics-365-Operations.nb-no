---
title: Terskelgrense og unntaksterskelgrense
description: Dette emnet beskriver terskelen og unntaksgrensene for TDS (Tax Deducted at Source).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 8391953024f302e75f23c72f8078d59a5541e24b
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2022
ms.locfileid: "8408210"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a>Terskelgrense og unntaksterskelgrense

[!include [banner](../includes/banner.md)]

Dette emnet beskriver terskelen og unntaksgrensene for TDS (Tax Deducted at Source). TDS for fakturaer og betalinger beregnes alltid med hensyn til terskelgrensen og unntaksterskelgrensen som er definert for TDS-avgiftskomponentene på siden **Komponenter for kildeskatt**. TDS-avgiftskomponentene er knyttet til TDS-avgiftskoder, som er inkludert i TDS-avgiftsgruppene. TDS-avgiftsgruppene er knyttet til leverandører og kunder for å beregne TDS på fakturanivået eller betalingsnivået.

TDS beregnes hvis beløpet for en transaksjon eller de kumulative transaksjonene som er postert med en bestemt TDS-gruppe for en leverandør, overskrider terskelgrensen som er angitt på siden **Komponenter for kildeskatt**. TDS blir ikke beregnet før det kumulative transaksjonsbeløpet overskrider den angitte terskelgrensen.

Hvis en unntaksterskelgrense angis sammen med terskelgrensen for en TDS-komponent, beregnes TDS når et bestemt transaksjonsbeløp overskrider unntaksterskelgrensen, selv om det kumulative transaksjonsbeløpet ikke overskrider den angitte terskelgrensen.

### <a name="example"></a>Eksempel
En avgiftskomponent kalt TDS konfigureres og knyttes til TDS-avgiftsgruppen kalt Oppdragstaker. Terskelen er definert som 50 000, og unntaksterskelen er definert som 20 000 for TDS-avgiftskomponenten. TDS-oppdragstakergruppen er definert som standard TDS-gruppe for leverandør 1.

En innkjøpsfaktura 001 posteres for leverandør 1 for 10 000. TDS beregnes ikke for fakturaen, fordi fakturabeløpet ikke har nådd terskelgrensen eller unntaksterskelgrensen. En innkjøpsfaktura 002 posteres for leverandør 1 for 25 000. TDS beregnes for fakturaen fordi fakturabeløpet har krysset terskelgrensen eller unntaksterskelgrensen. En innkjøpsfaktura 003 posteres for leverandør 1 for 20 000. TDS beregnes for fakturaen fordi det totale fakturabeløpet til de tre fakturaene som er utstedt for leverandøren, har krysset terskelgrensen. TDS beregnes for alle fakturaer som utstedes for leverandøren, der TDS ikke har blitt beregnet tidligere. Derfor beregnes TDS for 30 000, som er det totale fakturabeløpet i faktura 001 og 003.

Det tas ikke hensyn til terskelgrensen og unntaksterskelgrensen for TDS-beregningen hvis det er merket av for **Overse terskel** for TDS-avgiftskoder i TDS-gruppen som er knyttet til transaksjonen. Terskelgrensen brukes ikke i TDS-avgiftskodene i TDS-gruppen som **Overse terskel** er for.

Hvis det er merket av for **Overse terskel** for en bestemt TDS-gruppe for enkelte fakturaer, men ikke er merket av for andre fakturaer som ble opprettet for en bestemt leverandør/kunde, kan det hende at TDS beregnes uten å overse terskelgrensen for få fakturaer, der det tas hensyn til det kumulative beløpet for alle fakturaer som TDS ikke har blitt beregnet for tidligere.

La oss si at terskelgrensen er 25 000. Følgende fakturaer opprettes for leverandør A.

- Faktura 1 – 20 000 – (det er ikke merket av for **Overse terskel**): TDS beregnes ikke.

- Faktura 2 – 4 000 – (det er merket av for **Overse terskel**): TDS beregnes for 4 000.

- Faktura 2 – 3 000 – (det er ikke merket av for **Overse terskel**): TDS beregnes som det kumulative fakturabeløpet, det vil si 27 000 (20 000 + 4 000 + 3 000), som har overskredet terskelgrensen. TDS beregnes for det kumulative beløpet i fakturaer som TDS ikke er beregnet for tidligere, det vil si 23 000 (20 000 + 3 000).

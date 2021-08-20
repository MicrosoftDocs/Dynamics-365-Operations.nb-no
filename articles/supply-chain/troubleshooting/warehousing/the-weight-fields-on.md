---
title: Vektfeltene på lastlinjene stemmer ikke overens med vektfeltene på lasten
description: Vektfeltene på lastlinjene stemmer ikke overens med vektfeltene på lasten
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f71ac7b2777cb77fccdf1a4c72a47c9b406bbd68b2d20c41ddc96028d2ffc348
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756709"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a>Vektfeltene på lastlinjene stemmer ikke overens med vektfeltene på lasten

Feilkoder: WHSLoadWeightOnLinesDoNotMatchLoadWarning

## <a name="symptoms"></a>Symptomer

Systemet viser følgende feilmelding:

> Vektfeltene på lastlinjene stemmer ikke overens med vektfeltene på lasten %1. Kjør konsekvenskontroll av lagerlastvekt for å beregne vektfeltene på nytt.

## <a name="cause"></a>Årsak

Feltene **Nettovekt** og **Taravekt** settes til *0* (null) på lastlinjen. Vektfeltene settes imidlertid ikke til *0* for vektmålinger på produktet. Når vektfeltene ikke er angitt på lastlinjen, kan alle rettelser av antallet på lastlinjene føre til feil vektberegning på lasten. Dette problemet kan oppstå hvis vekten på produktet er endret siden lastlinjen ble opprettet.

## <a name="resolution"></a>Oppløsning

Når det opprettes en lastlinje, angis vektfeltene fra produktet som standard på den. Hvis vekten er null, kan du omberegne den ved å bruke funksjonaliteten for *konsekvenskontroll av lagerlastvekt*.

1. Gå til **Systemadministrasjon \> Periodiske oppgaver \> Database \> Konsekvenskontroll**.
1. I dialogboksen **Konsekvenskontroll** setter du **Modul**-feltet til *Lagerstyring*.
1. Sett feltet **Kontroller/korriger** til *Rett feil*.
1. Merk av for **Konsekvenskontroll av lagerlastvekt** i avmerkingslisteboksen, og kontroller at bare raden for denne avmerkingsboksen er uthvevet.
1. Øverst i avmerkingsbokslisten velger du ellipseknappen (**...**), og deretter velger du **Dialogboks** på menyen.
1. I **Konsekvenskontroll av lagerlastvekt** definerer du følgende felt for å angi kriteriene som konsekvenskontrollen skal kjøres for:

    - **Last-ID:** Angi en last-ID. La denne stå tom for å kontrollere alle last-IDene.
    - **Varenummer:** Angi et varenummer. La denne stå tom for å kontrollere alle elementer.
    - **Omberegn alltid vekt på last:** Sett dette alternativet til *Ja*.
    - **Tillat overskriving av vekt på lastlinjer:** Sett dette alternativet til *Ja*.

1. Velg **OK** for å lukke dialogboksen **Konsekvenskontroll av lagerlastvekt**.
1. Velg ellipseknappen, og velg deretter **Utfør** på menyen.

Vekten beregnes på nytt basert på kriteriene du har angitt. Velg koblingen **Meldingsdetaljer** for å vise resultatet av konsistenskontrollen.

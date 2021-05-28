---
title: Lagerbeholdningsjustering
description: Dette emnet gir informasjon om lagerjusteringsjournalen og -behandlingen når du bruker skaleringsenheter.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a451816078ca2e77f30379828777209dc48bd849
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026139"
---
# <a name="warehouse-inventory-adjustment"></a>Lagerbeholdningsjustering

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Funksjonen for lagerjusteringsjournal brukes når du kjører skaleringsenheter for sky og kant for [produksjonsarbeidsbelastninger](cloud-edge-workload-manufacturing.md) og [lagerstyringsarbeidsbelastninger](cloud-edge-workload-warehousing.md).

Når en arbeider utfører lagerjustering ved hjelp av lagerappen mot en arbeidsmengde for lagerstyring for skaleringsenhet, må den fysiske lageroppdateringen behandles av den satsvise jobben **Lagerjusteringsjournal**, som du kjører og planlegger ved å gå til **Lagerstyring > Periodiske oppgaver > Lagerjusteringsjournal**.

Følgende arbeidsprosesser for lagerapp bruker for øyeblikket **Lagerjusteringsjournal** på arbeidsbelastninger for skalaenhet:

- Justering inn/ut
- Syklustelling
- Nummerskiltlasting

Flere lagertransaksjoner opprettes som en del av hver lagerjusteringsprosess, fordi senterets og skalaenhetens distribusjoner deler lagerposter.

## <a name="inventory-adjustment-example"></a>Eksempel på lagerjustering

I dette eksemplet har en lagerarbeider brukt lagerappen til å registrere tilføyingen av lagerbeholdningen.

For det første oppretter arbeidsbelastningen for skalaenhet en lagerjusteringstransaksjon for den positive fysiske justeringen, som deretter synkroniseres til senteret og resulterer i en økning av lagerbeholdningen i senteret.

| Type                                    | Storskalaenhet | Retning | Hub |
|-----------------------------------------|------------|-----------|-----|
| Lagerbeholdningsjustering          | +1         | ->        | +1  |

Senteret behandler deretter en opptellingsjournalpostering, som mottas via [meldinger for meldingsprosessor](cloud-edge-message-processor-messages.md). Dette oppdaterer den ekstra lagerbeholdningen. For å hindre dobbel lagerbeholdning oppretter senteret en mottransaksjon som en del av denne prosessen, og fjerner den tidligere registrerte lagerbeholdningen som er relatert til lagerjusteringen.

| Type                                    | Storskalaenhet | Retning | Hub |
|-----------------------------------------|------------|-----------|-----|
| Opptelling                                | +1         | <-        | +1  |
| Lagerjustering (motregning) | -1         | <-        | -1  |

Når en skalaenhet har opprettet en **Lagerjusteringsjournal** i senteret, kan du gå gjennom både **Opptellingsjournal** og **Motposteringsjournalen**, som opprettes av senteret som en del av justeringsprosessen.

Du kan gå gjennom hver av disse journaloppføringene og transaksjonene i Supply Chain Management ved å gjøre følgende:

1. Logg deg på skaleringsenheten.
1. Gå til **Lagerstyring \> Periodiske oppgaver \> Lagerjusteringsjournal**.
1. På siden **Lagerjusteringsjournal** finner og åpner du journalen som registrerte endringene i lagerbeholdningen. **Journallinjer**-delen viser hver justering som registreres av denne journalen.
1. Logg deg på senteret.
1. Gå til **Lagerstyring \> Periodiske oppgaver \> Lagerjusteringsjournal**.
1. På siden **Lagerjusteringsjournal** skal du se den samme journalen oppført hvis senteret og skalaenheten er synkronisert.
1. Åpne journalen. Hvis [meldinger for meldingsprosessor](cloud-edge-message-processor-messages.md) er behandlet, vil du se koblinger til **Opptellingsjournal** og **Motposteringsjournal** i hodet.
    - **Opptellingsjournalen** bør vise de samme dimensjonsverdiene som journallinjene.
    - **Motposteringsjournal** skal vise motregningen, som fjerner den doble lagerjusteringen.
    > [!NOTE]
    > Når all synkronisering og behandling er fullført, synkroniseres **Opptellingsjournal** og **Motposteringsjournal** tilbake til skalaenheten. Disse kan også vises fra den relevante **Lagerjusteringsjournal**-siden.

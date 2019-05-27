---
title: Motta delleveringer av returnerte varer
description: Delvise leveringer defineres som returordrelinjer, ikke som returordreforsendelser.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2b7bfad1e0d80675848353d4118960d44f2dc01
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570325"
---
# <a name="receive-partial-deliveries-of-returned-items"></a>Motta delleveringer av returnerte varer    

[!include [banner](../includes/banner.md)]


Delvise leveringer defineres som returordrelinjer, ikke som returordreforsendelser.

Dette betyr at hvis du mottar hele antallet som er angitt på én returordrelinje, men ingenting fra de andre linjene i returordren, er leveringen ikke en delvis levering. Hvis en returordrelinje krever at ti enheter av en bestemt vare returneres, men du bare mottar fire, er dette imidlertid en delvis levering.

Hvis en returforsendelse inneholder mindre enn hele antallet i en returordrelinje, kan du sette forsendelsen til side og vente til resten av det returnerte antallet ankommer, eller du kan registrere og postere den delvise leveringen.

## <a name="register-and-post-a-partial-quantity"></a>Registrere og postere en delvis levering

1.  Når du har valgt en returordre for ankomst i skjemaet **Oversikt over ankomst - Lager: %1, Mottakssone: %2, Journalnavn: %3**, klikker du **Start ankomst** for å opprette ankomstjournalen, og klikk deretter **Journaler** \> **Vis ankomster fra mottak** for å åpne **Lokasjonsjournal-skjemaet**.

2.  Merk linjen du vil arbeide med i journalen, og klikk deretter **Linjer** for å åpne skjemaet **Journallinjer, lokasjoner**.

3.  Merk linjen til varenummeret som har ankommet med bare en del av antallet, og klikk deretter **Funksjoner** \> **Del** for å åpne **Del**-skjemaet.

4.  I feltet **Delingsantall** angir du det totale antallet av varer som er mottatt, og klikk deretter **OK**.

5.  I skjemaet **Journallinjer, lokasjoner** merker du linjen for antallet av varer som er ankommet, og klikk deretter **Poster**. Du kan postere linjen for resten av antallet etter at varene er ankommet.





---
title: Tilbakefør innstillinger for journaler og linjer
description: Dette emnet omhandler hvorfor en tilbakeføringsoppføring som ble angitt i en økonomijournal, kanskje ikke er tatt med i den posterte transaksjonen.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d0659fbd814d3fb86b2f4a1ecb6162614ab8a4f125029fbb04f08cc5fb52b45c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780828"
---
# <a name="reverse-settings-on-journals-and-lines"></a>Tilbakefør innstillinger for journaler og linjer

[!include [banner](../includes/banner.md)]

Dette emnet omhandler hvorfor en tilbakeføringsoppføring som ble angitt i en økonomijournal, kanskje ikke er tatt med i den posterte transaksjonen.  

## <a name="symptom"></a>Symptom

En økonomijournal inneholder en tilbakeføringsoppføring og tilbakeføringsdato i journalen. Når du posterer journalen, tilbakeføres ingen av bilagene. Hvorfor skjer dette?

## <a name="resolution"></a>Løsning

Når journalen posteres, ser tilbakeføringsprosessen bare på innstillingene for **tilbakeføringsoppføring** og **tilbakeføringsdato** i delen **Linjer** på bilaget. Ved hjelp av denne fremgangsmåten kan en journal omfatte noen bilag som er merket for tilbakeføring, mens andre som ikke er det.

Verdiene fra journalen brukes bare som standard når det legges til *nye* linjer. Endring av verdiene i journalen påvirker ikke eksisterende linjer. I dette eksemplet ble bilagslinjene lagt inn først. Når du angir linjedetaljene før du angir journalen som tilbakeføring, blir ikke betegnelsen som en tilbakeføringsoppføring og -dato brukt på noen eksisterende linjer.

Endring av tilbakeføringsoppføringen eller tilbakeføringsdatoen på en eksisterende linje overfører den til andre linjer i det samme bilaget. For å optimalisere ytelsen oppdateres ikke rutenettet etter at endringer er overført til andre linjer. Du kan vise de oppdaterte verdiene ved å oppdatere rutenettet.



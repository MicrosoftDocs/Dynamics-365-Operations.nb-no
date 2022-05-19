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
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ff8c0bda8e750e95261039b373cfb96a76034f6f
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724452"
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



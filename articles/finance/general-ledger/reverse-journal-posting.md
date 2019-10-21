---
title: Tilbakeføre journalpostering
description: Dette emnet beskriver funksjoner som lar deg tilbakeføre bilag fra bilagstransaksjonslisten eller fra finansjournaler.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248591"
---
# <a name="reverse-journal-posting"></a>Tilbakeføre journalpostering

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjonene i Microsoft Dynamics 365 Finance som lar deg tilbakeføre en hel journal eller tilbakeføre ett eller flere bilag fra bilagstransaksjonslisten, uavhengig av opprinnelsen. 

## <a name="reversing-journals"></a>Tilbakeføre journaler

Du kan tilbakeføre Journallinjer enkeltvis. Med tilbakeføring av journalpostering kan du også tilbakeføre en hel finansjournal. Slik tilbakefører du en journal: 
- Åpne finansjournalen, og filtrer på posterte journaler
- Klikk på Tilbakefør-menyen øverst på siden.
- Du vil se det totale antallet bilag og bilagslinjer i tillegg til total beløpet på linjene som blir tilbakeført
- Velg Ja hvis du vil bruke de eksisterende transaksjonsdatoene, eller Nei hvis du vil angi en ny. I noen tilfeller kan det hende at perioden for den opprinnelige transaksjonen er lukket og du vil angi en ny transaksjonsdato for tilbakeføringen.
- Hvis du valgte Nei, angir du en transaksjonsdato for tilbakeføringen. 
- Angi en kommentar som du vil legge til i tilbakeføringstransaksjonen
- Klikk på Tilbakefør-knappen

Transaksjonen blir tilbakeført. 

Hvis antallet bilagslinjer overskrider 100 linjer, kjøres tilbakeføringsprosessen ved hjelp av den satsvise prosessen. Du kan se gjennom resultatene av tilbakeføringen ved å vise kommentarene i den satsvise jobben som ble kjørt. Alle feil vil bli registrert i loggen for den satsvise jobben.

Hvis antallet bilagslinjer er 100 linjer eller færre, kjøres tilbakeføringsprosessen umiddelbart. Resultatene vises i en dialogboks som viser alle bilag som ikke kunne tilbakeføres og årsaken til at det ikke kunne tilbakeføres. Klikk på OK for å lukke dialogboksen.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Tilbakeføring av bilag fra bilagstransaksjonslisten. 

Du kan også tilbakeføre bilag fra **bilagstransaksjonslisten** på tvers av alle underfinansjournaler. I tillegg kan du tilbakeføre flere enn ett bilag om gangen. 

Slik tilbakefører du ett eller flere bilag: 
- Klikk på Tilbakefør-menyen øverst på siden.
- Du vil se det totale antallet bilag og bilagslinjer i tillegg til total beløpet på linjene som blir tilbakeført
- Velg Ja hvis du vil bruke de eksisterende transaksjonsdatoene, eller Nei hvis du vil angi en ny. I noen tilfeller kan det hende at perioden for den opprinnelige transaksjonen er lukket og du vil angi en ny transaksjonsdato for tilbakeføringen.
- Hvis du valgte Nei, angir du en transaksjonsdato for tilbakeføringen. 
- Angi en kommentar som du vil legge til i tilbakeføringstransaksjonen
- Klikk på Tilbakefør-knappen

Transaksjonen blir tilbakeført. 

Hvis antallet bilagslinjer overskrider 100 linjer, kjøres tilbakeføringsprosessen ved hjelp av den satsvise prosessen. Du kan se gjennom resultatene av tilbakeføringen ved å vise kommentarene i den satsvise jobben som ble kjørt. Alle feil vil bli registrert i loggen for den satsvise jobben.

Hvis antallet bilagslinjer er 100 linjer eller færre, kjøres tilbakeføringsprosessen umiddelbart. Resultatene vises i en dialogboks som viser alle bilag som ikke kunne tilbakeføres og årsaken til at det ikke kunne tilbakeføres. Klikk på OK for å lukke dialogboksen.


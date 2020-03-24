---
title: Tilbakeføre journalpostering
description: Dette emnet beskriver funksjoner som lar deg tilbakeføre bilag fra bilagstransaksjonslisten eller fra finansjournaler.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5d1c58463c24dc6a40b036f0bb803316bbb65c2
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091905"
---
# <a name="reverse-journal-posting"></a>Tilbakeføre journalpostering

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjonene i Microsoft Dynamics 365 Finance som lar deg tilbakeføre en hel journal eller tilbakeføre ett eller flere bilag fra bilagstransaksjonslisten, uavhengig av opprinnelsen. 

## <a name="reversing-journals"></a>Tilbakeføre journaler

Du kan tilbakeføre Journallinjer enkeltvis. Med tilbakeføring av journalpostering kan du også tilbakeføre en hel finansjournal. Slik tilbakefører du en journal: 

- Åpne finansjournalen, og filtrer på posterte journaler.
- Velg **Tilbakefør**-menyen øverst på siden.
- Du vil se det totale antallet bilag og bilagslinjer i tillegg til total beløpet på linjene som blir tilbakeført
- Velg **Ja** hvis du vil bruke de eksisterende transaksjonsdatoene, eller **Nei** hvis du vil angi en ny. I noen tilfeller kan det hende at perioden for den opprinnelige transaksjonen er lukket, og du må angi en ny transaksjonsdato for tilbakeføringen.
- Hvis du velger **Nei**, angir du en transaksjonsdato for tilbakeføringen. 
- Angi en kommentar som du vil legge til i tilbakeføringstransaksjonen.
- Velg **Tilbakeføring**-knappen.

Transaksjonen blir tilbakeført. 

Hvis antallet bilagslinjer overskrider 100 linjer, kjøres tilbakeføringsprosessen ved hjelp av den satsvise prosessen. Du kan se gjennom resultatene ved å vise kommentarene i den satsvise jobben. Alle transaksjoner som ikke kan tilbakeføres, vises i loggen for den satsvise jobben.

Hvis antallet bilagslinjer er 100 linjer eller færre, kjøres tilbakeføringsprosessen umiddelbart. Resultatene vises i en dialogboks som viser alle bilag som ikke kunne tilbakeføres, sammen med årsaken til at det ikke kunne tilbakeføres. Velg **OK** for å lukke dialogboksen.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Tilbakeføring av bilag fra bilagstransaksjonslisten. 

Du kan også tilbakeføre bilag fra **bilagstransaksjonslisten** på tvers av alle underfinansjournaler. I tillegg kan du tilbakeføre flere enn ett bilag om gangen. 

Slik tilbakefører du ett eller flere bilag: 

- Velg **Tilbakefør**-menyen øverst på siden.
- Du vil se det totale antallet bilag og bilagslinjer i tillegg til total beløpet på linjene som blir tilbakeført.
- Velg **Ja** hvis du vil bruke de eksisterende transaksjonsdatoene, eller **Nei** hvis du vil angi en ny. I noen tilfeller kan det hende at perioden for den opprinnelige transaksjonen er lukket, og du må angi en ny transaksjonsdato for å tilbakeføre den.
- Hvis du velger **Nei**, angir du en transaksjonsdato for tilbakeføringen. 
- Angi en kommentar for å beskrive tilbakeføringstransaksjonen.
- Velg **Tilbakeføring**-knappen.

Transaksjonen blir tilbakeført. 

Hvis det finnes mer enn 100 bilagslinjer, kjøres tilbakeføringsprosessen ved hjelp av den satsvise prosessen. Du kan se gjennom resultatene ved å vise kommentarene i den satsvise jobben. Alle transaksjoner som ikke kan tilbakeføres, registreres i loggen for den satsvise jobben.

Hvis antallet bilagslinjer er 100 linjer eller færre, kjøres tilbakeføringsprosessen umiddelbart. Resultatene vises i en dialogboks som viser alle bilag som ikke kunne tilbakeføres, sammen med årsaken til at det ikke kunne tilbakeføres. Velg **OK** for å lukke dialogboksen.

Transaksjoner kan bare tilbakeføres hvis de oppfyller forretningsreglene for tilbakeføring. Leverandørbetalinger kan ikke reverseres ved hjelp av funksjonen som er beskrevet i dette emnet. Leverandørbetalinger må tilbakeføres ved å følge fremgangsmåten i [Tilbakeføre en leverandørbetaling](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).


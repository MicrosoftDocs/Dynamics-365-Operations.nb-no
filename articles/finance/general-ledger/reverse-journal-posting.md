---
title: Tilbakefør journalpostering
description: Denne artikkelen beskriver funksjoner som lar deg tilbakeføre bilag fra bilagstransaksjonslisten eller fra finansjournaler.
author: kweekley
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.form: LedgerTransVoucher, LedgerJournalTable
ms.openlocfilehash: 8912409ec0d2016ea4af12843319febda98663c5
ms.sourcegitcommit: e700528679a821237e644b3e21058c36ae1323c3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2022
ms.locfileid: "9680391"
---
# <a name="reverse-journal-posting"></a>Tilbakefør journalpostering

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver funksjonene i Microsoft Dynamics 365 Finance som lar deg tilbakeføre en hel journal eller tilbakeføre ett eller flere bilag fra bilagstransaksjonslisten, uavhengig av opprinnelsen. 

Før du kan bruke en av funksjonene som beskrives i denne artikkelen, må du aktivere dem i systemet. Administratorer kan bruke **Funksjonsbehandling**-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:
 - Modul: Økonomimodul
 - Funksjonsnavn: **Massetilbakeføringer for flere dokumenter**

## <a name="reversing-journals"></a>Tilbakeføre journaler

Du kan tilbakeføre Journallinjer enkeltvis. Med tilbakeføring av journalpostering kan du også tilbakeføre en hel finansjournal. Slik tilbakefører du en journal: 

- Filtrer på de posterte journalene, og åpne **Linjer**-visningen på journalen.
- Velg menyen **Tilbakefør hele journalen** øverst på siden.
- Du vil se det totale antallet bilag og bilagslinjer i tillegg til total beløpet på linjene som blir tilbakeført.
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

- Velg **rullegardinlisten Tilbakefør hele journalen** øverst på siden.
- Du vil se det totale antallet bilag og bilagslinjer i tillegg til total beløpet på linjene som blir tilbakeført.
- Velg **Ja** hvis du vil bruke de eksisterende transaksjonsdatoene, eller **Nei** hvis du vil angi en ny. I noen tilfeller kan det hende at perioden for den opprinnelige transaksjonen er lukket, og du må angi en ny transaksjonsdato for å tilbakeføre den.
- Hvis du velger **Nei**, angir du en transaksjonsdato for tilbakeføringen. 
- Angi en kommentar for å beskrive tilbakeføringstransaksjonen.
- Velg **Tilbakeføring**-knappen.

Transaksjonen blir tilbakeført. 

Hvis det finnes mer enn 100 bilagslinjer, kjøres tilbakeføringsprosessen ved hjelp av den satsvise prosessen. Du kan se gjennom resultatene ved å vise kommentarene i den satsvise jobben. Alle transaksjoner som ikke kan tilbakeføres, registreres i loggen for den satsvise jobben.

Hvis antallet bilagslinjer er 100 linjer eller færre, kjøres tilbakeføringsprosessen umiddelbart. Resultatene vises i en dialogboks som viser alle bilag som ikke kunne tilbakeføres, sammen med årsaken til at det ikke kunne tilbakeføres. Velg **OK** for å lukke dialogboksen.

Transaksjoner kan bare tilbakeføres hvis de oppfyller forretningsreglene for tilbakeføring. Leverandørbetalinger kan ikke reverseres ved hjelp av funksjonen som er beskrevet i denne artikkelen. Leverandørbetalinger må tilbakeføres ved å følge fremgangsmåten i [Tilbakeføre en leverandørbetaling](../accounts-payable/reverse-vendor-payment.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

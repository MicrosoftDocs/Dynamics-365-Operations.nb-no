---
title: Utlign rest
description: Du kan utligne det gjenstående beløpet fra utligningsaktivitet ved å bruke dette beløpet i en finanskonto.
author: mikefalkner
ms.date: 10/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 1eb82c1f5982b30052acb2cb7659f6c07f2a4da54b68f602a2afb4e499fbcc73
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719794"
---
# <a name="settle-remainder"></a>Utlign rest

[!include [banner](../includes/banner.md)]

Du kan utligne det gjenstående beløpet fra utligningsaktivitet ved å bruke dette beløpet på en finanskonto eller en annen kunde. Du kan utligne resten når du utligner beløpene som er angitt i en journal, eller når du bare utligner åpne transaksjoner.

## <a name="setting-up-defaults"></a>Definere standarder 
Du må aktivere funksjonen Utlign rest og definere standardinnstillingene før du bruker Utlign rest.

1)  Klikk på **Kunder > Parametere > Utligninger** eller **Leverandører > Parametere > Utligninger**.
2)  Velg kategorien **Utligning**, og klikk på **Aktiver utligningsrest**.
3)  I **Standard årsakskode** velger du standard årsakskode. Årsakskodene må allerede være definert i **Kunder > Oppsett > Årsakskoder for kundeavskrivning** eller **Leverandører > Oppsett > Årsakskoder for kundeavskrivning**. **Standard utligningsrestkonto** vil som standard settes til kontoen som er tilordnet til årsakskoden for avskrivning.
3)  Oppdater **Standard utligningsrestkonto** etter behov.
4)  I **Standard journalnavn** velger du en betalingsjournal som skal brukes hvis du vil opprette en betalingsjournal når du bare utligner åpne transaksjoner. Hvis du aktiverer funksjonen for utligningsrest, må du legge til et standard journalnavn.

## <a name="settle-remainder-from-a-journal"></a>Utligne rest fra en journal
Hvis du ikke aktiverer **Utlign rest**-funksjonen, kan du likevel angi en transaksjon i en journal og deretter utligne transaksjoner mot den som du har gjort tidligere. Når du klikker på **OK**-knappen, reduseres den åpne saldoen på fakturaen med kontantbeløpet. Hvis kontanter ikke utligner fakturaen fullstendig, forblir fakturaen åpen med et restbeløp som utlignes på et senere tidspunkt.

Når **Utlign rest**-funksjonen er aktivert, kan du utligne det gjenstående beløpet til en finanskonto. Du kan også overføre resten til en annen kundekonto (for kundetransaksjoner) eller en annen leverandør (for leverandørtransaksjoner) i stedet for å la fakturaene være åpne. 

Hvis du vil utligne resten fra **Utligning**-siden, gjør du følgende:

1)  På **Utligning**-siden merker du fakturaene eller transaksjonene som du vil utligne.
2)  Klikk på **Utlign rest**-knappen.
3)  En dialogboks vises med beløpet som skal utlignes mot en finanskonto, datoen som skal brukes til å utligne resten, standard årsakskoden fra parameterne og standardkontoen fra parameterne. 
4)  Velg en årsak til ny utligning hvis du vil endre standardårsaken. Utligningskontoen endres til kontoen som er knyttet til årsakskoden.
5)  Rediger utligningskontoen hvis du vil endre den.
6)  Hvis du utligner kundetransaksjoner og vil at resten skal flyttes til en annen kunde, velger du en kunde i **Utlign rest mot kundekonto**. Hvis du utligner leverandørtransaksjoner og vil at resten skal flyttes til en annen leverandør, velger du en leverandør i **Utlign rest mot leverandørkonto**.
6)  Klikk på **Utlign rest**.
7)  **Journal**-siden vises. En ekstra journallinje legges til journalen med utligningsrestbeløpet som beløp og utligningsrestkontoen som motkonto. Hvis du har lagt til en kunde eller leverandør slik at du kan flytte utligningsbeløpet til en annen kunde eller leverandør, legges en ekstra linje til i journalen for å flytte utligningsbeløpet til denne kunden eller leverandøren.

Når du posterer journalen, vil den åpne transaksjonen utlignes helt. 

## <a name="settle-remainder-when-you-are-only-settling-open-transactions"></a>Utligne resten når du bare utligner åpne transaksjoner
Du kan også utligne resten når du utligner åpne transaksjoner uten en journal.

Hvis du vil utligne resten, gjør du følgende:

1)  På **Utligning**-siden merker du fakturaene eller transaksjonene som du vil utligne.
2)  Klikk på **Utlign rest**.
3)  En dialogboks vises med beløpet som skal utlignes mot en finanskonto, datoen som skal brukes til å utligne resten, standard årsakskoden fra parameterne og standardkontoen fra parameterne. 
4)  Velg en årsak til ny utligning hvis du vil endre standardårsaken. Utligningskontoen endres til kontoen som er knyttet til årsakskoden.
5)  Rediger **utligningskontoen** hvis du vil endre den.
6)  Hvis du utligner kundetransaksjoner og vil at resten skal flyttes til en annen kunde, velger du en kunde i **Utlign rest mot kundekonto**. Hvis du utligner leverandørtransaksjoner og vil at resten skal flyttes til en annen leverandør, velger du en leverandør i **Utlign rest mot leverandørkonto**.
7)  Du kan også opprette en betalingsjournal med utligningsresten eller bare postere den uten en journal. Velg **Ja** for **Rediger i journal** for å opprette en betalingsjournal. Du kan redigere betalingsjournalen som du oppretter.
8)  Klikk på **Utlign rest**. Hvis du velger å opprette en journal, endres knappen til **Opprett journal**. Klikk på **Opprett journal** i stedet.
9)  Hvis du har opprettet en betalingsjournal, åpnes journalsiden når du har klikket på **Utlign rest**. En journallinje legges til journalen med utligningsrestbeløpet som beløp og utligningsrestkontoen som motkonto. Hvis du har lagt til en kunde eller leverandør slik at du kan flytte utligningsbeløpet til en annen kunde eller leverandør, legges en ekstra linje til i journalen for å flytte utligningsbeløpet til denne kunden eller leverandøren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
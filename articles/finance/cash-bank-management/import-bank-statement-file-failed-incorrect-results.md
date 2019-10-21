---
title: Feilsøking for import av bankkontoutdragsfil
description: Det er viktig at bankkontoutdragsfilen fra banken stemmer overens med oppsettet som Microsoft Dynamics 365 Finance støtter. På grunn av strenge standarder for bankkontoutdrag vil de fleste integreringer fungere riktig. Noen ganger kan imidlertid ikke utdragsfilen importeres eller har feil resultater. Disse problemene forårsakes vanligvis av små forskjeller i bankkontoutdragsfilen. Denne artikkelen forklarer hvordan disse forskjellene kan korrigeres og problemene løses.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 612ded1f68cc8e1b26b8046501bae1707175e23a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188332"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Feilsøking for import av bankkontoutdragsfil

[!include [banner](../includes/banner.md)]

Det er viktig at bankkontoutdragsfilen fra banken stemmer overens med oppsettet som Microsoft Dynamics 365 Finance støtter. På grunn av strenge standarder for bankkontoutdrag vil de fleste integreringer fungere riktig. Noen ganger kan imidlertid ikke utdragsfilen importeres eller har feil resultater. Disse problemene forårsakes vanligvis av små forskjeller i bankkontoutdragsfilen. Denne artikkelen forklarer hvordan disse forskjellene kan korrigeres og problemene løses.

<a name="what-is-the-error"></a>Hva er feilen?
------------------

Når du har forsøkt å importere en bankkontoutdragsfil, går du til jobbloggen for databehandling og kjøringsdetaljene for å finne feilen. Feilen kan være til hjelp ved at du peker på utdraget, saldoen eller utdragslinjen. Det er imidlertid ikke sannsynligvis at dette gir nok informasjon til at du finner feltet eller elementet som forårsaker problemet.

## <a name="what-are-the-differences"></a>Hva er forskjellene?
Sammenlign bankfiloppsettsdefinisjonen med Finance-importdefinisjonen, og merk deg forskjellene i feltene og elementene. Sammenlign bankkontoutdragsfilen med den tilknyttede Finance-eksempelfilen. Eventuelle forskjeller bør være lett å se i ISO20022-filene.

## <a name="time-zone-differences-on-imported-bank-statements"></a>Tidssoneforskjeller på importerte bankkontoutdrag
Dato- og klokkeslettverdiene i importfilen kan være forskjellige fra dato- og klokkeslettverdiene som vises i Finance and Operations. Hvis du vil unngå dette avviket, angir du en tidssoneinnstilling på siden **Konfigurer datakilder**. Hvis du vil ha mer informasjon om hvordan du angir en tidssoneinnstilling, kan du se [Definere prosessen for avansert bankavstemmingsimport](set-up-advanced-bank-reconciliation-import-process.md).

## <a name="transformations"></a>Transformasjoner
Endringen må vanligvis foretas i én av tre transformasjoner. Hver enkelt transformasjon er skrevet for en bestemt standard.

| Ressursnavn                                         | Filnavn                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Feilsøking av transformasjoner
### <a name="adjust-the-bai2-and-mt940-files"></a>Juster BAI2- og MT940-filene

BAI2- og MT940-filene er tekstbaserte filer, og krever en justering for å gjøre det mulig med feilsøking av Extensible Stylesheet Language Transformations (XSLT). Programmet gjør denne justeringen når en fil importeres.

1.  Opprett en XML-fil, og kopier følgende tekst til den.

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  Kopier innholdet i bankkontoutdragsfilen og lim det inn i XML-filen slik at det erstatter **PASTESTATEMENTFILEHERE**.

### <a name="debug-the-xslt"></a>Feilsøking av XSLT

Hvis du vil ha mer informasjon, kan du se <https://msdn.microsoft.com/library/ms255605.aspx>.

1.  Start Microsoft Visual Studio.
2.  Opprett et konsollprogram.
3.  Åpne aktuell XSLT.
4.  Klikk XLST-en og den tilhørende egenskapssiden.
5.  Angi inndataene til plasseringen av bankkontoutdragsfilen.
6.  Definer en plassering og et filnavn for utdataene.
7.  Angi de nødvendige bruddpunktene.
8.  Klikk **XML** på menyen &gt; **Start XSLT Debugging**.

### <a name="format-the-xslt-output"></a>Formater XSLT-utdataene

Når transformeringen kjøres, opprettes det en utdatafil som du kan vise i Visual Studio. Bruk Ctrl + A, Ctrl + K og Ctrl + D til raskt å formatere utdatafilen.

### <a name="adjust-the-transformation"></a>Juster transformasjonen

Juster transformasjonen for å hente det riktige feltet eller elementet i bankkontoutdragsfilen. Tilordne deretter feltet eller elementet til det aktuelle elementet i Finance.

### <a name="debitcredit-indicator"></a>Indikator for debet/kredit

Noen ganger importeres debetbeløp som kreditbeløp og kreditbeløp som debetbeløp. Du kan løse dette problemet ved å endre riktig XSLT-fil. Hvis bankkontoutdrag kommer fra flere banker, må du kontrollere at alle bruker samme fremgangsmåte for debet/kredit, eller opprette egne transformasjoner.

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator-malen
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit-malen
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator-malen

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Eksempler på bankkontoutdragsformater og tekniske oppsett
Tabellen nedenfor inneholder eksempler på definisjonene av tekniske oppsett for avanserte bankavstemmingsimportfiler og tre tilknyttede filer med eksempler på bankkontoutdrag. Du kan laste ned eksempelfilene og tekniske oppsett her: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| Definisjon av teknisk oppsett                             | Fil med bankkontoutdragseksempler          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |





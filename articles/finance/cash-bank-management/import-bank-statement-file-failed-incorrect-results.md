---
title: Feilsøking for import av bankkontoutdragsfil
description: Denne artikkelen forklarer hvordan du løser problemer som forårsakes av små forskjeller i bankkontoutdragsfilen.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 422b2df6c4de3a948b0e62bfb70f99b12e04a8f9
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711180"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Feilsøking for import av bankkontoutdragsfil

[!include [banner](../includes/banner.md)]

Det er viktig at bankkontoutdragsfilen fra banken stemmer overens med oppsettet som Microsoft Dynamics 365 Finance støtter. På grunn av strenge standarder for bankkontoutdrag vil de fleste integreringer fungere riktig. Noen ganger kan imidlertid ikke utdragsfilen importeres eller har feil resultater. Disse problemene forårsakes vanligvis av små forskjeller i bankkontoutdragsfilen. Denne artikkelen forklarer hvordan disse forskjellene kan korrigeres og problemene løses.

## <a name="what-is-the-error"></a>Hva er feilen?

Når du har forsøkt å importere en bankkontoutdragsfil, går du til jobbloggen for databehandling og kjøringsdetaljene for å finne feilen. Feilen kan være til hjelp ved at du peker på utdraget, saldoen eller utdragslinjen. Det er imidlertid ikke sannsynligvis at dette gir nok informasjon til at du finner feltet eller elementet som forårsaker problemet.

> [!NOTE]
> Importerte bankkontoutdrag kan bare overlappe for ett enkelt tidspunkt.  Hvis et utdrag for eksempel slutter klokken 12:00 1. januar 2021, kan startdatoen for det neste utdraget være 12:00 1. januar 2021.

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

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
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
Tabellen nedenfor inneholder eksempler på definisjonene av tekniske oppsett for avanserte bankavstemmingsimportfiler og tre tilknyttede filer med eksempler på bankkontoutdrag. Du kan laste ned eksempelfilene og tekniske oppsett her: [Importer fileksempler](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Definisjon av teknisk oppsett                             | Fil med bankkontoutdragseksempler          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

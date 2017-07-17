---
title: "Feilsøking for import av bankkontoutdragsfil"
description: "Det er viktig at bankkontoutdragsfilen fra banken stemmer overens med oppsettet som Enterprise-utgaven av Microsoft Dynamics 365 for Finance and Operations støtter. På grunn av strenge standarder for bankkontoutdrag vil de fleste integreringer fungere riktig. Noen ganger kan imidlertid ikke utdragsfilen importeres eller har feil resultater. Disse problemene forårsakes vanligvis av små forskjeller i bankkontoutdragsfilen. Denne artikkelen forklarer hvordan disse forskjellene kan korrigeres og problemene løses."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 33b7a499caf9292e44c155a0e1bd6a8929558be5
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017


---

# Feilsøking for import av bankkontoutdragsfil
<a id="bank-statement-file-import-troubleshooting" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Det er viktig at bankkontoutdragsfilen fra banken stemmer overens med oppsettet som Enterprise-utgaven av Microsoft Dynamics 365 for Finance and Operations støtter. På grunn av strenge standarder for bankkontoutdrag vil de fleste integreringer fungere riktig. Noen ganger kan imidlertid ikke utdragsfilen importeres eller har feil resultater. Disse problemene forårsakes vanligvis av små forskjeller i bankkontoutdragsfilen. Denne artikkelen forklarer hvordan disse forskjellene kan korrigeres og problemene løses.

Hva er feilen?
<a id="what-is-the-error" class="xliff"></a>
------------------

Når du har forsøkt å importere en bankkontoutdragsfil, går du til jobbloggen for databehandling og kjøringsdetaljene for å finne feilen. Feilen kan være til hjelp ved at du peker på utdraget, saldoen eller utdragslinjen. Det er imidlertid ikke sannsynligvis at dette gir nok informasjon til at du finner feltet eller elementet som forårsaker problemet.

## Hva er forskjellene?
<a id="what-are-the-differences" class="xliff"></a>
Sammenlign bankfiloppsettsdefinisjonen med Finance and Operations-importdefinisjonen, og merk deg forskjellene i feltene og elementene. Sammenlign bankkontoutdragsfilen med den tilknyttede Finance and Operations-eksempelfilen. Eventuelle forskjeller bør være lett å se i ISO20022-filene.

## Transformasjoner
<a id="transformations" class="xliff"></a>
Endringen må vanligvis foretas i én av tre transformasjoner. Hver enkelt transformasjon er skrevet for en bestemt standard.

| Ressursnavn                                         | Filnavn                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## Feilsøking av transformasjoner
<a id="debugging-transformations" class="xliff"></a>
### Juster BAI2- og MT940-filene
<a id="adjust-the-bai2-and-mt940-files" class="xliff"></a>

BAI2- og MT940-filene er tekstbaserte filer, og krever en justering for å gjøre det mulig med feilsøking av Extensible Stylesheet Language Transformations (XSLT). Programmet gjør denne justeringen når en fil importeres.

1.  Opprett en XML-fil, og kopier følgende tekst til den.

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  Kopier innholdet i bankkontoutdragsfilen og lim det inn i XML-filen slik at det erstatter **PASTESTATEMENTFILEHERE**.

### Feilsøking av XSLT
<a id="debug-the-xslt" class="xliff"></a>

Hvis du vil ha mer informasjon, se <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.

1.  Start Microsoft Visual Studio.
2.  Opprett et konsollprogram.
3.  Åpne aktuell XSLT.
4.  Klikk XLST-en og den tilhørende egenskapssiden.
5.  Angi inndataene til plasseringen av bankkontoutdragsfilen.
6.  Definer en plassering og et filnavn for utdataene.
7.  Angi de nødvendige bruddpunktene.
8.  Klikk **XML** på menyen &gt; **Start XSLT Debugging**.

### Formater XSLT-utdataene
<a id="format-the-xslt-output" class="xliff"></a>

Når transformeringen kjøres, opprettes det en utdatafil som du kan vise i Visual Studio. Bruk Ctrl + A, Ctrl + K og Ctrl + D til raskt å formatere utdatafilen.

### Juster transformasjonen
<a id="adjust-the-transformation" class="xliff"></a>

Juster transformasjonen for å hente det riktige feltet eller elementet i bankkontoutdragsfilen. Tilordne deretter feltet eller elementet til det aktuelle elementet i Finance and Operations.

### Indikator for debet/kredit
<a id="debitcredit-indicator" class="xliff"></a>

Noen ganger importeres debetbeløp som kreditbeløp og kreditbeløp som debetbeløp. Du kan løse dette problemet ved å endre riktig XSLT-fil. Hvis bankkontoutdrag kommer fra flere banker, må du kontrollere at alle bruker samme fremgangsmåte for debet/kredit, eller opprette egne transformasjoner.

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator-malen
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit-malen
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator-malen

## Eksempler på bankkontoutdragsformater og tekniske oppsett
<a id="examples-of-bank-statement-formats-and-technical-layouts" class="xliff"></a>
Tabellen nedenfor inneholder eksempler på definisjonene av tekniske oppsett for avanserte bankavstemmingsimportfiler og tre tilknyttede filer med eksempler på bankkontoutdrag. Du kan laste ned eksempelfilene og teknisk oppsett her: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| Definisjon av teknisk oppsett                             | Fil med bankkontoutdragseksempler          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |







---
title: Definere importprosess for avansert bankavstemming
description: Funksjonen Avansert bankavstemming lar deg importere og avstemme elektroniske bankkontoutdrag og automatisk avstemme dem med banktransaksjoner i Microsoft Dynamics 365 for Operations. Denne artikkelen beskriver hvordan du definerer funksjonen for import av din bankkontoutdrag.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eab840b2974f4e9e8cf542c146482ba8e4239079
ms.openlocfilehash: acf7bacf6e95725024ff0a542a059349593d01a0
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Definere importprosess for avansert bankavstemming

Funksjonen Avansert bankavstemming lar deg importere og avstemme elektroniske bankkontoutdrag og automatisk avstemme dem med banktransaksjoner i Microsoft Dynamics 365 for Operations. Denne artikkelen beskriver hvordan du definerer funksjonen for import av din bankkontoutdrag. 

Oppsettet for import av bankkontoutdrag varierer, avhengig av formatet på der elektroniske bankkontoutdraget. Microsoft Dynamics-365 for operasjoner støtter tre bankkontoutdragsformater ut av esken: ISO20022, MT940 og BAI2.

## <a name="sample-files"></a>Eksempelfiler
Du må ha filene som oversetter elektroniske kontoutdraget fra det opprinnelige formatet til et format som kan bruke Dynamics 365 for operasjoner for alle tre formater. Du kan finne de nødvendige ressursfilene under **Ressurser**-noden i Programutforsker i Microsoft Visual Studio. Når du finner filene, kopierer du dem til én enkelt kjent plassering, slik at du kan lettere kan laste dem opp i løpet av installasjonsprosessen.

| Ressursnavn                                           | Filnavn                            |
|---------------------------------------------------------|--------------------------------------|
| BankStmtImport\_BAI2CSV\_til\_BAI2XML\_xslt              | BAI2CSV-to-BAI2XML.xslt              |
| BankStmtImport\_BAI2XML\_til\_avstemming\_xslt       | BAI2XML-to-Reconciliation.xslt       |
| BankStmtImport\_BankReconciliation\_til\_sammensatte\_xslt | BankReconciliation-to-Composite.xslt |
| BankStmtImport\_ISO20022XML\_til\_avstemming\_xslt   | ISO20022XML-to-Reconciliation.xslt   |
| BankStmtImport\_MT940TXT\_til\_MT940XML\_xslt            | MT940TXT-to-MT940XML.xslt            |
| BankStmtImport\_MT940XML\_til\_avstemming\_xslt      | MT940XML-to-Reconciliation.xslt      |
| BankStmtImport\_SampleBankCompositeEntity\_xml          | SampleBankCompositeEntity.xml        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Eksempler på bankkontoutdragsformater og tekniske oppsett
Nedenfor følger eksempler på avanserte bankavstemming Importer fil tekniske oppsettet definisjoner og tre relaterte filer med bankkontoutdrag eksempel: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  

| Definisjon av teknisk oppsett                             | Fil med bankkontoutdragseksempler          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |

 

## <a name="set-up-the-import-of-iso20022-bank-statements"></a>Definere import av ISO20022-bankkontoutdrag
Først må du definere behandlingsgruppen for bankkontoutdrag for ISO20022-bankkontoutdrag ved hjelp av rammeverket for dataenhet.

1.  Gå til **arbeidsområder**&gt;**behandling av**.
2.  Click **Import**.
3.  Angi et navn for formatet, for eksempel **ISO20022**.
4.  Sett feltet **Kildedataformat** til **XML-element**.
5.  Sett feltet **Enhetsnavn** til **Bankkontoutdrag**.
6.  Hvis du vil laste opp de importerte filene, klikker du **Last opp**, og deretter går du til **SampleBankCompositeEntity.xml**-filen som du lagret tidligere.
7.  Når enheten for bankkontoutdrag er lastet opp og tilordningen er fullført, klikker du handlingen **Vis kart** for enheten.
8.  Enheten for bankkontoutdrag er en sammensatt enhet som består av fire separate enheter. Velg **BankStatementDocumentEntity** i listen, og klikk deretter handlingen **Vis kart**.
9.  Klikk **Ny** i kategorien **Transformasjoner**.
10. For serienummer 1 klikker du **Last opp fil** og velger** ISO20022XML-to-Reconciliation.xslt**-filen som *du lagret tidligere. **Merk:** Dynamics 365 for operasjoner transformeringsfiler er bygget for standard-format. Fordi banker går ofte bort fra dette formatet, må du kanskje oppdatere transformeringsfilen som skal tilordnes til din bankkontoutdragsformat. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. Click **New**.
12. For serienummer 2 klikker du **Last opp fil** og velger **BankReconciliation-to-Composite.xslt**-filen som *du lagret tidligere.
13. Klikk **Bruk transformasjoner**.

Når behandlingsgruppen for format er definert, er neste trinn å definere formatreglene for bankkontoutdrag for ISO20022 bankkontoutdrag.

1.  Gå til **bankstyring**&gt;**Setup**&gt;**bankavstemming installere Advanced**&gt;**bankkontoutdragsformat**.
2.  Click **New**.
3.  Angi et bankkontoutdragsformat, for eksempel **ISO20022**.
4.  Angi et navn for formatet.
5.  Sett feltet **Behandlingsgruppe** til gruppen som du definerte tidligere, for eksempel **ISO20022**.
6.  Merk av for **XML-fil**.

Det siste trinnet er å aktivere avanserte bankavstemming og angi formatet for bankkontoutdrag på bankkontoen.

1.  Gå til **bankstyring**&gt;**bankkonti**.
2.  Velg bankkontoen, og åpne den for å vise detaljene.
3.  I kategorien **Avstemming** setter du alternativet **Avanserte bankavstemmingen **til **Ja**.
4.  Sett feltet **Utdragsformat **til formatet som du opprettet tidligere, for eksempel **ISO20022**.

## <a name="set-up-the-import-of-mt940-bank-statements"></a>Definere import av MT940-bankkontoutdrag
Først må du definere behandlingsgruppen for bankkontoutdrag for MT940-bankkontoutdrag ved hjelp av rammeverket for dataenhet.

1.  Gå til **arbeidsområder**&gt;**behandling av**.
2.  Click **Import**.
3.  Angi et navn for formatet, for eksempel **MT940**.
4.  Sett feltet **Kildedataformat** til **XML-element**.
5.  Sett feltet **Enhetsnavn** til **Bankkontoutdrag**.
6.  Hvis du vil laste opp de importerte filene, klikker du **Last opp**, og deretter går du til **SampleBankCompositeEntity.xml**-filen som du lagret tidligere.
7.  Når enheten for bankkontoutdrag er lastet opp og tilordningen er fullført, klikker du handlingen **Vis kart** for enheten.
8.  Enheten for bankkontoutdrag er en sammensatt enhet som består av fire separate enheter. Velg **BankStatementDocumentEntity** i listen, og klikk deretter handlingen **Vis kart**.
9.  Klikk **Ny** i kategorien **Transformasjoner**.
10. For serienummer 1 klikker du **Last opp fil** og velger**MT940TXT-to-MT940XML.xslt**-filen som *du lagret tidligere.
11. Klikk **Ny**.
12. For serienummer 2 klikker du **Last opp fil** og velger ** MT940XML-to-Reconciliation.xslt**-filen som *du lagret tidligere. **Merk:** Dynamics 365 for operasjoner transformeringsfiler er bygget for standard-format. Fordi banker går ofte bort fra dette formatet, må du kanskje oppdatere transformeringsfilen som skal tilordnes til din bankkontoutdragsformat. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. Click **New**.
14. For serienummer 3 klikker du **Last opp fil** og velger **BankReconciliation-to-Composite.xslt**-filen som *du lagret tidligere.
15. Klikk **Bruk transformasjoner**.

Når behandlingsgruppen for format er definert, er neste trinn å definere formatreglene for bankkontoutdrag for MT940 bankkontoutdrag.

1.  Gå til **bankstyring**&gt;**Setup**&gt;**bankavstemming installere Advanced**&gt;**bankkontoutdragsformat**.
2.  Click **New**.
3.  Angi et bankkontoutdragsformat, for eksempel **MT940**.
4.  Angi et navn for formatet.
5.  Sett feltet **Behandlingsgruppe** til gruppen som du definerte tidligere, for eksempel **MT940**.
6.  Sett **Filtype**-feltet til **TXT**.

Det siste trinnet er å aktivere avanserte bankavstemming og angi formatet for bankkontoutdrag på bankkontoen.

1.  Gå til **bankstyring**&gt;**bankkonti**.
2.  Velg bankkontoen, og åpne den for å vise detaljene.
3.  I kategorien **Avstemming** setter du alternativet **Avanserte bankavstemmingen **til **Ja**.
4.  Når du blir bedt om å bekrefte valget og aktivere avanserte bankavstemming, klikker du **OK**.
5.  Sett feltet **Utdragsformat **til formatet som du opprettet tidligere, for eksempel **MT940**.

## <a name="set-up-the-import-of-bai2-bank-statements"></a>Definere import av BAI2-bankkontoutdrag
Først må du definere behandlingsgruppen for bankkontoutdrag for BAI2-bankkontoutdrag ved hjelp av rammeverket for dataenhet.

1.  Gå til **arbeidsområder**&gt;**behandling av**.
2.  Click **Import**.
3.  Angi et navn for formatet, for eksempel **BAI2**.
4.  Sett feltet **Kildedataformat** til **XML-element**.
5.  Sett feltet **Enhetsnavn** til **Bankkontoutdrag**.
6.  Hvis du vil laste opp de importerte filene, klikker du **Last opp**, og deretter går du til **SampleBankCompositeEntity.xml**-filen som du lagret tidligere.
7.  Når enheten for bankkontoutdrag er lastet opp og tilordningen er fullført, klikker du handlingen **Vis kart** for enheten.
8.  Enheten for bankkontoutdrag er en sammensatt enhet som består av fire separate enheter. Velg **BankStatementDocumentEntity** i listen, og klikk deretter handlingen **Vis kart**.
9.  Klikk **Ny** i kategorien **Transformasjoner**.
10. For serienummer 1 klikker du **Last opp fil** og velger **BAI2CSV-to-BAI2XML.xslt**-filen som *du lagret tidligere.
11. Klikk **Ny**.
12. For serienummer 2 klikker du **Last opp fil** og velger ** BAI2XML-to-Reconciliation.xslt**-filen som *du lagret tidligere. **Merk:** Dynamics 365 for operasjoner transformeringsfiler er bygget for standard-format. Fordi banker går ofte bort fra dette formatet, og du må kanskje oppdatere transformeringsfilen som skal tilordnes til din bankkontoutdragsformat. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. Click **New**.
14. For serienummer 3 klikker du **Last opp fil** og velger **BankReconciliation-to-Composite.xslt**-filen som *du lagret tidligere.
15. Klikk **Bruk transformasjoner**.

Når behandlingsgruppen for format er definert, er neste trinn å definere formatreglene for bankkontoutdrag for BAI2 bankkontoutdrag.

1.  Gå til **bankstyring**&gt;**Setup**&gt;**bankavstemming installere Advanced**&gt;**bankkontoutdragsformat**.
2.  Click **New**.
3.  Angi et bankkontoutdragsformat, for eksempel **BAI2**.
4.  Angi et navn for formatet.
5.  Sett feltet **Behandlingsgruppe** til gruppen som du definerte tidligere, for eksempel **BAI2**.
6.  Sett **Filtype**-feltet til **TXT**.

Det siste trinnet er å aktivere avanserte bankavstemming og angi formatet for bankkontoutdrag på bankkontoen.

1.  Gå til **bankstyring**&gt;**bankkonti**.
2.  Velg bankkontoen, og åpne den for å vise detaljene.
3.  I kategorien **Avstemming** setter du alternativet **Avanserte bankavstemmingen **til **Ja**.
4.  Når du blir bedt om å bekrefte valget og aktivere avanserte bankavstemming, klikker du **OK**.
5.  Sett feltet **Utdragsformat **til formatet som du opprettet tidligere, for eksempel **BAI2**.

## <a name="test-the-bank-statement-import"></a>Teste import av bankkontoutdrag
Det siste trinnet er å teste at du kan importere bankkontoutdraget.

1.  Gå til **bankstyring**&gt;**bankkonti**.
2.  Velg bankkontoen som funksjonen Avanserte bankavstemming er aktivert for.
3.  I kategorien **Avstem** klikker du **Bankkontoutdrag**.
4.  På siden **Bankkontoutdrag** klikker du **Importer utdrag**.
5.  Sett **Bankkonto**-feltet til den valgte bankkontoen. Feltet **Utdragsformat** angis automatisk, basert på innstillingen i bankkontoen.
6.  Klikk **Bla gjennom**, og velg den elektroniske bankkontoutdragsfilen.
7.  Klikk **Last opp**.
8.  Klikk **OK**.

Hvis importen er vellykket, vises en melding om at utdraget ble importert. Hvis importen mislyktes, går du til arbeidsområdet **Databehandling** og delen **Jobblogg** for å finne jobben. Klikk **Utførelsesdetaljer** for jobben for å åpne siden **Utførelsessammendrag** , og klikk deretter **Vis utførelseslogg** for å vise importfeilene.



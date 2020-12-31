---
title: Definere importprosess for avansert bankavstemming
description: Avansert bankavstemming-funksjonen lar deg importere elektroniske bankkontoutdrag og automatisk avstemme dem med banktransaksjoner i Microsoft Dynamics 365 Finance. Denne artikkelen beskriver hvordan du definerer funksjonen for import av din bankkontoutdrag.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45f997a91701e3fc63278cdba3479dec9dc7a467
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446394"
---
# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Definere importprosess for avansert bankavstemming

[!include [banner](../includes/banner.md)]

Avansert bankavstemming-funksjonen lar deg importere elektroniske bankkontoutdrag og automatisk avstemme dem med banktransaksjoner i Dynamics 365 Finance. Denne artikkelen beskriver hvordan du definerer funksjonen for import av din bankkontoutdrag. 

Oppsettet for import av bankkontoutdrag varierer, avhengig av formatet på der elektroniske bankkontoutdraget. Finance støtter tre formater for bankkontoutdrag som standard: ISO20022, MT940 og BAI2.

## <a name="set-time-zone-preference"></a>Angi foretrukket tidssone
Når du konfigurerer importinnstillingene for bankkontoutdraget, kan det være viktig å ta hensyn til tidssonen for dato- og klokkeslettdataene i bankkontoutdragsfilene som skal importeres. Standard er å anta at alle dato- og klokkeslettverdier allerede er i UTC/format (Coordinated Universal Time), slik at ingen tidssonekonvertering brukes når du importerer dataene. 

Det finnes et alternativ som er tilgjengelig for å angi tidssonen som skal brukes til å importere data. Dette alternativet er i feltet **Foretrukket tidssone** på hver **Detaljer om kildedataformat**-sider (hurtigfanen **Arbeidsområdet for databehandling > Konfigurer datakilder > Velge et dataformat > Regionale innstillinger**). Den foretrukne tidssonen du angir, gjelder for alle importene som bruker dette kildedataformatet. Du kan opprette så mange datakildeformater du trenger for å importere data fra flere tidssoner.  

Denne tidssonen er kanskje ikke det samme som brukerens eller firmaets tidssone, så pass på at du klargjør hvilken tidssone dato- og klokkeslettdataene bruker. Vi anbefaler at du tar hensyn til punktene nedenfor når du angir en foretrukket tidssone. 

 - Den foretrukne tidssonen, gjelder for alle importene som bruker dette kildedataformatet. Du kan opprette så mange datakildeformater du trenger for å importere data fra flere tidssoner. 
 
 - Den foretrukne tidssonen bør være den lokale tidssonen for dato- og klokkeslettdataene i importfilen. 
 
 - Tidssonen for dato- og klokkeslettdata er kanskje ikke den samme som brukerens eller firmaets tidssone.
 
 - Brukere kan justere sine egne tidssoner ved hjelp av **Brukeralternativer**.

Legg merke til at handlingene nedenfor kan bidra til å redusere potensielle dato-og klokkeslettkonflikter når du importerer bankkontoutdrag. 

 - Unngå å endre foretrukket tidssone for bankkontoer som det allerede er importert utdrag for. Hvis du endrer foretrukket tidssone, kan det påvirke rekkefølgen av nye utdrag i forhold til eksisterende utdrag på grunn av justering av tidssonen. 
 
 - Se gjennom alle importene som bruker det valgte datakildeformatet. Foretrukket tidssone som er angitt for formatet, gjelder for alle de import prosjektene som bruker dette formatet. Kontroller at foretrukket tidssone som er riktig for alle de import prosjektene som bruker dette formatet.

## <a name="sample-files"></a>Eksempelfiler
For alle tre formater må du ha filene som oversetter det elektroniske bankkontoutdraget fra det opprinnelige formatet til et format som Finance kan bruke. Du kan finne de nødvendige ressursfilene under **Ressurser**-noden i Programutforsker i Microsoft Visual Studio. Når du finner filene, kopierer du dem til én enkelt kjent plassering, slik at du kan lettere kan laste dem opp i løpet av installasjonsprosessen.

| Ressursnavn                                           | Filnavn                            |
|---------------------------------------------------------|--------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt              | BAI2CSV-to-BAI2XML.xslt              |
| BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt       | BAI2XML-to-Reconciliation.xslt       |
| BankStmtImport\_BankReconciliation\_to\_Composite\_xslt | BankReconciliation-to-Composite.xslt |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt   | ISO20022XML-to-Reconciliation.xslt   |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt            | MT940TXT-to-MT940XML.xslt            |
| BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt      | MT940XML-to-Reconciliation.xslt      |
| BankStmtImport\_SampleBankCompositeEntity\_xml          | SampleBankCompositeEntity.xml        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Eksempler på bankkontoutdragsformater og tekniske oppsett
Nedenfor følger eksempler på definisjonene av tekniske oppsett for avansert bankavstemmingsimportfil og tre tilknyttede filer med eksempler på bankkontoutdrag: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  

| Definisjon av teknisk oppsett                             | Fil med bankkontoutdragseksempler          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |



## <a name="set-up-the-import-of-iso20022-bank-statements"></a>Definere import av ISO20022-bankkontoutdrag
Først må du definere behandlingsgruppen for bankkontoutdrag for ISO20022-bankkontoutdrag ved hjelp av rammeverket for dataenhet.

1.  Gå til **Arbeidsområder** &gt; **Databehandling**.
2.  Klikk på **Importer**.
3.  Angi et navn for formatet, for eksempel **ISO20022**.
4.  Sett feltet **Kildedataformat** til **XML-element**.
5.  Sett feltet **Enhetsnavn** til **Bankkontoutdrag**.
6.  Hvis du vil laste opp de importerte filene, klikker du **Last opp**, og deretter går du til **SampleBankCompositeEntity.xml**-filen som du lagret tidligere.
7.  Når enheten for bankkontoutdrag er lastet opp og tilordningen er fullført, klikker du handlingen **Vis kart** for enheten.
8.  Enheten for bankkontoutdrag er en sammensatt enhet som består av fire separate enheter. Velg **BankStatementDocumentEntity** i listen, og klikk deretter handlingen **Vis kart**.
9.  Klikk **Ny** i kategorien **Transformasjoner**.
10. For serienummer 1 klikker du **Last opp fil** og velger **ISO20022XML-to-Reconciliation.xslt**-filen som du lagret tidligere. **Obs!** Transformeringsfiler er bygget for standardformatet. Siden banker ofte avviker fra dette formatet, må du kanskje oppdatere transformeringsfilen som skal tilordnes til bankkontoutdragsformatet. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. Klikk på **Ny**.
12. For serienummer 2 klikker du **Last opp fil** og velger **BankReconciliation-to-Composite.xslt**-filen som du lagret tidligere.
13. Klikk **Bruk transformasjoner**.

Når behandlingsgruppen for format er definert, er neste trinn å definere formatreglene for bankkontoutdrag for ISO20022 bankkontoutdrag.

1.  Gå til **Kontant- og bankbehandling** &gt; **Oppsett** &gt; **Oppsett for avansert bankavstemming** &gt; **Bankkontoutdragsformat**.
2.  Klikk på **Ny**.
3.  Angi et bankkontoutdragsformat, for eksempel **ISO20022**.
4.  Angi et navn for formatet.
5.  Sett feltet **Behandlingsgruppe** til gruppen som du definerte tidligere, for eksempel **ISO20022**.
6.  Merk av for **XML-fil**.

Det siste trinnet er å aktivere avanserte bankavstemming og angi formatet for bankkontoutdrag på bankkontoen.

1.  Gå til **Kontant- og bankbehandling** &gt; **Bankkontoer**.
2.  Velg bankkontoen, og åpne den for å vise detaljene.
3.  I kategorien **Avstemming** setter du alternativet **Avanserte bankavstemmingen** til **Ja**.
4.  Sett feltet **Utdragsformat** til formatet som du opprettet tidligere, for eksempel **ISO20022**.

## <a name="set-up-the-import-of-mt940-bank-statements"></a>Definere import av MT940-bankkontoutdrag
Først må du definere behandlingsgruppen for bankkontoutdrag for MT940-bankkontoutdrag ved hjelp av rammeverket for dataenhet.

1.  Gå til **Arbeidsområder** &gt; **Databehandling**.
2.  Klikk på **Importer**.
3.  Angi et navn for formatet, for eksempel **MT940**.
4.  Sett feltet **Kildedataformat** til **XML-element**.
5.  Sett feltet **Enhetsnavn** til **Bankkontoutdrag**.
6.  Hvis du vil laste opp de importerte filene, klikker du **Last opp**, og deretter går du til **SampleBankCompositeEntity.xml**-filen som du lagret tidligere.
7.  Når enheten for bankkontoutdrag er lastet opp og tilordningen er fullført, klikker du handlingen **Vis kart** for enheten.
8.  Enheten for bankkontoutdrag er en sammensatt enhet som består av fire separate enheter. Velg **BankStatementDocumentEntity** i listen, og klikk deretter handlingen **Vis kart**.
9.  Klikk **Ny** i kategorien **Transformasjoner**.
10. For serienummer 1 klikker du **Last opp fil** og velger **MT940TXT-to-MT940XML.xslt**-filen som du lagret tidligere.
11. Klikk **Ny**.
12. For serienummer 2 klikker du **Last opp fil** og velger **MT940XML-to-Reconciliation.xslt**-filen som du lagret tidligere. **Obs!** Transformeringsfiler er bygget for standardformatet. Siden banker ofte avviker fra dette formatet, må du kanskje oppdatere transformeringsfilen som skal tilordnes til bankkontoutdragsformatet. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. Klikk på **Ny**.
14. For serienummer 3 klikker du **Last opp fil** og velger **BankReconciliation-to-Composite.xslt**-filen som du lagret tidligere.
15. Klikk **Bruk transformasjoner**.

Når behandlingsgruppen for format er definert, er neste trinn å definere formatreglene for bankkontoutdrag for MT940 bankkontoutdrag.

1.  Gå til **Kontant- og bankbehandling** &gt; **Oppsett** &gt; **Oppsett for avansert bankavstemming** &gt; **Bankkontoutdragsformat**.
2.  Klikk på **Ny**.
3.  Angi et bankkontoutdragsformat, for eksempel **MT940**.
4.  Angi et navn for formatet.
5.  Sett feltet **Behandlingsgruppe** til gruppen som du definerte tidligere, for eksempel **MT940**.
6.  Sett **Filtype**-feltet til **TXT**.

Det siste trinnet er å aktivere avanserte bankavstemming og angi formatet for bankkontoutdrag på bankkontoen.

1.  Gå til **Kontant- og bankbehandling** &gt; **Bankkontoer**.
2.  Velg bankkontoen, og åpne den for å vise detaljene.
3.  I kategorien **Avstemming** setter du alternativet **Avanserte bankavstemmingen** til **Ja**.
4.  Når du blir bedt om å bekrefte valget og aktivere avanserte bankavstemming, klikker du **OK**.
5.  Sett feltet **Utdragsformat** til formatet som du opprettet tidligere, for eksempel **MT940**.

## <a name="set-up-the-import-of-bai2-bank-statements"></a>Definere import av BAI2-bankkontoutdrag
Først må du definere behandlingsgruppen for bankkontoutdrag for BAI2-bankkontoutdrag ved hjelp av rammeverket for dataenhet.

1.  Gå til **Arbeidsområder** &gt; **Databehandling**.
2.  Klikk på **Importer**.
3.  Angi et navn for formatet, for eksempel **BAI2**.
4.  Sett feltet **Kildedataformat** til **XML-element**.
5.  Sett feltet **Enhetsnavn** til **Bankkontoutdrag**.
6.  Hvis du vil laste opp de importerte filene, klikker du **Last opp**, og deretter går du til **SampleBankCompositeEntity.xml**-filen som du lagret tidligere.
7.  Når enheten for bankkontoutdrag er lastet opp og tilordningen er fullført, klikker du handlingen **Vis kart** for enheten.
8.  Enheten for bankkontoutdrag er en sammensatt enhet som består av fire separate enheter. Velg **BankStatementDocumentEntity** i listen, og klikk deretter handlingen **Vis kart**.
9.  Klikk **Ny** i kategorien **Transformasjoner**.
10. For serienummer 1 klikker du **Last opp fil** og velger **BAI2CSV-to-BAI2XML.xslt**-filen som du lagret tidligere.
11. Klikk **Ny**.
12. For serienummer 2 klikker du **Last opp fil** og velger **BAI2XML-to-Reconciliation.xslt**-filen som du lagret tidligere. **Obs!** Transformeringsfiler er bygget for standardformatet. Siden banker ofte avviker fra dette formatet, må du kanskje oppdatere transformeringsfilen som skal tilordnes til bankkontoutdragsformatet. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. Klikk på **Ny**.
14. For serienummer 3 klikker du **Last opp fil** og velger **BankReconciliation-to-Composite.xslt**-filen som du lagret tidligere.
15. Klikk **Bruk transformasjoner**.

Når behandlingsgruppen for format er definert, er neste trinn å definere formatreglene for bankkontoutdrag for BAI2 bankkontoutdrag.

1.  Gå til **Kontant- og bankbehandling** &gt; **Oppsett** &gt; **Oppsett for avansert bankavstemming** &gt; **Bankkontoutdragsformat**.
2.  Klikk på **Ny**.
3.  Angi et bankkontoutdragsformat, for eksempel **BAI2**.
4.  Angi et navn for formatet.
5.  Sett feltet **Behandlingsgruppe** til gruppen som du definerte tidligere, for eksempel **BAI2**.
6.  Sett **Filtype**-feltet til **TXT**.

Det siste trinnet er å aktivere avanserte bankavstemming og angi formatet for bankkontoutdrag på bankkontoen.

1.  Gå til **Kontant- og bankbehandling** &gt; **Bankkontoer**.
2.  Velg bankkontoen, og åpne den for å vise detaljene.
3.  I kategorien **Avstemming** setter du alternativet **Avanserte bankavstemmingen** til **Ja**.
4.  Når du blir bedt om å bekrefte valget og aktivere avanserte bankavstemming, klikker du **OK**.
5.  Sett feltet **Utdragsformat** til formatet som du opprettet tidligere, for eksempel **BAI2**.

## <a name="test-the-bank-statement-import"></a>Teste import av bankkontoutdrag
Det siste trinnet er å teste at du kan importere bankkontoutdraget.

1.  Gå til **Kontant- og bankbehandling** &gt; **Bankkontoer**.
2.  Velg bankkontoen som funksjonen Avanserte bankavstemming er aktivert for.
3.  I kategorien **Avstem** klikker du **Bankkontoutdrag**.
4.  På siden **Bankkontoutdrag** klikker du **Importer utdrag**.
5.  Sett **Bankkonto**-feltet til den valgte bankkontoen. Feltet **Utdragsformat** angis automatisk, basert på innstillingen i bankkontoen.
6.  Klikk **Bla gjennom**, og velg den elektroniske bankkontoutdragsfilen.
7.  Klikk **Last opp**.
8.  Klikk **OK**.

Hvis importen er vellykket, vises en melding om at utdraget ble importert. Hvis importen mislyktes, går du til arbeidsområdet **Databehandling** og delen **Jobblogg** for å finne jobben. Klikk **Utførelsesdetaljer** for jobben for å åpne siden **Utførelsessammendrag** , og klikk deretter **Vis utførelseslogg** for å vise importfeilene.




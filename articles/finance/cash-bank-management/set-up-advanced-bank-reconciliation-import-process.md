---
title: Definere importprosess for avansert bankavstemming
description: Funksjonen Avansert bankavstemming lar deg importere elektroniske bankkontoutdrag og automatisk avstemme dem med banktransaksjoner i Microsoft Dynamics 365 Finance. Denne artikkelen beskriver hvordan du definerer funksjonen for import av din bankkontoutdrag.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60195962e50817b4d85840a2464848db6e666f46
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716025"
---
# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Definer prosessen for avansert bankavstemmingsimport

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Denne funksjonaliteten blir avskrevet i september 2022, og nye brukere må bruke elektronisk rapportering. For mer informasjon, se [Definer avansert bankavstemmingsimport ved hjelp av elektronisk rapportering](../accounts-payable/import-bai2-er.md).


Funksjonen Avansert bankavstemming lar deg importere elektroniske bankkontoutdrag og automatisk avstemme dem med banktransaksjoner i Dynamics 365 Finance. Denne artikkelen beskriver hvordan du definerer funksjonen for import av din bankkontoutdrag. 

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
Nedenfor følger eksempler på definisjonene av tekniske oppsett for avansert bankavstemmingsimportfil og tre tilknyttede filer med eksempler på bankkontoutdrag: [Importer fileksempler](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Definisjon av teknisk oppsett                             | Fil med bankkontoutdragseksempler          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |



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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

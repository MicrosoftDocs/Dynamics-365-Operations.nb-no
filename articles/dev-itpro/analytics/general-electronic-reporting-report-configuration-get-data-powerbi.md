---
title: "Konfigurere elektronisk rapportering for å hente data til Power BI"
description: "Dette emnet forklarer hvordan du kan bruke konfigurasjoner for elektronisk rapportering (ER) for å ordne overføring av data fra din forekomst av Finance and Operations til Power BI-tjenester."
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 45717bc1a7093c0282d214fc4ce5fdf153bb14a1
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="configure-electronic-reporting-to-pull-data-into-power-bi"></a>Konfigurere elektronisk rapportering for å hente data til Power BI

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du kan bruke konfigurasjoner for elektronisk rapportering (ER) for å ordne overføring av data fra din forekomst av Finance and Operations til Power BI-tjenester. Dette emnet bruker for eksempel Intrastat-transaksjoner som forretningsdata som må overføres. Kartvisningen for Power BI bruker disse Intrastat-transaksjonsdataene til å presentere en visning for analyse av firmaets aktiviteter for import og eksport i Power BI-rapporten.

<a name="overview"></a>Oversikt
--------

Microsoft Power BI er en samling av programvaretjenester, apper og koblinger som arbeider sammen for å aktivere eksterne datakilder til sammenhengende, visuelt altoppslukende og interaktive innsikter. Elektronisk rapportering (ER) lar brukere av Microsoft Dynamics 365 for Finance and Operations konfigurere datakilder og ordne dataoverføring fra Finance and Operations til Power BI. Dataene overføres som filer i formatet OpenXML-regneark (Microsoft Excel-arbeidsbokfil). De overførte filene lagres på en Microsoft SharePoint-server som er konfigurert for dette formålet. De lagrede filene brukes i Power BI til å opprette rapporter som inneholder visninger (tabeller, diagrammer, kart og så videre). Power BI-rapporter deles med Power BI-brukere, og det er tilgang til dem i Power BI-instrumentbord og på Finance and Operations-sider. Dette emnet forklarer følgende oppgaver:

-   Konfigurer Finance og Operations.
-   Klargjøre ER-formatkonfigurasjonen for å hente data fra Finance and Operations.
-   Konfigurer ER-miljøet for å overføre data til Power BI.
-   Bruke overførte data til å opprette en Power BI-rapport.
-   Gjør Power BI-rapporten tilgjengelig i Finance and Operations.

## <a name="prerequisites"></a>Forutsetninger
Hvis du vil fullføre eksemplet i dette emnet, må du ha følgende tilgang:

-   Tilgang til Finance and Operations for én av følgende roller:
    -   Utvikler av elektronisk rapportering
    -   Funksjonell konsulent for elektronisk rapportering
    -   Systemansvarlig
-   Tilgang til SharePoint-serveren som er konfigurert for bruk med Finance and Operations
-   Tilgang til Power BI-rammeverket

## <a name="configure-document-management-parameters"></a>Konfigurere parametere for dokumentstyring
1.  På siden **Parametere for dokumentstyring** konfigurerer du tilgang til SharePoint-serveren som skal brukes i firmaet som du er logget på (DEMF-firmaet i dette eksemplet).
2.  Test tilkoblingen til SharePoint-serveren for å være sikker på at du har fått tilgang. [![Siden Parametere for dokumentstyring](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)
3.  Åpne det konfigurerte SharePoint-området. Opprett en ny mappe hvor ER lagrer Excel-filer som har forretningsdataene som Power BI-rapportene krever som en kilde for Power BI-datasett.
4.  På **Dokumenttyper**-siden i Finance and Operations kan du opprette en ny dokumenttype som skal brukes for å få tilgang til SharePoint-mappen du nettopp opprettet. Angi **Fil** i **Gruppe**-feltet, og **SharePoint** i **Plassering**-feltet, og angi deretter adressen til SharePoint-mappen. [![Siden Dokumenttyper](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>Konfigurere ER-parametere
1.  I arbeidsområdet **Elektronisk rapportering** klikker du koblingen **Parametere for elektronisk rapportering**.
2.  I kategorien **Vedlegg** velger du dokumenttypen **Fil** for alle feltene.
3.  I arbeidsområdet **Elektronisk rapportering** aktiverer du den nødvendige leverandøren ved å klikke **Angi som aktiv**. Hvis du vil ha mer informasjon, kan du spille av oppgaveveiledningen **ER Velge tjenesteleverandør**.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>Bruke en ER-datamodell som datakilde
Du må ha en ER-datamodell som kilde for forretningsdata som skal brukes i Power BI-rapporter. Denne datamodellen lastes fra databasen for ER-konfigurasjoner. Hvis du vil ha mer informasjon, kan du se [Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services](download-electronic-reporting-configuration-lcs.md) eller spille av oppgaveveiledningen **ER Importere en konfigurasjon fra Lifecycle Services**. Velg **Intrastat** som datamodellen som lastes opp fra det valgte repositoriet for ER-konfigurasjoner. (I dette eksemplet brukes versjon 1 av modellen.) Du kan deretter få tilgang til **Intrastat** ER-modellkonfigurasjonen på **Konfigurasjoner**-siden. [![Siden Konfigurasjoner](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>Utforme en ER-formatkonfigurasjon
Du må opprette en ny ER-formatkonfigurasjon som bruker **Intrastat**-datamodellen som kilde for forretningsdata. Denne formatkonfigurasjonen må generere utdataresultatene som elektroniske dokumenter i OpenXML-format (Excel-fil). Hvis du vil ha mer informasjon, kan du spille av oppgaveveiledningen **ER Opprette en konfigurasjon for rapporter i OPENXML-format**. Gi navn til den nye konfigurasjonen **Importer/eksporter aktiviteter**, som vist i illustrasjonen nedenfor. Bruk Excel-filen [ER data - Import- og eksportdetaljer](https://go.microsoft.com/fwlink/?linkid=845208) som mal når du utformer ER-formatet. (Hvis du vil ha informasjon om hvordan du importerer en formatmal, spiller du av oppgaveveiledningen). [![Konfigurasjonen Importer/eksporter aktiviteter](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png) Følg fremgangsmåten nedenfor hvis du vil endre formatkonfigurasjonen **Importer/eksporter aktiviteter**.

1.  Klikk **Utforming**.
2.  I kategorien **Format** gir du navn til filelementet for dette formatet **Excel-utdatafil**. [![Elementet Excel-utdatafil](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)
3.  I kategorien **Tilordning** angir du navnet på Excel-filen som blir generert når dette formatet kjøres. Konfigurer det beslektede uttrykket for å returnere verdien **Import- og eksportdetaljer** (XLSX-filtypen legges til automatisk). [![Formatutforming](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)
4.  Legg til et nytt dataelement for kilden for dette formatet. (Denne opplistingen er nødvendig for ytterligere databinding.)
    1.  Gi navn til datakilden **direction\_enum**.
    2.  Velg **Datamodellopplisting** som datakildetype.
    3.  Se datamodellopplistingen **Retning**.

    [![direction\_enum](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)
5.  Fullføre bindingen av elementene i **Intrastat**-datamodellen og elementer som er utformet for format, som vist i illustrasjonen nedenfor. [![Fullføring av bindingen](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Når det er kjørt, genererer ER-formatet utdataresultatet i Excel-format. Den sender detaljene for Intrastat-transaksjonene til utdataresultatet, og skiller dem som transaksjoner som beskriver importaktiviteter eller eksportaktiviteter. Klikk **Kjør** for å teste det nye ER-formatet for Intrastat-transaksjoner på **Intrastat**-siden (**Mva** &gt; **Deklarasjoner** &gt; **Utenrikshandel** &gt; **Intrastat**). [![Siden Intrastat](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png) Følgende utdataresultat blir generert. Filen får navnet **Import- og eksportdetaljer.xlsx**, slik du angav i formatinnstillingene. [![Import- og eksportdetaljer.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>Konfigurere ER-målet
Du må konfigurere ER-rammeverket for å sende utdataresultatet av den nye ER-formatkonfigurasjonen på en spesiell måte.

-   Utdataresultatet må sendes til mappen for den valgte SharePoint-serveren.
-   Hver kjøring av formatkonfigurasjonen må opprette en ny versjon av samme Excel-fil.

På siden **Elektronisk rapportering** (**Organisasjonsstyring** &gt; **Elektronisk rapportering**) klikker du elementet **Mål for elektronisk rapportering** og legger til et nytt mål. I **Referanse**-feltet velger du formatkonfigurasjonen **Importer/eksporter aktiviteter** som du opprettet tidligere. Følg denne fremgangsmåten for å legge til en ny post for filmål for referansen.

1.  I **Navn**-feltet angir du tittelen for filmålet.
2.  I **Filnavn**-feltet velger du navnet **Excel-utdatafil** for Excel-filformatkomponenten.

Klikk **innstillinger** for den nye målposten. Følg deretter fremgangsmåten nedenfor i dialogboksen **Innstillinger for mål**.

1.  I kategorien **Power BI** setter du **Aktivert**-alternativet til **Ja**.
2.  I **SharePoint**-feltet velger du dokumenttypen **Delt** som du opprettet tidligere.

## <a name="schedule-execution-of-the-configured-er-format"></a>Planlegge kjøring av det konfigurerte ER-formatet
1. I trekonfigurasjonene på **Konfigurasjoner**-siden (**Organisasjonsstyring** &gt; **Elektronisk rapportering** &gt; **Konfigurasjoner**) velger du konfigurasjonen **Importer/eksporter aktiviteter** som du opprettet tidligere. 
2. Endre statusen til versjon 1.1 fra **Utkast** til **Fullført** for å gjøre dette formatet tilgjengelig for bruk. [![Siden Konfigurasjoner](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png) 
3. Velg den fullførte versjonen av konfigurasjonen **Importer/eksporter aktiviteter**, og klikk deretter **Kjør**. Legg merke til at det konfigurerte målet blir brukt til utdataresultatet som genereres i Excel-format. 
4. Sett alternativet **Satsvis behandling** til **Ja** for å kjøre denne rapporten i uovervåket modus. 
5. Klikk **Regelmessighet** for å planlegge nødvendige gjentakelse for den satsvise kjøringen. Gjentakelsen definerer hvor ofte de oppdaterte dataene overføres fra Finance and Operations til Power BI. [![Dialogboksen Parametere for elektronisk rapport](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png) 
6. Når den er konfigurert, finner du ER-rapportkjøringsjobben på siden **Satsvise jobber** (**Systemadministrasjon &gt; Forespørsler &gt; Satsvise jobber**). [![Siden Satsvise jobber](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png) 
7. Når denne jobben kjøres for første gang, opprettes en ny Excel-fil med det konfigurerte navnet i den valgte SharePoint-mappen i målet. Hver gang jobben kjøres, opprettes en ny versjon av denne Excel-filen i målet. [![Ny versjon av Excel-filen](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>Opprette et Power BI-datasett ved hjelp av utdataresultatet av ER-formatet
1. Logge på Power BI, og åpne en eksisterende Power BI-gruppen (arbeidsområde) eller opprett en ny gruppe. Klikk **Legg til** under **Filer** under **Importer eller koble til data**, eller klikk plusstegnet (**+**) ved siden av **Datasett** i ruten til venstre. [![Opprette et datasett](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png) 
2. Velg alternativet **SharePoint – gruppeområder**, og skriv inn banen til SharePoint-serveren du bruker (`https://ax7partner.litware.com` i vårt eksempel). 
3. Gå til mappen **/Shared Documents/GER data/PowerBI**, og velg Excel-filen du opprettet som datakilde for det nye Power BI-datasettet. [![Velge Excel-filen](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png) 
4. Klikk **Koble til**, og klikk deretter **Importer**. Det opprettes et nytt datasett som er basert på den valgte Excel-filen. Datasettet kan også legges til automatisk i det nyopprettede instrumentbordet. [![Datasett på instrumentbordet](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png) 
5. Konfigurer oppdateringsplanen for datasettet for å fremtvinge en regelmessig oppdatering. Periodiske oppdateringer aktiverer bruk av nye forretningsdata som kommer fra Finance and Operations via regelmessig kjøring av ER-rapporten gjennom nye versjoner av Excel-filen som opprettes på SharePoint-serveren.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Opprette en Power BI-rapport ved hjelp av det nye datasettet
1. Klikk på Power BI-datasettet **Import- og eksportdetaljer** som du opprettet. 
2. Konfigurer visningen. Velg for eksempel visningen **Fylt kart**, og konfigurere den på følgende måte:
   -   Tilordne **Opprinnelsesland**-datasettfeltet til **Plassering**-feltet for kartvisningen.
   -   Tilordne **Mengde**-datasettfeltet til **Fargemetning**-feltet for kartvisningen.
   -   Legg til datasettfeltene **Aktivitet** og **År** i **Filtre**-feltsamlingen for kartvisningen.

3. Lagre Power BI-rapporten som **Rapport for import- og eksportdetaljer**. [![Rapporten Import- og eksportdetaljer](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png) Vær oppmerksom på at kartet viser landene/områdene som er nevnt i Excel-filen (Østerrike og Sveits i dette eksemplet). Disse landene/områdene er fargelagt for å vise størrelsen på andelen av fakturerte beløp for hver av dem. 
4. Oppdater listen over Intrastat-transaksjoner. Eksporttransaksjonen som stammer fra Italia legges til. [![Listen Intrastat-transaksjoner](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png) 
5. Vent til den neste planlagte kjøringen av ER-rapporten og den neste planlagte oppdateringen av Power BI-datasettet. Deretter kan du se gjennom Power BI-rapporten (velg å bare vise importerte transaksjoner). Det oppdaterte kartet viser nå Italia. [![Oppdatert kart](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-finance-and-operations"></a>Gjør Power BI-rapporten tilgjengelig i Finance and Operations.
Konfigurer integrasjonen mellom Finance and Operations og Power BI. Hvis du vil ha mer informasjon, kan du se [Konfigurere Power BI-integrering for arbeidsområder](configure-power-bi-integration.md). 

1. På arbeidsområdesiden **Elektronisk rapportering** som støtter Power BI-integrering (**Organisasjonsstyring** &gt; **Arbeidsområder** &gt; **Arbeidsområde for elektronisk rapportering**), klikker du **Alternativer** &gt; **Åpne rapportkatalog**. 
2. Velg Power BI-rapporten **Import- og eksportdetaljer** som du opprettet, for å vise denne rapporten som et handlingselement på den valgte siden. 
3. Klikk handlingselementet for å åpne Finance and Operations-siden som viser rapporten som du utformet i Power BI. [![Rapporten Import- og eksportdetaljer](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

<a name="additional-resources"></a>Tilleggsressurser
--------

[Mål for elektronisk rapportering](electronic-reporting-destinations.md)

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)





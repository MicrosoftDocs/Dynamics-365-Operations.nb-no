---
title: "Definere elektronisk rapportering for å gi strøm BI med data fra Dynamics 365 for operasjoner"
description: "Dette emnet forklarer hvordan du kan bruke konfigurasjoner for elektronisk rapportering (ER) for å ordne overføring av data fra din forekomst av Dynamics 365 for Operations til Power BI-tjenester. Dette emnet bruker for eksempel Intrastat-transaksjoner som forretningsdata som må overføres. Kartvisningen for Power BI bruker disse Intrastat-transaksjonsdataene til å presentere en visning for analyse av firmaets aktiviteter for import og eksport i Power BI-rapporten."
author: kfend
manager: AnnBe
ms.date: 2016-10-31 13 - 22 - 29
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ed0192c44b6d7e88120c64e539ebb0ac3b379831
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-electronic-reporting-to-provide-power-bi-with-data-from-dynamics-365-for-operations"></a>Definere elektronisk rapportering for å gi strøm BI med data fra Dynamics 365 for operasjoner

Dette emnet forklarer hvordan du kan bruke konfigurasjoner for elektronisk rapportering (ER) for å ordne overføring av data fra din forekomst av Dynamics 365 for Operations til Power BI-tjenester. Dette emnet bruker for eksempel Intrastat-transaksjoner som forretningsdata som må overføres. Kartvisningen for Power BI bruker disse Intrastat-transaksjonsdataene til å presentere en visning for analyse av firmaets aktiviteter for import og eksport i Power BI-rapporten.

<a name="overview"></a>Oversikt
--------

Microsoft Power BI er en samling av programvaretjenester, apper og koblinger som arbeider sammen for å aktivere eksterne datakilder til sammenhengende, visuelt altoppslukende og interaktive innsikter. Elektronisk rapportering (ER) lar brukere av Microsoft Dynamics 365 for Operations konfigurere datakilder og ordne dataoverføring fra Dynamics 365 for Operations til Power BI.. Dataene overføres som filer i formatet OpenXML-regneark (Microsoft Excel-arbeidsbokfil). De overførte filene lagres på en Microsoft SharePoint-server som er konfigurert for dette formålet. De lagrede filene brukes i Power BI til å opprette rapporter som inneholder visninger (tabeller, diagrammer, kart og så videre). Power BI-rapporter deles med Power BI-brukere, og det er tilgang til dem i Power BI-instrumentbord og på Dynamics 365 for Operations-sider. Dette emnet forklarer følgende oppgaver:

-   Konfigurere Dynamics 365 for Operations.
-   Klargjøre ER-formatkonfigurasjonen for å hente data fra Dynamics 365 for Operations.
-   Konfigurer ER-miljøet for å overføre data til Power BI.
-   Bruke overførte data til å opprette en Power BI-rapport.
-   Gjør Power BI-rapporten tilgjengelig i Dynamics 365 for Operations.

## <a name="prerequisites"></a>Forutsetninger
Hvis du vil fullføre eksemplet i dette emnet, må du ha følgende tilgang:

-   Tilgang til Dynamics 365 for Operations for én av følgende roller:
    -   Utvikler av elektronisk rapportering
    -   Funksjonell konsulent for elektronisk rapportering
    -   Systemansvarlig
-   Tilgang til SharePoint-serveren som er konfigurert for bruk med Dynamics 365 for Operations
-   Tilgang til Power BI-rammeverket

## <a name="configure-document-management-parameters"></a>Konfigurere parametere for dokumentstyring
1.  På siden **Parametere for dokumentstyring** konfigurerer du tilgang til SharePoint-serveren som skal brukes i firmaet som du er logget på (DEMF-firmaet i dette eksemplet).
2.  Test tilkoblingen til SharePoint-serveren for å være sikker på at du har fått tilgang. [![Siden parametere for dokumentbehandling](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)
3.  Åpne det konfigurerte SharePoint-området. Opprett en ny mappe hvor ER lagrer Excel-filer som har forretningsdataene som Power BI-rapportene krever som en kilde for Power BI-datasett.
4.  På **Dokumenttyper**-siden i Dynamics 365 for Operations kan du opprette en ny dokumenttype som skal brukes for å få tilgang til SharePoint-mappen du nettopp opprettet. Angi **Fil** i **Gruppe**-feltet, og **SharePoint** i **Plassering**-feltet, og angi deretter adressen til SharePoint-mappen. [![Typer dokumentside](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>Konfigurere ER-parametere
1.  I arbeidsområdet **Elektronisk rapportering** klikker du koblingen **Parametere for elektronisk rapportering**.
2.  I kategorien **Vedlegg** velger du dokumenttypen **Fil** for alle feltene.
3.  I arbeidsområdet **Elektronisk rapportering** aktiverer du den nødvendige leverandøren ved å klikke **Angi som aktiv**. Hvis du vil ha mer informasjon, kan du spille av oppgaveveiledningen **ER Velge tjenesteleverandør**.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>Bruke en ER-datamodell som datakilde
Du må ha en ER-datamodell som kilde for forretningsdata som skal brukes i Power BI-rapporter. Denne datamodellen lastes fra databasen for ER-konfigurasjoner. Hvis du vil ha mer informasjon, kan du se [Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services](download-electronic-reporting-configuration-lcs.md) eller spille av oppgaveveiledningen **ER Importere en konfigurasjon fra Lifecycle Services**. Velg **Intrastat **som datamodellen som lastes opp fra det valgte repositoriet for ER-konfigurasjoner. (I dette eksemplet versjon 1 av modellen brukes.) Du kan deretter få tilgang til **Intrastat** ER konfigurasjon på den **konfigurasjoner** siden. [![Konfigurasjoner-siden](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>Utforme en ER-formatkonfigurasjon
Du må opprette en ny ER-formatkonfigurasjon som bruker **Intrastat**-datamodellen som kilde for forretningsdata. Denne formatkonfigurasjonen må generere utdataresultatene som elektroniske dokumenter i OpenXML-format (Excel-fil). Hvis du vil ha mer informasjon, kan du spille av oppgaveveiledningen **ER Opprette en konfigurasjon for rapporter i OPENXML-format**. Gi navn til den nye konfigurasjonen **Importer/eksporter aktiviteter**, som vist i illustrasjonen nedenfor. Bruk Excel-filen [ER data - import and export details](https://go.microsoft.com/fwlink/?linkid=845208) som mal når du utformer ER-formatet. (Du finner informasjon om hvordan du importerer en mal for format, spille av TV-guiden for oppgaven). [![Importer / Eksporter konfigurasjon av aktiviteter](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png) til å endre det **Import / export aktiviteter** format konfigurasjonen, følger du denne fremgangsmåten.

1.  Klikk **Utforming**.
2.  I kategorien **Format** gir du navn til filelementet for dette formatet **Excel-utdatafil**. [![Excel output-fil elementet](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)
3.  I kategorien **Tilordning** angir du navnet på Excel-filen som blir generert når dette formatet kjøres. Konfigurer det beslektede uttrykket for å returnere verdien **Import- og eksportdetaljer** (XLSX-filtypen legges til automatisk). [![Format designer](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)
4.  Legg til et nytt dataelement for kilden for dette formatet. (Denne opplistingen er nødvendig for ytterligere databinding.)
    1.  Gi navn til datakilden **retning\_enum**.
    2.  Velg **Datamodellopplisting** som datakildetype.
    3.  Se datamodellopplistingen **Retning**.

    [![retning\_enum](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)
5.  Fullføre bindingen av elementene i **Intrastat**-datamodellen og elementer som er utformet for format, som vist i illustrasjonen nedenfor. [![Fullfører bindingen](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Når det er kjørt, genererer ER-formatet utdataresultatet i Excel-format. Den sender detaljene for Intrastat-transaksjonene til utdataresultatet, og skiller dem som transaksjoner som beskriver importaktiviteter eller eksportaktiviteter. Klikk **kjører** til å teste det nye formatet for ER liste over Intrastat-transaksjoner på den **Intrastat** side (**mva**&gt;**deklarasjoner**&gt;**Utenrikshandel**&gt;**Intrastat**). [![Siden Intrastat](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png) følgende utdata resultatet blir generert. Filen får navnet **Import- og eksportdetaljer.xlsx**, slik du angav i formatinnstillingene. [![Importere og eksportere details.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>Konfigurere ER-målet
Du må konfigurere ER-rammeverket for å sende utdataresultatet av den nye ER-formatkonfigurasjonen på en spesiell måte.

-   Utdataresultatet må sendes til mappen for den valgte SharePoint-serveren.
-   Hver kjøring av formatkonfigurasjonen må opprette en ny versjon av samme Excel-fil.

På den **elektronisk rapportering** side (**organisasjonsadministrasjon**&gt;**elektronisk rapportering**), klikker du på **elektronisk rapportering mål** element, og legge til et nytt mål. I **Referanse**-feltet velger du formatkonfigurasjonen **Importer/eksporter aktiviteter** som du opprettet tidligere. Følg denne fremgangsmåten for å legge til en ny post for filmål for referansen.

1.  I **Navn**-feltet angir du tittelen for filmålet.
2.  I **Filnavn**-feltet velger du navnet **Excel-utdatafil** for Excel-filformatkomponenten.

Klikk **innstillinger** for den nye målposten. Følg deretter fremgangsmåten nedenfor i dialogboksen **Innstillinger for mål**.

1.  I kategorien **Power BI** setter du **Aktivert**-alternativet til **Ja**.
2.  I **SharePoint**-feltet velger du dokumenttypen **Delt** som du opprettet tidligere.

## <a name="schedule-execution-of-the-configured-er-format"></a>Planlegge kjøring av det konfigurerte ER-formatet
På den **konfigurasjoner** siden (**organisasjonsadministrasjon**&gt;**elektronisk rapportering**&gt;**konfigurasjoner**), i konfigurasjoner-treet, velger du den **Import / eksport aktiviteter** konfigurasjon som du opprettet tidligere. Endre statusen til versjon 1.1 fra **Utkast** til **Fullført** for å gjøre dette formatet tilgjengelig for bruk. [![Konfigurasjoner siden](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png) velger du den ferdige versjonen av den **Import / eksport aktiviteter** konfigurasjonen, og klikk deretter **kjører**. Legg merke til at det konfigurerte målet blir brukt til utdataresultatet som genereres i Excel-format. Sett alternativet **Satsvis behandling** til **Ja** for å kjøre denne rapporten i uovervåket modus. Klikk **Regelmessighet** for å planlegge nødvendige gjentakelse for den satsvise kjøringen. Gjentakelsen definerer hvor ofte de oppdaterte dataene overføres fra Dynamics 365 for Operations til Power BI. [![Dialogboksen elektronisk rapport](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png) etter at den er konfigurert, kan du finne ER rapporten kjøring av jobben på den **kjørslene** side (**systemadministrasjon &gt;forespørsler &gt;kjørslene**). [![Satsvise jobber side](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png) når denne jobben kjøres for første gang, målet oppretter en ny Excel-fil med navnet på konfigurerte i den valgte SharePoint-mappen. Hver gang jobben kjøres, opprettes en ny versjon av denne Excel-filen i målet. [![Ny versjon av Excel-filen](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>Opprette et Power BI-datasett ved hjelp av utdataresultatet av ER-formatet
Logge på Power BI, og åpne en eksisterende Power BI-gruppen (arbeidsområde) eller opprett en ny gruppe. Enten klikke **Legg til** under **filer** i den **importere eller koble til Data** -delen, eller klikk plusstegnet (**+**) siden **Datasets** i den venstre ruten. [![Oppretter et dataset](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png) velger du **SharePoint-gruppeområder** alternativet, og skriv deretter inn banen til SharePoint-serveren du bruker (**https://ax7partner.spoppe.com** i vårt eksempel). Gå deretter til mappen **/Shared Documents/GER data/PowerBI**, og velg Excel-filen du opprettet som datakilde for det nye Power BI-datasettet. [![Valg av Excel-filen](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png) klikker du **koble til**, og klikk deretter **Import**. Det opprettes et nytt datasett som er basert på den valgte Excel-filen. Datasettet kan også legges til automatisk i det nyopprettede instrumentbordet. [![DataSet på instrumentbordet](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png) konfigurere Oppdater tidsplanen å tvinge en periodisk oppdatering for dataset. Periodiske oppdateringer aktiverer bruk av nye forretningsdata som kommer fra Dynamics 365 for Operations via regelmessig kjøring av ER-rapporten gjennom nye versjoner av Excel-filen som opprettes på SharePoint-serveren.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Opprette en Power BI-rapport ved hjelp av det nye datasettet
Hvis du vil opprette en ny Power BI-rapport, klikker du Power BI-datasettet **Import- og eksportdetaljer** som du opprettet. Konfigurer deretter visningen. Velg for eksempel visningen **Fylt kart**, og konfigurere den på følgende måte:

-   Tilordne **Opprinnelsesland**-datasettfeltet til **Plassering**-feltet for kartvisningen.
-   Tilordne **Mengde**-datasettfeltet til **Fargemetning**-feltet for kartvisningen.
-   Legg til datasettfeltene **Aktivitet** og **År** i **Filtre**-feltsamlingen for kartvisningen.

Lagre Power BI-rapporten som **Rapport for import- og eksportdetaljer**. [![Importer og Eksporter rapport om](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png) Vær oppmerksom på at kartet viser landene/regionene som er nevnt i Excel-filen (Østerrike og Sveits i dette eksemplet). Disse landene/områdene er fargelagt for å vise størrelsen på andelen av fakturerte beløp for hver av dem. Oppdater listen over Intrastat-transaksjoner. Eksporttransaksjonen som stammer fra Italia legges til. [![Intrastat-transaksjoner listen](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png) venter på neste planlagte kjøring av rapporten ER og neste planlagte oppdatering av strømmen BI dataset. Deretter kan du se gjennom Power BI-rapporten (velg å bare vise importerte transaksjoner). Det oppdaterte kartet viser nå Italia. [![Oppdaterte kart](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-dynamics-365-for-operations"></a>Gå til Power BI-rapporter i Dynamics 365 for Operations
Konfigurer integrasjonen mellom Dynamics 365 for Operations og Power BI. Hvis du vil ha mer informasjon, kan du se [Konfigurere Power BI-integrering for arbeidsområder](configure-power-bi-integration.md). På den **elektronisk rapportering** arbeidsområde-side som støtter strømmen BI-integrasjon (**organisasjonsadministrasjon**&gt;**arbeidsområder**&gt;**elektronisk rapportering arbeidsområde**), klikker du **alternativer**&gt;**åpne rapporten katalog**. Velg Power BI-rapporten **Import- og eksportdetaljer** som du opprettet, for å vise denne rapporten som et handlingselement på den valgte siden. Klikk handlingselementet for å åpne Dynamics 365 for Operations-siden som viser rapporten som du utformet i Power BI. [![Detaljrapport for import og eksport](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

<a name="see-also"></a>Se også
--------

[Mål for elektronisk rapportering](electronic-reporting-destinations.md)

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)



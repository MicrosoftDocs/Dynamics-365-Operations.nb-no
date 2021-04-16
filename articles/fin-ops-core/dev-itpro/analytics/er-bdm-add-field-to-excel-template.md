---
title: Legge til nye felt i en forretningsdokumentmal i Microsoft Excel
description: Dette emnet inneholder informasjon om hvordan du legger til nye felt i en forretningsdokumentmal i Microsoft Excel ved hjelp av funksjonen for administrasjon av forretningsdokumenter.
author: NickSelin
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 991fe4ea56a2726c5df835cfc90a390cef2d5df5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751136"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a>Legge til nye felt i en forretningsdokumentmal i Microsoft Excel

[!include[banner](../includes/banner.md)]

Du kan legge til nye felt i en mal som brukes til å generere forretningsdokumenter i Microsoft Excel-format. Disse feltene kan legges til som plassholdere som brukes til å fylle genererte dokumenter med nødvendig informasjon fra programmet. For hvert felt du legger til, kan du også angi en binding til datakildene for å angi hvilke programdata som skal angis i feltet når malen brukes til å generere forretningsdokumenter.

Hvis du vil vite mer om denne funksjonen, kan du fullføre eksemplet i dette emnet. Dette eksemplet viser hvordan du oppdaterer en mal for å fylle ut feltene i skjemaer for fritekstfaktura som genereres.

## <a name="configure-business-document-management-to-edit-templates"></a>Konfigurere administrasjon av forretningsdokument til å redigere maler

Fordi Business Document Management (BDM) er bygd på toppen av rammeverket [Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md), må du konfigurere de nødvendige ER- og BDM-parameterne før du kan begynne å arbeide med BDM.

1.  Logg deg på forekomsten av Microsoft Dynamics 365 Finance som systemadministrator.
2.  Fullfør følgende trinn i eksemplet i [Oversikt over administrasjon av forretningsdokument](er-business-document-management.md):

    1.  Konfigurer ER-parametere.
    2.  Slå på BDM.

Du kan nå begynne å bruke BDM til å redigere maler for forretningsdokumenter.

## <a name="import-er-solutions-that-contain-a-template"></a>Importere ER-løsninger som inneholder en mal

Eksemplet i denne fremgangsmåten bruker løsningen offisielt publisert for ER. Du må importere ER-konfigurasjonene av denne løsningen til den gjeldende forekomsten av Finance.

ER-formatkonfigurasjonen **Fritekstfaktura (Excel)** for denne løsningen inneholder malen for forretningsdokumenter i Excel-format som kan redigeres ved hjelp av BDM. Importer den nyeste versjonen av denne ER-formatkonfigurasjonen fra Microsoft Dynamics Lifecycle Service (LCS). De tilsvarende tilordningskonfigurasjonene for ER-datamodell og ER-modell blir importert automatisk.

Hvis du vil ha mer informasjon om å importere ER-konfigurasjoner, kan du se [Administrere livssyklus til konfigurasjoner for elektronisk rapportering (ER)](general-electronic-reporting-manage-configuration-lifecycle.md)

![Siden Delt LCS-aktivabibliotek](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a>Rediger malen for ER-løsning

1.  Logg på som en bruker med tilgang til arbeidsområdet for **administrasjon av forretningsdokument**.
2.  Åpne arbeidsområdet for **administrasjon av forretningsdokument**.

    ![Arbeidsområdet Administrasjon av forretningsdokument](./media/BDM-AddFldExcel-Workspace.png)

3.  I rutenettet velger du malen **Fritekstfaktura (Excel)**.
4.  Velg **Ny mal** i den høyre ruten for å opprette en ny mal som er basert på den valgte malen.
5.  I **Tittel**-feltet angir du **Fritekstfaktura (Excel) Contoso** som tittel for den nye malen.
6.  Velg **OK** for å bekrefte starten på redigeringsprosessen.

Siden for BDM-malredigering vises. Du kan bruke Microsoft 365 til å redigere den valgte malen på nettet i den innebygde kontrollen.

![Siden for BDM-malredigering](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a>Legg til etiketten for et nytt felt i malen

1.  Merk av for **Overskrifter og støttelinjer** for den redigerbare Excel-malen i **Vis**-kategorien i Excel-båndet på siden for BDM-malredigering.

    ![Avmerkingsbokser for overskrifter og støttelinjer merket av](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  Merk cellene **E8:F8**.
3.  På Excel-båndet i kategorien **Hjem** velger du **Slå sammen og sentrer** for å slå samme de merkede cellene i en ny sammenslått **E8:F8**-celle.
4.  I den sammenslåtte cellen **E8:F8** skriver du **URL-adresse**.
5.  Merk sammenslått celle **E7:F7**, velg **Kopier format**, og velg deretter sammenslått celle **E8:F8** for å formatere den på samme måte som den sammenslåtte cellen **E7:F7**.

    ![Ny feltetikett lagt til i malen](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a>Formatere malen for å reservere plass for et nytt felt

1.  Velg sammenslått celle **GG8:H8** siden for BDM-malredigering.
2.  På Excel-båndet i kategorien **Hjem** velger du **Slå sammen og sentrer** for å slå samme de merkede cellene i en ny sammenslått **G8:H8**-celle.
3.  Merk sammenslått celle **G7:H7**, velg **Kopier format**, og velg deretter sammenslått celle **G8:H8** for å formatere den på samme måte som den sammenslåtte cellen **G7:H7**.

    ![Reservert plass for det nye feltet](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  I **Navn**-boksen velger du **CompanyInfo**.

    **CompanyInfo**-området for gjeldende Excel-mal inneholder alle feltene som brukes til å fylle hodet i en generert rapport med detaljene i det gjeldende firmaet som selgerpart.

    ![CompanyInfo-område valgt](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a>Legg til et nytt felt i malen

1.  Velg **Vis format** i handlingruten på siden **BDM-malredigering**.
2.  Velg **Legg til** i **Malstruktur**-ruten.

    > [!NOTE]
    > Du må justere delen av malen du vil bruke som et nytt felt. Du har allerede gjort denne justeringen ved å formatere sammenslått celle **G8:H8**.

    ![Legge til et nytt felt i malen](./media/BDM-AddFldExcel-AddCell.png)

3.  Velg **Excel\celle** for å legge til et nytt felt som en celle i malen.

    Du kan velge **Excel\Område** hvis du vil legge til et nytt område i malen. Området som skrives inn, kan inneholde flere celler. Du kan legge til disse cellene senere.
    
    Legg merke til at **CompanyInfo**-malkomponenten automatisk blir valgt i **Malstruktur**-ruten, fordi den er den mest egnede overordnede komponenten i den gjeldende malstrukturen for feltet du legger til.
    
4.  I feltet **Excel-område** angir du **CompanyURL_Value**.
5.  Velg **OK**.

    ![CompanyURL_Value-felt lagt til i malstrukturen](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  I **Malstruktur**-ruten velger du ellipseknappen (...), og velger deretter **Vis bindinger**.

    ![Vis bindinger valgt](./media/BDM-AddFldExcel-ShowBindings.png)

    **Malstruktur**-ruten viser nå datakildene som er tilgjengelige i det underliggende ER-formatet.

7.  Velg **CompanyInfo_Value** som feltet du vil binde til en datakilde av det underliggende ER-formatet.
8.  I delen **Datakilder** i ruten **Malstruktur** utvider du **Modell \> InvoiceBase \> CompanyInfo**.
9.  Under **CompanyInfo** velger du **WebsiteURI**-elementet.

    ![WebsiteURI-element valgt](./media/BDM-AddFldExcel-BindURL.png)

10. Velg **Bind**.
11. I ruten **Malstruktur** velger du **Lagre**, og lukker deretter siden for BDM-malredigering.

I arbeidsområdet **Administrasjon av forretningsdokument** viser **Mal**-kategorien i ruten til høyre den oppdaterte malen. I rutenettet legger du merke til at **Status**-feltet for den redigerte malen har blitt endret til **Utkast** og **Revisjon**-feltet er ikke lenger tomt. Dette betyr at prosessen for redigering av denne malen er startet.

![Redigert mal i arbeidsområdet for administrasjon av forretningsdokument](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a>Se gjennom firmainnstillinger

1.  Gå til **Organisasjonsstyring \> Organisasjoner \> Juridiske enheter**.
2.  Kontroller at URL-adressen for firma er angitt i hurtigfanen **Kontaktinformasjon**.

![Firma-URL angitt på juridisk enhet-siden](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a>Generere forretningsdokumenter for å teste den oppdaterte malen

1.  Endre firmaet til **USMF** i programmet, og gå til **Kunder \> Fakturaer \> Alle fritekstfakturaer**.
2.  Velg **FTI-00000002**-fakturaen, og velg deretter **Utskriftsbehandling**.
3.  I venstre rute utvider du **Modul - kunder \> Dokumenter \> Fritekstfaktura**.
4.  Under **Fritekstfaktura** velger du **Opprinnelig dokument** for å angi omfanget av fakturaer for behandling.
5.  I feltet **Rapportformat** i ruten til høyre velger du malen **Fritekstfaktura (Excel) Contoso** for det angitte dokumentnivået.

    ![Fritekstfaktura (Excel) Contoso-mal valgt](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  Trykk på **ESC** for å lukke den gjeldende siden.
7.  Velg **Skriv ut \> Valgt**.
8.  Last ned det genererte dokumentet, og åpne det i Excel.

    ![Fritekstfaktura i Excel](./media/BDM-AddFldExcel-PreviewReport.png)

Den endrede malen brukes til å generere rapporten fritekstfaktura for den valgte varen. Hvis du vil analysere hvordan denne rapporten påvirkes av endringene du gjør for malen, kan du kjøre denne rapporten i én programøkt rett etter at du endret malen i en annen programøkt.

## <a name="related-links"></a>Relaterte koblinger

[Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Oversikt over administrasjon av forretningsdokument](er-business-document-management.md)

[Utforme en konfigurasjon for generering av rapporter i OPENXML-format](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
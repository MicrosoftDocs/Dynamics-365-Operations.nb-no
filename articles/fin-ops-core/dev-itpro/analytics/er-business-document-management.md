---
title: Oversikt over administrasjon av forretningsdokument
description: Dette emnet gir informasjon om hvordan du bruker funksjonen for administrasjon av forretningsdokument i ER-rammeverket.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERSecurityAccessEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bc6363a96d87bf280a34dda34533bc71e21eb6b2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344936"
---
# <a name="business-document-management-overview"></a>Oversikt over administrasjon av forretningsdokument

[!include [banner](../includes/banner.md)]

Forretningsbrukere bruker [rammeverket for elektronisk rapportering (ER)](general-electronic-reporting.md) til å konfigurere formater for utgående dokumenter i overensstemmelse med de lovlige kravene i ulike land. Brukere kan også definere dataflyt for å angi hvilke programdata som skal plasseres i genererte dokumenter. ER-rammeverket genererer utgående dokumenter i Microsoft Office-formater (Excel-arbeidsbøker eller Word-dokumenter) ved å bruke forhåndsdefinerte maler. Malene fylles ut med nødvendige data i samsvar med konfigurert dataflyt mens påkrevde dokumenter genereres. Hvert konfigurerte format kan publiseres som en del av en ER-løsning for å generere bestemte utgående dokumenter. Dette representeres av en ER-formatkonfigurasjon som kan inneholde maler du kan bruke til å generere forskjellige utgående dokumenter. Forretningsbrukere kan bruke dette rammeverket til å administrere nødvendige forretningsdokumenter.

**Administrasjon av forretningsdokument** er bygd på toppen av ER-rammeverket og gjør det mulig for bedriftsbrukere å redigere dokumentmaler ved hjelp av Microsoft 365-tjenesteprogram eller passende Microsoft Office-skrivebordsprogram. Endringer i dokumentene kan inkludere endring av forretningsdokumentutforminger og tillegg av plassholdere for tilleggsdata uten kildekodeendringer og nye distribusjoner. Det er ikke nødvendig å ha kjennskap til ER-rammeverket for å oppdatere maler for forretningsdokumenter.

> [!NOTE]
> Vær oppmerksom på at administrasjon av forretningsdokument lar deg endre maler som brukes til å produsere forretningsdokumenter, for eksempel bestillinger, fakturaer osv. Når en mal er endret og en ny versjon av den har blitt publisert, brukes denne versjonen til å generere nødvendige forretningsdokumenter. Administrasjon av forretningsdokument kan ikke brukes til å endre forretningsdokumenter som allerede er generert.

## <a name="supported-deployments"></a>Støttede distribusjoner

For øyeblikket implementeres funksjonen for administrasjon av forretningsdokument bare for distribusjoner i skyen. Hvis denne funksjonen er kritisk for din lokale distribusjon, gir du oss beskjed ved å gi tilbakemelding på [Ideer](https://experience.dynamics.com/ideas/)-området.

## <a name="supported-microsoft-office-applications"></a>Microsoft Office-programmer som støttes

Hvis du vil bruke administrasjon av forretningsdokument for redigering av maler i Excel- eller Word-formater ved hjelp av Microsoft Office-skrivebordsprogrammer, må du ha Microsoft Office 2010 eller senere installert. Dette støttes i distribusjoner i skyen og lokalt.

Hvis du vil bruke administrasjon av forretningsdokument til å redigere maler i Excel- eller Word-formater ved hjelp av Microsoft 365-programmer, må du ha Microsoft 365 Office for nettabonnementet. Dette støttes i skydistribusjon.

## <a name="business-document-availability"></a>Tilgjengelighet av forretningsdokument

Du finner en fullstendig liste over alle rapportene som er planlagt for oktober 2019-utgivelsen, i [Rapportering av konfigurerbare forretningsdokumenter i Word og Excel](/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details).

Du finner en fullstendig liste over alle rapportene som er planlagt for oktober 2020-utgivelsen, i [Konfigurerbare forretningsdokumenter – Word-maler](/dynamics365-release-plan/2020wave1/dynamics365-finance/configurable-business-documents-word-templates).

Flere rapporter blir tilgjengelige i fremtidige versjoner. Spesielle varslinger om flere rapporter blir sendt separat. Hvis du vil vite hvordan du går gjennom listen over tilgjengelige rapporter, kan du se delen [Liste over ER-konfigurasjoner som er utgitt i Finance for å støtte konfigurerbare forretningsdokumenter](#list-of-configurations-cbd) nedenfor.

Hvis du vil vite mer om denne funksjonen, kan du fullføre eksemplet i dette emnet.

## <a name="configure-er-parameters"></a>Konfigurere ER-parametere

Ettersom administrasjon av forretningsdokument er bygd på toppen av ER-rammeverket, må du konfigurere ER-parameterne for å begynne å arbeide med administrasjon av forretningsdokument. Hvis du vil gjøre dette, må du definere nå ER-parameterne som beskrevet i [Konfigurere rammeverket for elektronisk rapportering (ER)](electronic-reporting-er-configure-parameters.md). Du må også legge til en ny konfigurasjonsleverandør som beskrevet i [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![ER-arbeidsområde.](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>Importere ER-løsninger

Eksempler på ER-konfigurasjoner brukes i eksemplet i denne fremgangsmåten. Du må importere, til den gjeldende forekomsten av Dynamics 365 Finance, ER-konfigurasjonene som inneholder malene for forretningsdokumenter som kan redigeres ved hjelp av administrasjon av forretningsdokumenter. Last ned og lagre følgende filer lokalt for å fullføre denne prosedyren.

**Eksempel på ER-kundefaktureringsløsning**

| Fil                                      | Innhold |
|-------------------------------------------|---------|
| Customer invoicing model.version.2.xml    | [ER-datamodellkonfigurasjon](https://download.microsoft.com/download/b/f/a/bfa5cb52-e6e2-42bc-a4c0-77014a4c54e6/Customerinvoicingmodel.version.2.xml) |
| Customer FTI report (GER).version.2.3.xml | [ER-formatkonfigurasjon for fritekstfaktura](https://download.microsoft.com/download/3/c/2/3c2e58f2-6e56-43d9-85ea-4c97252a108d/CustomerFTIreportGER.version.2.3.xml) |

**Eksempel på sjekkløsning for ER-betaling**

| Fil                                     | Innhold |
|------------------------------------------|---------|
| Modell for cheques.version.10.xml         | [ER-datamodellkonfigurasjon](https://download.microsoft.com/download/3/7/6/376cb0f6-181a-4895-a432-390ffca64162/Modelforcheques.version.10.xml) |
| Cheques printing format.version.10.9.xml | [ER-formatkonfigurasjon for betalingssjekk](https://download.microsoft.com/download/6/d/6/6d61bfff-3d89-4377-9e34-2e3ee6d6df91/Chequesprintingformat.version.10.9.xml) |

**Eksempel på ER-løsning for utenrikshandel**

| Fil                             | Innhold |
|----------------------------------|---------|
| Intrastat model.version.1.xml    | [ER-datamodellkonfigurasjon](https://download.microsoft.com/download/2/0/0/200d6ed1-eff8-48ec-ab75-175a4acf9714/Intrastatmodel.version.1.xml) |
| Intrastat report.version.1.9.xml | [ER-formatkonfigurasjon for Intrastat-kontrollrapport](https://download.microsoft.com/download/7/a/2/7a2a27c3-a8a5-42a1-9d04-f0a8e1ec1707/Intrastatreport.version.1.9.xml) |

Bruk fremgangsmåten nedenfor til å importere hver fil. Importer konfigurasjonen for ER-*datamodell* for hver av ER-løsningene i tabellene ovenfor før du importerer den tilsvarende konfigurasjonen for ER-*format*.

1. Åpne siden **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. Velg **Veksle** øverst på siden.
3. Velg **Last fra XML-fil**.
4. Velg **Bla gjennom** for å laste inn den påkrevde XML-filen.
5. Velg **OK** for å bekrefte konfigurasjonsimporten.

![ER-konfigurasjonsside der import av konfigurasjon bekreftes.](./media/BDM-Overview-ERSolutions.png)

Du kan også importere konfigurasjonene for offisielt publisert ER-format fra Microsoft Dynamics Lifecycle Service (LCS). Hvis du for eksempel vil fullføre denne prosedyren, kan du importere den siste versjonen av ER-formatkonfigurasjonen **Fritekstfaktura (Excel)**. De tilsvarende tilordningskonfigurasjonene for ER-datamodell og ER-modell blir importert automatisk.

![Innholdssiden Delt LCS-aktivabibliotek.](./media/BDM-Overview-SharedAssetLibrary.png)

Hvis du vil ha mer informasjon om å importere ER-konfigurasjoner, kan du se [Administrere livssyklus til konfigurasjoner for elektronisk rapportering (ER)](general-electronic-reporting-manage-configuration-lifecycle.md)

## <a name="enable-business-document-management"></a>Aktivere administrasjon av forretningsdokument

Hvis du vil starte administrasjon av forretningsdokument, må du åpne arbeidsområdet **Funksjonsbehandling** og aktivere funksjonen **Administrasjon av forretningsdokument**.

Bruk fremgangsmåten nedenfor til å aktivere funksjonalitet for administrasjon av forretningsdokument for alle juridiske enheter.

1. Åpne arbeidsområdet **Funksjonsbehandling**.
2. I fanen **Ny** velger du **Administrasjon av forretningsdokument** i listen.
3. Velg **Aktiver nå** for å aktivere den valgte funksjonen.
4. Oppdater siden for å få tilgang til den nye funksjonen.

> [!NOTE]
> Hvis du vil ha mer informasjon om bruk av det nye dokumentbrukergrensesnittet i forretningsdokumentadministrering, kan du se [Nytt dokumentbrukergrensesnitt i forretningsdokumentadministrering](er-business-document-management-new-template-ui.md).

![Arbeidsområde for funksjonsbehandling.](./media/BDM-Overview-FMEnabling.png)

Hvis du vil ha mer informasjon om hvordan du aktiverer nye funksjoner, kan du se [Oversikt over funksjonsbehandling](../../fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-parameters"></a>Konfigurere parametere

Bruk informasjonen i de følgende avsnittene til å definere de grunnleggende parameterne for administrasjon av forretningsdokument.

### <a name="prerequisites-for-parameter-setup"></a>Forutsetninger for parameteroppsett

Før du kan definere administrasjon av forretningsdokument, må du definere den nødvendige dokumenttypen i dokumentbehandlingsrammeverket. Denne dokumenttypen brukes til å angi en midlertidig lagring av dokumenter i Office-formater (Excel og Word) som brukes som maler for ER-rapporter. Den midlertidige lagringsmalen kan redigeres ved hjelp av Office-skrivebordsprogrammene.

Følgende attributtverdier må være valgt for denne dokumenttypen.

| Attributtnavn | Attributtverdi |
|----------------|-----------------|
| Klasse          | Tilknytt fil     |
| Gruppere          | Fil            |
| Lokasjon       | SharePoint      |

Hvis du vil ha informasjon om hvordan du definerer de nødvendige dokumentbehandlingsparameterne og dokumenttypene, kan du se [Konfigurere dokumentstyring](../../fin-ops/organization-administration/configure-document-management.md).

![Definere dokumenttype for dokumentstyring.](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a><a name="SetupBdmParameters"></a>Definere parametere

Grunnleggende parametere for administrasjon av forretningsdokument kan defineres på siden **Parametere for forretningsdokument**. Bare bestemte brukere har tilgang til siden. Inkludert følgende:

- Brukere som er tilordnet til rollen **Systemansvarlig**.
- Brukere som er tilordnet til en rolle som er konfigurert til å utføre plikten **Vedlikehold parametere for administrasjon av forretningsdokument** (AOT-navn **ERBDMaintainParameters**).

Bruk fremgangsmåten nedenfor til å definere de grunnleggende parameterne for alle juridiske enheter.

1. Logg på som en bruker med tilgang til siden **Parametere for forretningsdokument**.
2. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Administrasjon av forretningsdokument** \> **Parametere for forretningsdokument**.
3. På siden **Administrasjon av forretningsdokument**, i fanen **Vedlegg** i feltet **SharePoint-dokumenttype**, definerer du dokumenttypen som skal brukes til midlertidig lagring av maler i Office-formater mens de redigeres ved hjelp av Office-skrivebordsprogrammer. 

> [!NOTE]
> Bare dokumenttyper som er konfigurert ved hjelp av en SharePoint-plassering, er tilgjengelige for denne parameteren.

![Oppsett av parametere for administrasjon av forretningsdokument.](./media/BDM-Overview-BDMSetting.png)

Den valgte dokumenttypen er firmaspesifikk og vil bli brukt når brukeren arbeider med administrasjon av forretningsdokument i firmaet som den valgte dokumenttypen er konfigurert for. Når brukeren arbeider med administrasjon av forretningsdokument i et annet firma, vil den samme valgte dokumenttypen bli brukt hvis det ikke er definert en dokumenttype for dette firmaet. Når en dokumenttype er konfigurert, blir den brukt i stedet for den som er valgt i feltet **SharePoint-dokumenttype**.

> [!NOTE]
> **SharePoint-dokumenttype**-parameteren definerer en SharePoint-mappe som midlertidig lagringsplass for maler som kan redigeres ved å bruke Microsoft Excel eller Word. Du må definere denne parameteren hvis du har tenkt å bruke disse Office-skrivebordsapplikasjonene til å redigere maler. Hvis du vil ha mer informasjon, kan du se [Redigere en mal i Office-skrivebordsapplikasjonen](#EditInOfficeDesktopApp). Du kan la denne parameteren være tom hvis du planlegger å endre malen ved bare å bruke funksjonaliteten i Microsoft 365. Hvis du vil ha mer informasjon, kan du se [Redigere en mal i Microsoft 365](#EditInOffice365).

## <a name="configure-access-permissions"></a>Konfigurere tilgangstillatelser

Når tilgang til tillatelser for administrasjon av forretningsdokument ikke er aktivert, vil hver bruker med tilgang til arbeidsområdet for administrasjon av forretningsdokument som standard se alle de tilgjengelige ER-løsningsmalene som er tilgjengelige. Arbeidsområdet for administrasjon av forretningsdokument viser bare malene som finnes i ER-formatkonfigurasjoner, og som er merket med en **Forretningsdokumenttype**-kode.

![ER-konfigurasjonsside med kode for forretningsdokumenttype.](./media/BDM-Overview-ERFormatTags.png)

Listen over maler som er tilgjengelige i arbeidsområdet for administrasjon av forretningsdokument, kan begrenses ved å konfigurere tilgangstillatelser. Dette kan være viktig når forskjellige maler brukes til å produsere forretningsdokumenter for forskjellige forretningsdomener (funksjonsområder), og du vil gi bestemte brukere tilgang til ulike maler for redigering i arbeidsområdet for administrasjon av forretningsdokument.

Tillatelser for administrasjon av forretningsdokument kan angis i **Konfigurator av tilgangstillatelser**. Bare følgende brukere har tilgang til siden:

- Brukere som er tilordnet til rollen **Systemansvarlig**.
- Brukere som er tilordnet til en annen rolle som er konfigurert til å utføre plikten **Konfigurere tillatelser til å få tilgang til forretningsdokumentmaler** (AOT-navn **ERBDTemplatesSecurity**).

Bruk fremgangsmåten nedenfor til å aktivere tilgangstillatelser for administrasjon av forretningsdokument for alle juridiske enheter.

1. Logg på som en bruker med tilgang til siden **Konfigurator av tilgangstillatelser**.
2. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Administrasjon av forretningsdokument** \> **Administrer tilgangstillatelser**.

    Vær oppmerksom på varslingen som informerer deg om at bruken av tilgangstillatelser for administrasjon av forretningsdokument ikke er aktivert for øyeblikket.

    ![Siden Konfigurator for tilgangstillatelser for administrasjon av forretningsdokument.](./media/BDM-Overview-TemplatesAccess1.png)

    Med denne innstillingen kan hver bruker som er tilordnet en sikkerhetsrolle som er konfigurert til å utføre plikten **Administrer forretningsdokumentmaler** (AOT-navn **ERBDManageTemplates**), åpne arbeidsområdet Administrasjon av forretningsdokument og redigere alle maler som er tilgjengelige.

    Følgende grafikk viser hva som er tilgjengelig i arbeidsområdet for administrasjon av forretningsdokument for brukere som er tilordnet rollen **Regnskapsmedarbeider**. Med den gjeldende innstillingen for tilgangstillatelser kan brukeren redigere maler for forretningsdokumenter fra forskjellige funksjonsområder, inkludert fakturering, forskriftsmessig rapportering og betalinger.

    ![Arbeidsområdeside for administrasjon av forretningsdokument for regnskapsmedarbeider.](./media/BDM-Overview-TemplatesForAlice1.png)

3. På siden **Konfigurator av tilgangstillatelser** velger du **Innstilling for tilgangstillatelser**.
4. Aktiver alternativet **Bruk konfigurerte tilgangstillatelser** i dialogboksen **Innstillinger for tilgangstillatelser for redigering av maler**.
5. Velg **OK** for å bekrefte at tilgangstillatelser for administrasjon av forretningsdokument er aktivert.

    ![Bekrefte tilgangstillatelser for administrasjon av forretningsdokument.](./media/BDM-Overview-TemplatesAccess2.png)

6. Velg **Legg til** for å angi en ny forretningsrolle som det må konfigureres tillatelser til for å få tilgang til maler for administrasjon av forretningsdokument.
7. I dialogboksen **Sikkerhetsroller** velger du rollen **Regnskapsmedarbeider**, og deretter velger du **OK** for å bekrefte rollevalget.
8. Velg **Ny** i fanen **Tilgangstillatelser per konfigurasjonsbrikker**.
9. I **Brikketype**-feltet velger du **Funksjonsområde**, og deretter velger du **Fakturering** i **ID**-feltet.
10. Velg **Lagre** for å lagre konfigurerte tilgangstillatelser for den valgte rollen.

    Den gjeldende innstillingen betyr at for alle brukere som er tilordnet rollen **Regnskapsmedarbeider** og som utfører plikten **Administrer forretningsdokumentmaler** (AOT-navn **ERBDManageTemplates**), vil maler for ER-formatkonfigurasjon som har **Fakturering**-verdien for **Funksjonsområde**-brikken, være tilgjengelig for redigering på arbeidsområdesiden Administrasjon av forretningsdokument.

11. Bytt til **Beslektet informasjon**-ruten fra høyre side av gjeldende side. Ruten **Beslektet informasjon** viser hvordan de konfigurerte tilgangstillatelsene vil bli brukt, inkludert hvilke ER-konfigurasjonsmaler som er tilgjengelig for brukere som er tilordnet rollen **Regnskapsmedarbeider**.

    ![Ruten Beslektet informasjon på siden Konfigurator av tilgangstillatelser.](./media/BDM-Overview-TemplatesAccess3.png)

12. Velg alternativet **Legg til** i fanen **Tilgangstillatelser per konfigurasjoner**.
13. Merk ER-formatkonfigurasjonen **Intrastat-rapport** i dialogboksen **Velg konfigurasjon**.
14. Velg **OK** for å bekrefte oppføringen av de valgte konfigurasjonene, og velg deretter **Lagre** for å lagre de konfigurerte tilgangsrettighetene for den valgte rollen.

Den gjeldende innstillingen betyr at for alle brukere som er tilordnet rollen **Regnskapsmedarbeider** og utfører plikten **Administrer forretningsdokumentmaler** (AOT-navn **ERBDManageTemplates**), vil følgende maler være tilgjengelige for redigering i arbeidsområdet Administrasjon av forretningsdokument:

- Maler som har verdien **Fakturering** for **Funksjonsområde**-brikken.
- Maler fra ER-formatkonfigurasjoner som vises i fanen **Tilgangstillatelser per konfigurasjoner** (maler fra formatkonfigurasjonen **Intrastat-rapport** for **Lovbestemt rapportering** i dette eksemplet).

![Hurtigfaner for tilgangstillatelser på siden Konfigurator av tilgangstillatelser.](./media/BDM-Overview-TemplatesAccess4.png)

Følgende grafikk viser hva arbeidsområdet for administrasjon av forretningsdokument gir en bruker som er tilordnet rollen **Regnskapsmedarbeider**. Med den gjeldende innstillingen for tilgangstillatelser for administrasjon av forretningsdokument kan brukeren redigere forretningsdokumentmaler fra **Fakturering**-domenet og ER-formatkonfigurasjonen **Intrastat-rapport**. Maler fra **Betalinger**-domenet er ikke tilgjengelige for rollen **Regnskapsmedarbeider**.

![Redigere maler for forretningsdokumenter på arbeidsområdesiden for administrasjon av forretningsdokument.](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> Reglene i **Tilgangstillatelser per konfigurasjoner** lagres ved hjelp av den unike identifikasjons-IDen for en ER-formatkonfigurasjon. Dette betyr at disse reglene ikke blir slettet når en ER-konfigurasjon som refererer til dem, slettes. Når du importerer slettede konfigurasjoner tilbake til denne forekomsten, vil disse reglene referere til dem på nytt. Du trenger ikke definere reglene på nytt etter at de slettede konfigurasjonene er importert på nytt.

## <a name="use-business-document-management-to-edit-templates"></a>Bruke administrasjon av forretningsdokument til å redigere maler

Forretningsbrukere kan få tilgang til maler for forretningsdokumenter for redigering i arbeidsområdet for administrasjon av forretningsdokument. Bare følgende brukere har tilgang til arbeidsområdet for administrasjon av forretningsdokument:

- Brukere som er tilordnet til rollen **Systemansvarlig**.
- Brukere som er tilordnet til en rolle som er konfigurert til å utføre plikten **Administrer forretningsdokumentmaler** (AOT-navn **ERBDManageTemplates**).

Bruk fremgangsmåten nedenfor til å redigere maler for fritekstfaktura i arbeidsområdet for administrasjon av forretningsdokument. Før du fullfører denne fremgangsmåten, må du ha fullført alle fremgangsmåtene ovenfor i dette emnet.

1. Logg på som en bruker med tilgang til siden Arbeidsområdet for administrasjon av forretningsdokument.
2. Åpne arbeidsområdet for administrasjon av forretningsdokument.

Når funksjonen **Office-lignende brukergrensesnitterfaring for administrasjon av forretningsdokument** er slått av i arbeidsområdet **Funksjonsbehandling**, viser hovedrutenettet i arbeidsområdet **Administrasjon av forretningsdokument** følgende maler:

- Maler som eies av ER-konfigurasjonsleverandøren din (det vil si leverandøren som for øyeblikket er merket som aktiv i arbeidsområdet **Elektronisk rapportering**). Når du har valgt en av disse malene, kan du velge **Rediger mal** for å starte eller fortsette å redigere den.
- Maler som eies av andre ER-konfigurasjonsleverandører. Når du har valgt en av disse malene, kan du velge **Nytt dokument** for å opprette en kopi av det som eies av ER-konfigurasjonsleverandøren din, og deretter begynne å redigere kopien.

![Maloppføringer på arbeidsområdesiden for administrasjon av forretningsdokument.](./media/BDM-Overview-EditingTemplate1.png)

Fanen **Mal** viser innholdet i den valgte malen. Velg fanen **Detaljer** for å se gjennom detaljene for den valgte malen og detaljer om en ER-formatkonfigurasjon denne malen ligger i. Legg merke til at alle malene har statusen **Publisert** og ikke inneholder noen detaljer i **Endring**-kolonnen. Dette betyr at disse malene ikke redigeres for øyeblikket.

Når funksjonen **Office-lignende brukergrensesnitterfaring for administrasjon av forretningsdokument** er slått på i arbeidsområdet **Funksjonsbehandling**, viser hovedrutenettet i arbeidsområdet **Administrasjon av forretningsdokument** maler som eies av ER-konfigurasjonsleverandøren din (det vil si leverandøren som for øyeblikket er merket som aktiv i arbeidsområdet **Elektronisk rapportering**). Når du har valgt en av disse malene, kan du velge **Rediger mal** for å starte eller fortsette å redigere den.

Hvis du vil arbeide med maler som eies av andre ER-konfigurasjonsleverandører, velger du **Nytt dokument** for å opprette en kopi av malen som eies av ER-leverandøren din. Du kan deretter redigere kopien. For mer informasjon, se [Nytt dokumentbrukergrensesnitt i Forretningsdokumentbehandling](er-business-document-management-new-template-ui.md).

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Start redigering av maler som eies av konfigurasjonsleverandøren

1. I arbeidsområdet for administrasjon av forretningsdokument velger du malen **Utskriftsformat for sjekker** i listen.
2. Velg fanen **Detaljer**.

![Detaljer-fanen på arbeidsområdesiden for administrasjon av forretningsdokument.](./media/BDM-Overview-EditingTemplate2.png)

Alternativet **Rediger mal** er tilgjengelig for den valgte malen. Dette alternativet er alltid tilgjengelig for en mal i en ER-formatkonfigurasjon som eies av den aktive ER-konfigurasjonsleverandøren (**Litware, Inc.** i dette eksemplet). Når **Rediger mal** er valgt, vil den eksisterende malen fra kladdeversjonen av den underliggende ER-formatkonfigurasjonen være tilgjengelig for redigering.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Start redigering av maler som eies av andre leverandører

1. I Forretningsdokumentadministrering-arbeidsområdet velger du dokumentet du vil bruke som en mal.

    ![Velge et dokument på arbeidsområdesiden for administrasjon av forretningsdokument.](./media/BDM-Overview-EditingTemplate3.png)

2. Velg **Nytt dokument**, gå til **Tittel**-feltet og endre om nødvendig tittelen på den redigerbare malen. Teksten brukes til å navngi ER-formatkonfigurasjonen som opprettes automatisk. Legg merke til at utkastversjonen av denne konfigurasjonen (**Kunde-FTI-rapport (GER) – kopi**) som vil inneholde den redigerte malen, automatisk vil bli merket for å kjøre dette ER-formatet for gjeldende bruker. Samtidig brukes den uendrede opprinnelige malen fra den grunnleggende ER-formatkonfigurasjonen til å kjøre dette ER-formatet for alle andre brukere.
3. I **Navn** -feltet endrer du navnet på den første revisjonen av den redigerbare malen som skal opprettes automatisk.
4. I **Kommentar**-feltet endrer du kommentaren for den automatisk opprettede revisjonen av den redigerbare malen.
5. Velg **OK** for å bekrefte starten på redigeringsprosessen.

![Bekrefte begynnelsen på redigeringsprosessen for å opprette en ny mal.](./media/BDM-Overview-EditingTemplate4.png)

Hvis det ikke finnes noen leverandør, vil det bli tilbudt å opprette en. Hvis det ikke finnes en aktiv leverandør, vil det bli tilbudt en for aktivering.

Hvis du vil opprette en leverandør, endrer du navnet på leverandøren i **Navn**-feltet, oppdaterer Internett-adressen til den nye leverandøren i feltet **Internett-adresse** og velger **OK** for å bekrefte.

   ![Opprette ny leverandør i BDM.](./media/bdm_create_provider.png)

Hvis du vil aktivere eksisterende leverandør, velger du navnet på leverandøren i **Konfigurasjonsleverandør**-feltet, og velger **OK** for å angi leverandøren som aktiv.

   ![Aktivere leverandør i BDM.](./media/bdm_choose_provider.png)

> [!NOTE]
> Hver BDM-mal refererer til leverandøren som forfatteren av konfigurasjonen. Dette er årsaken til hvorfor en aktiv leverandør er nødvendig for malen.


**Nytt dokument**-alternativet er alltid tilgjengelig for en mal i en ER-formatkonfigurasjon levert av gjeldende og en annen leverandør (Microsoft i dette eksempelet) som ikke har noen revisjoner. Den redigerte malen blir deretter lagret i en ny ER-formatkonfigurasjon som genereres automatisk.



### <a name="start-editing-a-template"></a>Begynn å redigere en mal

1. Velg **Rediger dokument** fra den valgte malen.
2. I **Navn** -feltet endrer du navnet på den første revisjonen av den redigerbare malen som skal opprettes automatisk.
3. I **Kommentar**-feltet endrer du kommentaren for den automatisk opprettede revisjonen av den redigerbare malen.

    ![Redigere en mal på arbeidsområdesiden for administrasjon av forretningsdokument.](./media/BDM-Overview-EditingTemplate5.png)

4. Velg **OK** for å bekrefte starten på redigeringsprosessen.

Siden **BDM-malredigering** åpnes. Den valgte malen vil være tilgjengelig for elektronisk redigering ved hjelp av Microsoft 365.

![Side for redigering av mal for administrasjon av forretningsdokument.](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-microsoft-365"></a><a name="EditInOffice365"></a>Redigere en mal i Microsoft 365

Du kan endre malen ved å bruke Microsoft 365. I Office Online kan du for eksempel endre skrifttypen til feltledetekstene i maloverskriften fra **Vanlig** til **Fet**. Disse endringene lagres automatisk i den redigerbare malen som er lagret i den primære malens lagringsplass (som standard Azure Blob-lagring). Dette er konfigurert for ER-rammeverket.

![Endre skriften til fet skrift i malhodet på siden for redigering av mal for administrasjon av forretningsdokument.](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a><a name="EditInOfficeDesktopApp"></a>Redigere en mal i Office-skrivebordsprogrammet

> [!NOTE]
> Denne funksjonen er bare tilgjengelig når **SharePoint-dokumenttype**-parameteren er konfigurert riktig. Hvis du vil ha mer informasjon, kan du se [Konfigurere parametere](#SetupBdmParameters).

1. Velg alternativet **Åpne i skrivebordsprogram** for å endre malen ved hjelp av funksjonaliteten i Office-skrivebordsprogrammet (Excel i dette eksemplet). Den redigerbare malen kopieres fra det permanente lageret til den midlertidige lagringsplassen som er konfigurert i parameterne for administrasjon av forretningsdokument som en SharePoint-mappe.
2. Bekreft at du vil åpne malen fra den midlertidige fillagringen i Office Excel-programmet.

    ![Mal åpnet i skrivebordsversjonen av Excel.](./media/BDM-Overview-EditingLayout3.png)

3. Endre malen. Endre for eksempel skrifttypen til feltledetekstene i maloverskriften ved å oppdatere farge fra **Svart** til **Blå**.

    ![Endre skriftfargen i malhodet ved å bruke skrivebordsversjonen av Excel.](./media/BDM-Overview-EditingLayout4.png)

4. Velg **Lagre** i Excel-skrivebordsprogrammet for å lagre malendringene i den midlertidige lagringen.

    ![Lagre endringer på siden for redigering av mal for administrasjon av forretningsdokument ved å bruke skrivebordsversjonen av Excel.](./media/BDM-Overview-EditingLayout5.png)

5. Lukk Excel-skrivebordsprogrammet.
6. Velg **Synkroniser lagret kopi** for å synkronisere den midlertidige mallagringen i det permanente mallageret.

> [!NOTE]
> Kopien av den redigerbare malen i den midlertidige fillagringen beholdes bare for gjeldende økt med malredigering. Når du fullfører denne økten ved å lukke siden for **BDM-malredigering**, vil denne kopien bli slettet. Hvis du justerte malen i den midlertidige fillagringen og ikke merket av for **Synkroniser lagret kopi**, vil du bli spurt om du vil lagre endringer når du prøver å lukke siden for **BDM-malredigering**. Velg **Ja** hvis du vil lagre endringene i malen i den permanente filplasseringen.

### <a name="validate-a-template"></a>Validere en mal

1. På siden for **BDM-malredigering** velger du **Se etter problemer** for å validere den endrede malen mot den underliggende ER-formatkonfigurasjonen. Følg eventuelle anbefalinger for å justere malen med strukturen til formatet fra den grunnleggende ER-formatkonfigurasjonen.
2. Velg **Vis format** for å vise den gjeldende strukturen i formatet fra den grunnleggende ER-formatkonfigurasjonen som må justeres med den redigerbare malen. 
3. Velg **Skjul format** for å lukke ruten.

    ![Siden for BDM-malredigering.](./media/BDM-Overview-EditingTemplate6.png)

4. Lukk siden for **BDM-malredigering**.

Den oppdaterte malen vises i fanen **Mal**. Legg merke til at statusen for den redigerte malen nå er **Utkast**, og den gjeldende revisjonen er ikke lenger tom. Dette betyr at prosessen for redigering av denne malen er startet.

![Vise den oppdaterte malen på arbeidsområdesiden for administrasjon av forretningsdokument.](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>Teste den endrede malen 

1. I programmet bytter du til firmaet **USMF**.
2. Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.
3. Velg **FTI-00000002**-fakturaen, og velg deretter **Utskriftsbehandling**.
4. Velg **Modul - kunder** \> **Dokumenter** \> **Fritekstfaktura** \> **Opprinnelig dokument** for å angi omfanget av fakturaer for behandling.
5. I **Rapportformat**-feltet velger du ER-format **Kunde-FTI-rapport (GER) – kopi** for det angitte dokumentnivået.

    ![Siden for innstilling for utskriftsbehandling.](./media/BDM-Overview-TestRun1.png)

6. Trykk på **ESC** for å lukke den gjeldende siden.
7. Velg **Skriv ut**, og velg deretter **Valgt**.
8. Last ned dokumentet og åpne det ved hjelp av Excel-skrivebordsprogrammet.

![Siden Fritekstfakturaer.](./media/BDM-Overview-TestRun2.png)

Den endrede malen brukes til å generere rapporten fritekstfaktura for den valgte varen. Hvis du vil analysere hvordan denne rapporten påvirkes av endringene du har innført for malen, kan du kjøre denne rapporten i én programøkt rett etter at du endret malen i en annen programøkt.

### <a name="create-an-alternative-template-revision"></a>Opprette en alternativ malendring

1. Åpne siden for **BDM-malredigering** og velg malen **Kunde-FTI-rapport (GER) – kopi**.
2. Velg **Ny** i fanen **Endringer**.
3. Hvis det er nødvendig, endrer du navnet på den andre endringen i **Navn**-feltet og baserer den på første endringen som er aktiv for øyeblikket.
4. I **Kommentar**-feltet endrer du om nødvendig kommentaren for den automatisk opprettede revisjonen av den redigerbare malen.

    ![Gjøre endringer i malen på arbeidsområdesiden for administrasjon av forretningsdokument.](./media/BDM-Overview-AddRevision.png)

    Du har opprettet en ny endring av malen som er lagret i den permanente malens lagring. Nå kan du fortsette å redigere malen for den andre endringen som er valgt som aktiv.

5. Velg den første endringen, og velg deretter **Angi som aktiv**. Du kan når som helst velge en annen endring som aktiv hvis du vil gå tilbake til denne endringen av malen.
6. Velg den andre endringen, og velg deretter **Slett**.
7. Velg **OK** for å bekrefte at du vil slette den valgte endringen. Du kan slette alle ikke-aktive endringer når de ikke lenger er nødvendige.

### <a name="delete-a-modified-template"></a>Slette en endret mal

1. Velg fanen **Mal** på siden **BDM-malredigering**.
2. Velg **Slett**.
3. Hvis du velger **OK** for å bekrefte slettingen, slettes ER-formatet **Kunde-FTI-rapport (GER) – kopi** med den endrede malen. Velg **Avbryt** for å utforske andre alternativer.

### <a name="revoke-changes-of-template"></a>Tilbakekalle endringer i mal

Når du redigerer malen fra et ER-format som eies av gjeldende aktive leverandør, får du mulighet til å tilbakekalle endringer som er innført for malen.

![Forkaste endringer i malen på arbeidsområdesiden for administrasjon av forretningsdokument.](./media/BDM-Overview-RevokeChanges.png)

1. Velg fanen **Mal** på siden **BDM-malredigering**.
2. Velg **Angre**.
3. Hvis du velger **OK** for å oppheve endringene som er innført for malen, erstattes den endrede malen med den opprinnelige malen, og alle endringer fjernes. Når du tilbakekaller endringer i malen, kan du slette malen. Velg **Avbryt** for å utforske andre alternativer.

### <a name="publish-a-modified-template"></a>Publisere en endret mal

1. Velg **Publiser** på siden **BDM-malredigering** i fanen **Mal**.
2. Hvis du velger **OK** for å bekrefte publisering, merkes utkastversjonen av det avledede ER-formatet **Kunde-FTI-rapport (GER) – kopi** som inneholder den endrede malen, som fullført. Den endrede malen blir tilgjengelig for andre brukere. De fullførte versjonene av dette ER-formatet vil bare beholde den siste aktive endringen av malen. Andre endringer vil bli slettet. Velg **Avbryt** for å utforske andre alternativer.

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

### <a name="i-selected-edit-document-but-instead-of-going-to-the-bdm-template-editor-page-in-finance-i-was-sent-to-the-microsoft-365-webpage"></a>Jeg valgte Rediger dokument, men i stedet for å gå til siden for BDM-malredigering i Finance, ble jeg sendt til Microsoft 365-nettsiden.

Dette er et kjent problem som involverer Microsoft 365-omdirigeringen. Det skjer når du logger deg på Microsoft 365 for første gang. Du kan omgå dette problemet ved å velge **Tilbake** i nettleseren for å gå tilbake til forrige side.

### <a name="i-understand-how-to-edit-a-template-by-using-microsoft-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-and-adjust-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-use-the-office-desktop-application-in-the-same-way"></a>Jeg vet hvordan jeg skal redigere en mal ved å bruke Microsoft 365 i den første programøkten, og hvordan jeg skal bruke malen i den andre programøkten og justere malen for å se hvordan endringene påvirker det genererte forretningsdokumentet. Kan jeg bruke Office-skrivebordsprogrammet på samme måte?

Ja, det kan du. Velg **Åpne i skrivebordsprogram** i den første programøkten. Malen vil bli lagret i den midlertidige fillagringen og åpnes i Office-skrivebordsprogrammet. Deretter fullfører du følgende trinn for å forhåndsvise malendringene i det genererte forretningsdokumentet:

1. Utfør endringer i malen ved hjelp av Office-skrivebordsprogrammet.
2. Velg **Lagre** i Office-skrivebordsprogrammet.
3. Velg **Synkroniser lagret kopi** på siden **BDM-malredigering** for den første programøkten.
4. Utfør dette ER-formatet for mal i den andre programøkten.

### <a name="when-i-select-open-in-desktop-app-i-receive-the-following-error-message-value-cannot-be-null-parameter-name-externalid-how-do-i-work-around-this-issue"></a>Når jeg velger Åpne i skrivebordsprogrammet, får jeg følgende feilmelding: «Verdien kan ikke være null. Parameternavn: externalId.» Hvordan omgår jeg dette problemet?

Sannsynligvis er du logget på den gjeldende forekomsten av appen for Azure AD-domenet som er forskjellig fra Azure AD-domenet som ble brukt til å distribuere denne forekomsten. Fordi SharePoint-tjenesten, som brukes til å lagre maler for å gjøre dem tilgjengelige for redigering ved hjelp av Office-skrivebordsprogrammene, tilhører samme domene, har vi ingen tilgangstillatelser til SharePoint-tjenesten. Når du skal løse dette problemet, logger du på den gjeldende forekomsten ved hjelp av legitimasjonen til en bruker med riktig Azure AD-domene.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format (november 2016)](tasks/er-design-reports-openxml-2016-11.md)

[Utforme ER-konfigurasjoner for å generere rapporter i Word-format](tasks/er-design-configuration-word-2016-11.md)

[Bygge inn bilder og figurer i dokumenter du genererer ved hjelp av ER](electronic-reporting-embed-images-shapes.md)

[Konfigurere elektronisk rapportering (ER) for å hente data til Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)

## <a name="list-of-er-configurations-that-have-been-released-in-finance-to-support-configurable-business-documents"></a><a name="list-of-configurations-cbd"></a>Liste over ER-konfigurasjoner som er utgitt i Finance for å støtte konfigurerbare forretningsdokumenter

[Listen](general-electronic-reporting.md#list-of-configurations) over ER-konfigurasjoner for Finance oppdateres hele tiden. Åpne det [globale repositoriet](er-download-configurations-global-repo.md) for å se gjennom listen over ER-konfigurasjoner som støttes for øyeblikket. Du kan [filtrere](../../../finance/localizations/enhanced-filtering-global-repo.md) det globale repositoriet for å se gjennom listen over ER-konfigurasjoner som brukes til å støtte konfigurerbare forretningsdokumenter.

![Filtrere innholdet i det globale repositoriet på siden Konfigurasjonsrepositorium.](./media/bdm-overview-filterglobalrepo.gif)

Tabellen nedenfor viser listen over ER-konfigurasjoner som støtter konfigurerbare forretningsdokumenter, og som har blitt utgitt i Finance frem til desember 2020.

| Datamodellkonfigurasjon    | Formatkonfigurasjoner                           |
|-----------------------------|-------------------------------------------------|
| Fraktbrevmodell        | Fraktbrev (Excel)                          |
|                             | Fraktbrev (Word)                           |
| Modell for opprinnelsessertifikat | Opprinnelsessertifikat (Excel)                   |
|                             | Opprinnelsessertifikat (Word)                    |
| Fakturamodell               | Kundedebetnota og kundekreditnota (Excel)          |
|                             | Kundedebetnota og kundekreditnota (Word)           |
|                             | Fritekstfaktura (Excel)                       |
|                             | Fritekstfaktura (Excel) (BH)                  |
|                             | Fritekstfaktura (FR) (Excel)                  |
|                             | Fritekstfaktura (LT) (Excel)                  |
|                             | Fritekstfaktura (LV) (Excel)                  |
|                             | Fritekstfaktura (PL) (Excel)                  |
|                             | Fritekstfaktura (CZ) (Excel)                  |
|                             | Fritekstfaktura (EE) (Excel)                  |
|                             | Fritekstfaktura (HU) (Excel)                  |
|                             | Fritekstfaktura (TH) (Excel)                  |
|                             | Fritekstfaktura (Word)                        |
|                             | Linjeelementer for prosjektkontrakt (Excel)             |
|                             | Linjeelementer for prosjektkontrakt (CZ) (Excel)        |
|                             | Linjeelementer for prosjektkontrakt (Excel) (BH)        |
|                             | Linjeelementer for prosjektkontrakt (HU) (Excel)        |
|                             | Linjeelementer for prosjektkontrakt (LT) (Excel)        |
|                             | Linjeelementer for prosjektkontrakt (PL) (Excel)        |
|                             | Linjeelementer for prosjektkontrakt (Word)              |
|                             | Frigivelse av kundebevaring for prosjekt (Excel)      |
|                             | Frigivelse av kundebevaring for prosjekt (CZ) (Excel) |
|                             | Frigivelse av kundebevaring for prosjekt (HU) (Excel) |
|                             | Frigivelse av kundebevaring for prosjekt (LT) (Excel) |
|                             | Frigivelse av kundebevaring for prosjekt (PL) (Excel) |
|                             | Frigivelse av kundebevaring for prosjekt (TH) (Excel) |
|                             | Frigivelse av kundebevaring for prosjekt (Word)       |
|                             | Prosjektfaktura (Excel)                         |
|                             | Prosjektfaktura (Word)                          |
|                             | Prosjektfaktura (AE) (Excel)                    |
|                             | Prosjektfaktura (CZ) (Excel)                    |
|                             | Prosjektfaktura (Excel) (BH)                    |
|                             | Prosjektfaktura (HU) (Excel)                    |
|                             | Prosjektfaktura (JP) (Excel)                    |
|                             | Prosjektfaktura (LT) (Excel)                    |
|                             | Prosjektfaktura (PL) (Excel)                    |
|                             | Prosjektfaktura (TH) (Excel)                    |
|                             | Fullstendig prosjektfaktura (MY) (Excel)               |
|                             | Enkel prosjektfaktura (MY) (Excel)             |
|                             | Fakturaadministrasjon for prosjekt (Excel)                  |
|                             | Fakturaadministrasjon for prosjekt (CZ) (Excel)             |
|                             | Fakturaadministrasjon for prosjekt (Excel) (BH)             |
|                             | Fakturaadministrasjon for prosjekt (HU) (Excel)             |
|                             | Fakturaadministrasjon for prosjekt (JP) (Excel)             |
|                             | Fakturaadministrasjon for prosjekt (LT) (Excel)             |
|                             | Fakturaadministrasjon for prosjekt (PL) (Excel)             |
|                             | Fakturaadministrasjon for prosjekt (Word)                   |
|                             | Forskuddsfaktura for kjøp (Excel)                |
|                             | Forskuddsfaktura for kjøp (Word)                 |
|                             | Salgsforskuddsfaktura (Excel)                   |
|                             | Salgsforskuddsfaktura (Word)                    |
|                             | Salgsforskuddsfaktura (PL) (Excel)              |
|                             | Salgsfaktura (Excel)                           |
|                             | Salgsfaktura (Excel) (BH)                      |
|                             | Salgsfaktura (Excel) (CZ)                      |
|                             | Salgsfaktura (Excel) (EE)                      |
|                             | Salgsfaktura (Excel) (FR)                      |
|                             | Salgsfaktura (Excel) (HU)                      |
|                             | Salgsfaktura (Excel) (IN)                      |
|                             | Salgsfaktura (Excel) (LT)                      |
|                             | Salgsfaktura (Excel) (LV)                      |
|                             | Salgsfaktura (Excel) (PL)                      |
|                             | Salgsfaktura (Excel) (TH)                      |
|                             | Salgsfaktura (Word)                            |
|                             | Kommersiell faktura for TMS (Excel)                  |
|                             | Kommersiell faktura for TMS (Word)                   |
|                             | Leverandørfakturadokument (Excel)                 |
|                             | Leverandørfakturadokument (CZ) (Excel)            |
|                             | Leverandørfakturadokument (HU) (Excel)            |
|                             | Leverandørfakturadokument (IN) (Excel)            |
|                             | Leverandørfakturadokument (LT) (Excel)            |
|                             | Leverandørfakturadokument (LV) (Excel)            |
|                             | Leverandørfakturadokument (MY) (Excel)            |
|                             | Leverandørfakturadokument (MY)                  |
| Ordremodell                 | Avtalebekreftelse (Excel)                  |
|                             | Avtalebekreftelse (Word)                   |
|                             | Innkjøpsavtalebekreftelse (Excel)         |
|                             | Innkjøpsavtalebekreftelse (Word)          |
|                             | Bestilling (Excel)                          |
|                             | Bestilling (CZ) (Excel)                     |
|                             | Bestillingsforespørsel (CZ) (Excel)             |
|                             | Bestilling (HU) (Excel)                     |
|                             | Bestillingsforespørsel (HU) (Excel)             |
|                             | Bestilling (Word)                           |
|                             | Bestillingsforespørsel (Excel)                  |
|                             | Bestillingsforespørsel (Word)                   |
|                             | Salgsordrebekreftelse (Excel)                |
|                             | Salgsordrebekreftelse (CZ) (Excel)           |
|                             | Salgsordrebekreftelse (HU) (Excel)           |
|                             | Salgsordrebekreftelse (Word)                 |
| Modell for følgeseddelliste          | Containerinnhold (Excel)                      |
|                             | Containerinnhold (Word)                       |
|                             | Lastliste (Excel)                               |
|                             | Lastliste (Word)                                |
|                             | Plukkliste (Excel)                            |
|                             | Plukkliste (CZ) (Excel)                       |
|                             | Plukkliste (Word)                             |
|                             | Produksjonsplukkliste (Excel)                    |
|                             | Produksjonsplukkliste (Word)                     |
|                             | Forsendelsesplukkliste for last (Excel)             |
|                             | Forsendelsesplukkliste for last (Word)              |
|                             | Forsendelsesplukkliste for forsendelse (Excel)         |
|                             | Forsendelsesplukkliste for forsendelse (Word)          |
|                             | Forsendelsesplukkliste for bølge (Excel)             |
|                             | Forsendelsesplukkliste for bølge (Word)              |
| Betalingsmodell               | Betalingsmelding for kunde (Excel)                 |
|                             | Betalingsmelding for kunde (Word)                  |
|                             | Betalingsmelding for leverandør (Excel)                   |
|                             | Betalingsmelding for leverandør (Excel)                    |
| Tilbudsmodell             | Prosjekttilbud (Excel)                       |
|                             | Prosjekttilbud (Word)                        |
|                             | Tilbudsforespørsel (Excel)                   |
|                             | Tilbudsforespørsel (Godta) (Excel)          |
|                             | Tilbudsforespørsel (Godta) (Word)           |
|                             | Tilbudsforespørsel (Avvis) (Excel)          |
|                             | Tilbudsforespørsel (Avvis) (Word)           |
|                             | Tilbudsforespørsel (Returner) (Excel)          |
|                             | Tilbudsforespørsel (Returner) (Word)           |
|                             | Tilbudsforespørsel (Word)                    |
|                             | Salgstilbud (Excel)                         |
|                             | Salgstilbud (CZ) (Excel)                    |
|                             | Salgstilbud (HU) (Excel)                    |
|                             | Salgstilbud (Word)                          |
|                             | Salgstilbudsbekreftelse (Excel)            |
|                             | Salgstilbudsbekreftelse (Word)             |
| Avstemmingsmodell        | Kontoutdrag for kunde, ekstern (Excel)             |
|                             | Kontoutdrag for kunde, ekstern (CN) (Excel)        |
|                             | Kontoutdrag for kunde, ekstern (Word)              |
|                             | Kontoutdrag for kunde, Frankrike (Excel)          |
| Påminnelsesmodell              | Purrenota (Excel)                  |
|                             | Purrenota (CN) (Excel)             |
|                             | Purrenota (Word)                   |
|                             | Kunderentenota (Excel)                  |
|                             | Kunderentenota (Word)                   |
| Fraktbrevmodell               | Lastbetalingsmiddel (Excel)                             |
|                             | Lastbetalingsmiddel (Word)                              |
|                             | Følgeseddel for bestilling (Excel)             |
|                             | Følgeseddel for bestilling (CZ) (Excel)        |
|                             | Følgeseddel for bestilling (Word)              |
|                             | Rute (Excel)                                   |
|                             | Rute (Word)                                    |
|                             | Følgeseddel for salgsordre (Excel)                |
|                             | Følgeseddel for salgsordre (CZ) (Excel)           |
|                             | Følgeseddel for salgsordre (LT) (Excel)           |
|                             | Følgeseddel for salgsordre (PL) (Excel)           |
|                             | Følgeseddel for salgsordre (Word)                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

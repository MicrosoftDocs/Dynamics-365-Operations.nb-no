---
title: "Mål for elektronisk rapportering"
description: "Du kan konfigurere et mål for hver formatkonfigurasjon for elektronisk rapportering (ER) og utdatakomponenten (en mappe eller en fil). Brukere som er gitt riktige tilgangsrettigheter kan også endre målinnstillingene ved kjøretid. Denne artikkelen beskriver administrasjon av mål for elektronisk rapportering, måltyper som støttes og sikkerhetsvurderinger."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: d38d05fe445bf0326d408038dff84ccf8c0ff64c
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-destinations"></a>Mål for elektronisk rapportering

Du kan konfigurere et mål for hver formatkonfigurasjon for elektronisk rapportering (ER) og utdatakomponenten (en mappe eller en fil). Brukere som er gitt riktige tilgangsrettigheter kan også endre målinnstillingene ved kjøretid. Denne artikkelen beskriver administrasjon av mål for elektronisk rapportering, måltyper som støttes og sikkerhetsvurderinger.

Formatkonfigurasjoner for elektronisk rapportering (ER) inneholder vanligvis minst én utdatakomponent: en fil. Konfigurasjoner inneholder vanligvis flere filutdatakomponenter av forskjellige typer (for eksempel XML, TXT eller XLSX) som er gruppert i én eller flere mapper. Administrasjon av mål for elektronisk rapportering lar deg forhåndsdefinere hva som skjer når hver komponent kjøres. Som standard når en konfigurasjon er kjørt, vises en dialogboks som lar brukeren lagre eller åpne filen. Den samme virkemåten brukes også når du importerer en ER-konfigurasjon og ikke konfigurerer noen bestemte mål for den. Når et mål opprettes for en hovedutdatakomponent, overstyrer dette målet standard virkemåte, og mappen eller filen sendes i henhold til innstillingene for målet.

## <a name="availability-and-general-prerequisites"></a>Tilgjengelighet og generelle forutsetninger
ER mål-funksjonaliteten er ikke tilgjengelig i Microsoft Dynamics 365 for operasjoner 7.0 (februar 2016)-versjonen. Derfor må du installere Microsoft Dynamics 365 for operasjoner (November 2016 utgave) til å bruke alle funksjonene som er beskrevet i dette emnet. Du kan eventuelt installere en av følgende forutsetninger. Vær imidlertid oppmerksom på at disse alternative gir en mer begrenset ER målet opplevelse.

-   Microsoft Dynamics-365 for operasjoner programversjon 7.0.1 (mai 2016)
-   [Hurtigreparasjonen for program](https://fix.lcs.dynamics.com/issue/results/?q=3160213) for administrasjon av mål for elektronisk rapportering

Du kan definere mål bare for ER-konfigurasjoner som er importert, og formater som er tilgjengelige på siden **Elektroniske rapporteringskonfigurasjoner**.

## <a name="overview"></a>Oversikt
ER målet management-funksjonalitet er tilgjengelig på **organisasjonsadministrasjon**&gt;**elektronisk rapportering**. Her kan du overstyre standard virkemåte for en konfigurasjon. Importerte konfigurasjoner vises ikke her før du klikker **Ny** og deretter velger du en konfigurasjon å opprette innstillinger for i feltet **Referanse**.

[![Hvis du velger en konfigurasjon i feltet referanse](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Når du har opprettet en referanse, kan du opprette et mål for hver mappe eller en fil. 

[![Opprette et mål](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Obs! ** Du kan opprette ett filmål for hver utdatakomponent med samme format, for eksempel en mappe eller en fil som velges i **Filnavn**-feltet. Du kan aktivere og deaktivere individuelle mål for målfilen i den **målet innstillinger** dialogboks. **Innstillinger**-knappen brukes til å kontrollere alle mål for et valgt filmål. I dialogboksen **Innstillinger for mål** kan du kontrollere hver målet separat ved å sette alternativet **Aktivert** for det.

[![Dialogboksen Innstillinger for mål](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Måltyper
Forskjellige måltyper støttes. Du kan deaktivere eller aktivere alle typer samtidig. På denne måten kan du enten ikke gjør noe eller sende komponenten til alle konfigurerte mål. Avsnittene nedenfor beskriver målene som støttes.

### <a name="email-destination"></a>E-postmål

Sett **Aktivert **til **Ja** for å sende en utdatafil via e-post. Når dette alternativet er aktivert, kan du angi e-postmottakere, og Rediger emnet og meldingsteksten i e-postmeldingen. Du kan definere konstant tekster for e-postemnet og meldingsteksten, eller du kan bruke ER formler for dynamisk å opprette e-tekster. Du kan konfigurere e-postadresser for ER på to måter. Konfigurasjonen kan fullføres på samme måte som funksjonen for behandling av Skriv ut i Dynamics 365 for operasjoner fullfører den. Du kan eventuelt løse en e-postadresse ved å bruke en direkte referanse til konfigurasjonen ER gjennom en formel.

### <a name="email-address-types"></a>E-adressetyper

Når du klikker **Rediger** for det **til** eller **kopi** -feltet i **e-post til** vises. Du kan deretter velge hvilken type e-postadressen som skal brukes.

[![E-post til dialogboksen](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Utskriftsbehandling

Hvis du velger den **e-post for utskriftsbehandling** type, kan du angi fast e-postadresser i den **til** feltet. Hvis du vil bruke e-postadresser som ikke er løst, må du velge kildetypen e-post for et mål. Følgende verdier støttes: **kunden**, **leverandør**, **kundeemne**, **kontakt**, **konkurrent**, **arbeider**, **søker**, **potensiell leverandør**, og **ikke tillatt leverandør**. Når du har valgt Kildetype en e-post, bruker du knappen ved siden av **e-postkonto kilde** feltet for å åpne den ** formelen designer ** skjemaet. Du kan bruke dette skjemaet til å knytte en formel som representerer valgte parten-konto til e-post-målet.

[![Konfigurer utskriftsbehandling e-type](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Legg merke til at formler er spesifikke for ER-konfigurasjonen. Angi en dokumentspesifikk referanse til en kunde- eller leverandørparttype i **Formel**-feltet. I stedet for å skrive inn kan du finne en datakildenode som representerer kunde- eller leverandørkontoen, og deretter klikke **Legg til datakilde** for å oppdatere formelen. Hvis du for eksempel bruker konfigurasjonen ISO 20022 Kredittoverføring, er noden som representerer en leverandørkonto **'$PaymentsForCoveringLetter'. Creditor.Identification.SourceID**. Du kan eventuelt angi en hvilken som helst strengverdi, for eksempel **DE-001**, for å lagre en formel.

[![Formula designer](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

I den **e-post til** -dialogboksen, klikker du på Papirkurv bin Neste for å den **e-postkonto kilde** -feltet for å slette formelen for kildekontoen e-post. Du kan også åpne formeldesigner Hvis du vil endre en formel som tidligere ble lagret. Hvis du vil tildele e-postadresser, klikker du **redigere** å åpne den **tildele e-postadresser** dialogboks.

[![Tildele e-postadresser for en e-post-mål](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>E-post for konfigurasjon

Bruk denne e-post hvis konfigurasjonen du bruker, har en node i datakildene som representerer en e-postadresse. Du kan bruke datakilder og funksjoner i formelen designer til å få en riktig formatert e-postadresse.

[![Tilordne en e-postadresse datakilde for en e-post-mål](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Obs! ** En SMTP-server (Simple Mail Transfer Protocol) må være konfigurert og tilgjengelig. Du kan angi SMTP-serveren i Dynamics 365 for operasjoner, på **systemadministrasjon**&gt;**Setup**&gt;**e-post**&gt;**e-parametere**.

### <a name="archive-destination"></a>Arkivmål

Du kan bruke dette alternativet for å sende utdata til en Microsoft SharePoint-mappe eller Microsoft Azure Storage. Sett **Aktivert** til **Ja **for å sende utdata til et mål som er definert av den valgte dokumenttypen. Bare dokumenttyper der gruppen er satt til **Fil** er tilgjengelige for valg. Du definerer dokumenttyper ved **organisasjonsadministrasjon**&gt;**dokumentbehandling**&gt;**dokumenttyper som**. Konfigurasjonen for ER-mål er den samme som konfigurasjonen for systemet for dokumentbehandling.

[![Typer dokumentside](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Plasseringen bestemmer hvor filen lagres. Etter det **arkiv** mål er aktivert, kan resultatene av kjøringen av konfigurasjonen kan lagres i arkivet for jobben. Du kan vise resultatene på **organisasjonsadministrasjon**&gt;**elektronisk rapportering**&gt;**elektronisk rapportering arkivert jobber**. **Merk:** kan du velge en dokumenttype for jobb-arkiv i Dynamics 365 for operasjoner, på **organisasjonsadministrasjon**&gt;**arbeidsområder**&gt;**elektronisk rapportering**&gt;**elektronisk rapportering parametere**.

#### <a name="sharepoint"></a>SharePoint

Du kan lagre en fil i en bestemt SharePoint-mappe. Du definerer standard SharePoint-server på **organisasjonsadministrasjon**&gt;**dokumentbehandling**&gt;**Dokumentstyringsparametere**, på den **SharePoint** i kategorien. Når SharePoint-mappen er konfigurert, kan du velge den som mappen der ER utdataene lagres for dokumenttypen. 

[![Hvis du velger en SharePoint-mappe](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure Storage

Når type dokumentplasseringen er satt til **Arkivkatalog**, kan du lagre en fil i Azure Storage.

### <a name="file-destination"></a>Filmål

Hvis du setter **aktivert** til **Ja**, en åpne eller lagre-dialogboksen vises når konfigurasjonen er ferdig.

### <a name="screen-destination"></a>Målet for skjermen

Hvis du setter **aktivert** til **Ja**, opprettes det en forhåndsvisning av utdata. Du kan vise enkelte filtyper, for eksempel XML-, TXT- eller PDF-filen direkte i et leservindu. For andre filtyper, for eksempel Microsoft Excel eller Word, benyttes Microsoft Office Online tjenesten.

### <a name="power-bi-destination"></a>Power BI-mål

Angi **aktivert** til **Ja** du bruker ER konfigurasjonen til å ordne data kan overføres fra din forekomst av Dynamics 365 for operasjoner i Microsoft Power BI-tjenester. De overførte filene er lagret på en Microsoft SharePoint Server-forekomst som må være konfigurert for dette formålet. Hvis du vil ha mer informasjon, se [bruke en elektronisk rapportering konfigurasjon strøm BI med data fra Dynamics 365 for operasjoner](general-electronic-reporting-report-configuration-get-data-powerbi.md). **Tips:** Hvis du vil overstyre standard virkemåte (det vil si i dialogboksen for konfigurasjon), kan du opprette en målreferanse og et filmål for den primære utdatakomponenten, og deretter deaktivere alle mål.

## <a name="security-considerations"></a>Sikkerhetshensyn
To typer rettigheter og plikter brukes for ER-mål. Én type styrer muligheten til å opprettholde de generelle mål som er konfigurert for en juridisk enhet (det vil si den kontrollerer tilgang til den **elektronisk rapportering mål** side). Den andre typen styrer en muligheten for et program til å overstyre ved kjøretid, målinnstillingene som er konfigurert av en ER-utvikler eller ER-funksjonskonsulent.

| Rolle (AOT-navn)                     | Rollenavn                                  | Plikt (AOT-navn)                     | Pliktnavn                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Utvikler av elektronisk rapportering             | ERFormatDestinationConfigure        | Konfigurer mål for elektronisk rapporteringsformat                |
| ERFunctionalConsultant              | Funksjonell konsulent for elektronisk rapportering | ERFormatDestinationConfigure        | Konfigurer mål for elektronisk rapporteringsformat                |
| PaymAccountsPayablePaymentsClerk    | Leverandørbetalingsassistent            | ERFormatDestinationRuntimeConfigure | Konfigurer mål for elektronisk rapporteringsformat under kjøretid |
| PaymAccountsReceivablePaymentsClerk | Kundebetalingsassistent         | ERFormatDestinationRuntimeConfigure | Konfigurer mål for elektronisk rapporteringsformat under kjøretid |

**Obs! ** To rettigheter brukes i de forrige pliktene. Disse rettighetene har samme navn som tilsvarende plikter: **ERFormatDestinationConfigure** og **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Vanlige spørsmål
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Jeg har importert elektroniske konfigurasjoner, og jeg kan se dem på siden Elektroniske rapporteringskonfigurasjoner. Men Hvorfor ser jeg dem på siden for elektronisk rapportering mål?

Pass på at du klikker **ny**, og velg deretter en konfigurasjon i den **referanse** feltet. På siden **Mål for elektronisk rapportering** kan du bare vise konfigurasjoner som det er konfigurert mål for.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Er det mulig å definere hvilke Azure lagring konto og Azure Blob-lager skal brukes?

Nr. Standard Azure Blob-lagring som er definert og brukes for dokumentbehandlingssystemet brukes.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Hva er formålet med filen målet i mål-innstillingene? Hva gjør innstillingen?

**Fil**-målet brukes til å styre en dialogboks. Hvis du aktiverer dette målet, eller hvis ingen mål som er definert for en konfigurasjon, kan du se en åpen eller dialogboksen Lagre etter en utdatafil er opprettet.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Kan du gi et eksempel på en formel som refererer til en leverandørkonto som jeg kan sende e-post til?

Formelen er spesifikk for ER-konfigurasjonen. Hvis du for eksempel bruker konfigurasjonen ISO 20022 Kredittoverføring, kan du bruke **'$PaymentsForCoveringLetter'. Creditor.Identification.SourceID** eller **modell. Payments.Creditor.Identification.SourceID** for å hente en tilknyttet leverandørkonto.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>En av mine formatkonfigurasjoner inneholder flere filer som er gruppert i én mappe (Mappe1 inneholder for eksempel Fil1, Fil2 og Fil3). Hvordan konfigurerer jeg mål slik at Mappe1.ZIP ikke opprettes i det hele tatt, Fil1 sendes via e-post, Fil2 sendes til SharePoint og jeg kan åpne Fil3 umiddelbart etter at konfigurasjonen er kjørt?

Forutsetningen er at formatet må være tilgjengelig i konfigurasjonene ER. Hvis du har formatet, åpner du siden **Mål for elektronisk rapportering**, og oppretter en ny referanse til denne konfigurasjonen. Deretter må du ha fire filmål, ett for hver utdatakomponent. Opprette første filmålet, gi det et navn, for eksempel **Mappe**, og velg et filnavn som representerer en mappe i konfigurasjonen. Klikk deretter **Innstillinger**, og kontroller at alle mål er deaktivert. Mappen opprettes ikke for dette filmålet. Som standard, på grunn av hierarkiske avhengigheter mellom filer og overordnede mapper, vil filer fungere på samme måte. Med andre ord, de blir ikke sendt noe sted. Hvis du vil overstyre denne standard virkemåten, må du opprette tre filmål til, ett for hver fil. Du må aktivere målet som filen skal sendes til i målinnstillingene for hver av dem.

# <a name="see-also"></a>Se også

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)



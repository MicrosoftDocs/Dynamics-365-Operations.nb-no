---
title: "Mål for elektronisk rapportering"
description: "Du kan konfigurere et mål for hver formatkonfigurasjon for elektronisk rapportering (ER) og utdatakomponenten (en mappe eller en fil). Brukere som er gitt riktige tilgangsrettigheter kan også endre målinnstillingene ved kjøretid. Denne artikkelen beskriver administrasjon av mål for elektronisk rapportering, måltyper som støttes og sikkerhetsvurderinger."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: fb2aeee1f38823e7ea96071f773e8448d65ba8ff
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017


---

# Mål for elektronisk rapportering
<a id="electronic-reporting-destinations" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Du kan konfigurere et mål for hver formatkonfigurasjon for elektronisk rapportering (ER) og utdatakomponenten (en mappe eller en fil). Brukere som er gitt riktige tilgangsrettigheter kan også endre målinnstillingene ved kjøretid. Denne artikkelen beskriver administrasjon av mål for elektronisk rapportering, måltyper som støttes og sikkerhetsvurderinger.

Formatkonfigurasjoner for elektronisk rapportering (ER) inneholder vanligvis minst én utdatakomponent: en fil. Konfigurasjoner inneholder vanligvis flere filutdatakomponenter av forskjellige typer (for eksempel XML, TXT eller XLSX) som er gruppert i én eller flere mapper. Administrasjon av mål for elektronisk rapportering lar deg forhåndsdefinere hva som skjer når hver komponent kjøres. Når en konfigurasjon kjøres, vises det som standard en dialogboks for brukeren som kan brukes til å lagre eller åpne filen. Den samme virkemåten brukes også når du importerer en ER-konfigurasjon og ikke konfigurerer noen bestemte mål for den. Når et mål opprettes for en hovedutdatakomponent, overstyrer dette målet standard virkemåte, og mappen eller filen sendes i henhold til innstillingene for målet.

## Tilgjengelighet og generelle forutsetninger
<a id="availability-and-general-prerequisites" class="xliff"></a>
ER-målfunksjonaliteten er ikke tilgjengelig i Microsoft Dynamics AX 7.0 (februar 2016). Derfor må du installere Microsoft Dynamics 365 for Operations versjon 1611 (november 2016) for å bruke alle funksjonene som er beskrevet i dette emnet. Du kan også installere én av følgende forutsetninger. Vær imidlertid oppmerksom på at disse alternativene gir en mer begrenset ER-målopplevelse.

-   Microsoft Dynamics AX-applikasjonsobjekt 7.0.1 (mai 2016)
-   [Hurtigreparasjonen for program](https://fix.lcs.dynamics.com/issue/results/?q=3160213) for administrasjon av mål for elektronisk rapportering

Du kan definere mål bare for ER-konfigurasjoner som er importert, og formater som er tilgjengelige på siden **Elektroniske rapporteringskonfigurasjoner**.

## Oversikt
<a id="overview" class="xliff"></a>
Funksjonen for administrasjon av elektronisk rapportering er tilgjengelig på **Organisasjonsstyring** &gt; **Elektronisk rapportering**. Her kan du overstyre standard virkemåte for en konfigurasjon. Importerte konfigurasjoner vises ikke her før du klikker **Ny** og deretter velger du en konfigurasjon å opprette innstillinger for i feltet **Referanse**.

[![Velge en konfigurasjon i referansefeltet](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Når du har opprettet en referanse, kan du opprette et mål for hver mappe eller for en fil. 

[![Opprette et filmål](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Obs!** Du kan opprette ett filmål for hver utdatakomponent med samme format, for eksempel en mappe eller en fil som velges i **Filnavn**-feltet. Du kan deretter aktivere og deaktivere enkeltmål for filmålet separat i dialogboksen **Innstillinger for mål**. **Innstillinger**-knappen brukes til å kontrollere alle mål for et valgt filmål. I dialogboksen **Innstillinger for mål** kan du kontrollere hver målet separat ved å sette alternativet **Aktivert** for det.

[![Dialogboksen Innstillinger for mål](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## Måltyper
<a id="destination-types" class="xliff"></a>
Forskjellige måltyper støttes. Du kan deaktivere eller aktivere alle typer samtidig. På denne måten kan du enten ikke gjør noe eller sende komponenten til alle konfigurerte mål. Avsnittene nedenfor beskriver målene som støttes.

### E-postmål
<a id="email-destination" class="xliff"></a>

Sett **Aktivert** til **Ja** for å sende en utdatafil via e-post. Når dette alternativet er aktivert, kan du angi e-postmottakere og redigere emnet og brødteksten i e-postmeldingen. Du kan definere konstante tekster for e-postemnet og meldingsteksten, eller du kan bruke ER-formler for å opprette e-posttekster dynamisk. Du kan konfigurere e-postadresser for ER på to måter. Konfigurasjonen kan fullføres på samme måte som utskriftsbehandlingsfunksjonen i Finance and Operations fullfører den. Du kan eventuelt løse en e-postadresse ved å bruke en direkte referanse til ER-konfigurasjonen gjennom en formel.

### Typer e-postadresser
<a id="email-address-types" class="xliff"></a>

Når du klikker **Rediger** for **Til** eller **Kopi**-feltet, vises dialogboksen **E-post til**. Du kan deretter velge hvilken type e-postadresse som skal brukes.

[![Dialogboksen E-post til](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### Utskriftsbehandling
<a id="print-management" class="xliff"></a>

Hvis du velger typen **E-post for utskriftsbehandling**, kan du angi faste e-postadresser i **Til**-feltet. Hvis du vil bruke e-postadresser som ikke er faste, må du velge kildetypen e-post for et filmål. Følgende verdier støttes: **kunde**, **leverandør**, **kundeemne**, **kontakt**, **konkurrent**, **arbeider**, **søker**, **potensiell leverandør** og **sperret leverandør**. Når du har valgt en e-postkildetype, bruker du knappen ved siden av feltet **Kildekonto for e-post** til å åpne skjemaet **Formeldesigner **. Du kan bruke dette skjemaet til å knytte en formel som representerer den valgte partskontoen til e-postmålet.

[![Konfigurere e-posttypen for utskriftsbehandling](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Legg merke til at formler er spesifikke for ER-konfigurasjonen. Angi en dokumentspesifikk referanse til en kunde- eller leverandørparttype i **Formel**-feltet. I stedet for å skrive inn kan du finne en datakildenode som representerer kunde- eller leverandørkontoen, og deretter klikke **Legg til datakilde** for å oppdatere formelen. Hvis du for eksempel bruker konfigurasjonen ISO 20022 Kredittoverføring, er noden som representerer en leverandørkonto **'$PaymentsForCoveringLetter'. Creditor.Identification.SourceID**. Du kan eventuelt angi en hvilken som helst strengverdi, for eksempel **DE-001**, for å lagre en formel.

[![Formeldesigner](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

I dialogboksen **E-post til** klikker du på papirkurven ved siden av feltet **Kildekonto for e-post** for å slette formelen for kildekontoen for e-post permanent. Du kan også åpne formeldesigner for å endre en formel som tidligere ble lagret. Hvis du vil tilordne e-postadresser, klikker du **Rediger** for å åpne dialogboksen **Tilordne e-postadresser**.

[![Tilordne e-postadresser for et e-postmål](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### E-post for konfigurasjon
<a id="configuration-email" class="xliff"></a>

Bruk denne e-posttypen hvis konfigurasjonen du bruker, har en node i datakildene som representerer en e-postadresse. Du kan bruke datakilder og funksjoner i formeldesigner for å få en riktig formatert e-postadresse.

[![Tilordne en datakilde for en e-postadresse for et e-postmål](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Obs!** En SMTP-server (Simple Mail Transfer Protocol) må være konfigurert og tilgjengelig. Du kan angi SMTP-serveren i Finance and Operations på **Systemadministrasjon** &gt; **Oppsett** &gt; **E-post** &gt; **E-postparametere**.

### Arkivmål
<a id="archive-destination" class="xliff"></a>

Du kan bruke dette alternativet for å sende utdata til en Microsoft SharePoint-mappe eller Microsoft Azure Storage. Sett **Aktivert** til **Ja** for å sende utdata til et mål som er definert av den valgte dokumenttypen. Bare dokumenttyper der gruppen er satt til **Fil** er tilgjengelige for valg. Du definerer dokumenttyper under **Organisasjonsstyring** &gt; **Dokumentbehandling** &gt; **Dokumenttyper**. Konfigurasjonen for ER-mål er den samme som konfigurasjonen for systemet for dokumentbehandling.

[![Siden Dokumenttyper](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Plasseringen bestemmer hvor filen lagres. Etter at **Arkiv**-målet er aktivert, kan resultatene av konfigurasjonskjøringen lagres i jobbarkivet. Du kan vise resultatene på **Organisasjonsstyring** &gt; **Elektronisk rapportering** &gt; **Arkiverte jobber for elektronisk rapportering**. **Merk:** Du kan velge en dokumenttype for jobbarkivet i Finance and Operations, på **Organisasjonsstyring** &gt; **Arbeidsområder** &gt; **Elektronisk rapportering** &gt; **Parametere for elektronisk rapportering**.

#### SharePoint
<a id="sharepoint" class="xliff"></a>

Du kan lagre en fil i en bestemt SharePoint-mappe. Du definerer standard SharePoint-server på **Organisasjonsstyring** &gt; **Dokumentbehandling** &gt; **Parametere for dokumentstyring**, i kategorien **SharePoint**. Når SharePoint-mappen er konfigurert, kan du velge den som mappen der ER-utdataene lagres for dokumenttypen. 

[![Velge en SharePoint-mappe](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### Azure Storage
<a id="azure-storage" class="xliff"></a>

Når type dokumentplasseringen er satt til **Arkivkatalog**, kan du lagre en fil i Azure Storage.

### Filmål
<a id="file-destination" class="xliff"></a>

Hvis du angir **Aktivert** til **Ja**, vises en dialogboks for åpning eller lagring når konfigurasjonen er ferdig.

### Skjermmål
<a id="screen-destination" class="xliff"></a>

Hvis du setter **Aktivert** til **Ja**, opprettes det en forhåndsvisning av utdata. Du kan vise enkelte filtyper, for eksempel XML, TXT eller PDF, direkte i et leservindu. For andre filtyper, for eksempel Microsoft Excel eller Word, benyttes Microsoft Office Online-tjenesten.

### Power BI-mål
<a id="power-bi-destination" class="xliff"></a>

Sett **Aktivert** til **Ja** for å bruke ER-konfigurasjonen for å ordne overføring av data fra din forekomst av Finance and Operations til Microsoft Power BI-tjenester. De overførte filene lagres på en Microsoft SharePoint-serverforekomst som må konfigureres for dette formålet. Se [Bruk en elektronisk rapporteringskonfigurasjon til å forsyne Power BI med data fra Finance and Operations](general-electronic-reporting-report-configuration-get-data-powerbi.md) hvis du vil ha mer informasjon. **Tips:** Hvis du vil overstyre standard virkemåte (det vil si i dialogboksen for konfigurasjon), kan du opprette en målreferanse og et filmål for den primære utdatakomponenten, og deretter deaktivere alle mål.

## Sikkerhetshensyn
<a id="security-considerations" class="xliff"></a>
To typer rettigheter og plikter brukes for ER-mål. Én type styrer muligheten til å opprettholde de generelle målene som er konfigurert for en juridisk enhet (det vil si tilgang til siden **Mål for elektronisk rapportering**). Den andre typen styrer en muligheten for et program til å overstyre ved kjøretid, målinnstillingene som er konfigurert av en ER-utvikler eller ER-funksjonskonsulent.

| Rolle (AOT-navn)                     | Rollenavn                                  | Plikt (AOT-navn)                     | Pliktnavn                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Utvikler av elektronisk rapportering             | ERFormatDestinationConfigure        | Konfigurer mål for elektronisk rapporteringsformat                |
| ERFunctionalConsultant              | Funksjonell konsulent for elektronisk rapportering | ERFormatDestinationConfigure        | Konfigurer mål for elektronisk rapporteringsformat                |
| PaymAccountsPayablePaymentsClerk    | Leverandørbetalingsassistent            | ERFormatDestinationRuntimeConfigure | Konfigurer mål for elektronisk rapporteringsformat under kjøretid |
| PaymAccountsReceivablePaymentsClerk | Kundebetalingsassistent         | ERFormatDestinationRuntimeConfigure | Konfigurer mål for elektronisk rapporteringsformat under kjøretid |

**Obs!** To rettigheter brukes i de forrige pliktene. Disse rettighetene har samme navn som tilsvarende plikter: **ERFormatDestinationConfigure** og **ERFormatDestinationRuntimeConfigure**.

## Vanlige spørsmål
<a id="frequently-asked-questions" class="xliff"></a>
### Jeg har importert elektroniske konfigurasjoner, og jeg kan se dem på siden Elektroniske rapporteringskonfigurasjoner. Hvorfor jeg kan ikke se dem på siden Mål for elektronisk rapportering?
<a id="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page" class="xliff"></a>

Pass på at du klikker **Ny** og velger en konfigurasjon i feltet **Referanse**. På siden **Mål for elektronisk rapportering** kan du bare vise konfigurasjoner som det er konfigurert mål for.

### Er det mulig å definere hvilken Azure Storage-konto og Azure Blob Storage som brukes?
<a id="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used" class="xliff"></a>

Nr. Standard Azure Blob Storage som er definert og brukes for dokumentbehandlingssystemet, brukes.

### Hva er formålet med filmålet i målinnstillingene? Hva gjør innstillingen?
<a id="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do" class="xliff"></a>

**Fil**-målet brukes til å styre en dialogboks. Hvis du aktiverer dette målet, eller hvis ingen mål er definert for en konfigurasjon, vises en dialogboks for lagring eller åpning når en utdatafil er opprettet.

### Kan du gi et eksempel på en formel som refererer til en leverandørkonto som jeg kan sende e-post til?
<a id="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to" class="xliff"></a>

Formelen er spesifikk for ER-konfigurasjonen. Hvis du for eksempel bruker konfigurasjonen ISO 20022 Kredittoverføring, kan du bruke **'$PaymentsForCoveringLetter'. Creditor.Identification.SourceID** eller **modell. Payments.Creditor.Identification.SourceID** for å hente en tilknyttet leverandørkonto.

### En av mine formatkonfigurasjoner inneholder flere filer som er gruppert i én mappe (Mappe1 inneholder for eksempel Fil1, Fil2 og Fil3). Hvordan konfigurerer jeg mål slik at Mappe1.ZIP ikke opprettes i det hele tatt, Fil1 sendes via e-post, Fil2 sendes til SharePoint og jeg kan åpne Fil3 umiddelbart etter at konfigurasjonen er kjørt?
<a id="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run" class="xliff"></a>

Forutsetningen er at formatet må være tilgjengelig i ER-konfigurasjoner. Hvis du har formatet, åpner du siden **Mål for elektronisk rapportering**, og oppretter en ny referanse til denne konfigurasjonen. Deretter må du ha fire filmål, ett for hver utdatakomponent. Opprette første filmålet, gi det et navn, for eksempel **Mappe**, og velg et filnavn som representerer en mappe i konfigurasjonen. Klikk deretter **Innstillinger**, og kontroller at alle mål er deaktivert. Mappen opprettes ikke for dette filmålet. Som standard, på grunn av hierarkiske avhengigheter mellom filer og overordnede mapper, vil filer fungere på samme måte. Med andre ord, de blir ikke sendt noe sted. Hvis du vil overstyre denne standard virkemåten, må du opprette tre filmål til, ett for hver fil. Du må aktivere målet som filen skal sendes til i målinnstillingene for hver av dem.

# Se også
<a id="see-also" class="xliff"></a>

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)





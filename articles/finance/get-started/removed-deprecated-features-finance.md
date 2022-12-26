---
title: Fjernede eller avskrevne funksjoner i Dynamics 365 Finance
description: Denne artikkelen beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Finance.
author: kfend
ms.date: 10/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 25d13aa26565e5753b87c843b43cf46f8276b642
ms.sourcegitcommit: 6c05bcd27e6ee72f01cb66e2cfd1e929e0365830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/16/2022
ms.locfileid: "9854086"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Fjernede eller avskrevne funksjoner i Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Finance.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging. 

> [!NOTE]
> Detaljert informasjon om objekter i økonomi- og driftsapper finnes i [Tekniske referanserapporter](/dynamics/s-e/global/axtechrefrep_61). Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av økonomi- og driftsapper.

## <a name="features-removed-or-deprecated-in-the-finance-10031-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.31

### <a name="edifact-paymul-at-configuration-under-payment-model"></a>EDIFACT PAYMUL (AT)-konfigurasjon under Betalingsmodell

| &nbsp;  | &nbsp;  |
|---|---|
| **Årsak til avskrivning/fjerning** | Erstattes med et nytt format som er basert på ISO 20022 pain.001.001.09. | 
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Program |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Banker i Østerrike vil avskrive EDICFACT-PAYMUL for betalinger over grenser innen november 2022 og vil erstatte den med XML-versjon pain.001.001.09N. Det er lagt til en ny konfigurasjon under det globale konfigurasjonsrepositoriet som gjør det mulig for brukere å fullføre betalingsforespørselen over grenser. |

## <a name="features-removed-or-deprecated-in-the-finance-10030-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.30

### <a name="revenue-recognition"></a>Inntektsføring

[Inntektsføring](../../finance/accounts-receivable/revenue-recognition-overview.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Årsak til avskrivning/fjerning** |Erstattet av den forbedrede funksjonaliteten [Abonnementsfakturering](../../finance/accounts-receivable/subscription-billing-summary.md)
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder** | Program |
| **Distribusjonsalternativ** | Alle |
| **Status** | Avskrevet: Etter april 2023 blir ikke lenger funksjonen Inntektsføring i Dynamics 365 Finance støttet med feilrettinger. Kunder blir bedt om å bruke den forbedrede funksjonaliteten [Abonnementsfakturering](../../finance/accounts-receivable/subscription-billing-summary.md). I oktober 2023 slutter funksjonen Inntektsføring å være tilgjengelig. Kunder blir bedt om å gå over til den forbedrede funksjonaliteten Abonnementsfakturering. For buntfunksjonen som en del av inntektsføringe er det ikke planlagt noen erstatningsfunksjonalitet på dette tidspunktet.|

## <a name="features-removed-or-deprecated-in-the-finance-10029-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.29

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Lageroverføringsordrer som har avgift på overføringsprisen

[Lageroverføringsordrer som har avgift på overføringsprisen](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Årsak til avskrivning/fjerning** | Erstattet av forbedret funksjonalitet, [Lageroverføringsordrer for India](../../finance/localizations/apac-ind-stock-transfer.md)|
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder** | Program |
| **Distribusjonsalternativ** | Alle |
| **Status** | Avskrevet: Etter april 2023 vil ikke funksjonen **Lageroverføringsordrer som har avgift på overføringspris** lenger motta kundestøtte med feilrettinger og sikkerhetsreparasjon. Kunder blir bedt om å bruke den forbedrede funksjonaliteten [Lageroverføringsordrer for India](../../finance/localizations/apac-ind-stock-transfer.md). Etter oktober 2023 er ikke funksjonen **Lageroverføringsordrer som har avgift på overføringspris** lenger tilgjengelige, og kunder blir bedt om å flytte til den forbedrede funksjonen. |

### <a name="bank-statement-import-and-export-of-positive-pay-file"></a>Import og eksport av positiv lønnsfil for bankkontoutdrag

| &nbsp;  | &nbsp;  |
|---|---|
| **Årsak til avskrivning/fjerning** |Erstattes av forbedret funksjonalitet, importer bankkontoutdrag og eksporter positive lønnsfiler.| 
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Program |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: XSLT-funksjonaliteten for import og eksport av filer vil ikke lenger få støtte med feilrettinger og sikkerhetsrettinger. Kundene blir bedt om å bruke den forbedrede funksjonen: [Definer positive lønnsfiler ved hjelp av elektronisk rapportering](../../finance/accounts-payable/set-up-positive-pay-er.md) og [Definer avansert bankavstemming ved hjelp av elektronisk rapportering](../../finance/accounts-payable/import-bai2-er.md). Etter september 2022 vil ikke XSLT-funksjonaliteten lenger være tilgjengelig, og kunder blir bedt om å flytte til den forbedrede funksjonaliteten.|


## <a name="features-removed-or-deprecated-in-the-finance-10026-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.26

### <a name="sales-tax-report-for-finland-design-based-on-reporting-codes"></a>Rapport for mva-betaling for Finland (utforming basert på rapporteringskoder)

[Mva-rapport for Finland](../localizations/emea-fin-sales-tax-payment-report-finland.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet med en ny mva-deklareringsutforming, [mva-deklarering for Finland](../localizations/emea-fin-vat-declaration.md). |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Program |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Innen 1. mars 2023 planlegger vi å ikke lenger å støtte mva-rapporten for Finland (finsk rapportoppsett). Nye ER-formater for **MVA-deklarering XML (FI**) og **MVA-deklarering Excel (FI)** introduseres under **Avgiftsdeklarering**-modellen. |

## <a name="features-removed-or-deprecated-in-the-finance-10024-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.24

### <a name="sales-tax-report-for-sweden-design-based-on-reporting-codes"></a>Rapport for mva-betaling for Sverige (utforming basert på rapporteringskoder)

[Mva-rapport for Sverige](../localizations/emea-swe-sales-tax-payment-report-sweden.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet med en ny mva-deklareringsutforming, [mva-deklarering for Sverige](../localizations/emea-swe-vat-declaration-sweden.md) |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Program |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Innen 1. desember 2022 planlegger vi å ikke lenger å støtte mva-rapporten for Sverige (svensk rapportoppsett). Nye ER-formater for **MVA-deklarering XML (SE**) og **MVA-deklarering Excel (SE)** introduseres under **Avgiftsdeklarering**-modellen. |

### <a name="vat-statement-for-austria-design-based-on-reporting-codes"></a>Mva-oppgave for Østerrike (utforming basert på rapporteringskoder)

[Mva-oppgavedetaljer for Østerrike](../localizations/emea-aut-vat-statement-details.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet med en ny mva-deklareringsutforming, [mva-deklarering for Østerrike](../localizations/emea-aut-vat-declaration-austria.md) |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Program |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Innen 1. desember 2022 planlegger vi ikke lenger å støtte ER-formatet **Mva-deklarering (AT)** under **MVA-deklarasjonsmodell**. Nye formater for **MVA-deklarering XML (AT)** og **MVA-deklarering Excel (AT)** introduseres under **Avgiftsdeklarering**-modellen. |

### <a name="elster-declaration-for-germany-design-based-on-reporting-codes-electronic-tax-declaration-log-menu-item-and-page-electronic-tax-declaration-setup-menu-item-and-page-german-report-layout-taxreport_de-ssrs-format"></a>ELSTER-deklarering for Tyskland (utforming basert på rapporteringskoder), \"Logg for elektronisk avgiftsdeklarering\"-menyelement og side, \"Oppsett for elektronisk avgiftsdeklarering\"-menyelement og side, tysk rapportoppsett (TaxReport_DE) SSRS-format

[Mva-oppgave](../localizations/emea-de-vat-declaration.md)</br>
[Oppsett for elektronisk avgiftsdeklarering for Tyskland](../../fin-ops-core/dev-itpro/analytics/tasks/setup-electronic-tax-declaration-germany.md)</br>

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet med en ny mva-deklareringsutforming, [mva-deklarering for Tyskland](../localizations/emea-deu-vat-declaration-germany.md) |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Program |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Innen 1. desember 2022 vil vi ikke lenger støtte det elektroniske rapporteringsformatet (ER) **Elster (DE)** og **Elster-modell**. Nye ER-formater for **MVA-deklarering XML (DE)** og **MVA-deklarering Excel (DE)** introduseres under **Avgiftsdeklarering**-modellen. Vi støtter heller ikke lenger menyelement og side **Avgift** \> **Deklareringer** \> **Merverdiavgift** \> **Logg for elektronisk avgiftsdeklarering**, menyelement og side **Avgift** \> **Oppsett** \> **Merverdiavgift** \> **Oppsett for elektronisk avgiftsdeklarering**, menyelement og side **Avgift** \> **Oppsett** \> **Merverdiavgift** \> **Elektroniske avgiftssertifikater** og det tyske rapportoppsettet (TaxReport\_DE) SQL Server Reporting Services-formatet (SSRS). Prosessen med mva-rapportering i Tyskland støttes i funksjonaliteten [Elektroniske meldinger](../general-ledger/electronic-messaging.md). Hvis du vil ha mer informasjon, kan du se [Mva-deklarering for Tyskland](../localizations/emea-deu-vat-declaration-germany.md). |

### <a name="ob-declaration-for-netherlands-design-based-on-reporting-codes-electronic-ob-declaration-menu-item-and-page-dutch-report-layout-taxreport_nl-ssrs-format"></a>OB-deklarering for Nederland (utforming basert på rapporteringskoder), menyelement og side \"Elektronisk OB-deklarering\", nederlandsk rapportoppsett (TaxReport_NL) SSRS-format

[OB-deklarering](../localizations/emea-nl-vat-declaration.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet med en ny mva-deklareringsutforming, [Mva-deklarering for Nederland](../localizations/emea-nl-vat-declaration-netherlands.md) |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Program |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Innen 1. desember 2022 vil vi ikke lenger å støtte ER-formatene (elektronisk rapportering) **OB-deklarering (NL)** og **OB-deklareringsmodell**. Nye ER-formater for **MVA-deklarering XML (NL)** og **MVA-deklarering Excel (NL)** introduseres under **Avgiftsdeklarering**-modellen. Vi støtter heller ikke lenger menyelement og side **Avgift** \> **Deklarering** \> **Merverdiavgift** \> **Elektronisk OB-deklarering** , og det nederlandske rapportoppsettet (TaxReport_NL) SSRS-format. Prosessen med mva-rapportering i Nederland støttes i funksjonaliteten [Elektroniske meldinger](../general-ledger/electronic-messaging.md). Hvis du vil ha mer informasjon, kan du se [Mva-deklarering for Nederland](../localizations/emea-nl-vat-declaration-netherlands.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.20

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a>Formatkonfigurasjon for elektronisk rapportering (ER) "RTIR-spørring om fakturadataforespørsel (HU)"

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Utelatt fra behandling av elektroniske meldinger for samhandling med ungarsk elektronisk faktureringssystem |
| **Erstattet med en annen funksjon?**   | Nei |
| **Berørte produktområder**         | Søknad |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Etter 15. april 2022 planlegger vi ikke lenger å støtte formatkonfigurasjonen "RTIR-spørring om fakturadataforespørsel (HU)". |

### <a name="french-fec-audit-file-electronic-reporting-er-format-for-france-under-german-audit-file-output-format"></a>Elektronisk rapportering-formatet for Frankrike "Fransk FEC-revisjonsfil" under formatet "Tysk revisjonsfilutdata"

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattes med nytt "FEC-revisjonsfil (FR)"-format |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Søknad |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Innen 1. mai 2022 planlegger vi å ikke lenger støtte det elektroniske rapporteringsformatet "Fransk FEC-revisjonsfil" under formatet "Tysk revisjonsfilutdata". Nytt FEC-revisjonsfil (FR)-format introduseres i stedet under "Dataeksportmodellen". |

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.17

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>LCS-repositorium som lagringsalternativ for elektroniske rapporteringskonfigurasjoner

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattes med det nye globale RCS-repositoriet (Regulatory Configuration Service) |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Dynamics 365 Finance, Supply Chain Management og Project Operations-produkter|
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Innen 1. april 2022 planlegger vi ikke lenger å støtte repositoriet Microsoft Dynamics Lifecycle Services (LCS) som et lagringsalternativ for ER-konfigurasjoner (Electronic Reporting). Nye Microsoft ER-konfigurasjoner blir publisert for nedlasting utelukkende fra det globale repositoriet. Du kan få tilgang til det globale repositoriet fra Dynamics 365-produktene og RCS. Hvis du vil ha mer informasjon, kan du se [Importere ER-konfigurasjoner fra RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) og [Regulatory Configuration Service – avskrivning av lager for Lifecycle Services](../localizations/rcs-lcs-repo-dep-faq.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.16

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>"MVA-deklarering (CZ)" og "Kontrolloppgaveeksport (CZ)" Formater for elektronisk rapportering for Den tsjekkiske republikk

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattes med nye formater |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Søknad |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Innen 22. januar 2022 planlegger vi å ikke lenger støtte formater for elektronisk rapportering for "MVA-deklarering (CZ)", "Kontrolloppgaveeksport (CZ)". Nye formater for MVA-deklarering XML (CZ), MVA-deklarering Excel (CZ), MVA-kontrolloppgave XML (CZ) introduseres i stedet under "Mvh-deklarering"-modellen. |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>"Format for eksport av finanstransaksjon (BE)" Elektronisk rapporteringsformat og tilsvarende "modell for eksport av finanstransaksjon (BE)" for Belgia

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet med nytt ER-format under modellen "Standard revisjonsfil (SAF-T)".  |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Søknad |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Per 1. desember 2021 planlegger vi å ikke lenger støtte "Format for eksport av finanstransaksjon (BE) Elektronisk rapporteringformat (ER) og respektive modell for eksport av finanstransaksjon (BE). Et nytt format av typen "Dataeksport i økonomimodul (BE)" sammen med "Tilordning av datamodell for økonomimodul" introduseres i stedet under modellen "Standard revisjonsfil (SAF-T)". |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>"VAT 100"-rapport for Storbritannia i SSRS-format

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet med nytt ER-format – "Mva-deklarering Excel (UK)"-formatet under "Mva-deklareringsmodell".  |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Søknad |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Per 1. desember 2021 planlegger vi å ikke lenger støtte "Mva 100-rapporten" i SSRS-format. Det ble introdusert et nytt "Mva-deklarering Excel (Storbritannia)"-format under "Mva-deklareringsmodell" i [MTD-mva-funksjonen](../localizations/emea-gbr-mtd-vat-integration.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-støtte for Dynamics 365 er avskrevet

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Fra og med desember 2020 er Microsoft Internet Explorer 11-støtte for alle Dynamics 365-produkter avskrevet, og Internet Explorer 11 støttes ikke etter august 2021.<br><br>Dette vil påvirke kunder som bruker Dynamics 365-produkter som er utformet for bruk via et Internet Explorer 11-grensesnitt. Etter august 2021 støttes ikke Internet Explorer 11 for slike Dynamics 365-produkter. |
| **Erstattet med en annen funksjon?**   | Vi anbefaler at kundene går over til Microsoft Edge.|
| **Berørte produktområder**         | Alle Dynamics 365-produkter |
| **Distribusjonsalternativ**              | Alle|
| **Status**                         | Avskrevet. Internet Explorer 11 støttes ikke etter august 2021.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.12

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Ikke avskrevet: Polske SSRS-rapporter: register for utgående mva, register for inngående mva, sammendrag av mva-register for EU – funksjonsreferanser PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Ikke lovpålagt.  |
| **Erstattet med en annen funksjon?**   | Ja (Excel-format for standard revisjonsfil med mva-deklarering - JPK_VDEK) |
| **Berørte produktområder**         | Søknad |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Ikke avskrevet: Fra og med 27. april 2021 planlegger vi å fortsette å støtte SSRS-rapportene **: register for utgående mva, register for inngående mva, sammendrag av mva-register for EU – funksjonsreferanser PL-00014**. Excel-formateringseksempel for standard revisjonsfil med mva-deklarering (JPK_VDEK) er også introdusert. |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.11

### <a name="norwegian-standard-main-accounts"></a>Norske standard hovedkontoer

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Utform på nytt  |
| **Erstattet med en annen funksjon?**   | Ja (erstattet med programspesifikke parametere i ER-formatet) |
| **Berørte produktområder**         | Søknad |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: etter 1. april 2021 planlegger vi å ikke lenger støtte funksjonalitet relatert til standard hovedkontoer: referansefelt, relatert tabell, dataenhet. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.7

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialogboksen Endring av arbeidsflytforespørsel inneholder ikke lenger en rullegardinliste for brukervalg

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Endret til funksjonen med kontogruppevalg.  |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Arbeidsflyt |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Etter 1. desember 2020 planlegger vi å ikke lenger støtte kinesiske bilagstyper uten kontogruppevalg. Finne flere detaljer om den nye utformingen i [Hva er nytt i 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere kunngjøringer om fjernede eller avskrevne funksjoner
Hvis du vil lære mer om funksjoner som er fjernet eller avskrevet i tidligere versjoner, kan du se [Fjernede eller avskrevne funksjoner i tidligere versjoner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]


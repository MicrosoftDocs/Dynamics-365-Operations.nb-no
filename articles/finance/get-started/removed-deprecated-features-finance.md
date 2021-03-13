---
title: Funksjoner som er fjernet eller avskrevet i Dynamics 365 Finance
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7090a7461c7b77d74f081afd8f22db100cdf0792
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154183"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Funksjoner som er fjernet eller avskrevet i Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Finance.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging. 

> [!NOTE]
> Detaljert informasjon om objekter i Finance and Operations-apper finnes i [Tekniske referanserapporter](https://docs.microsoft.com/dynamics/s-e/). Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av Finance and Operations-apper.

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.16

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>"MVA-deklarering (CZ)" og "Kontrolloppgaveeksport (CZ)" Formater for elektronisk rapportering for Den tsjekkiske republikk

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattes med nye formater |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Søknad |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Innen 22. januar 2022 planlegger vi å ikke lenger støtte formater for elektronisk rapportering for "MVA-deklarering (CZ)", "Kontrolloppgaveeksport (CZ)". Nye formater for MVA-deklarering XML (CZ), MVA-deklarering Excel (CZ), MVA-kontrolloppgave XML (CZ) introduseres i stedet under "Mvh-deklarering"-modellen. |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>"Format for eksport av finanstransaksjon (BE)" Elektronisk rapporteringsformat og tilsvarende "modell for eksport av finanstransaksjon (BE)" for Belgia

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet med nytt ER-format under modellen "Standard revisjonsfil (SAF-T)".  |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Søknad |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Per 1. desember 2021 planlegger vi å ikke lenger støtte "Format for eksport av finanstransaksjon (BE) Elektronisk rapporteringformat (ER) og respektive modell for eksport av finanstransaksjon (BE). Et nytt format av typen "Dataeksport i økonomimodul (BE)" sammen med "Tilordning av datamodell for økonomimodul" introduseres i stedet under modellen "Standard revisjonsfil (SAF-T)". |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>"VAT 100"-rapport for Storbritannia i SSRS-format

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Erstattet med nytt ER-format – "Mva-deklarering Excel (UK)"-formatet under "Mva-deklareringsmodell".  |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Søknad |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Per 1. desember 2021 planlegger vi å ikke lenger støtte "Mva 100-rapporten" i SSRS-format. Det ble introdusert et nytt "Mva-deklarering Excel (Storbritannia)"-format under "Mva-deklareringsmodell" i [MTD-mva-funksjonen](../localizations/emea-gbr-mtd-vat-integration.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-støtte for Dynamics 365 er avskrevet

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Fra og med desember 2020 er Microsoft Internet Explorer 11-støtte for alle Dynamics 365-produkter avskrevet, og Internet Explorer 11 støttes ikke etter august 2021.<br><br>Dette vil påvirke kunder som bruker Dynamics 365-produkter som er utformet for bruk via et Internet Explorer 11-grensesnitt. Etter august 2021 støttes ikke Internet Explorer 11 for slike Dynamics 365-produkter. |
| **Erstattet med en annen funksjon?**   | Vi anbefaler at kundene går over til Microsoft Edge.|
| **Berørte produktområder**         | Alle Dynamics 365-produkter |
| **Distribusjonsalternativ**              | Alle|
| **Status**                         | Avskrevet. Internet Explorer 11 støttes ikke etter august 2021.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.12

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Polske SSRS-rapporter: register for utgående mva, register for inngående mva, sammendrag av mva-register for EU – funksjonsreferanser PL-00014

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Ikke lovpålagt.  |
| **Erstattet med en annen funksjon?**   | Ja (Excel-format for standard revisjonsfil med mva-deklarering - JPK_VDEK) |
| **Berørte produktområder**         | Søknad |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Innen 1. juli 2021 vi planlegger å ikke lenger kunne støtte SSRS-rapportene **: register for utgående mva, register for inngående mva, sammendrag av mva-register for EU – funksjonsreferanser PL-00014**. Excel-formateringseksempel for standard revisjonsfil med mva-deklarering (JPK_VDEK) blir introdusert i stedet. |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.11

### <a name="norwegian-standard-main-accounts"></a>Norske standard hovedkontoer

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Utform på nytt  |
| **Erstattet med en annen funksjon?**   | Ja (erstattet med programspesifikke parametere i ER-formatet) |
| **Berørte produktområder**         | Søknad |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: etter 1. april 2021 planlegger vi å ikke lenger støtte funksjonalitet relatert til standard hovedkontoer: referansefelt, relatert tabell, dataenhet. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Fjernede eller avskrevne funksjoner i Finance 10.0.7

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialogboksen Endring av arbeidsflytforespørsel inneholder ikke lenger en rullegardinliste for brukervalg
|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Endret til funksjonen med kontogruppevalg.  |
| **Erstattet med en annen funksjon?**   | Ja |
| **Berørte produktområder**         | Arbeidsflyt |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Etter 1. desember 2020 planlegger vi å ikke lenger støtte kinesiske bilagstyper uten kontogruppevalg. Finne flere detaljer om den nye utformingen i [Hva er nytt i 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere kunngjøringer om fjernede eller avskrevne funksjoner
Hvis du vil lære mer om funksjoner som er fjernet eller avskrevet i tidligere versjoner, kan du se [Fjernede eller avskrevne funksjoner i tidligere versjoner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).

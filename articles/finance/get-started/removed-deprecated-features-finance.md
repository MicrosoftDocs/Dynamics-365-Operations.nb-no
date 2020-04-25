---
title: Funksjoner som er fjernet eller avskrevet i Dynamics 365 Finance
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: aebce032d7d780b296ba74fea4467425a3cbe1a7
ms.sourcegitcommit: 4e9b3746790355f9f72bbfddc099c4065a49ad63
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/30/2020
ms.locfileid: "3175114"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Funksjoner som er fjernet eller avskrevet i Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Finance.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging. 

> [!NOTE]
> Detaljert informasjon om objekter i Finance and Operations-apper finnes i [Tekniske referanserapporter](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av Finance and Operations-apper.

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

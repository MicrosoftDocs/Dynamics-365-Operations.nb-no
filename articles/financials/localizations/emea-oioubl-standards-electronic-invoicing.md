---
title: "Standarder som støttes for elektronisk fakturering i Europa"
description: "Dette emnet forklarer dekningsnivået som finnes for elektronisk fakturering i Microsoft Dynamics 365 for Finance and Operations i den europeiske regionen."
author: mrolecki
manager: AnnBe
ms.date: 07/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10274
ms.search.region: Austria, Denmark, Italy, Norway, Spain, France, Belgium, Netherlands
ms.search.industry: 
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 354b9fd50dbd628b91fd4d77c4cb323ddc36428f
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="supported-standards-for-electronic-invoicing-in-europe"></a>Standarder som støttes for elektronisk fakturering i Europa

[!include [banner](../includes/banner.md)]

Dette emnet forklarer dekningsnivået som finnes for elektronisk fakturering for Europa. 

Implementering og bruk av elektronisk fakturering i hele EU er regulert [Council Directive 2010/45/EU](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), noe som påvirker alle EU-medlemsland. Bedrifter som ønsker å dra nytte av elektronisk fakturering må sende salgsordrefakturaer, fritekstfakturaer, prosjektfakturaer, salgsordre, kreditnotaer og prosjekt faktura kreditnotaer som XML-filer til den offentlig myndighet eller andre handelspartneren parter som kreve bruk av elektronisk fakturering. Disse XML-filer må oppfylle visse standarder. Landspesifikke behovene og implementeringen kan variere på tvers av EU-medlemsland, men de bruker ofte UNC Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) i forskjellige versjoner med tilpasninger i tillegg til [PEPPOL](http://www.peppol.eu) spesifikasjoner og tilgangspunkt for validering og transport. Primære fordelen med UBL er at forretningsdokumenter kan standardisert for ulike formål. Siden UBL er en fleksibel, internasjonal standard som støtter mange forretningskrav, kan disse forretningsdokumenter utveksles på tvers av landegrenser.

## <a name="what-electronic-invoice-formats-are-currently-available-in-finance-and-operations"></a>Hvilke formater for elektroniske fakturaer er tilgjengelige i Finance and Operations?

Følgende landspesifikke formater av elektroniske fakturaer er tilgjengelige:

-   OIOUBL v.2.02 for Danmark
-   EHF v.2.0.8 for Norge
-   PEPPOL BIS v.2 for Østerrike, Frankrike og Belgia
-   UBL-OHNL 1.9 for Nederland
-   FacturaE v.3.2.1 for Spania
-   FatturaPA v.1.2 for Italia

Elektronisk fakturering er basert på [elektronisk rapportering](../../dev-itpro/analytics/general-electronic-reporting.md). Det finnes en **Kundefakturamodell**-datamodell og et tallformat for landsspesifikke konfigurasjoner for elektronisk rapporteringsformat som er opprettet for Østerrike (AT), Danmark (DK), Italia (IT), Norge (NO), Spania (ES), Frankrike (FR), Belgia (BE) og Nederland (NL).

-   OIOUBL salgsfaktura - for AT, DK, og NO
-   OIOUBL salgskreditnota - for AT, DK, og NO
-   OIOUBL prosjektfaktura - for AT, DK, og NO
-   OIOUBL prosjektkreditnota - for AT, DK, og NO
-   UBL salgsfaktura FR
-   UBL salgskreditnota FR
-   UBL prosjektfaktura FR
-   UBL prosjektkreditnota FR
-   UBL salgsfaktura BE
-   UBL salgskreditnota BE
-   UBL prosjektfaktura BE
-   UBL prosjektkreditnota BE
-   UBL salgsfaktura NL
-   UBL salgskreditnota NL
-   UBL prosjektfaktura NL
-   UBL prosjektkreditnota NL 
-   Salgsfaktura (ES)
-   Salgsfaktura (IT)
-   Prosjektfaktura (ES)
-   Prosjektfaktura (IT)

De elektroniske fakturaene og kreditnotaene du genrerer, inneholder obligatorisk informasjon, for eksempel EAN-nummeret, ordrenummer, kontakt, dimensjonskontokode og adresseopplysninger for kunden. Valideringsregler brukes når fakturaer genereres, slik at du kan verifisere at riktig informasjon er angitt. Settet med nødvendig informasjon kan variere fra land til land. Siden både kravene og de støttede landene og formatene kan endres, bør du alltid gå til det delte ativabiblioteket i Microsoft Dynamics Lifecycle Services (LCS) og viser den mest oppdaterte listen over tilgjengelige filer som har aktivatypen **TYSK konfigurasjon**.

## <a name="additional-information"></a>Tilleggsinformasjon
Hvis du vil ha mer informasjon om hvordan du konfigurerer elektroniske fakturaer, kan du spille av følgende [Oppgaveveiledninger](../../fin-and-ops/get-started/help-overview.md#task-guides) i Hjelp-ruten:

 - Definere elektronisk fakturering for OIOUBL
 - Importere konfigurasjoner for elektroniske OIOUBL-faktureringer
 - Definere kundekontoer for elektronisk fakturering med OIOUBL

> [!NOTE] 
> Selv om disse oppgaveveiledningene ble opprettet for dansk spesifikt format for e-faktura *OIOUBL*, de som kan brukes av andre støttede land med mindre avvik.


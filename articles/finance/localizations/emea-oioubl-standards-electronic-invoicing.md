---
title: Standarder som støttes for elektronisk fakturering i Europa
description: Dette emnet forklarer dekningsnivået som finnes for elektronisk fakturering for Europa.
author: mrolecki
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 10274
ms.search.region: Austria, Denmark, Italy, Norway, Spain, France, Belgium, Netherlands
ms.search.industry: ''
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 7e5071e046c49847f5c11a1e258b0da506835c4daada4e96b463af0b2d70bda0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725984"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a>Standarder som støttes for elektronisk fakturering i Europa

[!include [banner](../includes/banner.md)]

Dette emnet forklarer dekningsnivået som finnes for elektronisk fakturering for Europa. 

Implementering og bruk av elektronisk fakturering i hele EU er regulert [Council Directive 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), noe som påvirker alle EU-medlemsland. Bedrifter som ønsker å dra nytte av elektronisk fakturering må sende salgsordrefakturaer, fritekstfakturaer, prosjektfakturaer, salgsordre, kreditnotaer og prosjekt faktura kreditnotaer som XML-filer til den offentlig myndighet eller andre handelspartneren parter som kreve bruk av elektronisk fakturering. Disse XML-filer må oppfylle visse standarder. Landspesifikke behovene og implementeringen kan variere på tvers av EU-medlemsland, men de bruker ofte UNC Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) i forskjellige versjoner med tilpasninger i tillegg til [PEPPOL](https://www.peppol.eu) spesifikasjoner og tilgangspunkt for validering og transport. Primære fordelen med UBL er at forretningsdokumenter kan standardisert for ulike formål. Siden UBL er en fleksibel, internasjonal standard som støtter mange forretningskrav, kan disse forretningsdokumenter utveksles på tvers av landegrenser.

## <a name="electronic-invoice-formats-currently-available-in-dynamics-365-finance"></a>Elektroniske fakturaformater er for øyeblikket tilgjengelige i Dynamics 365 Finance

Følgende landspesifikke formater av elektroniske fakturaer er tilgjengelige:

-   OIOUBL v.2.02 for Danmark
-   EHF v. 3.0 for Norge
-   PEPPOL BIS v.2 for Østerrike, Frankrike og Belgia
-   UBL-OHNL 1.9 for Nederland
-   FacturaE v.3.2.1 for Spania
-   FatturaPA v.1.2 for Italia
-   xRechnung v. 1.2 for Tyskland
-   Åpne PEPPOL BIS Billing v. 3.0 for den europeiske union
-   Estisk spesifikt format, versjon 1.2
-   Finvoice 3.0 for Finland

Elektronisk fakturering er basert på [elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md). En datamodell for **Fakturamodell**, fakturamodelltilordning og flere lands-/områdespesifikke ER-formatkonfigurasjoner er opprettet for følgende land/områder: 

- Østerrike (AT)
- Danmark (DK)
- Italia (IT)
- Norge (NO)
- Spania (ES)
- Frankrike (FR)
- Belgia (BE)
- Nederland (BE)
- Tyskland (DE)
- Estland (EE)
- Finland (FI)
- Den europeiske union (EU)

Datamodellen for **Fakturamodell**, fakturamodelltilordningen og de lands-/områdespesifikke ER-formatkonfigurasjonene omfatter følgende:

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
-   Salgsfaktura DE
-   Prosjektfaktura DE
-   Peppol-salgsfaktura - for EU
-   Peppol-salgskreditnota - for EU
-   Peppol-prosjektfaktura - for EU
-   Peppol-prosjektkreditnota - for EU
-   Salgsfaktura (EE)
-   Prosjektfaktura (EE)
-   Salgsfaktura (FI)
-   Prosjektfaktura (FI)

De elektroniske fakturaene og kreditnotaene du genrerer, inneholder obligatorisk informasjon, for eksempel EAN-nummeret, ordrenummer, kontakt, dimensjonskontokode og adresseopplysninger for kunden. Valideringsregler brukes når fakturaer genereres, slik at du kan verifisere at riktig informasjon er angitt. Settet med nødvendig informasjon kan variere fra land til land. Siden både kravene og de støttede landene og formatene kan endres, bør du alltid gå til det delte aktivabiblioteket i Microsoft Dynamics Lifecycle Services (LCS) og vise den mest oppdaterte listen over tilgjengelige filer som har aktivatypen **GER-konfigurasjon**.

## <a name="electronic-invoice-configuration"></a>Konfigurasjon av elektronisk faktura
Konfigurasjonen av og detaljene i elektroniske fakturaer avhenger av landet/området den er implementert for. Hvis du vil ha mer informasjon om hvordan du konfigurerer og bruker elektroniske fakturaer for kunder, kan du se de relaterte landsspesifikke emnene:

- [Italia](emea-ita-e-invoices.md)
- [Norge](emea-nor-e-invoices.md)
- [Tyskland](emea-deu-e-invoices.md)
- [Finland](https://support.microsoft.com/help/4559937)
- [Estland](https://support.microsoft.com/help/4552679)
- [PEPPOL](https://support.microsoft.com/help/4490320)

## <a name="additional-resources"></a>Tilleggsressurser
Hvis du vil ha mer informasjon om hvordan du konfigurerer elektroniske fakturaer, kan du spille av følgende [Oppgaveveiledninger](../../fin-ops-core/fin-ops/get-started/help-overview.md#task-guides) i Hjelp-ruten:

 - Definere elektronisk fakturering for OIOUBL
 - Importere konfigurasjoner for elektroniske OIOUBL-faktureringer
 - Definere kundekontoer for elektronisk fakturering med OIOUBL

> [!NOTE] 
> Selv om disse oppgaveveiledningene ble opprettet for det danske e-fakturaformatet *OIOUBL*, gjelder de for andre støttede land/områder med mindre avvik.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
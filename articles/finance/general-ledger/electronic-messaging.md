---
title: Elektroniske meldinger
description: Dette emnet gir oversikt og oppsettinformasjon for elektroniske meldinger i Microsoft Dynamics 365 Finance.
author: liza-golub
ms.date: 06/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 191abc37b7c349aaf3c9e871fe2f1885eec9fc896271d6fac27e5caa0b0fe3b0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768345"
---
# <a name="electronic-messaging"></a>Elektronisk meldingssystem

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over og installasjonsinformasjonen for EM-funksjonalitet **Elektroniske meldinger**.

Myndigheter og lovgivende myndighetene i forskjellige land og områder over hele verden har nylig implementert rapporteringskrav for firmaer som er registrert i disse landene eller regionene. Formålet med kravene er å aktivere data som hentes fra disse firmaene, i elektronisk format direkte fra systemene der de ble beregnet, lagret og behandlet.

EM-funksjonen i Microsoft Dynamics 365 Finance støtter forskjellige prosesser for elektronisk samhandling mellom Finance og systemene som myndigheter og juridiske myndigheter tilbyr for rapportering, sending og mottak av offisiell informasjon.

EM-funksjonen for elektroniske meldinger er integrert i modulen **Elektronisk rapportering**-modulen (ER). Du kan definere ER-formater for elektroniske meldinger. For mer informasjon, se [Elektronisk rapportering (ER)](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

## <a name="basic-concepts-for-em-functionality"></a>Grunnleggende begreper for EM-funksjonalitet

EM-funksjonaliteten er basert på følgende enheter:

- **Elektronisk melding** – En rapport eller deklarering som skal rapporteres eller overføres internt, for eksempel en rapport som sendes til et skattekontor.
- **Elektroniske meldingselementer** – poster som skal inkluderes i meldingen som rapporteres.
- **Behandling av elektronisk melding** – en handlingskjede som må kjøres for å samle de nødvendige dataene, generere rapporter, lagre data i Azure Blob-lagring, sende rapporter utenfor systemet, motta svar fra utenfor systemet og, basert på informasjonen som mottas, oppdatere databasen. Handlingene i kjeden kan være tilkoblet eller frakoblet.

Følgende illustrasjon viser dataflyten for EM.

![Dataflyt for elektroniske meldinger.](media/electronic-messaging-data-flow.png)

## <a name="scenarios-supported-by-the-em-functionality"></a>Scenarier som støttes av EM-funksjonaliteten

EM-funksjonen for elektroniske meldinger støtter følgende scenarioer:

- Manuelt opprette meldinger og generere rapporter som er basert på tilknyttede eksporterende ER-formater av ulike typer. Disse typene omfatter Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, tekst og Microsoft Word.
- Automatisk opprette og behandle meldinger som er basert på informasjonen som ble forespurt og mottatt fra en myndighet via et tilknyttet importerende ER-format.
- Samle inn og behandle informasjon fra en datakilde som meldingselementer. Datakilden er en Finance-tabell.
- Lagre mer informasjon og evaluere ulike verdier ved å kalle spesielt definerte kjørbare klasser i forhold til meldinger eller meldingselementer.
- Aggregere informasjon som samles inn, i meldingselementer, dele informasjonen inn i meldinger og generere rapporter som er i tilknyttede eksporterende ER-formater.
- Sende rapportene som genereres, til en webtjeneste ved hjelp av sikkerhetsinformasjon som lagres i Azure Key Vault.
- Motta et svar fra en webtjeneste, tolke svaret og oppdatere data i Finance etter behov.
- Lagre og gå gjennom alle rapportene som genereres.
- Lagre og gå gjennom all logginformasjon som er knyttet til handlinger som utføres for en melding eller et meldingselement.
- Styre behandlingen gjennom forskjellige meldingsstatuser og meldingselementstatuser.

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>Landspesifikke forskriftsmessige funksjoner som støttes av EM-funksjonaliteten

Følgende tabell inneholder informasjon om noen landspesifikke forskriftsmessige funksjoner som støttes av EM-funksjonaliteten.

| Land     | Funksjonsnavn | Funksjonsdemoregistrering |
|-------------|--------------|------------------------|
| Spania       | [Umiddelbar forsyning av informasjon om mva (Suministro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| Ungarn     | [Online faktureringssystem](../localizations/emea-hun-online-invoicing.md) | |
| Storbritannia | [Gjøre mva digital (MTD) – innsending av mva-oppgave](../localizations/emea-gbr-mtd-vat-integration.md) | [Finance and Operations: Digital mva for Storbritannia – mva-deklarering i Dynamics 365](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Litauen   | [i.SAF-rapportering](../localizations/emea-ltu-isaf.md) | |
| Polen      | [MVA-deklarering med registre (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance: SAF/JPK mva-revisjonsregistreringer](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Nederland | [Mva-deklarering for Nederland](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Tsjekkia | [Mva-deklarering](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brasil      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| Russland      | [Mva-deklarering](../localizations/rus-vat-declaration.md) | |
| Russland      | [Regnskapsrapportering i elektronisk format](../localizations/rus-accounting-reporting.md) | |
| Russland      | [Deklarering for fortjenesteavgift](../localizations/rus-profit-tax-declaration.md) | |
| Russland      | [Vurdert avgiftsdeklarering](../localizations/rus-assessed-tax-declaration.md) | |
| Russland      | [Avgiftsdeklarering for transport](../localizations/rus-transport-tax-declaration.md) | |
| Russland      | [Avgiftsdeklarering for land](../localizations/rus-land-tax-declaration.md) | |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]


---
title: Konfigurer merverdiavgift for nettordrer
description: Dette emnet gir en oversikt over valg av mva-grupper for ulike nettordretyper i Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: fff4f39703a146412b460dacc3805fde097ab756
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021446"
---
# <a name="configure-sales-tax-for-online-orders"></a>Konfigurer merverdiavgift for nettordrer

[!include [banner](includes/banner.md)]

Dette emnet gir en oversikt over valg av mva-gruppe for ulike nettordretyper ved hjelp av enten destinasjonsbaserte eller kundekontobaserte mva-innstillinger. 

Du kan få e-handelskanalen til å støtte alternativer som levering eller henting for nettordrer. Mva-relevansen er basert på alternativet som er valgt av nettkundene dine. 

## <a name="destination-based-taxes-for-online-orders"></a>Destinasjonsbaserte avgifter for nettordrer

Vanligvis defineres avgifter for nettbestillinger som sender til kundeadresser, av destinasjonen. Hver mva-gruppe har en destinasjonsbasert mva-konfigurasjon der virksomheten kan definere måldetaljer som land eller område, fylke, region og poststed i et hierarkisk skjema.

### <a name="orders-delivered-to-customer-address"></a>Bestillinger levert til kundeadresse

Når en nettordre bestilles, bruker Commerce-avgiftsmotoren leveringsadressen for hver linjevare i ordren, og finner mva-grupper med samsvarende målbaserte avgiftskriterier. For en nettordre med en leveringsadresse for linjevare til San Francisco, California, vil avgiftsmotoren for eksempel finne mva-gruppen og mva-koden for California, og deretter beregne merverdiavgift for hver linjevare i henhold til dette.

### <a name="order-pick-up-in-store"></a>Hent ordre i butikk

For ordrelinjer der henting i butikk eller henting utenfor butikk angitt, vil avgiftsgruppen fra det valgte butikken for henting, bli brukt. Hvis du vil ha mer informasjon om hvordan du konfigurerer mva for en gitt butikk, kan du se [Angi andre mva-alternativer for butikker](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

## <a name="customer-account-based-taxes-for-online-orders"></a>Avgifter basert på kundekonto for nettordrer

Det kan være et forretningsscenario der du vil konfigurere en mva-gruppe for en bestemt kundekonto i Commerce Headquarters. Det finnes to steder i Headquarters der du kan konfigurere merverdiavgift for en kundekonto. Hvis du vil ha tilgang til disse, må du først gå til en kundedetaljside ved å gå til **Retail og Commerce \> Kunder \> Alle kunder** og deretter velge en kunde.

De to stedene der du konfigurerer merverdiavgift for en kundekonto, er følgende:

- **Mva-gruppen** på hurtigfanen **Faktura og levering** på kundedetaljersiden. 
- **Merverdiavgift** på hurtigfanen **Generelt** på siden **Administrer adresser**. Du kan gå dit fra kundedetaljsiden ved å velge en spesifikk adresse på hurtigfanen **Adresser** og deretter velge **Avansert**.

> [!TIP]
> Hvis du bare vil bruke destinasjonsbaserte avgifter for ordrer fra nettkunder og unngå kundekontobaserte avgifter, må du sørge for at feltet **Mva-gruppe** er tomt på hurtigfanen **Faktura og levering** på kundedetaljsiden. For å sikre at nye kunder som registrerer seg ved hjelp av nettkanalen, ikke arver innstillingene for mva-gruppen fra standardinnstillingene for kunder eller kundegrupper, må du sørge for at feltet **Mva-gruppe** også er tomt for standard kundeinnstillinger og kundegruppeinnstillinger i nettkanalen (**Retail og Commerce \> Kunder \> Kundegrupper**).

## <a name="determine-destination-based-tax-or-customer-account-based-tax-applicability"></a>Fastslå relevans for destinasjonsbasert avgift eller kundekontobasert avgift 

Tabellen nedenfor beskriver om destinasjonsbaserte avgifter eller kundekontobaserte avgifter skal gjelde for nettordrer. 

| Kundetype | Leveringsadresse                   | Kunde > Faktura og levering > Mva-gruppe? | Adresse til kundekonto i Headquarters? | Kundeadresse > Avansert > Generelt > Mva-gruppe?                                              | Brukt mva-gruppe      |
|---------------|------------------------------------|-----------------------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------|------------------------------|
| Gjest         | Manhattan, NY                      | Nei (tom)                                                | Nei (tom)                              | Nei (tom)                                                                                                   | NY (destinasjonsbaserte avgifter) |
| Logget på     | Austin, TX                          | Nei (tom)                                             | Ja                               | None<br/><br/>Ny adresse lagt til via nettkanalen.                                                            | TX (destinasjonsbaserte avgifter) |
| Logget på     | San Francisco, CA (henting i butikk) | Ja (NY)                                            | Gjelder ikke                              | Gjelder ikke                                                                                                    | CA (destinasjonsbaserte avgifter) |
| Logget på     | Houston, TX                         | Ja (NY)                                            | Ja                               | Ja (NY)<br/><br/>Ny adresse lagt til via nettkanalen og mva-gruppe arvet fra kundekontoen. | NY (kundekontobaserte avgifter)  |
| Logget på     | Austin, TX                          | Ja (NY)                                            | Ja                               | Ja (NY)<br/><br/>Ny adresse lagt til via nettkanalen og mva-gruppe arvet fra kundekontoen. | NY (kundekontobaserte avgifter)  |
| Logget på     | Sarasota, FL                       | Ja (NY)                                            | Ja                               | Ja (WA)<br/><br/>Manuelt angitt til WA.                                                                          | WA (kundekontobaserte avgifter)  |
| Logget på     | Sarasota, FL                       | Nei (tom)                                                | Ja                               | Ja (WA)<br/><br/>Manuelt angitt til WA.                                                                          | WA (kundekontobaserte avgifter)  |

## <a name="additional-resources"></a>Tilleggsressurser

[Definere avgifter for nettbutikker basert på destinasjon](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)

[Oversikt over merverdiavgift](../finance/general-ledger/indirect-taxes-overview.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Beregningsmåter for merverdiavgift i grunnlagsfeltet](../finance/general-ledger/sales-tax-calculation-methods-origin-field.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[ Mva-tilordning og overstyringer](../supply-chain/procurement/tasks/sales-tax-assignment-overrides.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Hele beløp og alternativer for intervallberegning for mva-koder](../finance/general-ledger/whole-amount-interval-options-sales-tax-codes.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Beregning av mva-fritak](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
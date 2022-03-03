---
title: Konfigurere kundekontobetalingsmetode for B2B-e-handelsområder
description: Dette emnet beskriver hvordan du konfigurerer betalingsmetoden for kundekonto i Microsoft Dynamics 365 Commerce. Det beskriver også hvordan kredittgrenser påvirker a konto-betalingsregistrering på nettsteder for bedrift-til-bedrift-e-handelsområder (B2B).
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0366f7b51ac138cc7305f98d5607c554440e6d34
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323361"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Konfigurere kundekontobetalingsmetode for B2B-e-handelsområder

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer betalingsmetoden for kundekonto i Microsoft Dynamics 365 Commerce. Det beskriver også hvordan kredittgrenser påvirker a konto-betalingsregistrering på nettsteder for bedrift-til-bedrift-e-handelsområder (B2B).

Forhandlere kan ta imot ulike typer betaling i bytte mot produktene og tjenestene de selger i en e-handelskanal. Hver betalingstype som en forhandler godtar, må konfigureres i Dynamics 365 Commerce når systemet defineres. Betalingsmetoden for kundekonto (eller «a konto») må støttes på B2B-e-handelsområder. 

## <a name="prerequisites"></a>Forutsetninger

1. Legg til betalingsmåten for kundekonto i Commerce Headquarters.
2. Knytt kundekontobetalingsmåten til e-handelskanalen.
3. Kontroller at egenskapen **Tillat a konto** er aktivert for kunden i **Detaljhandel og handel \> Kunder \> Alle kunder \> Betalingsstandarder** i Commerce Headquarters.

    > [!NOTE]
    > Hvis alle kunder skal kunne ha betalingsmetoden for a konto aktivert, kan du angi **Ja** for egenskapen **Tillat a konto** for standardkunden i kanalen som er knyttet til B2B-området. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Aktivere kundekontobetalingsmetode i Commerce-områdebygger 

For å aktivere kundekontobetalingsmetode i Commerce-områdebygger, følger du trinnene nedenfor.

1. Gå til **Områdeinnstillinger \> Tillegg**.
1. Sett egenskapen **Aktiver kundekontobetalinger** til **Aktivert for B2B-kunder**. 
1. Velg **Lagre og publiser**.

> [!NOTE]
> De nye innstillingene trer i kraft bare etter at filen app.settings.json er oppdatert. Hvis du vil ha mer informasjon, kan du se [Oppdateringer for SDK og modulbibliotek](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Aktivere betalingsmåten for kundekonto på betalingssiden for B2B-e-handelsområdet

Følg disse trinnene for å aktivere betalingsmåten for kundekonto på betalingssiden for B2B-e-handelsområdet.

1. I Commerce-områdebygger finner og redigerer du utsjekkingsside eller fragmentet som inneholder utsjekkingsmodulen for B2B-e-handelsområdet.
1. I sporet **Container for betalingsdel** velger du **Legg til modul**, og deretter legger du til en **Kundekontobetaling**-modul.
1. Plasser modulen **Kundekontobetaling** ved å velge ellipsen (**...**) og deretter velge **Flytt ned** eller **Flytt opp** etter behov.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Bekrefte at betalingsmåten for kundekonto er aktivert og publisert

For å bekrefte at betalingsmåten for kundekonto er aktivert, følger du trinnene nedenfor.

1. Logg på e-handelsområdet.
1. Legg til et produkt i handlevognen.
1. Gå til utsjekkingssiden. Du skal nå¨se den nye betalingsmåten **Kundekonto**.

## <a name="work-with-credit-limits"></a>Arbeide med kredittgrenser

Når funksjonene for kundekontobetalinger er aktivert på B2B-området, ønsker organisasjoner vanligvis å kunne vise informasjon om kredittgrenser og kredittgrensesaldoer under ordreregistreringen. Kredittgrensen for en kunde defineres av egenskapen **Kredittgrense** i hurtigfanen **Kreditt og innkreving** i kundeposten i Commerce Headquarters. I B2B-scenarioer bør imidlertid en ordre som en kunde registrerer, ofte faktureres på kontoen til organisasjonen som kunden tilhører. Du må derfor angi kundekonto-ID-en for organisasjonen for egenskapen **Fakturakonto** i hurtigfanen **Faktura og levering** for kundeposten. Når kunden deretter registrerer en ordre på B2B-området, faktureres organisasjonen for ordren. B2B-området bruker også kredittgrensen for organisasjonen i stedet for kredittgrensen som er definert i kundeposten.

Beregningen av og saldoen for kredittgrensen som vises på B2B-nettstedet, er avhengig av innstillingen for egenskapen **Kredittgrensetype** i Commerce Headquarters. Plasseringen av denne egenskapen varierer avhengig av om funksjonen **Kredittbehandling** er aktivert i arbeidsområdet for **Funksjonsbehandling**:

- Hvis funksjonen **Kredittbehandling** er aktivert, er egenskapen i hurtigfanen **Kredittgrenser** i **Kreditt og innkreving \> Oppsett \> Parametere for kreditt og innkreving \> Kreditt**. 
- Hvis funksjonen **Kredittbehandling** er deaktivert, er egenskapen under **Kredittvurdering** i **Kunder \> Oppsett \> Kundeparametere \> Kredittvurdering**.

Egenskapen **Kredittgrensetype** støtter verdiene **Ingen**, **Saldo**, **Saldo + følgeseddel eller produktkvittering** og **Saldo+Alt**. Hvis du vil ha mer informasjon om disse verdiene, kan du se [Verdier for kredittgrensetype](/dynamics365/supply-chain/sales-marketing/credit-limits-customers).

> [!NOTE]
> Vi anbefaler at du angir **Saldo + følgeseddel eller produktkvittering** for egenskapen **Kredittgrensetype**, slik at åpne salgsordrer ikke bidrar til saldoberegningen. Hvis kundene deretter registrerer fremtidige ordrer, trenger de ikke å bekymre seg for at disse ordrene påvirker gjeldende saldo.

En annen egenskap som påvirker a konto-bestilling, er egenskapen **Obligatorisk kredittgrense**, som er i hurtigfanen **Kreditt og innkreving** i kundeposten. Hvis du angir **Ja** for denne egenskapen for bestemte kunder, kan du tvinge systemet til å kontrollere kredittgrensen, selv om **Ingen** er angitt for egenskapen **Kredittgrensetype** for å angi at kredittgrensen ikke skal kontrolleres for noen kunder.

B2B-områder som egenskapen **Obligatorisk kredittgrense** er aktivert for, har for øyeblikket ytterligere funksjonalitet. Hvis egenskapen er aktivert i en kundepost når kunden registrerer en ordre, hindrer B2B-området kunden i å bruke betalingsmetoden for a konto til å betale mer enn den gjenstående kredittsaldoen. Hvis den gjenstående kredittsaldoen for kunden for eksempel er USD 1000, men ordren er verdt USD 1200, kan kunden bare betale USD 1000 ved å bruke metoden for a konto. Kunden må bruke en annen betalingsmetode til å betale saldoen. Hvis egenskapen **Obligatorisk kredittgrense** er deaktivert i en kundepost, kan kunden betale et hvilket som helst beløp ved å bruke betalingsmetoden for a konto. Selv om en kunde kan registrere ordrer, tillater imidlertid ikke systemet at disse ordrene oppfylles hvis de overskrider kredittgrensen. Hvis du må kontrollere kredittgrensen for alle kunder som er kvalifisert for a konto-betalinger, anbefaler vi at du angir **Saldo + følgeseddel eller produktkvittering** for egenskapen **Kredittgrensetype** og **Nei** for egenskapen **Obligatorisk kredittgrense**.

Modulen **Kreditt og innkreving** har nye funksjoner for kredittbehandling. Hvis du vil aktivere disse funksjonene, aktiverer du funksjonen **Kredittbehandling** i arbeidsområdet **Funksjonsbehandling**. En av de nye funksjonene gjør at salgsordrer kan settes på vent basert på blokkeringsregler. Kredittlederidentiteten kan deretter frigi eller avvise ordrene etter ytterligere analyse. Funksjonen for å sette salgsordrer på vent, gjelder imidlertid ikke for Commerce-ordrer, fordi salgsordrer ofte har en forskuddsbetaling, og funksjonen **Kredittbehandling** har ikke fullstendig støtte for scenarioer med forskuddsbetaling. 

Uavhengig av om funksjonen **Kredittbehandling** er aktivert, havner ikke salgsordrene på vent hvis en kundesaldo går over kredittgrensen under ordreoppfyllelse. Commerce genererer i stedet en advarsel eller en feilmelding, avhengig av verdien i feltet **Melding ved overskridelse av kredittgrense** i hurtigfanen **Kredittgrenser**.

Egenskapen **Utelat fra kredittbehandling** som forhindrer at Commerce-salgsordrer havner på vent, ligger i salgsordrehodet (**Detaljhandel og handel \> Kunder \> Alle salgsordrer**). Hvis **Ja** (standardverdien) er angitt for denne egenskapen for Commerce-salgsordrer, utelates ordrene fra arbeidsflyten for vent for kredittbehandling. Legg merke til at selv om egenskapen kalles **Utelat fra kredittbehandling**, brukes likevel den definerte kredittgrensen under ordreoppfyllelse. Ordrene havner bare ikke på vent.

Funksjonen for å sette Commerce-salgsordrer på vent basert på blokkeringsregler planlegges for fremtidige Commerce-utgivelser. Hvis du må tvinge Commerce-salgsordrer til å gå gjennom de nye kredittbehandlingsflytene før denne funksjonen kommer, kan du tilpasse følgende XML-filer i Visual Studio-løsningen. Endre logikken i filene slik at **Nei** er angitt for flagget **CredManExcludeSalesOrder**. Dermed angis som standard **Nei** for egenskapen **Utelat fra kredittbehandling** for Commerce-salgsordrer.

- RetailCreateCustomerOrderExtensions_CredMan_Extension.xml
- RetailCallCenterOrderExtensions_CredMan_Extension.xml

Vær oppmerksom på at hvis **Nei** er angitt for flagget **CredManExcludeSalesOrder** og en B2B-kunde kan kjøpe fra butikker ved å bruke salgsstedsprogrammet, kan det hende at posteringen av hentesalgstransaksjoner mislykkes. La oss for eksempel si at en blokkeringsregel gjelder for kontantbetalingstypen, og B2B-kunden kjøpte noen varer i butikken med kontanter. I dette tilfellet blir ikke salgsordren fakturert, fordi den kommer til å settes på vent. Posteringen blir derfor mislykket. Vi anbefaler derfor at du foretar ende-til-ende-testing etter at du har implementert denne tilpasningen.

## <a name="additional-resources"></a>Tilleggsressurser

[Definere et e-handelsområde for B2B](set-up-b2b-site.md)

[Administrere B2B-forretningspartnere ved hjelp av kundehierarkier](partners-customer-hierarchies.md)

[Administrere forretningspartnerbrukere på e-handelsområder for B2B](manage-b2b-users.md)

[Angi produktantallsgrenser for B2B-e-handelsområder](quantity-limits.md)

[Oppdateringer for SDK og modulbibliotek](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

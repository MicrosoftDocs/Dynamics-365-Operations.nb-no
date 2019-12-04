---
title: Integrerte originalkunde
description: Dette emnet beskriver integreringen av kundedata mellom Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 09d985e5c6816ec0c718aaf418f4e85fb828f1c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769689"
---
# <a name="integrated-customer-master"></a>Integrerte originalkunde

[!include [banner](../includes/banner.md)]

Det er vanlig at kundeposter mestres i mer enn ett program. Salgsaktivitet kan for eksempel hente inn kommersielle kundeposter gjennom et Sales-program, og e-handel eller detaljsalg kan hente inn kundeposter gjennom et Finance and Operations-program. Uansett hvor kundeposten kommer fra, er den integrert bak kulissene på tvers av applikasjonsgrenser og infrastrukturforskjeller. Integrert kundemestring hjelper håndtere multi-Mastering scenarier og gir en omfattende visning av kunden til Dynamics 365-programpakken.

## <a name="customer-data-flow"></a>Kundedataflyt

*Kunde* er et veldefinert begrep i programmer. Integreringen av kundedata innebærer derfor bare å harmonisere kundekonseptet mellom de to programmene. Følgende illustrasjon viser kundedataflyten.

![Kundedataflyt](media/dual-write-customer-data-flow.png)

Kunder kan grovt klassifiseres i to typer: kommersielle/organisatoriske kunder og forbrukere/sluttbrukere. Disse to kundetypene lagres og håndteres forskjellig i Finance and Operations og Common Data Service.

I Finance and Operations, både kommersielle/organisatoriske kunder og forbrukere/sluttbrukere er mastret i en enkelt tabell som heter **CustTable** (CustomerCustomerV3Entity), og de er klassifisert basert på **Type**-attributtet. (Hvis **Type** er satt til **Organisasjon**, er kunden en kommersiell/organisastorisk kunde, og hvis **Type** er satt til **Person**, er kunden en forbruker/sluttbruker.) Den primære kontaktpersoninformasjonen håndteres via SMMContactPersonEntity-enheten.

I Common Data Service, kommersielle/organisatoriske kunder er mastret i kontoenheten og identifiseres som kunder når **RelationshipType**-attributtet er satt til **Kunde**. Både forbrukere/sluttbrukere og kontaktpersonen representeres av Kontakt-enheten. Hvis du vil gi et klart skille mellom en forbruker/sluttbruker og en kontaktperson, har **Kontakt**-enheten et boolsk flagg som heter **Sellable**. Når **Sellable** er **True**, er kontakten en forbruker/sluttbruker, og tilbud og ordrer kan opprettes for denne kontakten. Når **Sellable** er **False**, er kontakten bare en primærkontaktperson for en kunde.

Når en ikke-salgbar kontakt deltar i en tilbuds- eller en ordreprosess er **Sellable** satt til **True** for å flagge kontakten som en salgbar kontakt. En kontakt som har blitt en salgbar kontakt, forblir en salgbar kontakt.

## <a name="templates"></a>Maler

Kundedata inkluderer all informasjon om kunden, for eksempel kundegruppe, adresser, kontaktinformasjon, betalingsprofil, fakturaprofil og fordelsstatus. En samling enhetstilordninger fungerer sammen under kundedatasamhandling, som vist i følgende tabell.

Finance and Operations-apper | Andre Dynamics 365-apper         | Beskrivelse
----------------------------|---------------------------------|------------
CDS-kontakter V2             | kontakter                        | Denne malen synkroniserer all primær, sekundær og tertiær informasjon, både for kunder og leverandører.
Kundegrupper             | msdyn_customergroups            | Denne malen synkroniserer kundegruppeinformasjon.
Kundebetalingsmåte     | msdyn_customerpaymentmethods    | Denne malen synkroniserer informasjon om kundebetalingsmåte.
Kunder V3                | kontoer                        | Denne malen synkroniserer kundens hoveddata for kommersielle og organisatoriske kunder.
Kunder V3                | kontakter                        | Denne malen synkroniserer hoveddata for kunder for forbrukere og sluttbrukere.
Fordelskort                | msdyn_loyaltycards              | Denne malen synkroniserer informasjon om fordelskort.
Navnevedlegg                | msdyn_nameaffixes               | Denne malen synkroniserer referansedata for navnevedlegg, både for kunder og leverandører.
Betalingsdagslinjer, CDS V2    | msdyn_paymentdaylines           | Denne malen synkroniserer referansedata om betalingsdagslinjer, både for kunder og leverandører.
Betalingsdager, CDS            | msdyn_paymentdays               | Denne malen synkroniserer referansedata om betalingsdager, både for kunder og leverandører.
Linjer i betalingsplan      | msdyn_paymentschedulelines      | Synkroniserer referansedata om betalingsplanlinjer, både for kunder og leverandører.
Betalingsplan            | msdyn_paymentschedules          | Denne malen synkroniserer referansedata om betalingsplan, både for kunder og leverandører.
Betalingsbetingelser            | msdyn_paymentterms              | Denne malen synkroniserer referansedata om betalingsbetingelser, både for kunder og leverandører.

[!include [banner](../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](dual-write/CDSContactsV2-contacts.md)]

[!include [mapping customer group](dual-write/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](dual-write/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](dual-write/CustomersV3-accounts.md)]

[!include [mapping customer contacts](dual-write/CustomersV3-contacts.md)]

[!include [mapping loyalty card](dual-write/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](dual-write/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](dual-write/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](dual-write/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](dual-write/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](dual-write/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](dual-write/TermsofPayment-msdyn-paymentterms.md)]

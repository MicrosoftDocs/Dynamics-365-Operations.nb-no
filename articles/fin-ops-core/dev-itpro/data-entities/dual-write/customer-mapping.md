---
title: Integrerte originalkunde
description: Dette emnet beskriver integreringen av kundedata mellom Finance and Operations og Dataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 801538e320ca78b0cc55bb4e4b8a80d38b9b48d6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685645"
---
# <a name="integrated-customer-master"></a>Integrert original for kunde

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


Kundedata kan styres i mer enn ett Dynamics 365-program. En kunderad kan for eksempel komme fra salgsaktivitet i Dynamics 365 Sales (en modelldrevet app i Dynamics 365), eller en rad kan stamme fra detaljhandelsaktivitet i Dynamics 365 Commerce (en Finance and Operations-app). Uansett hvor kundedataene kommer fra, er de integrert bak kulissene. Integrert original for kunde gir deg fleksibilitet til å styre kundedata i alle Dynamics 365-programmer, og gir en omfattende visning av kunden på tvers av Dynamics 365-programserien.

## <a name="customer-data-flow"></a>Kundedataflyt

*Kunde* er et veldefinert begrep i programmer. Integreringen av kundedata innebærer derfor bare å harmonisere kundekonseptet mellom de to programmene. Følgende illustrasjon viser kundedataflyten.

![Kundedataflyt](media/dual-write-customer-data-flow.png)

Kunder kan grovt klassifiseres i to typer: kommersielle/organisatoriske kunder og forbrukere/sluttbrukere. Disse to kundetypene lagres og håndteres forskjellig i Finance and Operations og Dataverse.

I Finance and Operations administreres både kommersielle/organisatoriske kunder og forbrukere/sluttbrukere i én enkelt tabell som heter **CustTable** (CustCustomerV3Entity), og de klassifiseres basert på **Type**-attributtet. (Hvis **Type** er satt til **Organisasjon**, er kunden en kommersiell/organisastorisk kunde, og hvis **Type** er satt til **Person**, er kunden en forbruker/sluttbruker.) Den primære kontaktpersoninformasjonen håndteres via SMMContactPersonEntity-enheten.

I Dataverse, kommersielle/organisatoriske kunder er mastret i kontoenheten og identifiseres som kunder når **RelationshipType**-attributtet er satt til **Kunde**. Både forbrukere/sluttbrukere og kontaktpersonen representeres av Kontakt-enheten. Hvis du vil gi et klart skille mellom en forbruker/sluttbruker og en kontaktperson, har **Kontakt**-enheten et boolsk flagg som heter **Sellable**. Når **Sellable** er **True**, er kontakten en forbruker/sluttbruker, og tilbud og ordrer kan opprettes for denne kontakten. Når **Sellable** er **False**, er kontakten bare en primærkontaktperson for en kunde.

Når en ikke-salgbar kontakt deltar i en tilbuds- eller en ordreprosess er **Sellable** satt til **True** for å flagge kontakten som en salgbar kontakt. En kontakt som har blitt en salgbar kontakt, forblir en salgbar kontakt.

## <a name="templates"></a>Maler

Kundedata inkluderer all informasjon om kunden, for eksempel kundegruppe, adresser, kontaktinformasjon, betalingsprofil, fakturaprofil og fordelsstatus. En samling tabelltilordninger fungerer sammen under kundedatasamhandling, som vist i følgende tabell.

Finance and Operations-apper | Andre Dynamics 365-apper         | Beskrivelse
----------------------------|---------------------------------|------------
CDS-kontakter V2             | kontakter                        | Denne malen synkroniserer all primær, sekundær og tertiær informasjon, både for kunder og leverandører.
Kundegrupper             | msdyn_customergroups            | Denne malen synkroniserer kundegruppeinformasjon.
Kundebetalingsmåte     | msdyn_customerpaymentmethods    | Denne malen synkroniserer informasjon om kundebetalingsmåte.
Kunder V3                | kontoer                        | Denne malen synkroniserer kundens hoveddata for kommersielle og organisatoriske kunder.
Kunder V3                | kontakter                        | Denne malen synkroniserer hoveddata for kunder for forbrukere og sluttbrukere.
Navnevedlegg                | msdyn_nameaffixes               | Denne malen synkroniserer referansedata for navnevedlegg, både for kunder og leverandører.
Betalingsdagslinjer, CDS V2    | msdyn_paymentdaylines           | Denne malen synkroniserer referansedata om betalingsdagslinjer, både for kunder og leverandører.
Betalingsdager, CDS            | msdyn_paymentdays               | Denne malen synkroniserer referansedata om betalingsdager, både for kunder og leverandører.
Linjer i betalingsplan      | msdyn_paymentschedulelines      | Synkroniserer referansedata om betalingsplanlinjer, både for kunder og leverandører.
Betalingsplan            | msdyn_paymentschedules          | Denne malen synkroniserer referansedata om betalingsplan, både for kunder og leverandører.
Betalingsbetingelser            | msdyn_paymentterms              | Denne malen synkroniserer referansedata om betalingsbetingelser, både for kunder og leverandører.

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]

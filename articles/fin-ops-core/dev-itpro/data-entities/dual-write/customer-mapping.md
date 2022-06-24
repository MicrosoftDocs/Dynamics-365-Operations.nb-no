---
title: Integrert original for kunde
description: Denne artikkelen beskriver integreringen av kundedata mellom Økonomi og drift og Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 042042bb19b32d3c96b4e0c8521a8b1d65e7ab22
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890463"
---
# <a name="integrated-customer-master"></a>Integrert original for kunde

[!include [banner](../../includes/banner.md)]



Kundedata kan styres i mer enn ett Dynamics 365-program. En kunderad kan for eksempel komme fra salgsaktivitet i Dynamics 365 Sales (en kundeengasjementsapp), eller en rad kan stamme fra detaljhandelsaktivitet i Dynamics 365 Commerce (en Finance and Operations-app). Uansett hvor kundedataene kommer fra, er de integrert bak kulissene. Integrert original for kunde gir deg fleksibilitet til å styre kundedata i alle Dynamics 365-programmer, og gir en omfattende visning av kunden på tvers av Dynamics 365-programserien.

## <a name="customer-data-flow"></a>Kundedataflyt

*Kunde* er et veldefinert begrep i programmer. Integreringen av kundedata innebærer derfor bare å harmonisere kundekonseptet mellom de to programmene. Følgende illustrasjon viser kundedataflyten.

![Kundedataflyt.](media/dual-write-customer-data-flow.png)

Kunder kan grovt klassifiseres i to typer: kommersielle/organisatoriske kunder og forbrukere/sluttbrukere. Disse to kundetypene lagres og håndteres forskjellig i Finance and Operations og Dataverse.

I økonomi og drift er både kommersielle/organisatoriske kunder og forbrukere/sluttbrukere mastret i en enkelt tabell som heter **CustTable** (CustCustomerV3Entity), og de er klassifisert basert på **Type**-attributtet. (Hvis **Type** er satt til **Organisasjon**, er kunden en kommersiell/organisatorisk kunde, og hvis **Type** er satt til **Person**, er kunden en forbruker/sluttbruker.) Den primære kontaktpersoninformasjonen håndteres via SMMContactPersonEntity-tabellen.

I Dataverse styres kommersielle/organisatoriske kunder i kontotabellen og identifiseres som kunder når **RelationshipType**-attributtet er satt til **Kunde**. Både forbrukere/sluttbrukere og kontaktpersonen representeres av Kontakt-tabellen. Hvis du vil gi et klart skille mellom en forbruker/sluttbruker og en kontaktperson, har **Kontakt**-tabellen et boolsk flagg kalt **Kan selges**. Når **Sellable** er **True**, er kontakten en forbruker/sluttbruker, og tilbud og ordrer kan opprettes for denne kontakten. Når **Sellable** er **False**, er kontakten bare en primærkontaktperson for en kunde.

Når en ikke-salgbar kontakt deltar i en tilbuds- eller en ordreprosess er **Sellable** satt til **True** for å flagge kontakten som en salgbar kontakt. En kontakt som har blitt en salgbar kontakt, forblir en salgbar kontakt.

## <a name="templates"></a>Maler

Kundedata inkluderer all informasjon om kunden, for eksempel kundegruppe, adresser, kontaktinformasjon, betalingsprofil, fakturaprofil og fordelsstatus. En samling tabelltilordninger fungerer sammen under kundedatasamhandling, som vist i følgende tabell.

Finance and Operations-apper | Kundeengasjementsapper         | beskrivelse
----------------------------|---------------------------------|------------
[CDS-kontakter V2](mapping-reference.md#115) | kontakter | Denne malen synkroniserer all primær, sekundær og tertiær informasjon, både for kunder og leverandører.
[Kundegrupper](mapping-reference.md#126) | msdyn_customergroups | Denne malen synkroniserer kundegruppeinformasjon.
[Kundebetalingsmåte](mapping-reference.md#127) | msdyn_customerpaymentmethods | Denne malen synkroniserer informasjon om kundebetalingsmåte.
[Kunder V3](mapping-reference.md#101) | kontoer | Denne malen synkroniserer kundens hoveddata for kommersielle og organisatoriske kunder.
[Kunder V3](mapping-reference.md#116) | kontakter | Denne malen synkroniserer hoveddata for kunder for forbrukere og sluttbrukere.
[Navnevedlegg](mapping-reference.md#155) | msdyn_nameaffixes | Denne malen synkroniserer referansedata for navnevedlegg, både for kunder og leverandører.
[Betalingsdagslinjer, CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Denne malen synkroniserer referansedata om betalingsdagslinjer, både for kunder og leverandører.
[Betalingsdager, CDS](mapping-reference.md#158) | msdyn_paymentdays | Denne malen synkroniserer referansedata om betalingsdager, både for kunder og leverandører.
[Linjer i betalingsplan](mapping-reference.md#159) | msdyn_paymentschedulelines | Synkroniserer referansedata om betalingsplanlinjer, både for kunder og leverandører.
[Betalingsplan](mapping-reference.md#160) | msdyn_paymentschedules | Denne malen synkroniserer referansedata om betalingsplan, både for kunder og leverandører.
[Betalingsbetingelser](mapping-reference.md#161) | msdyn_paymentterms | Denne malen synkroniserer referansedata om betalingsbetingelser, både for kunder og leverandører.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

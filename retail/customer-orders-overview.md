---
title: Oversikt over ordrer for kunde
description: "Dette emnet gir informasjon om kundeordrer i Retail moderne POS (MPOS). Kundeordrer er også kjent som spesialbestillinger. Emnet inneholder en beskrivelse av relaterte parametere og flyter for transaksjonen."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2f466dfe53ccf0be15ed0793b4a6dd371bdacc0d
ms.lasthandoff: 03/31/2017


---

# <a name="customer-orders-overview"></a>Oversikt over ordrer for kunde

Dette emnet gir informasjon om kundeordrer i Retail moderne POS (MPOS). Kundeordrer er også kjent som spesialbestillinger. Emnet inneholder en beskrivelse av relaterte parametere og flyter for transaksjonen.

I en omni-kanals retail-verden gir mange detaljister muligheten til kundens ordrer og spesialordrer, til forskjellige behov for produkt og gjennomføring. Her er noen vanlige scenarier:

-   En kunde ønsker produkter som skal leveres til en bestemt adresse på en bestemt dato.
-   En kunde ønsker å plukke opp produkter fra en butikk eller lokasjon som er forskjellig fra butikken eller plasseringen der kunden kjøpte disse produktene.
-   En kunde ønsker noen andre til å plukke opp produkter som kunden har kjøpt.

Forhandlere kan også bruke kundeordrer for å minimere tapt salg som lager driftsstans ellers kan det hende, fordi varene kan leveres eller plukket på et annet tidspunkt eller sted.

## <a name="set-up-customer-orders"></a>Definer kundeordrer
Her er noen av parameterne som kan angis i den **parametere for detaljhandel** siden for å definere hvordan kundeordrer er oppfylt:

-   **Standard innskudd prosent** – Angi beløpet som kunden må betale som et innskudd før en ordre kan bekreftes. Innbetalingsbeløpet i standard beregnes som en prosentandel av order-verdien. Avhengig av rettigheter, Knytt en butikk kan kanskje overstyre beløpet ved hjelp av **overstyring av innbetaling**.
-   **Prosent for annulleringsgebyr** – Hvis et gebyr vil bli brukt når en kundebestilling er avbrutt, angi beløpet for gebyret.
-   **Kode for annulleringsgebyr** – Hvis et gebyr vil bli brukt når en kundebestilling er avbrutt, at tillegget vises under en tilleggskode i ordren i Microsoft Dynamics AX. Bruk denne parameteren til å definere tilleggskoden for annulleringen.
-   **Levering tilleggskoden** – forhandlere kan belaste en ekstra avgift for forsendelse av varer til en kunde. Hvor mye strøm som levering vises under en tilleggskode i ordren i Dynamics AX. Bruk denne parameteren til å tilordne levering tilleggskoden til forsendelsestillegg på kundeordren.
-   **Refundere forsendelseskostnadene** – angi om forsendelseskostnadene som er knyttet til en kundeordre refundable.
-   **Maksimalt beløp uten godkjenning** – Hvis forsendelseskostnader er refundable, angir den maksimale mengden levering gebyr refusjoner over returordrer. Hvis dette beløpet overstiges, er manager overstyring nødvendig for å fortsette med refusjonen. Refundert forsendelseskostnader kan overskride beløpet som opprinnelig ble betalt til følgende scenarier:
    -   Gebyrer, brukes på nivået av salgsordrehodet, og når et antall av en produktserie returneres, maksimal refusjon for forsendelsestillegg som er tillatt for produktene og antallet kan ikke bestemmes på måten som passer for alle detaljkunder.
    -   Forsendelseskostnader er påløpt for hver forekomst av levering. Hvis en kunde returnerer varer flere ganger, og fra forhandleren policyen angir at forhandleren vil bære kostnaden for retur forsendelseskostnader, blir mer enn faktiske forsendelseskostnadene i retur forsendelseskostnadene.

## <a name="transaction-flow-for-customer-orders"></a>Transaksjonsflyt for kundeordrer
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Opprette en kundeordre i moderne Priskontroll

1.  Legg til en kunde i transaksjonen.
2.  Legge til produkter i handlekurven.
3.  Klikk **opprette kundeordre**, og velg deretter typen bestilling. Ordretypen kan være enten **kundeordre** eller **tilbud**.
4.  Klikk **Lever valgt** eller **Send alle** for å levere produkter til en adresse i kundekontoen, kan du angi ønsket forsendelsesdato, og angi forsendelseskostnader.
5.  Klikk **plukke opp valgt** eller **avhenting alle** å velge produkter som plukkes fra det gjeldende lageret eller en annen på en bestemt dato.
6.  Samle innbetalingsbeløpet, hvis det kreves et depositum.

### <a name="edit-an-existing-customer-order"></a>Redigere en eksisterende kunde.

1.  Klikk på hjemmesiden, **finne en bestilling**.
2.  Finn og velg rekkefølgen for å redigere. Nederst på siden, klikker du **Rediger**.

### <a name="pick-up-an-order"></a>Plukke opp en ordre

1.  Klikk på hjemmesiden, **finne en bestilling**.
2.  Velg ordren som skal plukke opp. Nederst på siden, klikker du **plukking og pakking av**.
3.  Klikk **plukke opp**.

### <a name="cancel-an-order"></a>Annullere en ordre

1.  Klikk på hjemmesiden, **finne en bestilling**.
2.  Velg rekkefølgen for å avbryte. Nederst på siden, klikker du **avbryte**.

#### <a name="create-a-return-order"></a>Opprette en returordre

1.  Klikk på hjemmesiden, **finne en bestilling**.
2.  Velg rekkefølgen for å gå tilbake, Velg fakturaen for bestillingen, og velg produktlinje for varer å gå tilbake.
3.  Nederst på siden, klikker du **ordreretur**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynkron transaksjonsflyt for kundeordrer
Kundeordrer kan opprettes fra poenget med salg (POS) klienten i modus for synkron eller asynkron modus.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Aktiver kundeordrer i asynkron modus

1.  I Dynamics AX, klikker du **detaljhandel og commerce**&gt;**kanaloppsett**&gt;**POS installasjonsprogrammet**&gt;**profil POS**&gt;**Funksjonalitetsprofiler**.
2.  På den **Generelt** hurtigfanen satt til **Opprett kundeordre i asynkron modus** å **Ja**.

Når den **opprette kundeordre i asynkron modus** alternativet er satt til **Ja**, opprettes alltid kundeordrer i asynkron modus, selv om detaljhandel Transaction Service (RTS) er tilgjengelig. Hvis du setter dette alternativet til å **ingen**, opprettes alltid kundeordrer i synkron modus ved hjelp av RTS. Når det opprettes kundeordrer i asynkron modus, er de hentes og settes inn i Dynamics AX ved å trekke (P) jobber. Tilsvarende salgsordrene som er opprettet i Dynamics AX når **Synkroniser ordrer** kjøres manuelt eller via en satsvis prosess.

<a name="see-also"></a>Se også
--------

[Hybrid kundeordrer](hybrid-customer-orders.md)



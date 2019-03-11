---
title: Kundeordrer i Retail Modern POS (MPOS)
description: Dette emnet gir informasjon om kundeordrer i Retail Modern POS (MPOS). Kundeordrer er også kjent som spesialbestillinger. Emnet inneholder en beskrivelse av relaterte parametere og flyter for transaksjonen.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b54f39cc7896871d77f9371e6197bf6dbaac51de
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "336618"
---
# <a name="customer-orders-in-retail-modern-pos-mpos"></a>Kundeordrer i Retail Modern POS (MPOS)

[!include [banner](includes/banner.md)]

Dette emnet gir informasjon om kundeordrer i Retail Modern POS (MPOS). Kundeordrer er også kjent som spesialbestillinger. Emnet inneholder en beskrivelse av relaterte parametere og flyter for transaksjonen.

Omnikanal for detaljhandel gir mulighet for kundeordrer og spesialordrer, eller spesialordrer, for å møte ulike behov. Her er noen vanlige scenarier:

- En kunde ønsker produkter som skal leveres til en bestemt adresse på en bestemt dato.
- En kunde ønsker å plukke opp produkter fra en butikk eller lokasjon som er forskjellig fra butikken eller plasseringen der kunden kjøpte disse produktene.
- En kunde ønsker noen andre til å plukke opp produkter som kunden har kjøpt.

Forhandlere kan også bruke kundeordrer for å minimere tapt salg som ellers kan forårsakes av lagernedetid, fordi varene kan leveres eller hentes på et annet tidspunkt eller sted.

## <a name="set-up-customer-orders"></a>Definer kundeordrer

Her er noen av parameterne som kan angis på siden **Parametere for detaljhandel** for å definere hvordan kundeordrer er oppfylt:

- **Standard innbetalingsprosent** – Angi beløpet som kunden må betale som et innskudd før en ordre kan bekreftes. Standard innbetalingsbeløp beregnes som en prosentdel av ordreverdien. Avhengig av rettigheter kan en butikkmedarbeider kanskje overstyre beløpet ved hjelp av **Overstyring av innbetaling**.
- **Prosent for annulleringsgebyr** – Hvis et gebyr skal brukes når en kundebestilling annulleres, angir du beløpet for gebyret.
- **Kode for annulleringsgebyr** – Hvis et gebyr skal brukes når en kundebestilling annulleres, vises dette gebyret under en gebyrkode i salgsordren. Bruk denne parameteren til å definere koden for annulleringsgebyr.
- **Kode for forsendelsesgebyr** – Forhandlere kan belaste en ekstra avgift for forsendelse av varer til en kunde. Beløpet for forsendelsesgebyret vises under en gebyrkode i salgsordren. Bruk denne parameteren til å tilordne koden for forsendelsesgebyr til forsendelsegebyret på kundeordren.
- **Refundering av forsendelseskostnader** – Angi om forsendelseskostnadene som er knyttet til en kundeordre, kan refunderes.
- **Maksimumsbeløp uten godkjenning** – Hvis forsendelseskostnader kan refunderes, angir du maksimumsbeløpet for refundereringer av forsendelseskostnader på tvers av returordrer. Hvis dette beløpet overstiges, er lederoverstyring nødvendig for å fortsette med refunderingen. En refundering av forsendelseskostnader kan overskride beløpet som opprinnelig ble betalt, i følgende scenarier:

    - Gebyrer brukes på nivået til salgsordrehodet, og når et antall av en produktserie returneres, kan ikke maksimal refundering av forsendelseskostnader som er tillatt for produktene og antallet, bestemmes på en måte som passer for alle detaljkunder.
    - Forsendelseskostnader påløpes for hver forekomst av levering. Hvis en kunde returnerer varer flere ganger, og forhandlerens policy angir at forhandleren skal betale returgebyrene, blir returgebyrene større enn de faktiske forsendelseskostnadene.

## <a name="transaction-flow-for-customer-orders"></a>Transaksjonsflyt for kundeordrer

### <a name="create-a-customer-order-in-retail-modern-pos"></a>Opprette en kundeordre i Retail Modern POS

1. Legg til en kunde i transaksjonen.
2. Legg til produkter i handlevognen.
3. Klikk **Opprett kundeordre**, og velg deretter ordretypen. Ordretypen kan være enten **kundeordre** eller **tilbud**.
4. Klikk **Valgt for forsendelse** eller **Send alle** for å levere produktene til en adresse i kundekontoen, angi ønsket forsendelsesdato, og angi forsendelseskostnader.
5. Klikk **Valgt for plukking** eller **Plukk alle** for å velge produkter som plukkes fra det gjeldende lageret eller et annet lager på en bestemt dato.
6. Samle innbetalingsbeløpet, hvis det kreves et depositum.

### <a name="edit-an-existing-customer-order"></a>Rediger en eksisterende kundeordre

1. Klikk **Finn en ordre** på startsiden.
2. Finn og velg ordren for å redigere. Klikk **Rediger** nederst på siden.

### <a name="pick-up-an-order"></a>Hent en ordre

1. Klikk **Finn en ordre** på startsiden.
2. Velg ordren som skal hentes. Klikk **Plukk og pakking** nederst på siden.
3. Klikk **Plukk**.

### <a name="cancel-an-order"></a>Annullere en ordre

1. Klikk **Finn en ordre** på startsiden.
2. Velg ordren som skal annulleres. Klikk **Avbryt** nederst på siden.

### <a name="create-a-return-order"></a>Opprette en returordre

1. Klikk **Finn en ordre** på startsiden.
2. Velg ordren som skal returneres, velg fakturaen for ordren, og velg produktlinjen for varen som skal returneres.
3. Klikk **Returordre** nederst på siden.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynkron transaksjonsflyt for kundeordrer

Kundeordrer kan opprettes fra salgssted-klienten i synkron eller asynkron modus.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>La kundeordrer opprettes i asynkron modus

1. Klikk **Retail** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofil** &gt; **Funksjonalitetsprofiler**.
2. På **Generelt**-hurtigfanen angir du **Opprett kundeordre i asynkron modus** til **Ja**.

Når alternativet **Opprett kundeordre i asynkron modus** er satt til **Ja**, opprettes alltid kundeordrer i asynkron modus, selv om Retail Transaction Service (RTS) er tilgjengelig. Hvis du setter dette alternativet til **Nei**, opprettes alltid kundeordrer i synkron modus ved hjelp av RTS. Når det opprettes kundeordrer i asynkron modus, hentes og settes de inn i Retail ved hentejobber (P-jobber). De tilsvarende salgsordrene opprettes i Retail når **Synkroniser ordrer** kjøres manuelt eller via en satsvis prosess.

## <a name="additional-resources"></a>Tilleggsressurser

[Hybride kundeordrer](hybrid-customer-orders.md)

---
title: Konfigurere sentralisert betaling
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 44d51807cd6bb64ae2c4bef58d8a445417ffa3a9
ms.openlocfilehash: 815282422a6d7b8eef7d0628cf10b715449e1d1d
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-centralized-payments"></a>Konfigurere sentralisert betaling



Følg disse trinnene for å klargjøre for behandling av betalinger i en juridisk enhet på vegne av andre juridiske enheter i organisasjonen. Før du begynner, må følgende oppsett fullføres:

-   Opprette juridiske enheter.
-   Definere parametere for økonomimodul og kontoplaner.
-   Definere leverandørparametere og kundeparametere (avhengig av modulene som bruker sentralisert betaling).
-   Definere konserninternt regnskap.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Definere et organisasjonshierarki for sentralisert betaling
Du må definere et organisasjonshierarki for sentralisert betaling. Det samme organisasjonshierarkiet brukes til å behandle sentraliserte leverandørbetalinger og sentraliserte kundebetalinger. **Obs!**  Strukturen på hierarkiet spiller ingen rolle for sentraliserte betalinger. Alle juridiske enheter i hierarkiet kan behandle betalinger på vegne av andre juridiske enheter i hierarkiet. På siden **Organisasjonshierarkier** kan du opprette et nytt organisasjonshierarki.

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>Konfigurere konserninternt regnskap for sentralisert betaling
Når betalingstransaksjoner i gjeldende juridisk enhet utlignes mot fakturaer i andre juridiske enheter, opprettes de aktuelle inn- og utbetalingstransaksjonene for hver juridisk enhet. Du må angi den juridiske enheten hvor eventuelle kontantrabatter og realisert fortjeneste- eller tapsbeløp skal posteres. Før du begynner, må du avgjøre hvilken juridisk enhet du vil bruke til å behandle leverandør- og kundebetalinger. Hvis én juridisk enhet behandler leverandørbetalinger, men en annen juridisk enhet behandler kundebetalinger, må du bytte til hver enkelt juridiske enhet. På den **i det konserninterne regnskapet** siden, kan du velge en konsernintern relasjon-post for en juridisk enhet som du skal behandle betalinger på vegne av. På den **sentraliserte betalinger** -kategorien kan du velge om du vil postere kontanter rabatter til juridisk enhet for betalingen (eller andre transaksjoner som reduserer saldoen på leverandørkontoen) eller den juridiske enheten for fakturaen (eller andre transaksjoner som øker saldoen på leverandørkontoen). Dette valget fungerer sammen med feltet **Håndtering av kontantrabatt** på sidene **Leverandørparametere** og **Kundeparametere**. For overbetalinger og øredifferanse brukes innstillingen i den juridiske enheten for betalingen. For underbetalinger og øredifferanse brukes innstillingen i den juridiske enheten for fakturaen.

## <a name="map-vendor-accounts-across-legal-entities"></a>Tilordne leverandørkontoer på tvers av juridiske enheter
Hvis du betaler en leverandør fra én juridisk enhet og velge fakturaer for den samme leverandøren i andre juridiske enheter, må du sikre at alle de samsvarende leverandørkontoene i hver av de juridiske enhetene bruker samme adressebok-ID. Hvis du mottar en betaling fra en kunde som betaler fakturaer i flere enn én juridisk enhet, må du passe på at alle de tilsvarende kundekontoene i hver juridisk enhet alle bruker den samme adressebok-ID.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>Konfigurere posteringsprofiler for sentralisert betaling
Når du oppretter en betaling i en juridisk enhet som utligner fakturaer i andre juridiske enheter, må posteringsprofil-IDene være like i de to juridiske enhetene. For å garantere at betalingene opprettes riktig, konfigurerer du en posteringsprofil i hver juridisk enhet for faktura som tilsvarer posteringsprofilene som brukes i den juridiske enheten for betalingen. Bytt til den første juridiske enheten for fakturaen, og deretter på den **leverandørposteringsprofiler** siden, kan du opprette en ny posteringsprofil eller redigere en eksisterende posteringsprofil. Valgene du gjør for posteringsprofilen i den juridiske enheten for fakturaen trenger ikke å samsvare med oppsettet av posteringsprofilen i den juridiske enheten for betalingen.

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>Definere betalingsmåter for sentralisert betaling
Når du oppretter en betaling i en juridisk enhet som utligner fakturaer i andre juridiske enheter, må betalingsmåte-IDene være like i de to juridiske enhetene. For å garantere at betalingene opprettes riktig, konfigurerer du en betalingsmåte i hver juridisk enhet for faktura som tilsvarer betalingsmåtene som brukes i den juridiske enheten for betalingen. Bytt til den første juridiske enheten for fakturaen, og gå deretter til siden **Betalingsmåter**der du kan opprette en ny betalingsmåte eller redigere en eksisterende betalingsmåte. Valgene du gjør for betalingsmåten i den juridiske enheten for fakturaen, trenger ikke å stemme overens med konfigurasjonen av betalingsmåten i den juridiske enheten for betalingen.

## <a name="set-up-default-descriptions"></a>Definere standardbeskrivelser
Du kan definere standardbeskrivelser for bilagene for utligning på tvers av firmaer. Standardbeskrivelsen blir tatt med på innbetalings- og utbetalingstransaksjonene under prosessen med utligning på tvers av firmaer. På siden **Standardbeskrivelser** kan du opprette nye beskrivelser for både **Konsernintern kundeutligning** og **Konsernintern leverandørutligning** ved å velge et språk og deretter skrive inn tekst.



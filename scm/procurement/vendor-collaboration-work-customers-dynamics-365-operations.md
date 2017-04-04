---
title: "Leverandørsamarbeid med kunder"
description: "Dette emnet beskriver hvordan du kan bruke leverandørsamarbeid i Microsoft Dynamics 365 for Operations for å arbeide med bestillinger og overvåke forsendelseslager."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 11cd2242b5a575ae87b0dbcf6f8ce268fcea5377
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-with-customers"></a>Leverandørsamarbeid med kunder

Dette emnet beskriver hvordan du kan bruke leverandørsamarbeid i Microsoft Dynamics 365 for Operations for å arbeide med bestillinger og overvåke forsendelseslager.

Dette emnet beskriver hvordan du kan bruke leverandørsamarbeid for å arbeide med kunder i Microsoft Dynamics 365 for Operations. Den inneholder informasjon om hvordan du kan overvåke og respondere på bestillinger, og hvordan du overvåker lageret for forsendelse. Det er også mulig å bruke leverandør-samarbeid for å arbeide med fakturaer. Hvis du vil ha mer informasjon, se [leverandøren samarbeid fakturering arbeidsområde for](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace).

## <a name="working-with-purchase-orders"></a>Arbeide med bestillinger
Arbeidsområdet **Bestillingsbekreftelsen** lar deg svare på bestillingene som er sendt til deg for gjennomgang. Det lar deg også vise informasjon om bestillinger som venter på handling fra kunden og bestillinger som er bekreftet, men fremdeles er åpne. Det er tre lister i arbeidsområdet **Bestillingsbekreftelsen**:

-   **Bestillinger for gjennomgang** -denne listen viser POs som er sendt til deg, og venter på svar fra deg. Når du svarer, forsvinner Bestillingen fra listen. Hvis kunden sender deg en ny versjon av bestillingen før du har svart på den forrige, vises bare den nyeste versjonen.
-   **Venter på kundehandling** – Listen lar deg se bestillinger som du har svart på, men som ennå ikke er bekreftet av kunden. Hvis du godtok bestillingen, kan du overvåke den i denne listen til statusen endres til **Bekreftet**. Hvis du avviste bestillingen eller godtok den med endringene, kan du overvåke bestillingen her til kunden sender en ny versjon.
-   **Åpne bekreftede bestillinger** – Denne listen inneholder alle bestillingene for kontoen som har statusen **Bekreftet**. Når produkter eller tjenester er fullstendig mottatt mot bestillingen, forsvinner bestillingen fra listen.

Listen nedenfor viser de fire sidene som du kan bruke til å arbeide med bestillinger, der to inneholder den samme informasjonen som vises i arbeidsområdet:

-   **Bestillinger for vurdering** (se ovenfor)
-   **Logg for leverandørbekreftelse for bestilling** – Denne siden inneholder alle bestillinger og alle versjoner av bestillinger som er sendt til leverandøren, og alle svarene som er returnert fra leverandøren.
-   **Åpne bekreftede bestillinger** (se ovenfor)
-   **Alle bekreftede bestillinger** – Denne siden inneholder alle bestillinger som er bekreftet, inkludert de som inneholder produkter eller tjenester som er mottatt. Du kan bruke denne listen til å overvåke hvilke bestillinger du kan sende fakturaer for.

### <a name="responding-to-purchase-orders"></a>Svare på bestillinger

Bestillinger som kunden har sendt deg til å se er synlige i den **bestillingsbekreftelsen** arbeidsområdet og den **bestillinger for gjennomgang** siden. Når du åpner en bestilling, kan du velge å godta den, avvise den eller godta den med endringene. Det kan være vedlegg i bestillingshodet eller på de enkelte linjene. Du kan også legge til informasjon i svaret på bestillingshodet eller enkeltlinjer. Du kan for eksempel foreslå en erstatningsvare for én av linjene. Du kan forhåndsvise og skrive ut bestillingen som en PDF-fil ved hjelp av alternativet **Forhåndsvis/Skriv ut**. Du kan skjule eller vise følgende dimensjonskolonner ved hjelp av handlingen **Visningsdimensjoner**: område, lager, farge, størrelse, stil, konfigurasjon. Hvis du bruker den **godta med endringer** alternativet, kan du godta eller avvise enkeltlinjer. Du kan også gjøre følgende endringer på linjer:

-   Endre datoer eller antall. Hvis du vil oppdatere den bekreftede leveringsdatoen på alle linjene, kan du bruke alternativet **Oppdater leveringsdato** i bestillingshodet.
-   Dele linjer for ulike leveringsdatoer eller antall
-   Erstatte en vare. Hvis du vil gjøre dette, kan du angi en varebeskrivelse og varenummeret i **Ekstern**-feltet i delen **Linjedetaljer**.

Du kan ikke endre prisinformasjon eller gebyrer, men du kan foreslå endringer i disse ved hjelp av merknader. Hvis kunden sender deg en ny versjon av en bestilling, vil denne ha et versjonssuffiks for å angi at det er en endret versjon av en bestilling som tidligere ble formidlet. Siden **Logg for leverandørbekreftelse for bestilling** lar deg spore historikken for hver ordre.

## <a name="monitoring-consignment-inventory"></a>Overvåke forsendelseslager
Hvis du bruker forsendelseslager, kan du bruke grensesnittet for leverandørsamarbeid til å vise informasjon på følgende sider:

-   **Bestillinger forbruker forsendelse lager** -bestillinger for forsendelse lagerbeholdningen blir generert når kunden tar eierskap av lageret. Disse forsendelsesbestillingene vises bare på siden **Bruk av forsendelseslager for bestillinger**. De er ikke inkludert på siden **Alle bekreftede bestillinger**.
-   **Produkter mottatt fra forsendelseslager** – Denne siden viser alle transaksjoner der eierskapet for produkter er blitt overført til firmaet som bruker lageret. Du kan bruke denne informasjonen for fakturere kunden.
-   **Forsendelseslager for beholdning** – Denne siden viser forsendelseslageret for beholdning som eies av firmaet som er på lager på kundens lager.


<a name="see-also"></a>Se også
--------

[Administrere brukere av leverandørsamarbeid](manage-vendor-collaboration-users.md)



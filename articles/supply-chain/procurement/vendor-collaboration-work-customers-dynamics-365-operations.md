---
title: "Leverandørsamarbeid med kunder"
description: "Dette emnet beskriver hvordan du kan bruke leverandørsamarbeid i Finance and Operations for å arbeide med bestillinger og overvåke forsendelseslager."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 6119f1c85b68e6ed5dce01a266c4e681dfc4cd30
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="vendor-collaboration-with-customers"></a>Leverandørsamarbeid med kunder

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hvordan du kan bruke leverandørsamarbeid i Finance and Operations for å arbeide med bestillinger og overvåke forsendelseslager.

Dette emnet beskriver hvordan du kan bruke leverandørsamarbeid for å arbeide med kunder i Microsoft Finance and Operations. Det inneholder informasjon om hvordan du overvåker og svare på bestillinger og hvordan du overvåker forsendelseslageret. Det er også mulig å bruke leverandørsamarbeid for å arbeide med fakturaer. Hvis du vil ha mer informasjon, kan du se [Arbeidsområde for leverandørsamarbeidsfakturering](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md).

## <a name="working-with-purchase-orders"></a>Arbeide med bestillinger
Arbeidsområdet **Bestillingsbekreftelsen** lar deg svare på bestillingene som er sendt til deg for gjennomgang. Det lar deg også vise informasjon om bestillinger som venter på handling fra kunden og bestillinger som er bekreftet, men fremdeles er åpne. Det er tre lister i arbeidsområdet **Bestillingsbekreftelsen**:

-   **Bestillinger for vurdering** – Denne listen viser bestillinger som er sendt til deg og venter på svar fra deg. Når du har svart, forsvinner bestillingen fra listen. Hvis kunden sender deg en ny versjon av bestillingen før du har svart på den forrige, vises bare den nyeste versjonen.
-   **Venter på kundehandling** – Listen lar deg se bestillinger som du har svart på, men som ennå ikke er bekreftet av kunden. Hvis du godtok bestillingen, kan du overvåke den i denne listen til statusen endres til **Bekreftet**. Hvis du avviste bestillingen eller godtok den med endringene, kan du overvåke bestillingen her til kunden sender en ny versjon.
-   **Åpne bekreftede bestillinger** – Denne listen inneholder alle bestillingene for kontoen som har statusen **Bekreftet**. Når produkter eller tjenester er fullstendig mottatt mot bestillingen, forsvinner bestillingen fra listen.

Listen nedenfor viser de fire sidene som du kan bruke til å arbeide med bestillinger, der to inneholder den samme informasjonen som vises i arbeidsområdet:

-   **Bestillinger for vurdering** (se ovenfor)
-   **Logg for leverandørbekreftelse for bestilling** – Denne siden inneholder alle bestillinger og alle versjoner av bestillinger som er sendt til leverandøren, og alle svarene som er returnert fra leverandøren.
-   **Åpne bekreftede bestillinger** (se ovenfor)
-   **Alle bekreftede bestillinger** – Denne siden inneholder alle bestillinger som er bekreftet, inkludert de som inneholder produkter eller tjenester som er mottatt. Du kan bruke denne listen til å overvåke hvilke bestillinger du kan sende fakturaer for.

### <a name="responding-to-purchase-orders"></a>Svare på bestillinger

Bestillingene som kunden har sendt til deg for gjennomgang, vises i arbeidsområdet **Bestillingsbekreftelse** og på siden **Bestillinger for vurdering**. Når du har åpnet en bestilling, kan du velge å godta den, avvise den eller godta den med endringer. Det kan være vedlegg i bestillingshodet eller på de enkelte linjene. Du kan også legge til informasjon i svaret på bestillingshodet eller enkeltlinjer. Du kan for eksempel foreslå en erstatningsvare for én av linjene. Du kan forhåndsvise og skrive ut bestillingen som en PDF-fil ved hjelp av alternativet **Forhåndsvis/Skriv ut**. Du kan skjule eller vise følgende dimensjonskolonner ved hjelp av handlingen **Visningsdimensjoner**: område, lager, farge, størrelse, stil, konfigurasjon. Hvis du bruker alternativet **Godta med endringer**, kan du godta eller avvise enkeltlinjer. Du kan også foreta følgende endringer i linjer:

-   Endre datoer eller antall. Hvis du vil oppdatere den bekreftede leveringsdatoen på alle linjene, kan du bruke alternativet **Oppdater leveringsdato** i bestillingshodet.
-   Dele linjer for ulike leveringsdatoer eller antall
-   Erstatte en vare. Hvis du vil gjøre dette, kan du angi en varebeskrivelse og varenummeret i **Ekstern**-feltet i delen **Linjedetaljer**.

Du kan ikke endre prisinformasjon eller gebyrer, men du kan foreslå endringer i disse ved hjelp av merknader. Hvis kunden sender deg en ny versjon av en bestilling, vil denne ha et versjonssuffiks for å angi at det er en endret versjon av en bestilling som tidligere ble formidlet. Siden **Logg for leverandørbekreftelse for bestilling** lar deg spore historikken for hver ordre.

## <a name="monitoring-consignment-inventory"></a>Overvåke forsendelseslager
Hvis du bruker forsendelseslager, kan du bruke grensesnittet for leverandørsamarbeid til å vise informasjon på følgende sider:

-   **Bruk av forsendelseslager for bestillinger** – Bestillinger for forsendelseslager genereres når kunden blir eier av lageret. Disse forsendelsesbestillingene vises bare på siden **Bruk av forsendelseslager for bestillinger**. De er ikke inkludert på siden **Alle bekreftede bestillinger**.
-   **Produkter mottatt fra forsendelseslager** – Denne siden viser alle transaksjoner der eierskapet for produkter er blitt overført til firmaet som bruker lageret. Du kan bruke denne informasjonen for fakturere kunden.
-   **Forsendelseslager for beholdning** – Denne siden viser forsendelseslageret for beholdning som eies av firmaet som er på lager på kundens lager.


<a name="see-also"></a>Se også
--------

[Administrere brukere av leverandørsamarbeid](manage-vendor-collaboration-users.md)





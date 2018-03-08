---
title: Migrere produkter og lagerstyring fra AX 2012 til Finance and Operations
description: Dette emnet gir en oversikt over migreringsalternativer for produkt og lagerstyring.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7c6d40e3b80a0974c722ad3a88a29adc8dedf585
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="migrate-products-and-warehouse-management-from-ax-2012-to-finance-and-operations"></a>Migrere produkter og lagerstyring fra AX 2012 til Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emnet gir en oversikt over alternativene for migrasjon av produkt- og lagerstyring i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

<a name="introduction"></a>Introduksjon
------------

Under en oppgradering til Finance and Operations blokkeres produkter hvis de er knyttet til en lagringsdimensjonsgruppe som har innstillinger som ikke samsvarer med kravene til innstillingene for lagringsdimensjonsgrupper i Finance and Operations. Etter oppgraderingen, kan du imidlertid bruke et sett med alternativer for overføring i  **Endre lagringsdimensjonsgruppen for varer**-prosessen for å fjerne blokkeringen av produkter som er blokkert under oppgraderingen. Deretter kan du behandle transaksjoner for disse produktene. Noen av elementene kan allerede være knyttet til lagringsdimensjonsgrupper der lagerdimensjonene område, lager og lokasjon er aktiv og fysisk sporet. I så fall kan du bruke **Endre lagringsdimensjonsgruppen for varer**-prosessen for å aktivere elementene som skal brukes i lagerstyringsprosesser. Denne funksjonen er nyttig hvis du vil bruke i lagerstyringsfunksjonen for eksisterende varer.

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a>Oppgradering til Finance and Operations når AX 2012 R3 WMSII brukes
Finance and Operations støtter ikke lenger den gamle **WMSII**-modulen fra Microsoft Dynamics AX 2012. I stedet kan du bruke den nye **Lagerstyring**-modulen. I tidligere versjoner kunne du velge lagerdimensjonene lokasjon og pall-ID for økonomisk lager. Som en del av oppgraderingsprosessen, kan imidlertid lagerdimensjonen pall-ID ikke lenger aktiveres for økonomisk lager. Alle produkter som er tilknyttet en lagringsdimensjonsgruppe som bruker pall-ID-lagerdimensjonen, blokkeres, og vil ikke bli behandlet.

### <a name="enabling-items-in-finance-and-operations"></a>Aktivere varer i Finance og Operations

I Finance and Operations må varer som skal brukes som en del av lagerstyringsprosesser, være tilknyttet en lagringsdimensjonsgruppe hvor parameteren **Bruk lagerstyringsprosesser** er valgt. Når denne innstillingen er valgt, blir lagerdimensjonene område, lager, lagerstatus, lokasjon og nummerskilt aktive. Du kan bare endre til denne typen lagringsdimensjonsgruppe for varer som allerede er tilknyttet lagringsdimensjonsgrupper der lagerdimensjonen lokasjon er aktiv.

### <a name="items-that-are-blocked-for-inventory-updates"></a>Varer som er sperret for beholdningsoppdateringer

For å vise listen over frigitte produkter som er blokkert under oppgraderingen og ikke kan behandles, klikker du **Lagerstyring** &gt; **Oppsett** &gt; **Beholdning** &gt; **Varer som er sperret for beholdningsoppdateringer**.

### <a name="reapplying-blocked-products"></a>Bruke sperrede produkter på nytt

Hvis du vil oppheve blokkeringen av produkter som er blokkert under oppgraderingen, må du velge en ny lagringsdimensjonsgruppe for produktene. Vær oppmerksom på at du kan endre lagringsdimensjonsgruppen selv om det finnes åpne lagertransaksjoner. Hvis du vil bruke varer som ble blokkert under oppgradering, har du to alternativer:

-   Endre lagringsdimensjonsgruppen for varen til en lagringsdimensjonsgruppe som bare bruker lagerdimensjonene området lager og lokasjon. Som følge av denne endringen brukes ikke lagerdimensjonen pall-ID lenger.
-   Endre lagringsdimensjonsgruppen for varen til en lagringsdimensjonsgruppe som bare bruker lagerstyringsprosessene. Som følge av denne endringen brukes nå lagerdimensjonen nummerskilt.

### <a name="migration-processes"></a>Migreringsprosesser

I Finance and Operations er varesporing en del av lagerstyringsprosessene. For disse prosessene må alle lagre og deres lokasjoner være tilknyttet en lokasjonsprofil. Begrepsmessig, hvis du vil bruke lager lagerstyringsprosesser, må to prosesser behandles:

-   Eksisterende lagre må aktiveres for å bruke lagerstyringsprosesser.
-   Eksisterende frigitte produkter må være knyttet til en ny lagringsdimensjonsgruppe som bruker lagerstyringsprosesser.

Hvis kilde-lagringsdimensjonsgruppene bruker lagerdimensjonen pall-ID, må lokasjonene til eksisterende lagerbeholdning som brukte lagerdimensjonen pall-ID, tilknyttes en lokasjonsprofil der **Bruk sporing av nummerskilt**-parameteren er valgt. Hvis de eksisterende lagrene ikke skal aktiveres for bruk av lagerstyringsprosesser, kan du endre den eksisterende lagerbeholdningens lagringsdimensjonsgrupper til grupper som bare håndterer lagerdimensjonene område, lager og lokasjon.

### <a name="using-the-warehouse-management-processes"></a>Bruke lagerstyringsprosessene

Før du kan bruke frigitte produkter i **Lagerstyring**-modulen, må produktene bruke en lagringsdimensjonsgruppe hvor **Bruk lagerstyringsprosesser**-parameteren er valgt.

#### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Aktivere lagre for bruke av lagerstyringsprosesser

1.  Opprett minst én ny lokasjonsprofil.
2.  Klikk **Lagerstyring** &gt; **Oppsett** &gt; **Aktiver lagerstyringsprosesser** &gt; **Aktiver lageroppsettet**.
3.  På **Aktiver lageroppsettet**-siden, legger du til lagrene som du vil aktivere. Du kan fullføre dette trinnet, enten direkte på siden, eller ved hjelp av Microsoft Office-integrering.
4.  Tilordne en lokasjonsprofil til alle lokasjonene. Du kan enkelt fullføre dette trinnet, ved hjelp av Microsoft Office-integrering, direkte på siden. Du kan eksportere og importere dataene, eller bruke dataenhetsbehandlingen i [Databehandling](../../dev-itpro/data-entities/data-entities.md).
5.  Valider endringene. Som en del av valideringsprosessen forekommer ulike valideringer for dataintegritet. Som en del av en større oppgraderingsprosess må problemer som oppstår, kanskje justeres på kildeimplementeringen. I så fall kreves en ytterligere oppgradering av data.
6.  Behandle endringene.

#### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Endre lagringsdimensjonsgruppen for varer, slik at den bruker lagerstyringsprosesser

1.  Opprett en ny **lagerstatuse**-verdi, og tilordne den som **standard lagerstatus-ID**-verdi i innstillinger for **lagerstyringsparametere**.
2.  Opprett en ny lagringsdimensjonsgruppe der parameteren **Bruk lagerstyringsprosesser** er valgt.
3.  På  **Reservasjonshierarki**-siden kan du definere et nytt reservasjonshierarki i henhold til varens lagrings- og sporingsdimensjonsgrupper.
4.  Opprett én eller flere sekvensgrupper for enhet, som inneholder minst de samme enhetene som brukes for varens lagerenheter.
5.  Klikk **Lagerstyring** &gt; **Oppsett** &gt; **Aktivere lagerstyringsprosesser** &gt; **Endre lagringsdimensjonsgruppen for varer**.
6.  På **Endre lagringsdimensjonsgruppen for varer**-siden, legger du til varenumre, lagringsdimensjonsgrupper og sekvensgrupper for enhet. Du kan fullføre dette trinnet direkte på siden, ved hjelp av Microsoft Office-integrering, eller ved å bruke dataenhetsprosessen i [Databehandling](../../dev-itpro/data-entities/data-entities.md).
7.  Valider endringene. Som en del av valideringsprosessen forekommer ulike valideringer for dataintegritet. Som en del av en større oppgraderingsprosess må problemer som oppstår, kanskje justeres på kildeimplementeringen. I så fall kreves en ytterligere oppgradering av data.
8.  Behandle endringene. En oppdatering av alle lagerdimensjonene kan ta litt tid. Du kan overvåke fremdriften ved hjelp av satsvise jobboppgaver.




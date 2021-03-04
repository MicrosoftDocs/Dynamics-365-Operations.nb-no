---
title: Oppgradere lagerstyring fra Microsoft Dynamics AX 2012 til Supply Chain Management
description: Dette emnet gir en oversikt over migreringsalternativer for produkt og lagerstyring.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 123be2430f910dfbea438cb6a51be7203eb39fc8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434070"
---
# <a name="upgrade-warehouse-management-from-microsoft-dynamics-ax-2012-to-supply-chain-management"></a>Oppgradere lagerstyring fra Microsoft Dynamics AX 2012 til Supply Chain Management 


[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over prosessen med å oppgradere fra Microsoft Dynamics AX 2012 R3, kjører modulen WMSII til Supply Chain Management.

Supply Chain Management støtter ikke lenger den gamle **WMSII**-modulen fra Microsoft Dynamics AX 2012. I stedet kan du bruke **Lagerstyring**-modulen. I WMSII-modulen kan lagerdimensjonene Sted og Pall-ID velges for økonomisk lager, men lagerdimensjonen Pall-ID kan ikke brukes for økonomisk lager i Supply Chain Management.

Under en oppgradering blir alle produkter som er tilknyttet en lagringsdimensjonsgruppe som bruker lagerdimensjonen Pall-ID identifisert, merket som blokkert og ikke behandlet for oppgradering.

## <a name="upgrading-to-supply-chain-management-when-ax-2012-r3-wmsii-is-used"></a>Oppgradere til Supply Chain Management når AX 2012 R3 WMSII brukes
Etter oppgraderingen kan du bruke et sett med alternativer i skjemaet **Endre lagringsdimensjonsgruppen for varer** for å fjerne blokkeringen av produkter som ble blokkert under oppgraderingen, og deretter behandle transaksjoner for disse produktene.

### <a name="enabling-items-in-supply-chain-management"></a>Aktivere varer i Supply Chain Management 
Denne endringen er nødvendig fordi varesporing en del av lagerstyringsprosessene i Supply Chain Management. For disse prosessene må alle lagre og deres lokasjoner være tilknyttet en lokasjonsprofil. Hvis du vil bruke lagerstyringsprosesser, må følgende konfigureres:
-   Eksisterende lagre må aktiveres for å bruke lagerstyringsprosesser 
-   Eksisterende frigitte produkter må være knyttet til en lagringsdimensjonsgruppe som bruker lagerstyringsprosesser 

Hvis kilde-lagringsdimensjonsgruppene bruker lagerdimensjonen pall-ID, må lokasjonene til eksisterende lagerbeholdning som brukte lagerdimensjonen pall-ID, tilknyttes en lokasjonsprofil der **Bruk sporing av nummerskilt**-parameteren er valgt Hvis de eksisterende lagrene ikke skal aktiveres for bruk av lagerstyringsprosesser, kan du endre den eksisterende lagerbeholdningens lagringsdimensjonsgrupper til grupper som bare håndterer lagerdimensjonene område, lager og lokasjon. 

> [!NOTE] 
>  Du kan endre lagringsdimensjonsgruppen for varer, selv om det finnes åpne lagertransaksjoner.

## <a name="find-products-that-were-blocked-because-of-pallet-id"></a>Søke etter produkter som er blokkert på grunn av Pall-ID
For å vise listen over frigitte produkter som er blokkert under oppgraderingen og ikke kan behandles, klikker du **Lagerstyring** &gt; **Oppsett** &gt; **Beholdning** &gt; **Varer som er sperret for beholdningsoppdateringer**.

## <a name="change-storage-dimension-group-for-blocked-products"></a>Endre lagringsdimensjonsgruppe for sperrede produkter 
 
For å kunne brukes som en del av en lagerstyringsprosess må en vare være knyttet til en lagerdimensjonsgruppe der lokasjonsbeholdningsdimensjon er aktiv, og der parameteren **Bruk lagerstyringsprosesser** er valgt. Når denne innstillingen er valgt, blir lagerdimensjonene område, lager, lagerstatus, lokasjon og nummerskilt aktive.

Hvis du vil oppheve blokkeringen av produkter som er blokkert under oppgraderingen, må du velge en ny lagringsdimensjonsgruppe for produktene. Vær oppmerksom på at du kan endre lagringsdimensjonsgruppen selv om det finnes åpne lagertransaksjoner. Hvis du vil bruke varer som ble blokkert under oppgradering, har du to alternativer:

-   Endre lagringsdimensjonsgruppen for varen til en lagringsdimensjonsgruppe som bare bruker lagerdimensjonene området lager og lokasjon. Som følge av denne endringen brukes ikke lagerdimensjonen pall-ID lenger.
-   Endre lagringsdimensjonsgruppen for varen til en lagringsdimensjonsgruppe som bare bruker lagerstyringsprosessene. Som følge av denne endringen brukes nå lagerdimensjonen nummerskilt.

## <a name="configure-warehouse-management-processes"></a>Konfigurere lagerstyringsprosesser
Før du kan bruke frigitte produkter i **Lagerstyring**-modulen, må produktene bruke en lagringsdimensjonsgruppe hvor **Bruk lagerstyringsprosesser**-parameteren er valgt.

### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Aktivere lagre for bruke av lagerstyringsprosesser

1.  Opprett minst én ny lokasjonsprofil.
2.  Klikk **Lagerstyring** &gt; **Oppsett** &gt; **Aktiver lagerstyringsprosesser** &gt; **Aktiver lageroppsettet**.
3.  På **Aktiver lageroppsettet**-siden, legger du til lagrene som du vil aktivere. Du kan fullføre dette trinnet, enten direkte på siden, eller ved hjelp av Microsoft Office-integrering.
4.  Tilordne en lokasjonsprofil til alle lokasjonene. Du kan enkelt fullføre dette trinnet, ved hjelp av Microsoft Office-integrering, direkte på siden. Du kan eksportere og importere dataene, eller bruke dataenhetsbehandlingen i [Databehandling](../../dev-itpro/data-entities/data-entities.md).
5.  Valider endringene. Som en del av valideringsprosessen forekommer ulike valideringer for dataintegritet. Som en del av en større oppgraderingsprosess må problemer som oppstår, kanskje justeres på kildeimplementeringen. I så fall kreves en ytterligere oppgradering av data.
6.  Behandle endringene.

### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Endre lagringsdimensjonsgruppen for varer, slik at den bruker lagerstyringsprosesser

1.  Opprett en ny **lagerstatuse**-verdi, og tilordne den som **standard lagerstatus-ID**-verdi i innstillinger for **lagerstyringsparametere**.
2.  Opprett en ny lagringsdimensjonsgruppe der parameteren **Bruk lagerstyringsprosesser** er valgt.
3.  På  **Reservasjonshierarki**-siden kan du definere et nytt reservasjonshierarki i henhold til varens lagrings- og sporingsdimensjonsgrupper.
4.  Opprett én eller flere sekvensgrupper for enhet, som inneholder minst de samme enhetene som brukes for varens lagerenheter.
5.  Klikk **Lagerstyring** &gt; **Oppsett** &gt; **Aktivere lagerstyringsprosesser** &gt; **Endre lagringsdimensjonsgruppen for varer**.
6.  På **Endre lagringsdimensjonsgruppen for varer**-siden, legger du til varenumre, lagringsdimensjonsgrupper og sekvensgrupper for enhet. Du kan fullføre dette trinnet direkte på siden, ved hjelp av Microsoft Office-integrering, eller ved å bruke dataenhetsprosessen i [Databehandling](../../dev-itpro/data-entities/data-entities.md).
7.  Valider endringene. Som en del av valideringsprosessen forekommer ulike valideringer for dataintegritet. Som en del av en større oppgraderingsprosess må problemer som oppstår, kanskje justeres på kildeimplementeringen. I så fall kreves en ytterligere oppgradering av data.
8.  Behandle endringene. En oppdatering av alle lagerdimensjonene kan ta litt tid. Du kan overvåke fremdriften ved hjelp av satsvise jobboppgaver.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
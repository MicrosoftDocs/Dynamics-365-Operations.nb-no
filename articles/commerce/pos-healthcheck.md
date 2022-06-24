---
title: Tilstandskontroll for eksterne enheter og tjenester for salgssted
description: Denne artikkelen gir en oversikt over tilstandssjekkoperasjonen i salgsstedet (POS).
author: BrianShook
ms.date: 03/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 44fd4b6246d3d7947527416c2b8b447bd64f179f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863327"
---
# <a name="health-check-for-pos-peripherals-and-services"></a>Tilstandskontroll for eksterne enheter og tjenester for salgssted

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver tilstandssjekkoperasjonen i salgsstedet (POS).

## <a name="overview"></a>Oversikt

Detaljhandelbutikker kan være komplekse miljøer der det brukes mange programmer og enheter. Når operasjoner vokser, kan det bli vanskelig å sikre at operasjoner alltid går problemfritt, på grunn av avhengigheter. Eksterne enheter kan for eksempel ødelegges eller kobles fra ved et uhell i løpet av en dag. Feilsøking for problemer som er knyttet til enheter og tjenester, kan være kostbare for større forhandlere og like frustrerende for mindre operasjoner.

Microsoft Dynamics 365 Commerce-versjoner 10.0.10 og senere inneholder en tilstandskontroll som kan bidra til å forhindre noe av denne kostnaden og frustrasjon. Denne operasjonen inneholder en metode for å teste enheter direkte fra POS utenfor normal drift. Det kan derfor hjelpe forhandlere med å oppdage problemer før de oppstår.

## <a name="key-terms"></a>Viktige termer

| Semester | beskrivelse |
|---|---|
| Ekstern enhet | Alle enheter som POS-programmet bruker til å forenkle transaksjoner og andre operasjoner i butikken. Eksempler inkluderer kassaskuffer, strekkodeskannere og betalingsterminaler. |
| Tjeneste | I denne artikkelen er en tjeneste et tilleggsprogram som POS-programmet er avhengig av å utføre transaksjoner og daglige operasjoner. Eksempler inkluderer apper som kan hjelpe med skatt eller forsendelsesberegninger. |

## <a name="health-check-operation"></a>Tilstandskontrolloperasjon

Tilstandskontrollen er operasjon 717 på siden **POS-operasjoner** i Commerce Headquarters. Den kan brukes mens POS er i ikke-skuff-modus. En maskinvarestasjon må imidlertid være aktiv.

Som standard tester tilstandskontrollen bare enheter som er konfigurert i maskinvareprofilen for maskinvarestasjonen som for øyeblikket er aktiv for en kasse. Hvis en kasse bruker flere maskinvarestasjoner i løpet av en dag, må den koble til én maskinvarestasjon om gangen for å gjøre tilstandskontroller for alle. Det finnes ingen tilstandskontroll på butikknivå. Det er imidlertid mulig at denne typen kontroll kan utføres via Commerce Server-utvidelse.

### <a name="out-of-box-health-checks"></a>Medfølgende tilstandskontroller

| Type | Tilkobling | Detaljer |
|---|---|---|
| Skriver | OPOS | Denne kontrollen tester grunnleggende funksjoner for kobling og innebygging av objekter (OPOS). Her er noen eksempler:<ul><li>Åpne: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Lukk: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| Linjevisning | OPOS | Denne kontrollen tester grunnleggende OPOS-funksjoner. Her er noen eksempler:<ul><li>Åpne: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Lukk: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| Dobbel visning | Windows | Denne kontrollen sikrer at operativsystemet registrerer en ny Windows-skjerm. | 
| Kortleser | OPOS | Denne kontrollen tester grunnleggende OPOS-funksjoner. Her er noen eksempler:<ul><li>Åpne: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Lukk: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| Trassent | OPOS | Denne kontrollen tester grunnleggende OPOS-funksjoner. Her er noen eksempler:<ul><li>Åpne: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Lukk: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> | 
| Skanner | OPOS | Denne kontrollen tester grunnleggende OPOS-funksjoner. Her er noen eksempler:<ul><li>Åpne: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Lukk: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> | 
| Skala | OPOS | Denne kontrollen tester grunnleggende OPOS-funksjoner. Her er noen eksempler:<ul><li>Åpne: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Lukk: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| PIN-kodetastatur | OPOS | Denne kontrollen tester grunnleggende OPOS-funksjoner. Her er noen eksempler:<ul><li>Åpne: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Lukk: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| Betalingsterminal | SDK for betalinger | Denne avmerkingsboksen tester grunnleggende betalingsterminalfunksjoner fra SDK for betalinger. <ul><li>Lås</li><li>BeginTransaction</li><li>EndTransaction</li><li>ReleaseDevice</li><li>Close</li></ul> |

### <a name="using-the-health-check-operation-in-the-pos"></a>Bruke tilstandskontrollen i salgsstedet

Når tilstandskontrollen startes i POS, viser en rute til høyre de konfigurerte enhetene og statusen for hver enhet. Hvis du vil utføre en tilstandskontroll for en enkelt enhet, velger du enheten og velger deretter **Test valgt**. Hvis du vil utføre en tilstandskontroll for alle enheter, velger du **Test alle**. **Test alle**-funksjonen tester alle enhetene, én om gangen, og oppdaterer statusen for hver enhet i **Status**-kolonnen.

Kolonnen **Siste sjekk** viser når tilstandskontrollen sist ble utført for hver enhet.

Hvis tilstandskontrollen for en enhet lykkes (det vil si hvis det ikke oppstår feil), vil enhetens status være **OK**. Hvis tilstandskontrollen mislykkes, vil statusen angi at det var en feil. I dette tilfellet gir ruten til høyre detaljer som er relatert til feilen, eller instruerer brukeren om å kontakte systemadministratoren.

Noen enheter, for eksempel OPOS-tastelås, har ikke medfølgende tilstandskontroll. Hvis en tilstandskontroll ikke blir funnet for noen enheter som brukes, er statusen **Støttes ikke**.

### <a name="extending-health-checks"></a>Utvide tilstandskontroller

De medfølgende tilstandskontrollene er ikke konfigurert for å gi noen brukervennlige meldinger til vanlige feil. Men ikke alle scenariene dekkes. Gjennom utvidelse kan forhandlere tilordne brukervennlige meldinger til feil som kan være spesifikke for deres miljø.

Egendefinerte tilstandskontroller kan også opprettes for å teste enheter som ikke støttes som standard, eller til å teste tjenester som POS er avhengig av.

## <a name="related-articles"></a>Relaterte artikler

[Utløsere og utskrift for Modern POS (MPOS)](dev-itpro/pos-trigger-printing.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Velge mellom Modern POS (MPOS) og Cloud POS
description: Dette emnet beskriver viktige forskjeller mellom Modern POS og Cloud POS. Det beskriver også forskjellige faktorer som forhandlere som implementerer Dynamics 365 Commerce, må vurdere slik at de kan gjøre det beste valget for sine behov.
author: jblucher
manager: AnnBe
ms.date: 10/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 508fda28d8f815f030e7b163709393f70904a5fd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414552"
---
# <a name="choose-between-modern-pos-mpos-and-cloud-pos"></a>Velge mellom Modern POS (MPOS) og Cloud POS

[!include [banner](includes/banner.md)]

Dette emnet gir implementerere mer bakgrunn, tips og retningslinjer for faktorer som de bør vurdere når de distribuerer Dynamics 365 Commerce. Ved å se gjennom og følge denne veiledningen som en del av distribusjonsprosessen, kan implementerere unngå problemer som kan påvirke brukerens tilfredshet eller ytelse.

## <a name="insights"></a>Innsikt

Commerce inneholder en rekke distribusjons- og topologialternativer. Forhandlere kan derfor velge komponentene og konfigurasjonen som best dekker deres forretningsbehov og tekniske behov. En side ved implementering som krever nøye overveielse, er valget av plattform og formfaktor for komponenten salgssted (POS).

### <a name="pos-platform-and-form-factor-considerations"></a>Salgsstedsplattform- og formfaktorhensyn

Commerce støtter følgende salgsstedsalternativer:

- Modern POS (MPOS) for Microsoft Windows
- MPOS for Microsoft Windows Phone
- MPOS for Apple iPad eller Google Android-nettbrett
- Cloud POS (CPOS), som støtter Microsoft Edge, Internet Explorer og Google Chrome-nettlesere

I alle tilfellene deler POS (MPOS og CPOS) den samme kjerneprogramkoden. Dette er viktig av følgende årsaker:

- Brukergrensesnittet er konsekvent, uavhengig av plattform eller formfaktor.
- De fleste funksjonene er de samme, uavhengig av plattform eller formfaktor. Det er imidlertid noen viktige forskjeller. Disse ulikhetene går frem i dette emnet.
- Salgsstedsvariasjoner kan kombineres og kjøres samtidig i en gitt butikk. For hovedkassene kan for eksempel en forhandler bruke MPOS på datamaskiner som kjører Windows. Forhandleren kan imidlertid supplere disse kassene med leserbaserte terminaler eller mobilenheter.
- Tilpassinger og utvidelser kan enkelt brukes på tvers av plattformer og formfaktorer. Fordi kjerneprogramkoden deles, kan de fleste tilpasningene implementeres én gang i stedet for flere ganger.

### <a name="mpos-vs-cpos"></a>MPOS kontra CPOS

Selv om MPOS og CPOS stort sett er det samme, er det noen viktige forskjeller som du må forstå.

#### <a name="mpos"></a>MPOS

MPOS på en Windows-, iOS- eller Android-enhet er et program som er pakket, installert og betjent på denne enheten.

- **Windows** – MPOS for Windows-programmet inneholder all programkode og innebygd Commerce Runtime (CRT). 
- **iOS/Android** – På disse plattformene fungerer programmet som vert for CPOS-programkoden. Med andre ord kommer programkoden fra CPOS-serveren på Microsoft Azure eller Commerce Scale Unit. Hvis du vil ha mer informasjon, se [Oversikt over Commerce Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin).

#### <a name="cpos"></a>CPOS

Siden CPOS kjøres i en webleser, er ikke programmet installert på enheten. I stedet åpner nettleseren programkoden fra CPOS-serveren. Derfor kan ikke CPOS få tilgang til salgsstedsmaskinvare direkte eller fungere frakoblet.

### <a name="store-deployment-considerations"></a>Hensyn ved butikkdistribusjon

I tillegg til plattform og formfaktor må forhandlerne også velge et alternativ for distribusjon i butikken. Tabellen nedenfor inneholder konfigurasjonene som er tilgjengelige for hvert salgsstedsalternativ.

| POS-programmet         | Commerce Scale Unit | Tilgjengelig frakoblet |
|-------------------------|---------------|-------------------|
| MPOS for Windows        | Cloud eller RSSU | Ja               |
| MPOS for iOS eller Android | Cloud eller RSSU | Nei                |
| Skybasert salgssted               | Cloud eller RSSU | Nei                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

Commerce Scale Unit er en komponent som er vert for CRT. CRT inneholder all forretningslogikken som POS bruker, og det gir tilgang til kanaldatabasen. Når de er tilkoblet, bruker alle salgsstedsklientene i butikken Commerce Scale Unit Commerce Scale Unit kan distribueres i skyen eller butikken.

#### <a name="offline-mode"></a>Frakoblet modus

MPOS for Windows støtter frakoblet modus. I frakoblet modus kan salgsstedet fortsette å behandle salg selv om det er koblet fra Commerce Scale Unit. Det kan deretter synkroniseres med kanaldatabasen når tilkoblingen er gjenopprettet. MPOS bruker sin egen innebygde forekomst av CRT og bruker midlertidig sin egen lokale datakilde (frakoblet SQL Server-database). Hvis du vil ha mer informasjon om funksjonalitet for frakoblet bruk, kan du se [Frakoblet funksjonalitet for salgssted](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-offline-functionality).

### <a name="pos-peripheralhardware-considerations"></a>Vurderinger for salgsstedstilbehør/-maskinvare

Forhandlere må også vurdere hvordan salgsstedet får tilgang til enheter og tilbehør som skrivere, kassaskuffer og betalingsterminaler. Bare MPOS for Windows støtter direkte kommunikasjon med disse enhetene. MPOS for Windows Phone, iOS eller Android og Cloud POS krever en maskinvarestasjon for å få tilgang til disse enhetene. Maskinvarestasjoner kan dedikeres til en salgsstedskasse eller deles mellom kassene i en butikk. Hvis du vil ha mer informasjon om maskinvarestasjoner, kan du se [Konfigurere og installere Retail-maskinvarestasjon](https://docs.microsoft.com/dynamics365/unified-operations/retail/retail-hardware-station-configuration-installation).

## <a name="implementation-considerations"></a>Informasjon om implementering

Vurder følgende informasjon når du planlegger POS-implementeringen i butikkene:

- **Funksjonskrav** – De sentrale forretningsprosessene og funksjonene er de samme, uavhengig av plattform, formfaktor eller distribusjonstopologi. De fleste forhandlere trenger derfor ikke vurdere krav til funksjonalitet når de planlegger implementeringen.
- **Tilkobling** – Nettverkstilgjengelighet (regionnett \[WAN\] og lokalnett \[LAN\]) er en viktig faktor som krever nøye overveielse. Eventuelle fordeler som en nullavtrykks, skybasert vertsløsning bringer når det gjelder kostnader og enkelhet, går tapt hvis systemet ikke er tilgjengelig for forretningskritiske prosesser.

    Med mindre tilkoblingen for en gitt enhet er svært pålitelig og fleksibel, eller med mindre en viss nedetid er akseptabelt for forhandleren, anbefaler vi ett av følgende alternativer:

    - Bruk MPOS i Windows, og aktiver frakoblet modus.
    - Distribuer en lokal Commerce Scale Unit.

    Disse to alternativene ikke er gjensidig utelukkende. For den mest pålitelige topologien, kan forhandlere distribuere en lokal RSSU for å redusere avhengighet av Internett-tilkobling eller Azure-tilgjengelighet, og de kan også distribuere kasser på salgsstedet der frakoblet modus er aktivert hvis det er et problem med den lokale serveren eller nettverket.

- **Enheter / eksterne enheter for maskinvare** – En viktig del av et Retail POS-system er evnen til å bruke eksterne salgsstedsenheter som skrivere, pengeskuffer og betalingsterminaler. Selv om alle de tilgjengelige salgsstedsalternativene kan bruke eksterne enheter, er det bare MPOS for Windows som støtter dem direkte. For alle andre programmer kreves det én eller flere maskinvarestasjoner. Selv om denne fremgangsmåten gir fleksibilitet, må tilleggskomponenter distribueres, konfigureres og betjenes.
- **Systemkrav** – Systemkravene for POS-programmet varierer. Husk å sjekke den nyeste informasjonen før du foretar valget. Siden CPOS kjører i en webleser, støtter den for eksempel en rekke operativsystemer. Hvis du vil ha mer informasjon om systemkrav, kan du se [Systemkrav for skydistribusjoner](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/system-requirements).
- **Distribusjon og betjening** – Kompleksiteten ved distribusjons- og betjeningskravene kan variere, avhengig av program- og distribusjonsvalgene. For eksempel for en skybasert CPOS-distribusjon trenger du ikke installere og oppdatere på hver enhet. Derfor reduserer denne tilnærmingen kompleksiteten og kostnadene. Hvis du imidlertid distribuerer MPOS på hver kasse og aktiverer frakoblet modus, og du distribuerer delte maskinvarestasjoner, øker du betydelig antall sluttpunkt som må håndteres.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
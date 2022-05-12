---
title: Velg mellom Store Commerce og Cloud POS
description: Dette emnet beskriver de viktigste forskjellene mellom Store Commerce og Cloud POS, og beskriver forskjellige faktorer som forhandlere som implementerer Dynamics 365 Commerce, bør vurdere for å hjelpe dem med å gjøre det beste valget for kravene.
author: jblucher
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b62e1737bc9e3b9d9e25a7a88e693a9aece80776
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629296"
---
# <a name="choose-between-store-commerce-and-cloud-pos"></a>Velg mellom Store Commerce og Cloud POS

[!include [banner](includes/banner.md)]

Dette emnet beskriver de viktigste forskjellene mellom Store Commerce og Cloud POS, og beskriver forskjellige faktorer som forhandlere som implementerer Dynamics 365 Commerce, bør vurdere for å hjelpe dem med å gjøre det beste valget for kravene. Det gir implementerere mer bakgrunn, tips og retningslinjer for faktorer som de bør vurdere når de distribuerer Dynamics 365 Commerce. Ved å se gjennom og følge denne veiledningen som en del av distribusjonsprosessen, kan implementerere unngå problemer som kan påvirke brukerens tilfredshet eller ytelse.

## <a name="insights"></a>Innsikt

Commerce inneholder en rekke distribusjons- og topologialternativer. Forhandlere kan derfor velge komponentene og konfigurasjonen som best dekker deres forretningsbehov og tekniske behov. En side ved implementering som krever nøye overveielse, er valget av plattform og formfaktor for komponenten salgssted (POS).

### <a name="pos-platform-and-form-factor-considerations"></a>Salgsstedsplattform- og formfaktorhensyn

Commerce støtter følgende salgsstedsalternativer:

- Store Commerce for Microsoft Windows
- Store Commerce for iOS og Android
- Cloud POS (CPOS), som støtter Microsoft Edge og Google Chrome-nettlesere
- Modern POS (MPOS) for Microsoft Windows (MPOS blir avskrevet oktober 2023.) 

I alle tilfellene deler POS (Store Commerce og CPOS) den samme kjerneprogramkoden. Dette er viktig av følgende årsaker:

- Brukergrensesnittet er konsekvent, uavhengig av plattform eller formfaktor.
- De fleste funksjonene er de samme, uavhengig av plattform eller formfaktor. Det er imidlertid noen viktige forskjeller. Disse ulikhetene går frem i dette emnet.
- I hver butikk kan salgsstedsvariasjoner kombineres og kjøres samtidig. For hovedkassene kan for eksempel en forhandler bruke Store Commerce på datamaskiner som kjører Windows. Forhandleren kan imidlertid supplere disse kassene med leserbaserte terminaler eller mobilenheter.
- Tilpassinger og utvidelser kan enkelt brukes på tvers av plattformer og formfaktorer. Fordi kjerneprogramkoden deles, kan de fleste tilpasningene implementeres én gang i stedet for flere ganger.

### <a name="store-commerce-vs-cpos"></a>Store Commerce kontra CPOS

Selv om Store Commerce og CPOS stort sett er det samme, er det noen viktige forskjeller som du må forstå.

#### <a name="store-commerce"></a>Store Commerce

Store Commerce er et skrivebordsprogram som er installert og vedlikeholdt på en enhet.

- **Windows** – Store Commerce for Windows-programmet inneholder all programkode, Commerce Runtime (CRT) og Hardware Station (HWS).
- **iOS/Android** – På disse plattformene fungerer programmet som vert for CPOS-programkoden. Med andre ord kommer programkoden fra CPOS-serveren som er driftet på Commerce Scale Unit. Hvis du vil ha mer informasjon, se [Oversikt over Commerce Scale Unit](dev-itpro/retail-store-system-begin.md).

#### <a name="cpos"></a>CPOS

Siden CPOS kjøres i en webleser, er ikke programmet installert på enheten. I stedet åpner nettleseren programkoden fra CPOS-serveren. Derfor kan ikke CPOS få tilgang til salgsstedsmaskinvare direkte eller fungere frakoblet.

### <a name="store-deployment-considerations"></a>Hensyn ved butikkdistribusjon

I tillegg til plattform og formfaktor må forhandlerne også velge et alternativ for distribusjon i butikken. Tabellen nedenfor inneholder konfigurasjonene som er tilgjengelige for hvert salgsstedsalternativ.

| POS-programmet            | Commerce Scale Unit | Tilgjengelig frakoblet | Lokal HWS-støtte |
|----------------------------|---------------------|-------------------|-------------------|
| Store Commerce for Windows | Cloud eller RSSU       | Ja               | Ja               |
| Store Commerce for Android | Cloud eller RSSU       | Nei                | Ja               |
| Store Commerce for iOS     | Cloud eller RSSU       | Nei                | Nei                |
| Cloud POS                  | Cloud eller RSSU       | Nei                | Nei                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

Commerce Scale Unit er en komponent som er vert for CRT. CRT inneholder all forretningslogikken som POS bruker, og det gir tilgang til kanaldatabasen. Når de er tilkoblet, bruker alle salgsstedsklientene i butikken Commerce Scale Unit Commerce Scale Unit kan distribueres i skyen eller butikken.

#### <a name="offline-mode"></a>Frakoblet modus

Store Commerce for Windows støtter frakoblet modus. I frakoblet modus kan salgsstedet fortsette å behandle salg selv om det er koblet fra Commerce Scale Unit. Det kan deretter synkroniseres med kanaldatabasen når tilkoblingen er gjenopprettet. Store Commerce bruker sin egen innebygde forekomst av CRT og bruker midlertidig sin egen lokale datakilde (frakoblet SQL Server-database). Hvis du vil ha mer informasjon om funksjonalitet for frakoblet bruk, kan du se [Frakoblet funksjonalitet for salgssted](pos-offline-functionality.md).

### <a name="pos-peripheralhardware-considerations"></a>Vurderinger for salgsstedstilbehør/-maskinvare

Forhandlere må også vurdere hvordan salgsstedet får tilgang til enheter og tilbehør som skrivere, kassaskuffer og betalingsterminaler. Maskinvarestasjoner kan dedikeres til en salgsstedskasse eller deles mellom kassene i en butikk.

| POS-programmet            | Lokal HWS OPOS | Nettverksenheter | Delt HWS-støtte |
|----------------------------|----------------|---------------------|--------------------|
| Store Commerce for Windows | Ja            | Ja                 | Ja                |
| Store Commerce for Android | Nei             | Ja                 | Ja                |
| Store Commerce for iOS     | Nei             | Nei                  | Ja                |
| Cloud POS                  | Nei             | Nei                  | Ja                |

Hvis du vil ha mer informasjon om maskinvarestasjoner, kan du se [Konfigurere og installere Retail-maskinvarestasjon](retail-hardware-station-configuration-installation.md).

## <a name="implementation-considerations"></a>Informasjon om implementering

Vurder følgende informasjon når du planlegger POS-implementeringen i butikkene:

- **Funksjonskrav** – De sentrale forretningsprosessene og funksjonene er de samme, uavhengig av plattform, formfaktor eller distribusjonstopologi. De fleste forhandlere trenger derfor ikke vurdere krav til funksjonalitet når de planlegger implementeringen.
- **Tilkobling** – Nettverkstilgjengelighet (regionnett \[WAN\] og lokalnett \[LAN\]) er en viktig faktor som krever nøye overveielse. Eventuelle fordeler som en nullavtrykks, skybasert vertsløsning bringer når det gjelder kostnader og enkelhet, går tapt hvis systemet ikke er tilgjengelig for forretningskritiske prosesser.

    Med mindre tilkoblingen for en gitt enhet er svært pålitelig og fleksibel, eller med mindre en viss nedetid er akseptabelt for forhandleren, anbefaler vi ett av følgende alternativer:

    - Bruk Store Commerce i Windows, og aktiver frakoblet modus.
    - Distribuer en lokal Commerce Scale Unit.

    Disse to alternativene ikke er gjensidig utelukkende. For den mest pålitelige topologien, kan forhandlere distribuere en lokal RSSU for å redusere avhengighet av Internett-tilkobling eller Azure-tilgjengelighet, og de kan også distribuere kasser på salgsstedet der frakoblet modus er aktivert hvis det er et problem med den lokale serveren eller nettverket.

- **Enheter / eksterne enheter for maskinvare** – En viktig del av et Retail POS-system er evnen til å bruke eksterne salgsstedsenheter som skrivere, pengeskuffer og betalingsterminaler. Selv om alle de tilgjengelige salgsstedsalternativene kan bruke eksterne enheter, er det bare Store Commerce for Windows som støtter dem direkte. For alle andre programmer kreves det én eller flere maskinvarestasjoner. Selv om denne fremgangsmåten gir fleksibilitet, må tilleggskomponenter distribueres, konfigureres og betjenes.
- **Systemkrav** – Systemkravene for POS-programmet varierer. Husk å sjekke den nyeste informasjonen før du foretar valget. Siden CPOS kjører i en webleser, støtter den for eksempel en rekke operativsystemer. Hvis du vil ha mer informasjon om systemkrav, kan du se [Systemkrav for skydistribusjoner](../fin-ops-core/fin-ops/get-started/system-requirements.md).
- **Distribusjon og betjening** – Kompleksiteten ved distribusjons- og betjeningskravene kan variere, avhengig av program- og distribusjonsvalgene. For eksempel for en skybasert CPOS-distribusjon trenger du ikke installere og oppdatere på hver enhet. Derfor reduserer denne tilnærmingen kompleksiteten og kostnadene. Hvis du imidlertid distribuerer Store Commerce på hver kasse og aktiverer frakoblet modus, og du distribuerer delte maskinvarestasjoner, øker du betydelig antall sluttpunkt som må håndteres.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

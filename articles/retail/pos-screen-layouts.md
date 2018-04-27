---
title: Konfigurere skjermoppsett for salgssted
description: Dette emnet inneholder informasjon om skjermoppsett for Microsoft Dynamics 365 for Retail POS-opplevelser.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ad425ab0848ab04003b7378cb5c488650f01c441
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="configure-screen-layouts-for-pos"></a>Konfigurere skjermoppsett for salgssted

[!INCLUDE [banner](includes/banner.md)]

Dette emnet inneholder informasjon om skjermoppsett for Microsoft Dynamics 365 for Retail POS-opplevelser.

Brukergrensesnittet for Microsoft Dynamics 365 for Retail POS kan konfigureres ved hjelp av en kombinasjon av visuelle profiler og skjermoppsett, tilordnet til butikker, kasser og/eller brukere.

## <a name="visual-profile"></a>Visuell profil
Visuelle profiler tilordnes til kasser og brukes til å angi de visuelle elementene som er kassespesifikke og delt på tvers av brukere. Alle brukere som logger på kassen vil ha samme tema, farger og bilder. 

**Profilnummer** – Profilnummeret er den unike ID-en for den visuelle profilen. 

**Beskrivelse** – Beskrivelsen lar deg angi et beskrivende navn som vil hjelpe deg med å finne den riktige profilen for din situasjon.

**Tema** – Brukere kan velge mellom lyse eller mørke programtemaer. Disse innstillingene påvirker skrift- og bakgrunnsfargene i hele programmet.

**Uthevingsfarge** – Uthevingsfargen brukes på hele salgsstedet for å skille eller utheve enkelte visuelle elementer, for eksempel fliser, kommandoknapper eller hyperkoblinger. Disse elementene er vanligvis gjennomførbare.

**Topptekstfarge** – Topptekstfargen lar brukeren konfigurere fargen på sideoverskriften for å oppfylle varemerkebehovene til forhandleren. Denne funksjonen er bare tilgjengelig i Dynamics 365 for Retail versjon 1611.

**Påloggingsbakgrunner** – Brukere kan angi et bakgrunnsbilde for påloggingsskjermbildet. Størrelsen på bakgrunnsbilder bør holdes så liten som mulig, siden lagring og innlasting av store filer kan ha innvirkning på programmets virkemåte og ytelse.

**Programbakgrunn** – Salgsstedet kan også bruke et bilde som bakgrunn i programmet i stedet for heldekkende temafarge. I likhet med påloggingsbakgrunner, anbefales det å holde filstørrelsen så liten som mulig.

## <a name="screen-layouts"></a>Skjermoppsett
Oppsett for skjermkonfigurasjonen bestemmer handlinger, innhold og plassering av brukergrensesnittkontroller i velkomstskjermen og transaksjonsskjermbildet for salgsstedet. 

**Velkomstskjerm** – Velkomstskjermbildet er siden som brukerne ser når de logger på salgsstedet for første gang. Velkomstskjermbildet kan bestå av et varemerke og knappegrupper som gir tilgang til salgsstedsoperasjoner. Operasjoner som ikke er spesifikke for den gjeldende transaksjonen er vanligvis plassert her. 

**Transaksjoneskjermbilde** – Transaksjonsskjermbildet er hovedskjermbildet for salgsstedet for behandling av salgstransaksjoner og ordrer. Transaksjonsskjermbildet kan konfigureres ved hjelp av utforming av skjermoppsett. 

**Standard startskjermbilde** – Noen forhandlere foretrekker at kassereren navigere direkte til transaksjonsskjermbildet etter pålogging. Innstillingen for standard startskjermbilde lar brukerne angi dette for alle skjermoppsett.

### <a name="assignment"></a>Tildeling

Skjermoppsett kan tilordnes på butikk-, kasse- eller brukernivå. Brukertildelingen overstyrer kasse- og butikktildelingen, og kassetildelingen overstyrer butikktildelingen. I et enkelt scenario der alle brukere bruker det samme oppsettet uavhengig av kasse eller rolle, kan skjermoppsett bare angis for butikken. I tilfeller der bestemte kasser eller brukere krever spesialisert oppsett, kan de tilordnes etter behov.

### <a name="layout-sizes"></a>Oppsettstørrelser

Denne funksjonen gjelder bare for Dynamics 365 for Retail versjon 1611. Fordi skjermoppsett i mange tilfeller kan brukes på tvers av flere skjermstørrelser og -oppløsninger, kan brukere konfigurere sine oppsett og innholdet for hver av dem. Salgsstedsprogrammet vil automatisk velge den nærmeste oppsettstørrelsen for enheten ved oppstart. Et skjermoppsett kan også inneholde konfigurasjoner for både fullstendig og kompakt enheter. Denne konfigurasjonen gjør det mulig å tilordne en bruker til ett enkelt skjermoppsettet som fungerer på tvers av ulike størrelser og formfaktorer i butikken. 

**Modern POS - Fullstendig** – Fullstendige oppsett brukes vanligvis helst for større skjermer, for eksempel PC-skjermer eller nettbrett. Brukere kan velge hvilke brukergrensesnittelementer som skal inkluderes, bestemme størrelse og plassering og konfigurere de detaljerte egenskapene. Fullstendig oppsett støtter både liggende og stående konfigurasjoner. 

**Moderne POS - Kompakt** – Kompakt oppsett brukes vanligvis helst for telefoner eller små nettbrett. Utformingsmulighetene er begrenset for kompakte enheter. Brukere kan konfigurere kolonner og felt for rutene for kvittering og totaler.

### <a name="screen-layout-designer"></a>Utforming av skjermoppsett

Hver oppsettstørrelse i et skjermoppsettet må konfigureres ved hjelp av utforming av skjermoppsett. Utformingen lar brukere angi og konfigurere av brukergrensesnittelementene i transaksjonskjermbildet. Utforming av skjermoppsett bruker ClickOnce til å laste ned, installere og starte den nyeste versjonen av appen hver gang brukeren åpner den. Husk å sjekke nettleserkravene for å bruke ClickOnce – noen lesere, for eksempel Chrome, krever servertillegg. 

**Numerisk tastatur** – Det numeriske tastaturet er den primære brukerinndatametoden i transaksjonsskjermbilde for salgssted. Det kan konfigureres til å vise hele skjermtastaturet, som er ideelt for berøringsskjerm, eller bare inndatafeltene, som kan brukes med et fysisk tastatur. Innstillingene for det numeriske tastaturet er bare tilgjengelige i det fullstendige oppsettet. I Dynamics 365 for Retail versjon 1611 har kompakte oppsett alltid det fullstendige numeriske tasturet tilgjengelig i transaksjonskjermbildet.

**Totalerpanel** – Totalerpanelet kan konfigureres i én eller to kolonner, slik at det vises felt, som linjeantall, rabattbeløp, tillegg, delsum og mva. I Dynamics 365 for Retail versjon 1611 støtter kompakte oppsett bare én enkelt totalerkolonne. 

**Mottak** – Mottakspanelet inneholder salgslinjer, betalingslinjer og leveringsinformasjon for produktene og tjenestene som behandles i POS-systemet. Brukere kan angi kolonner, bredde og plassering. I et kompakt oppsett i Dynamics 365 for Retail versjon 1611 kan du også konfigurere tilleggsinformasjon som skal vises i raden under hovedlinjen. 

**Kundekort** – Kundekort viser informasjon om kunden som er knyttet til transaksjonen. Kundekortet kan konfigureres til å vise eller skjule tilleggsinformasjon. 

**Fanekontroll** –Fanekontrollen kan plasseres på skjermvisningen, og andre kontroller som nummertastatur, kundekort eller knapperad kan plasseres i fanen. Fanekontroller er en beholder som hjelper brukere å få plass til mer innhold på skjermen. Kategorikontrollen er bare tilgjengelig for fullstendige oppsett. 

**Bilde** – Bildekontrollen kan brukes til å vise en firmalogo eller annet varemerket i transaksjonskjermbildet. Bildekontrollen er bare tilgjengelig for fullstendige oppsett. 

**Anbefalte produkter** – Hvis konfigurert for miljøet, vil kontrollen for anbefalte produkter viser produktforslag basert på maskinlæring. Kontrollen for anbefalte produkter er bare tilgjengelig for fullstendige oppsett i Dynamics 365 for Retail versjon 1611. **Egendefinert kontroll** – Den egendefinerte kontrollen fungerer som en plassholder i skjermoppsettet, slik at brukere kan reservere plass for egendefinert innhold. Den egendefinerte kontrollen er bare tilgjengelig for fullstendige oppsett.

<a name="see-also"></a>Se også
--------

[Installere utforming av oppsett for Retail POS](install-pos-layout-designer.md)





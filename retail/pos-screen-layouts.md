---
title: Konfigurere skjermoppsett for POS
description: Dette emnet inneholder informasjon om skjermoppsett for Microsoft Dynamics-365 for operasjoner - Retail poenget med salg (POS) opplevelser.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application user
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d49c5c9773047940e524c71e59a674ebe8460ad7
ms.lasthandoff: 03/31/2017


---

# <a name="configure-screen-layouts-for-pos"></a>Konfigurere skjermoppsett for POS

Dette emnet inneholder informasjon om skjermoppsett for Microsoft Dynamics-365 for operasjoner - Retail poenget med salg (POS) opplevelser.

Microsoft Dynamics-365 for operasjoner - Retail poenget med salg (POS) brukergrensesnitt kan konfigureres ved hjelp av en kombinasjon av visuelle profiler og skjermoppsett, tilordnet til butikker, kasser og/eller brukere.

## <a name="visual-profile"></a>Visuell profil
Visuelle profiler som er tilordnet registre og brukes til å angi de visuelle elementene som er register-spesifikke og delt på tvers av brukere. Alle brukere som logger på til kassen vil ha samme oppsett, farger og bilder. **Profil nummer** -profil-nummeret er den unike identifikatoren for den visuelle profilen. **Beskrivelse** -beskrivelsen, kan du angi et beskrivende navn som vil hjelpe deg for å finne den korrekte profilen for din situasjon. **Temaet** -brukere kan velge mellom lys eller mørk program temaene. Disse innstillingene påvirker skrift- og bakgrunnsfargene fargene i hele programmet. **Uthevingsfarge farge** -uthevingsfargen brukes i hele Salgsstedet å skille eller utheve enkelte visuelle elementer, for eksempel brikker, kommandoknapper eller hyperkoblinger. Disse elementene er vanligvis gjennomførbart. **Topptekstfarge** -hodet fargen lar brukeren konfigurere fargen på sideoverskriften til varemerking behovene til forhandleren. Denne funksjonen er bare tilgjengelig i Dynamics 365 for operasjoner versjon 1611. **Pålogging bakgrunner** -brukere kan angi et bakgrunnsbilde for påloggingsskjermbildet for. Størrelsen på bakgrunnsbilder bør holdes så små som mulig, mens lagring og lasting av store filer kan ha innvirkning på programmets virkemåte og ytelse. **Programbakgrunn** -The POS kan også bruke et bilde som bakgrunn i programmet i stedet for heldekkende temafarge. I likhet med påloggings-bakgrunner, anbefales det å holde filstørrelsen så minimal som mulig.

## <a name="screen-layouts"></a>Skjermoppsett
Oppsett for skjermkonfigurasjonen bestemmer handlinger, innhold og plassering av UI kontrollene i POS på velkomstskjermen og skjermen for transaksjonen. ** Velkomstskjermen **-velkomstskjermen er siden som brukerne ser når de logger inn POS i de fleste tilfeller. Velkomstskjermbildet kan bestå av en varemerket og knappegrupper som gir tilgang til POS-operasjoner. Operasjoner som ikke er spesifikke for den gjeldende transaksjonen er vanligvis plassert her. **Transaksjonen skjermen** -egenskapen Transaction-skjermen er hovedskjermen i POS for behandling av innkjøps- og ordrer. Skjermbildet Transaction kan konfigureres ved hjelp av skjermen layout designer. **Standard oppstartsskjermbildet** -noen forhandlere foretrekker at kassereren navigere direkte til skjermen for transaksjonen etter pålogging. Standardinnstillingen for start-skjermen lar brukerne angi dette for hver skjermoppsettet.

### <a name="assignment"></a>Tildeling

Skjermoppsett kan tilordnes på lageret, kasse eller bruker nivå. Bruker tildelingen overstyrer kassen og lagre tildeling, og registrer tildeling overstyringer butikk-tildeling. I en enkel scenariet der alle brukere bruke det samme oppsettet uavhengig av Registrer- eller kan skjermoppsett bare angis på butikken. I tilfeller der bestemte journaler eller brukere krever spesialisert oppsett, kan de tilordnes på riktig måte.

### <a name="layout-sizes"></a>Oppsettstørrelser

Denne funksjonen gjelder bare for Dynamics 365 for operasjoner versjon 1611. Fordi skjermoppsett kan brukes på tvers av flere skjermstørrelser og løsninger i mange tilfeller, kan brukere konfigurere sine oppsettet og innholdet for hver. POS-programmet vil automatisk velge den nærmeste størrelsen oppsett for enheten ved oppstart. Et skjermoppsett kan også inneholde konfigurasjoner for både fullstendig og kompakt enheter. Denne konfigurasjonen gjør det mulig for en bruker som skal tilordnes til en enkelt skjermoppsettet som fungerer på tvers av ulike størrelser og formfaktorer i lageret. **Moderne POS - Full** -Full oppsett brukes vanligvis best for større skjermer, for eksempel PC-skjermer eller tegnebrett. Brukere kan velge hvilke grensesnittelementer du inkluderer, bestemme deres størrelse og plassering og konfigurere de detaljerte egenskapene. Fullstendig oppsett støtter både liggende og stående konfigurasjoner. **Moderne POS - komprimert** -kompakt oppsett brukes vanligvis best for telefoner eller liten tavler. Designmuligheter er begrenset for kompakt enheter. Brukere kan konfigurere kolonner og felt for kvittering og rutene.

### <a name="screen-layout-designer"></a>Utforming av skjermoppsett

Hvert oppsett-størrelse i en skjermoppsettet må konfigureres ved hjelp av skjermen layout designer. Utformeren kan brukere angi og konfigurere av UI-elementene på skjermen for transaksjonen. Utforming av skjermoppsett bruker ClickOnce til å laste ned, installere og starte den nyeste versjonen av programmet hver gang brukeren åpner den. Husk å sjekke leserkrav for å bruke ClickOnce – noen lesere, for eksempel krom, krever servertilleggene. **Tallblokk** -talltastaturet er den primære brukerinndata i skjermbildet POS-transaksjonen. Den kan konfigureres til å vise hele skjermen pad, som er ideell for berøringsskjerm, eller bare i felt som kan brukes med et fysisk tastatur. Tall pad-innstillinger er tilgjengelige i hele oppsettet. I Dynamics 365 for operasjoner versjon 1611 har kompakt oppsett alltid full talltastaturet tilgjengelig fra skjermbildet for transaksjonen. **Totaler-panelet** - panelet SUMMER kan konfigureres i én eller to kolonner til å vise feltene som linje antall, rabattbeløp, tillegg, delsum og mva. I Dynamics 365 for operasjoner versjon 1611 støtter kompakt oppsett bare en enkelt totaler-kolonne. **Mottak** -** ** mottak-panelet inneholder salgslinjer, betalingslinjer og leveringsinformasjon for produktene og tjenestene som er behandlet på salgsstedet. Brukere kan angi kolonner, bredde og plassering. I et kompakt oppsett i Dynamics 365 for operasjoner versjon 1611, kan du også konfigurere tilleggsinformasjon som skal vises i raden under hoved-linje. **Kundekortet** - kunde kort viser informasjon som er knyttet til kunden som er knyttet til transaksjonen. Kundekortet kan konfigureres til å vise eller skjule tilleggsinformasjon. **Kategorikontroll** - kategorikontrollen kan plasseres på skjermoppsett og andre kontroller, for eksempel talltastaturet, kundekort, eller knappegrupper kan plasseres inne i kategorien. Kategorikontrollen er en beholder som hjelper brukerne med plass til mer innhold på skjermen. Kategorikontrollen er bare tilgjengelig for fullstendig oppsett. ** Bilde **-bildekontrollen kan brukes til å vise en firmalogo eller annen varemerket på skjermen for transaksjonen. Bildekontrollen er bare tilgjengelig for fullstendig oppsett. **Anbefalte produkter** - hvis konfigurert for miljøet, anbefalte produkter kontroll viser produkt forslag basert på maskinen læring. Anbefalte produkter-kontrollen er bare tilgjengelig for fullstendig oppsett i Dynamics 365 for operasjoner versjon 1611. ** Egendefinert kontroll **-den egendefinerte kontrollen fungerer som en plassholder i skjermoppsett til tillater brukere å reservere plass for egendefinert innhold. Den egendefinerte kontrollen er bare tilgjengelig for fullstendig oppsett.

<a name="see-also"></a>Se også
--------

[Install the Retail POS Layout designer](install-pos-layout-designer.md)



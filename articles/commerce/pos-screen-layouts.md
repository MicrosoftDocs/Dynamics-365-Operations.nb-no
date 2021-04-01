---
title: Visuelle konfigurasjoner av POS-brukergrensesnittet
description: Dette emnet inneholder informasjon om skjermoppsett for Dynamics 365 Commerce POS-opplevelser.
author: boycezhu
manager: annbe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 521fbd2c73adca1db38ba7258abf183f7350b109
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231302"
---
# <a name="pos-user-interface-visual-configurations"></a>Visuelle konfigurasjoner av brukergrensesnittet for salgssted

[!include [banner](includes/banner.md)]


Brukergrensesnittet for Microsoft Dynamics 365 Commerce salgssted (POS) kan konfigureres ved hjelp av en kombinasjon av visuelle profiler og skjermoppsett, tilordnet til butikker, kasser og/eller brukere. Dette emnet inneholder informasjon om disse konfigurasjonsalternativene.

Illustrasjonen nedenfor viser forholdet mellom de forskjellige enhetene som utgjør de konfigurerbare delene av brukergrensesnittet for salgsstedet.

![Enheter for skjermoppsett for salgssted](../commerce/media/POS-layout-configuration-entities-diagram.png)

## <a name="visual-profile"></a>Visuell profil

Visuelle profiler tilordnes til kasser, og de brukes til å angi de visuelle elementene som er kassespesifikke og delt på tvers av brukere. Alle brukere som logger på kassen ser samme tema, oppsett, farger og bilder.

![Velkomstskjerm for salgsstedet med lyst tema](../commerce/media/POS-Welcome-Screen-with-Light-theme.png)

![Transaksjonsskjermbilde for salgssted med mørkt temaet](../commerce/media/POS-Transaction-Screen-with-Dark-theme.png)

- **Profilnummer** – Profilnummeret er den unike ID-en for den visuelle profilen.
- **Beskrivelse** – Du kan angi et beskrivende navn som vil hjelpe deg med å finne den riktige profilen for din situasjon.
- **Tema** – Du kan velge mellom **lyse** eller **mørke** programtemaer. Temaet påvirker skrift- og bakgrunnsfargene i hele programmet.
- **Uthevingsfarge** – Uthevingsfargen brukes på hele salgsstedet for å skille eller utheve spesifikke visuelle elementer, for eksempel fliser, kommandoknapper og hyperkoblinger. Disse elementene er vanligvis handlingskrevende.
- **Topptekstfarge** – Du kan konfigurere fargen på sideoverskriften for å oppfylle varemerkebehovet til forhandleren.
- **Skriftutvalg** – Du kan velge mellom **Standard** og **Stor** skrift. Skriftutvalget har innvirkning på skriftstørrelsen i hele programmet. Standardvalget er **Standard**.
- **Vis alltid strekkodeetiketter i programmet** – Når dette alternativet er aktivert, er etiketteksten alltid synlig under strekkodeknappene i programmet.
- **Oppsett** – Du kan velge mellom det **Midtstilt** og **Høyre**. Oppsettet har innvirkning på justeringen av påloggingsboksen på påloggingsskjermen. Standardvalget er **Midtstilt**.
- **Vis dato/klokkeslett** – Når dette alternativet er aktivert, vises gjeldende dato og klokkeslett i POS-hodet og på påloggingsskjermen.
- **Tastatur** – Du kan velge mellom **Standardtastatur for OS** og **Vis talltastatur** for å angi standardtastaturet som skal brukes for inndata på påloggingsskjermen. Talltastaturet er et virtuelt tastatur som hovedsakelig brukes til berøringsbaserte enheter. Standardvalget er **Standardtastatur for OS**.
- **Logobilde** – Du kan angi et logobilde som vises på påloggingsskjermen. Vi anbefaler at du bruker et bilde som har en gjennomsiktig bakgrunn. Filstørrelsen bør holdes så liten som mulig, siden programmets virkemåte og ytelse kan påvirkes når store filer lagres og lastes inn.
- **Påloggingsbakgrunn** – Du kan angi et bakgrunnsbilde for påloggingsskjermbildet. Filstørrelsen på bakgrunnsbilder bør holdes så liten som mulig.
- **Bakgrunn** – Du kan angi et bakgrunnsbilde som brukes i stedet for heldekkende temafarge i programmet. I likhet med bakgrunnsbilder for påloggingsskjermmen bør filstørrelsen holdes så liten som mulig.

> [!NOTE]
> **Høyre** oppsett og visning av dato/klokkeslett gjelder ikke for påloggingsskjermen i kompakt visning.

Du må kjøre distribusjonsplanjobben **1090** (**Registre**) for å synkronisere de siste visuelle profilkonfigurasjonene til kanaldatabasen.

## <a name="screen-layouts"></a>Skjermoppsett

Oppsett for skjermkonfigurasjoner bestemmer handlinger, innhold og plassering av brukergrensesnittkontroller i **velkomstskjermen** og **Transaksjon**-skjermbildet for salgsstedet.

![Visning for skjermoppsett for salgssted](../commerce/media/POS-Screen-Layout-View.png)

- **Velkomstskjerm** – Velkomstskjermbildet er siden som brukerne ser når de logger på salgsstedet for første gang. Velkomstskjermbildet kan bestå av et varemerke og knappegrupper som gir tilgang til salgsstedsoperasjoner. Operasjoner som ikke er spesifikke for den gjeldende transaksjonen er vanligvis plassert på dette skjermbildet.

    ![Velkomstskjerm for salgssted](../commerce/media/POS-Welcome-Screen.png)

- **Transaksjoneskjermbilde** – **Transaksjon**-skjermbildet er hovedskjermbildet for salgsstedet for behandling av salgstransaksjoner og ordrer. Innhold og oppsett konfigureres ved å bruke utforming av skjermoppsett.

    ![Transaksjonsskjermbilde for salgssted](../commerce/media/POS-Transaction-Screen.png)

- **Standard startskjermbilde** – Noen forhandlere foretrekker at kasserere går direkte til **Transaksjon**-skjermbildet etter pålogging. Innstillingen **Standard startskjermbilde** lar deg angi standard skjermbilde som vises etter pålogging for hvert skjermoppsett.

### <a name="assignment"></a>Tildeling

Skjermoppsett kan tilordnes på butikk-, kasse- eller brukernivå. Brukertildelingen overstyrer kasse- og butikktildelinger, og kassetildelingen overstyrer butikktildelingen. I et enkelt scenario der alle brukere bruker det samme oppsettet uavhengig av kasse eller rolle, kan skjermoppsett bare angis for butikknivået. I scenarier der bestemte kasser eller brukere krever spesialisert oppsett, kan oppsettene tilordnes.

Avhengig av hvilket nivå skjermoppsettene er tilordnet, må du kjøre distribusjonsplanjobbene **1070** (**Kanalkonfigurasjon**), **1090** (**Registre**) og/eller **1060** (**Stab**) for å synkronisere de siste konfigurasjonene av skjermoppsett til kanaldatabasen.

### <a name="layout-sizes"></a>Oppsettstørrelser

De fleste delene av brukergrensesnittet for salgsstedet er responsive, og oppsettet skaleres og justeres automatisk basert på skjermstørrelse og retning. Salgsstedskjermbildet **Transaksjon** må imidlertid konfigureres for hver skjermoppløsning som forventes.

Ved oppstart velger salgsstedsprogrammet automatisk den nærmeste oppsettstørrelsen som er konfigurert for enheten. Et skjermoppsettet kan også inneholde konfigurasjoner for både liggende og stående modus, og for enheter i full størrelse og kompakte enheter. Derfor kan brukere tilordnes til ett enkelt skjermoppsettet som fungerer på tvers av ulike størrelser og formfaktorer som brukes i butikken.

![Oppsettstørrelser for salgssted](../commerce/media/POS-Screen-Layout-Sizes.png)

- **Navn** – Du kan angi et beskrivende navn som identifiserer skjermstørrelsen.
- **Oppsettype** – Programmet for salgsstedet kan vise brukergrensesnittet i ulike modi for å levere den beste brukeropplevelsen på en bestemt enhet.

    - **Modern POS – Fullstendig** – Fullstendige oppsett brukes vanligvis helst for større skjermer, for eksempel PC-skjermer og nettbrett. Du kan velge elementene som brukergrensesnittet skal inneholde, angi størrelsen og plasseringen til elementene og konfigurere de detaljerte egenskapene. Fullstendig oppsett støtter både liggende og stående konfigurasjoner.
    - **Moderne POS – Kompakt** – Kompakt oppsett brukes vanligvis helst for telefoner og små nettbrett. Utformingsmulighetene er begrenset for kompakte enheter. Du kan konfigurere kolonner og felt for rutene for kvittering og totaler.

- **Bredde/høyden** – Disse verdiene representerer gjeldende skjermstørrelse, i piksler, som er forventet for oppsettet. Husk at noen operativsystemer bruker skalering for skjermer med høy oppløsning.

> [!TIP]
> Du kan finne ut oppsettstørrelsen som kreves for en skjerm på salgsstedet ved å vise oppløsningen i programmet. Start salgsstedet, og gå til **Innstillinger \> Øktinformasjon**. Salgsstedet viser skjermoppsettet som er lastet inn, oppsettstørrelsen og oppløsningen på programvinduet.

![Informasjonssiden for salgsstedsøkt viser skjermoppsettet som er lastet inn, oppsettstørrelsen og oppløsningen på programvinduet](../commerce/media/POS-Session-Information.png)

### <a name="button-grids"></a>Knappegrupper

For hvert oppsettstørrelse i et skjermoppsett kan du konfigurere og tilordne knappegrupper for velkomstskjermbildet for salgsstedet og **Transaksjon**-skjermbildet. Knappegrupper for velkomstskjermen plasseres automatisk fra venstre mot høyre, fra det laveste nummeret (velkomstskjerm 1) til det høyeste nummeret.

Plasseringen av knappegrupper er angitt i utforming av skjermoppsett i oppsett for fullstendig sakgssted.

Knappegrupper i oppsett for kompakt salgssted plasseres automatisk fra topp mot bunn, fra det laveste nummeret (transaksjonsskjerm 1) til det høyeste nummeret. Det er tilgang til dem fra **Handlinger**-menyen.

![Knappegrupper for kompakt oppsett](../commerce/media/Compact-View-Button-Grids.png)

> [!NOTE]
> Knappestørrelsene i utformingen tilpasses størrelsen på vinduet, og derfor kan det hende at de ikke gjenspeiler de faktiske knappene som gjengis på salgsstedet. Hvis du vil simulere knappegruppeoppsettet, kan du justere utformingsvinduene til samme størrelse som salgsstedet.

### <a name="images"></a>Bilder

Du kan angi bilder som skal inkluderes i brukergrensesnittet for salgsstedet for hvert oppsettstørrelse i et skjermoppsett. Ett enkelt bilde kan angis for velkomstskjermen for oppsett for fullstendig sakgssted. Dette bildet vises som det første grensesnittelement til venstre. I **Transaksjon**-skjermbildet kan bilder brukes som kategoribilder eller logoer. Oppsett for kompakt salgssted bruker ikke disse bildene.

### <a name="screen-layout-designer"></a>Utforming av skjermoppsett

Utforming av skjermoppsett lar deg konfigurere forskjellige eler av **Transaksjon**-skjermbildet for salgsstedet for hvert oppsettstørrelse, i både liggende og stående modus, og for både fullstendige og kompakte oppsett. Utforming av skjermoppsett bruker ClickOnce-distribusjonsteknologi til å laste ned, installere og starte den nyeste versjonen av appen hver gang brukeren åpner den. Husk å sjekke nettleserkravene for ClickOnce. Noen nettlesere, for eksempel Google Chrome, krever tillegg.

> [!IMPORTANT]
> Du må konfigurere et skjermoppsett for hver oppsettstørrelse som er definert og som brukes ved salgsstedet.

### <a name="full-layout-designer"></a>Utforming av fullstendig oppsett

Utformingen for fullstendig oppsett lar brukere dra grensesnittkontroller til **Transaksjon**-skjermbildet for salgsstedet og konfigurere innstillingene for disse kontrollene.

![Utforming for fullstendig oppsett for salgssted (liggende)](../commerce/media/POS-Full-Layout-Designer-Landscape.png)

- **Importere oppsett / eksporter oppsett** – Du kan eksportere og importere utforminger for oppsett for skjermbilde for salgssted som XML-filer, slik at du enkelt kan bruke på nytt og dele dem på tvers av miljøer. Det er viktig at du importerer oppsettutforminger for riktige oppsettstørrelser. Hvis ikke kan det hende grensesnittelementer ikke passer på skjermen.
- **Liggende/stående** – Hvis salgsstedsenheten lar brukere bytte mellom liggende og stående modus, må du definere et skjermoppsett for hver modus. Salgsstedet oppdager skjermrotering automatisk og viser riktig utformingen.
- **Rutenettoppsett** – Utforming av oppsett for salgssted rutenett med fire piksler. Grensesnittkontroller "festes" til rutenettet for å hjelpe deg med å justere innholdet på riktig måte.
- **Utformingszoom** – Du kan zoome utformingsvisningen inn og ut for å vise innholdet på skjermen for salgsstedet. Denne funksjonen er nyttig når skjermoppløsningen på salgsstedet er svært forskjellig fra oppløsningen på skjermen som skal brukes i utformingen.
- **Vis/skjul navigasjonsfelt** – For oppsett for fullstendig salgssted kan du velge om navigasjonsfeltet til venstre vises på **Transaksjon**-skjermen. Denne funksjonen er nyttig for skjermer med lavere oppløsning. Hvis du vil angi synligheten, høyreklikker du på navigasjonsfeltet i utforming og merker av for **Alltid synlig**. Hvis navigasjonsfeltet er skjult, har salgsstedsbrukere fremdeles tilgang til det ved hjelp av menyen øverst til venstre.

    ![Vis/skjul navigasjonsfelt](../commerce/media/Navigation-Bar.PNG)

- **Salgsstedskontrollerer** – Utforming for salgssted støtter følgende kontroller. Du kan konfigurere mange kontroller ved å høyreklikke og ved hjelp av hurtigmenyen.

    ![Brukergrensesnittkontroller for salgssted](../commerce/media/POS-UI-Controls.png)

    - **Numerisk tastatur** – Det numeriske tastaturet er den primære mekanisme for brukerinndata i **Transaksjon**-skjermbilde for salgssted. Du kan konfigurere kontrollen slik at hele talltastaturet vises. Dette alternativet er perfekt for enheter med berøringsskjerm. Du kan også konfigurere den slik at bare inndatafeltet vises. I så fall brukes et fysisk tastatur for inndata. Innstillingene for det numeriske tastaturet er bare tilgjengelige i det fullstendige oppsettet. For kompakte oppsett vises alltid det fullstendige talltastaturet på **Transaksjon**-skjermen.
    - **Totalerpanel** – Du kan konfigurere totalerpanelet i én eller to kolonner, slik at verdiene vises, for eksempel linjeantall, rabattbeløp, tillegg, delsum og mva. Kompakte oppsett støtter bare én kolonne.
    - **Mottakspanel** – Mottakspanelet inneholder salgslinjer, betalingslinjer og leveringsinformasjon for produktene og tjenestene som behandles i POS-systemet. Du kan angi kolonner, bredde og plassering. I kompakt modus kan du også konfigurere tilleggsinformasjon som vises i raden under hovedlinjen.
    - **Kundekort** – Kundekort viser informasjon om kunden som er knyttet til gjeldende transaksjon. Du kan konfigurere kundekortet til å vise eller skjule tilleggsinformasjon.
    - **Kategorikontroll** – Du kan legge til kategorikontrollen i skjermoppsettet og deretter legge til andre kontroller, for eksempel det numeriske tastaturet, kundekort, eller knappegrupper. Kategorikontrollen er en beholder som lar deg få plass til mer innhold på skjermen. Kategorikontrollen er bare tilgjengelig for fullstendige oppsett.
    - **Bilde** – Du kan bruke bildekontrollen til å vise en firmalogo eller annet varemerket i **Transaksjon**-skjermbildet. Bildekontrollen er bare tilgjengelig for fullstendige oppsett.
    - **Anbefalte produkter** – Hvis kontrollen for anbefalte produkter er konfigurert for miljøet, viser den produktforslag basert på maskinlæring.
    - **Egendefinert kontroll** – Den egendefinerte kontrollen fungerer som en plassholder i skjermoppsettet og lar deg kan reservere plass for egendefinert innhold. Den egendefinerte kontrollen er bare tilgjengelig for fullstendige oppsett.

### <a name="compact-layout-designer"></a>Utforming for kompakt oppsett

På samme måte som utforming for fullstendig oppsett kan du med utforming for kompakt oppsett konfigurere skjermoppsettet for salgsstedet for telefoner og små nettbrett. I dette tilfellet er imidlertid selve oppsettet fast. Du kan konfigurere kontrollene i oppsettet ved å høyreklikke og ved hjelp av hurtigmenyen. Du kan imidlertid ikke bruke dra og slipp-operasjoner for mer innhold.

![Utforming for kompakt oppsett](../commerce/media/Compact-Layout-Designer.png)

### <a name="button-grid-designer"></a>Utforming for knappegruppe

Utforming for knappegruppe lar deg konfigurere knappegrupper som kan brukes på velkomstskjermbildet for salgsstedet og **Transaksjon**-skjermen for både fullstendige og kompakte oppsett. Du kan bruke samme knappegruppen på tvers av oppsett og oppsettyper. På samme måte som utforming for skjermoppsett bruker utforming for knappegruppe ClickOnce-distribusjonsteknologi til å laste ned, installere og starte den nyeste versjonen av appen hver gang brukeren åpner den. Husk å sjekke nettleserkravene for ClickOnce. Noen nettlesere, for eksempel Google Chrome, krever tillegg.

![Utforming for knappegruppe](../commerce/media/Button-Grid-Designer.png)

- **Ny knapp** – Klikk for å legge til en ny knapp i knappegruppen. Som standard vises nye knapper i hjørnet øverst til venstre i gruppen. Du kan imidlertid endre knappene ved å dra dem i oppsettet.

    > [!IMPORTANT]
    > Innholdet i knappegruppen kan overlappe hverandre. Når du ordner knapper, må du kontrollere at de ikke skjuler andre knapper.

- **Ny utforming** – Klikk for automatisk oppsett av en knappegruppe ved å angi antall knapper per rad og kolonne.
- **Knappeegenskaper** – Du kan konfigurere knappeegenskaper ved å høyreklikke på knappen og bruke hurtigmenyen.

    > [!IMPORTANT]
    > Noen innstillinger for knappegruppe gjelder bare for Enterprise POS, ikke for Modern POS eller Cloud POS.

    ![Knappegenskaper for knappegruppe](../commerce/media/Button-grid-button-properties.png)

    - **Handling** – I listen over aktuelle POS-operasjoner velger du operasjonen som startes når knappen klikkes på salgsstedet.

        Hvis du vil vise listen over POS-operasjoner som støttes, kan du se [Tilkoblede og frakoblede salgsstedsoperasjoner (POS)](pos-operations.md).

    - **Handlingsparametere** – Noen POS-operasjoner bruker flere parametere når de startes. For operasjonen Legg til produkt kan for eksempel brukere angi produktet som skal legges til.
    - **Knappetekst** – Angi teksten som vises på knappen på salgsstedet.
    - **Skjule knappetekst** – Bruk denne avmerkingsboksen for å skjule eller vise knappeteksten. Knappeteksten er ofte skjult for små knapper som bare viser et ikon.
    - **Verktøytips** – Angi ekstra hjelpeteksten som vises når brukere holder pekeren over knappen.
    - **Størrelse i kolonner / Størrelse i rader** – Du kan angi hvor høy og bred knapppen er.

        ![Knappestørrelser for salgssted i rader og kolonner](../commerce/media/POS-Button-Sizes-In-Rows-And-Columns.png)

    - **Egendefinert skrift** – Når du merker av for **Aktiver egendefinert skrift for POS**, kan du angi en annen skrift enn standard systemskrift for salgsstedet.
    - **Egendefinert tema** – Salgsstedsknapper bruker som standard uthevingsfargen fra den visuelle profilen. Når du merker av for **Bruk egendefinert tema**, kan du angi flere farger.

        > [!NOTE]
        > Modern POS og Cloud POS bruker bare verdiene **Bakgrunnsfarge** og **Skriftfarge**.

    - **Knappebilde** – Knapper kan inneholde bilder eller ikoner. Velg blant de tilgjengelige bildene som er angitt under **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgssted \> Bilder**.

![Eksempel på knappegruppe på salgssted](../commerce/media/Example-Button-Grid-In-POS.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Installere utforming av oppsett for salgssted (POS) for detaljhandel](install-pos-layout-designer.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
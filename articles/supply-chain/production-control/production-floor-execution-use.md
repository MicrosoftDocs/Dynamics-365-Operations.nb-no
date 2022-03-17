---
title: Hvordan arbeidere bruker grensesnittet for produksjonsutførelse
description: Dette emnet beskriver hvordan du bruker grensesnittet for produksjonsutførelse fra synspunktet til en arbeider.
author: johanhoffmann
ms.date: 01/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: a677eb71f97a953c625a1f667b055e5b7696fbe6
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384431"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Hvordan arbeidere bruker grensesnittet for produksjonsutførelse

[!include [banner](../includes/banner.md)]

Grensesnittet for produksjonsutførelse er optimalisert for berøringsinteraksjon. Utformingen gir visuell kontrast som oppfyller tilgjengelighetskravene for Shop Floor-miljøer. Den har alle de samme funksjonene som jobbkortenheten. Det gjør imidlertid også at flere jobber kan startes parallelt fra en jobbliste. (Denne funksjonen er også kjent som *bunting av jobber*). I tillegg kan arbeidere fra en jobbliste åpne en veiledning som ble opprettet i Microsoft Dynamics 365-veiledningen. På denne måten kan de finne en visuell veiledning i en HoloLens.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Logge på grensesnittet for produksjonsutførelse som en arbeider

Før arbeidere kan begynne å bruke enheten, må en leder eller teknisk stab forberede den og åpne den riktige siden i Dynamics 365 Supply Chain Management. Hvis du vil ha mer informasjon om hvordan du definerer enheten, kan du se [Definere en enhet for å kjøre grensesnittet for produksjonsutførelse](production-floor-execution-setup.md).

Når enheten er forberedt, vises påloggingssiden på den. Denne siden viser informasjon om statusen for jobber for den lokale arbeidscellen. Denne informasjonen oppdateres med jevne mellomrom. På siden bruker arbeidere kort-IDer til å logge på. Selv om arbeidere ikke trenger å ha en brukerkonto for Supply Chain Management, må de ha en *tidregistrert arbeider*-konto de kan bruke når de logger på.

![Påloggingsside for grensesnittet for produksjonsutførelse.](media/pfei-sign-in-page.png "Påloggingsside for grensesnittet for produksjonsutførelse")

De gjenværende delene i dette emnet beskriver hvordan arbeiderne samhandler med grensesnittet.

## <a name="all-jobs-tab"></a>fanen Alle jobber

fanen **Alle jobber** inneholder en jobbliste som viser alle produksjonsjobbene som har statusen *Ikke startet*, *Stoppet* eller *Startet*. (Dette fanenavnet kan tilpasses og kan være et annet for systemet ditt.)

![fanen Alle jobber.](media/pfei-all-jobs-tab.png "fanen Alle jobber")

Jobblisten inneholder følgende kolonner: Tallene samsvarer med tallene i den forrige illustrasjonen.

1. **Velgerkolonne** – kolonnen lengst til venstre bruker hakemerker for å angi jobber som er valgt av arbeideren. Arbeidere kan velge flere jobber i listen samtidig. Hvis du vil velge alle jobbene i listen, merker du av i kolonneoverskriften. Når en enkelt jobb er valgt, vises detaljer om denne jobben i den nedre delen av siden.
1. **Jobbstatuskolonne** – denne kolonnen bruker symboler for å angi statusen for hver jobb. Jobber som ikke har symbol i denne kolonnen, har statusen *ikke startet*. En grønn trekant angir jobber med statusen *startet*. To gule loddrette linjer angir jobber som har statusen *stoppet*.
1. **Kolonne med høy prioritet** – denne kolonnen bruker utropstegn for å angi jobber med høy prioritet.
1. **Ordre** – denne kolonnen viser produksjonsordrenummeret for en jobb.
1. **Beskrivelse** – denne kolonnen viser en beskrivelse av operasjonen som en jobb er en del av.
1. **Ønsket** – denne kolonnen viser antallet som det er planlagt at en jobb skal produsere.
1. **Startet** – denne kolonnen viser antallet som allerede er startet for en jobb.
1. **Fullført** – denne kolonnen viser antallet som allerede er fullført for en jobb.
1. **Kassert** – denne kolonnen viser antallet som allerede er kassert for en jobb.
1. **Gjenstående** – denne kolonnen viser antallet som det gjenstår å fullføre for en jobb.

## <a name="active-jobs-tab"></a>Aktive jobber-fanen

**Aktive jobber**-fanene viser en liste over alle jobber som den påloggede arbeideren allerede har startet. (Dette fanenavnet kan tilpasses og kan være et annet for systemet ditt.)

![Aktive jobber-fanen.](media/pfei-active-jobs-tab.png "Aktive jobber-fanen")

Listen over aktive jobber inneholder følgende kolonner:

- **Velgerkolonne** – kolonnen lengst til venstre bruker hakemerker for å angi jobber som er valgt av arbeideren. Arbeidere kan velge flere jobber i listen samtidig. Hvis du vil velge alle jobbene i listen, merker du av i kolonneoverskriften. Når en enkelt jobb er valgt, vises detaljer om denne jobben i den nedre delen av siden.
- **Ordre** – denne kolonnen viser produksjonsordrenummeret for en jobb.
- **Beskrivelse** – denne kolonnen viser en beskrivelse av operasjonen som en jobb er en del av.
- **Ønsket** – denne kolonnen viser antallet som det er planlagt at en jobb skal produsere.
- **Startet** – denne kolonnen viser antallet som allerede er startet for en jobb.
- **Fullført** – denne kolonnen viser antallet som allerede er fullført for en jobb.
- **Kassert** – denne kolonnen viser antallet som allerede er kassert for en jobb.
- **Gjenstående** – denne kolonnen viser antallet som det gjenstår å fullføre for en jobb.

## <a name="my-jobs-tab"></a>Fanen Mine jobber

Med fanen **Mine jobber** kan arbeidere enkelt vise alle jobber som er tilordnet spesifikt til dem og ikke er påbegynt eller ferdige. Dette er nyttig i firmaer der jobber noen ganger eller alltid er tilordnet til bestemte arbeidere (personale) i stedet for andre typer ressurser (for eksempel maskiner). 

Planleggingssystemet tilordner automatisk hver produksjonsjobb til en bestemt ressurspost, og hver ressurspost har en type (for eksempel maskin eller menneske). Når du konfigurerer en ansatt som produksjonsarbeider, kan du knytte arbeiderkontoen til en unik personalpost. 

Fanen **Mine jobber** viser alle jobber som ikke er påbegynt eller ferdige, og som er tilordnet til personalposten til den påloggede arbeideren, hvis en arbeider har logget seg på. Den viser aldri jobber som er tilordnet til en maskin eller annen ressurstype, selv om den påloggede arbeideren har begynt å arbeide på disse jobbene.

Hvis du vil vise alle jobbene den påloggede arbeideren har begynt på, uavhengig av ressurstypen som hver jobb er tilordnet til, bruker du fanen **Aktive jobber**. Hvis du vil vise alle uferdige jobber som samsvarer med konfigurasjonen for det lokale jobbfilteret, bruker du fanen **Alle jobber** uavhengig av arbeideren eller startstatusen.

![Fanen Mine jobber.](media/pfei-my-jobs-tab.png "Fanen Mine jobber")

## <a name="my-machine-tab"></a>Min maskin-fanen

I **Min maskin**-fanen kan arbeidere velge et aktivum som er koblet til en maskinressurs i filteret som er angitt i **Alle jobber**-fanen. Arbeidere kan deretter vise statusen og tilstanden for det valgte aktivumet ved å lese verdier for opptil fire valgte tellere og lister over nylige meldinger og registrerte nedetider. Arbeidere kan også be om vedlikehold for det valgte aktivumet og registrere og redigere nedetid for maskinen. (Dette fanenavnet kan tilpasses og kan være et annet for systemet ditt.)
 
![Min maskin-fanen.](media/pfei-my-machine-tab.png "Min maskin-fanen")

**Min maskin**-fanen har følgende kolonner. Tallene samsvarer med tallene i den forrige illustrasjonen.

1. **Maskinaktivum** – Velg maskinaktivumet du vil spore. Begynn med å skrive inn et navn du vil velge fra en liste over samsvarende aktiva, eller velg forstørrelsesglassikonet for å velge fra en liste over alle aktiva som er knyttet til ressursene som er i filteret for jobblisten.

    > [!NOTE]
    > Brukere av Supply Chain Management kan tilordne en ressurs til hvert aktivum etter behov på **Alle aktiva**-siden (ved å bruke rullegardinlisten **Ressurs** i **Anleggsmiddel**-fanen). Hvis du vil ha mer informasjon, kan du se [Opprette et aktivum](../asset-management/objects/create-an-object.md).

1. **Innstillinger** – Velg tannhjulikonet for å åpne en dialogboks der du kan velge hvilke tellere du vil vise for det valgte maskinaktivumet. Verdiene for disse tellerne vises øverst i **Aktivastyring**-fanen. På **Innstillinger**-menyen (som vises på skjermbildet nedenfor) kan du aktivere opptil fire tellere. For hver teller du vil aktivere, bruker du oppslagsfeltet øverst i flisen til å velge en teller. Oppslagsfeltet viser alle tellerne som er knyttet til aktivumet som er valgt øverst på **Aktivastyring**-siden. Angi at hver teller skal overvåke **Aggregert**-verdien eller den siste **Faktisk**-verdien for telleren. Hvis du for eksempel angir en teller som sporer hvor mange timer maskinen har kjørt, setter du den til **Aggregert**. Hvis du angir at en teller skal måle sist oppdaterte temperatur eller trykk, setter du den til **Faktisk**. Velg **OK** for å lagre innstillingene og lukke dialogboksen.

    ![Innstillingene på Min maskin-fanen.](media/pfei-my-machine-tab-settings.png "Innstillingene på Min maskin-fanen")

1. **Be om vedlikehold** – Velg denne knappen for å åpne en dialogboks der du kan opprette en melding. Du kan gi en beskrivelse og en merknad. En bruker av Supply Chain Management blir gjort oppmerksom på forespørselen og kan deretter konvertere meldingen til en arbeidsordre for vedlikehold.
1. **Registrer nedetid** – Velg denne knappen for å åpne en dialogboks der du kan registrere nedetid for maskin. Du kan velge en årsakskode og angi en dato / et tidsrom for nedetiden. Registreringen av nedetid for maskin brukes til å beregne effektiviteten til maskinaktivumet.
1. **Vis eller rediger** – Velg denne knappen for å åpne en dialogboks der du kan redigere eller vise eksisterende poster for nedetid.

## <a name="starting-and-completing-production-jobs"></a>Starte og fullføre produksjonsjobber

Arbeidere starter en produksjonsjobb ved å velge en jobb i **Alle jobber**-fanen og deretter velge **Start jobb** for å åpne **Start jobb**-dialogboksen.

![Dialogboksen Start jobb.](media/pfei-start-job-dialog.png "Dialogboksen Start jobb")

Arbeidere bruker **Start jobb**-dialogboksen til å bekrefte produksjonsantallet, og starter deretter jobben. Arbeidere kan justere antallet ved å merke av i **Antall**-feltet og deretter bruke det numeriske tastaturet som vises. Arbeidere velger deretter **Start** for å begynne å arbeide på jobben. Dialogboksen **Start jobb** lukkes, og jobben legges til i fanen **Aktive jobber**.

Arbeidere kan starte en jobb som har en hvilken som helst status. Når en arbeider starter en jobb som har statusen *ikke startet*, vises **Antall**-feltet i dialogboksen **Start jobb** først hele antallet. Når en arbeider starter en jobb som har statusen *Startet* eller *Stoppet* viser **Antall**-feltet først restantallet.

## <a name="reporting-good-quantities"></a>Rapportere korrekte antall

Når en arbeider fullfører eller delvis fullfører en jobb, kan de rapportere korrekte antall som ble produsert ved å velge en jobb i fanen **Aktive jobber** og deretter velge **Rapportfremdrift**. I dialogboksen **Rapportfremdrift** angir arbeideren deretter det korrekte antallet ved hjelp av det numeriske tastaturet. Antallet er tomt som standard. Når et antall er angitt, kan arbeideren oppdatere statusen for jobben til *pågår*, *stoppet* eller *fullført*.

![Dialogboksen Rapportfremdrift.](media/pfei-report-progress-dialog.png "Dialogboksen Rapportfremdrift")

## <a name="reporting-good-quantities-on-batch-orders-that-have-co-products-and-by-products"></a>Rapportering korrekte antall varer på partiordrer som har koprodukter og biprodukter

Ansatte kan å bruke grensesnittet for produksjonsgulvutførelse til å rapportere fremdrift for partiordrer. Denne rapporten inkluderer rapportering på koprodukter og biprodukter.

Noen produsenter, spesielt i prosessindustri, bruker partiordrer til å administrere produksjonsprosessene. Partiordrer opprettes fra formler, og disse formlene kan defineres slik at de har koprodukter og biprodukter som utlevering. Når tilbakemelding om disse partiordrene er rapportert, må mengden utlevering registreres på formelvaren, og også på koproduktene og biproduktene.

Når en arbeider fullfører eller delvis fullfører en jobb i en partiordre, kan de rapportere korrekt antall eller svinn for hvert produkt som er definert som utlevering for ordren. Produkter som er definert som utlevering for en partiordre, kan være av typen *Formel*, *Koprodukt* eller *Biprodukt*.

Hvis en arbeider skal rapportere korrekt antall varer på produktene, velger han eller hun en jobb i kategorien **Aktive jobber**, og velger deretter **Rapportfremgang**.

I dialogboksen **Rapportfremgang** kan deretter arbeideren velge blant produktene som er definert som utdata for partiordren det skal rapporteres om. Arbeideren kan velge ett eller flere produkter i listen, og deretter velge **Rapportfremdrift**. For hvert produkt er antallet tomt som standard, og arbeideren kan bruke det numeriske tastaturet til å angi antallet. Arbeideren kan bruke knappene **Forrige** og **Neste** til å flytte mellom de valgte produktene. Når antallet er angitt for hvert produkt, kan arbeideren oppdatere statusen for jobben til *Pågår*, *Stoppet* eller *Fullført*.

![Rapporter koprodukter og biprodukter.](media/report-co-by-products.png "Rapportere koprodukter og biprodukter")

### <a name="reporting-on-batch-orders-for-planning-items"></a>Rapportering av partiordrer for planleggingselementer

Når en arbeider fullfører en jobb i en partiordre for et planleggingselement, rapporterer de bare antall på koprodukter og biprodukter, fordi planleggingselementer ikke inneholder en vare av *Formel*-typen.

### <a name="reporting-co-product-variation"></a>Rapportering av koproduktvariasjon

Hvis det opprettes en partiordre fra en formelversjon der alternativet **Koproduktvariasjoner** er satt til *Ja*, kan arbeideren rapportere på koprodukter som ikke er en del av definisjonen for partiordrene. Denne funksjonaliteten brukes i scenarier der uventede produktutdata kan forekomme i produksjonsprosessen.

I dette tilfellet kan arbeideren angi koproduktet og antallet som skal rapporteres, ved å velge **Koproduktvariasjoner** i dialogboksen Rapportfremgang. Arbeideren kan deretter velge blant alle de frigitte produktene som er definert som koprodukter.

### <a name="reporting-catch-weight-items"></a>Rapportere faktisk vekt-varer

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Arbeidere kan bruke grensesnittet for produksjonsutførelse til å rapportere fremdrift for partiordrer som opprettes for faktisk vekt-varer. Partiordrer opprettes fra formler, som kan defineres slik at de har faktisk vekt-varer som formelvarer, koprodukter og biprodukter. En formel kan også defineres slik at den har formellinjer for ingredienser som er definert for faktisk vekt. Faktisk vekt-varer bruker to måleenheter til å spore lager: faktisk vekt-antall og lagerantall. I næringsmiddelindustrien kan for eksempel kjøtt på boks defineres som en faktisk vekt-vare, der faktisk vekt-antallet brukes til å spore antall bokser og lagerantallet brukes til å spore vekten på boksene.

## <a name="reporting-scrap"></a>Rapportere svinn

Når en arbeider fullfører eller delvis fullfører en jobb, kan de rapportere svinn som ble produsert ved å velge en jobb i fanen **Aktive jobber** og deretter velge **Rapportere svinn**. I dialogboksen **Rapportere svinn** angir arbeideren deretter svinnantall ved hjelp av det numeriske tastaturet. Arbeideren velger også en årsak (*ingen*, *maskin*, *operatør* eller *materiale*).

![Dialogboksen Rapportere svinn.](media/pfei-report-scrap-dialog.png "Dialogboksen Rapportere svinn")

## <a name="adjust-material-consumption-and-make-material-reservations"></a>Justere materialforbruk og foreta materialreserveringer

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Arbeidere kan justere materialforbruket for hver produksjonsjobb. Denne funksjonaliteten brukes i scenarioer der det faktiske antallet materialer som ble forbrukt av en produksjonsjobb, var mer eller mindre enn det planlagte antallet. Det må derfor justeres for å holde lagernivåene gjeldende.

Arbeidere kan også reservere bunke- og serienumre for materialer. Denne funksjonaliteten brukes i scenarioer der en arbeider må angi hvilke materialparti- eller serienumre som ble forbrukt, for å oppfylle materialsporingskravene.

Arbeidere kan angi antallet som skal justeres, ved å velge **Juster materiale**. Denne knappen er tilgjengelig på følgende steder:

- I dialogboksen **Rapporter svinn**
- I dialogboksen **Rapporter fremdrift**
- På verktøylinjen til høyre

### <a name="adjust-material-consumption-from-the-report-scrap-and-report-progress-dialog-boxes"></a>Justere materialforbruk fra dialogboksene Rapporter svinn og Rapporter fremdrift

Når en arbeider har angitt antallet som skal rapporteres i dialogboksen **Rapporter fremdrift** eller **Rapporter svinn**, blir knappen **Juster materiale** tilgjengelig. Når brukeren velger denne knappen, vises dialogboksen **Juster materiale**. Denne dialogboksen viser en liste over varene som ifølge planen skal forbrukes når antallet for gode varer eller svinn rapporteres for jobben.

Listen i dialogboksen viser følgende informasjon:

- **Produktnummer** – Produktstandarden og produktvarianten.
- **Produktnavn** – Produktnavnet.
- **Forslag** – Det estimerte antallet materialer som vil bli forbrukt når fremdrift eller svinn rapporteres for det angitte antallet for jobben.
- **Forbruk** – Det faktiske antallet materialer som vil bli forbrukt når fremdrift eller svinn rapporteres for det angitte antallet for jobben.
- **Reservert** – Antall materialer som er fysisk reservert på lager.
- **Enhet** – Stykklisteenheten (BOM).

Høyre side i dialogboksen viser følgende informasjon:

- **Produktnummer** – Produktstandarden og produktvarianten.
- **Estimert** – Det estimerte antallet som skal forbrukes.
- **Startet** – Antallet som er startet på produksjonsjobben.
- **Restantall** – Av det estimerte antallet, antallet som gjenstår å forbrukes.
- **Frigitt antall** – Antallet som er forbrukt.

Følgende handlinger kan utføres:

- Arbeideren kan angi antallet som skal justeres for et materiale, ved å velge **Juster forbru**. Når antallet er bekreftet, oppdateres antallet i **Forbruk**-kolonnen med det justerte antallet.
- Når arbeideren velger **Juster materiale**, opprettes det en plukklistejournal for produksjon. Denne journalen inneholder de samme varene og antallene som listen **Juster materiale**.
- Når arbeideren justerer et antall i dialogboksen **Juster materiale**, oppdateres **Forslag**-feltet på den tilhørende journallinjen med det samme antallet. Hvis arbeideren velger **Avbryt** i dialogboksen **Juster materiale**, slettes plukklisten.
- Hvis arbeideren velger **OK**, slettes ikke plukklisten. Den posteres når jobben rapporteres i dialogboksen **Rapporter svinn** eller **Rapport fremdrift**.
- Hvis arbeideren velger **Avbryt** i dialogboksen **Rapporter fremdrift** eller **Rapporter svinn**, slettes plukklisten.

### <a name="adjust-material-from-the-toolbar-on-the-right"></a>Justere materiale fra verktøylinjen til høyre

Knappen **Juster materiale** kan konfigureres slik at den vises på verktøylinjen til høyre. (Hvis du vil ha mer informasjon, kan du se [Utforme grensesnittet for produksjonsutførelse](production-floor-execution-tabs.md).) En arbeider kan velge **Juster materiale** for en produksjonsjobb som pågår. I dette tilfellet vises dialogboksen **Juster materiale**, der arbeideren kan foreta de ønskede justeringene. Når dialogboksen åpnes, opprettes det en produksjonsplukkliste som inneholder linjer for de justerte antallene for produksjonsordren. Hvis arbeideren velger **Poster nå**, bekreftes justeringen og plukklisten posteres. Hvis arbeideren velger **Avbryt nå**, slettes plukklisten, og ingen justering foretas.

### <a name="adjust-material-consumption-for-catch-weight-items"></a>Justere materialforbruk for faktisk vekt-varer

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Arbeidere kan justere materialforbruk for faktisk vekt-varer. Denne funksjonaliteten brukes i scenarioer der det faktiske antallet av et faktisk vekt-materiale som ble forbrukt av en produksjonsjobb, var mer eller mindre enn det planlagte antallet. Det må derfor justeres for å holde lagernivåene gjeldende. Når arbeidere justerer forbruket av en faktisk vekt-vare, kan de justere både faktisk vekt-antallet og lagerantallet. Hvis det for eksempel er planlagt at en produksjonsjobb skal bruke fem bokser med en beregnet vekt på 2 kg per boks, kan arbeideren justere både antall bokser som skal brukes, og vekten på boksene. Systemet validerer at den angitte vekten på boksene er innenfor den definerte minimums- og maksimumsterskelen som er definert for det frigitte produktet.

### <a name="reserve-materials"></a>Reserver materialer

I dialogboksen **Juster materiale** kan en arbeider utføre og justere materialreserveringer ved å velge **Reserver materiale**. Dialogboksen **Reserver materiale** som vises, viser den fysisk tilgjengelige beholdningen for varen for hver lagrings- og sporingsdimensjon.

Hvis materialet er aktivert for de avanserte lagerprosessene, viser listen bare den fysisk tilgjengelige beholdningen for produksjonsinngangsstedet for materialet. Produksjonsinngangsstedet er definert på ressursen der produksjonsjobben er planlagt. Hvis varenummeret er parti- eller serienummerkontrollert, vises den fullstendige listen over fysisk tilgjengelige bunke- og serienumre. Når du skal angi et antall som skal reserveres, kan du velge **Reserver materiale**. Hvis du vil fjerne en eksisterende reservasjon, kan du velge **Fjern reservasjon**.

Hvis du vil ha mer informasjon om hvordan du definerer produksjonsinngangsstedet, kan du se følgende blogginnlegg: [Oppsett av produksjonsinngangsstedet](/archive/blogs/axmfg/deliver-picked-materials-to-the-locations-where-the-materials-are-consumed-by-operations-in-production).

> [!NOTE]
> Reservasjoner som en arbeider foretar i dialogboksen **Reserver materiale**, blir værende når arbeideren velger **Avbryt** i dialogboksen **Rapporter fremdrift** eller **Rapporter svinn**.
>
> Det går ikke an å justere reservasjoner for faktisk vekt-varer.

## <a name="completing-a-job-and-starting-a-new-job"></a>Fullføre en jobb og starte en ny jobb

Vanligvis fullfører arbeidere en jobb ved å velge én eller flere gjeldende jobber i fanen **Aktive jobber** og deretter velge **Rapportfremdrift**. Deretter angir du antallet som ble produsert (korrekt antall), og setter statusen til *Fullført*. Hvis mer enn én jobb ble valgt, bruker en arbeider **Forrige** - og **Neste**-knappene til å flytte mellom dem. For å starte en ny jobb velger arbeideren den i fanen **Alle jobber** og velger deretter **Start jobb**.

En arbeider kan også starte en ny jobb mens den forrige jobben fremdeles er åpen. Igjen velger arbeideren den nye jobben i fanen **Alle jobber** og velger deretter **Start jobb**. I dette tilfellet informerer imidlertid dialogboksen **Start jobb** arbeideren om at de for øyeblikket arbeider med en jobb, og de må derfor enten stoppe eller fullføre denne jobben før de starter den nye jobben.

## <a name="working-on-multiple-jobs-in-parallel"></a>Arbeide med flere jobber parallelt

Én arbeider kan arbeide med flere jobber samtidig (det vil si parallelt). I dette tilfellet kalles samlingen av jobber som arbeideren arbeider med, en *jobbunt*. Arbeideren kan legge til nye jobber i bunten, eller fullføre én eller flere jobber i bunten. Følgende to scenarier viser hvordan en arbeider kan arbeide med jobber parallelt.

### <a name="scenario-1-a-worker-who-has-no-active-jobs-wants-to-start-two-jobs-and-work-on-them-in-parallel"></a>Scenario 1: En arbeider som ikke har noen aktive jobber, vil starte to jobber og arbeide med dem parallelt

Arbeideren velger de to jobbene i fanen **Alle jobber** og velger deretter **Start jobb**. Dialogboksen **Start jobb** viser begge valgte jobber, og arbeideren kan justere antallet som skal startes i hver jobb. Deretter bekrefter arbeideren dialogboksen og kan starte begge jobbene.

### <a name="scenario-2-a-worker-who-has-two-active-jobs-that-are-in-progress-wants-to-start-a-third-job-and-work-on-it-in-parallel-with-the-other-two"></a>Scenario 2: En arbeider som har to aktive jobber, vil starte en tredje jobb, og arbeide på den parallelt med de to andre

Arbeideren velger den tredje jobben i fanen **Alle jobber** og velger deretter **Bunt**. I dialogboksen **Bunt** kan arbeideren justere antallet som skal startes. Deretter bekrefter arbeideren dialogboksen ved å velge **Bunt**.

## <a name="working-on-indirect-activities"></a>Arbeide på indirekte aktiviteter

Indirekte aktiviteter er aktiviteter som ikke er direkte knyttet til en produksjonsordre. Indirekte aktiviteter kan være fleksibelt definert, som beskrevet i [Definere indirekte aktiviteter for timeregistrering](/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance).

For eksempel Shannon, en produksjonsarbeider hos Contoso, vil delta på et firmamøte, og møter regnes som en indirekte aktivitet. Et av følgende to scenarioer gjelder:

- **Shannon arbeider på én eller flere aktive jobber.** Shannon velger **Aktivitet**, identifiserer aktiviteten (møtet) og bekrefter valget. En melding som vises, informerer henne om at hun har pågående jobber. Fra meldingen kan Shannon velge å fullføre eller stoppe jobbene som hun arbeider med før hun går til møtet.
- **Shannon har ingen aktive jobber.** Shannon velger **Aktivitet**, identifiserer aktiviteten (møtet) og bekrefter valget. Hun er nå registrert som å være på møtet.

I begge scenarioene, etter at Shannon bekrefter sitt valg, går hun enten til påloggingssiden eller en side som venter på at hun skal bekrefte at hun har returnert fra den indirekte aktiviteten. Hvilken side som vises, er avhengig av konfigurasjonen av grensesnittet for produksjonsutførelse. (Hvis du vil ha mer informasjon, kan du se [Konfigurere grensesnittet for produksjonsutførelse](production-floor-execution-configure.md).)

## <a name="registering-breaks"></a>Registrere pauser

Arbeidere kan registrere pauser. Pauser kan være fleksibelt definert, som beskrevet i [Lønn basert på registreringer](pay-based-on-registrations.md).

En arbeider registrerer en pause ved å velge **Pause** og deretter velge kortet som representerer pausetypen (for eksempel lunsj). Når arbeideren har bekreftet valget, viser enheten enten påloggingssiden eller en side som venter på at arbeideren skal bekrefte at de er returnert fra pausen. Hvilken side som vises, er avhengig av konfigurasjonen av grensesnittet for produksjonsutførelse. (Hvis du vil ha mer informasjon, kan du se [Konfigurere grensesnittet for produksjonsutførelse](production-floor-execution-configure.md).)

## <a name="opening-instructions"></a>Åpne instruksjoner

Arbeidere kan åpne et dokument som er knyttet til en jobb, ved å velge **Instruksjoner**. Knappen **Instruksjoner** er bare tilgjengelig hvis et dokument er knyttet til jobben i hoveddataene. Et dokument som er knyttet til et produkt på siden **Frigitte produkter** i Supply Chain Management, vil for eksempel være tilgjengelig for arbeidere for åpning i kjøringsgrensesnittet for produksjon.

## <a name="opening-mixed-reality-guides-for-hololens"></a>Åpne blandet virkelighet-veiledninger for HoloLens

[Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) kan bidra til å gi de ansatte praktisk læring som bruker blandet virkelighet. Du kan definere standardiserte prosesser der trinnvise instruksjoner leder de ansatte til verktøyene og delene de trenger, og viser de ansatte hvordan de skal bruke disse verktøyene i virkelige situasjoner. Her er en oversikt over prosessen.

1. Hver gang en arbeider åpner en jobbliste i kjøringsgrensesnittet for produksjon, finner grenesnittet alle de relevante veiledningene for jobbene som vises.
1. Arbeideren velger **Veiledninger** for å vise listen over veiledninger.
1. Arbeideren velger en relevant veiledning i listen.
1. Kjøringsgrensesnittet for produksjon viser en QR-kode for den valgte veiledningen.
1. Arbeideren tar på en HoloLens og ser på QR-koden for å starte veiledningen.
1. Arbeideren jobber seg gjennom veiledningen for å lære oppgaven.

Hvis du vil ha mer informasjon om hvordan du oppretter, tilordner og bruker veiledninger for HoloLens, kan du se [Formidle veiledninger for blandet virkelighet for arbeidere i produksjonen](instruction-guides-in-production-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

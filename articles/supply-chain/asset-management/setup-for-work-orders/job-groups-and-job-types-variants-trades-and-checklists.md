---
title: Kategorier for vedlikeholdsjobbtyper og vedlikeholdsjobbtyper, varianter av vedlikeholdsjobbtyper, vedlikeholdsjobbfag og sjekklister for vedlikehold
description: Dette emnet beskriver kategorier for vedlikeholdsjobbtyper og vedlikeholdsjobbtyper, varianter av vedlikeholdsjobbtyper, vedlikeholdsjobbfag og sjekklister for vedlikehold i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6cb53322b9bdaaa06c6040d8244b7e2ea05336ca
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249615"
---
# <a name="maintenance-job-type-categories-and-maintenance-job-types-maintenance-job-type-variants-maintenance-job-trades-and-maintenance-checklists"></a>Kategorier for vedlikeholdsjobbtyper og vedlikeholdsjobbtyper, varianter av vedlikeholdsjobbtyper, vedlikeholdsjobbfag og sjekklister for vedlikehold

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

En aktivatype er knyttet til hvert aktiva. Aktivatyper definerer vedlikeholdsjobbtypene (og dermed vedlikeholdsjobbene) som kan utføres på aktiva. Når du oppretter en arbeidsordre, må du velge en vedlikeholdsjobbtype. Du kan bare velge vedlikeholdsjobbtypene som er relatert til oppsettet for aktivatypen som brukes for aktivaet.

Hvis du vil ha en grafisk oversikt over aktiva og vedlikeholdsjobbtyper og deres tilknytning til arbeidsordrer, kan du se [Aktiva og arbeidsordrer](../overview/functional-locations-and-objects.md).

Du kan definere varianter av vedlikeholdsjobbtyper for en vedlikeholdsjobbtype. Varianter av vedlikeholdsjobbtyper angir variasjoner av en jobbtype, for eksempel størrelse (liten, middels eller stor), perioder (ukentlig, annenhver uke, én måned eller tre måneder) og konfigurasjoner (lav standard, fleksibel eller høy ytelse).

Vedlikeholdsjobbfag gir informasjon om profesjonsfag, for eksempel mekanisk, elektrisk og hydraulisk. Kompetansekrav kan defineres for et vedlikeholdsjobbfag. Alle vedlikeholdsjobbfag kan brukes i forbindelse med alle vedlikeholdsjobbtyper. Valg av variant av vedlikeholdsjobbtype og/eller vedlikeholdsjobbfag for en arbeidsordre er valgfritt.

For hver vedlikeholdsjobbtype kan varianter av vedlikeholdsjobbtypeoppsettet opprettes. Hvis du for eksempel har en vedlikeholdsjobbtype som heter **Service**, kan du opprette følgende variasjoner for vedlikeholdsjobbtypen: **Lastebiler 30 000 km**, **Biler 30 000 km** og **Varebiler 30 000 km**.

Kategoriene for vedlikeholdsjobbtype brukes til å gruppere vedlikeholdsjobbtyper for å få oversikt. Eksempler på kategorier for vedlikeholdsjobbtyper kan være **Kalibrering**, **Inspeksjon**, **Overhaling** og **Instrumentering**.

Maler for vedlikeholdsjekklister og variabler for vedlikeholdssjekklister brukes til å definere sjekklister for vedlikehold. Sjekklister for vedlikehold defineres i vedlikeholdsjobbtyper og brukes i arbeidsordrer.

Først definerer du de nødvendige kategoriene for vedlikeholdsjobbtype, varianter av vedlikeholdsjobbtype og vedlikeholdsjobbfag. Deretter oppretter du vedlikeholdsjobbtyper. På siden **Standarder for vedlikeholdstype** oppretter du til slutt alle variantene av vedlikeholdsjobbtyper som kreves for utstyret. På denne siden kan du også definere prognoser, sjekklister for vedlikehold og verktøy for en kombinasjon av vedlikeholdsjobbtyper.

> [!NOTE]
> En vedlikeholdsjobbtype kan bare knyttes til én kategori av vedlikeholdsjobbtype.

## <a name="create-a-maintenance-job-type-category"></a>Opprette en kategori for vedlikeholdsjobbtype

1. Velg **Aktivastyring** \> **Oppsett** \> **Jobber** \> **Kategorier for vedlikeholdsjobbtype**.
2. Velg **Ny**.
3. Angi en ID for kategorien av vedlikeholdsjobbtype i feltet **Kategori for vedlikeholdsjobbtype**.
4. Angi et navn i **Navn**-feltet.

    Når du har knyttet kategorier av vedlikeholdsjobbtyper til vedlikeholdsjobbtyper, viser **Jobbtyper**-feltet antallet vedlikeholdsjobbtyper som er knyttet til denne kategorien av vedlikeholdsjobbtype.

![Figur 1](media/01-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type-variant"></a>Opprette en variant av vedlikeholdsjobbtype

1. Velg **Aktivastyring** \> **Oppsett** \> **Jobber** \> **Varianter av vedlikeholdsjobbtype**.
2. Velg **Ny**.
3. Angi en ID for varianten av vedlikeholdsjobbtype i feltet **Variant av vedlikeholdsjobbtype**.
4. Angi en beskrivelse i **Beskrivelse**-feltet.
5. Velg **Legg til** for å legge til en vedlikeholdsjobbtype i hurtigfanen **Vedlikeholdsjobbtyper**.
6. I feltet **Vedlikeholdsjobbtype** velger du vedlikeholdsjobbtypen.
7. Gjenta trinn 5 til og med 6 for å legge til flere vedlikeholdsjobbtyper i varianten av vedlikeholdsjobbtype.

    I hurtigfanen **Detaljer** viser **Jobbtyper**-feltet antallet vedlikeholdsjobbtyper som er lagt til denne varianten av vedlikeholdsjobbtype.

![Figur 2](media/02-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-trade"></a>Opprette et vedlikeholdsjobbfag

1. Velg **Aktivastyring** \> **Oppsett** \> **Jobber** \> **Vedlikeholdsjobbfag**.
2. Velg **Ny**.
3. I **Handel**-feltet angir du en ID for vedlikeholdsjobbfaget.
4. Angi en beskrivelse i **Beskrivelse**-feltet.
5. Velg **Legg til** i hurtigfanen **Kompetanse** for å legge til en ny kompetanse som skal relateres til vedlikeholdsjobbfaget.
6. Velg kompetansen i **Kompetanse**-feltet.
7. Velg kompetansenivået i **Nivå**-feltet.
8. Gjenta trinn 5 til 7 for å legge til flere kompetanser i vedlikeholdsjobbfaget.

    I hurtigfanen **Detaljer** viser **Kompetanse**-feltet antallet kompetanser som er lagt til dette vedlikeholdsjobbfaget.

9. Velg **Legg til** i hurtigfanen **Sertifikater** for å legge til et sertifikat i vedlikeholdsjobbfaget.
10. I feltet **Sertifikattype** velger du sertifikatet.
11. Gjenta trinn 9 til 10 for å legge til flere sertifikater i vedlikeholdsjobbfaget.

    I hurtigfanen **Detaljer** viser **Sertifikater**-feltet antallet sertifikater som er lagt til dette vedlikeholdsjobbfaget.

![Figur 3](media/03-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-variable"></a>Opprette en variabel for vedlikeholdssjekkliste

Når du oppretter vedlikeholdssjekklistelinjer i standard vedlikeholdsjobbtype, må du velge type vedlikeholdssjekkliste. **Variabel** er én sjekklistetype for vedlikehold. Den brukes til å definere et mulig resultat i et område på en vedlikeholdssjekklistelinje som er knyttet til en arbeidsordrelinje. Med en variabel kan du opprette et sett med forhåndsdefinerte resultater uten å måtte opprette en nøyaktig måling.

**Eksempel 1:** Du kan måle oljenivå ved å definere tre verdier: **Nivå for høyt**, **Nivå for lavt** og **Nivå innenfor område**. For hver verdi definerer du om verdiresultatet er **Bestått**, **Ikke bestått** eller **Ingen**.

**Eksempel 2:** Du gjør en visuell inspeksjon av et utstyr for å vurdere slitasjen.

1. Velg **Aktivastyring** \> **Oppsett** \> **Vedlikeholdssjekklister** \> **Variabler for vedlikeholdssjekklister**.
2. Velg **Ny**.
3. I **Variabel**-feltet angir du en ID for vedlikeholdssjekklistevariabelen.
4. Angi et navn i **Navn**-feltet.
5. Velg **Legg til** i hurtigfanen **Generelt** for å legge til en linje for en variabel.

    Et sekvensielt linjenummer angis automatisk i feltet **Linjenummer**. Når du har lagt til alle linjene, kan du endre linjenumrene slik du ønsker. Når du velger linje og trykker på **Pil ned**, blir det neste tallet i sekvensen automatisk lagt inn på neste linje.

6. Angi en verdibeskrivelse i feltet **Verdi**.
7. I **Resultat**-feltet velger du et resultat for linjen.

![Figur 4](media/04-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-template"></a>Opprette en mal for vedlikeholdssjekkliste

Maler for vedlikeholdssjekklister kan brukes som et felles sett med oppgaver som en arbeider må utføre for å fullføre en arbeidsordre på riktig måte. Malene refereres fra vedlikeholdssjekklistelinjer i standard vedlikeholdsjobbtype. Det kan refereres til maler i flere standard vedlikeholdsjobbtypelinjer. Derfor kan du lett bruke et sett med vanlige vedlikeholdssjekklisteoppgaver på nytt. Eksempler på maler for vedlikeholdssjekkliste er generelle sikkerhetsinstruksjoner og en liste over elementer og betingelser som må kontrolleres på en bestemt pumpe eller lignende modeller for et transportbånd.

1. Velg **Aktivastyring** \> **Oppsett** \> **Vedlikeholdssjekklister** \> **Maler for vedlikeholdssjekklister**.
2. Velg **Ny**.

    En mal-ID angis automatisk i feltet **Mal for vedlikeholdssjekkliste**.

3. I **Navn**-feltet angir du et navn på malen for vedlikeholdssjekkliste.
4. Velg **Legg til** på hurtigfanen **Vedlikeholdssjekklistelinjer** for å legge til en mallinje.

    Et sekvensielt linjenummer angis automatisk i feltet **Linjenummer**. Når du har lagt til alle linjene, kan du endre linjenumrene slik du ønsker. Når du velger linje og trykker på **Pil ned**, blir det neste tallet i sekvensen automatisk lagt inn på neste linje.

5. Velg en type for vedlikeholdssjekklistelinjen i **Type**-feltet. For hver type vedlikeholdssjekkliste viser hurtigfanen **Linjedetaljer** relaterte felt. Følgende verdier er tilgjengelige:

    - **Tekst** – Linjen har tekst som beskriver hva som skal gjøres. Bruk denne vedlikeholdssjekklistetypen hvis du vil at en arbeider skal sjekke eller inspisere noe, men du ikke forventer et bestemt (målbart) resultat. Når du har valgt denne typen, skriver du inn et navn eller en overskrift i **Navn**-feltet. I **Instruksjoner**-feltet angir du en beskrivelse av hva som må gjøres. Hvis trinnet er obligatorisk for vedlikeholdssjekklisten, setter du alternativet **Obligatorisk** til **Ja**.
    - **Hode** – Linjen brukes som en overskrift for å gruppere vedlikeholdssjekklistelinjene som vises under det. Denne typen er nyttig hvis du har flere vedlikeholdssjekklistelinjer som kan deles inn i bestemte områder. Hoder gir en oversikt for arbeideren som skal fylle ut en vedlikeholdssjekkliste som har mange vedlikeholdssjekklistelinjer. Når du har valgt denne typen, skriver du inn et beskrivende navn i **Navn**-feltet.
    - **Mal** – Linjen brukes til å lage en referanse til en eksisterende mal. Når du har valgt denne typen, skriver du inn et navn på malen i **Navn**-feltet. Velg malen i **Mal**-feltet.
    - **Variabel** – Linjen brukes til å definere et mulig resultat i et område. Hvis du vil ha mer informasjon om hvordan du definerer variablene for vedlikeholdssjekklister, se delen [Opprette en variabel for vedlikeholdssjekkliste](#create-a-maintenance-checklist-variable). Når du har valgt denne typen, skriver du inn et beskrivende navn på variabelen i **Navn**-feltet. I **Variabel**-feltet velger du variabelen. I **Instruksjoner**-feltet angir du en beskrivelse av hva som må gjøres. Hvis trinnet er obligatorisk for vedlikeholdssjekklisten, setter du alternativet **Obligatorisk** til **Ja**.
    - **Måling** – Linjen brukes til å registrere en bestemt måling. Du kan definere målingen som skal knyttes til en forhåndsdefinert teller. Når du har valgt denne typen, skriver du inn et navn på malen i **Navn**-feltet. Hvis dette trinnet er obligatorisk for vedlikeholdssjekklisten, setter du alternativet **Obligatorisk** til **Ja**. Hvis du vil bruke målelinjen som en tellerregistrering, velger du telleren i **Teller**-feltet. Det tilknyttede **Enhet**-feltet oppdateres deretter automatisk. Hvis du har valgt en teller, velger du oppdateringsmetoden i **Verdi**-feltet. I feltene **Minimumsverdi** og **Maksimumsverdi** angir du tillatt verdiintervall. I **Instruksjoner**-feltet angir du en beskrivelse av hva som må gjøres.

        > [!NOTE]
        > Alle linjer av typen **Måling** som ikke har et telleroppsett, behandles som en uavhengig målingsregistrering som ikke har noen automatisk oppfølging i Aktivastyring. På samme måte behandles vedlikeholdssjekklisteoppgaven som en uavhengig måling hvis den valgte tellertypen ikke er til stede på aktivaet som er knyttet til arbeidsordren. Tellerverdien kan endres flere ganger. Den posteres ikke før [tilstanden for arbeidsordrelivssyklus](work-order-lifecycle-states.md) endres til en tilstand der alternativet **Behandle vedlikeholdssjekkliste** er satt til **Ja**.

    **Kontroller**-feltet i hurtigfanen **Detaljer** viser det totale antallet sjekklistelinjer i malen. Dette tallet inkluderer de nestede linjene i en eksisterende mal som du har referert til i malen.

![Figur 5](media/05-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type"></a>Opprette en vedlikeholdsjobbtype

1. Velg **Aktivastyring** \> **Oppsett** \> **Jobber** \> **Vedlikeholdsjobbtyper**.
2. Velg **Ny**.
3. Angi en ID for vedlikeholdsjobbtypen i feltet **Vedlikeholdsjobbtype**.
4. Angi et navn i **Navn**-feltet.

    Hurtigfanen **Detaljer** viser en oversikt over antall varianter av vedlikeholdsjobbtype, kompetanser, sertifikater, etterfølgende jobber og aktivatyper som er opprettet for denne vedlikeholdsjobbtypen. Feltet **Oppsettslinjer** viser antall linjer for vedlikeholdsjobbtypestandard som er definert for denne vedlikeholdsjobbtypen. **Aktiva**-feltet viser antall aktive aktiva som for øyeblikket bruker denne vedlikeholdsjobbtypen.

5. Velg en kategori for vedlikeholdsjobbtype i feltet **Kategori for vedlikeholdsjobbtype** i hurtigfanen **Generelt**.
6. Sett alternativet **Aktiviteter for vedlikeholdsnedetid** til **Ja** hvis vedlikeholdsjobbtypen krever et vedlikeholdsstopp på utstyret før jobben kan utføres.
7. I hurtigfanen **Beskrivelse** angir du en beskrivelse av vedlikeholdsjobbtypen.
8. Du kan legge til varianter av vedlikeholdsjobbtypen i hurtigfanen **Varianter av vedlikeholdsjobbtype**.
9. På hurtigfanene **Nødvendige kompetanser** og **Nødvendige sertifikater** kan du legge til krav til ferdigheter og sertifikat i vedlikeholdsjobbtypen.
10. Hvis det må utføres en bestemt vedlikeholdsjobbtype etterpå, legger du den til i hurtigfanen **Etterfølgende jobber**. Du kan også definere vedlikeholdsjobbtypevariant og -fag som er knyttet til vedlikeholdsjobbtypen. Hvis den etterfølgende jobben må starte et bestemt antall dager før eller etter at jobben som bruker denne vedlikeholdsjobbtypen har startet, angir du antallet dager i feltet **Forsinkelse etter dager**. Positive tall representerer dager etter starten på den tilknyttede jobben, og negative tall representerer dager før den planlagte starten på den tilknyttede jobben. Hvis du for eksempel angir **5**, vil den etterfølgende jobben starte fem dager etter starten på jobben som er knyttet til vedlikeholdsjobbtypen. Hvis du angir **-3**, vil den etterfølgende jobben starte tre dager før den planlagte starten på jobben som er knyttet til vedlikeholdsjobbtypen.

    > [!NOTE]
    > Hvis du legger til mer enn én vedlikeholdsjobbtypelinje, angir rekkefølgen på linjene rekkefølgen de skal utføres i. Sekvensen starter øverst på listen.

11. I hurtigfanen **Aktivatyper** kan du legge til aktivatyper i vedlikeholdsjobbtypen.

![Figur 6](media/06-setup-for-work-orders.png)

## <a name="create-maintenance-job-type-default-lines-and-related-forecasts-maintenance-checklists-tools-description-and-attachments"></a>Opprette linjer for vedlikeholdsjobbtypestandarder og tilknyttede prognoser, vedlikeholdssjekklister, verktøy, beskrivelse og vedlegg

1. Velg **Aktivastyring** \> **Oppsett** \> **Jobber** \> **Standarder for vedlikeholdsjobbtype**.

    – eller –

    Velg **Aktivastyring** \> **Oppsett** \> **Jobber** \> **Vedlikeholdsjobbtyper**, velg en vedlikeholdsjobbtype, og velg deretter **Standarder for vedlikeholdsjobbtype**.

2. Velg **Ny**.
3. I feltene **Arbeidssted**, **Aktivatype**, **Produsent**, **Modell** og **Aktivum** velger du aktuelle verdier, avhengig av hvor bestemt vedlikeholdsjobbtypestandarden skal være.
4. Velg en vedlikeholdsjobbtype i feltet **Vedlikeholdsjobbtype** hvis den ikke er valgt automatisk.
5. I feltene **Variant av vedlikeholdsjobbtype** og **Fag** velger du en vedlikeholdsjobbtypevariant og et vedlikeholdsjobbfag som du trenger.
6. Velg **Prognose**.
7. På siden **Prognose for standard vedlikeholdsjobbtype** kan du lage prognoser for timer, varer og utgifter. Velg **Legg til** i de relevante kategoriene, og gjør valg for å opprette de nødvendige prognosene for vedlikeholdsjobbtypen.
8. I kategorien **Vareprognose** kan du velge lagerdimensjoner som skal vises på varelinjen. Velg **Lager** \> **Dimensjoner**, velg dimensjonene som skal vises, sett alternativet **Lagre oppsett** til **Ja**, og velg **OK**.
9. Hvis du vil ha en oversikt over hvor i Aktivastyring varen på den valgte linjen brukes, i forhold til aktiva, vedlikeholdsjobbtypestandard, reservedeler og arbeidsordrer, velger du **Vare der brukt** i kategorien **Vareprognose**. 

    Hurtigfanen **Totaler for vedlikeholdsprognose** viser en oversikt over prognosetotaler. Denne oversikten inkluderer det totale antallet timer og prognoselinjer som er opprettet.

    > [!NOTE]
    > Hvis du vil kopiere prognoseoppsettet fra en annen vedlikeholdsjobbtype, velger du **Kopier prognose**, og deretter velger du vedlikeholdsjobbtypen du vil kopiere oppsettet fra.

11. Velg **Lagre** for å lagre endringene.
12. Lukk siden **Prognose for standard vedlikeholdsjobbtype** for å gå tilbake til siden **Standarder for vedlikeholdsjobbtype**.
13. Velg **Vedlikeholdssjekkliste**.
14. På siden **Sjekkliste for vedlikeholdsjobbtypestandarder** kan du legge til sjekklistelinjer for vedlikehold i den valgte vedlikeholdsjobbtypestandarden. Velg **Ny** på hurtigfanen **Vedlikeholdssjekklinjer** for å legge til en vedlikeholdssjekklistelinje.

    Linjenumre angis automatisk i **Linjenummer**-feltet for å angi rekkefølgen på linjene i vedlikeholdssjekklisten. Du kan redigere linjenumre etter behov. Når du har opprettet den første linjen for vedlikeholdssjekkliste, merker du linjen og trykker på **Pil ned**-tasten for å legge til en linje under den. Du kan også velge en vedlikeholdssjekklistelinje, og deretter velge **Ny**. I dette tilfellet legges det til en ny linje over den valgte sjekklistelinjen for vedlikehold.

15. I **Type**-feltet velger du linjetypen, og deretter legger du til informasjon som er relatert til vedlikeholdssjekklistetypen. Hvis du vil ha en beskrivelse av de tilgjengelige typene og tilknyttede felt, kan du se delen [Opprette en mal for vedlikeholdssjekkliste](#create-a-maintenance-checklist-template).

    > [!NOTE]
    > Hvis du vil kopiere oppsettet for vedlikeholdssjekklisten fra en annen vedlikeholdsjobbtype, velger du **Kopier vedlikeholdssjekkliste**, og deretter velger du vedlikeholdsjobbtypen du vil kopiere oppsettet fra.
    >
    > Du kan enkelt opprette en mal fra en eksisterende vedlikeholdssjekkliste. Du kan deretter bruke malen på nytt i flere vedlikeholdssjekklister, Den nye malen vil være en nøyaktig kopi av den aktive vedlikeholdssjekklisten. Velg **Opprett mal** og angi et navn for malen. Hvis du vil erstatte den eksisterende vedlikeholdssjekklisten med en enkelt linje som refererer til den nye malen, setter du alternativet **Erstatt** til **Ja**. Du kan vise innholdet i malen på detaljsiden **Maler for vedlikeholdssjekklister**.

16. Velg **Lagre** for å lagre endringene.
17. Gå tilbake til siden **Standarder for vedlikeholdsjobbtype**.
18. Velg **Verktøy**.
19. På siden **Verktøy for vedlikeholdsjobbtypestandard** kan du legge til verktøyene (ressursene) som skal brukes for vedlikeholdsjobbtypen. Velg **Ny**, og velg deretter verktøyet i **Ressurs**-feltet.

    > [!NOTE]
    > Hvis du vil kopiere verktøyoppsettet fra en annen vedlikeholdsjobbtype, velger du **Kopier verktøy**, og deretter velger du vedlikeholdsjobbtypen du vil kopiere oppsettet fra.

20. Velg **Lagre** for å lagre endringene.
21. Gå tilbake til siden **Standarder for vedlikeholdsjobbtype**.
22. Velg **Arbeidsbeskrivelse**.
23. Velg **Rediger** på **Arbeidsbeskrivelse**-siden, og legg deretter til en beskrivelse som er knyttet til den valgte vedlikeholdsjobbtypestandarden, slik du ønsker.
24. Velg **Lagre** for å lagre beskrivelsen.

    Hvis du legger til en arbeidsbeskrivelse her, overstyrer den eventuelle beskrivelser som er definert for vedlikeholdsjobbtypen på siden **Vedlikeholdsjobbtyper**. Hvis du ikke legger til en arbeidsbeskrivelse her, brukes alle beskrivelser som er definert for vedlikeholdsjobbtypen. Beskrivelser overføres automatisk til arbeidsordrer som bruker vedlikeholdsjobbtypen eller vedlikeholdsjobbtypestandarden.

25. Gå tilbake til siden **Standarder for vedlikeholdsjobbtype**.
26. Når du skal definere vedlegg på en valgt linje for vedlikeholdsjobbtypestandard, velger du **Legg ved dokumenter**. Vedlegg som er definert på en linje for vedlikeholdsjobbtypestandard, tas automatisk med i arbeidsordrelinjer som bruker denne linjen for vedlikeholdsjobbtypestandard.
27. Velg **Ny**, og velg deretter et dokumenttype.
28. Last opp dokumentet eller filen.
29. På siden **Vedlegg** angir du feltene. Vedleggsoppsettet bruker standard dokumentoppsettsfunksjonalitet.
30. Velg **Lagre** for å lagre vedlegget.

    > [!NOTE]
    > Vedlegg i en linje for vedlikeholdsjobbtypestandard skrives ut sammen med en arbeidsordrerapport bare hvis dokumenttypene til vedleggene er valgt i kategorien **Dokumenttyper** på siden **Aktivabehandlingsparametere** (**Aktivastyring** \> **Oppsett** \> **Aktivabehandlingsparametere**). Eksempler på vedlegg er retningslinjer som forklarer hvordan du utfører en bestemt jobb eller en forhåndsdefinert vedlikeholdssjekkliste (hvis du ikke bruker funksjonen for vedlikeholdssjekkliste for linjer for vedlikeholdsjobbtypestandard).

    På siden **Standarder for vedlikeholdsjobbtype** viser hver linje antall prognosetimer, og også antall linjer som er opprettet for varer, utgifter, sjekklister for vedlikehold og verktøy. **Aktiva**-feltet viser antall aktive aktiva som er knyttet til linjen for standard vedlikeholdsjobbtype.

31. Hvis du vil kopiere en vedlikeholdsjobbtypestandard til en annen vedlikeholdsjobbtypestandard, velger du linjen for vedlikeholdsjobbtypestandard for å kopiere et annet oppsett, velger **Kopier oppsett**, og velger deretter vedlikeholdsjobbtypestandarden som skal kopieres.
32. Hvis du vil vise en liste over aktiva, vedlikeholdsplaner eller vedlikeholdsrunder som for øyeblikket bruker en linje for vedlikeholdsjobbtypestandard, merker du linjen og velger **Brukt av**.

![Figur 7](media/07-setup-for-work-orders.png)

Når systemet velger den tilgjengelige vedlikeholdsjobbtypestandarden som skal brukes på en arbeidsordrelinje, baseres valget på aktivaet og det tilknyttede aktivatypeoppsettet. Aktivastyring går gjennom alle postene for vedlikeholdsjobbtypestandard som er relatert til vedlikeholdsjobbtypen som er knyttet til aktivatypen, for å finne et mulig treff. Den kontrollerer alltid den mest spesifikke kombinasjonen først. Med andre ord, for å finne den mest spesifikke kombinasjonen, sjekker Aktivastyring først for et mulig treff for **Handel**-feltet. Hvis det ikke blir funnet noe treff, kontrolleres det for et treff i feltet **Variant av vedlikeholdsjobbtype**. Hvis det ikke blir funnet noe treff, ser det etter treff for feltet **Vedlikeholdsjobbtype** og så videre (**Handel**, deretter **Variant av vedlikeholdsjobbtype**, deretter **Vedlikeholdsjobbtype**, deretter **Aktiva**, deretter **Modell**, deretter **Produsent**og deretter **Aktivatype**). Hvis det ikke blir funnet samsvar, brukes standardposten der bare vedlikeholdsjobbtypen er valgt.

En prosjektaktivitets-ID knyttes automatisk til hver linje for vedlikeholdsjobbtypestandard du oppretter. Prosjektaktiviteten opprettes for prognoseprosjektet som er valgt i feltet **Vedlikeholdsprognoseprosjekt** i kategorien **Aktiva** på siden **Aktivabehandlingsparametere**. Formålet med prosjektaktiviteten er å behandle prognoser for timer, varer og utgifter i forbindelse med arbeidsordrer. Vedlikeholdsjobbtypeprognoser overføres automatisk til arbeidsordrelinjen, og de kopieres fra prognoseprosjektet til arbeidsordreprosjektet som opprettes for arbeidsordrelinjen. Formålet med prosjektaktiviteten er å behandle prognoser i forbindelse med arbeidsordrer.

Du kan definere en satsvis jobb for å oppdatere referanser for standard vedlikeholdsjobbtype med jevne mellomrom, eller du kan kjøre jobben manuelt. Hvis du vil opprette en satsvis jobb eller kjøre en manuell oppdatering , velger du **Aktivastyring** \> **Periodisk** \> **Forebyggende vedlikehold** \> **Oppdater referanser for standard vedlikeholdsjobbtype**.

## <a name="overview-of-maintenance-job-types-that-are-related-to-assets"></a>Oversikt over vedlikeholdsjobbtyper som er knyttet til aktiva

Når du har opprettet de nødvendige kombinasjonene for standard vedlikeholdsjobbtype, kan du bruke siden **Alle aktiva** til å få en oversikt over gjeldende vedlikeholdsjobbtypestandard som er knyttet til et bestemt aktiva. Oversikten viser alle kombinasjoner for standard vedlikeholdsjobbtype som kan brukes for aktivatypen som er valgt for aktivaet. Disse kombinasjonene inkluderer kombinasjoner som har variasjoner av vedlikeholdsjobbtypevarianter og vedlikeholdsjobbfag.

1. Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva** eller **Aktive aktiva**.
2. I listen velger du aktivaet hvis du vil se en oversikt over kombinasjonene for vedlikeholdsjobbtype.
3. Velg **Vedlikeholdsjobbtyper** i handlingsruten i kategorien **Generelt** i gruppen **Beslektet informasjon**.

    Venstre rute på siden **Vedlikeholdsjobbtyper for aktiva** viser en liste over alle kombinasjonene for vedlikeholdsjobbtyper som gjelder for det valgte aktivaet.

4. Velg en kombinasjon for vedlikeholdsjobbtype for å se det tilknyttede oppsettet for vedlikeholdssjekklister, prognoser og verktøy. **Detaljer**-delen på hurtigfanen **Standarder for vedlikeholdsjobbtype** viser antall tilknyttede vedlikeholdssjekklister, prognosetimer, varer og så videre, som er knyttet til den valgte kombinasjonen for vedlikeholdsjobbtype.
5. Hvis du vil vise detaljer for den valgte vedlikeholdsjobbtypen, velger du **Vedlikeholdsjobbtyper**.

![Figur 8](media/08-setup-for-work-orders.png)

## <a name="automatic-update-of-maintenance-job-type-forecasts"></a>Automatisk oppdatering av prognoser for vedlikeholdsjobbtype

I Aktivastyring kan du automatisk oppdatere eventuelle endringer i vedlikeholdsjobbtypeprognoser for timekostnader, varekost og utgifter som er oppdatert i andre moduler. På denne måten bidrar du til å sikre at prognosene for vedlikeholdsjobbtype alltid bruker de siste kostprisene.

1. Velg **Aktivastyring** \> **Periodisk** \> **Prognose** \> **Oppdater prognose for vedlikeholdsjobbtype**.
2. I dialogboksen **Oppdater prognose for vedlikeholdsjobbtype** i hurtigfanen **Poster som skal inkluderes** kan du legge til valg for bestemte vedlikeholdsjobbtyper etter behov. Velg **Filter**, og velg deretter **Velg** for å utføre valgene.
3. På hurtigfanen **Kjør i bakgrunnen** kan du definere den automatiske oppdateringen som en satsvis jobb, slik du ønsker.
4. Velg **OK** for å starte prognoseoppdateringen.

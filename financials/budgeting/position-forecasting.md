---
title: Stillingsprognoser
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 64413
ms.assetid: 35e791d2-1905-4808-a579-7f181ddddd91
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 1bc458d58834be1e2e9b602619f76424b3bb449b
ms.lasthandoff: 03/31/2017


---

# <a name="position-forecasting"></a>Stillingsprognoser

[!include[banner](../includes/banner.md)]




Utgifter som er knyttet til arbeidere utgjør ofte en stor del av organisasjonens kostnader. Stillingsprognoser lar deg planlegge disse utgiftene og inkludere dem i planleggingen av budsjetter.

## <a name="position-forecasting-in-budget-planning"></a>Stillingsprognoser i budsjettplanlegging

[![Grafikk, topp](./media/graphic-top.png)](./media/graphic-top.png) 

Stillingsprognoser bruker tre hovedkomponenter for å gi nøyaktige budsjettbeløp for stillingsutgifter. Disse beløpene kan deretter hentes inn i en budsjettplan for budsjettberegninger. 

Den primære komponenten er den **prognosestilling**, som representerer alle kostnadsdata som er knyttet til en enkelt stilling. Du kan opprette flere versjoner av en prognosestilling ved å tilordne et forskjellig budsjettplanscenario for hver versjon. Flere versjoner gir mulighet for en iterativ tilnærming til budsjettering og lar deg sammenligne hva-skjer-hvis-scenarioer. Hver prognosestilling har en tilsvarende stilling i Personale.

Et **budsjettkostnadselement** er en installasjonskomponent som representerer en bestemt kostnad som er knyttet til en stilling, for eksempel grunnlønn, sykeforsikring betalt av arbeidsgiver, mobiltelefongodtgjørelse og så videre. Et budsjettkostnadselement omfatter hovedkontoen som skal brukes for kostnaden og alternativer for beregning. Hvert budsjettkostnadselement kan tilordnes til flere prognosestillinger. 

En **kompensasjonsgruppe** er en valgfri installasjonskomponent som brukes til å bruke et sett med budsjettkostnadselementer og lønnsberegninger med stillinger som har lignende egenskaper for lønn. En kompensasjon-gruppe kan inneholde et kompensasjonsrutenett for lønnssatser. Når gruppen er tilordnet til en prognosestilling, kan et nivå og trinn i rutenettet tilordne prognosestillingens inntekter. Settet med kostnadselementer legges til automatisk.

### <a name="position-forecasting-processes"></a>Stillingsprognoseprosesser

[![Grafikk1b](./media/graphic1b.png)](./media/graphic1b.png) 

I en vanlig prosess for stillingsprognose, oppretter du først installasjonskomponentene (budsjettkostnadselementer og kompensasjonsgrupper). Prognosestillinger genereres deretter basert på eksisterende stillinger. Deretter kan du foreta justeringer. Du kan for eksempel legge til eller avslutte stillinger, endre lønnssatser og fordelskostnader og legge til lønnsøkninger. Du kan opprette flere versjoner av en prognosestilling for å muliggjøre sammenligninger mellom ulike budsjetteringsscenarioer. Deretter kan du inkludere prognosestillingene i budsjettplaner og sette inn kostnadene fra prognosestillingene som budsjettplanlinjer.

Du kan opprette flere prognosestillingsversjoner når budsjettplaner revideres. Disse nye versjonene danner grunnlag for endringene.

## <a name="position-forecasting-setup"></a>Oppsett av stillingsprognoser
[![Grafikk2](./media/graphic2-1024x327.png)](./media/graphic2.png)

### <a name="budget-cost-elements"></a>Budsjettkostnadselementer

Budsjettkostnadselementer brukes til å definere kostnadsdetaljer for en prognosestilling. Denne informasjonen inkluderer type kostnad, hvordan kostnad blir beregnet og om kostnadene skal fordeles på flere datoer når prognosestillingen er inkludert i en budsjettplan. 

Bestemte felt definerer virkemåten til budsjettkostnadselementet. Hvert budsjettkostnadselement tilordnes til budsjettkostnadstypen **Inntekt**, **Fordel**, **Avgifter** eller **Annet**. Budsjettkostnadstypene brukes primært til å beregne totaler. Verdien for **Overstyring av prognosestilling** angir om beløpene i elementet kan endres for prognosestillingen. Feltet **Tildelingsmetode** brukes når en prognosestilling legges til i en budsjettplan. Du kan dele kostnadsbeløpet over separate budsjettplanlinjer som har forskjellige datoer, på et grunnlag månedlig, kvartalsvis, ukentlig eller annenhver uke. Når du velger en startdato, tilordner du kostnadene som et enkelt beløp på startdatoen som er angitt i prognosestillingen. 

Beregningen av kostnadsbeløpet for budsjettkostnadselementet bruker gyldige datoer for å aktivere det samme kostnadselementet for bruk i forskjellige perioder. En enkelt hovedkonto tilordnes i hver periode, sammen med en prosent eller et årlig beløp som angir kostnadsbeløpet. Et budsjettkostnadselement kan bruke en prosent av andre kostnadselementer eller et årlig beløp, men ikke begge deler. Du kan også angi en årlig grense. 

Hvis kostnadselementet er basert på en prosentandel, må du angi budsjettkostnadselementer som skal brukes som grunnlag for beregningen.

**Eksempel** 

Jodis organisasjon tilbyr en opplæringsrabatten på 5 prosent av den ansattes grunnlønn. Jodi ønsker å opprette et budsjettkostnadselement for denne kostnaden. Hun oppretter et nytt budsjettkostnadselement og tilordner budsjettkostnadstypen **Fordel**.

Jodi vil ikke at prosjektledere skal endre beløpet for fordelen. Derfor velger hun **Ikke tillat kostnadsendringer** i feltet **Overstyring av prognosestilling**. Organisasjonen vil at denne kostnaden skal tilordnes jevnt til hver måned. Derfor velger Jodi **Kvartalsvis** i **Tildelingsmetode**-feltet. 

Deretter legger Jodi til en kostnadsberegningslinje, angir datoene og en hovedkontoen og angir **5,00** som prosent. Organisasjonen har et lokk på 5 000 i året for denne fordelen. Jodi angir derfor dette beløpet som årlig grense. 

Til slutt legger Jodi til alle inntjeningskostnadselementer som brukes for grunnlønn som beregningsgrunnlag. Hennes budsjettkostnadselement er nå klart til å brukes.

### <a name="compensation-groups"></a>Kompensasjonsgrupper

Kompensasjonsgrupper kan brukes til å gruppere prognosestillinger med liknende kompensasjonsattributter. De kan også brukes til å definere en prognosestillings inntekter og årlige økninger, og tilordne et sett med vanlige budsjettkostnadselementer. 

En grunnleggende funksjon for kompensasjonsgrupper er å tilordne et sett med budsjettkostnadselementer til en prognosestilling. Derfor kan kompensasjonsgrupper brukes til å legge til vanlige kostnader, for eksempel fordelsplaner og avgifter. En leder som oppretter en prognosestilling trenger ikke å vite alle kostnadselementer som må legges til. Kostnadselementer kan i stedet legges til når kompensasjonsgruppen blir valgt. Elementene blir lagt til i kompensasjonsgruppeoppsettet i **Budsjettkostnadselementer** kategorien. 

Kompensasjonsgrupper kan også bestemme inntektssatsene for en prognosestilling. Du kan definere en gruppe for å bruke enten en timebaserte basis eller et årlig lønnsgrunnlag for å beregne inntekter for prognosestillingen. I kategorien for **kompensasjonssatstabeller** angir et kompensasjonsrutenett for lønnssatser inntektene som legges til for en prognosestilling, basert på et tilordnet nivå og trinn. Disse rutenett kan være basert på eksisterende kompensasjonsrutenett i Personale. Du kan også opprette nye kompensasjonsrutenett for budsjettplanlegging. 

Gyldige datoer og utløpsdatoer for kompensasjonssatstabellene lar deg endre lønnssatser på en hvilken som helst dato. Denne funksjonen er nyttig når en forhandlingsenhet har forhandlet frem en gjennomgående økning i midten av en budsjettsyklus. I dette tilfellet må du endre utløpsdatoen for den eksisterende tabellen til dagen før datoen for satsendringen og legge til en ny satstabell som starter på den nye datoen. Når du oppretter en ny satstabell, hvis du velger **Opprett et nytt kompensasjonsrutenett fra et eksisterende rutenett**, kan du velge en eksisterende satstabell fra Personale. I satstabellen som er opprettet, lar alternativet **Masseendring** deg bruke en prosent eller et flatt beløp for å øke eller redusere alle satsene i rutenettet. 

Feltene **Tidsplan for økning** og **Dato for økning** i kompensasjonsgruppen brukes når du må opprette lønnsøkninger fordi stillinger går fra ett trinn til det neste. En årlig lønnsøkningen er et typisk scenario. Økningsplanen bestemmer om stillingens jubileumsdato eller en enkelt fellesdato skal brukes for trinnøkningen. Økningsplanen gjelder for alle prognosestillingene i kompensasjonsgruppen. 

Inntjeningskostnadselementet som er valgt for kompensasjonsgruppen, brukes når du oppretter inntekter for prognosestillingene i gruppen, inkludert grunnlønnen og eventuelle trinnøkninger. Feltet **Fast plan for kompensasjon** knytter kompensasjonsgruppen til en fast kompensasjonsplan i Personale. Denne koblingen kan tilordne en arbeiders informasjon om fast kompensasjon til en prognosestilling, og kan derfor gjøre budsjettplanlegging mer nøyaktig. Husk at strukturen for kompensasjonsrutenettet (nivåer og trinn) for kompensasjonsgruppen skal samsvare med strukturen i den faste kompensasjonsplanen. Ellers kan ikke systemet koble riktig kompensasjonsgruppe til den faste kompensasjonsplanen.

## <a name="creating-forecast-positions"></a>Opprette prognosestillinger
[![Grafikk3](./media/graphic3-1024x327.png)](./media/graphic3.png)

### <a name="creating-forecast-positions-for-existing-positions"></a>Opprette prognosestillinger for eksisterende stillinger

For den mest nøyaktige budsjettplanleggingen kan du opprette prognosestillinger ved å bruke detaljer fra eksisterende stillinger i Microsoft Dynamics 365 for Operations, uavhengig av om stillingen er besatt eller ikke besatt. 

Funksjonen **Legg til eksisterende stillinger** viser alle stillingene for en organisasjon. Ved å angi **Per** dato kan du endre listen over stillinger slik at den inneholder stillingene som fantes på en dato i fortiden eller, mer vanlig, i fremtiden (for eksempel begynnelsen av neste budsjettsyklus). Velg en budsjettplanleggingsprosess og et budsjettplanscenario, velg stillinger i listen, og klikk deretter **OK** for å opprette prognosestillingene for de valgte stillingene. Vær oppmerksom på at du kan opprette bare én prognosestilling for hver eksisterende stilling i en budsjettplanleggingsprosess og et budsjettplanscenario. Du kan imidlertid opprette flere versjoner ved å tilordne forskjellige budsjettplanscenarioer. 

Hvis budsjettkostnadselementer er knyttet til stillingen i Personale, tilordnes disse budsjettkostnadselementene også til prognosestillingen og bruker standardbeløpene. Feltet **Tilordnet arbeider** i prognosestillingen settes til navnet på arbeideren som er tilordnet til stillingen, hvis en arbeider er tilordnet. Dette feltet er et enkelt tekstfelt. Ingen direkte kobling opprettes. 

Hvis et budsjettkostnadselement er valgt, tilordnes det årlige beløpet for fast kompensasjon til prognosestillingen ved hjelp av det valgte kostnadselementet, forutsatt at den tilordnede arbeideren har en fast kompensasjonsplan. Hvis du ikke har en fast kompensasjonsplan, eller hvis ingen arbeider er tilordnet, brukes standardbeløpet for budsjettkostnadselementet. 

Når alternativet **Tilordne en kompensasjonsgruppe** er satt til **Ja**, hvis arbeideren som er tilordnet til stillingen har en trinn-basert fast kompensasjonsplan som er knyttet til en kompensasjonsgruppe (som beskrevet tidligere), tilordnes nivået og trinnet fra arbeideren til prognosestillingen, sammen med kompensasjonsgruppen. Kostnadselementet for inntektsbudsjett fra kompensasjonsgruppen blir lagt til i prognosestillingen, og lønnssatsen på nivået og trinnet fra kompensasjonsgruppen brukes. 

Innstillingen for alternativet **Tilordne en kompensasjonsgruppe** får prioritet over innstillingen for **tilordning av budsjettkostnadselement**. De to innstillingene kan brukes samtidig. 

[![Grafikk4](./media/graphic4.png)](./media/graphic4.png) 

Et annet alternativ er å tilordne en jubileumsdato. Den valgte datoen (justert startdato, arbeiderstartdato, startdato for ansettelse eller ansiennitetsdato) fra den tilordnede arbeideren settes deretter som prognosestillingens jubileumsdato og brukes til informasjon og når lønnsøkninger genereres.

### <a name="creating-new-forecast-positions"></a>Opprette nye prognosestillinger

Du kan opprette nye prognosestillinger på to måter: ved å kopiere en eksisterende prognosestilling og ved å opprette en helt ny prognosestilling. 

Når det velges en prognosestilling, velger du **Kopier den valgte prognosestillingen** for å opprette en ny prognosestilling som har prognosetilstanden **Foreslått**. Denne prognosestillingen har alle de samme dataene som prognosestillingen som ble kopiert, bortsett fra den tilordnede arbeideren og eventuelle merknader om budsjettkostnadselementene. Legg merke til at det opprettes også en tilsvarende ny stilling i Personale. Denne stillingen har beskrivelsen **Opprettet etter prognose**. 

Du kan også opprette en helt ny prognosestilling. Velg en eksisterende jobb, og velg også budsjettplanleggingsprosessen og budsjettplanscenarioet. Du kan deretter legge til en hvilken som helst annen informasjon som du vil legge til. Igjen opprettes en ny stilling i Personale samtidig.

## <a name="working-with-forecast-positions"></a>Arbeide med prognosestillinger
[![Grafikk5](./media/graphic5-1024x327.png)](./media/graphic5.png)

### <a name="multiple-versions-of-a-forecast-position"></a>Flere versjoner av en prognosestilling

Du kan endre prognosestillingene enten for å ta i bruk kjente endringer for budsjettsyklusen eller modellere foreslåtte endringer. En vanlig metode er å opprette et grunnleggende sett for prognosestillinger, opprette kopier av disse prognosestillingene, og deretter bruke kopiene for å modellere ulike endringer. Kopiene tilordnes til et annet budsjettplanscenario, men er, i hvert fall før det gjøres endringer, ellers identiske med prognosestillingene som de kopieres fra. Originalene og kopiene deler samme stilling i Personale. 

Funksjonen **Kopier til scenario** gir denne funksjonaliteten. Legg merke til at hver stilling i Personale kan ha bare én prognosestilling i hvert budsjettplanscenario.

### <a name="modifying-forecast-positions"></a>Endre prognosestillinger

Endringer som gjøres med prognosestillinger, er begrenset til disse prognosestillingene. Endringene påvirker ikke stillingspostene i Personale. De fleste endringene er også begrenset til prognosestillingen som blir redigert. Med andre ord er endringene spesifikke for budsjettplanleggingsprosessen og budsjettplanscenarioet som tilordnes. Unntaket er endringer av felt som deles for stillingen på tvers av prosesser og scenarier. Disse feltene inkluderer feltene i **Generelt** kategorien og **Finansdimensjoner** kategorien. Når disse feltene endres, vil de nye verdiene gjelde for stillingen i alle scenarier for budsjettplanlegging. Derfor lar disse feltene deg raskt oppdatere alle versjoner.

#### <a name="budget-cost-elements"></a>Budsjettkostnadselementer

Budsjettkostnadselementer gir den viktigste informasjonen for budsjettplaner: budsjettbeløpet og hovedkontoen. Budsjettbeløpet er beløpet som sendes til budsjettplanen når en prognosestilling er inkludert i en plan. Budsjettbeløpet beregnes og kan ikke endres direkte. Dette beløpet er det årlige beløpet eller en beregning av prosenten av det årlige beløpets grunnlagselementer (som definert i oppsettet av budsjettkostnadselementet). Beløpet beregnes deretter basert på antall dager i elementets datointervall (startdato til sluttdato) og etter verdien for **fulltidsekvivalens** (FTE) for prognosestillingen. 

En budsjettkostnadselementlinje fra 1. januar 2017 til 30. juni 2017, med et årlig beløp på 100 000 og en FTE-verdi på **0,50** beregnes for eksempel som 100 000 × (181 dager ÷ 365 dager) × 0,50 = 24 794,52. 

Budsjettkostnadselementlinjene må omberegnes når FTE-verdien endres for prognosestillingen. Linjene må også omberegnes når datoene for aktivering eller pensjonsavgang endres. Endringer av disse datoene kan føre til en oppdatering av startdato og sluttdato for budsjettkostnadselementet, som må være innenfor datoene for prognosestillingen. Når omberegningen kreves, blir **Omberegn**-knappen tilgjengelig, og meldingen "Krever beregning" vises. Omberegningen er også nødvendig hvis du legger til eller fjerner et budsjettkostnadselement.

**Eksempel** 

Organisasjonen vurderer to alternativer for å redusere kostnadene for en regnskapsførerstilling. Ett alternativ er å avslutte stillingen delvis gjennom året. Det andre alternativet er å endre stillingen til halvtid for hele året. Brad har opprettet en prognosestilling for den eksisterende regnskapsførerstillingen i et grunnscenario. Han kopierer denne grunnleggende prognosestillingen til scenario A, angir avgangsdatoen til 31. mai og beregner på nytt. Brad overfører deretter den grunnleggende prognosestillingen til scenario B, endrer FTE-verdien til **0,50**, og beregner på nytt. Brad har nå tre versjoner, der hver har kostnadstotaler som er justert etter alternativene.

#### <a name="assigning-a-compensation-group"></a>Tilordne en kompensasjonsgruppe

Når du først tilordner en kompensasjonsgruppe til en prognosestilling, legges standard budsjettkostnadselementene kompensasjonsgruppen til. Hvis kostnadselementer allerede er tilordnet til prognosestillingen, beholdes disse kostnadselementene. Hvis en kompensasjonsgruppe allerede er tilordnet og endres, fjernes de eksisterende budsjettkostnadselementene og erstattes av settet fra kompensasjonsgruppen. 

Når du velger et kompensasjonsnivå og -trinn, legges det til et kostnadselement for inntektsbudsjett (som definert i kompensasjonsgruppen). Det årlige beløpet beregnes ved å bruke satsen i det valgte nivået og trinnet, og de årlige timene i kompensasjonsgruppen (eller for en årlig basert lønn, hele beløpet i nivået og trinnet). Igjen beregnes dette beløpet etter kostnadselementlinjens datointervall og prognosestillingens FTE-verdi.

#### <a name="generating-increases"></a>Generere økninger

Årlig økninger (én per kalenderår) kan opprettes automatisk for prognosestillinger som har en trinnbasert kompensasjonsgruppe tilordnet. Klikk **Generer økninger** for å legge til et kostnadselement for inntektsbudsjett på det nest høyeste trinnet. Startdatoen for det nye kostnadselementet for inntektsbudsjett er den planlagte økningsdatoen som vises på prognosestillingen. Denne datoen angis fra kompensasjonsgruppen på én av to måter. Hvis tidsplanen for kompensasjonsgruppens økning settes til **Fellesdato**, angis datoen for økning på kompensasjonsgruppen. Hvis tidsplanen for økning settes til **Jubileumsdato**, brukes jubileumsdatofeltet på prognosestillingen, og budsjettsyklusen forsyner året. Hvis det finnes flere kalenderår i en budsjettsyklus, legges det til flere økninger. 

Sluttdatoen for gjeldende kostnadselement for inntektsbudsjett oppdateres med dagen før økningsdatoen. Omberegningsprosessen brukes automatisk når økninger genereres. Derfor trenger du ikke å omberegne manuelt. 

Hvis du klikker **Generer økninger** en gang til, kjøres prosessen på nytt, men den legger ikke til flere poster. Det opprettes bare én økning per kalenderår.

#### <a name="changes-from-other-pages"></a>Endringer fra andre sider

Oppdateringer av prognosestillinger kan også komme fra andre områder, for eksempel konfigurasjonssidene for budsjettkostnadselementet og kompensasjonsgruppen. Du kan også endre prognosestillingene ved hjelp av masseoppdateringsprosessen. 

To alternativer er tilgjengelige på konfigurasjonssiden **Budsjettkostnadselement**: **Legg til stillinger** og **Oppdater stillinger**. Alternativet **Legg til stillinger** legger til budsjettkostnadselementet i valgte prognosestillinger. Hvis elementet allerede er tilordnet til en prognosestilling, hoppes det over denne prognosestillingen. Alternativet **Oppdater stillinger** tar i bruk de gjeldende verdiene (hovedkontoen, prosent, Årlig beløp og så videre) for den valgte prognosestillingen. 

Hver prosess har en lignende side der du kan velge prognosestillingene. Siden **Legg til stillinger** viser alle prognosestillinger som er tilgjengelige for valg, mens siden **Oppdater stillinger** viser bare de prognosestillingene som allerede er tilordnet budsjettkostnadselementet. (Derfor gir siden **Oppdater stillinger** deg en metode for å finne ut hvilke prognosestillinger som allerede har kostnadselementet tilknyttet.) Du kan flytte prognosestillingene fra et øvre rutenett til et lavere rutenett for å inkludere dem i oppdateringen. 

Legg merke til at funksjonen **Endre datoer** i kategorien **Kostnadsberegning** umiddelbart endrer budsjettkostnadselements startdato og sluttdato på prognosestillingene. Ingen alternativer for valg er tilgjengelige. 

På siden **Kompensasjonsgruppe** tar funksjonen for **oppdatering av stillingssatser** i bruk gjeldende satser fra kompensasjonssatstabellen for prognosestillinger som er tilordnet til gruppen. Satsene blir oppdatert, og flere kostnadselementlinjer blir lagt til for nye satstabellinjer (basert på datoer). Budsjettkostnadselementene og økningsdatoene blir imidlertid ikke er oppdatert. Du kan velge hvilken budsjettplanleggingsprosess og hvilket budsjettplanscenario som skal oppdateres. Derfor kan du oppdatere ett scenario, men la andre scenarier være uendret for sammenligning. 

Ved å velge prognosestillingene og deretter klikke **Masseoppdatering** kan du legge til eller endre mer enn én prognosestilling samtidig. Mange alternativer er tilgjengelig. Ett alternativ i kategorien **Finansdimensjoner** er litt annerledes enn de andre og er knyttet til budsjettkostnadselementer. Du kan legge til budsjettkostnadselementer ved å angi alternativet **Budsjettstandarder** som **Ja**. Hvis ingen budsjettkostnadselementer er valgt, men **Budsjettstandarder** er satt til **Ja**, fjernes alle budsjettkostnadselementer som er tilordnet for øyeblikket. 

Omberegningsprosessen brukes automatisk på alle prognosestillinger som endres.

## <a name="bringing-forecast-positions-into-budget-plans"></a>Overføre prognosestillinger til budsjettplaner

[![Grafikk6](./media/graphic6-1024x327.png)](./media/graphic6.png)

Formålet med å opprette og endre prognosestillingene er å legge dem til i budsjettplaner, slik at budsjettplanene omfatter de mest nøyaktige budsjettbeløpene. Det finnes to metoder for å legge til prognosestillingene i budsjettplaner. Du kan bruke enten en genereringsprosess eller en utvelgelsesprosess for budsjettplanen.

### <a name="generating-a-budget-plan-from-forecast-positions"></a>Generere en budsjettplan fra prognosestillinger

Funksjonen **Generer budsjettplan fra prognosestillinger** oppretter eller oppdaterer budsjettplaner slik at de har budsjettbeløpene og FTE-antallene fra prognosestillinger. Budsjettbeløpene fra prognosestillingen blir budsjettplanlinjebeløp og samles etter finansdimensjonsverdier og gyldighetsdato. Genereringsprosessen tilordner kildeprognosestillingen til budsjettplanlinjen. Hvis du vil vise stillingen, kan du enten legge til prognosestillingen som en rad i budsjettplanoppsettet eller bruke forespørselen **Budsjettplanlinjer**. Hvis du vil hoppe over denne tilordningen, kan du angi alternativet **Inkluder stilling i budsjettplanlinje** som **Nei**. 

Du kan velge en FTE-scenario for budsjettplan for å inkludere antallet heltidsansatte i budsjettplanen. Du kan velge bare scenarier av antallstypen som er inkludert i oppsettet for målbudsjettplanen. Når du velger et FTE-scenario, må du også angi en FTE-hovedkonto. Denne kontoen brukes til å opprette budsjettplanlinjene for antall. 

Budsjettplanleggingsprosessen og budsjettplanscenarioet som er valgt i kilden, bestemmer budsjettplanleggingsprosessen og budsjettplanscenarioet for målscenarioet. Fordi disse attributtene er tilordnet til prognosestillinger må de være synkronisert med budsjettplanen. Attributtene kan derfor ikke redigeres på målet. 

Som for andre prosesser for generering finnes det tre alternativer:

-   **Opprett en ny budsjettplan** – Opprett en ny plan som har attributtene som er valgt i **Mål**-delen.
-   **Erstatt eksisterende budsjettplanscenario** – Slett alle data i målbudsjettplanen i det valgte budsjettplanscenarioet og opprett nye linjer som inneholder dataene for den valgte prognosestillingen.
-   **Oppdater eksisterende budsjettplanscenario, og tilføy nye data** – Oppdater eksisterende linjer i målplanen som samsvarer med kildelinjene, og legg også til nye linjer for nye data. Samsvar er basert på finanskontoen, dato, budsjettklasse og andre verdier, for eksempel prognosestillingen. Alle linjer som har et stillingsnummer som samsvarer med kildestillingsnummeret, erstattes med de nye linjene fra kilden.

### <a name="selecting-forecast-positions"></a>Velge prognosestillinger

Du kan også legge budsjettbeløp for prognosestilling direkte i en budsjettplan. Bruk funksjonen **Legg til stillinger** over budsjettplanlinjene for å velge prognosestillingene som skal tas med. 

Budsjettplanscenarioene som du kan velge som kilde, er begrenset til scenariene som er inkludert i planens oppsett. Ett alternativ i kategorien **Mål** lar deg angi at FTE-scenarioet og hovedkontoen er tilgjengelige for å inkludere FTE-antall, men er ikke nødvendige. 

Denne utvelgelsesprosessen fungerer som alternativet **Oppdater eksisterende budsjettplanscenario, og tilføy nye data** for en prosess for generering. Alle eksisterende budsjettplanlinjer der prognosestillingen legges til, fjernes og erstattes med nye linjer som er basert på gjeldende status for prognosestillingen.

#### <a name="date-options"></a>Datoalternativer

For både genereringsprosessen og valgprosessen bestemmer startdatoen for budsjettkostnadselementlinjen den gyldige datoen for den tilsvarende budsjettplanlinjen. Feltet **Tildelingsmetode** på siden for konfigurasjon av budsjettkostnadselement angir tildelingsmetoden:

-   **Startdato** – Startdatoen for budsjettkostnadselementet brukes som gyldighetsdato for budsjettplanlinjen.
-   **Månedlig** – Budsjettbeløpet deles likt etter antall måneder i datoområdet for å produsere et vanlig månedlig beløp som tilordnes på den første dagen i hver måned. Hvis den første perioden er en delvis måned, beregnes beløpet for denne måneden etter antall dager kostnaden er aktiv i denne måneden, og resultatet tilordnes til startdatoen. Beløpet for den siste måneden er forskjellen mellom det totale budsjettbeløpet og summen av alle andre måneder. Derfor kan avrunding påvirke beløpet for den siste måneden.
-   **Kvartalsvis** – Denne metoden er den samme som **Månedlig**, men beregningene utføres for tremånedersperioder.
-   **Ukentlig** – Logikken ligner på logikken i metodene **Månedlig** og **Kvartalsvis**. Budsjettbeløpet deles likt etter antall uker i datoområdet for å produsere et vanlig ukentlig beløp som tilordnes på den første dagen i hver uke. Hvis den første perioden er en delvis uke, beregnes beløpet for denne uken etter antall dager kostnaden er aktiv i denne uken, og resultatet tilordnes til startdatoen. Beløpet for den siste uken er forskjellen mellom det totale budsjettbeløpet og summen av alle andre uker. Derfor kan avrunding påvirke beløpet for den siste uken.
-   **Annenhver uke** – Denne metoden er den samme som **Ukentlig**, men beregningene utføres for toukersperioder.

#### <a name="changing-budget-plan-lines-that-have-forecast-positions"></a>Endre budsjettplanlinjer som har prognosestillinger

Budsjettplanlinjer viser kilden til budsjettbeløpene (prognosestillingsnummeret), men er ikke koblet. Derfor vises ikke endringer i prognosestillingen på budsjettplanlinjen, og endringer i budsjettplanlinjen vises i prognosestillingen. Hvis du endrer en prognosestilling og vil at oppdateringene skal inkluderes i en budsjettplan, må du overføre prognosestillingen til planen på nytt. Husk imidlertid at denne prosessen fjerner alle linjer der denne prognosestillingen er tilordnet. Eventuelle endringer du har gjort i disse linjene fjernes derfor. 

For å se hvilke budsjettplaner en prognosestilling er inkludert i kan du generere rapporten **Prognosestillinger etter budsjettplan**. Alternativt kan du på prognosestillingen åpne faktaboksen **Tilknyttede budsjettplaner** for å vise planene.





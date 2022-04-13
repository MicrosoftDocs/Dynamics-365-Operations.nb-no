---
title: Opprett faktureringsplaner
description: Dette emnet forklarer hvordan du oppretter, sletter og redigerer faktureringsplaner.
author: JodiChristiansen
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 2c4e3c0edadd00fd3a3f2ae9968248a226147996
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462594"
---
# <a name="create-billing-schedules"></a>Opprett faktureringsplaner

[!include [banner](../includes/banner.md)]

Du kan opprette, slette eller redigere faktureringsplaner på siden **Faktureringsplan**. Du kan også gå gjennom listen over faktureringsplaner. Når du oppretter en faktureringsplan, fastsettes standardverdiene for den av faktureringsgruppen som er knyttet til den. Du definerer tilleggsinformasjon på siden **Parametere for gjentakende kontraktfakturering**.

## <a name="create-a-billing-schedule"></a>Opprette en faktureringsplan

Hvis du vil opprette en faktureringsplan, følger du trinnene nedenfor.

1. Velg **Ny** på siden **Faktureringsplan**.
2. Velg en faktureringsplangruppe i feltet **Opprett faktureringsplangruppe** i dialogboksen **Opprett faktureringsplan**.
3. Velg en kundekonto i **Kundekonto**-feltet.
4. I **Startdato**-feltet velger du startdatoen, og deretter angir du antall perioder i **Antall perioder**-feltet. **Sluttdato**-feltet oppdateres basert på antall perioder du angir. Hvis du oppdaterer feltet **Sluttdato for fakturering**, oppdateres **Antall perioder**-feltet til **0** (null).
5. Velg **OK**.
6. Angi en beskrivelse av faktureringsplanen i **Beskrivelse**-feltet i **Generelt**-fanen på **Faktureringsplan**-siden.
7. Velg en milepælmal for **Milepælfakturering** i **Milepælmal**-feltet.

Felter som **Fakturakonto** og **Valutakode** oppdateres med informasjon fra kunden.

Feltene **Faktureringsfrekvens** og **Faktureringsintervall** angis automatisk basert på den valgte faktureringsplangruppen.

8. Angi **Ja** for alternativet **Fakturer separat** hvis du vil opprette separate fakturaer.
9. Velg **Ja** for alternativet **Forny automatisk**, og velg deretter feltet **Linjer som skal legges til per fornyelse** for å fornye en faktureringsplan automatisk etter den endelige faktureringsperioden.

**Parametere**-feltene angis automatisk basert på verdiene på siden **Parametere for gjentakende kontraktfakturering**.

10. Hvis du vil fordele beløpet i en faktureringsplan, angir du **Ja** for **Fordel på delvise perioder**.
11. Hvis du vil tilpasse detaljlinjene for faktureringsplan til slutten av en måned, angir du **Ja** for **Tilpass til måned**.
12. I feltene **Startdato for kontrakt** og **Sluttdato for kontrakt** angir du start- og sluttdatoen for kontrakten. Disse datoene er bare til informasjon.

**Betaling**-feltet viser informasjon om kundebetaling fra kunden. Når en linjevare er på vent eller avsluttet, kan ikke betalingsinformasjonen endres.

> [!NOTE]
> Når du konsoliderer fakturaer etter vare, må verdien i feltene **Betalingsbetingelser**, **Metode** og **Faktureringsplan** samsvare. Ellers kan ikke fakturaene konsolideres.

13. I **Adresse**-fanen kan du gå gjennom og oppdatere feltene **Leveringsadresse** og **Fakturer til-adresse**.
14. I fanen **Kontaktinformasjon** kan du knytte en sluttbrukerkonto til faktureringsplanen.
15. I feltene **Kontaktinformasjon** kan du angi en kontakt, e-postadresse og Internett-adresse.
16. Hvis du vil spore informasjon om partnerprovisjon, angir du feltene **Partnerkonto** og **Provisjonssats for partner**. Disse feltene er bare til informasjon.
17. I **Total**-fanen kan du vise de ulike totalene som er beregnet for faktureringsplanen.
18. I **Vent**-fanen kan du vise revisjonsinformasjon om når faktureringsplanen ble satt på vent, da venting ble avsluttet.
19. I **Avslutning**-fanen kan du vise en logg over avslutningene som ble brukt på eller fjernet fra faktureringsplanen.
20. Velg **Lagre**.
21. I hurtigfanen **Faktureringsplanlinjer** velger du **Legg til linje**.
22. I feltet **Varenummer** velger du varenummeret. Hvis varen som legges til, er en overordnet vare i en inntektsdeling, oppdateres linjene automatisk med de underordnede varene. Du kan bare redigere den overordnede varen i en inntektsdeling. Alle underordnede varer blir deretter tilsvarende oppdatert.
23. I feltet **Varetype** velger du varetypen.
24. Oppdater start- og sluttdatoen.
25. Du kan endre faktureringsfrekvensen før fakturaene opprettes, ved å oppdatere feltet **Faktureringsfrekvens**. Etter at den første fakturaen for faktureringsplanen er opprettet, kan ikke faktureringsfrekvensen endres.
26. I **Enhet**-feltet velger du måleenheten for varen.
27. Velg prissettingsmetoden for varen i feltet **Prissettingsmetode**.

**Enhetspris**-feltet angis automatisk fra lageret. Du kan imidlertid oppdatere den hvis du endrer prissettingsmetoden til **Flat**.

## <a name="remove-a-line-item"></a>Fjerne en linjevare

Følg denne fremgangsmåten hvis du vil fjerne en vare fra en faktureringsplan.

1. Velg nummeret på faktureringsplanen du vil redigere, i feltet **Tidsplannummer** på siden **Faktureringsplan**.
2. Velg linjen du vil slette, i hurtigfanen **Faktureringsplanlinjer**, og velg deretter **Fjern**.
3. Velg **Lagre**.

Resten av dette emnet beskriver handlingene og detaljene som er tilgjengelige for linjer i hurtigfanen **Faktureringsplanlinjer**.

## <a name="billing-schedule-line-actions"></a>Handlinger for faktureringsplanlinjer

Med knappene i hurtigfanen **Faktureringsplanlinjer** kan du bruke handlinger på enkeltlinjer.

| Knapp | Beskrivelse |
|--------|-------------|
| Legg til linje | Legg til en linje i faktureringsplanen. |
| Legg til fra vareliste | Legg til flere varer i en faktureringsplan ved å velge dem i en liste. |
| Fjern | <p>Fjern den valgte linjen fra faktureringsplanen.</p><p>Når det gjelder varer som er del av en inntektsdeling, kan du bare fjerne den overordnede varen. Alle tilknyttede underordnede varer blir deretter fjernet automatisk.</p> |
| Vis faktureringsdetaljer | Vis faktureringsdetaljene. |
| Avslutt | <p>Avslutt de valgte linjene. Denne knappen er bare tilgjengelig når de valgte linjene har statusen **Aktiv**.</p><p>Når det gjelder varer som er del av en inntektsdeling, kan du bare avslutte den overordnede varen.</p> |
| Fjern avslutning | <p>Fjern avslutningen fra de valgte linjene. Denne knappen er bare tilgjengelig når de valgte linjene har statusen **Avsluttet**.</p><p>Når det gjelder varer som er del av en inntektsdeling, kan du bare fjerne avslutningen fra den overordnede varen.</p> |
| Sett på vent | <p>Velg detaljene for å sette den valgte linjen på vent.</p><p>Når det gjelder varer som er del av en inntektsdeling, kan du bare sette den overordnede varen på vent.</p> |
| Avslutt venting | <p>Avslutt ventingen for den valgte linjen.</p><p>Når det gjelder varer som er del av en inntektsdeling, kan du bare avslutte ventingen for den overordnede varen.</p> |
| Videresending og rabatt | Denne knappen er ikke tilgjengelig for varer som er del av en inntektsdeling, unntatt overordnede varer der inntektsdelingen bruker tildelingsmetoden **Nullbeløp**. |
| Henvisninger | <p>Angi henvisningsalternativer for den valgte linjen.</p><p>Denne knappen er ikke tilgjengelig for overordnede varer i en inntektsdeling.</p> |
| Milepæltildeling | <p>Gå gjennom og oppdater informasjonen om milepæltildeling for den valgte linjen.</p><p>Denne knappen er bare tilgjengelig når varen på faktureringsplanlinjen er en milepælvare.</p> |
| Støtte og fornying | <p>Gå gjennom og oppdater informasjonen om støtte og fornyelse for den valgte linjen.</p><p>Denne knappen er bare tilgjengelig når varen på faktureringsplanlinjen er en støtte- eller fornyelsesvare.</p> |
| Visningsdimensjoner | Vis eller skjul dimensjonskolonnene som vises i rutenettet **Faktureringsplanlinjer**. |
| Beregn enhetspris | <p>Beregn enhetsprisen på varen, slik at kunden kan betale kontraktbeløpet i avdrag (for eksempel daglig, månedlig, kvartalsvis, halvårig eller årlig). Du kan velge kontraktpris og prisfrekvens.</p><p>Du kan vise et revisjonsspor for endringene: den gamle kontraktprisen og -frekvensen, den nye kontraktprisen og -frekvensen, brukeren som gjorde endringen, og datoen og klokkeslettet for endringen.</p> |
| Justeringsdato | <p>Angi justeringsdatoen for fornyelsesvarer.</p><p>Hvis du velger en varegruppe i **Varegruppe**-feltet, bruker alle varer justeringsdatoen for den første varen i varegruppen i faktureringsplanen. Hvis **Varegruppe**-feltet er tomt, kan du angi en justeringsdato som skal brukes for alle varer.</p><p>Denne knappen er bare tilgjengelig når **Årlig** er angitt for feltet **Faktureringsfrekvens**.</p> |
| Ufakturert inntekt | <p>Angi at varen skal bruke funksjonen for ufakturert inntekt. Du kan deretter angi ufakturert inntekt og ufakturerte rabattkontoer for varen.</p><p>Denne knappen er bare tilgjengelig for varer der **Standard** er angitt for **Varetype**-feltet. Den er ikke tilgjengelig for eksisterende faktureringsplaner eller faktureringsplanlinjer der fakturaen allerede er opprettet.</p> |
| Legg til underordnet inntektsdeling | <p>Velg en underordnet vare som skal legges til salgsordren.</p><p>Denne knappen er bare tilgjengelig for overordnede varer i en inntektsdeling.</p> |
| Alternativer for avanserte prissetting | Rediger alternativene for prissetting for en vare. |

## <a name="billing-schedule-line-details"></a>Detaljer for faktureringsplanlinjer

Når du velger en linje i hurtigfanen **Faktureringsplanlinjer**, kan du vise bestemte detaljer for denne linjen. Disse detaljene er fordelt på ulike faner.

### <a name="general-tab"></a>Fanen Generelt

Følgende informasjon er tilgjengelig i **Generelt**-fanen.

| Felt eller del | Beskrivelse |
|------------------|-------------|
| Bruk | <p>Denne delen inneholder informasjon om bruksvarer. Den inneholder følgende felter:</p><ul><li>**Bruksidentifikator** – identifikatoren for måleren eller bruksvaren.</li><li>**Alternativ for lesing** – alternativet for brukslesing: **Lesing** eller **Forbruk**.</li><li>**Estimert forbruk** – Angi det estimerte forbruket for en bruksvare som har perioder der fakturaen ikke er opprettet. På siden **Faktureringsdetaljer** kan du se gjennom faktureringsdetaljlinjene for estimert forbruk.</li></ul> |
| Eksterne referanser\* | Denne delen inneholder feltene **Ekstern** og **Linjenummer**, der du kan angi ekstern referanseinformasjon. |
| Milepæl | <p>Denne delen inneholder informasjon om milepælvarer. Den inneholder feltet **Estimert fullføringsdato**, som viser fullføringsdatoen for varen.</li></ul> |
| Tekst | En kommentar for linjen. Teksten oversettes til standardspråket for kunden eller den juridiske enheten. |
| Varegruppe | Varegruppen for linjevaren. |
| Justeringsdato | Justeringsdatoen for faktureringsplanen. |

\* Når du konsoliderer fakturaer etter vare på siden **Generer faktura**, må feltene **Ekstern referanse** samsvare. Hvis selv ett tegn er forskjellig, blir ikke varene konsolidert på fakturaen. Det blir ikke utført valideringskontroll av noen av feltene i delen **Ekstern referanse**, og verdien i **Linjenummer**-feltet må være et positivt heltall.

### <a name="address-tab"></a>Adresse-fanen

Følgende informasjon er tilgjengelig i **Adresse**-fanen.

| Felt | Beskrivelse |
|-------|-------------|
| Leveringsadresse | <p>Velg leveringsadressen for linjevaren. Standard leveringsadresse er den primære leveringsadressen i hurtigfanen **Adresse**.</p><p>Når du endrer adressen, kan du velge følgende adressealternativer:</p><ul><li>**Adresser** – Velg en adresse for den gjeldende kunden.</li><li>**I bruk** – Velg en adresse som for øyeblikket brukes for den gjeldende kunden.</li><li>**Annen adresse** – Velg en adresse for en hvilken som helst kundepost.</li></ul><p>Når det gjelder varer som bruker inntektsdeling, kan bare adressen for den overordnede varen redigeres. Adressen til de underordnede varene samsvarer med adressen til den overordnede og kan ikke redigeres separat.</p> |
| Fakturer til-adresse | <p>Velg fakturer til-adressen for linjevaren. Standard leveringsadresse er den primære leveringsadressen i hurtigfanen **Adresse**. Du kan endre adressen etter behov, basert på formålet med de tilgjengelige adressene:</p><ul><li>Hvis ingen av adressene har formålet **Faktura**, er standard fakturer til-adresse primæradressen til kunden, uansett formål.</li><li>Hvis én eller flere av adressene har formålet **Faktura**, er standard fakturer til-adressen den samme adressen som ble angitt forrige gang.</li><li>Hvis en eller flere av adressene har formålet **Faktura**, og en av fakturaadressene er angitt som primæradresse, er standard fakturer til-adressen adressen som har formålet **Faktura** og er angitt som primæradresse.</li><li>Når det gjelder varer som bruker inntektsdeling, kan bare adressen for den overordnede varen redigeres. Adressen til de underordnede varene samsvarer med adressen til den overordnede og kan ikke redigeres separat.</li></ul> |

### <a name="product-tab"></a>Produkt-fane

Følgende informasjon er tilgjengelig i **Produkt**-fanen.

| Felt eller del | Beskrivelse |
|------------------|-------------|
| Lagringsdimensjoner | <p>Denne delen viser lagringsinformasjon for varen. Den inneholder **Serienummer**-feltet, som viser serienummeret for varen.</p><p>Serienummeret kopieres fra den opprinnelige salgsordren under støtte- og fornyelsesprosessen. Når det gjelder varer som bruker inntektsdeling, kopieres serienummeret for den overordnede varen til alle underordnede varer. Serienummeret kopieres når **Ja** er angitt for alternativet **Kopier serienummer** på siden **Parametere for gjentakende kontraktfakturering**.</li></ul> |
| Produktdimensjoner | Produktdetaljene for varen og verdiene oppdateres automatisk basert på **Variantnummer**-verdien som er valgt for faktureringsplanlinjen. |

### <a name="account-tab"></a>Konto-fanen

Følgende informasjon er tilgjengelig i **Konto**-fanen.

| Felt | Beskrivelse |
|-------|-------------|
| Hovedkonto | Hovedkontoen som opprettes på salgslinjen. Standardverdien kommer fra salgsordren. Dette feltet kan være tomt. |
| Finansdimensjoner for vare | <p>Standard finansdimensjonsverdier basert på kunde- og vareposten.</p><p>Når det gjelder varer som bruker inntektsdeling, bruker de underordnede varene finansdimensjonsverdiene for kunde- og varepostene, som beskrevet tidligere. Hvis du må oppdatere finansdimensjonsverdiene for underordnede varer, kan du importere dataenheten.</p> |

### <a name="renewals-tab"></a>Fornyelser-fanen

Følgende informasjon er tilgjengelig i **Fornyelser**-fanen.

| Felt | Beskrivelse |
|-------|-------------|
| Forny automatisk | <p>En verdi som angir om faktureringsplanlinjen fornyes automatisk for den neste faktureringsperioden:</p><ul><li>**Ja** – Faktureringsplanlinjen fornyes automatisk for den neste faktureringsperioden når du oppretter en faktura.</li><li>**Nei** – Faktureringsplanlinjen fornyes ikke automatisk. Du må fornye faktureringsplanen manuelt.</li></ul> |
| Linjer som skal legges til per fornying | Antall linjer som skal legges til i en fornyelse av faktureringsplan. |

Følgende knapper er også tilgjengelige i **Fornyelser**-fanen.

| Knapp | Beskrivelse |
|--------|-------------|
| Revisjon av journaloppføring som ikke er fakturert | Vis alle endringer for varer som bruker funksjonen for ufakturert inntekt. |
| Legg til fornyingsperiode | Legg til en fornyelsesperiode for varen. Startdatoen for den nye fornyelsesperioden er neste dato etter sluttdatoen for forrige periode. Du kan oppdatere feltene **Sluttdato for fornyelse**, **Startdato for henvisning**, **Sluttdato for henvisning**, **Vareantall** og **Enhetspris**. |
| Endre fornyingsperiode | <p>Endre en fornyelsesperiode. Når det gjelder den første perioden, kan du endre start- og sluttdatoen for henvisning før den første journaloppføringen opprettes. Når det gjelder etterfølgende perioder, kan ikke startdatoen endres. Den er alltid neste dato etter slutten av forrige periode.</p><p>Hvis det finnes en fornyelsesperiode etter perioden du endrer, kan ikke datoene for perioden endres. I dette tilfellet er det bare feltene **Antall** og **Enhetspris** for fornyelsesvaren som kan oppdateres.</p><p>La oss si at det for eksempel finnes tre perioder. <ul><li>Den første perioden kan ikke endres, fordi den allerede er startet.</li><li>Når det gjelder den andre perioden, er det bare antallet og enhetsprisen som kan endres.</li><li>Når det gjelder den tredje perioden, kan alle verdier unntatt startdatoen endres. Du kan i tillegg bruke alternativet **Planlegg fra mal** til å opprette en henvisningsplan som er basert på malen for den ufakturerte inntektsvaren. Når **Ja** er angitt for dette alternativet, velger du henvisningsmalen i **Mal**-feltet og endrer start- og sluttdatoen for henvisning etter behov. Etterfølgende fornyelsesperioder bruker samme henvisningsmal. Henvisningsmalen kan imidlertid endres.</p></li></ul> |

### <a name="termination-tab"></a>Avslutning-fanen

Følgende informasjon er tilgjengelig i **Avslutning**-fanen.

| Felt | Beskrivelse |
|-------|-------------|
| Avslutningsdato | Datoen faktureringsplanlinjen avsluttes. Standardverdien kommer fra **Avslutningsdato**-feltet i hodet. Du kan endre verdien etter behov. |
| Avslutningstype | Avslutningstypen. Standardverdien kommer fra **Avslutningstype**-feltet i hodet. |

### <a name="hold-tab"></a>Vent-fanen

Hvis inntekts- og utgiftshenvisninger brukes, vises henvisningsdatoen i **Vent**-fanen.

### <a name="escalation-and-discount-tab"></a>Fanen Eskalering og rabatt

Følgende informasjon er tilgjengelig i fanen **Eskalering og rabatt**.

| Felt | Beskrivelse |
|-------|-------------|
| Eskalering | <p>Velg om eskaleringer skal være tillatt for faktureringsplanlinjen. Alle eskaleringslinjer fra hodet brukes når faktureringsplanlinjen opprettes.</p><ul><li>**Ja** – Eskaleringer kan brukes på linjen. Når dette alternativet er valgt, kan du definere eskaleringene for faktureringsplanlinjene på siden **Eskalering og rabatt**.</li><li>**Nei** – Eskaleringer kan ikke brukes på linjen.</li></ul><p>Standardinnstillingen er basert på valgt **Faktureringsplangruppe**.</p> |

### <a name="price-changes-tab"></a>Prisendringer-fanen

Når det gjelder linjer som endres fra **Standardpris** til **Flat pris**, vises følgende kolonner i rutenettet i **Prisendringer**-fanen:

- Endringsdato
- Endret av bruker
- Standardpris
- Flat pris
- Prisoppdatering

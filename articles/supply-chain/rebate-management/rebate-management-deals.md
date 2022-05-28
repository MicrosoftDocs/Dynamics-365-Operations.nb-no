---
title: Rabattbehandlingsavtaler
description: Dette emnet beskriver hvordan du oppretter rabattbehandlingsavtaler. Avtaler brukes til å kontrollere forskjellige metoder og baser for beregning av rabatter og royalty. De inneholder regler for inkluderinger og utelukkelser.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 76cdbf21cfbc0db7b363d0fbf60a1ecd0046efc1
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689698"
---
# <a name="rebate-management-deals"></a>Rabattbehandlingsavtaler

[!include [banner](../includes/banner.md)]

Rabattbehandlingsavtaler brukes til å kontrollere forskjellige metoder og baser for beregning av rabatter og royalty. De inneholder regler for inkluderinger og utelukkelser. Det finnes tre typer rabattbehandlingsavtaler: kunderabatter, kunderoyalty og leverandørrabatter. Alle de tre typene bruker lignende innstillinger. Dette emnet påpeker forskjeller der de finnes.

## <a name="create-a-deal"></a>Opprett en avtale

1. Gå til **Rabattbehandling \> Rabattbehandlingsavtaler \> Alle rabattbehandlingsavtaler**. På listesiden **Alle rabattbehandlingsavtaler** kan du opprette og arbeide med avtaler av alle de tre typene.

    Alternativt kan du følge ett av disse trinnene. I hvert tilfelle har listesiden som vises, alle de samme innstillingene som listesiden **Alle rabattbehandlingsavtaler**, men den er filtrert til å vise avtaler av bare én type.

    - Gå til **Rabattbehandling \> Rabattbehandlingsavtaler \> Kunderabattavtaler** for å opprette bare kunderabattavtaler.
    - Gå til **Rabattbehandling \> Rabattbehandlingsavtaler \> Kunderoyaltyavtaler** for å opprette bare kunderoyaltyavtaler.
    - Gå til **Rabattbehandling \> Rabattbehandlingsavtaler \> Leverandørrabattavtaler** for å opprette bare leverandørrabattavtaler.

1. Velg **Ny** i handlingsruten.
1. I dialogboksen **Opprett ny avtale** angir du verdier i følgende felter:

    - **Rabattbehandlingsavtale** – Hvis du har [definert en nummersekvens](rebate-management-parameters.md) for rabattavtaler, settes dette feltet automatisk til en unik, systemgenerert ID. Ellers må angi en unik ID.
    - **Beskrivelse** – Angi en beskrivelse av avtalen.
    - **Modul** – Velg partnertypen som avtalen gjelder for (*Kunde* eller *Leverandør*). Dette feltet kan angis automatisk basert på den valgte avtaletypen, avhengig av siden du startet fra. I dette tilfellet er feltet skrivebeskyttet.
    - **Type** – Velg avtaletypen (*Rabatt* eller *Royalty*). Dette feltet kan angis automatisk basert på den valgte avtaletypen, avhengig av siden du startet fra. I dette tilfellet er feltet skrivebeskyttet.
    - **Avstem etter** – Velg hvordan avtalen skal beregnes og avstemmes:

        - *Avtale* – En enkelt rabatt skal behandles for alle rabatter og fradrag i avtalen.
        - *Linje* – Rabatter skal behandles for hver linje i en avtale.

    - **Posteringsprofil** – Velg [posteringsprofilen](rebate-management-posting.md) som skal brukes for transaksjoner der avtalen gjelder. Dette feltet er bare tilgjengelig når feltet **Avstem etter** er satt til *Avtale*. Hvis det er satt til *Linje*, tilordner du profilen senere, for hver linje du legger til i avtalen.
    - **Posteringsprofil for garanti** – Velg [posteringsprofilen](rebate-management-posting.md) som skal brukes for garantitransaksjoner. Posteringsprofiler er bare påkrevd for garantitransaksjoner hvis garantien gjelder for en royalty. Hvis ikke, selv om en posteringsprofil ikke er obligatorisk, og hvis ingen posteringsprofil er angitt, vises det en feil når garantier posteres. Dette feltet er bare tilgjengelig når feltet **Type** er satt til *Royalty*. 
    - **Rabattlevering** – Velg hvordan rabatten eller royaltyen skal betales:

        - *Økonomisk* – Generer en fritekstkreditnota eller leverandørdebetnota, slik at penger kan betales eller mottas senere. Legg merke til at avsetningene **kan** brukes med rabatter der dette alternativet er valgt. Dette alternativet er det eneste tilgjengelige alternativet når feltet **Type** er satt til *Royalty*.
        - *Vare* – Generer en salgsordre for varer i henhold til avtaleoppsettet. I denne salgsordren tilordnes en pris på 0 (null) til hver vare. Legg merke til at avsetningene **ikke kan** brukes med rabatter der dette alternativet er valgt.

    - **Rabattvaluta** – Velg valutaen som skal brukes når rabatten, fradraget eller royaltyen betales.
    - **Dokumentmerknader** – Skriv inn merknader om avtalen etter behov.
    - **Kumulativ garanti** – Du kan bare sette dette alternativet til *Ja* hvis **Type**-feltet er satt til *Royalty*. Dette alternativet påvirker beregningen av lønnstrekksbetalinger. Her er et eksempel:

        - Garantien for avtalen er å selge en verdi som vil føre til en betaling på USD 10 000 per kvartal.
        - Organisasjonen som selger varene, selger en verdi som fører til en fradragsbetaling på USD 12 000 i kvartal 1. Resultatet er en royalty på USD 12 000 som betales, minus garantien på USD 10 000.
        - Hvis alternativet **Kumulativ garanti** er satt til *Ja*, gjelder de ekstra USD 2000 i royaltyer som ble betalt i kvartal 1, for kvartal 2. Derfor er kunden garantert USD 8000 (garantien på USD 10 000 minus tilleggsbetaling på USD 2000).
        - I kvartal 2 registrerer du salg som utløser en royalty på USD 5000.
        - Systemet identifiserer en betaling på USD 3000 (USD 8000 minus USD 5000 i betalte royaltyer).
        - Hvis alternativet **Kumulativ garanti** er satt til *Nei*, garanteres det for hele beløpet på USD 10 000 hvert kvartal. Denne garantien tilsvarer en foreslått betaling på USD 5000 i kvartal 2 (garantien på USD 10 000 minus USD 5000 i betalte royaltyer).

1. Velg **OK** for å opprette avtalen og lukke dialogboksen.

Denne fremgangsmåten oppretter hodenivået for den nye avtalen. Deretter legger du til linjer i avtalen.

## <a name="add-lines-to-a-deal"></a>Legg til linjer i en avtale

Når du har opprettet en avtale som beskrevet i den forrige delen, kan du åpne den fra listesiden. Deretter kan du legge til linjer for å identifisere kundene eller leverandørene, varene, tidsrammene, en basis og beregningsmetoder for avtalen. En avtale kan ha én eller flere linjer. Hvis en avtale har flere linjer, er de vanligvis av samme type, eller de samme parameterne knyttes til dem. Avtalen vil ikke gjøre noe før du legger til linjer i en avtale.

1. Åpne den riktige listesiden for rabattavtaler, som beskrevet i den forrige delen.
1. Finn og åpne avtalen du vil arbeide med.
1. På hurtigfanen **Rabattbehandling** velger du en av følgende knapper for å legge til en avtalelinje i rutenettet:

    - **Legg til linje** – Legg til en ny, tom avtalelinje.
    - **Kopier linje** – Hvis en eksisterende avtalelinje ligner avtalelinjen du vil legge til, kan du velge denne knappen for å kopiere den. Den nye avtalelinjen inneholder alle innstillingene fra de tilknyttede detaljene for rabattbehandling. Du kan deretter redigere innstillingene. For eksempel vil du vanligvis oppdatere varerelasjonen og rabattprosenten.

1. Angi følgende felter på den nye avtalelinjen:

    - **Rabattbehandlingsnummer** – Hvis du har [definert en nummersekvens](rebate-management-parameters.md) for rabattbehandlingsnumre, settes dette feltet automatisk til en unik, systemgenerert ID. Ellers må angi en unik ID.
    - **Type** – Avtaletypen som linjen gjelder for (*Rabatt* eller *Royalty*). Verdien kopieres fra hodet og kan ikke endres.
    - **Beskrivelse** – Angi en beskrivelse av avtalelinjen.
    - **Firma** – Velg firmaet (juridisk enhet) som avtalelinjen gjelder for. Under behandlingen kan brukere bare behandle avtalelinjer som er tilordnet firmaet de bruker i øyeblikket. Listesiden **Kunderabattvataler** gir en flerfirmavisning basert på brukerens sikkerhetstilgang. Du kan imidlertid bare redigere og behandle rabatter for det firmaet du bruker i øyeblikket.
    - **Kontokode** – Velg omfanget av kunder eller leverandører som avtalelinjen gjelder for:

        - *Tabell* – Avtalelinjen gjelder for en bestemt kunde eller leverandør.
        - *Gruppe* – Avtalelinjen gjelder for en gruppe med kunder eller leverandører. Hvis du vil ha mer informasjon om hvordan du konfigurerer grupper, kan du se [Rabattbehandlingsgrupper](rebate-management-groups.md).
        - *Alle* – Avtalelinjen gjelder for alle kunder eller leverandører.

    - **Kontorelasjon** – Hvis du valgte *Tabell* i **Kontokode**-feltet, velger du kunden eller leverandøren som avtalen gjelder for. Hvis du valgte *Gruppe*, velger du kunde- eller leverandørgruppen. Hvis du valgte *Alle*, er dette feltet utilgjengelig.
    - **Varekode** – Velg omfanget av varer som avtalelinjen gjelder for:

        - *Tabell* – Avtalelinjen gjelder for en bestemt vare.
        - *Gruppe* – Avtalelinjen gjelder for en gruppe med varer. Hvis du vil ha mer informasjon om hvordan du konfigurerer grupper, kan du se [Rabattbehandlingsgrupper](rebate-management-groups.md).
        - *Alle* – Avtalelinjen gjelder for alle varer.

    - **Varerelasjon** – Hvis du valgte *Tabell* i **Varekode**-feltet, velger du varen som avtalelinjen gjelder for. Hvis du valgte *Gruppe*, velger du varegruppen. Hvis du valgte *Alle*, er dette feltet utilgjengelig.
    - **Enhetstype** – Velg enhetstypen som gjelder for avtalelinjen (*Lagerenhet* eller *Faktisk vektenhet*). Legg merke til at dette feltet kan være tomt for eldre poster. I dette tilfellet antas *lagerenhetsverdien*.
    - **(Lagerstyringsparametere)** – I de gjenværende feltene på avtalelinjen angir du verdier for lagerstyringsparameterne som skal brukes til å definere varene som er inkludert i avtalen (for eksempel varestørrelse, farge, stil, område og lager). Hvis du vil legge til eller fjerne dimensjoner, velger du **Vis dimensjoner** i handlingsruten.

1. Velg **Lagre** i handlingsruten.
1. Hvis du vil begrense ytterligere settet med varer som en avtalelinje gjelder for, kan du merke linjen og deretter gå til hurtigfanen **Rabattbehandling** og velge **Filter** for å åpne en standard **Forespørsel**-dialogboks.
1. For hver avtalelinje du legger til, definerer du beregningsdetaljene og andre detaljer på hurtigfanen **Detaljer om rabattbehandling**, som beskrevet i neste del.

## <a name="add-rebate-management-details-to-a-deal-line"></a>Legg til detaljer om rabattbehandling i en avtalelinje

For hver linje i avtalen må du definere detaljer på hurtigfanen **Detaljer om rabattbehandling**. Velg først avtalelinjen på hurtigfanen **Rabattbehandling**. Deretter angir du verdier for denne avtalelinjen ved å bruke de ulike fanene på hurtigfanen **Detaljer om rabattbehandling**. Følgende underdeler beskriver hvordan du bruker hver fane.

### <a name="settings-on-the-general-tab"></a>Innstillinger på Generelt-fanen

På **Generelt**-fanen på hurtigfanen **Detaljer om rabattbehandling** kan du sette opp beregningsmetoden og utgangspunktet for den valgte avtalelinjen. Dette oppsettet styrer om det kreves et minimumsinnkjøp, posteringsprofilene som er knyttet til avtalelinjen og detaljene i beregningen. Følgende tabell beskriver feltene som er tilgjengelige.

| Felt | beskrivelse |
|---|---|
| Beregningsmåte | Velg metoden som skal brukes når den valgte avtalelinjen kombineres med andre avtalelinjer (*Trinnvis*, *Kumulativ*, *Rullende* eller *Total*). Verdien i dette feltet kan påvirke resultatet av rabattberegningene dramatisk. Hvis du vil ha en fullstendig beskrivelse av hver metode og eksempler som viser hvordan den påvirker rabattberegningen, kan du se delen [Beregningsmetoder for avtalelinjer](#calc-methods) senere i dette emnet. |
| Basis | Velg om rabatten skal brukes basert på antall (det vil si totalt antall enheter som er kjøpt eller solgt) eller verdi (det vil si totalprisen på varer som kjøpes eller selges). |
| Transaksjonstype | <p>Velg tidspunktet i prosessen når beregningen skal skje:</p><ul><li>*Ordre* – Bruk det bestilte antallet eller verdien som grunnlag for beregningen.</li><li>*Levert* – Bruk det leverte antallet eller verdien som grunnlag for beregningen.</li><li>*Faktura* – Bruk det fakturerte antallet eller verdien som grunnlag for beregningen.</li></ul> |
| Enhet | Hvis du valgte *Antall* i **Basis**-feltet, velger du enheten som antallet må angis i. |
| Minimumsbeløp | Angi minimumsbeløpet som må betales per periode. Du kan angi en negativ verdi for å tillate negative rabattbeløp hvis kreditnotaer overskrider salg for perioden. |
| Prinsipp for rabattreduksjon | Velg [prinsippet for rabattreduksjon](rebate-reduction-principle.md) som gjelder for avtalelinjen. |
| Variantnummer | Hvis avtalelinjen gjelder for en vare som har varianter, velger du varianten som avtalelinjen gjelder for. |
| Basis for leverandørrabatt | <p>Dette feltet vises bare for leverandørrabatter (det vil si avtaler der **Modul**-feltet er satt til *Leverandør*). Velg basisen for leverandørrabatten:</p><ul><li>*Bestilling* – Rabatten som leverandøren får, er basert på antallet i eller verdien av bestillingen.</li><li>*Salgsordre* – Leverandøren får en rabatt bare etter at varene er solgt. Rabatten er basert på antallet i eller verdien av salgsordren.</li></ul> |
| Prisgrunnlag | <p>Dette feltet vises bare for leverandørrabatter (avtaler der **Modul**-feltet er satt til *Leverandør*). Hvis du valgte *Salgsordre* i feltet **Basis for leverandørrabatt**, velger du det aktuelle prisgrunnlaget:</p><ul><li><p>*FIFO* – Den periodiske oppgaven **Beregn FIFO-innkjøpspriser** må kjøres for å beregne rabatten. (Du kan kjøre oppgaven ved å gå til **Rabattbehandling \> Periodiske oppgaver \> Beregn FIFO-innkjøpspriser**.) En FIFO-regel (først inn, først ut) brukes til å beregne verdien av beholdningen som er solgt. Denne verdien blir deretter brukt til å beregne leverandørrabattene. Her er et eksempel:</p><ul><li>**Beholdning solgt:** 1000 enheter til USD 3,00 hver = USD 3000</li><li>**Gjeldende innkjøpspris, basert på FIFO:** USD 2,00</li><li>**Arbeidsberegning:** *Enheter solgt* × *Gjeldende innkjøpspris* = 1000 × USD 2,00 = USD 2000</li></ul></li><li><p>*Siste innkjøpspris* – Verdien fra den siste innkjøpstransaksjonen vil bli brukt til å beregne leverandørrabattene. Her er et eksempel:</p><ul><li>**Beholdning solgt:** 1000 enheter til USD 3,00 hver = USD 3000</li><li>**Siste innkjøpspris:** USD 2,00</li><li>**Arbeidsberegning:** *Enheter solgt* × *Siste innkjøpspris* = 1000 × USD 2,00 = USD 2000</li></ul></li><li><p>*Gjennomsnittlig innkjøpspris* – Den vektede gjennomsnittsverdien for de siste *X* månedene brukes til å beregne leverandørrabattene. Hvis du velger dette alternativet, må du angi antall måneder i **Antall måneder**-feltet (som bare er tilgjengelig når **Prisgrunnlag**-feltet er satt til *Gjennomsnittlig innkjøpspris*). Her er et eksempel:</p><ul><li>**Beholdning solgt:** 1000 enheter til USD 3,00 hver = USD 3000</li><li>**Gjennomsnittlig innkjøpspris:** USD 2,00</li><li>**Arbeidsberegning:** *Enheter solgt* × *Gjennomsnittlig innkjøpspris* = 1000 × USD 2,00 = USD 2000</li></ul></li><li><p>*Salgspris* – Salgsprisen vil bli brukt til å beregne leverandørrabattene. Her er et eksempel:</p><ul><li>**Beholdning solgt:** 1000 enheter til USD 3,00 hver = USD 3000</li><li>**Gjennomsnittlig innkjøpspris:** USD 2,00</li><li>**Arbeidsberegning:** *Enheter solgt* × *Salgspris* = 1000 × USD 3,00 = USD 3000</li></ul></li></ul> |
| Antall måneder | Dette feltet vises bare for leverandørrabatter (avtaler der **Modul**-feltet er satt til *Leverandør*). Hvis du valgte *Gjennomsnittlig innkjøpspris* i **Prisgrunnlag**-feltet, må du angi antall måneder som skal brukes. |
| Posteringsprofil | Velg [posteringsprofilen](rebate-management-posting.md) som gjelder for den valgte avtalelinjen. Denne profilen brukes bare når **Avstem etter**-feltet på avtalehodet er satt til *Linje*. Hvis **Avstem etter**-feltet er satt til *Avtale*, brukes posteringsprofilen som er definert for avtalehodet. Hvis ingen posteringsprofil er angitt på avtalelinjen, brukes posteringsprofilen som er definert for avtalehodet. |
| Posteringsprofil for garanti | Dette feltet fungerer som **Posteringsprofil**-feltet, men gjelder bare for royaltyer. |
| Betalingsmiddel | Betalingstypen for posteringsprofilen som er valgt for avtalen. |
| Inkludert merverdiavgift | Velg om transaksjonen inkluderer merverdiavgift. Inkludering av merverdiavgift er bare relevant når **Grunnlag**-feltet er satt til *Verdi*. Fakturabeløpet blir brukt som beløp for inkludering av merverdiavgift. Hvis rabattberegningen er basert på en prosentverdi, multipliserer systemet rabattprosenten med beløpet for merverdiavgift inkludert. Legg merke til at beregningen bruker mva-verdien fra avtalelinjen. |
| Inkluder kreditnotaer | <p>Sett dette alternativet til *Ja* hvis du vil ta med kreditnotaer i rabattberegningen.</p><p>Hvis du setter dette alternativet til *Ja*, varierer effekten, alt etter verdien i **Transaksjonstype**-feltet:</p><ul><li>Hvis **Transaksjonstype**-feltet er satt til *Faktura*, blir beregningen en faktor i kreditnotaer. Denne konfigurasjonen er den vanlige konfigurasjonen.</li><li>Hvis **Transaksjonstype**-feltet er satt til *Ordre*, vil beregningen ta med både salgsordrer som har negative verdier og åpne returordrer.</li></ul> |
| Rabattert beløp | Sett dette alternativet til *Ja* for å basere beregningen på det rabatterte beløpet for varen eller varene i tilfeller der avtalelinjerabatter er gitt. |
| Bare betalte fakturaer | Sett dette alternativet til *Ja* hvis beregningen bare skal vurdere fullt betalte fakturaer. (Rabatter beregnes med andre ord ikke for delvis betalte fakturaer.) Dette alternativet er bare tilgjengelig når **Transaksjonstype**-feltet er satt til *Faktura*. |
| Inkluder fritekst | Sett dette alternativet til *Ja* hvis du vil inkludere fritekstfakturaer i beregningen. Fritekstfakturaer kan bare tas med for avtalelinjer der **Varekode**-feltet er satt til *Alle*. |
| Inkluder utligningsrabatt | Sett dette alternativet til *Ja* for å redusere rabatten med den første utligningsrabatten. Det forutsettes at organisasjonen vil få den første utligningsrabatten. Sett dette alternativet til *Nei* for å aktivere utligningsrabatten som skal brukes senere. |
| Dokumentmerknader | Skriv inn merknader som skal brukes som transaksjonstekst på journallinjer i rabattransaksjoner. |

### <a name="settings-on-the-dates-tab"></a>Innstillinger i fanen Datoer

Innstillingene på **Datoer**-fanen på hurtigfanen **Detaljer om rabattbehandling** definerer hyppigheten og tidspunktet for beregningene som er spesifisert på **Generelt**-fanen. De bestemmer hvordan beregninger inntreffer ved behandlingstiden.

I denne kategorien kan du angi datoområdet som den valgte avtalelinjen er gyldig for, og beregningsfrekvensen. Du kan også angi om garantien skal posteres, og når.

Du kan bruke knappene på verktøylinjen til å legge til datolinjer i rutenettet eller fjerne dem. Hvis det finnes flere datolinjer, må ikke de gyldige datointervallene overlappe. Ellers får du en feilmelding når du prøver å lagre avtalen.

Følgende tabell beskriver feltene som er tilgjengelige for hver datolinje.

| Felt | beskrivelse |
|---|---|
| Fra dato | Angi den første datoen som datolinjen gjelder. Hvis fra- og til-datoer er angitt i avtalehodet, brukes de som standardverdier for hver nye datolinje. |
| Til dags dato | Angi den siste datoen som datolinjen gjelder. Hvis fra- og til-datoer er angitt i avtalehodet, brukes de som standardverdier for hver nye datolinje. |
| Per | Angi hvor ofte avtalelinjen skal beregnes. Skriv inn et heltall her, og velg deretter en enhet i **Kumuler etter**-feltet. Hvis du for eksempel vil beregne annenhver uke, setter du **Per**-feltet til *2* og **Kumuler etter**-feltet til *Uker*. |
| Kumuler etter | Velg enheten som gjelder for **Per**-innstillingen. Velg *Levetid* for å beregne gjennom hele levetiden til avtalelinjen. Velg *Tilpasset periode* for å velge en periode som er definert i økonomimodulen. I dette tilfellet må du også angi **Periodetype**-feltet. |
| Periodetype | Dette feltet er bare tilgjengelig når feltet **Kumuler etter** er satt til *Tilpasset periode*. Verdiene som kan velges, kommer fra periodetypene som er definert i økonomimodulen. |
| Første dag i uken | Angi hvordan ukene skal identifiseres for perioden. Dette feltet er bare tilgjengelig når feltet **Kumuler etter** er satt til *Uker*. |
| Krev per | Angi hvor ofte rabattyper kan kreves inn for avtalelinjen. Skriv inn et heltall her, og velg deretter en enhet i **Krev etter**-feltet. |
| Krev etter | Velg enheten som gjelder for **Krev per**-innstillingen. Velg *Levetid* for å tillate krav bare én gang i løpet av hele levetiden til avtalelinjen. Velg *Tilpasset periode* for å velge en periode som er definert i økonomimodulen. I dette tilfellet må du også angi **Kravperiodetype**-feltet. |
| Kravperiodetype | Dette feltet er bare tilgjengelig når feltet **Krev etter** er satt til *Tilpasset periode*. Verdiene som kan velges, kommer fra periodetypene som er definert i økonomimodulen. |
| Prosess ved postering | Merk av i denne avmerkingsboksen hvis kravlinjen skal behandles på posteringstidspunktet. Dette alternativet er bare tilgjengelig for avtalelinjer der **Transaksjonstype**-feltet på **Generelt**-fanen er satt til *Levert* eller *Faktura*. For avsetninger posteres avsetningen når følgeseddelen eller fakturaen genereres. |
| Garanti per | Dette feltet gjelder bare for royalty-avtaler. Angi hvor ofte garantien for royalty skal beregnes i løpet av perioden som er definert av **Kumuler etter**-innstillingen. Skriv inn et heltall her, og velg deretter et betalingstidspunkt i **Garanti betalt**-feltet. |
| Garanti betalt | <p>Dette feltet gjelder bare for royalty-avtaler. Det fungerer sammen med **Garanti per**-feltet for å definere hyppigheten for garantiberegningen. Velg én av følgende verdier:</p><ul><li><p>*Begynnelsen av perioden* – Garantien betales i begynnelsen av avtaleperioden som er definert for datolinjen. Den fulle garantien behandles først. Bare verdien av royaltyer som overskrider beløpet, posteres som en royalty. Her er et eksempel:</p><ul><li>**Minimumsgaranti:** USD 10 000 over to måneder.</li><li>**Måned 1:** USD 10 000 ble postert som garanti, og USD 0 i royalty ble postert.</li><li>**Måned 2:** USD 2000 ble postert til royalty, og USD 0 i garantier ble postert.</li><li>**Arbeidsberegning:** *Gjenværende garanti* – *Royalty postert* = USD 0 – USD 2000 = USD -2000.</li></ul><p>Fordi en royalty-betaling på USD 2000 kreves, opprettes det en journal for USD 2000.</p><p>**Merk:** Garantien bør beregnes og posteres sammen med fradragene for den første perioden.</p></li><li><p>*Periodeslutt* – Garantiperioden betales ikke før slutten av fratrekksavtalen, som definert på datolinjen. Her er et eksempel:</p><ul><li>**Minimumsgaranti:** USD 10 000 over to måneder.</li><li>**Måned 1:** USD 5000 ble postert som en royalty, og en journal ble opprettet.</li><li>**Måned 2:** USD 7000 ble postert som en royalty, og en journal ble opprettet.</li><li>**Arbeidsberegning:** Fordi royalty overskrider garantibeløpet, posteres USD 0 til garantien.</li></ul><p>**Merk:** Garantien bør beregnes og posteres bare sammen med fradragene for og rabattransaksjonen for den siste perioden.</p></li></ul> |
| Minimumsgaranti | Dette feltet gjelder bare for royalty-avtaler. Angi minimumsbeløpet for garantien for en royalty i valutaen som er definert i avtalehodet. |

### <a name="settings-on-the-lines-tab"></a>Innstillinger i fanen Linjer

På **Linjer**-fanen på hurtigfanen **Detaljer om rabattbehandling** kan du definere beregningslinjer for den valgte avtalelinjen. Hver beregningslinje fastsetter et antall eller en verditerskel, og et tilknyttet kompensasjonsbeløp eller varer. **Grunnlag**-feltet på **Generelt**-fanen spesifiserer om hver beregningslinje er basert på et antall eller en verdi.

Du kan bruke knappene på verktøylinjen til å legge til beregningslinjer i rutenettet eller fjerne dem. Du kan ha et hvilket som helst antall beregningslinjer. Hvis det finnes flere beregningslinjer, må imidlertid ikke til- og fra-antallet eller verdiintervallene overlappe.

Følgende tabell beskriver feltene som er tilgjengelige for hver beregningslinje.

| Felt | beskrivelse |
|---|---|
| Fra antall/verdi | Angi minimumsantallet eller verdien som beregningslinjen gjelder for. |
| Til antall/verdi | Angi maksimumsantallet eller verdien som beregningslinjen gjelder for. |
| Rabattbehandlingsmetode | <p>Dette feltet er bare tilgjengelig for avtaler der **Rabattlevering**-feltet i hodet er satt til *Økonomisk*. Velg metoden som skal brukes til å beregne tabatten:</p><ul><li>*Fast* – Et fast prisbeløp brukes for linjen.</li><li>*Prosent* – En prosent av salgsbeløpet brukes.</li><li>*Sats* – Et fast prisbeløp per ordre brukes.</li></ul><p>**Viktig:** Vi anbefaler på det sterkeste at du bruker den samme metoden for hver beregningslinje på **Linjer**-fanen. Hvis det kreves en ny metode, oppretter du en ny avtalelinje. Husk at du kan bruke **Kopier linje**-knappen på hurtigfanen **Rabattbehandling** til å opprette en ny avtalelinje fra en eksisterende avtalelinje.</p><p>**Merk:** Hvis **Rabattlevering**-feltet er satt til *Vare*, settes dette feltet alltid til *Fast*. Hvis du vil ha mer informasjon om hvordan du angir varene, kan du se teksten som følger denne tabellen. |
| Rabattbehandlingsbeløp | Dette feltet er bare tilgjengelig for avtaler der **Rabattlevering**-feltet i hodet er satt til *Økonomisk*. Angi beløpet som skal brukes til å beregne rabatten, basert på metoden du valgte i feltet **Rabattbehandlingsmetode**. |

Som nevnt i forrige tabell, for avtaler der **Rabattlevering**-feltet i hodet er satt til *Vare*, må du angi varene som skal oppgis for hver beregningslinje, på **Linjer**-fanen. Følg trinnene nedenfor for å angi varene.

1. På **Linjer**-fanen oppretter du den nødvendige beregningslinjen hvis den ikke finnes, og velger den.
1. Hvis avtalen ikke har vært lagret siden du opprettet beregningslinjen, velger du **Lagre** i handlingsruten.
1. På **Linjer**-fanen velger du **Varer**.
1. På **Varer**-siden bruker du knappene i handlingsruten til å legge til varer i rutenettet eller fjerne elementer etter behov. For hver rad angir du feltene nedenfor:

    - **Varenummer** – Velg varen som skal gis.
    - **(Andre dimensjoner)** – Hvis du må bruke flere dimensjoner for å definere varen (for eksempel varekonfigurasjon, størrelse, farge, stil, område eller lager), må du angi dem. Hvis du vil legge til eller fjerne tilgjengelige dimensjoner, velger du **Vis dimensjoner** i handlingsruten.
    - **Antall** – Angi antallet som skal gis etter at terskelen for den valgte beregningslinjen er oppfylt.
    - **Enhet** – Velg enheten som **Antall**-verdien er angitt i.
    - **Flere** – Dette feltet fungerer sammen med **Antall**-feltet. På en varelinje kan du for eksempel sette **Antall**-feltet til *2* og **Multiplum**-feltet til *100*. Hvis du deretter har et totalt salgsordreantall på 150, vil to av varene være fri (to per 100).

### <a name="settings-on-the-inventory-dimensions-tab"></a>Innstillinger på fanen Lagerdimensjoner

På **Lagerdimensjoner**-fanen på hurtigfanen **Rabattbehandlingsdetaljer** vises alle de tilgjengelige dimensjonsverdiene for produktet som er angitt for den valgte avtalelinjen. Det omfatter dimensjoner som vises ikke på hurtigfanen **Rabattbehandling**. Du kan bare redigere verdier for de dimensjonene som gjelder for det valgte produktet.

Du kan legge til flere dimensjoner i rutenettet på hurtigfanen **Rabattbehandling** ved å velge **Visningsdimensjoner** på handlingsruten.

## <a name="calculation-methods-for-deal-lines"></a><a name="calc-methods"></a>Beregningsmetoder for avtalelinjer

Hver gang du definerer detaljer for en av avtalelinjene, som beskrevet i den forrige delen, må du velge beregningsmåten for denne linjen. Denne delen forklarer hver beregningsmetode, og gir eksempler som viser hvordan hver metode beregner totalrabatten for ordrer og avtalelinjer. I disse eksemplene er ordrene og avtalelinjene identiske. Bare beregningsmetodene er forskjellige.

### <a name="stepped-calculation-method"></a>Trinnvis beregningsmetode

Den trinnvise beregningsmetoden beregning beregner trinnvis, der hver avtalelinje trinnvis bidrar til rabatten til salgsantallet eller -verdien er nådd. Trinnene kan baseres på enten antallet eller verdien på varene som selges, avhengig av innstillingen for **Grunnlag**-feltet på **Generelt**-fanen på hurtigfanen **Rabattbehandlingsdetaljer**.

En avtalelinje er for eksempel definert slik at feltet **Beregningsmetode** er satt til *Trinnvis* og **Grunnlag**-feltet er satt til *Verdi*. Det omfatter beregningslinjer som gir følgende rabatter:

- **Linje A:** 10 prosent opptil USD 1000
- **Linje B:** 25 prosent opptil USD 2500

Hvis verdien av varene som ble kjøpt eller solgt, er USD 2000, beregnes den resulterende rabatten på USD 350 slik:

- **Rabatt (A):** *Terskel (A)* × *Prosent (A)* = USD 1000 × 10 prosent = USD 100
- **Rabatt (B):** (*Verdi solgt* – *Terskel (A)*) × *Prosent (B)* = (USD 2000 – USD 1000) × 25 prosent = USD 250
- **Total rabatt:** *Rabatt (A)* + *Rabatt (B)* = USD 100 + USD 250 = USD 350

Hvis **Grunnlag**-feltet er satt til *Antall* i stedet for *Verdi*, fungerer den trinnvise beregningsmetoden på lignende måte. Det første trinnet brukes for det identifiserte antallet helt til det andre trinnet nås. Det andre trinnet brukes deretter for alt antall uover det første trinnet helt til det tredje trinnet nås. Denne prosessen forsetter deretter gjennom alle etterfølgende trinn.

### <a name="cumulative-calculation-method"></a>Kumulativ beregningsmetode

Den kumulative beregningsmetoden bruker bare én beregningslinje til å beregne rabatten. Hvis det er flere beregningslinjer tilgjengelig for avtalelinjen, brukes beregningslinjen med høyest verdi eller høyeste antall som nås, for hele antallet eller verdien. På samme måte som de andre beregningsmetodene bruker den kumulative metoden innstillingen i **Grunnlag**-feltet på **Generelt**-fanen på hurtigfanen **Rabattbehandlingsdetaljer** til å avgjøre om salgsantallet eller salgsverdien skal brukes til å beregne rabattene.

En avtalelinje er for eksempel definert slik at feltet **Beregningsmetode** er satt til *Kumulativ* og **Grunnlag**-feltet er satt til *Verdi*. Det omfatter beregningslinjer som gir følgende rabatter:

- **Linje A:** 10 prosent opptil USD 1000
- **Linje B:** 25 prosent opptil USD 2500

Hvis verdien av varene som ble kjøpt eller solgt, er USD 2000, bruker beregningen bare linje B. Den resulterende rabatten på USD 500 beregnes slik:

- **Total rabatt:** *Verdi solgt* × *Rabatt (B)* = USD 2000 × 25 prosent = USD 500

### <a name="rolling-calculation-method"></a>Rullende beregningsmetode

Den rullende beregningsmetoden beregner alle mulige beregningslinjer for avtalen. Hvis det finnes flere beregningslinjer, og flere enn én av dem nås, vil alle beregningslinjene som nås, bli brukt, men øvre terskler gjelder for hver prosent. På samme måte som de andre beregningsmetodene bruker den rullende metoden innstillingen i **Grunnlag**-feltet på **Generelt**-fanen på hurtigfanen **Rabattbehandlingsdetaljer** til å avgjøre om salgsantallet eller salgsverdien skal brukes til å beregne rabattene.

En avtalelinje er for eksempel definert slik at feltet **Beregningsmetode** er satt til *Rullende* og **Grunnlag**-feltet er satt til *Verdi*. Det omfatter beregningslinjer som gir følgende rabatter:

- **Linje A:** 10 prosent opptil USD 1000
- **Linje B:** 25 prosent opptil USD 2500

Hvis verdien av varene som ble kjøpt eller solgt, er USD 2000, beregnes den resulterende rabatten på USD 600 slik:

- **Rabatt (A):** *Terskel (A)* × *Prosent (A)* = USD 1000 × 10 prosent = USD 100
- **Rabatt (B):** *Verdi solgt* × *Prosent (B)* = USD 2000 × 25 prosent = USD 500
- **Total rabatt:** *Rabatt (A)* + *Rabatt (B)* = USD 100 + USD 500 = USD 600

### <a name="total-calculation-method"></a>Total beregningsmåte

Den totale beregningsmetoden bruker alle beregningslinjene til å beregne rabatten. Den bruker det totale antallet til å beregne rabatten for hver beregningslinje som nås, og hver beregningslinje bruker prosentsatsen på hele beløpet. På samme måte som de andre beregningsmetodene bruker den totale metoden innstillingen i **Grunnlag**-feltet på **Generelt**-fanen på hurtigfanen **Rabattbehandlingsdetaljer** til å avgjøre om salgsantallet eller salgsverdien skal brukes til å beregne rabattene.

En avtalelinje er for eksempel definert slik at feltet **Beregningsmetode** er satt til *Total* og **Grunnlag**-feltet er satt til *Verdi*. Det omfatter beregningslinjer som gir følgende rabatter:

- **Linje A:** 10 prosent opptil USD 1000
- **Linje B:** 25 prosent opptil USD 2500

Hvis verdien av varene som ble kjøpt eller solgt, er USD 2000, beregnes den resulterende rabatten på USD 700 slik:

- **Rabatt (A):** *Verdi solgt* × *Prosent (A)* = USD 2000 × 10 prosent = USD 200
- **Rabatt (B):** *Verdi solgt* × *Prosent (B)* = USD 2000 × 25 prosent = USD 500
- **Total rabatt:** *Rabatt (A)* + *Rabatt (B)* = USD 200 + USD 500 = USD 700

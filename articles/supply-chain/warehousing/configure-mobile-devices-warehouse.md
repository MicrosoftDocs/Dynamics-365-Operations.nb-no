---
title: Konfigurere mobilenheter for lagerarbeid
description: "Denne artikkelen beskriver hvordan du konfigurerer menyelementene lagerarbeidere bruker til å utføre arbeidet på en mobil enhet."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 29941
ms.assetid: 6dff6313-dc6e-4f06-9c0c-dab24eefe4da
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f711ef739e8b885f2f09586f34775e826b619c82
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-mobile-devices-for-warehouse-work"></a>Konfigurere mobilenheter for lagerarbeid

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan du konfigurerer menyelementene lagerarbeidere bruker til å utføre arbeidet på en mobil enhet.

**Obs!** Denne artikkelen gjelder funksjoner i Lagerstyring. Den gjelder ikke for funksjoner i Beholdningsstyring. Menyelementene som vises på menyer for en lagermobilenhet, konfigureres på siden **Menyelementer på mobilenheten**. Fordi menyelementene kan settes inn i flere menyer, er det enkelt å konfigurere menystrukturene slik at bare bestemte typer arbeid er tilgjengelig for bestemte brukere. Du kan konfigurere menyelementer for å gjøre følgende:

-   Behandle en forespørsel eller utfør en aktivitet, for eksempel utskrift av en etikett, generering av numre for nummerskilt, oppstart av en produksjonsordre eller raskt oppslag for informasjon om varer på en lokasjon.
-   Opprett arbeid som skal utføres via en annen prosess. Mottak av en vare for en bestilling kan for eksempel opprette plasseringsarbeid for en annen arbeider.
-   Utføre arbeid som ble opprettet av en annen prosess (eksisterende arbeid), for eksempel plasseringsarbeid som ble opprettet da du mottok en vare for en bestilling.

Hvis du vil opprette et menyelement for en aktivitet eller forespørsel, kan du angi **Modus**-feltet til **Indirekte**. En liste over **Aktivitetskode**-alternativer blir deretter tilgjengelig, slik at du kan velge hvilken type forespørsel eller aktivitet som menyelementet gjelder for. Hvis du vil opprette et menyelement for å generere lagerarbeid, kan du angi **Modus**-feltet til **Arbeid**. En liste over **Arbeidsopprettelsesprosess**-alternativer blir deretter tilgjengelig. Hvis du vil opprette et menyelement for å behandle eksisterende lagerarbeid, kan du angi **Modus**-feltet til **Arbeid**, og deretter angi alternativet **Bruk eksisterende arbeid** til **Ja**. **Merk:** Tilleggsfelt kan være tilgjengelige for menyelementer, avhengig av modusen du velger for menyelementet, og om menyelementet brukes til å utføre eksisterende arbeid. Hvis du vil ha informasjon om tilleggsvalgene for feltene, kan du se delen "Flere alternativer for menyelementer" senere i denne artikkelen.

## <a name="configure-menu-items-for-activities-and-inquiries"></a>Konfigurere menyelementer for aktiviteter og forespørsler
Hvis **Modus**-feltet for et menyelement er satt til **Indirekte**, kan du opprette et menyelement for å utføre en generell aktivitet eller en spørring som ikke fører til arbeid. Disse omfatter for eksempel ny utskrift av nummerskiltetiketter og forespørsler om varene på en lokasjon. Følgende tabell viser alternativene som er tilgjengelige.

| Alternativ                      | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ingen                        | Denne standardverdien aktiverer ikke en aktivitet eller en forespørsel.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Om                       | Vis informasjon om systemet, for eksempel versjonsnummeret, lager-ID og arbeideren som er logget på.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Endre lager            | Endre lageret en arbeider er logget på.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Lokasjonsforespørsel            | Vis informasjon om alle varer og antall for en lokasjon.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Nummerskiltforespørsel       | Vis antall varer på et nummerskilt, og lokasjonen til nummerskiltet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Start produksjonsordre      | Start en produksjonsordre.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Produksjonssvinn            | Angi svinnmengden som ble dannet under produksjon, for hver stykklistelinje.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Siste produksjonspall      | Angi at den siste pallen med varer er produsert for en produksjonsordre, og at statusen for produksjonsordren må oppdateres til **Ferdigmeldt**. Statusen for råvarene som ikke ble brukt under produksjonen, tilbakestilles fra **Plukket** til **I ordre/bestilling** , og varene kan returneres til lager.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Vareforespørsel                | Skann en vare for å finne ut om den finnes på lageret. Forespørselen returnerer alle lokasjoner og antall for den skannede varen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Skriv ut etikett på nytt               | Skriv ut en nummerskiltetikett på nytt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Nummerskilt-build         | Opprett et overordnet nummerskilt ved å kombinere flere nummerskilt på samme lokasjon. Dette alternativet er nyttig hvis du flytter flere nummerskilt samtidig. Når det overordnede nummerskiltet er flyttet, må du dele opp nummerskilt-builden ved å bruke Nummerskilt – bryt før du kan plukke varer fra hvert nummerskilt. **Tips:** Hvis du vil flytte et overordnet nummerskilt, må du bruke en mobilenhet som er konfigurert til å opprette arbeid for bevegelser.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Nummerskilt – bryt         | Del opp en nummerskilt-build, slik at du kan velge varer fra nummerskiltene som var i builden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Sjåførinnsjekking             | Hvis du bruker Transportstyring, registrerer du at en sjåfør har ankommet, ved å skanne ID-en for utgående last, avtale-ID-en eller forsendelses-ID-en. Dette krever at en last tilordnes til avtalen, og at statusen til lasten er **Lastet**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Sjåførutsjekking            | Registrer at en sjåfør har fullført avtalen sin.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Tøm hurtigbuffer for nummersekvens | Slett nummersekvensnumre fra nummersekvensbufferen. Denne aktiviteten utføres vanligvis av en systemadministrator for å løse problemer med hurtigbufring ved bruk av mobile enheter.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Endre partidisposisjon    | La en arbeider angi en partidisposisjonskode for en vare og et parti. Dette valget oppdaterer disposisjonskoden som er angitt for partiet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Vis liste over åpent arbeid      | Vis en liste over tilgjengelig arbeid for en bestemt bruker. Brukeren kan deretter velge arbeid som skal utføres, og vil bli dirigert til det. Denne listen er ment å vises på nettbrett med skjermstørrelser på 7 tommer eller mer. Når du velger dette alternativet, aktiveres menyelementene **Rediger spørring** og **Feltliste**. På siden **Rediger spørring** kan du definere kriterier for arbeid som vises i listen. På siden **Feltliste** kan du velge hvilke felt som vises i arbeidslisten. Du kan for eksempel redusere antall felt som vises, slik at brukeren raskere kan velge det mest aktuelle arbeidselementet. Du kan også velge hvor mange arbeidsposter som skal vises per side, i feltet **Poster per side** i hurtigfanen **Generelt**. Hvis det er merket av for **Tillat brukere å filtrere arbeid etter transaksjonstype**, inkluderer arbeidslisten en **Filtrer arbeid**-kontroll som brukeren kan bruke til å filtrere etter transaksjonstype. Brukere vil bare se arbeid i arbeidslisten som de har tilgang til. Du må kontrollere at brukere har tillatelse for ett eller flere brukerstyrte menyelementer som støtter den bestemte arbeidsklassetypene som de skal ha tilgang til. Tillatelser kontrolleres når en bruker forsøker å utføre arbeid fra listen. |

## <a name="configure-menu-items-to-create-work-for-another-worker-or-process"></a>Konfigurere menyelementer for å opprette arbeid for en annen arbeider eller prosess
Du kan definere et menyelement som oppretter arbeid for en annen arbeider etter at en innledende handling er utført på mobilenheten. Når én arbeider for eksempel bruker en mobilenhet til å motta en vare, opprettes det plasseringsarbeid for en annen arbeider. På siden **Menyelementer på mobilenheten** i **Modus**-feltet velger du **Arbeid** for å definere et menyelement som oppretter arbeid. I tabellen nedenfor er alternativene i feltet **Arbeidsopprettelsesprosess** ordnet etter arbeidsordretypen.

<table>
<tbody>
<tr>
<th>Arbeidsordretype</th>
<th>Alternativ</th>
<th>Beskrivelse</th>
</tr>
<tr>
<td rowspan="8">Bestilling</td>
<td>Mottak av bestillingslinje</td>
<td>Registrer mottaket av et antall av en vare ved hjelp av bestillingsnummeret og bestillingslinjenummeret, og opprett plasseringsarbeid for en annen arbeider.</td>
</tr>
<tr>
<td>Bestillingslinjen er mottatt og plassert</td>
<td>Registrer mottaket av et antall av en vare ved hjelp av bestillingsnummeret og bestillingslinjenummeret, og plasser varene. Samme arbeider utfører begge handlinger.</td>
</tr>
<tr>
<td>Mottak av bestillingsvare</td>
<td>Registrer mottaket av et antall av en vare for en bestilling ved å registrere bestillingsnummeret og varenummeret, og opprett plasseringsarbeid for en annen arbeider.</td>
</tr>
<tr>
<td>Motta og plassere bestillingsvarer</td>
<td>Registrer mottaket av et antall av en vare for en bestilling ved å registrere bestillingsnummeret og varenummeret, og plasser varen. Samme arbeider utfører begge handlinger.</td>
</tr>
<tr>
<td>Mottak av nummerskilt</td>
<td>Motta en innkommende last ved hjelp av nummerskilt-IDen.</td>
</tr>
<tr>
<td>Mottak og plassering av nummerskilt</td>
<td>Motta og plasser en innkommende last ved hjelp av nummerskilt-IDen.</td>
</tr>
<tr>
<td>Mottak av lastvare</td>
<td>Registrer mottaket av et antall for en last ved å bruke last-IDen, og opprett plasseringsarbeid for en annen arbeider. Varenummeret og produktdimensjonene samsvarer med kvitteringen til bestillingslinjene.</td>
</tr>
<tr>
<td>Mottak og plassering av lastvare</td>
<td>Registrer mottaket av et antall ved å bruke last-IDen, og plasser varene. Varenummeret og produktdimensjonene samsvarer med kvitteringen til bestillingslinjene. Samme arbeider utfører begge handlinger.</td>
</tr>
<tr>
<td>Returordre</td>
<td>Returordremottak</td>
<td>Registrer mottaket av et antall av en vare ved å registrere autorisasjonsreturnummeret, og opprett plasseringsarbeid for en annen arbeider.</td>
</tr>
<tr>
<td>Mottak og plassering av returordre</td>
<td>Registrer mottaket av et antall av en vare ved å registrere autorisasjonsreturnummeret, og plasser varene. Samme arbeider utfører begge handlinger.</td>
</tr>
<tr>
<td>Overføringsordre</td>
<td>Motta overføringsordrevare</td>
<td>Registrer mottaket av et antall av en vare, og opprett plasseringsarbeid for en annen arbeider.

<strong>Obs!</strong>Bruk dette alternativet bare hvis varene er levert fra et lager som ikke er aktivert for lagerstyringsprosesser.</td>
</tr>
<tr>
<td>Motta og plassere overføringsordrevare</td>
<td>Registrere mottaket av et antall av en vare, og plasser varene. Samme arbeider utfører begge handlinger.

<strong>Obs!</strong>Bruk dette alternativet bare hvis varene er levert fra et lager som ikke er aktivert for lagerstyringsprosesser.</td>
</tr>
<tr>
<td>Motta overføringsordrelinje</td>
<td>Registrer mottaket av et antall av en vare, og opprett plasseringsarbeid for en annen arbeider.</td>
</tr>
<tr>
<td>Mottak og plassering av overføringsordrelinje</td>
<td>Registrere mottaket av et antall av en vare, og plasser varene. Samme arbeider utfører begge handlinger.</td>
</tr>
<tr>
<td>Produksjon</td>
<td>Ferdigmeld</td>
<td>Registrere et antall av en ferdig vare som er fullført for en produksjon, og opprette plasseringsarbeid for en annen arbeider. Antallet kan være noe av eller hele antallet som ble planlagt for produksjon.</td>
</tr>
<tr>
<td>Ferdigmeld og plasser</td>
<td>Registrere et antall av en ferdig vare som er fullført for en produksjon, og plasser varene. Antallet kan være noe av eller hele antallet som ble planlagt for produksjon. Samme arbeider utfører begge handlinger.</td>
</tr>
<tr>
<td>Kanban</td>
<td>Angi at en Kanban er fullført, og opprett plasseringsarbeid for en annen arbeider.</td>
</tr>
<tr>
<td>Kanban plassert</td>
<td>Angi at en Kanban er fullført, og plasser varene. Samme arbeider utfører begge handlinger.</td>
</tr>
<tr>
<td>Beholdning</td>
<td>Bevegelse</td>
<td>Registrer at varer er flyttet fra én lokasjon til en annen. Arbeideren angir hvor varene skal flyttes fra og hvor de skal flyttes til.</td>
</tr>
<tr>
<td>Karantene</td>
<td>Endre statusen for lagerbeholdningen for et nummerskilt eller en lokasjon for å gjøre skadede eller manglende lagervarer utilgjengelige.</td>
</tr>
<tr>
<td>Flytting etter mal</td>
<td>Flytt varer fra én lokasjon til en annen på en delvis automatisert måte. Arbeideren velger lokasjonen som varer skal flyttes fra, og Finance and Operations bruker lokasjonsdirektivet til å avgjøre hvor varene skal flyttes.</td>
</tr>
<tr>
<td>Lageroverføring</td>
<td>Registrer at varer er overført fra ett lager til et annet. Dette alternativet krever at arbeideren har tillatelse til å utføre arbeid i begge lagre.

<strong>Obs!</strong> Dette menyelementet krever en standard lageroverføringsjournal der feltet for <strong>bilagstrekk</strong> er satt til <strong>Postering</strong>.</td>
</tr>
<tr>
<td>Nummerskiltlasting</td>
<td>Bruk dette alternativet når du klargjør lageret for første gang. Skann alle nummerskiltene i alle lokasjonene på lageret. Lokasjonene må være nummerskiltkontrollert Du kan ikke bruke dette alternativet hvis <strong>Serienummer</strong> eller <strong>Partinummer</strong> vises over <strong>Lokasjon</strong> i lagerreservasjonshierarkiet.</td>
</tr>
<tr>
<td>Syklustelling</td>
<td>Justering inn</td>
<td>Øk antallet av varer på lager. Angi lokasjonen, nummerskiltet, varen, antallet, måleenheten og statusen.</td>
</tr>
<tr>
<td>Justering ut</td>
<td>Reduser antallet av varer på lager. Angi lokasjonen, nummerskiltet, varen, antallet, måleenheten og statusen for beholdningen.</td>
</tr>
<tr>
<td>Spotsyklustelling</td>
<td>Start en telling for en lokasjon. Arbeideren må telle alle varene i lokasjonen. Når resultatet av en telling er mindre enn det forventede antallet, regnes det manglende antallet som et tap.</td>
</tr>
</tbody>
</table>

## <a name="configure-menu-items-to-process-existing-work"></a>Konfigurere menyelementer for å behandle eksisterende arbeid
I tillegg til å definere menyelementer for å opprette lagerarbeid, kan du definere menyelementer til å behandle arbeid som allerede er opprettet. Angi **Modus**-feltet til **Arbeid**, og velg alternativet **Bruk eksisterende arbeid**. Flere alternativer blir deretter tilgjengelig i **Generell**-kategorien. Du kan styre tilgang til menyelementet ved å tilordne én eller flere arbeidsklasser i hurtigkategorien **Arbeidsklasse**. Arbeidsklassene definerer arbeidet som kan behandles av menyelementet. Arbeidsklassen kan også brukes til å gi tilgang til bestemte brukerroller, eller til å skille behandling for ulike typer operasjoner. Følgende tabell beskriver alternativene som er tilgjengelige.

<table>




<thead>
<tr class="header">
<th>Alternativ</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ingen</td>
<td>Denne standardverdien behandler ikke arbeid.</td>
</tr>
<tr class="even">
<td>Systemstyrt</td>
<td>Microsoft Dynamics 365 for Finance and Operations kontrollerer hvilken type arbeid som er tilordnet til en arbeider, og rekkefølgen som arbeideren utfører arbeid i. Når du velger dette alternativet, kan du klikke <strong>Systemstyrt arbeid</strong> i handlingsruten for å åpne siden <strong>Systemstyrt sorteringsrekkefølge</strong>, der du kan definere sorteringskriterier for arbeidet. Sorteringskriteriene bestemmer i hvilken rekkefølge arbeideren vil utføre arbeidet. Du kan legge til så mange kriterier du vil.</td>
</tr>
<tr class="odd">
<td>Brukerstyrt</td>
<td>Arbeideren velger arbeidet som skal utføres og rekkefølgen det skal utføres i.</td>
</tr>
<tr class="even">
<td>Brukergruppering</td>
<td>Arbeideren grupperer arbeid manuelt. Dette alternativet er for eksempel nyttig når en arbeider kan velge flere varer samtidig på en lokasjon. Etter at arbeideren er ferdig med å plukke alle de nødvendige varene, kan han eller hun plassere dem.</td>
</tr>
<tr class="odd">
<td>Systemgruppering</td>
<td>Microsoft Dynamics 365 for Finance and Operations grupperer arbeid for arbeideren basert på et angitt felt. Plukkarbeid for eksempel, grupperes når en arbeider skanner en forsendelses-ID, last-ID eller alle verdier som kan koble hver arbeidsenhet. Hvis du velger dette alternativet, er følgende felt obligatoriske:
<ul>
<li><strong>Systemgrupperingsfelt</strong> – Velg feltet som arbeideren skanner for å gruppere arbeidet.</li>
<li><strong>Systemgrupperingsetikett</strong> – Skriv inn tekst for å informere arbeideren om hva som må skannes for å gruppere arbeidet.</li>
</ul></td>
</tr>
<tr class="even">
<td>Validert brukerstyrt</td>
<td>Arbeideren velger arbeidet som skal utføres når arbeid er tilknyttet en større enhet, for eksempel en last eller forsendelse. Arbeideren bestemmer hvilken rekkefølge varene skal plukkes i. Hvis du velger dette alternativet, er følgende felt obligatoriske:
<ul>
<li><strong>Validert brukerstyrt felt</strong> – Velg feltet som arbeideren skanner for å gruppere arbeidet.</li>
<li><strong>Validert brukerstyrt etikett</strong> – Angi teksten som informerer arbeideren om hva som skal skannes når plukkarbeid grupperes av systemet.</li>
</ul>
Dette alternativet er for eksempel nyttig når flere paller klargjøres for en last. Hvis du velger <strong>LoadId</strong> i feltet <strong>Validert brukerstyrt etikett</strong>, kan arbeideren velge en hvilken som helst pall som er knyttet til lasten. Arbeideren får en feilmelding hvis han eller hun skanner en vare som ikke er knyttet til lasten.</td>
</tr>
<tr class="odd">
<td>Gruppeplukking</td>
<td>Arbeidergruppene fungerer i klynger. Grupper gjør at arbeidere kan plukke varer fra én lokasjon for flere arbeidsordrer samtidig.</td>
</tr>
<tr class="even">
<td>Gruppering av syklustelling</td>
<td>Arbeideren velger en sone, arbeidspulje eller lokasjon, og Microsoft Dynamics 365 for Finance and Operations tilordner arbeid basert på valget. Hvis du velger dette alternativet, kan du klikke <strong>Syklustelling</strong> i handlingsruten for å angi tilleggsinformasjon du vil vise, og du kan også angi hvor mange ganger arbeideren må gjenta tellingen hvis det finnes en differanse.</td>
</tr>
</tbody>
</table>

## <a name="additional-menu-item-options"></a>Flere alternativer for menyelementer
Flere alternativer for menyelementer er tilgjengelige på siden **Menyelementer på mobilenheten**. Alternativene varierer avhengig av prosessen som du konfigurerer menyelementet for. 

Tabellen nedenfor beskriver disse alternativene.

<table>




<thead>
<tr class="header">
<th>Felt</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tillat arbeidsoppdeling</td>
<td>Velg dette alternativet for å la brukere plassere varer for en arbeidsordre i mer en ett målnummerskilt. Dette alternativet er for eksempel nyttig når et nummerskilt er fullt og arbeideren må legge til de gjenværende varene i et annet nummerskilt. Arbeideren kan klikke <strong>Full</strong> for å angi at nummerskiltet er fullt og slutte å motta plukkarbeid for det. Plasseringslokasjonen for de plukkede varene vil deretter vises, og plukkarbeidet som allerede er fullført, flyttes til en ny arbeidsordre. Gjenstående plukkarbeid for målnummerskiltet forblir på den opprinnelige arbeidsordren.</td>
</tr>
<tr class="even">
<td>Forankring</td>
<td>Velg dette alternativet for å tillate arbeidere å angi en lokasjon som overstyrer den foreslåtte oppsamlings- eller lastingslokasjonen. Alt gjenstående plasseringsarbeid sendes til den nye lokasjon. Dette alternativet er for eksempel nyttig når en arbeider må plassere varene for ordre 1 på en oppsamlingslokasjon ved Sone 1, men ikke kan gjøre det fordi en tidligere last ikke er fjernet fra lokasjonen. I stedet for å vente på at oppsamlingslokasjonen ved Sone 1 blir tilgjengelig, kan arbeideren bestemme å bruke oppsamlingslokasjonen ved Sone 2. I slike tilfeller overstyrer arbeideren oppsamlingslokasjonen. Plasseringslokasjonen hvor alle de andre elementene for arbeidsordren oppdateres deretter til oppsamlingslokasjonen for Sone 2. Hvis du velger dette alternativet, må du angi <strong>Forankre etter</strong>-feltet.</td>
</tr>
<tr class="odd">
<td>Forankre etter</td>
<td>Hvis du bruker forankring, må du angi om du vil forankre etter levering eller etter last.</td>
</tr>
<tr class="even">
<td>ID for revisjonsmal</td>
<td>Velg arbeidsrevisjonsmalen som vil avbryte arbeidsprosessen for dette menyelementet, slik at en annen operasjon kan utføres. Hvis dette menyelementet for eksempel er for innkommende varer, kan revisjonsmalen kreve at arbeideren kontrollerer temperaturen i leveringscontaineren. Punktet der denne prosessen avbrytes er angitt i revisjonsmalen. Dette punktet kan for eksempel være når arbeid er startet eller fullført, eller når statusen endres.</td>
</tr>
<tr class="odd">
<td>Gruppeprofil-ID</td>
<td>Velg gruppeprofilen som skal brukes til gruppeplukking. Gruppeprofilen inneholder innstillinger som hvorvidt klynger skal opprettes automatisk, navn på stillinger og hvor mange arbeidsenheter som de kan tilordnes, når grupper skal deles inn i enkeltenheter, og om det kreves bekreftelse. Dette feltet er bare tilgjengelig hvis <strong>Gruppeplukking</strong> er valgt i <strong>Styrt av</strong>-feltet.</td>
</tr>
<tr class="even">
<td>Tell totalt vareantall først</td>
<td>Velg dette alternativet for å kreve at en arbeider teller det totale antallet først under en telling. Hvis det finnes en differanse, må arbeideren angi tilleggsinformasjon, for eksempel nummerskiltnummeret, partinummeret, serienumrene og så videre.</td>
</tr>
<tr class="odd">
<td>Opprett bevegelse</td>
<td>Velg dette alternativet for gjøre det mulig for en arbeider å opprette arbeid for en bevegelse, uten at arbeideren skal være nødt til å utføre arbeidet umiddelbart. Dette er for eksempel nyttig hvis en kvalitetskontroll er fullført, og kontrolløren ønsker at varen flyttes fra kvalitetsinspeksjonsområdet.</td>
</tr>
<tr class="even">
<td>Direktivkode</td>
<td>Hvis du vil bruke et bestemt lokasjonsdirektiv, velger du direktivkoden som er tilknyttet lokasjonsdirektivet. Dette feltet er tilgjengelig når du oppretter arbeid og arbeidsopprettelsesprosessen er <strong>Flytting etter mal</strong>.</td>
</tr>
<tr class="odd">
<td>Deaktiver terskler for syklustelling</td>
<td>Velg dette alternativet for å ignorere tersklene i syklustellingen. Hvis du merker av for dette alternativet, opprettes ikke syklustellingsarbeid når terskelverdier overskrides.</td>
</tr>
<tr class="even">
<td>Vis partidisposisjonskode</td>
<td>Velg dette alternativet hvis du vil vise partidisposisjonskoder. Du kan for eksempel vise partidisposisjonskoder når du mottar et returnert parti. Arbeidere kan deretter evaluere statusen eller kvaliteten på et parti, og velge den aktuelle koden. Reglene på partidisposisjonskoden bestemmer om partiet blir tilgjengelig for andre lagerprosesser. Hvis du ikke velger dette alternativet, brukes ett av følgende partidisposisjonskoder:
<ul>
<li>Hvis du mottar et nytt partinummer, brukes standard partidisposisjonskode som er angitt i varemodellgruppen.</li>
<li>Partidisposisjonskode som allerede er tilordnet til den satsvise jobben.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vis disposisjonskode</td>
<td>Velg dette alternativet hvis du vil vise disposisjonskoder. Du kan for eksempel vise disposisjonskoder når du mottar returvarer. Arbeidere kan deretter evaluere statusen eller kvaliteten på varene, og velge den aktuelle koden. Reglene på partidisposisjonskoden bestemmer om varene blir tilgjengelige for andre lagerprosesser.</td>
</tr>
<tr class="even">
<td>Vis beholdningsstatus</td>
<td>Velg dette alternativet for å vise status for varer på lager. Dette alternativet er tilgjengelig for alle menyelementer som bruker eksisterende arbeid, unntatt syklustelling.</td>
</tr>
<tr class="odd">
<td>Vis sammendrag for plukkskjermbilde</td>
<td>Velg dette alternativet for å vise et sammendrag av plukkarbeidet for den valgte arbeidsordren. Sammendraget vises til den første arbeidslinjen behandles for arbeidsordren.</td>
</tr>
<tr class="even">
<td>Generer nummerskilt</td>
<td>Velg dette alternativet for å generere et unikt skiltnummer basert på den valgte nummerserien. Du kan for eksempel generere et nummerskilt for varene som er mottatt for bestillinger.</td>
</tr>
<tr class="odd">
<td>Gruppe plassert</td>
<td>Velg dette alternativet for å gruppere plasseringsarbeidet. Dette alternativet er tilgjengelig når arbeidet ble gruppert av arbeideren eller av Microsoft Dynamics 365 for Finance and Operations. Når arbeideren er ferdig med alt plukkarbeidet i gruppen, opprettes plasseringsarbeid for den samme gruppen.</td>
</tr>
<tr class="even">
<td>Lagerjusteringstyper</td>
<td>Velg lagerjusteringstypen som bestemmer lageropptellingsjournalen som brukes til å postere justeringen, og hvorvidt reservasjoner skal fjernes. Dette feltet er bare tilgjengelig for arbeidsopprettelsesprosessene <strong>Justering inn</strong> eller <strong>Justering ut</strong>.</td>
</tr>
<tr class="odd">
<td>Overstyr partinummer</td>
<td>Velg dette alternativet for å tillate arbeidere som rapporterer et antall som ferdigmeldt for en produksjonsordre, å angi et partinummer som er forskjellig fra partinummeret som er tilordnet produksjonsordren.</td>
</tr>
<tr class="even">
<td>Overstyr målnummerskilt</td>
<td>Velg dette alternativet for å tillate arbeidere å angi et målskiltnummer som er forskjellig fra det foreslåtte målskiltnummeret. Bruk dette alternativet hvis første plukking for en arbeidsordre gjelder hele antallet for en vare på et nummerskilt. Dette er for eksempel nyttig når du bruker en pall på nytt.</td>
</tr>
<tr class="odd">
<td>Plukk og pakk</td>
<td>Velg dette alternativet for å tillate arbeidere å kombinere arbeid for en salgsordre eller last i en enkelt arbeidsenhet. En arbeider kan bare utføre arbeid for salgsordren eller lasten. Dette er for eksempel nyttig når du må øke et antall for en salgsordre etter at lasten, leveringen og arbeidet er opprettet for salgsordren. Dette alternativet er tilgjengelig når menyelementet bruker eksisterende arbeid, og arbeidet styres av brukeren eller systemet.</td>
</tr>
<tr class="even">
<td>Ingen</td>
<td>Angir om arbeideren først må velge det eldste partiet på lokasjonen. Følgende alternativer er tilgjengelige:
<ul>
<li><strong>Ingen</strong> – Arbeideren kan plukke et hvilket som helst parti i lokasjonen. Arbeideren mottar ingen melding.</li>
<li><strong>Advarsel</strong> – Arbeideren kan plukke et hvilken som helst parti i lokasjonen, men det vises en advarsel hvis partiet ikke er det eldste.</li>
<li><strong>Fremtving</strong> – Arbeideren må velge det eldste partiet i lokasjonen. Arbeideren får en feilmelding hvis et parti ikke er det eldste partiet. <strong>Obs!</strong> Dette alternativet gjelder bare hvis <strong>Partinummer</strong> er lavere enn <strong>Lokasjon</strong> i reserveringshierarkiet som er tilordnet til varen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skriv ut etikett</td>
<td>Velg dette alternativet for å tillate arbeidere å skrive ut etiketter for nummerskilt.</td>
</tr>
<tr class="even">
<td>Systemgrupperingsfelt</td>
<td>Velg feltet som bestemmer hvordan Microsoft Dynamics 365 for Finance and Operations grupperer plukkarbeid for arbeidere. Hvis du for eksempel felger <strong>ShipmentId</strong>-feltet vil arbeideren skanne forsendelses-IDen for å gruppere plukkarbeidet. Alt arbeid for forsendelsen tilordnes deretter til arbeideren. Dette feltet krever at du oppretter et menyelement for å bruke eksisterende arbeid som er gruppert av systemet. Du må også skrive inn tekst i feltet <strong>Systemgrupperingsetikett</strong> for å informere arbeideren om hva som må skannes.</td>
</tr>
<tr class="odd">
<td>Systemgrupperingsetikett</td>
<td>Angi teksten som skal informere arbeideren om hva som skal skannes når plukkarbeid grupperes av Microsoft Dynamics 365 for Finance and Operations. Hvis du for eksempel bruker <strong>ShipmentId</strong>-feltet til å gruppere plukkarbeid etter forsendelse, kan du angi <strong>Forsendelses-ID</strong> i feltet. Dette feltet krever at du oppretter et menyelement for å bruke eksisterende arbeid som er gruppert av systemet. Du må også velge feltet du vil gruppere etter i <strong>Systemgrupperingsfelt</strong>-feltet.</td>
</tr>
<tr class="even">
<td>Bruk standarddata</td>
<td>Velg dette alternativet for å aktivere <strong>Standarddata</strong>-knappen i handlingsruten, der du kan velge feltene for å vise data som en arbeider vanligvis trenger i det daglige arbeidet. Dette er for eksempel nyttig hvis en arbeider ofte plukker varer fra samme lokasjon. Du kan velge <strong>Fra lokasjon</strong>-feltet for å vise lokasjonen som standard.</td>
</tr>
<tr class="odd">
<td>Validert brukerstyrt felt</td>
<td>Velg feltet som arbeideren skal skanne for å gruppere arbeidet. Hvis du for eksempel velger<strong>LoadId</strong>, kan en arbeider plukke alt arbeid som tilknyttet en valgt last. Du må også skrive inn tekst i feltet <strong>Validert brukerstyrt etikett</strong> for å informere arbeideren om hva som må skannes.</td>
</tr>
<tr class="even">
<td>Validert brukerstyrt etikett</td>
<td>Angi teksten som vil informere arbeideren om hva som skal skannes når plukkarbeid grupperes av et validert brukerrettet felt. Hvis du for eksempel bruker <strong>LoadId</strong>-feltet til å gruppere plukkarbeid for en last, kan du angi <strong>Last-ID</strong> i feltet.</td>
</tr>
<tr class="odd">
<td>Arbeidsmalkode</td>
<td>Velg arbeidsmalen som oppretter arbeidet for en prosess. Hvis du for eksempel mottar en vare for en bestilling, blir plasseringsarbeidet generert basert på arbeidsmalen. Hvis du ikke velger en arbeidsmal, tilordner Microsoft Dynamics 365 for Finance and Operations en mal basert på spørringskriterier. Hvis du vil ha mer informasjon om arbeidsmaler, kan du se <a href="control-warehouse-location-directives.md">Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver</a>.</td>
</tr>
</tbody>
</table>

## <a name="require-workers-to-confirm-the-product-location-or-quantity-when-they-pick-items"></a>Krev at arbeidere bekrefter produktet, lokasjonen eller antallet ved plukking av varer
Du kan definere arbeidsbekreftelser som krever at en arbeider bruker en mobilenhet til å registrere lokasjonen eller antallet når det utføres arbeid på lageret. Arbeidsbekreftelser bidrar til å sikre at arbeideren er på riktig sted, eller behandler det riktige antallet varer. Du kan også få Microsoft Dynamics 365 for Finance and Operations til å bekrefte arbeiderens registrering automatisk. Hvis du aktiverer automatisk bekreftelse, kan du ikke også kreve bekreftelser for lokasjon eller antall. Arbeidsbekreftelser inneholder også produkter og produktvarianter. I tillegg kan du registrere bekreftelser ved å skanne en strekkode. Hvis du vil bekrefte produkter og produktvarianter, må du angi en ID for produktet eller produktvarianten. Denne IDen kan være en produkt-ID, produktsøk-ID, ekstern ID, GTIN eller strekkode. Når du har angitt ID-en eller skannet strekkoden, vises dimensjonene for produktvarianten på mobilenheten. 

Tabellen nedenfor beskriver de ulike arbeidstypene som du kan bruke arbeidsbekreftelser med.

| Alternativ                 | Beskrivelse                                                                |
|------------------------|----------------------------------------------------------------------------|
| Plukk                   | Krev bekreftelse ved plukking av varer.                                |
| Plasser                    | Krev bekreftelse ved plassering av varer på en lokasjon.                     |
| Opptelling               | Krev bekreftelse under syklustelling.                                |
| Justeringer            | Krev bekreftelse ved justering av lagerantallet.               |
| Tilpasset                 | Krev bekreftelse for egendefinert arbeid.                                      |
| Karantene             | Krev bekreftelse ved flytting av varer til karantene.                   |
| Nummerskiltbygging | Krev bekreftelse ved konsolidering av varene for å bygge et nummerskilt. |
| Skriv ut                  | Krev bekreftelse ved utskrift av etiketter for nummerskilt.                |
| Statusendring          | Krev bekreftelse når du endrer lagerstatusen.              |

**Obs!** Du kan kreve produktbekreftelse bare for arbeid av plukkings- og plasseringstyper.

<a name="see-also"></a>Se også
--------

[Visningsinnstillinger for lagermobilenheten](change-warehouse-mobile-device-displays.md)

[Definere et menyelement for mobilenhet for å fullføre arbeid av typen Bestilling (oppgaveveiledning)](tasks/set-up-mobile-device-menu.md)

[Definere et menyelement for mobilenhet for å registrere mottatte varer (oppgaveveiledning)](tasks/set-up-mobile-device-menu-item-register-received-items.md)
[Fordeler ved å bruke lagerstatuser](../inventory/inventory-statuses.md)




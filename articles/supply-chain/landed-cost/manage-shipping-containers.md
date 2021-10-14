---
title: Administrere forsendelsescontainere
description: Dette emnet beskriver hvordan du arbeider med forsendelsescontainere. Forsendelsescontainere brukes til å gruppere varer som er fysisk gruppert sammen. De brukes også i tilfeller der kostnader bare må deles på tvers av disse varene, vanligvis fordi de er fysisk sammen.
author: sherry-zheng
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: d3a47aa2ae36cd36a7e92aa2503252021e03f739
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573783"
---
# <a name="manage-shipping-containers"></a>Administrere forsendelsescontainere

[!include [banner](../../includes/banner.md)]

Forsendelsescontainere brukes til å gruppere varer som er fysisk gruppert sammen. De brukes også i tilfeller der kostnader bare må deles på tvers av disse varene, vanligvis fordi de er fysisk sammen.

Hvis du vil vise og behandle varer via siden for forsendelsescontainere, kan du gå til **Netto innkjøpspris \> Forsendelsescontainere \> Alle forsendelsescontainere**. Siden **Alle forsendelsescontainere** viser en liste over alle tilgjengelige forsendelsescontainere. Du kan bruke knappene i handlingsruten til å opprette, slette og arbeide med forsendelsescontainere. Velg en forsendelsescontainer i listen for å vise detaljer om den på siden **Forsendelsescontainere**.

Den øvre delen av siden for detaljer om forsendelsescontainer viser informasjon om forsendelse og etterkalkulering. Delen **Linjer** viser folioene, varene og bestillingene eller overføringsordrene som er knyttet til containeren.

## <a name="action-pane"></a>Handlingsrute

Handlingsruten på sidene **Alle forsendelsescontainere** og **Forsendelsescontainere** inneholder knapper du kan bruke til å arbeide med en valgt forsendelsescontainer. Hver knapp utfører én handling. Handlingsruten inneholder også faner, der hver av dem igjen inneholder et sett med relaterte knapper. Med unntak av der det er bemerket, er alle knapper og faner som er beskrevet i følgende underdeler, tilgjengelige både i listevisningen (det vil si på siden **Alle forsendelsescontainere**) og i den detaljerte visningen (det vil si på siden **Forsendelsescontainere**).

### <a name="buttons-on-the-manage-tab"></a>Knapper i fanen Administrer

Tabellen nedenfor beskriver knappene som er tilgjengelige i handlingsruten på siden **Administrer**.

| Knapp | Beskrivelser |
|---|---|
| Poster tilgangsliste | Poster en mottaksliste eller vis produktmottakslistene for alle bestillingslinjer i forsendelsescontaineren. Hvis det brukes flere firmaforsendelser, åpnes det en ny posteringsdialogboks for mottaksliste for hvert firma. |
| Poster mottaksseddel | Poster en produktkvittering for alle bestillingslinjer i forsendelsescontaineren. |
| Poster faktura | Poster en faktura for alle bestillingslinjer i forsendelsescontaineren. Hvis det brukes flere forsendelser, åpnes det en ny dialogboks for fakturapostering for hvert firma. |
| Send overføringsordre | Poster en forsendelse for overføringsordre for alle overføringsordrelinjer i forsendelsescontaineren. Bare linjene i forsendelsescontaineren som er en type overføringsordre, vises i dialogboksen. |
| Motta overføringsordre | Poster en kvittering for overføringsordre for alle overføringsordrelinjer i forsendelsescontaineren. Dialogboksen for mottak er den enkleste måten å motta varer på i en forsendelsescontainer eller forsendelse, og er ett av tre tilgjengelige alternativer. Du kan også motta via ankomstjournaler eller behandling av mobilenheter. |
| Opprett ankomstjournal | Du kan generere en ankomstjournal for organisasjoner ved hjelp av avanserte lagerfunksjoner. Alternativen er _Initialiser antall_ (anbefales), og _Opprett fra varer i transitt_ eller _Opprett fra bestillinger_. De siste to alternativene avhenger av om behandling av varer i transitt brukes. |
| Gi nytt navn | Åpne en dialogboks der du kan gi nytt navn til en valgt forsendelsescontainer. |
| Endre reisemal | Endre reisemalen. Når du har endret reisemalen, kan det hende at du må velge **Søk etter automatiske kostnader** eller legge til kostnader manuelt igjen, fordi forsendelseskostnadene vil bli slettet. |
| Konverter til leie | Konverter en valgt forsendelsescontainer til en forsendelsescontainer for leie. |

### <a name="buttons-on-the-general-tab"></a>Knapper i fanen Generelt

Tabellen nedenfor beskriver knappene som er tilgjengelige i handlingsruten på siden **Generelt**.

| Knapp | Beskrivelser |
|---|---|
| Tilgangsliste | Poster en mottaksliste for alle bestillingslinjer i forsendelsescontaineren. Hvis det brukes flere sjøreiser, åpnes det en ny dialogboks for mottakslistepostering for hvert firma. |
| Produktkvittering | Vis produktmottaksposten, hvis den brukes. Produktmottaksprosessen brukes bare hvis varene ikke bruker funksjonaliteten for varer i transitt. |
| Vareankomst | Vis vareankomstjournalen for forsendelsescontaineren, hvis den journalen brukes. |
| Strekninger | Etapper brukes til å identifisere atskilte deler av en reise. Leveringstiden kan knyttes til hver etappe for å få hjelp til forsendelsessporing. Hvis du vil ha mer informasjon, kan du se [Oppsett for reise med flere etapper](multi-leg-journey-setup.md). |
| Sporing | Vis eller oppdater forsendelsessporing. |
| Varer i transitt-ordrer | Du kan åpne siden **Varer i transitt** direkte fra containeren. Denne siden viser poster for varer i transitt bare for den valgte forsendelsescontaineren. |

## <a name="header-view"></a>Topptekstvisning

Hvis du vil åpne visningen **Topptekst**, åpner du en forsendelsescontainer, og deretter velger du fanen **Topptekst** øverst til høyre i overskriften i forsendelsescontaineren.

### <a name="settings-on-the-general-fasttab"></a>Innstillinger i hurtigfanen Generelt

I tabellen nedenfor beskrives innstillingene som er tilgjengelige i hurtigfanen **Generelt** i visningen **Topptekst** for en forsendelsescontainer.

| Felt | beskrivelse |
|---|---|
| Fraktcontainer | Navnet på forsendelsescontaineren. |
| Sjøreise | Sjøreisen som er knyttet til forsendelsescontaineren. |
| Fraktcontainertype | Angi typen forsendelsescontainer. Dette feltet må angis. Du kan bruke det til å fastslå kostnaden for frakt, for eksempel ved å velge den automatiske kostnaden som er knyttet til typen forsendelsescontainer. |
| Fartøy | Angi eller velg fartøyet. Hvis fartøyet ikke er oppført som en verdi, kan du angi fartøy-ID-en som fritekst. I så fall oppdateres ikke hovedtabellen slik at du kan velge fartøy-ID-en i dette feltet senere. Hvis du vil ha mer informasjon, kan du se [Transportmidler](shipping-information-setup.md#vessels). |
| Enhetstype | Enhetstyper brukes som en ekstra måte å gruppere og identifisere forsendelsescontainere på. De vises og velges på siden for forsendelsescontainer. Hvis du vil ha mer informasjon, kan du se [Definere enhetstyper](shipping-container-setup.md#unit-types). |
| Kjøletype | Kjøletyper brukes som en ekstra måte å gruppere og identifisere forsendelsescontainere på, vanligvis kjølecontainere. De vises og velges på siden for forsendelsescontainer. Hvis du vil ha mer informasjon, kan du se [Definere kjøletyper](shipping-container-setup.md#refrigeration-types). |
| Mål | Ved hjelp av dette feltet kan det angis et mål i modulen **Netto innkjøpspris**. Mål brukes ofte av organisasjoner som ikke kjenner til det enkelte volumet eller vekten av varer, men som krever en mer nøyaktig fordeling enn alternativene Beløp eller Antall leverandører. Fraktspeditøren vil formidle vekten i kilo eller kubikkmålet til organisasjonen, og du kan plassere den på nivå med en vare eller bestillingen. Det kan oppdateres automatisk hvis parameteren er valgt, eller det kan angis manuelt. |
| Måleenhet | Måleenheten som gjelder for tallet i feltet **Mål**. |
| Faktisk vekt | Du kan registrere den faktiske vekten til kartongen eller containeren. Denne verdien kan brukes for verifisering mot den maksimale vekten som er tillatt i oppsettet av en forsendelsescontainer. |
| Antall kartonger | Antall kartonger oppdateres automatisk hvis parameteren er valgt. |
| Beskrivelse av varer | Du kan velge en beskrivelse av varer i forsendelsescontaineren eller foliotopptekst. Den brukes til å identifisere en sjøreise, forsendelsescontainer eller en folio med varer. Hvis du vil ha mer informasjon, kan du se [Beskrivelse av varer](shipping-information-setup.md#description-of-goods). |
| HAWB/fraktbrev | Du kan angi flyfraktbrevet eller fraktbrevet til forsendelsescontaineren. |
| Kommentarer | Tilleggsinformasjon som er knyttet til forsendelsescontaineren. |
| Returnerbar | En verdi som angir om forsendelsescontaineren kan returneres etter sjøreisen. |
| Sjøreisestatus | Statusen til reisen som er knyttet til forsendelsescontaineren. |
| Bestillingsstatus | Statusen til bestillingen som er knyttet til forsendelsescontaineren. |

### <a name="settings-on-the-delivery-fasttab"></a>Innstillinger i hurtigfanen Levering

I tabellen nedenfor beskrives innstillingene som er tilgjengelige i hurtigfanen **Levering** i visningen **Topptekst** for en forsendelsescontainer.

| Felt | beskrivelse |
|---|---|
| Opprettingsdato og -klokkeslett | Datoen og klokkeslettet da containeren ble opprettet. |
| Dato for ab fabrikk | Denne datoen formidles vanligvis til fabrikken/leverandøren for å vise når du forventer at varene skal forlate lokalene. Når du samarbeider med en fabrikk i Asia, er denne datoen ofte nødvendig i stedet for datoen du forventer varene innen. (I motsetning til en lokal levering, er datoen du forventer varene på, obligatorisk.) Dette feltet kan fylles ut fra bestillingslinjene i listen for forsendelsescontainer. Du kan også angi feltet manuelt her. |
| Forsendelsesdato | Denne datoen kan skrives ut på bestillingsdokumentet. Datoen informerer vanligvis fabrikken/leverandøren om datoen varene skal leveres til havnen innen. Dette feltet er bare beregnet til informasjon. Den vil ikke bli brukt til å estimere den forventede leveringsdatoen for varene i forsendelsescontaineren. Dette feltet kan settes til at det automatisk oppdateres når sporingskontrollsiden oppdateres. |
| Til butikk-dato | Den tidligste datoen da varene fra bestillingene som er koblet til forretningsforbindelsen, vil være tilgjengelige for salg.|
| Estimert leveringsdato | Vanligvis er dette datoen da varene skal ankomme til lageret. Dette feltet er bare beregnet til informasjon. Den trenger ikke brukes til å beregne hovedplanleggingen på bestillingslinjene i forsendelsescontaineren. Den forventede leveringsdatoen på bestillingslinjene oppdateres ved hjelp av sporingskontroll. Dette feltet kan settes opp slik at det oppdateres når sporingskontrollsiden oppdateres. |
| Avreisedato | Vanligvis datoen da flyet eller fartøyet faktisk forlater havnen i utlandet. |
| Beregnet ankomst ved forsendelseshavn | Estimert ankomsttid ved målhavnen ("til"-havn). |
| Opprinnelige dokumenter mottatt | Valgfritt: Oppdater datoen da de opprinnelige dokumentene ble mottatt. |
| Megler informert | Valgfritt: Oppdater datoen da mekleren ble rådført. |
| Opprinnelig fraktbrev sendt | Valgfritt: Oppdater datoen da det opprinnelige fraktbrevet ble sendt. |
| Varer frigitt | Valgfritt: Oppdater datoen da de varene ble frigitt. |
| Kundeavtale | Valgfritt: Oppdater kundeavtaledatoen. |
| Levert ved lager | Valgfritt: Oppdater datoen da varene ble levert til lageret. |
| Bekreftelsesdato | Valgfritt: Oppdater verifiseringsdatoen. |
| Leveringsinstruksjoner | Valgfritt: Oppdater datoen for leveringsinstruksjonene. |
| Fra-havn | Havnen som varene skal sendes fra. |
| Til-havn | Havnen som varene skal sendes til. |
| Lokal videresender | Dette feltet er bare beregnet til informasjon. Den lokale speditøren bør kunne velges fra leverandørtabellen. |
| Dato for lokal transport | Angi datoen som den lokale transporten er bestilt for. Dette feltet kan hjelpe lageret med planlegging. |
| Klokkeslett for lokal transport | Angi tidspunktet. Dette feltet kan hjelpe lageret med planlegging. |
| Reisemal | Reisemalen som er angitt for sjøreisen. Reisemalen inneholder detaljene for til- og fra-havnene, og leveringstidene som er knyttet til sporingskontroll av forsendelsescontaineren. |

### <a name="settings-on-the-other-fasttab"></a>Innstillinger i hurtigfanen Annet

I tabellen nedenfor beskrives innstillingene som er tilgjengelige i hurtigfanen **Annet** i visningen **Topptekst** for en forsendelsescontainer.

| Felt | beskrivelse |
|---|---|
| Utleie | Verdi som angir om forsendelsescontaineren er en forsendelsescontainer for leie. Leiepriser kan knyttes til leiecontainere. |
| Konvertert til leie | Verdi som angir om forsendelsescontaineren ble konvertert til en forsendelsescontainer for leie. Leiepriser kan knyttes til leiecontainere. |
| Original sjøreise | Hvis forsendelsescontaineren ble flyttet til en ny sjøreise, den opprinnelige sjøreisen. |
| Brukt | Bruk denne til å registrere om det er brukt en forsendelsescontainer for leie. Den er bare til informasjon. |
| Forventet lastedato | Datoen da forsendelsescontaineren forventes å bli lastet med varer. |
| Vårt serienummer | Angi serienummeret som firmaet bruker internt for forsendelsescontaineren. |
| Serienummer for forsendelsesfirma | Angi serienummeret som forsendelsesfirmaet eller agenten angav for forsendelsescontaineren. |
| Ikrafttredelsesdato for undersøkelsessertifikat | Datoen da det ble bedt om en kontroll av forsendelsescontaineren. |
| Mottaksdato for undersøkelsessertifikat | Datoen da kontrollsertifikatet ble mottatt. |
| Utløpsdato for undersøkelsessertifikat | Datoen da kontrollsertifikatet utløper. |
| Undersøkelsessertifikatnummer | Sertifikatnummeret som ble utstedt etter at en kontroll ble utført. |

## <a name="lines-view"></a>Visningen Linjer

Hvis du vil åpne visningen **Linjer**, åpner du en forsendelsescontainer, og deretter velger du fanen **Linjer** øverst til høyre i overskriften i forsendelsescontaineren.

### <a name="information-on-the-shipping-container-fasttab"></a>Informasjon om hurtigfanen Forsendelsescontainer

Hurtigfanen **Forsendelsescontainer** i visningen **Linjer** viser informasjon om folioen. Mesteparten av denne informasjonen vises også i visningen **Topptekst**, som beskrevet tidligere i dette emnet.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Informasjon og knapper i hurtigfanen Linjer

Hurtigfanen **Linjer** i visningen **Linjer** viser detaljer om alle fullstendige eller delvise bestillingslinjer som er inkludert i gjeldende forsendelsescontainer.

Følgende tabell beskriver knappene som er tilgjengelige i hurtigfanen **Linjer** i visningen **Linjer**.

| Knapp | beskrivelse |
|---|---|
| Fjern | Fjern den valgte bestillingslinjen fra sjøreisen. |
| Lager \> Transaksjoner | Vis lagertransaksjoner for den valgte bestillingslinjen. Vær oppmerlsom på at dersom du bruker varer i transitt, vises også den opprinnelige ordren og ordrene for varer i transitt. |
| Lager \> Visningsdimensjoner | Åpne en dialogboks der du kan velge lagerdimensjonene som vises for transaksjonene du viser. |
| Forny | Oppdater informasjon som er knyttet til linjebeløpet, vekten eller volumet for den valgte bestillingslinjen. |

### <a name="information-on-the-lines-details-fasttab"></a>Informasjon i hurtigfanen Linjedetaljer

Hurtigfanen **Linjedetaljer** i visningen **Linjer** viser detaljer om bestillingslinjen som for øyeblikket er valgt i hurtigfanen **Linjer**.

---
title: Netto innkjøpspris vs. Transportstyring
description: 'Microsoft Dynamics 365 Supply Chain Management tilbyr to forskjellige moduler for arbeid med transport: Transportstyring (TMS) og Netto innkjøpspris. Dette emnet oppsummerer funksjonaliteten de to modulene har til felles, og fremhever forskjellene mellom dem.'
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 244d378316caf639c3520a1179dd82955d94220a
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909481"
---
# <a name="landed-cost-vs-transportation-management"></a>Netto innkjøpspris vs. Transportstyring

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management tilbyr to forskjellige moduler for arbeid med transport: **Transportstyring** (TMS) and **Netto innkjøpspris**. Dette emnet oppsummerer funksjonaliteten de to modulene har til felles, og fremhever forskjellene mellom dem. Du kan bruke denne informasjonen til å avgjøre hvilken modul som passer best til din forretningspraksis. Du vil kanskje finne ut at en forretningspraksis fungerer bedre med TMS, mens en annen fungerer best med Netto innkjøpspris. Avhengig av forretningskravene kan du deretter velge å bruke én modul eksklusivt, eller du kan kombinere de to modulene.

Dette emnet er ikke en omfattende gjennomgang av alle funksjonene i hver modul. I stedet fremhever det den tilgjengelige funksjonaliteten i forhold til transport av varer fra en leverandør til forretningens lager, der den kan forbrukes.

## <a name="terminology-reference-data-and-reporting-differences"></a>Terminologi, referansedata og rapporteringsforskjeller

### <a name="terminology-comparison"></a>Terminologisammenligning

TMS og Netto innkjøpspris bruker forskjellige termer for lignende begreper. Tabellen nedenfor summerer disse termene og bruken av dem i de to modulene.

| TMS-term | Netto innkjøpspris-term | Notater |
|----------|------------------|-------|
| **Belastning**<p>En *last* er en samling forsendelser som transporteres samtidig på samme transportenhet (for eksempel en trailer eller et skip). Laster kan være enten innkommende eller utgående.</p> | **Sjøreise**<p>En *sjøreise* er som regel ett transportmiddel som fullfører én *reise*. En sjøreise kan inneholde flere *forsendelsescontainere*, og den kan også inkludere innkommende ordrer fra forskjellige juridiske enheter i organisasjonen. Sjøreiser kan bare være innkommende.</p> | TMS bruker også termen *sjøreisenummer*, som refererer til et informasjonsfelt der du kan angi en identifikator. Funksjonaliteten er imidlertid ikke knyttet til TMS-feltet, og den er ikke knyttet til konseptet *sjøreise* i Netto innkjøpskost. |
| **Rute**<p>En *rute* er den geografiske banen til en transport fra opprinnelse til mål.</p> | **Reise**<p>En *reise* er den abstrakte varigheten av en transport fra opprinnelse til mål. Hver sjøreise må tilordnes en reise.</p> | |
| **Rutesegmenter**<p>En rute kan ha flere *rutesegmenter*, og hver av disse representerer et trinn i reisen. En rute kan omfatte flere transportører eller tjenester, som hver betraktes som et rutesegment.</p> | **Strekninger**<p>Hver reise kan ha flere *etapper*, og hver av disse representerer et trinn i reisen. En etappe kan være del av transporten, tollhåndtering eller en annen aktivitet.</p> | |
| **Containere**<p>En *container* kan være hvilken som helst type pakke eller emballasje som brukes av TMS.</p> | **Fraktcontainere**<p>En *forsendelsescontainer* er en bokstavelig, fysisk forsendelsescontainer, som kjent fra containerskip.</p> | |
| **Artikkelkoder**<p>I TMS (og andre steder i Supply Chain Management) identifiserer *artikkelkoder* typer artikler. De kan påvirke tariffer, håndtering av farlige materialer og så videre.</p> | **Artikkelkoder**<p>I Netto innkjøpspris er *artikkelkoder* etablert på nivået til den juridiske enheten. De brukes for det meste til rapportering.</p> | Netto innkjøpspris kan også bruke artikkelkodene som brukes for TMS og andre steder i Supply Chain Management. Artikkelkodene for Netto innkjøpspris brukes imidlertid bare av Netto innkjøpspris. |

### <a name="some-reference-data-isnt-shared"></a>Noen referansedata deles ikke

TMS og Netto innkjøpspris deler ikke referansedata for enheter som kostnadsoppsett, reiser og etapper. Hvis du bruker begge modulene, må du opprette referansedataene som ikke er delt, på nytt.

### <a name="intercompany-reports-dont-work-with-goods-in-transit"></a><a name="intercompany-reports"></a>Konserninterne rapporter fungerer ikke med varer i transitt

Følgende rapporter fungerer ikke sammen med funksjonen for varer i transitt som Netto innkjøpspris gir:

- [Rapporten Totalsummer for konserninterne varer i transitt](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)
- [Rapporten Totalsummer for konserninterne varer i transitt](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)

Disse rapportene forutsetter at varer settes i transitt så snart du har utstedt en salgsfølgeseddel, og at de tas til lager fra transitt ved mottak. Varer i transitt behandles imidlertid ikke på denne måten. Hvis du bruker varene i transitt og konserninterne funksjoner sammen, vil derfor resultatene for begge disse rapportene være feil.

## <a name="using-the-two-modules-together"></a>Bruke de to modulene sammen

Du kan bruke TMS for både innkommende og utgående operasjoner. Selv om Netto innkjøpspris formidler mesteparten av den samme grunnleggende funksjonaliteten som TMS for innkommende operasjoner, tilfører modulen også ekstra funksjonalitet. Derfor kan det være lurt å vurdere å bruke TMS til utgående operasjoner og Netto innkjøpspris til innkommende operasjoner.

Generelt sett anbefales det ikke at du bruker begge modulene til innkommende operasjoner. Du bør bruke modulen som passer best til dine krav. Hvis du bruker de to modulene sammen, må du ikke dele kildedokumenter mellom dem. Du må for eksempel ikke bruke den samme bestillingen for både en last i TMS og en reise i Netto innkjøpspris. Du må særskilt sørge for at du ikke konfigurerer systemet til å opprette innkommende laster automatisk. Hvis varer fra bestillinger blir inkludert i en reise, kan de ikke behandles som en del av en last.

## <a name="goods-in-transit"></a>Varer i transitt

En av hovedfunksjonene i Netto innkjøpspris er evnen til å behandle varer i transitt. Ved hjelp av behandling av varer i transitt kan du ta økonomisk eierskap til sendte varer før de mottas fysisk ved mållageret. Behandling av varer i transitt kreves ofte for internasjonal handel.

### <a name="tms-goods-in-transit-features"></a>Funksjoner for varer i transitt i TMS

TMS støtter i øyeblikket ikke behandling av varer i transitt.

### <a name="landed-cost-goods-in-transit-features"></a>Funksjoner for varer i transitt i Netto innkjøpspris

Behandling av varer i transitt er en hovedfunksjon i Netto innkjøpspris og gir følgende funksjonalitet:

- **Varer i transittlager** – En vare i transittlager kan knyttes til hvert lager i Supply Chain Management. Varer overføres til varer i transittlagre etter at den opprinnelige bestillingen er fakturert. Varer som er fysisk reservert, blir ikke tilgjengelige for bruk før de mottas på det fysiske lageret. Derfor kan du ta økonomisk eierskap av varer ved å fakturering av bestillingen.
- **Finanskonto for varer i transitt** – Netto innkjøpspris legger til en bestemt posteringskonto i økonomimodulen i posteringsprofilen for bestilling for å håndtere behandling av varer i transitt. Denne finanskontoen for varen i transitt fungerer som en konto av typen Varer som ikke er fakturert. Når den opprinnelige bestillingen faktureres, og varene i transittordren opprettes, posteres den direkte bestillingskostnaden til varene i transittfinanskontoen til varene mottas ved den endelige fysiske lokasjonen.
- **Sporingskontrolloppdateringer** – Ordrer for varer i transitt støtter sporingskontrollfunksjonalitet i Netto innkjøpspris. Sporingskontroll lar deg oppdatere forventet ankomstdato for varer mens de er i transitt. Sporingskontroll oppdaterer deretter bestillingen og de tilknyttede bestillingslinjene. Den forventede leveringsdatoen er da tilgjengelig for hovedplanlegging og logistikk.
- **Utløsing av over-/undertransaksjoner** – Hvis det oppstår et avvik mellom de forventede varene på en reiselinje og de faktiske varene som mottas på lageret, løser Netto innkjøpspris det ved å opprette over- og/eller undertransaksjoner. Deretter kan du styre disse transaksjonene, basert på den måten du vil behandle dem på, via en bestilling eller en bevegelsesjournal. Over- og undertransaksjonene formidler en kobling tilbake til bestillingen, den opprinnelige bestillingen og den nye bevegelsesjournalen eller bestillingen for avviket.
- **Ordrer for varer i transitt** – Netto innkjøpspris introduserer et nytt kildedokument som kalles en *ordre for varer i transitt*. Ved hjelp av en ordre for varer i transitt kan du fakturere den opprinnelige bestillingen for å ta økonomisk eierskap av varene. Når bestillingen faktureres, opprettes det nye kildedokumentet for hver bestillingslinje som har en kombinasjon av lagerdimensjoner. Varer flyttes da fysisk til et lager for varer i transitt, der de blir fysisk reservert mot ordren for varer i transitt og ikke kan brukes hvis ikke ordrer for varer i transitt mottas.

## <a name="miscellaneous-charges-and-shipment-costs"></a>Tillegg og forsendelseskostnader

Et av de viktigste aspektene ved forsendelse og forsendelsesadministrasjon av varer er en anerkjennelse av de indirekte kostnadene som er knyttet til forsendelser. Disse administrasjonskostnadene er ikke de direkte lagerkostnadene som er knyttet til en bestilling og forsendelse eller reise. I stedet er det tilleggskostnader som innføres av innholdet i varebevegelsen mellom leverandøren og organisasjonen. Disse kostnadene kan omfatte fraktkostnader som er knyttet til forsendelsen av varer fra en fysisk lokasjon til en annen, eller avgiftskostnader som er knyttet til import av varer fra en utenlandsk leverandør.

Netto innkjøpspris håndterer disse kostnadene ved å opprette en ny type kostnadsstruktur som kalles *automatiske kostnader*. TMS håndterer disse kostnadene ved hjelp av tilleggsfunksjonalitet.

### <a name="tms-charge-and-cost-features"></a>Funksjoner for tillegg og kostnad i TMS

TMS bruker tillegg for å administrere tilleggskostnader for laster som er tilordnet de relaterte kildedokumentlinjene. Disse tilleggene kan defineres på nivået til enten bestillingslinjen eller bestillingshodet.

I TMS kan tillegg fordeles, eller deles på vekten, volumet eller antallet på lageret. Tillegg kan deles på frakt- eller adgangstillegg. Ytterligere utvikling vil være nødvendig for å bruke flere fordelingsmetoder i TMS.

### <a name="landed-cost-charge-and-cost-features"></a>Funksjoner for tillegg og kostnad i Netto innkjøpspris

Netto innkjøpspris formidler et sett med kostnadsfunksjoner som håndterer tilleggskostnader som er knyttet til forsendelsen av varer. Disse kostnadene kalles automatiske kostnader, og de brukes samtidig som forsendelsesfakturen ved bruk av det estimerte kostnadsbeløpet. Hver kostnadstype administreres i sin egen postering. Når de faktiske fakturaene for administrasjonskostnader posteres, oppdateres de estimerte kostnadene automatisk slik at de gjenspeiler de faktiske kostnadene.

I tillegg kan de indirekte kostnadene som er knyttet til forsendelsen av varer, faktureres under transporten fra opprinnelseshavnen eller når som helst etter at varene mottas. Denne funksjonen gir større fleksibilitet for forbruk av varer.

I listen nedenfor finner du en oversikt over noen begreper for tillegg- og kostnadsfunksjonene i Netto innkjøpspris:

- **Kostnadsområde** – Kostnader og tillegg kan tilordnes ulike nivåer, eller *kostnadsområder*, på en sjøreise. Kostnaden kan brukes på sjøreisenivået og deles inn i hver vare i sjøreisen. I tillegg kan kostnader brukes på nivået til containeren, bestillingen, varen eller overføringsordren. Hvert kosttillegg kan behandles separat i de forskjellige områdene, og deles inn i en kostnad per vare.
- **Fordelingsmetoder** – Flere fordelingsmetoder er tilgjengelige i Netto innkjøpspris. Kosttillegg kan fordeles etter antall, kronebeløp, verdi, vekt, volum, mål eller et brukerdefinert volumetrisk mål.
- **Klarerings-/avvikskontroll** – Kostnadstillegg defineres som sin egen kostkodetype i Netto innkjøpspris. Med hver kostkodetype kan du definere en avsetningskonto for kostnadstillegg i tillegg til påløpte kostnader og avvik i kjøpspris for avvik i estimerte kostnader kontra faktiske kostnader. Når de estimerte kostnadene i utgangspunktet blir postert, genereres det en kreditering til avsetningskontoen. Når de faktiske fakturaene er postert, posteres de faktiske kostprisene, og de estimerte kostnadene debiteres basert på avklaringskontoen.

## <a name="matching-freight-bills-and-invoices"></a>Samsvare fraktbrev og fakturaer

### <a name="tms-bill-and-invoice-matching-features"></a>Funksjoner for samsvar mellom regning og faktura i TMS

TMS kan samsvare fraktbrev som inneholder estimerte kostnader og fakturaer, med de faktiske kostnadene for frakten. Fakturaer kan mottas elektronisk eller på papir. Samsvarende avvik mellom den estimerte kostnaden og de faktiske kostnadene påvirker ikke lagervurderingen.

Hvis du vil ha mer informasjon, kan du se [Avstemme frakt i transportstyring](../transportation/reconcile-freight-transportation-management.md).

### <a name="landed-cost-bill-and-invoice-matching-features"></a>Funksjoner for samsvar mellom regning og faktura i Netto innkjøpspris

Netto innkjøpspris kan samsvare fraktbrev med estimerte kostnadstillegg, og kan fakturere de faktiske kostnadstilleggene til de estimerte kostnadene. Fraktgebyrene ligger i en fakturajournal, og de estimerte kostnadene tømmes fra avstemmingskontoen når de faktureres. I tillegg posteres de faktiske kostprisene mot kostnadene for solgte varer for varen, sammen med avvikene mellom de estimerte tilleggene og de faktiske tilleggene. Denne virkemåten gir deg fleksibilitet under fakturering.

## <a name="tracking"></a>Sporing

En viktig funksjon i både TMS og Netto innkjøpspris er muligheten til å spore varer og identifisere hvor de er i reisen fra opprinnelsesstedet til det endelige destinasjonslageret. Ved bruk av sporing kan du følge og oppdatere hvor varene befinner seg, og når det forventes at de ankommer lageret for forbruk. I tillegg til varestatusen under transporten, formidler Netto innkjøpspris forventede og faktiske datoer for hvert trinn i reisen.

### <a name="tms-tracking-features"></a>Funksjoner for sporing i TMS

TMS inneholder begrensede funksjoner for sporing av innkommende laster. Den viser datoer og gjør det mulig å bygge en integrering for å finne den nøyaktige posisjonen (for eksempel på siden **Transportstatus**).

For hvert rutesegment kan du angi estimerte planer og ankomsttider.

### <a name="landed-cost-tracking-features"></a>Funksjoner for sporing i Netto innkjøpspris

Netto innkjøpspris kan formidle sporingskontroll for hver sjøreise, fra opprinnelseshavnen til det endelige målet. Sporingskontroll definerer statusen for sjøreisen. Statusen indikerer om sjøreisen pågår, er ved tollbesøk eller er ved lokal levering på vei til det endelige lageret. Statusen kan angis på nivået til bestillingslinjen, containeren og hodet til sjøreisen. Derfor har du mer detaljert kontroll.

I tillegg vil en bekreftet forventet dato som er basert på angitte leveringstider, være knyttet til hvert trinn i en reise. De bekreftede og forventede leveringsdatoene legges til på bestillingslinjen og i ordrer for varer i transitt, og kan brukes til hovedplanlegging og logistikk. I tillegg til forventede datoer, kan de faktiske datoene oppdateres. De påfølgende trinnene i en sjøreise vil deretter oppdateres i henhold til dette.

## <a name="multi-leg-journeys"></a>Reiser med flere strekninger

Sjøreisekonseptet identifiserer hvor varene er i prosessen, og kontrollerer statusen til varene mens de er i transitt. Varer kan fullføre flere etapper av en sjøreise, og du kan knytte ulike kostnader til en bestemt etappe. Eksempler inkluderer en fraktkostnad på bruken av et transportmiddel og lokale transportkostnader for transporten av varer fra havnen til målet.

### <a name="tms-multi-leg-journey-features"></a>Funksjoner for flere etapper i TMS

I TMS kan ruter deles opp i rutesegmenter for å representere sjøreiser med flere etapper. TMS kan tildele spotkurser og adgangstillegg til individuelle rutesegmenter.

Hvis du vil ha mer informasjon, kan du se [Planlegge frakttransportruter med flere stopp](../transportation/plan-freight-transportation-routes-multiple-stops.md).

### <a name="landed-cost-multi-leg-journey-features"></a>Funksjoner for sjøreiser med flere etapper i Netto innkjøpspris

Netto innkjøpspris formidler et rammeverk for flytting av varer fra opprinnelsesstedet til målet gjennom en serie med etapper, som er stoppene eller trinnene i en sjøreise. Etappene kombineres for å opprette sjøreisemaler, som definerer hvordan varer flyttes fra leverandøren til organisasjonen.

I hver etappe av en sjøreise kan du ytterligere definere statusen for hver bestillingslinje og leveringstidene som er knyttet til den. Den kombinerte leveringstiden for alle etappene brukes til å identifisere den forventede leveringsdatoen. Behandling av varer i transitt er imidlertid nødvendig for at sjøreiser med flere etapper skal kunne brukes. Reisen med varer for en sjøreise administreres i en tabell som er spesifikk for Netto innkjøpspris.

## <a name="receiving-by-container"></a>Mottak i container

Det kan være viktig å styre hvordan varer deles og oppbevares i et transportmiddel. I et transportmiddel kan varer oppbevares i én eller flere containere. Når varene mottas, mottas de i containere, og ulike containere for en sjøreise mottas kanskje til ulike tider eller på forskjellige datoer.

Både TMS og Netto innkjøpspris formidler funksjonalitet for administrasjon av mottak av varer i en container. TMS bruker konseptet med laster til å administrere varene, bestillingene og overføringsordrene som er knyttet til en forsendelsescontainer. TMS støtter mottak på grunnlag av en emballasjestruktur som mottas via ASN (Advance Shipping Notice). Netto innkjøpspris bruker konseptet med forsendelsescontainere til å behandle bestillinger og kontrollere indirekte kostnader som er knyttet til en container for et transportmiddel.

### <a name="tms-receiving-by-container-features"></a>Funksjoner for mottak i container i TMS

TMS støtter innkommende ASN-er, alle varianter av mottak via mobilappen Lagerstyring og alle mottaksmetoder via Supply Chain Management-klienten.

### <a name="landed-cost-receiving-by-container-features"></a>Funksjoner for mottak i container i Netto innkjøpspris

Når det gjelder mottak i container, oppretter Netto innkjøpspris forsendelsescontainerposter og knytter bestillinger til en bestemt forsendelsescontainer ved hjelp av container-ID-en. Indirekte kostnader kan deretter brukes på denne forsendelsescontaineren, slik at de knyttes til de relevante bestillingene.

Containere i Netto innkjøpspris kan mottas ved hjelp av en ny mottakstype som er kjent som *mottak av varer i transitt*, via ankomstjournaler eller mobilenhetsmottak. Når ankomstjournaler brukes, kan antallene initialiseres fra ordren for varene i transitt eller de opprinnelige bestillingslinjene i containeren. Netto innkjøpspris formidler to arbeidstyper for mottak via mobilappen Lagerstyring.

Netto innkjøpspris formidler ikke et ASN for elektronisk mottak av varer. I tillegg støtter ikke modulen flyter i mobilappen Lagerstyring som behandler lastmottak, numerskiltmottak eller mottak av kombinert nummerskilt.

## <a name="rate-shopping-by-vendor"></a>Innhenting av rater etter leverandør

Ved hjelp av innhenting av rater kan et firma velge en transportleverandør basert på den laveste prisen, den raskeste ruten eller en kombinasjon av begge.

### <a name="tms-rate-shopping-features"></a>Funksjoner for innhenting av rater i TMS

Med TMS kan du identifisere leverandør- og ruteløsninger for innkommende og utgående ordrer. Du kan for eksempel identifisere den raskeste ruten eller den billigste for en forsendelse.

TMS tilbyr fullstending innhenting av rater og fraktoptimalisering via arbeidsområdet for rutesats, fleksible vurderingsalternativer via vurderingsmotoren, en API for vurderingsmotoren for integrering med eksterne parter samt støtte for volumvekt.

Hvis du vil ha mer informasjon, kan du se [Transportstyringsmotorer](../transportation/transportation-management-engines.md).

### <a name="landed-cost-rate-shopping-features"></a>Funksjoner for innhenting av rater i Netto innkjøpspris

Netto innkjøpspris formidmler bare begrenset støtte for innhenting av rater etter leverandør. Selv om man kan angi verdier for fraktbrev, sammenligner ikke Netto innkjøpspris dem på tvers av flere leverandører.

## <a name="driver-check-incheck-out-with-appointment-scheduling"></a>Inn- og utsjekking av sjåfør med avtaleplanlegging

Med funksjoner for inn- og utsjekking av sjåfør kan systemet overvåke ankomster og forhindre koordinering i lastesonene.

### <a name="tms-driver-check-incheck-out-features"></a>Funksjoner for inn- og utsjekking av sjåfør i TMS

I TMS kan du opprette *avtaler*. En avtale representerer hendelser som oppstår i en lastesone under mottak av en bestilling, sending av en salgsordre eller behandling av en innkommende eller utgående last på en bestemt dato og klokkeslett. Avtaler sikrer at lastesoner er tilgjengelige for lasting og lossing av varer, og de hindrer situasjoner der flere transportører ankommer et sted samtidig.

Systemet støtter tillater at sjåførene kan sjekke inn ved en bestemt lastesonedør.

### <a name="landed-cost-driver-check-incheck-out-features"></a>Funksjoner for inn- og utsjekking av sjåfør i Netto innkjøpspris

Netto innkjøpspris kan lagre estimater for datoen og klokkeslettet når en container blir levert.

## <a name="transfer-orders-and-additional-costs"></a>Overføre ordrer og tilleggskostnader

Virksomheter må ofte kunne overføre varer mellom lagre. Når denne typen overføring skjer, knyttes kostnader til den, og du vil kanskje gjenkjenne disse kostnadene. I Netto innkjøpspris kan overføringsordrer legges til en sjøreise eller et transportmiddel for å spore flytting av varer fra ett lager eller område til et annet område, estimere leveringstid og forventet leveringsdato og legge til indirekte kostnader i overføringen av varer.

### <a name="tms-transfer-order-cost-features"></a>Funksjoner for kostnader for overføringsordre i TMS

TMS støtter oppretting av fraktgebyrer som er koblet til overføringer. Selv om disse gebyrene kan vises fra overføringsordren, vil netto innkjøpspris ikke legges til varekostnaden. Fraktavstemming støttes ved oppretting av et fraktbrev som er basert på disse gebyrene. Dette fraktbrevet blir deretter sammenlignet mot en leverandørfraktfaktura.

### <a name="landed-cost-transfer-order-cost-features"></a>Funksjoner for kostnader for overføringsordre i Netto innkjøpspris

Med Netto innkjøpspris kan du legge til overføringsordrer for et transportmiddel eller en sjøreise. På denne måten kan du legge til forsendelseskostnader i sjøreisen som lagerutligninger når overføringsordren blir mottatt. De indirekte kostnadene kan faktureres for de faktiske kostnadene og spores mot en oppdatering for å oppdatere kostnadene for solgte varer. Selv om overføringsordrer ikke bruker behandling av varer i transitt i standardutgivelsen, kan de legges til for sjøreiser. Netto innkjøpspris blir lagt til i totalkostnaden for hver vare.
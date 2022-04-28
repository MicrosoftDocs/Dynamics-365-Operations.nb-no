---
title: Hva er nytt eller endret i Dynamics 365 for Operations versjon 1611 (november 2016)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 for Operations versjon 1611.
author: sericks007
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 221294
ms.assetid: 357931ed-f843-4bf5-bc85-0da3de0619ec
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 43a53d5940b2595abb305a08e6f52661bee8ca62
ms.sourcegitcommit: 4c8223c9540fbc1c1e554962938058d432e4c681
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/05/2022
ms.locfileid: "8548087"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-operations-version-1611-november-2016"></a>Hva er nytt eller endret i Dynamics 365 for Operations versjon 1611 (november 2016)

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 for Operations versjon 1611.

## <a name="cost-accounting"></a>Kostnadsregnskap

<table>
<thead>
<tr>
<th>Hva du kan gjøre</th>
<th>Hvorfor dette er viktig</th>
</tr>
</thead>
<tbody>
<tr>
<td>Angi kostnadselementdimensjoner og importer medlemmer av kostnadselementdimensjonen.</td>
<td>Kostnadselementer brukes til å kategorisere kostnader og dokumentere flyten av kostnader. Primærkostnadselementene importeres ved hjelp av en datakobling for Microsoft Dynamics 365 for Operations for å hente hovedkontoer direkte fra Operations, eller ved hjelp av en generell datakobling, der du henter hovedkontoer via Microsoft Excel fra et kildesystem. Når hovedkontoer importeres til Kostnadsregnskap, kan de brukes som medlemmer av kostnadselementdimensjoner. De sekundære kostnadselementene er brukerdefinerte, og de brukes i fordelinger til å dokumentere flyten av kostnader.</td>
</tr>
<tr>
<td>Tilordne kostnadselementdimensjoner.</td>
<td>Hvis hovedkontoene på tvers av juridiske enheter ikke kan deles på grunn av lovbestemte krav for regnskap, kan du tilordne dem når du importerer dem til kostnadsregnskap for å få en helhetlig oversikt på tvers av organisasjonen.</td>
</tr>
<tr>
<td>Definer kostnadsobjektdimensjoner, og importer medlemmer av kostnadsobjektdimensjonen.</td>
<td>Kostnadsobjekter er en hvilken som helst type objekt som kostnadene tilordnes til. Vanlige kostnadsobjekter omfatter produkter, prosjekter, ressurser, avdelinger, kostsentre og geografiske områder. Du kan bruke en datakobling for Microsoft Dynamics 365 for Operations til å hente finansdimensjoner og verdier fra Operations, eller du kan bruke en generell datakobling, der du kan hente dimensjoner og verdier via Excel fra et hvilket som helst kildesystem. Hvis du bruker den økonomiske dimensjonen for kostsenter som objektdimensjonen, er alle kostsentre som importeres, dimensjonsmedlemmene for kostnadsobjektet.</td>
</tr>
<tr>
<td>Definer eller importer statistiske dimensjoner.</td>
<td>Medlemmer av statistiske dimensjoner måles i ikke-pengemessige enheter, for eksempel maskindriftstid, antall ansatte og felt. De brukes i utdrag, eller som grunnlag for fordelinger og distribusjoner.</td>
</tr>
<tr>
<td>Opprett maler for leverandør av statistisk måling.</td>
<td>En mal for leverandør av statistisk måling brukes til å transformere Dynamics 365 for Operations-data til statistiske målinger. Malen blir deretter tilknyttet et medlem av statistisk dimensjon. Malene forhåndsfiltreres slik at de bare viser tabeller som er forbundet med finansdimensjoner.</td>
</tr>
<tr>
<td>Opprett kostnadsregnskapsfinanser.</td>
<td>En kostnadsregnskapsfinans er en agnostisk finans som bruker en egen kalender og valuta. Den spiller en viktig rolle i behandlingen av alle kostnadstransaksjonene. En kostnadsregnskapsfinans klassifiserer for eksempel kostnader basert på egne kostnadselementer, og samler kostnader basert på egne objektdimensjoner. Du kan opprette så mange kostnadsregnskapsfinanser du trenger for å utføre administrasjonsrapportering fra forskjellige perspektiver.</td>
</tr>
<tr>
<td>Opprett kostnadskontrollenheter.</td>
<td>Kostnadskontrollenheter utgjør kostnadsstrukturen og definerer flyten av kostnader i en kostnadsregnskapsfinans. De må være knyttet til kostnadsobjektdimensjoner for å representere kostnadsobjektdimensjonene i Finans.</td>
</tr>
<tr>
<td>Behandle økonomimoduloppføringer.</td>
<td>Hvis du vil måle faktisk ytelse, må du ha data. Dataene importeres ved hjelp av koblingene du definerer for kostnadsregnskapsfinansen. Når du behandler finansoppføringene, importeres dataene trinnvis.</td>
</tr>
<tr>
<td>Behandle budsjettoppføringer.</td>
<td>Hvis du vil måle budsjettert ytelse, må du ha data. Dataene importeres ved hjelp av koblingene du definerer for kostnadsregnskapsfinansen. Når du behandler budsjettoppføringene, importeres dataene trinnvis.</td>
</tr>
<tr>
<td>Opprett og bruk policyer for kostnadsatferd.</td>
<td>Du kan bruke en policy for kostnadsatferd til å klassifisere kostnader som faste, variable eller delvis variable. En policy er regelbasert og datoeffektiv. Alle kostnader er som standard merket som uklassifiserte før du kan bruke en policy for kostnadsatferd og beregne virkningen av regelen. Etter beregningen klassifiseres kostnadene.</td>
</tr>
<tr>
<td>Spor kostnader.</td>
<td>For å hjelpe deg med å forstå virkningen av kostnadspolicyer, kan du bruke Kostnadsregnskap til å spore kostnader til kildeverdiene og brukte regler som de kommer fra. Denne funksjonaliteten gir full sporbarhet om når kostnader oppstod, hvilken type kostnader som oppstod, og hvilke regler for kostnadsatferd som ble brukt.</td>
</tr>
<tr>
<td>Definer dimensjonshierarkier.</td>
<td>Du kan opprette dimensjonshierarkier for kategoriserings- eller klassifiseringsformål. Du kan for eksempel definere et kategoriseringshierarki som er basert på en kostnadselementdimensjon og dens medlemmer. Du kan eventuelt definere et klassifiseringshierarki som er basert på en kostnadsobjektdimensjon og dens medlemmer. Rapporteringsstrukturene brukes i følgende situasjoner:
<ul>
<li>Du definerer fordelinger, kostnadssatser og regler for opprullet kost.</li>
<li>Du kan vise setninger ved hjelp av arbeidsområdet.</li>
<li>Du definerer tilgang for å vise samlede data.</li>
<li>Du viser data i Excel.</li>
</ul></td>
</tr>
<tr>
<td>Lag setninger som kan vises i arbeidsområdet.</td>
<td>Bruk arbeidsområdet til å få et raskt overblikk over faktiske og budsjetterte kostnader og avvik. Du kan filtrere dataene etter periode eller kostnadsnivå. Arbeidsområdet er utformet for ledere som er ansvarlige for kostnadskontroll. Det følger tilgangsreglene som er definert for dimensjonshierarkier.</td>
</tr>
<tr>
<td>Opprett rapporter ved hjelp av Excel.
<blockquote>[!NOTE] Du må kjøre Microsoft Excel 2016.</blockquote>
</td>
<td>Du kan eksportere kostnadsregnskapsdata direkte til Excel via dataenheter og bruke Microsoft PivotTable til å opprette rapporter.</td>
</tr>
</tbody>
</table>

## <a name="expense-management"></a>Reiseregning og utlegg

| Hva du kan gjøre | Hvorfor dette er viktig |
|-----------------|-----------------------|
| Tilordne avsluttede kredittkorttransaksjoner for ansatte på nytt. | Noen ganger når en ansatt er sluttet, blir hans eller hennes konto i Active Directory Domain Services (AD DS) deaktivert når aktive kredittkorttransaksjoner som må oppføres som utgift, blir importert. Tidligere kunne du ikke tilordne en representant for utgiftsregistrering og knytte kredittkorttransaksjonene til en utgiftsrapport. Nå kan du bruke siden **Kredittkorttransaksjoner** til å tilordne kredittkorttransaksjon på nytt for den ansatte der den tilknyttede ansatte er sluttet. Når du tilordner kredittkorttransaksjonen, kan transaksjonen velges for en utgiftsrapport og betales gjennom den vanlige prosessen for refusjon av utgiftsrapport. |
| Endre informasjonen for utgiftskredittkort for ventende og tidligere ansatte. | Du kan endre kredittkortinformasjon for reiseregning for ventende og tidligere arbeidere. Tidligere kunne du endre kredittkortinformasjonen for utgift bare hvis man var aktivt ansatt. |
| Kopier en utgiftsrapport. | Du kan nå kopiere en eksisterende utgift når du oppretter en ny utgift i den samme utgiftsrapporten. Du kan kopiere en utgift og alle de tilknyttede ikke-kredittutgiftene til en ny utgiftsrapport. Du må fremdeles utføre alle nødvendige spesifiseringer og tilknytte nødvendige mottak basert på definerte utgiftspolicyer og -kategorier. Du kan legge til kredittkorttransaksjoner i utgiftsrapporten ved å velge å legge til ikke-avstemte utgifter. |
| Masserediger utgifter. | Noen kredittkorttransaksjoner er kanskje ikke tilordnet til en utgiftskategori, eller de kan være feil tilordnet når de importeres. I så fall må ansatte manuelt endre tilknyttede den tilknyttede utgiftskategorien. Når du administrerer ikke-avstemte utgifter, kan du nå masseredigere utgiftskategorien for de valgte utgiftene. Når du i tillegg administrerer valgte utgifter for en bestemt utgiftsrapport, kan du masseredigere prosjektet og tilleggsinformasjonen. |
| Endre valutakursen for kredittkorttransaksjoner. | Den faktiske valutakursen som skal brukes for en kredittkorttransaksjon, kan være forskjellig fra valutakursen som er definert i systemet. Tidligere kunne ikke ansatte endre valutakursen for en hvilken som helst kredittkorttransaksjonen som ble importert til reiseregning. Du kan nå angi en parameter på siden **Parametere for reiseregning** for å tillate at valutakursen endres for kredittkorttransaksjoner. |
| Definer en antikorrupsjonsattestering for utgifter. | Noen ansatte i en organisasjon har kanskje inngått avtaler med statstjenestemenn, og noen utgifter som oppstår som en del av de avtalene, kan bli oppfattet som bestikkelser. I Reiseregning kan du nå definere en antikorrupsjonsattestasjon som vises for valgte utgiftskategorier, for eksempel mat og gaver. Ansatte må velge om utgifter som defineres for antikorrupsjonsattestering oppfyller vilkårene som defineres av organisasjonens policyer. |
| Hindre manuell registrering av utgifter for bestemte utgiftskategorier. | En utgiftskategori kan defineres til å representere en kredittkorttransaksjon som kategorien ikke kan endres for. Et eksempel er en avgift for sen betaling av kredittkortet. Du kan nå sette opp en utgiftskategori som gjør at utgifter bare opprettes via import. Denne funksjonen hindrer ansatte i å opprette en utgift for kategorien manuelt. Den tillater heller ikke at kategorien endres for transaksjoner som er importert og som bruker denne kategorien. |
| Knytt et mottak til flere utgifter. | Et mottak som er lastet opp til Reiseregning, kan være knyttet til flere utgifter. Tidligere måtte et mottak som var knyttet til flere utgifter, lastes opp én gang for hver utgift. Nå kan du knytte et mottak til en utgift som allerede er lastet opp og knyttet til en annen utgift på den samme utgiftsrapporten. Hvis du i tillegg laster opp et mottak til hodet i utgiftsrapporten, kan du velge én eller flere linjer som mottaket skal knyttes til. |
| Opprett fremtidsdaterte utgifter. | Når du kopierer en utgiftsrapport, har for eksempel transaksjonsdatoen for en utgift en fremtidig dato. Tidligere versjoner tillater ikke fremtidsdaterte utgifter. Du kan nå opprette og lagre utgifter som har en fremtidig dato. Men kan imidlertid ikke sende fremtidsdatert utgift. |
| Definer utgiftsavgifter for delstat/område. | I enkelte land/områder kan det hende utgifter som er påløpt i forskjellige delstater/områder, blir underlagt forskjellige mva-satser. Du kan nå definere konfigurasjoner for mva på områdenivå, ikke bare på nivået for landet/regionen. Hvis du lar feltet **Delstat/område** stå tomt på siden **Avgiftskonfigurasjon**, gjelder mva-gruppen for alle delstatene/områdene for det angitte landet/området. |
| Definer typer utgiftskredittkort. | Tidligere fantes det ingen side der du kunne opprette nye kredittkorttyper, for eksempel Visa, MasterCard eller AMEX, som kunne brukes med Reiseregning. Du kan nå opprette kredittkorttyper skal brukes med Reiseregning. Siden er plassert i området **Oppsett** i delen **Beregninger og koder**. |
| Definer en godkjenningsarbeidsflyt med flere nivåer for utgiftsrapporter. | En ny arbeidsflyt for utgiftsrapporter støtter en godkjenningsprosess med flere nivåer. Ansatte angir de midlertidige og endelige godkjennerne ved oppretting av utgiftsrapporten. Arbeidsflyten ruter deretter utgiftsrapporten til midlertidige godkjennerne først. Etter at utgiftsrapporten er godkjent på det nivået, rutes arbeidsflyten til de siste godkjennerne for endelig godkjenning. |
| Opprett og vedlikehold utgifter som ikke er koblet til en utgiftsrapport. | Brukeren kan nå opprette utgifter og opprettholde dem (for eksempel ved å tilknytte eller spesifisere mottak eller tilordne gjester) uten å måtte opprette en utgiftsrapport. Én eller flere utgifter kan velges og legges til en ny utgiftsrapport slik at de kan sendes til godkjenning. Det finnes en ny side for å vedlikeholde utgifter på **Reiseregning** &gt; **Mine utgifter** &gt; **Utgifter**. |

## <a name="financial-management"></a>Økonomistyring

<table>
<thead>
<tr>
<th>Hva du kan gjøre</th>
<th>Hvorfor dette er viktig</th>
</tr>
</thead>
<tbody>
<tr>
<td>Spor vurderinger for anleggsmiddel ved hjelp av ett "tablå"-begrep.</td>
<td>Tidligere ble to ulike typer vurdering brukt til å spore anleggsmiddelverdier: verdimodeller og avskrivningstablåer. Disse to begrepene er slått sammen til ett vurderingsbegrep kalt "tablåer" i den gjeldende versjonen. Tablåer har all funksjonaliteten i både verdimodeller og avskrivningstablåer. Du kan for eksempel deaktivere postering til økonomimodulen. Tablåer som posteres til Finans, brukes vanligvis for finansrapportering for firmaer. Tablåer som ikke posteres i Finans, kan brukes til mva-rapporteringsformål.</td>
</tr>
<tr>
<td>Utfør årsavslutningen for økonomimodulen for flere juridiske enheter.</td>
<td>Du kan gjennomføre årsavslutningen raskere ved å kjøre den for flere juridiske enheter fra en delt årsavslutningsside. Grupper med juridiske enheter kan defineres sammen med innstillinger som bør beholdes fra ett år til neste. Andre forbedringer i anvendeligheten er også gjort for årsavslutningsprosessen.</td>
</tr>
<tr>
<td>Dra nytte av forbedringer i revaluering av utenlandsk valuta for finans.</td>
<td>Følgende forbedringer er gjort i økonomimodulprosessen for revaluering av utenlandsk valuta:
<ul>
<li>En valutakurstype er lagt til hovedkontoen. Denne valutakursen brukes nå til å fastslå valutakursen under revaluering av valuta. Hvis ingen valutakurstype er definert, fortsetter prosessen med å bruke valutakursen som er definert i Finans.</li>
<li>Nå er det enklere å velge et område med hovedkontoer og valutaer til å kjøre prosessen for revaluering.</li>
<li>Revaluering kan kjøres for flere juridiske enheter.</li>
<li>Systemet opprettholder nå en logg over alle revalueringer som ble utført, som det gjøres i revalueringsprosesser for kunder (AR) og leverandører (AP).</li>
<li>Når du starter prosessen, kan du nå forhåndsvise resultatene av revalueringen. Forhåndsvisningen viser resultatene for alle juridiske enheter som prosessen ble kjørt for. Deretter kan du postere de juridiske enhetene, eller et delsett av dem, fra forhåndsvisningen. Du kan også eksportere resultatene i forhåndsvisningen til Excel.</li>
</ul></td>
</tr>
<tr>
<td>Vis transaksjoner for ekstra posteringslag.</td>
<td>På listesiden <strong>Råbalanse</strong> og i rapporten <strong>Dimensjonsoppgave</strong> kan du nå velge flere posteringslag som er lagt til økonomimodulen. Når du velger tilleggsposteringslagene, er justeringene for disse posteringslagene inkludert i saldoene på listesiden eller i rapporten.</td>
</tr>
<tr>
<td>Definer hvordan dokumentasjonen knyttes til malen for for regnskapsperiodeavslutning.</td>
<td>Tidligere kunne du knytte til dokumentasjonen etter at en oppgave var fullført. Du kunne for eksempel knytte til en rapport som ble generert. Nå kan du også knytte til et instruksjonsdokumentet i malen. Dette instruksjonsdokumentet blir deretter kopiert til hver oppgave i den økonomiske timeplanen, slik at eieren av oppgaven kan vise informasjon om hvordan du kan fullføre oppgaven.</td>
</tr>
<tr>
<td>Definer det konserninterne kontooppsettet fra en delt side.</td>
<td>Siden <strong>Konserninternt kontooppsett</strong> er nå delt slik at en organisasjon kan definere alle par med juridiske enheter som kan forhandle med hverandre. I tillegg kan du nå angi en transaksjon i den opprinnelige juridiske enheten, men ikke fra den juridiske enheten for målet. Hvis en juridisk enhet kan starte en konsernintern transaksjon, må det gjensidige paret være definert. Derfor defineres den juridiske enheten for målet også som en opprinnelige juridisk enhet.</td>
</tr>
<tr>
<td>Send begrunnelsesdokumenter for budsjettplaner.</td>
<td>Du kan opprette en begrunnelsesmal som ytterligere dokumentasjon for alle ønskede budsjettbeløp. Brukere kan fylle ut detaljene for malen og tilknytte den til budsjettplanen, slik at den kan brukes i godkjenningsprosessen.</td>
</tr>
<tr>
<td>Aktiver avanserte regler for budsjettregisteroppføringer.</td>
<td>Hvis avanserte regler konfigureres i økonomimodulen, kan disse reglene brukes for nye oppføringer og overføringer i budsjettjournalen.</td>
</tr>
<tr>
<td>Dra nytte av bedre oversikt over forskuddsfaktureringsaktiviteten.</td>
<td>En ny forekomst av listesiden <strong>Åpne forskuddsbetalinger</strong> gir en oversikt over statusen for forskuddsfaktureringsaktiviteten. Siden formidler informasjon til AP-avdelingen om bestillinger som har gjenstående forskuddsbetalingsverdier som må faktureres, faktureringsverdier som må betales, og betalte fakturaverdier som må utlignes mot standardfakturaer. I tillegg gjør forbedringer i den automatiske bruken av betalte forskuddsfakturaer til standardfakturaer at faktureringsmedarbeidere kan registrere data mer effektivt.</td>
</tr>
<tr>
<td>Bruk arbeidsområdet <strong>Leverandørsamarbeidsfakturering</strong>.</td>
<td>Et nytt <strong>Fakturering</strong>-arbeidsområde i området <strong>Leverandørsamarbeid</strong> gjør det mulig for eksterne leverandører å få sikker tilgang til sin egen fakturainformasjon. Leverandører kan for eksempel se om en faktura er betalt, og sende egne fakturaer. Denne endringen fremmer mer effektiv og betimelig kommunikasjon med eksterne leverandører. Dermed har faktureringsmedarbeidere færre avbrudd i arbeidet.</td>
</tr>
<tr>
<td>Bytt juridiske enheter under registrering av faktura.</td>
<td>Forbedringene gir faktureringsmedarbeidere som må registrere fakturaer for flere juridiske enheter, muligheten til raskt å endre den juridiske enheten på faktureringssidene. Denne funksjonen sparer tid for faktureringsmedarbeiderne, fordi de ikke lengre må logge av den gjeldende juridiske enheten og logge på en annen juridisk enhet. Både siden <strong>Global fakturajournal</strong> og siden <strong>Leverandørfakturaer</strong> lar brukere endre den juridiske enheten under dataregistrering.</td>
</tr>
<tr>
<td>Støtte for elektroniske filer for det kombinerte føderale/statlige arkiveringsprogrammet for IRS-tjenesten (Internal Revenue Service)</td>
<td>Når konfigurasjonsnøkkelen <strong>US</strong> er aktivert, tilbyr den elektroniske 1099-arkiveringsprosessen flere funksjoner som er i samsvar med IRS-bestemmelsene for det kombinerte føderale/statlige arkiveringsprogrammet. IRS opprettet dette programmet slik at det kan videresende informasjonsreturer elektronisk tilbake til deltakende stater.</td>
</tr>
<tr>
<td>Utligningsforbedringer</td>
<td>Forbedringer hjelper betalingsmedarbeidere med å utligne mer effektivt, ettersom medarbeidere kan tillate at flere uposterte betalinger utlignes mot den samme fakturaen.</td>
</tr>
<tr>
<td>Kryssfirmavisning</td>
<td>Medarbeidere for sentralisert betaling kan nå vise forfalte fakturaer på tvers av firmaer. Arbeidsområdene <strong>Leverandørbetalinger</strong> og <strong>Kundebetalinger</strong> gir nå bedre innsikt i og kontroll over forfalte fakturaer ved hjelp av en metode for å vise og filtrere på tvers av firmaer, som inngår i et organisasjonshierarki for sentralisert betaling.</td>
</tr>
<tr>
<td>Bruk arbeidsområdet <strong>Bankstyring</strong>.</td>
<td>Det nye arbeidsområdet <strong>Bankstyring</strong> bidrar til å spore bankkontoer og saldoer for de juridiske enhetene. Gjeldende og utestående saldoer er umiddelbart tilgjengelige for alle kontoer, og du kan gå tilbake fra saldoene til de detaljerte transaksjonsbilagene. Du kan også se de historiske saldodataene for hver bankkonto, eller et sammendrag for alle bankkontoer i firmaet, i både kortsiktige og langsiktige visninger. Du kan få bedre innsikt i bankkontoavstemming, fordi datoen for den forrige avstemmingen rapporteres for hver bankkonto, og det finnes også en indikator for avstemminger som pågår.</td>
</tr>
<tr>
<td>Importer elektroniske bankkontoutdrag for alle juridiske enheter i ett trinn.</td>
<td>Du kan nå importere elektroniske bankkontoutdrag for alle juridiske enheter i ett trinn. Filer med bankkontoutdrag kan inneholde informasjon fra mange bankkontoer og juridiske enheter, og zip-filer kan inneholde flere filer med bankkontoutdrag. Ved hjelp av én importprosess kan du starte avstemmingen for alle rapporterte bankkontoer i alle juridiske enheter. Denne funksjonen sparer deg tid, fordi du ikke trenger å bytte mellom firmaer og flere utdragsimporter. Du kan også kjøre samsvarsregler automatisk mot alle importerte setninger i hvert firma.</td>
</tr>
<tr>
<td>Vurderingssporing</td>
<td>Ett anleggsmiddel kan ha flere vurderinger for forskjellige regnskapsstandarder, og kan også postere transaksjonene knyttet til økonomimodulen. Disse vurderingene ble tidligere spores ved hjelp av enten verdimodeller eller avskrivningstablåer. Nå kan du spore disse vurderingene, som kalles nå tablåer, ved hjelp av et felles sett med journaler, forespørsler og rapporter. Den samordnede opplevelsen forenkler implementeringen og reduserer antall grensesnitt som periodiske forretningsprosesser krever.</td>
</tr>
<tr>
<td>Dra nytte av forbedringer som avskrivning på tvers av firmaer medfører.</td>
<td>Nå kan du starte en avskrivning for anleggsmidler på tvers av alle juridiske enheter fra én side. Du kan postere journalene automatisk når de opprettes. Du kan sende oppretting og postering av journalene til satsvis behandling, slik at avskrivningen kjøres i bakgrunnen. Disse forbedringene reduserer ineffektivitet, fordi du ikke trenger å starte enkeltstående avskrivninger separat for hvert firma. Forbedringen muliggjør også bedre sentralisert behandling av aktiva.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Forvaltning av menneskelig kapital

<table>
<thead>
<tr>
<th>Hva du kan gjøre</th>
<th>Hvorfor dette er viktig</th>
</tr>
</thead>
<tbody>
<tr>
<td>Opprett en ytelsesjournal.</td>
<td>Før du fullfører gjennomgangen, samler du ofte informasjon om aktiviteter eller hendelser som bidro til din suksess som ansatt i løpet av gjennomgangsperioden. Du kan legge til en oppføring for ytelsesjournalen for å dokumentere de aktivitetene og hendelsene. Du kan også koble disse aktivitetene og hendelsene til et mål eller en evaluering av ytelse for å gi mer informasjon til kontrolløren.</td>
</tr>
<tr>
<td>Opprett mer detaljerte mål.</td>
<td>Du har mer kontroll over innholdet i målene du angir. Du kan opprette målinger for målene, koble oppføringer for ytelsesjournal til målingene, og legge ved og vise dokumenter. Du kan lagre mål som maler og bruke dem på nytt for rask installasjon.</td>
</tr>
<tr>
<td>Opprett mer detaljerte ytelsesgjennomganger.</td>
<td>Ytelsesgjennomganger, formelt kalt diskusjoner, er nå fleksible nok til å støtte både fortløpende tilbakemelding og mer formelle gjennomganger. Du kan trekke inn aktive mål og legge inn kommentarer om dem, og legge til inndelinger for en evaluering av din kompetanse. Flere inndelinger er angitt, der du kan legge til eller vise målinger, ytelse, loggoppføringer, vedlegg og godkjenninger som er knyttet til gjennomgangen.</td>
</tr>
<tr>
<td>Knytt flere stillingshierarkier til arbeidsflyter.</td>
<td>Du kan knytte en arbeidsflyt til et stillingshierarki. Du kan også endre trinn i arbeidsflyten for å optimalisere godkjenningsprosessen slik at den passer til dine forretningskrav. Derfor kan du definere en effektiv godkjenningsstruktur som passer til ulike rapproteringsforhold som organisasjonen din bruker.</td>
</tr>
<tr>
<td>Arbeidsflytstøtte for angivelse av personlige identifikasjonsnumre (PIN-koder) i selvbetjening for ansatte.</td>
<td>Arbeidsflytkapasiteten for personale (HR) er utvidet, og har nå støtte for PIN-koder. Ansatte kan legge til og redigere sin PIN for å forbedre effektiviteten. Personalarbeidere kan imidlertid bruke denne informasjonen for nøyaktighet og kompletthet for å legge den til den ansattes post.</td>
</tr>
<tr>
<td>Opprett maler for mål, og bruk dem til å legge til nye mål.</td>
<td>Du kan opprette maler for mål for mål som deles av mange ansatte i firmaet. Ansatte kan legge til egne mål fra en mal, ledere kan legge til mål for grupper fra en mal, og personalgruppemedlemmer kan legge til mål for ansatte i firmaet.</td>
</tr>
<tr>
<td>Opprett målgrupper, og bruk dem til å legge til nye mål.</td>
<td>Du kan legge til målmaler i en gruppe, og du kan bruke gruppen til å opprette ett eller flere mål for en ansatt, en gruppe, en posisjon, en avdeling eller firmaet.</td>
</tr>
<tr>
<td>Få bedre styring på gjennomgangsprosessen.</td>
<td>Du kan bruke en arbeidsflyt til å kontrollere gjennomgangsprosessen. Du kan opprette maler for gjennomgang og bruke dem til å opprette gjennomganger. Du kan også legge til vurderinger i en gjennomgang.</td>
</tr>
<tr>
<td>Bruk gjennomgangsperioder til å definere tidsrammen for gjennomgangen.</td>
<td>Du kan definere en tidsperiode for en evaluering av ytelse, og start- og sluttdatoene for gjennomgangen angis automatisk. Du kan imidlertid endre disse standarddatoene etter behov.</td>
</tr>
<tr>
<td>Få tilgang til fem nye Power BI-innholdspakker for Personale</td>
<td>De nye innholdspakkene lar personalorganisasjoner og personalledere analysere følgende:
<p>Metrikk for arbeidsstyrke</p>
<ul>
<li>Demografiske detaljer etter alder, kjønn og sivilstatus</li>
<li>Sammenligne årlige tall for avgang og se en liste over årsaker ansatte har oppgitt for å forlate organisasjonen</li>
<li>Vise en liste over åpne stillinger, samt en sammenligning av åpne og lukkede stillinger</li>
</ul>
<p>Kompensasjon og fordeler</p>
<ul>
<li>Sammenligne ansatte med timebetaling og fast lønn</li>
<li>Vise antall ansatte som er registrert i tilgjengelige fordeler</li>
<li>Vise ansatte etter ansettelsestype</li>
</ul>
<p>Rekrutterer</p>
<ul>
<li>Analysere søkere basert på antall søkere, hvor de kommer fra, og hvilke stillinger de søker på</li>
</ul>
<p>Organisasjonsopplæring</p>
<ul>
<li>Kursregistrering etter sted</li>
<li>Kursdeltakelse etter status</li>
<li>Liste over ansatte som er registrert for kurs</li>
</ul>
<p>Kompetanser og utvikling for ansatt</p>
<ul>
<li>Liste over kompetanse som ansatte har</li>
<li>Detaljer om kompetansetyper etter teammedlem</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="localizations"></a>Lokaliseringer

<table>
<thead>
<tr>
<th>Hva du kan gjøre</th>
<th>Hvorfor dette er viktig</th>
</tr>
</thead>
<tbody>
<tr>
<td>Lokaliseringer er tilgjengelige for 18 flere land:
<ul>
<li>Østerrike</li>
<li>Belgia</li>
<li>Brasil</li>
<li>Kina</li>
<li>Tsjekkia</li>
<li>Estland</li>
<li>Finland</li>
<li>Ungarn</li>
<li>Italia</li>
<li>Latvia</li>
<li>Litauen</li>
<li>Norge</li>
<li>Polen</li>
<li>Saudi-Arabia</li>
<li>Spania</li>
<li>Sverige</li>
<li>Sveits</li>
<li>Thailand</li>
</ul>
<p>Følgende land vil også kreve lokalisering av detaljhandel. Lokalisering av detaljhandel for disse landene ikke er fullført og er planlagt for H1 CY2017:</p>
<ul>
<li>Brasil</li>
<li>Tsjekkia</li>
<li>Estland</li>
<li>Ungarn</li>
<li>Latvia</li>
<li>Litauen</li>
<li>Malaysia</li>
<li>Polen</li>
<li>Sverige</li>
</ul>
</td>
<td>Dynamics 365 for Operations er tilgjengelig i 18 flere land. Forskriftsmessige, elektroniske rapporteringsfunksjoner er konvertert til ER-konfigurasjoner (elektroniske rapporteringskonfigurasjoner) som en del av vår arbeid for å gjøre lokalisering enklere og mer konfigurerbar, og noen forskriftsmessig rapporter for Microsoft SQL Server Reporting Services (SSRS) har blitt konvertert til ER-konfigurasjoner med Excel-maler. Disse konverterte funksjonene er spesifikt nevnt senere i denne tabellen.</td>
</tr>
<tr>
<td>Japan – grupper anleggsmidler når du skriver ut skjema 26 og dets nye tabeller.</td>
<td>Skjema 26 må sendes til hver by der selskapet opererer. Hvis du vil lagre du arbeid når du skriver ut skjema 26, kan anleggsmidler automatisk grupperes og sorteres etter lokasjon.</td>
</tr>
<tr>
<td>Japan – se beløpene for raskere og mer avskrivning i profilen.</td>
<td>Profilen kan gi et nøyaktig mål for beløpene for raskere og mer avskrivning.</td>
</tr>
<tr>
<td>Japan – beregn kildeskatt gradvis.</td>
<td>Japanske myndigheter krever at du beregner kildeskatt gradvis basert på betalingsbeløpet.</td>
</tr>
<tr>
<td>Japan – importer postnummerfilen for bestemte, store bedriftsbygninger.</td>
<td>Postnummerfilen som myndigheten formidler for bestemte, store bedriftsbygninger, kan importeres til systemet. Adressen kan deretter avledes fra postnumrene.</td>
</tr>
<tr>
<td>Japan – konfigurer en inaktiv periode for anleggsmidler.</td>
<td>Inaktive perioder lar brukeren stanse avskrivning av anleggsmidler i en angitt periode. Denne funksjonen kreves av forskriften.</td>
</tr>
<tr>
<td>Europa – konfigurer et registreringsnummer for merverdiavgift (mva) for en parts adresse ved hjelp av rammeverket for registrerings-ID.</td>
<td>Du kan konfigurere et mva-registreringsnummer for en parts adresse ved hjelp av rammeverket for registrerings-ID og en ny registreringskategori for <strong>Mva-ID</strong>.</td>
</tr>
<tr>
<td>Finland – konfigurer et kundenummer for tollbehandling for en parts adresse ved hjelp av rammeverket for registrerings-ID.</td>
<td>Du kan konfigurere et tollkundenummer for en parts adresse ved hjelp av rammeverket for registrerings-ID og en ny registreringskategori for <strong>Tollkunde-ID</strong>.</td>
</tr>
<tr>
<td>Frankrike – skriv ut kundefakturaer i et oppsett som er spesifikt for Frankrike.</td>
<td>Utskrift av kundefaktura justeres for å oppfylle spesifikke krav i Frankrike.</td>
</tr>
<tr>
<td>France – bruk kronologisk nummerering av dokumenter etter regnskapsperiode.</td>
<td>For å oppfylle spesifikke krav i Frankrike til nummerering av kundefakturaer, kan du definere nummerserier for kundefakturaer per regnskapsperiode.</td>
</tr>
<tr>
<td>Lokalisering i Østerrike – ER-konfigurasjoner</td>
<td>
<ul>
<li>EU-salgsliste i XML-format for Østerrike</li>
<li>Intrastat-format for Østerrike</li>
<li>ISO20022 Betalingsformat for kredittoverføring for Østerrike</li>
<li>ISO20022 Avtalegiroformat for Østerrike</li>
<li>Østerriksk EDIFACT-PAYMUL-format</li>
<li>Mva-oppgave for Østerrike</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisering i Belgia – ER-konfigurasjoner</td>
<td>
<ul>
<li>BLWI-format for Belgia</li>
<li>EU-salgsliste i XML-format for Belgia</li>
<li>Anleggsmiddelrapport for Belgia</li>
<li>Intervat-format for Belgia</li>
<li>Intrastat-format for Belgia</li>
<li>Fakturaomsetningsrapport for Belgia</li>
<li>Format for eksport av finanstransaksjon for Belgia</li>
<li>Format for SWIFT-leverandørbetaling for Belgia</li>
<li>Format for import av CODA-bankkontoutdrag for Belgia</li>
<li>ISO20022 Betalingsformat for kredittoverføring for Belgia</li>
<li>ISO20022 Avtalegiroformat for Belgia</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisering i Brasil – ER-konfigurasjoner</td>
<td>
<ul>
<li>GIA SP for Brasil</li>
<li>GIA-ST for Brasil</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisering i Tsjekkia – ER-konfigurasjoner</td>
<td>
<ul>
<li>EU-salgsliste i XML-format for Tsjekkia</li>
<li>Intrastat-format for Tsjekkia</li>
<li>Mva-oppgave for Tsjekkia</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisering i Kina – ER-konfigurasjoner</td>
<td>
<ul>
<li>Format for aldersfordeling for kunde for Kina</li>
<li>Format for analyserapport for kundens forfalte beløp for Kina</li>
<li>Format for aldersfordeling for leverandører for Kina</li>
<li>Format for analyserapport for leverandørens forfalte beløp for Kina</li>
<li>Kundebetalingsformat for aldersfordelingsanalyse for Kina</li>
<li>Format for kundesaldorapport for Kina</li>
<li>Format for rapport for finanskontosaldo for Kina</li>
<li>Format leverandørsaldorapport for Kina</li>
<li>GBT-fil for Kina</li>
<li>Format for eksportfil for gyllen avgift</li>
<li>Format for rapport om avvik i produksjonsforbruk for Kina</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisering i Estland – ER-konfigurasjoner</td>
<td>
<ul>
<li>EU-salgsliste i XML-format for Estland</li>
<li>Intrastat-format for Estland</li>
<li>Erklæring for omklassifisering av lager for Estland</li>
<li>ISO20022 Betalingsformat for kredittoverføring for Estland</li>
<li>Rapport for kunde-/leverandørsaldovarsel for Estland</li>
<li>Mva-oppgave for Estland</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisering i Finland – ER-konfigurasjoner</td>
<td>
<ul>
<li>TXT-format for EU-salgsliste for Finland</li>
<li>Intrastat-format for Finland</li>
<li>ISO20022 Betalingsformat for kredittoverføring for Finland</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisering i Ungarn – ER-konfigurasjoner</td>
<td>
<ul>
<li>EU-salgsliste i XML-format for Ungarn</li>
<li>Intrastat-format for Ungarn</li>
<li>Forenklet Intrastat-format for Ungarn</li>
<li>Eksportformat for fakturaliste for Ungarn</li>
<li>Mva-oppgave for Ungarn</li>
<li>Spesifisert mva-oppgave for Ungarn</li>
<li>Lageroppgave for Ungarn</li>
<li>MultiCash-betalingsformat for Ungarn</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisering i Italia – ER-konfigurasjoner</td>
<td>
<ul>
<li>Intrastat-format for Italia</li>
<li>Prosjektfakturaformat for Italia</li>
<li>Salgsfakturaformat for Italia</li>
<li>ISO20022 Betalingsformat for kredittoverføring for Italia</li>
<li>ISO20022 Avtalegiroformat for Italia</li>
<li>Format for RIBA-inkassoremisse for Italia</li>
<li>Rapport om avgiftstransaksjoner innenlands for Italia</li>
<li>Blokkeringslisterapport for Italia</li>
<li>Modello770-rapport for Italia</li>
<li>Rapport om årlig mva-kommunikasjon for Italia</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisering i Latvia – ER-konfigurasjoner</td>
<td>
<ul>
<li>Rapport om bruk av kontantkvitteringer (LV)</li>
<li>XML-format for EU-salgsliste for Latvia</li>
<li>Korrigeringer i XML-format for EU-salgsliste for Latvia</li>
<li>Intrastat-format (A) for Latvia</li>
<li>Intrastat-format (B) for Latvia</li>
<li>Lageropptellingsliste for Latvia</li>
<li>Lageropptellingserklæring for Latvia</li>
<li>Lagerbevegelse for Latvia</li>
<li>Følgeseddel for intern overføring for Latvia</li>
<li>Dokument for omklassifisering av lager for Latvia</li>
<li>ISO20022 Betalingsformat for kredittoverføring for Latvia</li>
<li>Mva-oppgave for Latvia</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisering i Litauen – ER-konfigurasjoner</td>
<td>
<ul>
<li>EU-salgsliste i XML-format for Litauen</li>
<li>Intrastat-format for Litauen</li>
<li>Beholdningsoppgave for Litauen</li>
<li>ISO20022 Betalingsformat for kredittoverføring for Litauen</li>
<li>Kunde-/leverandørrapport for mellomavstemming for Litauen</li>
<li>Mva-oppgave for Litauen</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisering i Norge – ER-konfigurasjoner</td>
<td>
<ul>
<li>Inkassobrevformat for Norge</li>
<li>AutoGiro-betalingsformat for Norge</li>
<li>Format for AvtaleGiro-kundebetalingsformat for Norge</li>
<li>Format for eFaktura-kundebetalingsformat for Norge</li>
<li>ISO20022 Betalingsformat for kredittoverføring for Norge</li>
<li>NETS-betalingsformat for Norge</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisering i Polen – ER-konfigurasjoner</td>
<td>
<ul>
<li>Intrastat-format for Polen</li>
<li>Lagerdokumenter for Polen</li>
<li>Dokument for omklassifisering av lager for Polen</li>
<li>MultiCash-betalingsformat for Polen</li>
<li>MultiCash-betalingsformat utenlands for Polen</li>
<li>Bekreftelsesrapport for kunde-/leverandørsaldovarsel for Polen</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisering i Saudi-Arabia – ER-konfigurasjoner</td>
<td>Format for tildeling av tillegg for banklokasjon for Saudi-Arabia</td>
</tr>
<tr>
<td>Lokalisering i Spania – ER-konfigurasjoner</td>
<td>
<ul>
<li>TXT-format for EU-salgsliste for Spania</li>
<li>Intrastat-format for Spania</li>
<li>Prosjektfakturaformat for Spania</li>
<li>Salgsfakturaformat for Spania</li>
<li>ISO20022 Betalingsformat for kredittoverføring for Spania</li>
<li>ISO20022 Avtalegiroformat for Spania</li>
<li>Bokformat for spansk mva-register</li>
<li>Format for sammendrag av spansk mva-register</li>
<li>Eksport av rapport 347 til ASCII for Spania</li>
<li>Rapport 347 for Spania</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisering i Sverige – ER-konfigurasjoner</td>
<td>
<ul>
<li>Intrastat-format for Sverige</li>
<li>Format for Bankgirot-autogirokundebetaling for Sverige</li>
<li>Format for Bankgirot-leverandørbetalinger for Sverige</li>
<li>Format for SWIFT-leverandørbetaling for Sverige</li>
<li>Format for SIE-eksport for Sverige</li>
<li>ISO20022 Betalingsformat for kredittoverføring for -format</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalisering i Sveits – ER-konfigurasjoner</td>
<td>
<ul>
<li>DebitDirect-betalingsformat for Sveits</li>
<li>LSV DebitDirect-betalingsformat for Sveits</li>
<li>ISO20022 Betalingsformat for kredittoverføring for Sveits</li>
<li>ISO20022 DebitDirect-betalingsformat for Sveits</li>
<li>Format for import av ESR-bankkontoutdrag for Sveits</li>
</ul>
</td>
</tr>
<tr>
<td>Tyskland – Eksportere leverandørbetalinger i DTAZV-format</td>
<td>Tyskland krever DTAZV med utenlandsk formatspesifisering, som representerer en kredittoverføringsmelding (leverandørbetaling) i henhold til spesifikasjonen for betalinger over grenser fra Tyskland til en konto i en utenlandsk bank eller en innenlands bank i en fremmed valuta.</td>
</tr>
</tbody>
</table>

### <a name="electronic-reporting"></a>Elektronisk rapportering

| Hva du kan gjøre | Hvorfor dette er viktig |
|-----------------|-----------------------|
| Konfigurer ER-rapporter for å sette inn data, i flere formater, fra lager for dokumentbehandling i elektroniske meldinger som genereres. | ER-rapporter kan sette inn data i elektroniske meldinger som genereres, fra lageret for dokumentbehandling. Derfor kan vedleggene i et forretningsdokument legges til elektroniske meldinger som genereres for dokumentet, i samsvar med de lovlige kravene. For øyeblikket kan disse vedleggene legges til i MIME-format i en XML-postmelding som genereres. Vedlegg kan eventuelt legges til i Base64-format i en binær melding som genereres. |
| Konfigurer ER rapporter til å generere elektroniske dokumenter i Excel-, Microsoft Word- eller PDF-format. | Én konfigurasjon gir ER-rapporter muligheten til å generere elektroniske dokumenter i tre forskjellige formater: OpenXML-regneark (Excel), Word og XML Forms Data Format (XFDF) (PDF). Brukere kan velge et format ved å legge til en formatmal i en ER-rapport som et Excel-, Word- eller PDF-dokument. |
| Konfigurer ER-rapporter til å sette inn data i topp- og bunntekster i elektroniske dokumenter som er generert i OpenXML-regnearkformat, og til å kontrollere sideskift. | ER-rapporter kan skrive inn forretningsdata i topp- og bunntekster, og de kan også styre hvor sideskift oppstår. Rapportene kan derfor støtte statisk topp- og bunndeler for sidene i de elektroniske dokumentene som genereres. De kan også støtte bestemt sideveksling til disse dokumentene, slik at de overholder juridiske krav. |
| Konfigurer målet for ER-rapporter slik at utdataene sendes som e-post, og slik at forretningsdata og ER-logikk (uttrykk) kan brukes til å angi e-postadressen skal brukes under kjøring. | Da du tidligere konfigurerte et ER-mål, kunne e-postadressen til utdataenes mottaker defineres under utformingen. Du kan nå konfigurere et uttrykk i ER-formatet. Dette uttrykket kan deretter velges i et mål som kilde for e-postadressen for hver formatkonfigurasjon og hver komponent (mappe eller fil) separat. Når du kjører en ER-rapport, kan hver fil som er genereres, derfor sendes til en annen mottaker, og e-postadressen kan defineres basert på ER-logikken og forretningsdataene. |
| Konfigurer målet for ER-rapporter slik at utdataene sendes til Microsoft SharePoint-mappen som en ny navngitt fil eller en ny versjon av den eksisterende filen, og slik at forretningsdata kan brukes i rammeverket for Microsoft Power BI som et datasett eller en rapport. | Når du konfigurerer ER-rapporter, kan du nå lett (uten koding) forberede de ønskede forretningsdataene slik at de kan brukes av Power BI-rammeverket. Når du kjører disse ER-rapportene, kan du formidle riktige forretningsdata og/eller Excel-rapporter som er tilgjengelige, til Power BI-rammeverket. Hvis du planlegger at rapporten kjøres i gjentakende modus, kan du opprette den planlagte sendingen av forretningsdata fra Dynamics 365 for Operations til Power BI for å støtte oppdateringstidsplanen Power BI-baserte rapporter. |
| Konfigurer ER-rapporter til å bruke delen av det elektroniske dokumentet som allerede har blitt generert som en datakilde for å generere resten av dokumentet. | Du kan konfigurere ER-rapporter som oppretter utdataene i tekstformat, til dokumentets linjeopptelling. Denne informasjonen kan deretter brukes i andre deler av dokumentet til å opprette linjer med detaljer for sammendrag. Sammendragsinformasjonen (totaler og nummer) kan beregnes og skrives til de elektroniske dokumentene som er generert, uten at det kreves ekstra transformasjoner av dataene. Denne funksjonen forbedrer derfor ytelsen for kjøring av rapporten, og bidrar til å gjøre fremtidig vedlikehold av det konfigurerte ER-formatet enklere. |
| Konfigurer ER-rapporter til å angi filtypen for elektroniske dokumenter som genereres i tekstformat. | Du kan konfigurere ER-rapporter til å opprette utdataene i tekstformat, slik at de kan lagres som en fil som har en bestemt filtype. I tillegg til standard TXT-filtype, kan du konfigurere filtyper som CSV og PRN, i samsvar med formatspesifikasjonen. |
| Opprett nye ER-rapporter som er basert på en bestemt versjon av en ER-modell. | Da du tidligere opprettet et nytt ER-format, kunne bare den nyeste versjonen av den valgte ER-modellen brukes som formatets datakildeplassering. Nå kan du velge en tilgjengelig versjon av den valgte ER-modellen. Med denne funksjonen kan du vedlikeholde ER-rapporter for gjeldende år og utforme en ny versjon av ER-modellen det neste året parallelt. |
| Søk i datakilder og formater/modeller etter tekst eller valgte artefakter med ett klikk. Løs rebaseringskonflikter proaktivt, og løs konflikter mellom konfigurasjoner. Konfigurer ER-rapporter til å opprette flere valideringsmeldinger for feil som oppdages før kjøring av rapporten stoppes. | Flere forbedringer i brukererfaringen i ER-rammeverket hjelper brukere med å arbeide mer effektivt og enklere med ER. |
| Vis arbeidsområdet **ER** i Power BI-rapporter. | Brukere kan konfigurere siden **ER-arbeidsområde** slik at den inneholder nye menyelementer og dynamiske fliser som kjører de Power BI-baserte rapportene. |

## <a name="payroll"></a>Lønn

<table>
<thead>
<tr>
<th>Hva du kan gjøre</th>
<th>Hvorfor dette er viktig</th>
</tr>
</thead>
<tbody>
<tr>
<td>Konfigurer lønnsposter og behandle lønn ved hjelp av funksjonen som tilsvarer funksjonaliteten til modulen <strong>Lønn</strong> i Microsoft Dynamics AX 2012 R3.</td>
<td>Du kan nå konfigurere og behandle amerikansk lønn ved hjelp av et funksjonssett som tilsvarer funksjonssettet i AX 2012 R3.
<ul>
<li>Du kan konfigurere lønnssykluser og lønnsperioder, arbeidssykluser og arbeidsperioder, inntektskoder og inntektskodegrupper, tidsplaner, permisjonstyper og fordelsavsetninger.</li>
<li>Du kan også definere obligatoriske fradrag for både fordeler og avgifter, og du kan registrere lønnsinformasjon for stillinger og arbeidere for rapportering og analyse.</li>
<li>Du kan også opprette og administrere fradrag for tredjemannsutlegg og skattefradrag, og for eventuelle tilknyttede administrative avgifter.</li>
</ul>
</td>
</tr>
<tr>
<td>Overvåk og behandle lønnsperiodeprosessen ved å bruke det nye arbeidsområdet <strong>Lønnsbehandling</strong>.</td>
<td>Du kan nå overvåke lønnsprosessen enkelt. Lønnsadministratorer kan raskt se inntekts- og betalingsoppgaver som krever handling, slik at betalingskjøringen blir komplett og nøyaktig. Arbeidsområdet <strong>Lønnsbehandling</strong> lar brukere overvåke og kjøre ende-til-ende-prosesser fra ett arbeidsområde.</td>
</tr>
<tr>
<td>Generer positive betalingsfiler for lønnssjekker.</td>
<td>Det finnes en ny filtype i funksjonaliteten for positiv betaling for kontant- og bankbehandlingen for lønnsutbetalinger. Egne menyelementer er lagt til i kjerneprosessen for å aktivere isolert konfigurasjon som er spesifikk for lønn. Funksjonen er identisk med funksjonen for positiv betaling for kjerne som ble lansert i Microsoft Dynamics AX versjon 7.0.1 (mai 2016). På grunn av denne filtypen er lønnsdata fullstendig isolert fra resten av dine positive betalingstransaksjoner. Denne isolasjonen bidrar til å sikre at bare lønnsbrukere har tilgang til og kan vise data som gjelder lønn.</td>
</tr>
<tr>
<td>Importer linjer i inntektsoppgave fra en ekstern kilde ved å bruke den nye enheten for linje i inntektsoppgave.</td>
<td>Ved hjelp av en viktig ny dataenhet kan du integrere med eksterne tids- og inntektsberegningssystemer. Dataenheten importerer inntektsoppgavelinjer og utfører all den samme standardlogikken som brukeren registrerte direkte i inntektsoppgaven. Etter import blir linjene automatisk knyttet til det riktige inntektsoppgavedokumentet. Hvis et riktig dokument for inntektsoppgave ikke finnes, opprettes det automatisk et dokument.</td>
</tr>
</tbody>
</table>

## <a name="planning-and-scheduling"></a>Planlegge og tidsplanlegge

| Hva du kan gjøre | Hvorfor dette er viktig |
|-----------------|-----------------------|
| Angi standardordreinnstillinger for salg og innkjøp basert på en hvilken som helst aktiv produktdimensjon i hovedplanleggingen for produktet. Derfor kan du definere standardordreinnstillinger for lagerføringsenheten (LFE) eller en delvis LFE. | Du kan angi standard ordreinnstillinger som gjelder for en produktdimensjon eller en kombinasjon av produktdimensjoner.<p>**Eksempel**</p><p>Du kan selge et produkt som heter Polo-t-skjorte. Dette produktet er tilgjengelig i to farger: grønn og blå. Det er også tilgjengelig i to størrelser: Liten eller Middels. Farge og størrelse er aktive produktdimensjoner for Polo-t-skjorte. Du kan blokkere innkjøp av alle grønne Polo-t-skjorter, uavhengig av størrelse.</p> |

## <a name="product-master-data"></a>Produkthoveddata

<table>
<thead>
<tr>
<th>Hva du kan gjøre</th>
<th>Hvorfor dette er viktig</th>
</tr>
</thead>
<tbody>
<tr>
<td>Definer alle standardinnstillingene for bestilling og stedsbestemte bestillingsinnstillinger samtidig, fra én side.</td>
<td>Denne funksjonen gir bedre oversikt over innstillinger.</td>
</tr>
<tr>
<td>Opprett en nomenklatur for produktvariantnumre.</td>
<td>Du kan inkludere elementer, for eksempel produktdimensjoner, attributter og tegn i produktvariantnumrene. Når du oppretter en salgsordre eller en kjøpsordre, kan du raskt finne den bestemte produktvarianten.</td>
</tr>
<tr>
<td>Søk etter produkter og produktvarianter i salg- og kjøpsscenarier.</td>
<td>Når du oppretter en salgslinje eller bestillingslinje, kan du søke etter produkter ved hjelp av produktdimensjoner og produktnumre unntatt GTIN-numre (Global Trade Item Numbers) og strekkoder. Dette søket er et fulltekstsøk som erstatter eksisterende "begynner med"-søket som brukes i oppslagslisten for salg og kjøp. Med denne funksjonen kan du finne grupper med varer som har like egenskaper eller ett produkt som har unike egenskaper. Hvis du vil aktivere denne funksjonen, velger du parameteren <strong>Aktiver oppslag for produktsøk</strong> på siden <strong>Søkeparametere</strong>.</td>
</tr>
<tr>
<td>Angi produktvarianten direkte når du oppretter en salgs- eller bestillingstransaksjon. Du kan også velge i en liste over gyldige dimensjonskombinasjoner.</td>
<td>Denne funksjonen øker produktiviteten.
<p><strong>Eksempel</strong></p>
<p>Du kan selge et produkt som heter Polo-t-skjorte. Dette produktet er tilgjengelig i to farger: grønn og blå. Det er også tilgjengelig i to størrelser: Liten eller Middels. Farge og størrelse er aktive produktdimensjoner for Polo-t-skjorte. Når du angir en salgslinje for Polo-t-skjorte som har Grønn for farge og Liten for størrelse, trenger du ikke lenger skrive inn data i feltene <strong>Varenummer</strong>, <strong>Farge</strong> og <strong>Størrelse</strong>. Du kan opprette linjen ved å gjøre ett av følgende:</p>
<ul>
<li>I feltet <strong>Varenummer</strong> angir du produktvariantnummeret, verdien for en farge eller størrelsen. Finn den bestemte varianten som du vil selge, i oppslaget, og opprett salgslinjen.</li>
<li>I feltet <strong>Varenummer</strong> angir du varenummeret. Gå til et produktdimensjonsfelt. I oppslaget <strong>Produktdimensjon</strong> ser du alle de frigitte dimensjonskombinasjonene som gjelder for Polo-t-skjorte. Du kan velge produktvarianten du vil selge, i ett trinn.</li>
</ul>
</td>
</tr>
<tr>
<td>Angi om produktnumre vises på transaksjonssider.</td>
<td>Transaksjonssidene, for eksempel salgsordrer og bestillinger, viser bare feltene <strong>Varenummer</strong> og <strong>Produktnavn</strong>. Hvis du vil vise feltet <strong>Produktnummer</strong>, velger parameteren <strong>Vis produktnumre i skjemaer</strong> under <strong>Parametere for produktinformasjonsbehandling</strong>.</td>
</tr>
</tbody>
</table>

## <a name="project-management-and-accounting"></a>Prosjektstyring og regnskap

| Hva du kan gjøre | Hvorfor dette er viktig |
|-----------------|-----------------------|
| Bruk senere valg når du posterer fakturaforslag i en satsvis jobb. | Regnskapsførerne kan definere at en satsvis jobb skal plukke opp fakturaforslag for postering automatisk, hvis disse forslagene oppfyller kriteriene som er angitt for den satsvise jobben. Denne funksjonen forbedrer automatisering av postering av fakturaen, fordi den satsvise jobben kan kjøre fortløpende og automatisk plukker opp forslag for postering. |
| Opprett analyse på Power BI Desktop. | Business intelligence-innhold (BI) for prosjektrelaterte og ressursrelaterte data kan lett opprettes i Power BI Desktop. |
| Bruk forskuddsbetalinger for bestillinger, og inkluder dem riktig i prosjektestimatprosessen. | For prosjektbestillinger må forskuddsbetalinger behandles før det gis ut noen betaling til leverandører. Disse forskuddsfakturaene vises nå i prosessen for prosjektestimat/-føring for typen **Fastpris**. |
| Få tilgang til og behandle estimater for kostnader og inntekter og varebehov, direkte fra en WBS-oppgave (arbeidsnedbrytningsstruktur). | Du kan styre kostnadsestimater, omsetningsestimater og varebehov for en bestemt WBS-oppgave i dialogboksen Detaljer for den aktiviteten i visningen WBS-planlegging. |
| Velg en finansieringskilde for gebyrjournaler. | Hvis kontrakten for et prosjekt inneholder flere finansieringskilder, kan du velge én bestemt finansieringskilde ved postering av gebyrer. Hvis ikke du velger en bestemt finansieringskilde, brukes finansieringsreglene som er angitt i kontrakten, til å tildele gebyret. |
| Åpne prosjektoppgaver i Excel. | Med enheter for nye data for finansoppdateringer og budsjettoppdateringer kan du åpne prosjektoppgavedata i Excel og opprette analyse ved hjelp av Excel-funksjonalitet. |
| Bruk bare én konfigurasjonsnøkkel til å aktivere funksjonaliteten for prosjektstyring og regnskap (PMA). | De prosjektrelaterte konfigurasjonsnøklene har blitt erstattet av én konfigurasjonsnøkkel for prosjekt som aktiverer PMA-funksjonaliteten. |

## <a name="retail-and-commerce"></a>Detaljhandel og handel

### <a name="advanced-warehouse-management-in-a-retail-store"></a>Avansert lagerstyring i en butikk

Forhandlere kan bruke den avanserte løsningen for lagerstyring (WHS) i sine butikker, og gjøre de nødvendige oppdateringene i de gjeldende POS-funksjonene (Point of Sale) du vil aktivere. Prosessene for den håndholdte løsningen skal fungere i en butikk som de gjør i alle andre lagertyper. Alle gjeldende butikklagerprosesser og POS-prosesser som oppretter eller oppdaterer lagertransaksjoner, oppdateres slik at de bruker de spesifikke kravene for WHS-aktiverte lagre.

| Hva du kan gjøre | Hvorfor dette er viktig |
|-----------------|-----------------------|
| Bruk POS til å slå opp tilgjengelig lager i WHS-aktiverte butikker. | Når du bruker lageroppslag, bør prosessen fungere på samme måte som tidligere. Oppslaget skal vise det disponible antallet på lagernivå, og bør ikke vurdere dimensjonene Sted, Lagerstatus eller Nummerskilt. |
| Bruk POS til å behandle en produktkvittering for en overføringsordre i en WHS-aktivert butikk. | Du kan motta overføringsordrer på salgsstedet for et WHS-aktivert lager og varer. Brukeren skal kunne velge hvilke lokasjoner varer skal mottas på, og skal kunne angi nummerskilt-ID-er for å fylle ut mottakslinjene automatisk. |
| Bruk POS til å behandle en produktkvittering for en bestilling i en WHS-aktivert butikk. | Du kan motta bestillinger på salgsstedet for et WHS-aktivert lager og varer. Brukeren skal kunne velge hvilke lokasjoner varer skal mottas på, og skal kunne angi nummerskilt-ID-er for å fylle ut mottakslinjene automatisk. |
| Bruk POS til å behandle en levering av produkter fra en WHS-aktivert butikk. | Du kan registrere overføringer fra salgsstedet for et WHS-aktivert lager og varer. Brukeren må være i stand til å velge hvilke lokasjoner leveringer skal sendes fra, statusen på varelageret må genereres automatisk, og nummerskilt må ignoreres. |

### <a name="enable-seamless-omni-channel-commerce"></a>Aktiver sømløse omnikanalhandelsfunksjoner

Sømløse omnikanalhandelsfunksjoner refererer til administrasjon og ordrebehandling på tvers av bankens fysiske butikker, nettbutikkfasader, telefonsentre og mobile utsalgssteder. Følgende investeringer er gjort i dette området for denne versjonen:

- Forbedringer for publisering for e-handelsfasader
- En ny mobilapp rettet mot forbrukere som muliggjør produktsøk, kontobehandling og netthandel

| Hva du kan gjøre | Hvorfor dette er viktig |
|-----------------|-----------------------|
| Kunde: Den gjeldende versjonen av den forbrukerrettede appen legger til rette for følgende funksjoner: Produktsøk, Kategorilesing, Legg til handlekurv og Sjekk ut som gjest. Forhandlere kan også bruke firmaets merking i programmet, og deretter merke den for Android- App Store-butikkene. | Forhandlere kan enkelt opprette en forbrukerrettet app som lar kundene bla gjennom, søke etter produkter og levere produkter som gjest fra mobile enheter. |
| Kundeønskelister for e-handelsnettfasader | Uavhengige programvareleverandører (ISV-er) kan bruke ønskelistekontrollen til å la brukere opprette og administrere flere lister i sin nettbutikkfasade, og viser eller bruke de listene i POS. |
| Oppretting av asynkron kunde via e-handelsnettfasader | Uavhengige programvareleverandører kan nå opprette kundekontoer selv om Commerce Data Exchange: Real-time Service er ikke tilgjengelig. |
| Publiser kanalprodukter fra detaljhandelsserveren til tredjepartsfasader. | Detaljhandelsserveren støtter nå tjeneste-til-tjeneste-godkjenning. Uavhengige programvareleverandører kan dra nytte av publisering av kanalprodukt fra detaljhandelsserveren til tredjepartsfasader. |

### <a name="extensibility"></a>Utvidelsesmuligheter

- Commerce-kjøretidsprosjekter blir nå forseglet fra Retail SDK.
- Enklere distribusjon og vedlikehold med komponentinndelte Microsoft-komponentpakker og ISV-pakker for salgssted, detaljhandelsserver, databaser, betaling og maskinvarestasjoner.

| Hva du kan gjøre | Hvorfor dette er viktig |
|-----------------|-----------------------|
| CRT-/detaljhandelsserver: Forhandlere eller ISV-er kan utvide CRT med utvidelsesbindinger. Innebygde kodeendringer støttes ikke lenger. | Hvis du vil aktivere fortløpende og kontinuerlig distribusjon, bør innebygde kodeendringer unngås helt. Hvis du i tillegg vil støtte enkel implementering av hurtigreparasjon uten kodesammenslåing og distribusjon for CRT-komponenter. |

### <a name="personalized-product-recommendations"></a>Personlige produktanbefalinger

| Hva du kan gjøre | Hvorfor dette er viktig |
|-----------------|-----------------------|
| Vis personlig produktanbefalinger på flere berøringspunkter på salgsstedet (POS) for å avgjøre hva en kunde kan være interessert i basert på kjøpshistorikken, varer i ønskelisten og varer som andre kunder har kjøpt på nettet og i fysiske butikker | For forhandlere med store kataloger bidrar personlige anbefalinger det enklere for kunden å finne produkter og gir butikkansatte intelligente kunderelasjoner. Ved å presentere produkter som er rettet mot en kundes interesser og kjøpsvaner, kan produktanbefalinger bidra til mersalg for forhandlere og forbedring av kundebevaring. I Retail er produktanbefalinger drevet av kognitive tjenester og Microsoft Azure Machine Learning. |

### <a name="pos-task-recorder"></a>Oppgaveregistrering for salgssted

| Hva du kan gjøre | Hvorfor dette er viktig |
|-----------------|-----------------------|
| Forhandlere kan bruke Oppgaveregistrering for salgssted til å lage opplæringsmateriell, BPM-diagrammer (Business Process Modeler), og generere hjelpeinnhold for å øke produktiviteten og gjennomføre bedre analyse og utforming av programmer. | Hvis du vil aktivere fortløpende og kontinuerlig distribusjon, må innebygde endringer unngås helt. Hvis du i tillegg vil støtte enkel implementering av hurtigreparasjon uten kodesammenslåing og distribusjon for CRT-komponenter. |
| Sanntidshjelp i POS. | Kassereren/lederen kan få hjelp i sanntid fra POS i forretningsprosessen uten å bytte kontekst. |

### <a name="store-system-providing-a-seamless-on-premises-store-experience"></a>Butikksystem: Gir en sømløs, lokal butikkopplevelse

Butikksystemet er et distribusjonsvalg for forhandlere som bidrar til å gjennomføre et sett med operasjoner i butikken, enten det er i en lokal butikk, i Microsoft-skyen eller i kundens egne private sky. For denne versjonen er omfanget bare i butikken. For å gi bedre støtte for miljøer som har langsom og upålitelig nettverkstilkobling, må vi formidle et alternativ for forhandlere for å distribuere kanaldatabasen og detaljhandelsserveren i butikken. De kan deretter fortsette å kjøre sine kjerneforretningsscenarier selv om det ikke er noen forbindelse til hovedkvarterene (HQ). Basert på de forskjellige datapunktene, som inkluderte diskusjoner i ingeniørteamet, resultater av kundeundersøkelser og analyse av konkurrenter, har vi angitt følgende løsningsomfang som det ideelle svaret for våre målkunder:

- En selvbetjeningspakke er tilgjengelig for butikksystemet.
- Standardinstallasjon er en distribusjon med én boks, men egendefinert distribusjon er tillatt.
- Gir enkel distribusjon/selvbetjening.
- Detaljshandelsserveren og butikkdatabasen er i butikken sammen med Async-klienttjenesten.
- Detaljhandelsserveren i butikken kommuniserer direkte med AOS (Application Object Server) i hovedkvarteret for butikksystemet.
- Støtter scenarier på tvers av terminaler der det mangler HQ-tilkobling.
- Retail Modern POS og Cloud POS kommuniserer alltid med detaljhandelsserveren i butikken.
- Støtter Retail Modern POS og Cloud POS der det ikke finnes HQ-tilkobling.
- Støtter en spesifikk frakoblet database for Retail Modern POS (isolert til hver Retail Modern POS-forekomst) der det mangler HQ-tilkobling.
- Godkjenning er basert på tjeneste-til-tjeneste bare for butikksystemet.
- Servicebesøk i sanntid støttes ikke uten en Internett-tilkobling.
- Direkte databasetilkobling for Retail Modern POS til kanaldatabasen støttes ikke.
- Aktiver telemetri/overvåking.

| Hva du kan gjøre | Hvorfor dette er viktig |
|-----------------|-----------------------|
| En forhandler laster ned det selvbetjente installasjonsprogrammet for butikksystemet fra kanaldatabasesiden i Dynamics AX-hovedkontoret, og laster også ned konfigurasjonsfilen. | Forhandleren kan laste ned selvbetjeningspakken sømløst. |
| En forhandler installerer butikksystemet ved hjelp av det selvbetjente installasjonsprogrammet. | Forhandleren kan installere butikksystemet ved hjelp av selvbetjeningspakken. |
| IT-sjefen konfigurerer butikksystemet i Dynamics 365 for Operations (kanaldatabase, kanalprofil, butikk og distribusjonspakke). | IT-sjefen kan konfigurere butikksystemet enkelt og effektivt. |
| En forhandler styrer Retail Modern POS i lokale butikker og kan utføre sanntidsoperasjoner, for eksempel utstede gavekort, når det finnes en tilkobling. | Forhandleren kan utføre sanntidshandlinger fra butikksystemet når det finnes en tilkobling. |
| En forhandler kan synkronisere data fra det lokale butikksystemet til hovedkvarteret når det finnes en tilkobling. | Forhandleren kan synkronisere til og fra butikksystemet når det finnes en tilkobling. |
| En forhandler kan etablere sikker kommunikasjon mellom det lokale butikksystemet og hovedkvarteret. | Forhandleren kan kommunisere sikkert fra butikksystemet når det finnes en tilkobling. |
| Den IT-ansvarlige og Microsoft Operations kan overvåke og rapportere om det lokale butikksystemet (endringer i diagnostikk og rapportering). | Den IT-ansvarlige og Microsoft Operations kan overvåke butikksystemet sikkert og feilsøke effektivt. |

### <a name="universal-windows-platform-app-for-retail-modern-pos"></a>Universal Windows Platform-app for Retail Modern POS

For øyeblikket er Retail Modern POS bare tilgjengelig som et Windows 8.1-program for stasjonære datamaskiner og nettbrett og som skysalgssted for stasjonære PC-er eller nettbrett. I denne versjonen blir moderne salgssted for detaljhandel konvertert til en UWP-app (Universal Windows Platform). Denne endringen gjør at Retail Modern POS kan kjøres på alle Windows 10-enheter (PC, nettbrett eller telefon), og du kan til og med veksle mellom visninger for Continuum-aktiverte enheter.

| Hva du kan gjøre | Hvorfor dette er viktig |
|-----------------|-----------------------|
| Aktiver viktig POS-funksjonalitet for enheter med liten formfaktor. | Retail POS-funksjonalitet er tilgjengelig for telefoner og andre enheter med liten formfaktor som kjører Windows 10. |

## <a name="supply-chain-management"></a>Forsyningskjedeadministrasjon

### <a name="consignment-inventory"></a>Forsendelseslager

| Hva du kan gjøre | Hvorfor dette er viktig |
|-----------------|-----------------------|
| Som leverandør kan du lagre råvarer i kundens lager. Som kunde kan du utsette den faktiske bestillingen til råmaterialer kreves for produksjonen. | Å holde oversikt over råvarer kan være svært dyrt. Ved hjelp av forsendelseslageret kan en leverandør lagre råvarer i kundens lager. Kunden kan deretter utsette den faktiske bestillingen til råmaterialer kreves for produksjonen. Råvarer bestilles og mottas ved hjelp av en etterfyllingsordre for forsendelse. Denne etterfyllingsordren registrerer fysiske transaksjoner, men påvirker ikke økonomimodulen. Hvis du vil skille mellom varer på lager som eies av kunden og leverandøren, kan du bruke dimensjonen for eierlager. Endringen av eierskap for lager håndteres av en journalprosess som håndterer overføringen av eierskap for råvarer fra leverandøreid lager til kundeeid lager. Denne prosessen utløser opprettingen av en bestilling og en produktkvittering.<blockquote>[!NOTE] Denne funksjonen er begrenset til innkommende forsendelse av råvarer for produksjon. Det er ikke integrert med lagerstyring (WHS) og transportbehandling (TMS).</blockquote> |
| Som leverandør kan du få informasjon om hvor mye av forsendelseslageret som overføres til kunden. | Når du fakturerer en kunde, krever leverandøren informasjon om råvarene som ble kjøpt fra forsendelseslageret og datoen for innkjøpet. Leverandøren kan også overvåke lagerbeholdningen hos kunden ved hjelp av grensesnittet for leverandørsamarbeid. |
| Flytt leverandøreid lager ved hjelp av en overføringsjournal. | Hvis du vil spore den fysiske plasseringen av leverandøreid lager, må du kunne registrere plasseringen i systemet. Bruk en overføringsjournal til å registrere den fysiske flyttingen av lageret, for eksempel flytting fra ett sted på et lager til et annet sted i det lageret. |
| Juster leverandøreid lager ved hjelp av en tellingsjournal. | Det er viktig at du beholder den systemets lagerbeholdningen synkronisert med den faktiske fysiske beholdningen. Det leverandøreide lageret kan justeres inn og ut ved hjelp av tellingsprosesser, for eksempel justering av antall og prosesser for journaltelling. |
| Få mer informasjon om støtte for forsendelse i Dynamics 365 for Operations | Hvis du vil ha mer informasjon om støtte for forsendelsesprosesser, kan du se [Forsendelse](../../../supply-chain/inventory/consignment.md), [Definere forsendelse](/d365F-O/fin-ops-core/fin-ops/get-started/consignment), [Opprette en etterfyllingsordre for forsendelse (oppgaveveiledning)](../../../supply-chain/inventory/tasks/create-consignment-replenishment-order.md) og [Endre eierskap for forsendelseslager basert på produksjonsbehov (oppgaveveiledning)](../../../supply-chain/inventory/tasks/change-ownership-consignment.md). |

### <a name="vendor-collaboration-previously-known-as-the-vendor-portal"></a>Leverandørsamarbeid (tidligere kjent som leverandørportalen)

| Hva du kan gjøre | Hvorfor dette er viktig |
|-----------------|-----------------------|
| Gi leverandører muligheten til å respondere på hver bestillingslinje og foreslå endringer. | I noen tilfeller vil leverandører godta noen bestillingslinjer, men avviser andre. Leverandører kan nå administrere bestillingslinjer individuelt. Hver linje kan avvises, godkjennes eller godkjennes med endringer. Leverandører kan for eksempel endre leveringsdatoen, dele opp levering og antall, eller foreslå en alternativ vare. |
| Gi leverandører mulighet til å administrere informasjon for kontaktpersonen. | Leverandører kan vedlikeholde informasjon om kontaktperson for sitt firma. Denne informasjonen inkluderer navn, e-postadresser og telefonnumre. Det gis tilgang til denne funksjonen via en dedikert sikkerhetsrolle. |
| Del dokumenter som er knyttet til bestillinger og leverandører. | Når du må dele dokumenter med en leverandør, for eksempel et dokument om krav, er det nyttig å koble dokumentet til den relevante bestillingen. Leverandøren kan dele notater og vedlegg med kunden ved å koble dokumentet til hans eller hennes svar på bestillingen. Dokumentbehandling er det underliggende støttende rammeverket, og bare notater og vedlegg som er klassifisert som "eksterne", kan deles med leverandører. |
| Klargjør nye leverandørbrukere. | Hvis leverandørene bruker grensesnittet for leverandørsamarbeid, har de en sømløs måte å be om nye brukerkontoer på når nye kontakter må ha tilgang til leverandørsamarbeid. Innkjøpsansvarlige kan sende en forespørsel om en brukerkonto for en kontaktperson i leverandørorganisasjonen. En kontaktperson for leverandøren som allerede er en bruker av leverandørsamarbeid, kan også sende denne typen forespørsel. Denne forespørselen oppretter til slutt en ny bruker i Dynamics 365 for Operations med leverandørspesifikke sikkerhetsroller. Det gjør det også enklere en foreta en forespørsel til Microsoft Azure B2B-portalen for å klargjøre brukeren med en ny Azure Active Directory (Azure AD)-brukerkonto. Leverandører kan også be om at bestemte leverandørbruker deaktiveres, eller at sikkerhetsroller endres. |
| Få mer informasjon om støtte for leverandørsamarbeid i Dynamics 365 for Operations. | Hvis du vil ha mer informasjon om leverandørsamarbeid, kan du se [leverandørsamarbeid med eksterne leverandører](../../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md), [Leverandørsamarbeid med kunder](../../../supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations.md), [Administrere brukere av leverandørsamarbeid](../../../supply-chain/procurement/manage-vendor-collaboration-users.md), [Konfigurere og vedlikeholde leverandørsamarbeid](../../../supply-chain/procurement/set-up-maintain-vendor-collaboration.md) og [Arbeidsområde for leverandørsamarbeidsfakturering](../../../finance/accounts-payable/vendor-portal-invoicing-workspace.md). |

### <a name="intercompany-order-processing"></a>Konsernintern ordrebehandling

<table>
<thead>
<tr>
<th>Hva du kan gjøre</th>
<th>Hvorfor dette er viktig</th>
</tr>
</thead>
<tbody>
<tr>
<td>Direkte på salgsordrelinjer definerer du der behovet skal hentes fra, og hvordan det skal hentes.
<p><strong>Eksempel</strong></p>
<p>Opprett en salgsordrelinje, og angi direktelevering som leveringstype. Hovedleverandøren legges til på salgsordrelinjen som det kildepunktet.</p>
</td>
<td>Flyten for ordrebestilling har blitt betydelig forbedret. Direkte på salgsordrelinjer kan du nå definere der behovet skal hentes fra, og hvordan det skal hentes. Du trenger ikke lenger vente til alle linjene er lagt til salgsordren. Ved hjelp av nye alternativer på salgsordrelinjer kan du angi leveringstypen når du angir en leverandør. Når du knytter en leverandør til salgsordrelinjer, opprettes det ordrekjeder for levering fra leverandøren.
<ul>
<li>Leverandøren kan være en konsernintern leverandør som bruker en intern bestilling og salgsordre, eller det kan være en ekstern leverandør som bruker en ekstern bestilling.</li>
<li>Leveringstypen kan være <strong>Direktelevering</strong> eller <strong>Lager</strong>. Leveringstypen <strong>Lager</strong> angir at leverandøren skal levere til det lokale lageret før den leverer til kunden.</li>
</ul>
</td>
</tr>
<tr>
<td>Opprett et ordreløfte direkte fra salgsordrelinjer.
<p><strong>Eksempel</strong></p>
<p>Opprett en salgsordrelinje som hentes fra en konsernintern leverandør. Forlat linjen. Leveringsdatoer beregnes i henhold til tilgjengeligheten i kildefirmaet.</p>
</td>
<td>Når du oppretter salgsordrelinjer som bruker den nye informasjonen i kilder, beregnes leveringsdatoer i henhold til kontrollen <strong>Leveringsdato</strong>. Hvis det for eksempel er merket av for en konsernintern leverandør, beregnes tilgjengeligheten i kildefirmaet. Dermed opprettes det ordrekjeder automatisk sammen med salgsordrelinjer. Denne funksjonaliteten hjelper med å sikre at leveringsdatoer vises i kildefirmaet, slik at ATP-profilene (available-to-promise) kan håndtere de forventede behovene direkte mens salgordrer opprettes.</td>
</tr>
<tr>
<td>Se gjennom produkttilgjengelighet på tvers av alle kildelokasjoner, og velg beste kildealternativet.</td>
<td>Siden <strong>Leveringsalternativer</strong> har fått ny utforming, og den har nå nyttig informasjon om alle godkjente interne og eksterne leverandører. Denne informasjonen inkluderer kildealternativer for leverandørinnkjøp. Når du velger en leveringsmåte, beregnes mulige leveringsdatoer. Du kan velge det beste alternativet for kunden sømløst, og du kan bruke dette alternativet for alle salgsordrelinjer.</td>
</tr>
</tbody>
</table>

### <a name="warehouse-enhancements-for-high-volume-distribution-centers"></a>Forbedringer i lageret for distribusjonssentre med store volumer

| Hva du kan gjøre | Hvorfor dette er viktig |
|-----------------|-----------------------|
| Opprett arbeid etter at varene er pakket ved en pakkestasjon. | Denne funksjonen er nyttig når det er flere prosesser etter manuelt pakkearbeid (for eksempel lagring på paller, kvalitetsinspeksjon, konsolidering av leveringer, eller endringer i lastesoner). Med den nye arbeidstypen **Plukking av containerpakking** kan du utforme disse oppgavene ved å bruke separate arbeidslinjer. Nå kan du utforme pakkestasjoner for å generere arbeid etter pakking. Dette arbeidet kan brukes til å organisere flytting av pakket lager. |
| Grupper containere ved pakkstasjonen. | Denne funksjonen gjør at flere pakker kan grupperes til én container eller ett nummerskilt på pakkestasjonen. En e-handels-/engrosoperatør kan for eksempel gruppere 100 separat pakkede pakker til én container (for eksempel en pall eller korg). Denne containeren kan deretter flyttes, samles opp eller lastes ved hjelp av én arbeidsinstruksjon som en arbeider genererer ved å skanne én strekkode (nummerskilt) for den grupperte containeren. Denne funksjonen reduserer arbeidstransaksjonene for flytting av mange mindre pakkede containere. Hvis du vil ha mer informasjon, kan du se [Opprette et nytt menyelement for en mobilenhet for skiltnummerkonsolidering (oppgaveveiledning)](../../../supply-chain/warehousing/tasks/create-mobile-device-license-plate-consolidation.md). |
| Opprett en frigivelsespolicy for pakkede containere. | Arbeid som utløses av containerfrigivelse, kan opprettes enten automatisk eller manuelt. Når det skjer automatisk, genereres arbeid når containeren lukkes ved hjelp av lokasjonsdirektivet og rammeverket for arbeidsmal. Når frigivelsen er manuell, kan pakkeren bestemme om arbeidet skal genereres for én container eller en gruppe med containere. Denne funksjonen reduserer risikoen for at lukkede containere blir plukket og flyttet før de er klar til å flyttes fra pakkestasjonen. Det gjør det også mulig for gruppert frigivelse som ikke er systemstyrt. |
| Ny fordeling for plukk med mangler | Har lagt inn støtte for prosesser for plukk med mangler for å hjelpe en kollega som kan ikke plukke varene og ønsker å oppfylle ordren når varen som kreves, er tilgjengelig på et annet sted. Du kan bruke en automatisk prosess for ny fordeling som bruker de samme lokasjonsdirektivene til å hente varene hvis de er tilgjengelige på et annet sted. Når det brukes ny manuell fordeling, viser den mobile enheten en liste over steder sammen med det tilgjengelige antallet. Lagermedarbeideren kan deretter velge hvilket sted lageret skal brukes. fra. Disse to metodene kan angis separat eller kombinert som én kommando på menyen for lagerarbeider. Når manuell ny forordning brukes, kan lagermedarbeideren velge vareantallet for plukk med mangler fra flere steder. Hvis du vil ha mer informasjon, kan du se [Konfigurere ny tildeling av vare for plukking med mangler (oppgaveveiledning)](../../../supply-chain/warehousing/tasks/set-up-short-picking-item-reallocation.md). |
| Flytt beholdning som har arbeid tilknyttet. | Nå kan du flytte beholdning som har arbeid tilknyttet. Denne funksjonen kan være nyttig hvis for eksempel en arbeider vil rydde i mottakssonen og flytte registrerte paller som venter på plassering, til et annet mottakssted. Sonen ryddes og kan motta en ekstra last med varer, og beholdningen som er blitt flyttet, oppdateres med ny plasseringsinformasjon. Denne funksjonen kan også brukes til å frigjøre plass på plukksteder ved å flytte beholdningen med arbeid som er knyttet til det, og å lage plass for etterfylling. Du kan også bruke den til å flytte last fra et oppsamlingssted til et annet uten å miste lastearbeidet som er generert. På denne måten kan funksjonen bidra til å optimalisere tiden det tar å laste lastebiler når de ankommer. Du kan flytte beholdningen som er reservert for salgsordrer, overføre ordreproblemer, overføre ordrekvitteringer og bestillinger. Bevegelse hindres hvis det fører til at linjer deles opp. Hvis du for eksempel har en arbeidslinje for 100 eksemplarer av en vare, kan du bare flytte 30 av dem til en annen plassering. |
| Slå sammen nummerskilt som har arbeid som er tilknyttet. | Du kan slå sammen nummerskilt som har utgående arbeid som er tilknyttet. Når en plukking for eksempel er delt inn i flere arbeidsoppgaver, kan det være nyttig å tillate at nummerskiltene slås sammen når de leveres på oppsamlingslokasjonen. Nummerskilt kan konsolideres bare hvis de er på samme sted, er medlemmer av samme last og har den samme forsendelsesinformasjonen. |
| Frys plukkarbeid som er knyttet til etterfylling på linjenivå. | Nå kan du fryse arbeid på linjenivå i stedet for på overskriftsnivå, slik at arbeidere kan oppfylle plukklinjene som ikke er frosset ved behov for etterfylling. Derfor kan en grossist med store salgsordrer eller en forhandler som har store salgsordrer eller overføringsordrer for etterfylling, tillate at plukkarbeidet starter på alle linjene som ikke er underlagt etterfyllingsarbeid. Plukk- og etterfyllingsarbeidet kan deretter fullføres parallelt. Denne funksjonen kan konfigureres slik at du kan velge om du vil fryse på overskrifts- eller linjenivå. Du kan også bruke begge metodene og opprette en arbeidsmal for hver metode. Hode-/linjekonfigurasjonen er angitt i arbeidsmaler, men du kan endre den direkte i det genererte arbeidet. |
| Avbryt arbeid ved hjelp av mobilenheten. | Nå kan du avbryte arbeidet ved hjelp av mobilenheten med eller uten behov for etterfylling. Tidligere måtte du bruke den rike klienten. Hvis du vil aktivere denne funksjonaliteten, kan du opprette et menyelement for mobil enhet som er satt til **Indirekte**, og med aktivitetskoden satt til **Avbryt arbeid**. |

### <a name="warehouse-operation-enhancements"></a>Forbedringer i lageroperasjon

| Hva du kan gjøre | Hvorfor dette er viktig |
|-----------------|-----------------------|
| Modeller forskjellige containertyper. | Du kan bruke andre containertyper i lageret for å optimalisere lagring og av andre grunner. Den nye containertypeenheten har de fysiske egenskapene til containertypene. Nå kan du knytte nummerskilt med en bestemt containertype og bruke lagringsgrenser for lokasjon. Du kan for eksempel bruke denne funksjonen til å kontrollere hvor mange paller (eller andre typer container) du tillater på et bestemt sted. Containertyper er også lagt til i enhetssekvensgrupper for å legge til standard containertyper for mottaksprosessen. Containertypene kan brukes med innkommende og utgående lokasjonsdirektiver. De kan også brukes i lagerbeholdningsvisningen for å finne ut hvor mange containere som for tiden finnes på lager. Hvis du vil ha mer informasjon, kan du se blogginnlegget [Bruk av nummerskilt som er tilknyttet en containertype for å drive lagerstyringsprosesser](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/20/use-of-license-plates-associated-with-a-container-type-to-drive-warehouse-management-processes/). Selv om dette blogginnlegget beskriver en oppdatering for Microsoft Dynamics AX 2012, er den samme støtten nå lagt til Dynamics 365 for Operations. |
| Tilbakefør forsendelser. | I et lager må du kunne håndtere sene endringer. Noen varer kan for eksempel bli skadet slik at du ikke kan levere. En kunde kan også sende en sen forespørsel om å avbryte eller endre en ordre. I Dynamics 365 for Operations er det nå mulig å tilbakeføre en forsendelse. Derfor kan du annullere en følgeseddel slik at du kan oppdatere den med riktig antall senere. På samme måte kan du annullere produktkvitteringer på den innkommende flyten slik at du kan opprette en oppdatert versjon. |
| Bruk paller som har ulike varer. | Du kan nå motta og registrere en "blandet" pall. En blandet pall består av ulike varer som er samlet på en pall for én eller flere bestillinger eller linjer. Alle registreringer kan oppsummeres i ett målnummerskilt. Denne prosessen aktiveres via mobilenheten for lageret. Når pallen med blandede varer mottas på lageret, identifiserer for eksempel mottaksassistenten varene og antallene på pallen før pallen flyttes til dedikerte plasseringslokasjoner. Plasseringslokasjonene identifiseres av arbeidsmaler og lokasjonsdirektiver. Hvis plasseringslokasjonene er spredt over flere varer som har faste lokasjoner, oppretter denne funksjonen så mange plasseringsarbeidslinjer som det finnes ulike varer på den blandede pallen. Denne funksjonen gjør registrering og plassering av de mottatte pallene med blandede varer raskere og mer fleksibel. Hvis du vil ha mer informasjon, kan du se blogginnlegget [Motta og registrere en pall med blandede kildedokumentlinjer som bruker ett nummerskilt](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/13/receive-and-register-a-pallet-with-mixed-source-document-lines-using-1-license-plate-purchase-order-matching/) og informasjon om støtte for blandet pall i [annonseringen av vår nyeste kumulative oppdatering](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/30/whats-new-in-cu11-for-wms-and-tms/). Selv om dette blogginnlegget beskriver en oppdatering for AX 2012, er den samme støtten nå lagt til Dynamics 365 for Operations. |

### <a name="minor-feature-enhancements-in-supply-chain-management"></a>Små funksjonsforbedringer i forsyningskjedeadministrasjonen

<table>
<thead>
<tr>
<th>Hva du kan gjøre</th>
<th>Hvorfor dette er viktig</th>
</tr>
</thead>
<tbody>
<tr>
<td>Bruk nye dataenheter til å importere og eksportere data.</td>
<td>Du kan importere og eksportere data ved hjelp av disse dataenhetene:
<ul>
<li>Fraktfaktura</li>
<li>Slå sammen lagerbeholdning etter lager og beholdningsstatus</li>
<li>Beholdningsgebyrer</li>
<li>Tilbud</li>
</ul>
</td>
</tr>
<tr>
<td>Bruk den forbedrede Gantt-kontrollen til å utvikle interaktive planscenarier.</td>
<td>Den forbedrede Gantt-kontrollen kan brukes til å utvikle nye interaktive planscenarier og gir forbedrede API-er som kan brukes til å tilpasse utseendet til aktiviteter. Her er noen av de nye API-ene:
<ul>
<li>Loddrett draing og slipping av aktiviteter</li>
<li>Tillegg/fjerning av aktiviteter</li>
<li>Forhåndsvisning av bestilte perioder på sammendragslinje</li>
<li>Endring av farge og stil for aktivitetskantlinjer</li>
<li>Endring av farge, stil og bakgrunn på tekst i rutenett</li>
</ul>
</td>
</tr>
<tr>
<td>Håndter material- og ressursplanlegging på en bedre måte.</td>
<td>Noen forbedringer er gjort i material- og ressursplanleggingen:
<ul>
<li>Antall sikkerhetsdager håndteres nå når en vare er på lager.</li>
<li>Overskriv leveringsdatoen når du autoriserer planlagte bestillinger.</li>
<li>Prioriter fullføring av ordrer over sikkerhetslager.</li>
<li>Forhindre planlegging av planlagte bestillinger i fortiden.</li>
</ul>
</td>
</tr>
<tr>
<td>Rapporter faktisk forbruk for produksjon, og vis lagerstatus.</td>
<td>Du kan vise faktisk forbruk for produksjon. I tillegg er en ny avmerkingsboks, kalt <strong>Vis lagerstatus</strong>, lagt til i <strong>Bevegelse</strong> på menyelementet <strong>Arbeidsopprettelse</strong>, og du kan bruke den til å vise lagerstatus.</td>
</tr>
<tr>
<td>Beregn volumetrisk vekt hvis satsene for transportøren er basert på volumetrisk tykkelse.</td>
<td>En ny motor for TMS-sats, som er basert på volumetrisk vekt, er lagt til, slik at du kan beregne volumetrisk vekt.</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Tilleggsressurser

[Startsiden Hva er nytt eller endret i Finance and Operations](whats-new-changed.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
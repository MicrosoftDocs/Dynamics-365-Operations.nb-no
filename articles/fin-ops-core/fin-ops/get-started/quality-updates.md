---
title: Proaktive kvalitetsoppdateringer
description: Denne artikkelen gir informasjon om proaktiv levering av kvalitetsoppdateringer.
author: rashmansur
ms.date: 09/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 60f9d84b240016671ff726fc3cca2e02cfd811ca
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689234"
---
# <a name="proactive-quality-updates"></a>Proaktive kvalitetsoppdateringer

[!include[banner](../includes/banner.md)]

I løpet av de siste årene har Microsoft gjort fortløpende fremgang for det vi henviser til som [One Version](../../dev-itpro/lifecycle-services/oneversion-overview.md). Forutsetningen for One Version er enkel: Jo nærmere vi kan ha alle kunder i samme programvareversjon, jo høyere kvalitet kan vi levere. Vi finner og retter problemer én gang, og vi får disse løsningene ut til kundene raskere.

Dette premisset bekreftes av resultatene: lavere hendelsestellinger på tvers av produktene våre. Når kunder ikke har samme versjon, ser vi konsekvent at de blir påvirket av problemer som det allerede er en løsning tilgjengelig for. Vi har allerede gjort stor fremgang med Dynamics 365 Finance, Dynamics 365 Supply Chain, Dynamics 365 Project Operations og Dynamics 365 Commerce, og takket være nylige tekniske fremskritt er det nå mulig å gå videre til neste trinn. Informasjonen nedenfor legger opp hva vi skal gjøre, hva vi allerede har gjort for å definere stadiet, og hvordan og når vi skal innføre de nye funksjonene uten avbrudd.

## <a name="focus-on-quality-updates"></a>Fokus på kvalitetsoppdateringer

For øyeblikket tilbyr vi sju [tjenesteoppdateringer](public-preview-releases.md) per år. Versjon 10.0.29 er for eksempel en serviceoppdatering. Inntil nylig var det åtte oppdateringer per år. Vi droppet imidlertid én oppdatering som svar på tilbakemeldinger fra kunder som ønsket å unngå endringer nær slutten av kalenderåret.

Vi endrer ikke frekvensen på serviceoppdateringene. I stedet fokuserer neste trinn i One Version-reisen på *kvalitetsoppdateringer*. Kvalitetsoppdateringer er kumulative bygg på feilrettinger. De inneholder ikke nye funksjoner. På et eller annet tidspunkt er hele kundefellesskapet vår spredt mellom de tre eller fire nyeste serviceoppdateringene. For en eventuell serviceoppdatering kan du imidlertid bruke dusinvis av ulike kvalitetskontrollversjoner i gruppen, avhengig av datoene da personer distribuerte. I neste trinn vil vi proaktivt kringkaste kvalitetsoppdateringer. Vi bruker allerede denne modellen for våre Dataverse-baserte programmer og har sett de forventede resultatene av forbedret kvalitet og reduserte kundestøttehendelser.

En reduksjon i defekter kan selvfølgelig redusere eller fullstendig eliminere behovet for kvalitetsoppdateringer. Vi har flere initiativ i testversjonering for å redusere manglene som krever kvalitetsoppdateringer. Selv om nyttelast reduseres i kvalitetsoppdateringen, vil konsekvensen i hele kundebasen forbedre støtten, få forbedringer til kundene raskere og redusere hyppigheten til kunder som oppdager problemer som det allerede finnes løsninger på.

## <a name="making-proactive-distribution-possible"></a>Gjør proaktiv distribusjon mulig

Det er allerede distribuert flere fremskritt som aktiverer proaktiv levering av kvalitetsoppdateringer:

- **Nær null nedetid-oppdatering** – For å fremskynde hyppigere miljøer er det vesentlig at innvirkningen på tilgjengelighet av miljøet reduseres for å bevare servicenivåavtaler for Dynamics 365. Det ble opprinnelig innført nær null nedetid-oppdatering for å forbedre månedlig oppdatering av operativsystemet ved å bruke en klyngereserve til å aktivere det oppdaterte bildet med minimale forstyrrelser. Mekanismen for bruk av oppdateringer utvides slik at den blir enda mindre forstyrrende, og den dekker både oppdatering av operativsystemet og distribusjon av kvalitetsoppdateringer.

    For interaktive brukere kan en aktiv økt avbrytes, og det gjøres et nytt forsøk i det nå oppdaterte miljøet. Innføringen av [prioritetsbasert satsvis planlegging](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md), som nå er tilgjengelig på forespørsel, partiplanlegging og behandling av gjenoppretting og startes igjen rett etter oppdateringen. Prioritetsbasert partiplanlegging vil være på plass for kunder før de begynner å delta i proaktiv distribusjon av kvalitetsoppdateringer for produksjonsmiljøene.

- **Mørketimer** – Mørketimer defineres for hvert Azure-område og nær null nedetid-oppdateringer skjer i mørketimeperioden.

## <a name="the-proactive-update-process"></a>Den proaktive oppdateringsprosessen

Distribusjon av proaktive kvalitetsoppdateringer vil følge en sikker distribusjonsprosess (SDP). Detaljene i SDP-en vil utvikle seg, men kvalitetsoppdateringer vil i utgangspunktet bli distribuert til sandkassemiljøer. Prosessen starter med miljøer som velger tidlig distribusjon. Etter hvert som prosenten av økningene i distribusjonen av avmerkingsboksene er fullført, vil distribusjonen til produksjonsmiljøer begynne. Igjen starter prosessen med miljøer som velger tidlig distribusjon. Lyttesystemer overvåker systemtemetri og Livesite-hendelser, og vil stoppe utrullingen av en bestemt versjon hvis det oppdages en regresjon. Kundene vil fortsatt kunne hente kvalitetsoppdateringene før proaktiv distribusjon hvis de ønsker det.

Nåværende frigivelsesbehandlingsdata viser at mindre enn tre prosent av regresjonene innføres i kvalitetsoppdateringer. Med økt fokus på eliminering av regresjon og utvidet SDP vil den potensielle virkningen av regresser være lavere enn kvalitetsgevinstene som oppnås ved å gjøre reparasjonene raskere for kundene generelt.

## <a name="process-changes"></a>Behandle endringer

Et sett med prosessendringer implementeres før aktiveringen av distribusjon av proaktiv kvalitetsoppdatering:

- **Skjema** – Verktøy vil sikre at kvalitetsoppdateringsbuilds omfatter bare skjemaendringer som kan brukes mens tjenesten er tilkoblet. Denne fremgangsmåten vil bidra til å bevare muligheten til å bruke oppdateringen med nær null nedetid.
- **Økt endringsgransking** – For øyeblikket er det allerede et ekstra prosesstrinn som skal godkjenne endringer for inkludering i en kvalitetsoppdatering. Granskingen i det ekstra trinnet økes for å redusere faren for regresjoner. Det å bryte endringer som ikke er tillatt i kvalitetsoppdateringer, og den økte endringsgranskingen vil bidra til å sikre at vi oppfyller dette målet.
- **Synlighet** – Vi sender meldinger via administrasjonssenteret, Lifecycle Services (LCS) og andre tilgjengelige kanaler for kommende proaktive kvalitetsoppdateringer. I tillegg vil støttegrupper og hendelses kundeemner ha oversikt over hvor kvalitetsoppdateringer er distribuert proaktivt.
 > [!NOTE]
 > Microsoft Communications-teamet undersøker en pågående nedgradering av e-postverktøyet som forhindrer levering av e-postvarslinger. Fortsett å overvåke Microsoft 365-meldingssenteret for pålasting og varslingsrelaterte meldinger.
- **Sikkerhet via testversjonering** - Testversjonering brukes til å verne kodeendringer der det er aktuelt i en reparasjon av kvalitetsoppdatering eller bruke den eksisterende testversjoneringen som er relevant for reparasjonen. Hvis du må tilbakefalle eller slå av en endring etter en proaktiv distribusjon, kan du gjøre det via testversjoneringen for å unngå ytterligere feil.
- **Synkroniseringsbetegnelsen for sandkasse** – Mindre enn 20 prosent av kundene i dag har flere avmerkingsbokser, og én avmerkingsboks er distribuert der versjonen samsvarer med produksjonen, som hjelp til feilsøking. Hvis en kunde bruker en sandkasse til å teste en nyere versjon enn produksjonen, vil denne sandkassen motta kvalitetsoppdateringer for den nyere versjonen.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Hva er utrullingsveikartet for kvalitetsoppdateringer?

Distribusjon av proaktive kvalitetsoppdateringer for sandkassemiljøer ventes å starte i slutten av september eller oktober 2022 for de offentlige Azure-skykundene. Prøvemiljøer vil også begynne å motta proaktiv oppdateringsdistribusjon på det tidspunktet. I september sendes det en melding til hver kunde for å informere dem om den forventede planen for miljøet. Unntak til den proaktive oppdaterte distribusjonsprosessen vil bare være tillatt for FDA-regulerte kunder. Vi holder fremdeles på med hvordan regulerte miljøer og kunde av nasjonale skyer og skyer for offentlig sektor skal administreres.

I løpet av den neste seksmåneders perioden vil vi gradvis øke prosenten av sandkassemiljøer som mottar proaktive oppdateringer, til alle utpekte miljøer er inkludert, og fremdriften for oppdatering av produksjonsmiljøer. Gjennom hele perioden overvåker vi for å sikre at distribusjonsprosessen er sømløs, og at vi når målet vårt for ikke-forstyrrende nyttelast.

Siden kunder regelmessig vil motta mindre nyttelaster, forventer vi at prosessen med nåværende behov blir enklere. Vi justerer frekvensen til oppdateringsdistribusjonen når vi viser muligheten til å kjøre prosessen uten avbrudd. Denne prosessen fungerer allerede effektivt for Dataverse-plattformen og programmene våre og leverer de forventede forbedringene i servicekvaliteten. Vi ønsker å ta det samme steget fremover for økonomi- og driftsapper.

## <a name="when-will-quality-updates-start-for-production-environments"></a>Når starter kvalitetsoppdateringer for produksjonsmiljøer?
På dette tidspunktet er kvalitetsoppdateringer bare rettet mot sandkasser. Vi oppdaterer dette området med startdatoen for produksjonsmiljøer når vi har flere data og mål fra proaktive oppdateringer for avmerkingsbokser til måling av beredskap for prod.

## <a name="what-is-the-schedule-for-sandbox-proactive-quality-updates"></a>Hva er tidsplanen for proaktive kvalitetsoppdateringer for sandkassemiljøer?
Hvis du vil ha informasjon om mørketimer for hvert område, kan du se [Hva er de planlagte vedlikeholdsperiodene etter område?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).

### <a name="proactive-quality-update-release-10028"></a>Proaktiv kvalitetsoppdateringsutgivelse: 10.0.28
**Appversjon: 10.0.1265.89**
**Tilsvarende siste KB-artikkel: 745340**

| Stasjon | Områder | Fullført tidsplan| Kommende sandkasseplan
|---|---|---|---|
| Stasjon 1 | Canada, sentralt; Canada, øst; Frankrike, sentralt; India, sentralt; Norge, øst; Sveits, vest | 15. september til 18. september 2022, 19. september til 22. september 2022 og 7. oktober til 10. oktober 2022 | 25. til 28. oktober 2022 |
| Stasjon 2 | Frankrike, sør; India, sør; Norge, vest; Sveits, nord; Sør-Afrika, nord; Australia, øst; Storbritannia, sør; De forente arabiske emirater, nord; Japan, øst; Australia, sørøst; Asia, sørøst | 25. til 28. september 2022 og 7. til 10. oktober 2022 | 25. til 28. oktober 2022 |
| Stasjon 3 | Øst-Asia; Storbritannia, vest; Japan, vest; Brasil, sør; Europa, vest; USA, øst; De forente arabiske emirater, sentralt | 26. til 29. september 2022 og 7. til 10. oktober 2022 | 25. til 28. oktober 2022 |
| Stasjon 4 | Europa, nord; USA, sentralt; USA, vest | 28. til 1. oktober 2022 og 7. til 10. oktober 2022 | 25. til 28. oktober 2022 |
| Stasjon 5 | DoD, Government Community Cloud, Kina | Ikke planlagt | Ikke planlagt |

### <a name="proactive-quality-update-release-10029"></a><a name="schedule"></a> Proaktiv kvalitetsoppdateringsutgivelse: 10.0.29
**Appversjon: 10.0.1326.70**
**Tilsvarende siste KB-artikkel: 748926**

| Stasjon | Områder | Kommende sandkasseplan
|---|---|---|
| Stasjon 1 | Canada, sentralt; Canada, øst; Frankrike, sentralt; India, sentralt; Norge, øst; Sveits, vest | 14. til 17. oktober 2022 |
| Stasjon 2 | Frankrike, sør; India, sør; Norge, vest; Sveits, nord; Sør-Afrika, nord; Australia, øst; Storbritannia, sør; De forente arabiske emirater, nord; Japan, øst; Australia, sørøst; Asia, sørøst | 15. til 18. oktober 2022 |
| Stasjon 3 | Øst-Asia; Storbritannia, vest; Japan, vest; Brasil, sør; Europa, vest; USA, øst; De forente arabiske emirater, sentralt | 16. til 19. oktober 2022 |
| Stasjon 4 | Europa, nord; USA, sentralt; USA, vest | 17. til 20. oktober 2022 |
| Stasjon 5 | DoD, Government Community Cloud, Kina | Ikke planlagt |

> [!IMPORTANT] 
> Fem dager i forveien vil Microsoft oppdatere planen og sende e-postmeldinger til settet med miljøer som skal motta disse kvalitetsoppdateringene. Den forrige planen gjelder bare miljøer som har blitt varslet om en forestående oppdatering. Hvis du vil ha informasjon om mørketimer for hvert område, kan du se [Hva er de planlagte vedlikeholdsperiodene etter område?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).
>
> Planen viser et intervall på fire dager for hver områdegruppe, eller *stasjon*, der det for øyeblikket planlegges en kvalitetsoppdatering. Kvalitetsoppdateringer starter med bare sandkassemiljøer. Deretter, etter hvert som prosenten av økningene i distribusjonen av avmerkingsboksene er fullført, vil distribusjonen til produksjonsmiljøer begynne med forhåndsvarsling til kunder.
> 
> Kvalitetsoppdateringer vil alltid forekomme på en rullende måte som gjør det mulig for oss å målrette et sett med miljøer per plan, og fylle ut alle settene innen slutten av fjerde dag for en stasjon. Dette betyr imidlertid ikke at en miljøoppdatering vil strekke seg over fire dager. Det betyr bare at vi ikke kan forhåndsdefinere hvilke miljøer som oppdateres på en gitt dag innen firedagers intervallet. Alle oppdateringer gjøres i mørketimer, med nesten null nedetid. Oppdateringer avsluttes definitivt i mørketidsvinduet til et angitt område.

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Hvordan håndteres mørketimene for kunder som har én forekomst av økonomi- og operasjonsapper, men som er aktive i flere tidssoner? 
Det finnes ingen spesielle tidsplaner utenom de mørke timene der en forekomst av økonomi- og driftsapper eksisterer, siden vi planlegger å rulle ut kvalitetsoppdateringer på en minimalt forstyrrende måte med [nZDT](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean).

## <a name="what-is-the-current-rollout-cadence-for-proactive-quality-updates"></a>Hva er nåværende utrullingsfrekvens for proaktive kvalitetsoppdateringer?
Proaktive kvalitetsoppdateringer (PQU-er) sendes for øyeblikket én gang i måneden for hver versjon som støttes av en serviceoppdatering. Bare én oppdatering per måned fremskyndes for utvalgte sandkassemiljøer med mindre kunder flytter til en ny serviceoppdateringsversjon. I så fall kan de få en forhåndsplanlagt PQU som del av et eksisterende tog for den nye serviceoppdateringen. Når den globale utrullingen er fullført i 2023, øker frekvensen for disse oppdateringene. Du mottar alltid minst én måneds varsel hver gang det er en endring i forsendelsesfrekvensen.

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Hvordan sikrer Microsoft kvaliteten på disse oppdateringene?
Microsoft gjør sitt ytterste for å holde lanseringsforløpet effektivt nok til å levere små nyttelaster, slik at valideringskostnadene holdes lave. Hver reparasjon i en kvalitetsoppdatering går gjennom en streng og sikker distribusjonsprosess som bidrar til å forbedre kvaliteten og påliteligheten, og dermed reduserer innvirkning for kunden. Distribusjonen vil skje i faser, først i sandkassemiljøer, etterfulgt av produksjon. Distribusjoner i faser sørger for ordentlig overvåking for å finne ut om ytterligere distribusjon er sikkert. Vi stopper utrullingen hvis det oppdages problemer med hver kundegruppe som distribueres, og sikrer at hvert trinn i utrullingen har nok tid til at problemer kan oppdages. For hver kommende kvalitetsoppdatering vil vi gi en oversikt over tidsplanen gjennom oppdateringer i offentlig dokumentasjon og e-postmeldinger, slik at kundene kan planlegge i forveien.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Kan kunder utsette, planlegge på nytt eller stanse en kvalitetsoppdatering midlertidig?
Nei. Hovedmålet med kvalitetsoppdateringer er å sikre at det grunnleggende, for eksempel sikkerhet, personvern, pålitelighet, tilgjengelighet og ytelse, forbedres kontinuerlig for kundene våre. Ved å utsette eller pause en oppdatering vil sikkerhet, tilgjengelighet og pålitelighet være i fare.

## <a name="how-do-i-know-what-set-of-changes-went-into-a-quality-update-payload"></a>Hvordan vet jeg hvilket settet med endringer som ble lagt inn i en kvalitetsoppdateringsnyttelast?
Følgende fremgangsmåte er en midlertidig løsning mens vi fortsetter å arbeide med å gi en bedre løsning for å identifisere listen over endringer som går inn i en kvalitetsoppdateringsnyttelast. 

Bruk KB# 745340 gjelder 10.0.28-kvalitetsoppdateringstoget og den tilknyttede appversjonen 10.0.1265.89.

1. I LCS åpner du siden **Miljødetaljer** for sandkassen. 
2. I delen **Tilgjengelige oppdateringer** velger du **Vis oppdatering** for den nyeste kvalitetsoppdateringsbuilden. 
3. Eksporter builden til en CSV- eller Microsoft Excel-fil.
4. I den eksporterte filen sorterer du informasjonen basert på tid (eldste først) og søker deretter etter KB-nummeret 745340 i kolonnen **Oppdaterings-ID**. Du skal nå se deltalisten over KB-er.
 
 > [!NOTE]
 > Eksporten til en CSV- eller Excel-fil må skje før miljøet oppdateres. Ellers kan du bruke et miljø med en lignende konfigurasjon som ikke har oppdateringen installert, og følge fremgangsmåten ovenfor.

[![Eksempel på miljø med kvalitetsoppdatering.](./media/how-to-get-kb-list-pqu.png)](./media/how-to-get-kb-list-pqu.png)

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Hva er prosessen hvis det blir funnet en kritisk feil etter en kvalitetsoppdatering?
Et kritisk problem eller en regresjon er én eller flere hendelser som vanligvis fører til at flere kunder får redusert opplevelse med én eller flere av tjenestene våre. Disse problemene kan forårsake uplanlagt nedetid, inkludert utilgjengelighet, nedgradering av ytelse og forstyrrelser i tjenestebehandlingen. Hvis kundene blir bredt påvirket av slike regresjoner, stopper vi utrullingen av en kvalitetsoppdatering til vi kan kommunisere og rette opp problemet. Den neste kvalitetsoppdateringen vil vanligvis ha den nødvendige reparasjonen for å gjenoppta utrullingen.

Hvis ett enkelt kundemiljø blir berørt, kan du kontakte med Microsofts kundestøtte for å åpne en forespørsel. Basert på begrunnelsen vil vi stoppe utrullingen av kvalitetsoppdateringen til alle andre miljøer i dette prosjektet til problemet er løst.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lcs"></a>Kan kunder fortsatt bruke hurtigreparasjonsoppdateringer manuelt fra LCS?
Ja. For å sikre kontinuerlig paritet med hvordan hurtigreparasjoner fungerer, kan oppdateringen av disse hurtigreparasjonene fortsatt brukes i kundemiljøer i LCS. Det er imidlertid viktig å legge merke til at produktmodellene som distribueres som en del av en kvalitetsoppdatering, går gjennom standard SDP før oppdateringen distribueres. Dette reduserer risikoen for regresjoner på grunn av høyere kvalitet. Vi anbefaler at du velger en kvalitetsoppdatering over manuell bruk av hurtigreparasjoner, for økt pålitelighet.

## <a name="can-customers-proactively-install-a-quality-update-build-ahead-of-the-schedule"></a>Kan kundene proaktivt installere en kvalitetsoppdateringbuild før planen?
Ja. Du kan installere en kvalitetsoppdatering proaktivt. Microsoft hopper over oppdateringen hvis miljøets gjeldende build-versjon er lik eller høyere enn den aktuelle kvalitetsoppdateringen.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Hvis et miljø har en kommende planlagt månedlig serviceoppdatering i løpet av en uke, vil det fremdeles motta kvalitetsoppdateringer?
- Kvalitetsoppdateringer brukes ikke på produksjonsmiljøer hvis det er planlagt en forestående serviceoppdatering innen en uke fra det er planlagt at kvalitetsoppdateringen skal skje.
- Hvis et sandkassemiljø har samme eller høyere build-versjon enn den forestående kvalitetsoppdateringen, blir den hoppet over.
- Hvis et produkjonsmiljø har samme eller høyere build-versjon enn den forestående kvalitetsoppdateringen, blir den hoppet over.
- Hvis en sandkasse har samme eller høyere build-versjon på grunn av en kvalitetsoppdatering eller en manuell oppdatering i produksjonen, vil produksjonen fremdeles få den planlagte versjonen av den månedlige serviceoppdateringen. Hvis du ikke vil at det planlagte produksjonsmiljøet skal oppdateres til oppdateringsversjonen for tjenesten, kan du stanse serviceoppdateringen midlertidig fra LCS. 
- Vi anbefaler at du bruker den siste kvalitetsoppdateringen for å teste endringene dine for en kommende serviceoppdatering, for bedre utnyttelse og resultater.

## <a name="if-an-environment-has-an-upcoming-scheduled-action-and-a-scheduled-quality-update-in-the-same-maintenance-window-will-it-still-receive-the-quality-update"></a>Hvis et miljø har en forestående planlagt handling og en planlagt kvalitetsoppdatering i den samme vedlikeholdsperioden, vil det fremdeles motta kvalitetsoppdateringen?
Hvis det er noe innhold med en forhåndsplanlagt handling, for eksempel tidspunktsbasert gjenoppretting (PITR), vil kvalitetsoppdateringen bli planlagt på nytt til neste tilgjengelige vedlikeholdsperiode i firedagersvinduet. For mer informasjon om planen kan du se [Hva er tidsplanen for proaktive kvalitetsoppdateringer?](#schedule). 

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Kan et miljø føres tilbake til den forrige tilstanden hvis det er problemer etter at en kvalitetsoppdatering er brukt?
Etter at en kvalitetsoppdatering er brukt, er det ikke mulig med tilbakerulling under noen omstendigheter. Det finnes bare alternativer for oppdatering fremover for å løse problemer.

## <a name="what-about-fda-regulation-and-gpx"></a>Hva med FDA-regulering og GPX?
Tidsplanen for kunder som er underlagt FDA-validering og -regulering, er fremdeles i utvikling. Du kan forvente flere oppdateringer i dette området snart. For øyeblikket er alle slike kunder unntatt kvalitetsoppdateringer. Hvis du vil sikre at en kunde faller inn under FDA-bestemmelsene, kan du gå til [Microsoft Azure GPX-tilbud](/azure/compliance/offerings/offering-gxp).

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Hvilke versjoner av serviceoppdateringer støttes for disse kvalitetsoppdateringene?
Kunder på alle støttede versjoner av serviceoppdateringer er kvalifisert for kvalitetsoppdateringer. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retailsdk"></a>Distribusjoner av økonomi- og driftsapper med Retail-komponenter krever vanligvis mer arbeid i tillegg til at du må distribuere MPOS på nytt. Hvordan vil disse kvalitetsoppdateringene påvirke RetailSDK? 
Ettersom naturen til selve hurtigreparasjonene ikke endrer seg i kvalitetsoppdateringene, forventer vi ikke noen ekstra innvirkning spesifikt relatert til Retail-komponenter på dette tidspunktet.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che"></a>Er det noen innvirkning på skybaserte miljøer? 
CHE-miljøer er utenfor området for kvalitetsoppdateringer fordi de er utenfor virkningsområdet til Microsoft

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Er det integreringsproblemer med Microsoft Dataverse? 
Det er ingen kjente integreringsproblemer for kvalitetsoppdateringer med Dataverse.


---
title: Proaktive kvalitetsoppdateringer
description: Denne artikkelen gir informasjon om proaktiv levering av kvalitetsoppdateringer.
author: rashmansur
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9d81cb15e9a127e7bea7ad9b5e0f50a1ee543f71
ms.sourcegitcommit: 78e85ad49634cd31459fdb7325cb273352bf1501
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9338144"
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
- **Synlighet** – Vi sender meldinger via e-post og Lifecycle Services (LCS) for kommende proaktive kvalitetsoppdateringer. I tillegg vil støttegrupper og hendelses kundeemner ha oversikt over hvor kvalitetsoppdateringer er distribuert proaktivt.
- **Versjonstilbakefall** – Testversjonering blir brukt til å gruppere alle endringer i en proaktiv kvalitetsoppdatering. Hvis tilbakefall er nødvendig etter en proaktiv distribusjon, kan det gjøres via testversjoneringssystemet.
- **Synkroniseringsbetegnelsen for sandkasse** – Mindre enn 20 prosent av kundene i dag har flere avmerkingsbokser, og én avmerkingsboks er distribuert der versjonen samsvarer med produksjonen, som hjelp til feilsøking. I fremtiden vil vi introdusere kundenes mulighet til å spesifisere et sandkassemiljø som ikke skal motta den proaktive kvalitetsoppdateringsdistribusjonen sammen med andre sandkasser, men som i stedet skal motta det senere, sammen med produksjonsmiljøet. Merk deg at hvis en kunde bruker en sandkasse til å teste en nyere versjon enn produksjonen, vil denne boksen motta kvalitetsoppdateringer for den nyere versjonen.
- 
## <a name="when-will-proactive-quality-updates-start"></a>Når starter proaktive kvalitetsoppdateringer?

Distribusjon av proaktive kvalitetsoppdateringer for sandkassemiljøer ventes å starte i slutten av september eller oktober 2022 for de offentlige Azure-skykundene. Prøvemiljøer vil også begynne å motta proaktiv oppdateringsdistribusjon på det tidspunktet. I september sendes det en melding til hver kunde for å informere dem om den forventede planen for miljøet. Unntak til den proaktive oppdaterte distribusjonsprosessen vil bare være tillatt for FDA-regulerte kunder. Vi holder fremdeles på med hvordan regulerte miljøer og kunde av nasjonale skyer og skyer for offentlig sektor skal administreres.

I løpet av den neste seksmåneders perioden vil vi gradvis øke prosenten av sandkassemiljøer som mottar proaktive oppdateringer, til alle utpekte miljøer er inkludert, og fremdriften for oppdatering av produksjonsmiljøer. Gjennom hele perioden overvåker vi for å sikre at distribusjonsprosessen er sømløs, og at vi når målet vårt for ikke-forstyrrende nyttelast.

Siden kunder regelmessig vil motta mindre nyttelaster, forventer vi at prosessen med nåværende behov blir enklere. Vi justerer frekvensen til oppdateringsdistribusjonen når vi viser muligheten til å kjøre prosessen uten avbrudd. Denne prosessen fungerer allerede effektivt for Dataverse-plattformen og programmene våre og leverer de forventede forbedringene i servicekvaliteten. Vi ønsker å ta det samme steget fremover for økonomi- og driftsapper.

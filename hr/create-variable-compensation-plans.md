---
title: Opprette variable kompensasjonsplaner
description: "Variabel kompensasjon utgjør en ansatts uregelmessige betaling, for eksempel tillegg eller aksjebonuser. Dette emnet beskriver komponentene må defineres før du kan bruke variabel kompensasjon og registrere ansatte i en variabel kompensasjonsplan."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: be156afa73de731e54985485b617bcbae883db3a
ms.lasthandoff: 03/31/2017


---

# <a name="create-variable-compensation-plans"></a>Opprette variable kompensasjonsplaner

Variabel kompensasjon utgjør en ansatts uregelmessige betaling, for eksempel tillegg eller aksjebonuser. Denne artikkelen beskriver komponentene som må defineres før du kan bruke variabel kompensasjon og registrere ansatte i en variabel kompensasjonsplan.

Beregningen av variable kompensasjonsbeløp for de ansatte kan baseres på flere faktorer, for eksempel den ansattes ytelse, den ansattes kompensasjonsnivå og ytelsen til avdelingen.

## <a name="variable-compensation-components"></a>Komponenter i variabel kompensasjon
### <a name="create-compensation-types"></a>Opprette kompensasjonstyper

**Typer av variabel kompensasjon **er en nødvendig komponent. Typer av variabel kompensasjon gjør at du kan beskrive typene variabel kompensasjon som organisasjonen gir. De lar deg også angi om kompensasjonen skal være i kontanter eller i ikke-monetære form, for eksempel beholdning.

### <a name="describe-vesting-rules"></a>Beskrive overdragelsesregler

Firmaer kan eventuelt også definere **overdragelsesregler**. Overdragelsesregler beskriver hvordan den variable bonusen skal fordeles over tid. En overdragelsesregelen kan for eksempel angi at ansatt vil motta 25 prosent av hans eller hennes totale belønningen hvert år i de neste fire årene. Overdragelsesregler er bare informativt.

## <a name="variable-compensation-plans"></a>Variable kompensasjonsplaner
Den **variable kompensasjonsplanen** inneholder reglene, beregningsmetodene og standardverdiene for beregningen av variabel kompensasjon for ansatte som er registrert. Når du oppretter en variabel kompensasjonsplan, må du angi den variable kompensasjonstypen. Den variable kompensasjonstypen bestemmer om systemet beregner et valutabeløp eller antall enheter som bonusen. Du må også angi beregningsmetoden:

-   **Tidspunkt** – beregningen for den variable bonusen som er basert på fast kompensasjon som ansatt har på en bestemt dato. Denne datoen er angitt for prosesshendelsen når nye kompensasjonsbeløp er behandlet.
-   **Sammensatt** – Et belønningsbeløp beregnes for hver unike lønnssats for fast kompensasjon som den ansatte hadde mellom startdatoen og sluttdatoen for syklusen i prosesshendelsen. Kursene blir deretter lagt sammen for å bestemme den endelige belønningen. Under syklusen overført for eksempel en ansatt til en annen posisjon som hadde en annen lønnssats. I dette tilfellet justeres den variable belønningen etter hvor lenge den ansatte hadde hver lønnssats.

Beløpet i den variable belønningen kan være basert på en prosent av den ansattes vanlige grunnlagsinntekt eller et angitt antall enheter.

-   Velg alternativet **Prosent av grunnlag** for å angi en standardprosent, og angi om grunnlaget skal være den ansattes faste lønnssats eller kontrollpunktet for den ansattes kompensasjonsnivå. Kompensasjonsnivået er angitt på den ansattes jobb. En av referansepunktene fra kompensasjonsstrukturen kan angis som kontrollpunktet på den faste kompensasjonsplanen. Systemet bruker kompensasjonsnivået fra den ansatte jobben og kryssreferere det med kontrollpunktet som er oppført på den faste kompensasjonsplanen til den ansatte for å finne control point beløpet til den ansattes kompensasjonsnivå. Control point beløpet vil deretter bli brukt i stedet for den ansattes faste lønnssats som grunnlag for belønningen.
-   Velg alternativet **Antall enheter** for å angi et standard antall enheter, verdien til hver enhet og valutaen for enhetsverdien hvis kompensasjonsplanen gjelder en ikke-monetær belønning (for eksempel 200 enheter av beholdning med en verdi på NOK 400), eller bare antallet enheter hvis kompensasjonsplanen gjelder en kontantbelønning. For en kontantbonus får ansatt det angitte antallet enheter av valutaen som brukes for hans eller hennes faste kompensasjonsplaner samtidig (for eksempel 500 enheter 1 USD). Kontrollen én relasjon kan brukes til å angi om det er en direkte-tilordningen mellom antall enheter og enhetsverdien. Når du oppretter en variabel kompensasjonsplan for en kontant-baserte plan ved hjelp av antall enheter, låses automatisk dette alternativet til å **Ja**, og enhetsverdien er **1,0000**.

Den **ansettelsesregelen** innstillingen lar deg angi om alle ansatte skal motta den samme økningen, uavhengig av datoen de ble leid inn (**ansettelsesregelen** = **ingen**), eller om ansatte skal motta en prosentandel av bonusen som er basert på lengden på ansettelsesforholdet under syklusen (**ansettelsesregelen** = **prosent**). 

**Utnyttelse** kan du justere bonusen til en ansatt, basert på ytelsen til den ansattes avdeling. Ytelsesmål kan angis for hver avdeling i den **avdelinger** side, under **tilknyttede skjemaer**&gt;**kompensasjon**&gt;**ytelse**. Belønningen som ansatte i denne avdelingen får, avhenger av verdien av den **prosent av det oppnådde målet** -feltet, som angir avdelingens ytelse:

-   Hvis ytelsen til avdelingen er 100 prosent, tas prosenten som er angitt i feltet **Utbetaling ved 100 %**, med i beregningen av belønningen for ansatte i denne avdelingen.
-   Hvis ytelsen til avdelingen er over 100 prosent, legger systemet sammen prosenten som er angitt i feltet **For 1 % over mål**, med prosenten som er angitt i feltet **Utbetaling ved 100 %**, til verdien som er angitt i feltet **Høyeste tillatte utbetaling**, er nådd.
-   Hvis ytelsen til avdelingen er under 100 prosent, trekker systemet prosenten som er angitt i feltet **For 1 % under mål**, fra prosenten som er angitt i feltet **Utbetaling ved 100 %**, til verdien som er angitt i feltet **Laveste tillatte utbetaling**, er nådd.

Du kan angi** toleransenivåer** for terskelprosentene, slik at det vises en advarsel hvis utnyttelsen fører til at prosentandelen havner utenfor terskelprosenten. 

Som standard leter systemet etter avdelingen som er angitt på den ansattes stilling. Men kan belønningen for noen ansatte avhenge av ytelsen til flere avdelinger. I dette tilfellet kan de ulike avdelingene, og prosentandelen av bonusen som er allokert til ytelsen til hver avdeling angi på den ansattes registrering for variabel kompensasjon. Hvis du vil ha mer informasjon, kan du se delen "variabel kompensasjon for registrering" som følger. 

Utnyttelse brukes bare hvis **Betal for ytelse** er valgt når kompensasjonsprosessen kjøres. 

Den **nivåer, overstyrer** i kategorien kan du overstyre standard prosentandelen eller antallet enheter, basert på ansatt kompensasjonsnivå av bonusen. Hvis **overstyrer Aktiver nivåer** er satt til **Ja** for ansatte som er registrert i den variable kompensasjonsplanen, tar systemet nivå fra jobb for en ansatt, og deretter ser etter den i nivåene overstyrer tabellen for å finne den prosentandelen eller antallet enheter for nivået. Hvis nivået ikke blir funnet i nivået overstyrer tabellen, standard prosentandelen eller antallet enheter fra den **Generelt** kategorien brukes. Prosent og antall enheter som kan også overstyres i den ansattes registrering i den variable kompensasjonsplanen.

## <a name="variable-compensation-enrollment"></a>Variabel kompensasjonsregistrering
### <a name="determine-who-is-eligible-for-the-plan"></a>Avgjøre hvem som har rett til planen

Når du er klar til å registrere ansatte i en variabel kompensasjonsplan, må du først å avgjøre hvem som har rett til kompensasjonen som er angitt i planen. Du kan ikke tilordne planen til ansatte med mindre du finner ut hvem som er berettiget. Du definerer berettigelse ved å åpne siden **Rettighetsregler** for å opprette en ny rettighetsregel for planen, og deretter definerer du vilkårene som en ansatt må oppfylle for å ha rett til kompensasjonsplanen. Du kan begrense rettighet etter avdeling, fagforening, kompensasjonsområde (lokasjon), jobb, jobbfunksjon, jobbtype og/eller kompensasjonsnivå. Ansatte kan registreres i en kompensasjonsplan bare hvis de oppfyller **alle** kriteriene som er angitt i rettighetsregelen. 

**Obs! ** Rettighetsregler avgjør berettigelse for både faste kompensasjonsplaner og variable kompensasjonsplaner. Rettighetsreglene bruker følgende felt i poster for jobb, stilling og ansatt til å avgjøre om en ansatt har rett til en kompensasjonsplan:

-   På **Jobb**-siden:
    -   **Jobb**-feltet
    -   Feltene **Funksjon** og **Jobbtype** i fanen **Jobbklassifisering**
    -   **Nivå**-feltet i **Kompensasjon**-fanen
-   På **Stillinger**-siden: Feltene **Avdeling** og **Kompensasjonsområde**
-   På den **ansatte** side: informasjon om fagforeninger som er knyttet til ansatt under **personlig informasjon**&gt;**fagforeninger** på den *** arbeider *** kategorien

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Aktivere registrering for den variable kompensasjonsplanen

På siden **Variable kompensasjonsplaner** setter du alternativet **Aktiver registrering** til **Ja** for å la berettigede ansatte bli registrert i planen.

### <a name="enroll-the-employee"></a>Registrere den ansatte

Du kan nå registrere ansatte i den variable kompensasjonsplanen. Hvis du vil registrere en ansatt, kan du gå til **Ansatte**-siden og velge den ansatte. Klikk på handlingsruten **kompensasjon**&gt;**registrering av variabel plan**. 

**Obs! ** **Registrering** må settes til **Ja** for den variable kompensasjonsplanen. Den **planlegger** feltet viser bare planer som ansatt er kvalifisert for, basert på rettighetsregler som er definert for disse planene. Hvis en rettighetsregel ikke er angitt for en plan, vil ingen ansatte være kvalifisert for denne planen. 

Forsikre deg om at den **ikrafttredelsesdato** -feltet er satt på riktig måte. Hvis du bruker den variable kompensasjonsplanen i **sammensatte** beregningsmåten, den effektive datoen for registreringen kan vurderes under beregningen av den ansattes belønning. 

Du kan bruke den **overstyrer** kategorien for å overstyre bestemte verdier for ansatt. For eksempel hvis **ansettelsesregelen** er satt til **prosent** på planen, og en forskjellig ansettelsesdato som skal brukes ved beregningen av den ansattes ansettelsesprosenten, kan du angi ansettelsesdatoen i den **ansettelsesregeldato** feltet. Du kan også overstyre enten den **belønningsprosent** verdi eller **antall enheter** verdien for en bestemt ansatt, avhengig av innstillingene i planen. Disse verdiene blir fortsatt tas i betraktning ved ansettelsesregelen ytelsesfaktorer og andre innstillinger i planen. 

**Organisasjonsmessige overstyringer** brukes til å basere bonusen til en ansatt på ytelsen til én eller flere avdelinger. Prosentandelen som er fordelt på tvers av avdelinger, bør utgjøre 100 prosent. Den ansattes individuelle ytelse regnes også. Disse innstillingene brukes bare hvis **Betal for ytelse** er valgt når kompensasjonsprosessen kjøres.

<a name="see-also"></a>Se også
--------

[Kompensasjonsplaner](compensation-plans.md)



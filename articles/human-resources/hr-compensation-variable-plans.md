---
title: Opprette variable kompensasjonsplaner
description: Dette emnet beskriver komponentene som må defineres før du kan bruke variabel kompensasjon og registrere ansatte i en variabel kompensasjonsplan.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan, HcmCompensationWorkspace
audience: Application User
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 589990c48d115266b57589f905de20572e76a040
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688664"
---
# <a name="create-variable-compensation-plans"></a>Opprette variable kompensasjonsplaner


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Variabel kompensasjon utgjør en ansatts uregelmessige betaling, for eksempel tillegg eller aksjebonuser. Dette emnet forklarer hvoran du setter opp komponentene som kreves for variabel kompensasjon og registrering av en ansatt i en variabel kompensasjonsplan.

Beregningen av variable kompensasjonsbeløp for de ansatte kan baseres på flere faktorer, for eksempel den ansattes ytelse, den ansattes kompensasjonsnivå og ytelsen til avdelingen.

## <a name="variable-compensation-components"></a>Komponenter i variabel kompensasjon
### <a name="create-compensation-types"></a>Opprette kompensasjonstyper

**Typer av variabel kompensasjon** er en nødvendig komponent. **Typer av variabel kompensasjon** gjør at du kan beskrive typene variabel kompensasjon som organisasjonen gir. De lar deg også angi om kompensasjonen skal være i kontanter eller i ikke-monetære form, for eksempel beholdning.

### <a name="describe-vesting-rules"></a>Beskrive overdragelsesregler

Firmaer kan eventuelt også definere **Overdragelsesregler**. **Overdragelsesregler** beskriver hvordan den variable bonusen skal fordeles over tid. En overdragelsesregel kan for eksempel angi at ansatt vil motta 25 prosent av den totale belønning hvert år i de neste fire årene. Overdragelsesregler er kun til informasjon.

## <a name="variable-compensation-plans"></a>Variable kompensasjonsplaner
Den **variable kompensasjonsplanen** inneholder reglene, beregningsmetodene og standardverdiene for beregningen av variabel kompensasjon for ansatte som er registrert. Når du oppretter en variabel kompensasjonsplan, må du angi den variable kompensasjonstypen. Den variable kompensasjonstypen bestemmer om systemet beregner et valutabeløp eller antall enheter som bonusen. Du må også angi beregningsmetoden:

-   **Tidspunkt** – beregningen av den variable bonusen er basert på den faste kompensasjonen som ansatt har på en bestemt dato. Denne datoen er angitt for prosesshendelsen når nye kompensasjonsbeløp er behandlet.
-   **Sammensatt** – Et belønningsbeløp beregnes for hver unike lønnssats for fast kompensasjon som den ansatte hadde mellom startdatoen og sluttdatoen for syklusen i prosesshendelsen. Satsene blir deretter lagt sammen for å bestemme den endelige belønningen. Under syklusen blir for eksempel en ansatt overført til en annen stilling som hadde en annen lønnssats. I dette tilfellet justeres den variable belønningen etter hvor lenge den ansatte hadde hver lønnssats.

Beløpet i den variable belønningen kan være basert på en prosent av den ansattes vanlige grunnlagsinntekt eller et angitt antall enheter.

-   Velg alternativet **Prosent av grunnlag** for å angi en standardprosent, og angi om grunnlaget skal være den ansattes faste lønnssats eller kontrollpunktet for den ansattes kompensasjonsnivå. Kompensasjonsnivået er angitt på den ansattes jobb. Ett av referansepunktene fra kompensasjonsstrukturen kan angis som kontrollpunktet på den faste kompensasjonsplanen. Kompensasjonsnivået fra den ansattes jobb vil bli brukt og kryssrefereres til det med kontrollpunktet som er oppført i den ansattes faste kompensasjonsplan, for å finne kontrollpunktbeløpet for den ansattes kompensasjonsnivå. Kontrollpunktbeløpet brukes deretter som grunnlaget for belønningen i stedet for den ansattes faste lønnssats.
-   Velg alternativet **Antall enheter** for å angi et standard antall enheter, verdien til hver enhet og valutaen for enhetsverdien hvis kompensasjonsplanen gjelder en ikke-monetær belønning (for eksempel 200 enheter av beholdning med en verdi på NOK 400), eller bare antallet enheter hvis kompensasjonsplanen gjelder en kontantbelønning. Når det gjelder en kontantbelønning, får den ansatte det angitte antallet enheter av valutaen som brukes for den faste kompensasjonsplan (for eksempel 500 enheter på USD 1). Kontrollen for én-til-én-relasjon kan brukes til å angi om det er en direkte én-til-én-tilordning mellom antallet enheter og enhetsverdien. Når du oppretter en variabel kompensasjonsplan for en kontantbasert plan ved hjelp av antallet enheter, låses dette alternativet automatisk til **Ja**, og enhetsverdien er **10,0000**.

**Ansettelsesregel** angir om om alle de ansatte skal få den samme økningen, uavhengig av ansettelsesdatoen (**Ansettelsesregel** = **Ingen**), eller om ansatte skal få en prosent av belønningen som er basert på hvor lenge de har vært ansatt, i syklusen (**Ansettelsesregel** = **Prosent**). 

**Utnyttelse** justerer bonusen til en ansatt basert på ytelsen til den ansattes avdeling. Ytelsesmål kan angis for hver avdeling på siden **Avdelinger**, under **Tilknyttede skjemaer** &gt; **Kompensasjon** &gt; **Ytelse**. Belønningen som ansatte i denne avdelingen får, avhenger av verdien i feltet **Prosent av mål oppnådd**, som angir avdelingens ytelse:

-   Hvis ytelsen til avdelingen er 100 prosent, tas prosenten som er angitt i feltet **Utbetaling ved 100 %**, med i beregningen av belønningen for ansatte i denne avdelingen.
-   Hvis ytelsen til avdelingen er over 100 prosent, legger systemet sammen prosenten som er angitt i feltet **For 1 % over mål**, med prosenten som er angitt i feltet **Utbetaling ved 100 %**, til verdien som er angitt i feltet **Høyeste tillatte utbetaling**, er nådd.
-   Hvis ytelsen til avdelingen er under 100 prosent, trekker systemet prosenten som er angitt i feltet **For 1 % under mål**, fra prosenten som er angitt i feltet **Utbetaling ved 100 %**, til verdien som er angitt i feltet **Laveste tillatte utbetaling**, er nådd.

**Toleransenivåer** kan angis for terskelprosentene, slik at det vises en advarsel hvis utnyttelsen fører til at prosentandelen havner utenfor terskelprosenten. 

Som standard brukes avdelingen som er angitt på den ansattes stilling, for ansattbonuser. Belønningen for noen ansatte kan imidlertid avhenge av ytelsen til flere avdelinger. I dette tilfellet kan de ulike avdelingene og prosentandelen av belønningen som er tilordnet til ytelsen til hver avdeling, angis i den ansattes variable kompensasjonsregistrering. Hvis du vil ha mer informasjon, kan du se delen «Variabel kompensasjonsregistrering» nedenfor. 

Utnyttelse brukes bare hvis **Betal for ytelse** er valgt når kompensasjonsprosessen kjøres. 

Fanen **Nivåoverstyringer** lar deg overstyre belønningens standardprosent eller standard antall enheter basert på kompensasjonsnivået til den ansatte. Hvis **Aktiver overstyringer for nivåer** er satt til **Ja** for ansatte som er registrert i den variable kompensasjonsplanen, vil nivået fra en ansatts jobb sammenlignes med nivåoverstyringstabellen for å finne prosenten eller antallet enheter for dette nivået. Hvis nivået ikke blir funnet i tabellen for nivåoverstyringer, brukes standard prosent eller antall enheter fra **Generelt**-fanen. Prosent og antall enheter kan også overstyres i den ansattes registrering i den variable kompensasjonsplanen.

## <a name="variable-compensation-enrollment"></a>Variabel kompensasjonsregistrering
### <a name="determine-who-is-eligible-for-the-plan"></a>Avgjøre hvem som har rett til planen

Når du er klar til å registrere ansatte i en variabel kompensasjonsplan, må du først å avgjøre hvem som har rett til kompensasjonen som er angitt i planen. Du kan ikke tilordne planen til ansatte med mindre du finner ut hvem som er berettiget. Du definerer berettigelse ved å åpne siden **Rettighetsregler** for å opprette en ny rettighetsregel for planen, og deretter definerer du vilkårene som en ansatt må oppfylle for å ha rett til kompensasjonsplanen. Du kan begrense rettighet etter avdeling, fagforening, kompensasjonsområde (lokasjon), jobb, jobbfunksjon, jobbtype og/eller kompensasjonsnivå. Ansatte kan registreres i en kompensasjonsplan bare hvis de oppfyller **alle** kriteriene som er angitt i rettighetsregelen. 

**Obs!** Rettighetsregler avgjør berettigelse for både faste kompensasjonsplaner og variable kompensasjonsplaner. Rettighetsreglene bruker følgende felt i poster for jobb, stilling og ansatt til å avgjøre om en ansatt har rett til en kompensasjonsplan:

- På **Jobb**-siden:
  -   **Jobb**-feltet
  -   Feltene **Funksjon** og **Jobbtype** i fanen **Jobbklassifisering**
  -   **Nivå**-feltet i **Kompensasjon**-fanen
- På **Stillinger**-siden: Feltene **Avdeling** og **Kompensasjonsområde**
- På <strong>Ansatte</strong>-siden: Informasjonen om fagforeninger som er knyttet til den ansatte under <strong>Personlige opplysninger</strong> &gt; <strong>Fagforeninger</strong> i *<strong><em>Arbeider</em></strong>*-fanen

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Aktivere registrering for den variable kompensasjonsplanen

På siden **Variable kompensasjonsplaner** setter du alternativet **Aktiver registrering** til **Ja** for å la berettigede ansatte bli registrert i planen.

### <a name="enroll-the-employee"></a>Registrere den ansatte

Du kan nå registrere ansatte i den variable kompensasjonsplanen. Hvis du vil registrere en ansatt, kan du gå til **Ansatte**-siden og velge den ansatte. Klikk deretter **Kompensasjon** &gt; **Registrering av variabel plan** i handlingsruten. 

**Obs!** **Registrering** må settes til **Ja** for den variable kompensasjonsplanen. **Plan**-feltet viser bare planene som den ansatte har rett til i henhold til rettighetsreglene som defineres for disse planene. Hvis ingen rettighetsregel er definert for en plan, har ingen ansatte rett til denne planen. 

Kontroller at feltet **Ikrafttredelsesdato** er riktig angitt. Hvis den variable kompensasjonsplanen bruker beregningsmetoden **Sammensatt**, blir kanskje ikrafttredelsesdatoen for registreringen vurdert i beregningen av den ansattes belønning. 

Du kan bruke **Overstyrer**-fanen til å overstyre bestemte verdier for den ansatte. Hvis **Ansettelsesregel** er satt til **Prosent** i planen, og en annen ansettelsesdato skal brukes i beregningen av den ansattes ansettelsesprosent, kan du angi ansettelsesdatoen i feltet **Ansettelsesregeldato**. Du kan også overstyre **Belønningsprosent**-verdien eller **Antall enheter**-verdien for en bestemt ansatt, avhengig av innstillingene for planen. Disse verdiene er fortsatt gjeldende i ansettelsesregelen, ytelsesfaktorer og andre innstillinger for planen. 

**Organisasjonsmessige overstyringer** brukes til å basere belønningen til en ansatt på ytelsen til én eller flere avdelinger. Prosenten som er fordelt på tvers av avdelinger skal til sammen utgjøre 100 prosent. Det tas også hensyn til den ansattes individuelle ytelse. Disse innstillingene brukes bare hvis **Betal for ytelse** er valgt når kompensasjonsprosessen kjøres.





[!INCLUDE[footer-include](../includes/footer-banner.md)]

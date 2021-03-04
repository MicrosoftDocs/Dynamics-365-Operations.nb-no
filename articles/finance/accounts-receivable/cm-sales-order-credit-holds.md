---
title: Kredittgrenser for salgsordrer
description: Dette emnet beskriver oppsettet av regler som brukes til å angi kredittsperre for en salgsordre.
author: mikefalkner
manager: AnnBe
ms.date: 01/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 102ea4285407a4f4985cc8dd46ebc1ad21fc6f67
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446268"
---
# <a name="credit-holds-for-sales-orders"></a>Kredittgrenser for salgsordrer
[!include [banner](../includes/banner.md)]

Dette emnet beskriver oppsettet av regler som brukes til å angi kredittsperre for en salgsordre. Blokkeringsreglene for kredittbehandling kan gjelde for en individuell kunde eller en gruppe kunder. Blokkeringsregler definerer svar på følgende omstendigheter:

1. Antall dager forfalt
2. Kontostatus
3. Betalingsbetingelser
4. Kredittgrense utløpt
5. Forfalt beløp
6. Salgsordrebeløp
7. Del av tilgjengelig kreditt brukt

I tillegg finnes det to parametere som kontrollerer andre scenarier som vil blokkere en salgsordre

1. Endring i betalingsvilkår
2. Endring i utligningsrabatter

## <a name="set-up-blocking-rules-and-exclusion-rules"></a>Definere blokkeringsregler og utelatelsesregler

Når en kunde starter en salgstransaksjon, blir informasjonen i salgsordren vurdert mot et sett med blokkeringsregler som hjelper med å bestemme om kreditten til kunden skal forlenges og salget skal gå videre. Du kan også definere utelatelser som overstyrer blokkeringsreglene og tillater at en salgsordre behandles. Du kan definere blokkeringsregler og utelatelsesregler på siden **Kredittbehandling > Oppsett > Oppsett for kredittbehandling > Blokkeringsregler**.

### <a name="days-overdue"></a>Dager etter forfall

Åpne fanen **Dager etter forfall** hvis blokkeringsregelen gjelder for kunde med én eller flere fakturaer som er forfalt for et bestemt antall dager.
1. Velg området for kunde som denne regelen **Gjelder for**.
   - Velg **Tabell** hvis regelen gjelder for en bestemt kunde.
   - Velg **Gruppe** hvis regelen brukes på kundegruppenivå. 
   - Velg **Alle** hvis regelen gjelder for alle kunder.
2. Når du har angitt området, må du angi **Konto/gruppe** som skal brukes i området.
   - For **Tabell**-området vil oppslaget vise en liste over kunder som skal velges. 
   - Velg en **Gruppe** hvis regelen gjelder for en kundekredittgruppe.
   - Velg **Alle** hvis regelen gjelder for alle kunder. 
3. Velg **Risikogruppe** for å bruke kriterier for å bruke en kredittbehandlingssperre for kunder som er gruppert etter et felles sett med faktorer, for eksempel deres Dun and Bradstreet-klassifisering, antall år de har vært i virksomhet, hvor lenge de har vært din kunde, og så videre.  
4. Velg regeltypen du konfigurerer. Alternativet **Blokkering** vil opprette en regel som blokkerer en ordre. Alternativet **Utelatelse** vil opprette en regel som utelater en annen regel fra å blokkere en ordre. 
5. Velg en **Verditype**. Standardoppføringen er et fast antall dager. Hvis du oppretter en utelatelse, kan du angi et fast antall dager eller et beløp i stedet. 
6. Angi antall dager **Forfalt** som skal være tillatt for den valgte blokkeringsregelen, før en ordre settes på kredittbehandlingssperre for gjennomgang. Antall dager forfalt representerer et ekstra antall respittdager som legges til antall dager utover forfallsdatoen for betaling som fakturaen kan ha før den regnes som forfalt. Hvis du har angitt **Verditype** som et beløp for en utelatelse, angir du et beløp og en valuta for dette beløpet.

### <a name="accounts-status"></a>Kontostatus

Åpne kategorien **Kontostatus** hvis blokkeringsregelen gjelder for en kunde med den valgte kontostatusen.
1. Velg regeltypen du konfigurerer.  **Blokkering** vil opprette en regel som blokkerer en ordre. **Utelatelse** oppretter en regel som utelater en regel fra å blokkere en ordre. 
2. Velg **Kontostatus** som vil føre til at regelen plasserer en salgsordre på vent eller utelater den.

### <a name="terms-of-payment"></a>Betalingsbetingelser

Velg **Betalingsbetingelser** hvis blokkeringsregelen gjelder for den valgte betalingsbetingelsen.
1. Velg regeltypen du konfigurerer.  **Blokkering** vil opprette en regel som blokkerer en ordre. **Utelatelse** oppretter en regel som utelater en regel fra å blokkere en ordre. 
2. Velg **Betalingsbetingelser** som vil føre til at regelen plasserer en salgsordre på vent eller utelater den.

### <a name="credit-limit-expired"></a>Kredittgrense utløpt

Åpne kategorien **Kredittgrense utløpt** hvis blokkeringsregelen gjelder for kunder med kredittgrenser som er utløpt.
1. Velg området for kunde som denne regelen **Gjelder for**.
   - Velg **Tabell** hvis regelen gjelder for en bestemt kunde.
   - Velg **Gruppe** hvis regelen brukes på kundegruppenivå. 
   - Velg **Alle** hvis regelen gjelder for alle kunder.
2. Når du har angitt området, må du angi **Konto/gruppe** som brukes i området.
   - For **Tabell**-området vil oppslaget vise en liste over kunder å velge fra. 
   - Velg en **Gruppe** hvis regelen gjelder for en kundekredittbehandlingsgruppe.
   - Velg **Alle** hvis regelen gjelder for alle kunder. 
3. Velg en **Risikogruppe** for ytterligere å begrense listen over kunder som skal plasseres på vent for kredittbehandling. 
4. Velg regeltypen du konfigurerer. 
   - Velg **Blokkering** for å opprette en regel som blokkerer en ordre. 
   - Velg **Utelatelse** for å opprette en regel som utelater en annen regel fra å blokkere en ordre. 
5. Angi **Dager kredittgrense utløpt** for den valgte blokkeringsregelen før en ordre settes på vent for kredittbehandling. Antallet dager forfalt representerer ekstra respittdager som legges til antallet dager som kredittgrensen har vært utløpt.

### <a name="overdue-amount"></a>Forfalt beløp

Åpne kategorien **Forfalt beløp** hvis blokkeringsregelen gjelder for kunder med forfalte beløp.
1. Velg området for kunde som denne regelen **Gjelder for**.
   - Velg **Tabell** hvis regelen gjelder for en bestemt kunde.
   - Velg **Gruppe** hvis regelen brukes på kundegruppenivå. 
   - Velg **Alle** hvis regelen gjelder for alle kunder.
2. Når du har angitt området, må du angi **Konto/gruppe** som brukes i området.
   - For **Tabell**-området vil oppslaget vise et kundeoppslag. 
   - Velg en **Gruppe** hvis regelen gjelder for en kundekredittbehandlingsgruppe.
   - Velg **Alle** hvis regelen gjelder for alle kunder. 
3. Velg en **Risikogruppe** hvis du vil begrense ytterligere listen over kunder som settes på vent for kredittbehandling. 
4. Velg regeltypen du konfigurerer. 
   - Velg **Blokkering** for å opprette en regel som blokkerer en ordre. 
   - Velg **Utelatelse** for å opprette en regel som utelater en annen regel fra å blokkere en ordre. 
5. Angi **Forfalt beløp** for den valgte blokkeringsregelen før en ordre settes på kredittbehandlingssperre for gjennomgang. 
6. Velg **Verditype** som definerer verditypen som skal brukes til også å teste hvor mye av kredittgrensen som er brukt. Blokkeringsregler krever en prosent, men en utelatelse kan ha et fast beløp eller en fast prosentsats. Terskelen er knyttet til kredittgrensen.
7. Angi **Terskel for kredittgrense**-verdien for den valgte regelen før en kunde settes på kredittbehandlingssperre. Dette kan være et beløp eller en prosent basert på verditypevalget i verditype.
8. Regelen kontrollerer om **Forfalt beløp** er overskredet og om **Terskel for kredittgrense** er overskredet. 

### <a name="sales-order"></a>Salgsordre 

Velg **Salgsordre** hvis blokkeringsregelen gjelder for verdien for salgsordren.
1. Velg området for kunde som denne regelen **Gjelder for**.
   - Velg **Tabell** hvis regelen gjelder for en bestemt kunde.
   - Velg **Gruppe** hvis regelen brukes på kundegruppenivå. 
   - Velg **Alle** hvis regelen gjelder for alle kunder.
2. Når du har angitt området, må du angi **Konto/gruppe** som brukes i området.
   - For **Tabell**-området vil oppslaget vise et kundeoppslag. 
   - Velg en **Gruppe** hvis regelen gjelder for en kundekredittbehandlingsgruppe.
   - Velg **Alle** hvis regelen gjelder for alle kunder. 
3. Velg en **Risikogruppe** hvis du vil begrense ytterligere listen over kunder som settes på vent for kredittbehandling. 
4. Velg regeltypen du konfigurerer.  
   - Velg **Blokkering** for å opprette en regel som blokkerer en ordre. 
   - Velg **Utelatelse** for å opprette en regel som utelater en annen regel fra å blokkere en ordre. 
5. Angi **Salgsordrebeløp** for den valgte blokkeringsregelen før en ordre settes på kredittbehandlingssperre. 

Salgsordreregelen inneholder en tilleggsinnstilling som overstyrer alle andre regler. Hvis du vil opprette en utelatelse som vil frigi salgsordren uten å ta hensyn til andre regler, merker du av for **Frigi salgsordre** på utelatelseslinjen.

### <a name="credit-limit-used"></a>Kredittgrense brukt

Velg **Kredittgrense brukt** hvis blokkeringsregelen gjelder for kundekredittgrensebeløpet som er utnyttet.
1. Velg området for kunde som denne regelen **Gjelder for**.
   - Velg **Tabell** hvis regelen gjelder for en bestemt kunde.
   - Velg **Gruppe** hvis regelen brukes på kundegruppenivå. 
   - Velg **Alle** hvis regelen gjelder for alle kunder.
2. Når du har angitt området, må du angi **Konto/gruppe** som brukes i området.
   - For **Tabell**-området vil oppslaget vise et kundeoppslag. 
   - Velg en **Gruppe** hvis regelen gjelder for en kundekredittbehandlingsgruppe.
   - Velg **Alle** hvis regelen gjelder for alle kunder. 
3. Velg en **Risikogruppe** hvis du vil begrense ytterligere listen over kunder som settes på vent for kredittbehandling. 
4. Velg regeltypen du konfigurerer.
   - Velg **Blokkering** for å opprette en regel som blokkerer en ordre. 
   - Velg **Utelatelse** for å opprette en regel som utelater en annen regel fra å blokkere en ordre. 
5. Velg **Gjenværende terskel** som definerer prosenten for kredittgrensen som vil blokkere salgsordren. Hvis verdien for en ordre øker beløpet for kredittgrensen som brukes over prosenten, sperres ordren. 

## <a name="put-a-sales-order-on-hold-based-on-other-criteria"></a>Sette en salgsordre på vent basert på andre kriterier
  
### <a name="rank-payment-terms"></a>Ranger betalingsbetingelser  

Du kan tvinge kredittkontrollreglene til å utføres når betalingsbetingelser endres. Du må rangere betalingsbetingelsene og tilordne dem en rangeringsverdi. Hvis du endrer betalingsbetingelsene på ordren til betalingsbetingelser som er rangert høyere enn de gamle betalingsbetingelsene, sendes ordren til kredittbehandling og krever godkjenning.

Du kan definere rangeringer av betalingsbetingelser på siden **Kredittbehandling > Oppsett > Kredittbehandlingsoppsett > Ranger betalingsbetingelser**.

1. Velg betalingsbetingelser som **Betalingsbetingelser**-feltet skal rangere. Når du velger en betingelse, vises beskrivelsen i **Beskrivelse**-feltet.
2. Velg betingelsens rangering i **Rangering**-feltet. Verdiene er alle relative i forhold til hverandre, slik at du kan bruke 1,2,3 eller 10,20,30. Du kan også bruke den samme verdien for de fleste betalingsbetingelsene, slik at bare én eller to betalingsbetingelser vil utløse kredittkontrollen.

### <a name="rank-settlement-discounts"></a>Ranger utligningsrabatter   

Du kan tvinge kredittkontrollreglene til å utføres når utligningsrabatter endres. Du må rangere utligningsrabattene og tilordne dem en rangeringsverdi. Hvis du endrer utligningsrabattene på ordren til utligningsrabatter som er rangert høyere enn de gamle utligningsrabattene, sendes ordren til kredittbehandling og krever godkjenning.

Du kan definere rangeringer av betalingsbetingelser på siden **Kredittbehandling > Oppsett > Kredittbehandlingsoppsett > Ranger utligningsrabatter**.

1. Velg **kontantrabatten** du vil rangere. **Beskrivelsen** av utligningsrabatten vises.
2. Velg **Rangering**-verdien. Verdiene er alle relative i forhold til hverandre, slik at du kan bruke 1,2,3 eller 10,20,30. Du kan også bruke den samme verdien for de fleste utligningsrabattene, slik at bare én eller to utligningsrabatter vil utløse kredittkontrollen.

## <a name="sequence-the-application-of-rules"></a>Ordne bruken av regler

Reglene kjøres i en bestemt rekkefølge som du endrer etter organisasjonens behov. 

- Én forekomst av reglene for utelatelse av salgsordrer lar deg overstyre alle regler som kan blokkere en salgsordre. Opprett en regel for utelatelse av salgsordre, og merk alternativet **Frigi salgsordre**. Ordren vil ikke bli satt på vent hvis denne regelen for utelukkelse er sann, og ingen andre regler vil bli kontrollert.
- Blokkeringsregler kan sette ordren på vent.
- Utelatelsesregler kjøres etter blokkeringsregler. Utelatelsesregler vil bare ha innvirkning på regelen som de er definert for. 
- Blokkerings- og utelatelsesregler kjøres i tabell, deretter gruppe og deretter alle ordrer. På grunn av denne behandlingsrekkefølgen er det mulig å ha en blokkeringsregel på alle nivåene som ikke skal kjøres fordi det kjøres en utelatelsesregel på tabell- eller gruppenivå.
- Utelatelser overstyrer ikke blokkeringsregelen hvis de er på samme nivå. En utelatelsesregel på gruppenivå vil for eksempel ikke overstyre blokkeringsregelen på gruppenivå. Du trenger ikke definere utelatelser på alle nivåer, unntatt som beskrevet ovenfor, med den ene forekomsten av utelatelsesregelen for salgsordrer. 

Virkemåten for regelen **Kredittgrense brukt** endres basert på innstillingene for parameteren **Kontroller kredittgrense for salgsordre** som finnes i parameterskjemaet for kreditt og innkreving.
- Hvis parameteren settes til Nei, kjøres ikke regelen for Kredittgrense brukt.
- Hvis parameteren settes til Ja og **Melding ved kredittoverskridelse** settes til advarsel, får du en advarsel når kredittgrensen overskrides. Reglene for **Kredittgrense brukt** kjøres for å se om du har regler du vil kjøre. Men i dette scenariet vil du vanligvis ikke legge til noen regler.
- Hvis parameteren settes til Ja og **Melding ved kredittoverskridelse** settes til feil, blir kredittgrensen kontrollert, og ordren vil bli satt på vent hvis kredittgrensen er overskredet. Reglene for **Kredittgrense brukt** kjøres også for å se om det er flere regler som skal kjøres. En feilmelding vises ikke, men blokkeringsårsaken **Kredittgrense overskredet** vises. 

## <a name="settings-that-will-change-the-way-an-order-is-placed-on-hold"></a>Innstillinger som endrer måten en ordre plasseres på vent

Ordrer kan utelates fra kredittbehandling selv om det finnes regler. 

- Hvis du endrer innstillingene **Utelat kunde fra kredittbehandling** i **Alle kunder > velg en kunde > Kreditt og innkreving-hurtigfanen** til **Ja**, så blir ingen ordrer for denne kunden behandlet.
- Hvis du endrer verdien **Utelat fra kredittbehandling** i **salgsordrehodet** i **hurtigfanen Kredittbehandling** til **Ja**, behandles ikke kredittbehandlingsreglene. Denne innstillingen kan bare utføres av kredittmedarbeideren eller kredittlederen.

## <a name="processing-orders-on-hold-using-the-credit-management-hold-list"></a>Behandle ordrer på vent ved hjelp av listen for kredittbehandling på vent

Listen over kredittbehandling på vent lar kredittledere vise alle salgsordrer som er satt på vent, og lar dem fjerne sperrene når kredittproblemene er begrenset. Siden **Liste over kredittbehandling på vent** viser alle salgsordrer som har blitt satt på vent. Du kan vise på vent-listen på siden **Alle kredittsperrer** (**Kredittbehandling > Liste over kredittbehandling på vent > Alle kredittsperrer**).
Salgsordrer fra alle juridiske enheter sendes til samme liste over kredittbehandling på vent, og gir en sentral visning av alle transaksjoner som krever oppmerksomhet. Brukere vil bare se informasjon for juridiske enheter de har tilgang til.

En salgsordre kan plasseres i sperrelisten av følgende årsaker:
1. Kunden har en faktura som har vært forfalt i et bestemt antall dager. 
2. Ordren har en bestemt kontostatus.
3. Ordren har bestemte betalingsbetingelser.
4. Kunden har en utløpt kredittgrense.
5. Kunden har et forfalt beløp og har brukt en bestemt prosent av kredittgrensen
6. Salgsordren overskrider et bestemt beløp.
7. Kunden har overskredet en bestemt prosent av kredittgrensen.
8. Betalingsbetingelsene er forskjellige fra standard betalingsbetingelser for kunden.
9. Utligningsrabattene er forskjellige fra standard utligningsrabatt for kunden.

Blokkeringsårsaken vises for hver salgsordre i sperrelisten. Hvis det er mer enn én årsak til sperringen, vil årsaken vises som **Flere**. Du kan bruke **Blokkeringsårsaker**-menyen i handlingsruten til å vise alle årsakene til at salgsordren ble satt på vent. Du kan også vise **blokkeringsårsakene** i en faktaboks.

### <a name="releasing-orders-from-the-hold-list-for-processing"></a>Frigi ordrer fra sperrelisten for behandling

Når du har undersøkt årsakene til sperringen, og du har begrenset dem, kan du frigi salgsordrene for videre behandling.

1) Velg en linje i sperrelisten. Du kan frigi flere ordrer ved å merke mer enn én linje.
2) Velg en **Frigivelsesårsak** for ordren som er valgt for frigivelse.  
3) Angi **gjennomgangsdatoen** for hver ordre som er valgt for frigivelse.  
4) Velg **Frigi**-menyen i handlingsruten for å frigi en ordre. Denne menyen vil bare være tilgjengelig når det er valgt transaksjoner. Brukeren vises med to alternativer:
   - Velg **Med postering** for å fjerne sperren og postere dokumentet ved å bruke den samme posteringsprosessen som ble brukt da den ble satt på vent. Hvis for eksempel salgsordrebekreftelsen ble satt på vent, ville salgsordrebekreftelsen blitt fullført etter frigivelsen. Salgsordreposteringsskjemaet vil vises og tillate brukeren å postere bekreftelsen.
   - Velg **Uten postering** for å fjerne sperren uten å utføre videre behandling. Salgsordren kan posteres manuelt.

### <a name="rejecting-orders-in-the-hold-list"></a>Avvise ordrer i på vent-listen
Du kan bruke **Avvis**-menyen i handlingsruten for å avvise en salgsordre
1. Velg en linje i sperrelisten. Du kan frigi flere ordrer ved å merke mer enn én linje.
2. Ordren blir fjernet fra sperrelisten, og salgsordrehodet oppdateres for å vise at ordren ble avvist.

### <a name="automatically-releasing-credit-management-holds"></a>Automatisk frigi kredittbehandlingssperrer
Salgsordrer plasseres i listen over sperrer basert på blokkeringsreglene. Noen årsaker til sperrer kan imidlertid endres over tid hvis salgsordren blir værende i sperrelisten over en tidsperiode. En kunde kan for eksempel betale fakturaen, som frigjør kredittgrensen. 

Du kan bruke menyen **Evaluer for frigivelse** til å se gjennom salgsordrene i sperrelisten og frigi dem automatisk hvis årsaken til sperren har blitt begrenset.
1.  Velg menyen **Evaluer for frigivelse**
2.  Velg **Behandle blokkeringsregler** for å gå gjennom alle salgsordrene. Velg **Behandle blokkeringsregler for valgte linjer** for å se gjennom bare de linjene du har valgt.
3. En glidebryter vises slik at du kan velge en enkelt kunde. La kunderullegardinlisten stå tom for alle kunder. 
4. Når du klikker på OK, kjøres prosessen i bakgrunnen, og du kan fortsette å arbeide på andre oppgaver. Hvis du velger satsvis behandling før du klikker på OK, kjøres prosessen satsvis når du klikker på OK. Det kan ta litt tid å behandle ordrene på vent i listen, så bruk Oppdater til å oppdatere statusen for ordrene. 
5.  Hvis en blokkeringsårsak ikke lenger gjelder for en ordre, vil blokkeringsårsaken ikke være gyldig lenger, og du vil ikke lenger se en hake ved siden av årsaken når du viser blokkeringsårsakene.
6.  Hvis alle blokkeringsårsaker fjernes, legges det til en ny årsak, **Klar til frigivelse**, i listen over blokkeringsårsaker. Salgsordren kan frigis automatisk.
7.  Hvis parameteren **Automatisk frigivelse** i **Kreditt og innkreving > Oppsett > Parametere for kreditt og innkreving > Kreditt > Automatisk frigivelse**-kategorien settes til **Med postering**, blir du bedt om å postere ved hjelp av posteringsskjemaet for dokumentet som ble blokkert.
8.  Hvis parameteren **Automatisk frigivelse** i **Kreditt og innkreving > Oppsett > Parametere for kreditt og innkreving > Kreditt > Automatisk frigivelse**-kategorien settes til **Uten postering**, må du postere ordren manuelt.

### <a name="credit-management-approval-workflow"></a>Arbeidsflyt for godkjenning av kredittbehandling

Du kan også opprette **arbeidsflyter for kredittbehandling** for å kontrollere frigivelsen av kredittsperrer. Når du har definert arbeidsflyt ved hjelp av siden **Kredittbehandling > Oppsett > Arbeidsflyter for kredittbehandling**, sendes ordrene som er merket for frigivelse eller avslag, til arbeidsflyten der de må godkjennes først før de blir frigitt eller avvist. 

Hvis du inkluderer oppgavene for frigivelse med postering eller frigivelse uten postering i arbeidsflyten, vil arbeidsflytgodkjenningen også frigi salgsordren. Hvis det imidlertid oppstår en feil i frigivelsesprosessen på grunn av manglende oppsettsinformasjon eller andre årsaker, må du tilbakekalle salgsordren fra arbeidsflyten, løse problemet som forårsaket feilen, og deretter sende ordren til arbeidsflyten på nytt.

Hvis du ikke inkluderer oppgavene for frigivelse med postering eller frigivelse uten postering i arbeidsflyten, vil arbeidsflytgodkjenningsprosessen ganske enkelt la deg frigi salgsordren manuelt når godkjenningen er fullført.

### <a name="forced-credit-hold"></a>Tvungen kredittsperre  
  
Noen ganger kan det hende at salgsordrer må blokkeres selv om ordren ikke oppfyller kriteriene i blokkeringsreglene. En kredittleder kan for eksempel bli varslet om et ikke-kreditt-relatert problem med kunden, og bestemme seg for å legge ordrer på vent manuelt umiddelbart til problemet er ordnet. Du kan manuelt tvinge en salgsordre til å være på vent hvis denne situasjonen oppstår.

1. Åpne salgsordren du vil sette på vent.  
2. Velg **Tving kredittsperre** i kategorien **Kredittbehandling** i handlingsruten **Kredittbehandling**.
3. Velg en **tvungen sperreårsak**.
4. Klikk på **OK**. Salgsordren returneres til listen over kredittbehandling på vent.

Du kan også tvinge flere ordrer til å være sperret, på siden **Kredittbehandling > Periodiske oppgaver > Tving kredittsperre**. Du kan for eksempel sette alle salgsordrer på vent for en bestemt kunde.
1. Velg **tvungen sperreårsak**. 
2. Klikk på **Poster som skal inkluderes** for å velge salgsordrene du vil sette på vent. 
3. Klikk på **OK** for å behandle de valgte salgsordrene.

Salgsordrer som er tvunget på vent, kan ikke behandles med arbeidsflyt.

#### <a name="releasing-orders-that-were-added-to-the-credit-management-hold-list-with-a-forced-credit-hold"></a>Frigi ordrer som ble lagt til i listen over kredittbehandling på vent med en tvungen kredittsperre
Salgsordrer som har en tvungen sperreårsak, kan ikke frigis automatisk. Hvis salgsordren ble tvunget på vent, og du har brukt en prosess som automatisk frigir salgsordrer, vises salgsordren som **Klar til frigivelse** og forblir i sperrelisten. Du må bruke **Frigi**-menyen til å frigi ordren.
 
## <a name="free-text-invoices-orders-and-project-invoice-support-in-credit-management"></a>Fritekstfakturaer, ordrer og prosjektfakturastøtte i kredittbehandling 
Kredittbehandling kan bare brukes for salgsordrer for øyeblikket. Fritekstfakturaer, salgsstedsordrer og telefonsenterordrer bruker de midlertidige kredittgrensene og forsikring/garantier du legger til for å justere kredittgrensen. De bruker ikke blokkeringsreglene, og de plasseres ikke i sperrelisten hvis det oppstår et problem med kredittgrensen.

Det er ikke støtte for prosjektfakturaer i kredittbehandling.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
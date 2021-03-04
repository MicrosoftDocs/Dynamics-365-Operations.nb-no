---
title: Oversikt over selvbetjening for ansatte og ledere
description: Denne artikkelen inneholder en oversikt over arbeidsområdet for selvbetjening for ansatte og ledere.
author: andreabichsel
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 116c85c53b0ec2fe1e1fd2d1fbc2738f5b6351fb
ms.sourcegitcommit: 1fdca917e01470fbd5d3051adb85fd63e8624b47
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/20/2020
ms.locfileid: "4419974"
---
# <a name="employee-and-manager-self-service-overview"></a>Oversikt over selvbetjening for ansatte og ledere

Denne artikkelen inneholder en oversikt over arbeidsområdet for selvbetjening for ansatte og ledere.

## <a name="edit-personal-details"></a>Rediger personopplysninger

Hvis du må legge til eller endre personlige opplysninger, kan du [Redigere personlige opplysninger](hr-employee-manager-self-service-edit-personal-information.md).

## <a name="user-not-assigned-to-a-worker-record"></a>Brukeren er ikke tilordnet til en arbeiderpost

Hvis du ikke har koblet brukeren til en **Arbeider**-post på siden **Brukere**, vil følgende melding vises:

**Bruker-ID-en din er ikke tilknyttet ansattposten i systemet. Du vil ikke kunne vise eller oppdatere informasjon før den er tilknyttet. Kontakt leder eller støtteteam for hjelp.**

Hvis du vil knytte en bruker til en **Arbeider**-post, går du til **Brukere** og velger brukeren. Velg **Rediger** og legg til den tilsvarende arbeideren i feltet **Person** på skjemaet, og velg **Lagre**. Du skal nå ha tilgang til Ansattselvbetjening.

## <a name="security-requirements-for-employee-and-manager-self-service"></a>Sikkerhetskrav for selvbetjening for ansatte og ledere

Selvbetjening for ansatte og ledere krever to sikkerhetsroller:

- Ansatte krever rollen Ansatt.
- Ledere krever både rollene Ansatt og Leder.

>[!NOTE]
>Du kan også bruke egendefinerte roller til å få tilgang til selvbetjening for ansatte og ledere så lenge de har fått tilgang til arbeidsområder for ansatte og ledere.<br>
>Ledertilgang til ansattinformasjon er basert på linjehierarkiet for gjeldende stilling i Human Resources.

## <a name="employee-self-service"></a>Ansattselvbetjening

I kategorien **Min informasjon** vises følgende informasjon om ansattselvbetjening.  

### <a name="summary"></a>Sammendrag

**Arbeidselementer som er tilordnet til meg** viser alle godkjenninger og arbeidsflytelementer som er tilordnet den ansatte. Du kan konfigurere arbeidsflytelementer for å sende e-post til brukeren.

**Spørreskjemaer som er tilordnet til meg** viser alle planlagte spørreskjemaer som er tilordnet direkte til den ansatte eller gruppen.

**Firmakatalog** lar ansatte søke etter informasjon som er knyttet til enkeltpersoner i organisasjonen. Offentlig kontaktinformasjon er tilgjengelig for alle ansatte. Firmakatalogen er begrenset til firmaet som den ansatte har logget seg på.

**Teamkalender** viser teamets kalenderinformasjon. Hvis du vil ha mer informasjon, kan du se [Vise team- og firmakalendere](hr-employee-self-service-calendar.md).

### <a name="my-career-information"></a>Informasjon om min karriere

Delen **Min karriereinformasjon** i Ansattselvbetjening inneholder kort relatert til permisjon og fravær, ytelsesstyring, kompetanse, fordeler, oppgaver og vedlegg.

Kortet **Avspaseringssaldoer** viser saldoene for eventuelle registrerte planer. Dette kortet forutsier saldoen basert på avsetningsmetoden. Du kan angi og sende fraværsforespørsler, som deretter vil gå gjennom en arbeidsflyt prosess for godkjenning. Hvis du vil ha mer informasjon om permisjons- og fraværsadministrasjon, kan du se [Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md).

**Oppgaver**-kortet viser oppgaver som er tilordnet til deg, og lar deg vise og administrere dem.

Kortet **Neste registrerte kurs** viser det neste kurset du er registrert for. Du kan vise og registrere deg for alle åpne kurs. Alle kurs som er åpne for påmelding, har statusen **Startet**, og tillater at ansatte kan registrere seg selv på dette kortet. Avhengig av organisasjonens innstillinger kan kursregistreringen gå gjennom en godkjenningsprosess.

**Sertifikat**-kortet viser sertifikatet og utløpsdatoen for sertifikatet som utløper nærmest gjeldende dato. Du kan oppdatere, legge til eller fjerne sertifikater. Avhengig av organisasjonens innstillinger kan sertifikatoppdateringer gå gjennom en godkjenningsprosess.

Kortet **Neste planlagte gjennomgang** viser neste ytelsesvurdering. Du kan starte en ny gjennomgang fra dette kortet. Lederen eller HR-representanten kan også begynne gjennomganger. Avhengig av organisasjonens innstillinger vil du kanskje også kunne vise, oppdatere og sende inn avslutningsomtaler fra dette kortet.

Du kan administrere målene med **Ytelsesmål**-kortet. Dette kortet viser hvor mange mål du har i hver status (**Ikke startet**, **I rute** og **Trenger forbedring**). Du kan opprette, oppdatere og fjerne mål, avhengig av din tilordnede rollebaserte sikkerhet. Hvis du vil, kan du legge til nye mål fra grupper eller maler. Ledere og HR-ansvarlige kan også opprette mål på vegne av ansatte og bestemme hvor detaljert hvert mål skal være. Ledere og ansatte kan samarbeide om mål, og oppdatere aktiviteter, målinger og status. Du kan også inkludere vedlegg.

Du kan vise dine eksisterende ferdigheter på **Kompetanse**-kortet. Du kan oppdatere ferdigheter, legge til nye eller fjerne alle som ikke lenger er relevante. Avhengig av organisasjonens innstillinger kan kompetanseendringer gå gjennom en godkjenningsprosess.

Du kan vise gjeldende kompensasjon via **Kompensasjon**-kortet. Velg **Vis** for å vise årslønn og siste økningsbeløp. Hvis du er ansatt i flere enn ett firma, vises hvert enkelt årlige beløp på kortet. Hvis du vil vise den detaljerte kompensasjonsloggen, velger du det årlige lønnsbeløpet for å åpne skjemaet **Fast og variabel kompentasjonslogg**. Fremtidig kompensasjon vises ikke i dette skjemaet. Hvis du har mer enn ett ansettelsesforhold, kan du bytte mellom firmaer i dette skjemaet for å vise kompensasjonsloggen uten å logge inn i hvert firma.

Vis og administrer dokumenter med **Vedlegg**-kortet. Du kan administrere alle **eksterne** vedlegg. Både HR og ansatte kan legge til vedlegg via ansattselvbetjening eller **Arbeider**-skjemaet. Vedlegg er som standard satt til **Ekstern**.

### <a name="additional-information"></a>Tilleggsinformasjon

Denne delen inneholder koblinger til andre ansattselvbetjeningsområder, lik delen **Min karriereinformasjon**.

Registrer deg for fordeler gjennom **Fordeler**-koblingen. Hvis du vil ha mer informasjon om fordelsbehandling, kan du se [Oversikt over fordeler](hr-benefits-management-overview.md)

Under **Ytelse** kan du velge **Ytelsesjournaler** for å opprette ytelsesjournaloppføringer som skal brukes på både ytelsesmål og -gjennomganger. Du kan velge **Send tilbakemelding** for å gi tilbakemelding til andre ansatte i organisasjonen. Avhengig av organisasjonens innstillinger kan e-postmeldinger sendes til mottakeren, avsenderen og lederne. Du kan sende tilbakemelding til alle ansatte i organisasjonen. Sending av tilbakemelding er ikke begrenset av firmaet.

Under **Kompetanser** kan du gjøre endringer i **Kurs**, **Utdanning**, **Tillitsverv** og **Yrkeserfaring**. Avhengig av organisasjonens innstillinger kan oppdateringer av disse kompetansene gå gjennom en godkjenningsprosess.

Du kan vise jobbdetaljer under **Organisasjon**. Jobbdetaljer omfatter ferdigheter, attester og ansvarsområder for den primære stillingen. Du kan også se ethvert lånt utstyr som er sjekket ut til deg. Avhengig av organisasjonens innstillinger kan endringer av lånt utstyr gå gjennom en godkjenningsprosess.

Under **Spørreskjema** kan du se utfylte spørreskjemaer. Du kan også se spørreskjemaer som ikke er fullført, for hele firmaet. Du kan velge å fylle ut et spørreskjema når som helst. Forfatteren av spørreskjemaet kan bestemme tidsrammen og for hvem spørreskjemaet gjelder for.

Du kan konfigurere brukerdefinerte koblinger i **Parametere for Personale**. Du kan for eksempel definere koblinger til lønnsoppgaver, årsavslutningsdokumentasjon eller eksterne løsninger. Disse koblingene vises nederst i denne delen, men du kan flytte dem ved hjelp av tilpassing.

Du kan også opprette flere kategorier ved å bygge Power Apps inn i arbeidsområdet Ansattselvbetjening. Bruk **Innstillinger**-menyen til å tilpasse siden med en Power Apps. På **Innstillinger**-menyen kan du velge å legge til en Power App, fullføre detaljene og sette inn appen. Som standard vises Power Apps som den første kategorien i sekvensen. Du kan endre rekkefølgen ved å bruke standard tilpasning.

## <a name="my-team"></a>Mitt team

I kategorien **Mitt team** vises følgende informasjon om Lederselvbetjening. Bare ledere har tilgang til **Mitt team**.

### <a name="personnel-actions"></a>Personalhandlinger

Personalhandlinger vises basert på konfigurasjonsalternativer i **Delte parametere for personaladministrasjon** og **Personalparametere**. Når det er aktivert for **Arbeidere**, aktiverer personalhandlinger nye menyalternativer, inkludert:

- **Be om ny ansatt**
- **Be om ny oppdragstaker**
- **Be om ny tilordning for arbeider**
- **Be om avslutning**
- **Be om endring av fast kompensasjon**

Du kan konfigurere disse alternativene til å gå gjennom en valgfri gjennomgangs- og godkjenningsarbeidsflyt.

Aktivering av **Stillingshandlinger** aktiverer følgende alternativer:

- **Be om ny stilling**
- **Be om endring i stillingsdetaljer**

Du kan også konfigurere disse alternativene til å gå gjennom en valgfri gjennomgangs- og godkjenningsarbeidsflyt.

### <a name="summary"></a>Sammendrag

Informasjonen i **Sammendrag**-delen er avhengig av alternativene HR har valgt i **Personalparametere**. I kategorien **Lederselvbetjening** på **Personalparametere**-siden kan du konfigurere alternativer for visning av poster som utløper, og åpne stillinger. Hvis du aktiverer disse alternativene, bestemmer du hva overordnede kan se i **Sammendrag**-delen.

Du kan konfigurere følgende fliser for ledere:

- **Sertifikater som utløper for teamet mitt**
- **Identifikasjonsnumre som utløper for teamet mitt**
- **Prøveperioder som utløper for teamet mitt**
- **Screeninger som utløper for teamet mitt**
- **Tester som utløper for teamet mitt**
- **Åpne stillinger for direkte og/eller utvidede rapporter**
- **Ventende fritidsforespørsler for teamet mitt**
- **Vurdering av teamkompetanse**
- **Kompetansegapanalyse**
- **Ytelsesjournaler for team**
- **Ytelsesmål for team**
- **Gjennomganger av teamytelse**
- **Avsluttende arbeidere**

Du kan konfigurere følgende alternativer for overordnede for å gjøre endringer eller legge til permisjonsforespørsler på vegne av sine direkte underordnede:

- Attester
- Kurs
- Utlånsvarer
- Kompetanse
- Permisjons- og fraværsforespørsler

### <a name="my-team-information"></a>Informasjon om mitt team

Med informasjon om mitt team kan ledere vise og oppdatere direkte og utvidede rapporter. Hvis du vil ha tilgang til utvidede rapporter, velger du den ansatte som har direkterapporter, og deretter velger du **Vis team** på kortet. Alle de samme alternativene gjelder utvidede rapporter som direkte rapporter. 

#### <a name="summary-tab"></a>Fanen Sammendrag

Fanen **Sammendrag** gir en rask oversikt over dine direkte rapporter. Hvis en direkte underordnet også har arbeidere som rapporterer til dem, viser kortet antall direkte underordnede i den øvre delen, sammen med en **Vis team** -knapp. Alternativer over hvert kort gjelder for den ansatte som er valgt. Hvis du for eksempel vil angi en permisjonsforespørsel på vegne av en ansatt, velger du den ansatte og velger deretter **Be om fritid** over kortene. 

Hvis du velger **Detaljer**-knappen etter å ha valgt en ansatt, vises følgende alternativer:

- **Attester**
- **Kompensasjon**
- **Kurs**
- **Vurderinger**
- **Fridager**
- **Utlånte varer**
- **Ytelsesmål**
- **Registrerte kurs**
- **Kompetanse**
- **Send tilbakemelding**

Du kan enten bare utføre endringer eller vise, avhengig av organisasjonens innstillinger.

#### <a name="position-tab"></a>Kategorien Stilling

Kategorien **Stillinger** gir en sammendragsvisning av ansatte i deres primære stilling. Navn, flis og avdeling vises i overskriftsområdet for hvert kort. Dette kortet omfatter:

- **Ansiennitetsdato** - vises fra arbeidersammendrags-delen for arbeiderskjemaet
- **Arbeidserfaring** - beregnet på grunnlag av den ansattes startdato for ansettelse
- **Antall tidligere stillinger** - basert på stillingslogg. Når du velger dette nummeret, åpnes den detaljerte visningen av alle tidligere stillinger
- **Fødselsdato** - måneden og dagen i den ansattes fødselsdato

Du kan vise stillingsdata for både direkte og utvidede rapporter.

#### <a name="compensation-tab"></a>Kategorien Kompensasjon

Kategorien **Kompensasjon** viser den ansattes årlige lønn. En firma-ID vises under lønnsbeløpet. Hvis en ansatt har mer enn én ansettelse og blir betalt fra flere juridiske enheter, vil den ansatte ha flere kompensasjonsplaner. Hvis du vil se alle kompensasjonsplaner på tvers av juridiske enheter uten å bytte mellom firmaer, må du aktivere krysskompensasjon under **Personal > Delte parametere > Avansert tilgang > Aktivere kompensasjon på tvers av firmaer**.

Hvis du vil vise kompensasjonsloggen, velger du lønnsbeløpet for å åpne **Detaljer**-skjemaet. Bare gjeldende og historiske, faste og variable kompensasjonsposter vises i **Kompensasjon**-skjemaet. Hvis en ansatt har mer enn ett ansettelsesforhold, kan du bytte mellom firmaer for å vise kompensasjonslogg i hvert firma, eller aktivere kompensasjon på tvers av firmaer i delte parametere for Personal for å vise alle kompensasjonsplaner.

Du kan vise kompensasjon for både direkte og utvidede rapporter.

#### <a name="leave-and-absence-tab"></a>Kategorien Permisjon og fravær

Kategorien **Permisjon og fravær** viser de øvre saldoene for ansatte som har aktivitet. Hvis du vil utføre en handling eller vise en fullstendig liste over aktiviteter, velger du **Detaljer** og deretter **Fridager**. I **Fridager**-skjemaet kan du vise saldoer, forespørsler, godkjent fritid og prognosesaldoer for å hjelpe ansatte med å administrere tid bedre. Avhengig av organisasjonens innstillinger kan du også be om fritid for direkte rapporter og utvidede rapporter.

#### <a name="performance-goals-tab"></a>Kategorien Ytelsesmål

I kategorien **Ytelsesmål** vises en oversikt over ytelsesmål etter status. Velg et nummer for en status, eller velg ytelsesmål fra **detaljene** for å se alle målene for en ansatt. Ledere og ansatte kan oppdatere mål etter behov over hele målet.

Ledere kan se alle mål for teamet ved hjelp av flisen **Ytelsesmål for team** i **Sammendrag**-delen i **Mitt team**.

#### <a name="reviews-tab"></a>Kategorien Omtaler

I kategorien **Omtaler** oppsummeres omtalene den ansatte har i hver tilstand: **Pågår**, **Klar til gjennomgang** og **Endelig vurdering**. Hvis du vil ha tilgang til vurderingen av en ansatt, velger du **Detaljer**-knappen og velger deretter vurderinger du vil samarbeide om. Avhengig av hvor en vurdering er i arbeidsflytprosessen, kan du se om vurderingen er tilgjengelig for oppdatering. 

Du kan se alle vurderinger for teamet ved hjelp av flisen **Gjennomgang av teamytelse** i **Sammendrag**-delen i **Mitt team**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
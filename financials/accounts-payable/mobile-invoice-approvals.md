---
title: Faktura-mobilstil godkjenninger
description: "Mobile funksjoner i Microsoft Dynamics 365 for operasjoner kan utforme mobile erfaringer forretningsvirksomhet. For avanserte scenarier plattformen også la oss utviklere utvide egenskapene som de ønsker. Den mest effektive måten å lære noen av de nye konseptene på mobile er å gå gjennom prosessen med å utforme et par scenarier. Dette emnet er ment å gi en praktisk tilnærming til utforming av mobile scenarier ved å ta leverandøren fakturaen godkjenninger for mobil som et brukstilfelle. Dette emnet hjelper deg med å utforme andre variasjoner av scenarier, og kan også brukes til andre scenarier som ikke er relatert til leverandørfakturaer."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 30229c0d24aed0bd927993b9af76b32d9bb073ee
ms.lasthandoff: 03/31/2017


---

# <a name="mobile-invoice-approvals"></a>Faktura-mobilstil godkjenninger

Mobile funksjoner i Microsoft Dynamics 365 for operasjoner kan utforme mobile erfaringer forretningsvirksomhet. For avanserte scenarier plattformen også la oss utviklere utvide egenskapene som de ønsker. Den mest effektive måten å lære noen av de nye konseptene på mobile er å gå gjennom prosessen med å utforme et par scenarier. Dette emnet er ment å gi en praktisk tilnærming til utforming av mobile scenarier ved å ta leverandøren fakturaen godkjenninger for mobil som et brukstilfelle. Dette emnet hjelper deg med å utforme andre variasjoner av scenarier, og kan også brukes til andre scenarier som ikke er relatert til leverandørfakturaer.

<a name="prerequisites"></a>Forutsetninger
-------------

| Forutsetning                                                                                            | beskrivelse                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mobile handbook før lese                                                                                |(/ dynamics365/operasjoner/dev-itpro/mobil-apps / mobile-platform.md)                                                                                                  |
| Dynamics 365 for operasjoner                                                                             | Et miljø som har Microsoft Dynamics 365 for operasjoner versjon 1611 og Microsoft Dynamics for operasjoner plattform oppdatere 3 (November 2016)                   |
| Installere hurtigreparasjonen KB 3204341.                                                                              | Oppgaveregistrering kan feilaktig registrere to Lukk kommandoer for rullegardin dialoger dette er inkludert i Dynamics 365 for operasjonen Plattformoppdatering 3 (November 2016 oppdatering) |
| Installere hurtigreparasjonen KB 3207800.                                                                              | Denne hurtigreparasjonen gjør at vedlegg skal vises på den mobile klienten dette er inkludert i Dynamics 365 for operasjonen Plattformoppdatering 3 (November 2016 oppdatering).           |
| Installere hurtigreparasjonen KB 3208224.                                                                              | Programkode for mobile leverandøren fakturaen godkjenning programmet dette er inkludert i Microsoft Dynamics AX application 7.0.1 (mai 2016).                          |
| En Android eller iOS eller en Windows-enhet som har den mobile app installert for Dynamics 365 for operasjoner | Søk etter app i riktig app lager.                                                                                                                     |

## <a name="introduction"></a>Innledning
Mobile godkjenninger for leverandørfakturaer krever tre hurtigreparasjonene som er nevnt i delen "Forutsetninger". Disse hurtigreparasjonene gir ikke et arbeidsområde for faktura-godkjenninger. Hvis du vil vite hva leses et arbeidsområde i forbindelse med mobil, mobile handbook som er nevnt i delen "Forutsetninger". Godkjenninger arbeidsområdet fakturaen må være utformet. 

Organisasjoner av alle orchestrates og definerer sin forretningsprosess for leverandørfakturaer annerledes. Før du utformer en mobil opplevelse for leverandøren fakturaen godkjenninger, bør du vurdere følgende aspekter av forretningsprosessen. Tanken er å bruke disse datapunkter som er så mye som mulig å optimalisere brukerens opplevelse på enheten.

-   Hvilke felt fra fakturahodet brukeren vil se i mobil opplevelse, og i hvilken rekkefølge?
-   Hvilke felt fra fakturalinjene brukeren vil se i mobil opplevelse, og i hvilken rekkefølge?
-   Hvor mange fakturalinjene er det i en faktura? Bruke 80-20 regelen her, og optimalisere 80 prosent.
-   Brukere vil se regnskapsdistribusjoner (faktura koding) på den mobile enheten under anmeldelser? Hvis svaret på dette spørsmålet er Ja, kan du vurdere følgende spørsmål:
    -   Hvor mange regnskapsdistribusjoner (utvidet pris, merverdiavgift, tillegg, delinger og så videre) er det for en fakturalinje? Igjen, bruke 80-20 regelen.
    -   Fakturaene også har regnskapsdistribusjoner i fakturahodet? I så fall bør disse regnskapsdistribusjoner være tilgjengelig på enheten?

> [!NOTE]
> Dette emnet forklarer ikke hvordan du redigerer regnskapsdistribusjoner, fordi denne funksjonaliteten ikke støttes for øyeblikket for mobile scenarier.

-   Brukere vil se vedlegg for fakturaen på enheten?

Utformingen av mobil opplevelse for fakturaen godkjenninger, varierer avhengig av svarene på disse spørsmålene. Målet er å optimalisere brukerens opplevelse for forretningsprosessen på mobile i en organisasjon. I resten av dette emnet, vil vi se på to scenario variasjoner som er basert på forskjellige svar på spørsmålene ovenfor. 

Som en generell veiledning, når du arbeider med mobile designer, må du kontrollere ' ut ' endringer for ikke å miste oppdateringer.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Utforme et scenario for godkjenning av enkel faktura for Contoso
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenarieattributt</th>
<th>Svar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hvilke felt fra fakturahodet brukeren vil se i mobil opplevelse, og i hvilken rekkefølge?</td>
<td><ol>
<li>Navn på leverandør</li>
<li>Fakturatotal</li>
<li>Fakturakonto</li>
<li>Fakturanummer</li>
<li>Fakturadato</li>
<li>Fakturabeskrivelse</li>
<li>Forfallsdato</li>
<li>Fakturavaluta</li>
</ol></td>
</tr>
<tr class="even">
<td>Hvilke felt fra fakturalinjene brukeren vil se i mobil opplevelse, og i hvilken rekkefølge?</td>
<td><ol>
<li>Innkjøpskategori</li>
<li>Antall</li>
<li>Enhetspris</li>
<li>Nettobeløp for linje</li>
<li>1099-beløp</li>
</ol></td>
</tr>
<tr class="odd">
<td>Hvor mange fakturalinjene er det i en faktura? Bruke 80-20 regelen her, og optimalisere 80 prosent.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Brukere vil se regnskapsdistribusjoner (faktura koding) på den mobile enheten under anmeldelser?</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Hvor mange regnskapsdistribusjoner (utvidet pris, merverdiavgift, tillegg og så videre) er det for en fakturalinje? Igjen, bruke 80-20 regelen.</td>
<td>Utvidet pris: 2 mva: 0 gebyrer: 0</td>
</tr>
<tr class="even">
<td>Fakturaene også har regnskapsdistribusjoner i fakturahodet? I så fall bør disse regnskapsdistribusjoner være tilgjengelig på enheten?</td>
<td>Brukes ikke</td>
</tr>
<tr class="odd">
<td>Brukere vil se vedlegg for fakturaen på enheten?</td>
<td>Ja</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Opprette arbeidsområdet

1.  Åpne Dynamics 365 for operasjoner i en webleser, og Logg på.
2.  Etter at du har logget på, kan du legge **& mode = mobile** til URL-adressen som vist i følgende eksempel, og Oppdater siden: https://&lt;yoururl&gt;/? cmp = usmf & mi = DefaultDashboard**& modus = mobil**
3.  Klikk på **innstillinger** (Tannhjul)-knappen øverst til høyre på siden, og klikk deretter **Mobile app**. Mobile app-designer må vises akkurat slik aktivitet opptaker som vises.
4.  Klikk **Legg til** til å opprette et nytt arbeidsområde. Gi navn til arbeidsområdet for eksempel **Mine godkjenninger**.
5.  Angi en beskrivelse.
6.  Velg en farge for arbeidsområdet. Arbeidsområdet fargen vil bli brukt for den generelle stilen for mobil opplevelse for arbeidsområdet.
7.  Velg et ikon for arbeidsområdet.
8.  Klikk **gjort**
9.  Klikk **publisere arbeidsområde** til å lagre endringene

### <a name="vendor-invoices-assigned-to-me"></a>Leverandørfakturaer som er tilordnet til meg

Den første mobile siden som du bør utforme er listen over fakturaer som er tilordnet til brukeren for gjennomgang. Hvis du vil utforme Mobil-siden, kan du bruke den **VendMobileInvoiceAssignedToMeListPage** -siden i Dynamics 365 for operasjoner. Før du fullfører denne prosedyren, må du kontrollere at minst en leverandørfaktura er tilordnet til deg for gjennomgang, og at fakturalinjen har to distribusjoner. Dette oppsettet oppfyller kravene for dette scenariet.

1.  I Dynamics 365 for URL-adressen for operasjoner, erstatter du navnet på menyelementet med **VendMobileInvoiceAssignedToMeListPage** å åpne den mobile versjonen av den **ventende leverandørfakturaer som er tilordnet til meg** listesiden i den **leverandørreskontro** modul. Avhengig av hvor mange fakturaer som du har i systemet tilordnet deg viser denne siden de fakturaene. Hvis du vil finne en bestemt faktura, kan du bruke filteret på venstre side. Men krever vi ikke en bestemt faktura for dette eksemplet. Vi krever bare noen fakturaen som er tilordnet til deg som kommer til å la deg utforme Mobil-siden. De nye sidene som er tilgjengelige er utformet spesielt for utvikling av mobile scenarier for leverandørfaktura. Derfor må du bruke disse sidene. URL-adressen skal ligne på følgende URL-adresse, og når du har angitt det, siden som vises i illustrasjonen må vises: https://&lt;yourURL&gt;/? cmp = usmf & mi =**VendMobileInvoiceAssignedToMeListPage**& mode = mobile [![ventende leverandørfakturaer som er tilordnet til meg side](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  Klikk på **innstillinger** (Tannhjul)-knappen øverst til høyre på siden, og klikk deretter **Mobile app**
3.  Velg arbeidsområdet og klikk **Rediger**
4.  Klikk **siden Legg til** til å opprette den første mobile siden.
5.  Skriv inn et navn som **min leverandørfakturaer**, og en beskrivelse, som **leverandørfakturaer som er tilordnet til meg for vurdering**.
6.  Klikk **gjort**.
7.  I mobile designer på den **feltene**, klikk **velge felt**. Kolonner på siden liste over må ligner på følgende illustrasjon. [![Kolonner på de ventende leverandørfakturaene som er tilordnet til meg side](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  Legge til de påkrevde kolonnene fra listesiden som vises til brukerne i Mobil-siden. Rekkefølgen som du legger til, er rekkefølgen som feltene vises til sluttbrukeren. Vil være den eneste måten å endre rekkefølgen på feltene ved å velge alle feltene på nytt. Basert på kravene for dette scenariet, er følgende åtte felt obligatoriske. Men noen brukere kan vurdere å åtte felt for mye informasjon å ha på en mobil enhet. Derfor vil vi vise bare de viktigste feltene i mobile listevisningen. De gjenværende feltene vises i detaljvisningen, som vi vil utforme senere. Nå skal vi legge til følgende felt. Klikk plusstegnet (**+**) i disse kolonnene du vil legge til Mobil-siden.
    1.  Navn på leverandør
    2.  Fakturatotal
    3.  Fakturakonto
    4.  Fakturanummer
    5.  Fakturadato

    Når feltene er lagt til, må Mobil-siden ligner på følgende illustrasjon. [![Siden når felt er lagt til](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  Du må også legge til følgende kolonner nå, slik at vi kan aktivere arbeidsflythandlinger senere.
    1.  Vis fullføre oppgaven
    2.  Vis Deleger aktivitet
    3.  Vis tilbakekalling oppgave
    4.  Vis Avvis oppgave
    5.  Vis fullføringsoppgaven for forespørsel
    6.  Vis Send på nytt

10. Klikk **gjort** å avslutte redigeringsmodus.
11. Klikk **tilbake** og **gjort** å avslutte arbeidsområdet
12. Klikk **publisere arbeidsområde for** å lagre arbeidet.
13. Aktiver **Vis fakturatotal på vent fakturaer listen** i Leverandørparametere-skjemaet for kontoer under **faktura**. Vær oppmerksom på at bare ved å aktivere denne parameteren, fakturatotaler beregnes som skal vises på den ventende listesiden leverandørfakturaer. Dette er en ny funksjon som en del av den nødvendige hurtigreparasjonen 3208224.

### <a name="vendor-invoice-details"></a>Fakturaopplysninger for leverandør

Hvis du vil utforme siden fakturaen detaljer for mobil, kan du bruke den **VendMobileInvoiceHeaderDetails** -siden i Dynamics 365 for operasjoner. Legg merke til at, avhengig av antall fakturaer som du har på maskinen, denne siden viser den eldste fakturaen (faktura som var opprettet først). Hvis du vil finne en bestemt faktura, kan du bruke filteret på venstre side. Men krever vi ikke en bestemt faktura for dette eksemplet. Vi krever bare noen fakturadata slik at vi kan utforme Mobil-siden. [![Arbeidsflyt](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1.  I Dynamics 365 for URL-adressen for operasjoner, erstatter du navnet på menyelementet med **VendMobileInvoiceHeaderDetails** å åpne-skjemaet
2.  Åpne mobile utforming fra den **innstillinger** (Tannhjul)-knappen.
3.  Klikk på **Rediger** for å starte redigeringsmodus i arbeidsområdet.
4.  Velg den ** min leverandørfakturaer ** som du opprettet tidligere, og klikk deretter **Rediger**.
5.  På den **felt**, klikker du **rutenett** kolonneoverskriften.
6.  Klikk **Egenskaper**&gt;**siden Legg til**. **Merk:** når du klikker på **rutenett** overskrift og legge til en side, i forhold til detaljene siden opprettes automatisk.
7.  Angi en tittel, som **Fakturaopplysninger**, og en beskrivelse, som **Vis fakturahodet og detaljer om**.
8.  Klikk **merker feltene**. Vær oppmerksom på at rekkefølgen du legger til, er rekkefølgen som feltene vises til sluttbrukeren. Vil være den eneste måten å endre rekkefølgen på feltene ved å velge alle feltene på nytt.
9.  Legg til følgende felt fra hodet, basert på kravene for dette scenariet:
    1.  Navn på leverandør
    2.  Fakturatotal
    3.  Fakturakonto
    4.  Fakturanummer
    5.  Fakturadato
    6.  Fakturabeskrivelse
    7.  Forfallsdato
    8.  Fakturavaluta

10. Legg til følgende felt fra linjer rutenettet på siden:
    1.  Innkjøpskategori
    2.  Antall
    3.  Enhetspris
    4.  Nettobeløp for linje
    5.  1099-beløp

11. Når du har lagt til alle feltene fra de forrige to trinnene, klikker du **gjort**. Siden må ligner på følgende illustrasjon. [![Siden når felt er lagt til](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. Klikk **gjort** å avslutte redigeringsmodus.
13. Klikk **tilbake** og **gjort** å avslutte arbeidsområdet
14. Klikk **publisere arbeidsområde** til å lagre arbeidet ditt

### <a name="workflow-actions"></a>Arbeidsflythandlinger

Hvis du vil legge til handlinger i arbeidsflyten, kan du bruke den **VendMobileInvoiceHeaderDetails** -siden i Dynamics 365 for operasjoner. Hvis du vil åpne denne siden, erstatter du navnet på menyelementet i URL-adressen, slik du gjorde tidligere. Deretter åpner du den mobile designeren fra den **innstillinger** (Tannhjul)-knappen. Følg disse trinnene for å legge til handlinger i arbeidsflyten på detaljer-siden.

1.  Klikk på **Rediger** for å starte redigeringsmodus i arbeidsområdet.
2.  Velg den **Fakturaopplysninger** som du opprettet tidligere, og klikk deretter **Rediger**.
3.  På den **handlinger**, klikk **legge til handlingen**.
4.  Angi en tittel for handling, som **Godkjenn**, og en beskrivelse, som **Godkjenn faktura**. Legg merke til at handlingen tittelen du angir her, blir navnet på handlingen som vises for brukeren i den mobile app.
5.  Klikk **gjort**.
6.  Klikk **merker feltene**.
7.  Gå gjennom arbeidsflytprosessen på den **VendMobileInvoiceHeaderDetails** siden og fullføre handlingen som du vil registrere. Kontroller at du skriver inn kommentarer for arbeidsflyten under denne prosessen, slik at felt kommentarene er også inkludert i mobil opplevelse.
8.  Når handlingen er kjørt, klikker du **gjort** å fullføre aktiviteten Velg felt.
9.  Klikk **gjort** å avslutte redigeringsmodus.
10. Klikk **tilbake** og **gjort** å avslutte arbeidsområdet
11. Klikk **publisere arbeidsområde** til å lagre arbeidet ditt
12. Gjenta trinn 3 til 11 for å spille inn alle nødvendige arbeidsflythandlinger. Vær oppmerksom på at det er et krav for at fakturaer som er tilordnet til deg, som er i en tilstand for å gjøre arbeidsflythandlingen tilgjengelig for at du skal utforme for.
13. Åpne Notisblokk eller Microsoft Visual Studio, og Lim inn følgende kode. Lagre filen som en js-fil. Denne koden gjør to ting:
    1.  Ekstra arbeidsflytrelaterte kolonnene som vi tidligere lagt til på siden mobile skjules. Vi har lagt til disse kolonnene slik at programmet får denne informasjonen i konteksten og kan gjøre det neste trinnet.
    2.  Basert på Arbeidsflyttrinn som er aktiv, bruker logikk til å vise bare disse handlingene.

Legg merke til at navnet på sidene og andre kontroller i JS-koden må være det samme fra arbeidsområdet.

1.  Funksjonen main (metadataService, dataService, cacheService, $q) {returnere {appInit: funksjon (appMetadata) {/ / skjul kontroller som må være til stede, men ikke synlig metadataService.configureControl (' min--leverandørfakturaer, 'ShowAccept', {skjult: SANN}); metadataService.configureControl (' min--leverandørfakturaer, 'ShowApprove', {skjult: SANN}); metadataService.configureControl (' min--leverandørfakturaer, 'ShowReject', {skjult: true}); metadataService.configureControl (' min--leverandørfakturaer, 'ShowDelegate', {skjult: SANN}); metadataService.configureControl (' min--leverandørfakturaer, 'ShowRequestChange', {skjult: true}); metadataService.configureControl (' min--leverandørfakturaer, 'ShowRecall', {skjult: true}); metadataService.configureControl (' min--leverandørfakturaer, 'ShowComplete', {skjult: SANN}); metadataService.configureControl (' min--leverandørfakturaer, 'ShowResubmit' { skjulte: SANN}); }, pageInit: funksjon (pageMetadata, "params") {Hvis (pageMetadata.Name == 'Fakturaopplysninger') {/ / Vis/Skjul arbeidsflythandlinger basert på arbeidsflyt trinn metadataService.configureAction (godta, {synlig: true}); metadataService.configureAction (Godkjenn, {synlig: SANN}); metadataService.configureAction (Avvis, {synlig: true}); metadataService.configureAction (representant, {synlig: true}); metadataService.configureAction (' Be om endring ', {synlig: true}); metadataService.configureAction (tilbakekalling, {synlig: SANN}); metadataService.configureAction (fullstendig, {synlig: SANN}); metadataService.configureAction ('Send på nytt' {synlig: SANN});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  Laste opp kodefilen til arbeidsområdet ved å velge den **Logic** kategorien
3.  Klikk **gjort** å avslutte redigeringsmodus.
4.  Klikk **tilbake** og **gjort** å avslutte arbeidsområdet
5.  Klikk **publisere arbeidsområde** til å lagre arbeidet ditt

### <a name="vendor-invoice-attachments"></a>Leverandøren fakturaen vedlegg

1.  Klikk på **innstillinger** (Tannhjul)-knappen øverst til høyre på siden, og klikk deretter **Mobile app**
2.  Klikk på **Rediger** for å starte redigeringsmodus i arbeidsområdet.
3.  Velg den ** Fakturaopplysninger ** som du opprettet tidligere, og klikk deretter **Rediger**.
4.  Angi de **dokumentbehandling** å **Ja** som vist nedenfor. **Merk:** Hvis det er ingen krav til å vise vedlegg på den mobile enheten, kan du la dette alternativet være angitt til **ingen**, som er standardinnstillingen.
5.  [![docmanagement](./media/docmanagement-216x300.png)](./media/docmanagement.png)
6.  Klikk **gjort** å avslutte redigeringsmodus.
7.  Klikk **tilbake** og **gjort** å avslutte arbeidsområdet
8.  Klikk **publisere arbeidsområde** til å lagre arbeidet ditt

### <a name="vendor-invoice-line-distributions"></a>Linje for leverandørfakturadistribusjoner

Kravene for dette scenariet bekrefter at det vil bli bare linje-nivå distribusjoner og en faktura har alltid bare én linje. Fordi dette scenariet er enkelt, må også brukeropplevelsen på den mobile enheten være enkelt nok til at brukeren ikke trenger å bore ned flere nivåer for å vise distribusjonen. Leverandørfakturaer i Dynamics 365 for operasjoner omfatter muligheten til å vise alle distribusjoner fra fakturahodet. Denne erfaringen er det vi trenger for mobile scenariet. Derfor vil vi bruke den **VendMobileInvoiceAllDistributionTree** siden for å utforme denne delen av mobile scenariet. 

> [!NOTE] 
> Å kjenne kravene hjelper oss med å bestemme hvilke bestemte siden for å bruke og hvordan nøyaktig å optimalisere mobil opplevelse for brukeren når vi utformer scenariet. Vi vil bruke en annen side til å vise distribusjoner, fordi har ulike krav for scenariet, i det andre scenariet.

1.  I URL-adressen, erstatter du navnet på menyelementet, slik du gjorde tidligere. Siden som vises bør ligne på følgende illustrasjon. [![Alle distribusjoner side](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Åpne mobile utforming fra den **innstillinger** (Tannhjul)-knappen.
3.  Klikk på **Rediger** for å starte redigeringsmodus i arbeidsområdet. **Merk:** vil du se to nye sider ble opprettet automatisk. Fordi du har aktivert dokumentbehandling i den forrige delen, oppretter systemet disse sidene. Du kan ignorere disse nye sider.
4.  Klikk **siden Legg til**.
5.  Angi en tittel, som **Vis regnskap**, og en beskrivelse, som **Vis regnskap for fakturaen**.
6.  Klikk **gjort**.
7.  På den **feltene**, klikk **velge felt**, velger du følgende felt fra siden distribusjoner, og klikk deretter **gjort**:
    1.  Beløp
    2.  Valuta
    3.  Finanskonto

> [!NOTE] 
> Vi valgte den **beskrivelse** kolonnen fra rutenettet distribusjoner, fordi kravene for dette scenariet bekreftet at den utvidede prisen er bare beløpet som det skal være distribusjoner for. Brukeren vil ikke derfor krever et annet felt til å bestemme beløpet som er fordelingen for. Men i neste scenario, vi **vil** bruker denne informasjonen, fordi kravene for scenariet angir at andre beløpstyper har distribusjoner (for eksempel merverdiavgift).
8.  Klikk **gjort** å avslutte redigeringsmodus.
9.  Klikk **tilbake** og **gjort** å avslutte arbeidsområdet
10. Klikk **publisere arbeidsområde** til å lagre arbeidet ditt

**Merk:** de **Vis regnskap** Mobil-siden er ikke koblet til noen av mobile sidene som vi har utviklet så langt. Fordi brukeren bør være i stand til å navigere til den **Vis regnskap** siden fra den **Fakturaopplysninger** siden på den mobile enheten, må vi gi navigasjon fra den **Fakturaopplysninger** siden skal den **Vis regnskap** siden. Vi etablerer denne navigasjonen ved hjelp av flere logikk via JavaScript.

1.  Åpne js-fil som du opprettet tidligere, og Legg til linjer som er uthevet i følgende kode. Denne koden gjør to ting:
    1.  Det hjelper å garantere at brukerne ikke kan gå direkte fra arbeidsområdet til den **Vis regnskap** siden.
    2.  Det oppretter en navigasjonskontroll fra den **Fakturaopplysninger** side til den **Vis regnskap** siden.

> [!NOTE] 
> Navnet på sidene og andre kontroller i JS-koden må være det samme fra arbeidsområdet.

1.  Funksjonen main (metadataService, dataService, cacheService, $q) {returnere {appInit: funksjon (appMetadata) {/ / skjul kontroller som må være til stede, men ikke synlig metadataService.configureControl (' min--leverandørfakturaer, 'ShowAccept', {skjult: SANN}); metadataService.configureControl (' min--leverandørfakturaer, 'ShowApprove', {skjult: SANN}); metadataService.configureControl (' min--leverandørfakturaer, 'ShowReject', {skjult: true}); metadataService.configureControl (' min--leverandørfakturaer, 'ShowDelegate', {skjult: SANN}); metadataService.configureControl (' min--leverandørfakturaer, 'ShowRequestChange', {skjult: true}); metadataService.configureControl (' min--leverandørfakturaer, 'ShowRecall', {skjult: true}); metadataService.configureControl (' min--leverandørfakturaer, 'ShowComplete', {skjult: SANN}); metadataService.configureControl (' min--leverandørfakturaer, 'ShowResubmit' { skjulte: SANN}); Skjule sider er ikke tilgjengelig for root navigasjon metadataService.hideNavigation('View-accounting'); Koblingen for å vise metadataService.addLink for regnskap ('-Fakturaopplysninger, ' View-regnskapet ', ' View-regnskapet-nav-control', 'Vis regnskap', true); }, pageInit: funksjon (pageMetadata, "params") {Hvis (pageMetadata.Name == 'Fakturaopplysninger') {/ / Vis/Skjul arbeidsflythandlinger basert på arbeidsflyt trinn metadataService.configureAction (godta, {synlig: true}); metadataService.configureAction (Godkjenn, {synlig: SANN}); metadataService.configureAction (Avvis, {synlig: true}); metadataService.configureAction (representant, {synlig: true}); metadataService.configureAction (' Be om endring ', {synlig: true}); metadataService.configureAction (tilbakekalling, {synlig: SANN}); metadataService.configureAction (fullstendig, {synlig: SANN}); metadataService.configureAction ('Send på nytt' {synlig: SANN});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  Laste opp kodefilen til arbeidsområdet ved å velge den **Logic** tab for å overskrive den foregående koden
3.  Klikk **gjort** å avslutte redigeringsmodus.
4.  Klikk **tilbake** og **gjort** å avslutte arbeidsområdet
5.  Klikk **publisere arbeidsområde** til å lagre arbeidet ditt

### <a name="validation"></a>Validering

Åpne programmet fra den mobile enheten, og koble til din Dynamics 365 for forekomsten av operasjoner. Kontroller at du logger deg på firmaet hvor leverandørfakturaer som er tilordnet til deg for gjennomgang. Du skal kunne utføre følgende handlinger:

-   Se den **Mine godkjenninger** arbeidsområde.
-   Gå nedover i den **Mine godkjenninger** arbeidsområde og se den **min leverandørfakturaer** siden.
-   Gå nedover i den **min leverandørfakturaer** siden og se en oversikt over fakturaer som er tilordnet til deg.
-   Gå nedover i ett av fakturaer, og se topp Fakturaopplysninger og detaljer.
-   Hvis du vil se en kobling til vedlegg på detaljer-siden, og Bruk denne koblingen til å navigere til listen vedlegg og vise vedleggene.
-   På detaljer-siden, vises en kobling til den **vise regnskap** side, og Bruk denne koblingen til å navigere til siden distribusjoner og vise distribusjonen.
-   Klikk på detaljer-siden, den **handlinger** -menyen nederst, og utføre handlinger i arbeidsflyten som gjelder for arbeidsflyttrinnet.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Utforme et scenario for godkjenning av komplekse faktura for Fabrikam
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenarieattributt</th>
<th>Svar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hvilke felt fra fakturahodet brukeren vil se i mobil opplevelse, og i hvilken rekkefølge?</td>
<td><ol>
<li>Navn på leverandør</li>
<li>Fakturabeløp</li>
<li>Fakturakonto</li>
<li>Fakturanummer</li>
<li>Fakturadato</li>
<li>Fakturabeskrivelse</li>
<li>Forfallsdato</li>
<li>Fakturavaluta</li>
</ol></td>
</tr>
<tr class="even">
<td>Hvilke felt fra fakturalinjene brukeren vil se i mobil opplevelse, og i hvilken rekkefølge?</td>
<td><ol>
<li>Innkjøpskategori</li>
<li>Antall</li>
<li>Enhetspris</li>
<li>Nettobeløp for linje</li>
<li>1099-beløp</li>
</ol></td>
</tr>
<tr class="odd">
<td>Hvor mange fakturalinjene er det i en faktura? Bruke 80-20 regelen her, og optimalisere 80 prosent.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Brukere vil se regnskapsdistribusjoner (faktura koding) på den mobile enheten under anmeldelser?</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Hvor mange regnskapsdistribusjoner (utvidet pris, merverdiavgift, tillegg og så videre) er det for en fakturalinje? Igjen, bruke 80-20 regelen.</td>
<td>Utvidet pris: 2 mva: 2 gebyrer: 2</td>
</tr>
<tr class="even">
<td>Fakturaene også har regnskapsdistribusjoner i fakturahodet? I så fall bør disse regnskapsdistribusjoner være tilgjengelig på enheten?</td>
<td>Brukes ikke</td>
</tr>
<tr class="odd">
<td>Brukere vil se vedlegg for fakturaen på enheten?</td>
<td>Ja</td>
</tr>
</tbody>
</table>

### <a name="exercise"></a>Øvelse

Følgende variasjoner kan gjøres for scenario 1, basert på kravene for scenario 2. Bruk denne inndelingen som en øvelse som du kan fullføre for læring.

1.  Fordi flere fakturalinjer er forventet i scenario 2, hjelper følgende endringer i utformingen optimalisere brukerens opplevelse på den mobile enheten:
    1.  I stedet for å vise fakturalinjer på detaljer-siden (som i scenario 1), kan brukere velge å vise linjer på en egen side for mobil.
    2.  Fordi mer enn én fakturalinjen forventes i dette tilfellet hvis den **VendMobileInvoiceAllDistributionTree** -siden brukes til å utforme siden distribusjoner for mobil (som i scenario 1), kan det være forvirrende for brukeren å koordinere linjer til distribusjoner. Derfor bruker den **VendMobileInvoiceLineDistributionTree** siden du utformer siden distribusjoner.
    3.  Ideelt sett bør distribusjonene vises i konteksten for en fakturalinje i dette scenariet. Sørg derfor for at brukeren kan gå til en linje for å se siden distribusjoner. Bruk siden koblingen muligheten til å opprette gjennomgang, akkurat som du gjorde for topp- og detaljer om sidene i scenario 1.

2.  Fordi mer enn én beløpstype forventes på distribusjoner i scenario 2 (merverdiavgift, tillegg og så videre), vil det være nyttig å vise beskrivelsen av beløpstype. (Vi utelatt informasjonen i scenario 1.)

## <a name="conclusion"></a>Konklusjon
Mobil plattform og applikasjons-egenskaper kan du utforme mobile scenarier som er optimalisert for en bruker som er grunnleggende i en organisasjon. Basert på eksemplene som finnes i dette emnet, kan du prøve andre variasjoner og opprette ulike opplevelser som oppfyller et bestemt behov.



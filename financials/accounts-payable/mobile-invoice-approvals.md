---
title: Fakturagodkjenninger for mobil
description: "Mobile funksjoner i Microsoft Dynamics 365 for Operations kan utforme mobile erfaringer forretningsvirksomhet. For avanserte scenarier lar plattformen også utviklere utvide egenskapene som de ønsker. Den mest effektive måten å lære noen av de nye konseptene på mobil er å gå gjennom prosessen med å utforme et par scenarier. Dette emnet er ment å gi en praktisk tilnærming til utforming av mobile scenarier ved å ta godkjenning av leverandørfaktura for mobil som et brukstilfelle. Dette emnet hjelper deg med å utforme andre variasjoner av scenarier, og kan også brukes til andre scenarier som ikke er relatert til leverandørfakturaer."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 511dc31b96f2f5133dd0c22712d2c8d6f8746e8c
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="mobile-invoice-approvals"></a>Fakturagodkjenninger for mobil

[!include[banner](../includes/banner.md)]


Mobile funksjoner i Microsoft Dynamics 365 for Operations kan utforme mobile erfaringer forretningsvirksomhet. For avanserte scenarier lar plattformen også utviklere utvide egenskapene som de ønsker. Den mest effektive måten å lære noen av de nye konseptene på mobil er å gå gjennom prosessen med å utforme et par scenarier. Dette emnet er ment å gi en praktisk tilnærming til utforming av mobile scenarier ved å ta godkjenning av leverandørfaktura for mobil som et brukstilfelle. Dette emnet hjelper deg med å utforme andre variasjoner av scenarier, og kan også brukes til andre scenarier som ikke er relatert til leverandørfakturaer.

<a name="prerequisites"></a>Forutsetninger
-------------

| Forutsetning                                                                                            | beskrivelse                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Før du leser håndboken for mobil                                                                                |(/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform.md)                                                                                                  |
| Dynamics 365 for Operations                                                                             | Et miljø som har Microsoft Dynamics 365 for Operations versjon 1611 og for Microsoft Dynamics for Operations plattformoppdatering 3 (november 2016)                   |
| Installer hurtigreparasjon KB 3204341.                                                                              | Oppgaveregistrering kan feilaktig registrere to Lukk-kommandoer for rullegardindialoger. Dette er inkludert i Dynamics 365 for Operations plattformoppdatering 3 (November 2016 oppdatering) |
| Installer hurtigreparasjon KB 3207800.                                                                              | Denne hurtigreparasjonen gjør at vedlegg skal vises på den mobile klienten. Dette er inkludert i Dynamics 365 for Operations plattformoppdatering 3 (November 2016 oppdatering).           |
| Installer hurtigreparasjon KB 3208224.                                                                              | Programkode for godkjenning av leverandørfaktura på mobil : Dette er inkludert i Microsoft Dynamics AX 7.0.1 (mai 2016).                          |
| En Android- eller iOS- eller Windows-enhet som har mobilappen installert for Dynamics 365 for Operations | Søk etter appen i riktig applager.                                                                                                                     |

## <a name="introduction"></a>Innledning
Mobile godkjenninger for leverandørfakturaer krever de tre hurtigreparasjonene som er nevnt i delen "Forutsetninger". Disse hurtigreparasjonene gir ikke et arbeidsområde for fakturagodkjenninger. Hvis du vil vite hva et arbeidsområde er i forbindelse med mobil, kan du lese håndboken for mobil som er nevnt i delen "Forutsetninger". Arbeidsområdet for fakturagodkjenninger må være utformet. 

Alle organisasjoner lager og definerer sin forretningsprosess for leverandørfakturaer annerledes. Før du utformer en mobil opplevelse for godkjenning av leverandørfakturaer, bør du vurdere følgende aspekter av forretningsprosessen. Tanken er å bruke disse datapunkter som er så mye som mulig å optimalisere brukerens opplevelse på enheten.

-   Hvilke felt fra fakturahodet brukeren vil se i mobil opplevelse, og i hvilken rekkefølge?
-   Hvilke felt fra fakturalinjer brukeren vil se i mobil opplevelse, og i hvilken rekkefølge?
-   Hvor mange fakturalinjene er det i en faktura? Bruke 80-20 regelen her, og optimalisere 80 prosent.
-   Brukere vil se regnskapsdistribusjoner (fakturakoding) på den mobile enheten under anmeldelser? Hvis svaret på dette spørsmålet er Ja, kan du vurdere følgende spørsmål:
    -   Hvor mange regnskapsdistribusjoner (utvidet pris, merverdiavgift, tillegg, delinger og så videre) er det for en fakturalinje? Igjen, bruke 80-20 regelen.
    -   Fakturaene også har regnskapsdistribusjoner i fakturahodet? I så fall bør disse regnskapsdistribusjoner være tilgjengelig på enheten?

> [!NOTE]
> Dette emnet forklarer ikke hvordan du redigerer regnskapsdistribusjoner, fordi denne funksjonaliteten ikke støttes for øyeblikket for mobile scenarier.

-   Brukere vil se vedlegg for fakturaen på enheten?

Utformingen av mobil opplevelse for fakturagodkjenninger varierer avhengig av svarene på disse spørsmålene. Målet er å optimalisere brukerens opplevelse for forretningsprosessen på mobil i en organisasjon. I resten av dette emnet vil vi se på to scenariovariasjoner som er basert på forskjellige svar på spørsmålene ovenfor. 

Som en generell veiledning, når du arbeider med mobile designer, må du "publisere" endringene for ikke å miste oppdateringer.

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
<td>Hvilke felt fra fakturalinjer brukeren vil se i mobil opplevelse, og i hvilken rekkefølge?</td>
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
<td>Brukere vil se regnskapsdistribusjoner (fakturakoding) på den mobile enheten under anmeldelser?</td>
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

### <a name="create-the-workspace"></a>Opprett arbeidsområdet

1.  Åpne Dynamics 365 for operasjoner i en webleser, og logg på.
2.  Etter at du har logget på, kan du legge til **& mode = mobile** i URL-adressen som vist i følgende eksempel, og oppdater siden: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**
3.  Klikk på **Innstillinger** (tannhjul)-knappen øverst til høyre på siden, og klikk deretter **Mobile app**. Mobile app-designer må vises akkurat slik oppgaveopptaker vises.
4.  Klikk på **Legg til** for å opprette det nye arbeidsområdet. For dette eksemplet gir du arbeidsområdet navnet **Mine godkjenninger**.
5.  Angi en beskrivelse.
6.  Velg en farge for arbeidsområdet. Arbeidsområdefargen vil bli brukt for den generelle stilen for mobil opplevelse for arbeidsområdet.
7.  Velg et ikon for arbeidsområdet.
8.  Klikk **Ferdig**.
9.  Klikk **Publiser arbeidsområde** for å lagre endringene

### <a name="vendor-invoices-assigned-to-me"></a>Leverandørfakturaer som er tilordnet til meg

Den første mobile siden som du bør utforme er listen over fakturaer som er tilordnet til brukeren for gjennomgang. Hvis du vil utforme Mobil-siden, kan du bruke **VendMobileInvoiceAssignedToMeListPage**-siden i Dynamics 365 for Operations. Før du fullfører denne prosedyren, må du kontrollere at minst en leverandørfaktura er tilordnet til deg for gjennomgang, og at fakturalinjen har to distribusjoner. Dette oppsettet oppfyller kravene for dette scenariet.

1.  I Dynamics 365 for URL-adressen for operasjoner, erstatter du navnet på menyelementet med **VendMobileInvoiceAssignedToMeListPage** for å åpne den mobile versjonen av listesiden **Ventende leverandørfakturaer som er tilordnet til meg** i **Leverandører**-modulen. Avhengig av hvor mange fakturaer som du har i systemet tilordnet deg viser denne siden de fakturaene. Du kan bruke filteret til venstre for å finne en spesifikk faktura. Men krever vi ikke en bestemt faktura for dette eksemplet. Vi krever bare noen fakturaen som er tilordnet til deg som kommer til å la deg utforme Mobil-siden. De nye sidene som er tilgjengelige er utformet spesielt for utvikling av mobile scenarier for leverandørfaktura. Derfor må du bruke disse sidene. URL-adressen skal ligne på følgende URL-adresse, og når du har angitt det, må siden som vises i illustrasjonen, vises: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Ventende leverandørfakturaer som er tilordnet til meg-siden](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  Klikk på **Innstillinger** (tannhjul)-knappen øverst til høyre på siden, og klikk deretter **Mobile app**
3.  Velg arbeidsområdet og klikk **Rediger**
4.  Klikk **Legg til side** for å opprette den første mobilsiden.
5.  Skriv inn et navn som **Mine leverandørfakturaer** og en beskrivelse som **Leverandørfakturaer som er tilordnet til meg for gjennomgang**.
6.  Klikk **Ferdig**.
7.  I mobile designer på **Felt**-kategorien, klikk **Velg felt**. Kolonnene på listesiden over må ligne på følgende illustrasjon. [![Kolonner på siden Ventende leverandørfakturaer som er tilordnet til meg](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  Legg til de påkrevde kolonnene fra listesiden som vises til brukerne på mobilsiden. Rekkefølgen som du legger til, er rekkefølgen som feltene vises til sluttbrukeren. Vil være den eneste måten å endre rekkefølgen på feltene ved å velge alle feltene på nytt. Basert på kravene for dette scenariet, er følgende åtte felt obligatoriske. Men noen brukere kan vurdere at åtte felt er for mye informasjon å ha på en mobil enhet. Derfor vil vi vise bare de viktigste feltene i den mobile listevisningen. De gjenværende feltene vises i detaljvisningen, som vi vil utforme senere. Nå skal vi legge til følgende felt. Klikk plusstegnet (**+**) i disse kolonnene for å legge dem til på den mobile siden.
    1.  Navn på leverandør
    2.  Fakturatotal
    3.  Fakturakonto
    4.  Fakturanummer
    5.  Fakturadato

    Når feltene er lagt til, må mobilsiden ligne på følgende illustrasjon. [![Side når felt er lagt til](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  Du må også legge til følgende kolonner nå, slik at vi kan aktivere arbeidsflythandlinger senere.
    1.  Vis fullført oppgave
    2.  Vis delegert oppgave
    3.  Vis tilbakekallt oppgave
    4.  Vis avvist oppgave
    5.  Vis oppgave for å be om fullføring
    6.  Vis send på nytt-oppgave

10. Klikk **Ferdig** for å avslutte redigeringsmodus.
11. Klikk **Tilbake** og deretter **Ferdig** for å gå ut av arbeidsområdet.
12. Klikk **Publiser arbeidsområde** for å lagre arbeidet.
13. Aktiver **Vis fakturatotal på listen over leverandørfakturaer på vent** i skjemaet med leverandørparametere under **Faktura**. Vær oppmerksom på at bare ved å aktivere denne parameteren, fakturatotaler beregnes som skal vises på den ventende listesiden leverandørfakturaer. Dette er en ny funksjon som en del av den nødvendige hurtigreparasjonen 3208224.

### <a name="vendor-invoice-details"></a>Leverandørfakturadetaljer

Hvis du vil utforme siden med fakturadetaljer for mobil, kan du bruke siden **VendMobileInvoiceHeaderDetails** i Dynamics 365 for Operations. Legg merke til at, avhengig av antall fakturaer som du har på maskinen, denne siden viser den eldste fakturaen (faktura som var opprettet først). Du kan bruke filteret til venstre for å finne en spesifikk faktura. Men krever vi ikke en bestemt faktura for dette eksemplet. Vi krever bare noen fakturadata slik at vi kan utforme mobilsiden. [![Arbeidsflytside](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1.  I Dynamics 365 for Operations erstatter du navnet på menyelementet med **VendMobileInvoiceHeaderDetails** for å åpne skjemaet
2.  Åpne utformingen for mobil fra **Innstillinger** (tannhjul)-knappen.
3.  Klikk på **Rediger**-knappen for å starte redigeringsmodus i arbeidsområdet.
4.  Velg siden **Mine leverandørfakturaer** som du opprettet tidligere, og klikk deretter **Rediger**.
5.  På kategorien **Felt** klikker du **Rutenett**-kolonneoverskriften.
6.  Klikk **Egenskaper** &gt; **Legg til side**. **Obs!** Når du klikker på **Rutenett**-overskriften og legger til en side, i forhold til detaljene siden opprettes automatisk.
7.  Angi en tittel, som **Fakturaopplysninger**, og en beskrivelse, som **Vis fakturahode og linjedetaljer**.
8.  Klikk **Velg felt**. Legg merke til at rekkefølgen som du legger til, er rekkefølgen som feltene vises til sluttbrukeren. Vil være den eneste måten å endre rekkefølgen på feltene ved å velge alle feltene på nytt.
9.  Legg til følgende felt fra hodet, basert på kravene for dette scenariet:
    1.  Navn på leverandør
    2.  Fakturatotal
    3.  Fakturakonto
    4.  Fakturanummer
    5.  Fakturadato
    6.  Fakturabeskrivelse
    7.  Forfallsdato
    8.  Fakturavaluta

10. Legg til følgende felt fra rutenettlinjene på siden:
    1.  Innkjøpskategori
    2.  Antall
    3.  Enhetspris
    4.  Nettobeløp for linje
    5.  1099-beløp

11. Når du har lagt til alle feltene fra de forrige to trinnene, klikker du **Ferdig**. Siden må ligne på følgende illustrasjon. [![Side når felt er lagt til](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. Klikk **Ferdig** for å avslutte redigeringsmodus.
13. Klikk **Tilbake** og deretter **Ferdig** for å gå ut av arbeidsområdet.
14. Klikk **Publiser arbeidsområde** for å lagre arbeidet

### <a name="workflow-actions"></a>Arbeidsflythandlinger

Hvis du vil legge til handlinger i arbeidsflyten, kan du bruke siden **VendMobileInvoiceHeaderDetails** i Dynamics 365 for Operations. Hvis du vil åpne denne siden, erstatter du navnet på menyelementet i URL-adressen, slik du gjorde tidligere. Åpne deretter utformingen for mobil fra **Innstillinger** (tannhjul)-knappen. Følg disse trinnene for å legge til handlinger i arbeidsflyten på detaljer-siden.

1.  Klikk på **Rediger**-knappen for å starte redigeringsmodus i arbeidsområdet.
2.  Velg siden **Mine leverandørfakturaer** som du opprettet tidligere, og klikk deretter **Rediger**.
3.  På kategorien **Handlinger** klikker du **Legg til handling**.
4.  Angi en tittel for handling, som **Godkjenn**, og en beskrivelse, som **Godkjenn faktura**. Legg merke til at handlingstittelen du angir her, blir navnet på handlingen som vises for brukeren i den mobile app.
5.  Klikk **Ferdig**.
6.  Klikk **Velg felt**.
7.  Gå gjennom arbeidsflytprosessen på siden **VendMobileInvoiceHeaderDetails**, og fullfør handlingen som du vil registrere. Kontroller at du skriver inn kommentarer for arbeidsflyten under denne prosessen, slik at et kommentarfelt også er inkludert i mobilopplevelsen.
8.  Når arbeidsflythandlingen er utført, klikker du **Ferdig** å fullføre Velg felt-oppgaven.
9.  Klikk **Ferdig** for å avslutte redigeringsmodus.
10. Klikk **Tilbake** og deretter **Ferdig** for å gå ut av arbeidsområdet.
11. Klikk **Publiser arbeidsområde** for å lagre arbeidet
12. Gjenta trinn 3 til 11 for å registrere alle nødvendige arbeidsflythandlinger. Vær oppmerksom på at det er et krav at fakturaer er tilordnet til deg er i en tilstand som gjør arbeidsflythandlingene tilgjengelige som du skal utforme for.
13. Åpne Notisblokk eller Microsoft Visual Studio, og lim inn følgende kode. Lagre filen som en .js-fil. Denne koden gjør to ting:
    1.  De ekstra arbeidsflytrelaterte kolonnene som vi tidligere lagt til på den mobile listesiden, skjules. Vi har lagt til disse kolonnene slik at appen får denne informasjonen i kontekst og kan utføre det neste trinnet.
    2.  Basert på arbeidsflyttrinnet som er aktivt, brukes logikk til å vise bare disse handlingene.

Legg merke til at navnet på sidene og andre kontroller i JS-koden må være det samme fra arbeidsområdet.

1.  function main(metadataService, dataService, cacheService, $q) {        return {            appInit: function (appMetadata) {                // Hide controls that need to be present, but not visible                metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });              metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });            metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });            },            pageInit: function (pageMetadata, params) {     if (pageMetadata.Name == 'Invoice-details') {                    // Show/hide workflow actions based on workflow step                    metadataService.configureAction('Accept', { visible: true });                    metadataService.configureAction('Approve', { visible: true });                    metadataService.configureAction('Reject', { visible: true });                    metadataService.configureAction('Delegate', { visible: true });                    metadataService.configureAction('Request-change', { visible: true });                    metadataService.configureAction('Recall', { visible: true });                    metadataService.configureAction('Complete', { visible: true });                    metadataService.configureAction('Resubmit', { visible: true });

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

2.  Last opp kodefilen til arbeidsområdet ved å velge **Logic**-kategorien
3.  Klikk **Ferdig** for å avslutte redigeringsmodus.
4.  Klikk **Tilbake** og deretter **Ferdig** for å gå ut av arbeidsområdet.
5.  Klikk **Publiser arbeidsområde** for å lagre arbeidet

### <a name="vendor-invoice-attachments"></a>Leverandørfakturavedlegg

1.  Klikk på **Innstillinger** (tannhjul)-knappen øverst til høyre på siden, og klikk deretter **Mobile app**
2.  Klikk på **Rediger**-knappen for å starte redigeringsmodus i arbeidsområdet.
3.  Velg siden **Mine leverandørfakturaer** som du opprettet tidligere, og klikk deretter **Rediger**.
4.  Angi **Dokumentbehandling** til **Ja** som vist nedenfor. **Obs!** Hvis det er ingen krav til å vise vedlegg på den mobile enheten, kan du la dette alternativet være angitt til **Nei**, som er standardinnstillingen.
5.  [![dokumentbehandling](./media/docmanagement-216x300.png)](./media/docmanagement.png)
6.  Klikk **Ferdig** for å avslutte redigeringsmodus.
7.  Klikk **Tilbake** og deretter **Ferdig** for å gå ut av arbeidsområdet.
8.  Klikk **Publiser arbeidsområde** for å lagre arbeidet

### <a name="vendor-invoice-line-distributions"></a>Leverandørfakturalinjedistribusjoner

Kravene for dette scenariet bekrefter at det vil bli bare distribusjoner på linjenivå, og at en faktura har alltid bare én linje. Fordi dette scenariet er enkelt, må også brukeropplevelsen på den mobile enheten være enkel nok til at brukeren ikke trenger å bore ned flere nivåer for å vise distribusjonen. Leverandørfakturaer i Dynamics 365 for Operations omfatter muligheten til å vise alle distribusjoner fra fakturahodet. Denne opplevelsen er det vi trenger for det mobile scenariet. Derfor vil vi bruke siden **VendMobileInvoiceAllDistributionTree** til å utforme denne delen av det mobile scenariet. 

> [!NOTE] 
> Å kjenne kravene hjelper oss med å bestemme hvilke bestemte siden for å bruke og hvordan nøyaktig å optimalisere mobil opplevelse for brukeren når vi utformer scenariet. Vi vil bruke en annen side til å vise distribusjoner, fordi har ulike krav for scenariet, i det andre scenariet.

1.  Erstatt navnet på menyelementet i URL-adressen, slik du gjorde tidligere. Siden som vises bør ligne på følgende illustrasjon. [![Alle distribusjoner-siden](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Åpne utformingen for mobil fra **Innstillinger** (tannhjul)-knappen.
3.  Klikk på **Rediger**-knappen for å starte redigeringsmodus i arbeidsområdet. **Obs!** Du skal se at to nye sider ble opprettet automatisk. Fordi du har aktivert dokumentbehandling i den forrige delen, oppretter systemet disse sidene. Du kan ignorere disse nye sider.
4.  Klikk **Legg til side**.
5.  Angi en sidetittel, som **Vis regnskap**, og en beskrivelse, som **Vis regnskap for fakturaen**.
6.  Klikk **Ferdig**.
7.  På kategorien **Felt**, klikk **Velg felt**, velg du følgende felt fra siden med distribusjoner, og klikk deretter **Ferdig**:
    1.  Beløp
    2.  Valuta
    3.  Finanskonto

> [!NOTE] 
> Vi valgte ikke **Beskrivelse**-kolonnen fra rutenettet over distribusjoner, fordi kravene for dette scenariet bekreftet at den utvidede prisen er bare beløpet som det skal være distribusjoner for. Brukeren vil derfor ikke trenge et annet felt til å bestemme beløpet som er fordelingen for. Men i neste scenario **vil** vi bruke denne informasjonen, fordi kravene for scenariet angir at andre beløpstyper har distribusjoner (for eksempel merverdiavgift).
8.  Klikk **Ferdig** for å avslutte redigeringsmodus.
9.  Klikk **Tilbake** og deretter **Ferdig** for å gå ut av arbeidsområdet.
10. Klikk **Publiser arbeidsområde** for å lagre arbeidet

**Obs!** Mobilsiden **Vis regnskap** er ikke koblet til noen av mobilsidene som vi har utviklet så langt. Fordi brukeren bør være i stand til å navigere til siden **Vis regnskap** fra siden **Fakturaopplysninger** på den mobile enheten, må vi gi navigasjon fra siden **Fakturaopplysninger** til siden **Vis regnskap**. Vi etablerer denne navigasjonen ved hjelp av ekstra logikk via JavaScript.

1.  Åpne .js-filen som du opprettet tidligere, og legg til linjene som er uthevet i følgende kode. Denne koden gjør to ting:
    1.  Den hjelper å garantere at brukerne ikke kan gå direkte fra arbeidsområdet til siden **Vis regnskap**.
    2.  Den oppretter en navigasjonskontroll fra siden **Fakturaopplysninger** til siden **Vis regnskap**.

> [!NOTE] 
> Navnet på sidene og andre kontroller i JS-koden må være det samme fra arbeidsområdet.

1.  function main(metadataService, dataService, cacheService, $q) {        return {            appInit: function (appMetadata) {                // Hide controls that need to be present, but not visible                metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });              metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });            metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });                // Hide pages not applicable for root navigation                metadataService.hideNavigation('View-accounting');                //Link to view accounting                metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);            },            pageInit: function (pageMetadata, params) {     if (pageMetadata.Name == 'Invoice-details') {                    // Show/hide workflow actions based on workflow step                    metadataService.configureAction('Accept', { visible: true });                    metadataService.configureAction('Approve', { visible: true });                    metadataService.configureAction('Reject', { visible: true });                    metadataService.configureAction('Delegate', { visible: true });                    metadataService.configureAction('Request-change', { visible: true });                    metadataService.configureAction('Recall', { visible: true });                    metadataService.configureAction('Complete', { visible: true });                    metadataService.configureAction('Resubmit', { visible: true });

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

2.  Last opp kodefilen til arbeidsområdet ved å velge **Logic**-kategorien for å overskrive den forrige koden
3.  Klikk **Ferdig** for å avslutte redigeringsmodus.
4.  Klikk **Tilbake** og deretter **Ferdig** for å gå ut av arbeidsområdet.
5.  Klikk **Publiser arbeidsområde** for å lagre arbeidet

### <a name="validation"></a>Validering

Åpne programmet fra mobilenheten, og koble til din Dynamics 365 for Operations-forekomst. Kontroller at du logger deg på firmaet der leverandørfakturaer er tilordnet til deg for gjennomgang. Du skal kunne utføre følgende handlinger:

-   Se arbeidsområdet **Mine godkjenninger**.
-   Gå nedover i arbeidsområdet **Mine godkjenninger** og se siden **Mine leverandørfakturaer**.
-   Gå nedover på siden **Mine leverandørfakturaer** og se en oversikt over fakturaer som er tilordnet til deg.
-   Gå nedover i en av fakturaene, og se fakturahodedetaljer og linjedetaljer.
-   På detaljer-siden ser du en kobling til vedlegg. Bruk denne koblingen til å navigere til vedleggslisten og vise vedleggene.
-   På detaljer-siden ser du en kobling til siden **Vis regnskap**. Bruk denne koblingen til å navigere til distribusjonssiden og vise distribusjonene.
-   På detaljer-siden, klikker du **Handlinger**-menyen nederst, og utfør handlinger i arbeidsflyten som gjelder for arbeidsflyttrinnet.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Utforme et scenario for godkjenning av komplisert faktura for Fabrikam
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
<td>Hvilke felt fra fakturalinjer brukeren vil se i mobil opplevelse, og i hvilken rekkefølge?</td>
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
<td>Brukere vil se regnskapsdistribusjoner (fakturakoding) på den mobile enheten under anmeldelser?</td>
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
    2.  Fordi mer enn én fakturalinjen forventes i dette tilfellet hvis siden **VendMobileInvoiceAllDistributionTree** brukes til å utforme distribusjonssiden mobil (som i scenario 1), kan det være forvirrende for brukeren å koordinere linjer til distribusjoner. Bruk derfor siden **VendMobileInvoiceLineDistributionTree** til å utforme distribusjonssiden.
    3.  Ideelt sett bør distribusjonene vises i konteksten for en fakturalinje i dette scenariet. Sørg derfor for at brukeren kan gå til en linje for å se siden distribusjoner. Bruk sidekoblingsmuligheten til å opprette gjennomgangen, akkurat som du gjorde for hode- og detaljer-sidene i scenario 1.

2.  Fordi mer enn én beløpstype forventes på distribusjoner i scenario 2 (merverdiavgift, gebyrer og så videre), vil det være nyttig å vise beskrivelsen av beløpstype. (Vi har utelatt informasjonen i scenario 1.)

## <a name="conclusion"></a>Konklusjon
Mobilplattformen og applikasjonsegenskapene lar deg utforme mobile scenarier som er optimalisert for en brukerbase i en organisasjon. Basert på eksemplene som finnes i dette emnet, kan du prøve andre variasjoner og opprette ulike opplevelser som oppfyller et bestemt behov.





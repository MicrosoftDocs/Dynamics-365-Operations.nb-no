---
title: Gjennomgang av funksjonen for behandling av teknisk endring
description: Dette emnet inneholder en omfattende gjennomgang som viser hvordan du arbeider med behandling av teknisk endring.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b6270bbb6780786ed4535ca2987ed44448bd81ad
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434868"
---
# <a name="engineering-change-management-feature-walkthrough"></a>Gjennomgang av funksjonen for behandling av teknisk endring

[!include [banner](../includes/banner.md)]

Dette emnet inneholder en omfattende gjennomgang som viser hvordan du arbeider med behandling av teknisk endring. Den går gjennom alle de viktigste scenarioene:

- Grunnleggende funksjonskonfigurasjon
- Hvordan et teknisk firma oppretter et nytt teknisk produkt
- Hvordan et teknisk firma frigir et teknisk produkt til et lokalt firma
- Hvordan et lokalt firma kan se gjennom og godta et produkt som er frigitt til det av et teknisk firma
- Hvordan et lokalt firma kan bruke et teknisk produkt i standardtransaksjoner
- Hvordan du legger til et teknisk produkt i en salgsordre
- Hvordan du ber om endring i et teknisk produkt ved å opprette en forespørsel om teknisk endring
- Hvordan du planlegger og implementerer endringer ved å opprette en ordre om teknisk endring
- Hvordan du frigir et produkt som er endret

Alle øvelsene i dette emnet bruker standard eksempeldata som leveres med Microsoft Dynamics 365 Supply Chain Management. I tillegg bygger hver øvelse på den forrige øvelsen. Derfor anbefaler vi at du arbeider deg gjennom øvelsene i rekkefølge fra begynnelse til slutt, spesielt hvis du aldri har brukt funksjonen for behandling av teknisk endring. På denne måten får du en fullstendig forståelse av funksjonen.

## <a name="set-up-for-the-sample-scenario"></a>Konfigurer for eksempelscenarioet

Hvis du vil følge eksempelscenarioet i dette emnet, må du først klargjøre funksjonen ved å gjøre demonstrasjonsdata tilgjengelige og legge til noen egendefinerte poster.

Før du prøver å utføre noen av øvelsene i resten av dette emnet, følger du instruksjonene i alle under avsnittene nedenfor. Disse avsnittene introduseres også med flere viktige innstillingssider som du vil bruke når du konfigurerer behandling av teknisk endring for din egen organisasjon.

### <a name="make-standard-demo-data-available"></a>Gjøre standard demodata tilgjengelig

Arbeid på et system der [standard demodata er installert](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Standard demonstrasjonsdata legger til data i flere juridiske enheter i demo (firmaer og organisasjoner). Når du arbeider gjennom øvelsene, bruker du firmavelgeren på høyre side av navigasjonsfeltet til å bytte mellom et firma (*DEMF*) som er definert som *teknisk organisasjon* og et annet firma (*USMF*) som er definert som en *driftsorganisasjon*.

### <a name="set-up-an-engineering-organization"></a>Definere en teknisk organisasjon

En teknisk organisasjon eier de tekniske dataene, og er ansvarlig for produktdimensjoneringer og produktendringer. Gjør følgende for å konfigurere tekniske organisasjoner.

1. Gå til **behandling av teknisk endring &gt; Oppsett &gt; Tekniske organisasjoner**.
1. Velg **Ny** for å legge til en rad i rutenettet, og angi deretter følgende verdier for den:

    - **Teknisk organisasjon**: *DEMF*
    - **Organisasjonsnavn:** *Contoso Entertainment System Germany*

    ![Legge til en teknisk organisasjon](media/engineering-org.png "Legge til en teknisk organisasjon")

### <a name="set-up-the-version-product-dimension-group"></a>Definere dimensjonsgruppen for versjonsproduktet

1. Gå til **Behandling av produktinformasjon &gt; Oppsett &gt; Dimensjoner og variantgrupper &gt; Produktdimensjonsgrupper**.
1. Velg **Ny** for å opprette en produktdimensjonsgruppe.
1. Sett **Navn**-feltet til *Versjon*.
1. Velg **Lagre** for å lagre den nye dimensjonen og laste inn verdier på hurtigfanen **Produktdimensjoner**.
1. Angi **Versjon** som en aktiv produktdimensjon på hurtigfanen **Produktdimensjoner**.

    ![Legge til en produktdimensjonsgruppe](media/product-dimension-groups.png "Legge til en produktdimensjonsgruppe")

### <a name="set-up-product-lifecycle-states"></a>Konfigurer produktstatuser

Når et teknisk produkt går gjennom livssyklusen, er det viktig at du kan kontrollere hvilke transaksjoner som er tillatt for hver status. Hvis du vil konfigurere en produktstatusene, gjør du følgende.

1. Gå til **Behandling av teknisk endring &gt; Oppsett &gt; Produktstatus**.
1. Velg **Ny** for å legge til en status, og angi deretter følgende verdier for den:

    - **Tilstand:** *Drift*
    - **Beskrivelse:** *Drift*

1. Velg **Lagre** for å lagre den nye statusen og laste inn verdier på hurtigfanen **Aktiverte forretningsprosesser**.
1. Velg forretningsprosessene som skal være tilgjengelige, på hurtigfanen **Aktiverte forretningsprosesser**. I dette eksemplet lar du **Policy**-feltet være satt til *Aktivert* for alle forretningsprosesser.

    ![Aktivere forretningsprosesser for en status](media/product-lifecycle-states-1.png "Aktivere forretningsprosesser for en status")

1. Velg **Ny** for å legge til en ny status, og angi deretter følgende verdier for den:

    - **Tilstand:** *Prototype*
    - **Beskrivelse:** *Prototype*

1. Velg **Lagre** for å lagre den nye statusen og laste inn verdier på hurtigfanen **Aktiverte forretningsprosesser**.
1. Velg forretningsprosessene som skal være tilgjengelige, på hurtigfanen **Aktiverte forretningsprosesser**. I dette eksemplet setter du **Policy**-feltet til *Aktivert med advarsel* for alle forretningsprosesser.

    ![Aktivere (med advarsler) forretningsprosesser for en status](media/product-lifecycle-states-2.png "Aktivere (med advarsler) forretningsprosesser for en status")

### <a name="set-up-a-version-number-rule"></a>Definere en versjonsnummerregel

1. Gå til **Behandling av teknisk endring &gt; Oppsett &gt; Nummerregel for produktversjon**.
1. Velg **Ny** for å legge til en regel, og angi deretter følgende verdier for den:

    - **Navn:** *Automatisk*
    - **Nummerregel:** *Automatisk*
    - **Format:** *V-\#\#*

    ![Legge til en nummerregel for produktversjon](media/version-number-rule.png "Legge til en nummerregel for produktversjon")

### <a name="set-up-a-product-release-policy"></a>Definere en policy for produktfrigivelse

1. Gå til **Behandling av teknisk endring &gt; Oppsett &gt; Policyer for produktfrigivelse**.
1. Velg **Ny** for å legge til en frigivelsespolicy, og angi deretter følgende verdier for den:

    - **Navn:** *Komponenter*
    - **Beskrivelse:** *Komponenter*

1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Produkttype:** *Vare*
    - **Bruk maler:** *Alltid*
    - **Aktiv:** *Ja*

1. På **Alle produkter**-hurtigfanen velger du **Legg til** for å legge til en linje, og angi deretter følgende verdier for den:

    - **Firma:** *DEMF*
    - **Malfrigitt produkt** *D0006*

1. Velg **Legg til** for å legge til en ny linje, og angi deretter følgende verdier:

    - **Firmakonto-ID:** *USMF*
    - **Malfrigitt produkt** *D0006*
    - **Motta stykkliste:** Velg denne avmerkingsboksen.
    - **Kopier stykklistegodkjenning:** Velg denne avmerkingsboksen.
    - **Kopier stykklisteaktivering** Velg denne avmerkingsboksen.
    - **Motta rute:** Velg denne avmerkingsboksen.
    - **Kopier rutegodkjenning:** Velg denne avmerkingsboksen.
    - **Kopier ruteaktivering:** Velg denne avmerkingsboksen.

    ![Legge til en policy for produktfrigivelse](media/product-release-policy.png "Legge til en policy for produktfrigivelse")

### <a name="set-up-an-engineering-product-category"></a>Konfigurere en kategori for teknisk produkt 

Kategorier for teknisk produkt danner grunnlaget for oppretting av tekniske produkter (det vil si produkter som er versjonsstyrt og kontrollert gjennom behandling av teknisk endring). Gjør følgende for å konfigurere kategorier for teknisk produkt.

1. Gå til **Behandling av teknisk endring &gt; Detaljer om kategori for teknisk produkt**.
1. Velg **Ny** for å opprette en kategori.
1. Angi følgende verdier i **Detaljer**-hurtigfanen:

    - **Navn:** *Komponenter*
    - **Teknisk organisasjon**: *DEMF*
    - **Produkttype:** *Vare*
    - **Spor versjon i transaksjoner:** *Ja*
    - **Produktdimensjonsgruppe:** *Versjon*
    - **Produktstatus ved oppretting:** *Drift*
    - **Versjonsnummerregel:** *Automatisk*
    - **Håndhev gyldighet:** *Nei*
    - **Bruk nummerregelterminologi:** *Nei*
    - **Bruk navneregelterminologi:** *Nei*
    - **Bruk beskrivelsesregelterminologi:** *Nei*

1. I hurtigfanen **Frigivelsespolicy** setter du feltet **Produktfrigivelsespolicy** til *Komponenter*.
1. Velg **Lagre**.

    ![Legge til en kategori for teknisk produkt](media/product-category-details.png "Legge til en kategori for teknisk produkt")

### <a name="set-up-product-acceptance-conditions"></a>Definere betingelser for produktaksept

1. Bruk firmavelgeren på høyre side av navigasjonsfeltet til å bytte til den juridiske enheten *USMF* (firma).
1. Gå til **behandling av teknisk endring &gt; Oppsett &gt; Parametere for behandling av teknisk endring**.
1. I **Frigivelseskontroll**-fanen i delen **Produktaksept** setter du feltet **Produktaksept** til *Manuell*.

    ![Definere betingelser for produktaksept](media/engineering-change-management-parameters.png "Definere betingelser for produktaksept")

## <a name="create-a-new-engineering-product"></a>Opprette et nytt teknisk produkt

Et teknisk produkt er et produkt som er versjonsstyrt og kontrollert gjennom behandling av teknisk endring. Med andre ord kan du kontrollere endringene i løpet av levetiden, og endringsinformasjonen blir lagret ved hjelp av ordrer for teknisk endring. Hvis du vil opprette tekniske produkter, følger du disse trinnene.

1. Kontroller at du er i den juridiske enheten for den tekniske organisasjonen (*DEMF* for dette eksemplet). Bruk firmavelgeren på høyre side av navigasjonsfeltet, etter behov.
1. Åpne siden **Frigitte produkter** ved å følge et av følgende trinn:

    - Gå til **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.
    - Gå til **Behandling av teknisk endring &gt; Felles &gt; Frigitte produkter**.

1. I handlingsruten, i **Produkt**-fanen og **Ny**-gruppen velger du **Teknisk produkt**.
1. Angi følgende verdier i dialogboksen **Nytt produkt**:

    - **Kategori for teknisk produkt:** *Komponenter*
    - **Produktnummer:** *Z0001*
    - **Produktnavn:** *Høyttalersett*

    ![Legge til et teknisk produkt](media/new-product-dialog.png "Legge til et teknisk produkt")

    Legg merke til at **Versjon**-feltet angis automatisk ved hjelp av nummerregelen for produktversjon som du konfigurerer tidligere.

1. Velg **OK** for å opprette produktet og lukke dialogboksen.
1. Detaljsiden for det nye produktet åpnes. Legg merke til at verdier allerede er fylt ut for noen felter, for eksempel **Lagringsdimensjonsgruppe**, **Sporingsdimensjonsgruppe** eller **Varemodellgruppe**. Disse feltene ble automatisk angitt fordi produktet frigis i den juridiske enheten *DEMF*, og bruker produktfrigivelsespolicyen *Komponenter*, som er knyttet til kategorien *Komponenter* for teknisk produkt. Siden du tidligere brukte vare *D0006* som mal for å definere en linje for den juridiske enheten *DEMF*, ble verdiene som ble fylt ut, hentet fra vare *D0006*.

    ![Detaljer om frigitt produkt](media/product-details.png "Detaljer om frigitt produkt")

1. Velg **Tekniske versjoner** I handlingsruten, i **Tekniker**-fanen i **Behandling av teknisk endring**-gruppen for å vise versjonene av produktet i kategorien ingeniør.

    ![Tekniske versjoner](media/engineering-versions-list.png "Tekniske versjoner")

1. Legg merke til at det bare er én versjon for produktet på siden **Tekniske versjoner**, og at den er aktiv.
1. Velg versjonen for å vise detaljene.

    ![Detaljer for teknisk versjon](media/engineering-version-details.png "Detaljer for teknisk versjon")

1. Velg **Opprett stykkliste** på siden **Teknisk versjon** på **Stykkliste**-hurtigfanen.
1. Angi følgende verdier i dialogboksen **Opprett stykkeliste**:

    - **Stykklistenummer:** Z0001
    - **Navn:** Høyttalersett
    - **Område:** 1

    ![Opprette en stykkeliste](media/create-bom.png "Opprette en stykkeliste")

1. Velg **OK** for å legge til stykklisten og lukke dialogboksen.
1. Velg **Stykkliste** på hurtigfanen **Stykklister**.
1. På **Stykklister**-siden på hurtigfanen **Stykklistelinjer** legger du til tre linjer, én for hvert av varenumrene *D0001*, *D0003* og *D0006*.

    ![Legge til stykklistelinjer](media/bom.png "Legge til stykklistelinjer")

1. Velg **Lagre**.
1. Lukk siden.
1. Velg **Godkjenn** på siden **Teknisk versjon** på **Stykkliste**-hurtigfanen.
1. I dialogboksen som vises, velger du **OK**.

    ![Godkjenne stykklisten](media/approve-dialog.png "Godkjenne stykklisten")

1. Velg **Aktiver** på siden **Teknisk versjon** på **Stykkliste**-hurtigfanen.
1. Legg merke til at avmerkingsboksene **Aktiv** og **Godkjent** er valgt for stykklisten.

    ![Aktiv og godkjent stykkeliste](media/approved-bom.png "Aktiv og godkjent stykkeliste")

1. Lukk siden.

## <a name="release-an-engineering-product-to-a-local-company"></a><a name="release"></a>Frigi et teknisk produkt til et lokalt firma

Produktet er nå utformet av teknisk avdeling. I dette eksemplet er produktet en prototype som teknisk avdeling har utformet for en kunde. Fordi kunden er en kunde i den juridiske enheten *USMF*, må produktet frigis til den juridiske enheten.

1. Hold den juridiske enheten satt til *DEMF*. (Bruk firmavelgeren på høyre side av navigasjonsfeltet, etter behov.)
1. Gå til **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.
1. Velg produkt *Z0001*.
1. I handlingsruten, i **Produkt**-fanen i **Vedlikehold**-gruppen, velger du **Frigi produktstruktur** for å åpne veiviseren **Frigi produkter**.
1. På siden **Velg tekniske produkter som skal frigis** velger du avmerkingsbokden **Velg** for produkt *Z0001*.

    ![Velge tekniske produkter som skal frigis](media/select-eng-product-to-release.png "Velge tekniske produkter som skal frigis")

1. Velg **Frigivelsesdetaljer**.
1. Siden **Produktfrigivelsesdetaljer** vises, der du kan se gjennom detaljene for produktet som blir frigitt, og produktstrukturen. Legg merke til at alternativet **Send stykkliste** er satt til *Ja*. Derfor vil både produkt *Z0001* og alle underordnede varer fra stykklisten frigis.

    Du kan velge en hvilken som helst underordnet vare i venstre rute for å se detaljene for den. Hvis en underordnet vare har en stykkliste, kan du også velge å frigi stykklisten for den underordnede varen.

    ![Se gjennom produktfrigivelsesdetaljer](media/product-release-details.png "Se gjennom produktfrigivelsesdetaljer")

1. Lukk siden for å gå tilbake til veiviseren **Frigi produkter**.
1. Velg **Neste** for å åpne siden **Velg produktet som skal frigis**. Hvis du hadde valgt alle standard (ikke-tekniske) produkter, vil de vises på denne siden. Vær oppmerksom på at når du frigir et standardprodukt ved å velge **Frigi produktstruktur**, frigis også stykklisten og ruten.

    ![Velge standardprodukter som skal frigis](media/select-std-product-to-release.png "Velge standardprodukter som skal frigis")

1. Velg **Neste** for å åpne siden **Velg produktvarianter som skal frigis**. I dette eksemplet finnes det ingen varianter.
1. Velg **Neste** for å åpne siden **Velg firmaer**.
1. Velg firmaene som produktet skal frigis til. I dette eksemplet velger du avmerkingsboksen for **USMF**.

    ![Velge firmaene det skal frigis til](media/select-release-companies.png "Velge firmaene det skal frigis til")

1. Velg **Neste** for å åpne siden **Firmavalg**.
1. Velg **Fullfør**.

## <a name="review-and-accept-the-product-before-you-release-it-in-the-local-company"></a><a name="accept"></a>Les gjennom og godta produktet før du frigir det i det lokale firmaet

Den tekniske avdelingen har nå frigitt informasjonen til de lokale firmaene der produktet vil bli brukt. I dette eksemplet er det lokale firmaet *USMF*.

Fordi du angir feltet **Produktgodkjenning** til *Manuell* på siden **Parametere for behandling av teknisk produkt** for *USMF*-firmaet, må produkter godtas manuelt før de frigis til dette firmaet. De må med andre ord gjennomgås og godtas før de blir frigitte produkter.

Hvis du vil se gjennom produktet og frigi det i *USMF*-firmaet, følger du denne fremgangsmåten.

1. Sett den juridiske enheten til *USMF*. (Bruk firmavelgeren på høyre side av navigasjonsfeltet.)
1. Gå til **Behandling av teknisk endring &gt; Felles &gt; Produktfrigivelser &gt; Åpne produktfrigivelser**.

    Siden **Åpne produktfrigivelser** viser produkt *Z0001*, som har statusen *Venter på godkjenning*.

    ![Åpne produktutgivelser](media/open-product-releases.png "Åpne produktutgivelser")

1. Velg verdien i kolonnen **Produktnummer** for å åpne siden **Detaljer for produktfrigivelse**. Legg merke til følgende detaljer:

    - Hurtigfanen **Generelt** viser informasjon om produktfrigivelsen, for eksempel frigivelsen av selskapet (*DEMF* i dette eksemplet), området som frigis (*1*) og mottaksområdet (*1*). Fordi du ikke angav et mottaksområde i veiviseren **Frigi produkt**, kopieres verdien for frigivelsesområde til mottaksområdet.
    - Hurtigfanen **Frigivelsesdetaljer** viser informasjon om produktet og versjonen som ble frigitt. Her kan du endre innstillinger som ikrafttredelsesdatoene.
    - Hurtigfanen **Rute** viser ruten til produktet. I dette eksemplet har du imidlertid ikke frigitt noen ruter.

    ![Produktfrigivelsesdetaljer](media/product-release-details-2.png "Produktfrigivelsesdetaljer")

1. Når du er ferdig med å gjennomgå informasjonen, er du klar til å godta produktet, og på denne måten frigir du det i *USMF*-firmaet. Velg **Handlinger &gt; Godta** i handlingsruten.
1. Prduktet er nå frigitt i *USMF*-firmaet. Gå til **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Du skal se varen *Z0001*.

## <a name="use-the-product-in-transactions-in-the-local-company"></a>Bruk produktet i transaksjoner i det lokale firmaet

Behandling av hoveddata for *USMF*-firmaet vil sørge for at produktet er i statusen *Prototype*, for å sikre at brukerne blir advart hvis de ved et uhell legger det til i prosesser de arbeider på.

1. Gå til **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.
1. Velg produktet *Z0001* for å åpne detaljsiden. (Du kan bruke filteret til å finne frem til produktet.)
1. Velg **Tekniske versjoner** I handlingsruten, i **Tekniker**-fanen i **Behandling av teknisk endring**-gruppen.
1. Velg versjonsnummeret **V-01** for å åpne detaljsiden på *Tekniske versjoner*.
1. I handlingsruten, i **Produkt**-kategorien og **Status**-gruppen, velger du **endre status**.
1. I rullegardinlisten **Endre status** setter du feltet **Tilstand** til *Prototype* og velger **OK**..

    ![Endre statusen](media/change-lifecycle-state.png "Endre statusen")

## <a name="add-the-engineering-product-to-a-sales-order"></a>Legg til det tekniske produktet i en salgsordre

Produktet kan nå selges til en kunde. Hvis du vil legge til produktet i en salgsordre, gjør du følgende.

1. Gå til **Salg og markedsføring &gt; Salgsordrer &gt; Alle salgsordrer**.
1. Velg **Ny** i handlingsruten.
1. I **Opprett salgsordre**-dialogboksen setter du **Kundekonto**-feltet til *US-0002* og velger **OK**.
1. Den nye salgsordren åpnes. Legg til en rad i hurtigfanen **Salgsordrelinjer**, og sett feltet **Varenummer** til *Z000* for det.
1. Velg **Lagre** i handlingsruten.

    Du får en advarsel som informerer deg om at elementet har statusen *Prototype*. Fordi meldingen bare er en advarsel, ble imidlertid salgsordren fremdeles opprettet.

    ![Salgsordre for et teknisk produkt](media/sales-order-eng-product.png "Salgsordre for et teknisk produkt")

## <a name="request-changes-in-the-engineering-product"></a>Be om endringer i det tekniske produktet

Produktet ble sendt til en kunde, men kunden var ikke helt fornøyd og gir tilbakemelding som inneholder forslag til forbedring. Mens kunden snakker med en salgsassistent på telefonen, kan salgsassistenten be om endringene som kunden beskriver.

1. Gå til **Salg og markedsføring &gt; Salgsordrer &gt; Alle salgsordrer**.
1. Finn og åpne salgsordren du opprettet i den forrige øvelsen.
1. På hurtigfanen **Salgsordrelinjer** velger du **Behandling av teknisk endring &gt; Ny forespørsel om teknisk endring**.

    ![Opprette en forespørsel om teknisk endring fra en salgsordre](media/sales-order-eng-change-request.png "Opprette en forespørsel om teknisk endring fra en salgsordre")

1. Fyll ut forespørselen om teknisk endring basert på kundens tilbakemelding. Angi følgende verdier i dette eksemplet:

    - **Endringsforespørsel:** *555*
    - **Tittel:** *Z0001 kundeendring*
    - **Prioritet:** *lav*
    - **Kategori:** angi endring
    - **Alvorsgrad:** *middels*

1. På **Informasjon**-hurtigfanen velger du **Ny &gt; Merknad** for å legge til en merknad i rutenettet.
1. I **Beskrivelse**-feltet for den nye merknaden angir du at varen *D0003* skal slettes fra stykklisten. Hvis du må legge til mer informasjon for merknaden, kan du skrive inn tekst i **Merknader**-feltet.

    ![Forespørsel om teknisk endring](media/eng-change-request.png "Forespørsel om teknisk endring")

1. Velg **Lagre** i handlingsruten.
1. Legg merke til at varen automatisk er lagt til i hurtigfanen **Produkter**, og at kilden til den forespørselen om teknisk endring (salgsordren) er lagt til i hurtigfanen **Kilde**.

## <a name="make-changes-to-the-product-by-using-an-engineering-change-order"></a>Gjør endringer i produktet ved å bruke en ordre om teknisk endring

Salgsassistenten vet at produktet er viktig og er utformet spesielt for kunden. Salgsassistenten ringer derfor en tekniker i *DEMF*-firmaet for å gi dem beskjed om om endringsforespørselen. På denne måten kan teknikeren gjøre prosessen raskere.

Teknikeren gjennomgår nå forespørselen fra kunden og oppretter en endringsordre for produktet.

1. Fordi teknikeren jobber i *DEMF*-firmaet, setter du den juridiske enheten til *DEMF*. (Bruk firmavelgeren på høyre side av navigasjonsfeltet.)
1. Gå til **Behandling av teknisk endring &gt; Felles &gt; Forespørsler om teknisk endring**.
1. Åpne endringsforespørsel *555*.
1. Gå gjennom informasjonen, og godkjenn deretter endringen. Velg **Godkjenn** i gruppen **Endringsstatus** i fanen **Endringsforespørsel** i handlingsruten.
1. Gå til **Behandling av teknisk endring &gt; Felles &gt; Ordrer om teknisk endring**.
1. I handlingsruten velger du **Ny** for å opprette en endringsordre, og deretter angir du følgende verdier for den:

    - **Endringsordre:** *555*
    - **Tittel:** *Z0001 kundeendring*
    - **Kategori:** *Kundeendring*
    - **Prioritet:** *Lav*
    - **Alvorsgrad:** *middels*

1. På hurtigfanen **Berørte produkter** velger du **Ny &gt; Legg til eksiterende produkt** for å legge til en rad i rutenettet og angir deretter følgende verdier den:

    - **Produkt:** *Z0001*
    - **Innvirkning:** *Ny versjon*

    ![Opprette en ordre om teknisk endring](media/eng-change-order.png "Opprette en ordre om teknisk endring")

1. Legg merke til at fordi du angir feltet **Innvirkning** til *Ny versjon* viser felet **Ny versjon** i **Produktdetaljer**-hurtigfanen i **Detaljer**-fanen hva det nye versjonnummeret blir (*V-02* i dette eksemplet).

    ![Produktdetaljer for en ordre om teknisk endring](media/eng-change-order-product-details.png "Produktdetaljer for en ordre om teknisk endring")

1. Velg **Lagre** i handlingsruten.
1. På hurtigfanen **Produktdetaljer** i fanen **Stykkliste** velger du **Linjer** for å åpne stykklisten for versjon *V-01* av produktet *Z0001*.

    ![Stykklistelinjer for teknisk produkt](media/eng-product-bom-lines.png "Stykklistelinjer for teknisk produkt")

1. Velg linje for varenummeret *D0003*, og velg deretter **Slett** i handlingsruten. Verdien for **Endringstype**-feltet for denne linjen endres til *Slettet*.
1. Velg **Lagre** i handlingsruten.

    ![Endrede stykklistelinjer for teknisk produkt](media/eng-product-bom-lines-modified.png "Endrede stykklistelinjer for teknisk produkt")

1. Lukk siden **Stykklistelinje** for å gå tilbake til siden **Ordre om teknisk endring**.
1. I hurtigfanen **Produktdetaljer** på fanen **Stykkliste** ser du at verdien for **Endringstype**-feltet for stykklisten *Z0001* nå er *Endret*.

    ![Ordre om teknisk endring som inneholder en endret stykkliste](media/eng-change-order-changed-bom.png "Ordre om teknisk endring som inneholder en endret stykkliste")

    Ordren må nå godkjennes før endringene kan behandles. Når endringene er behandlet, oppdateres produktene med endringene som er tatt med i ordren om teknisk endring. I dette eksemplet er personen som oppretter ordren om teknisk endring, angitt som godkjenneren.

1. Velg **Godkjenn** i gruppen **Endringsordre** i fanen **Endringsforespørsel** i handlingsruten.
1. Velg **Behandle** for å oppdatere produktets informasjon.
1. Velg **Fullfør** for å markere endringsordren som fullført.

## <a name="release-the-changed-product"></a>Frigi det endrede produktet

Produktet kan nå frigis til *USMF*-firmaet og deretter sendes til kunden. Følg denne fremgangsmåten for å frigi produktet direkte fra ordren om teknisk endring.

1. Åpne ordren om teknisk endring som du opprettet i forrige øvelse, hvis den ikke allerede er åpen.
1. Velg **Søk** i fanen **Endringsordre** i gruppen **Produktfrigivelser** i handlingsruten.
1. Søkeresultatene viser hvilke firmaer de aktuelle produktene er blitt frigitt til. Lukk søkeresultatene.
1. Velg **Vis** i handlingruten på **Endringsordre**-fanen i **Produktfrigivelser**-gruppen for å åpne **Frigivelser**, der du kan vise resultatene av det forrige søket.
1. Velg hvert firma du vil frigi produkter til.
1. Velg **OK** for å lukke dialogboksen **Frigivelser** og gå tilbake til endringsordren.
1. Velg **Behandle** i handlingsruten i fanen **Endringsordre** i **Produktfrigivelser**-gruppen for å frigi de berørte produktene til de valgte firmaene. Du kan også velge **Frigi produktstruktur** for å starte frigivelsesprosessen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
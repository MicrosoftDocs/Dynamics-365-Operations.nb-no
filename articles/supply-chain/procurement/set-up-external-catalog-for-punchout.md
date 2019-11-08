---
title: Definere en ekstern katalog for PunchOut eProcurement
description: Dette emnet beskriver bruken av en ekstern katalog for å samle inn tilbudsinformasjon fra en leverandør og legge den til i en rekvisisjon.
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1bddb65fd5fd73e879d8a95decc9f3e4f7f37e4
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653447"
---
# <a name="set-up-an-external-catalog-for-punchout-eprocurement"></a>Definere en ekstern katalog for PunchOut eProcurement

[!include [banner](../includes/banner.md)]

Ved hjelp av den eksterne katalogen kan du sikre at produkt- og prisinformasjonen som du deretter behandler i Supply Chain Management, er nøyaktig og oppdatert. Rekvisisjonen kan deretter godkjennes og konverteres til en bestilling, og en ordre kan plasseres hos leverandøren.

Når den eksterne katalogen er definert og en ansatt forbereder en rekvisisjon, vil det være et alternativ som omdirigerer til et eksternt område, den eksterne katalogen, og returnere handlekurven som ble opprettet på det eksterne området. Denne kommunikasjonen er basert på cXML-protokollen og den må være definert mellom systemene for i kjøper- og selgerorganisasjonen.

Hvis du vil opprette kommunikasjonen, må leverandøren gi deg informasjon til bruk i konfigurasjonen avl den eksterne katalogen, for eksempel identitet, domenet til kjøperens firma, for eksempel "DUNS" og "DUNS-nummer" legitimasjon og URL-adressen leverandørens katalog ligger på.

## <a name="setting-up-an-external-catalog"></a>Definere en ekstern katalog

Den eksterne katalogen skal kunne omdirigere en ansatt som legger inn en innkjøpsrekvisisjon, til et eksternt område for å velge produkter. Produktene som de ansatte velger fra den eksterne katalogen, returneres med oppdatert prisinformasjon, og herfra kan de legges til i innkjøpsrekvisisjonen. Hensikten er ikke å la ansatte å bestille på det eksterne området. Når du setter opp den eksterne katalogen, må du å være sikker på at formålet med området den eksterne katalogen har tilgang til, er å innhente tilbudsinformasjon og ikke å foreta en ekte bestilling.

### <a name="to-set-up-an-external-vendor-catalog-complete-the-following-tasks"></a>Fullfør følgende oppgaver hvis du vil definere en ekstern levernadørkatalog:

1. Definer et innkjøpskategorihierarki. Hvis du vil ha mer informasjo, kan du se [Definere policyer for innkjøpskategori](tasks/set-up-policies-procurement-category-hierarchies.md)
2. Registrer leverandøren i Supply Chain Management. Før du kan definere konfigurasjoner for tilgang til en ekstern leverandørs katalog, må du definere leverandøren og leverandørkontakten i Microsoft Dynamics 365. Den eksterne katalogens leverandør må også legges til den valgte innkjøpskatagorien. Hvis du vil ha mer informasjon om hvordan du registrerer leverandører, kan du se [Administrere brukere av leverandørsamarbeid](manage-vendor-collaboration-users.md). Hvis du vil ha informasjon om hvordan du tilordner leverandører til en innkjøpskategori, kan du se [Godkjenne leverandører for spesifikke innkjøpskategorier](tasks/approve-vendors-specific-procurement-categories.md).
3. Kontroller at måleenhetene og valutaen som leverandøren bruker, er konfigurert. Hvis du vil ha informasjon om hvordan du oppretter en måleenhet, se [Administrere måleenheter](../pim/tasks/manage-unit-measure.md).
4. Konfigurer den eksterne leverandørkatalogen ved hjelp av kravene til leverandørens eksterne katalogområde. Hvis du vil ha mer informasjon om denne oppgaven, kan du se [Konfigurere den eksterne leverandørkatalogen](#configure-the-external-vendor-catalog).
5. Test konfigurasjonene for leverandørens eksterne katalog for å kontrollere at innstillingene er gyldige og at du har tilgang til leverandørens eksterne katalog. Bruk handlingen **Valider innstillinger** til å validere meldingen du har definert for oppsettforespørsel. Denne meldingen skal få leverandørens eksterne katalogområde til å åpnes i et nettleservindu. Under validering, kan du ikke bestille varer og tjenester fra leverandøren. For å bestille varer og tjenester, må du åpne leverandørens katalog fra en innkjøpsrekvisisjon.
6. Aktiver den eksterne katalogen ved hjelp av **Aktiver katalog**-knappen på **Eksterne kataloger**-siden. Den eksterne katalogen må aktiveres før ansatte kan bruke den. Du kan deaktivere den eksterne katalogen når som helst.


## <a name="configure-the-external-vendor-catalog"></a>Konfigurere den eksterne leverandørkatalogen

Denne delen gir mer informasjon om oppgave 4 i forrige del.

1. Skriv inn et navn og en beskrivelse for leverandørens eksterne katalog. Navnet du angir, vises i handlekurven som representerer den eksterne katalogen som vises til ansatte som oppretter en rekvisisjon. Ansatte kan klikke handlekurven for å åpne katalogen på leverandørens eksterne katalogområde.
2. Legg til et bilde ved hjelp av handlingen **Bilde av ekstern katalog**. Bidet vises i handlekurven som representerer den eksterne katalogen som vises til ansatte som oppretter en rekvisisjon. Legg merke til at bildets bredde og høyde må være lik. Hvis ikke vises bildet ikke på riktig måte.
3. Velg om nettstedet for leverandørens eksterne katalog skal vises i samme webleservindu som vinduet hvor den ansatte har opprettet rekvisisjonen, eller om det skal åpnes i et nytt vindu.
4. Velg leverandøren for katalogen. I **juridiske enheter**-listen er det en rad for hver juridiske enhet der leverandøren er definert. Hvis du vil tillate brukere å be om produkter direkte fra leverandørens katalog i noen juridiske enheter, men ikke andre, kan du bruke **Hindre tilgang**- eller **Tillat tilgang**-knappen for hver juridiske enhet der du vil at katalogen skal, eller ikke skal, være tilgjengelig.
5. I feltet **Standard utløp (dager)** angir du antallet dager som et tilbud mottatt fra den eksterne katalogen, er gyldig og kan brukes til innkjøp fra den eksterne leverandøren. Når et tilbud opprettes og hentes fra leverandørens eksterne katalogområde, er tilbudet gyldig i henhold til den gjeldende systemdatoen og forblir gyldig i antallet dager du angir i dette feltet.
6. Klikk **Legg til** for å starte tilordning av innkjøpskategoriene til den eksterne katalogen. Velg deretter en kategori i kategorinavn-listen. Listen over kategorier er et overordnet sett innkjøpskategorier som leverandøren er tilordnet til i alle juridiske enheter som er definert for leverandøren.

    > [!NOTE]
    > Innkjøpspolicyer brukes til å tillate eller begrense tilgangen til kategorier for den juridiske enheten for innkjøp eller mottaksdriftsenheten. Utstempling til en ekstern katalog krever at det gis tilgang til minst én av innkjøpskategoriene som er tilordnet til katalogen.

7. Definer forespørselsmeldingen for cXML-oppsett som skal sendes til leverandøren. Formatet for automatisk generert melding er den minste malen som kreves for å starte en økt. Fyll ut verdier for kodene.

Du kan når som helst laste den systemgenererte meldingsmalen på nytt ved å klikke **Gjenopprett meldingsformatet**. 
Legg merke til at hvis du gjenoppretter meldingsformatet, erstattes den gjeldende meldingen med det automatisk genererte meldingsformatet, som har tomme koder.

### <a name="cxml-setup-message"></a>cXML-oppsettmelding
Nedenfor finner du en beskrivelse av kodene som er inkludert i malen:

| Felt | beskrivelse | 
|---------|---------|
|< Header >< From >< Credential domain=”” >|Domenet til kjøperens firma.|
|< Header >< From >< Credential>< Identity >< /Identity > | Identiteten til kjøperens firma.|
|< Header >< To >< Credential domain=”” > | Domenet til leverandørens firma.|
|< Header >< To >< Credential>< Identity >< /Identity> | Identiteten til leverandørens firma.|
|< Header >< Sender >< Credential domain=”” > | Domenet til kjøperens firma.|
|< Header >< Sender >< Credential >< Identity >< /Identity> | Identiteten til kjøperens firma.|
|< Header >< Sender >< Credential >< SharedSecret >< /SharedSecret >|Den delte hemmeligheten for kjøperens firma.|
|< Request deploymentMode=”” >|Test- eller produksjonsdistribusjonen.|
|< Request >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|URL-adressen til sluttpunktet for leverandørens eksterne katalog.|

### <a name="extrinsic-elements"></a>Eksterne elementer

Et eksternt element er tilleggsinformasjon, for eksempel et brukernavn som er basert på en bruker som stempler seg ut. Det eksterne elementet er satt når utstempling oppstår, og det kan sendes i oppsettmeldingen for forespørsel.
Leverandøren kan ha behov for å motta et eksternt element i oppsettforespørselen. I så fall bør du legge til det eksterne elementet i listen over eksterne elementer i **Meldingsformat**-delen av **Ekstern katalog**-siden. Angi et navn for det eksterne elementet som leverandøren kan kjenne igjen, og tilordne det til en verdi. Alternativene for verdier er: brukernavn, en brukers e-postadresse eller tilfeldig verdi.
Hvis du vil ha mer informasjon om cXML-protokollen, se [cXML.org-nettsiden](http://cxml.org/).

## <a name="post-back-message"></a>Tilbakemelding
Tilbakemeldingen er meldingen som mottas fra leverandøren når brukeren sjekker ut fra det eksterne området og går tilbake til Supply Chain Management. Tilbakemeldinger kan ikke konfigureres. Meldingene er basert på definisjonen i cXML-protokollen. Her er informasjonen som kan være en del av tilbakemeldingen som mottas på en rekvisisjonslinje.

| Melding som mottas fra leverandøren | Kopiert til rekvisisjonslinje|
|------------------------------|----------------------------------------------------------|
|< ItemIn quantity=”” > |Antall|
|< ItemIn>< ItemID >< SupplierPartID >< /SupplierPartID >|ID for ekstern vare|
|< ItemDetail>< UnitPrice >< Money currency=”” >| Valuta|
|< ItemDetail >< UnitPrice >< Money >< /Money >| Enhetspris|
|< ItemDetail >< Description ShortName=”” >|Produktnavn|
|< ItemDetail >< Description >< /Description >|Inkludert i beskrivelsen av varen. Produktnavn hvis kort navn ikke er angitt.|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|Enhet|
|< ItemDetail >< Classification >< /Classification >|Inkludert i varebeskrivelsen|
|< ItemDetail >< Classification domain=”” >|Inkludert i varebeskrivelsen|

## <a name="delete-an-external-catalog"></a>Slette en ekstern katalog
Slett en ekstern katalog med slettehandlingen på siden.

Hvis et produkt fra den eksterne leverandørkatalogen er forespurt, kan den eksterne leverandørkatalogen ikke slettes. I stedet settes den eksterne leverandørkatalogens status til inaktiv. Hvis du vil fjerne tilgang til den eksterne leverandørens katalogområde, men ikke slettee det, kan du endre den eksterne katalogstatusen til inaktiv.


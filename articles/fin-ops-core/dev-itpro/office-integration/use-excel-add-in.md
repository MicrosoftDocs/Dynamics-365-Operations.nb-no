---
title: Vise og oppdatere enhetsdata med Excel
description: Dette emnet forklarer hvordan du kan åpne enhetsdata i Microsoft Excel, og deretter vise, oppdatere og redigere dataene ved hjelp av Excel-tillegget for Microsoft Dynamics.
author: jasongre
ms.date: 10/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1902e80313c5460ac38896bc2f46d83897e3a58
ms.sourcegitcommit: 49f29aaa553eb105ddd5d9b42529f15b8e64007e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2021
ms.locfileid: "7592671"
---
# <a name="view-and-update-entity-data-with-excel"></a>Vise og oppdatere enhetsdata med Excel 

[!include [applies to](../includes/applies-to-commerce-finance-scm.md)]

[!include [banner](../includes/banner.md)]


Dette emnet forklarer hvordan du kan åpne enhetsdata i Microsoft Excel, og deretter vise, oppdatere og redigere dataene ved hjelp av Excel-tillegget for Microsoft Dynamics. Hvis du vil åpne enhetsdataene, kan du starte fra enten Excel eller Finance and Operations-apper.

Ved å åpne enhetsdata i Excel, kan du raskt og enkelt vise, oppdatere og redigere dataene ved hjelp Excel-tillegget. Dette tillegget krever Microsoft Excel 2016 eller nyere.

> [!NOTE]
> Hvis Microsoft Azure Active Directory-leieren (Azure AD) er konfigurert til å bruke Active Directory Federation Services (AD FS), må du kontrollere at oppdateringen for Office fra mai 2016 er installert, slik at Excel-tillegg kan logge deg på på riktig måte.

Hvis du vil vite mer om hvordan du bruker Excel-tillegget, kan du se den korte videoen [Opprette en Excel-mal for hode- og linjemønstre](https://youtu.be/RTicLb-6dbI).

## <a name="open-entity-data-in-excel-when-you-start-from-a-finance-and-operations-app"></a>Åpne enhetsdata i Excel når du starter fra en Finance and Operations-app
1. På en side i en Finance and Operations-app velger du **Åpne i Microsoft Office**.

    Hvis rotdatakilden (tabell) for siden er den samme som rotdatakilden for alle enheter, genereres standard **Åpne i Excel**-alternativer for siden. **Åpne i Excel**-alternativer finnes på ofte brukte sider, som **Alle leverandører** og **Alle kunder**.
 
2. Velg et **Åpne i Excel**-alternativ, og åpne arbeidsboken som genereres. Denne arbeidsboken har bindingsinformasjonen for enheten, en peker til miljøet og en peker til Excel-tillegget.
3. I Excel velger du **Aktivere redigering** for å aktivere kjøring av Excel-tillegget. Excel-tillegg kjøres i en rute til høyre i Excel-vinduet.
4. Hvis du kjører Excel-tillegget for første gang, velger du **Klarer tillegget**.
5. Hvis du blir bedt om å logge på, velger du **Logg på**, og deretter logger du på ved å bruke samme legitimasjon som du brukte til å logge på Finance and Operations-appen. Excel-tillegget bruker en tidligere påloggingskontekst fra nettleseren og logger deg automatisk på, hvis det er mulig. (Hvis du vil ha mer informasjon om nettleseren som brukes basert på operativsystemet, kan du se [Nettlesere som brukes av Office-tillegg](/office/dev/add-ins/concepts/browsers-used-by-office-web-add-ins.)) For å sikre at påloggingen var vellykket, kontrollerer du brukernavnet i øvre høyre hjørne i Excel-tillegget. 

Excel-tillegg leser automatisk dataene for enheten du valgte. Legg merke til at det ikke vises data i arbeidsboken før Excel-tillegget leser dem inn.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Åpne enhetsdata i Excel når du starter fra Excel
1. I Excel, i fanen **Sett inn** i **Tillegg**-gruppen, velger du **Butikk** for å åpne Office Store.
2. Søk etter nøkkelordet **Dynamics** i Office Store, og velg deretter **Legg til** ved siden av **Microsoft Dynamics Office-tillegg** (Excel-tillegget).
3. Hvis du kjører Excel-tillegget for første gang, velger du **Klarer tillegget** for å aktivere kjøring av Excel-tillegget. Excel-tillegg kjøres i en rute til høyre i Excel-vinduet.
4. Velg **Legg til serverinformasjon** for å åpne **Alternativer**-ruten.
5. I nettleseren kopierer du nettadressen fra målforekomsten av Finance and Operations-appen, limer den inn i **Server-URL**-feltet og sletter deretter alt etter vertsnavnet. Den resulterende nettadressen skal bare inneholde vertsnavnet.

    Hvis nettadressen for eksempel er `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage`, sletter du alt unntatt `https://xxx.dynamics.com`.

6. Velg **OK**, og velg deretter **Ja** for å bekrefte endringen. Excel-tillegget startes på nytt og laster inn metadata.

    **Utforming**-knappen er nå tilgjengelig. Hvis Excel-tillegget har koblingen **Laste inn appleter**-knapp, er du sannsynligvis ikke logget på som riktig bruker. Hvis du vil ha mer informasjon om hvordan du håndterer dette problemet, kan du se feilsøkingsoppføringen [Laste inn appleter](../office-integration/office-integration-troubleshooting.md#issue-the-excel-add-in-loads-but-instead-of-showing-data-it-displays-load-applets-in-the-task-pane).

7. Velg **Utforming**. Excel-tillegget henter metadata for enhet.
8. Velg **Legg til tabell**. Det vises en liste over enheter. Enhetene vises i formatet "Navn – Etikett".
9. Velg en enhet i listen, for eksempel **Kunde – Kunder**, og velg deretter **Neste**.
10. Hvis du vil legge til et felt fra listen **Tilgjengelige felt** i listen **Valgte felt**, velger du feltet og deretter **Legg til**. Dobbeltklikk eventuelt på feltet i listen **Tilgjengelige felt**.
11. Når at du har lagt til de aktuelle feltene i listen **Valgte felt**, kontrollerer du at markøren er på riktig sted i regnearket (for eksempel celle A1), og velger deretter **Fullført**. Velg deretter **Fullfør** for å avslutte utformingen.
12. Velg **Oppdater** for å trekke inn et sett med data.

## <a name="view-and-update-entity-data-in-excel"></a>Vise og oppdatere enhetsdata i Excel
Når Excel-tillegget har lest inn enhetsdata i arbeidsboken, kan du oppdatere dataene når som helst ved å velge **Oppdater** i Excel-tillegget.

## <a name="edit-entity-data-in-excel"></a>Redigere enhetsdata i Excel
Du kan endre enhetsdata som du trenger, og deretter publisere dem tilbake til Finance and Operations-apper ved å velge **Publiser** i Excel-tillegget. Hvis du vil redigere en post, merker du en celle i regnearket og endre deretter celleverdien. Hvis du vil legge til en ny post, gjør du ett av følgende:

- Klikk på hvor som helst i datakildetabellen, og velg deretter **Ny** i Excel-tillegget.
- Klikk hvor som helst i den siste raden i datakildetabellen, og trykk deretter på Tab-tasten til markøren flyttes ut av den siste kolonnen i denne raden og det opprettes en ny rad.
- Klikk på hvor som helst i raden like under datakildetabellen, og begynner å skrive inn data i en celle. Når du flytter fokus fra cellen, utvides tabellen, slik at den nye raden tas med.
- For feltbindinger for hodeposter velger du ett av feltene, og deretter **Ny** i Excel-tillegget.

Legg merke til at en ny post bare kan opprettes hvis alle viktige og obligatorisk felt er bundet i regnearket, eller hvis standardverdiene er fylt ut ved hjelp av filterbetingelsen.

Hvis du vil slette en post, gjør du ett av følgende:

- Høyreklikk på radnummeret ved siden av regnearkraden som skal slettes, og velg deretter **Slett**.
- Høyreklikk hvor som helst i regnearkraden som skal slettes, og velg deretter **Slett** &gt; **Tabellrader**.

Hvis datakilder har blitt lagt til som tilknyttede datakilder, publiseres hodet før linjene. Hvis det finnes avhengigheter mellom andre datakilder, må du kanskje endre standard publiseringsrekkefølge. Hvis du vil endre publiseringsrekkefølgen, går du til Excel-tillegget og velger **Alternativer**-knappen (tannhjulsymbolet), og velger **Konfigurer publiseringsrekkefølge** i hurtigfanen **Datakobling**.

## <a name="add-or-remove-columns"></a>Legg til eller fjern kolonner
Du kan bruke utformingen til å justere kolonnene som automatisk legges til i regnearket.

> [!NOTE]
> Hvis **Utforming**-knappen ikke vises under **Filter**-knappen i Excel-tillegget, må du aktivere datakildeutformingen. Velg **Alternativer**-knappen (tannhjulsymbolet), og merk deretter av for **Aktiver utforming**.

1. Velg **Utforming** i Excel-tillegget. Alle datakildene vises.
2. Velg **Rediger**-knappen (blyantsymbolet) ved siden av datakilden.
3. I listen **Valgt felt** justerer du feltlisten etter behov:

    - Hvis du vil legge til et felt fra listen **Tilgjengelige felt** i listen **Valgte felt**, velger du feltet og deretter **Legg til**. Dobbeltklikk eventuelt på feltet i listen **Tilgjengelige felt**.
    - Hvis du vil fjerne et felt fra listen **Valgte felt**, velger du feltet og deretter **Fjern**. Du kan også dobbeltklikke på feltet.
    - Hvis du vil endre rekkefølgen på feltene i listen **Valgte felt**, velger du et felt og deretter **Opp** eller **Ned**.

4. Hvis du vil bruke endringene for datakilden, velger du **Oppdater**. Velg deretter **Fullfør** for å avslutte utformingen.
5. Hvis du har lagt til et felt (kolonne), velger du **Oppdater** for å trekke inn et oppdatert sett med data.

## <a name="change-the-publish-batch-size"></a>Endre størrelsen på publiseringspartiet
Når brukere publiserer endringer i dataposter ved hjelp av Excel-tillegget, sendes oppdateringene i partier. Standardstørrelsen på publiseringspartiet er 100 rader. I versjon 10.0.17 og nyere får du fleksibel kontroll over størrelsen på publiseringspartiet med funksjonen **Tillat konfigurasjon av størrelsen på publiseringspartiet i Excel-tillegget**.

Systemadministratorer kan angi en grense for størrelsen på publiseringspartiet som gjelder for hele systemet, for arbeidsbøker som åpnes i Excel, ved å bruke feltet **Grense for publiseringsparti** under **App-parametere** på siden **Parametere til Office-app**.

Du kan også endre størrelsen på publiseringspartiet for en individuell arbeidsbok ved hjelp av Excel-tillegget.

1. Åpne arbeidsboken i Excel.
2. Velg **Alternativer**-knappen (tannhjulet) øverst til høyre i Excel-tillegget.
3. Angi ønsket verdi i **Størrelse på publiseringsparti**. Verdien du angir, må være mindre enn grensen for publiseringsparti som gjelder for hele systemet.
4. Velg **OK**.
5. Lagre arbeidsboken. Hvis du ikke lagrer arbeidsboken etter at du har gjort endringer i innstillingene for tillegget, beholdes ikke disse endringene når du åpner arbeidsboken på nytt.

Forfattere av Excel-arbeidsbokmaler kan bruke den samme fremgangsmåten til å angi størrelsen på publiseringsparti for maler før de laster dem opp i systemet.

## <a name="copy-environment-data"></a>Kopier miljødata

Dataene som leses inn i arbeidsboken fra ett miljø kan kopieres til et annet miljø. Du kan imidlertid ikke bare endre nettadressen for tilkobling, fordi datahurtigbufferen i arbeidsboken vil fortsette å behandle dataene som eksisterende data. I stedet må du bruke funksjonen Kopier miljødata for å publisere dataene til et nytt miljø som nye data.

1. Velg **Alternativer**-knappen (tannhjulsymbolet), og velg deretter **Kopier miljødata** i hurtigfanen **Datakobling**. 
2. Angi nettadressen for serveren for det nye miljøet. 
3. Velg **OK**, og velg deretter **Ja** for å bekrefte handlingen. Excel-tillegget starter på nytt og kobler til det nye miljøet. Eksisterende data i arbeidsboken behandles som nye data.

    Når Excel-tillegget startes på nytt, vises en meldingsboks med informasjon om at arbeidsboken er i miljøkopieringsmodus.

4. Hvis du vil kopiere dataene til det nye miljøet som nye data, velger du **Publiser**. Hvis du vil avbryte kopieringen av miljøet og se gjennom de eksisterende dataene i det nye miljøet, velger du **Oppdater**.

## <a name="troubleshooting"></a>Feilsøking
Det finnes enkelte problemer som kan løses ved hjelp av noen enkle trinn.

- **Koblingen "Last inn appleter" vises** – Hvis du vil ha mer informasjon om dette problemet, kan du se feilsøkingsoppføringen [Laste inn appleter](../office-integration/office-integration-troubleshooting.md#issue-the-excel-add-in-loads-but-instead-of-showing-data-it-displays-load-applets-in-the-task-pane). 
- **Du får feilmeldingen "Forbudt"** – Hvis du får feilmeldingen "Forbudt" når Excel-tillegget laster inn metadata, har kontoen som er logget Excel-tillegget, ikke tillatelse til å bruke tjenesten, forekomsten eller databasen. Hvis du vil løse dette problemet, kontrollerer du at riktig brukernavn vises øverst til høyre i Excel-tillegget. Hvis feil brukernavn vises, velger du det, logger av og på igjen.
- **En tom nettside vises over Excel** – Hvis det åpnes en tom nettside i løpet av påloggingsprosessen, krever kontoen AD FS, men versjonen av Excel som kjører Excel-tillegget, er ikke ny nok til å laste inn dialogboksen for pålogging. Hvis du vil løse dette problemet, oppdaterer du Excel-versjonen du bruker. Hvis du vil oppdatere versjonen av Excel når du er i en virksomhet som er på den utsatte kanalen, kan du bruke [distribusjonsverktøyet for Office](/deployoffice/overview-office-deployment-tool) til [flytte fra den utsatte kanalen til gjeldende kanal](/deployoffice/overview-update-channels).
- **Du får et tidsavbrudd når du publiserer dataendringer** – Hvis du får tidsavbruddsmeldinger mens du prøver å publisere dataendringer til en enhet, bør du vurdere å redusere størrelsen på publiseringspartiet for den berørte arbeidsboken. Enheter som utløser større mengder logikk for postendringer, kan kreve at oppdateringer sendes i mindre partier, slik at tidsavbrudd kan unngås.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: Simulator for eksterne detaljhandelsenheter
description: "Dette emnet beskriver simulatorverktøyet for ekstern enheter som følger med Microsoft Dynamics 365 for Operations - Retail."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 894aaaaa844447030dae73826d326f99366aa068
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="retail-peripheral-simulator"></a>Simulator for eksterne detaljhandelsenheter

[!include[banner](includes/banner.md)]


Dette emnet beskriver simulatorverktøyet for ekstern enheter som følger med Microsoft Dynamics 365 for Operations - Retail.

<a name="overview"></a>Oversikt
--------

Ekstern simulator for Microsoft Dynamics 365 for Operations - Retail er et verktøy som gjør det enklere å konfigurere, teste og feilsøke eksterne enheter som brukes i detaljhandelsmiljøer. Du kan bruke den simulatoren for eksterne enheter til å strømlinjeforme testingen av eksterne detaljhandelsenheter, og til å isolere problemer som er forårsaket av feil oppsett eller enhetsdrivere med feil. Simulatoren for eksterne enheter omfatter et skrivebordsprogram som har virtuelle versjoner av enheter som støttes i Dynamics 365 for Operations - Retail. En inndeling for hver enhet viser kommunikasjonen mellom enheten og salgssted for detaljhandel (POS). Du kan også bruke det til å registrere data som er gyldig for ulike scenarier for salgsstedet. Simulatoren for eksterne enheter støtter kommunikasjon mellom salgsstedet og følgende virtuelle enheter:

-   **Skriver** – Simulatoren for eksterne enheter kan vise kvitteringer som er konfigurert for en skriver på salgsstedet.
-   **Linjevisning** – Du kan konfigurere en virtuell linjevisningsenhet for å vise aktivitet på et fysisk linjevisningsenhet.
-   **Kortleser (MSR)** – Du kan sende simulerte magnetstripehendelser til salgsstedet fra simulatoren for eksterne enheter.
-   **Skuff** – Du kan simulere en fysisk kassaskuff.
-   **Skuff 2** – Ved å definere en ekstra kassaskuff i simulatoren for eksterne enheter, kan du simulere scenarier som omfatter én enkelt kasse på salgsstedet som har to aktive skift.
-   **Skanner** – Den virtuelle strekkodeskanneren som simulatoren for eksterne enheter støtter, kan utstede hendelser for strekkodeskanning.
-   **Vekt** – En virtuell vekt lar deg simulere samhandling med varer som veies på salgsstedet.
-   **PIN-kodetastatur (Personal Identification Number)** – Du kan simulere handlinger på et PIN-kodetastatur. **Obs!** Du må implementere støtte for et fysisk PIN-kodetastatur via betalingskoblingen.
-   **Signaturregistrering** – Simulatoren for eksterne enheter inneholder en virtuell enhet for registrering av signatur som du kan konfigurere til å be om signaturer som kreves for enkelte betalingsmidler, for eksempel kundekontobetalinger.

Du kan også bruke simulatoren for eksterne enheter til å simulere hendelser for tastaturkortlesere som kommer fra en strekkodeskanner og kortleser. Simulatoren for eksterne enheter støtter spesielt kobling og innebygging av objekter for Retail POS-enheter (OPOS).

## <a name="key-scenarios"></a>Nøkkelscenarier
### <a name="troubleshooting"></a>Feilsøking

Du kan bruke simulatoren for eksterne enheter til feilsøking av enhetsoppsett. Hvis du ikke har simulatoren for eksterne enheter eller en annen enhet i samme klasse, kan det være vanskelig å finne ut hva som forårsaker problemene. Når du har simulatoren for eksterne enheter, kan du imidlertid konfigurere virtuelle enheter og kjøre samme kodebaner og forretningslogikk som brukes for fysiske enheter. Sett fra den eksterne simulatoren, er den viktigste forskjellen mellom virtuelle enheter og fysiske enheter tjenesteobjekt eller enhetsdriveren. For fysiske enheter leveres tjenesteobjektet av enhetsprodusenten. For simulatoren for eksterne enheter leveres imidlertid tjenesteobjekter som en del av simulatoren for eksterne enheter. Når den simulatoren for eksterne enheter fungerer slik den skal, og en enhet ikke fungerer slik den skal etter at navnet på enheten i maskinvareprofilen er endret til navnet på en virkelig enhet, kan du anta at det er et problem med tjenesteobjektet som produsenten har levert.

### <a name="training"></a>Kurs

Du kan bruke simulatoren for eksterne enheter til å legge til et realistisk lag for opplæring av kasserer når et oppsett for fysisk maskinvare ikke er tilgjengelig. Når simulatoren for eksterne enheter inkluderes i opplæringenscenarier, kan kassereren samhandle med effektivt med salgsstedet ved å registrere inndata som skanning av strekkoder på produkter, innlesing av gavekort og observere hvilke kvitteringer som skrives ut for en bestemt transaksjon.

### <a name="testing"></a>Testing

Du kan bruke simulatoren for eksterne enheter til å teste produktstrekkoder, kvitteringsformater og så videre, uten å måtte distribuere fysisk maskinvare i et virtuelt miljø. Siden det ikke er nødvendig med fysisk maskinvare, og du trenger ikke å distribuere en salgsstedsklient på en maskinvarestasjon eller en fysisk datamaskin, kan du raskt teste endringer som gjøres på underkontoen.

## <a name="set-up-the-peripheral-simulator"></a>Konfigurere simulatoren for eksterne enheter
### <a name="set-up-a-hardware-profile"></a>Konfigurere en maskinvareprofil

1.  Hvis du vil konfigurere simulatoren for eksterne enheter, kan du gå til **Detaljhandel og handel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofiler** &gt; **Maskinvareprofiler**.
2.  Klikk på **Ny** for å opprette en ny profil.
3.  Skriv inn verdier i feltene **Profilnummer** og **Beskrivelse**.
4.  Bruk tabellen nedenfor til å definere de virtuelle enhetene som skal testes. Her er en forklaring for kolonnene i tabellen:
    -   **Enhet** – Denne kolonnen inneholder navnet på hurtigfanen du viser for å konfigurere enheten.
    -   **Enhetstype** – Denne kolonnen viser verdien som du velger i feltet som er merket med navnet på enheten.
    -   **Enhetsnavn** – Denne kolonnen inneholder den nøyaktige verdien som du angir for enhetsnavnet. **Viktig!** Enhetsnavnene som angis her, er nødvendige, fordi maskinvarestasjonen bruker disse spesifikke navnene for å kommunisere med enhetene. Hvis du ikke bruker disse spesifikke navnene, kan ikke enheten brukes.

    | Enhet            | Enhetstype | Enhetsnavn              |
    |-------------------|-------------|--------------------------|
    | Skriver           | OPOS        | MockOPOSPrinter          |
    | Linjevisning      | OPOS        | MockOPOSLineDisplay      |
    | Kortleser               | OPOS        | MockOPOSMSR              |
    | Trassent            | OPOS        | MockOPOSDrawer1          |
    | Drawer2           | OPOS        | MockOPOSDrawers          |
    | Skanner           | OPOS        | MockOPOSScanner          |
    | Skaler             | OPOS        | MockOPOSScale            |
    | PIN-kodetastatur           | OPOS        | MockOPOSPinPad           |
    | Signaturregistrering | OPOS        | MockOPOSSignatureCapture |

**Obs!** Det kreves ikke et bestemt oppsett i maskinvareprofilen for å simulere hendelser for tastaturkortleser fra strekkodeskanner og kortleser.

### <a name="assign-the-hardware-profile-to-a-register"></a>Tilordne maskinvareprofilen til en kasse

1.  Når maskinvareprofilen er opprettet, kan du gå til **Detaljhandel og handel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Kasser**.
2.  I listen **Kasser på salgssted** klikker du på koblingen i feltet **Kassenummer** for kassen som skal bruke simulatoren for eksterne enheter.
3.  Klikk **Rediger**.
4.  I delen **Profiler** i feltet **Maskinvareprofil**, velger du maskinvareprofilen du opprettet for virtuelle eksterne enheter.
5.  Klikk på **Lagre**.

### <a name="synchronize-changes-to-the-channel-database"></a>Synkronisere endringer til kanaldatabasen

1.  Gå til **Detaljhandel og handel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplan**.
2.  Velg distribusjonsplanen **1090**.
3.  Klikk på **Kjør nå** for å synkronisere endringer til salgsstedet.

Når dataene er synkronisert, er den nye maskinvareprofilen og endringene for kassen tilgjengelige i kanaldatabasen.

## <a name="install-the-peripheral-simulator"></a>Installere simulatoren for eksterne enheter
1.  Gå til **Detaljhandel og handel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofiler** &gt; **Maskinvareprofiler**.
2.  Klikk på **Last ned**, og klikk deretter på **PeripheralSimulator**. **Obs!** Du må deaktivere popup-blokkeringer før du kan laste ned simulatoren for eksterne enheter.
3.  Når nedlastingen er fullført, kan du åpne mappen **Nedlastinger** og dobbeltklikke på **VirtualPeripherals.msi** for å starte installasjonsprogrammet.
4.  Installer simulatoren for eksterne enheter ved hjelp av standardinnstillingene.

I tillegg til simulatoren for eksterne enheter må du installere Common Control Objects fra Monroe Consulting Services. Hvis ikke, vil ikke simulatoren for eksterne enheter fungere slik den skal. Hvis du vil laste ned de Common Control Objects, kan du gå til <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Bruke simulatoren for eksterne enheter
Hvis du vil starte simulatoren for eksterne enheter, klikker du på **Start** på datamaskinen, skriver inn **Simulator for eksterne enheter**, og deretter velger du programmet når det vises i søkeresultatene. Når du starter simulatoren for eksterne enheter, klikker du på et enhetsnavn for å se enheter som støttes. Disse enhetene vises som kategorier til venstre i vinduet. Hvis du vil vise en bestemt enhet, klikker du på kategorien for enheten.

### <a name="line-display-capabilities"></a>Linjevisningsfunksjoner

Linjevisningsenhet er den første enheten som vises i simulatoren for eksterne enheter. Når den virtuelle linjevisningsenheten er konfigurert, viser den linjeelementer når de skannes i transaksjonen på salgsstedet. I tillegg til linjeelementer viser totalsummen når et betalingsmiddel er valgt på salgsstedet. Den viser også saldoen hvis det angis et betalingsmiddel, men en saldo fortsatt gjenstår for transaksjonen. Når salgsstedet ikke brukes, kan en melding vises for å angi at kassen er lukket. Du må konfigurere meldingen i hurtigfanen **Linjevisning** i maskinvareprofilen.

### <a name="cash-drawer-capabilities"></a>Kassaskuffunksjoner

Kassaskuffen er den andre enheten som vises i simulatoren for eksterne enheter. Når maskinvareprofilen er konfigurert til å bruke virtuelle kassaskuffer, åpner salgsstedet kassaskuffen for det aktive skiftet som svar på skuffeoperasjoner, for eksempel deklarasjon av betalingsmiddel, slik at kassereren kan veksle eller sette inn kontanter under standard kontanttransaksjoner. De virtuelle kassaskuffene har etikettene **Hovedskuff** og **Andre skuff**. Disse etikettene representerer henholdsvis skuff og skuff 2 i maskinvareprofilen. Når en skuff er lukket, vises et bilde av en lukket kassaskuff, og knappen på den lukkede kassaskuffen er merket **Åpne skuff**. Hvis du klikker på denne knappen, erstattes bildet av et bilde av en åpen kassaskuff for å angi at skuffen er nå åpen. Knappen på den åpne kassaskuffen er merket **Lukk skuff**. Flere operasjoner på salgsstedet kan føre til at kassaskuffen åpnes. De fleste operasjoner kan ikke fortsette mens kassaskuffen er åpen. Unntakene er noen prosedyrer for sluttoppgjør. Hvis salgsstedsbrukeren får en feilmelding som sier at en operasjon ikke kan utføres mens kassaskuffen er åpen, må brukeren lukker den virtuelle eller fysiske kassaskuffen for å fortsette. Hvis en kassaskuff er merket som **Delt** i maskinvareprofilen, kontrollerer ikke systemet at skuffen er lukket før en operasjon. Operasjonen fortsetter på vanlig måte, selv om kassaskuffen er åpen. Denne virkemåten støtter scenarier der pengeskuffer er delt mellom selgere, og der én selger bruker en kassaskuff mens en annen selger utfører ubeslektede oppgaver på sin egen salgsstedsenhet. Endringer som gjøres i kassaskuffen, ikke tydelige før gjeldende skiftet avsluttes og et nytt skift starter.

### <a name="msr-capabilities"></a>Kortleserfunksjoner

Simulatoren for eksterne enheter har robust støtte for virtuelle kortleseroperasjoner ved å arbeide i OPOS-modus eller tastaturkortlesermodus. OPOS-modus krever at kortleseren konfigureres i maskinvareprofilen til å fungere som en OPOS-enhet. Tastaturkortlesermodus sender bare datahendelser for tastaturkortleser til Microsoft Windows. I tillegg til forskjeller i oppsettet, er OPOS-modus og tastaturkortlesermodus forskjellige på følgende måter:

-   POS-klient aktiverer OPOS-kortleserenheter for bestemte scenarier, for eksempel scenarier som tillater magnetstripedata for registrering av fordel eller gavekort.
-   I tastaturkortlesermodus sender simulatoren for eksterne enheter data til feltet som er aktivt når dataene sendes. Denne virkemåten ligner på virkemåten som oppstår hvis dataene angis ved hjelp av et tastatur For å bruke kortleseren som tastaturkortleser må brukeren bytte til moderne salgssted for detaljhandel for å sikre at dataene mottas i riktig felt. Derfor kan du konfigurere en forsinkelse, slik at brukeren har tid til å sikre at dataene sendes til riktig felt.

#### <a name="testing-gift-and-payment-card-swipes"></a>Teste registrering av gave- og betalingskort

Den virtuelle kortleseren som simulatoren for eksterne enheter inneholder, lar deg konfigurere bestemte kortleserdata for å teste scenarier for registrering av gave- og betalingskort. Hvis du vil opprette et kort, klikker du på plusstegnet (**+**) og velger korttype. Deretter angir du kortnummeret eller sporingsdataene som skal sendes til salgsstedet, sammen med utløpsmåned og -år for kortet du definerer. Verdien du velger i feltet **Korttype** er bare en etikett som kan tilordnes til et kort. Denne etiketten gjør det enklere å identifisere kort når de registreres i simulatoren for eksterne enheter. Du kan velge kort som er konfigurert i simulatoren for eksterne enheter ved hjelp av pil venstre (**&lt;**) og pil høyre (**&gt;**) over bildet av kortet. Du kan redigere og slette kort ved hjelp av knappene **Rediger** og **Slett** ved siden av plusstegnet (**+**).

### <a name="pin-pad"></a>PIN-kodetastatur

Du kan konfigurere simulator for PIN-kodetastatur for å simulere er OPOS-PIN-kodetastatur. Når en elektronisk pengeoverføring (EFT) utføres på salgsstedet, og salgsstedet krever registrering av PIN-kode, kaller maskinvarestasjonen PIN-enheten for å be om registrering av PIN-kode. PIN-kodetastaturet i simulatoren for eksterne enheter krever støtte for tilkobling for EFT-betaling for å fungere.

### <a name="printer"></a>Skriver

Den virtuell eksterne skriveren viser bare kvitteringer slik skrives ut fra salgsstedet. Hvis en utskriftsoperasjon produserer flere kvitteringer, kan du bla gjennom kvitteringene.

#### <a name="configure-receipt-printing"></a>Konfigurere kvitteringsutskrift

1.  Gå til **Detaljhandel og handel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofiler** &gt; **Maskinvareprofiler**.
2.  Velg maskinvareprofilen du opprettet for virtuelle enheter.
3.  Klikk på **Rediger** i hurtigfanen **Skriver**.
4.  Velg en kvitteringsprofil i feltet **Kvitteringsprofil-ID**.
5.  Klikk på **Lagre**.

### <a name="scale"></a>Skaler

Når et vektprodukt legges til salgsstedstransaksjonen, og en vekt er konfigurert, henter salgsstedet vekten fra vekten. For både den virtuelle og fysiske vekten må produktet eller vekten angis før produktet legges til i transaksjonen. Før du legger til vektproduktet i transaksjonen, går du til vekten i simulatoren for eksterne enheter og bruke plusstegnet (**+**) og minustegnet (**–**) for å justere vekten som vekten skal rapportere. Du kan også angi ønsket vekt direkte i feltet **Gjeldende verdi**. Du kan justere vektenhetene for vektene ved hjelp av plusstegnet (**+**), **Rediger**, og **Slett**. På denne måten kan enheter angis basert på produktene som veies, eller de nasjonale innstillingene for stedet der vekten brukes.

#### <a name="configure-a-scale-product"></a>Konfigurere et vektprodukt

1.  Gå til **Detaljhandel og** **handel** &gt; **Produkter og kategorier** &gt; **Utgitte produkter etter kategori**.
2.  Åpne produktposten.
3.  Velg produktet som skal veies.
4.  På hurtigfanen **Detaljhandel** endrer du alternativet **Vektprodukt** fra **Nei** til **Ja**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Synkronisere endringer til kanaldatabasen

1.  Gå til **Detaljhandel og handel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplan**.
2.  Velg distribusjonsplanen **1040**.
3.  Klikk på **Kjør nå** for å synkronisere endringer til salgsstedet.

Når et vektprodukt legges til salgsstedstransaksjonen etter at dataene er synkroniserte, kontrollerer salgsstedet vekten for vekten.

### <a name="signature-capture"></a>Signaturregistrering

Den virtuelle enheten for registrering av signatur ber brukeren om å angi en signatur på den virtuelle signaturregistreringsplaten når betalingsmiddelet som brukes, krever en signatur. Brukeren kan godta signaturen for å vise den på salgsstedet. Kassereren kan deretter godta signaturen. Signaturen lagres deretter sammen med betalingsmiddelet og synkroniseres med underkontoen sammen med andre transaksjonsdata.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Definer et betalingsmiddel for å kreve en signatur

1.  Gå til **Detaljhandel og handel** &gt; **Kanaler** &gt; **Detaljhandelsbutikker** &gt; **Alle detaljhandelsbutikker**.
2.  Velg detaljhandel.
3.  Klikk **Rediger**.
4.  Klikk på **Oppsett**, og gå deretter til **Oppsett**-delen og klikk på **Betalingsmåter**.
5.  Klikk **Rediger**.
6.  Velg betalingsmåten som krever en signatur.
7.  I **Generelt**-delen under **Signaturregistrering**, setter du alternativet **Bruk registreringsenhet for signatur** til **Ja**.
8.  I feltet **Minimumsbeløp for signaturregistrering** angir du minimumsbeløpet som skal utløse signaturregistrering.

#### <a name="synchronize-changes-to-the-channel-database"></a>Synkronisere endringer til kanaldatabasen

1.  Gå til **Detaljhandel og handel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplan**.
2.  Velg distribusjonsplanen **1070**.
3.  Klikk på **Kjør nå** for å synkronisere endringer til salgsstedet.

Når dataene er synkroniserte og det brukes et betalingsmiddel som krever en signatur, og beløpet oppfyller signaturterskelen, ber salgsstedet om en signatur på den virtuelle enheten for registrering av signatur.

## <a name="additional-configuration"></a>Tilleggskonfigurasjon
Du kan redigere konfigurasjonsfilen for simulatoren for eksterne enheter for å håndtere testscenarier på en passende måte. Du finner konfigurasjonsfilen i C:\\Programfiler (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Konfigurasjonsfilen definerer enhetene som er tilgjengelige for testing på vekten, korttypene som er tilgjengelige for testing og strekkodetypene. Ved for eksempel å endre tekstverdier i konfigurasjonsfilen, du kan legge til en ny korttype eller måleenhet som kan velges ved kjøretid. De nye verdiene vises når programmet startes på nytt.

## <a name="troubleshooting"></a>Feilsøking
Aktivitetene logges i simulatoren for eksterne enheter. Du finner loggen i C:\\Programfiler (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Simulatoren for eksterne enheter rapporterer også problemer til hendelsesloggen i Windows, som du får tilgang til i **Program- og tjenestelogger** &gt; **Microsoft** &gt; **DynamicsAX**. Hvis endringer du har gjort i maskinvareprofilen eller på andre områder, ikke er vises når du bruker MPOS eller simulatoren for eksterne enheter, kan du se planleggerjobbene for distribusjon som du brukte for å synkronisere dataene til databaskanalen. Hvis endringene ble synkronisert, men fremdeles ikke vises på salgsstedet, starter du salgsstedsklienten på nytt. Endringer i konfigurerte kassaskuffer tas ikke i bruk før det opprettes et nytt skift. Hvis du gjør endringer for kassaskuffer, må du kontrollere at du alltid lukker eksisterende skift for å teste det nye oppsettet for kassaskuffen. Hvis en produsentdriver installeres etter Common Control Objects fra Monroe Consulting Services, kan driveren noen ganger føre til at Common Control Objects slutter å fungere slik det skal. I slike tilfeller må du installere Common Control Objects på nytt.

<a name="see-also"></a>Se også
--------

[Oversikt over detaljhandelsenheter](retail-peripherals-overview.md)





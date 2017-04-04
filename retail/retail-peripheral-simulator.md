---
title: Detaljhandel eksterne simulator
description: "Dette emnet beskriver eksterne simulator-verktøyet som følger med Microsoft Dynamics 365 for operasjoner - detaljhandel."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 42dc414ff2bb6359b47d89c3bd3c510e4258f816
ms.openlocfilehash: b2229466040351d8c2b9494b30b4c928651820b8
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripheral-simulator"></a>Detaljhandel eksterne simulator

Dette emnet beskriver eksterne simulator-verktøyet som følger med Microsoft Dynamics 365 for operasjoner - detaljhandel.

<a name="overview"></a>Oversikt
--------

Microsoft Dynamics-365 for operasjoner - Retail eksterne simulator er et verktøy som hjelper deg med å konfigurere, teste og feilsøke eksterne enheter som brukes i miljøer med retail. Du kan bruke eksterne simulator å strømlinjeforme testing av retail Tilbehør, og til å isolere problemer som er forårsaket av feil oppsett eller den fungerer feil enhetsdrivere. Eksterne simulator inkluderer en desktop program som har virtuelle versjoner av enheter som Dynamics 365 for operasjoner - støtte for detaljhandel. En inndeling for hver enhet viser kommunikasjon mellom enheten og detaljhandel poenget med salg (POS). Du kan også bruke den til å legge inn data som er gyldig for ulike POS-scenarier. Eksterne simulator støtter kommunikasjon mellom Salgsstedet og følgende virtuelle enheter:

-   **Skriver** – peripheral simulator kan vise mottak som er konfigurert for en POS-skriver.
-   **Linjen viser** – du kan konfigurere en virtuell linjen skjermen for å vise aktivitet på et fysisk linjevisningen.
-   **Kortleser (MSR)** – du kan sende simulerte Magnetstripen hendelser til Salgsstedet fra eksterne simulator.
-   **Skuffen** – du kan simulere en fysisk kassaskuff.
-   **Skuff 2** – ved å sette opp en andre kassaskuff i eksterne simulator, kan du simulere scenarier som involverer en enkelt POS-kasse som har to aktive SKIFT.
-   **Skanner** – den virtuelle strekkodeskanner som støtter eksterne simulator kan utstede strekkode skanning hendelser.
-   **Skala** – en virtuell skala kan du simulere interaksjon med veide elementer med Salgsstedet.
-   **Personlig ID Tallblokk (PIN)** – du kan simulere PIN pad operasjoner. **Merk:** må du implementere støtte for en fysisk PIN-pad via betalingskoblingen.
-   **Signaturregistrering** – peripheral simulator inkluderer en registreringsenhet for virtuelle signatur som du kan sette opp til å be om signaturer som kreves for enkelte anbud, for eksempel kundebetalinger.

Du kan også bruke eksterne simulator for å simulere kant tastaturhendelser som kommer fra en strekkodeskanner og MSR. Den virtuelle eksterne simulator støtter spesielt objektkobling og -innebygging for Retail POS (OPOS)-enheter.

## <a name="key-scenarios"></a>Viktige scenarier
### <a name="troubleshooting"></a>Feilsøking

Du kan bruke eksterne simulator du feilsøker installasjonsprogrammet for enheten. Hvis du ikke har den eksterne simulator eller en annen enhet i samme klasse, kan det være vanskelig å finne der problemer stammer fra. Når du har eksterne simulator, kan du imidlertid konfigurere virtuelle enheter og kjøre samme kodebaner og forretningslogikk som brukes for fysiske enheter. Fra perspektivet til den eksterne simulator er den viktigste forskjellen mellom virtuelle enheter og fysiske enheter serviceobjekt eller enhetsdriver. Serviceobjektet er levert av enhetsprodusenten for fysiske enheter. Derimot for den eksterne simulator var serviceobjektene en del av den eksterne simulator. Når den eksterne simulator fungerer som den skal, hvis en enhet ikke fungerer på riktig måte etter at navnet på enheten i gjeldende maskinvareprofil endres til navnet på en virkelig enhet, kan du anta at det er et problem med serviceobjektet som leveres av produsenten.

### <a name="training"></a>Kurs

Du kan bruke eksterne simulator å legge til en realistisk laget for å kasserers opplæring når et oppsett for fysisk maskinvare er ikke tilgjengelig. Når den eksterne simulator er inkludert i opplæringen scenarier, vil mer effektivt kassereren kan samhandle med Salgsstedet ved å oppgi inndata for eksempel produkt kode skanninger og gave kort swipes og observere hvilke mottak som skrives ut for en bestemt transaksjon.

### <a name="testing"></a>Testing

Du kan bruke eksterne simulator for å teste produktstrekkoder, mottak formater og så videre, uten å måtte distribuere fysisk maskinvare i et virtuelt miljø. Fordi fysisk maskinvare som ikke er nødvendig, og du trenger ikke å distribuere en POS-klient på en maskinvare-stasjon eller en fysisk datamaskin, kan du raskt teste endringer som gjøres i back-office.

## <a name="set-up-the-peripheral-simulator"></a>Definer eksterne simulator
### <a name="set-up-a-hardware-profile"></a>Sette opp en maskinvareprofil

1.  Hvis du vil konfigurere den eksterne simulator, kan du gå til **Retail og commerce**&gt;**kanaloppsett**&gt;**POS installasjonsprogrammet**&gt;**POS profiler**&gt;**maskinvareprofiler**.
2.  Klikk for å opprette en ny profil, **ny**.
3.  Angi verdier i de **profil nummer** og **beskrivelse** felt.
4.  Bruk tabellen nedenfor til å definere de virtuelle enhetene som må testes. Her er en forklaring på kolonnene i tabellen:
    -   **Enheten** – denne kolonnen inneholder navnet på hurtigfanen du utvide for å konfigurere enheten.
    -   **Enhetstypen** – denne kolonnen viser verdien som du velger i feltet som er merket med navnet på enheten.
    -   **Enhetsnavn** – denne kolonnen gir den nøyaktige verdien du angir for enhetsnavnet. **Viktig:** enhetsnavn som er gitt her er nødvendig, fordi maskinvare-stasjonen bruker disse spesifikke navn for å løse enheter. Hvis du ikke bruker disse spesifikke navn, vil ikke enheten kan brukes.

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

**Merk:** kreves ikke bestemt oppsett i maskinvareprofilen profil til å simulere tastaturhendelser kant fra strekkodeskanner og MSR.

### <a name="assign-the-hardware-profile-to-a-register"></a>Tilordne maskinvareprofilen til en journal

1.  Når maskinvareprofilen er opprettet, kan du gå til **Retail og commerce**&gt;**kanaloppsett**&gt;**POS installasjonsprogrammet**&gt;**registrerer**.
2.  I den **POS-kasser**, klikker du koblingen i den **registernummer** felt for journalen som skal bruke den eksterne simulator.
3.  Klikk **Rediger**.
4.  I den **profiler** -delen i den **maskinvareprofil** velger maskinvareprofilen du opprettet for virtuelle enheter.
5.  Click **Save**.

### <a name="synchronize-changes-to-the-channel-database"></a>Synkronisere endringer i databasen for kanal

1.  Gå til **Retail og commerce**&gt;**Retail IT**&gt;**distribusjonsplan**.
2.  Velg den **1090** distribusjonsplan.
3.  Klikk **kjører nå** å synkronisere endringer på Salgsstedet.

Etter at dataene er synkronisert, er ny maskinvareprofil og endringer i journalen tilgjengelige i kanal-databasen.

## <a name="install-the-peripheral-simulator"></a>Installere ekstern simulator
1.  Gå til **Retail og commerce**&gt;**kanaloppsett**&gt;**installasjonsprogrammet for POS**&gt;**POS profiler**&gt;**maskinvareprofiler**.
2.  Klikk **Last ned**, og klikk deretter **PeripheralSimulator**. **Merk:** du må slå av Popup-blokkeringer før du kan laste ned eksterne simulator.
3.  Når nedlastingen er fullført, kan du åpne den **nedlastinger** -mappen, og dobbeltklikk **VirtualPeripherals.msi** til å starte installasjonsprogrammet.
4.  Installere ekstern simulator ved hjelp av standardinnstillingene.

I tillegg til eksterne simulator, må du installere de vanlige kontrollen objektene fra Monroe konsulenttjenester. Hvis ikke, eksterne simulator fungerer ikke på riktig måte. Hvis du vil laste ned de vanlige kontroll-objektene, kan du gå til <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Ved hjelp av eksterne simulator
Klikk for å starte den eksterne simulator, **Start** på datamaskinen, skriver du inn **Retail eksterne simulator**, og velg deretter programmet når det vises i søkeresultatene. Når du starter den eksterne simulator, klikker du navnet på en enhet for å se støttede enheter. Disse enhetene vises som kategorier på venstre side av vinduet. Hvis du vil vise en bestemt enhet, klikker du kategorien for enheten.

### <a name="line-display-capabilities"></a>Linjen visningsmulighetene

Linjevisningen er den første enheten som er oppført i den eksterne simulator. Når virtual linjevisningen er konfigurert, viser linjeelementer som de blir skannet i POS-transaksjonen. I tillegg til linjeelementer viser totalsummen som er forfalt når et betalingsmiddel er valgt på Salgsstedet. Den viser også saldoen som forfaller Hvis registreres som et betalingsmiddel, men en balanse er fortsatt forfallsdatoen for transaksjonen. Når Salgsstedet ikke brukes, kan en melding vises for å angi at kasseapparatet er lukket. Du må konfigurere meldingen på den **linje skjerm** hurtigfanen i maskinvareprofilen.

### <a name="cash-drawer-capabilities"></a>Muligheter for kontanter skuff

Kassaskuffen er den andre enheten som er oppført i den eksterne simulator. Når maskinvareprofilen er konfigurert til å bruke virtuelle kontanter skuffer, åpnes Salgsstedet kassaskuff for aktive forskyvningen som svar på skuffen operasjoner som betalingsmiddel deklarasjoner, og slik at kassereren kan endre eller sette inn kontanter under standard cash-and-carry transaksjoner. De virtuelle pengeskuff har etiketter **hoved skuffen** og **sekundære skuffen**. Disse etikettene representerer skuffen og skuff 2 i maskinvareprofilen, henholdsvis. Når en skuffen er lukket, vises et bilde av en lukket kassaskuff og knappen på lukkede kassaskuff heter **Åpne skuff**. Hvis du klikker denne knappen, er bildet erstattet med et bilde av en åpen kassaskuff for å angi at skuffen er nå åpen. Knappen på den åpne kassaskuffen heter **Lukk skuffen**. Flere operasjoner på Salgsstedet kan forårsake kassaskuff å åpne. De fleste operasjoner kan ikke fortsette mens kassaskuffen er åpen. Unntakene er noen prosedyrer på slutten av dagen. Hvis POS-brukeren mottar en feilmelding som sier at en operasjon ikke kan utføres mens kassaskuffen er åpen, må brukeren lukker virtuelle eller fysiske kassaskuff Hvis du vil fortsette. Hvis en kassaskuff er merket som **delte** i maskinvareprofilen, ikke systemet Kontroller at skuffen er lukket før en operasjon. Operasjonen fortsetter på vanlig måte, selv om kassaskuffen er åpen. Dette støtter scenarier der pengeskuff er delt mellom selgere, og der én knytte bruker en kassaskuff mens en annen Knytt utfører ubeslektede aktiviteter på sin egen POS-enheten. Endringer som gjøres i kassaskuffen ikke tydelig før gjeldende skiftet lukkes og åpnes et nytt SKIFT.

### <a name="msr-capabilities"></a>MSR-funksjoner

Eksterne simulator gir robust støtte for virtuelle MSR-operasjoner ved å arbeide i OPOS-modus eller tastaturmodus kant. OPOS-modus krever at Kortleser konfigureres i maskinvareprofilen profil kan fungere som en OPOS-enhet. Kant tastaturmodus sender bare tastaturhendelser kant data til Microsoft Windows. I tillegg til forskjeller i oppsettet, OPOS og tastatur kant modi er forskjellige på følgende måter:

-   POS-klient kan OPOS MSR enheter for bestemte scenarier, for eksempel scenarier som tillater Magnetstripen data for lojalitet eller gave kort post.
-   I kant tastaturmodus, eksterne simulator tastatur kant dataene sendes til feltet som er aktiv når dataene er sendt. Dette ligner på problemet som oppstår hvis det er angitt data ved hjelp av et tastatur. Hvis du vil bruke Kortleser som en kant på tastaturet, må brukeren bytte til detaljhandel moderne POS (MPOS) å forsikre deg om at data er mottatt i riktig felt. Derfor kan du konfigurere en forsinkelse, slik at brukeren har tid til å sikre at dataene sendes til riktig felt.

#### <a name="testing-gift-and-payment-card-swipes"></a>Testing av gave- og kort swipes

Den virtuelle MSR eksterne simulator gir også lar deg konfigurere bestemte MSR-data for å teste scenarier for gave- og kort swipes. Hvis du vil opprette et kort, klikker du plusstegnet (**+**), og velger hvilken type kort. Deretter angir du hvor kort eller spore data som skal sendes til POS, sammen med utløpsdato for måneden og året for kort som du definerer. Verdien du velger i den **Type kort** -feltet er bare en etikett som kan tilordnes til et kort. Denne etiketten gjør det enklere å identifisere kort når de er lest gjennom eksterne simulator. Du kan velge kort som er konfigurert i eksterne simulator ved hjelp av venstrepilen (**&lt;**) og høyrepilen (**&gt;**) knappene over bildet på kortet. Du kan redigere og slette kort ved hjelp av den **Rediger** og **sletter** knapper ved siden av plusstegnet (**+**) knappen.

### <a name="pin-pad"></a>PIN-kodetastatur

Du kan konfigurere simulator for PIN-pad for å simulere en OPOS-PIN-pad. Når en elektronisk pengeoverføring lageroverføringstransaksjonen (EFT) utføres på Salgsstedet, og krever PIN-kodeoppføringen, kaller stasjonen maskinvare PIN-enheten til å be om PIN-kodeoppføringen. Hvis du vil arbeide, krever PIN-blokken i eksterne simulator EFT betaling connector støtte.

### <a name="printer"></a>Skriver

Virtuell eksterne skriveren viser bare mottak slik de er skrevet ut fra Salgsstedet. Hvis en utskriftsoperasjonen produserer flere mottak, kan du Bla gjennom kvitteringene.

#### <a name="configure-receipt-printing"></a>Konfigurere Kvitteringsutskrift

1.  Gå til **Retail og commerce**&gt;**kanaloppsett**&gt;**installasjonsprogrammet for POS**&gt;**POS profiler**&gt;**maskinvareprofiler**.
2.  Velg maskinvareprofilen du opprettet for virtuelle enheter.
3.  På den **skriver** hurtigfanen, klikker du **Rediger**.
4.  I den **mottak profil-ID** velger en profil for mottak.
5.  Click **Save**.

### <a name="scale"></a>Skaler

Når et produkt skala legges til POS-transaksjonen, og en skala er konfigurert, henter Salgsstedet vekten fra skalaen. For både virtuelle og fysiske skalaen, må produktet eller vekt angis før produktet er lagt til transaksjonen. Før du legger til produktet skala transaksjonen, gå til skala i eksterne simulator, og bruk plusstegnet (**+**) og minustegn (**–**)-knappene for å justere vekt som skalaen rapporterer. Du kan også angi ønsket vekt direkte i den **gjeldende verdi** feltet. Du kan justere enheter av vekt for skala ved hjelp av plusstegnet (**+**), **Rediger**, og **sletter** knapper. På denne måten kan enheter angis basert på produktene som er vektet eller nasjonale der skalaen brukes.

#### <a name="configure-a-scale-product"></a>Konfigurere en skala-produktet

1.  Gå til **Retail og****commerce**&gt;**-produkter og -kategorier**&gt;**utgitt produkter av kategori**.
2.  Åpne oppføringen for produktet.
3.  Velg produktet til veie.
4.  På den **Retail** hurtigfanen satt til **skala produktet** alternativ fra **Nei** til **Ja**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Synkronisere endringer i databasen for kanal

1.  Gå til **Retail og commerce**&gt;**Retail IT**&gt;**distribusjonsplan**.
2.  Velg den **1040** distribusjonsplan.
3.  Klikk **kjører nå** å synkronisere endringer på Salgsstedet.

Når dataene er synkronisert, når et produkt skala legges til POS-transaksjon, kontrollerer Salgsstedet skala for vekten.

### <a name="signature-capture"></a>Signaturregistrering

Registreringsenhet for virtuelle signatur ber brukeren om å oppgi en signatur i virtuelle signatur opptak pad når betalingsmiddel som krever en signatur. Brukeren kan godta signatur for å vise den på Salgsstedet. Kassereren kan deretter godta signaturen. Signaturen er deretter lagret sammen med betalingsmiddelet og synkroniseres med back office sammen med andre transaksjonsdata.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Definer et betalingsmiddel for å kreve en signatur

1.  Gå til **Retail og commerce**&gt;**kanaler**&gt;**forretninger**&gt;**alle forretninger**.
2.  Velg forhandler.
3.  Klikk **Rediger**.
4.  Klikk **satt opp**, og deretter, i den **satt opp** -delen, klikker du **betalingsmåter**.
5.  Klikk **Rediger**.
6.  Velg betalingsmetode som krever en signatur.
7.  I den **Generelt** -delen under **signatur fange opp**, angis den **Bruk registreringsenhet for signatur** å **Ja**.
8.  I den **signatur opptak minimumsbeløpet** angir det minste beløpet som skal utløse opptak av signaturen.

#### <a name="synchronize-changes-to-the-channel-database"></a>Synkronisere endringer i databasen for kanal

1.  Gå til **Retail og commerce**&gt;**Retail IT**&gt;**distribusjonsplan**.
2.  Velg den **1070** distribusjonsplan.
3.  Klikk **kjører nå** å synkronisere endringer på Salgsstedet.

Etter at dataene er synkronisert, brukes et betalingsmiddel som krever en signatur, og beløpet oppfyller signatur terskelen, ber Salgsstedet om en signatur på registreringsenhet for virtuelle signatur.

## <a name="additional-configuration"></a>Ytterligere konfigurasjon
Du kan redigere det eksterne simulator konfigurasjonsfil for å løse mer passende scenarier som du tester. Du kan finne konfigurasjonsfilen på C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Konfigurasjonsfilen definerer enhetene som er tilgjengelige for testing på skalaen, korttyper som er tilgjengelige for testing og strekkodetyper. For eksempel ved å endre tekstverdier i konfigurasjonsfilen, du kan legge til en ny korttype eller enheten som kan velges ved kjøretid. De nye verdiene vises når programmet er startet på nytt.

## <a name="troubleshooting"></a>Feilsøking
Aktiviteter for eksterne simulator logges i eksterne simulator. Du kan finne loggen på C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Eksterne simulator rapporterer også problemer til hendelsesloggen i Windows, som du får tilgang til på **program- og tjenestelogger**&gt;**Microsoft**&gt;**DynamicsAX**. Hvis endringer du har gjort i maskinvareprofilen eller andre områder ikke er tydelig når du bruker MPOS eller eksterne simulator, kan du se fordelingen Oppgaveplanlegging-jobber som du brukte til å synkronisere dataene til databasen kanal. Hvis endringene ble synkronisert, men fremdeles ikke er tydelig på Salgsstedet, Start POS-klienten på nytt. Endringer i konfigurerte kontanter skuffer ikke effektive før det opprettes et nytt SKIFT. Hvis du gjør endringer i kontanter skuffer, Sørg derfor at du alltid lukke eksisterende SKIFT for å teste det nye oppsettet for kontanter skuffen. Noen ganger, hvis en produsent er installert etter vanlige kontroll objektene fra Monroe konsulenttjenester, driveren kan føre til felles kontroll objektene slutter å fungere på riktig måte. I dette tilfellet bør du installere vanlige kontroll-objekter.

<a name="see-also"></a>Se også
--------

[Retail peripherals overview](retail-peripherals-overview.md)



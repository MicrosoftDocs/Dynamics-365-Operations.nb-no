---
title: "Oversikt over Retail-Tilbehør"
description: "Dette emnet forklarer konseptene som er knyttet til detaljhandel enheter. Den beskriver ulike måter tilbehør kan kobles til punktet for salg (POS) og komponentene som er ansvarlig for å administrere tilkoblingen til Salgsstedet."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 268444
ms.assetid: 2ea93e43-8019-49a0-a7f8-325565ebc52d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 79a43c35691f16d773b88faad63c4ab79cb93f1f
ms.openlocfilehash: c6fb3922ba2c4b15f1043d0bcbac40ff2da9a469
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripherals-overview"></a>Oversikt over Retail-Tilbehør

Dette emnet forklarer konseptene som er knyttet til detaljhandel enheter. Den beskriver ulike måter tilbehør kan kobles til punktet for salg (POS) og komponentene som er ansvarlig for å administrere tilkoblingen til Salgsstedet.

<a name="concepts"></a>Begreper
--------

### <a name="pos-registers"></a>Kasser på salgssted

Navigasjon: Velg **Retail og commerce**&gt;**kanaloppsett**&gt;**POS installasjonsprogrammet**&gt;**registrerer**. Poenget med salg (POS) register er en enhet som brukes til å definere egenskapene til en bestemt forekomst av Salgsstedet. Disse egenskapene inkluderer maskinvareprofil eller oppsettet for retail-enheter som skal brukes i journalen lager som er tilordnet journalen og den visuelle opplevelsen for brukeren som logger på denne kassen.

### <a name="devices"></a>Enheter

Navigasjon: Velg **Retail og commerce**&gt;**kanaloppsett**&gt;**POS installasjonsprogrammet**&gt;**enheter**. En enhet er en enhet som representerer en fysisk forekomst av en enhet som er tilordnet en kasse på salgsstedet. Når en enhet er opprettet, tilordnes den til en POS kassen. Enhetsenheten registrerer informasjon om når en kasse på salgsstedet aktiveres, klienttypen som brukes og programpakken som er distribuert til en bestemt enhet. Enheter som kan tilordnes til følgende programtyper: moderne Kvitteringen, sky Kvitteringen, moderne Priskontroll – Windows Phone, moderne Priskontroll – Android og moderne Priskontroll – iOS.

### <a name="retail-modern-pos"></a>Retail Modern POS

Moderne POS er POS-programmet for Microsoft Windows. Den kan distribueres på 10 for Windows-operativsystemer (OSs).

### <a name="cloud-pos"></a>Skybasert salgssted

Sky POS er en Web-basert versjon av moderne POS-program som kan åpnes i en webleser.

### <a name="modern-pos-for-ios"></a>Moderne POS for iOS

Moderne POS for iOS er en iOS-basert versjon av moderne POS-program som kan distribueres på iOS enheter.

### <a name="modern-pos-for-android"></a>Moderne POS for Android

Moderne POS for Android er en Android-basert versjon av moderne POS-program som kan distribueres på Android-enheter.

### <a name="pos-peripherals"></a>POS-tilbehør

POS-enheter er enheter som er eksplisitt støttet for POS-funksjoner. Disse eksterne enheter deles vanligvis inn i bestemte klasser. Hvis du vil ha mer informasjon om disse klassene, kan du se delen "Enhetsklassene" i dette emnet.

### <a name="hardware-station"></a>Maskinvarestasjon

Navigasjon: Velg **Retail og commerce**&gt;**kanaler**&gt;**forretninger**&gt;**alle forretninger**. Velg en butikk, og klikk deretter hurtigfanen **Maskinvarestasjoner**. Den **maskinvare station** er en innstilling på kanal-nivå som brukes til å definere forekomster der retail eksterne logikken skal distribueres. Denne innstillingen på nivå kanalen brukes til å bestemme karakteristikkene for stasjonen maskinvare. Det brukes også til listen maskinvare radiostasjoner som er tilgjengelige for en moderne POS-forekomst i et angitt lager. Maskinvare-stasjonen er bygget i moderne POS-programmet for Windows. Maskinvare-stasjon kan også distribueres uavhengig som et frittstående program for Microsoft Internet Information Services (IIS). I dette tilfellet kan det være tilgang til via et nettverk.

### <a name="hardware-profile"></a>Maskinvareprofil

Navigasjon: Velg **Retail og commerce**&gt;**kanaloppsett**&gt;**POS installasjonsprogrammet**&gt;**POS profiler**&gt;**maskinvareprofiler**. Maskinvareprofilen er en liste over enheter som er konfigurert for en POS-kasse eller en maskinvare-stasjon. Maskinvareprofilen kan tilordnes direkte til en POS-kasse eller en maskinvare-stasjon.

## <a name="devices-classes"></a>Klasser av enheter
POS-tilbehør er vanligvis delt inn i klasser. Denne delen beskriver, og gir en oversikt over enhetene som støtter moderne POS.

### <a name="printer"></a>Skriver

-Skrivere inkluderer tradisjonell POS mottak og helsides skrivere. Skriveren støttes gjennom Object Linking and Embedding for Retail POS (OPOS) og Microsoft Windows driver-grensesnitt. Opptil to skrivere kan brukes samtidig. Denne funksjonen støtter situasjoner der cash-and-carry Kundemottak skrives ut på skrivere for mottak, mens kundeordrer, som inneholder mer informasjon, skrives ut på en helsides skriver. Kvittering skrivere kan koblet direkte til en datamaskin via USB, koblet til et nettverk via Ethernet eller koblet via Bluetooth.

### <a name="scanner"></a>Skanner

Opptil to strekkode kan skannere brukes samtidig. Denne funksjonen støtter situasjoner der en skanner som er mer mobile er nødvendig for å skanne store eller tunge varer, mens en fast innebygd skanner brukes til de fleste elementer i standardformat, raskere betaling ganger. Skannere støttes gjennom OPOS, Universal Windows Platform (UWP) eller tastatur kant grensesnitt. USB eller Bluetooth kan brukes til å koble en skanner til en datamaskin.

### <a name="msr"></a>Kortleser

Én USB kortleser (MSR) kan settes opp ved hjelp av OPOS-drivere. Hvis du vil bruke en frittstående MSR for elektronisk pengeoverføring betalingstransaksjoner for overføring (EFT), må MSR styres av en betalingstilkobling. Frittstående MSRs kan brukes for kundeposten lojalitet, ansatt-påloggingen og gave kort oppføring, uavhengig av betalingskoblingen.

### <a name="cash-drawer"></a>Kassaskuff

To kontanter skuffer kan støttes per maskinvareprofilen. Denne funksjonen gjør det mulig for to aktive SKIFT per kasse skal være tilgjengelig på samme tid. Hvis det er en delt SKIFT, eller en kassaskuff som brukes av flere mobile enheter for POS samtidig, er bare én kassaskuff tillatt per maskinvareprofilen. Pengeskuff kan koblet direkte til en datamaskin via USB, koblet til et nettverk eller koblet til en kvitteringsskriver via et RJ12-grensesnitt. I noen tilfeller kan kan kontanter skuffer også kobles til via Bluetooth.

### <a name="line-display"></a>Linjevisning

Linjen viser brukes til å vise produkter, transaksjonen saldoer og annen nyttig informasjon til kunden under en transaksjon. Én linje skjerm kan være koblet til datamaskinen via USB ved hjelp av OPOS-drivere.

### <a name="signature-capture"></a>Signaturregistrering

Signatur fototekniske enheter kan kobles direkte til en datamaskin via USB ved hjelp av OPOS-drivere. Når signaturregistrering er konfigurert, kan kunden blir bedt om å logge på enheten. Etter at signaturen er angitt, vises det til kassereren for godkjenning.

### <a name="scale"></a>Skaler

Skalerer kan kobles til datamaskinen via USP ved hjelp av OPOS-drivere. Når et produkt som er merket som "Weighed" er lagt til en transaksjon, Salgsstedet leser vekten fra skalaen, legger til produktet i transaksjonen, og bruker antallet som er angitt av skalaen.

### <a name="pin-pad"></a>PIN-kodetastatur

Personlig ID-nummer (PIN) pads støttes gjennom OPOS, men de må administreres via en betalingstilkobling.

### <a name="secondary-display"></a>Sekundær skjerm

Når en sekundær skjerm er konfigurert, brukes nummer 2 Windows skjermen til å vise grunnleggende informasjon. Formålet med den sekundære skjermen er å støtte utvidelse for uavhengig programvare leverandør (ISV), fordi ut av boksen sekundær skjerm ikke kan konfigureres, og viser begrenset innhold.

### <a name="payment-device"></a>Betalingsenhet

Støtte for betaling-enheter er implementert via betalingskoblingen. Betaling enheter kan utføre én eller mange av funksjonene som gir andre klasser for enheten. For eksempel kan en betalingsenheten fungere som en MSR/kortleser, linjevisningen, registreringsenhet for signatur eller PIN-pad. Støtte for betaling enheter implementeres uavhengig av støtte for frittstående enheter som er tilgjengelig for andre enheter som er inkludert i maskinvareprofilen.

## <a name="supported-interfaces"></a>Støttede grensesnitt
### <a name="opos"></a>OPOS

For å garantere at den største utvalg av enheter kan brukes med Microsoft Dynamics 365 for operasjoner - detaljhandel, OLE for POS industristandard er den primære retail ekstern enhet som støttes i Microsoft Dynamics 365 for operasjoner - detaljhandel. OLE for POS-standarden ble produsert ved den National Retail Federation (NRF), som etablerer industristandard kommunikasjonsprotokoller for detaljhandel eksterne enheter. OPOS er en brukte implementering av OLE for POS-standarden. Den ble utviklet i mid-1990s, og har blitt oppdatert flere ganger siden da. OPOS gir en enhet driverarkitektur som gir enkel integrering av POS maskinvare med Windows – baserte POS-systemer. OPOS styrer håndtere kommunikasjon mellom kompatibel maskinvare og programvare, POS. En OPOS-kontroll består av to deler:

-   **Control-objekt** – control-objekt for en enhetsklasse (for eksempel viser) inneholder grensesnittet for programmet. Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) gir et standardisert sett med OPOS kontroll objekter som er kjent som felles kontroll-objekter (CCOs). I CCOs brukes til å teste POS-komponenten for Microsoft Dynamics-365 for operasjoner - handel. Derfor testing bidrar til å garantere at hvis Microsoft Dynamics 365 for operasjoner - Retail støtter en enhetsklassen gjennom OPOS, mange enhetstyper kan støttes, gitt at produsenten har et serviceobjekt som er bygd for OPOS. Du trenger ikke å eksplisitt teste hver enhetstype.
-   **Serviceobjektet** – serviceobjektet gir kommunikasjon mellom control-objekt (CCO) og enheten. Serviceobjektet for en enhet er vanligvis levert av produsenten av enheten. I noen tilfeller kan du imidlertid har laste ned serviceobjektet fra produsentens webområde. Et nyere serviceobjekt kan for eksempel være tilgjengelig. Hvis du vil finne adressen til produsentens webområde, kan du se i maskinvaredokumentasjonen.

[![Kontrollere objektet og serviceobjektet](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) støtte for OPOS-implementering av OLE for POS bidrar til å garantere at hvis enhetsprodusenter og POS utgivere implementerer standarden på riktig måte, POS-systemer og støttede enheter kan arbeide sammen, selv om de ikke var tidligere testet sammen. **Merk:** OPOS støtte garanterer ikke støtte for alle enheter som har OPOS-drivere. Microsoft Dynamics 365 for operasjoner - Retail må først støtte enhetstype, eller til og med OPOS-klassen. I tillegg kanskje serviceobjekter ikke alltid oppdatert med den nyeste versjonen av CCOs. Du bør også være oppmerksom på at, Generelt, kvaliteten på serviceobjekter varierer.

### <a name="windows"></a>Windows

Skrive ut kvittering på Salgsstedet er optimalisert for OPOS. OPOS pleier å være mye raskere enn utskrift i Windows. Det er derfor en god idé å bruke OPOS, spesielt i detaljhandel miljøer der 40-kolonners mottak skal skrives ut, og transaksjonen må være rask. For de fleste enheter, kan du bruke OPOS-kontroller. Noen OPOS kvittering skrivere støtter også Windows-drivere. Ved hjelp av en Windows-driver, kan du tilgang til siste skriftene og en nettverksskriver for flere kasser. Det finnes imidlertid ulemper ved hjelp av Windows-drivere. Her er noen eksempler på disse ulemper:

-   Når du bruker Windows-drivere, gjengis bilder før utskrift. Derfor pleier utskrift å være lavere enn på skrivere som bruker OPOS-kontroller.
-   Enheter som er koblet til skriveren ("kjedes sammen") fungerer kanskje ikke på riktig måte når Windows-driverne brukes. For eksempel kassaskuffen kan ikke åpne eller slip-skriveren kan ikke word som forventet.
-   OPOS støtter også et mer omfattende sett med variabler som er spesifikke for detaljhandel kvittering skrivere, for eksempel kutting av papir eller slip-utskrift.

Hvis OPOS-kontroller er tilgjengelige for Windows-skriveren du bruker, bør fremdeles skriveren fungerer riktig med Microsoft Dynamics 365 for operasjoner - handel.

### <a name="universal-windows-platform"></a>Universell Windows-plattformen

UWP, når det gjelder retail-enheter, er relatert til Windows-støtte for Plug and Play-enheter. Når en Plug and Play-enhet er koblet til en Windows-OS-versjon som støtter denne typen enhet, kreves ingen driver for enheten som skal brukes som det skal. For eksempel hvis Windows oppdager en Bluetooth-enhet for høyttaler, OS vet at enheten har den **høyttaler** klasse type. Derfor, og den behandler den enheten som en høyttaler. Mer er ikke obligatorisk. Mange USB-enheter kan plugges inn når det gjelder POS-enheter, og Windows vil gjenkjenne dem som enheter for menneskelig grensesnitt (HIDs). Det kan imidlertid ikke bestemme muligheter som gir enheten, fordi enheten ikke angir klassen eller enhetstypen. Enhetsklassene for strekkodeskannere og MSRs har lagt til i Windows-10. Derfor, hvis en enhet deklarerer selve Windows 10 som en enhet av en av disse klassene, Windows vil lytte for hendelser fra enheten på riktig tidspunkt. Moderne POS støtter UWP MSRs og skannere. Derfor, når det er klart for inndata fra en av disse enhetene, og en enhet som tilhører en av disse klassene er tilkoblet, enheten kan brukes. For eksempel hvis en UWP strekkodeskanner er koblet til en datamaskin for Windows 10 og strekkode-pålogging som er konfigurert for moderne POS, bli strekkode skanneren aktiv på skjermen for pålogging. Mer er ikke obligatorisk. Flere klasser av poenget med tjenesten UWP enheter legges til Windows. Disse klassene inkluderer klasser for kontanter skuffer og kvittering skrivere. Støtte for disse enhetsklassene nye i moderne POS venter.

### <a name="keyboard-wedge"></a>Tastatur-kant

Tastaturet kant enheter sender data til datamaskinen som om dataene ble skrevet på et tastatur. Som standard, vil feltet som er aktive på Salgsstedet derfor motta data som er skannet eller lest. I noen tilfeller kan dette forårsake feil type data som skal skannes i feil felt. En strekkode kan for eksempel skannes inn i et felt som er ment for registrering av data for kredittkort. I mange tilfeller er det logikk på Salgsstedet som bestemmer om data som er skannet eller lest er en strekkode eller Kortlesing. Derfor behandles dataene på riktig måte. Når enheter er angitt som OPOS i stedet for tastatur kant enheter, er det imidlertid mer kontroll over hvordan dataene fra disse enhetene kan brukes, fordi flere er "kjent" om enheten som dataene kommer fra. Hvis du for eksempel data fra en strekkodeskanner gjenkjennes automatisk som en strekkode, og den tilknyttede posten i databasen finnes enklere og raskere enn hvis et generisk streng Søk ble brukt, som er tilfelle i tastaturet kant enheter.

### <a name="native-printer"></a>Opprinnelig skriver

Opprinnelig (eller "Enhet" som heter i maskinvareprofilen profil) skrivere kan konfigureres til å be brukeren om å velge en skriver som er konfigurert for datamaskinen. Når en skriver av den **enhet** type er konfigurert, hvis moderne POS oppdager en print-kommandoen, brukeren blir bedt om å velge en skriver i en liste. Denne virkemåten er forskjellig fra virkemåten for Windows-drivere, fordi den **Windows** skriver maskinvareprofil viser ikke en liste over skrivere. I stedet, det krever at en navngitt skriver angis i den **enhetsnavn** feltet.

### <a name="windows"></a>Windows

Den **Windows** enheten brukes for bare skrivere. Når en Windows-skriveren er konfigurert i maskinvareprofilen, må bestemte skrivernavn angis. Når moderne POS støter ut hendelser, hvis en Windows-skriver er konfigurert, vil hendelsen bli sendt til den angitte Windows-skriveren. Brukeren vil ikke bli bedt om å velge en skriver.

### <a name="network"></a>Nettverk

Nettverk-adresserbare pengeskuff, kvittering skrivere og betalingsterminaler kan brukes over et nettverk, direkte via Interprocess kommunikasjon (IPC) maskinvare stasjonen som er bygd inn i moderne POS for Windows-program eller IIS maskinvare station for andre moderne POS-klienter.

## <a name="hardware-station-deployment-options"></a>Maskinvare station distribusjonsalternativer
### <a name="ipc-built-in"></a>IPC (innebygd)

Maskinvare stasjonen Interprocess kommunikasjon (IPC) er bygd inn i moderne POS for Windows-program. Hvis du vil bruke IPC maskinvare station, kan du tilordne en maskinvareprofil til en journal som bruker moderne POS for Windows-program. Deretter oppretter du en maskinvare-stasjon av den **dedikert** type for butikken der journalen skal brukes. Når du starter moderne POS, IPC maskinvare-stasjonen skal være aktiv, og POS-enheter som er konfigurert, vil være klar til bruk. Hvis du midlertidig ikke krever den lokale maskinvaren for en eller annen grunn, kan du bruke den **behandle maskinvare radiostasjoner** operasjon for å slå av stasjonen maskinvarefunksjoner. Moderne POS kan også bruke IPC maskinvare stasjonen til å kommunisere direkte med network peripherals.

### <a name="iis"></a>IIS

Du kan bruke IIS eller frittstående versjon av maskinvare-stasjonen på to måter. Beskrivelsen "IIS" betyr at POS-programmet kobler til stasjonen maskinvare via Microsoft Internet Information Services. POS-programmet kobler til IIS maskinvare stasjon via webtjenester som kjører på en datamaskin der enheten er tilkoblet. Når IIS brukes, detaljhandel eksterne enheter som er koblet til en maskinvare-stasjon kan brukes av alle POS-register som er på samme nettverk som IIS maskinvare station. Fordi bare moderne POS for Windows inneholder innebygd støtte for retail-enheter, må alle andre moderne POS-programmer bruke IIS maskinvare stasjonen til å kommunisere med POS-enheter som er konfigurert i maskinvareprofilen. Derfor krever hver forekomst av IIS maskinvare stasjonen en datamaskin som kjører web-tjenesten, og programmet som kommuniserer med enheter. IIS maskinvare-stasjon er nødvendig for alle ikke - Windows moderne POS-programmer.

#### <a name="dedicated"></a>Dedikert

Moderne POS bruker maskinvare stasjoner på den **dedikert** type for å oppdage at eksterne enheter er koblet direkte til datamaskinen der programmet brukes. Men den **dedikert** kan også brukes for IIS maskinvare stasjoner. I en tradisjonell, faste POS-scenario som bruker sky POS som POS-program på **dedikert** maskinvare stasjonstype brukes for IIS maskinvare stasjoner som er distribuert på samme datamaskin som kjører sky POS. Fra et perspektiv for retail-Tilbehør, har bedre dedikert IIS maskinvare stasjonen detaljhandel ekstern støtte for tradisjonell, faste POS-scenarier. Dedikert maskinvare-stasjoner støtter alle eksterne enheter som støttes i maskinvareprofilen.

#### <a name="shared"></a>Delt

Delt maskinvare stasjoner er ment å brukes av flere POS-enheter i løpet av dagen. Delte stasjoner er optimalisert til å støtte bare kontanter skuffer, kvittering skrivere og betalingsterminaler maskinvare. Du kan ikke direkte koble frittstående strekkodeskannere, MSRs, viser, skalerer eller andre enheter. Ellers oppstår konflikter når flere enheter for POS prøver å hevde at de eksterne enhetene samtidig. Her er hvordan konflikter behandles for enheter som støttes:

-   **Kassaskuff** – kontanter skuffen åpnes via en hendelse som er sendt til enheten. Bare problemet som kan oppstå når en kassaskuff kalles oppstår hvis kassaskuffen er allerede åpen. Når det gjelder maskinvare delte stasjoner på kassaskuff bør settes til **delte** i maskinvareprofilen. Denne innstillingen hindrer Salgsstedet kontrollerer om kassaskuffen er allerede åpen når det sender åpne-kommandoer.
-   **Kvitteringsskriver** – Hvis to mottak utskriftskommandoer sendes til stasjonen maskinvare på samme tid, en av kommandoene kan gå tapt, avhengig av enheten. Noen enheter har interne minnet eller pooling som kan forhindre at dette problemet. Hvis en print-kommandoen ikke er vellykket, kassereren mottar en feilmelding, og kan kommandoen på nytt ut fra Salgsstedet.
-   **Betaling terminal** – Hvis en kasserer forsøker å betalingsmiddel en transaksjon i en betaling terminal som allerede er i bruk, en melding varsler om kassereren at terminalen som brukes, og spør kassereren å prøve på nytt senere. Kasserere kan vanligvis se at en terminal er allerede i bruk og venter til andre transaksjonen fullføres før de prøver å betalingsmiddel på nytt.

Validering er planlagt for en fremtidig versjon, til å oppdage om enheter som ikke støttes, er satt opp for en maskinvareprofil som er tilordnet en delt maskinvare-stasjon. Hvis ingen enheter støttes ikke blir funnet, få vil brukeren en melding om at enhetene ikke er støtte for maskinvare delte stasjoner. Når det gjelder maskinvare delte stasjoner på **Velg ved tendering** alternativet er satt til **Ja** på register-nivå. POS-brukeren er deretter bedt om å velge en maskinvare-stasjon når et betalingsmiddel som er valgt for en transaksjon på Salgsstedet. Når maskinvare-stasjonen er valgt bare samtidig som betalingsmiddel, maskinvare station valget er lagt til direkte POS-arbeidsflyt for mobile scenarier. Som en ekstra fordel er ikke linjevisningen på betalingen terminal brukes for delte scenarier. Hvis betalingen terminal brukes som en linje-skjerm, kan andre brukere være blokkert fra å bruke denne terminalen før transaksjonen er fullført. I mobile scenarier kan linjer legges til en transaksjon over en lengre periode. Derfor den **Velg ved tendering** alternativet er nødvendig for å sikre optimal enheten tilgjengelighet.

### <a name="network-peripherals"></a>Nettverk-Tilbehør

Nettverk-angivelsen for enheter i maskinvareprofilen profil kan kontanter skuffer, kvittering skrivere og betalingsterminaler kobles via en nettverkstilkobling.

#### <a name="modern-pos-for-windows"></a>Moderne POS for Windows

Du kan angi IP-adresser for nettverket enheter på to steder. Moderne POS-Windows-klienten bruker et enkelt sett med enheter på nettverket, bør du angi IP-adressene for disse enhetene ved hjelp av den **IP-konfigurasjon for** alternativet i handlingsruten for å registrere seg selv. Når det gjelder nettverksenheter som vil bli delt blant POS-kasser, en maskinvareprofil som er tilordnet nettverksenheter kan tilordnes direkte til en delt maskinvare-stasjon. For å tildele IP-adresser, velger du denne maskinvare-stasjonen på den **forretninger** side, og deretter bruke den **IP-konfigurasjon** alternativ i den **maskinvare radiostasjoner** delen for å angi nettverksenheter som er tilordnet til denne stasjonen maskinvare. For maskinvare-stasjoner som har bare nettverksenheter, trenger du ikke å distribuere selve maskinvaren stasjonen. I dette tilfellet kreves stasjonen maskinvare bare for å gruppere begrepsmessig nettverk adresserbare enheter i henhold til deres plassering i Detaljhandel Lager.

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>Sky POS, moderne POS for iOS og moderne POS for Android

Logikken som styrer fysisk tilkoblet og nettverk-adresserbare enheter finnes i stasjonen maskinvare. For alle klienter som POS bortsett fra moderne POS for Windows, må derfor station en IIS-maskinvare er distribuert og aktiv for å aktivere POS til å kommunisere med eksterne enheter, uavhengig av om de eksterne enhetene er fysisk koblet til en stasjon for maskinvare eller adressert over nettverket.

## <a name="setup-and-configuration"></a>Installasjon og konfigurasjon
### <a name="hardware-station-installation"></a>Maskinvareinstallering station

For informasjon, kan du se [Retail station maskinvarekonfigurasjonen og installasjon](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Moderne POS for Windows-installasjon og konfigurasjon

For informasjon, kan du se [moderne Priskontroll konfigurering og installering](retail-modern-pos-device-activation.md).

### <a name="opos-device-setup-and-configuration"></a>OPOS enhet installasjon og konfigurasjon

Hvis du vil ha mer informasjon om OPOS-komponenter, kan du se delen "Støttet grensesnitt" i dette dokumentet. OPOS-drivere er vanligvis levert av produsenten av enheten. Når en OPOS-enhetsdriver er installert, legges det til en nøkkel i Windows-registret i ett av følgende steder:

-   **32-biters system:** HKEY\_lokale\_MACHINESOFTWAREOLEforRetailServiceOPOS
-   **64-biters system:** HKEY\_lokale\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

I ServiceOPOS-registerplassering er konfigurerte enheter organisert i henhold til enhetsklassen OPOS. Flere enhetsdrivere, lagres.

## <a name="supported-scenarios-by-hardware-station-type"></a>Scenarier etter stasjonstype for maskinvare som støttes
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Klientstøtte for – IPC maskinvare station vs. IIS maskinvare station

Tabellen nedenfor viser topologi og installasjonsscenarier som støttes.

| Kunde      | IPC maskinvare station | IIS maskinvare station |
|-------------|----------------------|----------------------|
| Windows-app | Ja                  | Ja                  |
| Skybasert salgssted   | Ingen                   | Ja                  |
| Android     | Ingen                   | Ja                  |
| iOS         | Ingen                   | Ja                  |

### <a name="network-peripherals"></a>Nettverk-Tilbehør

Network peripherals kan støttes direkte gjennom maskinvare-stasjonen som er bygd inn i moderne POS for Windows-program. For alle andre klienter, må du distribuere station en IIS-maskinvare.

| Kunde      | IPC maskinvare station | IIS maskinvare station |
|-------------|----------------------|----------------------|
| Windows-app | Ja                  | Ja                  |
| Skybasert salgssted   | Ingen                   | Ja                  |
| Android     | Ingen                   | Ja                  |
| iOS         | Ingen                   | Ja                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Støttede enhetstyper etter maskinvaretype station
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Moderne POS for Windows med en stasjon for IPC (innebygd)-maskinvare

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Støttede enhetsklasse</th>
<th>Støttede grensesnitt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Skriver</td>
<td><ul>
<li>OPOS</li>
<li>Windows-driver</li>
<li>Enhet</li>
<li>Nettverk</li>
</ul></td>
</tr>
<tr class="even">
<td>Skriver 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows-driver</li>
<li>Enhet</li>
<li>Nettverk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Linjevisning</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Dobbel visning</td>
<td>Windows-driver</td>
</tr>
<tr class="odd">
<td>Kortleser</td>
<td><ul>
<li>OPOS</li>
<li>UWP (ikke er obligatorisk.)</li>
<li>Tastatur-kant (ikke er obligatorisk.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Trassent</td>
<td><ul>
<li>OPOS</li>
<li>Nettverk <strong>notat:</strong> bare én skuff kan defineres Hvis <strong>bruke delte SKIFT</strong> er konfigurert på skuffen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skuff 2</td>
<td><ul>
<li>OPOS</li>
<li>Nettverk <strong>notat:</strong> bare én skuff kan defineres Hvis <strong>bruke delte SKIFT</strong> er konfigurert på skuffen.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skanner</td>
<td><ul>
<li>OPOS</li>
<li>UWP (ikke er obligatorisk.)</li>
<li>Tastatur-kant (ikke er obligatorisk.)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skanner 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (ikke er obligatorisk.)</li>
<li>Tastatur-kant (ikke er obligatorisk.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Skaler</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>PIN-kodetastatur</td>
<td>OPOS (det ytes kundestøtte gjennom tilpasning av betalingskoblingen.)</td>
</tr>
<tr class="even">
<td>Signaturregistrering</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Betalingsterminal </td>
<td><ul>
<li>Støtte for egendefinerte enheter</li>
<li>Nettverk (For mer informasjon, se dokumentasjonen for betaling-kobling.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Alle moderne POS-klienter som har en dedikert maskinvare-stasjon for IIS

**Merk:** når IIS maskinvare-stasjonen er "reservert", det er en fotballkamp mellom POS-klienten og maskinvare-stasjonen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Støttede enhetsklasse</th>
<th>Støttede grensesnitt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Skriver</td>
<td><ul>
<li>OPOS</li>
<li>Windows-driveren <strong>notat:</strong> For Windows-skrivere på et nettverk, må brukeren av maskinvare-stasjonen har tilgang til skriveren.</li>
<li>Nettverk</li>
</ul></td>
</tr>
<tr class="even">
<td>Skriver 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows-driver</li>
<li>Nettverk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Linjevisning</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Kortleser</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Trassent</td>
<td><ul>
<li>OPOS</li>
<li>Nettverk <strong>notat:</strong> Hvis du kan angi bare én skuff per maskinvareprofil <strong>bruke delte SKIFT</strong> er konfigurert på skuffen.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skuff 2</td>
<td><ul>
<li>OPOS</li>
<li>Nettverk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skanner</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Skanner 2</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Skaler</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>PIN-kodetastatur</td>
<td>OPOS (det ytes kundestøtte gjennom tilpasning av betalingskoblingen.)</td>
</tr>
<tr class="odd">
<td>SIG. registrering</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Betalingsterminal </td>
<td><ul>
<li>Støtte for egendefinerte enheter</li>
<li>Nettverk (For mer informasjon, se dokumentasjonen for betaling-kobling.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Alle moderne POS-klienter som har en delt stasjon for IIS-maskinvare

**Merk:** når IIS maskinvare-stasjonen er "delt", flere enheter kan bruke stasjonen maskinvare på samme tid. I dette scenariet bør du bruke bare enhetene som er oppført i følgende tabell. Hvis du prøver å dele enheter som ikke er nevnt her, for eksempel strekkodeskannere og MSRs, vil det oppstå feil når flere enheter forsøker å hevde at den samme eksterne enheten. I fremtiden, vil en slik konfigurasjon bli eksplisitt forhindret.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Støttede enhetsklasse</th>
<th>Støttede grensesnitt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Skriver</td>
<td><ul>
<li>OPOS</li>
<li>Windows-driveren <strong>notat:</strong> For Windows-skrivere på et nettverk, må brukeren av maskinvare-stasjonen har tilgang til skriveren.</li>
<li>Nettverk</li>
</ul></td>
</tr>
<tr class="even">
<td>Skriver 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows-driver</li>
<li>Nettverk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Trassent</td>
<td><ul>
<li>OPOS</li>
<li>Nettverk <strong>notat:</strong> Hvis du kan angi bare én skuff per maskinvareprofil <strong>bruke delte SKIFT</strong> er konfigurert på skuffen.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skuff 2</td>
<td><ul>
<li>OPOS</li>
<li>Nettverk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Betalingsterminal </td>
<td><ul>
<li>Støtte for egendefinerte enheter</li>
<li>Nettverk (For mer informasjon, se dokumentasjonen for betaling-kobling.)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Konfigurasjon for scenarier som støttes
Hvis du vil ha mer informasjon om hvordan du kan opprette maskinvareprofiler, se [definere og vedlikeholde kanal-klienter, inkludert registre og maskinvare stasjoner](define-maintain-channel-clients-registers-hw-stations.md). **Merk:** For Microsoft Dynamics-365 for operasjoner versjon 1611, brukes ikke lenger station maskinvareprofilen. Attributter som du tidligere har definert i maskinvareprofilen station er nå en del av selve maskinvaren stasjonen.

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Moderne POS for Windows med en stasjon for IPC (innebygd)-maskinvare

Denne konfigurasjonen er mest vanlig konfigurasjon for tradisjonelle, fast kasser på Salgssted. I dette scenariet er profilinformasjonen maskinvare tilordnet direkte til å registrere seg selv. EFT-terminalnummer bør også angis i selve journalen. Hvis du vil angi denne konfigurasjonen, følger du denne fremgangsmåten.

1.  Opprette en maskinvareprofil der alle nødvendige enheter er konfigurert.
2.  Tilordne maskinvareprofilen til POS-journalen.
3.  Opprette en maskinvare-stasjon av den **dedikert** type for detaljhandel der POS-journalen som skal brukes. En beskrivelse er valgfri. **Merk:** du trenger ikke å angi eventuelle andre egenskaper på maskinvare-stasjonen. Alle andre nødvendige informasjonen, for eksempel maskinvareprofilen, kommer fra selve journalen.
4.  Klikk **Retail og commerce**&gt;**Retail IT**&gt;**distribusjonsplan**.
5.  Velg den **1090** distribusjonsplan for å synkronisere den nye maskinvareprofilen til butikken. Klikk **kjører nå** å synkronisere endringer på Salgsstedet.
6.  Velg den **1040** distribusjonsplan for å synkronisere den nye maskinvare-stasjonen til butikken. Klikk **kjører nå** å synkronisere endringer på Salgsstedet.
7.  Installer og Aktiver moderne POS for Windows.
8.  Start moderne POS for Windows, og begynner å bruke de tilkoblede ytre enhetene.

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Alle moderne POS-klienter som har en dedikert maskinvare-stasjon for IIS

Denne konfigurasjonen kan brukes for alle moderne POS-klienter som har en maskinvare-stasjon som brukes av en POS registrere. Hvis du vil angi denne konfigurasjonen, følger du denne fremgangsmåten.

1.  Opprette en maskinvareprofil der alle nødvendige enheter er konfigurert.
2.  Opprette en maskinvare-stasjon av den **dedikert** type for detaljhandel der POS-journalen som skal brukes.
3.  På dedikert maskinvare-stasjonen, kan du angi følgende egenskaper:
    -   **Vertsnavn** – navnet på vertsdatamaskinen hvor maskinvare-stasjonen skal kjøres. **Merk:** sky POS kan løse **localhost** til å bestemme den lokale datamaskinen der sky POS kjøres. Sertifikatet som kreves for å opprette en parkobling sky POS maskinvare-stasjon må imidlertid også "Localhost" som navnet på datamaskinen. For å unngå problemer, anbefaler vi at du angir en forekomst av hver stasjon på dedikert maskinvare for butikken, etter behov. For hver enkelt maskinvare station, bør vertsnavnet være navnet på bestemte datamaskinen der stasjonen maskinvare skal distribueres.
    -   **Port** -porten som skal brukes for maskinvare-stasjon til å kommunisere med moderne POS-klienten.
    -   **Maskinvareprofil** – Hvis ikke maskinvareprofilen forutsatt maskinvareprofilen som er tilordnet journalen skal brukes på maskinvare station selve,.
    -   **EFT-POS nummer** – The EFT terminal-ID skal brukes ved autorisering av EFT sendes. Denne IDen er levert av kredittkortbehandleren.
    -   **Pakkenavnet** – maskinvare station pakken skal brukes når stasjonen maskinvare er distribuert.

4.  Klikk **Retail og commerce**&gt;**Retail IT**&gt;**distribusjonsplan**.
5.  Velg den **1090** distribusjonsplan for å synkronisere den nye maskinvareprofilen til butikken. Klikk **kjører nå** å synkronisere endringer på Salgsstedet.
6.  Velg den **1040** distribusjonsplan for å synkronisere den nye maskinvare-stasjonen til butikken. Klikk **kjører nå** å synkronisere endringer på Salgsstedet.
7.  Installer maskinvare-stasjonen. Hvis du vil ha mer informasjon om hvordan du installerer maskinvare-stasjonen, se [Retail station maskinvarekonfigurasjonen og installasjon](retail-hardware-station-configuration-installation.md).
8.  Installer og Aktiver moderne POS. Hvis du vil ha mer informasjon om hvordan du installerer moderne POS, se [moderne Priskontroll konfigurering og installering](retail-modern-pos-device-activation.md).
9.  Logg moderne POS, og velg **utføre operasjoner for ikke-skuff**.
10. Start den **behandle maskinvare radiostasjoner** operasjonen.
11. Klikk **behandle**.
12. På siden for behandling av maskinvare station, angir du alternativet for å aktivere stasjonen maskinvare.
13. Velg stasjonen maskinvare til å bruke, og klikk deretter **par**.
14. Når stasjonen maskinvare er forbundet, klikker du **Lukk**.
15. På siden for valg maskinvare station, klikker du den sist valgte maskinvare-stasjonen for å gjøre den aktiv.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Alle moderne POS-klienter som har en delt stasjon for IIS-maskinvare

Denne konfigurasjonen kan brukes for alle moderne POS-klienter som deler maskinvare-stasjoner med andre enheter. Hvis du vil angi denne konfigurasjonen, følger du denne fremgangsmåten.

1.  Opprette en maskinvareprofil der de nødvendige enhetene er konfigurert.
2.  Opprette en maskinvare-stasjon av den **delte** type for detaljhandel der POS-journalen som skal brukes.
3.  På den delte maskinvare-stasjonen, kan du angi følgende egenskaper:
    -   **Vertsnavn** – navnet på vertsdatamaskinen hvor maskinvare-stasjonen skal kjøres.
    -   **Beskrivelse** – tekst som hjelper med å identifisere maskinvare-stasjon som **returnerer** eller **Front av butikken**.
    -   **Port** -porten som skal brukes for maskinvare-stasjon til å kommunisere med moderne POS-klienten.
    -   **Maskinvareprofil** – hver maskinvare stasjon bør ha en maskinvareprofil For maskinvare delte stasjoner. Maskinvareprofiler kan deles mellom maskinvare-stasjoner, men de må være tilordnet hver maskinvare-stasjon. I tillegg anbefaler vi at du bruker delte SKIFT når flere enheter som bruker den samme delte maskinvare-stasjonen. Klikk for å opprette en delt SKIFT, **Retail og commerce**&gt;**kanaloppsett**&gt;**POS installasjonsprogrammet**&gt;**POS profiler**&gt;**maskinvareprofiler**. Velg kassaskuffen for hver delte maskinvareprofil, og angi de **delte SKIFT skuffen** å **Ja**.
    -   **EFT-POS nummer** – The EFT terminal-ID skal brukes ved autorisering av EFT sendes. Denne IDen er levert av kredittkortbehandleren.
    -   **Pakkenavnet** – maskinvare station pakken skal brukes når stasjonen maskinvare er distribuert.

4.  Gjenta trinn 2 og 3 for hver ekstra maskinvare-stasjon som er nødvendig i lageret.
5.  Klikk **Retail og commerce**&gt;**Retail IT**&gt;**distribusjonsplan**.
6.  Velg den **1090** distribusjonsplan for å synkronisere den nye maskinvareprofilen til butikken. Klikk **kjører nå** å synkronisere endringer på Salgsstedet.
7.  Velg den **1040** distribusjonsplan for å synkronisere den nye maskinvare-stasjonen til butikken. Klikk **kjører nå** å synkronisere endringer på Salgsstedet.
8.  Installer maskinvare-stasjonen på hver vertsdatamaskin som du opprettet i trinn 2 og 3. Hvis du vil ha mer informasjon om hvordan du installerer maskinvare-stasjonen, se [Retail station maskinvarekonfigurasjonen og installasjon](retail-hardware-station-configuration-installation.md).
9.  Installer og Aktiver moderne POS. Hvis du vil ha mer informasjon om hvordan du installerer moderne POS, se [moderne Priskontroll konfigurering og installering](retail-modern-pos-device-activation.md).
10. Logg moderne POS, og velg **utføre operasjoner for ikke-skuff**.
11. Start den **behandle maskinvare radiostasjoner** operasjonen.

12. Klikk **behandle**.
13. På siden for behandling av maskinvare station, angir du alternativet for å aktivere stasjonen maskinvare.
14. Velg stasjonen maskinvare til å bruke, og klikk deretter **par**.
15. Gjenta trinn 14 for hver stasjon for maskinvare som bruker moderne POS.
16. Når all nødvendig maskinvare-stasjoner er forbundet, klikker du **Lukk**.
17. På siden for valg maskinvare station, klikker du den sist valgte maskinvare-stasjonen for å gjøre den aktiv. **Merk:** Hvis enheter bruker ofte forskjellig maskinvare radiostasjoner, anbefaler vi at du konfigurerer moderne POS for å spørre kasserere å velge en maskinvare-stasjon når de begynner betalingsmiddel prosessen. Klikk **Retail og commerce**&gt;**kanaloppsett**&gt;**POS installasjonsprogrammet**&gt;**registrerer**. Velg journalen, og angi deretter den **Velg når betalingen** å **Ja**. Bruk av **1090** distribusjonsplan for å synkronisere endringer i kanal-databasen.

## <a name="extensibility"></a>Utvidelsesmuligheter
Informasjon om utvidelse scenarier for maskinvare-stasjonen, kan du se [maskinvare Station extensibility](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Sikkerhet
Følgende innstillinger i henhold til gjeldende sikkerhetsstandarder, skal brukes i et produksjonsmiljø: **notat:** maskinvare station installasjonsprogrammet vil automatisk gjøre disse endringene i registret som en del av installasjonen gjennom Self Service.

-   Secure Sockets Layer (SSL) skal deaktiveres.
-   Bare Transport Layer Security (TLS) versjon 1.2 (eller gjeldende høyeste versjon) skal være aktivert og brukes. **Merk:** som standard, SSL og alle versjon av TLS unntatt TLS 1.2 er deaktivert. Hvis du vil redigere, eller aktivere disse verdiene, følger du denne fremgangsmåten:
    1.  Trykke Windows-tasten + R for å åpne en **kjører** vindu.
    2.  I den **åpne** skriver du inn **Regedit**, og klikk deretter **OK**.
    3.  Hvis en **Brukerkontokontroll** melding vises, klikker du **Ja**.
    4.  I den **Registerredigering** vindu, gå til **HKEY\_lokale\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Følgende taster er automatisk registrert for å tillate TLS 1.2 bare:
        -   TLS-1.2Server: aktivert = 1
        -   TLS-1.2Server:DisabledByDefault = 0
        -   TLS-1.2Client: aktivert = 1
        -   TLS-1.2Client:DisabledByDefault = 0
        -   TLS-1.1Server: aktivert = 0
        -   TLS-1.1Client: aktivert = 0
        -   TLS-1.0Server: aktivert = 0
        -   TLS-1.0Client: aktivert = 0
        -   SSL-3.0Server: aktivert = 0
        -   SSL-3.0Client: aktivert = 0
        -   SSL-2.0Server: aktivert = 0
        -   SSL-2.0Client: aktivert = 0
-   Ingen flere nettverksporter skal være åpne, med mindre de er nødvendige for kjente, angitte årsaker.
-   Kryss-opprinnelse ressursdeling må være deaktivert og må angi tillatte opprinnelse som godtas.
-   Bare klarerte sertifiseringsinstanser skal brukes til å skaffe sertifikater som skal brukes på datamaskiner som kjører stasjonen maskinvare.

**Merk:** er det svært viktig at du ser gjennom retningslinjene for sikkerhet for IIS og kravene til betaling kort bransjen (PCI).

## <a name="peripheral-simulator"></a>Ekstern simulator
For informasjon, kan du se [Retail eksterne simulator](retail-peripheral-simulator.md).

## <a name="microsofttested-peripheral-devices"></a>Microsofttested eksterne enheter
### <a name="ipc-built-in-hardware-station"></a>IPC (innebygd) maskinvare station

Følgende enheter ble testet ved hjelp av IPC maskinvare stasjonen som er bygd inn i moderne POS for Windows.

#### <a name="printer"></a>Skriver

| Produsent | Modell    | Grensesnitt | Kommentarer                |
|--------------|----------|-----------|-------------------------|
| Epson        | TM-T88IV | OPOS      |                         |
| Epson        | TM-T88V  | OPOS      |                         |
| Star         | TSP650II | OPOS      |                         |
| Star         | TSP650II | Egendefinert    | Koblet via nettverket   |
| Star         | mPOP     | OPOS      | Koblet via Bluetooth |
| HP           | F7M67AA  | OPOS      | Strømforsynt USB             |

#### <a name="bar-code-scanner"></a>Strekkodeskanner

| Produsent  | Modell         | Grensesnitt | Kommentarer |
|---------------|---------------|-----------|----------|
| Motorola      | DS9208        | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| Symbol        | LS2208        | OPOS      |          |
| Integrert HP | E1L07AA       | OPOS      |          |
| Datalogic     | Magellan 8400 | OPOS      |          |

#### <a name="pin-pad"></a>PIN-kodetastatur

| Produsent | Modell  | Grensesnitt | Kommentarer                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Krever tilpasning av betalingskoblingen |

#### <a name="payment-terminal"></a>Betalingsterminal 

| Produsent | Modell | Grensesnitt | Kommentarer                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Egendefinert    | Krever tilpasning av betalingskoblingen                                |
| VeriFone     | MX925 | Egendefinert    | Krever tilpasning av betalingskobling; koblet via nettverks- og USB |
| VeriFone     | MX915 | Egendefinert    | Krever tilpasning av betalingskobling; koblet via nettverks- og USB |

#### <a name="cash-drawer"></a>Kassaskuff

| Produsent | Modell     | Grensesnitt | Kommentarer                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Koblet via Bluetooth |
| APG          | Atwood    | Egendefinert    | Koblet via nettverket   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |

#### <a name="line-display"></a>Linjevisning

| Produsent  | Modell   | Grensesnitt | Kommentarer |
|---------------|---------|-----------|----------|
| Integrert HP | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Signaturregistrering

| Produsent | Modell  | Grensesnitt | Kommentarer |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Skaler

| Produsent | Modell         | Grensesnitt | Kommentarer |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>Kortleser

| Produsent | Modell       | Grensesnitt | Kommentarer |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="dedicated-iis-hardware-station"></a>Dedikert maskinvare station for IIS

Følgende enheter ble testet ved hjelp av en dedikert (ikke delt) IIS maskinvare station sammen med moderne POS for Windows og sky POS.

#### <a name="printer"></a>Skriver

| Produsent | Modell    | Grensesnitt | Kommentarer                  |
|--------------|----------|-----------|---------------------------|
| Epson        | TM-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Egendefinert    | Koblet via nettverket     |
| Star         | TSP100   | OPOS      | Krever TSP650II-drivere |
| HP           | F7M67AA  | OPOS      | Strømforsynt USB               |

#### <a name="bar-code-scanner"></a>Strekkodeskanner

| Produsent  | Modell   | Grensesnitt | Kommentarer |
|---------------|---------|-----------|----------|
| Motorola      | DS9208  | OPOS      |          |
| Symbol        | LS2208  | OPOS      |          |
| Integrert HP | E1L07AA | OPOS      |          |

#### <a name="pin-pad"></a>PIN-kodetastatur

| Produsent | Modell  | Grensesnitt | Kommentarer                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Krever tilpasning av betalingskoblingen |

#### <a name="payment-terminal"></a>Betalingsterminal 

| Produsent | Modell | Grensesnitt | Kommentarer                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Egendefinert    | Krever tilpasning av betalingskoblingen                                |
| VeriFone     | MX925 | Egendefinert    | Krever tilpasning av betalingskobling; koblet via nettverks- og USB |
| VeriFone     | MX915 | Egendefinert    | Krever tilpasning av betalingskobling; koblet via nettverks- og USB |

#### <a name="cash-drawer"></a>Kassaskuff

| Produsent | Modell     | Grensesnitt | Kommentarer              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Egendefinert    | Koblet via nettverket |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

#### <a name="line-display"></a>Linjevisning

| Produsent  | Modell   | Grensesnitt | Kommentarer |
|---------------|---------|-----------|----------|
| Integrert HP | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Signaturregistrering

| Produsent | Modell  | Grensesnitt | Kommentarer |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Skaler

| Produsent | Modell         | Grensesnitt | Kommentarer |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>Kortleser

| Produsent | Modell       | Grensesnitt | Kommentarer |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="shared-iis-hardware-station"></a>Delt stasjon for IIS-maskinvare

Følgende enheter ble testet ved hjelp av en delt stasjon for IIS maskinvare sammen med moderne POS for Windows og sky POS. **Merk:** bare en skriver, betaling terminal og kassaskuff støttes.

#### <a name="printer"></a>Skriver

| Produsent | Modell    | Grensesnitt | Kommentarer                  |
|--------------|----------|-----------|---------------------------|
| Epson        | TM-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Egendefinert    | Koblet via nettverket     |
| Star         | TSP100   | OPOS      | Krever TSP650II-drivere |
| HP           | F7M67AA  | OPOS      | Strømforsynt USB               |

#### <a name="payment-terminal"></a>Betalingsterminal 

| Produsent | Modell | Grensesnitt | Kommentarer                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Egendefinert    | Krever tilpasning av betalingskobling; koblet via nettverks- og USB |
| VeriFone     | MX915 | Egendefinert    | Krever tilpasning av betalingskobling; koblet via nettverks- og USB |

#### <a name="cash-drawer"></a>Kassaskuff

| Produsent | Modell     | Grensesnitt | Kommentarer              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Egendefinert    | Koblet via nettverket |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

## <a name="troubleshooting"></a>Feilsøking
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Moderne POS kan gjenkjenne stasjonen maskinvare i listen for valg, men det kan ikke fullføre parkoblingen

**Løsning:** bekrefte følgende liste over potensielle feil poeng:

-   Datamaskinen som kjører moderne POS klarerer sertifikatet som er brukt på datamaskinen som kjører stasjonen maskinvare.
    -   Hvis du vil bekrefte dette oppsettet, i en webleser, kan du gå til følgende URL: https://&lt;navnet&gt;:&lt;portnummer&gt;/HardwareStation/ping.
    -   Denne URL-adressen bruker en ping til å kontrollere at datamaskinen kan få tilgang til, og leseren angir om sertifikatet er klarert. (For eksempel i Internet Explorer, et låseikon vises på adresselinjen. Når du klikker dette ikonet, kontrollerer Internet Explorer om sertifikatet er klarert for øyeblikket. Du kan installere sertifikatet på den lokale datamaskinen ved å vise detaljene for sertifikatet vises.)
-   På datamaskinen som kjører stasjonen maskinvare, åpnes porten som brukes av stasjonen maskinvare i brannmuren.
-   Maskinvare-stasjonen er riktig installert handelskonto informasjon gjennom installasjon forretningsenhet informasjon verktøyet som kjører på slutten av stasjonen installer maskinvare.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Moderne POS gjenkjenner ikke maskinvaren-stasjon i listen for valg

**Løsning:** ett av følgende faktorer kan forårsake dette problemet:

-   Maskinvare-stasjonen ikke er riktig konfigurert i headquarters. Bruk fremgangsmåten tidligere i dette emnet for å bekrefte at maskinvareprofilen station og maskinvare-stasjonen er riktig skrevet.
-   Jobbene har kjørt for å oppdatere kanalkonfigurasjonen. I dette tilfellet Kjør jobben 1070 for konfigurasjon.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Moderne POS gjenspeiler ikke nye kontanter skuff-innstillinger

**Løsning:** lukke det gjeldende partiet. Endringer i kassaskuffen er ikke oppdatert til moderne POS før gjeldende bunke er lukket.

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Moderne POS rapporterer et problem med en ekstern forhandler

**Løsning:** her er noen vanlige årsaker til dette problemet:

-   Kontroller at andre enhet driver konfigurasjonsverktøyet er lukket. Hvis disse verktøyene er åpne, kan de hindre moderne POS eller maskinvare-station hevder at enheten.
-   Hvis den eksterne enheten detaljhandel deles av flere POS-enheter, må du kontrollere at det tilhører én av følgende kategorier:
    -   Kassaskuff
    -   Kvitteringsskriver
    -   Betalingsterminal 

    Hvis den eksterne enheten ikke tilhører en av disse kategoriene, ikke er maskinvare-stasjonen utformet for å aktivere den eksterne enheten kan deles mellom flere enheter for POS.
-   Enhetsdrivere kan noen ganger føre til felles kontroll objektene (CCOs) til å slutte å virke på riktig måte. Hvis en enhet har nylig installert, men den fungerer ikke riktig eller du oppdager andre problemer, kan du ofte løse problemet ved å installere CCOs. Du kan laste ned CCOs <http://monroecs.com/oposccos_current.htm>.
-   Hvis du foretar hyppige eksterne endringer under testing eller feilsøking, må du kanskje tilbakestille IIS i stedet for å vente på hurtigbufferen å oppdatere seg selv. Hvis du vil tilbakestille IIS, gjør du følgende:
    1.  Fra den **Start** -menyen, skriver du inn **CMD**.
    2.  Høyreklikk i søkeresultatene, **ved ledeteksten**, og klikk deretter **Kjør som administrator**.
    3.  I den **ved ledeteksten** vindu, type **iisreset/restart** og trykk deretter Enter.
    4.  Når IIS er startet på nytt, starter på nytt moderne POS.
-   Mens du gjør hyppige endringer til eksterne enheter, hvis du også ofte starter og avslutter POS-klienten, kan det påvirke dllhost prosessen fra en tidligere POS-økt med gjeldende økt. I dette tilfellet kan en enhet ikke brukes før du lukker den dynamiske koblingsbibliotek (DLL)-verten som administrerer den forrige økten. Hvis du vil lukke DLL-vert, følger du denne fremgangsmåten:
    1.  Fra den **Start** -menyen, skriver du inn **i Oppgavebehandling**.
    2.  I søkeresultatene, velger du **Oppgavebehandling**.
    3.  I Oppgavebehandling, på den **detaljer**, klikker du kolonneoverskriften som heter **navn** å sortere tabellen alfabetisk etter navn.
    4.  Rull nedover til du finner dllhost.exe.
    5.  Velg hver enkelt DLL-vert, og klikk deretter **Avslutt oppgave**.
    6.  Når DLL-verter er avsluttet, starter på nytt moderne POS.


<a name="see-also"></a>Se også
--------

[Detaljhandel eksterne simulator](retail-peripheral-simulator.md)



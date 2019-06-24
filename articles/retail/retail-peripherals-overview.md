---
title: Eksterne enheter for detaljhandel
description: Dette emnet forklarer begrepene som er knyttet til detaljhandelsenheter.
author: rubencdelgado
manager: AnnBe
ms.date: 01/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice, RetailHardwareProfile
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a9fa49d0b3553ae70547aeea19d14bc6e6e08983
ms.sourcegitcommit: ffc37f7c2a63bada3055f37856a30424040bc9a3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/16/2019
ms.locfileid: "1577935"
---
# <a name="retail-peripherals"></a>Eksterne enheter for detaljhandel

[!include [banner](includes/banner.md)]

Dette emnet forklarer begrepene som er knyttet til detaljhandelsenheter. Det beskriver ulike måter enheter kan kobles til salgsstedet og komponentene som er ansvarlig for å administrere tilkoblingen til salgsstedet.

## <a name="concepts"></a>Begreper

### <a name="pos-registers"></a>Kasser på salgssted

Navigering: Klikk **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Kasser**. Kassen på salgsstedet er en enhet som brukes til å definere egenskapene til en bestemt forekomst av salgsstedet. Disse egenskapene inkluderer maskinvareprofilen eller oppsettet for detaljhandelsenheter som skal brukes i kassen, butikken som kassen er tilordnet og den visuelle opplevelsen for brukeren som logger på kassen.

### <a name="devices"></a>Enheter

Navigering: Klikk **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Enheter**. En enhet er en enhet som representerer en fysisk forekomst av en enhet som er tilordnet en kasse på salgsstedet. Når en enhet opprettes, tilordnes den til en kasse på salgsstedet. Enhetsenheten registrerer informasjon om når en kasse på salgsstedet aktiveres, klienttypen som brukes og programpakken som er distribuert til en bestemt enhet. Enheter som kan tilordnes til følgende programtyper: Retail Modern POS, Retail Cloud POS, Retail Modern POS – Windows Phone, Retail Modern POS – Android og Retail Modern POS – iOS.

### <a name="retail-modern-pos"></a>Retail Modern POS

Modern POS er POS-programmet for Microsoft Windows. Den kan distribueres på Windows 10-operativsystemer (OS-er).

### <a name="cloud-pos"></a>Skybasert salgssted

Cloud POS er en webbasert versjon av Modern POS-programmet som kan åpnes i en nettleser.

### <a name="modern-pos-for-ios"></a>Modern POS for iOS

Modern POS for iOS er en iOS-basert versjon av Modern POS-programmet som kan distribueres på iOS-enheter.

### <a name="modern-pos-for-android"></a>Modern POS for Android

Modern POS for Android er en Android-basert versjon av Modern POS-programmet som kan distribueres på Android-enheter.

### <a name="pos-peripherals"></a>POS-enheter

POS-enheter er enheter som er eksplisitt støttes for POS-funksjoner. Disse eksterne enhetene deles vanligvis inn i bestemte klasser. Hvis du vil ha mer informasjon om disse klassene, kan du se delen "Enhetsklasser" i dette emnet.

### <a name="hardware-station"></a>Hardware Station

Navigering: Klikk **Detaljhandel** &gt; **Kanaler** &gt; **Detaljhandelbutikker** &gt; **Alle detaljhandelsbutikker**. Velg en butikk, og klikk deretter hurtigfanen **Maskinvarestasjoner**. Innstillingen **Maskinvarestasjon** er en innstilling på kanalnivå som brukes til å definere forekomster der ekstern logikk for detaljhandel skal distribueres. Denne innstillingen på kanalnivå, brukes til å bestemme egenskapene til maskinvarestasjonen. Den brukes også til å vise maskinvarestasjoner som er tilgjengelige for en Modern POS-forekomst i et angitt lager. Maskinvarestasjonen er bygget inn i Modern POS-programmet for Windows. Maskinvarestasjonen kan også distribueres uavhengig som et frittstående program for Microsoft Internet Information Services (IIS). I slike tilfeller er det tilgang via et nettverk.

### <a name="hardware-profile"></a>Maskinvareprofil

Navigering: Klikk **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofiler** &gt; **Maskinvareprofiler**. Maskinvareprofilen er en liste over enheter som er konfigurert for en kasse på salgssted eller en maskinvarestasjon. Maskinvareprofilen tilordnes direkte til en kasse på salgsstedet eller til en maskinvarestasjon.

## <a name="devices-classes"></a>Enhetsklasser
POS-enheter deles vanligvis inn i bestemte klasser. Denne delen beskriver og inneholder en oversikt over enhetene som støtter i Modern POS.

### <a name="printer"></a>Skriver

Skrivere omfatter tradisjonell kvitteringsskrivere for salgssted og helsideskrivere. Skrivere støttes gjennom kobling og innebygging av objekter for Retail POS-enheter og Microsoft Windows-drivergrensesnitt. Opptil to skrivere kan brukes samtidig. Denne funksjonen støtter scenarier der kundekvitteringer ved hentesalg skrives ut på kvitteringsskrivere, mens kundeordrer, som inneholder mer informasjon, skrives ut på en helsideskriver. Kvitteringsskrivere kan kobles direkte til en datamaskin via USB, kobles til et nettverk via Ethernet eller kobles til via Bluetooth.

### <a name="scanner"></a>Skanner

Opptil to strekkodeskannere kan brukes samtidig. Denne funksjonen støtter situasjoner der en skanner som er mer mobil er nødvendig for å skanne store eller tunge varer, mens en fast innebygd skanner brukes til de fleste elementer i standardstørrelse for raskere utsjekking. Skannere støttes gjennom OPOS, UWP (Universal Windows Platform) eller tastaturkortlesergrensesnitt. USB eller Bluetooth kan brukes til å koble en skanner til en datamaskin.

### <a name="msr"></a>Kortleser

Én USB-kortleser (MSR) kan konfigureres ved hjelp av OPOS-drivere. Hvis du vil bruke en frittstående kortleser for EFT-betalingstransaksjoner, må kortleseren styres av en betalingstilkobling. Frittstående kortlesere kan brukes til registrering av kundefordeler, ansattpåloggingen og registrering av gavekort, uavhengig av betalingskoblingen.

### <a name="cash-drawer"></a>Kassaskuff

To kassaskuffer kan støttes per maskinvareprofil. Denne funksjonen gjør det mulig å ha tilgjengelig to aktive skift per kasse samtidig. Hvis det er et delt skift eller en kassaskuff brukes av flere POS-mobilenheter samtidig, er bare én kassaskuff tillatt per maskinvareprofil. Kassaskuffer kan kobles direkte til en datamaskin via USB, kobles til et nettverk eller kobles til en kvitteringsskriver via et RJ12-grensesnitt. I noen tilfeller kan kassaskuffer også kobles til via Bluetooth.

### <a name="line-display"></a>Linjevisning

Linjevisningsenheter brukes til å vise produkter, transaksjonssaldoer og annen nyttig informasjon til kunden under en transaksjon. Linjevisningsenhet med én linje kan kobles til datamaskinen via USB ved hjelp av OPOS-drivere.

### <a name="signature-capture"></a>Signaturregistrering

Registreringsenheter for signatur kan kobles direkte til en datamaskin via USB ved hjelp av OPOS-drivere. Når signaturregistrering er konfigurert, blir kunden bedt om å signere på enheten. Når signaturen er angitt, vises den til kassereren for godkjenning.

### <a name="scale"></a>Skaler

Veker kan kobles til datamaskinen via USP ved hjelp av OPOS-drivere. Når et produkt som er merket som et "veid" produkt legges til i en transaksjon, leser salgsstedet vekten fra vekten, legger til produktet i transaksjonen og bruker mengden som er angitt av vekten.

### <a name="pin-pad"></a>PIN-kodetastatur

PIN-kodetastaturer støttes gjennom OPOS, men de må administreres via en betalingstilkobling.

### <a name="secondary-display"></a>Sekundær skjerm

Når en sekundær skjerm er konfigurert, brukes Windows-skjermen nummer to til å vise grunnleggende informasjon. Formålet med den sekundære skjermen er å støtte ISV-utvidelser fra uavhengig programvareleverandører, fordi den sekundær skjermen i utgangspunktet ikke kan konfigureres og viser begrenset innhold.

### <a name="payment-device"></a>Betalingsenhet

Støtte for betalingsenheter er implementert via betalingskoblingen. Betalingsenheter kan utføre én eller mange av funksjonene som andre enhetsklasser leverer. En betalingsenhet kan for eksempel fungere som en kortleser, linjevisningsenhet, registreringsenhet for signatur eller PIN-kodetastatur. Støtte for betalingsenheter implementeres uavhengig av støtte for frittstående enheter som er tilgjengelig for andre enheter som er inkludert i maskinvareprofilen.

## <a name="supported-interfaces"></a>Grensesnitt som støttes

### <a name="opos"></a>OPOS

For å garantere at et størst mulig utvalg av enheter kan brukes med Microsoft Dynamics 365 for Retail, er industristandarden OLE for POS den primære plattformen for eksterne enheter for detaljhandel som støttes i Microsoft Dynamics 365 for Retail. OLE for POS-standarden ble produsert ved den National Retail Federation (NRF), som etablerer industristandard kommunikasjonsprotokoller for detaljhandel eksterne enheter. OPOS er en mye brukte implementering av OLE for POS-standarden. Den ble utviklet på midten av 1990-tallet, og har blitt oppdatert flere ganger siden da. OPOS gir en enhetsdriverarkitektur som gir enkel integrering av POS-maskinvare med Windows-baserte POS-systemer. OPOS-kontroller håndterer kommunikasjon mellom kompatibel maskinvare og POS-programvare. En OPOS-kontroll består av to deler:

- **Kontrollobjekt** – Kontrollobjektet for en enhetsklasse (for eksempel linjevisningsenheter) inneholder grensesnittet for programmet. Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) leverer et standardisert sett med OPOS-kontrollobjekter som kalles Common Control Objects (CCO-er). CCOs brukes til å teste POS-komponenten i Microsoft Dynamics 365 for Retail. Derfor bidrar testingen til å garantere at hvis Microsoft Dynamics 365 for Retail støtter en enhetsklasse gjennom OPOS, kan mange enhetstyper støttes, forutsatt at produsenten leverer et tjenesteobjekt som er bygget for OPOS. Du trenger ikke å eksplisitt teste hver enhetstype.
- **Tjenesteobjekt** – Tjenesteobjektet leverer kommunikasjon mellom kontrollobjektet (CCO) og enheten. Tjenesteobjektet for en enhet leveres vanligvis av enhetsprodusenten. I noen tilfeller må du imidlertid laste ned tjenesteobjektet fra produsentens nettsted. Et nyere tjenesteobjekt kan for eksempel være tilgjengelig. Hvis du vil finne adressen til produsentens nettsted, kan du se i maskinvaredokumentasjonen.

[![Kontrollobjekt og tjenesteobjekt](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png)

Støtte for OPOS-implementering av OLE for POS bidrar til å garantere at hvis enhetsprodusentene og POS-utgivere implementerer standarden på riktig måte, kan POS-systemer og støttede enheter samarbeide, selv om de ikke var tidligere testet sammen.

> [!NOTE]
> OPOS-støtte garanterer ikke støtte for alle enheter som har OPOS-drivere. Microsoft Dynamics 365 for Retail må først støtte denne enhetstypen, eller klassen, gjennom OPOS. I tillegg er tjenesteobjekter kanskje ikke alltid oppdaterte med den nyeste versjonen av CCO-er. Du må også være oppmerksom på at kvaliteten på tjenesteobjekter vanligvis varierer.

### <a name="windows"></a>Windows

Kvitteringsutskrift på salgsstedet er optimalisert for OPOS. OPOS pleier å være mye raskere enn utskrift i Windows. Det er derfor smart å bruke OPOS, spesielt i detaljhandelsmiljøer der 40-kolonners kvitteringer skrives ut og transaksjonen må gjennomføres raskt. Du bruker OPOS-kontroller for de fleste enheter. Noen OPOS-kvitteringsskrivere støtter imidlertid også Windows-drivere. Ved å bruke en Windows-driver, har du tilgang til de nyeste skriftene og en nettverksskriveren for flere kasser. Det er imidlertid ulemper med å bruke Windows-drivere. Her er noen eksempler på disse ulempene:

- Når du bruker Windows-drivere, gjengis bilder før utskrift. Derfor pleier utskrift å være langsommere enn på skrivere som bruker OPOS-kontroller.
- Enheter som er koblet gjennom skriveren ("seriekoblet") fungerer kanskje ikke slik de skal når Windows-drivere brukes. En kassaskuffen åpnes for eksempel kanskje ikke eller følgeseddelskriveren fungerer kanskje ikke som forventet.
- OPOS støtter også et mer omfattende sett med variabler som er spesifikke for kvitteringsskrivere for detaljhandel, for eksempel papirkutting eller følgeseddelutskrift.

Hvis OPOS-kontroller er tilgjengelige for Windows-skriveren du bruker, skal skriveren fungere riktig med Microsoft Dynamics 365 for Retail.

### <a name="universal-windows-platform"></a>Universal Windows Platform

Når det gjelder enheter for detaljhandel, er UWP relatert til Windows-støtte for Plug and Play-enheter. Når en Plug and Play-enhet er koblet til en Windows-operativsystemversjon som støtter denne typen enhet, kreves ingen driver for at enheten skal brukes som ment. Hvis Windows for eksempel oppdager en Bluetooth-høyttalerenhet, vet operativsystemet at enheten har klassetypen **Høyttaler**. Derfor behandles enheten som en høyttaler. Ingen tilleggskonfigurasjon kreves. Mange USB-enheter for salgssted kan kobles til, og Windows vil gjenkjenne dem som enheter for menneskelig grensesnitt (HID-er). Det kan imidlertid hende at Windows ikke kan fastslå hvilke funksjoner enheten leverer, fordi enheten ikke angir klassen eller enhetstypen. I Windows 10 er det lagt til enhetsklasser for strekkodeskannere og kortlesere. Hvis en enhet deklarerer seg selve for Windows 10 som en enhet av en av disse klassene, vil Windows derfor lytte etter hendelser fra enheten på riktige tidspunkt. Modern POS støtter UWP-kortlesere og -skannere. Når det er klart for inndata fra en av disse enhetene og en enhet som tilhører en av disse klassene er tilkoblet, kan enheten derfor brukes. Hvis en UWP-strekkodeskanner for eksempel er koblet til en Windows 10-datamaskin og strekkodepålogging er konfigurert for Modern POS, blir strekkodeskanneren aktiv på påloggingsskjermen. Ingen tilleggskonfigurasjon kreves. Flere klasser av UWP-enheter for salgssted legges til Windows. Disse klassene omfatter klasser for kassaskuffer og kvitteringsskrivere. Vi venter på støtte for disse nye enhetsklassene i Modern POS.

### <a name="keyboard-wedge"></a>Tastaturkortleser

Tastaturkortleserenheter sender data til datamaskinen som om dataene ble skrevet på et tastatur. Feltet som er aktivt på salgsstedet vil derfor motta dataene som skannes eller leses. I enkelte tilfeller kan denne virkemåten føre til at feil type data skannes inn i feil felt. En strekkode kan for eksempel skannes inn i et felt som er ment for registrering av kredittkortdata. I mange tilfeller er det logisk at det er salgsstedet som bestemmer om dataene som skannes eller leses, er en strekkode eller kortlesing. Derfor behandles dataene på riktig måte. Når enheter konfigureres som OPOS-enheter i stedet for tastaturkortleserenheter, er det imidlertid mer kontroll over hvordan dataene fra disse enhetene kan brukes, fordi mer er "kjent" om enheten som dataene kommer fra. Data fra en strekkodeskanner gjenkjennes for eksempel automatisk som en strekkode, og den tilknyttede posten i databasen finnes enklere og raskere enn hvis et søk etter en generell streng blir brukt, noe som er tilfelle for tastaturkortleserenheter.

### <a name="native-printer"></a>Opprinnelig skriver

Opprinnelige skrivere (eller "Enhet" som typen heter i maskinvareprofilen) kan konfigureres til å be brukeren om å velge en skriver som er konfigurert for datamaskinen. Når en skriver av **Enhet**-typen er konfigurert og Modern POS oppdager en utskriftskommando, blir brukeren bedt om å velge en skriver i en liste. Denne virkemåten er forskjellig fra virkemåten for Windows-drivere, fordi **Windows**-skrivertypen i maskinvareprofilen ikke viser en liste over skrivere. I stedet kreves det at en navngitt skriver angis i **Enhetsnavn**-feltet.

### <a name="windows"></a>Windows

**Windows**-enhetstypen brukes bare for skrivere. Når en Windows-skriveren er konfigurert i maskinvareprofilen, må det bestemte skrivernavnet angis. Når Modern POS registrerer utskrifthendelser og en Windows-skriver er konfigurert, vil hendelsen bli sendt til den angitte Windows-skriveren. Brukeren vil ikke bli bedt om å velge en skriver.

### <a name="network"></a>Nettverk

Nettverksadresserbare kassaskuffer, kvitteringsskrivere og betalingsterminaler kan brukes via et nettverk, direkte via IPC-maskinvarestasjonen som er bygget inn i Modern POS for Windows-programmet eller IIS-maskinvarestasjonen for andre Modern POS-klienter.

## <a name="hardware-station-deployment-options"></a>Distribusjonsalternativer for maskinvarestasjon

### <a name="ipc-built-in"></a>IPC (innebygd)

IPC-maskinvarestasjonen er bygget inn i Modern POS for Windows-programmet. Hvis du vil bruke IPC-maskinvarestasjonen, tilordner du en maskinvareprofil til en kasse som skal bruke Modern POS for Windows-programmet. Deretter oppretter du en maskinvarestasjon av **Dedikert**-typen for butikken der kassen skal brukes. Når du starter Modern POS, vil IPC-maskinvarestasjonen være aktiv, og POS-enheter som er konfigurert, vil være klare til bruk. Hvis du midlertidig ikke trenger den lokale maskinvaren, kan du bruke operasjonen **Administrer maskinvarestasjoner** for å deaktivere funksjonene for maskinvarestasjon. Modern POS kan også bruke IPC-maskinvarestasjonen til å kommunisere direkte med nettverksenheter.

### <a name="iis"></a>IIS

Du kan bruke IIS eller en frittstående versjon av maskinvarestasjonen på to måter. Beskrivelsen "IIS" betyr at POS-programmet kobler til maskinvarestasjonen via Microsoft Internet Information Services. POS-programmet kobler til IIS-maskinvarestasjonen via webtjenester som kjører på en datamaskin der enheten er tilkoblet. Når IIS brukes, kan eksterne enheter for detaljhandel, som er koblet til en maskinvarestasjonen, brukes av alle kasser på salgsstedet som er på samme nettverk som IIS-maskinvarestasjonen. Siden bare Modern POS for Windows inneholder innebygd støtte for detaljhandelsenheter, må alle andre Modern POS-programmer bruke IIS-maskinvarestasjonen til å kommunisere med POS-enheter som er konfigurert i maskinvareprofilen. Derfor krever hver forekomst av IIS-maskinvarestasjonen en datamaskin som kjører webtjenesten, og programmet som kommuniserer med enhetene. IIS-maskinvarestasjonen er nødvendig for alle Modern POS-programmer som ikke er for Windows.

#### <a name="dedicated"></a>Dedikert

Modern POS bruker maskinvarestasjoner av **Dedikert**-typen for å registrere at eksterne enheter kobles direkte til datamaskinen der programmet brukes. **Dedikert**-typen kan imidlertid også brukes for IIS-maskinvarestasjoner. I et tradisjonelt, fast POS-scenario som bruker Cloud POS som POS-program, brukes **Dedikert**-typen for maskinvarestasjon for IIS-maskinvarestasjoner som er distribuert på samme datamaskin som kjører Cloud POS. Den dedikerte IIS-maskinvarestasjonen har bedre ekstern støtte for tradisjonell, faste POS-scenarier for detaljhandelsenheter. Dedikerte maskinvarestasjoner støtter alle eksterne enheter som støttes i maskinvareprofilen.

#### <a name="shared"></a>Delt

Delte maskinvarestasjoner er ment å brukes av flere POS-enheter i løpet av dagen. Delte maskinvarestasjoner er optimalisert til å støtte bare kassaskuffer, kvitteringsskrivere og betalingsterminaler. Du kan ikke koble til direkte frittstående strekkodeskannere, kortlesere, linjevisningsenheter, vekter eller andre enheter. Da vil det oppstå konflikter når flere POS-enheter prøver å gjøre krav på de eksterne enhetene samtidig. Slik håndteres konflikter for enheter som støttes:

- **Kassaskuff** – Kassaskuffen åpnes via en hendelse som sendes til enheten. Det eneste problemet som kan oppstå når en kassaskuff kalles, oppstår hvis kassaskuffen allerede et åpen. For delte maskinvarestasjoner skal kassaskuffen settes til **Delt** i maskinvareprofilen. Denne innstillingen hindrer at salgsstedet kontrollerer om kassaskuffen allerede er åpen når det sendes åpne-kommandoer.
- **Kvitteringsskriver** – Hvis to kommandoer for kvitteringsskriver sendes samtidig til maskinvarestasjonen, kan én av kommandoene gå tapt, avhengig av enheten. Noen enheter har internt minnet eller gruppering som kan hindre dette problemet. Hvis en utskriftskommando ikke kan fullføres, mottar kassereren en feilmelding og kan prøve utskriftskommandoen på nytt ut fra salgsstedet.
- **Betalingsterminal** – Hvis en kasserer forsøker å utføre en betalingstransaksjon på en betalingsterminal som allerede er i bruk, vises en melding som varsler om at terminalen er i bruk og spør kassereren om å prøve på nytt senere. Kasserere kan vanligvis se at en terminal er allerede i bruk, slik at de kan vente til den andre transaksjonen er fullført før de prøver å betale på nytt.

Validering er planlagt for en fremtidig versjon for å registrere om enheter som ikke støttes, er konfigurert for en maskinvareprofil som er tilordnet en delt maskinvarestasjon. Hvis det blir funnet enheter som ikke støttes, vil brukeren motta en melding om at enhetene ikke støttes for delte maskinvarestasjoner. For delte maskinvarestasjoner blir alternativet **Velg ved betaling** satt til **Ja** på kassanivå. Salgsstedsbrukeren blir deretter bedt om å velge en maskinvarestasjon når et betalingsmiddel er valgt for en transaksjon på salgsstedet. Når maskinvarestasjonen velges samtidig som betalingsmiddel, blir valget av maskinvarestasjonen lagt til direkte i salgsstedsarbeidsflyten for mobile scenarier. Som en ekstra fordel brukes ikke linjevisningsenheten på betalingsterminalen i delte scenarier. Hvis betalingensterminalen brukes som en linjevisningsenhet, kan andre brukere bli blokkert fra å bruke denne terminalen til transaksjonen er fullført. I mobile scenarier kan linjer legges til en transaksjon over en lengre periode. Derfor er alternativet **Velg ved betaling** nødvendig for å sikre optimal tilgjengelig for enheten.

### <a name="network-peripherals"></a>Nettverksenheter

Nettverksangivelsen for enheter i maskinvareprofilen lar kassaskuffer, kvitteringsskrivere og betalingsterminaler kobles til via en nettverkstilkobling.

#### <a name="modern-pos-for-windows"></a>Moderne salgssted for Windows

Du kan angi IP-adresser for nettverksenheter på to steder. Hvis Modern POS-Windows-klienten bruker ett enkelt sett med nettverksenheter, må du angi IP-adressene for disse enhetene ved hjelp av alternativet **IP-konfigurasjon** i handlingsruten for selve kassen. For nettverksenheter som skal deles mellom kasser på salgsstedet, kan en maskinvareprofil som er tilordnet nettverksenheter, tilordnes direkte til en delt maskinvarestasjon. Hvis du vil tildele IP-adresser, velger du denne maskinvarestasjonen på siden **Detaljhandelbutikker**, og deretter bruke du alternativet **IP-konfigurasjon** i delen **Maskinvarestasjoner** for å angi nettverksenhetene som er tilordnet til denne maskinvarestasjonen. For maskinvarestasjoner som bare har nettverksenheter trenger du ikke å distribuere selve maskinvarestasjonen. I slike tilfeller kreves maskinvarestasjonen bare for å begrepsmessig gruppere nettverksadresserbare enheter i henhold til deres plassering i detaljhandelsbutikken.

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>Cloud POS, Modern POS for iOS og Modern POS for Android

Logikken som styrer fysisk tilkoblede og nettverksadresserbare enheter finnes i maskinvarestasjonen. For alle salgsstedsklienter bortsett fra Modern POS for Windows, må derfor en IIS-maskinvarestasjon distribueres og aktives for å aktivere kommunikasjon mellom salgsstedet og eksterne enheter, uavhengig av om de eksterne enhetene er fysisk koblet til en maskinvarestasjon eller adresseres over nettverket.

## <a name="setup-and-configuration"></a>Oppsett og konfigurasjon

### <a name="hardware-station-installation"></a>Installasjon av maskinvarestasjon

Hvis du vil ha mer informasjon, kan du se [Konfigurere og installere maskinvarestasjon for detaljhandel](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Oppsett og konfigurasjon av Modern POS for Windows

Hvis du vil ha mer informasjon, kan du se [Konfigurasjon og installasjon av Retail Modern POS](retail-modern-pos-device-activation.md).

### <a name="opos-device-setup-and-configuration"></a>Oppsett og konfigurasjon av OPOS-enhet

Hvis du vil ha mer informasjon om OPOS-komponenter, kan du se delen "Grensesnitt som støttes" i dette dokumentet. OPOS-drivere leveres vanligvis av produsenten av enheten. Når en OPOS-enhetsdriver er installert, legger den til en nøkkel i Windows-registret på én av følgende plasseringer:

- **32-biters system**: HKEY\_LOCAL\_MACHINESOFTWAREOLEforRetailServiceOPOS
- **64-biters system**: HKEY\_LOCAL\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

I ServiceOPOS-registerplassering er konfigurerte enheter organisert i henhold til enhetsklassen OPOS. Flere enhetsdrivere lagres.

## <a name="supported-scenarios-by-hardware-station-type"></a>Scenarier som støttes etter maskinvarestasjonstype

### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Klientstøtte – IPC-maskinvarestasjon kontra IIS maskinvarestasjon

Tabellen nedenfor viser topologier og distribusjonsscenarier som støttes.

| Kunde      | IPC-maskinvarestasjon | IIS-maskinvarestasjon |
|-------------|----------------------|----------------------|
| Windows-app | Ja                  | Ja                  |
| Skybasert salgssted   | Nr.                   | Ja                  |
| Android     | Nr.                   | Ja                  |
| iOS         | Nr.                   | Ja                  |

### <a name="network-peripherals"></a>Nettverksenheter

Nettverksenheter kan støttes direkte gjennom maskinvarestasjonen som er bygd inn i Modern POS for Windows-appen. For alle andre klienter må du distribuere en IIS-maskinvarestasjon.

| Kunde      | IPC-maskinvarestasjon | IIS-maskinvarestasjon |
|-------------|----------------------|----------------------|
| Windows-app | Ja                  | Ja                  |
| Skybasert salgssted   | Nr.                   | Ja                  |
| Android     | Nr.                   | Ja                  |
| iOS         | Nr.                   | Ja                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Enhetstyper som støttes av maskinvarestasjonstype

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Moderne POS for Windows med en IPC-maskinvarestasjon (innebygd)

<table>
<thead>
<tr>
<th>Enhetsklasse som støttes</th>
<th>Grensesnitt som støttes</th>
</tr>
</thead>
<tbody>
<tr>
<td>Skriver</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows-driver</li>
<li>Enhet</li>
<li>Nettverk</li>
</ul>
</td>
</tr>
<tr>
<td>Skriver 2</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows-driver</li>
<li>Enhet</li>
<li>Nettverk</li>
</ul>
</td>
</tr>
<tr>
<td>Linjevisning</td>
<td>OPOS</td>
</tr>
<tr>
<td>Dobbel visning</td>
<td>Windows-driver</td>
</tr>
<tr>
<td>Kortleser</td>
<td>
<ul>
<li>OPOS</li>
<li>UWP (krever ikke oppsett)</li>
<li>Tastaturkortleser (krever ikke oppsett)</li>
</ul>
</td>
</tr>
<tr>
<td>Trassent</td>
<td>
<ul>
<li>OPOS</li>
<li>Nettverk
<p><strong>Merk:</strong> Bare én skuff kan defineres hvis <strong>Bruk delte skift</strong> er konfigurert på skuffen.</p>
</li>
</ul>
</td>
</tr>
<tr>
<td>Skuff 2</td>
<td>
<ul>
<li>OPOS</li>
<li>Nettverk
<p><strong>Merk:</strong> Bare én skuff kan defineres hvis <strong>Bruk delte skift</strong> er konfigurert på skuffen.</p>
</li>
</ul>
</td>
</tr>
<tr>
<td>Skanner</td>
<td>
<ul>
<li>OPOS</li>
<li>UWP (krever ikke oppsett)</li>
<li>Tastaturkortleser (krever ikke oppsett)</li>
</ul>
</td>
</tr>
<tr>
<td>Skanner 2</td>
<td>
<ul>
<li>OPOS</li>
<li>UWP (krever ikke oppsett)</li>
<li>Tastaturkortleser (krever ikke oppsett)</li>
</ul>
</td>
</tr>
<tr>
<td>Skaler</td>
<td>OPOS</td>
</tr>
<tr>
<td>PIN-kodetastatur</td>
<td>OPOS (det gis støtte gjennom tilpasning av betalingskoblingen)</td>
</tr>
<tr>
<td>Signaturregistrering</td>
<td>OPOS</td>
</tr>
<tr>
<td>Betalingsterminal </td>
<td>
<ul>
<li>Støtte for egendefinerte enheter</li>
<li>Nettverk (Hvis du vil ha mer informasjon om sporing, kan du se koblingsdokumentasjonen.)</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Alle Modern POS-klienter som har en dedikert IIS-maskinvarestasjon

> [!NOTE]
> Når IIS-maskinvarestasjonen er "dedikert", er det et 1-1-relasjon mellom salgsstedsklienten og maskinvarestasjonen.

<table>
<thead>
<tr>
<th>Enhetsklasse som støttes</th>
<th>Grensesnitt som støttes</th>
</tr>
</thead>
<tbody>
<tr>
<td>Skriver</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows-driver
<p><strong>Merk:</strong> For Windows-skrivere på et nettverk må brukeren av maskinvarestasjonen har tilgang til skriveren.</p>
</li>
<li>Nettverk</li>
</ul>
</td>
</tr>
<tr>
<td>Skriver 2</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows-driver</li>
<li>Nettverk</li>
</ul>
</td>
</tr>
<tr>
<td>Linjevisning</td>
<td>OPOS</td>
</tr>
<tr>
<td>Kortleser</td>
<td>OPOS</td>
</tr>
<tr>
<td>Trassent</td>
<td>
<ul>
<li>OPOS</li>
<li>Nettverk
<p><strong>Merk:</strong> Bare én skuff per maskinvareprofil kan defineres hvis <strong>Bruk delte skift</strong> er konfigurert på skuffen.</p>
</li>
</ul>
</td>
</tr>
<tr>
<td>Skuff 2</td>
<td>
<ul>
<li>OPOS</li>
<li>Nettverk</li>
</ul>
</td>
</tr>
<tr>
<td>Skanner</td>
<td>OPOS</td>
</tr>
<tr>
<td>Skanner 2</td>
<td>OPOS</td>
</tr>
<tr>
<td>Skaler</td>
<td>OPOS</td>
</tr>
<tr>
<td>PIN-kodetastatur</td>
<td>OPOS (det gis støtte gjennom tilpasning av betalingskoblingen)</td>
</tr>
<tr>
<td>Sig. registrering</td>
<td>OPOS</td>
</tr>
<tr>
<td>Betalingsterminal </td>
<td>
<ul>
<li>Støtte for egendefinerte enheter</li>
<li>Nettverk (Hvis du vil ha mer informasjon om sporing, kan du se koblingsdokumentasjonen.)</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Alle Modern POS-klienter som har en delt IIS-maskinvarestasjon

> [!NOTE]
> Når IIS-maskinvarestasjonen er "delt", kan flere enheter bruke maskinvarestasjonen samtidig. I slike scenarier bør du bruke bare enhetene som vises i tabellen nedenfor. Hvis du prøver å dele enheter som ikke vises her, for eksempel strekkodeskannere og kortlesere, vil det oppstå feil når flere enheter forsøker å kreve den samme eksterne enheten. I fremtiden vil en slik konfigurasjon bli eksplisitt forhindret.

<table>
<thead>
<tr>
<th>Enhetsklasse som støttes</th>
<th>Grensesnitt som støttes</th>
</tr>
</thead>
<tbody>
<tr>
<td>Skriver</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows-driver
<p><strong>Merk:</strong> For Windows-skrivere på et nettverk må brukeren av maskinvarestasjonen har tilgang til skriveren.</p>
</li>
<li>Nettverk</li>
</ul>
</td>
</tr>
<tr>
<td>Skriver 2</td>
<td>
<ul>
<li>OPOS</li>
<li>Windows-driver</li>
<li>Nettverk</li>
</ul>
</td>
</tr>
<tr>
<td>Trassent</td>
<td>
<ul>
<li>OPOS</li>
<li>Nettverk
<p><strong>Merk:</strong> Bare én skuff per maskinvareprofil kan defineres hvis <strong>Bruk delte skift</strong> er konfigurert på skuffen.</p>
</li>
</ul>
</td>
</tr>
<tr>
<td>Skuff 2</td>
<td>
<ul>
<li>OPOS</li>
<li>Nettverk</li>
</ul>
</td>
</tr>
<tr>
<td>Betalingsterminal </td>
<td>
<ul>
<li>Støtte for egendefinerte enheter</li>
<li>Nettverk (Hvis du vil ha mer informasjon om sporing, kan du se koblingsdokumentasjonen.)</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Konfigurasjon for scenarier som støttes

Hvis du vil ha mer informasjon om hvordan du kan opprette maskinvareprofiler, kan du se [Definere og vedlikeholde kanalklienter, inkludert kasser og maskinvarestasjoner](define-maintain-channel-clients-registers-hw-stations.md).

> [!NOTE]
> For Microsoft Dynamics 365 for Retail versjon 1611 brukes ikke maskinvarestasjonprofilen lenger. Egenskaper som du tidligere har definert i profilen for maskinvarestasjon, er nå en del av selve maskinvarestasjonen.

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Moderne POS for Windows med en IPC-maskinvarestasjon (innebygd)

Denne konfigurasjonen er mest vanlig konfigurasjonen for tradisjonelle, fast kasser på salgssted. I slike scenarier tilordnes profilinformasjonen for maskinvare direkte til selve kassen. EFT-terminalnummeret bør også angis for selve kassen. Følg fremgangsmåten nedenfor for å definere denne konfigurasjonen.

1. Opprett en maskinvareprofil der alle nødvendige enheter er konfigurert.
2. Tilordne maskinvareprofilen til kassen på salgsstedet.
3. Opprett en maskinvarestasjon av **Dedikert**-typen for detaljhandelsbutikken der kassen på salgsstedet skal brukes. Beskrivelse er valgfritt.

    > [!NOTE]
    > Du behøver ikke å angi eventuelle andre egenskaper for maskinvarestasjonen. All annen nødvendig informasjonen, for eksempel maskinvareprofilen, kommer fra selve kassen.

4. Klikk på **Detaljhandel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplan**.
5. Velg distribusjonsplanen **1090** for å synkronisere den nye maskinvareprofilen til butikken. Klikk på **Kjør nå** for å synkronisere endringer til salgsstedet.
6. Velg distribusjonsplanen **1040** for å synkronisere den nye maskinvarestasjonen til butikken. Klikk på **Kjør nå** for å synkronisere endringer til salgsstedet.
7. Installer og aktiver Modern POS for Windows.
8. Start Modern POS for Windows, og begynn å bruke de tilkoblede eksterne enhetene.

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Alle Modern POS-klienter som har en dedikert IIS-maskinvarestasjon

Denne konfigurasjonen kan brukes for alle Modern POS-klienter som har en maskinvarestasjon som brukes av bare én kasse på salgsstedet. Følg fremgangsmåten nedenfor for å definere denne konfigurasjonen.

1. Opprett en maskinvareprofil der alle nødvendige enheter er konfigurert.
2. Opprett en maskinvarestasjon av **Dedikert**-typen for detaljhandelsbutikken der kassen på salgsstedet skal brukes.
3. Angi følgende egenskaper for den dedikerte maskinvarestasjonen:

    - **Vertsnavn** – Navnet på vertsdatamaskinen der maskinvarestasjonen skal kjøres.

        > [!NOTE]
        > Cloud POS kan løse **localhost** for å finne den lokale datamaskinen der Cloud POS kjøres. Sertifikatet som kreves for å koble Cloud POS sammen med maskinvarestasjonen, må imidlertid også ha "Localhost" som navnet på datamaskinen. For å unngå problemer anbefaler vi at du angir en forekomst av hver dedikerte maskinvarestasjon for butikken etter behov. For hver enkelt maskinvarestasjon må vertsnavnet være navnet på den spesifikke datamaskinen der maskinvarestasjonen skal distribueres.

    - **Port** – Porten som skal brukes for kommunikasjon mellom maskinvarestasjonen og Modern POS-klienten.
    - **Maskinvareprofil** – Hvis maskinvareprofilen ikke er angitt på selve maskinvarestasjonen, brukes maskinvareprofilen som er tilordnet kassen.
    - **EFT-salgsstedsnummer** – EFT-terminal-ID-en skal brukes ved sending av EFT-autoriseringer. Denne ID-en leveres av kredittkortbehandleren.
    - **Pakkenavn** – Maskinvarestasjonspakken som skal brukes når maskinvarestasjonen distribueres.

4. Klikk på **Detaljhandel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplan**.
5. Velg distribusjonsplanen **1090** for å synkronisere den nye maskinvareprofilen til butikken. Klikk på **Kjør nå** for å synkronisere endringer til salgsstedet.
6. Velg distribusjonsplanen **1040** for å synkronisere den nye maskinvarestasjonen til butikken. Klikk på **Kjør nå** for å synkronisere endringer til salgsstedet.
7. Installer maskinvarestasjonen. Hvis du vil ha mer informasjon om hvordan du installerer maskinvarestasjonen, kan du se [Konfigurere og installere maskinvarestasjon for detaljhandel](retail-hardware-station-configuration-installation.md).
8. Installer og aktiver Modern POS. Hvis du vil ha mer informasjon om hvordan du installerer Modern POS, kan du se [Konfigurere og installere Retail Modern POS](retail-modern-pos-device-activation.md).
9. Logg på Modern POS, og velg **Utfør en ikke-skuff-operasjon**.
10. Start operasjonen **Administrer maskinvarestasjoner**.
11. Klikk på **Administrer**.
12. På siden for administrasjon av maskinvarestasjonen angir du alternativet for å aktivere maskinvarestasjonen.
13. Velg maskinvarestasjonen som skal brukes, og klikk deretter på **Par**.
14. Når maskinvarestasjonen er sammenkoblet, klikker du på **Lukk**.
15. På siden for valg av maskinvarestasjonen klikker du på den sist valgte maskinvarestasjonen for å aktivere den.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Alle Modern POS-klienter som har en delt IIS-maskinvarestasjon

Denne konfigurasjonen kan brukes for alle Modern POS-klienter som deler maskinvarestasjoner med andre enheter. Følg fremgangsmåten nedenfor for å definere denne konfigurasjonen.

1. Opprett en maskinvareprofil der nødvendige enheter er konfigurert.
2. Opprett en maskinvarestasjon av **Delt**-typen for detaljhandelsbutikken der kassen på salgsstedet skal brukes.
3. Angi følgende egenskaper for den delte maskinvarestasjonen:

    - **Vertsnavn** – Navnet på vertsdatamaskinen der maskinvarestasjonen skal kjøres.
    - **Beskrivelse** – Tekst som bidrar til å identifisere maskinvarestasjonen, for eksempel **Returer** eller **Butikkfront**.
    - **Port** – Porten som skal brukes for kommunikasjon mellom maskinvarestasjonen og Modern POS-klienten.
    - **Maskinvareprofil** – Hver enkelt delte maskinvarestasjon bør ha en maskinvareprofil. Maskinvareprofiler kan deles mellom maskinvarestasjoner, men de må være tilordnet hver maskinvarestasjon. I tillegg anbefaler vi at du bruker delte skift når flere enheter bruker den samme delte maskinvarestasjonen. Hvis du vil konfigurere et delt skift, klikker du på **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofiler** &gt; **Maskinvareprofiler**. Velg kassaskuffen for hver av de delte maskinvareprofilene, og sett alternativet **Skuff for delt skift** til **Ja**.
    - **EFT-salgsstedsnummer** – EFT-terminal-ID-en skal brukes ved sending av EFT-autoriseringer. Denne ID-en leveres av kredittkortbehandleren.
    - **Pakkenavn** – Maskinvarestasjonspakken som skal brukes når maskinvarestasjonen distribueres.

4. Gjenta trinn 2 og 3 for hver ekstra maskinvarestasjon som kreves i butikken.
5. Klikk på **Detaljhandel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplan**.
6. Velg distribusjonsplanen **1090** for å synkronisere den nye maskinvareprofilen til butikken. Klikk på **Kjør nå** for å synkronisere endringer til salgsstedet.
7. Velg distribusjonsplanen **1040** for å synkronisere den nye maskinvarestasjonen til butikken. Klikk på **Kjør nå** for å synkronisere endringer til salgsstedet.
8. Installer maskinvarestasjonen på hver vertsdatamaskin som du opprettet i trinn 2 og 3. Hvis du vil ha mer informasjon om hvordan du installerer maskinvarestasjonen, kan du se [Konfigurere og installere maskinvarestasjon for detaljhandel](retail-hardware-station-configuration-installation.md).
9. Installer og aktiver Modern POS. Hvis du vil ha mer informasjon om hvordan du installerer Modern POS, kan du se [Konfigurere og installere Retail Modern POS](retail-modern-pos-device-activation.md).
10. Logg på Modern POS, og velg **Utfør en ikke-skuff-operasjon**.
11. Start operasjonen **Administrer maskinvarestasjoner**.
12. Klikk på **Administrer**.
13. På siden for administrasjon av maskinvarestasjonen angir du alternativet for å aktivere maskinvarestasjonen.
14. Velg maskinvarestasjonen som skal brukes, og klikk deretter på **Par**.
15. Gjenta trinn 14 for hver maskinvarestasjon som Modern POS bruker.
16. Når all nødvendig maskinvarestasjoner er sammenkoblet, klikker du på **Lukk**.
17. På siden for valg av maskinvarestasjonen klikker du på den sist valgte maskinvarestasjonen for å aktivere den.

    > [!NOTE]
    > Hvis enheter ofte bruker forskjellig maskinvarestasjoner, anbefaler vi at du konfigurerer Modern POS til å spørre kasserere å velge en maskinvarestasjon når de begynner betalingsprosessen. Klikk **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Kasser**. Velg kassen, og sett deretter alternativet **Velg ved betalingen** til **Ja**. Bruk distribusjonsplanen **1090** for å synkronisere endringer i kanaldatabasen.

## <a name="extensibility"></a>Utvidelsesmuligheter

Hvis du vil ha informasjon om scenarier for utvidelsesmuligheter for maskinvarestasjonen, kan du se [Utvidelsesmuligheter for maskinvarestasjon](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Sikkerhet

Følgende innstillinger skal brukes i et produksjonsmiljø i henhold til gjeldende sikkerhetsstandarder:

> [!NOTE]
> Installasjonsprogrammet for maskinvarestasjonen vil automatisk gjøre disse registerendringene som en del av installasjonen gjennom selvbetjening.

- SSL (Secure Sockets Layer) må deaktiveres.
- Bare TLS (Transport Layer Security) versjon 1.2 (eller gjeldende nyeste versjon) skal være aktivert og brukes.

    > [!NOTE]
    > SSL og alle versjoner av TLS, unntatt TLS 1.2, er deaktivert som standard.

    Følg denne fremgangsmåten for å redigere eller aktivere disse verdiene:

    1. Trykke på Windows-logotasten+R for å åpne et **Kjør**-vindu.
    2. I **Åpne**-feltet skriver du inn **Regedit**, og deretter klikker du på **OK**.
    3. Hvis det vises en **Brukerkontokontroll**-melding, klikker du på **Ja**.
    4. I vinduet **Registerredigering** går du til **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Følgende nøkler er angitt automatisk for å bare tillate TLS 1.2:

        - TLS 1.2Server:Enabled=1
        - TLS 1.2Server:DisabledByDefault=0
        - TLS 1.2Client:Enabled=1
        - TLS 1.2Client:DisabledByDefault=0
        - TLS 1.1Server:Enabled=0
        - TLS 1.1Client:Enabled=0
        - TLS 1.0Server:Enabled=0
        - TLS 1.0Client:Enabled=0
        - SSL 3.0Server:Enabled=0
        - SSL 3.0Client:Enabled=0
        - SSL 2.0Server:Enabled=0
        - SSL 2.0Client:Enabled=0

- Ingen flere nettverksporter skal være åpne, med mindre de er nødvendige av kjente, angitte årsaker.
- Cross-origin-ressursdeling må være deaktivert og må angi de tillatte opprinnelsene som godtas.
- Bare klarerte sertifiseringsinstanser skal brukes til å skaffe sertifikater som skal brukes på datamaskiner som kjører maskinvarestasjonen.

> [!NOTE]
> Det er svært viktig at du ser gjennom retningslinjene for sikkerhet for IIS og kravene til betalingskortbransjen (PCI).

## <a name="peripheral-simulator"></a>Ekstern simulator

Hvis du vil ha mer informasjon, kan du se [Simulator for eksterne detaljhandelsenheter](dev-itpro/retail-peripheral-simulator.md).

## <a name="microsoft-tested-peripheral-devices"></a>Microsoft-testede eksterne enheter

### <a name="ipc-built-in-hardware-station"></a>IPC-maskinvarestasjon (innebygd)

De eksterne enhetene nedenfor ble testet ved hjelp av IPC-maskinvarestasjonen som er bygget inn i Modern POS for Windows.

#### <a name="printer"></a>Skriver

| Produsent | Modell    | Grensesnitt | Kommentarer                |
|--------------|----------|-----------|-------------------------|
| Epson        | Tm-T88IV | OPOS      |                         |
| Epson        | TM-T88V  | OPOS      |                         |
| Star         | TSP650II | OPOS      |                         |
| Star         | TSP650II | Egendefinert    | Tilkoblet via nettverket   |
| Star         | mPOP     | OPOS      | Tilkoblet via Bluetooth |
| HP           | F7M67AA  | OPOS      | USB-drevet             |

#### <a name="bar-code-scanner"></a>Strekkodeleser

| Produsent  | Modell         | Grensesnitt | Kommentarer |
|---------------|---------------|-----------|----------|
| Motorola      | DS9208        | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| Symbol        | LS2208        | OPOS      |          |
| HP-integrert | E1L07AA       | OPOS      |          |
| Datalogic     | Magellan 8400 | OPOS      |          |

#### <a name="pin-pad"></a>PIN-kodetastatur

| Produsent | Modell  | Grensesnitt | Kommentarer                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Krever tilpassing av betalingskoblingen |

#### <a name="payment-terminal"></a>Betalingsterminal 

| Produsent | Modell | Grensesnitt | Kommentarer                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Egendefinert    | Krever tilpassing av betalingskoblingen                                |
| VeriFone     | MX925 | Egendefinert    | Krever tilpassing av betalingskoblingen, tilkobling via nettverk og USB |
| VeriFone     | MX915 | Egendefinert    | Krever tilpassing av betalingskoblingen, tilkobling via nettverk og USB |

#### <a name="cash-drawer"></a>Kassaskuff

| Produsent | Modell     | Grensesnitt | Kommentarer                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Tilkoblet via Bluetooth |
| APG          | Atwood    | Egendefinert    | Tilkoblet via nettverket   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |

#### <a name="line-display"></a>Linjevisning

| Produsent  | Modell   | Grensesnitt | Kommentarer |
|---------------|---------|-----------|----------|
| HP-integrert | G6U79AA | OPOS      |          |
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

### <a name="dedicated-iis-hardware-station"></a>Dedikert IIS-maskinvarestasjon

De eksterne enhetene nedenfor ble testet ved hjelp av en dedikert (ikke delt) IIS-maskinvarestasjon sammen med Modern POS for Windows og Cloud POS.

#### <a name="printer"></a>Skriver

| Produsent | Modell    | Grensesnitt | Kommentarer                  |
|--------------|----------|-----------|---------------------------|
| Epson        | Tm-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Egendefinert    | Tilkoblet via nettverket     |
| HP           | F7M67AA  | OPOS      | USB-drevet               |

#### <a name="bar-code-scanner"></a>Strekkodeleser

| Produsent  | Modell   | Grensesnitt | Kommentarer |
|---------------|---------|-----------|----------|
| Motorola      | DS9208  | OPOS      |          |
| Symbol        | LS2208  | OPOS      |          |
| HP-integrert | E1L07AA | OPOS      |          |

#### <a name="pin-pad"></a>PIN-kodetastatur

| Produsent | Modell  | Grensesnitt | Kommentarer                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Krever tilpassing av betalingskoblingen |

#### <a name="payment-terminal"></a>Betalingsterminal 

| Produsent | Modell | Grensesnitt | Kommentarer                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Egendefinert    | Krever tilpassing av betalingskoblingen                                |
| VeriFone     | MX925 | Egendefinert    | Krever tilpassing av betalingskoblingen, tilkobling via nettverk og USB |
| VeriFone     | MX915 | Egendefinert    | Krever tilpassing av betalingskoblingen, tilkobling via nettverk og USB |

#### <a name="cash-drawer"></a>Kassaskuff

| Produsent | Modell     | Grensesnitt | Kommentarer              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Egendefinert    | Tilkoblet via nettverket |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

#### <a name="line-display"></a>Linjevisning

| Produsent  | Modell   | Grensesnitt | Kommentarer |
|---------------|---------|-----------|----------|
| HP-integrert | G6U79AA | OPOS      |          |
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

### <a name="shared-iis-hardware-station"></a>Delt IIS-maskinvarestasjon

De eksterne enhetene nedenfor ble testet ved hjelp av en delt IIS-maskinvarestasjon sammen med Modern POS for Windows og Cloud POS.

> [!NOTE]
> Bare en skriver, betalingsterminal og kassaskuff støttes.

#### <a name="printer"></a>Skriver

| Produsent | Modell    | Grensesnitt | Kommentarer                  |
|--------------|----------|-----------|---------------------------|
| Epson        | Tm-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Egendefinert    | Tilkoblet via nettverket     |
| HP           | F7M67AA  | OPOS      | USB-drevet               |

#### <a name="payment-terminal"></a>Betalingsterminal 

| Produsent | Modell | Grensesnitt | Kommentarer                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Egendefinert    | Krever tilpassing av betalingskoblingen, tilkobling via nettverk og USB |
| VeriFone     | MX915 | Egendefinert    | Krever tilpassing av betalingskoblingen, tilkobling via nettverk og USB |

#### <a name="cash-drawer"></a>Kassaskuff

| Produsent | Modell     | Grensesnitt | Kommentarer              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Egendefinert    | Tilkoblet via nettverket |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

## <a name="troubleshooting"></a>Feilsøking

### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Modern POS kan gjenkjenne maskinvarestasjonen i listen for valg, men kan ikke fullføre sammenkoblingen

**Løsning**: Kontroller følgende liste over potensielle feil:

- Datamaskinen som kjører Modern POS klarerer sertifikatet som brukes på datamaskinen som kjører maskinvarestasjonen.

    - Hvis du vil kontrollere dette oppsettet, kan du gå til følgende URL-adresse i en nettleser: `https://<Computer Name>:<Port Number>/HardwareStation/ping`.
    - Denne nettadressen bruker en ping-kommando til å kontrollere at det er tilgang til datamaskinen, og nettleseren angir om sertifikatet er klarert. (Eksempel: I Internet Explorer vises et låseikon på adresselinjen. Når du klikker på dette ikonet, kontrollerer Internet Explorer om sertifikatet er klarert. Du kan installere sertifikatet på den lokale datamaskinen ved å vise detaljene for sertifikatet som vises.)

- På datamaskinen som kjører maskinvarestasjonen blir porten som skal brukes av maskinvarestasjonen, åpnet i brannmuren.
- Maskinvarestasjonen har riktig installert forhandlerkontoinformasjon gjennom Installer forhandlerinformasjon-verktøyet som kjører på slutten av installasjonsprogrammet for maskinvarestasjonen.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Modern POS gjenkjenner ikke maskinvarstasjonen i listen over valg

**Løsning**: Én av følgende faktorer kan forårsake dette problemet:

- Maskinvarestasjonen ikke er riktig konfigurert i hovedkontorene. Bruk fremgangsmåten tidligere i dette emnet for å kontrollere at det er angitt riktig profil for maskinvarestasjon og maskinvarestasjon.
- Jobbene er ikke kjørt for å oppdatere kanalkonfigurasjonen. I slike tilfeller kjører du 1070-jobben for kanalkonfigurasjon.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Modern POS gjenspeiler ikke nye innstillinger for kassaskuff

**Løsning**: Lukk gjeldende bunke. Endringer i kassaskuffen oppdateres ikke til Modern POS før gjeldende bunke er lukket.

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Modern POS rapporterer et problem med en ekstern enhet for detaljhandel

**Løsning**: Her er noen vanlige årsaker til dette problemet:

- Kontroller at andre konfigurasjonsverktøy for enhetsdriver er lukket. Hvis disse verktøyene er åpne, kan de hindre at Modern POS eller maskinvarestasjonen krever enheten.
- Hvis den eksterne enheten for detaljhandel deles av flere POS-enheter, må du kontrollere at den tilhører én av følgende kategorier:

    - Kassaskuff
    - Kvitteringsskriver
    - Betalingsterminal 

    Hvis den eksterne enheten ikke tilhører én av disse kategoriene, er ikke maskinvarestasjonen utformet for å aktivere deling av den eksterne enheten mellom flere POS-enheter.

- Enhetsdrivere kan noen ganger føre til at Common Control Objects (CCO-er) slutter å fungere slik de skal. Hvis en enhet nylig er installert, men den ikke fungerer slik den skal eller du legger merke til andre problemer, kan du ofte løse problemet ved å installere CCO-er. Du kan laste ned CCO-er ved å gå til <http://monroecs.com/oposccos_current.htm>.
- Hvis du ofte endrer eksterne enheter under testing eller feilsøking, må du kanskje tilbakestille IIS i stedet for å vente på at hurtigbufferen skal oppdatere seg selv. Følg denne fremgangsmåten for å tilbakestille IIS:

    1. Skriv inn **CMD** på **Start**-menyen.
    2. Høyreklikk **Ledetekst** i søkeresultatet, og klikk deretter på **Kjør som administrator**.
    3. I **Ledetekst**-vinduet skriver du inn **iisreset /Restart** og trykker deretter på Enter.
    4. Når IIS er startet på nytt, starter du Modern POS på nytt.

- Hvis du ofte endrer eksterne enheter og du også ofte starter og avslutter POS-klienten, kan dllhost-prosessen fra en tidligere POS-økt påvirke gjeldende økt. I slike tilfeller kan en enhet ikke brukes før du lukker DLL-verten som administrerer den forrige økten. Følg denne fremgangsmåten for å lukke DLL-verten:

    1. Skriv inn **Oppgavebehandling** på **Start**-menyen.
    2. Klikk på **Oppgavebehandling** i søkeresultatene.
    3. I kategorien **Detaljer** i Oppgavebehandling, klikker du på kolonneoverskriften som er merket **Navn** for å sortere tabellen alfabetisk etter navn.
    4. Rull nedover til du finner dllhost.exe.
    5. Velg hver enkelt DLL-vert, og klikk deretter på **Avslutt oppgave**.
    6. Når DLL-vertene er avsluttet, starter du Modern POS på nytt.

## <a name="additional-resources"></a>Tilleggsressurser

[Simulator for eksterne enheter for Retail](dev-itpro/retail-peripheral-simulator.md)

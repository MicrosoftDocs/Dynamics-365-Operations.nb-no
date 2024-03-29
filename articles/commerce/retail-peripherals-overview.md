---
title: Eksterne enheter
description: Denne artikkelen forklarer begrepene som er knyttet til eksterne enheter i Commerce.
author: BrianShook
ms.date: 09/08/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.custom:
- "268444"
- intro-internal
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b3113626b18ad7f074c808d7631d13b09071bef2
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460001"
---
# <a name="peripherals"></a>Eksterne enheter

[!include[banner](includes/banner.md)]

Denne artikkelen forklarer begrepene som er knyttet til eksterne enheter i butikker. Det beskriver ulike måter enheter kan kobles til salgsstedet og komponentene som er ansvarlig for å administrere tilkoblingen til salgsstedet.

## <a name="concepts"></a>Begreper

### <a name="pos-registers"></a>Kasser på salgssted

Navigasjon: Gå til **Detaljhandel og handel \> Kanaloppsett \> Salgsstedsoppsett \> Kasser**. Kassen på salgsstedet er en enhet som brukes til å definere egenskapene til en bestemt forekomst av salgsstedet. Disse egenskapene inkluderer maskinvareprofilen eller oppsettet for eksterne enheter som skal brukes i kassen, butikken som kassen er tilordnet og den visuelle opplevelsen for brukeren som logger på kassen.

### <a name="devices"></a>Enheter

Navigasjon: Gå til **Detaljhandel og handel \> Kanaloppsett \> Salgsstedsoppsett \> Enheter**. En enhet er en enhet som representerer en fysisk forekomst av en enhet som er tilordnet en kasse på salgsstedet. Når en enhet opprettes, tilordnes den til en kasse på salgsstedet. Enhetsenheten registrerer informasjon om når en kasse på salgsstedet aktiveres, klienttypen som brukes og programpakken som er distribuert til en bestemt enhet. 

Enheter som kan tilordnes til følgende apptyper: Retail Modern POS, Retail Cloud POS, Retail Modern POS – Android og Retail Modern POS – iOS.

### <a name="modern-pos"></a>Moderne salgssted

Modern POS er POS-programmet for Microsoft Windows. Den kan distribueres på operativsystemene Windows 10 og Windows 11.

### <a name="cloud-pos"></a>Cloud POS

Cloud POS er en webbasert versjon av Modern POS-programmet som kan åpnes i en nettleser.

### <a name="modern-pos-for-ios"></a>Modern POS for iOS

Modern POS for iOS er en iOS-basert versjon av Modern POS-programmet som kan distribueres på iOS-enheter.

### <a name="modern-pos-for-android"></a>Modern POS for Android

Modern POS for Android er en Android-basert versjon av Modern POS-programmet som kan distribueres på Android-enheter.

### <a name="pos-peripherals"></a>POS-enheter

POS-enheter er enheter som er eksplisitt støttes for POS-funksjoner. Disse eksterne enhetene deles vanligvis inn i bestemte klasser. Hvis du vil ha mer informasjon om disse klassene, kan du se delen "Enhetsklasser" i denne artikkelen.

### <a name="hardware-station"></a>Maskinvarestasjon

Navigasjon: Gå til **Detaljhandel og handel \> Kanaler \> Butikker \> Alle butikker**. Velg en butikk, og velg deretter hurtigfanen **Maskinvarestasjoner**. Innstillingen **Maskinvarestasjon** er en innstilling på kanalnivå som brukes til å definere forekomster der ekstern logikk skal distribueres. Denne innstillingen på kanalnivå, brukes til å bestemme egenskapene til maskinvarestasjonen. Den brukes også til å vise maskinvarestasjoner som er tilgjengelige for en Modern POS-forekomst i et angitt lager. Maskinvarestasjonen er bygget inn i Modern POS-programmer for Windows og Android. Maskinvarestasjonen kan også distribueres uavhengig som et frittstående program for Microsoft Internet Information Services (IIS). I slike tilfeller er det tilgang via et nettverk.

### <a name="hardware-profile"></a>Maskinvareprofil

Navigasjon: Gå til **Detaljhandel og handel \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Maskinvareprofiler**. Maskinvareprofilen er en liste over enheter som er konfigurert for en kasse på salgssted eller en maskinvarestasjon. Maskinvareprofilen tilordnes direkte til en kasse på salgsstedet eller til en maskinvarestasjon.

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

### <a name="scale"></a>Skala

Veker kan kobles til datamaskinen via USB ved hjelp av OPOS-drivere. Når et produkt som er merket som et "veid" produkt legges til i en transaksjon, leser salgsstedet vekten fra vekten, legger til produktet i transaksjonen og bruker mengden som er angitt av vekten.

### <a name="pin-pad"></a>PIN-kodetastatur

PIN-kodetastaturer støttes gjennom OPOS, men de må administreres via en betalingstilkobling.

### <a name="secondary-display"></a>Sekundær skjerm

Når en sekundær skjerm er konfigurert, brukes Windows-skjermen nummer to til å vise grunnleggende informasjon. Den sekundære skjermen kan som standard ikke konfigureres, og viser begrenset innhold. Formålet med den sekundære skjermen er å støtte en utvidelse fra en uavhengig programvareleverandør. 

### <a name="payment-device"></a>Betalingsenhet

Støtte for betalingsenheter er implementert via betalingskoblingen. Betalingsenheter kan utføre én eller mange av funksjonene som andre enhetsklasser leverer. En betalingsenhet kan for eksempel fungere som en kortleser, linjevisningsenhet, registreringsenhet for signatur eller PIN-kodetastatur. Støtte for betalingsenheter implementeres uavhengig av støtte for frittstående enheter som er tilgjengelig for andre enheter som er inkludert i maskinvareprofilen.

## <a name="supported-interfaces"></a>Grensesnitt som støttes
### <a name="opos"></a>OPOS

For å garantere at et størst mulig utvalg av enheter kan brukes med Commerce, er industristandarden OLE for POS den primære plattformen for eksterne enheter som støttes. OLE for POS-standarden ble produsert ved den National Retail Federation (NRF), som etablerer industristandard kommunikasjonsprotokoller for eksterne enheter. OPOS er en mye brukte implementering av OLE for POS-standarden. Den ble utviklet på midten av 1990-tallet, og har blitt oppdatert flere ganger siden da. OPOS gir en enhetsdriverarkitektur som gir enkel integrering av POS-maskinvare med Windows-baserte POS-systemer. OPOS-kontroller håndterer kommunikasjon mellom kompatibel maskinvare og POS-programvare. En OPOS-kontroll består av to deler:

-   **Kontrollobjekt** – Kontrollobjektet for en enhetsklasse (for eksempel linjevisningsenheter) inneholder grensesnittet for programmet. Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) leverer et standardisert sett med OPOS-kontrollobjekter som kalles Common Control Objects (CCO-er). CCOs brukes til å teste POS-komponenten i Commerce. Derfor bidrar testingen til å garantere at hvis Commerce støtter en enhetsklasse gjennom OPOS, kan mange enhetstyper støttes, forutsatt at produsenten leverer et tjenesteobjekt som er bygget for OPOS. Du trenger ikke å eksplisitt teste hver enhetstype.
-   **Tjenesteobjekt** – Tjenesteobjektet leverer kommunikasjon mellom kontrollobjektet (CCO) og enheten. Tjenesteobjektet for en enhet leveres vanligvis av enhetsprodusenten. I noen tilfeller må du imidlertid laste ned tjenesteobjektet fra produsentens nettsted. Et nyere tjenesteobjekt kan for eksempel være tilgjengelig. Hvis du vil finne adressen til produsentens nettsted, kan du se i maskinvaredokumentasjonen.

[![Kontrollobjekt og tjenesteobjekt.](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) Støtte for OPOS-implementering av OLE for POS bidrar til å garantere at hvis enhetsprodusentene og POS-utgivere implementerer standarden på riktig måte, kan POS-systemer og støttede enheter samarbeide, selv om de ikke var tidligere testet sammen. 

> [!NOTE]
> OPOS-støtte garanterer ikke støtte for alle enheter som har OPOS-drivere. Commerce må først støtte denne enhetstypen, eller klassen, gjennom OPOS. I tillegg er tjenesteobjekter kanskje ikke alltid oppdaterte med den nyeste versjonen av CCO-er. Du må også være oppmerksom på at kvaliteten på tjenesteobjekter vanligvis varierer.

### <a name="windows"></a>Windows

Kvitteringsutskrift på salgsstedet er optimalisert for OPOS. OPOS pleier å være mye raskere enn utskrift i Windows. Det er derfor smart å bruke OPOS, spesielt i miljøer der 40-kolonners kvitteringer skrives ut og transaksjonen må gjennomføres raskt. Du bruker OPOS-kontroller for de fleste enheter. Noen OPOS-kvitteringsskrivere støtter imidlertid også Windows-drivere. Ved å bruke en Windows-driver, har du tilgang til de nyeste skriftene og en nettverksskriveren for flere kasser. Det er imidlertid ulemper med å bruke Windows-drivere. Her er noen eksempler på disse ulempene:

-   Når du bruker Windows-drivere, gjengis bilder før utskrift. Derfor pleier utskrift å være langsommere enn på skrivere som bruker OPOS-kontroller.
-   Enheter som er koblet gjennom skriveren ("seriekoblet") fungerer kanskje ikke slik de skal når Windows-drivere brukes. Kassaskuffen åpnes for eksempel kanskje ikke, eller kvitteringsskriveren fungerer kanskje ikke som forventet.
-   OPOS støtter også et mer omfattende sett med variabler som er spesifikke for kvitteringsskrivere, for eksempel papirkutting eller følgeseddelutskrift.
-   Windows-skrivere støttes ikke gjennom IIS-maskinvarestasjonen. 

Hvis OPOS-kontroller er tilgjengelige for Windows-skriveren du bruker, skal skriveren fungere riktig med Commerce.

### <a name="plug-and-play-devices"></a>Plug and play-enheter

Når en Plug and Play-enhet er koblet til en Windows-operativsystemversjon som støtter denne typen enhet, kreves ingen driver for at enheten skal brukes som ment. Hvis Windows for eksempel oppdager en Bluetooth-høyttalerenhet, vet operativsystemet at enheten har klassetypen "Høyttaler", og behandler denne enheten som en høyttaler. Ingen tilleggskonfigurasjon kreves. 

Mange eksterne USB-enheter for salgssted kan kobles til, og de gjenkjennes av Windows som enheter for menneskelig grensesnitt (HID-er). Det kan imidlertid hende at Windows ikke kan fastslå hvilke funksjoner enheten leverer, fordi enheten ikke angir klassen eller typen enhet. I Windows 10 er det lagt til enhetsklasser for strekkodeskannere og kortlesere. Hvis en enhet deklarerer seg selve for Windows 10 som en enhet av en av disse klassene, vil Windows derfor lytte etter hendelser fra enheten på riktige tidspunkt.

Modern POS støtter UWP-kortlesere og -skannere. Når Modern POS er klart for inndata fra en av disse enhetene og en enhet som tilhører en av disse enhetsklassene er tilkoblet, kan enheten derfor brukes. Hvis en Plug and Play-strekkodeskanner for eksempel er koblet til en Windows 10-datamaskin og strekkodepålogging er konfigurert for Modern POS, blir strekkodeskanneren aktiv på påloggingssiden. Ingen tilleggskonfigurasjon kreves.

Flere klasser eksterne enheter for salgssted legges til i Windows, for eksempel klasser for kassaskuffer og kvitteringsskrivere. Vi venter på støtte for disse nye enhetsklassene i Modern POS.

> [!NOTE] 
> Enkelte USB-enheter kan kanskje ikke reagere eller bli upålitelige når de administreres av en strømstyringsfunksjon i Windows 10 kalt for [Selektiv suspendering av USB](/windows-hardware/drivers/usbcon/usb-selective-suspend). Hvis en ekstern USB-enhet ikke svarer, kan det være nødvendig å deaktivere den selektive suspenderingsfunksjonen for enheten. Hvis du vil ha mer informasjon, kan du se [Aktivere selektiv suspendering](/windows-hardware/drivers/usbcon/usb-selective-suspend#enabling-selective-suspend). 

### <a name="keyboard-wedge"></a>Tastaturkortleser

Tastaturkortleserenheter sender data til datamaskinen som om dataene ble skrevet på et tastatur. Feltet som er aktivt på salgsstedet vil derfor motta dataene som skannes eller leses. I enkelte tilfeller kan denne virkemåten føre til at feil type data skannes inn i feil felt. En strekkode kan for eksempel skannes inn i et felt som er ment for registrering av kredittkortdata. I mange tilfeller er det logisk at det er salgsstedet som bestemmer om dataene som skannes eller leses, er en strekkode eller kortlesing. Derfor behandles dataene på riktig måte. Når enheter konfigureres som OPOS-enheter i stedet for tastaturkortleserenheter, er det imidlertid mer kontroll over hvordan dataene fra disse enhetene kan brukes, fordi mer er "kjent" om enheten som dataene kommer fra. Data fra en strekkodeskanner gjenkjennes for eksempel automatisk som en strekkode, og den tilknyttede posten i databasen finnes enklere og raskere enn hvis et søk etter en generell streng blir brukt, noe som er tilfelle for tastaturkortleserenheter.

> [!NOTE]
> Når tastaturkortleserskannere brukes på salgsstedet, må de programmeres for å kunne sende en vognretur, eller en **Enter**-hendelse, etter det sist skannede tegnet. Hvis denne konfigurasjonen ikke utføres, vil ikke tastaturkortleserskannere fungere riktig. Se i dokumentasjonen som leveres av enhetsprodusenten, for informasjon om hvordan du legger til vognreturhendelsen.  

### <a name="device-printers"></a>Enhetsskrivere

Skrivere av "Enhet"-typen kan konfigureres til å be brukeren om å velge en skriver som er konfigurert for datamaskinen. Når en skriver av "Enhet"-typen er konfigurert og Modern POS oppdager en utskriftskommando, blir brukeren bedt om å velge en skriver i en liste. Denne virkemåten er forskjellig fra virkemåten for Windows-drivere, fordi "Windows"-skrivertypen i maskinvareprofilen ikke viser en liste over skrivere til brukeren. I stedet kreves det at en navngitt skriver angis i **Enhetsnavn**-feltet.

### <a name="network"></a>Nettverk

Nettverksadresserbare kassaskuffer, kvitteringsskrivere og betalingsterminaler kan brukes via et nettverk, direkte via IPC-maskinvarestasjonen som er bygget inn i Modern POS for Windows-programmet eller IIS-maskinvarestasjonen for andre Modern POS-klienter.

## <a name="hardware-station-deployment-options"></a>Distribusjonsalternativer for maskinvarestasjon

### <a name="dedicated"></a>Dedikert

Modern POS-klienter for Windows og Android inkluderer **dedikerte** eller innebygde maskinvarestasjoner. Disse klientene kan kommunisere direkte med eksterne enheter ved hjelp av forretningslogikk som er innebygd i applikasjonene. Android-programmet støtter bare nettverksenheter. Hvis du vil ha mer informasjon om støtte for eksterne enheter for Android, kan du se artikkelen [Definere POS Hybrid-app på Android og iOS](./dev-itpro/hybridapp.md).

Følg fremgangsmåten nedenfor for å bruke den dedikerte maskinvarestasjonen.

1. Tilordne en maskinvareprofil til en kasse som skal bruke Modern POS for Windows- eller Android-appen.
1. Opprett en maskinvarestasjon av "Dedikert"-typen for butikken der kassen skal brukes. 
1. Åpne Modern POS i ikke-skuffmodus, og bruk operasjonen **Administrer maskinvarestasjoner** for å aktivere funksjonene på maskinvarestasjonen. Den dedikerte maskinvarestasjonen vil være aktiv som standard. 
1. Logg av Modern POS. Logg deretter på igjen, og åpne et skift. De eksterne enhetene som er konfigurert i maskinvareprofilen, kan nå brukes. 

### <a name="shared"></a>Delt

Noen ganger kalles også "IIS" for "IIS"-maskinvarestasjon, som antyder at POS-appen kobles til maskinvarestasjonen via Microsoft Internet Information Services. POS-programmet kobler til IIS-maskinvarestasjonen via webtjenester som kjører på en datamaskin der enheten er tilkoblet. Når den delte maskinvarestasjonen brukes, kan eksterne enheter, som er koblet til en maskinvarestasjon, brukes av alle kasser på salgsstedet som er på samme nettverk som IIS-maskinvarestasjonen. Siden bare Modern POS for Windows og Android inneholder innebygd støtte for eksterne enheter, må alle andre Modern POS-programmer bruke IIS-maskinvarestasjonen til å kommunisere med POS-enheter som er konfigurert i maskinvareprofilen. Derfor krever hver forekomst av IIS-maskinvarestasjonen en datamaskin som kjører webtjenesten, og programmet som kommuniserer med enhetene. 

Den delte maskinvarestasjonen kan brukes til å tillate at flere salgsstedsklienter deler eksterne enheter, eller den kan brukes til å administrere et igangsatt sett med eksterne enheter for et enkelt salgssted. 

Når en maskinvarestasjon brukes til å støtte deling av eksterne enheter mellom flere POS-klienter, bør bare kassaskuffer, kvitteringsskrivere og betalingsterminaler brukes. Du kan ikke koble til direkte frittstående strekkodeskannere, kortlesere, linjevisningsenheter, vekter eller andre enheter. Da vil det oppstå konflikter når flere POS-enheter prøver å gjøre krav på de eksterne enhetene samtidig. Slik håndteres konflikter for enheter som støttes:

-   **Kassaskuff** – Kassaskuffen åpnes via en hendelse som sendes til enheten. Det kan oppstå problemer hvis en kassaskuff kalles opp mens den allerede er åpen. En delt kassaskuff som brukes i en delt maskinvarestasjonskonfigurasjon skal settes til **Delt** i maskinvareprofilen. Denne innstillingen hindrer at salgsstedet kontrollerer om kassaskuffen allerede er åpen når det sendes åpne-kommandoer.
-   **Kvitteringsskriver** – Hvis to kommandoer for kvitteringsskriver sendes samtidig til maskinvarestasjonen, kan én av kommandoene gå tapt, avhengig av enheten. Noen enheter har internt minnet eller gruppering som kan hindre dette problemet. Hvis en utskriftskommando ikke kan fullføres, mottar kassereren en feilmelding og kan prøve utskriftskommandoen på nytt ut fra salgsstedet.
-   **Betalingsterminal** – Hvis en kasserer forsøker å utføre en betalingstransaksjon på en betalingsterminal som allerede er i bruk, vises en melding som varsler om at terminalen er i bruk og spør kassereren om å prøve på nytt senere. Kasserere kan vanligvis se at en terminal er allerede i bruk, slik at de kan vente til den andre transaksjonen er fullført før de prøver å betale på nytt.

Validering er planlagt for en fremtidig versjon for å registrere om enheter som ikke støttes, er konfigurert for en maskinvareprofil som er tilordnet en delt maskinvarestasjon. Hvis det blir funnet enheter som ikke støttes, vil brukeren motta en melding om at enhetene ikke støttes for delte maskinvarestasjoner. For delte maskinvarestasjoner blir alternativet **Velg ved betaling** satt til **Ja** på kassanivå. Salgsstedsbrukeren blir deretter bedt om å velge en maskinvarestasjon når et betalingsmiddel er valgt for en transaksjon på salgsstedet. Når maskinvarestasjonen velges samtidig som betalingsmiddel, blir valget av maskinvarestasjonen lagt til direkte i salgsstedsarbeidsflyten for mobile scenarier. Som en ekstra fordel brukes ikke linjevisningsenheten på betalingsterminalen i delte scenarier. Hvis betalingensterminalen brukes som en linjevisningsenhet, kan andre brukere bli blokkert fra å bruke denne terminalen til transaksjonen er fullført. I mobile scenarier kan linjer legges til en transaksjon over en lengre periode. Derfor er alternativet **Velg ved betaling** nødvendig for å sikre optimal tilgjengelig for enheten.

### <a name="network-peripherals"></a>Nettverksenheter

Nettverksangivelsen for enheter i maskinvareprofilen lar kassaskuffer, kvitteringsskrivere og betalingsterminaler kobles til via en nettverkstilkobling.

#### <a name="modern-pos-for-windows"></a>Moderne salgssted for Windows

Du kan angi IP-adresser for nettverksenheter på to steder. Hvis Modern POS-Windows-klienten bruker ett enkelt sett med nettverksenheter, må du angi IP-adressene for disse enhetene ved hjelp av alternativet **IP-konfigurasjon** i handlingsruten for selve kassen. For nettverksenheter som skal deles mellom kasser på salgsstedet, kan en maskinvareprofil som er tilordnet nettverksenheter, tilordnes direkte til en delt maskinvarestasjon. Hvis du vil tildele IP-adresser, velger du denne maskinvarestasjonen på siden **Butikker**, og deretter bruker du alternativet **IP-konfigurasjon** i delen **Maskinvarestasjoner** for å angi nettverksenhetene som er tilordnet til denne maskinvarestasjonen. For maskinvarestasjoner som bare har nettverksenheter trenger du ikke å distribuere selve maskinvarestasjonen. I slike tilfeller kreves maskinvarestasjonen bare for å begrepsmessig gruppere nettverksadresserbare enheter i henhold til deres plassering i butikken.

#### <a name="cloud-pos-and-modern-pos-for-ios"></a>Cloud POS og Modern POS for iOS

Logikken som styrer fysisk tilkoblede og nettverksadresserbare enheter finnes i maskinvarestasjonen. For alle salgsstedsklienter bortsett fra Modern POS for Windows og Android må derfor en IIS-maskinvarestasjon distribueres og aktives for å aktivere kommunikasjon mellom salgsstedet og eksterne enheter, uavhengig av om de eksterne enhetene er fysisk koblet til en maskinvarestasjon eller adresseres over nettverket.

## <a name="setup-and-configuration"></a>Oppsett og konfigurasjon
### <a name="hardware-station-installation"></a>Installasjon av maskinvarestasjon

Hvis du vil ha veiledning for installasjon av en IIS-maskinvarestasjon, kan du se [Konfigurere og installere maskinvarestasjon](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Oppsett og konfigurasjon av Modern POS for Windows

Hvis du vil ha mer informasjon, kan du se [Konfigurere, installere og aktivere Modern POS (MPOS)](retail-modern-pos-device-activation.md).

### <a name="modern-pos-for-android-and-ios-setup-and-configuration"></a>Oppsett og konfigurasjon av Modern POS for Android og iOS

For informasjon, se [Definere POS Hybrid-app på Android og iOS](./dev-itpro/hybridapp.md).

### <a name="opos-device-setup-and-configuration"></a>Oppsett og konfigurasjon av OPOS-enhet

Hvis du vil ha mer informasjon om OPOS-komponenter, kan du se delen "Grensesnitt som støttes" i dette dokumentet. OPOS-drivere leveres vanligvis av produsenten av enheten. Når en OPOS-enhetsdriver er installert, legger den til en nøkkel i Windows-registret på én av følgende plasseringer:

-   **32-biters system:** HKEY\_LOCAL\_MACHINE\SOFTWARE\OLEforRetail\ServiceOPOS
-   **64-biters system:** HKEY\_LOCAL\_MACHINE\SOFTWARE\WOW6432Node\OLEforRetail\ServiceOPOS

I ServiceOPOS-registerplassering er konfigurerte enheter organisert i henhold til enhetsklassen OPOS. Flere enhetsdrivere lagres.

## <a name="supported-scenarios-by-hardware-station-type"></a>Scenarier som støttes etter maskinvarestasjonstype
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Klientstøtte – IPC-maskinvarestasjon kontra IIS maskinvarestasjon

Tabellen nedenfor viser topologier og distribusjonsscenarier som støttes.

| Kunde      | IPC-maskinvarestasjon | IIS-maskinvarestasjon |
|-------------|----------------------|----------------------|
| Windows-app | Ja                  | Ja                  |
| Skybasert salgssted   | Nei                   | Ja                  |
| Android     | Ja                  | Ja                  |
| iOS         | Nei                   | Ja                  |

### <a name="network-peripherals"></a>Nettverksenheter

Nettverksenheter kan støttes direkte gjennom maskinvarestasjonen som er bygd inn i Modern POS for Windows- og Android-apper. For alle andre klienter må du distribuere en IIS-maskinvarestasjon.

| Kunde      | IPC-maskinvarestasjon | IIS-maskinvarestasjon |
|-------------|----------------------|----------------------|
| Windows-app | Ja                  | Ja                  |
| Skybasert salgssted   | Nei                   | Ja                  |
| Android     | Ja                  | Ja                  |
| iOS         | Nei                   | Ja                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Enhetstyper som støttes av maskinvarestasjonstype
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Moderne POS for Windows med en IPC-maskinvarestasjon (innebygd)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Enhetsklasse som støttes</th>
<th>Grensesnitt som støttes</th>
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
<li>UWP (krever ikke oppsett)</li>
<li>Tastaturkortleser (krever ikke oppsett)</li>
</ul></td>
</tr>
<tr class="even">
<td>Trassent</td>
<td><ul>
<li>OPOS</li>
<li>Nettverk </br><strong>Merk:</strong> Bare én skuff kan defineres hvis <strong>Bruk delte skift</strong> er konfigurert på skuffen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skuff 2</td>
<td><ul>
<li>OPOS</li>
<li>Nettverk </br><strong>Merk:</strong> Bare én skuff kan defineres hvis <strong>Bruk delte skift</strong> er konfigurert på skuffen.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skanner</td>
<td><ul>
<li>OPOS</li>
<li>UWP (krever ikke oppsett)</li>
<li>Tastaturkortleser (krever ikke oppsett)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skanner 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (krever ikke oppsett)</li>
<li>Tastaturkortleser (krever ikke oppsett)</li>
</ul></td>
</tr>
<tr class="even">
<td>Skaler</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>PIN-kodetastatur</td>
<td>OPOS (det gis støtte gjennom tilpasning av betalingskoblingen)</td>
</tr>
<tr class="even">
<td>Signaturregistrering</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Betalingsterminal </td>
<td><ul>
<li>Støtte for egendefinerte enheter</li>
<li>Nettverk (Hvis du vil ha mer informasjon om sporing, kan du se koblingsdokumentasjonen.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Alle Modern POS-klienter som har en forpliktet "delt" IIS-maskinvarestasjon

> [!NOTE]
> Når IIS-maskinvarestasjonen er "forpliktet", er det en 1-1-relasjon mellom salgsstedsklienten og maskinvarestasjonen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Enhetsklasse som støttes</th>
<th>Grensesnitt som støttes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Skriver</td>
<td><ul>
<li>OPOS</li>
<li>Nettverk</li>
</ul></td>
</tr>
<tr class="even">
<td>Skriver 2</td>
<td><ul>
<li>OPOS</li>
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
<li>Nettverk </br><strong>Merk:</strong> Bare én skuff per maskinvareprofil kan defineres hvis <strong>Bruk delte skift</strong> er konfigurert på skuffen.</li>
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
<td>OPOS (det gis støtte gjennom tilpasning av betalingskoblingen)</td>
</tr>
<tr class="odd">
<td>Sig. registrering</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Betalingsterminal </td>
<td><ul>
<li>Støtte for egendefinerte enheter</li>
<li>Nettverk (Hvis du vil ha mer informasjon om sporing, kan du se koblingsdokumentasjonen.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-share-an-iis-hardware-station"></a>Alle Modern POS-klienter som deler en IIS-maskinvarestasjon

> [!NOTE]
> Når IIS-maskinvarestasjonen er "delt", kan flere enheter bruke maskinvarestasjonen samtidig. I slike scenarier bør du bruke bare enhetene som vises i tabellen nedenfor. Hvis du prøver å dele enheter som ikke vises her, for eksempel strekkodeskannere og kortlesere, vil det oppstå feil når flere enheter forsøker å kreve den samme eksterne enheten. I fremtiden vil en slik konfigurasjon bli eksplisitt forhindret.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Enhetsklasse som støttes</th>
<th>Grensesnitt som støttes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Skriver</td>
<td><ul>
<li>OPOS</li>
<li>Nettverk</li>
</ul></td>
</tr>
<tr class="even">
<td>Skriver 2</td>
<td><ul>
<li>OPOS</li>
<li>Nettverk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Trassent</td>
<td><ul>
<li>OPOS</li>
<li>Nettverk </br><strong>Merk:</strong> Bare én skuff per maskinvareprofil kan defineres hvis <strong>Bruk delte skift</strong> er konfigurert på skuffen.</li>
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
<li>Nettverk (Hvis du vil ha mer informasjon om sporing, kan du se koblingsdokumentasjonen.)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Konfigurasjon for scenarier som støttes
Hvis du vil ha mer informasjon om hvordan du oppretter maskinvareprofiler, se [Koble eksterne enheter til salgsstedet](define-maintain-channel-clients-registers-hw-stations.md). 

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Moderne POS for Windows med en IPC-maskinvarestasjon (innebygd)

Denne konfigurasjonen er mest vanlig konfigurasjonen for tradisjonelle, fast kasser på salgssted. I slike scenarier tilordnes profilinformasjonen for maskinvare direkte til selve kassen. EFT-terminalnummeret bør også angis for selve kassen. Følg fremgangsmåten nedenfor for å definere denne konfigurasjonen.

1.  Opprett en maskinvareprofil der alle nødvendige enheter er konfigurert.
2.  Tilordne maskinvareprofilen til kassen på salgsstedet.
3.  Opprett en maskinvarestasjon av **Dedikert**-typen for butikken der POS-kassen skal brukes. Beskrivelse er valgfritt. 

    > [!NOTE]
    > Du behøver ikke å angi eventuelle andre egenskaper for maskinvarestasjonen. All annen nødvendig informasjonen, for eksempel maskinvareprofilen, kommer fra selve kassen.

4.  Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.
5.  Velg distribusjonsplanen **1090** for å synkronisere den nye maskinvareprofilen til butikken. Velg **Kjør nå** for å synkronisere endringer til salgsstedet.
6.  Velg distribusjonsplanen **1040** for å synkronisere den nye maskinvarestasjonen til butikken. Velg **Kjør nå** for å synkronisere endringer til salgsstedet.
7.  Installer og aktiver Modern POS for Windows.
8.  Start Modern POS for Windows, og begynn å bruke de tilkoblede eksterne enhetene.

### <a name="modern-pos-for-android-with-an-ipc-built-in-hardware-station"></a>Moderne POS for Android med en IPC-maskinvarestasjon (innebygd)

**Nytt for 10.0.8** – Epson-nettverksskrivere og kassaskuffer som er koblet til disse skriverne via DK-porten, støttes nå for Modern POS for Android-appen. Hvis du vil ha mer informasjon, kan du se artikkelen [Definere POS Hybrid-app på Android og iOS](./dev-itpro/hybridapp.md).

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Alle Modern POS-klienter som har en forpliktet delt IIS-maskinvarestasjon

Denne konfigurasjonen kan brukes for alle Modern POS-klienter som har en maskinvarestasjon som brukes av bare én kasse på salgsstedet. Følg fremgangsmåten nedenfor for å definere denne konfigurasjonen.

1.  Opprett en maskinvareprofil der alle nødvendige enheter er konfigurert.
2.  Opprett en maskinvarestasjon av **Dedikert**-typen for butikken der POS-kassen skal brukes.
3.  Angi følgende egenskaper for den dedikerte maskinvarestasjonen:
    -   **Vertsnavn** – Navnet på vertsdatamaskinen der maskinvarestasjonen skal kjøres. 
    
        > [!NOTE]
        > Cloud POS kan løse **localhost** for å finne den lokale datamaskinen der Cloud POS kjøres. Sertifikatet som kreves for å koble Cloud POS sammen med maskinvarestasjonen, må imidlertid også ha "Localhost" som navnet på datamaskinen. For å unngå problemer anbefaler vi at du angir en forekomst av hver dedikerte maskinvarestasjon for butikken etter behov. For hver enkelt maskinvarestasjon må vertsnavnet være navnet på den spesifikke datamaskinen der maskinvarestasjonen skal distribueres.
    
    -   **Port** – Porten som skal brukes for kommunikasjon mellom maskinvarestasjonen og Modern POS-klienten.
    -   **Maskinvareprofil** – Hvis maskinvareprofilen ikke er angitt på selve maskinvarestasjonen, brukes maskinvareprofilen som er tilordnet kassen.
    -   **EFT-salgsstedsnummer** – EFT-terminal-ID-en skal brukes ved sending av EFT-autoriseringer. Denne ID-en leveres av kredittkortbehandleren.
    -   **Pakkenavn** – Maskinvarestasjonspakken som skal brukes når maskinvarestasjonen distribueres.

4.  Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.
5.  Velg distribusjonsplanen **1090** for å synkronisere den nye maskinvareprofilen til butikken. Velg **Kjør nå** for å synkronisere endringer til salgsstedet.
6.  Velg distribusjonsplanen **1040** for å synkronisere den nye maskinvarestasjonen til butikken. Velg **Kjør nå** for å synkronisere endringer til salgsstedet.
7.  Installer maskinvarestasjonen. Hvis du vil ha mer informasjon om hvordan du installerer maskinvarestasjonen, kan du se [Konfigurere og installere Retail Hardware Station](retail-hardware-station-configuration-installation.md).
8.  Installer og aktiver Modern POS. Hvis du vil ha mer informasjon om hvordan du installerer Modern POS, kan du se [Konfigurere, installere og aktivere Modern POS (MPOS)](retail-modern-pos-device-activation.md).
9.  Logg på Modern POS, og velg **Utfør en ikke-skuff-operasjon**.
10. Start operasjonen **Administrer maskinvarestasjoner**.
11. Velg **Behandle**.
12. På siden for administrasjon av maskinvarestasjonen angir du alternativet for å aktivere maskinvarestasjonen.
13. Velg maskinvarestasjonen som skal brukes, og velg deretter **Par**.
14. Når maskinvarestasjonen er sammenkoblet, velger du **Lukk**.
15. På siden for valg av maskinvarestasjonen velger du den sist valgte maskinvarestasjonen for å aktivere den.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Alle Modern POS-klienter som har en delt IIS-maskinvarestasjon

Denne konfigurasjonen kan brukes for alle Modern POS-klienter som deler maskinvarestasjoner med andre enheter. Følg fremgangsmåten nedenfor for å definere denne konfigurasjonen.

1.  Opprett en maskinvareprofil der nødvendige enheter er konfigurert.
2.  Opprett en maskinvarestasjon av **Delt**-typen for butikken der POS-kassen skal brukes.
3.  Angi følgende egenskaper for den delte maskinvarestasjonen:
    -   **Vertsnavn** – Navnet på vertsdatamaskinen der maskinvarestasjonen skal kjøres.
    -   **Beskrivelse** – Tekst som bidrar til å identifisere maskinvarestasjonen, for eksempel **Returer** eller **Butikkfront**.
    -   **Port** – Porten som skal brukes for kommunikasjon mellom maskinvarestasjonen og Modern POS-klienten.
    -   **Maskinvareprofil** – Hver enkelt delte maskinvarestasjon bør ha en maskinvareprofil. Maskinvareprofiler kan deles mellom maskinvarestasjoner, men de må være tilordnet hver maskinvarestasjon. I tillegg anbefaler vi at du bruker delte skift når flere enheter bruker den samme delte maskinvarestasjonen. Hvis du vil konfigurere et delt skift, går du til **Detaljhandel og handel \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Maskinvareprofiler**. Velg kassaskuffen for hver av de delte maskinvareprofilene, og sett alternativet **Skuff for delt skift** til **Ja**.
    -   **EFT-salgsstedsnummer** – EFT-terminal-ID-en skal brukes ved sending av EFT-autoriseringer. Denne ID-en leveres av kredittkortbehandleren.
    -   **Pakkenavn** – Maskinvarestasjonspakken som skal brukes når maskinvarestasjonen distribueres.

4.  Gjenta trinn 2 og 3 for hver ekstra maskinvarestasjon som kreves i butikken.
5.  Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.
6.  Velg distribusjonsplanen **1090** for å synkronisere den nye maskinvareprofilen til butikken. Velg **Kjør nå** for å synkronisere endringer til salgsstedet.
7.  Velg distribusjonsplanen **1040** for å synkronisere den nye maskinvarestasjonen til butikken. Velg **Kjør nå** for å synkronisere endringer til salgsstedet.
8.  Installer maskinvarestasjonen på hver vertsdatamaskin som du opprettet i trinn 2 og 3. Hvis du vil ha mer informasjon om hvordan du installerer maskinvarestasjonen, kan du se [Konfigurere og installere Retail Hardware Station](retail-hardware-station-configuration-installation.md).
9.  Installer og aktiver Modern POS. Hvis du vil ha mer informasjon om hvordan du installerer Modern POS, kan du se [Konfigurere, installere og aktivere Modern POS (MPOS)](retail-modern-pos-device-activation.md).
10. Logg på Modern POS, og velg **Utfør en ikke-skuff-operasjon**.
11. Start operasjonen **Administrer maskinvarestasjoner**.

12. Velg **Behandle**.
13. På siden for administrasjon av maskinvarestasjonen angir du alternativet for å aktivere maskinvarestasjonen.
14. Velg maskinvarestasjonen som skal brukes, og velg deretter **Par**.
15. Gjenta trinn 14 for hver maskinvarestasjon som Modern POS bruker.
16. Når all nødvendig maskinvarestasjoner er sammenkoblet, velger du **Lukk**.
17. På siden for valg av maskinvarestasjonen velger du den sist valgte maskinvarestasjonen for å aktivere den. 

> [!NOTE]
> Hvis enheter ofte bruker forskjellig maskinvarestasjoner, anbefaler vi at du konfigurerer Modern POS til å spørre kasserere å velge en maskinvarestasjon når de begynner betalingsprosessen. Gå til **Detaljhandel og handel \> Kanaloppsett \> Salgsstedsoppsett \> Kasser**. Velg kassen, og sett deretter alternativet **Velg ved betalingen** til **Ja**. Bruk distribusjonsplanen **1090** for å synkronisere endringer i kanaldatabasen.

## <a name="extensibility"></a>Utvidelsesmuligheter
Hvis du vil ha informasjon om utvidbarhetsscenarier for maskinvarehendelsen, kan du se [Integrere salgssted med en ny maskinvareenhet og generere installering av utvidelsen](dev-itpro/hardware-device-extension.md).

## <a name="security"></a>Sikkerhet
Følgende innstillinger skal brukes i et produksjonsmiljø i henhold til gjeldende sikkerhetsstandarder: 

### <a name="hardware-station-installer"></a>Installasjonsprogram for maskinvarestasjon
Installasjonsprogrammet for maskinvarestasjonen vil automatisk gjøre disse registerendringene som en del av installasjonen gjennom selvbetjening.

-   SSL (Secure Sockets Layer) må deaktiveres.
-   Bare TLS (Transport Layer Security) versjon 1.2 (eller gjeldende nyeste versjon) skal være aktivert og brukes. 

### <a name="ssl-and-tls"></a>SSL og TLS
SSL og alle versjoner av TLS, unntatt TLS 1.2, er deaktivert som standard. Følg denne fremgangsmåten for å redigere eller aktivere disse verdiene:
    1.  Trykke på Windows-logotasten+R for å åpne et **Kjør**-vindu.
    2.  I **Åpne**-feltet skriver du inn **Regedit**, og deretter velger du **OK**.
    3.  Hvis det vises en **Brukerkontokontroll**-melding, velger du **Ja**.
    4.  I vinduet **Registerredigering** går du til **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Følgende nøkler er angitt automatisk for å bare tillate TLS 1.2:
        -   TLS 1.2Server:Enabled=1
        -   TLS 1.2Server:DisabledByDefault=0
        -   TLS 1.2Client:Enabled=1
        -   TLS 1.2Client:DisabledByDefault=0
        -   TLS 1.1Server:Enabled=0
        -   TLS 1.1Client:Enabled=0
        -   TLS 1.0Server:Enabled=0
        -   TLS 1.0Client:Enabled=0
        -   SSL 3.0Server:Enabled=0
        -   SSL 3.0Client:Enabled=0
        -   SSL 2.0Server:Enabled=0
        -   SSL 2.0Client:Enabled=0
-   Ingen flere nettverksporter skal være åpne, med mindre de er nødvendige av kjente, angitte årsaker.
-   Cross-origin-ressursdeling må være deaktivert og må angi de tillatte opprinnelsene som godtas.
-   Bare klarerte sertifiseringsinstanser skal brukes til å skaffe sertifikater som skal brukes på datamaskiner som kjører maskinvarestasjonen.

> [!NOTE]
> Det er svært viktig at du ser gjennom retningslinjene for sikkerhet for IIS og kravene til betalingskortbransjen (PCI).

## <a name="peripheral-simulator"></a>Ekstern simulator
Hvis du vil ha mer informasjon, kan du se [Ekstern simulator for Commerce](dev-itpro/retail-peripheral-simulator.md).

## <a name="microsoft-tested-peripheral-devices"></a>Microsoft-testede eksterne enheter
### <a name="ipc-built-in-hardware-station"></a>IPC-maskinvarestasjon (innebygd)

De eksterne enhetene nedenfor ble testet ved hjelp av IPC-maskinvarestasjonen som er bygget inn i Modern POS for Windows.

#### <a name="printer"></a>Skriver

| Produsent | Modell    | Grensesnitt | Kommentarer                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | USB-drevet             |
| Star         | TSP650II | Egendefinert    | Tilkoblet via nettverket   |
| Star         | mPOP     | OPOS      | Tilkoblet via Bluetooth |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

> [!NOTE]
> Skriveren Star TSP 100 støttes ikke av den innebygde maskinvarestasjonen. Den innebygde maskinvarestasjonen bruker en 64-biters prosess, som ikke er kompatibel med eksisterende TP 100-drivere. 

#### <a name="bar-code-scanner"></a>Strekkodeleser

| Produsent  | Modell         | Grensesnitt | Kommentarer |
| ------------- | ------------- | --------- | -------- |
| Datalogic     | Magellan 8400 | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| HP-integrert | E1L07AA       | OPOS      |          |
| Symbol        | LS2208        | OPOS      |          |

#### <a name="payment-terminals-and-pin-pads"></a>Betalingsterminaler og PIN-kodetastatur

Dynamics 365 Commerce har en bruksklar løsning for integrering med Adyen for betalingstjenester. [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md) bruker den enhetsagnostiske [API-en (Application Programming Interface) for Adyen Payment Terminal](https://www.adyen.com/blog/introducing-the-terminal-api) og kan samhandle med alle betalingsterminaler som denne API-en støtter. Hvis du vil ha en fullstendig liste over betalingsterminaler som støttes, kan du se [Adyen POS-terminaler](https://www.adyen.com/pos-payments/terminals).

Du kan også bruke andre betalingsleverandører med Dynamics 365 Commerce ved å opprette en egendefinert kobling. Enhver betalingsterminal som støttes av betalingsleverandøren, kan brukes med Dynamics 365 Commerce. Med Dynamics 365 Commerce kan du likeledes bruke enhver integreringsmodell for betalingsenhet som støttes av betalingsleverandøren, for eksempel lokal IP, sky-API eller direkte tilkobling (for eksempel via USB) til salgsstedet. Hvis du vil ha mer informasjon, kan du se [Opprett en komplett betalingsintegrering for en betalingsterminal](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Kassaskuff

| Produsent | Modell     | Grensesnitt | Kommentarer                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Tilkoblet via Bluetooth |
| APG          | Atwood    | Egendefinert    | Tilkoblet via nettverket   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |
| Epson        |           | Egendefinert    | Koblet til Epson-nettverksskriver via DK-porten |

#### <a name="line-display"></a>Linjevisning

| Produsent | Modell    | Grensesnitt | Kommentarer |
| ------------ | -------- | --------- | -------- |
| Epson        | DM-D110  | OPOS      |          |
| HP           | T-serien | OPOS      |          |

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

| Produsent | Modell    | Grensesnitt | Kommentarer                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | USB-drevet             |
| Star         | TSP650II | Egendefinert    | Tilkoblet via nettverket   |
| Star         | mPOP     | OPOS      | Tilkoblet via Bluetooth |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

#### <a name="bar-code-scanner"></a>Strekkodeleser

| Produsent  | Modell         | Grensesnitt | Kommentarer |
| ------------- | ------------- | --------- | -------- |
| Datalogic     | Magellan 8400 | OPOS      |          |
| HP-integrert | E1L07AA       | OPOS      |          |
| Symbol        | LS2208        | OPOS      |          |

#### <a name="payment-terminals-and-pin-pads"></a>Betalingsterminaler og PIN-kodetastatur

Dynamics 365 Commerce har en bruksklar løsning for integrering med Adyen for betalingstjenester. [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md) bruker den enhetsagnostiske [API-en for Adyen Payment Terminal](https://www.adyen.com/blog/introducing-the-terminal-api) og kan samhandle med alle betalingsterminaler som denne API-en støtter. Hvis du vil ha en fullstendig liste over betalingsterminaler som støttes, kan du se [Adyen POS-terminaler](https://www.adyen.com/pos-payments/terminals).

Du kan også bruke andre betalingsleverandører med Dynamics 365 Commerce ved å opprette en egendefinert kobling. Enhver betalingsterminal som støttes av betalingsleverandøren, kan brukes med Dynamics 365 Commerce. Med Dynamics 365 Commerce kan du likeledes bruke enhver integreringsmodell for betalingsenhet som støttes av betalingsleverandøren, for eksempel lokal IP, sky-API eller direkte tilkobling (for eksempel via USB) til salgsstedet. Hvis du vil ha mer informasjon, kan du se [Opprett en komplett betalingsintegrering for en betalingsterminal](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Kassaskuff

| Produsent | Modell     | Grensesnitt | Kommentarer              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Egendefinert    | Tilkoblet via nettverket |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Egendefinert    | Koblet til Epson-nettverksskriver via DK-porten |

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

| Produsent | Modell    | Grensesnitt | Kommentarer                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | USB-drevet             |
| Star         | mPOP     | OPOS      | Tilkoblet via Bluetooth |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

#### <a name="payment-terminal"></a>Betalingsterminal

Dynamics 365 Commerce har en bruksklar løsning for integrering med Adyen for betalingstjenester. [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md) bruker den enhetsagnostiske [API-en for Adyen Payment Terminal](https://www.adyen.com/blog/introducing-the-terminal-api) og kan samhandle med alle betalingsterminaler som denne API-en støtter. Hvis du vil ha en fullstendig liste over betalingsterminaler som støttes, kan du se [Adyen POS-terminaler](https://www.adyen.com/pos-payments/terminals).

Du kan også bruke andre betalingsleverandører med Dynamics 365 Commerce ved å opprette en egendefinert kobling. Enhver betalingsterminal som støttes av betalingsleverandøren, kan brukes med Dynamics 365 Commerce. Med Dynamics 365 Commerce kan du likeledes bruke enhver integreringsmodell for betalingsenhet som støttes av betalingsleverandøren, for eksempel lokal IP, sky-API eller direkte tilkobling (for eksempel via USB) til salgsstedet. Hvis du vil ha mer informasjon, kan du se [Opprett en komplett betalingsintegrering for en betalingsterminal](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Kassaskuff

| Produsent | Modell     | Grensesnitt | Kommentarer              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Egendefinert    | Tilkoblet via nettverket |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Egendefinert    | Koblet til Epson-nettverksskriver via DK-porten |


## <a name="troubleshooting"></a>Feilsøking
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Modern POS kan gjenkjenne maskinvarestasjonen i listen for valg, men kan ikke fullføre sammenkoblingen

**Løsning**: Kontroller følgende liste over potensielle feil:

-   Datamaskinen som kjører Modern POS klarerer sertifikatet som brukes på datamaskinen som kjører maskinvarestasjonen.
    -   Hvis du vil kontrollere dette oppsettet, åpner du en nettleser og går til følgende nettadresse: https://&lt;datamaskinnavn&gt;:&lt;portnummer&gt;/HardwareStation/ping.
    -   Denne nettadressen bruker en ping-kommando til å kontrollere at det er tilgang til datamaskinen, og nettleseren angir om sertifikatet er klarert. (Eksempel: I Internet Explorer vises et låsesymbol på adresselinjen. Når du velger dette symbolet, kontrollerer Internet Explorer om sertifikatet er klarert. Du kan installere sertifikatet på den lokale datamaskinen ved å vise detaljene for sertifikatet som vises.)
-   På datamaskinen som kjører maskinvarestasjonen blir porten som skal brukes av maskinvarestasjonen, åpnet i brannmuren.
-   Maskinvarestasjonen har riktig installert forhandlerkontoinformasjon gjennom Installer forhandlerinformasjon-verktøyet som kjører på slutten av installasjonsprogrammet for maskinvarestasjonen.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Modern POS gjenkjenner ikke maskinvarstasjonen i listen over valg

**Løsning**: Én av følgende faktorer kan forårsake dette problemet:

-   Maskinvarestasjonen ikke er riktig konfigurert i Headquarters. Hvis du vil ha mer informasjon, kan du se [Konfigurere og installere Retail Hardware Station](retail-hardware-station-configuration-installation.md#troubleshooting). 
-   Jobbene er ikke kjørt for å oppdatere kanalkonfigurasjonen. I slike tilfeller kjører du 1070-jobben for kanalkonfigurasjon.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Modern POS gjenspeiler ikke nye innstillinger for kassaskuff

**Løsning**: Lukk gjeldende bunke. Endringer i kassaskuffen oppdateres ikke til Modern POS før gjeldende bunke er lukket.

### <a name="modern-pos-is-reporting-an-issue-with-a-peripheral"></a>Modern POS rapporterer et problem med en ekstern enhet

**Løsning**: Her er noen vanlige årsaker til dette problemet:

-   Kontroller at andre konfigurasjonsverktøy for enhetsdriver er lukket. Hvis disse verktøyene er åpne, kan de hindre at Modern POS eller maskinvarestasjonen krever enheten.
-   Hvis den eksterne enheten deles av flere POS-enheter, må du kontrollere at den tilhører én av følgende kategorier:
    -   Kassaskuff
    -   Kvitteringsskriver
    -   Betalingsterminal 

    Hvis den eksterne enheten ikke tilhører én av disse kategoriene, er ikke maskinvarestasjonen utformet for å aktivere deling av den eksterne enheten mellom flere POS-enheter.
-   Enhetsdrivere kan noen ganger føre til at Common Control Objects (CCO-er) slutter å fungere slik de skal. Hvis en enhet nylig er installert, men den ikke fungerer slik den skal eller du legger merke til andre problemer, kan du ofte løse problemet ved å installere CCO-er. Du kan laste ned CCO-er ved å gå til <http://monroecs.com/oposccos_current.htm>.
-   Hvis du ofte endrer eksterne enheter under testing eller feilsøking, må du kanskje tilbakestille IIS i stedet for å vente på at hurtigbufferen skal oppdatere seg selv. Følg denne fremgangsmåten for å tilbakestille IIS:
    1.  Skriv inn **CMD** på **Start**-menyen.
    2.  Høyreklikk **Ledetekst** i søkeresultatet, og velg deretter **Kjør som administrator**.
    3.  I **Ledetekst**-vinduet skriver du inn **iisreset /Restart** og trykker deretter på Enter.
    4.  Når IIS er startet på nytt, starter du Modern POS på nytt.
-   Hvis du ofte endrer eksterne enheter og du også ofte starter og avslutter POS-klienten, kan dllhost-prosessen fra en tidligere POS-økt påvirke gjeldende økt. I slike tilfeller kan en enhet ikke brukes før du lukker DLL-verten som administrerer den forrige økten. Følg denne fremgangsmåten for å lukke DLL-verten:
    1.  Skriv inn **Oppgavebehandling** på **Start**-menyen.
    2.  Velg **Oppgavebehandling** i søkeresultatene.
    3.  I kategorien **Detaljer** i Oppgavebehandling, velger du kolonneoverskriften som er merket **Navn** for å sortere tabellen alfabetisk etter navn.
    4.  Rull nedover til du finner dllhost.exe.
    5.  Velg hver enkelt DLL-vert, og velg deretter **Avslutt oppgave**.
    6.  Når DLL-vertene er avsluttet, starter du Modern POS på nytt.


## <a name="additional-resources"></a>Tilleggsressurser

[Ekstern simulator for Commerce](dev-itpro/retail-peripheral-simulator.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]

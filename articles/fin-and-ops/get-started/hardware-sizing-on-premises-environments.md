---
title: "Krav til størrelsesangivelse for maskinvare for lokale miljøer"
description: "Dette emnet viser kravene til størrelsesangivelse for maskinvare for et lokalt miljø."
author: kfend
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fecffd83f32c8424e3ddcd77fb0651631f73c055
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="hardware-sizing-for-on-premises-environments"></a>Størrelsesangivelse for maskinvare for lokale miljøer

[!include[banner](../includes/banner.md)]

Før du begynner maskinvaren og infrastruktur endrer størrelsen på arbeid for et lokale miljø, gjøre deg kjent med den [systemkrav](system-requirements.md) og [instruksjoner for installasjon og distribusjon](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) for å få en grundig forståelse av den underliggende infrastrukturen. 

  **Obs!** Se nøye på anbefalte fremgangsmåter for systemoppsett for optimal ytelse. 

Når du har gått gjennom dokumentasjonen, kan du starte prosessen med å beregne transaksjonelle og samtidig bruker volumet og endre størrelse på miljøet basert på gjennomsnittlig kjerneinstallasjon produksjonen.

## <a name="factors-that-affect-sizing"></a>Faktorer som påvirker størrelse
Alle faktorene som vises i den følgende illustrasjonen, bidrar til størrelse. Jo mer detaljert informasjon som samles inn, jo mer nøyaktig kan du bestemme størrelse. Maskinvarestørrelse, uten støttedata, vil sannsynlig bli unøyaktig. Det absolutte minstekravet for nødvendige data er toppverdi for transaksjonslinjer per time. 

[![Størrelsesangivelse for maskinvare for lokale miljøer](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)

Sett fra venstre mot høyre, er den første og viktigste faktoren som kreves for å beregne nøyaktig størrelse, en transaksjonsprofil eller en transaksjonenkarakterisering. Det er viktig at du alltid finner toppverdien for transaksjonsvolum per time. Hvis det finnes flere perioder med stor belastning, må disse periodene defineres korrekt. 

Når du forstår belastningen som virker inn på infrastrukturen, må du også forstå mer detaljert informasjon om disse faktorene: 

- **Transaksjoner** - Vanligvis har transaksjoner bestemte topper gjennom hele dagen/uken. Dette avhenger hovedsakelig av transaksjonstypen. Tid- og utgiftspostene viser vanligvis topper én gang per uke, mens salgsordreoppføringer ofte kommer samtidig via integrasjon eller renner inn i løpet av dagen. 

- **Antall samtidige brukere** – Antallet samtidige brukere er den nest viktigste størrelsesfaktoren. Du får ikke pålitelige størrelsesestimater som er basert på antallet samtidige brukere, så hvis dette er de eneste dataene du har tilgjengelig, må du beregne et omtrentlig antall og deretter finne det igjen når du har flere data. En nøyaktig definisjon av samtidige brukere betyr følgende: 
  - Navngitte brukere er ikke samtidige brukere.
  - Samtidige brukere er alltid et delsett av navngitte brukere. 
  - Maksimal arbeidsmengde definerer den største samtidigheten for størrelser.
 
- Kriterier for samtidige brukere er at du oppfyller alle vilkårene nedenfor: 
  - Logget på. 
  - Aktive transaksjoner/forespørsler ved telling. 
  - Ikke en inaktiv økt. 
 
- **Datasammensetning** – Dette handler for det meste om hvordan systemet skal settes opp og konfigureres. For eksempel antallet juridiske enheter, hvor mange varer, hvor mange stykklistenivåer og hvor omfattende sikkerhetsoppsettet vil være. Hver av disse faktorene kan ha liten innvirkning på ytelsen, så disse faktorene kan forskyves ved hjelp av smarte valg når det gjelder infrastruktur. 

- **Tillegg** – Tilpasninger kan være enkle eller komplekse. Hvor mange tilpasninger og hvilken kompleksitet og bruk har en variert innvirkning på størrelsen på infrastruktur som er nødvendig. For omfattende tilpasninger er det anbefalt å utføre prestasjonsvurderinger for å sikre at de ikke er bare testet for effektivitet, men også bidra til å forstå infrastrukturbehov. Dette er enda mer kritisk når tilleggene ikke er kodet i henhold til anbefalte fremgangsmåter for ytelse og skalerbarhet. 

- **Rapportering og analyse** – Disse faktorene omfatter vanligvis kjøring av tunge spørringer mot de forskjellige databasene i databasesystemene i Finance and Operations. Forstå og redusere hyppigheten når kostbar rapporter kjøres, hjelper deg med å forstå virkningen av dem.. 

- **Tredjepartsløsninger** – Disse løsningene, som uavhengige programvareleverandører, har de samme konsekvensene og anbefalingene som tillegg. 

## <a name="sizing-your-finance-and-operations-environment"></a>Finne størrelsen på Finance and Operations-miljøet
For å forstå kravene til størrelse, må du vite høyeste antall transaksjoner som du skal behandle. De fleste ekstrasystemer, for eksempel Management Reporter eller SSRS, er mindre driftskritiske. Som et resultat fokuserer dette dokumentet mest på AOS og SQL Server. 

**Obs!** Generelt skaleres beregningslagene ut, og må defineres på en N+1-måte, noe som betyr at hvis du beregner tre AOS, må du legge til et fjerde AOS. Databaselaget må være definert i et alltid lett tilgjengelig oppsett. 


## <a name="sql-server-oltp"></a>SQL Server (OLTP)

### <a name="sizing"></a>Størrelse

- 3K til 15K transaksjonslinjer per time per kjerne på databaseserver.
- Vanlig AOS-til-SQL-kjerneforhold 3:1 for den primære SQL-serveren. Ekstra kjerner er nødvendig, basert på den valgte konfigurasjonen med høy tilgjengelighet. 
  - Ved behandling av databasetunge operasjoner kan dette skaleres ned til 2:1. 
- Følgende faktorer påvirker variasjoner: 
  - Parameterinnstillingene i bruk. 
  - Utvidelsesnivåer. 
  - Bruk av ekstra funksjonalitet, for eksempel databaseloggen og varsler. Ekstrem databaselogging reduserer ytelse per time per kjerne under 3K linjer. 
  - Kompleksiteten i sammensetningen av data – En enkel kontoplan og en detaljert spesifisert kontoplan har implikasjoner på gjennomstrømming (som et eksempel). 
  - Beskrivelse av transaksjonen.
  - 2 GB til 4 GB minne for hver kjerne. 
  - Ekstra databaser på databaseserver, som Management reporter og SSRS-databaser.
  - Temp DB = 15 % av DB-størrelse, med så mange filer som fysiske prosessorer. 
  - SAN-størrelsen og kapasiteten basert på totalt samtidig transaksjonsvolum/-bruk. 

### <a name="high-availability"></a>Høy tilgjengelighet 
Vi anbefaler alltid bruk av SQL Server enten i en klynge eller et speiloppsett. Den andre SQL-noden skal ha samme antall tilgjengelige kjerner som primærnoden. 

### <a name="active-directory-federation-services-ad-fs"></a>Active Directory Federation Services (AD FS)
For AD FS-størrelser kan du se [dokumentasjonen for AD FS-serverkapasitet](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).

Et [størrelsesregneark](http://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) er tilgjengelig for planlegging av antall forekomster i distribusjonen.

<a name="aos-online-and-batch"></a>AOS (online og satsvis)
----------------------

### <a name="sizing"></a>Størrelse

- Størrelse etter transaksjonsvolum/-bruk
  - 2K til 6K linjer per kjerne
  - 16 GB per forekomst
  - Standardboks – 4 til 24 kjerner
  - 10 til 15 virksomhetsbrukere per kjerne
  - 15 til 25 aktivitetsbrukere per kjerne
  - 25 til 50 teammedlemmer per kjerne
- Bunke
   - 1 til 4 bunketråder per kjerne
   - Størrelse basert på karakterisering av bunkevindu
- Legg merke til at AOS, Databehandling og Bunke på den samme rollen i Service Fabric. Du må angi størrelsen for disse tre arbeidsmengder kombinert, og ikke skille dem på samme måte som i Microsoft Dynamics AX 2012.
- De samme faktorene for variasjon for SQL Server gjelder her.

### <a name="high-availability"></a>Høy tilgjengelighet
- Sørg for at du har minst 1 til 2 flere AOS-er tilgjengelig enn det du beregner.
- Sørg for at du har minst 3 til 4 virtuelle verter tilgjengelig.

## <a name="management-reporter"></a>Administrasjonsreporter
I de fleste tilfeller, med mindre brukes ofte, skal anbefalte minimumskravene ved hjelp av to noder fungere bra. Bare i tilfeller der det er mye brukt du trenger mer enn to noder. Skaler etter behov.

## <a name="sql-server-reporting-services"></a>SQL Server Reporting Services
For utgivelsen med generell tilgjengelighet, kan bare én SSRS-node distribueres. Overvåk din SSRS-node under testing og øk antall tilgjengelige kjerner for SSRS etter behovet. Pass på at du har en forhåndskonfigurert sekundær node som er tilgjengelig på en virtuell vert som er forskjellig fra SSRS VM. Dette er viktig hvis det er et problem med den virtuelle maskinen som er vert for SSRS eller den virtuelle verten. Hvis dette er tilfellet, må de erstattes. 

## <a name="environment-orchestrator"></a>Environment Orchestrator
Tjenesten Orchestrator styrer distribusjonen og den tilknyttede kommunikasjonen med LCS. Denne tjenesten brukes som den primære Service Fabric-tjenesten og krever minst tre virtuelle maskiner. Denne tjenesten er plassert side om side med Service Fabric-orkestreringstjenester. Denne må også skaleres i henhold til toppbelastningen i klyngen. Hvis du vil ha mer informasjon, se [Betraktninger ved kapasitetsplanlegging for Service Fabric-klynger](/azure/service-fabric/service-fabric-cluster-capacity).  


## <a name="virtualization-and-oversubscription"></a>Virtualisering og overabonnering
Bedriftskritiske tjenester som AOS skal ligge på virtuelle verter som har dedikerte ressurser – kjerner, minne og diskplass.   



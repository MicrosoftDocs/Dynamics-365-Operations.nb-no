---
title: Etterfylling
description: Denne artikkelen beskriver etterfyllingsstrategier som er tilgjengelige for lagre som bruker funksjoner som er tilgjengelige i Lagerstyring.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSReplenishmentTemplates
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90043
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c808ec202bdb271f08a36a2b25ebed22a9477414
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="replenishment"></a>Etterfylling

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver etterfyllingsstrategier som er tilgjengelige for lagre som bruker funksjoner som er tilgjengelige i Lagerstyring.

Denne artikkelen beskriver etterfyllingsstrategier som er tilgjengelige for lagre som bruker funksjoner som er tilgjengelige i Lagerstyring. Informasjonen gjelder ikke for datalagerstyringsløsningen som er tilgjengelig i Lagerstyring. Det finnes tre etterfyllingsstrategier:

-   **Etterfylling basert på bølgebehov**– Denne strategien oppretter etterfyllingsarbeid for utgående ordrer eller laster, hvis beholdning ikke er tilgjengelig når bølgen oppretter arbeidet. Etterfyllingsarbeid kan for eksempel opprettes hvis antallet som kreves for en salgsordre ikke er tilgjengelig når en bølge behandles.
-   **Etterfylling basert på minimums- og maksimumsantall** – Denne strategien bruker minimums og maksimumsgrenser for lagring til å bestemme når lokasjoner skal etterfylles. Vare- og lokasjonskriteriene definere beholdningen som evalueres for etterfylling. Maler for etterfylling basert på minimums- og maksimumsantall er den primære mekanismen for å opprettholde optimal nivåer på plukklokasjoner. Du kan bruke behovsetterfylling for å garantere at nok pålydende plukking av lager er tilgjengelig for å dekke bølgeetterspørselen, som et supplement mellom sykluser for etterfylling basert på minimums- og maksimumsantall.
-   **Etterfylling basert på lastbehov** – Denne strategien summerer behovet for flere laster og oppretter etterfyllingsarbeidet som kreves for å fylle de relevante plukklokasjonene. Denne strategien bidrar til å garantere at lastene som opprettes, kan plukkes på lageret når de er frigitt.

Alle tre strategier opprette etterfyllingsarbeid basert på en etterfyllingsmal.

## <a name="wave-demand-replenishment"></a>Etterfylling basert på bølgebehov
Etterfylling basert på bølgebehov oppretter etterfyllingsarbeid basert på behov, hvis antallet som kreves for utgående ordrer eller laster ikke er tilgjengelig når en bølge oppretter arbeid. Etterfyllingsmalen inneholder informasjon om varekriteriene, måleenhet, behovsintervall og lokasjon. 

Lokasjonsdirektiver brukes til å fastsette hvilken lokasjon som skal etterfylles. Du koble disse lokasjonsdirektivene til etterfyllingsmalen ved hjelp av feltet **Direktivkode**. Hvis feltet **Direktivkode** er ikke satt, brukes spørringer til å bestemme hvilket lokasjonsdirektiv som skal brukes. Vær oppmerksom på at hvis en direktivkode ikke er angitt i etterfyllingsmalen, og lokasjonsdirektivet har en direktivkode, ignoreres direktivlokasjonen selv om spørringen i lokasjonsdirektivet er riktig. Lokasjonsdirektiver for plukking brukes til å avgjøre hvor beholdning hentes fra for etterfyllingen. 

I tillegg til å opprette en mal, må du angi noen innstillinger for etterfylling i bølgemalen. Bølgemalen må inneholde et bølgetrinn for etterfylling som bare kjøres hvis tildelingen av en vare ikke er vellykket. Dette bølgetrinnet for etterfylling bruker en bølgetrinnkode for å avgjøre hvilken etterfyllingsmal som skal brukes. I tillegg til å ha et bølgetrinn for etterfylling, må du kontrollere at **etterfylle** er valgt i **Metoder**-delen av bølgemalen. 

Siden **Etterfyllingsmal** inneholder alternativet **Tillat at bølgebehov kan bruke ureserverte antall**. Du må merke av for dette alternativet hvis du vil tillate at behovsetterfylling skal trekkes fra ikke-reservert antall fra arbeidet som er generert fra den valgte etterfyllingsmalen. Hvis du vil aktivere maler for behovsetterfylling til å bruke denne logikken, må du merke av for alternativet for alle eksisterende etterfyllingsmaler. Når etterfylling for behov utløses på lageret, vil dette trekke etterspørselen fra eksisterende etterfyllingsarbeid som har ikke-reservert antall, hvis jobben stammer fra etterfyllingsmaler der alternativet **La bølgebehov bruke ureserverte antall** er aktivert.

## <a name="minmax-replenishment"></a>Etterfylling basert på minimums- og maksimumsantall
I etterfylling basert på minimums- og maksimumsantall etterfylles lageret slik at det er mellom minimums- og maksimumsgrensene som er angitt. Denne prosessen oppstår vanligvis én gang hver dag for å garantere at alle plukklokasjoner er fylt til det maksimale nivået før plukkingen starter. 

Minimums- og maksimumsantallet angis i en etterfyllingsmal. Mange av de andre innstillingene i malen ligner på innstillinger i malene som brukes etterfylling basert på bølgebehov. Malen må inneholde én linje for hver vare og lokasjon. Når du kjører etterfylling ved hjelp av den satsvise jobben, evaluerer Microsoft Dynamics 365 for Operations om etterfylling kreves i rekkefølgen linjene er organisert i. 

Vær oppmerksom på at strategien for etterfylling basert på minimums- og maksimumsantall ikke kan etterfylle en tom lokasjon med mindre lokasjonen er definert som fast lokasjon for varen. Hvis lokasjonen som skal etterfylles ikke er en fast lokasjon, kan ikke Dynamics 365 for Operations fastslå hvilken vare som skal etterfylles. Derfor kreves det minst noe beholdning før etterfylling oppstår.

## <a name="load-demand-replenishment"></a>Etterfylling av lastbehov
Etterfylling basert på lastbehov summerer behovet for flere laster og oppretter etterfyllingsarbeidet som kreves for å fylle de relevante plukklokasjonene. Etterfylling basert på lastbehov ligner på mange måter på etterfylling basert på bølgebehov. Den største forskjellen er hvordan og når etterfylling basert på lastbehov og etterfylling basert på bølgebehov kjøres. Etterfylling basert på lastbehov kjøres ved hjelp av en satsvis jobb, på samme måte som etterfylling basert på minimums- og maksimumsantall. Hvis du vil definere den satsvise jobben, går du til siden **Etterfylling basert på lastbehov**, velger etterfyllingsmalen som skal brukes, og angir en filterspørring for å angi hvilke laster som skal brukes til å bestemme behovet. Lokasjonsspørringen definerer lokasjonene som tilgjengelige antall trekkes fra for å dekke det samlede behovet for lastene.

## <a name="replenishment-prerequisites"></a>Forhåndskrav for etterfylling
| Forutsetning            | Beskrivelse                                                                                                                                                                                                                                        |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Element                    | Varn må aktiveres for lagerstyringsprosesser.                                                                                                                                                                                       |
| Lager               | Lageret må aktiveres for lagerstyringsprosesser. Hvis du vil aktivere lageret for lagerstyringsprosesser, går du til siden **Lagre**, velger lageret og merker deretter av for **Bruk lagerstyringsprosesser**. |
| Etterfyllingsmaler | Minst én etterfyllingsmal må defineres for etterfylling basert på minimums- og maksimumsantall, etterfylling basert på bølgebehov eller etterfylling basert på lastbehov.                                                                                                             |
| Lokasjoner               | Lokasjoner må opprettes og kobles til en lokasjonsprofil.                                                                                                                                                                                     |
| Lokasjonsprofiler       | Lokasjonsprofiler er nødvendig for å opprette lokasjoner.                                                                                                                                                                                       |
| Lokasjonsdirektiver     | Lokasjonsdirektiver er nødvendig for å veilede arbeidet til lokasjoner der etterfylling er nødvendig, og til lokasjoner som beholdning hentes fra.                                                                                     |
| Arbeidsmaler          | Arbeidsmaler av typen **Etterfylling** er nødvendig for å opprette etterfyllingsarbeid, slik at beholdning kan flyttes til ønskede lokasjoner.                                                                                           |







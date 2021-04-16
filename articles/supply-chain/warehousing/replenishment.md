---
title: Oversikt over etterfylling
description: Dette emnet beskriver etterfyllingsstrategiene som er tilgjengelige for lagre som bruker funksjonaliteten som er tilgjengelig i Lagerstyring.
author: Mirzaab
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSReplenishmentTemplates, WHSInventFixedLocation, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 90043
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2b9ae560a991d50b9e63e6c3d73f01ce72394fb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814470"
---
# <a name="replenishment-overview"></a>Oversikt over etterfylling

[!include [banner](../includes/banner.md)]

Dette emnet beskriver etterfyllingsstrategiene som er tilgjengelige for lagre som bruker funksjonaliteten som er tilgjengelig i Lagerstyring. Informasjonen i dette emnet gjelder ikke for lagrerløsningen som er tilgjengelig i Lagerstyring.

Følgende etterfyllingsstrategier er tilgjengelige:

- **Etterfylling basert på bølgebehov**– Denne strategien oppretter etterfyllingsarbeid for utgående ordrer eller laster, hvis beholdning ikke er tilgjengelig når bølgen oppretter arbeidet. Etterfyllingsarbeid kan for eksempel opprettes hvis antallet som kreves for en salgsordre ikke er tilgjengelig når en bølge behandles.
- **Etterfylling basert på minimums- og maksimumsantall** – Denne strategien bruker minimums og maksimumsgrenser for lagring til å bestemme når lokasjoner skal etterfylles. Vare- og lokasjonskriteriene definere beholdningen som evalueres for etterfylling. Maler for etterfylling basert på minimums- og maksimumsantall er den primære mekanismen for å opprettholde optimal nivåer på plukklokasjoner. Du kan bruke behovsetterfylling for å garantere at nok pålydende plukking av lager er tilgjengelig for å dekke bølgeetterspørselen, som et supplement mellom sykluser for etterfylling basert på minimums- og maksimumsantall.
- **Etterfylling basert på lastbehov** – Denne strategien summerer behovet for flere laster og oppretter etterfyllingsarbeidet som kreves for å fylle de relevante plukklokasjonene. Denne strategien bidrar til å garantere at lastene som opprettes, kan plukkes på lageret når de er frigitt.
- **Umiddelbar etterfylling** – Denne strategien etterfyller beholdningen før en bølge kjøres hvis allokering mislykkes for en stedsdirektivlinje som har en etterfyllingsmal. 

Alle fire strategiene oppretter etterfyllingsarbeid, basert på en etterfyllingsmal.

## <a name="wave-demand-replenishment"></a>Etterfylling basert på bølgebehov
Etterfylling basert på bølgebehov oppretter etterfyllingsarbeid basert på behov, hvis mengden som kreves for produksjonsordrer, kanbans, utgående ordrer eller laster ikke er tilgjengelige når en bølge oppretter arbeid. Etterfyllingsmalen inneholder informasjon om varekriteriene, måleenhet, behovsintervall og lokasjon. 

Lokasjonsdirektiver brukes til å fastsette hvilken lokasjon som skal etterfylles. Du koble disse lokasjonsdirektivene til etterfyllingsmalen ved hjelp av feltet **Direktivkode**. Hvis feltet **Direktivkode** er ikke satt, brukes spørringer til å bestemme hvilket lokasjonsdirektiv som skal brukes. Vær oppmerksom på at hvis en direktivkode ikke er angitt i etterfyllingsmalen, og lokasjonsdirektivet har en direktivkode, ignoreres direktivlokasjonen selv om spørringen i lokasjonsdirektivet er riktig. Lokasjonsdirektiver for plukking brukes til å avgjøre hvor beholdning hentes fra for etterfyllingen. 

I tillegg til å opprette en mal, må du angi noen innstillinger for etterfylling i bølgemalen. Denne bølgemalen bør inneholde et bølgetrinn for etterfylling, som kjøres kun hvis et element ikke er vellykket allokert. Dette bølgetrinnet for etterfylling bruker en bølgetrinnkode for å avgjøre hvilken etterfyllingsmal som skal brukes. I tillegg til å ha bølgetrinn for etterfylling, må du forsikre deg om at **Etterfylling** er valgt i delen **Metoder** for bølgemalen. 

Siden **Etterfyllingsmal** inneholder alternativet **Tillat at bølgebehov kan bruke ureserverte antall**. Marker denne avkrysningsruten hvis behovsetterfylling skal kunne trekke ubehandlede mengder fra arbeid som genereres fra den valgte etterfyllingsmalen. Hvis du vil aktivere maler for behovsetterfylling til å bruke denne logikken, må du merke av for alternativet for alle eksisterende etterfyllingsmaler. Når etterfylling for behov utløses på lageret, vil dette trekke etterspørselen fra eksisterende etterfyllingsarbeid som har ikke-reservert antall, hvis jobben stammer fra etterfyllingsmaler der alternativet **La bølgebehov bruke ureserverte antall** er aktivert.

**Etterfyllingsenhet** er minimumsenheten som skal etterfylles. Dette må være et heltall som er et multiplum av enheten. Systemet runder opp til den høyeste enheten som er mulig når du oppretter arbeid.

Etterfylling av behov støttes for salgsordrer, overføringsordrer, produksjonsordrer og Kanbaner. 

## <a name="minmax-replenishment"></a>Etterfylling basert på minimums- og maksimumsantall
I etterfylling basert på minimums- og maksimumsantall etterfylles lageret slik at det er mellom minimums- og maksimumsgrensene som er angitt. Vanligvis skjer denne prosessen en gang hver dag for å sikre at alle plukklokasjoner fylles til maksimumsnivået før plukkingen starter. 

Minimums- og maksimumsantallet angis i en etterfyllingsmal. Mange av de andre innstillingene i malen ligner på innstillinger i malene som brukes etterfylling basert på bølgebehov. Malen må inneholde én linje for hver vare og lokasjon. Når du kjører etterfylling ved hjelp av den satsvise jobben, evaluerer systemet om etterfylling kreves, ved å bruke rekkefølgen linjene er organisert i. 

Vær oppmerksom på at strategien for etterfylling basert på minimums- og maksimumsantall ikke kan etterfylle en tom lokasjon med mindre lokasjonen er definert som fast lokasjon for varen. Hvis lokasjonen som skal etterfylles ikke er en fast lokasjon, kan ikke systemet fastsette hvilket element som skal etterfylles. Derfor kreves det minst noe beholdning før etterfylling oppstår.

## <a name="load-demand-replenishment"></a>Etterfylling av lastbehov
Etterfylling basert på lastbehov summerer behovet for flere laster og oppretter etterfyllingsarbeidet som kreves for å fylle de relevante plukklokasjonene. Etterfylling basert på lastbehov ligner på mange måter på etterfylling basert på bølgebehov. Den største forskjellen er hvordan og når etterfylling basert på lastbehov og etterfylling basert på bølgebehov kjøres. Etterfylling basert på lastbehov kjøres ved hjelp av en satsvis jobb, på samme måte som etterfylling basert på minimums- og maksimumsantall. Hvis du vil definere den satsvise jobben, går du til siden **Etterfylling basert på lastbehov**, velger etterfyllingsmalen som skal brukes, og angir en filterspørring for å angi hvilke laster som skal brukes til å bestemme behovet. Lokasjonsspørringen definerer lokasjonene som tilgjengelige antall trekkes fra for å dekke det samlede behovet for lastene.

## <a name="immediate-replenishment"></a>Umiddelbar etterfylling
I stedet for å måtte oppsummere kravet på slutten av en allokasjonsprosess og gjøre etterfylling på grunnlag av den oppsummerte mengden, kan du søke om umiddelbar etterfyllingsstrategi. Når du bruker denne strategien, kan beholdningen etterfylles umiddelbart etter at lokaliseringsdirektivet mislykkes. Derfor kan du sette opp etterfyllingen slik at den er begrenset av bestemte enheter, og slik at den bruker mengder som er angitt for bestemte lokasjoner.

## <a name="replenishment-prerequisites"></a>Forhåndskrav for etterfylling

|      Forutsetning       |                                                                                                                                beskrivelse                                                                                                                                 |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|          Element           |                                                                                                        Varn må aktiveres for lagerstyringsprosesser.                                                                                                        |
|        Lager        | Lageret må aktiveres for lagerstyringsprosesser. For å aktivere et lager for lagerbehandlingsprosesser, velg lageret på siden <strong>Lager</strong>, og velg deretter alternativet <strong>Bruk lagerstyringsprosesser</strong>. |
| Etterfyllingsmaler |                                                                   Minst én etterfyllingsmal må defineres for etterfylling basert på minimums- og maksimumsantall, etterfylling basert på bølgebehov eller etterfylling basert på lastbehov.                                                                   |
|        Lokasjoner        |                                                                                                       Lokasjoner må opprettes og kobles til en lokasjonsprofil.                                                                                                       |
|    Lokasjonsprofiler    |                                                                                                        Lokasjonsprofiler er nødvendig for å opprette lokasjoner.                                                                                                        |
|   Lokasjonsdirektiver   |                                                       Lokasjonsdirektiver kreves for å veilede arbeidet til de lokasjonene hvor etterfylling er nødvendig, og til lokasjonene som beholdningen er hentet fra.                                                        |
|     Arbeidsmaler      |                                                   Arbeidsmaler av typen <strong>Etterfylling</strong> er nødvendig for å opprette etterfyllingsarbeid, slik at beholdning kan flyttes til ønskede lokasjoner.                                                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
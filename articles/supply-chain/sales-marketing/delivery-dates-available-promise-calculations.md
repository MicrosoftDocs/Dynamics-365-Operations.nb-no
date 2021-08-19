---
title: Ordrebekreftelse
description: Dette emnet inneholder informasjon om ordrebekreftelser. Ordrebekreftelse bidrar til at du trygt kan love leveringsdatoer til kundene dine og gir deg fleksibilitet slik at du oppfyller disse datoene.
author: ShylaThompson
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesATP, SalesAvailableDlvDates, SalesCarrier
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b8317362a67b1b7e63f340b4badb722b28ea20709edc35bbbddef0d0e7a3e1b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711741"
---
# <a name="order-promising"></a>Ordrebekreftelse

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon om ordrebekreftelser. Ordrebekreftelse bidrar til at du trygt kan love leveringsdatoer til kundene dine og gir deg fleksibilitet slik at du oppfyller disse datoene.

Ordrebekreftelse beregner de tidligste leverings- og mottaksdatoene og er basert på kontrollmetoden for leveringsdato og transportdager. Du kan velge blant fire kontrollmetoder for leveringsdato:

-   **Salgsleveringstid** – Salgsleveringstiden er tiden mellom opprettelsen av salgsordren og leveringen av varene. Beregningen av leveringsdato er basert på et standard antall dager, og vurderer ikke lagertilgjengelighet, kjente behov eller planlagt forsyning.
-   **ATP (tilgjengelig for ordre)** – ATP er antallet av en vare som er tilgjengelig og kan loves til en kunde på en bestemt dato. ATP-beregningen inkluderer ikke igangsatt lager, leveringstider, planlagte mottak, og avganger.
-   **ATP + Avgang-margin**– Forsendelsesdatoen er lik ATP-datoen pluss antall sikkerhetsdager for varen. Sikkerhetsdager er tiden det tar å klargjøre varene for forsendelse.
-   **CTP (leveringskapasitet)**– Tilgjengelighet beregnes via nedbryting.

> [!NOTE]
> Når en salgsordre oppdateres, oppdateres bare informasjonen i ordrebekreftelsen hvis den eksisterende ordrebekreftelsesdatoen ikke kan oppfylles, som vist i følgende eksempler:
> 
> - **Eksempel 1**: Den gjeldende ordrebekreftelsesdatoen er 20. juli, men på grunn av økt antall, kan du ikke levere før 25. juli. Fordi gjeldende dato ikke lenger kan oppfylles, utløses ordrebekreftelsen.
> -  **Eksempel 2**: Den gjeldende ordrebekreftelsesdatoen er 20. juli, men på grunn av redusert antall, det er nå mulig å levere 15. juli. Fordi den gjeldende datoen fremdeles kan oppfylles, utløses ikke ordrebekreftelsen, og 20. juli forblir ordrebekreftelsesdatoen.

## <a name="atp-calculations"></a>ATP-beregninger
ATP-antallet beregnes basert på metoden "kumulativ ATP med blikk fremover". Den største fordelen med denne ATP-beregningsmetoden er at den kan håndtere tilfeller der summen av avganger mellom mottak er større enn siste mottak (for eksempel når et antall fra et tidligere mottak må brukes for å oppfylle et behov). Beregningsmetoden "kumulativ ATP med blikk fremover" inneholder alle avganger helt til det kumulative antallet som skal mottas, overskrider det kumulative antallet i avgang. Derfor evaluerer denne ATP-beregningsmetoden om noe av antallet fra en tidligere periode kan brukes i en senere periode.  

ATP-antallet er den ikke-fordelte lagerbalansen i den første perioden. Vanligvis beregnes det for hver periode der det er planlagt et mottak. Programmet beregner ATP-perioden i dager og beregner gjeldende dato som den første datoen for ATP-antallet. I den første perioden tar ATP med lagerbeholdning minus kundeordrer som forfaller eller er forfalt.  

ATP beregnes ved hjelp av følgende formel:  

ATP = ATP for forrige periode + mottak for gjeldende periode - avganger for gjeldende periode - netto avgangsantall for hver fremtidige periode, til perioden da summen av mottak for alle fremtidige perioder, opptil og inkludert den fremtidige perioden, er større enn summen av avganger, opptil og inkludert den fremtidige perioden.  

Legg merke til at ATP-beregningen ikke inneholder informasjon om utløpsdato og utover ATP-horisonten som systemet forventer når et hvilket som helst antall kan loves.

Når det ikke er flere avganger eller mottak å vurdere, er ATP-antallet for de etterfølgende datoene det samme som det sist beregnede ATP-antallet.  

Hvis ikke alle dimensjonene som brukes for en vare, er angitt når ATP-kontrollen er fullført, kan de likevel angis på avgangen eller mottakene. I dette tilfellet må mottakene og avgangene samles i de eksisterende dimensjonene i ATP-beregningen, for å redusere antall mottaks- og avgangslinjer som brukes i ATP-beregningen.  

ATP-antallet som vises, er alltid større enn eller lik 0 (null). Hvis beregningen returnerer et negativt ATP-antall (for eksempel hvis antallet som er lovet tidligere, overstiger det tilgjengelige antallet), settes antallet automatisk til 0.

### <a name="example"></a>Eksempel

Feltet **Horisont bakover for ATP-behov** kontrollerer hvor langt tilbake i tid det skal søkes etter forsinkede behovsordrer eller lageravganger. Feltet **Horisont bakover for ATP-forsyning** kontrollerer hvor langt tilbake i tid det skal søkes etter forsinkede forsyningsordrer eller lagermottak. Hvis for eksempel ordrer som er forsinket med bare sju dager, skal vurderes i ATP-beregningen, skal begge feltene settes til **7**.  

Feltene **Forskyvningstid for forsinket ATP-behov** og **Forskyvningstid for forsinket ATP-forsyning** styrer når forsinket behov eller forsyning skal vurderes i ATP-beregningen. Hvis for eksempel forsinket forsyning eller behov skal vurderes i ATP-beregningen om to dager, skal begge feltene settes til **2**. En verdi på **2** betyr at antallet for en vare i en forsinket bestilling som skal vurderes i ATP-beregningen, skal vises som tilgjengelig to dager etter dagens dato.  

I følgende eksempel angis **7** i feltene **Horisont bakover for ATP-behov** og **Horisont bakover for ATP-forsyning**, og **1** angis i feltene **Forskyvningstid for forsinket ATP-behov** og **Forskyvningstid for forsinket ATP-forsyning**.  

En bestilling på 200 enheter av et produkt som skulle ha vært mottatt for tre dager siden, er ikke mottatt ennå. Derfor er en salgsordrelinje for 75 stykk av det samme produktet som skulle være sendt i går, ikke sendt.  

En kunde ringer og ønsker å bestille 150 stykk av det samme produktet. Når du har kontrollert produktets tilgjengelighet, finner du ut at en ny bestilling for 100 enheter av produktet vil bli levert 10 dager senere.  

Du oppretter en salgsordrelinje for produktet og angir **150** som antall.  

Fordi leveringsdatokontrollen er metoden ATP, beregnes ATP-data for å finne den tidligst mulige forsendelsesdatoen. Basert på innstillingene vurderes den forsinkede bestillingen og salgsordren, og det resulterende ATP-antallet for den gjeldende datoen er 0. I morgen, når den forsinkede bestillingen forventes å mottas, beregnes ATP-antallet som mer enn 0 (i dette tilfellet beregnes det som 125). Men 10 dager fra nå, når tilleggsbestillingen på 100 enheter forventes å bli mottatt, blir ATP-antallet mer enn 150.  

Derfor settes forsendelsesdatoen til 10 dager fra nå basert på ATP-beregningen. Derfor kan du informere kunden om at det forespurte antallet kan leveres 10 dager fra nå.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Appen Lagersynlighet
description: Denne artikkelen beskriver hvordan du bruker Lagersynlighet-appen.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a360b8beaad2bf6916c22765131e37f90e40282b
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306181"
---
# <a name="use-the-inventory-visibility-app"></a>Bruk Inventory Visibility-appen

[!include [banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan du bruker Lagersynlighet-appen.

Lagersynlighet er en modelldrevet app for visualisering. Appen inneholder tre sider: **Konfigurasjon**, **Driftssynlighet** og **Lagersammendrag**. Den har følgende egenskaper:

- Det har et brukergrensesnitt for konfigurasjon av lagerbeholdning og konfigurasjon av ikke-forpliktende reservasjon.
- Den støtter spørringer av lagerbeholdning i sanntid for forskjellige dimensjonskombinasjoner.
- Den har et grensesnitt for postering av reservasjonsforespørsler.
- Den har en tilpasset visning av lagerbeholdningen for produkter sammen med alle dimensjoner.

## <a name="prerequisites"></a>Forutsetninger

Før du begynner, må du installere og konfigurere tillegget Lagersynlighet som beskrevet i [Installere og definere lagersynlighet](inventory-visibility-setup.md).

## <a name="open-the-inventory-visibility-app"></a>Åpne lagersynlighetsapen

Hvis du vil åpne Lagersynlighet-appen, kan du logge på Power Apps miljøet og åpne **Lagersynlighet**.

## <a name="configuration"></a><a name="configuration"></a>Konfigurasjon

**Konfigurasjon**-siden i Lagersynlighet-appen deg med konfigurasjon av lagerbeholdning og konfigurasjon av ikke-forpliktende reservasjon. Når tillegget er installert, inkluderer standardkonfigurasjonen en standardverdi for Microsoft Dynamics 365 Supply Chain Management (datakilden `fno`). Du kan gå gjennom standardinnstillingen. Heretter kan du, basert på forretningskravene og lagerposteringskravene i det eksterne systemet, endre konfigurasjonen for å standardisere hvordan lagerendringer kan posteres, organiseres og spørres i alle systemene.

Hvis du vil ha fullstendig informasjon om hvordan du konfigurerer løsningen, kan du se [Konfigurere lagersynlighet](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Driftssynlighet

På siden **Driftssynlighet** vises resultatene av en lagerbeholdningsspørring i sanntid, basert på diverse dimensjonskombinasjoner. Når *OnHandReservation*-funksjonen er aktivert, kan du også postere reservasjonsforespørsler fra siden **Driftssynlighet**.

### <a name="on-hand-query"></a>Beholdningsspørring

Fanen **Beholdningsspørring** viser resultatene av en lagerbeholdningsspørring i sanntid.

Når du velger fanen **Beholdningsspørring**, ber systemet deg om legitimasjon slik at det kan hente bærertokenet som kreves for å utføre en spørring i Lagersynlighet-tjenesten. Du kan bare lime inn bærertokenet i **Bærertoken**-feltet og lukke dialogboksen. Du kan deretter postere en forespørsel om lagerbeholdning.

Hvis bærertokenet ikke er gyldig, eller hvis det er utløpt, må du lime inn et nytt i **Bærertoken**-feltet. Angi riktige verdier for **Klient-ID**, **Leier-ID** og **Klienthemmelighet**, og velg deretter **Oppdater**. Systemet får automatisk et nytt, gyldig bærertoken.

Hvis du vil postere en lagerbeholdningsspørring, angir du spørringen i forespørselsteksten. Bruk mønsteret som er beskrevet i [Spør ved å bruke posteringsmetoden](inventory-visibility-api.md#query-with-post-method).

![Innstillinger for beholdningsspørring](media/inventory-visibility-query-settings.png "Innstillinger for beholdningsspørring")

### <a name="reservation-posting"></a>Postering av reservasjon

Bruk fanen **Postering av reservasjon** til å postere en reservasjonsforespørsel. Før du kan postere en reservasjonsforespørsel, må du aktivere funksjonen *OnHandReservation*. Hvis du vil ha mer informasjon om denne funksjonen, kan du se [Lagersynlighetsreservasjoner](inventory-visibility-reservations.md).

Hvis du vil postere en reservasjonsforespørsel, må du angi en verdi i forespørselsteksten. Bruk mønsteret som er beskrevet i [Opprett én reservasjonshendelse](inventory-visibility-api.md#create-one-reservation-event). Velg deretter **Poster**. Hvis du vil vise detaljer for forespørselssvaret, velger du **Vis detaljer**. Du kan også hente `reservationId`-verdien fra svardetaljene.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Lagersammendrag

Siden **Lagersammendrag** gir et lagersammendrag for produkter, sammen med alle dimensjoner. Det er en tilpasset visning for enheten *Lagerbeholdningssum*. Lagersammendragsdataene synkroniseres periodisk fra Lagersynlighet.

### <a name="enable-the-inventory-summary-and-set-the-synchronization-frequency"></a>Aktivere lagersammendraget og angi synkroniseringsfrekvensen

For å aktivere siden **Lagersammendraget** og angi synkroniseringsfrekvensen følger du denne fremgangsmåten:

1. Åpne **Konfigurasjon**-siden.
1. Åpne fanen **Funksjonsbehandling og -innstillinger**.
1. Sett veksleknappen for **OnHandMostSpecificBackgroundService**-funksjonen til *Ja*.
1. Når funksjonen er aktivert, blir **tjenestekonfigurasjonsdelen** tilgjengelig og inkluderer en rad for konfigurasjon av funksjonen **OnHandMostSpecificBackgroundService**. Med denne innstillingen kan du velge hvor ofte lagersammendragsdata skal synkroniseres. Bruk **Opp**- og **Ned**-knappene i **Verdi**-kolonnen til å endre tiden mellom synkroniseringene (som kan være så lave som 5 minutter). Velg deretter **Lagre**.
1. Velg **Oppdater konfigurasjon** for å lagre alle endringene.

![Innstillingen OnHandMostSpecificBackgroundService](media/inventory-visibility-ohms-freq.PNG "Innstillingen OnHandMostSpecificBackgroundService")

> [!NOTE]
> *OnHandMostSpecificBackgroundService*-funksjonen sporer bare endringer i lagerbeholdning som inntraff etter at du aktiverte funksjonen. Data for produkter som ikke har endret seg siden du aktiverte funksjonen, vil ikke bli synkronisert fra lagertjenestebufferen til Dataverse-miljøet. Hvis **Lagersammendrag**-siden ikke viser all lagerbeholdningsinformasjonen du forventer, kan du gå til **Lagerstyring > Periodiske oppgaver > Integrering av lagersynlighet**, deaktivere den satsvise jobben og aktivere den på nytt. Dette utfører den innledende overføringen, og alle data synkroniseres med enheten *Lagerbeholdningssum* i løpet av de neste 15 minuttene. Hvis du vil bruke denne funksjonen, anbefaler vi at du aktiverer den før du oppretter lagerbeholdningsendringer og aktiverer den satsvise jobben **Integrering av lagersynlighet**.

### <a name="work-with-the-inventory-summary"></a>Arbeid med lagersammendraget

Ved hjelp av det **avanserte filteret** i Dataverse kan du opprette en personlig visning som viser radene som er viktige for deg. Med de avanserte filteralternativene kan du opprette en rekke visninger, fra enkel til kompleks. I tillegg kan du legge til grupperte og nestede betingelser i filtrene. Hvis du vil lære mer om hvordan du bruker det **avanserte filteret**, kan du se [Rediger eller opprett personlige visninger ved hjelp av avanserte rutenettfiltre](/powerapps/user/grid-filters-advanced).

Øverst i den tilpassede visningen finner du tre felter: **Standarddimensjon**, **Egendefinert dimensjon** og **Mål**. Du kan bruke disse feltene til å bestemme hvilke kolonner som skal vises.

Du kan velge kolonnehodet for å filtrere eller sortere det gjeldende resultatet.

Nederst i den tilpassede visningen vises informasjon som for eksempel "50 poster (29 valgt)" eller "50 poster". Denne informasjonen refererer til postene som er lastet inn for øyeblikket fra resultatet av det **avanserte filteret**. Teksten "29 valgt" refererer til antall poster som er valgt ved hjelp av kolonnehodefilteret for de innlastede postene.

Nederst i visningen finner du en **Last inn flere**-knapp som du kan bruke til å laste inn flere poster fra Dataverse. Standard antall poster som lastes inn, er 50. Når du velger **Last inn flere**, lastes de neste 1000 tilgjengelige postene inn i visningen. Antallet på **Last inn flere**-knappen angir postene som er lastet inn for øyeblikket, og det totale antallet poster for resultatet av det **avanserte filteret**.

![Lagersammendrag](media/inventory-visibility-onhand-list.png "Lagersammendrag")

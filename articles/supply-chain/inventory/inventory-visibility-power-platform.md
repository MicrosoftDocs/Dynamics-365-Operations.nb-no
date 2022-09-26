---
title: Appen Lagersynlighet
description: Denne artikkelen beskriver hvordan du bruker Lagersynlighet-appen.
author: yufeihuang
ms.date: 09/15/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 674adb70cc4372a8c5ca8c75ed3ef840d8ec7b79
ms.sourcegitcommit: d2046cad5de570e6302a4390b41881a7ecb12e26
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/15/2022
ms.locfileid: "9520871"
---
# <a name="use-the-inventory-visibility-app"></a>Bruk Inventory Visibility-appen

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du bruker Lagersynlighet-appen.

Lagersynlighet er en modelldrevet app for visualisering. Appen inneholder tre sider: **Konfigurasjon**, **Driftssynlighet** og **Lagersammendrag**. Den har følgende egenskaper:

- Det har et brukergrensesnitt for konfigurasjon av lagerbeholdning og konfigurasjon av ikke-forpliktende reservasjon.
- Den støtter spørringer av lagerbeholdning i sanntid for forskjellige dimensjonskombinasjoner.
- Den har et grensesnitt for postering av reservasjonsforespørsler.
- Den har en visning av lagerbeholdningen for produkter sammen med alle dimensjoner.
- Den har en visning av en lagerbeholdningsliste for produkter sammen med forhåndsdefinerte dimensjoner.


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

Når du åpner fanen **Beholdningsspørring** på siden **Driftssynlighet**, ber systemet deg om legitimasjon slik at det kan hente bærertokenet som kreves for å utføre en spørring i Lagersynlighet-tjenesten. Du kan bare lime inn bærertokenet i **Bærertoken**-feltet og lukke dialogboksen. Du kan deretter postere en forespørsel om lagerbeholdning.

Hvis bærertokenet ikke er gyldig, eller hvis det er utløpt, må du lime inn et nytt i **Bærertoken**-feltet. Angi riktige verdier for **Klient-ID**, **Leier-ID** og **Klienthemmelighet**, og velg deretter **Oppdater**. Systemet får automatisk et nytt, gyldig bærertoken.

Hvis du vil postere en lagerbeholdningsspørring, angir du spørringen i forespørselsteksten. Bruk mønsteret som er beskrevet i [Spør ved å bruke posteringsmetoden](inventory-visibility-api.md#query-with-post-method).

![Innstillinger for beholdningsspørring](media/inventory-visibility-query-settings.png "Innstillinger for beholdningsspørring")

### <a name="reservation-posting"></a>Postering av reservasjon

Bruk fanen **Postering av reservasjon** på siden **Driftssynlighet** til å postere en reservasjonsforespørsel. Før du kan postere en reservasjonsforespørsel, må du aktivere funksjonen *OnHandReservation*. Hvis du vil ha mer informasjon om denne funksjonen og hvordan du aktiverer den, kan du se [Lagersynlighetsreservasjoner](inventory-visibility-reservations.md).

Hvis du vil postere en reservasjonsforespørsel, må du angi en verdi i forespørselsteksten. Bruk mønsteret som er beskrevet i [Opprett én reservasjonshendelse](inventory-visibility-api.md#create-one-reservation-event). Velg deretter **Poster**. Hvis du vil vise detaljer for forespørselssvaret, velger du **Vis detaljer**. Du kan også hente `reservationId`-verdien fra svardetaljene.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Lagersammendrag

Siden **Lagersammendrag** gir et lagersammendrag for produkter, sammen med alle dimensjoner. Det er en tilpasset visning for enheten *Lagerbeholdningssum*. Lagersammendragsdataene synkroniseres periodisk fra Lagersynlighet.

For å aktivere siden **Lagersammendraget** og angi synkroniseringsfrekvensen følger du denne fremgangsmåten:

1. Åpne **Konfigurasjon**-siden.
1. Åpne fanen **Funksjonsbehandling og -innstillinger**.
1. Sett veksleknappen for **OnHandMostSpecificBackgroundService**-funksjonen til *Ja*.
1. Når funksjonen er aktivert, blir **tjenestekonfigurasjonsdelen** tilgjengelig og inkluderer en rad for konfigurasjon av funksjonen **OnHandMostSpecificBackgroundService**. Med denne innstillingen kan du velge hvor ofte lagersammendragsdata skal synkroniseres. Bruk **Opp**- og **Ned**-knappene i **Verdi**-kolonnen til å endre tiden mellom synkroniseringene (som kan være så lave som 5 minutter). Velg deretter **Lagre**.

    ![Innstillingen OnHandMostSpecificBackgroundService](media/inventory-visibility-ohms-freq.png "Innstillingen OnHandMostSpecificBackgroundService")

1. Velg **Oppdater konfigurasjon** for å lagre alle endringene.


> [!NOTE]
> *OnHandMostSpecificBackgroundService*-funksjonen sporer bare endringer i lagerbeholdning som inntraff etter at du aktiverte funksjonen. Data for produkter som ikke har endret seg siden du aktiverte funksjonen, vil ikke bli synkronisert fra lagertjenestebufferen til Dataverse-miljøet. Hvis **Lagersammendrag**-siden ikke viser all lagerbeholdningsinformasjonen du forventer, kan du åpne Supply Chain Management, gå til **Lagerstyring > Periodiske oppgaver > Integrering av lagersynlighet**, deaktivere den satsvise jobben og aktivere den på nytt. Dette utfører den innledende overføringen, og alle data synkroniseres med enheten *Lagerbeholdningssum* i løpet av de neste 15 minuttene. Hvis du vil bruke *OnHandMostSpecificBackgroundService*-funksjonen, anbefaler vi at du aktiverer den før du oppretter lagerbeholdningsendringer og aktiverer den satsvise jobben **Integrering av lagersynlighet**.

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-the-inventory-visibility-onhand-query"></a>Forhåndslast en strømlinjeformet beholdningsspørring

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management har lagret mye informasjon om den gjeldende lagerbeholdningen, og gjør den tilgjengelig for en rekke formål. Imidlertid krever mange daglige operasjoner og tredjepartsintegrering bare et lite delsett av disse detaljene, og spørringer på systemet for alle kan føre til store datasett som tar tid å sette sammen og overføre. Derfor kan lagersynlighetstjenesten regelmessig hente og lagre et strømlinjeformet sett med lagerbeholdningsdata for å gjøre denne optimaliserte informasjonen kontinuerlig tilgjengelig. De lagrede detaljene for lagerbeholdning filtreres basert på konfigurerbare driftskriterier for å sikre at bare den mest relevante informasjonen inkluderes. Fordi de filtrerte lagerbeholdningslistene lagres lokalt i lagersynlighetstjenesten og oppdateres regelmessig, støtter de rask tilgang til dataeksporter etter behov og strømlinjeformet integrasjon med eksterne systemer.

> [!NOTE]
> Den gjeldende forhåndsversjonen av denne funksjonen kan bare gi forhåndslastede resultater som inkluderer nettsted og plassering. I den endelige versjonen av funksjonen forventes det at du skal kunne velge andre dimensjoner som forhåndslastes sammen med resultatene.

På siden **Forhåndslast lagersynlighetssammendraget** finner du en visning for enheten *Forhåndslast lagerindeksspørring*. I motsetning til enheten *Lagersammendrag* inneholder enheten *Forhåndslast lagerindeksspørring* en lagerbeholdningsliste for produkter sammen med valgte dimensjoner. Lagersynlighet synkroniserer de forhåndslastede sammendragsdataene hvert 15. minutt.

Hvis du vil vise data på fanen **Forhåndslast lagersynlighetssammendraget**, må du aktivere funksjonen *OnHandIndexQueryPreloadBackgroundService* på **Funksjonsbehandling**-fanen på **Konfigurasjon**-siden og deretter velge **Oppdater konfigurasjon** (se også [Konfigurer lagersynlighet](inventory-visibility-configuration.md)).

> [!NOTE]
> Som med funksjonen *OnhandMostSpecificBackgroudService* sporer funksjonen *OnHandIndexQueryPreloadBackgroundService* kun endringer i lagerbeholdningen som oppstod etter at du aktiverte funksjonen. Data for produkter som ikke har endret seg siden du aktiverte funksjonen, vil ikke bli synkronisert fra lagertjenestebufferen til Dataverse-miljøet. Hvis **Lagersammendrag**-siden ikke viser all lagerbeholdningsinformasjonen du forventer, kan du gå til **Lagerstyring > Periodiske oppgaver > Integrering av lagersynlighet**, deaktivere den satsvise jobben og aktivere den på nytt. Dette utfører den innledende overføringen, og alle data synkroniseres med enheten *Forhåndslast lagerindeksspørring* i løpet av de neste 15 minuttene. Hvis du vil bruke denne funksjonen, anbefaler vi at du aktiverer den før du oppretter lagerbeholdningsendringer og aktiverer den satsvise jobben **Integrering av lagersynlighet**.

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a>Filtrer og bla gjennom lagersammendragene

Ved hjelp av det **avanserte filteret** i Dataverse kan du opprette en personlig visning som viser radene som er viktige for deg. Med de avanserte filteralternativene kan du opprette en rekke visninger, fra enkel til kompleks. I tillegg kan du legge til grupperte og nestede betingelser i filtrene. Hvis du vil lære mer om hvordan du bruker det avanserte filteret, kan du se [Rediger eller opprett personlige visninger ved hjelp av avanserte rutenettfiltre](/powerapps/user/grid-filters-advanced).

Siden **Lagersammendrag** inneholder tre felter over rutenettet (**Standarddimensjon**, **Egendefinert dimensjon** og **Mål**) som du kan bruke til å kontrollere hvilke kolonner som er synlige. Du kan også velge et kolonnehode for å filtrere eller sortere det gjeldende resultatet etter denne kolonnen. Skjermbildet nedenfor uthever dimensjonen, filtreringen, resultatantallet og "last inn flere"-feltene som er tilgjengelige på siden **Lagersammendrag**.

![Siden Lagersammendrag.](media/inventory-visibility-onhand-list.png "Siden Lagersammendrag")

Siden du vil ha forhåndsdefinert dimensjonene som brukes til å laste inn sammendragsdata, viser siden **Forhåndslast lagersynlighetssammendraget** dimensjonsrelaterte kolonner. *Dimensjonene kan ikke tilpasses &mdash; systemet støtter bare dimensjonene nettsted og plassering for forhåndslastede lagerlister.* Siden **Forhåndslast lagersynlighetssammendraget** inneholder filtre som ligner på filtrene på siden **Lagersammendrag**, bortsett fra at dimensjonene allerede er valgt. Skjermbildet nedenfor uthever filtreringsfeltene som er tilgjengelige på siden **Forhåndslast lagersynlighetssammendraget**.

![Siden Forhåndslast lagersynlighetssammendraget.](media/inventory-visibility-preload-onhand-list.png "Siden Forhåndslast lagersynlighetssammendraget")

Nederst på sidene **Forhåndslast lagersynlighetssammendraget** og **Lagersammendrag** finner du informasjon, for eksempel "50 poster (29 valgt)" eller "50 poster". Denne informasjonen refererer til postene som er lastet inn for øyeblikket fra resultatet av det **avanserte filteret**. Teksten "29 valgt" refererer til antall poster som er valgt ved hjelp av kolonnehodefilteret for de innlastede postene. Det finnes også en **Last inn flere**-knapp som du kan bruke til å laste inn flere poster fra Dataverse. Standard antall poster som lastes inn, er 50. Når du velger **Last inn flere**, lastes de neste 1000 tilgjengelige postene inn i visningen. Antallet på **Last inn flere**-knappen angir postene som er lastet inn for øyeblikket, og det totale antallet poster for resultatet av det **avanserte filteret**.

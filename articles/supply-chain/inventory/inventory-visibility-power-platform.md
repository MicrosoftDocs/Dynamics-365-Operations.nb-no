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
ms.openlocfilehash: 0a4e436cc1af6b71049f75fb66bdfb89ca38df9f
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831781"
---
# <a name="use-the-inventory-visibility-app"></a>Bruk Inventory Visibility-appen

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du bruker Lagersynlighet-appen.

Lagersynlighet er en modelldrevet app for visualisering. Appen inneholder tre sider: **Konfigurasjon**, **Driftssynlighet** og **Lagersammendrag**. Den har følgende egenskaper:

- Det har et brukergrensesnitt for konfigurasjon av lagerbeholdning og konfigurasjon av ikke-forpliktende reservasjon.
- Den støtter spørringer av lagerbeholdning i sanntid for forskjellige dimensjonskombinasjoner.
- Den har et grensesnitt for postering av reservasjonsforespørsler.
- Den har en visning av lagerbeholdningen for produkter sammen med alle dimensjoner.
- Den har en visning av en lagerbeholdningsliste for produkter sammen med forhåndsdefinerte dimensjoner. Visningen av råvarelisten kan enten være et fullstendig sammendrag eller et forhåndslastet resultat fra en beholdningsspørring.

## <a name="prerequisites"></a>Forutsetninger

Før du begynner, må du installere og konfigurere tillegget Lagersynlighet som beskrevet i [Installere og definere lagersynlighet](inventory-visibility-setup.md).

## <a name="open-and-authenticate-the-inventory-visibility-app"></a><a name="open-authenticate"></a>Åpne og godkjenne Lagersynlighet-appen

For å åpne og godkjenne Lagersynlighet-appen følger du disse trinnene.

1. Logg på Power Apps-miljøet.
1. Åpne **Lagersynlighet**-app.
1. Åpne siden **Driftssynlighet** fra den venstre ruten.
1. Velg **Innstillinger**-knappen (tannhjulsymbol) øverst til høyre på siden.
1. I dialogboksen **Innstillinger** angir du du verdiene **Klient-ID**, **Leietaker-ID** og **Klienthemmelighet** som du noterte da du [installerte og konfigurerte Lagersynlighet](inventory-visibility-setup.md).
1. Velg **Oppdater**-knappen ved siden av **Bærertoken**-feltet. Systemet genererer et nytt bærertoken basert på informasjonen du har angitt.

    ![Innstillinger for beholdningsspørring.](media/inventory-visibility-query-settings.png "Innstillinger for beholdningsspørring")

1. Når du mottar et gyldig bærende token, lukker du dialogboksen. Bærertokenet utløper etter en tid. Derfor må du noen ganger oppdatere det når du må oppdatere konfigurasjonen, postere data eller spørredata.

## <a name="configure-the-inventory-visibility-app"></a><a name="configuration"></a>Konfigurere Lagersynlighet-appen

**Konfigurasjon**-siden i Lagersynlighet-appen lar deg konfigurere generell databehandling og funksjonskonfigurasjon. Når tillegget er installert, inkluderer standardkonfigurasjonen en standardverdi for Microsoft Dynamics 365 Supply Chain Management (datakilden `fno`). Du kan gå gjennom standardinnstillingen. Deretter kan du, basert på forretningskravene og lagerposteringskravene i det eksterne systemet, endre konfigurasjonen for å standardisere hvordan lagerendringer kan posteres, organiseres og spørres i alle systemene.

Hvis du vil ha fullstendig informasjon om hvordan du konfigurerer løsningen, kan du se [Konfigurere lagersynlighet](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Driftssynlighet

På siden **Driftssynlighet** vises resultatene av en lagerbeholdningsspørring i sanntid, reservasjonspostering og tildeling basert på diverse dimensjonskombinasjoner. Når *OnHandReservation*-funksjonen er [aktivert](inventory-visibility-configuration.md), kan du også postere reservasjonsforespørsler fra siden **Driftssynlighet**.

### <a name="on-hand-query"></a>Beholdningsspørring

Fanen **Beholdningsspørring** på siden **Driftssynlighet** lar deg spørre etter lagerbeholdningsspørring i sanntid. Følg disse trinnene for å angi og kjøre en spørring.

1. Åpne **Lagersynlighet**-app.
1. Åpne siden **Driftssynlighet** fra den venstre ruten.
1. I kategorien **Beholdningsspørring** angir du verdiene **Organisasjons-ID**, **Område-ID** og **Lokasjons-ID** som du vil utføre spørringer for.
1. I **Produkt-ID**-feltet angir du én eller flere produkt-IDer for å få et nøyaktig samsvar for spørringen. Hvis du lar **Produkt-ID**-feltet stå tomt, vil resultatene inkludere alle produkter på det angitte området og lokasjonen.
1. Hvis du vil få et mer detaljert resultat (for eksempel en visning etter dimensjonsverdier som farge og størrelse), velger du gruppert etter dimensjoner i **Grupper resultat etter**-feltet.
1. Hvis du vil finne varer som har en bestemt dimensjonsverdi (for eksempel farge = rød), velger du dimensjonen i **Filterdimensjoner**-feltet og angir deretter en dimensjonsverdi.
1. Velg **Spørring**. Du mottar enten en vellykket (grønn) melding eller en mislykket (rød) melding. Hvis spørringen mislykkes, må du kontrollere spørringskriteriene og kontrollere at [bærertoken](#open-authenticate) ikke er utløpt.

En annen måte å lage en lagerbeholdning-spørring på, er å sende direkte API-forespørsler. Du kan bruke `/api/environment/{environmentId}/onhand/indexquery` eller `/api/environment/{environmentId}/onhand`. Hvis du vil ha mer informasjon, kan du se [Offentlige API-er for lagersynlighet](inventory-visibility-api.md).

### <a name="reservation-posting"></a>Postering av reservasjon

Bruk fanen **Postering av reservasjon** på siden **Driftssynlighet** til å postere en reservasjonsforespørsel. Før du kan postere en reservasjonsforespørsel, må du aktivere funksjonen *OnHandReservation*. Hvis du vil ha mer informasjon om denne funksjonen og hvordan du aktiverer den, kan du se [Lagersynlighetsreservasjoner](inventory-visibility-reservations.md).

> [!NOTE]
> Muligheten til å foreta en ikke-forpliktende reservasjon i brukergrensesnittet er ment å la deg teste funksjonen. Hver ikke-forpliktende reserveringsforespørsel skal knyttes til en linjeendring for transaksjon (oppretting, endre, slette og så videre). Vi anbefaler derfor at du bare gjør en ikke-forpliktende reservervasjon som er koblet til en serverdelsordre. Hvis du vil ha mer informasjon, kan du se [Lagersynlighetsreservasjoner](inventory-visibility-reservations.md).

Følg denne fremgangsmåten for å postere en ikke-forpliktende reservasjonsforespørsel ved hjelp av brukergrensesnittet.

1. Åpne **Lagersynlighet**-app.
1. Åpne siden **Driftssynlighet** fra den venstre ruten.
1. Angi antallet du vil gjøre en ikke-forpliktende reservasjon for, i feltet **Antall** i kategorien **Postering av reservasjon**.
1. Fjern merket i boksen **Aktiver negativt lager for å støtte oversalg** for å hindre at aksjene blir oversolgt eller overreservert.
1. I **Operatør**-feltet velger du datakilden og det fysiske målet som skal gjelde for det mykt reserverte antallet.
1. Angi verdiene **Organisasjons-ID**, **Område-ID**, **Lokasjons-ID** og **Produkt-ID** som du vil utføre spørringer for.
1. Hvis du vil få et mer detaljert resultat, velger du en datakilde, dimensjoner og dimensjonsverdier.

En annen måte å gjøre en ikke-forpliktende reserervasjon på, er å sende direkte API-forespørsler. Bruk mønsteret som er beskrevet i [Opprett én reservasjonshendelse](inventory-visibility-api.md#create-one-reservation-event). Velg deretter **Poster**. Hvis du vil vise detaljer for forespørselssvaret, velger du **Vis detaljer**. Du kan også hente `reservationId`-verdien fra svardetaljene.

### <a name="allocation"></a>Tildeling

Hvis du vil ha informasjon om hvordan du administrerer fordelinger fra brukergrensesnittet og APIer, kan du se [Lagertildeling for Inventory Visibility](inventory-visibility-allocation.md).

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Lagersammendrag

Siden **Lagersammendrag** gir et lagersammendrag for produkter, sammen med alle dimensjoner. Det er en tilpasset visning for enheten *Lagerbeholdningssum*. Lagersammendragsdataene synkroniseres periodisk fra Lagersynlighet.

For å aktivere siden **Lagersammendraget** og angi synkroniseringsfrekvensen følger du denne fremgangsmåten:

1. Åpne **Konfigurasjon**-siden.
1. Åpne fanen **Funksjonsbehandling og -innstillinger**.
1. Sett veksleknappen for *OnHandMostSpecificBackgroundService*-funksjonen til *Ja*.
1. Når funksjonen er aktivert, blir **tjenestekonfigurasjonsdelen** tilgjengelig og inkluderer en rad for konfigurasjon av funksjonen **OnHandMostSpecificBackgroundService**. Med denne innstillingen kan du velge hvor ofte lagersammendragsdata skal synkroniseres. Bruk **Opp**- og **Ned**-knappene i **Verdi**-kolonnen til å endre tiden mellom synkroniseringene (som kan være så lave som 5 minutter). Velg deretter **Lagre**.

    ![Innstillingen OnHandMostSpecificBackgroundService](media/inventory-visibility-ohms-freq.png "Innstillingen OnHandMostSpecificBackgroundService")

1. Velg **Oppdater konfigurasjon** for å lagre alle endringene.

> [!NOTE]
> *OnHandMostSpecificBackgroundService*-funksjonen sporer bare endringer i lagerbeholdning som inntraff etter at du aktiverte funksjonen. Data for produkter som ikke har endret seg siden du aktiverte funksjonen, vil ikke bli synkronisert fra lagertjenestebufferen til Dataverse-miljøet. Hvis **Lagersammendrag**-siden ikke viser all lagerbeholdningsinformasjonen du forventer, kan du åpne Supply Chain Management, gå til **Lagerstyring > Periodiske oppgaver > Integrering av lagersynlighet**, deaktivere den satsvise jobben og aktivere den på nytt. Dette utfører den innledende overføringen, og alle data synkroniseres med enheten *Lagerbeholdningssum* i løpet av de neste 15 minuttene. Hvis du vil bruke *OnHandMostSpecificBackgroundService*-funksjonen, anbefaler vi at du aktiverer den før du oppretter lagerbeholdningsendringer og aktiverer den satsvise jobben **Integrering av lagersynlighet**.

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-streamlined-onhand-query"></a>Forhåndslast en strømlinjeformet beholdningsspørring

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management har lagret mye informasjon om den gjeldende lagerbeholdningen, og gjør den tilgjengelig for en rekke formål. Imidlertid krever mange daglige operasjoner og tredjepartsintegrering bare et lite delsett av disse detaljene, og spørringer på systemet for alle kan føre til store datasett som tar tid å sette sammen og overføre. Derfor kan lagersynlighetstjenesten regelmessig hente og lagre et strømlinjeformet sett med lagerbeholdningsdata for å gjøre denne optimaliserte informasjonen kontinuerlig tilgjengelig. De lagrede detaljene for lagerbeholdning filtreres basert på konfigurerbare driftskriterier for å sikre at bare den mest relevante informasjonen inkluderes. Fordi de filtrerte lagerbeholdningslistene lagres lokalt i lagersynlighetstjenesten og oppdateres regelmessig, støtter de rask tilgang til dataeksporter etter behov og strømlinjeformet integrasjon med eksterne systemer.

På siden **Forhåndslast lagersynlighetssammendraget** finner du en visning for enheten *Forhåndslast lagerindeksspørring*. I motsetning til enheten *Lagersammendrag* inneholder enheten *Forhåndslast lagerindeksspørring* en lagerbeholdningsliste for produkter sammen med valgte dimensjoner. Lagersynlighet synkroniserer de forhåndslastede sammendragsdataene hvert 15. minutt.

Hvis du vil vise data på fanen **Forhåndslast sammendraget for lagersynlighet**, må du slå på og konfigurere funksjonen *OnHandIndexQueryPreloadBackgroundService*. Se [Slå på og konfigurer forhåndslastede lagerbeholdningsspørringer](inventory-visibility-configuration.md#query-preload-configuration) for instruksjoner.

> [!NOTE]
> Som med funksjonen *OnHandMostSpecificBackgroundService* sporer funksjonen *OnHandIndexQueryPreloadBackgroundService* kun endringer i lagerbeholdningen som oppstod etter at du aktiverte funksjonen. Data for produkter som ikke har endret seg siden du aktiverte funksjonen, vil ikke bli synkronisert fra lagertjenestebufferen til Dataverse-miljøet. Hvis **Lagersammendrag**-siden ikke viser all lagerbeholdningsinformasjonen du forventer, kan du gå til **Lagerstyring > Periodiske oppgaver > Integrering av lagersynlighet**, deaktivere den satsvise jobben og aktivere den på nytt. Dette utfører den innledende overføringen, og alle data synkroniseres med enheten *Forhåndslast lagerindeksspørring* i løpet av de neste 15 minuttene. Hvis du vil bruke denne funksjonen, anbefaler vi at du aktiverer den før du oppretter lagerbeholdningsendringer og aktiverer den satsvise jobben **Integrering av lagersynlighet**.

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a>Filtrer og bla gjennom lagersammendragene

Ved hjelp av det **avanserte filteret** i Dataverse kan du opprette en personlig visning som viser radene som er viktige for deg. Med de avanserte filteralternativene kan du opprette en rekke visninger, fra enkel til kompleks. I tillegg kan du legge til grupperte og nestede betingelser i filtrene. Hvis du vil lære mer om hvordan du bruker det avanserte filteret, kan du se [Rediger eller opprett personlige visninger ved hjelp av avanserte rutenettfiltre](/powerapps/user/grid-filters-advanced).

Siden **Lagersammendrag** inneholder tre felter over rutenettet (**Standarddimensjon**, **Egendefinert dimensjon** og **Mål**) som du kan bruke til å kontrollere hvilke kolonner som er synlige. Du kan også velge et kolonnehode for å filtrere eller sortere det gjeldende resultatet etter denne kolonnen. Skjermbildet nedenfor uthever dimensjonen, filtreringen, resultatantallet og "last inn flere"-feltene som er tilgjengelige på siden **Lagersammendrag**.

![Siden Lagersammendrag.](media/inventory-visibility-onhand-list.png "Siden Lagersammendrag")

Siden du vil ha forhåndsdefinert dimensjonene som brukes til å laste inn sammendragsdata, viser siden **Forhåndslast lagersynlighetssammendraget** dimensjonsrelaterte kolonner. *Dimensjonene kan ikke tilpasses &mdash; systemet støtter bare dimensjonene nettsted og plassering for forhåndslastede lagerlister.* Siden **Forhåndslast lagersynlighetssammendraget** inneholder filtre som ligner på filtrene på siden **Lagersammendrag**, bortsett fra at dimensjonene allerede er valgt. Skjermbildet nedenfor uthever filtreringsfeltene som er tilgjengelige på siden **Forhåndslast lagersynlighetssammendraget**.

![Siden Forhåndslast lagersynlighetssammendraget.](media/inventory-visibility-preload-onhand-list.png "Siden Forhåndslast lagersynlighetssammendraget")

Nederst på sidene **Forhåndslast lagersynlighetssammendraget** og **Lagersammendrag** finner du informasjon, for eksempel "50 poster (29 valgt)" eller "50 poster". Denne informasjonen refererer til postene som er lastet inn for øyeblikket fra resultatet av det **avanserte filteret**. Teksten "29 valgt" refererer til antall poster som er valgt ved hjelp av kolonnehodefilteret for de innlastede postene. Det finnes også en **Last inn flere**-knapp som du kan bruke til å laste inn flere poster fra Dataverse. Standard antall poster som lastes inn, er 50. Når du velger **Last inn flere**, lastes de neste 1000 tilgjengelige postene inn i visningen. Antallet på **Last inn flere**-knappen angir postene som er lastet inn for øyeblikket, og det totale antallet poster for resultatet av det **avanserte filteret**.

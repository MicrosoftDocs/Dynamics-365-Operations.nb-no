---
title: Spør data med Warehouse Management-mobilappomveier
description: Denne artikkelen beskriver hvordan du konfigurerer menyelementer for mobilenheter for dataforespørsler og bruker dem som en del av omveier.
author: perlynne
ms.date: 08/01/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour,WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: c3ea53379badb3cb2ed71b7f102956d71c3f047a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220570"
---
# <a name="query-data-using-warehouse-management-mobile-app-detours"></a>Spør data med Warehouse Management-mobilappomveier

[!include [banner](../includes/banner.md)]

## <a name="feature-introduction"></a>Funksjonsinnføring

Ved hjelp av funksjoner for strekkodeskanning gir Warehouse Management-mobilappen deg en enkel og nøyaktig måte å registrere data på som en del av lagerprosessene. Strekkoder skades imidlertid noen ganger og blir uleselig, eller det kan hende at den nødvendige datainformasjonen ikke finnes som en strekkode i forretningsprosessflytene. I slike tilfeller kan manuell registrering av dataene ta lang tid, og til og med føre til at feil data registreres. Resultatene kan reduseres og gi et lavere servicenivå.

Ved hjelp av en fleksibel dataforespørselsprosess kan arbeidere enkelt slå opp den nødvendige informasjonen som en del av de innebygde Warehouse Management-mobilappflytene og bruke filtreringsalternativer slik at bare de relevante dataene vises. Derfor er manuell valg raskere og mer nøyaktig.

I den mottaksflyten for bestillingen kreves det for eksempel et bestillingsnummer for å samsvare med det ankommende lageret. Som en del av denne prosessen kan du lett konfigurere menyelementene slik at den gir en kortlistevisning av de relevante bestillingsnumrene. På denne måten kan du fortsette mottaksflyten ved å bruke en rask pek-og-velge-metode. Denne artikkelen inneholder eksempelscenarioer, men funksjonaliteten kan også brukes i noen av eller alle Warehouse Management-mobilappflytene.

## <a name="turn-on-the-data-inquiry-flow-feature-and-its-prerequisites"></a>Aktiver flytfunksjonen for dataforespørsler og forutsetningene

Før du kan bruke funksjonaliteten som er beskrevet i denne artikkelen, må du fullføre fremgangsmåten nedenfor for å aktivere de nødvendige funksjonene.

1. Gå til **Systemadministrasjon \> Arbeidsområder \> Funksjonsbehandling**. (Hvis du vil ha mer informasjon om hvordan du bruker arbeidsområdet **Funksjonsbehandling**, kan du se [Oversikt over funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Aktiver funksjonen som vises på følgende måte:

    - **Modul:** *Lagerstyring*
    - **Funksjonsnavn:** *Trinnvise instruksjoner i lagerapp*

    Denne funksjonen er en forutsetning for funksjonen *Dataforespørselsflyt for Warehouse Management-appen*. Hvis du vil ha mer informasjon om funksjonen *Trinnvise instruksjoner i lagerapp*, kan du se [Tilpass trinntitler og instruksjoner for mobilappen Warehouse Management](mobile-app-titles-instructions.md).

1. Aktiver funksjonen som vises på følgende måte:

    - **Modul:** *Lagerstyring*
    - **Funksjonsnavn:** *Omveier i Warehouse Management-appen*

    Denne funksjonen er en forutsetning for funksjonen *Dataforespørselsflyt for Warehouse Management-appen*. Hvis du vil ha mer informasjon om *Omveier i Warehouse Management-mobilappen*, kan du se [Konfigurer omveier for trinn i menyelementer for mobilenheter](warehouse-app-detours.md).

1. Hvis funksjonen *Omveier i Warehouse Management-mobilappen* ikke allerede var slått på, oppdaterer du feltnavnene i mobilappen Warehouse Management ved å gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Feltnavn i lagerapp** og velger **Opprett standardoppsett**. Gjenta dette trinnet for hver juridiske enhet (firma) der du bruker mobilappen Warehouse Management. For mer informasjon, se [Konfigur felter for mobilappen Lagerstyring](configure-app-field-names-priorities-warehouse.md).
1. Aktiver funksjonen som vises på følgende måte:

    - **Modul:** *Lagerstyring*
    - **Funksjonsnavn:** *Dataforespørselsflyt i Warehouse Management-appen*

    Denne funksjonen er en som er beskrevet i denne artikkelen.

## <a name="example-scenarios"></a>Eksempelscenarioer

Denne artikkelen bruker eksempelscenarioer for å vise hvordan du kan bruke funksjonen *Dataforespørselsflyt for Warehouse Management-mobilappen* til å forbedre innkjøpsmottaksflyten. Scenarioene bruker standard eksempeldata, som inkluderer en flyt kalt *Innkjøpsmottak*. Denne flyten starter ved å be arbeidere om å identifisere et bestillingsnummer de vil motta mot. For å gjøre det lettere for arbeiderne å identifisere bestillingen vil du forbedre den første siden i flyten ved å legge til følgende nye spørringsalternativer som [omveier](warehouse-app-detours.md):

- **Slå opp bestillinger etter leverandør** – Åpne en side der ansatte blir bedt om å angi et leverandørnavn eller en del av et leverandørnavn. Du kan bruke jokertegn. Hvis for eksempel en medarbeider forventer en innkommende levering i dag fra en leverandør som har *Tailspin* i navnet, kan vedkommende skrive **Tail\*** for å vise et sett med kort for åpne bestillinger som inneholder denne teksten. Hvert kort har flere felter som inneholder informasjon om hver bestilling. I tillegg til leverandørnavnet kan du utforme kortene slik at de viser leverandørens kontonummer, leveringsdato og dokumentstatus.
- **Slå opp bestillinger for i dag** – Åpne en side som ikke ber ansatte om å angi data, men i stedet vise forhåndskonfigurerte filtre (for eksempel dagens dato). Siden viser deretter et sett med kort som samsvarer med filteret. Arbeidere fortsetter ved å velge et kort for bestillingen som de vil registrere lagervarer mot.
- **Slå opp bestillinger etter vare** – Åpne en side som ber arbeiderne om å skanne strekkoden til en hvilken som helst vare i det ankomne lageret. Flyten viser deretter alle åpne bestillinger som inneholder linjer for det skannede varenummeret. For å dekke situasjoner der en strekkode ikke kan leses kan du legge til et annet omslagsoppslag på denne siden, der arbeiderne kan søke etter varenumre i en bestemt bestilling.

I hvert tilfelle identifiserer arbeideren en bestilling ved å velge et kort og returneres deretter til den første siden, som viser det valgte bestillingsnummeret. Arbeideren kan deretter fortsette den innkommende lagervareregistreringsflyten.

## <a name="enable-sample-data"></a>Aktivere eksempeldata

For å arbeide deg gjennom eksempelscenarioene som er beskrevet i denne artikkelen, må du arbeide på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert. Du må også velge den juridiske enheten *USMF* (firma) før du begynner.

## <a name="configure-the-mobile-device-menu-items"></a>Konfigurere mobilenhetsmenyelementene

Hvis du vil opprette alle de nye spørringsalternativene du må legge til på den første siden i flyten, må du definere det som menyelement for mobilenheter. Senere gjør du spørringsalternativene tilgjengelige som omveier til *innkjøpsmottaksflyten*.

### <a name="create-the-look-up-pos-by-vendor-menu-item"></a>Opprette menyelementet Slå opp bestillinger etter leverandør

Opprett **Slå opp bestillinger etter leverandør**-menyelementet ved å følge denne fremgangsmåten.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg **Ny** i handlingsruten for å legge til et menyelement for mobilenhet.
1. Angi deretter følgende verdier for det nye menyelementet:

    - **Menyelementnavn:** *Slå opp bestillinger etter leverandør*
    - **Tittel:** *Slå opp bestillinger etter leverandør*
    - **Modus:** *Indirekte*

1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Aktivitetskode:** *Dataforespørsler*
    - **Bruk prosesshåndbok:** *Ja* (Denne verdien velges automatisk.)
    - **Tabellnavn:** *PurchTable* (Du vil slå opp bestillingsnumre fra denne tabellen.)

1. Velg **Rediger spørring** i handlingsruten for å definere en spørring som er basert på den valgte basistabellen (i dette tilfellet bestillingstabellen).
1. I redigeringsprogrammet i fanen **Område** legger du til følgende linjer i rutenettet.

    | Tabell | Avledet tabell | Felt | Vilkår |
    |---|---|---|---|
    | Bestillinger | Bestillinger | Bestillingsstatus | Åpen ordre |
    | Bestillinger | Bestillinger | Leveringsdato | (dayRange(-10,10)) |
    | Bestillinger | Bestillinger | Navn på leverandør | |

1. Velg **OK**.

    I dette eksemplet konfigureres det nye menyelementet til å finne åpne bestillinger som forventes å ankomme når som helst mellom 10 dager i fortiden og 10 dager i fremtiden.

    I spørringen er **Kriterier**-kolonnen for *Leverandørnavn* tom. Derfor kan arbeidere angi denne verdien mens de bruker mobilappen Warehouse Management.

    Hvis du vil angi hvordan listen skal sorteres, kan du sette opp sorteringen i fanen **Sortering**.

1. I tillegg til å definere spørringen må du velge hvilke felter som skal vises på kortene på forespørselslistesiden. Velg derfor **Feltliste** på handlingsruten.
1. Angi følgende verdier på siden **Feltliste**:

    - **Vis felt 1:** *PurchId* (Dette feltet vil bli vist som hode for hvert kort.)
    - **Visningsfelt 2:** *PurchStatus*
    - **Visningsfelt 3:** *PurchName*
    - **Visningsfelt 4:** *OrderAccount*
    - **Visningsfelt 5:** *DeliveryDate*
    - **Vis felt 6:** *displayDocumentStatus()* (Denne verdien er en visningsmetode, som () på slutten angir.)

1. Velg **Lagre** i handlingsruten. Lukk deretter siden.

### <a name="create-the-look-up-pos-for-today-menu-item"></a>Opprette menyelementet Slå opp bestillinger for i dag

Opprett **Slå opp bestillinger for i dag**-menyelementet ved å følge denne fremgangsmåten.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg **Ny** i handlingsruten for å legge til et menyelement for mobilenhet.
1. Angi følgende verdier for det nye elementet:

    - **Menyelementnavn:** *Slå opp bestillinger for i dag*
    - **Tittel:** *Slå opp bestillinger for i dag*
    - **Modus:** *Indirekte*

1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Aktivitetskode:** *Dataforespørsler*
    - **Bruk prosesshåndbok:** *Ja* (Denne verdien velges automatisk.)
    - **Tabellnavn:** *PurchTable* (Du vil slå opp bestillingsnumre fra denne tabellen.)

1. Velg **Rediger spørring** i handlingsruten for å definere en spørring som er basert på den valgte basistabellen (i dette tilfellet bestillingstabellen).
1. I redigeringsprogrammet i fanen **Område** legger du til følgende linjer i rutenettet.

    | Tabell | Avledet tabell | Felt | Vilkår |
    |---|---|---|---|
    | Bestilling | Bestilling | Bestillingsstatus | Åpen ordre |
    | Bestilling | Bestilling | Leveringsdato | (Day(0)) |

1. Velg **OK**.

    I dette eksemplet konfigureres det nye menyelementet til å finne åpne bestillinger som forventes å ankomme i dag.

    Hvis du vil angi hvordan listen skal sorteres, kan du sette opp sorteringen i fanen **Sortering**.

1. I tillegg til å definere spørringen må du velge hvilke felter som skal vises på kortene på forespørselslistesiden. Velg derfor **Feltliste** på handlingsruten.
1. Angi følgende verdier på siden **Feltliste**:

    - **Vis felt 1:** *PurchName* (Dette feltet vil bli vist som hode for hvert kort.)
    - **Visningsfelt 2:** *PurchId*
    - **Visningsfelt 3:** *PurchStatus*
    - **Visningsfelt 4:** *DlvMode*
    - **Visningsfelt 5:** *DlvTerm*
    - **Visningsfelt 6:** *OrderAccount*
    - **Vis felt 7:** *VendorName()* (Denne verdien er en visningsmetode, som () på slutten angir.)

1. Velg **Lagre** i handlingsruten. Lukk deretter siden.

### <a name="create-the-look-up-pos-by-item-menu-item"></a>Opprette menyelementet Slå opp bestillinger etter element

Opprett **Slå opp bestillinger etter element**-menyelementet ved å følge denne fremgangsmåten.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg **Ny** i handlingsruten for å legge til et menyelement for mobilenhet.
1. Angi følgende verdier for det nye elementet:

    - **Menyelementnavn:** *Slå opp bestillinger etter element*
    - **Tittel:** *Slå opp bestillinger etter element*
    - **Modus:** *Indirekte*

1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Aktivitetskode:** *Dataforespørsler*
    - **Bruk prosesshåndbok:** *Ja* (Denne verdien velges automatisk.)
    - **Tabellnavn:** *PurchLine* (Du vil slå opp bestillingsnumre basert på varenummer via linjedataene.)

1. Velg **Rediger spørring** i handlingsruten for å definere en spørring som er basert på den valgte basistabellen (i dette tilfellet tabellen bestillingslinjer, men du kan bruke en hvilken som helst av verdiene som er knyttet til hodet ved å bli med i *PurchTable*).
1. I redigeringsprogrammet i fanen **Område** legger du til følgende linjer i rutenettet.

    | Tabell | Avledet tabell | Felt | Vilkår |
    |---|---|---|---|
    | Bestillingslinjer | Bestillingslinjer | Linjestatus | Åpen ordre |
    | Bestillingslinjer | Bestillingslinjer | Leveringsdato | (dayRange(-10,10)) |
    | Bestillingslinjer | Bestillingslinjer | Varenummer | |

1. Velg **OK**.

    I dette eksemplet konfigureres det nye menyelementet til å finne åpne bestillingslinjer som forventes å ankomme når som helst mellom 10 dager i fortiden og 10 dager i fremtiden.

    I spørringen er **Kriterier**-kolonnen for *Varenummer* tom. Derfor kan arbeidere angi denne verdien mens de bruker mobilappen Warehouse Management.

    Hvis du vil angi hvordan listen skal sorteres, kan du sette opp sorteringen i fanen **Sortering**.

1. I tillegg til å definere spørringen må du velge hvilke felter som skal vises på kortene på forespørselslistesiden. Velg derfor **Feltliste** på handlingsruten.
1. Angi følgende verdier på siden **Feltliste**:

    - **Vis felt 1:** *PurchId* (Denne feltverdien vil bli brukt som hode for hvert kort.)
    - **Visningsfelt 2:** *VendAccount*
    - **Visningsfelt 3:** *PurchQty*
    - **Visningsfelt 4:** *PurchUnit*
    - **Visningsfelt 5:** *PurchStatus*

1. Velg **Lagre** i handlingsruten. Lukk deretter siden.

## <a name="add-the-new-mobile-device-menu-items-to-a-menu"></a>Legge til nye menyelementer på en meny for mobilenhet

De tre nye menyelementene for mobilenheter er nå klare til å legges til i mobilenhetsmenyen. Denne oppgaven må være fullført før menyelementene kan brukes som en del av en omveisprosess. I dette eksemplet oppretter du en ny undermeny og legger til de nye menyelementene i den.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.
1. Velg **Ny** i handlingsruten.
1. Angi følgende verdier på toppteksten for den nye posten:

    - **Navn:** *Forespørsel*
    - **Beskrivelse:** *Forespør*

1. I listen **Tilgjengelige menyer og menyelementer** velger du først menyelementet for mobilenheten du nettopp opprettet. Velg høyre pil for å flytte det valgte menyelementet til **Menystruktur**-listen.
1. Gjenta det forrige trinnet for de to andre to nye menyelementene.
1. I listeruten til venstre velger du menyen **Hoved**.
1. I listen **Tilgjengelige menyer og menyelementer** ruller du ned til **Menyer**-delen og velger den nye **Forespørsel**-menyen. Velg høyre pil for å flytte det valgte menyelementet til **Menystruktur**-listen.

## <a name="configure-detours-in-your-mobile-device-steps"></a>Konfigurere omveier for trinnene for mobilenheter

For å fullføre oppsettet må du nå bruke avgangskonfigurasjonen på siden **Trinn for mobilenhet** til å legge til de tre nye menyelementene for mobilenhet i det eksisterende trinnet for bestillingsidentifikasjon i *Innkjøpsmottak*-flyten.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet > Trinn for mobilenhet**.
1. Angi *PONum* i **Filter**-feltet. Velg deretter *Trinn-ID: PONum* i rullegardinlisten.
1. Velg **Legg til trinnkonfigurasjon** i handlingsruten mens posten som blir funnet, velges i rutenettet. I rullegardinlisten som vises, bruker du **Menyelement**-feltet til å finne og velge *Innkjøpsmottak*. Velg **OK** for å lukke dialogboksen.
1. På detaljsiden for den nye trinnkonfigurasjonen (**Innkjøpsmottak: PONum**) i hurtigfanen **Tilgjengelige omveier (menyelementer)** velger du **Legg til** på verktøylinjen.
1. I dialogboksen **Legg til omvei** finner du og velger **Slå opp bestillinger etter leverandør**-menyelement som du opprettet tidligere.
1. Velg **OK** for å lukke dialogboksen og legge til det valgte menyelementet i omveislisten.
1. Velg den nye omveien, og velg deretter **Velg feltene som skal sendes** på verktøylinjen.
1. Ikke legg til noe i delen **Send fra innkjøpsmottak** i **Velg felter som skal sendes**-feltene, fordi du ikke vil sende noen verdier til omveismenyelementet. I delen **Hent tilbake fra slå opp bestillinger etter leverandør** angir du imidlertid følgende verdi for den tomme raden som allerede er lagt til der:

    - **Kopier fra Slå opp bestillinger etter leverandør:** *Bestilling*
    - **Lim inn i Innkjøpsmottak:** *Bestilling*

1. Velg **OK** for å lukke dialogboksen.
1. Gjenta trinn 4 til og med 9 for de to andre nye menyelementene (**Slå opp bestillinger for i dag** og **Slå opp bestillinger etter vare**). Som for **Slå opp bestillinger etter leverandør**-menyelement ønsker du ikke å sende data til disse omveiene, men du vil returnere et bestillingsnummer.
1. Lukk siden.

## <a name="try-a-purchase-receiving-flow-that-has-a-data-inquiry-as-part-of-a-detour"></a>Prøv en innkjøpsmottaksflyt som har en dataforespørsler som del av en omvei

Følg denne fremgangsmåten for å teste det nye mobilappoppsettet.

1. Opprett flere bestillinger som har linjer for lager 51.
1. Gå til en mobilenhet eller emulator som kjører mobilappen Lagerstyring, og logg på lager 51 ved å bruke *51* som bruker-ID og *1* som passord.
1. Velg **Innkommende** og deretter **Innkjøpsmottak** på mobilappmenyen.

    Du skal se den neste siden, som inneholder de tre nye menyelementene.

    ![Innkjøpsmottak med bestillingsnummer.](media/wma-purchase-receive-po-num-with-detours.png "Innkjøpsmottak med bestillingsnummer")

1. Prøv ut de forskjellige funksjonene, og legg merke til at du kan sende tilbake et bestillingsnummer ved å velge et av kortene i listen.

    ![Innkjøpsmottak med bestillingsoppslag etter leverandør, eksempel 1.](media/wma-purchase-receive-lookup-po-vendor-keyin-detours.png "Innkjøpsmottak med bestillingsoppslag etter leverandør, eksempel 1")

    ![Innkjøpsmottak med bestillingsoppslag etter leverandør, eksempel 2.](media/wma-purchase-receive-lookup-po-vendor-detours.png "Innkjøpsmottak med bestillingsoppslag etter leverandør, eksempel 2")

> [!TIP]
> I stedet for å kjøre mottaksflyten ved å gjøre et oppslag fra menyelementet **Innkjøpsmottak**, kan du starte fra en forespørselsflyt (**Hoved \> Forespørsel \> Slå opp bestillinger etter leverandør**), og starte en omvei for å kjøre den ønskede flyten ved å velge et av kortene i listen. Når du skal bruke denne fremgangsmåten, kan du definere en omvei på siden **Mobilenhetstrinn** for trinnet som har **Trinn-ID**-verdien til *GenericDataInquiryList*. Fordi denne flyten er en omvei, kan du ikke starte flere omveier fra den. Når du for eksempel kommer til registreringsskjermbildet for varenummer, er ikke oppslaget tilgjengelig på den, fordi systemet bare støtter ett nivå av omveier.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

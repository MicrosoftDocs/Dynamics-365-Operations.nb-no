---
title: Opprette lokasjonsdirektiver
description: Dette emnet forklarer hvordan du oppretter lokasjonsdirektiver. Lokasjonsdirektiver er brukerdefinerte regler som bidrar til å identifisere plukke- og plasseringslokasjoner for lagerbevegelse.
author: Mirzaab
manager: tfehr
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-28
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 4f634b7f526fd198b394af6d3870c43ee560813e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016776"
---
# <a name="create-location-directives"></a>Opprette lokasjonsdirektiver

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du oppretter lokasjonsdirektiver. Lokasjonsdirektiver er brukerdefinerte regler som bidrar til å identifisere plukke- og plasseringslokasjoner for lagerbevegelse. For en salgsordretransaksjon bestemmer for eksempel et lokasjonsdirektiv hvor varer blir plukket og hvor de plukkede varene skal plasseres.

> [!NOTE]
> Dette emnet gjelder funksjoner i **Lagerstyring** -modulen. Det gjelder ikke for funksjoner i modulen [Lagerstyring](../inventory/inventory-home-page.md).

Du kan bruke lokasjonsdirektiver til å utføre følgende oppgaver:

- Plasser innkommende varer.
- Plukk og plasser varer for utgående transaksjoner.
- Plukk og plasser råvarer for produksjon.
- Etterfyll lokasjoner.

## <a name="prerequisites"></a>Forutsetninger

Før du kan opprette et lokasjonsdirektiv, må du følge denne fremgangsmåten for å kontrollere at forutsetningene er på plass.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lagre**.
1. Opprett et lager.
1. På hurtigfanen **Lager** setter du alternativet **Bruk lagerstyringsprosesser** til *Ja*.
1. Opprett lokasjoner, lokasjonstyper, lokasjonsprofiler og lokasjonsformater. Hvis du vil ha mer informasjon, kan du se [Konfigurere lokasjoner i et WMS-aktivert lager](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).
1. Opprett steder, soner og sonegrupper. Hvis du vil ha mer informasjon, kan du se [Lageroppsett](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) og [Konfigurere lokasjoner i et WMS-aktivert lager](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).

## <a name="setup"></a>Installasjon

### <a name="create-location-directives"></a>Opprette lokasjonsdirektiver

Hvis du vil opprette et lokasjonsdirektiv, gjør du følgende.

1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. I listeruten angir du feltet **Arbeidsordretype** til den typen lagertransaksjon du skal opprette et lokasjonsdirektiv for.
1. I handlingsruten velger du **Ny** for å opprette et lokasjonsdirektiv.
1. For det nye lokasjonsdirektivet angir du feltene som beskrevet i følgende tabell.

    | Felt | beskrivelse |
    |---|---|
    | Serienummer | Angi et heltall som angir sekvensposisjonen til lokasjonsdirektivet. Sekvensposisjoner bestemmer når hvert lokasjonsdirektiv behandles for den valgte arbeidsordretypen. |
    | Navn | Angi et navn på lokasjonsdirektivet. | 
    | Arbeidstype | Velg hvilken type arbeid som skal utføres. Listen over verdier avhenger av typen lagertransaksjon som du har valgt i feltet **Arbeidsordretype**. Følgende verdier kan være tilgjengelige:<ul><li>**Plasser** – Lokasjonsdirektivet vil prøve å finne den beste lokasjonen for å plassere eller finne beholdning som kommer inn i systemet via mottak, produksjon eller lagerjusteringer. Lokasjonsdirektivet brukes også til å definere lokasjonen for plasseringen eller den endelige plasseringen på en forsendelseslokasjon i den utgående flyten.</li><li>**Plukk** – Lokasjonsdirektivet vil prøve å finne de beste lokasjonene for å reservere beholdning fysisk fra (opprette arbeid). Plukkingen kan fullføres (det vil si at plukklinjen kan lukkes), selv om arbeidet ikke er fullført. Brukeren kan fullføre fysisk plukking. I systemet er denne handlingen et plukketrinn. Brukeren kan deretter avbryte fra en mobilenhet og fullføre arbeidet (for eksempel plassering) senere. Arbeidshodet lukkes imidlertid først når den endelige plasseringen er fullført.</li><li>**Telling** , **Justeringer** , **Tilpasset** , **Endring av beholdningsstatus** , **Nummerskiltbygging** , **Utskrift** , **Statusendring** og **Pakk til nestede nummerskilt** – Disse verdiene kan ikke brukes i oppsettet av lokasjonsdirektivet.</li></ul> |
    | Site | Velg området der arbeidet skal fullføres. |
    | Lager | Velg lagerlokasjonen der arbeidet skal fullføres. |
    | Direktivkode | Velg en direktivkode for å veilede valget av lokasjonsdirektiver som er knyttet til plasseringslinjene for arbeidsmalen der denne koden er tilordnet. På siden **Direktivkode** kan du opprette nye koder som kan brukes til å koble en arbeidsmal til et lokasjonsdirektiv. Du kan også bruke denne siden til å opprette koblingen mellom en hvilken som helst linje i en arbeidsmal og et lokasjonsdirektiv (for eksempel en rampedør eller en stadieplassering). Hvis du vil ha mer informasjon om hvordan du konfigurerer en direktivkode med en arbeidsmal, kan du se [Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver](control-warehouse-location-directives.md).<p>Hvis en direktivkode er angitt, når arbeid må genereres, søker systemet etter lokasjonsdirektiver per direktivkode i stedet for per sekvens. På denne måten kan du være mer nøyaktig angående lokasjonsmalen som brukes for et spesifikt trinn i en arbeidsmal, for eksempel trinnet for oppsamling av materialer.</p> |
    | Disposisjonskode | Velg en disposisjonskode for å omdirigere plasseringen av mottatte varer til en lokasjon. (Hvis du vil ha mer informasjon, kan du se [Definere disposisjonskoder](tasks/set-up-dispositions-codes.md).) Dette feltet er bare tilgjengelig når **Arbeidsordretype** -feltet er angitt til *Bestillinger* , *Returordrer* eller *Plasser ferdigvarer*. |
    | Flere SKUer | Sett dette alternativet til *Ja* for å bruke flere lagerenheter (SKU-er) på en lokasjon. Dette alternativet må for eksempel angis til *Ja* for rampedøren.<p>Hvis alternativet **Flere SKUer** er satt til *Ja* , blir plasseringslokasjonen angitt i arbeidet (som forventet). Plasseringslokasjonen kan imidlertid bare håndtere plassering av flere varer hvis arbeidet inneholder forskjellige SKU-er som må plukkes og plasseres, ikke hvis arbeidet bare omfatter én enkelt SKU som må plasseres.</p><p>Hvis **Flere SKUer** er satt til *Nei* , blir plasseringslokasjonen bare angitt hvis plasseringen bare har én type SKU.</p><p>Hvis du skal bruke begge fremgangsmåtene, må du angi to linjer som har samme struktur og oppsett, men angi alternativet **Flere SKUer** til *Ja* for én av linjene og *Nei* for den andre. Det kreves med andre ord to identiske lokasjonsdirektiver for plasseringsoperasjoner, selv om du ikke trenger å skille mellom én eller flere SKU-er i arbeids-ID-en. Du må også angi et lokasjonsdirektiv for plukking hvis du har en ordre med mer enn én vare.</p><p>**Obs!** Hvis du setter **Flere SKUer** til *Ja* for et lokasjonsdirektiv av arbeidstypen *Plasser* , vil systemet alltid velge den første linjen i lokasjonsdirektivet, uavhengig av andre begrensninger som er opprettet i linjene.</p> |

1. Valgfritt: Velg **Rediger spørring** i handlingsruten for å velge lokasjonene eller for å angi begrensninger som gjelder når du velger et bestemt lokasjonsdirektiv.
1. I hurtigfanen **Linjer** oppretter du én eller flere linjer for å angi enheter og finne eller reservere antall på et lager.
1. På hver nye linje angir du feltene som beskrevet i følgende tabell.

    | Felt | beskrivelse |
    |---|---|
    | Serienummer | Angi et heltall som angir sekvensposisjonen til lokasjonsdirektivet. Sekvensposisjoner bestemmer når hvert lokasjonsdirektiv behandles for den valgte arbeidstypen. |
    | Fra-antall | Angi det begynnende antallsområdet for når sekvensen i midten av rutenettet skal velges. Angi antallet i måleenheten som er valgt i **Enhet** -feltet. |
    | Til antall | Angi det avsluttende antallsområdet for når sekvensen i midten av rutenettet skal velges. Angi antallet i måleenheten som er valgt i **Enhet** -feltet. |
    | Enhet | Velg måleenhet for varene.<p>Du kan angi et minimumsantall og et maksimumsantall som direktivet skal gjelde for. Du kan også angi at direktivet skal brukes for en bestemt lagerenhet. **Enhet** -feltet brukes bare for evaluering av antall.</p><p>For å finne ut om en lokasjonsdirektivlinje gjelder evaluerer systemet antall ved hjelp av **Enhet** -verdien som er angitt på linjen. Hver gang en lokasjonsdirektivlinje nås, prøver systemet å konvertere behovsenheten til enheten som er angitt på linjen. Hvis enhetskonverteringen ikke finnes, går systemet videre til neste linje.</p> |
    | Plasser antall | Dette feltet er bare gyldig når du prøver å plassere eller finne antall på lageret. Med andre ord er det bare gyldig for *Plassering* -arbeid. Velg metoden som brukes til å evaluere om antallet er i området som er angitt i feltene **Fra-antall** og **Til-antall**. Hvis lokasjonsdirektivet er for en inngående transaksjon, velger du ett av følgende alternativer:<ul><li>**Nummerskiltantall** – Når du skal vurdere om et antall er innenfor målantallsområdet, kan du bruke antallet på nummerskiltet som mottas.</li><li>**Antall delt opp i enheter** – Når du skal vurdere om et antall er innenfor målantallsområdet, kan du bruke antallet som er delt opp i enheter under transaksjonen. Hvis du for eksempel kan motta et antall på 1000 på et lager, og dele det opp i 10 nummerskilt på 100 hver, kan du bruke et antall på 1000 varer i stedet for nummerskiltantallet på 100.</li><li>**Restantall** – Når du skal vurdere om et antall er innenfor målantallsområder, kan du bruke antallet som gjenstår for mottak på bestillingslinjen som sjekkes inn.</li><li>**Forventet antall** – Når du skal vurdere om et antall er innenfor målantallsområdet, kan du bruke det totale tallet på bestillingslinjen, uavhengig av antallet som allerede er mottatt.</li></ul> |

1. Valgfritt: Du kan angi følgende ekstra felt på hurtigfanen **Linjer**.

    | Felt | beskrivelse |
    |---|---|
    | Begrens etter enhet | Merk av i denne boksen for å begrense måleenhetene som vurderes som gyldige valgkriterier for lokasjonsdirektivlinjene. Når det er angitt måleenheter, regnes bare varer der enheten samsvarer med minst én enhet som er definert for enhetssekvensgruppen, som gyldig for linjevalget.<p>Enheten er for eksempel begrenset til paller, og varen er knyttet til en enhetssekvensgruppe som inkluderer *Paller* -enheten. I dette tilfellet vil varene anses som et gyldig alternativ for lokasjonsdirektivet.</p><p>Avmerkingsboksen **Begrens etter enhet** styrer imidlertid ikke enheten eller enhetene som brukes på arbeidslinjer. Enhetsbegrensningen gjelder bare for enhetene som gjøres tilgjengelige via enhetssekvensgruppen.</p><p>En vare er for eksempel knyttet til en enhetssekvensgruppe som inkluderer både *Paller* -enheten og *Stykk* -enheten. En måleenhet er definert der 1 pall = 100 stykk, og lokasjonsdirektivet bruker funksjonen **Begrens etter enhet** bare for paller. I tillegg er det definert en arbeidsmal som begrenser opprettelsen av arbeidshodet til 50 stykk. I dette tilfellet vil det bli opprettet arbeidslinjer på 50 stykk.</p><p>Følg denne fremgangsmåten for å angi måleenheten for begrensning</p><ol><li>På hurtigfanen **Linjer** velger du **Begrens etter enhet**. Denne knappen blir tilgjengelig når du merker av for **Begrens etter enhet** på linjen og deretter velger **Lagre**.</li><li>I **Enhet** -feltet velger du måleenheten det skal begrenses etter, for plukkingen og plasseringen.</li></ol> |
    | Avrund oppover til enhet | Velg dette alternativet for å angi at råvareplukking skal rundes opp til et multiplum av håndteringsenheten som er angitt i feltet **Begrens etter enhet**. Dette feltet gjelder bare for råvareplukking og lokasjonsdirektiver av typen *Plukk*. |
    | Plasser pakkeantall | Merk av i denne boksen hvis et emballasjeenhetsantall er angitt på siden **Salgordre**. Hvis du merker av for dette alternativet, velges bare lokasjoner som har dette emballasjeenhetsantallet. |
    | Tillat deling | Velg denne avmerkingsboksen for å dele antallet på flere lokasjoner. |
    | Mal for umiddelbar etterfylling | Opprett en tilkobling til en etterfyllingsmal, slik at etterfylling starter umiddelbart hvis varer ikke er tildelt. Hvis dette feltet er tomt, starter ikke etterfylling før alle linjene i lokasjonsdirektivet er behandlet.<p>Dette feltet er bare tilgjengelig på valgte arbeidsordretyper der etterfylling er tillatt, for eksempel *Salgsordrer* og *Råvareplukking*.</p> |

1. På hurtigfanen **Handlinger for lokasjonsdirektiv** velger du **Ny** for å velge lokasjon eller lokasjonsområder.
1. **Sevkensnummer** -feltet viser sekvensen som lokasjons direktivetblir behandlet i, for den valgte arbeidstypen. Du kan endre rekkefølgen. Vær imidlertid forsiktig med sekvensnumre for lokasjonsdirektivhandlinger, fordi lokasjonsdirektiver alltid vil kjøre i denne sekvensen.
1. I **Navn** -feltet angir du navnet på lokasjonsdirektivhandlingen. Vær spesifikk, slik at det er tydelig hva handlingen er.
1. Valgfritt: Velg **Rediger spørring** for å endre lagerlokasjoner og andre kriterier.
1. Valgfritt: Du kan angi følgende tilleggsfelt for et lokasjonsdirektiv.

    | Felt | beskrivelse |
    |---|---|
    | Bruk av fast lokasjon | Velg hvilke lokasjoner som lokasjonsdirektivet skal vurdere:<ul><li>**Faste og ikke-faste lokasjoner** – Lokasjonsdirektivet tar alle lokasjoner i betraktning.</li><li>**Bare faste lokasjoner for produktet** – Lokasjonsdirektivet tar bare faste lokasjoner for produkter i betraktning.</li><li>**Bare faste lokasjoner for produktvarianten** – Lokasjonsdirektivet tar bare faste lokasjoner for produktvarianter i betraktning.</li></ul> |
    | Tillat negativ beholdning | Velg denne avmerkingsboksen for å tillate negativ beholdning på den angitte lagerlokasjonen. |
    | Parti aktivert | Velg denne avmerkingsboksen for å bruke partistrategier for varene som er partiaktivert. Hvis det er merket av i denne avmerkingsboksen, og **Strategi** -feltet er satt til *Ingen* , går systemet videre til den neste handlingslinjen. |
    | Strategi | Velg strategien som lokasjonsdirektivet skal bruke:<ul><li>**Ingen** – Ingen strategi blir brukt.</li><li>**Samsvar pakkeantall** – Denne strategien kontrollerer om en plukklokasjon har det angitte pakkeantallet. Denne strategien er bare gyldig når feltet **Arbeidstype** er satt til *Plukk*.</li><li>**Konsolider** – Denne strategien konsoliderer varer på en spesifikk lokasjon når det allerede finnes like varer. Denne strategien er bare gyldig når feltet **Arbeidstype** er satt til *Plasser*. I et typisk oppsett for plassering forsøker systemet å konsolidere på den første handlingslinjen, og deretter prøver det å plassere uten konsolidering på den andre handlingslinjen. Konsolidering av varer gjør senere plukking mer effektivt.</li><li>**FEFO-partireservering** – Denne strategien brukes når beholdningen plasseres ved hjelp av en utløpsdato for parti og tilordnes partireserveringen. Partireserveringsstrategien FEFO brukes også når beholdningen plasseres ved hjelp av en best før-dato for parti i tillegg til utløpsdatoen. Du kan bare bruke denne strategien for partiaktiverte varer. Denne strategien er bare gyldig når feltet **Arbeidstype** er satt til *Plukk*. Når du velger denne strategien, overstyrer du enhver spørringssortering for partinumre som er brukt.</li><li>**Avrund oppover til fullstendig nummerskilt** – Denne strategien avrunder lagerantallet oppover, slik at det tilsvarer nummerskiltantallet som er tilordnet varene som må plukkes. Denne strategien kan bare brukes for lokasjonsdirektiver av etterfyllingstypen, og bare når feltet **Arbeidstype** er satt til *Plukk*.</li><li>**Tom plassering med innkommende arbeid** – Denne strategien brukes til å finne tomme lokasjoner. En lokasjon anses som tom hvis den ikke har fysisk beholdning og ikke forventet innkommende arbeid. Denne strategien er bare gyldig når feltet **Arbeidstype** er satt til *Plasser*.</li></ul> |

## <a name="example-of-the-use-of-location-directives"></a>Eksempel på bruk av lokasjonsdirektiver

I dette eksemplet vurderes det en bestillingsprosess der lokasjonsdirektivet må finne ledig kapasitet i et lager for lagervarer som nettopp er registrert i mottakssonen. Først må du prøve å finne ledig kapasitet i lageret ved å konsolidere med eksisterende lagerbeholdning. Hvis konsolidering ikke er mulig, må du finne en ledig lokasjon.

I dette scenariet må du definere to lokasjonsdirektivhandlinger. Den første handlingen i sekvensen må bruke strategien **Konsolider** og andre må bruke strategien **Tom lokasjon uten innkommende arbeid**. Med mindre du definerer en tredje handling for å håndtere et overflytscenario er to resultater mulig når det er ikke mer kapasitet i lageret: arbeid kan opprettes selv om ingen lokasjoner defineres, eller arbeidsopprettingsprosessen kan mislykkes. Resultatet bestemmes av oppsettet på siden **Feil med lokasjonsdirektiv** der du kan bestemme om du vil velge alternativet **Stopp arbeid ved feil med lokasjonsdirektiv** for hver arbeidsordretype.

## <a name="next-step"></a>Neste trinn

Når du har opprettet lokasjonsdirektiver, kan du knytte hver direktivkode til en arbeidsmalkode for arbeidsoppretting. Hvis du vil ha mer informasjon, kan du se [Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="technical-information-for-system-admins"></a>Teknisk informasjon for systemansvarlige

Hvis du ikke har tilgang til sidene som brukes til å fullføre denne oppgaven, kontakt systemansvarlig, og angi informasjonen som vises i følgende tabell.

| Kategori | Forutsetning |
|---|---|
| Konfigurasjonsnøkler | Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon**. Utvid lisensnøkkelen **Handel** , og velg deretter konfigurasjonsnøkkelen **Lager- og transportstyring**. |

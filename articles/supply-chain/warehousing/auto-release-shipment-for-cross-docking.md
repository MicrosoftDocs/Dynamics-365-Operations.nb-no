---
title: Automatisk frigivelse av forsendelse for direkteoverføring
description: Denne artikkelen beskriver en kryssoverføringsstrategi som lar deg automatisk frigi en behovsordre til lageret når produksjonsordren som leverer behovsantallet, rapporteres som ferdig, slik at antallet flyttes direkte fra produksjonsutleveringsstedet til den utgående lokasjonen.
author: Mirzaab
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: c7199f5a5a401e627bb5fac9dece3950900e5f97
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067919"
---
# <a name="auto-release-shipment-for-cross-docking"></a>Automatisk frigivelse av forsendelse for direkteoverføring

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver en direkteoverføringsstrategi som lar deg automatisk frigi en behovsordre til lageret når produksjonsordren som leverer behovsantallet, rapporteres som fullført. På denne måten flyttes antallet som kreves for å fullføre behovsordren, direkte fra produksjonsutleveringslokasjonen til den utgående lokasjonen.

Direkteoverføring er en lagerhåndteringsflyt der antallet som kreves for å oppfylle en utgående ordre, dirigeres til ordrens utleveringsport eller oppsamlingsområde fra lokasjonen der den inngående bestillingen ble mottatt. (Den inngående ordren kan være en bestilling, en overføringsordre eller en produksjonsordre.) Mens den avanserte direkteoverføringfunksjonen støtter alle forsynings- og behovsordrer, og det krever at det utgående behovet frigis før direkteoverføringsmuligheten identifiseres, har funksjonen for automatisk frigivelse av forsendelse disse egenskapene:

- Det støtter bare produksjonsordrer som forsyning, og bare salgsordrer og overføringsordrer som behov.
- Direkteoverføringsoperasjonen kan startes selv om behovsordren ikke ble frigitt til lageret før forsyningsmottaket ble registrert (det vil si før produksjonen ble rapportert som fullført).

Denne direkteoverføringsfunksjonaliteten har to fordeler:

- Lageroperasjonene kan hoppe over trinn med å plassere ferdigmeldte varer i den vanlige lagerbeholdningen hvis disse antallene bare blir plukket opp igjen for å oppfylle den utgående ordren. I stedet kan antallet flyttes én gang, fra utleveringslokasjonen til en emballasje-/forsendelseslokasjon. På denne måten bidrar funksjonaliteten til å minimere antall ganger lageret behandles, og det bidrar til å maksimere tids- og plassbesparelser på lagerproduksjonsgulvet.
- Lageroperasjonene kan utsette frigivelsen av salgsordrer og overføringsordrer til lageret inntil ferdigmelding av ferdige varer for den tilknyttede produksjonsordren er ferdigmeldt. Denne fordelen kan være spesielt relevant i produksjonsmiljøer med produser-etter-ordre, der fremskaffelsestid pleier å være lengre enn leveringstiden i produser-til-lager-miljøer.

## <a name="prerequisites"></a>Forutsetninger

| Forutsetning | Beskrivelse |
|---|---|
| Element | Varen må aktiveres for Warehouse Management-prosesser (WMS).<p>**Merk:** Faktisk vekt-aktiverte varer kan ikke inkluderes i direkteoverføringprosessene.</p> |
| Lager | Lageret må aktiveres for Warehouse Management-prosesser (WMS). |
| Direkteoverføringsmaler | Minst én direkteoverføringsmal som bruker **Ved forsyningsmottak**-policyen for behovsfrigivelse, må defineres for et gitt lager. |
| Arbeidsklasse | En arbeidsklasse-ID for direkteoverføring må opprettes for arbeidsordretypen **Direkteoverføring**. |
| Arbeidsmaler | Arbeidsmaler i **Direkteoverføring**-arbeidoppdragstypen kreves for å opprette plukke- og plasseringsarbeid for direkteoverføring. |
| Lokasjonsdirektiver | Plasseringsdirektiver for **Direkteoverføring**-arbeidsordretypen kreves for å få styre plasseringsarbeid i lokasjonene der salgsordremengder skal pakkes og sendes. |
| Merke mellom en behovsordre og en produksjonsordre | Lagersystemet kan utløse automatisk frigivelse av den utgående ordreforsendelsen og opprette direkteoverføringsarbeid fra utleveringslokasjonen bare i handlingen ferdigmeldt hvis salgsordrer og overføringsordrer er reservert og merket mot en produksjonsordre. |

## <a name="example-cross-docking-flow"></a>Eksempel på direkteoverføringflyt

En vanlig direkteoverføringsflyt består av følgende hovedtrinn.

1. En salgsordretaker oppretter en salgsordre for et produser-til-ordre-produkt. Det forespurte antallet er vanligvis ikke på lager og må først produseres.
2. Salgsordretakeren oppretter en produksjonsordre direkte fra salgsordrelinjen. På denne måten reserverer og merker ordretakeren salgsordreantallet mot produksjonsordreantallet. 

    En produksjonsplanlegger angir eventuelt at merking må oppdateres når planlagte ordrer autoriseres.

3. Produksjonsordren går gjennom følgende trinn:

    1. En produksjonsplanlegger beregner og frigir produksjonsordren. (Estimering omfatter råvarereservering, og frigivelsen tar med utgivelsen til et lager.)
    2. En lagerarbeider starter og fullfører råvareplukking fra lagringslokasjonen til produksjonstilførselslokasjonen, i henhold til produksjonsplukkarbeidet.
    3. En Shop Floor-operatør starter produksjonsordren.
    4. I den siste operasjonen bruker en maskinoperatør den mobile enheten til å rapportere produksjonsordren som ferdigmeldt.

4. Systemet bruker oppsettet til å identifisere direkteoverføringhendelsen for de to koblede ordrene, og fullfører deretter disse oppgavene:

    1. Frigi den tilknyttede salgsordren automatisk til et lager for å opprette en forsendelse.
    2. Opprett automatisk direkteoverføringarbeid som har instruksjoner for å plukke ferdigvarene fra utleveringslokasjonen, og flytte dem til den utgående lokasjonen som direkteoverføringlokasjonen tilordnet til salgsordren.
    3. Be en maskinoperatør om å fullføre direkteoverføringsjobben umiddelbart etter at produksjonsordren er ferdigmeldt.

5. Når direkteoverføringen er fullført, og antallene lastes inn på kjøretøyet, bekrefter en utgående lagerplanlegger salgsforsendelsen.

## <a name="example-scenario"></a>Eksempelscenario

For dette scenarioet må du ha demonstrasjonsdata installert, og du må bruke demonstrasjonsdataene for firmaet **USMF**.

### <a name="set-up-cross-docking-that-uses-the-auto-release-shipment-feature"></a>Konfigurer direkteoverføring som bruker funksjonen for automatisk frigivelse av forsendelse

#### <a name="cross-docking-template"></a>Direkteoverføringsmal

1. Gå til **Lagerstyring** \> **Oppsett** \> **Arbeid** \> **Direkteoverføringsmaler**.
2. Velg **Ny**.
3. Angi **1** i feltet **Serienummer**.
4. I feltet **Direkteoverføringsmal-ID** angir du et navn, for eksempel **XDock\_Ferdigmeld**.
5. I feltet for **Policy for behovsfrigivelse** velger du **Ved forsyningsmottak**.
6. I **Lager**-feltet angir du nummeret til lageret der du vil definere direkteoverføringprosessen. Velg **51** for dette eksemplet.

    > [!NOTE]
    > Så snart du velger **Ved forsyningsmottak** som policy for behovsfrigivelse for malen, blir alle andre felt på siden tilgjengelige. På samme måte kan du ikke definere noen forsyningskilder. Dette skjer fordi direkteoverføringen som bruker funksjonen for automatisk frigivelse av forsendelse, bare støtter produksjonsordrer som forsyningskilder, og den krever at det finnes en merking mellom salgsordrer og produksjonsordrer. Hvis du velger **Før forsyningsmottak** som policy for behovsfrigivelse, er feltene i fanene **Planlegging** og **Forsyningskilder** tilgjengelige og kan redigeres.

#### <a name="work-classes"></a>Arbeidsklasser

1. Gå til **Lagerstyring** \> **Oppsett** \> **Arbeid** \> **Arbeidsklasser**.
2. Velg **Ny**.
3. I feltet **Arbeidsklasse-ID** skriver du inn et navn, for eksempel **Direkteoverføring**.
4. Velg **Direkteoverføring** i feltet **Arbeidsordretype**.

Du kan angi én eller flere gyldige lokasjonstyper for å begrense plasseringstypene der direkteoverførte varer kan plasseres.

#### <a name="work-templates"></a>Arbeidsmaler

1. Gå til **Lagerstyring** \> **Oppsett** \> **Arbeid** \> **Arbeidsmaler**.
2. Velg **Direkteoverføring** i feltet **Arbeidsordretype**.
3. Velg **Ny**.
4. Angi **1** i feltet **Serienummer**.
5. I feltet **Arbeidsklassemal** skriver du inn et navn, for eksempel **Direkteoverføring\_51**.
6. Velg **Lagre**.
7. I delen **Arbeidsmaldetaljer** velger du **Ny**.
8. For den nye linjen velger du **Plukk** i feltet **Arbeidstype**. I feltet **Arbeidsklasse-ID** velger du **Direkteoverføring**.
9. Velg **Ny**.
10. For den nye linjen velger du **Plasser** i feltet **Arbeidstype**. I feltet **Arbeidsklasse-ID** velger du **Direkteoverføring**.

#### <a name="location-directives"></a>Lokasjonsdirektiver

En standard plasseringsprosess for ferdigvarer krever et **Plasser**-direktiv for plassering for å styre flyttingen av plukkede produksjonsantall til en vanlig lagringsplass. På samme måte må du definere et **Plasser**-sted for direkteoverføring for å instruere arbeidet med å plassere det ferdige antallet på en bestemt utgående lokasjon som betjener forsendelsen av den tilknyttede salgsordren.

For direkteoverføring, som for vanlig plassering av ferdigvarer, trenger du ikke å opprette et lokasjonsdirektiv for plukkarbeidshandlingen, fordi utleveringslokasjonen er angitt. I tillegg forventes det at denne utleveringslokasjonen defineres enten som standard utleveringssted for en av de ressursrelaterte postene (det vil si ressursen, ressursgrupperelasjonen eller ressursgruppen) eller som en standardlokasjon for ferdigvarer for et lager.

1. Gå til **Lagerstyring** \> **Oppsett** \> **Lokasjonsdirektiver**.
2. Velg **Direkteoverføring** i feltet **Arbeidsordretype**.
3. Velg **Ny**.
4. Angi **1** i feltet **Serienummer**.
5. I feltet **Navn** angir du navnet, for eksempel **Rampedør**.
6. Velg **Plasser** i **Arbeidstype**-feltet.
7. I **Område**-feltet velger du **5**.
8. I **Lager**-feltet velger du **51**.
9. Velg **Ny** i hurtigfanen **Linjer**.
10. I feltet **Til antall** angir du maksimumsantallet for området, for eksempel **1000000**.
11. Velg **Lagre**.
12. I **lokasjonsdirektivhandlinger** velger du **Ny**.
13. I feltet **Navn** angir du navnet, for eksempel **Rampedør**.
14. Velg **Lagre**.
15. Du kan bruke standardspørringsfunksjonen til å begrense plasseringslokasjoner til én eller flere bestemte lokasjoner. Velg **Rediger spørring**, og velg **51** som kriterium for feltet **Lager** i tabellen **Lokasjoner**.

### <a name="cross-dock-finished-goods-to-the-outbound-location"></a>Direkteoverføre ferdigvarer til den utgående lokasjonen

Hvis du vil direkteoverføre antallet ferdigvarer til den utgående lokasjonen for den tilknyttede salgsordren, følger du disse trinnene.

1. Gå til **Salg og markedsføring** \> **Salgsordrer** \> **Alle salgsordrer**.
2. Velg **Ny**.
3. For salgsordrehodet velger du kundekonto **US-001** og et lager som er definert for direkteoverføring som bruker funksjonen for automatisk frigivelse av forsendelse.
4. Legg til en linje for et ferdig produkt, og angi **10** som antallet.
5. I delen **Salgsordrelinjer** velger du **Produkt og forsyning** \> **Produksjonsordre**.
6. I dialogboksen **Opprettelse av produksjonsordre** ser du på standardverdiene, og deretter velger du **Opprett**. En ny produksjonsordre opprettes og kobles til salgsordren (det vil si at den er reservert og merket).
7. Valgfritt: Endre verdien i feltet **Antall** slik at den blir mer enn verdien som kreves for å oppfylle salgsordren. Når produksjonsantallet rapporteres som ferdig, vil systemet opprette direkteoverføringarbeid for det merkede antallet og plasseringsarbeidet for det gjenværende antallet i henhold til den vanlige prosedyren for håndtering av plassering av ferdigvarer.

    Som ble nevnt tidligere må det finnes en markering mellom salgsordren og produksjonsordren. Hvis ikke vil direkteoverføring ikke fungere. En merking kan opprettes på flere måter:

    - Systemet kan automatisk opprette merkingen i følgende situasjoner:

        - Produksjonsordren opprettes manuelt direkte fra salgsordrelinjen (se trinn 6).
        - Planlagte produksjonsordrer autoriseres, og feltet **Oppdater merking** er satt til **Standard**.

    - Brukeren kan opprette merkingen manuelt ved å åpne siden **Merking** fra behovsordrelinjen.

    > [!NOTE]
    > En merking kan ikke opprettes manuelt for varer som er konfigurert til å bruke standard og avveid gjennomsnitt som lagermodeller.

8. På siden **Produksjonsordre**, i handlingsruten i fanen **Produksjonsordre** i gruppen **Prosess**, velger du **Estimat**, og deretter velger du **OK**. Ordren er estimert, og råvareantallet er reservert for produksjonen.
9. I handlingsruten i fanen **Produksjonsordre** i gruppen **Prosess** velger du **Frigi**, og deretter velger du **OK**. Lagerplukkarbeid opprettes for råvarene.
10. Åpne og se gjennom arbeidet. Velg **Arbeidsdetaljer** i gruppen **Generelt** i fanen **Lager** i handlingsruten. Noter arbeids-ID-en.
11. Logg på mobilappen Lagerstyring for å kjøre arbeid i lager 51.
12. Gå til **Produksjon** \> **Produksjonsplukking**.
13. Angi arbeids-IDen for å starte og fullføre råvareplukkingen. 

    Når arbeidet er rapportert som ferdig, er antallet råvarer tilgjengelig på produksjonsinnleveringsstedet (**005** i USMF-demonstrasjonsdataene), og utføringen av produksjonsordren kan starte.

14. På siden **Produksjonsordre**, i handlingsruten i fanen **Produksjonsordre** i gruppen **Prosess**, velger du **Start**, og deretter velger du **OK**.
15. I appen går du til **Produksjon** \> **Ferdigmeld og plasser**.
16. Angi produksjonsordrenummeret og andre obligatoriske detaljer i **Produkt-ID**-feltet, og velg deretter **OK**.

Merk at følgende hendelser oppstår:

- Frigivelsen til et lager utløses for den koblede salgsordren.
- Det opprettes en forsendelse og direkteoverføring basert på frigivelsen. Dette arbeidet instruerer lageroperatøren til å plukke antallene som kreves for å oppfylle salgsordrelinjen og plassere dem på den utgående lokasjonen som er angitt i direktivet for direkteoverføringslokasjonen.
- Hvis produksjonsordreantallet er større enn antallet som kreves av salgsordren, opprettes vanlig plasseringsarbeid. Dette arbeidet instruerer lageroperatøren om å plukke antallet ferdigvarer som gjenstår etter direkteoverføring, og flytte det til vanlig lagring i henhold til lokasjonsdirektivet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
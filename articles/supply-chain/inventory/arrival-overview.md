---
title: Ankomstoversikt
description: Dette emnet gir informasjon om Ankomstoversikt-funksjonen. Ankomstoversikt-siden er en del av denne funksjonen og gir en oversikt over alle varene som forventes å ankomme som innkommende varer.
author: perlynne
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverview, WMSArrivalOverviewProfile, WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 734fbdd6f62c192580029a24844fff78fda8b919
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809596"
---
# <a name="arrival-overview"></a>Ankomstoversikt

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om Ankomstoversikt-funksjonen. Ankomstoversikt-siden er en del av denne funksjonen og gir en oversikt over alle varene som forventes å ankomme som innkommende varer.

**Ankomstoversikt**-siden gir en oversikt over alle forventede innkommende varer. Den viser også ankomster som kan initialiseres basert på oversikten. Dette emnet beskriver mottaksprosessen.

## <a name="business-scenario"></a>Foretningsscenario
Tenk deg følgende scenario i de innkommende prosessene.

[![Foretningsscenario](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png)

Sammy, en mottaksassistent, ønsker å vite hva som skal mottas på den gjeldende dagen. På **Ankomstoversikt**-siden kan Sammy få en oversikt over gjeldende oppgaver, og et grovt estimat av antall, volum, vekt, forskjellige ordretyper og så videre. Senere kommer en levering til ett av innleveringsportene, og Sammy mottar en liste over leveringen. På siden **Ankomstoversikt** kan Sammy utføre følgende oppgaver:

-   Identifisere den samsvarende mottaksordren og registrere mottaket som **pågår**. Linjene som kreves for en registrering, genereres automatisk og mottaket kan overvåkes, selv om transaksjonene ennå ikke er postert som **registrerte**.
-   Få tilgang til den riktige ankomstjournalreferansen (det vil si **Vareankomst**-journalen eller **Produksjonsinnlevering**-journalen), og identifiserer journaler som er klare for en oppdatering av mottaksseddel.

## <a name="arrival-overview-page"></a>Siden Ankomstoversikt
Du åpner siden **Ankomstoversikt** ved å klikke på **Lagerstyring** &gt; **Innkommende ordrer** &gt; **Ankomstoversikt**. Du kan vise en liste over bestillinger som skal mottas. Oversikten er delt inn i et hode og linjer. Informasjonen i hodet er gruppert etter ordretype, forventet mottaksdato og mottaksadresse. Når en overskriftslinje er valgt for vareankomst, merkes alle detaljlinjene som er knyttet til mottaksreferansen, for ankomst i linjedetaljdelen på siden. Når alle de tilknyttede journallinjene er postert, vises ikke denne informasjonen.

### <a name="arrival-overview-profiles"></a>Profiler for ankomstoversikt

Siden **Ankomstoversikt** gir en oversikt over varene som forventes å ankomme og datoen da de er forventet å ankomme. Flere sett med personlige innstillinger kan brukes som en del av ankomstprosessen. Individuelle brukere kan definere sine egne innstillinger på siden **Profiler for ankomstoversikt**.

### <a name="set-up-item-arrival"></a>Definer vareankomst

I vårt eksempel vil Sammy sette opp en ny datamaskin på en lokasjon som skal brukes til å motta ferdigvarer som leveres fra produksjon på område 1. På siden **Profiler for ankomstoversikt** oppretter Sammy et nytt oppsett som heter **Område 1 – produksjon** og angir følgende innstillinger.

1.  I hurtigfanen **Ankomstalternativer** i feltgruppen **Område** angir du informasjon om et dagsintervall og lagrene som skal tas med i oversikten.
2.  I hurtigfanen **Ankomstsalternativer** i feltgruppen **Journal** angir du et mottakende lager, en plassering og et journalnavn (vareankomst/produksjonsinnlevering).
3.  I hurtigfanen **Detaljer om spørring etter ankomst** i **Område**-feltgruppen, i feltet **Begrens til område**, angir du et område for å begrense visningen i oversiktsområdet.
4.  I hurtigfanen **Detaljer om spørring etter ankomst** i feltgruppen **Transaksjonstyper som vises** angir du alternativet **Produksjonsordrer** til **Ja**.
5.  I hurtigfanen **Detaljer om spørring etter ankomst** i **Diverse**-gruppen setter du alternativet **Oppdater ved oppstart** til **Ja** hvis visningen skal oppdateres automatisk ved oppstart. Angi alternativet **Oppdater ved områdeendring** til **Ja** hvis visningen skal oppdateres automatisk når verdier endres.

For dette eksemplet er feltet **Profilnavn for ankomstoversikt** i hurtigfanen **Ankomstoversikt** på siden **Ankomstoversikt** satt til **Område 1 – produksjon**.

### <a name="prerequisites-for-arrival-journals"></a>Forutsetninger for ankomstjournaler

For automatisk å opprette ankomstjournaler fra **Ankomstoversikt**-siden må du definere riktig informasjon i **Journal**-feltgruppen i hurtigfanen **Ankomstalternativer**.

-   Du må angi et journalnavn når du oppretter en journal.

[![Angi et journalnavn](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)

-   Hvis du angir verdier i feltene **Lager** og **Plassering**, brukes disse verdiene i journallinjene. Hvis du ikke angir verdier, bruker systemet verdiene fra dimensjonen som er angitt i lagertransaksjonene.

#### <a name="items-that-are-received-from-one-expected-receipt-order"></a>Varer som mottas fra én forventet mottaksordre

På **Mottak**-hurtigfanen velger Sammy en linje og klikker deretter **Start ankomst**. Alle relaterte linjer i det angitte området som har et antall å registrere, velges automatisk. Det genereres en vareankomstjournal som har et samsvar mellom den forventede mottaksordren og journalen. Antallet initialiseres automatisk på alle linjene som opprettes.

#### <a name="items-that-are-received-from-more-than-one-expected-receipt-order"></a>Varer som mottas fra mer enn én forventet mottaksordre

På **Mottak**-hurtigfanen velger Sammy flere linjer og klikker deretter **Start ankomst**. Det genereres en vareankomstjournal som har et samsvar mellom alle de forventede mottaksordrene og journalen. Alle linjer opprettes på ett hode for vareankomstjournal, og antallet initialiseres automatisk.

### <a name="receive-items-from-one-or-more-expected-receipt-orders"></a>Fjerne varer fra én eller flere forventede mottaksordrer

#### <a name="view-information"></a>Vis informasjon

For å få en oversikt over forventede mottak i et datointervall, angir Sammy følgende informasjon i feltene på hurtigfanen **Ankomstalternativer** på siden **Ankomstoversikt**, og klikker deretter **Oppdater** for å oppdatere visningen:

-   Profilnavn for ankomstoversikt: **Forespørsel**
-   Vis linjer: **Alle**
-   Dager bakover: (tom)
-   Dager fremover: **0**
-   Lagre: **HL, ML**

Sammy kan vise følgende informasjon:

-   Alle relaterte mottaksordrer for systemdatoen og et ubegrenset antall dager fra den (**InventTrans.StatusDate**-intervallet), og mottak til lagre HL og ML, uansett status.
-   Detaljert linjeinformasjon for mer enn én ordre. Sammy kan velge flere hodelinjer i oversikten og deretter klikke **Vis alle valgte** for å vise all tilsvarende linjedetaljinformasjon for alle valgte ordrer.
-   Informasjon om en bestemt bestilling. Hvis Sammy bare vil vise informasjon som er knyttet til et bestemt referansenummer i oversikten, kan han angi et kontonummer i **Kontonummer**-feltet og et ordrenummer i **Referansenummer**-feltet.
-   En oversikt over registreringsoppgavene som forfaller for alle ordrelinjene som en vareankomstjournal er opprettet for, men som ennå ikke er postert. For å vise denne informasjonen kan Sammy velge **pågår** i **Vis linjer**-feltet.

### <a name="update-journals"></a>Oppdatere journaler

For å registrere én eller flere ordrelinjer som forfaller for behandling, kan Sammy velge linjene i oversiktsrutenettet eller i rutenettet, og deretter klikke **Journaler** &gt; **Vis ankomster fra mottak**. Hodene for vareankomst som tilsvarer linjene, vises. For å oppdatere de registrerte varene i bestillingen kan Sammy få tilgang til journalhodene for vareankomst som er klare for oppdatering. For å få tilgang til disse journalhodene for vareankomst klikker han **Journaler** &gt; **Journaler klare for mottaksseddel**. Alle topptekstlinjene som er klare for oppdatering av mottaksseddel i det angitte lageret, vises. (Topptekstlinjene som vises, er ikke knyttet til dagsintervallet).

### <a name="start-an-arrival-registration"></a>Starte en ankomstregistrering

Ved å velge flere linjer på **Ankomstoversikt**-siden kan Sammy starte en ankomst av mer enn én mottaksreferanse. Når han velger en linje fra mottaksoversikten, velges de tilsvarende linjedetaljene. Hvis det finnes et antall for registrering, er knappen **Start ankomst** tilgjengelig. Sammy kan bruke to metoder for å starte ankomstregistreringen:

-   For å filtrere siden slik at den bare viser poster som oppfyller bestemte vilkår, kan han i feltet **Leverandørreferanse** skanne et referansenummer fra en leverandør, for eksempel strekkoden for en følgeseddel.
-   I oversiktsdelen eller detaljdelen på siden **Ankomstoversikt** kan han manuelt merke eller oppheve merkingen av poster for ankomstregistrering. Deretter, når Sammy klikker **Start ankomst**, opprettes automatisk de valgte postene i en vareankomstjournal. Postene inkluderer linjeinformasjon, og all unik feltinformasjon er tilordnet.

## <a name="update-arrival-information-and-process-a-product-receipt"></a>Oppdatere ankomstinformasjon og behandle en mottaksseddel
Når alle varene er registrert, kan lagersjefen eller innkjøpssjefen oppdatere de mottatte varene med en produktkvittering for å legge til den fysiske kostnaden. Bruk følgende fremgangsmåte for å oppdatere ankomstinformasjonen og postere en produktkvittering.

1.  Klikk på **Lagerstyring** &gt; **Innkommende ordrer** &gt; **Ankomstoversikt**.
2.  På siden **Ankomstoversikt** klikker du **Journaler** &gt; **Journaler klare for mottaksseddel** for å vise en liste over journalene som er klare for oppdatering av produktkvittering.
3.  Velg journalene som må oppdateres, og klikk deretter **Funksjoner** &gt; **Produktkvittering**.
4.  På **Postering**-siden angir du produktkvitteringsnummeret, hvis det ikke allerede er tilgjengelig i journalen, og klikker deretter **OK** for å behandle produktkvitteringen.

## <a name="summary"></a>Sammendrag
**Ankomstoversikt**-siden kan hjelpe lagersjefen og lagermedarbeidere med å få en oversikt over forventet arbeid som må utføres som en del av en innkommende prosess. Siden kan også brukes til å starte vareankomstprosessen, for å garantere at varer spores på den første posten på lageret.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
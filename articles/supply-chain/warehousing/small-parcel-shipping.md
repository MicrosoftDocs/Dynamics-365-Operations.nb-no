---
title: Forsendelse av småpakker
description: Denne artikkelen inneholder informasjon om funksjonen for forsendelse av småpakker. Denne funksjonen gjør at Microsoft Dynamics 365 Supply Chain Management kan sende informasjon om en pakket container til transportøren, og deretter motta en forsendelsesetikett, en forsendelsessats og et sporingsnummer tilbake fra denne transportøren.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 6ccc9c795e2da121acf9c0809aef99a5f9d5889e
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219726"
---
# <a name="small-parcel-shipping"></a>Forsendelse av småpakker

[!include [banner](../../includes/banner.md)]

Med funksjonen for forsendelse av småpakker kan Microsoft Dynamics 365 Supply Chain Management kommunisere direkte med transportører ved å sørge for et rammeverk for kommunikasjon via transportør-API-er. Denne funksjonaliteten er nyttig når du sender individuelle salgsordrer via kommersielle transportører i stedet for å bruke containerforsendelse eller LTL-forsendelse (Less-than-truckload).

Funksjonen for forsendelse av småpakker kommuniserer med transportøren via en egen *ratemotor*. Organisasjonen må utvikle denne ratemotoren i samarbeid med transportørtjenesten. Ratemotoren gjør at Supply Chain Management kan sende informasjon om en pakket container til transportøren, og deretter motta en forsendelsesetikett, en forsendelsessats og et sporingsnummer tilbake fra denne transportøren.

Forsendelsessatsen som returneres, legges til i den tilknyttede salgsordren som et tillegg. Forsendelsesetiketten som returneres, kan deretter skrives ut automatisk ved hjelp av en ZPL-skriver (Zebra Programming Language) og brukes på forsendelsen. Transportøren skanner denne forsendelsesetiketten når vedkommende henter pakkene på lageret.

## <a name="prepare-your-system-to-support-sps"></a>Klargjøre systemet slik at det støtter forsendelse av småpakker

Før du kan begynne å bruke funksjonen for forsendelse av småpakker, må du aktivere den i Funksjonsbehandling, legge til ratemotoren og definere modulene **Transportstyring** og **Lagerstyring** for å støtte den.

### <a name="turn-on-the-sps-feature"></a>Aktivere funksjonen for forsendelse av småpakker

Før du kan bruke funksjonen for forsendelse av småpakker, må den være aktivert i systemet. Administratorer kan bruke arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere statusen for funksjonen og aktivere den om nødvendig. Funksjonen vises på følgende måte:

- **Modul:** *Transportstyring*
- **Funksjonsnavn:** *Forsendelse av småpakker*

### <a name="deploy-and-set-up-rate-engines"></a>Distribuere og definere ratemotorer

Supply Chain Management inneholder ingen ratemotorer. Du må skaffe eller opprette alle ratemotorer du trenger, og deretter legge dem til i systemet. Microsoft tilbyr imidlertid en demoratemotor du kan bruke til testing.

#### <a name="download-and-deploy-the-demo-rate-engine"></a>Laste ned og distribuere demoratemotoren

Følg denne fremgangsmåten for å hente demoratemotoren.

1. Last ned [biblioteket for dynamiske koblinger (DLL) for demoratemotoren](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS) på GitHub.
1. På Supply Chain Management-serveren lagrer du DLL-filen i mappen **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.

#### <a name="create-and-deploy-functional-rate-engines"></a>Opprette og distribuere praktiske ratemotorer

Hvis du vil ha informasjon om hvordan du oppretter og distribuerer praktiske ratemotorer slik at de kan brukes i et produksjons- eller testmiljø, kan du se følgende artikler:

- [Opprette en ny transportstyringsmotor](../transportation/create-new-transportation-management-engine.md)
- [Definere transportbehandlingsmotorer](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

Hvis du vil ha mer informasjon om hvordan du oppretter en ratemotor for forsendelse av småpakker, kan du se følgende blogginnlegg: [Forsendelse av småpakker: utnytte funksjonen for forsendelse av småpakker i Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a>Definere en ratemotor i Supply Chain Management

Etter at du har opprettet og distribuert en ratemotor for forsendelse av småpakker, følger du fremgangsmåten nedenfor for å definere den.

1. Gå til **Transportstyring \> Oppsett \> Motorer \> Ratemotor**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.
1. I den nye raden angir du følgende felter:

    - **Ratemotor** – Angi et unikt navn for ratemotoren. Hvis du bruker demoratemotoren, angir du *Demoratemotor*.
    - **Navn** – Angi en kort beskrivelse av ratemotoren. Hvis du bruker demoratemotoren, angir du *Demoratemotor*.
    - **ID for metadata for vurdering** – Velg grunnlaget som skal brukes til å beregne satsen. Satsen kan for eksempel beregnes basert på avstand. Hvis du bruker demoratemotoren, kan du la dette feltet stå tomt.
    - **Motormontering** – Angi filnavnet på DLL-pakken du distribuerte. Hvis du bruker demoratemotoren, angir du *TMSSmallParcelShippingEngine.dll*.
    - **Motorklasse** – Angi klassenavnet som ble opprettet for ratemotoren. Hvis du bruker demoratemotoren, angir du *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.

## <a name="example-scenario"></a>Eksempelscenario

Dette eksempelscenarioet viser hvordan du definerer og bruker forsendelse av småpakker etter at du har klargjort systemet som beskrevet tidligere i denne artikkelen. Dette scenarioet bruker den tidligere nevnte demoratemotoren.

### <a name="make-demo-data-available"></a>Gjøre demodata tilgjengelig

For å kunne arbeide deg gjennom dette scenariet ved å bruke de angitte demopostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

### <a name="set-up-the-scenario"></a>Definer scenariet

I dette eksempelscenarioet må du ha en demotransportør, transportørgruppe, pakkepolicy og pakkeprofil. De følgende underdelene forklarer hvordan du klargjør postene som kreves for scenarioet. I et produksjonsscenario ligner fremgangsmåten for konfigurasjon vanligvis på fremgangsmåten som er beskrevet her. Du angir imidlertid andre verdier.

#### <a name="set-up-carriers"></a>Definere transportører

Følg denne fremgangsmåten for å definere en transportør.

1. Gå til **Transportstyring \> Oppsett \> Transpotører \> Transportører**.
1. I handlingsruten velger du **Ny** for legge til en transportør.
1. I hodet angir du følgende verdier:

    - **Transportør:** *Demotransportør*
    - **Navn:** *Demotransportør*
    - **Modus:** *Landtransport*

1. Angi følgende verdier i **Oversikt**-hurtigfanen:

    - **Aktiver transportør:** *Ja*
    - **Aktiver transportørrangering:** *Ja*

1. I hurtigfanen **Tjenester** velger du **Ny** for å legge til en tjeneste i rutenettet.
1. Angi følgende verdier for den nye tjenesten:

    - **Transportørtjeneste:** *Demotransportørtjeneste*
    - **Navn:** *Demotransportørtjeneste*
    - **Transportmetode:** *Landtransport*

    Angi vilkårlige verdier i alle de andre feltene etter behov. (Når du lagrer den nye transportørposten, opprettes det en ny leveringsmåte, og **Leveringsmåte**-feltet angis automatisk.)

1. Velg **Ny** i hurtigfanen **Vurderingsprofiler** for å legge til en vurderingsprofil i rutenettet.
1. Angi følgende verdier for den nye profilen:

    - **Vurderingsprofil:** *Demotransportørtjeneste*
    - **Navn:** *Demotransportørtjeneste*
    - **Ratemotor:** *Demoratemotor*

    Angi vilkårlige verdier i alle de andre feltene etter behov.

1. Velg **Lagre** i handlingsruten.

Hvis du vil ha mer informasjon om hvordan du definerer transportører, kan du se [Definere transportører](../transportation/tasks/set-up-shipping-carriers.md).

#### <a name="set-up-carrier-service-accounts"></a>Definere transportørtjenestekontoer

Følg denne fremgangsmåten for å definere en transportørtjenestekonto.

1. Gå til **Transportstyring \> Oppsett \> Vurdering \> Transportørtjenestekonto**.
1. I handlingsruten velger du **Ny** for å legge til en transportørtjenestekonto.
1. Angi følgende verdier for den nye kontoen:

    - **Transportør:** *Demotransportør*
    - **Transportørtjeneste:** *Demotransportørtjeneste*
    - **Kundekontonummer for transportør:** Kundekontonummeret for transportøren som brukes til å bekrefte og autentisere tilkoblingen til transportøren. Transportøren sørger for denne verdien. Hvis du bruker demotjenesten, kan du angi en vilkårlig verdi.
    - **Område:** *6*
    - **Lager:** *62*

    > [!NOTE]
    > Verdien for **Kundekontonummer for transportør** er ofte den eneste verdien som kreves for å autentisere tilkoblingen. Hvis transportøren imidlertid krever flere autentiseringsparametere, bør organisasjonen tilpasse denne siden for å legge til ekstra felter etter behov.

#### <a name="set-up-a-container-packing-policy"></a>Definere en policy for containerpakking

Følg denne fremgangsmåten for å definere en policy for containerpakking.

1. Hvis du ikke allerede har konfigurert en ZPL-skriverdefinisjon, bruker du programmet Dokumentrutingsagent til å konfigurere den. Hvis du vil ha mer informasjon, kan du se [Oversikt over utskrift av dokument](../../fin-ops-core/dev-itpro/analytics/print-documents.md) og beslektede artikler.
1. Gå til **Lagerstyring \> Oppsett \> Containere \> Policyer for containerpakking**.
1. I handlingsruten velger du **Ny** for å legge til en policy for containerpakking.
1. I toppteksten i den nye policyen angir du følgende verdier:

    - **Policy for containerpakke:** *Demopakkepolicy*
    - **Beskrivelse:** en beskrivelse av policyen

1. Angi følgende verdier i **Oversikt**-hurtigfanen:

    - **Lager:** *62*
    - **Standardlokasjon for endelig forsendelse:** *Rampedør*
    - **Vektenhet:** *kg*
    - **Policy for containerlukking:** *Automatisk frigivelse*
    - **Policy for containerfrigivelse:** *Gjør tilgjengelig på endelig leveringslokasjon*

1. I hurtigfanen **Containermanifest** angir du følgende verdier:

    - **Automatisk manifest ved containerlukking:** *Ja*
    - **Manifestkrav for container:** *Transportstyring*
    - **Skriv ut containerinnhold:** *Nei*

1. I hurtigfanen **Utskrift av transportøretikett** angir du følgende verdier:

    - **Skriv ut containerforsendelsesetikett:** *Alltid*
    - **Skrivernavn:** Navnet på ZPL-skriveren som skal skrive ut forsendelsesetiketter

#### <a name="set-up-a-packing-profile"></a>Definere en pakkeprofil

Følg denne fremgangsmåten for å definere en pakkeprofil.

1. Gå til **Lagerstyring \> Oppsett \> Pakking \> Pakkeprofiler**.
1. I handlingsruten velger du **Ny** for å legge til en pakkeprofil i rutenettet.
1. Angi følgende verdier for den nye profilen:

    - **Pakkeprofil-ID:** *Demopakkeprofil*
    - **Beskrivelse:** en beskrivelse av profilen
    - **Policy for containerpakke:** *Demopakkepolicy*
    - **Modus for container-ID:** *Automatisk*
    - **Containertype:** *SmallBox*

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a>Definere en kunde som kan bruke transportøren for forsendelse av småpakker

Følg denne fremgangsmåten for å definere en kunde, slik at vedkommende kan bruke transportøren du har opprettet.

1. Gå til **Kunder \> kunder \> Alle kunder**.
1. Finn og velg kunden *US-027* i rutenettet.
1. Gå til handlingsruten, **Generelt**-fanen, **Oppsett**-gruppen, og velg **Kundekontoer for transportør**.
1. Velg **Ny** i handlingsruten på siden **Kundekontoer for transportør** for å legge til en konto i rutenettet.
1. Angi følgende verdier for den nye kontoen:

    - **Transportør:** *Demotransportør*
    - **Kundekontonummer for transportør:** *12345* (Verdien er ikke viktig i dette scenarioet, men vi henviser til den i neste del.)

### <a name="go-through-the-example-scenario"></a>Gå gjennom eksempelscenarioet

Når du har definert alle eksempeldataene som beskrevet i forrige del, er du klar til å gå gjennom eksempelscenarioet.

#### <a name="create-a-sales-order-and-process-the-work"></a>Opprette en salgsordre og behandle arbeidet

Følg denne fremgangsmåten for å opprette en salgsordre.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** for å opprette en salgsordre.
1. I dialogboksen **Opprett salgsordre** angir du *US-027* i **Kundekonto**-feltet.
1. Velg **OK** for å opprette salgsorden og lukke dialogboksen.
1. Den nye salgsordren åpnes. I hurtigfanen **Salgsordrehode** angir du verdien du valgte for denne kunden tidligere (*12345*), i feltet **Kundekontonummer for transportør**.
1. Legg til en salgslinje i delen **Salgsordrelinjer**, og angi følgende verdier for den:

    - **Varenummer:** *A0002*
    - **Antall:** *1*
    - **Område:** *6*
    - **Lager:** *62*

1. Bytt til **Topptekst**-visningen.
1. Angi følgende verdier i hurtigfanen **Levering**:

    - **Transportør:** *Demotransportør*
    - **Transportørtjeneste:** *Demotransportørtjeneste*

1. Gå tilbake til **Linjer**-visningen. Hvis du blir bedt om å oppdatere leveringsmåten for salgslinjene, velger du **Ja**.
1. Velg ordrelinjen du definerte tidligere, i delen **Salgsordrelinjer**, og velg deretter **Lager \> Reservasjon**.
1. På **Reservasjon**-siden velger du **Reserver parti** for å reservere den valgte linjens fulle antall i lageret.
1. Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.
1. Velg **Frigi til lager** i fanen **Lager** i handlingsruten.

    Det opprettes arbeid for å flytte varer fra plukklokasjonen til pakkestasjonen.

1. I delen **Salgsordrelinje** velger du **Lager \> Forsendelsesdetaljer**.
1. Noter deg forsendelses-ID-en på siden **Forsendelsesdetaljer**. Du trenger denne når du pakker forsendelsen ved pakkestasjonen.
1. Lukk siden **Forsendelsesdetaljer** for å gå tilbake til salgsordren.
1. Noter deg salgsordrenummeret, og gå deretter til **Lagerstyring \> Arbeid \> Alt arbeid**.
1. Bruk salgsordrenummeret til å finne og velge arbeidet som ble opprettet for ordren.
1. Velg **Fullfør arbeid** i **Arbeid**-fanen i handlingsruten.
1. Velg en bruker-ID i **Bruker-ID**-feltet på siden **Arbeidsfullføring**. Velg deretter **Valider arbeid** i handlingsruten.
1. Hvis arbeidet består valideringen, velger du **Fullfør arbeid** i handlingsruten.

    Arbeidet merkes som fullført for å simulere flyttingen av varer til pakkestasjonen.

#### <a name="pack-the-shipment"></a>Pakke forsendelsen

Følg denne fremgangsmåten for å pakke forsendelsen.

1. Gå til **Lagerstyring \> Oppsett \> Arbeider**, og kontroller at brukerkontoen din er knyttet til en arbeiderkonto for lagerstyring.
1. Gå til **Lagerstyring \> Plukking og containerbruk \> Pakke**.
1. I dialogboksen **Velg pakkstasjon** angir du følgende verdier:

    - **Område:** *6*
    - **Lager:** *62*
    - **Plassering:** *Pakke*
    - **Pakkeprofil-ID:** *Demopakkeprofil*

1. Velg **OK**.
1. **Pakke**-siden vises. I et produksjonsscenario skanner en arbeider et nummerskilt eller en forsendelses-ID. I dette scenariet åpner du i stedet siden **Alle forsendelser** og slår opp forsendelsesnummeret for forsendelsen du nettopp opprettet. Deretter angir du denne verdien i feltet **Nummerskilt eller forsendelse** på **Pakke**-siden. Du kan også angi forsendelses-ID-en du noterte tidligere.
1. I handlingsruten velger du **Ny container**.
1. Dialogboksen som vises, inneholder detaljer om den nye containeren. La standardverdiene stå, og velg deretter **OK**.
1. Gå til **Pakke**-siden og deretter hurtigfanen **Varepakking**, og velg *A0002* i **Identifikator**-feltet for å pakke denne varen. Varen legges til i containeren.
1. Velg **Containere til forsendelse** i handlingsruten.

    Siden **Containere til forsendelse** som vises, har en rad for containeren du nettopp opprettet. Feltet **ID for containermanifest** i denne raden er imidlertid tomt fordi du ennå ikke har mottatt forsendelsesetiketten og sporingsnummeret fra transportøren.

1. I handlingsruten velger du **Lukk container**.
1. I dialogboksen **Lukk container** angir du *1 kg* i **Bruttovekt**-feltet og velger deretter **OK**.

    Forsendelsesetiketten skal nå skrives ut på ZPL-skriveren du valgte tidligere. Den skal ligne følgende eksempel.

    ![Eksempel på forsendelsesetikett.](media/sps-label-example.png "Eksempel på forsendelsesetikett")

1. Legg merke til at verdiene for **ID for containermanifest** og **Total frakt** er lagt til som mottatt fra transportøren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
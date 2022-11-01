---
title: Konfigurere Regulatory Configuration Service (RCS)
description: Denne artikkelen forklarer hvordan du konfigurerer Regulatory Configuration Service (RCS).
author: gionoder
ms.date: 10/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 32ced98925ee66e02f0b073b4acbd586666ac20c
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710788"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>Konfigurere Regulatory Configuration Service (RCS)

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du konfigurerer Regulatory Configuration Service (RCS).

## <a name="turn-on-globalization-features"></a>Aktivere globaliseringsfunksjoner

1. Logg på RCS-kontoen.
2. Velg flisen **Funksjonsbehandling**.
3. I **Funksjonsbehandling**-arbeidsområdet velger du **Globaliseringsfunksjoner** i listen, og deretter velger du **Aktiver nå**.

Det skal nå vises en flis for arbeidsområdet **Globaliseringsfunksjoner** på hovedinstrumentbordet for RCS.

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Konfigurere parametere for RCS-integrasjon med elektronisk fakturering

1. I arbeidsområdet **Globaliseringsfunksjoner** i delen **Relaterte innstillinger** velger du koblingen **Parametere for elektronisk rapportering**.
2. Første gang du definerer parameterne, blir du bedt om å koble til Life Cycle Services (LCS). Velg **Klikk her for å koble til Lifecycle Services**, og etter at tilkoblingen er fastsatt, velger du **OK**.

    > [!IMPORTANT]
    > I land eller områder der dataresidens fremtvinges, og hvis RCS ble klargjort i et annet område der LCS er klargjort, kan du få følgende tilkoblingsfeilmelding i RCS: Ingen HTTP-ressurs ble funnet som samsvarer med forespørsels-URIen. Velg **OK**. Du kan få en feilmelding i RCS: Kan ikke generere brukertokenet for Dynamics Lifecycle Services på vegne av brukeren. Kontakt systemansvarlig.
    >  
    > Dette skjer fordi LCS er en global tjeneste, og klargjøres i et amerikansk område. På grunn av personvernpolicyen kan ikke RCS fra gjeldende område koble seg til LCS. Under disse omstendighetene finnes det 2 mulige løsninger:
    > - Slett RCS fra gjeldende område, og opprett det på nytt i amerikansk område.
    > - Ignorer feilene og fortsett med oppsettet for elektronisk fakturering. Disse feilene påvirker ikke funksjonaliteten for elektronisk fakturering.

3. I feltet **URI for endepunkt for tjeneste** i fanen **Elektronisk fakturering** angir du riktig endepunkt for tjeneste for Microsoft Azure-geografien, som vist i følgende tabell.

    | Datasenter Azure-geografi | URI for tjenestesluttpunkt |
    |----------------------------|----------------------|
    | USA              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Europa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Storbritannia             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Asia                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Japan                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Sveits                | <p>`https://gw.ch-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Brasil                     | <p>`https://gw.br-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.br-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | De forente arabiske emirater       | <p>`https://gw.ae-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Australia                  | <p>`https://gw.au-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.au-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Canada                     | <p>`https://gw.ca-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.ca-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Frankrike                     | <p>`https://gw.fr-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | India                      | <p>`https://gw.in-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Norge                     | <p>`https://gw.no-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Sør-Afrika               | <p>`https://gw.za-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Gå gjennom og angi den faste verdien i **Program-ID**-feltet **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Kontroller at det bare er angitt en globalt unik identifikator (GUID), og at verdien ikke har noen andre symboler, for eksempel mellomrom, kommaer, punktum eller anførselstegn.
4. I feltet **ID for LCS-miljø** angir du ID-en for Microsoft Dynamics Lifecycle Services-miljøet (LCS). Denne verdien er referansen til Finance- eller Supply Chain Management-miljøet som du skal bruke med tjenesten for elektronisk fakturering. Du kan hente ID-en ved å logge deg på [LCS](https://lcs.dynamics.com/), åpne prosjektet og deretter se i feltet **Miljø-ID** i **Miljødetaljer**-delen i fanen **Administrer miljø**.

    > [!IMPORTANT]
    > Hvis tilleggsprogrammet for elektronisk fakturering er installert i flere Finance- eller Supply Chain Management-miljøer i LCS, må du alltid bruke miljø-ID-en for det sist installerte miljøet. Hvis du beslutter å installere tilleggsprogrammet i et nytt miljø, oppdaterer du feltet **ID for LCS-miljø** i RCS til den nyeste verdien etter at du har konfigurert og arbeidet med funksjonaliteten for elektronisk fakturering.

5. Velg **Lagre**, og lukk deretter siden.

## <a name="configuration-providers"></a>Konfigurasjonsleverandører

Du kan bruke konfigurasjonsleverandører til å skille mellom eierne av konfigurasjoner for elektronisk rapportering (ER) som brukes i elektroniske faktureringsprosesser og eierne av globaliseringsfunksjoner. **Microsoft** (`http://microsoft.com`) er angitt for konfigurasjonsleverandøren for alle globaliseringsfunksjoner som kommer fra Microsoft og er publisert i det globale repositoriet.

Du kan bare justere ER-konfigurasjoner og globaliseringsfunksjoner som tilhører den aktive konfigurasjonsleverandøren. Du kan bruke disse konfigurasjonene og funksjonene som maler til å opprette konfigurasjoner og funksjoner som tilhører den aktive konfigurasjonsleverandøren, slik at du kan justere dem.

Opprett først konfigurasjonsleverandørene. Angi deretter den ene av dem som aktiv. Du kan ikke angi konfigurasjonsleverandøren fra **Microsoft** som aktiv.

### <a name="create-a-configuration-provider"></a>Opprette en konfigurasjonsleverandør

1. I delen **Relaterte koblinger** i arbeidsområdet **Elektronisk rapportering** velger du **Konfigurasjonsleverandører**.
2. Velg **Ny**.
3. I feltet **Navn** angir du et unikt navn på konfigurasjonsleverandøren.
4. Angi den unike nettadressen til konfigurasjonsleverandøren i feltet **Internett-adresse**.
5. Velg **Lagre**, og lukk deretter siden.

### <a name="select-a-configuration-provider-as-active"></a>Velge en konfigurasjonsleverandør som aktiv

1. I listen over konfigurasjonsleverandører velger du konfigurasjonsleverandøren du vil angi som aktiv.
2. Velg **Angi som aktiv**.

## <a name="import-er-configurations-from-the-global-repository"></a>Importer ER-konfigurasjoner fra det globale repositoriet

1. I delen **Relaterte koblinger** i arbeidsområdet **Elektronisk rapportering** velger du **Konfigurasjonsleverandører**.
2. Velg **Microsoft** i listen over konfigurasjonsleverandører, og velg deretter **Repositorier**.
3. Velg **Globalt**, og velg deretter **Åpne** i handlingsruten.
4. Importer følgende ER-modeller:

    - **Kontekstmodell for kundefaktura**
    - **Fakturamodell**
    - **Regnskapsdokumenter** (for brasilianske scenarioer om nødvendig)
    - **Svarmeldingsmodell**

5. Hvis **Fakturamodelltilordning** ikke ble importert automatisk, importerer du den.
6. Lukk siden.

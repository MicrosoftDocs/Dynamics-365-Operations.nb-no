---
title: Støtte for avgiftsfunksjon for overføringsordrer
description: Dette emnet forklarer den nye avgiftsfunksjonsstøtten for overføringsordrer ved å bruke avgiftsberegningstjenesten.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1c47c327841b8c712220e440e2aa6b4fe2b31b4a1ccd03dc0a200dbeb7394071
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721695"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Støtte for avgiftsfunksjon for overføringsordrer

[!include [banner](../../includes/banner.md)]

Dette emnet gir informasjon om beregning av avgift og posteringsintegrering i overføringsordrer. Ved hjelp av denne funksjonaliteten kan du definere avgiftsberegning og -postering i overføringsordrer for lageroverføringer. I henhold til mva-regler i EU anses lageroverføringer som fellesskapsforsyning og fellesskapsanskaffelse.

Hvis du vil konfigurere og bruke denne funksjonaliteten, må du gå gjennom tre hovedtrinn:

1. **RCS-oppsett:** I Regulatory Configuration Service setter du opp avgiftsfunksjonen, avgiftskoder og relevans for avgiftskoder for å bestemme avgiftskoden i overføringsordrer.
2. **Finance-oppsett:** I Microsoft Dynamics 365 Finance aktiverer du funksjonen **Avgift i overføringsordre**, setter opp avgiftstjenesteparametere for beholdningen og setter opp kjerneavgiftsparametere.
3. **Beholdningsoppsett:** Definer beholdningskonfigurasjonen for overføringsordretransaksjoner.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>Konfigurer RCS for avgifts- og overføringsordretransaksjoner

Følg denne fremgangsmåten for å definere avgiften som er involvert i en overføringsordre. I eksemplet som vises her, er overføringsordren fra Nederland til Belgia.

1. På siden **Avgiftsfunksjoner**, på **Versjoner**-fanen velger du utkastfunksjonsversjonen, og deretter velger du **Rediger**.

    ![Valg av Rediger.](../media/tax-feature-support-01.png)

2. På siden **Oppsett av avgiftsfunksjoner**, på fanen **Avgiftskoder**, velger du **Legg til** for å opprette nye avgiftskoder. For dette eksemplet opprettes det tre avgiftskoder: **NL-Exempt**, **BE-RC-21** og **BE-RC+21**.

    - Når en overføringsordre sendes fra et lager i Nederland, brukes koden for mva-fritak i Nederland (**NL-Exempt**).
      
        Opprett mva-koden **NL-Exempt**.
        1. Velg **Legg til**, angi **NL-Exempt** i feltet **Mva-kode**.
        2. Velg **Etter nettobeløp** i feltet **Avgiftskomponent**.
        3. Velg **Lagre**.
        4. Velg **Legg til** i **Sats**-tabellen.
        5. Bytt **Er Fritak** til **Ja** i **Generelt**-delen.

        ![Avgiftskoden NL-Exempt.](../media/tax-feature-support-02.png)

    - Når en overføringsordre mottas ved et lager i Belgia, brukes mekanismen for snudd avregning ved hjelp av avgiftskodene **BE-RC-21** og **BE-RC+21**.
        
        Opprett avgiftskoden **BE-RC-21**.      
        1. Velg **Legg til**, angi **BE-RC-21** i feltet **Mva-kode**.
        2. Velg **Etter nettobeløp** i feltet **Avgiftskomponent**.
        3. Velg **Lagre**.
        4. Velg **Legg til** i **Sats**-tabellen.
        5. Angi **-21** i **Avgiftssats**-feltet.
        6. Bytt **Er Snudd avregning** til **Ja** i **Generelt**-delen.
        7. Velg **Lagre**.

        ![BE-RC-21-avgiftskoden for snudd avregning.](../media/tax-feature-support-03.png)
        
        Opprett avgiftskoden **BE-RC+21**.
        1. Velg **Legg til**, angi **BE-RC-21** i feltet **Mva-kode**.
        2. Velg **Etter nettobeløp** i feltet **Avgiftskomponent**.
        3. Velg **Lagre**.
        4. Velg **Legg til** i **Sats**-tabellen.
        5. Angi **21** i **Avgiftssats**-feltet.
        6. Velg **Lagre**.

        ![BE-RC+21-avgiftskoden for snudd avregning.](../media/tax-feature-support-04.png)

3. Definer relevansen for avgiftskodene.

    1. Velg **Administrer kolonner**, og velg deretter kolonner som skal brukes til å bygge opp relevanstabellen.

        > [!NOTE]
        > Legg til kolonnene **Forretningsprosess** og **Avgiftsretninger** i tabellen. Begge kolonnene er vesentlige for funksjonaliteten for avgift i overføringsordrer.

    2. Legg til relevansregler. Ikke la feltene **Avgiftskoder**, **Avgiftsgruppe** og **Vareavgiftsgruppe** være tomme.
        
        Legg til en ny regel for forsendelse av overføringsordren.
        1. Velg **Legg til** i **Relevansregler**-tabellen.
        2. I feltet **Forretningsprosess** velger du **Beholdning** for å gjøre regelen aktuall for en overføringsordre.
        3. I feltet **Send fra land/område** angir du **NLD**.
        4. I feltet **Send til land/område** angir du **BEL**.
        5. I feltet **Avgiftsretning** velger du **Utgang** for å gjøre regelen aktuell for overføringsordreforsendelsen.
        6. I **Avgiftskoder**-feltet velger du **NL-Exempt**.
        7. I **Avgiftsgruppe**-feltet og i **Vareavgiftsgruppe** angir du den relatert mva-gruppen og vareavgiftsgruppen som er definert i Finance-systemet ditt.
        
        Legg til en annen regel for mottak av overføringsordren.
        1. Velg **Legg til** i **Relevansregler**-tabellen.
        2. I feltet **Forretningsprosess** velger du **Beholdning** for å gjøre regelen aktuall for en overføringsordre.
        3. I feltet **Send fra land/område** angir du **NLD**.
        4. I feltet **Send til land/område** angir du **BEL**.
        5. I feltet **Avgiftsretning** velger du **Innkommende** for å gjøre regelen aktuell for overføringsordremottaket.
        6. I **Avgiftskoder**-feltet velger du **BE-RC+21** og **BE-RC-21**.
        7. I **Avgiftsgruppe**-feltet og i **Vareavgiftsgruppe** angir du den relatert mva-gruppen og vareavgiftsgruppen som er definert i Finance-systemet ditt.

        ![Relevansregler.](../media/image5.png)

4. Fullfør og publiser den nye avgiftsfunksjonsversjonen.

    [![Endring av statusen for den nye versjonen.](../media/image6.png)](../media/image6.png)

## <a name="set-up-finance-for-transfer-order-transactions"></a>Konfigurer Finance for avgiftsordretransaksjoner

Følg disse trinnene for å aktivere og konfigurere avgifter for overføringsordrer.

1. I Finance går du til **Arbeidsområder** \> **Funksjonsbehandling**.
2. I listen finner du og velger funksjonen **Avgift i overføringsordre**, og deretter velger du **Aktiver nå** for å aktivere den.

    > [!IMPORTANT]
    > Funksjonen **Avgift i overføringsordre** er fullstendig avhengig av avgiftstjenesten. Derfor kan den bare aktiveres etter at du har installert avgiftstjenesten.

    ![Funksjonen Avgift i overføringsordre.](../media/image7.png)

3. Aktiver avgiftstjenesten, og velg forretningsprosessen **Beholdning**.

    > [!IMPORTANT]
    > Du må fullføre dette trinnet for hver juridiske enhet i Finance der du vil at avgiftstjenesten og funksjonaliteten for avgift i overføringsordrer skal være tilgjengelig.

    1. Gå til **Avgift** \> **Oppsett** \> **Avgiftskonfigurasjon** \> **Oppsett av avgiftstjeneste**.
    2. I **Forretningsprosess**-feltet velger du **Beholdning**.

    ![Angi Forretningsprosess-feltet.](../media/image8.png)

4. Kontroller at mekanismen for snudd avregning er konfigurert. Gå til **Økonomimodul** \> **Oppsett** \> **Parametere**, og gå deretter til fanen **Snudd avregning** og bekreft at **Aktiver snudd avregning** er satt til **Ja**.

    ![Aktiver alternativet for snudd avregning.](../media/image9.png)

5. Kontroller at de tilknyttede avgiftskodene, avgiftsgruppene, vareavgiftsgruppene og mva-registreringsnumrene er definert i Finance i henhold til retningslinjene for avgiftstjenesten.
6. Definer en midlertidig transittkonto. Dette trinnet er bare nødvendig når avgiften som brukes på overføringsordrer, ikke gjelder for en mekanisme for avgiftsfritak eller snudd avregning.

    1. Gå til **Avgift** \> **Oppsett** \> **Merverdiavgift** \> **Finansposteringsgrupper**.
    2. I feltet **Midlertidig transitt** velger du en finanskonto.

    ![Velge en midlertidig transittkonto.](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a>Konfigurer enkel beholdning for avgiftsordretransaksjoner

Følg denne fremgangsmåten for å sette opp enkel beholdning for å aktivere overføringsordretransaksjoner.

1. Opprett stedene for send fra og sendt til for lagrene dine i forskjellige land eller områder, og legg til primæradressen for hvert område.

    1. Gå til **Lagerstyring** \> **Oppsett** \> **Lager** \> **Steder**.
    2. Velg **Ny** for å opprette stedet du vil tilordne til et lager senere.
    3. Gjenta trinn 2 for alle de andre stedene du må opprette.

    > [!NOTE]
    > Ett av stedene du oppretter, bør ha navnet **Transitt**. I senere trinn i denne fremgangsmåten tilordner du dette området til transittlageret, slik at avgiftsrelaterte beholdningsbilag kan posteres i "send"- og "motta"-transaksjoner for overføringsordrer. Adressen til transittstedet er ikke relevant for avgiftsberegningen. Du kan derfor la det stå tomt.

    ![Sette opp steder.](../media/image11.png)

2. Opprett lagre for send fra, transitt og send til. Alle adresseopplysninger som vedlikeholdes på et lager, vil overstyre stedsadressen under avgiftsberegningen.

    1. Gå til **Lagerstyring** \> **Oppsett** \> **Lager** \> **Lagre**.
    2. Velg **Ny** for å opprette et lager, og tilordne det til det tilsvarende stedet.
    3. Gjenta trinn 2 for å opprette et lager for hvert sted etter behov.

    ![Definere lagre.](../media/image12.png)

    > [!NOTE]
    > For et send fra-lager må et transittlager være valgt i i **Transittlager**-feltet for overføringsordretransaksjoner.
    >
    > ![Velge et transittlager.](../media/image13.png)

3. Kontroller at konfigurasjonen for beholdningspostering er definert for overføringsordretransaksjoner.

    1. Gå til **Lagerstyring** \> **Oppsett** \> **Postering** \> **Postering**.
    2. På **Beholdning**-fanen kontrollerer du at en beholdningskonto er definert både for postering av **Lageravgang** og **Lagertilgang**.

        ![Definere lageravgangs- og lagertilgangspostering.](../media/image14.png)

    3. Kontroller at en finanskonto er satt opp for postering av typen **Overføring, skyldig**.

        ![Definere postering av typen Overføring, skyldig.](../media/image15.png)

    4. Kontroller at en finanskonto er satt opp for postering av typen **Overføring, tilgode**.

        ![Definere postering av typen Overføring, tilgode.](../media/image16.png)

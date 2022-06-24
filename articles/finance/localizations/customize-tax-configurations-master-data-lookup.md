---
title: Tilpass avgiftskonfigurasjoner for hoveddataoppslag
description: Denne artikkelen beskriver hvordan du tilpasser mva-konfigurasjoner for å utvide funksjonaliteten for hoveddataoppslag.
author: kai-cloud
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 31c15c47fa1dc6861ff555a991d5f9233b7df35e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845191"
---
# <a name="customize-tax-configurations-for-master-data-lookup"></a>Tilpass avgiftskonfigurasjoner for hoveddataoppslag

[!include [banner](../includes/banner.md)]

Følg trinnene i denne artikkelen for å tilpasse mva-konfigurasjoner for å utvide funksjonaliteten for hoveddataoppslag.

## <a name="import-a-tax-configuration-provided-by-microsoft"></a>Importere en mva-konfigurasjon som leveres av Microsoft

1. I RCS (Regulatory Configuration Service) i arbeidsområdet **Elektronisk rapportering** velger du **Microsoft**-konfigurasjonsleverandøren.
2. Velg **Repositorier**.
3. Velg **Global**, og velg deretter **Åpne**.
4. Velg en mva-konfigurasjon, for eksempel **Konfigurasjon for avgiftsberegning**, og velg deretter en versjon i kategorien **Versjoner**.
5. Velg **Import**.

> [!NOTE]
> Som standard importeres Dataverse-modelltilordningen. Hvis du mottar advarsler under konfigurasjonsimportprosessen, må du aktivere de virtuelle enhetene i Dataverse. Hvis du vil ha mer informasjon, kan du se [Aktiver Dataverse virtuelle enheter](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="create-a-customized-data-model-configuration"></a>Opprette en tilpasset datamodellkonfigurasjon

1. I arbeidsområdet for **elektronisk rapportering** velger du **Mva-konfigurasjoner**, og deretter velger du datamodellkonfigurasjonen som skal forlenges. Velg for eksempel **Datamodell for avgiftsberegning**.
2. Velg **Opprett konfigurasjon**.
3. Velg **Modell for avgiftsbelagte dokumenter utledet fra navnet: Datamodell for avgiftsberegning, Microsoft**.
4. I feltet **Navn** angir du **Datamodell for tilpasning**.
5. Velg **Opprett konfigurasjon**.

## <a name="create-customized-reference-models"></a>Opprette tilpassede referansemodeller

1. På siden **Mva-konfigurasjoner** velger du **Datamodell for tilpasning**, og deretter velger du **Utforming**.
2. Velg ellipseknappen (**...**), og velg deretter visningen **Referansemodell**.

    [![Referansemodell.](./media/pic2.png)](./media/pic2.png)

3. Opprette den tilpassede referansemodellen. Den tilpassede modellen er en rotmodell. Den tilpassede enheten er en postliste. Det tilpassede feltet er et strengfelt som du vil bruke i oppslaget. Du kan legge til flere felt etter behov.
4. Velg ellipseknappen (**...**), og velg deretter visningen **Avgiftsbelagt dokument**.
5. Velg attributtet som skal knyttes til den tilpassede referansemodellen. Velg for eksempel **Tilpasset attributt**, og følg deretter denne fremgangsmåten:

    1. Velg **Velg referansemodell**.
    2. Velg **Tilpasset modell**, og velg deretter **OK**. Navnet på referansemodellen oppdateres til verdien i feltet **Naturlig nøkkel**.

        [![Velg dialogboksen for referansemodell.](./media/pic5.png)](./media/pic5.png)

    3. Velg **Lagre**, og velg deretter **Fullfør**.

## <a name="create-a-customized-model-mapping-configuration"></a>Opprette en tilpasset modelltilordningskonfigurasjon

1. I arbeidsområdet for **Elektronisk rapportering** velger du **Mva-konfigurasjoner**, og deretter velger du **Dataverse-modelltilordning**-konfigurasjonen.
2. Velg **Ja** i feltet **Standardalternativ for modelltilordning**.
3. Velg **Opprett konfigurasjon**.
4. Velg **Modelltilordning for avgiftsbelagte dokumenter utledet fra navnet: Dataverse-modelltilordning, Microsoft**.
5. I feltet **Navn** angir du **Tilordning av tilpasningsmodell**.
6. Velg **Datamodell for tilpasning**-datamodellen i feltet **Målmodell**.
7. Velg **Opprett konfigurasjon**.

    [![Rullegardinlisten Opprett konfigurasjon.](./media/pic6.png)](./media/pic6.png)

8. Velg **Tilordning av tilpasningsmodell**, og sett feltet **Tilkoblet program** til tilkoblingen som ble opprettet i trinn 8 i [Konfigurer et miljø for hoveddataoppslag](tax-service-set-up-environment-master-data-lookup.md).
9. Sett feltet **Standard for modelltilordning** til **Ja**.

## <a name="create-customized-model-mappings"></a>Opprette tilpassede modelltilordninger

1. På siden **Avgiftskonfigurasjoner** velger du **Tilordning av tilpasningsmodell**.
2. Velg **Utforming**, og velg deretter **Tilpasningsmodell**.

    [![Tilpasningsmodell.](./media/pic8.png)](./media/pic8.png)

## <a name="map-a-model-mapping-to-a-dataverse-entity"></a>Tilordne en modelltilordning til en Dataverse-enhet

1. På siden **Modelltilordningsutforming** velger du **Tilpasningsmodell**, og deretter velger du **Utforming**.
2. I treet **Datakildetyper** velger du **Dataverse-tabell**.
3. I fanen **Datakilder** velger du **Legg til rot**.
4. I **Navn**-feltet angir du **Tilpasset Dataverse**.
5. I det andre **Navn**-feltet velger du en enhet.
6. Velg **OK**.

    [![Dialogboksen for Tabell-datakildeegenskaper.](./media/pic9.png)](./media/pic9.png)

7. Velg **Tilpasset Dataverse** og **Tilpasset enhet**, og velg deretter **Bind**.

    [![Tilpasset Dataverse og Tilpasset enhet-binding.](./media/pic10.png)](./media/pic10.png)

8. Under **Tilpasset Dataverse** og **Tilpasset felt** velger du et felt, og deretter velger du **Bind**.

    [![Tilpasset Dataverse og Tilpasset felt-binding.](./media/pic11.png)](./media/pic11.png)

9. Velg **Lagre**, og velg deretter **Fullfør**.

## <a name="create-a-customized-tax-configuration"></a>Opprette en tilpasset mva-konfigurasjon

1. I arbeidsområdet for **Elektronisk rapportering** velger du **Mva-konfigurasjoner**, og deretter velger du **Konfigurasjon for avgiftsberegning**.
2. Velg **Opprett konfigurasjon**.
3. Velg **Konfigurasjon av avgiftstjeneste utledet fra navnet: Konfigurasjon for avgiftsberegning, Microsoft**.
4. I feltet **Navn** angir du **Tilpasningskonfigurasjon**.
5. Velg **Opprett konfigurasjon**.
6. Velg **Tilpasningskonfigurasjon**, og velg deretter **Utforming**.
7. Velg **Datamodell**-feltet velger du **Datamodell for tilpasning**.
8. I feltet **Datamodellversjon** velger du den tilsvarende datamodellversjonen.

    [![Egenskaper-delen.](./media/pic13.png)](./media/pic13.png)

9. Velg **Fullfør**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

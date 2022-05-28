---
title: Oppdatere sertifikatnumre og -datoer for TDS-transaksjoner
description: Dette emnet forklarer hvordan du oppdaterer numrene og datoene for fradragsberettigede sertifikater som ble registrert for leverandør-, kunde- og finanskontoer for TDS (Tax Deducted at Source).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7f8b5713e8ce3f9e9c89b8b3bc6ea84fe1f0fa54
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724818"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a>Oppdatere sertifikatnumre og -datoer for TDS-transaksjoner

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du oppdaterer numrene og datoene for fradragsberettigede sertifikater som ble registrert for leverandør-, kunde- og finanskontoer for TDS (Tax Deducted at Source). Du kan vise sertifikatene for TDS-transaksjoner på siden **Fradragsberettigede sertifikater**. Du kan oppdatere sertifikatene ved å bruke **Oppdater sertifikater**-siden.

Følg denne fremgangsmåten for å oppdatere sertifikatnumrene og -datoene for TDS-transaksjoner.

1. Gå til **Avgift \> Deklareringer \> Kildeskatt \> Oppdater sertifikat**.

    [![Siden Oppdater sertifikat.](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)

2. Velg **TDS** i **Avgiftstype**-feltet i **Velg**-delen på siden **Oppdater sertifikat**.
3. Velg kundens eller leverandørens TDS-sertifikatnummer i **Sertifikatnummer**-feltet.

    > [!NOTE]
    > **Sertifikatnummer**-feltet viser bare TDS-sertifikatnumre som alternativet **Lukket** ikke er avmerket for, på siden **Fradragsberettigede sertifikater**.

    **Sertifikatdato**-feltet viser sertifikatdatoen. **Kontotype**-feltet viser kontotypen som TDS-sertifikatnummeret mottas for, og **Navn**-feltet viser navnet på kontoen.

5. Velg start- og sluttdatoene for perioden du vil vise TDS-transaksjonene for, i feltene **Fra-dato** og **Til-dato** .
6. Velg **Vis data** for å vise TDS-transaksjonene som ble postert i løpet av den valgte perioden.

    Rutenettet i den øvre ruten i **Oversikt**-fanen viser følgende informasjon om hver TDS-transaksjon som ble postert for leverandøren eller kunden i løpet av den valgte perioden:

    - **Bilag** – Bilagsnummeret for TDS-transaksjonen.
    - **Dato** – Datoen for TDS-transaksjonen.
    - **Beløp** – Fakturabeløpet som TDS ble beregnet for.
    - **Avgiftsbeløp** – TDS-avgiftsbeløpet som ble beregnet for transaksjonen.

7. Hvis du vil flytte bestemte TDS-transaksjoner fra det øvre til det nedre rutenettet, velger du transaksjonene og deretter **Inkluder**. Du kan også velge **Inkluder alle** hvis du vil flytte alle TDS-transaksjoner fra det øvre til det nedre rutenettet.

    Hvis du vil flytte bestemte TDS-transaksjoner eller alle TDS-transaksjoner fra det nedre til det øvre rutenettet, bruker du knappen **Utelat** eller **Utelat alle**.

8. Velg **Oppdater** for å oppdatere feltene **Sertifikatnummer** og **Sertifikatdato** for TDS-transaksjoner i det nedre rutenettet.
10. Gå til **Avgift \> Indirekte avgifter \> Kildeskatt \> Fradragsberettigede sertifikater**, og velg **Forespørsel** for å vise de oppdaterte transaksjonslinjene som har de nye sertifikatnumrene på **Sertifikattransaksjoner**.

    [![Siden Sertifikattransaksjoner.](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)

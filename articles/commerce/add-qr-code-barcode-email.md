---
title: Legge til en QR-kode eller strekkode i e-postmeldinger for transaksjon og kvittering
description: Denne artikkelen beskriver hvordan du setter inn QR-koder og strekkoder som representerer ordre-ID-er, i e-postmeldinger for transaksjoner og kvitteringer i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 2832d1df3893e124759e4719a64341494cea2204
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272051"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a>Legge til en QR-kode eller strekkode i e-postmeldinger for transaksjon og kvittering

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du setter inn QR-koder og strekkoder som representerer ordre-ID-er, i e-postmeldinger for transaksjoner og kvitteringer i Microsoft Dynamics 365 Commerce.

Du kan lett ta med QR-koder og strekkoder i transaksjons-e-postmeldinger for å gjøre ordreoppslagsprosessen raskere i et detaljhandelsmiljø. Hvis du vil sette inn QR-koder og strekkoder i e-postmeldinger, bruker du en HTML-kode **\<img\>** som ber om en QR-kode eller strekkodebilde fra en genererings- og gjengivelsestjeneste. Microsoft tilbyr ikke denne tjenesten. Det finnes imidlertid mange gratis- eller tilbudstjenester som kan tjene QR-koder eller strekkoder som genereres dynamisk basert på en verdi som sendes i en spørringsstreng.

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a>Legge til en QR-kode eller strekkode i transaksjons-e-post

Følg denne fremgangsmåten for å sette inn en QR-kode eller strekkode i en transaksjons-e-post som sendes som en del av et e-commerce-innkjøp.

1. Åpne HTML-kilden for den transaksjonsbaserte e-postmalen, og legg til en HTML-kode **\<img\>** som peker til QR-koden eller strekkodetjenesten. Her er et eksempel:

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    Her er en forklaring av det forrige eksemplet:

    - **DIN\_QR-\_KODE\_STREK\_KODE\_TJENESTE** representerer domenet for QR-koden eller strekkodetjenesten din.
    - **dara** representerer parameteren som QR-koden eller strekkodetjenesten bruker til å motta innholdet som skal gjengis som en QR-kode eller strekkode.

        Verdien **%salesid%** må tilordnes til denne parameteren. I dette eksemplet kan du legge merke til at verdien også brukes som alternativ tekst for bildet.

    - **param1** og **param2** representerer ekstra valgfrie parametere.

1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Maler for e-post til organisasjon**, og last opp den oppdaterte HTML-en til den riktige malen for transaksjons-e-post.

> [!NOTE]
> Parametere kan være forskjellige blant leverandørene av QR-kode og strekkodetjeneste. Husk derfor å ta kontakt med leverandøren for å bekrefte parameterne du må tilordne verdier til.

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a>Legge til en QR-kode eller strekkode i en kvitterings-e-post 

Følg denne fremgangsmåten for å sette inn en QR-kode eller strekkode i en kvitterings-e-post som kan sendes etter at et kjøp er foretatt ved salgsstedet (POS).

1. Åpne HTML-kilden for malen for kvitterings-e-post, og legg til en HTML-kode **\<img\>** som peker til QR-koden eller strekkodetjenesten. Nedenfor ser du et eksempel.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    Her er en forklaring av det forrige eksemplet:

    - **DIN\_QR-\_KODE\_STREK\_KODE\_TJENESTE** representerer domenet for QR-koden eller strekkodetjenesten din.
    - **dara** representerer parameteren som QR-koden eller strekkodetjenesten bruker til å motta innholdet som skal gjengis som en QR-kode eller strekkode.

        Verdien **%receiptid%** må tilordnes til denne parameteren. I dette eksemplet kan du legge merke til at verdien også brukes som alternativ tekst for bildet.

    - **param1** og **param2** representerer ekstra valgfrie parametere.

1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Maler for e-post til organisasjon**, og last opp den oppdaterte HTML-en til e-postmalen som har e-post-ID-en **emailrecpt**.

> [!NOTE]
> Parametere kan være forskjellige blant leverandørene av QR-kode og strekkodetjeneste. Husk derfor å ta kontakt med leverandøren for å bekrefte parameterne du må tilordne verdier til.

## <a name="additional-resources"></a>Tilleggsressurser

[Sende e-postkvitteringer fra Modern POS (MPOS)](email-receipts.md)

[Opprette e-postmaler for transaksjonshendelser](email-templates-transactions.md)

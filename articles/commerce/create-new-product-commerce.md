---
title: Opprette et nytt produkt i Commerce
description: Dette emnet beskriver hvordan du oppretter et nytt produkt i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3b578c1bdfe1c6b4bf66cc85cc09ed906fb812a8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965324"
---
# <a name="create-a-new-product-in-commerce"></a>Opprette et nytt produkt i Commerce


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du oppretter et nytt produkt i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Et produkt er først og fremst definert av produktnummer, navn og beskrivelse. Andre data er imidlertid også nødvendig for å beskrive et produkt eller en tjeneste:

## <a name="create-a-new-product"></a>Opprette et nytt produkt

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Produkter og kategorier \> Produkter etter kategori**.
1. I handlingsruten velger du **Ny**.
1. I **Produkttype**-rullegardinlisten velger du **Element** eller **Tjeneste**.
1. I **Produktundertype**-rullegardinlisten velger du **Produkt** (hvis produktet ikke har noen varianter) eller **Produktstandard** (hvis produktet kommer til å ha varianter).
1. I **Produktnummer**-boksen angir du et produktnummer hvis det ikke allerede er forhåndsutfylt.
1. I **Produktnavn**-boksen angir du et produktnavn.
1. I **Søk etter navn**-boksen angir du et søkenavn.
1. I **Handelskategori**-rullegardinlisten velger du en passende kategori.
1. Hvis produktet er et sett, velger du **Ja** for **Produktsett**.
1. Hvis produktundertypen er produktstandard, setter du **Produktdimensjonsgruppe** til å inkludere de støttede variantene. Alternativene inkluderer **Farge**, **Størrelse**, **Stil** og **Konfigurasjon**. Det er mulig at du om nødvendig må opprette flere produktdimensjonsgrupper.
1. I **Konfigurasjonsteknologi**-rullegardinlisten velger du et passende alternativ.
1. Velg **OK**.

Følgende bilde viser et eksempelprodukt som legges til.

![Opprette et produkt](media/create-new-product.png)

Når et produkt er lagt til, kan ekstra data angis for det, for eksempel **Produktbeskrivelse**, **Variantgrupper**, **Dimensjonsgrupper**, **Produktattributter** og **Relaterte produkter**.

Det følgende bildet viser flere detaljer for produktet.

![Produktdetaljer](media/create-new-product-2.png)

### <a name="create-product-variants"></a>Opprett produktvarianter

Hvis produktundertypen er **Produktstandard**, må spesifikke varianter opprettes. 

Hvis du vil opprette produktvarianter, følger du disse trinnene.

1. I handlingsruten velger du **Produktvarianter**.
1. Hvis variantgrupper er valgt i handlingsruten, velger du **Variantforslag*.
1. Velg variantene du vil støtte for produktet.
1. Velg **Opprett**.

## <a name="release-a-product"></a>Frigi et produkt

Hvis du vil selge et produkt, må det først frigis til en juridisk enhet.

1. Fra produktsiden velger du **Frigi produkter**.

    ![Frigi produkt](media/create-new-product-3.png)

1. Velg produktet som skal frigis, og velg deretter **Neste**.

    ![Velg produktet som skal frigis](media/create-new-product-4.png)

1. Velg produktvariantsettet som skal frigis, og velg deretter **Neste**.

    ![Velg variantene som skal frigis](media/create-new-product-5.png)

1. Velg den juridiske enheten, og velg deretter **Neste**.

    ![Velg juridisk enhet](media/create-new-product-6.png)

1. Velg **Fullfør**.

    ![Avslutte produktfrigivelse](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a>Konfigurer et frigitt produkt

Når et produkt er frigitt, vil det kreve ytterligere konfigurasjon som omfatter tilføying av en pris for produktet.

1. I navigasjonsruten går du til **Moduler \> Handel og detaljhandel \> Produkter og kategorier \> Frigitte produkter etter kategori**.
1. Velg produktkategorinoden for produktet som ble frigitt, og velg deretter produktet fra produktlisten.
1. I handlingsruten velger du **Rediger**.
1. I **Kjøp**-delen konfigurerer du eventuelle påkrevde egenskaper, inkludert **Enhet**, **Pris** og **Antall**.
1. I handlingsruten velger du **Valider** for å sikre at det ikke rapporteres noen feil for manglende felt.
1. Velg **Lagre** i handlingsruten.

Bildet nedenfor viser en eksempelkonfigurasjon for et frigitt produkt.

![Konfigurere et frigitt produkt](media/create-new-product-8.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Opprett juridiske enheter](channels-legal-entities.md)

[Opprette en variantgruppe](create-variant-group.md) 

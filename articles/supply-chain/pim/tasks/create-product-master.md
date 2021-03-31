---
title: Opprette en produktstandard
description: Opprett en produktstandard for de forhåndsdefinerte variantene.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d580d323409d84bab66dc03d39e084f5ee0cfc64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218495"
---
# <a name="create-a-product-master"></a>Opprette en produktstandard

[!include [banner](../../includes/banner.md)]

Opprett en produktstandard for de forhåndsdefinerte variantene. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne fremgangsmåten er ment for produktdesigneren.


## <a name="create-a-new-product-master"></a>Opprette en ny produktstandard
1. Gå til **Navigasjonsrute > Moduler > Behandling av produktinformasjon > Produkter > Produktstandarder**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i feltet **Produktnummer**. Nummeret må være unikt. Du kan angi en nummerserie for feltet **Produktnummer**. I så fall trenger ikke brukeren å angi en verdi.
4. Skriv inn en verdi i feltet **Produktnavn**. Angi et beskrivende produktnavn. Verdien angis som standard til søkenavnet, men dette kan endres av brukeren.
5. Klikk på rullegardinknappen i feltet **Produktdimensjonsgruppe** for å åpne oppslaget. Produktdimensjonsgruppen bestemmer hvilke 4 produktdimensjoner som kan brukes til å opprette produktvarianter. Dette eksemplet brukes en gruppe med farge og størrelse.
6. Finn og velg ønsket post i listen.
7. Klikk på koblingen i den valgte raden i listen. Standard **Konfigurasjonsteknologi** er Forhåndsdefinert variant. Denne vil bli brukt i dette eksemplet.
8. Klikk på **OK**.

## <a name="select-product-dimension-groups"></a>Velg produktdimensjonsgrupper
1. Klikk på rullegardinknappen i feltet **Fargegruppe** for å åpne oppslaget.
2. Finn og velg ønsket post i listen.
3. Klikk på koblingen i den valgte raden i listen.
4. Klikk på rullegardinknappen i feltet **Størrelsesgruppe** for å åpne oppslaget.
5. Finn og velg ønsket post i listen.
6. Klikk på koblingen i den valgte raden i listen.

## <a name="add-dimension-groups"></a>Legge til dimensjonsgrupper
1. I **handlingsruten** klikker du på **Produkt**.
2. Klikk på **Dimensjonsgrupper** for å åpne nedtrekksdialogen.
3. Klikk på rullegardinknappen i **Lagringsdimensjonsgruppe**-feltet for å åpne oppslaget. Lagringsdimensjoner hjelper deg styre hvordan varer lagres og hentes fra lageret. En lagringsdimensjon kan for eksempel inkludere Område og lager.
4. Finn og velg ønsket post i listen.
5. Klikk på koblingen i den valgte raden i listen.
6. Klikk på rullegardinknappen i **Sporingsdimensjonsgruppe**-feltet for å åpne oppslaget. Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner du kan legge til et produkt. Parti- eller serienummer brukes for eksempel til å spore varer på lager.
7. Finn og velg ønsket post i listen.
8. Klikk på koblingen i den valgte raden i listen.
9. Klikk på **OK**.
10. Klikk på **Lagre**.
11. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
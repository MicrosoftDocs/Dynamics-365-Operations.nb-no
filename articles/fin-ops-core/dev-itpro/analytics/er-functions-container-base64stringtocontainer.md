---
title: ER-funksjonen Base64StringToContainer
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen (Elektronisk rapportering) Base64StringToContainer.
author: NickSelin
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: bcbbead1155a7270a329c23055340492c73cdfda
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879927"
---
# <a name="base64stringtocontainer-er-function"></a>ER-funksjonen Base64StringToContainer

[!include [banner](../includes/banner.md)]

[Funksjonen](er-formula-language.md#Functions) `BASE64STRINGTOCONTAINER` konverterer de angitte inndataene for *Streng*-typen til et dataelement av typen *[Beholder](er-functions-category-container.md)*.

## <a name="syntax"></a>Syntaks

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a>Argumenter

`input`: *Streng*

Den gyldige banen til en datakilde av *Streng*-typen.

## <a name="return-values"></a>Returverdier

*Beholder*

Den resulterende binærverdien i format for stort binærobjekt (BLOB-format).

## <a name="usage-notes"></a>Bruksnotater

Unntaket «Parameteren er ikke gyldig» oppstår hvis inndatastrengen ikke inneholder en riktig Base64-gruppe med binær-til-tekst-kodingsoppsett.

## <a name="example"></a>Eksempel

Du definerer de følgende datakildene i modelltilordningen:

- Rotdatakilden **DocuTypeGroupEnum** av typen *Dynamics 365 for Operations / Opplisting* som refererer til programopplistingen **DocuTypeGroup**
- Rotdatakilden **Customer** av typen *Dynamics 365 for Operations / Tabellposter* som refererer til programtabellen **CustTable**
- Datakilden **\#Media** av typen *Beregnet felt* som konfigureres på følgende måte:

    - Den legges til som en underordnet datakilde for datakilden **Customer**.
    - Den inneholder uttrykket `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.

- Datakilden **\#MediaAsBase64String** av typen *Beregnet felt* som konfigureres på følgende måte:

    - Den legges til som en underordnet datakilde for datakilden **Customer.'\#Media'**.
    - Den inneholder uttrykket `Customer.'#Media'.'getFileContentAsBase64String()'`.

- Datakilden **\#BlobFomBase64** av typen *Beregnet felt* som konfigureres på følgende måte:

    - Den legges til som en underordnet datakilde for datakilden **Customer.'\#Media'**.
    - Den inneholder uttrykket `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.

I dette eksemplet koder datakilden **\#MediaAsBase64String** det binære innholdet i det gjeldende medievedlegget som tekst som representerer en Base64-gruppe med binær-til-tekst-kodingsoppsett. Datakilden **\#BlobFomBase64** dekoder Base64-strengen og returnerer en binær verdi i BLOB-format.

![Eksempeldatakilder på siden ER-utforming av modelltilordning.](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Containerfunksjoner](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

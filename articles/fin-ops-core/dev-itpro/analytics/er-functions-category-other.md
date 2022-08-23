---
title: Liste over ER-funksjoner i kategorien for domenespesifikke forretningsfunksjoner
description: Denne artikkelen inneholder informasjon om domenespesifikke forretningsfunksjoner som støttes i elektronisk rapportering (ER).
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: b1ac46cf10d57b40af1fa99021156ad97a17ba20
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272690"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a>Liste over ER-funksjoner i kategorien for domenespesifikke forretningsfunksjoner

[!include [banner](../includes/banner.md)]

Domenespesifikke funksjoner for elektronisk rapportering (ER) kan brukes til å utføre beregninger og datatilgangsforespørsler som er spesifikke for implementeringen av Microsoft Dynamics 365 Finance. Denne artikkelen inneholder et sammendrag av disse funksjonene.

## <a name="list-of-supported-functions"></a>Liste over funksjoner som støttes

| Funksjon| Beskrivelse |
|---------|-------------|
| [CH_Bank_Mod_10](er-functions-other-chbankmode10.md) | Denne funksjonen returnerer en *streng*-verdi som representerer en kreditorreferanse som et MOD10-uttrykk, basert på sifrene i det angitte fakturanummeret. |
| [CN_GBT_AdditionalDimensionID](er-functions-other-cngbtadditionaldimensionid.md) | Denne funksjonen returnerer en *streng*-verdi som representerer en enkelt finansdimensjons-ID som er hentet fra den angitte strengen. Den angitte strengen viser alle dimensjonene som en kommadelt liste over IDer. |
| [ConvertCurrency](er-functions-other-convertcurrency.md) | Denne funksjonen returnerer en *reell* verdi som representerer resultatet av å konvertere det angitte pengebeløpet fra den angitte kildevalutaen til den angitte målvalutaen ved å bruke innstillingene for det aktuelle firmaet på den angitte datoen. |
| [CurCredRef](er-functions-other-curcredref.md) | Denne funksjonen returnerer en *streng*-verdi som representerer en kreditorreferanse, basert på sifrene i det angitte fakturanummeret. |
| [FA_Balance](er-functions-other-fabalance.md) | Denne funksjonen returnerer en *Container (post)*-verdi som består av data for anleggsmiddelsaldoen for den angitte anleggsmiddelvaren, verdimodellkoden, rapporteringsåret og rapporteringsdatoen. |
| [FA_Sum](er-functions-other-fasum.md) | Denne funksjonen returnerer en *Container (post)*-verdi som består av data for anleggsmiddelbeløpene for den angitte anleggsmiddelvaren, verdimodellkoden, rapporteringsåret og datoperioden. |
| [GetCurrentCompany](er-functions-other-getcurrentcompany.md) | Denne funksjonen returnerer en *streng*-verdi som representerer koden for den juridiske enheten (firma) som en bruker er logget på nå. |
| [ISOCredRef](er-functions-other-isocredref.md) | Denne funksjonen returnerer en *streng*-verdi som representerer en ISO-kreditorreferanse (International Organization for Standardization) basert på sifrene og de alfabetiske symbolene i det angitte fakturanummeret. |
| [IsValidCharacterISO7064](er-functions-other-isvalidchariso7064.md) | Denne funksjonen returnerer den *boolske* verdien **SANN** hvis den angitte strengen representerer et gyldig internasjonalt bankkontonummer (IBAN). Hvis ikke returneres den *boolske* verdien **USANN**. |
| [Mod_97](er-functions-other-mod97.md) | Denne funksjonen returnerer en *streng*-verdi som representerer en kreditorreferanse som et MOD97-uttrykk, basert på sifrene i det angitte fakturanummeret. |
| [NumSeqValue](er-functions-other-numseqvalue.md) | Denne funksjonen returnerer en *streng* verdi som representerer den nye genererte verdien av en nummerserie, basert på den angitte nummerserien, omfanget og område-IDen. Område-IDen er lik firmakoden som angis av konteksten som ER-formatet kjøres under. |
| [RoundAmount](er-functions-other-roundamount.md) | Denne funksjonen returnerer en *reell* verdi som representerer resultatet av avrunding av det angitte beløpet til det angitte antallet desimaler i henhold til den angitte avrundings regelen. |
| [TableName2ID](er-functions-other-tablename2id.md) | Denne funksjonen returnerer en numerisk representasjon av tabell-IDen for det angitte tabellnavnet som en *heltall*-verdi. |

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelspråk i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

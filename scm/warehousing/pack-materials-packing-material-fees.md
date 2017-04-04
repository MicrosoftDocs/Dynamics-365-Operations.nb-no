---
title: Emballasjematerialer og gebyrer
description: "Emballasjematerialegebyrer betales til et resirkuleringsfirma med bestemte intervaller. Et beløp betales per vektenhet for hvert materiale som en emballasjeenhet består av. Emballasjematerialegebyrer beregnes og rapporteres, men ingen finanstransaksjoner posteres fordi gebyrene ikke regnes som avgifter som må betales til en myndighet."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 7c0bc5b5d86956336012096c11d0d7621abab1f9
ms.lasthandoff: 03/31/2017


---

# <a name="packing-materials-and-fees"></a>Emballasjematerialer og gebyrer

Emballasjematerialegebyrer betales til et resirkuleringsfirma med bestemte intervaller. Et beløp betales per vektenhet for hvert materiale som en emballasjeenhet består av. Emballasjematerialegebyrer beregnes og rapporteres, men ingen finanstransaksjoner posteres fordi gebyrene ikke regnes som avgifter som må betales til en myndighet.

Emballasjevekt og -gebyrer beregnes for både salgsordrelinjer og bestillingslinjer.

Du kan definere én eller flere emballasjeenheter for en vare, for en pakkegruppe med varer eller for alle varer. En emballasjeenhet består av emballasjematerialer, vekt og antall varer som er tatt med i emballasjeenheten. En emballasjekode er tilordnet til hver type emballasje som er definert. Basert på emballasjekoden kan du angi en pris for en bestemt periode. Emballasjegebyret beregnes basert på denne informasjonen.

| **Obs! **                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Selv om firmaet ikke betaler emballasjegebyrer, kan du bruke funksjonaliteten til å beregne statistikk for emballasjevekt. |

## <a name="setup-requirements-for-packing-material-fees"></a>Installasjonskrav for emballasjegebyr
Før du beregner emballasjevekt eller -gebyrer, eller begge deler, oppretter du følgende stamdata:

-   Pakkegrupper – Opprett emballasjegrupper som skal tilordnes varer.
-   Emballasjekoder – Opprett emballasjekoder for hver type emballasje som er definert.
-   Emballasjeenheter – Angi en emballasjeenhet for en vare, for en emballasjegruppe eller for alle varer. For hver emballasjeenhet definerer du hvilke emballasjematerialer som skal inkluderes, tilordner vekter og angir omregningsfaktor fra lagerenheten i feltet Emballasjeenhetsfaktor.
-   Emballasjematerialegebyrer – Angi emballasjegebyrer per emballasjekode. For hver type emballasje definerer du perioden for gyldighet, prisen per emballasje, valutaen og enheten.

## <a name="packing-units-on-sales-order-lines"></a>Emballasjeenheter på salgsordrelinjer
Når du oppretter en salgsordrelinje, kontrollerer systemet om emballasjeenheter er angitt for varen. Hvis emballasjeenheter er angitt, oppdaterer systemet salgsordrelinjen med den angitte emballasjeenheten og antallet for emballasjeenheten. Antallet for emballasjeenheten er basert på det bestilte antallet dividert med antallet varer i den valgte emballasjeenheten. Hvis en emballasjeenhet ikke er angitt, kan du angi en emballasjeenhet manuelt og et antall for emballasjeenhet på salgsordrelinjen. Du kan også endre emballasjeenheten og antallet for emballasjeenhet når du posterer salgsordrelinjen. Dette er aktuelt hvis salgsordrelinjen bare er delvis levert eller delvis fakturert. Når du fakturerer salgsordren, opprettes emballasjetransaksjoner. Emballasjetransaksjoner inneholder vekt for emballasjematerialer for salgslinjen. Du kan også redigere transaksjonene etter fakturering og deretter opprette nye transaksjoner.

## <a name="packing-units-on-purchase-order-lines"></a>Emballasjeenheter på bestillingslinjer
Emballasjematerialetransaksjoner for en bestillingslinje opprettes ikke av systemet. Du kan opprette transaksjoner for fakturerte bestillingslinjer manuelt på siden **Emballasjematerialetransaksjoner**.

## <a name="set-up-customer-packagingmaterialfee-license-numbers"></a>Angi kundens lisensnumre for packagingmaterialfee
Hvis kundene betaler emballasjegebyrene, angir du kundenes lisensnumre for emballasjegebyr på siden **Kunder**. Når et lisensnummer er tilordnet en kunde, beregnes emballasjegebyrene automatisk når salgsordrene faktureres. Etter fakturering fjernes merket for **Beregn gebyr** på siden **Emballasjematerialetransaksjoner** fordi du ikke trenger å beregne og skrive ut rapporten. Du kan skrive ut emballasjevekten og informere kundene om at de må betale gebyrene. 

Hvis firmaet betaler emballasjegebyrene, angir du ikke kundens lisensnumre. Etter fakturering merker du av for **Beregn gebyr** på siden **Emballasjematerialetransaksjoner**. Dette viser at gebyrene beregnes når en rapport opprettes. Du kan skrive ut vekten på fakturaen og angi at firmaet betaler gebyrene.

## <a name="print-packaging-material-weights-on-invoices"></a>Skrive ut emballasjevekt på fakturaer
Du kan skrive ut emballasjevekten på fakturaen og angi hvem som betaler emballasjegebyrene. Vekten summeres etter emballasjekode.
 




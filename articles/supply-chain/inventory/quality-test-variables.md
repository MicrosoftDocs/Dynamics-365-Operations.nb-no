---
title: Testvariabler for kvalitetsstyring
description: Denne artikkelen beskriver hvordan du oppretter testvariabler som kan brukes for kvalitative tester på kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10fe206b76f2e50e09cb6aaa6055614c2fe9425d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857641"
---
# <a name="quality-management-test-variables"></a>Testvariabler for kvalitetsstyring

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du oppretter testvariabler som kan brukes for kvalitative tester på kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.

Du må definere en testvariabel og mulige resultater for hver kvalitative test som defineres på siden **Tester**. (For kvalitative tester er **Type**-feltet på **Tester**-siden satt til *Alternativ*.)

Du kan bruke **Testvariabler**-siden til å definere, redigere og vise de mulige resultatene for en testvariabel som er knyttet til en kvalitativ test. For hvert resultat tilordner du resultatstatusen til enten *Bestått* eller *Mislykket* for å angi om testen er bestått eller mislyktes når dette resultatet er valgt som et testresult. Bruk siden **Testgrupper** for å tilordne en testvariabel og et standardresultat for den til en enkelt kvalitetstest.

For hver testvariabel anbefaler vi at du definerer minst to resultater: ett som har resultatstatusen *Bestått*, og ett som har resultatstatusen *Mislykket*. Det er ingen grense for totalt antall variabler eller resultater som kan defineres. I tillegg kan flere tester bruke de samme testvariablene til å registrere resultater.

## <a name="examples-of-test-variables"></a>Eksempler på testvariabler

### <a name="example-1"></a>Eksempel 1

Et produksjonsfirma utfører to tester på produserte materialer. I en test er pH-nivået knyttet til en fargestripe. Akseptable pH-nivåer er i lysere farger, og uakseptabelt pH-nivåer er i mørkere farger. I en annen test utføres det flere visuelle inspeksjoner, og kvalitetsarbeidere bruker sitt skjønn for å fastslå om varen består eller feiler den visuelle inspeksjonen.

### <a name="example-2"></a>Eksempel 2

En produksjonsfirma som produserer kjeks, bruker en inspeksjonstest til det ferdige produktet. Denne inspeksjonstesten har flere variabler. Én variabel er smak, og de mulige resultatene for den er god og dårlig. En annen variabel er farge, og de mulige resultatene for den er for mørk, for lys og riktig.

## <a name="create-a-test-variable"></a>Opprette en testvariabel

Hvis du vil opprette en testvariabel, følger du disse trinnene.

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Testvariabler**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Variabel** – Angi en unik ID eller et unikt navn for variabelen.
    - **Beskrivelse** – Angi en detaljert beskrivelse av variabelen.

1. Mens den nye raden fremdeles er valgt, velger du **Resultater** i handlingsruten.
1. Velg **Ny** i handlingsruten på siden **Testvariabelresultater** for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Resultat** – Angi en unik ID eller et unikt navn for resultatet.
    - **Beskrivelse** – Angi en detaljert beskrivelse av resultatet.
    - **Resultatstatus** – Velg enten *Bestått* eller *Mislykket* for å angi om testen er bestått eller mislyktes når resultatet er valgt som et testresult.

1. Gjenta det forrige trinnet for hvert tilleggsresultat. Kontroller at minst ett resultat har resultatstatusen *Bestått*, og at minst én har resultatstatusen *Mislykket*.
1. Lukk sidene.

## <a name="additional-resources"></a>Tilleggsressurser

- [Testinstrumenter for kvalitetsstyring](quality-test-instruments.md)
- [Kvalitetsstyringstester](quality-tests.md)
- [Testgrupper for kvalitetsstyring](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

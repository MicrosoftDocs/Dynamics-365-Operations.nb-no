---
title: Definere tillegg i konserninterne ordrer
description: Denne artikkelen forklarer hvordan du definerer tillegg i konserninterne ordrer
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7b84c0bac6c31139170a99afc65cd08d70bd018e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885848"
---
# <a name="set-up-charges-on-intercompany-orders"></a>Definere tillegg i konserninterne ordrer

[!include [banner](../../includes/banner.md)]

Du kan definere tillegg som skal legges til i konserninterne ordrer. Når en avgift legges til i en konsernintern salgsordre, synkroniseres den automatisk med den konserninterne bestillingen. Fungerer begge veier – fra den konserninterne salgsordren til bestillingen, og omvendt.

Du kan også bruke tillegg til å legge til en fortjeneste i en konsernintern salgsordre ved å definere tillegget som en konsernintern prosentandel.

Når du definerer tillegg som skal brukes i konserninterne ordrer, aktiverer du beregningen av intern fortjeneste for en konsernintern salgsordre fra nettobeløpet for den opprinnelige salgsordren. Du vil kanskje gjøre dette hvis den konserninterne leverandøren selger til deg til kostpris. Følgende fremgangsmåte beskriver hvordan du gjør dette for konserninterne kunder. Du kan bruke samme fremgangsmåte for leverandører.

1. Gå til **Kundee \> Oppsett \> Tillegg \> Kundetilleggsgrupper**.
1. Opprett en tilleggsgruppe.
1. Gå til **Kunder \> Kunder \> Alle kunder**. Velg en kundekontokobling. I handlingsruten velger du **Kunde**-fanen og deretter hurtigfanen **Salgsordre**.
1. Velg **Rediger** i handlingsruten for å aktivere endringer i feltet. Velg den konserninterne tilleggsgruppen du definerte i trinn 2, i **Tilleggsgruppe**-feltet.
1. Gå til **Kunder \> Oppsett \> Tillegg \> Automatiske gebyrer**.
1. Definer tilleggene ved å fylle ut de relevante feltene.
1. Velg den konserninterne tilleggsgruppen du definerte i trinn 2, i **Kunderelasjon**-feltet.
1. På **Linjer**-hurtigfanen i **Kategori**-feltet velger du **Konsernintern prosent**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

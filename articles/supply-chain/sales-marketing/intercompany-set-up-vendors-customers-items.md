---
title: Definere leverandører, kunder og varer for konsernintern handel
description: Dette emnet forklarer hvordan du definerer leverandører, kunder og varer for konsernintern handel
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 062b8fe956fef0f8172d26aac3df54b93e1941ef
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548439"
---
# <a name="set-up-vendors-customers-and-items-for-intercompany-trade"></a>Definere leverandører, kunder og varer for konsernintern handel

[!include [banner](../../includes/banner.md)]

Hvis du vil klargjøre organisasjonen for konsernintern handel, må du definere leverandørene og kundene du skal handle med internt. Deretter må du knytte disse leverandørene og kundene til varene du skal kjøpe eller selge.

1. Gå til **Innkjøp og leverandører \> Leverandører \> Alle leverandører**.
1. Velg leverandøren du vil definere som en konsernintern leverandør.
1. Velg **Konsernintern** i fanen **Generelt** i handlingsruten.
1. Angi konserninterne oppsettparametere for leverandørkontoen. Disse parameterne omfatter den juridiske enheten for kunde og konto, salgsordrepolicyer, bestillingspolicyer, verditilordning og policyer for innkjøpsavtale og salgsavtale. Du angir også om stamdataverdier skal brukes fra leverandørkontoen eller fra kundekontoen i den andre juridiske enheten.
1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. På listesiden **Frigitte produkter** velger du varene som skal tilordnes leverandøren, slik at varene er tilgjengelige for konsernintern handel. På siden **Detaljer om frigitt produkt** for hvert element. Skriv inn leverandørnummeret i kategorien **Kjøp** i feltet **Leverandør**.
1. Gå til **Kunder \> Kunder \> Alle kunder**.
1. Velg kunden du vil definere som en konsernintern kunde.
1. Velg **Konsernintern** i fanen **Generelt** i handlingsruten.
1. Angi konserninterne oppsettparametere for kundekontoen. Disse parameterne omfatter den juridiske enheten for leverandør og konto, bestillingspolicyer, salgsordrepolicyer, verditilordning og policyer for salgsavtale og bestilling. Du angir også om stamdataverdier skal brukes fra kundekontoen eller fra leverandørkontoen i den andre juridiske enheten.
1. På **Kunder**-siden i hurtigfanen **Faktura og levering** merker du av for **Opprett konserninterne ordrer**. Hvis du vil at ordrer skal leveres direkte til kunder, merker du av for **Direkte levering**.

    > [!NOTE]
    > Hvis det er noen varer som organisasjonen har på lager eller leverer til kunder, er det ikke sikkert at du vil opprette konserninterne ordrer automatisk, selv om du har varen på lager. Hvis du vil deaktivere den automatiske genereringen av ordrer for varer du noen ganger har på lager, merker du ikke av for **Opprett konserninterne ordrer**.

1. Hvis du vil tillate at det opprettes ekstra linjer indirekte i en salgsordre, merker du av for **Opprett indirekte ordrelinjer**. Dette gjør at en bruker kan legge til linjer i den opprinnelige salgsordren fra den konserninterne salgsordren.

> [!WARNING]
> Hvis du tillater indirekte oppretting av ordrelinjer, tillater du alle anskaffelser i den opprinnelige salgsordren fra den konserninterne salgsordren. Hver anskaffelse sendes deretter til kunden og legges til i ordren og fakturaen. I tillegg skrives alle dokumenter som er involvert i salget, ut og posteres automatisk. Brukere blir ikke varslet om tillegget.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

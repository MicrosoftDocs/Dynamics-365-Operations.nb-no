---
title: Definere leverandører, kunder og varer for konsernintern handel
description: Denne artikkelen forklarer hvordan du definerer leverandører, kunder og varer for konsernintern handel
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
ms.openlocfilehash: 4c928435a4e66832b09dbc805664934cfb1236be
ms.sourcegitcommit: b666289f5113d0a3fa2220fe337d5aacf07cbd92
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/08/2022
ms.locfileid: "8945762"
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
1. Når du er ferdig med å definere de konserninterne parameterne, lukker du siden **Konsernintern** for å gå tilbake til de valgte kundedetaljene.
1. Utvid hurtigfanen **Diverse detaljer**, og sett **Opprett konserninterne ordrer** til *Ja*. Hvis du også vil at ordrer skal leveres direkte til kunder, setter du **Direkte levering** til *Ja*.

    > [!NOTE]
    > Hvis det er noen varer som organisasjonen har på lager eller leverer til kunder, er det ikke sikkert at du vil opprette konserninterne ordrer automatisk, selv om du har varen på lager. Hvis du vil deaktivere den automatiske genereringen av ordrer for varer du noen ganger har på lager, setter du **Opprett konserninterne ordrer** til *Nei*.

1. Hvis du vil tillate at det opprettes ekstra linjer indirekte i en salgsordre, setter du **Opprett indirekte ordrelinjer** til *Ja*. Dette gjør at en bruker kan legge til linjer i den opprinnelige salgsordren fra den konserninterne salgsordren.

> [!WARNING]
> Hvis du tillater indirekte oppretting av ordrelinjer, tillater du alle anskaffelser i den opprinnelige salgsordren fra den konserninterne salgsordren. Hver anskaffelse sendes deretter til kunden og legges til i ordren og fakturaen. I tillegg skrives alle dokumenter som er involvert i salget, ut og posteres automatisk. Brukere blir ikke varslet om tillegget.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

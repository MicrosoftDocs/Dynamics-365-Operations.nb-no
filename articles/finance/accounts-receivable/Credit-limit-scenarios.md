---
title: Kredittgrensescenarioer
description: Denne artikkelen beskriver hvordan kundens kredittgrense blir kontrollert når kunden tilhører en kundekredittgrensegruppe.
author: JodiChristiansen
ms.date: 06/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-06-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 60b17a6b7f57b468610974ae9bd05b7db3584cc1
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130261"
---
# <a name="credit-limit-scenarios"></a>Kredittgrensescenarioer

I Kredittbehandling kan du tilordne en kredittgrense til kunder på kundenivå. Hver kunde kan tilordnes en *kundekredittgrensegruppe*, og hver gruppe har en kredittgrense. Derfor kan en kredittgrense også tilordnes til kunder på gruppenivå. Alle kunder som er tilordnet den samme kundekredittgruppen, har samme kredittgrense.

Generelt kontrolleres gruppekredittgrenser før individuelle kredittgrenser. Den enkelte kredittgrensen overstyrer ikke alltid gruppens kredittgrense.

Denne artikkelen beskriver fem scenarier som er knyttet til kundekredittgrupper og individuelle kredittgrenser.

## <a name="the-customer-group-credit-limit-is-more-than-the-individual-credit-limit"></a>Kredittgrensen for kundegruppen er mer enn den individuelle kredittgrensen

Kunden har for eksempel en individuell kredittgrense på USD 10 000. Kunden er tilordnet en kundekredittgruppe, og gruppens kredittgrense er USD 15 000. I dette tilfellet er kundens "effektive kredittgrense" på USD 10 000 fordi dette beløpet er mindre enn gruppegrensen. Blokkeringsregler kontrollerer først gruppegrensen. Deretter kontrollerer de grensen for enkeltpersoner. Alle salgsordrer over USD 10 000 blokkeres.

## <a name="the-individual-credit-limit-is-more-than-the-customer-group-credit-limit"></a>Kredittgrensen for enkeltpersoner er mer enn kundegruppekredittgrensen

Kunden har for eksempel en individuell kredittgrense på USD 20 000. Kunden er tilordnet en kundekredittgruppe, og gruppens kredittgrense er USD 15 000. I dette tilfellet er kundens effektive kredittgrense på USD 15 000, fordi blokkeringsreglene alltid kontrollerer gruppegrensen først. Alle salgsordrer over USD 15 000 blokkeres.

## <a name="the-individual-credit-limit-is-set-to-000-and-mandatory-credit-limit-is-set-to-yes"></a>Den individuelle kredittgrensen er satt til 0,00, og obligatorisk kredittgrense er satt til Ja

Hvis kunden har en individuell kredittgrense som er satt til **0,00**, og alternativet **Obligatorisk kredittgrense** er satt til **Ja**, er kundens effektive kredittgrense på USD 0,00, selv om kunden er tilordnet en kundekredittgruppe. På denne måten kan kunden være en del av en gruppe, men alle ordrene vil gå til Kredittbehandling.

## <a name="the-individual-credit-limit-is-set-to-000-and-unlimited-credit-limit-is-set-to-yes"></a>Den individuelle kredittgrensen er satt til 0,00, og Ubegrenset kredittgrense er satt til Ja

Hvis kunden har en individuell kredittgrense som er satt til **0,00**, med alternativet **Ubegrenset kredittgrense** er satt til **Ja**, vil kunden ha ubegrenset kreditt, selv om kunden er tilordnet en kundekredittgruppe.

## <a name="the-individual-credit-limit-is-set-to-000-and-the-customer-is-part-of-a-customer-credit-group"></a>Den individuelle kredittgrensen er satt til 0,00, og kunden er en del av en kundekredittgruppe

Kunden har for eksempel en individuell kredittgrense som er satt til **0,00**, alternativet **Ubegrenset kreditt** er satt til **Nei**, ogalternativet **Obligatorisk kredittgrense** er satt til **Nei**. Kunden er tilordnet en kundekredittgruppe, og gruppens kredittgrense er USD 15 000. I dette tilfellet er kundens gjeldende kredittgrense gruppens grense, på USD 15 000. Derfor blir alle salgsordrer over dette beløpet blokkert. Ved hjelp av denne virkemåten kan kredittgrensen behandles på kundekredittgruppenivå i stedet for på individuelt kundenivå. Alle kunder som er tilordnet den samme gruppen, har samme kredittgrense.

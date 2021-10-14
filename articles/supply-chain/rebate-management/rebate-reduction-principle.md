---
title: Prinsippene for rabattreduksjon
description: Dette emnet beskriver hvordan du setter opp reduksjonsprinsipper. Reduksjonsprinsipper styrer virkemåten når flere rabatter gjelder for den samme varen eller transaksjonen.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e6b178704fde18036d526e7a645cb9b4f8bd66c7
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579070"
---
# <a name="rebate-reduction-principles"></a>Prinsippene for rabattreduksjon

[!include [banner](../includes/banner.md)]

Du kan gruppere rabattbehandlingsavtaler i *reduksjonsprinsipper* for å redusere andre avsetninger som er knyttet til en vare, og/eller for å redusere de resulterende verdiene til rabattberegninger. Når prinsippene for rabattreduksjon er definert, kan du velge å tilordne dem til linjene i rabattbehandlingsavtalene dine, etter behov.

Reglene for rabattreduksjon gjelder bare når rabattavtaler overlapper. De kan derfor gi flere rabatter i situasjoner der du ikke er skyldig flere rabatter.

## <a name="manage-rebate-reduction-principles"></a>Administrer prinsipper for rabattreduksjon

Hvis du vil arbeide med prinsippene for rabattreduksjon, kan du gå til **Rabattbehandling \> Oppsett \> Prinsipper for rabattreduksjon**. Deretter kan du bruke knappene i handlingsruten til å legge til og fjerne reduksjonsprinsipper etter behov. For hvert prinsipp angir du feltene som beskrevet i følgende tabell.

| Felt | beskrivelse |
|---|---|
| Prinsipp for rabattreduksjon | Angi et unikt navn for rabattreduksjonsprinsippet. |
| beskrivelse | Angi en beskrivelse av rabattreduksjonsprinsippet. |
| Bruk reduksjon | Merk av i denne avmerkingsboksen for å bruke et reduksjonsgrunnlag for rabatter som tilhører dette rabattreduksjonsprinsippet. |
| Reduksjonsgrunnlag | Hvis du merket av for **Bruk reduksjon**, velger du reduksjonsgrunnlaget (*Avsetning*, *Rabatter* eller *Begge*). Hvis du velger *Begge*, og hvis både en avsetning og en rabatt er postert for en tidligere avtale, vil bare rabatten bli brukt. |
| Ekskluder fra reduksjon | Hvis det er merket av i denne avmerkingsboksen, vil avsetninger og rabatter som tilhører dette rabattreduksjonsprinsippet, utelates fra etterfølgende reduksjoner. Innstillingen i **Reduksjonsgrunnlag**-feltet gjelder ikke for denne innstillingen. |

## <a name="examples-of-rebate-reduction-principle-setups"></a>Eksempler på oppsett av rabattreduksjonsprinsipper

Tabellen nedenfor viser noen vanlige eksempler på oppsett av rabattreduksjonsprinsipper. For hvert av disse prinsippene for rabattreduksjon beskriver verdien i **Beskrivelse**-feltet formålet med rabattreduksjonsprinsippet.

| Prinsipp for rabattreduksjon | beskrivelse | Bruk reduksjon | Reduksjonsgrunnlag | Ekskluder fra reduksjon |
|---|---|---|---|---|
| Utsatt | Reduser rabatt | Ja | Begge | Ingen |
| Exclreb | Ekskluder rabatt | Ja | Rabatt | Ja |
| Flere | Flere rabatter | Ja | Begge | Ja |
| None | Bare avs. og rabatt | Ingen | Begge | Ja |
| Klargjør | Bare avsetning | Ja | Klargjør | Ingen |
| Rabatt | Bare rabatt | Ja | Rabatt | Ja |

## <a name="examples-of-rebate-reduction-principle-calculations"></a>Eksempler på beregninger av rabattreduksjonsprinsipper

Du har en salgsordre som har én enkelt salgsordrelinje. Denne linjen har en verdi på USD 1000. Følgende avtaler gjelder for ordren:

- **Avtale 1:** 10 prosent på USD 1000
- **Avtale 2:** 15 prosent på USD 1000
- **Avtale 3:** 20 prosent på USD 1000
- **Avtale 4:** 25 prosent på USD 1000

Behandlingsrekkefølgen er svært viktig. Behandlingsrekkefølgen er basert på måten du arbeider på, som beskrevet i [Behandle, gjennomgå og postere rabatter](process-review-post.md).

Følgende tabell oppsummerer for eksempel resultatet hvis du bruker rekkefølgen *1, 2, 3, 4*, og hvis du bare behandler avsetningene.

| Avtale | Beskrivelse og innstillinger | Avsetningsresultat |
|---|---|---|
| 1 | <p>Klassifiseringen kontrollerer ikke andre avtaler for reduksjoner. Kontrollen utføres for både avsetninger og rabatter.</p><ul><li>**Bruk reduksjon:** *Nei*</li><li>**Reduksjonsgrunnlag:** *Begge*</li><li>**Ekskluder fra reduksjon:** *Nei*</li></ul> | USD 1000 × 10 % = USD 100 |
| 2 | <p>Klassifiseringen kontrollerer andre avtaler for reduksjoner, men flagges slik at den selv ignoreres. Sjekken utføres bare for rabatter.</p><ul><li>**Bruk reduksjon:** *Ja*</li><li>**Reduksjonsgrunnlag:** *Rabatt*</li><li>**Ekskluder fra reduksjon:** *Ja*</li></ul> | USD 1000 × 15 % = USD 150 |
| 3 | <p>Klassifiseringen kontrollerer andre avtaler for reduksjoner. Kontrollen utføres for både avsetninger og rabatter.</p><ul><li>**Bruk reduksjon:** *Ja*</li><li>**Reduksjonsgrunnlag:** *Begge*</li><li>**Ekskluder fra reduksjon:** *Nei*</li></ul> | (USD 1000 – Avtale 1) × 20 % = USD 180 |
| 4 | <p>Klassifiseringen kontrollerer andre avtaler for reduksjoner. Kontrollen utføres for både avsetninger og rabatter.</p><ul><li>**Bruk reduksjon:** *Ja*</li><li>**Reduksjonsgrunnlag:** *Begge*</li><li>**Ekskluder fra reduksjon:** *Nei*</li></ul> | (USD 1000 – Avtale 1 – Avtale 3) × 25 % = USD 180 |

Følgende tabell viser noen eksempler der avsetningen behandles i ulike rekkefølger, og der ulike totaler derfor oppnås. Avviket i avsetningene avhenger av rekkefølgen systemet behandler avtalene i. Det er viktig at du forstår hvordan behandlingsrekkefølgen påvirker det endelige rabattbeløpet.

| Rekkefølge | Beregning |
|---|---|
| 1<br>(1, 2, 3, 4) | <ul><li>**Avtale 1:** USD 1000 × 10 % = USD 100</li><li>**Avtale 2:** USD 1000 × 15 % = USD 150</li><li>**Avtale 3:** (USD 1000 – Avtale 1) × 20 % = USD 180</li><li>**Avtale 4:** (USD 1000 – Avtale 1 – Avtale 2) × 25 % = USD 180</li><li>**Total avsetning:** USD 610</li></ul> |
| 2<br>(4, 3, 2, 1) | <ul><li>**Avtale 4:** USD 1000 x 25 % = USD 250</li><li>**Avtale 3:** (USD 1000 – Avtale 4) × 20 % = USD 150</li><li>**Avtale 2:** USD 1000 x 15 % = USD 150</li><li>**Avtale 1:** USD 1000 x 10 % = USD 100</li><li>**Total avsetning:** USD 650</li></ul> |
| 3<br>(3, 2, 1, 4) | <ul><li>**Avtale 3:** USD 1000 x 20 % = USD 200</li><li>**Avtale 2:** USD 1000 x 15 % = USD 150</li><li>**Avtale 1:** USD 1000 x 10 % = USD 100</li><li>**Avtale 4:** (USD 1000 – Avtale 3 – Avtale 1) × 25 % = USD 175</li><li>**Total avsetning:** USD 625</li></ul> |
| 4<br>(2, 4, 1, 3) | <ul><li>**Avtale 2:** USD 1000 × 15 % = USD 150</li><li>**Avtale 4:** USD 1000 × 25 % = USD 250</li><li>**Avtale 1:** USD 1000 × 10 % = USD 100</li><li>**Avtale 3:** (USD 1000 – Avtale 4 – Avtale 1) × 20 % = USD 130</li><li>**Total avsetning:** USD 630</li></ul> |

---
title: Oppsett for kostnadsparameterverdier
description: Når du konfigurerer modulen Netto innkjøpspris, kan du definere flere sett med fellesverdier som vil være tilgjengelige når du velger bestemte typer kostnadsparameterverdier i andre deler av appen. Dette emnet beskriver hvordan du konfigurerer disse settene med verdier.
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMCostTypeTable, ITMCostTypeGroup, ITMCostTransferGroup, ITMCostTemplateTable, ITMVolumetricDivisorTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 51c3360afc48f4f9143118ee6139803b95e5df28
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500484"
---
# <a name="costing-parameter-values-setup"></a>Oppsett for kostnadsparameterverdier

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Når du konfigurerer modulen **Netto innkjøpspris**, kan du definere flere sett med fellesverdier og tilknyttede innstillinger per verdi. Disse verdiene vil da være tilgjengelige når du velger bestemte typer kostnadsparameterverdier i andre deler av appen. Dette emnet beskriver hvordan du konfigurerer disse settene med verdier.

## <a name="set-up-cost-type-codes"></a>Definere kosttypekoder

Kosttypekoder bestemmer kosttypen som påløper når varene ankommer lageret, eller netto innkjøpspris for sjøreisen. Selv om de vanligvis øker verdien på varene, kan de også brukes til å avsette beløp i finans. Finansjusteringer brukes når en kostnad avsettes over tid eller under en serie med sjøreiser og motposteringer i én transaksjon.

> [!NOTE]
> Hvis kostnadstypetabellen deles på tvers av juridiske enheter, må kontoplanen også deles på tvers av juridiske enheter. Hvis ikke, fungerer ikke posteringstransaksjonene riktig.

Hvis du vil definere kosttypekoder, kan du gå til **Netto innkjøpspris \> Kontnadsoppsett \> Kosttypekoder**. Du kan bruke knappene i handlingsruten til å opprette nye kosttypekoder, redigere eksisterende koder eller slette en valgt kostnadstype.

Følgende tabell beskriver feltene som er tilgjengelige for hver kosttypekode.

| Felt | beskrivelse |
|---|---|
| Kosttypekode | Skriv inn et navn på kosttypekoden. |
| beskrivelse | Angi en beskrivelse av kosttypekoden. |
| Bruk forsendelsessats | Sett dette alternativet til *Ja* hvis valutakursen for sjøreise (noen ganger omtalt som en styringssats) må brukes til å beregne verdien av disse kostnadene. I dette tilfellet brukes forsendelsessatsen i stedet for standard eller vekslingskurs for utenlandske valutafakturaer. |
| Rapporteringskategori | Dette feltet etablerer en rapporteringskategori for kostnadstypen. Rapporter kan skrives ut enten ved hjelp av rapporteringskategorier eller etter kosttype. |
| Debettype | Velg om kostnadstypen skal debitere varen, finanskontoen eller leverandøren. |
| Debetpostering | Hvis feltet **Debettype** er satt til *Finanskonto*, velger du posteringsbeskrivelsen. |
| Debetkonto | Hvis feltet **Debettype** er satt til *Finanskonto*, velger du finanskontoen som skal brukes. |
| Kredittype | Velg om denne kostnadstypen skal kreditere varen, finanskontoen eller leverandøren. |
| Kreditpostering | Hvis feltet **Kreditttype** er satt til *Finanskonto*, velger du posteringsbeskrivelsen. |
| Kreditkonto | Hvis feltet **Kredittype** er satt til *Finanskonto*, velger du finanskontoen som skal brukes. |
| Avregningskonto | Velg avregningskontoen for kostnadstypen. Det anbefales at du angir en egen avregningskonto per kostnadstype for å få hjelp til avstemming. |
| Posteringstype for standardkostnad | Hvis du bruker standardkostnad, velger du posteringsbeskrivelsen. |
| Avvikskonto for standardkostnad | <p>Hvis du bruker standardkostnad, brukes kontoen som er angitt her, til å postere eventuelle avvik. Denne kontoen bruker oppdeling av landerte kostnader på siden **Varepriser**. Denne analysen opprettes ved å bruke den periodiske rutinen til å oppdatere priser.</p><p>Standardkostnaden for en vare er for eksempel 15,00 dollar, med FOB til 13,00 dollar og frakt på 2,00 dollar. Når fakturaen mottas for lageret, mottas varen ved 15,00 dollar, men det er et standard prisavvik på 2,00 dollar for varen ettersom den faktiske FOB-en er 13,00 dollar. Dette avviket posteres til standard prisavvikskonto som er definert i vareposteringsprofilen. Ettersom den estimerte frakten er 2,00 dollar, er det ingen avvik når lagerfakturaen posteres. Når fakturaen for frakt mottas, vil imidlertid frakten være 2,50 dollar per enhet. Derfor posteres det et avvik på 0,50 dollar til den angitte kostnaden. |
| Glidende gjennomsnitt for avvikskonto | <p>Hvis du bruker etterkalkuleringsmetoden for glidende gjennomsnitt, brukes kontoen som er angitt her, til å postere eventuelle avvik.</p><p>Den estimerte frakten vil for eksempel være 2,00 dollar. Når fakturaen for frakt mottas, vil imidlertid frakten være 2,50 dollar per enhet. Derfor må et avvik på 0,50 dollar posteres.</p><p>Når alternativet **Poster justeringer som avvik** er satt til *Ja* på siden **Parametere for netto innkjøpspris**, blir alle avvik mellom estimerte og reelle forsendelseskostnader postert til avvikskontoen for glidende gjennomsnitt som er angitt her. Når alternativet **Poster justeringer som avvik** er satt til *Nei*, brukes standardfunksjonaliteten, og avviket vil bli brukt på lageret eller på avvikskontoen for glidende gjennomsnitt som er angitt her, avhengig av lagerbeholdningen.</p> |
| Avsetningskonto for gebyr | Velg kontoen som brukes til å avsette for kostnadsestimater når innkjøpsfakturaen posteres. Dette feltet brukes bare når alternativet **Bruk avsetningskonto for avregning av kostnadstype** er satt til *Ja* i hurtigfanen **Etterkalkulering** i fanen **Generelt** på siden **Parametere for netto innkjøpspris**. |
| Gebyrkonto | Velg kontoen som brukes til å registrere innkommende transportkostnader som er fakturert av en leverandør. Beløpet blir postert som et debetbeløp. Motkontoen er lagervariasjonskontoen. Denne posteringen brukes bare når alternativet **Poster for belastning av konto i finans** er satt til *Ja* på siden **Leverandørparametere**. |
| Avvikskonto | Kontoen som skal brukes til å motpostere tilleggene når innkjøpsfakturaen posteres. Dette feltet brukes bare når alternativet **Bruk avsetningskonto for avregning av kostnadstype** er satt til *Ja* i hurtigfanen **Etterkalkulering** i fanen **Generelt** på siden **Parametere for netto innkjøpspris**. |

## <a name="vendor-cost-type-groups"></a>Kostnadstypegrupper for leverandør

Kosttypegrupper for leverandør hjelper deg med å fastslå hvordan avregninger for *automatisk kostnad* blir funnet og brukt på en sjøreise. Leverandører som har lignende importkostnader, er koblet sammen. Alle leverandører fra fremvoksende markeder betaler for eksempel samme avgiftsprosent for samme type produkt som kjøpes fra et etablert marked.

Du kan vedlikeholde kosttypegrupper for leverandør ved å gå til **Netto innkjøpspris \> Kostnadsoppsett \> Kosttypegrupper for leverandør**. Siden **Kosttypegrupper for leverandør** inneholder et rutenett som viser alle eksisterende kosttypegrupper for leverandør. Du kan bruke knappene i handlingsruten til å legge til, fjerne og redigere rader i rutenettet.

Følgende tabell beskriver feltene som er tilgjengelige på hver rad i rutenettet.

| Felt | beskrivelse |
|---|---|
| Kostnadstypegrupper for leverandør | Angi et unikt navn for kosttypegruppen for leverandør (for eksempel *Fremvoksende markeder*). |
| beskrivelse | Angi en beskrivelse av kosttypegruppen for leverandør. Denne beskrivelsen kan gi detaljer om nivået eller typen tillegg som er knyttet til leverandørgruppen. |

## <a name="item-cost-type-groups"></a>Kostnadstypegrupper for vare

Kosttypegrupper for vare hjelper deg med å fastslå hvordan avregninger for *automatisk kostnad* blir funnet og brukt på en sjøreise. Like varer er koblet sammen. Alle varer som for eksempel har en avgiftssats på 5 prosent, tilhører en bestemt kosttypegruppe.

Du kan vedlikeholde kosttypegrupper for vare ved å gå til **Netto innkjøpspris \> Kostnadsoppsett \> Kosttypegrupper for vare**. Siden **Kosttypegrupper for vare** inneholder et rutenett som viser alle eksisterende kosttypegrupper for vare. Du kan bruke knappene i handlingsruten til å legge til, fjerne og redigere rader i rutenettet.

Følgende tabell beskriver feltene som er tilgjengelige på hver rad i rutenettet.

| Felt | beskrivelse |
|---|---|
| Kostnadstypegrupper for vare | Angi et unikt navn for kosttypegruppen for vare (for eksempel *Toll på 5 %*). |
| beskrivelse | Angi en beskrivelse av kosttypegruppen for vare. Denne beskrivelsen kan gi detaljer om nivået eller typen tillegg som er knyttet til varegruppen. |

> [!NOTE]
> Varekosttypen er knyttet til varen via feltet **Kosttypegruppe** i hurtigfanen **Innkjøp** på siden **Frigitt produkt** for varen.

## <a name="transfer-order-cost-type-groups"></a>Kosttypegrupper for overføringsordre

Kosttypegrupper for overføringsordre hjelper deg med å fastslå hvordan avregninger for *automatisk kostnad* blir funnet. Like varer er koblet sammen. Alle varer som for eksempel har en avgiftssats på 7 prosent, tilhører en bestemt kosttypegruppe.

Du kan vedlikeholde kosttypegrupper for overføringsordre ved å gå til **Netto innkjøpspris \> Kostnadsoppsett \> Kosttypegrupper for overføringsordre**. Siden **Kosttypegrupper for overføringsordre** inneholder et rutenett som viser alle eksisterende kosttypegrupper for overføringsordre. Du kan bruke knappene i handlingsruten til å legge til, fjerne og redigere rader i rutenettet.

Følgende tabell beskriver innstillingene som er tilgjengelige på hver rad i rutenettet.

| Felt | beskrivelse |
|---|---|
| Kosttypegrupper for overføringsordre | Angi et unikt navn for kosttypegruppen for overføringsordre (for eksempel *Toll på 7 %*). |
| beskrivelse | Angi en beskrivelse av kosttypegruppen for overføringsordre. Denne beskrivelsen kan gi detaljer om nivået eller typen tillegg som er knyttet til kosttypegruppen for overføringsordre. |

> [!NOTE]
> Kosttypen for overføringsordre er knyttet til varen via feltet **Kostgruppe for overføringsordre** i hurtigfanen **Innkjøp** på siden **Frigitt produkt** for varen.

## <a name="cost-templates"></a>Kostnadsmaler

Du bruker kostnadsmaler til å definere standardverdier for innstillinger som brukere som får et kostnadsestimat, kanskje ikke kjenner til. Kostnadsmaler kan bidra til å redusere kompleksiteten i estimeringsprosessen ved å minimere valgene brukerne må gjøre for å få et nøyaktig estimat.

Hvis du vil arbeide med kostnadsmaler, kan du gå til **Netto innkjøpspris \> Kostnadsoppsett \> Kostnadsmaler**. På siden **Kostnadsmaler** viser listen til venstre alle gjeldende kostnadsmaler. Du kan bruke knappene i handlingsruten til å legge til, fjerne og redigere maler.

Følgende tabell beskriver innstillingene som er tilgjengelige for hver mal.

| Felt | beskrivelse |
|---|---|
| Kostnadsmal | Angi et unikt navn for kostnadsmalen. Navnet beskriver vanligvis faktoren eller kostnadsmultiplikatoren for malen. |
| beskrivelse | Angi en beskrivelse av kostnadsmalen. |
| Forsendelsesfirma | Velg leverandørkontoen til forsendelsesfirmaet som skal knyttes til kostnadsmalen. |
| Leveringsmiddel | Velg leveringsmåten som kostnadsmalen skal bruke når den estimerte kostnaden for en vare beregnes. Dette feltet vil være med på å bestemme de automatiske kostnadene som er knyttet til varene i forhåndsberegningen. |
| Fraktcontainertype | Velg typen forsendelsecontainer som skal knyttes til kostnadsmalen. Dette feltet vil være med på å bestemme de automatiske kostnadene som er knyttet til varene i forhåndsberegningen. |
| Tollmegler | Velg tollmekleren (leverandøren) som skal knyttes til kostnadsmalen. Dette feltet vil være med på å bestemme de automatiske kostnadene som er knyttet til kostnadsestimatet. |
| Omregningsfaktor | Angi en faktor som skal brukes for det endelige kostnadsestimatet for varer. Hvis du for eksempel vil legge til 10 prosent i det beregnede kostnadsestimatet, skriver du inn *1,10*. |

## <a name="volumetric-divisors"></a>Volumetriske divisorer

Volumetriske divisorer brukes til å beregne den volumetriske vekten. Hvert forsendelses-/fraktfirma formulerer sine egne volumetriske divisorer. I tillegg varierer et firmas divisorer vanligvis, avhengig av leveringsmåten. Luft- og sjøtransport har for eksempel svært forskjellige divisorer. Et firma kan også gjøre reglene mer komplekse, avhengig av hvor varer sendes fra.

En pakke som sendes med fly, har for eksempel et volum på 3 kubikkmeter (m³). Firmaet avregner etter volumetrisk vekt og bruker en volumetrisk divisor på 6. Denne divisoren multipliseres med volumet for å bestemme volumvekten. Derfor er volumvekten for dette eksemplet 3 × 6 = 18 kilo (kg).

Hvis du vil definere volumetriske divisorer, kan du gå til **Netto innkjøpspris \> Kontnadsoppsett \> Volumetriske divisorer**. Siden **Volumetriske divisorer** viser et rutenett med alle eksisterende volumetriske divisorer. Du kan bruke knappene i handlingsruten til å legge til, fjerne og redigere rader i rutenettet.

Følgende tabell beskriver feltene som er tilgjengelige på hver rad i rutenettet.

| Felt | beskrivelse |
|---|---|
| Forsendelsesfirma | Velg leverandørkontoen for forsendelsesfirmaet som er knyttet til den volumetriske divisoren. |
| Kosttypekode | Velg kosttypekoden som er knyttet til den volumetriske divisoren. Bruk dette feltet til å plassere kosttyper i rapporteringsperioder. Rapporter kan skrives ut enten ved hjelp av rapporteringskategorier eller etter kosttype. |
| Fra-havn | Velg fra-havnen som den volumetriske divisoren gjelder for. |
| Volumetrisk divisor | Angi verdien for den volumetriske divisoren som gjelder for raden. Verdien du angir, *multipliseres* med volumet i hver pakke for å fastslå emballasjens volumetriske vekt. |

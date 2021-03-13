---
title: Simulere kostprissendinger ved hjelp av en kostnadsberegningsversjon for planlagte kostnader
description: Denne artikkelen beskriver hvordan du kan simulere virkningen av kostnadsendringer på beregningen av kostpris for en produsert vare med en egen kostnadsberegningsversjon for planlagt kostpris.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 78183
ms.assetid: 1e41953f-cdb9-4598-b776-46e49383a773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 053709cb7a4ffb30e1e4968096ea4df5e67242e5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011828"
---
# <a name="simulate-cost-changes-by-using-a-costing-version-for-planned-costs"></a>Simulere kostprissendinger ved hjelp av en kostnadsberegningsversjon for planlagte kostnader

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du kan simulere virkningen av kostnadsendringer på beregningen av kostpris for en produsert vare med en egen kostnadsberegningsversjon for planlagt kostpris.

Du kan simulere virkningen av kostnadsendringer på beregningen av kostpris for en produsert vare med en egen kostnadsberegningsversjon for planlagt kostpris. Bruk denne separate kostnadsberegningsversjonen til å angi uavsluttede kostprisposter som gjenspeiler inkrementelle kostprisendringer, og til å beregne kostprisenes innvirkning på produserte varer. Siden tilbakefallsprinsippet for aktive kostnader vil bli brukt i stykklisteberegningene, må bare de inkrementelle kostprisendringene angis.

## <a name="guidelines-for-defining-the-simulation-costing-version"></a>Retningslinjer for å definere kostnadsberegningsversjonen for simuleringen
Bruk retningslinjene nedenfor når du definerer kostnadsberegningsversjonen for simuleringer:

-   Tilordne en kostnadsberegningstype for **planlagte kostnader**.
-   Tilordne en meningsfull identifikator for kostnadsberegningsversjonen, for eksempel **Simulering**.
-   Kontroller at innholdet omfatter kostprisposter.
-   Tillat innlegging av kostprisposter. Ikke sperr for innlegging av uavsluttede kostpriser.
-   Tillat innlegging av kostprisposter for alle områder. Hvis du angir et område, vil innlegging av kostprisposter begrenses til det angitte området.
-   Forhindre aktiveringen av uavsluttede kostpriser. Bare uavsluttede kostpriser må legges inn for kostprisposter i kostnadsberegningsversjonen for simulering.
-   Ikke angi noen fra-dato. Det vil bli angitt en beregningsdato for hver stykklisteberegning som bruker kostnadsberegningsversjonen for simulering.
-   Angi et tilbakefallsprinsipp for **Gjeldende aktiv**. Tilbakefallsprinsippet gjør det mulig å angi inkrementelle kostprisendringer for simuleringsformål, samtidig som gjeldende aktive kostpris brukes som kilde for alle andre kostprisposter. Vi antar at alle gjeldende aktive kostpriser finnes for alle andre kostprisposter.
-   Angi en kostprismodell av **versjonskostprisen**, men ikke begrens beregningene. Simuleringene kan for eksempel også bruke en kostprismodell for **stykklisteberegningsgruppe** til å angi kilden av kostbidragsdata for innkjøpte elementer.
-   Angi nedbrytingsmodusen **Flere nivåer**, men ikke begrens beregningene. Simuleringene kan bruke andre nedbrytingsmoduser.

## <a name="costing-versions"></a>Etterkalkuleringsversjoner
Scenariene nedenfor viser hvordan kostversjonen for simulering brukes til å simulere virkningen av kostprisendringer. Før du angir en simulert kostprisendring, sletter du uavsluttede kostprisposter i kostversjonen for simulering, slik at du har et rent utgangspunkt. Bruk siden **Varepris** til å vise og slette uavsluttede kostprisposter som er knyttet til varepriser og kostpriskategoripriser.

-   Simuler kostprisendringer for en innkjøpt vare. Kostprisendringen kan for eksempel gjenspeile en forventet økning eller reduksjon i kostprisen for viktige innkjøpte materialer. Definer den endrede kostprisen for en innkjøpte vare ved å angi en uavsluttet kostprispost i kostnadsberegningsversjonen for simulering på siden **Varepris**.
-   Simuler kostnadsendringer for en kostpriskategori. Kostprisendringen kan for eksempel gjenspeile en forventet økning eller reduksjon i utgiftene til arbeidskraft, eller i timeprisene for operasjonsressurs. Definer den endrede beregningsformelen for indirekte kostnader ved å angi en uavsluttet kostprispost i kostnadsberegningsversjonen for simulering på siden **Kostnadskategoripris**.
-   Simuler kostprisendringen i en beregningsformel for indirekte kostnader. Kostprisendringen kan for eksempel gjenspeile en forventet økning eller reduksjon i de generelle administrasjonskostnadene for produksjon. Definer den endrede beregningsformelen for indirekte kostnader ved å angi en uavsluttet kostnadspost i kostnadsberegningsversjonen for simulering på siden **Oppsett av kostark**, hvor du også validerer og lagrer endringen.

Når du har angitt de simulerte kostprisendringene, beregner du kostprisen for produserte varer som påvirkes av kostprisendringene. Bruk **Beregning**-siden for kostnadsberegningsversjonen for simulering, og identifiser de valgte produserte varene som vil bli påvirket av kostprisendringene. Stykklisteberegningene vil gjelde alle produserte varer hvis du ikke velger bestemte varer. Du kan også bruke alternativet for stykklisteberegning for brukssted. Vis varekostprispostene i kostnadsberegningsversjonen for simulering for å analysere hvordan de simulerte kostprisendringene påvirket kostprisen for de valgte produserte varene. Bruk sidene **Varepris** og **Beregn varekostnad** for å vise og analysere kostnadene.




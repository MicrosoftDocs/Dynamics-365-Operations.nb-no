---
title: Prissimulering
description: Denne artikkelen inneholder informasjon om prissimulering for tilbud. Prissimulering hjelper deg med å vurdere effekten av fradrag på den fremtidige salgsprisen under tilbudsprosessen, før du fastsetter en bestemt pris.
author: omulvad
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationPriceSimulation, SalesQuotationsTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 12254
ms.assetid: 92be7c85-73cf-4f77-833c-d37ce779a031
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 354b6c769c86934489924a6c56734695307cfb70
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830628"
---
# <a name="price-simulation"></a>Prissimulering

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om prissimulering for tilbud. Prissimulering hjelper deg med å vurdere effekten av fradrag på den fremtidige salgsprisen under tilbudsprosessen, før du fastsetter en bestemt pris.

En prissimulering for et tilbud viser et nytt totalbeløp basert på en nytt prisforslag. En prissimulering kan også vise et nytt beløp for en bestemt linje som er opprettet i et eksisterende tilbud. Du kan angi en prissimulering og bruke den senere. Du kan alternativt bruke det opprinnelige tilbudet uten en prissimulering og gjøre ytterlige endringer mens du går gjennom salgsprosessen med kunden.  

En prissimulering endrer ikke prisen i tilbudet. Hvis prissimuleringen brukes på hele tilbudet, behandles den som en spesialrabatt i tilbudshodet. Hvis prissimuleringen brukes på bestemte varer, behandles den som en spesialrabatt i tilbudslinjene. Enhetssalgsprisen på tilbudslinjen som opprettes, endres ikke når prissimuleringen brukes. I stedet brukes det en rabattprosent som tilsvarer prisreduksjonen i tilbudslinjen. Når en prissimuleringen brukes, overføres enhetssalgsprisen og rabattprosenten til tilbudslinjen eller tilbudshodet.  

>Obs! Når du kjører en prissimulering, brukes bare gjeldende salgsvaluta til å opprette simuleringen. Når du viser totalbeløpene for tilbudet, vises det imidlertid en blanding av firmaets valuta og salgsvaluta.  

Tilleggsvarer som legges til tilbudslinjene, kan utløse linjerabatter eller samkjøpsrabatter. De kan også utløse sluttrabatter som endrer dekningsbidragene og dekningsgradene til tilbudslinjene og hele rabatten.  

Du kan kjøre flere prissimuleringer samtidig for å spore virkningen av prisendringer på målene for et tilbud. Ved å kjøre disse simuleringene kan du endre den samlede prisen i tilbudet eller prisen på en eller flere bestemte linjer i tilbudet. Deretter kan du bruke prissimuleringen som kan bidra mest til å få salget i boks.  

Når du oppretter et tilbud, kan du definere et varsel. Her er noen av måtene varsler kan brukes:

-   De kan holde deg informert om statusen for tilbud i organisasjonen.
-   De kan utløse en gjennomgang av et bestemt tilbud eller informere deg når rabattgrenser overskrides.

## <a name="price-simulation-and-discounts"></a>Prissimulering og rabatter
For å sikre at rabatter og priser beregnes på riktig måte, må du være forsiktig når du kjører prissimuleringer på tilbud med rabatter. Fordi alle prissimuleringer behandles som spesialrabatter på den aktive tilbudslinjen eller hele tilbudet, er det viktig å spore forskjellene i rabattene.

### <a name="types-of-discounts-in-trade-agreements"></a>Rabattypene i forretningsavtaler

Forretningsavtalene i Supply Chain Management kan ha fire typer prisrabatter. Disse rabattene kan defineres for ulike varer, kunder eller prisgrupper, og kan begrenses etter dato. Hvis du vil unngå feilberegninger, må du vurdere forretningsavtaler når du kjører prissimuleringer. Her er fire rabattypene i forretningsavtaler:

-   **Salgspris** – Separate salgspriser kan angis for varer. Når det opprettes tilbudslinjer, søker programmet etter den riktige salgsprisen for en vare, og overfører den til tilbudslinjene. Derfor påvirkes ikke en forretningsavtale med denne typen rabatt, prissimuleringen. Salgsprisen som brukes i tilbudslinjen, reflekterer forretningsavtalen.
-   **Linjerabatt** – Spesialrabatter angis for varer, avhengig av antallet som er bestilt. Linjebeløp reduseres typisk av linjerabatten før det kjøres en prissimulering. Derfor påvirkes en forretningsavtale med denne typen rabatt, prissimuleringen.
-   **Samkjøpsrabatt** – Hvis de kombinerte antallene overskrider grensen du har definert, vil forhåndsdefinerte kombinasjoner av bestilte varer utløse en rabatt på hele ordren. Linjebeløp reduseres typisk av linjerabatten før det kjøres en prissimulering. Derfor påvirkes en forretningsavtale med denne typen rabatt, prissimuleringen.
-   **Sluttrabatt** – Hvis de kombinerte beløpene overskrider grensen du har definert, vil forhåndsdefinerte bestilte varer utløse en rabatt på hele ordren. Totalrabatten genereres av tilbudslinjene. Fordi den samlede rabatten brukes i tilbudstotalen som en rabatt, kan det imidlertid reduserer det totale beløpet for tilbudet. Derfor påvirkes en forretningsavtale med denne typen rabatt, prissimuleringen.

### <a name="quotation-lines-and-trade-agreements"></a>Tilbudslinjer og forretningsavtaler

Når du oppretter eller justerer en tilbudslinje, beregnes linjerabatter automatisk. Den relevante salgsprisen blir funnet for varen, basert på forretningsavtalen.

## <a name="price-simulation-examples"></a>Eksempler på prissimulering
Følgende eksempler bruker prissimulering for tilbudshoder og enkeltlinjevarer.

### <a name="price-simulation-for-quotation-headers"></a>Prissimulering for tilbudshoder

Du oppretter et tilbud som har følgende linjer:

-   10 enheter av varen BR-12 (kostpris per enhet: USD 9,52, og salgspris per enhet: USD 15,32)
-   12 enheter av varen BR-14 (kostpris per enhet: USD 7,48, og salgspris per enhet: USD 13,75)

Tabellen nedenfor viser tilbudslinjene.

|                            | Beregning                          | Resultat   |
|----------------------------|--------------------------------------|----------|
| Salgsantall             | 10 enheter + 12 enheter                  | 22 enheter |
| Salgsverdi i USD         | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Kostverdi i USD          | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Dekningsbidrag i USD | 318,20 – 184,96                      | 133,24   |
| Dekningsgrad         | (\[318,20 – 184,96\] ÷ 318,20) × 100 | 41,87 %   |

Du kjører en prissimulasjon og bruker 15 prosent sluttrabatt for hele tilbudet eller tilbudshodet. Tabellen nedenfor viser de nye totalsummene for tilbudet etter at prissimuleringen er kjørt.

|                                                      | Beregning                               | Resultat   |
|------------------------------------------------------|-------------------------------------------|----------|
| Salgsantall                                       | 10 enheter + 12 enheter                       | 22 enheter |
| Gammel salgsverdi i USD                               | (10 × 15,32) + (12 × 13,75)               | 318,20   |
| Gammel kostverdi i USD                                | (10 × 9,52) + (12 × 7,48)                 | 184,96   |
| Gammelt dekningsbidrag i USD                       | 318,20 – 184,96                           | 133,24   |
| Gammel dekningsgrad                               | (\[318,20 – (10 × 9,52)\] ÷ 318,20) × 100 | 41,87 %   |
| Prissimulering av 15 % totalrabatt i USD | (15 × 318,2) ÷ 100                        | 47,73    |
| Ny salgsverdi i USD                               | 318,20 – 47,73                            | 270,47   |
| Nytt dekningsbidrag i USD                       | 270,47 – 184,96                           | 85,51    |
| Nytt dekningsbidrag                               | \[(270,47 – 184,96) ÷ 270,47\] × 100      | 31,61 %   |

### <a name="price-simulation-for-single-line-items"></a>Prissimulering for enkeltlinjevarer

Du oppretter et tilbud som har følgende linjer:

-   10 enheter av varen BR-12 (kostpris per enhet: USD 9,52, og salgspris per enhet: USD 15,32)
-   12 enheter av varen BR-14 (kostpris per enhet: USD 7,48, og salgspris per enhet: USD 13,75)

Tabellen nedenfor viser tilbudslinjene.

|                                      | Beregning                          | Resultat   |
|--------------------------------------|--------------------------------------|----------|
| Salgsantall                       | 10 enheter + 12 enheter                  | 22 enheter |
| Salgsverdi i USD for BR-12         | 10 × 15,32                           | 153,20   |
| Salgsverdi i USD for BR-14         | 12 × 13,75                           | 165,00   |
| Kostverdi i USD for BR-12          | 10 × 9,52                            | 95,20    |
| Kostverdi i USD for BR-14          | 12 × 7,48                            | 89,76    |
| Dekningsbidrag i USD for BR-12 | 153,20 – 95,20                       | 58,00    |
| Dekningsbidrag i USD for BR-14 | 165,00 – 89,76                       | 75,24    |
| Dekningsgrad i USD for BR-12  | \[(153,20 – 95,20) ÷ 153,20\] × 100  | 37,86    |
| Dekningsgrad i USD for BR-14  | \[(165,00 – 89,76) ÷ 165,00\] × 100  | 45,60    |
| Total salgsverdi i USD             | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Total kostverdi i USD              | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Totalt dekningsbidrag i USD     | 318,20 – 184,96                      | 133,24   |
| Total dekningsgrad             | \[(318,20 – 184,96) ÷ 318,20\] × 100 | 41,87 %   |

Du kjører en prissimulering og bruker en sluttrabatt på 10 prosent på BR-12-enhetene. Tabellen nedenfor viser de nye totalsummene for tilbudet etter at prissimuleringen er kjørt for enkeltlinjevaren.

|                                                   | Beregning                             | Resultat   |
|---------------------------------------------------|-----------------------------------------|----------|
| Salgsantall                                    | 10 enheter + 12 enheter                     | 22 enheter |
| Gammel salgsverdi i USD for BR-12                  | 10 × 15,32                              | 153,20   |
| Prissimulering av 10 % rabatt for BR-12 | (10 × 153,2) ÷ 100                      | 15,32    |
| Ny salgsverdi i USD for BR-12                  | (10 × 15,32) – 15,32                    | 137,88   |
| Salgsverdi i USD for BR-14                      | 12 × 13,75                              | 165,00   |
| Kostverdi i USD for BR-12                       | 10 × 9,52                               | 95,20    |
| Kostverdi i USD for BR-14                       | 12 × 7,48                               | 89,76    |
| Nytt dekningsbidrag i USD for BR-12          | 137,88 – 95,20                          | 42,68    |
| Dekningsbidrag i USD for BR-14              | 165,00 – 89,76                          | 75,24    |
| Ny dekningsgrad i USD for BR-12           | \[(137,88 – 95,20) ÷ 137,88\] × 100     | 30,95    |
| Dekningsgrad i USD for BR-14               | \[(165,00 – 89,76) ÷ 165,00\] × 100     | 45,60    |
| Ny total salgsverdi i USD                      | \[(10 × 15,32) – 15,32\] + (12 × 13,75) | 302,88   |
| Total kostverdi i USD                           | (10 × 9,52) + (12 × 7,48)               | 184,96   |
| Nytt totalt dekningsbidrag i USD              | 302,88 – 184,96                         | 117,92   |
| Nytt totalt dekningsbidrag                      | \[(302,88 – 184,96) ÷ 302,88\] × 100    | 38,93 %   |

Prissimuleringen påvirker bare linjen der den brukes, og reduserer totalsummen for denne linjen.




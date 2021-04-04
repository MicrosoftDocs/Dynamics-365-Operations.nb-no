---
title: Legge til kredittbehandlingsinformasjon for kunder
description: Dette emnet beskriver hvordan du legger til informasjon om kredittbehandling for en kunde.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 13ea8c2600e93379c9e3c71b97b919cbbca3b5eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257710"
---
# <a name="add-credit-management-information-for-customers"></a>Legge til kredittbehandlingsinformasjon for kunder

[!include [banner](../includes/banner.md)]

Når du har definert parameterne som styrer kredittbehandlingen, kan du legge til flere detaljer for hver kunde. Denne informasjonen styrer kredittbehandlingsprosessene, og inneholder også tilleggsinformasjon som hjelper medlemmer i innkrevingsteamet med å håndtere kunder.

## <a name="customer-information"></a>Kundeopplysninger

Du kan legge til kundedetaljer i hurtigfanen **Kreditt og innkreving** på **Alle kunder**-siden (**Kunder \> Kunder \> Alle kunder**).

1. Sett alternativet **Ubegrenset kredittgrense** til **Ja** hvis kunden ikke skal være begrenset av noen kredittgrensetester.
2. Sett alternativet **Utelat fra kredittbehandling** til **Ja** for å utelate kunden fra handlinger som vanligvis skjer under kredittbehandlingsprosesser.
3. Velg gruppen for kredittbehandling for kunden.
4. Hvis du vil beregne kredittgrensen i kundens valuta, angir du kundens kredittgrense i feltet **Kredittgrense i kundens valuta**. Kredittgrensen i firmavalutaen konverteres ved hjelp av valutakursene som er definert av valutakurstypen for kredittgrense som er valgt i parameterne for kredittbehandling.
5. I feltet **Siste gjennomgangsdato** angir du datoen da kundens kredittgrense sist ble vurdert av en kredittleder.
6. I feltet **Neste planlagte gjennomgangsdato** angir du datoen da det er planlagt kredittgjennomgang og -oppdatering for kunden.
7. I feltet **Kvalifisert kredittgrense** angir du den høyeste kredittgrensen som kan tilordnes til kunden, basert på din gjennomgang av kundens kreditthistorie. Den kvalifiserte kredittgrensen kan variere fra kredittgrensen som vises i hurtigfanen **Kreditt og innkreving**.
8. I feltet **Valuta for kvalifisert kredittgrense** angir du valutaen for den kvalifiserte kredittgrensen.
9. I feltet **Dato for kvalifisert kredittgrense** angir du datoen da den kvalifiserte kredittgrensen ble opprettet.
10. I feltet **Kredittkontostatus** angir du kredittkontostatusen for kunden.
11. I **Statusårsak**-feltet angir du årsaken som er knyttet til kontostatusen.
12. Sett alternativet **Med byrå** til **Ja** for å angi at kunden for øyeblikket er tilordnet til et kredittbyrå. Denne verdien er bare til informasjon. Den brukes ikke i noen kredittbehandlingsprosesser.
13. Sett alternativet **Tittel** til **Ja** for å angi at en tittel innehas for firmaet. Denne verdien er bare til informasjon. Den brukes ikke i noen kredittbehandlingsprosess.
14. I feltet **Dato for virksomhet startet** angir du datoen da kunden begynte å gjøre forretninger første gang. Denne informasjonen brukes når det opprettes risikopoeng.
15. I feltet **Kunden siden** angir du datoen da de første transaksjonene ble behandlet for kunden. Denne informasjonen brukes når det opprettes risikopoeng.
16. Angi merknader som kreditteamet kan bruke til å vurdere kundens kredittverdighet ytterligere.

Legg merke til at noe av informasjonen som vises på **Kunde**-siden, er opprettet i en annen prosess:

- Feltet **Utløpsdato for kredittgrense** viser datoen da kredittgrensen utløper. Hvis du ikke angir dette feltet, vil ikke kundens kredittgrense utløpe.
- Feltet **Dato for kredittgrense** viser datoen da kredittgrensen ble opprettet. Dette feltet oppdateres hver gang kredittgrensen justeres.
- Midlertidige kredittgrenser overstyrer kundekredittgrensen for en periode. De brukes i stedet for kredittgrensen for å beregne den totale kredittgrensen. Denne informasjonen vises bare hvis det finnes en aktiv kredittgrense. Du kan legge til midlertidige kredittgrenser gjennom kredittgrensejusteringer.
- Feltet **Forsikring og garantier** viser den totale verdien for forsikringer og garantier som kan øke kredittgrensen for kunden.
- Feltet **Total kredittgrense** viser den endelige kredittgrensen for kunden. Den totale kredittgrensen omfatter forsikring og garantier og midlertidige kredittgrenser.

## <a name="temporary-credit-limits"></a>Midlertidige kredittgrenser

Midlertidige kredittgrenser overstyrer kundekredittgrenser for en definert periode. Du kan legge til midlertidige kredittgrenser ved hjelp av kredittgrensejusteringer. Kredittgrensejusteringer lar kredittledere oppdatere kredittgrensene og utløpsdatoene for en enkelt kunde, en gruppe kunder eller alle kunder via en posteringsprosess.

Du kan opprette oppføringer for kredittgrensejusteringer på siden **Kredittgrensejusteringer** (**Kredittbehandling \> Kredittgrensejusteringer \> Kredittgrensejusteringer**).

## <a name="create-insurance-policies-and-guarantees"></a>Opprette forsikringspoliser og garantier

Du kan opprette én eller flere forsikringspoliser og garantier for hver kunde. Deretter kan du bruke dem til å beregne eksponeringen som firmaet har når det tilbyr kreditt til en kunde. Forsikringspoliser og garantier kan også inkluderes i kredittgrensen for en kunde.

Du kan opprette forsikringspoliser og garantier på **Alle kunder**-siden (**Kunder \> Kunder \> Alle kunder**). Velg en kunde, og gå deretter til handlingsruten, kategorien **Kredittbehandling**, og velg **Forsikring og garantier**.

> [!NOTE]
> I fremgangsmåten nedenfor velger du en forsikringsgiver eller garantist fra den globale adresseboken. Før du begynner på denne prosedyren må du derfor sørge for at forsikringsgiverne og garantistene er lagt til i den globale adresseboken,

1. I feltet **Identifikator** angir du **Garanti** eller **Forsikring**.
2. I feltet **Garanti-/forsikringstype** velger du en av garanti- eller forsikringstypene du tidligere har definert.
3. I feltet **Forsikringsgiver/garantist** velger du forsikringsgiveren eller garantisten fra den globale adresseboken. 
4. Hvis du valgte **Forsikring** i feltet **Identifikator**, i feltet **Polisedekningstype** velger du én av dekningstypene du har definert tidligere. Du kan ikke velge en polisedekningstype for en garanti.
5. I **Identifikasjon**-feltet angir du ID-en til polisen. Denne ID-en er vanligvis et polisenummer.
6. Angi startdatoen for forsikringspolisen eller garantien i **Gyldig**-feltet.
7. Angi datoen da forsikringspolisen eller garantien utløper i **Utløp**-feltet. utløper.
8. Angi verdien for forsikringspolisen eller garantien i **Verdi**-feltet. Denne verdien er den fullstendige verdien for polisen.
9. Velg valutaen for poliseverdien i **Valuta**-feltet. 
10. I feltet **Oppdater kredittgrense** angir du en prosentverdi mellom **0** og **100**. Denne prosenten vil bli brukt på poliseverdien, og det resulterende beløpet blir brukt til å øke kredittgrensen som brukes i kredittgrenseberegninger. Den beregnede verdien vises under **Total kredittgrense, forsikring og garantier** på hurtigfanen **Kreditt og innkreving** på **Kunder**-siden.

    Her er et eksempel:

    - Kredittgrensen (A) er 100 000.
    - Poliseverdien (B) er 50 000.
    - **Oppdater kredittgrense**-prosenten (C) er 50,00.
    
    I dette tilfellet er den effektive kredittgrensen 125 000 (= A + \[B × C\]).

11. Merk av for **Inkludert i eksponering** for å redusere kredittgrensen som brukes i kredittgrenseberegninger etter den fullstendige verdien av polisen. Hvis det er merket av i denne avmerkingsboksen, vil verdien som beregnes når **Oppdater kredittgrense**-prosenten er angitt, ikke brukes i kredittgrenseberegninger.

    Her er et eksempel:

    - Kredittgrensen (A) er 100 000.
    - Poliseverdien (B) er 50 000.
    - **Oppdater kredittgrense**-prosenten (C) er 50,00.

    I dette tilfellet er den effektive kredittgrensen 125 000 (= A + \[B × C\]).
    
    Hvis du imidlertid merker av for **Inkludert i eksponering**, fjernes **Oppdater kredittgrense**-verdien på 50 000 (= 50,00 prosent av 100 000), og eksponeringsverdien er 75 000 (= A + \[B × C\] – B).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Kundeemne til kontanter i dobbel skriving
description: Denne artikkelen inneholder informasjon om kundeemne til kontanter i dobbel skriving.
author: RamaKrishnamoorthy
ms.date: 01/07/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: f0d5339190f7e2aff7b084fa73e559af28e10ee8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860116"
---
# <a name="prospect-to-cash-in-dual-write"></a>Kundeemne til kontanter i dobbel skriving

[!include [banner](../../includes/banner.md)]

Et viktig mål for de fleste bedrifter er å konvertere kundeemner til kunder, og deretter opprettholde et løpende forretningsforhold med disse kundene. I Microsoft Dynamics 365-apper inntreffer kundeemne til kontanter-prosessen gjennom tilbud eller arbeidsflyter for ordrebehandling, og finansene avstemmes og føres. Integrering av kundeemne til kontanter med dobbel skriving oppretter en arbeidsflyt som tar et tilbud og en ordre som kommer fra enten Dynamics 365 Sales eller Dynamics 365 Supply Chain Management, og gjør tilbudet og ordren tilgjengelig i begge appene.

I app-grensesnittene kan du få tilgang til behandlingsstatusene og fakturainformasjonen i sanntid. Derfor er det enklere å administrere funksjoner som produktlagring, lagerhåndtering og oppfyllelse i Supply Chain Management, uten å måtte opprette tilbudene og ordrene på nytt.

![Dataflyt for dobbel skriving i kundeemne til kontanter.](../dual-write/media/dual-write-prospect-to-cash[1].png)

Hvis du vil ha informasjon om kunde- og kontaktintegrering, kan du se [Integrert originalkunde](customer-mapping.md). Hvis du vil ha informasjon om produktintegrering, kan du se [Samlet produktopplevelse](product-mapping.md).

> [!NOTE]
> Både kundeemne og kunde refererer i Dynamics 365 Sales til en post i tabellen **Forretningsforbindelse** der kolonnen **RelationshipType** er enten **Kundeemne** eller **Kunde**. Hvis forretningslogikken omfatter en kvalifikasjonsprosess for **Forretningsforbindelse** der posten **Forretningsforbindelse** opprettes og kvalifiseres først som et kundeemne og deretter som en kunde, synkroniseres denne posten bare med økonomi og driftsappen når den er en kunde (`RelationshipType=Customer`). Hvis du vil at raden **Forretningsforbindelse** skal synkroniseres som et kundeemne, må du ha en egendefinert tilordning for å integrere kundeemnedataene.

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

Før du kan synkronisere salgstilbud, må du oppdatere følgende innstillinger.

### <a name="setup-in-sales"></a>Oppsett i salg

I Sales går du til **Innstillinger \> Administrasjon \> Systeminnstillinger \> Salg**, og sørger for å bruke følgende innstillinger:

- Alternativet **Bruk systemets priskalkuleringssystem** er satt til **Ja**.
- Kolonnen **Rabattkalkuleringsmetode** settes til **Linjeelement**.

### <a name="sites-and-warehouses"></a>Områder og lagre

I Supply Chain Management kreves **Område**- og **Lager**-kolonnene for tilbudslinjer og ordrelinjer. Hvis du angir området og lageret i standard ordreinnstillinger, blir disse kolonnene automatisk definert når du legger til et produkt i en tilbudslinje eller en ordrelinje. 

### <a name="number-sequences-for-quotations-and-orders"></a>Nummerserier for tilbud og ordrer

Nummerseriene for Supply Chain Management og Sales er ikke tilkoblet når tilbud og ordrer opprettes og synkroniseres i Sales og Supply Chain Management. Hvis en salgsordre som er opprettet i Sales, blir synkronisert til Supply Chain Management, har den samme salgsordrenummeret i Supply Chain Management. For å sikre at salgsordrenummeret ikke dupliseres, må du bruke andre nummerseriesystemer i de to appene.

Nummerserien i Supply Chain Management er for eksempel **1, 2, 3, 4, 5, ...**, og nummerserien i Sales er **100, 99, 98, ...**. Hvis du oppretter 100 salgsordrer i Sales, blir det generert et ordrenummer som allerede finnes i Supply Chain Management. Med andre ord vil de to nummerseriene overlappes etter hvert som salgsordrene opprettes i Supply Chain Management og Sales. I stedet kan du bruke en nummerserie som **F1, F2, F3, ...** i Supply Chain Management og en nummerserie som **C1, C2, C3, ...** i Sales. Disse nummerseriene vil aldri generere dupliserte salgsordrenumre.

## <a name="sales-quotations"></a>Salgstilbud

Salgstilbud kan opprettes i både Sales og Supply Chain Management. Hvis du oppretter et tilbud i Sales, blir det synkronisert til Supply Chain Management i sanntid. Tilsvarende, hvis du oppretter et tilbud i Supply Chain Management, blir det synkronisert til Sales i sanntid. Merk følgende punkt:

+ Du kan legge til en rabatt i produktet på tilbudet. I dette tilfellet blir rabatten synkronisert til Supply Chain Management. Kolonnene **Rabatt**, **Gebyrer** og **Avgift** i hodet kontrolleres av et oppsett i Supply Chain Management. Dette oppsettet støtter ikke integreringstilordning. I stedet vedlikeholdes og behandles kolonnene **Pris**, **Rabatt**, **Gebyrer** og **Avgift** i Supply Chain Management.
+ Kolonnene **Rabattprosent**, **Rabatt** og **Fraktbeløp** i salgstilbudshodet er skrivebeskyttede kolonner.
+ Kolonnene **Fraktvilkår**, **Betalingsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke en del av standardtilordningene. Hvis du vil tilordne disse kolonnene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som tabellen synkroniseres mellom.

Hvis du også bruker Field Service-løsningen, må du kontrollere at parameteren **Hurtigoppretting av tilbudslinje** aktiveres på nytt. Hvis du aktiverer parameteren på nytt, kan du fortsette å opprette tilbudslinjer ved hjelp av funksjonen for hurtigoppretting.

1. Gå til Dynamics 365 Sales-programmet.
2. Velg innstillinger-ikonet i det øverste navigasjonsfeltet.
3. Velg **Avanserte innstillinger**.
4. Velg **Tilpass systemet**-alternativet.
5. Velg menyelementet **Tilbudslinje**.
6. Gå til **Datatjenester**-delen, og merk av for **Tillat hurtigoppretting**.

## <a name="sales-orders"></a>Salgsordre

Salgsordrer kan opprettes i både Sales og Supply Chain Management. Hvis du oppretter en salgsordre i Sales, blir den synkronisert til Supply Chain Management i sanntid. Tilsvarende, hvis du oppretter en salgsordre i Supply Chain Management, blir den synkronisert til Sales i sanntid. Merk følgende punkt:

+ Innskrivningsprodukter på Dynamics 365 Sales vil vises som produktkategorier i Dynamics 365 Supply Chain Management.
+ Rabattberegning og -avrunding:

    - Modellen for rabattberegningen i Sales er forskjellig fra modellen for rabattberegningen i Supply Chain Management. I Supply Chain Management kan det endelige rabattbeløpet på en salgslinje være resultatet av en kombinasjon av rabattbeløp og rabattprosenter. Hvis dette endelige rabattbeløpet deles på antallet på linjen, kan det forekomme avrunding. Denne avrunding blir imidlertid ikke tatt hensyn til hvis et avrundet per enhet-rabattbeløp synkroniseres til Sales. For å sikre at hele rabattbeløpet fra en salgslinje i Supply Chain Management synkroniseres riktig med Sales, må hele beløpet synkroniseres uten at det blir delt på linjeantallet. Derfor må du definere rabattkalkuleringsmetoden som **Linjeelement** i Sales.
    - Når en salgsordrelinje synkroniseres fra Sales til Supply Chain Management, brukes hele linjerabattbeløpet. Supply Chain Management har ingen kolonner som kan lagre fullstendige rabattbeløpet for en linje, og beløpet deles derfor på antallet og lagres i kolonnen **Linjerabatt**. Avrunding som forekommer under denne delingen, lagres i kolonnen **Salgstillegg** på salgslinjen.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Eksempel: Synkronisering fra Sales til Supply Chain Management

Du har følgende salgsordre:

+ **Sales**: Antall = 3, per linjerabatt = $ 10,00
+ **Supply Chain Management:** Antall = 3, linjerabattbeløp = $ 3,33, salgstillegg= -$ 0,01

Hvis du synkroniserer fra Supply Chain Management til Sales, får du følgende resultat:

+ **Supply Chain Management:** Antall = 3, linjerabattbeløp = $ 3,33, salgstillegg= -$ 0,01
+ **Sales**: Antall = 3, per linjerabatt = = (3 × $ 3,33) + $ 0,01 = $ 10,00

## <a name="dual-write-solution-for-sales"></a>Løsning for dobbel skriving for Sales

Nye kolonner er lagt til i tabellen **Ordre** og vises på siden. De fleste av disse kolonnene vises i **Integrering**-fanen i Sales. Hvis du vil ha mer informasjon om hvordan statuskolonnene tilordnes, kan du se [Definere tilordningen for salgsordrens statuskolonner](sales-status-map.md).

+ Knappene **Opprett faktura** og **Avbryt ordre** på **Salgsordre**-siden er skjult i Sales.
+ **Salgsordrestatus**-verdien vil fortsatt være **Aktiv** for å sikre at endringer fra Supply Chain Management kan flyte fra salgsordren i Sales. Dette kontrolleres ved å sette standardverdien **Statuskode \[Status\]** til **Aktiv**.

## <a name="invoices"></a>Fakturaer

Salgsfakturaer er opprettet i Supply Chain Management og synkronisert til Sales. Merk følgende punkt:

+ Et **Fakturanummer**-kolonnen er lagt til i **Faktura**-tabellen og vises på siden.
+ Knappen **Opprett faktura** på siden **Salgsordre** er skjult fordi fakturaer vil opprettes i Supply Chain Management og synkroniseres til Sales. Siden **Faktura** kan ikke redigeres fordi fakturaer vil synkroniseres fra Supply Chain Management.
+ **Salgsordrestatus**-verdien endres automatisk til **Fakturert** når relaterte fakturaer fra Supply Chain Management er synkronisert til Sales. Eieren av salgsordren som fakturaen ble opprettet fra, tildeles også som eier av fakturaen. Eieren av salgsordren kan derfor vise fakturaen.
+ Kolonnene **Fraktvilkår**, **Leveringsbetingelser** og **Leveringsmåte** er ikke inkludert i standardtilordningene. Hvis du vil tilordne disse kolonnene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som tabellen synkroniseres mellom.

## <a name="templates"></a>Maler

Kundeemne til kontanter inkluderer en samling tabelltilordninger for viktige områder som fungerer sammen under datasamhandling, som vist i følgende tabell.

| Finance and Operations-apper | Kundeengasjementsapper | Beskrivelse |
|-----------------------------|-----------------------------------|-------------|
[Alle produkter](mapping-reference.md#138) | msdyn_globalproducts | |
[Kunder V3](mapping-reference.md#101) | kontoer | |
[Kunder V3](mapping-reference.md#116) | kontakter | |
[Kontakter V2](mapping-reference.md#221) | msdyn_contactforparties | |
[CDS-salgsordrehoder](mapping-reference.md#217) | salesorders | |
[CDS-salgsordrelinjer](mapping-reference.md#216) | salesorderdetails | |
[CDS-salgstilbudshode](mapping-reference.md#215) | tilbud | |
[CDS-salgstilbudslinjer](mapping-reference.md#214) | quotedetails | |
[Frigitte produkter V2](mapping-reference.md#189) | msdyn_sharedproductdetails | |
[Salgsfakturahoder V2](mapping-reference.md#118) | fakturaer | Tabellen Salgsfakturahoder V2 i økonomi- og driftsappen inneholder fakturaer for salgsordrer og fritekstfakturaer. Det brukes et filter for dobbel skriving i Dataverse som filtrerer ut alle fritekstfakturadokumenter. |
[Salgsfakturalinjer V2](mapping-reference.md#117) | invoicedetails | |
[Koder for salgsordregrunnlag](mapping-reference.md#186) | msdyn_salesorderorigins | |

Hvis du vil ha informasjon om prislister, kan du se [Samlet produktopplevelse](product-mapping.md).

## <a name="limitations"></a>Begrensninger

- Returordrer støttes ikke.
- Kreditnotaer støttes ikke.
- Finansdimensjoner må angis for hoveddataene, for eksempel kunde og leverandør. Når en kunde legges til i et tilbud eller en salgsordre, flyter finansdimensjonene som er knyttet til kundeposten, til ordren automatisk. Dobbel skriving omfatter foreløpig ikke finansdimensjonsdata for hoveddata.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

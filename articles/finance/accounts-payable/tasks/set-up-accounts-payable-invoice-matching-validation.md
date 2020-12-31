---
title: Definere validering av leverandørfakturakontroll
description: Dette emnet gir informasjon om hvordan du definerer validering av leverandørfakturakontroll.
author: abruer
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a101edd9e25fba1aa2325cb2193c6ea56282c9d1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446337"
---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Definere validering av leverandørfakturakontroll

[!include [banner](../../includes/banner.md)]

Før du begynner, må du kontrollere at konfigurasjonsnøkkelen for fakturasamsvar er valgt. Hvis den juridiske enheten sporer utgifter, for eksempel frakt, ved hjelp av tillegg, må du kontrollere at konfigurasjonsnøkkelen for Tillegg er valgt.  Leverandørfakturakontroll er prosessen med å sjekke samsvar mellom leverandørfakturaen, bestillingen og produktkvitteringsinformasjonen. Forskjeller mellom disse dokumentene kalles samsvarende avvik. Samsvarende avvik blir sammenlignet med toleransen som er angitt. Hvis et samsvarende avvik er større enn toleranseprosenten eller -beløpet, vises ikoner for samsvarsavvik på siden **Leverandørfaktura** og på siden **Fakturakontrolldetaljer**.

## <a name="determine-which-invoice-matching-validation-to-use"></a>Avgjøre hvilken validering av fakturakontroll som skal brukes
Det finnes fire ulike kontrollvalideringstyper. 

- **Linjenivåkontroll** – Den vanligste kontrolltypen er linjekontroll. Linjenivåkontroll kan være toveis eller treveis kontroll. Standard linjenivåkontroll kan angis for en juridisk enhet på siden **Leverandørparametere**. Toveis kontroll sammenligner enhetsprisen på fakturaen med enhetsprisen på bestillingen. Treveis kontroll sammenligner i tillegg fakturaantallet med det samsvarende antallet på mottaksseddelen.
- **Samsvar av fakturatotaler** – Sammenlign det totale beløpet på fakturaen med det totale beløpet i bestillingen. Denne typen fakturakontroll inneholder færrest detaljer slik at du kan bruke dette alternativet til å definere kontroller som begrenser tiden det tar for staben å se gjennom informasjon om fakturakontroll. Seks totaler sammenlignes, inkludert delsum, sluttrabatt, tillegg, merverdiavgift, avrunding og fakturabeløp. Systemet validerer om noen av disse verdiene på fakturaen avviker fra forventede beløp med en større margin enn det som er akseptabelt.
- **Samsvar av tillegg** – Sammenlign tilleggsinformasjonen (beløp) på fakturaen med tilleggsinformasjonen (beløp) på bestillingen.
- **Kontroll av pristotaler for linjeelementer** – Denne kontrolltypen er nyttig for firmaer som vanligvis mottar flere fakturaer for én bestillingslinje. Hvis du vanligvis bare mottar én faktura per bestillingslinje, er ikke denne kontrolltypen nødvendig. Denne kontrollen krever at toveis eller treveis kontroll er aktivert, og fungerer som en validering av nettobeløp som ikke kan overskrides, basert på toleranseprosenter og -beløp.  Denne kontrolltypen sammenligner prisinformasjon for nettobeløpet for hver linje på fakturaen, og alle ventende og tidligere posterte fakturalinjer, med nettobeløpet for den tilhørende bestillingslinjen. Nettobeløpet fastsettes med følgende formel: (enhetspris * linjeantall) + linjetillegg - linjerabatter. Når samlet pris tilpasses til prosent, sammenligner systemet verdier ved hjelp av transaksjonsvalutaen. Når samlet pris tilpasses til beløp, sammenligner systemet verdiene ved hjelp av regnskapsvalutaen.

## <a name="set-up-parameters-to-enable-invoice-matching-validation"></a>Definere parametere for å aktivere validering av fakturakontroll
1. Gå til **Leverandører > Oppsett > Leverandørparametere**.
2. Velg **Fakturavalidering**-fanen.
3. Merk av eller fjern merket for **Aktiver validering av fakturakontroll**.
    * Velg om godkjenning skal kreves før en faktura som inneholder avvik for fakturakontroll, kan posteres. Hvis dette er satt til **Tillat med advarsel**, vises en visuell indikasjon når et avvik for fakturakontroll overskrider toleransen. Du vil imidlertid kunne postere fakturaen. Hvis du vil bruke arbeidsflyter sammen med validering av fakturakontroll, må du sørge for at feltet **Poster faktura med avvik** er satt til **Tillat med advarsel** for å unngå å godkjenne flere ganger.  
    * I feltet **Oppdater status for fakturahodekontroll automatisk** velger du om kontroll skal utføres automatisk under registrering av data i systemet. Den anbefalte innstillingen er **Ja**, med mindre du opplever ytelsesproblemer med dataregistrering. Deaktivering av automatiske oppdateringer kan gi raskere systemytelse fordi validering av fakturakontroll vil hoppes over under dataregistrering. Dataregistrereren må manuelt oppdatere fakturaens samsvarsstatus for å se valideringsresultater av fakturakontroll når det er satt til **Nei**.  
4. Angi **Samsvar av fakturatotaler**.
5. Merk av eller fjern merket for **Samsvar fakturatotaler** for å samsvare faktiske fakturatotaler med forventede summer.
    * Velg om et ikon skal vises hvis et avvik for fakturakontroll overskrider toleransen. Du kan velge å vise ikonet når et positivt avvik overskrider toleransen, eller når enten et positivt eller et negativt avvik overskrider toleransen.  
    * Toleransen er for eksempel 5 prosent, og det totale fakturabeløpet, basert på bestillingen, er 100,00. Derfor vises et ikon for prissamsvar hvis det totale fakturabeløpet overskrider 105,00. Hvis du velger **Hvis større eller mindre enn toleransen**, vises også et ikon hvis fakturabeløpet er mindre enn 95,00.  
6. I feltet **Toleranseprosent for fakturatotaler** angir du prosentavviket som er akseptabelt. Denne verdien er standardverdien for firmaet. Denne verdien kan overstyres for bestemte leverandører på siden **Toleranser for fakturatotaler**. Hvis du vil ha informasjon om hvordan du overstyrer toleranseprosent for fakturatotaler for en bestemt leverandør, kan du se delen «Definere fakturatotaler som samsvarer med toleranser for leverandører» senere i dette emnet.
7. Angi **Pris- og antallssamsvar**.
8. I feltet **Linjekontrollpolicy** velger du en verdi som skal brukes som standardpolicy for den juridiske enheten du arbeider med. **Ikke nødvendig** betyr at det ikke kreves noen kontroll av individuelle fakturalinjepriser til bestillingspris eller fakturaantall til antallet på følgeseddelen. **Toveis samsvar** betyr at det kreves bekreftelse av fakturalinjer, men bare bestillingen og leverandørens fakturadokumenter er involvert i kontrollen. Produktkvitteringen tas ikke med i de samsvarende valideringene. **Treveis samsvar** betyr at fakturaens nettoenhetspris skal sammenlignes med bestillingens nettoenhetspris, og antallet produktkvitteringer skal sammenlignes med fakturaantallet.
9. Hvis du vil gjøre det mulig å bruke et annet samsvarsnivå for en vare, leverandør, kombinasjon av leverandør og vare eller bestillingslinje, velger du en verdi i feltet **Tillat overstyring av kontrollpolicy**. Linjekontrollpolicyen for juridisk enhet kan overstyres for en bestemt leverandør, vare eller kombinasjon av leverandør og vare på **Kontrollpolicy**-siden.
    * Hvis du bruker en linjekontrollpolicy med toveis eller treveis samsvar, kan du definere pristoleranseprosenter for juridisk enhet, varer og leverandører på siden **Pristoleranse for vare**. Standard pristoleranse for juridisk enhet settes til null prosent for toveis og treveis kontroll. Når leverandørfakturaer blir sammenlignet med informasjonen i bestillinger, søkes det etter den aktuelle pristoleranseprosenten.   
10. Hvis du vil samsvare pristotaler for linjeelementer på fakturaer, velger du en verdi i feltet **Tilpass samlet pris**. Denne typen samsvar er nyttig når leverandøren sender flere fakturaer for samme bestillingslinje. Du kan sammenligne prisinformasjon for nettobeløpet for hver linje på fakturaen, og alle ventende og tidligere posterte fakturalinjer, med nettobeløpet for den tilhørende bestillingslinjen.  Alternativene omfatter **Ingen**, **Prosent**, **Beløp** eller **Prosent og beløp**.
11. I feltet **Toleranseprosent for total innkjøpspris** angir du en avviksprosent du vil godta. Dette feltet er tilgjengelig når **Prosent** eller **Prosent og beløp** er angitt i feltet **Tilpass samlet pris**.
12. I feltet **Toleranse for total innkjøpspris** angir du et beløp i regnskapsvalutaen. Dette feltet er tilgjengelig når **Beløp** eller **Prosent og beløp** er angitt i feltet **Tilpass samlet pris**.
13. I feltet **Vis ikon for totalprissamsvar** velger du når et ikon skal vises hvis et avvik for fakturakontroll overskrider toleransen for netto enhetspris. Ikonet kan vises når et positivt avvik overskrider toleransen, eller når enten et positivt eller et negativt avvik overskrider toleransen.
Toleransen er for eksempel 5 prosent, og linjeprissummen, basert på bestillingen, er 10,00. Derfor vises et ikon for prissamsvar hvis linjeprissummen på fakturaen overskrider 10,50. Hvis du velger **Hvis større eller mindre enn toleransen**, vises også et ikon hvis linjeprissummen på fakturaen er mindre enn 9,50.
13. Angi samsvar av tillegg.
14. Når du skal samsvare faktiske tillegg med forventede tillegg basert på opplysningene i bestillingen, merker du av for **Samsvar tillegg**.

## <a name="set-up-unit-price-tolerance-percentages"></a>Definere toleranseprosenter for enhetspris
Gå til **Leverandører > Oppsett > Fakturakontrolloppsett > Pristoleranser** for å definere tillatte pristoleranseprosenter. Hvis du bruker en linjekontrollpolicy med toveis eller treveis kontroll, kan du definere pristoleranseprosenter for juridisk enhet, varer og leverandører. Når leverandørfakturaer blir sammenlignet med informasjonen i bestillinger, søkes det etter den aktuelle pristoleranseprosenten. Dette er standard søkerekkefølge:
* Tabell/tabell
* Tabell/gruppe
* Tabell/alle
* Gruppe/tabell
* Gruppe/gruppe
* Gruppe/alle
* Alle/tabell
* Alle/gruppe
* Alle/alle

Den juridiske enhetens standard pristoleranseprosent er 0 prosent, og denne pristoleransen brukes for alle varer og alle kontoer (Alle, Alle). Du kan ikke slette posten for standard pristoleranse for juridisk enhet.

Negative prisavvik er som standard tillatt. Du kan imidlertid ikke angi et negativt tall som pristoleranseprosenten. Hvis du vil spore negative pristoleranseprosenter, velger du **Hvis større eller mindre enn toleransen** i feltet **Vis ikon for enhetsprissamsvar** på siden **Leverandørparametere**. Deretter angir du pristoleranseprosenter **Pristoleranser**-siden.

## <a name="set-up-matching-policy-override"></a>Konfigurere overstyring av kontrollpolicy

Gå til **Leverandører > Oppsett > Fakturakontrolloppsett > Kontrollpolicy** for å definere standardoppføringen for Kontrollpolicy-feltet for linjer i bestillingsskjemaet. Dette er en valgfri konfigurasjon. Bruk dette skjemaet til å definere toveis eller treveis kontroll for varer, leverandører eller kombinasjoner av vare og leverandør. Disse oppføringene gjør at du kan definere mer detaljerte kontrollpolicyer enn kontrollpolicyen for juridisk enhet du definerte på siden **Leverandørparametere**. Standard linjekontrollpolicy for juridisk enhet gjelder for alle varer og leverandører, unntatt de som det er angitt en annen linjekontrollpolicy for på denne siden.

På denne siden velger du **Kontrollpolicynivå**. Velg nivået i kontrollpolicyhierarkiet du vil angi linjekontrollpolicyer for.

- **Vare og leverandør** – Angi kontrollpolicyen for bestemte varer som kjøpes fra bestemte leverandører.
- **Vare** – Angi kontrollpolicyen for bestemte varer som kjøpes fra en hvilken som helst leverandør, unntatt de som er angitt på vare- og leverandørnivået.
- **Leverandør** – Angi kontrollpolicyen for alle varer som kjøpes fra bestemte leverandører, unntatt de som er angitt på vare- og leverandørnivået.
  
Følgende hierarki brukes til å fastsette kontrollpolicyen som brukes:
  *  Vare og leverandør
  *  Element
  *  Leverandør
  *  Juridisk enhet
  
## <a name="set-up-invoice-totals-matching-tolerance-for-vendors"></a>Definere fakturatotaler som samsvarer med toleranse for leverandører

Gå til **Leverandører > Oppsett > Fakturakontrolloppsett > Toleranser for fakturatotaler** for å angi leverandørspesifikke toleranser for kontroll for fakturatotaler. Kontrollberegningen bruker toleranseprosent for fakturatotaler fra leverandørkontoen som er angitt som ordrekontoen på leverandørfakturaen. Hvis leverandørkontoen ikke har en angitt toleranseprosent for fakturatotaler, brukes toleranseprosenten for fakturatotaler som er angitt for den juridiske enheten på siden **Leverandørparametere**.

1. Du kan angi toleranser for enkeltleverandører som overstyrer standardtoleransen, ved å velge en **Leverandørkonto**.
2. Angi avviksprosenten du vil godta for denne leverandøren.

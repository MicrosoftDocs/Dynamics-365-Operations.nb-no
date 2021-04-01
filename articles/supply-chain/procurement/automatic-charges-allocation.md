---
title: Automatisk tilordning av tillegg
description: Med gebyrer-funksjonen i Microsoft Dynamics 365 Supply Chain Management kan du automatisk tilordne tillegg til bestillinger eller salgsordrer.
author: dasani-madipalli
manager: tfehr
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: eddcf275c14565dfe77fbe7efa676be4a34da686
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244165"
---
# <a name="automatic-allocation-of-charges"></a>Automatisk tilordning av tillegg

[!include [banner](../includes/banner.md)]

Avhengig av hvilken kunde du jobber med eller varen du selger, kan det hende at du vil bruke bestemte tilleggskostnader. Med *gebyrer*-funksjonen i Microsoft Dynamics 365 Supply Chain Management kan du automatisk tilordne tillegg til bestillinger eller salgsordrer.

Automatiske tillegg brukes automatisk når du oppretter en salgsordre eller bestilling. Du kan definere automatiske gebyrer for bestemte leverandører, kunder, grupper med leverandører, kunder eller varer. Du kan også definere automatiske gebyrer som gjelder for alle leverandører, kunder eller varer.

## <a name="set-up-charges-codes"></a>Definere gebyrkoder

Hvis du vil tilordne tillegg, må du først definere tilleggskoder.

1. Følg ett av disse trinnene:

    - For bestillinger: Gå til **Leverandør \> Oppsett for tillegg \> Tilleggskode**.
    - For salgsordrer: Gå til **Kunde \> Oppsett for tillegg \> Tilleggskode**.

1. I handlingsruten velger du **Ny** for å opprette en tilleggskode.
1. I toppteksten for den nye posten angir du følgende felt:

    - **Tilleggskode** – Angi en kode for gebyrene.
    - **Beskrivelse** – Angi en beskrivelse av gebyrene.
    - **Merverdiavgiftsgruppe for vare** – Velg en mva-gruppe for vare, hvis det er aktuelt.
    - **Fordeling** – Angi dette alternativet til *Ja* hvis du vil fordele kostnadene. Dette alternativet er bare tilgjengelig for salgsordrer.
    - **Maksimalbeløp** – Angi det maksimale beløpet som er tillatt for tilleggskoden. Dette feltet brukes til å validere gebyrer for leverandørfakturaer. Det er bare tilgjengelig for bestillinger.

        > [!NOTE]
        > Hvis du vil aktivere funksjonaliteten for validering av tillegg for bestillinger, går du til **Leverandører \> Oppsett \> Leverandørparametere**. I hurtigfanen **Fakturavalidering**, i delen **Fakturavalidering**, angir du alternativet **Aktiver validering av fakturakontroll** til *Ja*.

1. Hurtigfanen **Postering** inneholder **Debet** og **Kredit**-deler. Angi følgende felt, avhengig av finans som du vil postere tillegg for:

    - **Type** – Velg kontotypen du posterer til (*Finans*, *Kunde* eller *Vare*).
    - **Postering** – Velg hvilke posteringer som skal opprettes (for eksempel *Meglergebyr* eller *Kundeutligning*).
    - **Konto** – Velg kontoen du vil postere tillegget for.

1. Velg **Lagre** i handlingsruten.

## <a name="create-charge-groups"></a>Opprette gebyrgrupper

Gebyrgrupper tildeler automatisk bestemte tillegg til en gruppe kunder eller leverandører. Underdelene nedenfor beskriver hvordan du oppretter og tilordner disse tilleggsgruppene.

### <a name="charge-groups-for-purchase-orders"></a>Tilleggsgrupper for bestillinger

Hvis du vil opprette tilleggsgrupper for bestillinger, følger du disse trinnene.

1. Gå til **Leverandører \> Oppsett for tillegg \> Leverandørtilleggsgruppe**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet, og angi deretter følgende felt:

    - **Tilleggsgruppe** – Angi navnet på tilleggsgruppen.
    - **Beskrivelse** – Angi en beskrivelse av tilleggsgruppen.

1. Velg **Lagre** i handlingsruten.
1. Gå til **Leverandør \> Leverandører \> Alle leverandører**, og åpne en eksisterende leverandør eller opprett en ny leverandør.
1. I hurtigfanen **Bestillingsstandarder**, i **Bestilling**-delen, angir du **Tilleggsgruppe**-feltet for tilleggsgrupen du nettopp opprettet.

### <a name="charge-groups-for-sales-orders"></a>Tilleggsgrupper for salgsordrer

Hvis du vil opprette tilleggsgrupper for salgsordrer, følger du disse trinnene.

1. Gå til **Kunde \> Oppsett for tillegg \> Kundetilleggsgrupper**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet, og angi deretter følgende felt:

    - **Tilleggsgruppe** – Angi navnet på tilleggsgruppen.
    - **Beskrivelse** – Angi en beskrivelse av tilleggsgruppen.

1. Velg **Lagre** i handlingsruten.
1. Gå til **Kunde \> Kunder \> Alle kunder**, og åpne en eksisterende kunde eller opprett en ny kunde.
1. I hurtigfanen **Bestillingsstandarder**, i **Salgsordre**-delen, angir du **Tilleggsgruppe**-feltet for tilleggsgrupen du nettopp opprettet.

## <a name="define-auto-charges"></a>Definere automatiske gebyrer

Når tilleggskodene er definert, følger du disse trinnene for å definere de automatiske tilleggene.

1. Følg ett av disse trinnene:

    - For bestillinger: Gå til **Innkjøp og leverandører \> Oppsett \> Gebyrer \> Automatiske tillegg**.
    - For salgsordrer: Gå til **Kunde \> Oppsett \> Oppsett for tillegg \> Automatiske gebyrer**.

1. I listeruten, i **Nivå**-feltet, velger du nivået der det automatisk gebyret gjelder:

    - *Hoved* – Beregn tillegg i ordrehodet.
    - *Linje* – Beregn tillegg i ordrelinjene.

1. Velg et eksisterende automatisk gebyr som skal redigeres, eller velg **Ny** for å definere et nytt automatisk gebyr.
1. Velg en av følgende verdier for å angi kontoområdet som vil bli påvirket, i **Kontokode**-listen:

    - *Tabell* – Knytt tillegg til en bestemt kunde eller leverandør.
    - *Gruppe* – Knytt tilleggene til en tilleggsgruppe.
    - *Alle* – Knytt tillegg til alle kunder eller leverandører.

1. I feltet **Kunderelasjon** eller **Leverandørrelasjon** velger du en bestemt kunde eller leverandør hvis du angir **Kontokode**-feltet til *Tabell*. Hvis du angir **Kontokode**-feltet til *Gruppe*, velger du en kunde- eller leverandørtilleggsgruppe.
1. Velg en av følgende verdier for å angi vareområdet som vil bli påvirket, i **Varekode**-listen. Du kan bare velge en varekode når du definerer automatiske gebyrer på linjenivået.

    - *Tabell* – Knytt tillegg til en bestemt vare.
    - *Gruppe* – Knytt tillegg til en varetilleggsgruppe.
    - *Alle* – Knytt tillegg til alle varer.

1. Velg en bestemt vare i **Varerelasjon**-feltet hvis du angir **Varekode**-feltet til *Tabell*. Hvis du valgte **Gruppe** i *Varekode*-feltet, må du velge en tilleggsgruppe for varen.
1. **Bare for salgsordrer:** I feltet **Kode for leveringsmåte** velger du en av følgende verdier for å angi omfanget for leveringsmåter som blir påvirket:

    - *Tabell* – Knytt tillegg til en bestemt leveringsmåte.
    - *Gruppe* – Knytt tillegg til en leveringsmåtegruppe.
    - *Alle* – Knytt tillegg til alle leveringsmåter.

1. **Bare for salgsordrer:** I feltet **Relasjon for leveringsmåte** velger du en bestemt leveringsmåte hvis du angir feltet **Kode for leveringsmåte** til *Tabell*. Hvis du velger **Gruppe** for feltet *Kode for leveringsmåte*, må du velge en leveringsmodusgruppe.
1. I hurtigfanen **Linjer** definerer du tilleggene og tilleggssatsene som skal brukes når det gjeldende automatiske tillegget brukes. Du kan bruke verktøylinjen i denne hurtigfanen til å legge til så mange linjer som du trenger. For hver linje angir du feltene nedenfor:

    - **Valuta** – Velg valutaen som skal brukes til å beregne tillegget.
    - **Tilleggskode** – Velg koden for tillegget.
    - **Kategori** – Velg én av følgende verdier:

        - *Fast* – Gebyret er angitt som et fast beløp på linjen. Faste tillegg kan brukes på tillegg både i ordrehodet og på ordrelinjene.
        - *Stk.* – Gebyret er basert på enheten. Disse tilleggene kan bare brukes på ordrelinjer. De vil vises når du beregner totalsummen for ordren.
        - *Prosent* – Gebyret er angitt som en prosent på linjen. Prosenttillegg kan brukes på tillegg både i ordrehodet og på ordrelinjene.
        - *Konserneintern prosent* – Tillegget blir angitt som en prosent på linjen for konserninterne ordrer. Konserninterne prosenttillegg kan bare brukes på ordrelinjer.
        - *Ekstern* – Gebyret beregnes av en tredjepartstjeneste som er tilknyttet én eller flere transportører.

    - **Gebyrverdi** – Angi gebyrverdien basert på kategorien du har valgt.
    - **Valutakode for tillegg** – Angi en valuta for tillegget hvis du vil bruke en annen valuta enn valutaen du har angitt i **Valuta**-feltet. Du kan bare bruke en annen valuta hvis **Debettype** eller **Kredittype**-feltet er satt *Finanskonto* eller *Vare* for den valgte tilleggskoden.
    - Angi et startbeløp som det automatiske tillegget skal brukes på, **Fra beløp**-feltet. Beløpet i denne sammenhengen refererer til totalsummen for ordren.
    - Angi sluttbeløpet som det automatiske tillegget skal brukes på, **Til beløp**-feltet. Beløpet i denne sammenhengen refererer til totalsummen for ordren.
    - **Mva-gruppe** – Angi en mva-gruppe.
    - **Område** og **Lager** – Angi et område og lager hvis tillegg bare skal brukes for et bestemt område og lager.
    - **Behold** – Merk av i denne boksen for å beholde tilleggstransaksjonene etter fakturering, slik at tillegget brukes hver gang du oppretter en ny faktura for den valgte kundekontoen.

1. **Bare for salgsordrer:** Hvis du vil beregne fordelte tillegg, kan du se [Fordelte tillegg i salgsordrer](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders) for mer informasjon.

## <a name="allocate-charges-from-the-header-to-a-line"></a>Tilordne tillegg fra hodet til en linje

Følgende fremgangsmåte viser hvordan du tildeler gebyrer på hodenivå til en linje. Før du starter denne fremgangsmåten, bør du ha et tillegg på hodenivå for typen *Fast beløp* og en ordre der gebyret brukes. I tillegg bør ordren allerede inneholde minst ett linjeelement.

1. Åpne bestillingen eller tilleggsordren.
1. I hurtigruten følger du ett av disse trinnene:

    - For bestillinger: I **Kjøp**-fanen, i **Tillegg**-gruppen, velger du **Tilordne tillegg**.
    - For salgsordrer: I **Salg**-fanen, i **Tillegg**-gruppen, velger du **Tilordne tillegg**.

1. I dialogboksen **Tilordne tillegg til ordrelinjer** angir du følgende felt:

    - **Gebyrfordeling** – Velg en av følgende verdier for å angi hvordan gebyrene skal tilordnes:

        - *Nettobeløp* – Tildel tillegg i henhold til hvert linjebeløp i forhold til totalt nettobeløp.
        - *Antall* – Tildel tillegg i henhold til antallet enheter for hver linje i forhold til det totale antallet enheter.
        - *Per linje* – Tildel tillegg likt i henhold til det totale antallet linjer.

    - **Tilordne tillegg til linjer** – Velg en verdi for å angi om tillegg skal fordeles på alle linjer, bare til positive linjer eller til negative linjer.
    - **Tildel alle** – Merk av i denne avmerkingsboksen for å fordele tillegg i bestillingslinjer selv om tilleggskoden har en annen debettype enn *Vare*.
    - **Mottatt** – Merk av i denne avmerkingsboksen hvis du bare vil fordele tillegg til mottatte ordrelinjer.
    - **Lagerført** – Merk av i denne avmerkingsboksen hvis du bare vil fordele tillegg til lagerførte ordrelinjer.
    - **Vis valg og fjern bestemte linjer** – Merk av i denne avmerkings boksen for å utelate bestemte linjer fra denne fordelingen. Når du merker av i denne avmerkingsboksen, åpnes rutenettet **Velg linjer som skal utelates fra tildeling**. Dette rutenettet omfatter bare linjene som oppfyller vilkårene i feltene **Tilordne tillegg til linjer** og **Lagerført**. Hvis du velger feltet **Tilordne tillegg til linjer** til *Positive linjer* og merker av for **Lagerført**, vises for eksempel bare linjer som er både positive og lagerført, i rutenettet. I tillegg filtrerer rutenettet automatisk ut alle linjer der hele antallet allerede er mottatt. Når rutenettet er åpent, fjerner du merket for **Inkluder** for hver linje som skal utelates fra fordeling. 

        > [!IMPORTANT]
        > Når du arbeider med rutenettet **Velg linjer som skal utelates fra tildeling**, må du huske å la rutenettet være åpent til du velger **Tildel**. Hvis du lukker rutenettet før du velger **Tildel**, vil innstillingene i rutenettet gå tapt. Tillegg vil derfor bli fordelt basert på kriteriene du har definert tidligere.

1. Velg **Tildel** for å bruke innstillingene og lukke dialogboksen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
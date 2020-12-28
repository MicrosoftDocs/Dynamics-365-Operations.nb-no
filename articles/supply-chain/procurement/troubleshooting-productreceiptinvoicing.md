---
title: Feilsøke mottakssedler og fakturering
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med mottakssedler og fakturering.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: a89effb686d60dde9d11f99be51d4101897ad4ea
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434833"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a>Feilsøke mottakssedler og fakturering

Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med mottakssedler og fakturering.

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Jeg kan ikke postere mer enn én faktura for en bestillingslinje som har kategoribaserte varer.

Et antall er obligatorisk hvis du vil postere fakturaer. Hvis hele antallet av en linje er fakturert bare for et delvis beløp, kan du fakturere restbeløpet på en annen faktura.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Jeg får feilmeldingen "Objektreferanse er ikke angitt" under bestillingsbekreftelsen, eller unntaket "Målet forårsaket et unntak under aktivering" oppstår ved postering av leverandørfaktura.

Dette problemet kan oppstå på grunn av inkonsekvens i bestillingsdistribusjonene.

Du fjerner blokkeringen av dette problemet og tilbakestiller bestillingen til en *Utkast*-tilstand ved å gå til **Innkjøp og leverandører \> Periodiske oppgaver \> Opprydding \> Tilbakestill bestillingsdistribusjon**. Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Løse bestillingsdistribusjonsfeil i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Jeg får ikke til å konsolidere flere produktkvitteringer til én bestilling.

Du kan ikke konsolidere flere produktkvitteringer i én enkelt bestilling hvis de ulike produktkvitteringslinjene har forskjellige regnskapsdatoer.

I tidligere versjoner av Microsoft Dynamics 365 Supply Chain Management var konsolidering tillatt i denne situasjonen. Dette er imidlertid utsatt for feil. Regnskapsdatoen på bestillingslinjene som opprettes, må ikke være forskjellige fra regnskapsdatoen på produktkvitteringslinjene som disse bestillingslinjene ble opprettet fra. (Regnskapsdatoen i bestillingslinjene samsvarer med regnskapsdatoen i bestillingshodet.) Derfor er ikke konsolideringen av flere produktkvitteringer i én enkelt bestillinger tillatt.

Regnskapsdatoen brukes for eksempel for budsjettreservasjoner og disposisjoner. Derfor bør den holdes i løpet av overgangen fra produktkvittering til bestilling.

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a>Når produktkvitteringer annulleres, kan transaksjoner posteres til en suspendert finanskonto.

### <a name="issue-description"></a>Problembeskrivelse

Hvis en produktkvittering avlyses, tillater systemet at transaksjoner posteres til utestengte finanskontoer, selv om hovedkontoene er deaktivert.

### <a name="reproduce-the-issue"></a>Reprodusere problemet

Følgende prosedyre viser én måte å reprodusere problemet på.

1. På siden for **Leverandørparametere**, i kategorien **Generelt**, må du kontrollere at alternativet **Poster produktkvittering i finans** er satt til *Ja*.
1. Opprett en bestilling, og legg til en ordrelinje som har et antall på *1000* for et produkt.
1. Bekreft bestillingen.
1. Poster produktkvitteringen, og sjekk bilagene.
1. Stopp de aktuelle hovedkontoene, *200140* og *140200*.
1. Avbryt den posterte produktkvitteringen.
1. Legg merke til at transaksjoner kan posteres til de suspenderte finanskontoene.

### <a name="issue-resolution"></a>Problemløsning

Transaksjoner kan posteres til de suspenderte finanskontoene når produktkvitteringer avbrytes, fordi denne virkemåten sørger for riktige posteringer.

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a>Et bilagsnummer for produktkvitteringen forbrukes selv om det ikke genereres et økonomisk bilag under produktkvitteringen.

Hvis alternativet **Gjeldsavsetning på produktkvittering** er satt til *Nei* for varemodellgruppen, vil ingen posteringer til økonomimodulen forekomme. En fysisk hendelse vil imidlertid bli registrert for regnskapsformål i en underfinans, og denne hendelsen krever et bilagsnummer. Dette bilagsnummeret er bilagsnummeret som det refereres til i lagertransaksjonene.

Vi anbefaler at du setter alternativet **Gjeldsavsetning på produktkvittering** til *Ja*, som beskrevet i følgende blogginnlegg: [Poster tilleggskostnader på tidspunktet for produktkvitteringen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Innstillingen Postere i belastningskonto i finans er ikke aktivert.

### <a name="issue-description"></a>Problembeskrivelse

Dette problemet oppstår når en bestilling faktureres hvis alternativet **Postere i belastningskonto i finans** er satt til *Ja* i kategorien **Faktura** på siden **Leverandørparametere**.

### <a name="reproduce-the-issue"></a>Reprodusere problemet

Følgende prosedyre viser én måte å reprodusere problemet på.

1. Gå til **Leverandører \> Oppsett \> Leverandørparametere**.
1. I kategorien **Faktura** setter du alternativet **Postere i belastningskonto i finans** til *Ja*.
1. Gå til **Lagerstyring \> Oppsett \> Postering \> Postering**.
1. I kategorien **Bestilling** må du kontrollere at du har slettet alle linjene i innkjøpsutgiften for produktet.
1. Gå til **Leverandører \> Bestillinger \> Alle bestillinger**.
1. Opprett en bestilling. I feltet **Leverandørkonto** velger du *1001 Acme-kontorutstyr*.
1. Legg til en bestillingslinje som har følgende innstillinger:

    - **Varenummer:** *D0011 laserprojektor*
    - **Område:** *1*
    - **Lager:** *11*
    - **Antall:** *4*

1. I handlingsruten i kategorien **Bestilling** i gruppen **Handling** velger du **Bekreft**.
1. I handlingsruten i kategorien **Motta** i gruppen **Generer** velger du **Produktkvittering**.
1. I dialogboksen **Poster mottaksseddel**, i feltet **Produktkvittering**, angir du et vilkårlig nummer og velger **OK**.
1. I handlingsruten, på **Faktura**-fanen i **Generer**-gruppen, velger du **Faktura**.
1. I **Nummer**-feltet angir du et tilfeldig nummer som fakturanummeret.
1. Oppdater samsvarsstatusen, og poster.
1. Legg merke til at du nå får følgende feilmelding når du genererer en faktura fra en bestilling: "Kontonummeret for transaksjonstypen Innkjøpsutgift for produkt finnes ikke".

### <a name="issue-resolution"></a>Problemløsning

Dette avhenger av parameterinnstillingene for fakturaer og fakturagrupper. Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Regnskap for innkjøpstillegg og lageravvik](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).

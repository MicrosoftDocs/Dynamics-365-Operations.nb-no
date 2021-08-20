---
title: Feilsøke bestillinger
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med bestillinger.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 963a2363ee7cdca6ed25be805e69eeb41331b6f4773c1c59da903fda68ba570b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744756"
---
# <a name="troubleshoot-purchase-orders"></a>Feilsøke bestillinger

Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med bestillinger.

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a>En handling kan bare fullføres etter at linjenummeret er ferdig distribuert.

Dette problemet kan oppstå på grunn av inkonsekvens i bestillingsdistribusjonene.

Du fjerner blokkeringen av dette problemet og tilbakestiller bestillingen til en *Utkast*-tilstand ved å gå til **Innkjøp og leverandører \> Periodiske oppgaver \> Opprydding \> Tilbakestill bestillingsdistribusjon**. Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Løse bestillingsdistribusjonsfeil i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a>Når bestillinger importeres via databehandling, følger ikke bestillingslinjenumrene den økningen som er definert i systemparametere.

### <a name="issue-description"></a>Problembeskrivelse

Som standard vil automatisk genererte linjenumre for bestillingslinjer som importeres via *Bestillingslinjer v2*-dataenheten, ikke bruke systemets linjenummerøkning som er angitt i systemparametere. Hvis du oppretter en bestilling manuelt og legger til linjer via bruker grensesnittet, økes linjenumrene på riktig måte. Hvis du imidlertid bruker Data Management Framework (DMF), økes de ikke riktig.

Dette problemet oppstår fordi når du importerer linjer via DMF, hvis linjenumre ikke allerede er tilordnet i den importerte enheten, bruker systemet DMFs metode for å tilordne dem. Denne metoden øker alltid linjenumrene med én.

### <a name="issue-workaround"></a>Problemløsning

Kontroller at de ønskede linjenumrene allerede er angitt i linjenummerfeltene for dataenhet når du importerer bestillingslinjer. I dette tilfellet vil ikke DMF overskrive linjenumrene.

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a>En standard mva-gruppe og en standard kontantrabatt blir ikke fylt ut fra fakturakontoen.

Hvis du bruker en fakturakonto som er forskjellig fra kundekontoen, blir det ikke fylt ut en standard mva-gruppe og en standard kontantrabatt fra fakturakontoen når en bestilling opprettes.

Denne virkemåten er standard. Standardverdiene for mva-gruppen, kontantrabattene og annen prisinformasjon er basert på kundekontoen, ikke fakturakontoen.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Jeg får feilmeldingen "Objektreferanse er ikke angitt" under bestillingsbekreftelsen, eller unntaket "Målet forårsaket et unntak under aktivering" oppstår ved postering av leverandørfaktura.

Dette problemet kan oppstå på grunn av inkonsekvens i bestillingsdistribusjonene.

Du fjerner blokkeringen av dette problemet og tilbakestiller bestillingen til en *Utkast*-tilstand ved å gå til **Innkjøp og leverandører \> Periodiske oppgaver \> Opprydding \> Tilbakestill bestillingsdistribusjon**. Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Løse bestillingsdistribusjonsfeil i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Én eller flere regnskapsdistribusjoner er enten over- eller underdistribuert.

### <a name="issue-description"></a>Problembeskrivelse

Du får følgende feilmelding: "Én eller flere regnskapsdistribusjoner er enten over- eller underdistribuert".

### <a name="issue-resolution"></a>Problemløsning

Dette problemet kan oppstå på grunn av inkonsekvens i bestillingsdistribusjonene.

Du fjerner blokkeringen av dette problemet og tilbakestiller bestillingen til en *Utkast*-tilstand ved å gå til **Innkjøp og leverandører \> Periodiske oppgaver \> Opprydding \> Tilbakestill bestillingsdistribusjon**. Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Løse bestillingsdistribusjonsfeil i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Kan jeg bare vise bestillinger som jeg har opprettet?

Denne funksjonen er ikke tilgjengelig nå.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Kan jeg reservere lager og opprette transaksjoner mot registrert lager i en bestilling?

### <a name="issue-description"></a>Problembeskrivelse

Selv når varene er i en *Registrert*-tilstand på en bestilling, kan du likevel reservere lageret. Du kan med andre ord opprette transaksjoner mot det registrerte lageret.

### <a name="reproduce-the-issue"></a>Reprodusere problemet

Følgende prosedyre viser én måte å reprodusere problemet på.

1. Opprett en bestilling.
2. Registrere bestillingslinjen.
3. Legg merke til at du kan generere reservasjoner eller transaksjoner mot det registrerte lageret.

### <a name="issue-resolution"></a>Problemløsning

Denne virkemåten er standard. Forventningen er at de registrerte varene fysisk har ankommet på lageret, og at de derfor er tilgjengelige for reservasjon.

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Bestillinger reflekterer ikke språkinnstillingene til den juridiske enheten.

### <a name="issue-description"></a>Problembeskrivelse

Produktnavnet på en bestilling vises på systemspråket i stedet for språket som er angitt for den juridiske enheten der bestillingen ble opprettet.

### <a name="reproduce-the-issue"></a>Reprodusere problemet

Følgende prosedyre viser én måte å reprodusere problemet på.

1. Sett systemspråket til *EN-US* (amerikansk engelsk).
1. Kontroller at det finnes et produkt der språkene *EN-US* og *DE* (tysk) blir vedlikeholdt for oversettelser av produktnavnet.
1. Endre språket for en juridisk enhet til *DE*.
1. I den juridiske enheten der *DE* er angitt som språk, oppretter du en bestilling som inkluderer produktet.
1. Legg merke til at produktnavnet fremdeles vises på amerikansk engelsk (systemspråket).

### <a name="issue-resolution"></a>Problemløsning

Denne virkemåten er standard. I bestillinger vises produktet alltid på systemspråket. Bestillingsspråket brukes når det opprettes en bekreftelsesjournal.

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a>Listen over godkjente leverandører per produktenhet tillater ikke at ikrafttredelsesdatoen endres.

### <a name="issue-description"></a>Problembeskrivelse

Et produkt har en godkjent leverandør som for eksempel har gyldighetsdato 11. januar 2018 (*01/11/2018*) og utløpsdatoen *Aldri*. Hvis du prøver å endre ikrafttredelsesdatoen til 10. januar 2018 (*01/10/2018*) eller 12. januar 2018 (*01/12/2018*), får du følgende feilmelding:

> Kan ikke opprette en post i liste over godkjente leverandører (PdsApproveVendorList). Verdien for utløpsdato må være større enn eller lik verdien for gyldighetsdato.

### <a name="issue-resolution"></a>Problemløsning

Du kan bare forlenge perioden leverandøren er godkjent for. Følgende regler gjelder:

- Hvis du vil endre ikrafttredelsesdatoen slik at den er tidligere enn noen av de eksisterende postene (perioder) for vareleverandøren, må utløpsdatoen for den nye perioden være før alle utløpsdatoene i de eksisterende postene.
- Hvis du vil endre utløpsdatoen slik at den er senere enn noen av de eksisterende periodene, må ikrafttredelsesdatoen være etter den seneste utløpsdatoen i alle eksisterende poster.
- Hvis du vil redusere den overordnede perioden som leverandøren er godkjent for, må du slette eller endre eksisterende poster. Du kan også bruke bryteren for **avkorting** under import. Denne bryteren sletter alle eksisterende poster i tabellen for godkjente leverandører etter vare.

For eksempel scenarioet som er beskrevet i problembeskrivelsen, der en post har en gyldighetsdato på *01/11/2018* og utløpsdatoen *Aldri*, kan du importere en ny post som har en gyldighetsdato på *01/10/2018* og utløpsdatoen *Aldri*. Du kan imidlertid ikke redusere perioden slik at ikrafttredelsesdatoen oppdateres til *01/12/2018* via databehandling. Du må gjøre denne endringen i brukergrensesnittet.

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-name-isnt-synced"></a>Etter at jeg endret leveringsadressen i et bestillingshode, blir ikke leveringsnavnet synkronisert.

### <a name="issue-description"></a>Problembeskrivelse

Adressen på hodet til en bestilling oppdateres til en adresse som ikke er en leveringsadresse. Selv om adressen oppdateres på bestillingen, oppdateres ikke leveringsnavnet basert på den oppdaterte adressen.

### <a name="issue-resolution"></a>Problemløsning

Denne virkemåten er standard. Den valgte adressen må klassifiseres som leveringsadresse. Hvis ikke oppdateres ikke leveringsnavnet basert på den valgte adressen.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Kan jeg finne brukeren som annullerte en bestilling?

Denne informasjonen spores bare hvis bestillingen er underlagt endringsstyring. Hvis du bruker endringsstyring, kan du se hvem som sendte inn endringen (annulleringen), og hvem som godkjente den.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
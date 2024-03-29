---
title: Kopier leverandører ved hjelp av delte nummerserier
description: Denne artikkelen forklarer hvordan du bruker delte nummerserier til å kopiere en leverandør til en annen juridisk enhet og samtidig beholde samme leverandør-ID.
author: sunfzam
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7b7285cdf454955656c4fb20c3abf68f3f9c39dc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904908"
---
# <a name="copy-vendors-by-using-shared-number-sequences"></a>Kopier leverandører ved hjelp av delte nummerserier

[!include [banner](../includes/banner.md)]

Du kan bruke delte nummerserier til å tilordne leverandør-ID-er. Delte nummerserier lar deg også kopiere leverandører fra én juridisk enhet til en annen juridisk enhet, og bruke samme leverandør-ID-er i begge juridiske enheter.

## <a name="setup"></a>Oppsett

Funksjonen er aktivert når du bruker en delt nummerserie til å tilordne leverandør-ID-er. Du må bruke samme nummerserie i alle juridiske enheter som du vil kopiere en leverandør til. Du kan endre leverandørnummerserien på siden **Leverandørparametere** for hver juridiske enhet. Velg **Leverandører** \> **Oppsett** \> **Leverandørparametere**, og velg deretter fanen **Nummerserier**.

Du kan også definere leverandørnummerserier for hver leverandørgruppe. Disse nummerseriene må også være delt. Nummerrekkefølgen for en leverandørgruppe brukes først. Hvis ingen nummerserie er angitt for en leverandørgruppe, brukes nummerserien som er angitt på siden **Leverandørparametere**.

Du kan også kopiere leverandører mellom juridiske enheter hvis du bruker manuelle leverandør-ID-er. Hvis du imidlertid prøver å kopiere en leverandør til en juridisk enhet der leverandør-ID-en allerede finnes, starter ikke kopieringen.

## <a name="copy-a-vendor"></a>Kopiere en leverandør

Hvis du vil kopiere en leverandør, velger du **Ny** på listesiden **Alle leverandører** for å åpne siden **Alle leverandører, ny post**. Den nye leverandør-ID-en tilordnes ikke umiddelbart. Denne virkemåten skiller seg fra virkemåten i tidligere versjoner. Riktig nummerserie å bruke kan ikke fastslås fordi du ennå ikke har valgt leverandørgruppe. I tillegg kan det heller ikke fastslå om du prøver å opprette en ny leverandør eller kopiere en leverandør. Derfor tilordnes ikke leverandør-ID-en før du velger **Lagre** nederst på siden.

Hvis du oppretter en ny leverandør, kan du fortsette å fylle ut alle feltene på vanlig måte. Når du er ferdig og du velger **Lagre**, tildeles leverandør-ID-en automatisk. For manuelle nummerserier ser du også at den manuelle leverandør-ID-en ble brukt.

Hvis du vil kopiere en leverandør, går du til feltet **Navn** og angir ett eller flere tegn som representerer leverandøren som du leter etter. En dialogboks for søk viser en liste over parter som kan representere leverandøren du leter etter. Når du velger en av partene, vises tilleggsinformasjon til høyre i dialogboksen:

- Fanen **Generelt** viser partens telefonnummer og adresse.
- Fanen **Roller** viser rollene som den valgte parten kan ha, og den juridiske enheten der den har hver rolle.
- Fanen **ID for mva-registrering** viser ID-er for mva-registrering som er tilordnet til parten.

Du kan kopiere en part bare hvis den har en leverandørrollen og hvis den har denne rollen i en juridisk enhet som ikke er gjeldende juridisk enhet. Følg denne fremgangsmåten når du finner en part som oppfyller disse kriteriene.

1. Alternativet **Kopier leverandør** vises. Dette alternativet er satt til **Nei** som standard. Hvis du vil kopiere leverandør til gjeldende juridisk enhet, setter du alternativet til **Ja**. 
2. Feltet **Juridisk enhet** vises. Velg den juridiske enheten du skal kopiere leverandøren fra. Hvis leverandøren finnes i bare én juridisk enhet, er feltet satt til den juridiske enheten som standard.
3. Velg **Velg**. Den nye leverandøren opprettes.

## <a name="validation"></a>Validering

Når du kopierer en leverandør, forsøkes det å lagre den nye leverandørinformasjonen. Valideringer kjøres for å bekrefte at dataene som ble kopiert, er korrekte. Du får en feilmelding for hver validering som mislykkes. Feilmeldingene forklarer hvilken informasjon som må oppdateres. Kopien av leverandøren kan ikke lagres før du retter alle valideringsfeilene.

## <a name="copy-a-vendor-by-using-the-tax-exempt-number-search-feature"></a>Kopiere en leverandør ved hjelp av søkefunksjonen for mva-organisasjonsnummer

Du kan også kopiere leverandører ved hjelp av søkefunksjonen for **mva-organisasjonsnummer** i gruppen **Registrering** i fanen **Leverandør** i handlingsruten på siden **Alle leverandører**. Dialogboksen for **søk etter mva-organisasjonsnummer** som vises, viser mva-organisasjonsnumre, leverandør-ID, leverandørnavn og den juridiske enheten der ID-en for mva-organisasjonsnummeret brukes. Du kan kopiere en leverandør bare hvis den er i en juridisk enhet som ikke er gjeldende juridisk enhet. Følg fremgangsmåten nedenfor når du har valgt en leverandør som oppfyller dette kriteriet.

1. Alternativet **Kopier leverandør** vises. Dette alternativet er satt til **Nei** som standard. Hvis du vil kopiere leverandør til gjeldende juridisk enhet, setter du alternativet til **Ja**.
2. Velg **Velg**. Den nye leverandøren opprettes.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

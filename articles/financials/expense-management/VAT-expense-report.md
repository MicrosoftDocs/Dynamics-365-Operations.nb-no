---
title: Mva-fradrag i Reiseregning og utlegg
description: "Dette emnet forklarer hvordan du kan få refusjoner for transaksjoner som er kvalifisert for mva-refusjon."
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: d1c9357f8f51e1a87aebeb8f802dbe3b5fdd5aa0
ms.contentlocale: nb-no
ms.lasthandoff: 03/13/2018

---

# <a name="vat-recovery-in-expense-management"></a>Mva-fradrag i Reiseregning og utlegg

[!include [banner](../includes/banner.md)]

For å motta refusjoner for transaksjoner som er kvalifisert for mva-refusjon, må et firma eller organisasjon identifisere, samle inn, kontrollere og sende nøyaktig informasjon. Denne prosessen omfatter flere oppgaver, og avhengig av størrelsen på firmaet ditt, kan den omfatte flere ansatte eller roller.

Hvis du vil få refusjon for mva ved hjelp av Reiseregning og utlegg, må følgende forutsetninger være tilstede:

- Mva-koder må opprettes for land/regioner som er tilordnet til utgiftskategorier.
- En mva-gruppe må opprettes for hver mva-kode.
- En mva-kode for vare må opprettes for hver mva-gruppe.

Når forutsetningene er tilstede, gjør ansatte følgende for å be om refusjoner for mva-transaksjoner.

1. I en reiseregning kan du angi avgiftsinformasjon om kredittkorttransaksjoner som er kvalifisert for mva-refusjon.
2. Kontroller at all avgiftsinformasjon er oppgitt, og poster deretter reiseregningen.
3. Behandle utgifter som er kvalifisert for internasjonal mva-refusjon.
4. Send data om mva-refusjon til tredjepartsleverandører for å søke om internasjonal refusjon.
5. Behandle utgifter for innenlandsk mva-refusjon.

Delene nedenfor inneholder eksempler som viser hvordan Contoso-ansatte har fullført hvert trinn.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>I en reiseregning kan du angi avgiftsinformasjon om kredittkorttransaksjoner som er kvalifisert for mva-refusjon

Nina, en selger hos Contoso som er basert i USA, kom nettopp tilbake fra en forretningsreise til Storbritannia. Mens hun var på reise brukte hun sitt eget kredittkort for å betale for måltider. Nina må nå opprette en reiseregning for å kunne avstemme utgiftene.

Når Nancy registrerer informasjon om reiseregningen, velger hun **Storbritannia** i feltet **land/område** på siden  **Rediger reiseregning**. Listen over mva-grupper blir deretter filtrert slik at den viser bare gruppene som gjelder for Storbritannia. Nina velger mva-gruppen **Storbritannia 001**, og deretter velger hun mva-gruppen **Måltider**. Hun legger deretter til en ny transaksjon for overnattingene. Fordi det bare er én mva-gruppe og mva-gruppe for vare for overnatting i Storbritannia, blir denne informasjonen automatisk fylt ut i Nancys reiseregning.

Det er en Contoso-policy at alle utgifter må ha et samsvarende mottak. Når Nancy lagrer reiseregningen, får hun derfor en melding om at hun må knytte en kvittering til hver transaksjon som står oppført i reiseregningen. Nina kontrollerer at hun har knyttet et digitalt bilde av hver transaksjonskvittering til reiseregningen, og sender deretter rapporten for godkjenning. Hun sender så orginalene til fakturabehandlingsteamet. Dette teamet sender informasjonen om mva-refusjon videre til tredjepartsleverandører som sender en søknad om fradragsberettigede MVA-tilbakebetalinger for Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Kontroller at all avgiftsinformasjon er oppgitt, og poster deretter reiseregningen

April, leverandørkoordinator for Contoso, må angi avgiftsinformasjon som mangler i reiseregninger før regningen kan posteres. Hun åpner **Reiseregningdetaljer**-siden og ser Nancys godkjente reiseregning. April åpner reiseregningen for å se transaksjonsdetaljene. Hun ser at Nancy ikke har angitt en mva-gruppe for vare for én av transaksjonene. Fordi denne informasjonen ikke er angitt, kan April ikke postere reiseregningen. Derfor ser April på siden **mva-konfigurasjoner**  i Reiseregning og utlegg, og finner riktig mva-gruppe for vare for landet/området, og transaksjonstypen. Så kan April postere reiseregningen til økonomimodulen.

Når April posterer reiseregningen, opprettes et arbeidselement for mva-refusjon. Dette arbeidselementet er tilordnet til et medlem av Back Office-teamet. April mottar en melding som bekrefter at posteringen var vellykket. Denne meldingen viser også hvor mange mva-transaksjoner som ble identifisert for gjenoppretting.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Behandle utgifter som er kvalifisert for internasjonal mva-refusjon

Magnus, et medlem av gruppen til Contosos Back Office behandlingsteamet, er ansvarlig for å bekrefte at all nødvendig informasjon for merverdiavgift er inkludert i reiseregninger. Han åpner siden **Avgiftsfradrag for utgifter** og velger reiseregningen som Nancy har sendt inn. Magnus bekrefter at alle nødvendige kvitteringene er vedlagt, og at riktig mva-gruppe og mva-koder for vare er angitt.

Når Magnus mottar orginalene fra Nancy, kontrollerer han orginalene mot de digitale kvitteringene og endrer deretter statusen for reiseregningen til **Klar for fradrag**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Send data om mva-refusjon til tredjepartsleverandører for å søke om internasjonal refusjon

Når Magnus er klar til å sende utgiftsrapportdata til tredjepartsleverandører som skal sende inn søknader om mva-fradrag, han åpner siden **Avgiftsfradrag for utgifter**. Han filtrerer siden slik at den bare viser reiseregningene som er merket som **Klar for fradrag**. Så velger Magnus **Fil** &gt; **Eksporter til Excel**. Mva-informasjonen fra reiseregningene eksporteres til et Excel-regneark. Magnus sender regnearket til en tredjeparts-leverandør og inkluderer en melding om at orginalene er sent med bud.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Behandle utgifter for innenlandsk mva-refusjon

Magnus må kontrollere at transaksjonene for reiseregningen er kvalifisert for mva-refusjon og at de digitale kvitteringene er knyttet til regningene. For å behandle kvalifiserte utgifter for innenlandsk refusjon, åpner Magnes siden **Avgiftsfradrag for utgifter** og velger reiseregningen som krever verifisering. Han kontrollerer at kvitteringene står registrert på bedriften, og ikke på den ansette. For mva-fradrag må kvitteringene registreres på selskapet. Magnus bekrefter deretter at riktig mva-gruppe og mva-koder for vare ble brukt.

Når Magnus mottar orginalene, endrer han statusen for reiseregningen til **Klar for fradrag**. Han kan deretter sende refusjonen til den riktige skattemyndigheten. I dette tilfellet er den rette skattemyndighet i USA tjenesten IRS (Internal Revenue).


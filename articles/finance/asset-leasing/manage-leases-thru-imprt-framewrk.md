---
title: Administrere leie via rammeverket for leieimport
description: Dette emnet forklarer hvordan du bruker rammeverket for leieimport til å justere flere leieavtaler samtidig.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseImportHeader
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 083adf0a4bb74ac65e6f8b5077f65c74eb3fa337
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880916"
---
# <a name="manage-leases-through-the-lease-import-framework"></a>Administrere leie via rammeverket for leieimport

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du bruker rammeverket for leieimport til å justere flere leieavtaler i ett trinn. Ved å bruke denne funksjonen kan du spare tid, og du kan også sikre mer nøyaktige justeringer ved å redusere faren for menneskelige feil. I tillegg kan denne funksjonen koble Microsoft Dynamics 365 Finance sammen med eksterne dataenheter for å kunne laste opp data effektivt.

Følgende dataenheter kan brukes til å integrere aktivaleie med eksterne systemer:

- Leieklargjøring
- Klargjøring av betalingskontrakt
- Klargjøring av fullbyrdelseskontrakt

Du kan bruke importprosessen til å justere en leieavtale, oppdatere ikke-økonomisk informasjon eller legge til nye leieavtaler. Du kan vise og redigere leiedataene før du importerer dem.

Systemet kan kjøre følgende tre prosesser via leieimportserien.

| Prosesstype  | beskrivelse |
|---------------|-------------|
| Legge til post    | Overførte leieavtaler som har denne prosesstypen, oppretter en leieavtale i systemet. Betalingsplanen må bekreftes manuelt, og journaloppføringen for opprinnelig føring må posteres manuelt etter overføringen. |
| Oppdater post | Overførte leieavtaler som har denne prosesstypen, oppdaterer feltverdier for en leieavtale som allerede finnes i systemet. Bare feltene som er valgt på siden for **Oppdater feltvalg**, oppdateres. Vi anbefaler at du velger ikke-finansielle felt på siden for **Oppdater feltvalg**, fordi denne prosesstypen ikke justerer leieavtalen. |
| Juster post | Overførte leieavtaler som har denne prosesstypen, justerer leieavtalen. Denne justeringen fører til en finansiell endring av leieavtalen. Når leieavtalen er behandlet, oppretter systemet en ny betalingsplan ved å bruke de nye dataene fra leieimportserien. Systemet bekrefter ikke betalingsplanen eller posterer justeringsjournaloppføringen. |

Når informasjonen er lastet opp via **Databehandling**-arbeidsområdet, åpner du siden **Importhode** (**Aktivaleie \> Rammeverk for import av leieavtale \> Importhode**). Denne siden viser alle importer av de tre dataenhetene som ble vist tidligere.

Hvis du vil vise leieroppsamlingsdata før behandling kjøres, velger du **Oppsamlingsdata**.

Med sammenligningsfunksjonen kan du sammenligne en post du skal importere, med den tilsvarende posten som allerede finnes i systemet. Hvis du vil sammenligne en enkelt leieoppføring, velger du en leieavtale og deretter **Sammenlign**. Du bør fullføre dette trinnet for å generere en **Forskjeller**-rapport før du overfører leiepostene. Sammenligningsfunksjonaliteten sammenligner verdiene i oppsamlingsdataene med verdiene for leieavtaler som for øyeblikket finnes i systemet.

> [!NOTE]
> Sammenligningsfunksjonaliteten fungerer ikke for leieavtaler som har prosesstypen **Legg til post**, fordi det ikke er noe å sammenligne mot denne leieavtalen.
>
> Hvis du vil sammenligne flere leieavtaler samtidig, går du til **Aktivaleie \> rammeverket for import av leieavtale \> Periodisk**, og deretter velger du **Sammenlign**.

For hver enhet kan du vise forskjellene mellom det som finnes i systemet, og det som finnes i oppsamlingstabellene. Velg **Vis forskjeller** for hver enhet i oppsamlingstabellene. Dialogboksen som vises, viser den gjeldende verdien og den foreslåtte oppsamlingsverdien.

Du kan også oppdatere oppsamlingsverdien ved å endre den i kolonnen **Ny verdi** og deretter velge valget for **Oppdater oppsamling**.

Du kan validere leieavtaler for å sikre at postene kan hentes inn i systemet uten å introdusere feil. Før en leieavtale overføres, kjører systemet flere valideringer for å sikre at posten blir importert. Velg **Valider** for å validere en enkelt leieavtale.

> [!NOTE]
> Hvis du vil validere flere leieavtaler samtidig, går du til **Aktivaleie \> rammeverket for import av leieavtale \> Periodisk**, og deretter velger du **Valider**.

Hvis du vil behandle en enkelt leieavtale, velger du å **overføre leieposter** på siden **Importhode**. Når en leieavtale overføres, utfører systemet handlingen som er angitt i **Prosesstype**-feltet.

> [!NOTE]
> Hvis du vil overføre flere leieavtaler samtidig, går du til **Aktivaleie \> rammeverket for import av leieavtale \> Periodisk**, og deretter velger du **Overfør**.

Når leieavtalene er sammenlignet, kan du kjøre en rapport for å vise forskjellene for hver leieavtale som er inkludert i import-IDen. Hvis du vil kjøre rapporten for én leieavtale, velger du leieavtalen i oppsamlingsdataene, og deretter velger du **sammenlign og vis rapport \> rapport om forskjeller**.

> [!NOTE]
> Hvis du vil sammenligne flere leieavtaler samtidig, går du til **Aktivaleie \> rammeverket for import av leieavtale \> Periodisk**, og deretter velger du **Sammenlign**. 

## <a name="set-up-update-fields"></a>Definere oppdateringsfelt

Hvis du bruker rammeverket for import av leieavtale til å oppdatere leieavtaler, og prosesstypen er **Oppdater post**, kan du velge bestemte felt som skal oppdateres.

1. Gå til **Aktivaleie \> rammeverket for leieimport \> Oppsett \> Oppdater feltvalg**.
2. På siden som vises, velger du feltene som skal oppdateres, og deretter velger du den grønne pilen for å flytte dem til listen for **Valgte felt**. Bare felt i listen for **Valgte felt** kan oppdateres ved å bruke leieimportserien.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

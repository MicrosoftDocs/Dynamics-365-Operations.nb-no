---
title: Abonner-modul
description: Dette emnet dekker abonneringsmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e70bc01d4c662d08a9171a9d2feb0e2f7901ccbb
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479515"
---
# <a name="subscribe-module"></a>Abonner-modul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet dekker abonneringsmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

Moduler som er forskjellige, kan brukes på områdesider for å registrere kundeinformasjon for nyhetsbrev eller kampanjer.

Illustrasjonen nedenfor viser et eksempel på en abonneringsmodul i bunnteksten til en Adventure Works-områdeside.

![Eksempel på en abonneringsmodul i bunnteksten til en Adventure Works-områdeside](./media/Subscribe.PNG)

> [!IMPORTANT]
> - Abonneringsmodulen er tilgjengelig i Commerce-modulbiblioteket fra Dynamics 365 Commerce 10.0.20-versjonen.
> - Abonneringsmodulen presenteres i Adventure Works-emnet.
> - Abonneringsmodulen krever en utvidelse av datahandling for å fungere med noen e-postleverandører for markedsføring, slik at nyhetsbrev eller kampanje-e-poster kan sendes etter at kundeinformasjonen er registrert.

## <a name="subscribe-module-properties"></a>Egenskaper for abonneringsmodul

| Egenskapsnavn | Verdier | beskrivelse |
|---------------|--------|-------------|
| Overskrift       | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | En tekstoverskrift for abonneringsmodulen, for eksempel **Abonner på nyhetsbrevet** eller **Registrer deg og få10 % i rabatt**. |
| Avsnitt     | Avsnittstekst | Abonneringsmodulen støtter paragraftekst i rikt tekstformat, for å gi flere opplysninger om handlingsoppfordringen i overskriften. |

## <a name="add-a-subscribe-module-to-a-new-page"></a>Legge til en abonneringsmodul på en ny side

Hvis du vil legge til en abonneringslistemodul på en ny side og angi de nødvendige egenskapene i Commerce-områdebyggeren, følger du disse trinnene.

1. Gå til **Maler**, og åpne markedsføringsmalen for områdets hjemmeside (eller opprett en ny markedsføringsmal).
1. I **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Abonner**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og åpne områdets hjemmeside (eller opprett en ny hjemmeside ved hjelp av markedsføringsmalen).
1. På **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Abonner**-modulen, og deretter velger du **OK**.
1. Legg til en overskrift i egenskapsruten for abonneringsmodulen, for eksempel **Abonner**.
1. Legg til avsnittetstekst, for eksempel **Siste trender, stiler og kampanjer. Er du på listen? Abonner og få de siste avtalene!**
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Adventure Works-tema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

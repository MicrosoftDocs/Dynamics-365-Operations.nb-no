---
title: NMFC-koder (National Motor Freight Classification)
description: Dette emnet beskriver hvordan du arbeider med NMFC-koder (National Motor Freight Classification) i Microsoft Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 8e6aac6b3a8b730b6adc5c3d4410b98c3e8d5090eac866c337ed1d03409ba765
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731157"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a>NMFC-koder (National Motor Freight Classification)

[!include [banner](../includes/banner.md)]

NMFC-koder (National Motor Freight Classification) hjelper deg med å klassifisere varer som kan sendes. NMFC-koden er en betegnelse som brukes til å gruppere varer. På denne måten kan transportfirmaer evaluere varer for forsendelse ved å klassifisere varer basert på hensyn som lastebilegenskaper, lasteproblemer, håndteringsproblemer og forgjengelighet. Varer grupperes i én av 18 fraktklasser ved hjelp av en rekke tall, fra 50 til 500. Klassen som en vare grupperes i, er basert på evaluering av fire transportegenskaper: tetthet, oppbevaringsevne, håndtering og skyld. Til sammen fastsetter disse egenskapene varens transporterbarhet.

En NMFC-kode er tilknyttet alle forsendelsesvarene som er mindre enn vognlastklasser (LTL). En bærbar datamaskin kan for eksempel være tilordnet en NMFC som er klasse 2.5, mens strømkabler kan være tilordnet en NMFC som er klasse 65.

Denne funksjonen kan hjelpe arbeidere med å bruke NMFC-koder til å klassifisere LTL-forsendelsesvarer. Her er noen eksempler:

- Hvis firmaet inneholder en fraktbeskrivelse på fraktbrevet, vil transportøren ha en anelse om hva frakten er. Frakt er en viktig klassifisering, fordi mange transportfirmaer baserer hele forretningsmodellen på hvilke typer frakt de sender.
- Denne klassifiseringen kan være vesentlig for ditt firma fordi den brukes til å avgjøre kostnadene ved en gitt last.
- Firmaet kan identifisere lønnsomheten til et LTL-logistikk- og transportfirma.

Dette emnet beskriver hvordan du arbeider med NMFC-koder i Microsoft Dynamics 365 Supply Chain Management.

## <a name="prerequisites"></a>Forutsetninger

Før du kan opprette NMFC-koder må du konfigurere alle LTL-fraktklassene som må tilordnes dem. LTL-fraktklasser representerer varekategorier, mens NMFC-koder er relatert til bestemte varer i hver av de 18 fraktklassene. Hvis du vil ha mer informasjon om hvordan du arbeider med LTL-klasser, kan du se [Mindre enn vognlastklasser](ltl-class.md).

## <a name="create-an-nmfc-code"></a>Opprette en NMFC-kode

Hvis du vil opprette en NMFC-kode, følger du disse trinnene.

1. Følg ett av disse trinnene:

    - Gå til **Lagerstyring \> Oppsett \> Lager \> NMFC-koder**.
    - Gå til **Transportstyring \> Oppsett \> Transportstandarder \> NMFC-koder**.

1. Velg **Ny** for å opprette en NMFC-kode. Deretter angir du følgende felt:

    - **NMFC-kode** – Angi NMFC-koden for varetypen.
    - **Navn** – Angi et navn for NMFC-koden.
    - **LTL-klasse** – Velg LTL-klassen som er knyttet til NMFC-koden.
    - **BOL-håndteringsenhet** – Definer standard håndteringstype for forsendelsen.

## <a name="example-set-up-nmfc-codes"></a>Eksempel: Definer NMFC-koder

Følgende eksempel viser hvordan du konfigurerer to ulike NMFC-koder som du kan brukes med forskjellige produkter.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> NMFC-koder**.
1. Velg **Ny** i handlingsruten.
1. På den nye linjen angir du følgende verdier:

    - **NMFC-kode:** *92.5*
    - **Navn:** *Datamaskiner*
    - **LTL-klasse:** *92.5*
    - **BOL-håndteringsenhet:** *Enhet*

1. Velg **Lagre** i handlingsruten.
1. Velg **Ny** i handlingsruten.
1. På den nye linjen angir du følgende verdier:

    - **NMFC-kode:** *125*
    - **Navn:** *Telefoner*
    - **LTL-klasse:** *125*
    - **BOL-håndteringsenhet:** *Enhet*

1. Velg **Lagre** i handlingsruten.

## <a name="additional-resources"></a>Tilleggsressurser

- [Mindre enn vognlastklasser](ltl-class.md)
- [Opprette et fraktbrev](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Du kan ikke bruke en mal på et frigitt produkt
description: Du kan ikke bruke en mal på et frigitt produkt.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026772"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a>Du kan ikke bruke en mal for å opprette et frigitt produkt

KB-nummer: 4612097

## <a name="symptoms"></a>Symptomer

Når du oppretter et nytt frigitt produkt ved hjelp av dialogboksen **Nytt frigitt produkt**, kan du velge en mal. Malen skal angi standardinnstillinger for mange felt i det nye frigitte produktet. Noen eller alle feltene velges imidlertid ikke etter at du har valgt malen.

## <a name="cause"></a>Årsak

På mange sider i Microsoft Dynamics 365 Supply Chain Management kan du opprette en mal som oppretter innledende innstillinger for postene som vises på disse sidene. Du kan opprette én av disse malene ved å velge **Postinformasjon** i kategorien **Alternativer** i handlingsruten. Frigitte produkter er imidlertid mye mer komplekse enn de fleste andre typer poster. Selv om du kan velge **Postinformasjon** på siden **Frigitte produkter** for å opprette en mal, og selv om du kan velge den malen når du oppretter et frigitt produkt, vil ikke malen gi de forventede feltverdiene for det nye frigitte produktet. Derfor kan du ikke bruke postinformasjon-maler for frigitte produkter. I stedet må du opprette dedikerte produktmaler.

## <a name="resolution"></a>Oppløsning

Hvis du vil opprette en produktmal, bruker du **Mal**-menyen i kategorien **Produkt** i handlingsruten, og ikke **Postinformasjon**-knappen i kategorien **Alternativer**.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. I handlingsruten i kategorien **Produkt** i gruppen **Ny**, velger du **Mal**, og velg deretter enten **Opprett personlig mal** eller **Opprett delt mal** etter behov.

---
title: Omklassifisere den kortsiktige delen av en leieforpliktelse
description: Dette emnet forklarer hvordan du oppretter en månedlig journaloppføring for å reklassifisere en del av leieforpliktelsen som kortsiktig.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3a71b809b4bb16c2b918b7acd4fbb8bc49278ff6
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727741"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>Omklassifisere den kortsiktige delen av leieforpliktelse

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du oppretter en månedlig journaloppføring for å reklassifisere en del av leieforpliktelsen som kortsiktig. Når planen som er valgt i den satsvise prosessen, er **Omklassifisering av kortsiktig leieforpliktelse**, opprettes det en journaloppføring. Denne oppføringen brukes til å postere den gjeldende delen av leieforpliktelsen på den siste dagen i måneden. Samtidig posteres en tilbakeføringspost per den første dagen i neste måned.

Den kortsiktige delen av leieforpliktelsen vises i tidsplanen for nedbetalingsplanen for gjeld. Når journaloppføringen posteres, blir kolonnen for **journal for omklassifisering av gjeld opprettet** tilgjengelig, og journal-IDen blir også fylt ut på tidsplanen.

Følg denne fremgangsmåten for å opprette og postere en journaloppføring for omklassifisering av kortsiktig gjeld.

1. Gå til **Aktivaleie \> Periodisk \> Opprettelse av bunkejournal**.
2. I dialogboksen **Opprettelse av bunkejournal**, i feltet for **Velg tidsplan**, velger du **Omklassifisering av kortsiktig leieforpliktelse**.
3. I feltet **Leiegruppe** velger du en leiegruppe. Du kan også velge tablå-ID i feltet **Tablå-ID**.
4. Aktiver **Post**-parameteren. Hvis posten skal opprettes, men ikke posteres, lar du denne parameteren være deaktivert.
5. Velg **OK**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Opprette en produktnummerterminologi for konfigurerte produktvarianter
description: Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7711d9832288327e700acd47fb30cce0c76e5e9a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568405"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>Opprette en produktnummerterminologi for konfigurerte produktvarianter

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard. Prosedyren viser også hvordan du kan bygge konfigurasjonsterminologi for en komponent i en produktkonfigurasjonsmodell. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Den nye produktnummerterminologien tilordnes til produktstandarden D0004. Denne oppgaven vil vanligvis bli utført av en produktdesigner.

## <a name="create-a-product-number-nomenclature"></a>Opprette produktnummerterminologi

1. Gå til **Behandling av produktinformasjon \> Oppsett \> Produktterminologi**.
1. Velg **Ny**.
1. Skriv inn en verdi i **Navn**-feltet.
1. Skriv inn en verdi i **Beskrivelse**-feltet.
1. Velg **Legg til**.
1. Velg **Produktstandardnummer**.
1. Velg **Legg til**.
1. Velg **Tekstkonstant**.
1. Merk den valgte raden i listen.
1. Skriv inn en verdi i **Tekst**-feltet.
1. Velg **Legg til**.
1. Velg **Konfigurasjon**.
1. Lukk siden.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Tilordne produktnummerterminologien til en produktstandard

1. Gå til **Behandling av produktinformasjon \> Produkter \> Produktstandarder**.
1. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på **Produktnummer**-feltet med verdien D.
1. Velg koblingen i den valgte raden i listen.
1. Velg **Rediger**.
1. Velg *Ja* i feltet **Bruk nomenklatur**.
1. Angi eller velg en verdi i feltet **Produktvariantnummerterminologi**.
1. Lukk siden.
1. Lukk siden.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Opprette terminologi for en komponent i en produktkonfigurasjonsmodell

1. Gå til **Behandling av produktinformasjon \> Produkter \> Produktkonfigurasjonsmodeller**.
1. Finn og velg ønsket post i listen.
1. Velg koblingen i den valgte raden i listen.
1. Velg **Rediger**.
1. Velg *Ja* i feltet **Bruk konfigurasjonsnomenklatur**.
1. Velg **Legg til**.
1. Velg **Attributtverdi**.
1. Merk den valgte raden i listen.
1. Angi eller velg en verdi i feltet **Attributt**.
1. Velg **Legg til**.
1. Velg **Tekstkonstant**.
1. Merk den valgte raden i listen.
1. Skriv inn en verdi i **Tekst**-feltet.
1. Velg **Legg til**.
1. Velg **Attributtverdi**.
1. Merk den valgte raden i listen.
1. Angi eller velg en verdi i feltet **Attributt**.
1. Velg **Legg til**.
1. Velg **Tekstkonstant**.
1. Merk den valgte raden i listen.
1. Skriv inn en verdi i **Tekst**-feltet.
1. Velg **Legg til**.
1. Velg **Attributtverdi**.
1. Merk den valgte raden i listen.
1. Angi eller velg en verdi i feltet **Attributt**.
1. Velg **Legg til**.
1. Velg **Tekstkonstant**.
1. Merk den valgte raden i listen.
1. Skriv inn en verdi i **Tekst**-feltet.
1. Velg **Legg til**.
1. Velg **Attributtverdi**.
1. Merk den valgte raden i listen.
1. Angi eller velg en verdi i feltet **Attributt**.
1. Velg **Legg til**.
1. Velg **Tekstkonstant**.
1. Merk den valgte raden i listen.
1. Skriv inn en verdi i **Tekst**-feltet.
1. Velg **Legg til**.
1. Velg **Nummerserieverdi**.
1. Merk den valgte raden i listen.
1. Angi eller velg en verdi i **Nummerserieverdi**-feltet.
1. Lukk siden.
1. Lukk siden.
1. Lukk siden.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
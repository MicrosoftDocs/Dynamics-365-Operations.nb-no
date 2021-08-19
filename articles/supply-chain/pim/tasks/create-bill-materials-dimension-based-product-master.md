---
title: Opprette en stykkliste for en dimensjonsbasert produktstandard
description: For denne prosedyren skal du har fullført de 4 forrige veiledningene i disse trinnene med åtte registreringer.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 696cb96c6e934eaa44bfe6f51347df4541e5648f75f1ce07139787a1b235d69d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715777"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Opprette en stykkliste for en dimensjonsbasert produktstandard

[!include [banner](../../includes/banner.md)]

For denne prosedyren skal du har fullført de 4 forrige veiledningene i disse trinnene med åtte registreringer. De 4 første registreringene definerer dataene som kreves for å fullføre denne prosedyren. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne oppgaven håndteres vanligvis av produktdesigneren.

## <a name="select-the-product"></a>Velg produkt

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Merk den valgte raden i listen.
    * Finn den frigitte produktstandarden med dimensjonsbasert konfigurasjonsteknologi, som du opprettet i den første oppgaveveiledningen i disse trinnene.  
1. Velg **Utvikle** i handlingsruten.
1. Velg **BOM-versjoner**.

## <a name="create-new-bom-and-bom-version"></a>Opprette ny stykkliste og stykklisteversjon

1. Velg **Ny**.
1. Velg **Stykkliste og stykklisteversjon**.
1. Skriv inn en verdi i **Navn**-feltet.
    * Angi et område  
    * Vi angir ikke et bestemt område for stykklisten i denne prosedyren.  
1. Velg **OK**.
1. Velg **Ny**.
    * I denne fremgangsmåten skal vi legge til fire linjer i stykklisten. To linjer representerer kabelalternativer og to linjer representerer kabinettalternativer.  
1. Merk den valgte raden i listen.
1. Angi eller velg en verdi i **Varenummer**-feltet.
    * Velge varenummer A0001, HDMI 6' Kabler.  
1. Angi eller velg en verdi i feltet **Konfigurasjonsgruppe**.
    * Velg konfigurasjonsgruppen Kabel, som ble opprettet i veiledning 4 i disse trinnene.  
1. Velg **Ny**.
    * Velge varenummer A0002, HDMI 12' Kabler.  
1. Merk den valgte raden i listen.
1. Angi eller velg en verdi i **Varenummer**-feltet.
1. Angi eller velg en verdi i feltet **Konfigurasjonsgruppe**.
    * Velg konfigurasjonsgruppen Kabel på nytt.  
1. Velg **Ny**.
1. Merk den valgte raden i listen.
1. Angi eller velg en verdi i **Varenummer**-feltet.
    * Velge varenummer D0002 Kabinett.  
1. Angi eller velg en verdi i feltet **Konfigurasjonsgruppe**.
    * Velg konfigurasjonsgruppen Kabinett for denne stykklistelinjen.  
1. Velg **Ny**.
1. Merk den valgte raden i listen.
1. Angi eller velg en verdi i **Varenummer**-feltet.
    * Velg varenummer M0007 StandardCabinet som siste stykklistelinje.  
1. Angi eller velg en verdi i feltet **Konfigurasjonsgruppe**.
    * Velg konfigurasjonsgruppen Kabinett for den siste stykklistelinjen.  

## <a name="approve-and-activate"></a>Godkjenn og aktiver

1. Lukk siden.
1. Velg **Godkjenn**.
1. Angi eller velg en verdi i feltet **Godkjent av**.
1. Velg *Ja* i feltet **Vil du også godkjenne stykklisten?**.
1. Velg **OK**.
1. Velg **Aktiver**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
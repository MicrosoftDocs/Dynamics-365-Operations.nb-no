---
title: Opprett juridiske enheter
description: Denne artikkelen beskriver hvordan du oppretter juridiske enheter i Microsoft Dynamics 365 Commerce, som må opprettes og konfigureres før du oppretter kanaler.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: e99536d3706c842d69060136f23508208b16b461
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276326"
---
# <a name="create-legal-entities"></a>Opprett juridiske enheter

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du oppretter juridiske enheter i Microsoft Dynamics 365 Commerce, som må opprettes og konfigureres før du oppretter kanaler.

En juridisk enhet er en organisasjon som har en registrert eller lovfestet juridisk struktur. Juridiske enheter kan inngå juridiske kontrakter og er påkrevd for å klargjøre oppgjør som rapporterer om prestasjonen.

Et firma er en type juridisk enhet. Firmaer er for øyeblikket den eneste typen juridisk enhet som du kan opprette, og hver juridisk enhet er tilknyttet en firma-IDen. Denne tilknytningen finnes fordi noen funksjonsområder i programmet bruker en firma-ID eller *dataområde-ID*, i sine datamodeller. I disse funksjonsområdene brukes firmaer som en grense for datasikkerhet. Brukere har bare tilgang til data for firmaet de er logget på. 

Når du oppretter en kanal, må du angi hvilken juridisk enhet kanalen tilhører.

## <a name="create-a-new-legal-entity"></a>Opprette en ny juridisk enhet

Hvis du vil opprette en ny juridisk enhet i Dynamics 365 Commerce, gjør du følgende:

1. I navigasjonsruten går du til **Moduler \> Hovedkvarteroppsett \> Juridiske enheter**.
1. I handlingsruten velger du **Ny**. Ruten **Ny juridisk enhet** vises til høyre.
1. Angi en verdi i feltet **Navn**.
1. Angi en verdi i feltet **Firma**.
1. Angi eller velg en verdi i **Land/område**-feltet.
1. Velg **OK**. 

   ![Opprette juridisk enhet.](media/legal-entities.png)

1. I **Generelt**-seksjonen angir du følgende generelle informasjon om den juridiske enheten: 
   1. Angi et søkenavn hvis et søkenavn er påkrevd. Et søkenavn er et alternativt navn som kan brukes til å søke etter den juridiske enheten. 
   1. Velg om den juridiske enheten brukes som et konsoliderte firma.
   1. Velg om den juridiske enheten brukes som et elimineringsfirma. 
   1. Velg **standardspråket** for enheten. 
   1. Velg **tidssonen** for enheten.
1. I **Adresser**-delen velger du **Rediger** for å angi adresseinformasjon, for eksempel gatenavn og -nummer, postnummer og poststed.
1. I delen **Kontaktinformasjon** angir du informasjon om kommunikasjonsmetoder, for eksempel e-postadresse, URL-adresser og telefonnumre.
1. I delen **Lovbestemt rapportering** skriver du inn registreringsnumrene som brukes ved lovbestemt rapportering.
1. I delen **Registreringsnumre** angir du eventuell informasjon som kreves av den juridiske enheten.
1. I delen **Bankkontoinformasjon** angir du bankkontoer og registreringsnumre for den juridiske enheten.
1. I delen **Utenrikshandel og logistikk** angir du forsendelsesinformasjon for den juridiske enheten.
1. I delen **Nummerserier** kan du vise nummerseriene som er tilknyttet den juridiske enheten. Dette vil være tomt til å begynne med.
1. I delen **Instrumentbordbilde** viser eller endrer du logoen og instrumentbordbildet som er knyttet til den juridiske enheten.
1. I delen **Avgiftsregistrering** skriver du inn registreringsnumrene som brukes til å rapportere til skattemyndighetene.
1. I delen **1099-avgift** skriver du inn 1099-informasjon for den juridiske enheten.
1. I delen **Skatteinformasjon** angir du skatteinformasjon for den juridiske enheten.
1. Velg **Lagre**.

Bildet nedenfor viser et detaljer om et eksempel på en juridisk enhet.

![Generell del om juridisk enhet.](media/legal-entities-general.png)
   
## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over organisasjoner og organisasjonshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Planlegge organisasjonshierarkiet](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organisasjonshierarkier](channels-org-hierarchies.md)

[Oversikt over kanaler](channels-overview.md)

[Forutsetninger for kanaloppsett](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

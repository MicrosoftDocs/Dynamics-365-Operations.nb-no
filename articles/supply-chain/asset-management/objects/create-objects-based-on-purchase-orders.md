---
title: Opprette aktiva basert på bestillinger
description: Dette emnet forklarer hvordan du kan opprette en liste over aktiva som kan brukes som grunnlag for oppretting av aktiva for vedlikeholdsjobber i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54c129d93e13e032cc5526a91c73d3363ed183db
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434355"
---
# <a name="create-assets-based-on-purchase-orders"></a>Opprette aktiva basert på bestillinger

[!include [banner](../../includes/banner.md)]

 

Dette emnet forklarer hvordan du kan opprette en liste over aktiva som kan brukes som grunnlag for oppretting av aktiva for vedlikeholdsjobber i Aktivastyring. Du kan vise en liste over bestillingslinjene som er opprettet på disse varene, basert på aktivavarene. Formålet med denne funksjonaliteten er å enkelt opprette et aktivum i Aktivastyring basert på en bestilling.

Først definerer du varene som skal brukes til å opprette aktiva fra en bestilling, i **Aktivavarer**. Når du har opprettet en bestillingslinje, oppretter du aktivaene i **Ventende aktiva**. Det er mulig å bestemme på hvilket stadium av bestillingen aktivumet skal opprettes.


## <a name="select-asset-items"></a>Velg aktivavarer

1. Klikk på **Aktivastyring** > **Oppsett** > **Aktiva** > **Varer**.
2. Klikk **Ny** for å opprette en ny aktivavare.
3. Velg varen i **Varenummer**-feltet. Når du forlater dette feltet, settes vare navnetautomatisk inn i feltet **Produktnavn**.
4. På hurtigfanen **Generelt** velger du en aktivatype for varen.
5. Velg aktivaprodusenten og -modellen for varen.
6. Lagre varen.


## <a name="create-assets-from-pending-assets"></a>Opprette aktiva fra ventende aktiva

1. Klikk på **Aktivastyring** > **Felles** > **Aktiva** > **Ventende aktiva**.
2. Du vil se en oppdatert liste over bestillingene basert på varene som er valgt, i **Aktivavarer**.
3. Du kan filtrere statusen for bestillinger for å velge i hvilken livsløpstilstand aktivumet skal opprettes. Du vil for eksempel kanskje bare opprette aktiva når en produktkvittering er postert på en bestilling.
4. Velg koblingen **Referansenummer** på en bestillingslinje for å vise detaljert informasjon om varen.
5. Hvis du vil redigere hvilke dimensjoner som vises i hurtigfanen **Lagerdimensjoner**, klikker du på knappen **Visningsdimensjoner** og gjør dine valg.
6. Hvis du vil opprette et aktivum basert på en bestillingslinje, merker du av i **Merk**-kolonnen for denne linjen på listesiden, og klikker på **Opprett aktiva**. Det vises en melding som informerer deg om ID-en for aktivumet.
7. Velg aktivumet i **Alle aktiva**-listen, og klikk på **Rediger** for å legge til mer informasjon om aktivumet.
8. I **Ventende aktiva**, hvis du ikke vil slette en linje fordi du ikke ønsker å opprette et aktivum, merker du av i **Merk**-kolonnen for denne linjen og klikker på **Forkast ventende aktiva**. Det vises en melding som informerer deg om ID-en for aktivumet. Du sletter ikke bestillingen eller salgsordren, bare posten som du kunne ha opprettet et aktivum for, i **Aktivastyring**.

>[!NOTE]
>Alle produktdimensjoner (størrelse, farge, konfigurasjon etc.) blir automatisk overført til aktivaattributtene. Sporingsdimensjoner (serienummer) lagres direkte på aktivaet når det opprettes.


## <a name="find-pending-assets"></a>Finne ventende aktiva

Du kan kjøre en **telling av ventende aktiva** for å se etter ventende aktiva. Denne funksjonen kan for eksempel brukes til å motta et varsel hver gang et ventende aktivum er klart til å opprettes som et aktivum.

1. Klikk på **Aktivastyring** > **Periodisk** > **Aktiva** > **Telling av ventende aktiva**.
2. Klikk **OK** for å kjøre jobben og oppdatere listen i **Ventende aktiva**.
3. Du kan angi at denne jobben skal kjøres som en satsvis jobb, for eksempel én gang per dag.

**Forsiktig:** Hvis data endres på en bestilling *etter* at du har opprettet et aktivum basert på den fra varen, gjenspeiles ikke disse endringene på aktivaet.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
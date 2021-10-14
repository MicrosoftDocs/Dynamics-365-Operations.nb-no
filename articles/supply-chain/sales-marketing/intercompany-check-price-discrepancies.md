---
title: Kontroller prisavvik for konsernintern bestilling
description: Dette emnet beskriver hvordan du kontrollerer prisavvik for konsernintern bestilling
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f9a0ba4980f8acf56d84dc865094b405b7402ad5
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548438"
---
# <a name="check-intercompany-order-price-discrepancies"></a>Kontroller prisavvik for konsernintern bestilling

[!include [banner](../../includes/banner.md)]

Du kan bruke denne prosedyren til å se etter prisavvik for konserninterne bestillinger.

1. Gå til **Innkjøp og leverandører \> Periodisk \> Opprydding \> Kontroller prisavvik for konsernintern bestilling**.
1. Definer en satsvis jobb om nødvendig, og klikk deretter **OK** for å kontrollere prisene og rabattene for konserinterne salgsordrer og bestillinger. Ellers velger du **Avbryt** for å lukke siden uten å utføre kontrollen.

    > [!TIP]
    > Eventuelle synkroniseringsproblemer eller problemer med prisene vil vises i en informasjonsmelding. Du kan skrive ut informasjonsmeldingen for referanse.

1. Dobbeltklikk den relevante linjen i informasjonsmeldingen for å åpne bestillingen i den gjeldende juridiske enheten. Åpne ordren i den relaterte juridiske enheten ved å velge **Konsernintern**, og deretter **Konsernintern bestilling** eller **Konsernintern salgsordre**.

    > [!NOTE]
    > Slik tillater du en oppdatering av den konserninterne bestillingen:
    >
    > 1. Gå til **Kunder \> Kunder \> Alle kunder**.
    > 1. Velg kategorien **Generelt**, og velg deretter **Konsernintern**.
    > 1. På siden **Konsernintern** velger du **Bestillingspolicyer** eller **Salgsordrepolicyer**.
    > 1. Velg **Tillat prisredigering** og **Tillat rabattredigering** i begge områdene.

1. Åpne den relevante konserninterne ordren hvor du vil beholde prisen.
1. For hver ordrelinje endrer du først feltet **Enhetspris** for linjen og endrer det deretter tilbake til den opprinnelige verdien. Endre **Rabatt**-feltet for linjen frem og tilbake, og endre de relevante feltene **Innkjøpstillegg** eller **Salgstillegg** frem og tilbake. Når du endrer verdiene frem og tilbake, utløses en synkronisering av priser, rabatter og tillegg fra denne konserninterne bestillingslinjen til den konserninterne bestillingslinjen som det refereres til, slik at de blir justert automatisk.

    > [!NOTE]
    > Denne synkroniseringen er bare gyldig hvis den konserninterne salgsordren ikke er fakturert. Hvis den konserninterne salgsordren er fakturapostert, og det er opprettet en kundefakturajournal, kan du bare utføre endringer direkte i de konserninterne bestillingslinjene ved å definere prisene, rabattene og tilleggene på samme måte som i den konserninterne kundefakturajournalen. Hvis du ikke gjør dette, kan du ikke fakturapostere den konserninterne bestillingen, fordi det vil være en uoverensstemmelse i ordresummen.

1. Gjenta fremgangsmåten til alle konserninterne bestillinger og salgsordrer er synkronisert.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

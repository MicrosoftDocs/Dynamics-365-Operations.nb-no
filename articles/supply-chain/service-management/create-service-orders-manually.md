---
title: Opprette serviceordrer manuelt
description: Du kan opprette serviceordrer manuelt ved å bruke en serviceavtale eller ved å bruke **Serviceordrer**-skjemaet.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1fad4abcf39021f94db50c07a39803af31f85c2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578854"
---
# <a name="create-service-orders-manually"></a>Opprette serviceordrer manuelt    

[!include [banner](../includes/banner.md)]


Du kan opprette serviceordrer manuelt ved å bruke en serviceavtale eller ved å bruke **Serviceordrer**-skjemaet. Du kan også opprette en serviceordre fra et prosjekt.

> [!TIP]
> <P>Du kan bruke automatiserte prosesser til å opprette serviceordrer. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Opprette en serviceordre manuelt fra en serviceavtale

1.  Velg **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.

2.  Velg en serviceavtale eller opprett en ny serviceavtale.

3.  Velg fanen **Lever**, og i gruppen **Opprett** velger du **Planlagte serviceordrer** for å åpne skjemaet **Opprett serviceordre**.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>Opprette en serviceordre manuelt i Serviceordrer-skjemaet

1.  Velg **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.

2.  Velg **Ny** for å opprette en ny serviceordre.

3.  Opprett serviceordrelinjer for serviceordren.

> [!NOTE]
> <P>Hvis det er merket av for <STRONG>Tillat uten serviceavtale</STRONG> i skjemaet <STRONG>Servicestyringsparametere</STRONG>, kan du postere transaksjonene fra serviceordrelinjene uten å knytte serviceordren til en serviceavtale. Hvis avmerkingen er fjernet, må du knytte den manuelt opprettede serviceordren til et prosjekt før du posterer serviceordrelinjene.</P>

## <a name="create-a-service-order-from-a-project"></a>Opprette en serviceordre fra et prosjekt

1.  Gå til **Prosjektstyring og regnskap** \> **Felles** \> **Prosjekter** \> **Alle prosjekter**.

2.  I skjemaet **Prosjekter** i **handlingsruten** velger du fanen **Administrer** \> og velger **Tjeneste** \> **Tjenesteordrer**.

3.  Følg forrige fremgangsmåte for å opprette en serviceordre manuelt i **Serviceordrer**-skjemaet. Feltet **Prosjekt-ID** viser prosjektreferansen.

> [!NOTE]
> <P>Hvis det er merket av for <STRONG>Tillat uten serviceavtale</STRONG> i skjemaet <STRONG>Servicestyringsparametere</STRONG>, kan du postere transaksjonene fra serviceordrelinjene uten å knytte serviceordren til en serviceavtale. Hvis avmerkingen er fjernet, må du knytte den manuelt opprettede serviceordren til et prosjekt før du posterer serviceordrelinjene.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Opprette en serviceordre fra Salgsordre-skjemaet

Du kan opprette en serviceordre fra skjemaet **Salgsordrer** ved å bruke veiviseren **Opprett en ny serviceordre basert på salgsordren**.

1.  Gå til **Salg og markedsføring** \> **Vanlig** \> **Salgsordrer** \> **Alle salgsordrer**.

2.  Åpne den relevante salgsordren.

3.  På fanen **Salgsordre** velger du **Serviceordre** for å starte veiviseren **Opprett en ny serviceordre basert på salgsordren**.

4.  Velg **Neste \>**, og følg trinnene nedenfor på siden **Velg avtale for serviceordre**:
    
      - Bruk **Serviceavtale**-feltet til å velge serviceavtalen som den nye serviceordren skal knyttes til.
    
      - (Valgfritt): Bruk feltet **Prosjekt-ID** til å knytte denne serviceordren til et bestemt prosjekt.

5.  Velg **Neste \>**, og følg trinnene nedenfor på siden **Opprett serviceordre**:
    
      - Angi en dato og et klokkeslett for servicebesøkets begynnelse i feltet **Foretrukket servicetidspunkt**.
    
      - Valgfritt: Endre teksten i **Beskrivelse**-feltet. Dette feltet inneholder som standard beskrivelsen av serviceavtalen du valgte på forrige side.
    
      - I **Ansvarlig**-feltet velger du ID-en til den ansatte som er ansvarlig for avtalen. Hvis du kjenner til den, kan du også angi ID-en til kundens foretrukne tekniker for servicebesøk.
    
      - I feltet **Kontakt-ID** velger du personen i kundens firma som skal kontaktes angående serviceordren.

6.  Velg **Neste \>**, og velg deretter **Fullfør**.


## <a name="see-also"></a>Se også

[Serviceordrer](service-orders.md)

[Opprette serviceordrer automatisk](create-service-orders-automatically.md)

[Opprette serviceordrer (klasseskjema)](https://technet.microsoft.com/library/aa553901\(v=ax.60\)) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
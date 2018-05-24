---
title: Opprette serviceordrer manuelt
description: "Du kan opprette serviceordrer manuelt ved å bruke en serviceavtale eller ved å bruke **Serviceordrer**-skjemaet."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a0cc6b2646929776f4efb20474de6b0fc5c4719c
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-orders-manually"></a>Opprette serviceordrer manuelt    

[!include [banner](../includes/banner.md)]


Du kan opprette serviceordrer manuelt ved å bruke en serviceavtale eller ved å bruke **Serviceordrer**-skjemaet. Du kan også opprette en serviceordre fra et prosjekt.

> [!TIP]
> <P>Du kan bruke automatiserte prosesser til å opprette serviceordrer. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Opprette en serviceordre manuelt fra en serviceavtale

1.  Klikk **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.

2.  Velg en serviceavtale eller opprett en ny serviceavtale.

3.  Klikk fanen **Lever**, og i **Opprett**-gruppen klikker du **Planlagte serviceordrer** for å åpne skjemaet **Opprett serviceordre**.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>Opprette en serviceordre manuelt i Serviceordrer-skjemaet

1.  Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.

2.  Trykk Ctrl+N for å opprette en ny serviceordre.

3.  Opprett serviceordrelinjer for serviceordren.

> [!NOTE]
> <P>Hvis det er merket av for <STRONG>Tillat uten serviceavtale</STRONG> i skjemaet <STRONG>Servicestyringsparametere</STRONG>, kan du postere transaksjonene fra serviceordrelinjene uten å knytte serviceordren til en serviceavtale. Hvis avmerkingen er fjernet, må du knytte den manuelt opprettede serviceordren til et prosjekt før du posterer serviceordrelinjene.</P>

## <a name="create-a-service-order-from-a-project"></a>Opprette en serviceordre fra et prosjekt

1.  Klikk på **Prosjektstyring og regnskap** \> **Felles** \> **Prosjekter** \> **Alle prosjekter**.

2.  I **Prosjekter**-skjemaet i **handlingsruten** klikker du på **Administrer**-fanen \> klikk på **Service**\> **Serviceordrer**.

3.  Følg forrige fremgangsmåte for å opprette en serviceordre manuelt i **Serviceordrer**-skjemaet. Feltet **Prosjekt-ID** viser prosjektreferansen.

> [!NOTE]
> <P>Hvis det er merket av for <STRONG>Tillat uten serviceavtale</STRONG> i skjemaet <STRONG>Servicestyringsparametere</STRONG>, kan du postere transaksjonene fra serviceordrelinjene uten å knytte serviceordren til en serviceavtale. Hvis avmerkingen er fjernet, må du knytte den manuelt opprettede serviceordren til et prosjekt før du posterer serviceordrelinjene.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Opprette en serviceordre fra Salgsordre-skjemaet

Du kan opprette en serviceordre fra skjemaet **Salgsordrer** ved å bruke veiviseren **Opprett en ny serviceordre basert på salgsordren**.

1.  Klikk **Salg og markedsføring** \> **Vanlig** \> **Salgsordrer** \> **Alle salgsordrer**.

2.  Åpne den relevante salgsordren.

3.  På fanen **Salgsordre** klikker du på **Serviceordre** for å starte veiviseren **Opprett en ny serviceordre basert på salgsordren**.

4.  Klikk på **Neste \>**, og følg trinnene nedenfor på siden **Velg avtale for serviceordre**:
    
      - Bruk **Serviceavtale**-feltet til å velge serviceavtalen som den nye serviceordren skal knyttes til.
    
      - (Valgfritt): Bruk feltet **Prosjekt-ID** til å knytte denne serviceordren til et bestemt prosjekt.

5.  Klikk på **Neste \>**, og følg trinnene nedenfor på siden **Opprett serviceordre**:
    
      - Angi en dato og et klokkeslett for servicebesøkets begynnelse i feltet **Foretrukket servicetidspunkt**.
    
      - Valgfritt: Endre teksten i **Beskrivelse**-feltet. Dette feltet inneholder som standard beskrivelsen av serviceavtalen du valgte på forrige side.
    
      - I **Ansvarlig**-feltet velger du ID-en til den ansatte som er ansvarlig for avtalen. Hvis du kjenner til den, kan du også angi ID-en til kundens foretrukne tekniker for servicebesøk.
    
      - I feltet **Kontakt-ID** velger du personen i kundens firma som skal kontaktes angående serviceordren.

6.  Klikk **Neste \>**, og klikk deretter **Fullfør**.


## <a name="see-also"></a>Se også

[Serviceordrer](service-orders.md)

[Opprette serviceordrer automatisk](create-service-orders-automatically.md)

[Opprette serviceordrer (klasseskjema)](https://technet.microsoft.com/en-us/library/aa553901\(v=ax.60\)) 



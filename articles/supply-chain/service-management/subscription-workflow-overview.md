---
title: Oversikt over abonnementsarbeidsflyt
description: Dette emnet gir en oversikt over abonnementsarbeidsflyt.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc2b2dc724adf53bfc6cb8de79c14c7414cbc40a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974166"
---
# <a name="subscription-workflow-overview"></a>Oversikt over abonnementsarbeidsflyt 

[!include [banner](../includes/banner.md)]


Du er abonnementsadministrator for et lysselskap som tilbyr abonnement for vedlikehold av lysrigger. En kunde tar kontakt for å kjøpe et årlig sabonnement på vedlikehold av lysrigger.

## <a name="setting-up-subscriptions"></a>Definere abonnement

Når du skal definere et abonnement, må du først opprette en abonnementsgruppe for den nye tjenesteavtalen, eller bekrefte at det finnes en abonnementsgruppe. Hvis det finnes en abonnementsgruppe, må du angi den til å fakturere kunden årlig og utligne salgsinntekter hver måned i året. Hvis du vil ha mer informasjon om hvordan du definerer abonnementer, kan du se [Definere abonnementsgrupper](set-up-subscription-groups.md).

Når abonnementsgruppen er opprette, kan du opprette abonnementet. Hvis du vil ha mer informasjon om hvordan du oppretter serviceabonnementer, kan du se [Opprette serviceabonnementer fra en abonnementsgruppe](create-service-subscriptions-from-subscription-group.md).

## <a name="create-and-modify-subscription-transactions"></a>Opprette og endre abonnementstransaksjoner

Når du har definert abonnementet, oppretter du abonnementsavgiftstransaksjonen for den første faktureringsterminen, som er ett år. Transaksjonene er av typen **Vanlig**. Derfor kan du bare opprette abonnementstransaksjoner der fra-datoen og til-datoen tilsvarer periodene som tidligere ble opprettet i skjemae **Periodetyper**. Hvis du vil ha mer informasjon om gebyrtransaksjoner, kan du se [Opprette abonnementsgebyrtransaksjoner](create-subscription-fee-transactions.md).

Når du har angitt abonnementet for kunden, husker du at de har forhandlet en 10 prosents rabatt på alle listeprisene for servicetilbudene. Derfor må du redusere prisen for transaksjonsavgiften du har opprettet.

Senere på dagen ringer kundekontakten for å si at selv om de fortsatt vil ha serviceavtalen for lysriggen, planlegger de å introdusere en ny lysrigg senere på året. De trenger derfor bare vedlikeholdsdekning til oktober 2013. For å redusere antall måneder i kundens abonnement oppretter du en ny abonnementutgiftstransaksjon av typen **Reduksjonsdager**. Hvis du vil ha mer informasjon om hvordan du kan redusere dager, kan du se [Redusere dagene på abonnementsgebyr](reduce-the-days-on-subscription-fees.md).

## <a name="invoice-and-accrue-subscription-transactions"></a>Fakturere og avsette abonnementstransaksjoner

Du har nå definert abonnementet, og du er klar til å fakturere kunden for det. Hvis du vil ha mer informasjon om hvordan du fakturerer abonnementer, kan du se [Fakturere abonnementtransaksjoner](invoice-subscription-transactions.md).

To dager senere ringer kunden for å si at abonnementet bør faktureres i amerikanske dollar, ikke euro. Du oppretter derfor en kreditnota, og du oppretter også en ny abonnementstransaksjon i korrekt valuta. Hvis du vil ha mer informasjon om hvordan du krediterer abonnementstransaksjoner, kan du se [Kreditere abonnementstransaksjoner](credit-subscription-transactions.md).

På slutten av hver måned kan én måneds inntekt avsettes fra kundens abonnement til resultatkontoen og VIA-kontoene. Hvis du vil ha mer informasjon om hvordan du avsetter inntekt for abonnementer, kan du se [Avsette abonnementsomsetning](accrue-subscription-revenue.md).

  



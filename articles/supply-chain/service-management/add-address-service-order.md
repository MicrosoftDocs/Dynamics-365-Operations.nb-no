---
title: Legge til en adresse i en serviceordre
description: Dette emnet beskriver hvordan du legger til en kundeadresse i en serviceordre.
author: ShylaThompson
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a54ec439fc88dc9688bbb3d6b833b5d80482f024
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824660"
---
# <a name="add-an-address-to-a-service-order"></a>Legge til en adresse i en serviceordre    

[!include [banner](../includes/banner.md)]


Dette emnet beskriver hvordan du legger til en kundeadresse i en serviceordre. Når du oppretter en serviceordre, overføres adresseinformasjonen fra prosjektet som serviceordren er knyttet til. Du kan imidlertid velge en alternativ lokasjon fra adressene som allerede er angitt i Microsoft Dynamics AX for kunder, leverandører, områder, lagre, serviceordrer og prosjekter.

Du kan også opprette en ny adresse. Den nye adressen overføres som standard til prosjektet. Du kan imidlertid angi at den nye adressen bare gjelder for denne forekomsten av servicen. Hvis du gjør dette, overføres ikke den nye adressen til prosjektet.

## <a name="create-a-customer-address-for-a-service-order"></a>Opprette en kundeadresse for en serviceordre

Hvis du vil legge til en adresse i en serviceordre, gjør du følgende:

1.  Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.

2.  Åpne serviceordren som du vil opprette en adresse for.

3.  I **handlingsruten** klikker du på **Rediger** og deretter på **Topptekstvisning**.

4.  På hurtigfanen **Adresse** klikker du på **Legg til adresse**.

5.  I **Ny adresse**-skjemaet angir du et unikt navn for adressen og fyller ut de gjenstående feltene. 
    

    > [!WARNING]
    > <P>Hvis du angir samme navn som en eksisterende adresse, overskriver informasjonen du angir i de gjenstående feltene, informasjon for den eksisterende adressen.</P>


6.  Klikk på **OK** for å kopiere den nye adressen til serviceordren.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Angi en alternativ adresse på en serviceordre

Hvis du vil legge til en alternativ adresse i en serviceordre, gjør du følgende:

1.  Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.

2.  Åpne serviceordren som du vil angi en alternativ adresse for.

3.  I **handlingsruten** klikker du på **Rediger** og deretter på **Topptekstvisning**.

4.  På hurtigfanen **Adresse** klikker du på **Annen adresse**.

5.  I skjemaet **Adressevalg**, i feltet **Oppføringstype** velger du **Serviceordrer**.

6.  Velg en adresse, og klikk deretter **OK** for å kopiere den til serviceordren.


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
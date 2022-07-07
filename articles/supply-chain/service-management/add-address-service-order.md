---
title: Legge til en adresse i en serviceordre
description: Denne artikkelen beskriver hvordan du legger til en kundeadresse i en serviceordre.
author: sorenva
ms.date: 06/15/2020
ms.topic: article
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c485c50bab7c2e945aa0f0fc0601008dcebd3328
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015732"
---
# <a name="add-an-address-to-a-service-order"></a>Legge til en adresse i en serviceordre

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du legger til en kundeadresse i en serviceordre. Når du oppretter en serviceordre, overføres adresseinformasjonen fra prosjektet som serviceordren er knyttet til. Du kan imidlertid velge en alternativ lokasjon fra adressene som allerede er angitt i Microsoft Dynamics AX for kunder, leverandører, områder, lagre, serviceordrer og prosjekter.

Du kan også opprette en ny adresse. Den nye adressen overføres som standard til prosjektet. Du kan imidlertid angi at den nye adressen bare gjelder for denne forekomsten av servicen. Hvis du gjør dette, overføres ikke den nye adressen til prosjektet.

## <a name="create-a-customer-address-for-a-service-order"></a>Opprette en kundeadresse for en serviceordre

Hvis du vil legge til en adresse i en serviceordre, gjør du følgende:

1. Gå til **Servicestyring** \> **Serviceordrer** \> **Serviceordrer**.

1. Åpne serviceordren som du vil opprette en adresse for.

1. Åpne **Hode**-fanen.

1. Utvid hurtigfanen **Adresse**, og velg deretter **Legg til adresse** på verktøylinjen i hurtigfanen.

1. I dialogboksen **Ny adresse** angir du et unikt navn for adressen og fyller ut de gjenstående feltene. 

    > [!WARNING]
    > Hvis du angir samme navn som en eksisterende adresse, overskriver informasjonen du angir i de gjenstående feltene, informasjon for den eksisterende adressen.

1. Velg **OK** for å kopiere den nye adressen til serviceordren.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Angi en alternativ adresse på en serviceordre

Hvis du vil legge til en alternativ adresse i en serviceordre, gjør du følgende:

1. Gå til **Servicestyring** \> **Serviceordrer** \> **Serviceordrer**.

1. Åpne serviceordren som du vil angi en alternativ adresse for.

1. Åpne **Hode**-fanen.

1. Utvid hurtigfanen **Adresse**, og velg deretter **Annen adresse** på verktøylinjen i hurtigfanen.

1. Velg **Serviceordrer** fra rullegardinlisten ovenfor rutenettet, i dialogboksen **Adressevalg**.

1. Velg en adresse, og velg deretter **OK** for å kopiere den til serviceordren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
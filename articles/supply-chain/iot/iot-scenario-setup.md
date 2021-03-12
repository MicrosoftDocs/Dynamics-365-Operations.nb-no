---
title: Scenariooppsett for IoT-intelligens
description: Dette emnet forklarer hvordan du konfigurerer scenarier for IoT-intelligens i Microsoft Dynamics 365 Supply Chain Management.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 91deb080121d50794e6ff6fe79f9ca876b76deb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005258"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="c756c-103">Scenariooppsett for IoT-intelligens</span><span class="sxs-lookup"><span data-stu-id="c756c-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c756c-104">Dette emnet forklarer hvordan du konfigurerer scenarier for IoT-intelligens i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c756c-104">This topic explains how to configure scenarios for IoT Intelligence in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c756c-105">Før du kan definere scenarioene, må du [konfigurere Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="c756c-105">Before you can set up the scenarios, you must [set up Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>

<span data-ttu-id="c756c-106">I dette emnet skal du konfigurere **Nedetid for utstyr**, slik at et varsel genereres i Supply Chain Management når en maskin går ned.</span><span class="sxs-lookup"><span data-stu-id="c756c-106">In this topic, you will configure the **Equipment downtime** scenario so that a notification is generated in Supply Chain Management when a machine goes down.</span></span> <span data-ttu-id="c756c-107">Emnet viser også hvordan du konfigurerer **Produktkvalitet**-scenarioet, slik at det genereres et varsel hvis et attributt for en vare er utenfor et bestemt område, og hvordan du konfigurerer **Produksjonsforsinkelser**-scenarioet, slik at det genereres et varsel hvis produksjonsgjennomstrømningen faller under en terskelverdi.</span><span class="sxs-lookup"><span data-stu-id="c756c-107">The topic also shows how to configure the **Product quality** scenario so that a notification is generated if an attribute of an item is outside a specified range, and how to configure the **Production delays** scenario so that a notification is generated if the production throughput falls below a threshold value.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="c756c-108">Konfigurere  Nedetid for utstyr i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c756c-108">Configure the Equipment downtime scenario in Supply Chain Management</span></span>

<span data-ttu-id="c756c-109">**Nedetid for utstyr** tilordner et signal om **PartOut** til en maskinvarslingsterskel.</span><span class="sxs-lookup"><span data-stu-id="c756c-109">The **Equipment downtime** scenario maps a **PartOut** signal to a machine alert threshold.</span></span> <span data-ttu-id="c756c-110">Maskinen blir bare overvåket når den er valgt for scenarioet, og når den er satt til **Kjører** i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c756c-110">The machine is monitored only when it's selected for the scenario and when is set to **Running** in Supply Chain Management.</span></span> <span data-ttu-id="c756c-111">Hvis klokkeslettet da maskinen sist mottok signalet **PartOut**, er større enn varselterskelen, utløses varslingen **Maskin nede**.</span><span class="sxs-lookup"><span data-stu-id="c756c-111">If the time since a **PartOut** signal was last received from the machine exceeds the alert threshold, a **Machine down** notification is triggered.</span></span> <span data-ttu-id="c756c-112">Hvis maskinen fortsatt kjører, utløses varslingen **Maskin oppe** når neste **PartOut**-signal mottas.</span><span class="sxs-lookup"><span data-stu-id="c756c-112">If the machine is still running, a **Machine up** notification is triggered when the next **PartOut** signal is received.</span></span> <span data-ttu-id="c756c-113">Hvis en maskin forblir nede i 30 minutter, utløses en ny varsling av typen **Maskin nede**.</span><span class="sxs-lookup"><span data-stu-id="c756c-113">If a machine stays down for 30 minutes, a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="c756c-114">**Nedetid for utstyr** har følgende avhengigheter:</span><span class="sxs-lookup"><span data-stu-id="c756c-114">The **Equipment downtime** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="c756c-115">Et varsel kan bare utløses hvis en produksjonsordre kjører på en tilordnet maskin.</span><span class="sxs-lookup"><span data-stu-id="c756c-115">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="c756c-116">Et signal som representerer en tilordnet maskins **PartOut**-signal, må sendes til IoT-huben, og et unikt egenskapsnavn må inkluderes.</span><span class="sxs-lookup"><span data-stu-id="c756c-116">A signal that represents a mapped machine's **PartOut** signal must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="c756c-117">En UNIX **timestamp**-egenskap, der verdien angis i millisekunder (MS), må finnes i meldingen for Azure IoT-hub.</span><span class="sxs-lookup"><span data-stu-id="c756c-117">A UNIX **timestamp** property, where the value is expressed in milliseconds (ms), must be present in the Azure IoT Hub message.</span></span>

<span data-ttu-id="c756c-118">For å konfigurere gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="c756c-118">To configure the scenario, follow these steps.</span></span>

1. <span data-ttu-id="c756c-119">Logg på Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c756c-119">Sign in to Supply Chain Management.</span></span>
2. <span data-ttu-id="c756c-120">Aktiver funksjonsflagget for IoT-intelligens.</span><span class="sxs-lookup"><span data-stu-id="c756c-120">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="c756c-121">Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="c756c-121">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
3. <span data-ttu-id="c756c-122">Konfigurer måleverdiene.</span><span class="sxs-lookup"><span data-stu-id="c756c-122">Configure the metrics.</span></span> <span data-ttu-id="c756c-123">Hvis du vil ha mer informasjon, kan du se [Konfigurere måleverdier](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="c756c-123">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="c756c-124">Gå til **Produksjonskontroll \> Oppsett \> IoT-intelligens \> Scenariobehandling**.</span><span class="sxs-lookup"><span data-stu-id="c756c-124">Go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="c756c-125">På flisen **Utstyr** velger du **Konfigurer** for å åpne konfigurasjonsveiviseren.</span><span class="sxs-lookup"><span data-stu-id="c756c-125">On the **Equipment downtime** tile, select **Configure** to open the configuration wizard.</span></span>

   <span data-ttu-id="c756c-126">Den første siden i veiviseren er siden **Definisjon av sensorskjema for utstyr**.</span><span class="sxs-lookup"><span data-stu-id="c756c-126">The first page in the wizard is the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="c756c-127">På denne siden er målet å sette opp skjemaet i Supply Chain Management, slik at det samsvarer med JSON-formatet (JavaScript Object Notation) i IoT-hub-meldingene.</span><span class="sxs-lookup"><span data-stu-id="c756c-127">On this page, your goal is to set up the schema in Supply Chain Management so that it matches the JavaScript Object Notation (JSON) format of the IoT Hub messages.</span></span> <span data-ttu-id="c756c-128">Flere meldingsskjemaer kan defineres.</span><span class="sxs-lookup"><span data-stu-id="c756c-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="c756c-129">Hvis du vil ha mer informasjon, kan du se [Skjemaformater for IoT-hub-meldinger](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="c756c-129">For more information, see [Schema formats for IoT Hub messages](iot-schema-format.md).</span></span> <span data-ttu-id="c756c-130">I dette eksemplet inneholder meldingslasten en gruppe meldinger som har følgende format.</span><span class="sxs-lookup"><span data-stu-id="c756c-130">In this example, the message payload contains a batch of messages that has the following format.</span></span>

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. <span data-ttu-id="c756c-131">Legg til en rad i tabellen, og angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="c756c-131">Add a row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="c756c-132">Sett **Skjemanavn**-feltet til **ID**.</span><span class="sxs-lookup"><span data-stu-id="c756c-132">Set the **Schema name** field to **ID**.</span></span>
    2. <span data-ttu-id="c756c-133">Sett feltet **Skjemabane** til **/payload\[\*\]/id**.</span><span class="sxs-lookup"><span data-stu-id="c756c-133">Set the **Schema path** field to **/payload\[\*\]/id**.</span></span>
    3. <span data-ttu-id="c756c-134">Sett **Beskrivelse**-feltet til **Meldings-ID**.</span><span class="sxs-lookup"><span data-stu-id="c756c-134">Set the **Description** field to **Message ID**.</span></span>

8. <span data-ttu-id="c756c-135">Legg til en ny rad i tabellen, og angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="c756c-135">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="c756c-136">Sett **Skjemanavn**-feltet til **Tidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="c756c-136">Set the **Schema name** field to **Timestamp**.</span></span>
    2. <span data-ttu-id="c756c-137">Sett feltet **Skjemabane** til **/payload\[\*\]/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="c756c-137">Set the **Schema path** field to **/payload\[\*\]/timestamp**.</span></span>
    3. <span data-ttu-id="c756c-138">Sett **Beskrivelse**-feltet til **Meldingstidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="c756c-138">Set the **Description** field to **Message timestamp**.</span></span>

9. <span data-ttu-id="c756c-139">Legg til en ny rad i tabellen, og angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="c756c-139">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="c756c-140">Sett **Skjemanavn**-feltet til **Verdi**.</span><span class="sxs-lookup"><span data-stu-id="c756c-140">Set the **Schema name** field to **Value**.</span></span>
    2. <span data-ttu-id="c756c-141">Sett feltet **Skjemabane** til **/payload\[\*\]/value**.</span><span class="sxs-lookup"><span data-stu-id="c756c-141">Set the **Schema path** field to **/payload\[\*\]/value**.</span></span>
    3. <span data-ttu-id="c756c-142">Sett **Beskrivelse**-feltet til **Meldingsverdi**.</span><span class="sxs-lookup"><span data-stu-id="c756c-142">Set the **Description** field to **Message value**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c756c-143">Du trenger ikke å definere alle egenskapene i meldingen.</span><span class="sxs-lookup"><span data-stu-id="c756c-143">You don't have to define all the properties in the message.</span></span> <span data-ttu-id="c756c-144">Definer bare de egenskapene du trenger.</span><span class="sxs-lookup"><span data-stu-id="c756c-144">Define only the properties that you require.</span></span> <span data-ttu-id="c756c-145">I de foregående trinnene opprettet du ikke en rad for **Rottidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="c756c-145">In the preceding steps, you didn't create a row for **Root timestamp**.</span></span> <span data-ttu-id="c756c-146">Banen til **Rottidsstempel** vil være **/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="c756c-146">The path of **Root timestamp** would be **/timestamp**.</span></span>

10. <span data-ttu-id="c756c-147">Velg **Neste** for å gå til siden **Tilordning av sensorskjema for utstyr**.</span><span class="sxs-lookup"><span data-stu-id="c756c-147">Select **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="c756c-148">I raden for **Ressurs-ID for utstyr** i feltet **Skjemanavn** velger du **ID**.</span><span class="sxs-lookup"><span data-stu-id="c756c-148">In the row for **Equipment resource ID**, in the **Schema name** field, select **ID**.</span></span>
12. <span data-ttu-id="c756c-149">I raden for **UTC-tidspunkt** i feltet **Skjemanavn** velger du **Tidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="c756c-149">In the row for **UTC time**, in the **Schema name** field, select **Timestamp**.</span></span>
13. <span data-ttu-id="c756c-150">I raden for **Delprodusert signal** i feltet **Skjemanavn** velger du **Verdi**.</span><span class="sxs-lookup"><span data-stu-id="c756c-150">In the row for **Part produced signal**, in the **Schema name** field, select **Value**.</span></span>
14. <span data-ttu-id="c756c-151">Velg **Neste** for å gå til siden **Konfigurasjon av ressurs-ID for utstyr**.</span><span class="sxs-lookup"><span data-stu-id="c756c-151">Select **Next** to go to the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="c756c-152">Følg disse trinnene for å tilordne verdiene i IoT-hubenmeldingen til ressursene for Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="c756c-152">Follow these steps to map the values in the IoT Hub message to the Supply Chain Management resources:</span></span>

    1. <span data-ttu-id="c756c-153">I tabellen **Signaldataverdier** legger du til en ny rad.</span><span class="sxs-lookup"><span data-stu-id="c756c-153">In the **Signal Data Values** table, add a new row.</span></span> <span data-ttu-id="c756c-154">I feltet **Verdi** angir du **IoTInt.Machine1225.PartOut**.</span><span class="sxs-lookup"><span data-stu-id="c756c-154">In the **Value** field, enter **IoTInt.Machine1225.PartOut**.</span></span> <span data-ttu-id="c756c-155">Denne verdien kommer fra JSON **id**-egenskapen i IoT-hubmeldingen.</span><span class="sxs-lookup"><span data-stu-id="c756c-155">This value  comes from the JSON **id** property in the IoT Hub message.</span></span>
    2. <span data-ttu-id="c756c-156">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c756c-156">Select **Save**.</span></span>
    3. <span data-ttu-id="c756c-157">I tabellen **Tilordning av forretningspost** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c756c-157">In the **Business Record Mapping** table, select **New**.</span></span> <span data-ttu-id="c756c-158">En standardverdi for feltet for **forretningsposttype** fylles ut automatisk, og du trenger ikke endre den.</span><span class="sxs-lookup"><span data-stu-id="c756c-158">A default value for the **Business record type** field is automatically filled in, and you don't have to change it.</span></span>
    4. <span data-ttu-id="c756c-159">I feltet **Forretningspost** velger du maskinressursen for Supply Chain Management som signalverdien sendes fra.</span><span class="sxs-lookup"><span data-stu-id="c756c-159">In the **Business record** field, select the Supply Chain Management machine resource that the signal value is being sent from.</span></span>
    5. <span data-ttu-id="c756c-160">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c756c-160">Select **Save**.</span></span>
    6. <span data-ttu-id="c756c-161">Gjenta disse trinnene for å legge til en ny tilordning av forretningspost for **Machine1226**.</span><span class="sxs-lookup"><span data-stu-id="c756c-161">Repeat these steps to add a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="c756c-162">Du kan tilordne flere signaldataverdier til én post i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c756c-162">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="c756c-163">Bruk kolonnen **Valgt** for å velge maskinene du vil behandle.</span><span class="sxs-lookup"><span data-stu-id="c756c-163">Use the **Selected** column to select the machines that you want to process.</span></span> <span data-ttu-id="c756c-164">Du trenger ikke definere alle signalverdiene, og du behøver ikke å velge alle maskiner.</span><span class="sxs-lookup"><span data-stu-id="c756c-164">You don't have to define all signal values, and you don't have to select all machines.</span></span>
17. <span data-ttu-id="c756c-165">Velg **Neste** for å gå til siden **Konfigurasjon av delprodusert signal**.</span><span class="sxs-lookup"><span data-stu-id="c756c-165">Select **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="c756c-166">I tabellen **Signaldataverdier** legger du til en rad og setter **Verdi**-feltet til **Sann**.</span><span class="sxs-lookup"><span data-stu-id="c756c-166">In the **Signal Data Values** table, add a row, and set the **Value** field to **True**.</span></span> <span data-ttu-id="c756c-167">Denne verdien kommer fra JSON **value**-egenskapen i IoT-hubmeldingen.</span><span class="sxs-lookup"><span data-stu-id="c756c-167">This value comes from the JSON **value** property in the IoT Hub message.</span></span> <span data-ttu-id="c756c-168">Du kan legge til så mange verdier du trenger i scenarioet.</span><span class="sxs-lookup"><span data-stu-id="c756c-168">You can add as many values as you require for your scenario.</span></span>
19. <span data-ttu-id="c756c-169">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c756c-169">Select **Save**.</span></span>
20. <span data-ttu-id="c756c-170">Velg **Neste** for å gå til siden **Terskal for nedetid for utstyr**.</span><span class="sxs-lookup"><span data-stu-id="c756c-170">Select **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="c756c-171">De oppførte maskinene er de som tidligere var tilordnet til signalverdier.</span><span class="sxs-lookup"><span data-stu-id="c756c-171">The machines that are listed are the machines that were previously mapped to signal values.</span></span> <span data-ttu-id="c756c-172">På denne siden kan du definere en terskel for å fastslå om en maskin er nede.</span><span class="sxs-lookup"><span data-stu-id="c756c-172">On this page, you will define a threshold to determine whether a machine is down.</span></span> <span data-ttu-id="c756c-173">Hvis du for eksempel setter terskelen til **10**, genererer Supply Chain Management en varsling hvis det ikke mottas et **PartOut**-signal fra en maskin på 10 minutter.</span><span class="sxs-lookup"><span data-stu-id="c756c-173">For example, if you set the threshold to **10**, Supply Chain Management will generate a notification if no **PartOut** signal is received from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="c756c-174">Velg **Neste** for å gå til siden **Aktiver scenario**.</span><span class="sxs-lookup"><span data-stu-id="c756c-174">Select **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="c756c-175">Sett alternativet til å aktivere scenarioet.</span><span class="sxs-lookup"><span data-stu-id="c756c-175">Set the option to enable the scenario.</span></span>
22. <span data-ttu-id="c756c-176">Velg **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="c756c-176">Select **Finish**.</span></span>

<span data-ttu-id="c756c-177">Scenariooppsettet er nå fullført.</span><span class="sxs-lookup"><span data-stu-id="c756c-177">The scenario setup is now completed.</span></span> <span data-ttu-id="c756c-178">IoT-intelligens starter behandlingen av IoT-hubmeldingene automatisk.</span><span class="sxs-lookup"><span data-stu-id="c756c-178">IoT Intelligence will automatically start to process the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="c756c-179">Konfigurere  Produktkvalitet i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c756c-179">Configure the Product quality scenario in Supply Chain Management</span></span>

<span data-ttu-id="c756c-180"> **Produktkvalitet** genererer en varsling hvis et attributt for en vare er utenfor et bestemt område.</span><span class="sxs-lookup"><span data-stu-id="c756c-180">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="c756c-181">En sensor kan for eksempel sende vekten for hver vare til IoT-huben.</span><span class="sxs-lookup"><span data-stu-id="c756c-181">For example, a sensor sends the weight of each item to IoT Hub.</span></span> <span data-ttu-id="c756c-182">Hvis et element er for tungt eller for lett, blir det generert en varsling i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c756c-182">If an item is too heavy or too light, a notification is generated in Supply Chain Management.</span></span>

<span data-ttu-id="c756c-183">**Produktkvalitet**-scenarioet har følgende avhengigheter:</span><span class="sxs-lookup"><span data-stu-id="c756c-183">The **Product quality** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="c756c-184">Et varsel utløses bare hvis en produksjonsordre kjører på en tilordnet maskin og produserer et produkt med et tilordnet partiattributt.</span><span class="sxs-lookup"><span data-stu-id="c756c-184">An alert can be triggered only if a production order is running on a mapped machine and producing a product that has a mapped batch attribute.</span></span>
+ <span data-ttu-id="c756c-185">Et signal som representerer partiattributtet, må sendes til IoT-huben, og et unikt egenskapsnavn må inkluderes.</span><span class="sxs-lookup"><span data-stu-id="c756c-185">A signal that represents the batch attribute must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="c756c-186">En UNIX **timestamp**-egenskap, der verdien angis i millisekunder, må finnes i meldingen for IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c756c-186">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="c756c-187">Konfigurere  Produksjonsforsinkelser i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c756c-187">Configure the Production delays scenario in Supply Chain Management</span></span>

<span data-ttu-id="c756c-188">**Produksjonsforsinkelser** genererer en varsling hvis produksjonsgjennomstrømningen faller under en terskelverdi.</span><span class="sxs-lookup"><span data-stu-id="c756c-188">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="c756c-189">I dette scenarioet sendes det et **PartOut**-signal til IoT-hub for hver vare som produseres.</span><span class="sxs-lookup"><span data-stu-id="c756c-189">In this scenario, a **PartOut** signal is sent to IoT Hub for each item that is produced.</span></span> <span data-ttu-id="c756c-190">I Supply Chain Management beregnes forsinkelsen på grunnlag av hvor lenge produksjonsordren er planlagt å kjøre, antall varer som skal produseres, hvor lenge jobben har vært aktiv, og antall **PartOut**-signaler som er mottatt.</span><span class="sxs-lookup"><span data-stu-id="c756c-190">In Supply Chain Management, the order delay is calculated based on the amount of time that the production order is scheduled to run, the number of items that should be produced, the amount of time that the job has been running, and the number of **PartOut** signals that are received.</span></span> <span data-ttu-id="c756c-191">Det vil bli generert en forsinkelsesvarsling hvis antallet **PartOut**-signaler for jobben faller under terskelverdien.</span><span class="sxs-lookup"><span data-stu-id="c756c-191">A delay notification is generated if the number of **PartOut** signals for the job falls below the threshold value.</span></span>

<span data-ttu-id="c756c-192">**Produktforsinkelser**-scenarioet har følgende avhengigheter:</span><span class="sxs-lookup"><span data-stu-id="c756c-192">The **Production delays** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="c756c-193">Et varsel kan bare utløses hvis en produksjonsordre kjører på en tilordnet maskin.</span><span class="sxs-lookup"><span data-stu-id="c756c-193">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="c756c-194">Et signal som representerer en tilordnet maskins **PartOut**-signal, må sendes til Azure IoT-huben, og et unikt egenskapsnavn må inkluderes.</span><span class="sxs-lookup"><span data-stu-id="c756c-194">A signal that represents a mapped machine's **PartOut** signal must be sent to the Azure IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="c756c-195">En UNIX **timestamp**-egenskap, der verdien angis i millisekunder, må finnes i meldingen for IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c756c-195">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="disable-a-scenario"></a><span data-ttu-id="c756c-196">Deaktivere et scenario</span><span class="sxs-lookup"><span data-stu-id="c756c-196">Disable a scenario</span></span>

<span data-ttu-id="c756c-197">Hvis du vil deaktivere et scenario, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="c756c-197">To disable a scenario, follow these steps.</span></span>

1. <span data-ttu-id="c756c-198">I Supply Chain Management går du til **Produksjonskontroll \> Oppsett \> IoT-intelligens \> Scenariobehandling**.</span><span class="sxs-lookup"><span data-stu-id="c756c-198">In Supply Chain Management, go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="c756c-199">Velg **Konfigurer** under flis for scenarioet.</span><span class="sxs-lookup"><span data-stu-id="c756c-199">On the tile for the scenario, select **Configure**.</span></span>
3. <span data-ttu-id="c756c-200">Velg **Neste** for å gå til den siste veivisersiden.</span><span class="sxs-lookup"><span data-stu-id="c756c-200">Select **Next** to go to the last wizard page.</span></span>
4. <span data-ttu-id="c756c-201">Sett alternativet til å deaktivere scenarioet.</span><span class="sxs-lookup"><span data-stu-id="c756c-201">Set the option to disable the scenario.</span></span>

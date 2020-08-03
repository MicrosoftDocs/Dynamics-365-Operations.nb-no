---
title: Scenariooppsett for IoT-intelligens
description: Dette emnet beskriver hvordan du konfigurerer et scenario i Supply Chain Management for IoT-intelligens.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5633741fcd9c04b68e5b174447d7ead3c521ccd7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597174"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="480be-103">Scenariooppsett for IoT-intelligens</span><span class="sxs-lookup"><span data-stu-id="480be-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="480be-104">Dette emnet beskriver hvordan du konfigurerer et scenario i Supply Chain Management for IoT-intelligens.</span><span class="sxs-lookup"><span data-stu-id="480be-104">This topic describes how to configure a scenario in Supply Chain Management for IoT Intelligence.</span></span> <span data-ttu-id="480be-105">Før du kan sette opp scenarioene, må du [konfigurere LCS](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="480be-105">Before you can setup the scenarios, you must [setup LCS](iot-lcs-setup.md).</span></span>

<span data-ttu-id="480be-106">I dette emnet skal du konfigurere  **Nedetid for utstyr** til å generere et varsel i Supply Chain Management når en maskin går ned.</span><span class="sxs-lookup"><span data-stu-id="480be-106">In this topic, you will configure the **Equipment downtime** scenario to generate a notification in Supply Chain Management when a machine goes down.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="480be-107">Konfigurere  **Nedetid for utstyr** i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="480be-107">Configure the **Equipment downtime** scenario in Supply Chain Management</span></span>

<span data-ttu-id="480be-108"> **Nedetid for utstyr** tilordner et signal om at en del er ute til en maskinvarslingsterskel.</span><span class="sxs-lookup"><span data-stu-id="480be-108">The **Equipment downtime** scenario maps a part out signal to a machine alert threshold.</span></span> <span data-ttu-id="480be-109">Maskinen blir bare overvåket når den er valgt for  og er satt til å kjøre i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="480be-109">The machine is monitored only when the machine is selected for the scenario and is set to running in Supply Chain Management.</span></span> <span data-ttu-id="480be-110">Hvis klokkeslettet da maskinen sist mottok signalet om del som er ute, er større enn varselterskelen, utløses varslingen **Maskin nede**.</span><span class="sxs-lookup"><span data-stu-id="480be-110">If the time since the machine’s last received Part Out signal is greater than the alert threshold, then a **Machine down** notification is triggered.</span></span> <span data-ttu-id="480be-111">Hvis manskinen fortsatt kjører når neste **PartOut**-signal mottas, utløses varslingen **Maskin oppe**.</span><span class="sxs-lookup"><span data-stu-id="480be-111">If the machine is still running, when the next **PartOut** signal is received a **Machine up** notification is triggered.</span></span> <span data-ttu-id="480be-112">Hvis en maskin forblir nede i 30 min, utløses en ny varsling av typen **Maskin nede**.</span><span class="sxs-lookup"><span data-stu-id="480be-112">If a machine stays down for 30 mins a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="480be-113"> **Nedetid for utstyr** har følgende avhengigheter:</span><span class="sxs-lookup"><span data-stu-id="480be-113">The **Equipment downtime** scenario has these dependencies:</span></span>

+ <span data-ttu-id="480be-114">En produksjonsordre må kjøre på en tilordnet maskin for at et varsel skal kunne utløses.</span><span class="sxs-lookup"><span data-stu-id="480be-114">A production order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="480be-115">Et signal som representerer en tilordnet maskins signal for del ute, må sendes til IoT-huben med et unikt egenskapsnavn.</span><span class="sxs-lookup"><span data-stu-id="480be-115">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="480be-116">En egenskap for millisekundstidsstempel for Unix må finnes i IoT-hubmeldingen.</span><span class="sxs-lookup"><span data-stu-id="480be-116">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

<span data-ttu-id="480be-117">Hvis du vil konfigurere , gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="480be-117">To configure the scenario, follow these steps:</span></span>

1. <span data-ttu-id="480be-118">Logg på Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="480be-118">Log into Supply Chain Management.</span></span>
2. <span data-ttu-id="480be-119">Aktiver funksjonsflagget for IoT-intelligens.</span><span class="sxs-lookup"><span data-stu-id="480be-119">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="480be-120">Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="480be-120">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="480be-121">Konfigurer måleverdiene.</span><span class="sxs-lookup"><span data-stu-id="480be-121">Configure the metrics.</span></span> <span data-ttu-id="480be-122">Hvis du vil ha mer informasjon, kan du se [Konfigurere måleverdier](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="480be-122">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="480be-123">Gå til **Produksjonskontroll**.</span><span class="sxs-lookup"><span data-stu-id="480be-123">Navigate to **Production control**.</span></span>
5. <span data-ttu-id="480be-124">Gå til **Konfigurer \> IoT-Intelligence \> Scenariobehandling**.</span><span class="sxs-lookup"><span data-stu-id="480be-124">Navigate to **Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="480be-125">Klikk **Konfigurer** i flisen **Nedetid for utstyr**.</span><span class="sxs-lookup"><span data-stu-id="480be-125">Click **Configure** on the **Equipment downtime** tile.</span></span> <span data-ttu-id="480be-126">Konfigurasjonsveiviseren starter med siden **Definisjon av sensorskjema for utstyr**.</span><span class="sxs-lookup"><span data-stu-id="480be-126">The configuration wizard starts with the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="480be-127">Målet her er å konfigurere skjemaet i Supply Chain Management slik at det samsvarer med JSON-formatet til IoT-meldingene.</span><span class="sxs-lookup"><span data-stu-id="480be-127">The goal here is to setup the schema in Supply Chain Management to match the JSON format of the IoT messages.</span></span> <span data-ttu-id="480be-128">Flere meldingsskjemaer kan defineres.</span><span class="sxs-lookup"><span data-stu-id="480be-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="480be-129">Hvis du vil ha mer informasjon, kan du se [Meldingsskjemaformater for IoT-hub](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="480be-129">For more information, see [Message schema formats for IoT Hub](iot-schema-format.md).</span></span> <span data-ttu-id="480be-130">I dette eksemplet inneholder meldingslasten en gruppe meldinger med dette formatet:</span><span class="sxs-lookup"><span data-stu-id="480be-130">In this example, the message payload contains a batch of messages with this format:</span></span>

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

7. <span data-ttu-id="480be-131">Legg til en rad i tabellen.</span><span class="sxs-lookup"><span data-stu-id="480be-131">Add a row to the table.</span></span>

    1. <span data-ttu-id="480be-132">Sett **Skjemanavn** til **ID**.</span><span class="sxs-lookup"><span data-stu-id="480be-132">Set the **Schema name** to **ID**.</span></span>
    2. <span data-ttu-id="480be-133">Sett **Skjemabane** til **/payload[\*]/id**.</span><span class="sxs-lookup"><span data-stu-id="480be-133">Set the **Schema path** to **/payload[\*]/id**.</span></span>
    3. <span data-ttu-id="480be-134">Sett **Beskrivelse** til **Meldings-ID**.</span><span class="sxs-lookup"><span data-stu-id="480be-134">Set the **Description** to **Message ID**.</span></span>

8. <span data-ttu-id="480be-135">Legg til en rad i tabellen.</span><span class="sxs-lookup"><span data-stu-id="480be-135">Add a row to the table.</span></span>

    1. <span data-ttu-id="480be-136">Sett **Skjemanavn** til **Tidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="480be-136">Set the **Schema name** to **Timestamp**.</span></span>
    2. <span data-ttu-id="480be-137">Sett **Skjemabane** til **/payload[\*]/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="480be-137">Set the **Schema path** to **/payload[\*]/timestamp**.</span></span>
    3. <span data-ttu-id="480be-138">Sett **Beskrivelse** til **Meldingstidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="480be-138">Set the **Description** to **Message timestamp**.</span></span>

9. <span data-ttu-id="480be-139">Legg til en rad i tabellen.</span><span class="sxs-lookup"><span data-stu-id="480be-139">Add a row to the table.</span></span>

    1. <span data-ttu-id="480be-140">Sett **Skjemanavn** til **Verdi**.</span><span class="sxs-lookup"><span data-stu-id="480be-140">Set the **Schema name** to **Value**.</span></span>
    2. <span data-ttu-id="480be-141">Sett **Skjemabane** til **/payload[\*]/value**.</span><span class="sxs-lookup"><span data-stu-id="480be-141">Set the **Schema path** to **/payload[\*]/value**.</span></span>
    3. <span data-ttu-id="480be-142">Sett **Beskrivelse** til **Meldingsverdi**.</span><span class="sxs-lookup"><span data-stu-id="480be-142">Set the **Description** to **Message value**.</span></span>

    <span data-ttu-id="480be-143">Du trenger ikke å definere alle egenskapene i meldingen, men bare de du trenger.</span><span class="sxs-lookup"><span data-stu-id="480be-143">You don't need to define all the properties in the message, only the ones that you need.</span></span> <span data-ttu-id="480be-144">I dette eksemplet har du ikke opprettet en rad for **Rottidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="480be-144">In this example, you did not create a row for **Root timestamp**.</span></span> <span data-ttu-id="480be-145">Banen til **Rottidsstempel** vil være **/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="480be-145">The path for **Root timestamp** would be **/timestamp**.</span></span>
  
10. <span data-ttu-id="480be-146">Klikk **Neste** for å gå til siden **Tilordning av sensorskjema for utstyr**.</span><span class="sxs-lookup"><span data-stu-id="480be-146">Click **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="480be-147">I raden for **Ressurs-ID for utstyr** setter du **Skjemanavn** til **ID**.</span><span class="sxs-lookup"><span data-stu-id="480be-147">In the row for **Equipment resource ID** set the **Schema name** to **ID**.</span></span> <span data-ttu-id="480be-148">De gyldige verdiene vises i en rullegardintabell.</span><span class="sxs-lookup"><span data-stu-id="480be-148">The valid values are displayed in a dropdown table.</span></span>
12. <span data-ttu-id="480be-149">I raden for **UTC-tidspunkt** setter du **Skjemanavn** til **Tidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="480be-149">In the row for **UTC time** set the **Schema name** to **Timestamp**.</span></span> <span data-ttu-id="480be-150">De gyldige verdiene vises i en rullegardintabell.</span><span class="sxs-lookup"><span data-stu-id="480be-150">The valid values are displayed in a dropdown table.</span></span>
13. <span data-ttu-id="480be-151">I raden for **Delprodusert signal** setter du **Skjemanavn** til **Verdi**.</span><span class="sxs-lookup"><span data-stu-id="480be-151">In the row for **Part produced signal** set the **Schema name** to **Value**.</span></span> <span data-ttu-id="480be-152">De gyldige verdiene vises i en rullegardintabell.</span><span class="sxs-lookup"><span data-stu-id="480be-152">The valid values are displayed in a dropdown table.</span></span>
14. <span data-ttu-id="480be-153">Klikk **Neste** for siden **Konfigurasjon av ressurs-ID for utstyr**.</span><span class="sxs-lookup"><span data-stu-id="480be-153">Click **Next** for the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="480be-154">I dette trinnet tilordner du meldingsverdiene for IoT-huben til ressursene for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="480be-154">In this step, you map the IoT Hub message values to the Supply Chain Management resources.</span></span>

    1. <span data-ttu-id="480be-155">I tabellen **Signaldataverdier** legger du til en ny rad og angir **IoTInt.Machine1225.PartOut** i kolonnen **Verdi**.</span><span class="sxs-lookup"><span data-stu-id="480be-155">In the **Signal Data Values** table, add a new row, and enter **IoTInt.Machine1225.PartOut** in the **Value** column.</span></span> <span data-ttu-id="480be-156">Verdien **IoTInt.Machine1225.PartOut** kommer fra egenskapen JSON **id** i IoT-hubmeldingen.</span><span class="sxs-lookup"><span data-stu-id="480be-156">The value **IoTInt.Machine1225.PartOut** comes from the JSON **id** property in the IoT hub message.</span></span>
    2. <span data-ttu-id="480be-157">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="480be-157">Click **Save**.</span></span>
    3. <span data-ttu-id="480be-158">I tabellen **Tilordning av forretningspost** klikker du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="480be-158">In the **Business Record Mapping** table, click **New**.</span></span> <span data-ttu-id="480be-159">Standardverdien for **typen forretningspost** fylles ut automatisk, og du trenger ikke endre den.</span><span class="sxs-lookup"><span data-stu-id="480be-159">The default value for the **Business record type** is autopopulated, and you don't need to change it.</span></span>
    4. <span data-ttu-id="480be-160">I kolonnen **Forretningspost** velger du maskinressursen for Supple Chain Management som denne signalverdien sendes fra.</span><span class="sxs-lookup"><span data-stu-id="480be-160">In the **Business record** column, select the Supple Chain Management machine resource this signal value is being sent from.</span></span>
    5. <span data-ttu-id="480be-161">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="480be-161">Click **Save**.</span></span>
    6. <span data-ttu-id="480be-162">Gjenta disse trinnene ved å legge til en ny tilordning av forretningspost for **Machine1226**.</span><span class="sxs-lookup"><span data-stu-id="480be-162">Repeat these steps, adding a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="480be-163">Du kan tilordne flere signaldataverdier til én post i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="480be-163">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="480be-164">Bruk kolonnen **Valgte** til å velge hvilke maskiner du vil behandle.</span><span class="sxs-lookup"><span data-stu-id="480be-164">Use the **Selected** column to choose which machines you want to process.</span></span> <span data-ttu-id="480be-165">Du trenger ikke definere alle signalverdiene, og du behøver ikke å velge alle maskiner.</span><span class="sxs-lookup"><span data-stu-id="480be-165">You do not have to define all signal values and you do not have to select all machines.</span></span>
17. <span data-ttu-id="480be-166">Klikk **Neste** for å gå til siden **Konfigurasjon av delprodusert signal**.</span><span class="sxs-lookup"><span data-stu-id="480be-166">Click **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="480be-167">I tabellen **Signaldataverdier** legger du til en rad og setter **Verdi** til **Sann**.</span><span class="sxs-lookup"><span data-stu-id="480be-167">In the **Signal Data Values** table, add a row, and set **Value** to **True**.</span></span> <span data-ttu-id="480be-168">Verdien **Sann** kommer fra egenskapen JSON **value** i IoT-hubmeldingen.</span><span class="sxs-lookup"><span data-stu-id="480be-168">The value **True** comes from the JSON **value** property in the IoT hub message.</span></span> <span data-ttu-id="480be-169">Du kan legge til så mange verdier du trenger i .</span><span class="sxs-lookup"><span data-stu-id="480be-169">You can add as many values as you need for your scenario.</span></span>
19. <span data-ttu-id="480be-170">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="480be-170">Click **Save**.</span></span>
20. <span data-ttu-id="480be-171">Klikk **Neste** for å gå til siden **Terskal for nedetid for utstyr**.</span><span class="sxs-lookup"><span data-stu-id="480be-171">Click **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="480be-172">De oppførte maskinene er de som tidligere var tilordnet til signalverdier.</span><span class="sxs-lookup"><span data-stu-id="480be-172">The machines listed are the machines previously mapped to signal values.</span></span> <span data-ttu-id="480be-173">I dette trinnet definerer du en terskel for å fastslå om en maskin er nede.</span><span class="sxs-lookup"><span data-stu-id="480be-173">In this step, you define a threshold to determine if a machine is down.</span></span> <span data-ttu-id="480be-174">Hvis du for eksempel setter terskelen til 10, genererer Supply Chain Management en varsling hvis det ikke vises en melding om en del ute fra en maskin på 10 minutter.</span><span class="sxs-lookup"><span data-stu-id="480be-174">For example, if you set the threshold to 10, Supply Chain Management generates a notification if there is no part out message from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="480be-175">Klikk **Neste** for å gå til siden **Aktiver scenario**.</span><span class="sxs-lookup"><span data-stu-id="480be-175">Click **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="480be-176">Aktiver/deaktiver glidebryteren for å aktivere .</span><span class="sxs-lookup"><span data-stu-id="480be-176">Toggle the slider to enable the scenario.</span></span>
22. <span data-ttu-id="480be-177">Klikk **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="480be-177">Click **Finish**.</span></span>

<span data-ttu-id="480be-178">Scenariooppsettet er fullført.</span><span class="sxs-lookup"><span data-stu-id="480be-178">The scenario setup is complete.</span></span> <span data-ttu-id="480be-179">IoT-intelligens starter behandlingen av IoT-hubmeldingene automatisk.</span><span class="sxs-lookup"><span data-stu-id="480be-179">IoT Intelligence will automatically start processing the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="480be-180">Konfigurere  **Produktkvalitet** i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="480be-180">Configure the **Product quality** scenario in Supply Chain Management</span></span>

<span data-ttu-id="480be-181"> **Produktkvalitet** genererer en varsling hvis et attributt for en vare er utenfor et bestemt område.</span><span class="sxs-lookup"><span data-stu-id="480be-181">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="480be-182">En sensor kan for eksempel sende vekten for hver vare til IoT-huben.</span><span class="sxs-lookup"><span data-stu-id="480be-182">For example, a sensor could send the weight of each item to IoT Hub.</span></span> <span data-ttu-id="480be-183">I Supply Chain Management blir det generert en varsling hvis varen er for tung eller for lett.</span><span class="sxs-lookup"><span data-stu-id="480be-183">In Supply Chain Management, a notification would be generated if the item was too heavy or too light.</span></span>

<span data-ttu-id="480be-184"> har disse avhengighetene:</span><span class="sxs-lookup"><span data-stu-id="480be-184">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="480be-185">En produksjonsordre må kjøre på en tilordnet maskin og produsere et produkt med et tilordnet partiattributt for at et varsel skal kunne utløses.</span><span class="sxs-lookup"><span data-stu-id="480be-185">A Production Order must be running on a mapped machine and producing a product with a mapped batch attribute for an alert to be triggered.</span></span>
+ <span data-ttu-id="480be-186">Et signal som representerer partiattributtet, må sendes til IoT-huben med et unikt egenskapsnavn.</span><span class="sxs-lookup"><span data-stu-id="480be-186">A signal representing the batch attribute must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="480be-187">En egenskap for millisekundstidsstempel for Unix må finnes i IoT-hubmeldingen.</span><span class="sxs-lookup"><span data-stu-id="480be-187">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="480be-188">Konfigurere  **Produksjonsforsinkelser** i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="480be-188">Configure the **Production delays** scenario in Supply Chain Management</span></span>

<span data-ttu-id="480be-189"> **Produksjonsforsinkelser** genererer en varsling hvis produksjonsgjennomstrømningen faller under en terskelverdi.</span><span class="sxs-lookup"><span data-stu-id="480be-189">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="480be-190">I dette scenarioet sendes det et **PartOut**-signal til IoT-hub for hver vare som produseres.</span><span class="sxs-lookup"><span data-stu-id="480be-190">In this scenario, a **PartOut** signal is sent to IoT Hub for each item produced.</span></span> <span data-ttu-id="480be-191">I Supply Chain Management beregnes ordreforsinkelsen på grunnlag av hvor lenge produksjonsordren er planlagt å kjøres, hvor mange varer som skal produseres, hvor lenge jobben har kjørt og hvor mange **PartOuts**-signaler som mottas.</span><span class="sxs-lookup"><span data-stu-id="480be-191">In Supply Chain Management, the order delay is calculated based on how long the production order is scheduled to run, how many items should be produced, how long the job has been running, and how many **PartOut** signals are received.</span></span> <span data-ttu-id="480be-192">Det vil bli generert en forsinkelsesvarsling hvis antallet **PartOuts**-signaler for jobben faller under terskelverdien for den forventede verdien.</span><span class="sxs-lookup"><span data-stu-id="480be-192">A delay notification would be generated if the number of the **PartOut** signals for the job falls below the threshold value of the expected value.</span></span>

<span data-ttu-id="480be-193"> har disse avhengighetene:</span><span class="sxs-lookup"><span data-stu-id="480be-193">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="480be-194">En produksjonsordre må kjøre på en tilordnet maskin for at et varsel skal kunne utløses.</span><span class="sxs-lookup"><span data-stu-id="480be-194">A Production Order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="480be-195">Et signal som representerer en tilordnet maskins signal for del ute, må sendes til IoT-huben med et unikt egenskapsnavn.</span><span class="sxs-lookup"><span data-stu-id="480be-195">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="480be-196">En egenskap for millisekundstidsstempel for Unix må finnes i IoT-hubmeldingen.</span><span class="sxs-lookup"><span data-stu-id="480be-196">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="how-to-disable-a-scenario"></a><span data-ttu-id="480be-197">Deaktivere et scenario</span><span class="sxs-lookup"><span data-stu-id="480be-197">How to disable a scenario</span></span>

<span data-ttu-id="480be-198">Hvis du vil deaktivere et scenario, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="480be-198">To disable a scenario, follow these steps:</span></span>

1. <span data-ttu-id="480be-199">I Supply Chain Management går du til **Produksjonskontroll \> Oppsett \> IoT-intelligens \> Scenariobehandling**.</span><span class="sxs-lookup"><span data-stu-id="480be-199">In Supply Chain Management, navigate to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="480be-200">Klikk **Konfigurer** i .</span><span class="sxs-lookup"><span data-stu-id="480be-200">Click **Configure** on the scenario.</span></span>
3. <span data-ttu-id="480be-201">Klikk **Neste** for å gå til den siste veiviserkategorien.</span><span class="sxs-lookup"><span data-stu-id="480be-201">Click **Next** to get to the last wizard tab.</span></span>
4. <span data-ttu-id="480be-202">Veksle glidebryteren for å deaktivere .</span><span class="sxs-lookup"><span data-stu-id="480be-202">Toggle the slider to disable the scenario.</span></span>

---
title: 'Data-Driven Manufacturing Operations'
subtitle: 'Fostering a culture of data-driven decision-making in pharmaceutical manufacturing.'
date: 2025-01-01 00:00:00
description: 'Data-Driven Manufacturing Operations'
featured_image: '/images/projects/digital-manufacturing/1.jpg'
---

![](/images/projects/digital-manufacturing/1.jpg)

## Summary

A biopharmaceutical, also known as a biological medical product, or **biologic**, is any pharmaceutical **drug product** manufactured in, extracted from, or semisynthesized from biological sources. Biopharmaceuticals may be produced from microbial cells, mammalian cell lines, or plant cell cultures in **bioreactors**. In the final stage of the (sterile) manufacture of such large molecules, the active pharmaceutical ingredient (or **drug substance**), excipients, and water must be amalgamated and transferred into the designated containers (i.e., vials or syringes). Despite the automation of the actual production processes (e.g., filling or visual inspection), numerous other processes such as planning and troubleshooting are manual and time-consuming.

<center>
<figure>
<img src="/images/projects/digital-manufacturing/schema.png" width="1000">
<figcaption><b>Fig. 1:</b> Operational workflow diagram.</figcaption>
</figure>
</center>

A plethora of **data** is generated in this setting, which can be utilized for decision-making or for sampling. This encompasses data from manufacturing instructions, deviation reports, electronic batch records, sensor and alarm data from the operational historian, or business data from the enterprise resource planning system. 

<center>
<figure>
<img src="/images/projects/digital-manufacturing/data_sources.png" width="1000">
<figcaption><b>Fig. 2:</b> A subset of data sources and their relationship with each other.</figcaption>
</figure>
</center>

The objective of this endeavour was to scrutinize and digitalize the (remaining) manual processes and to leverage the available data to cultivate a culture of data-driven pharmaceutical manufacturing. This culminated, for instance, in the establishment of a **digital hub**.

<!-- <div class="gallery" data-columns="1">
    <img src="/images/projects/digital-manufacturing/digital_hub.png">
</div> -->

<center>
<figure>
<img src="/images/projects/digital-manufacturing/digital_hub.png" width="1000">
<figcaption><b>Fig. 3:</b> Digital hub.</figcaption>
</figure>
</center>

<!-- > "Do not wait; the time will never be 'just right.' Start where you stand, and work with whatever tools you may have at your command, and better tools will be found as you go along." - George Herbert -->

## Examples

### Retrieval-Augmented Generation

Important text documents can be manufacturing instructions, regulatory documents or guidelines for operational excellence, for example.

#### Regulatory Bot

**User**: What are relevant principles applicable to sterile manufacturing?

**Assistant**: The relevant principles applied to sterile manufacturing can be summarized as follows:

1. Facility, Equipment, and Process Design  
    - Must be optimized, qualified, and validated according to Good Manufacturing Practices (GMP) guidelines. Use of appropriate technology such as Restricted Access Barriers Systems (RABS), isolators, and rapid microbial testing systems to protect the product from potential contamination.[^1]
    - Should include measures to prevent contamination, such as cleanrooms, airlocks, RABS, and isolator.

2. Personnel  
    - Personnel should possess adequate qualifications, experience, training, and attitude focused on protecting sterile products during manufacturing, packaging, and distribution.
    - Proper gowning and hygiene practices are crucial to minimizing contamination risks.

3. Quality Risk Management (QRM)  
    - Processes, equipment, facilities, and activities should be managed in accordance with QRM principles to proactively identify, evaluate, and control potential risks to quality.
    - QRM should be integrated into all areas of the product life cycle, aiming to minimize microbial contamination and ensure product quality.

4. Quality Assurance and Quality Control (QA/QC)  
    - Quality Assurance (QA) should involve established and validated methods of manufacturing and control, and a Contamination Control Strategy (CCS) covering all critical control points and assessing the effectiveness of contamination control measures must be implemented.
    - QC includes specific requirements for testing raw materials, components, products, and environmental monitoring, especially focusing on microbial quality and bioburden testing.

5. Premises and Cleanroom Standards  
    - Sterile manufacturing must be carried out in appropriately designed cleanrooms maintained to specific cleanliness standards and fitted with efficient air filtration systems. There are defined grades (A, B, C, and D) for cleanroom environments based on the activity and contamination risk involved.

6. Production and Sterilization Technologies  
    - Specific approaches and technologies for aseptic and terminal sterilization processes, including handling of materials, equipment sterilization, and microbial contamination detection must be employed. The process simulation and validation are important to ensure sterility throughout the production.

7. Contamination Control  
    - Continuous and effective contamination control, including cleaning, disinfection, and depyrogenation (removal/inactivation of pyrogens) are critical. Proper environment monitoring, including viable and non-viable particle monitoring, is essential to ensure ongoing sterility compliance.

8. Documentation and Record Keeping  
    - Thorough documentation and review of records related to aseptic processing, including process simulations, interventions, environmental monitoring data, and microbial testing results, are required to verify compliance and address any issues effectively.

Understanding and implementing these principles are key to maintaining the quality and sterility of manufactured products, ensuring their safety and efficacy for patients.

[^1]: EU Guidelines for Good Manufacturing Practice for Medicinal Products for Human and Veterinary Use

#### Operational Excellence Bot

**User**: What is overall asset effectiveness and how is it defined?

**Assistant**: Overall Asset Effectiveness (OAE) is a metric used to measure the utilization and efficiency of assets within a production environment. It is typically calculated by evaluating several key factors related to the performance and utilization of assets over a given period. This metric helps in ensuring that assets are being used optimally to maximize productivity and minimize downtime.

The specific definition and calculation methods for Overall Asset Effectiveness are detailed in the relevant documentation for Novartis Operational Standards for Supply Chain Excellence (NOSSCE).

The precise definition and applicable methods may vary slightly based on the implementation details from the NOSSCE manual for different sites or aspects of the supply chain. Therefore, for the most accurate and complete understanding, it is recommended to refer to the specific metrics handbook and related documents.

If you have any more specific questions or need further details, feel free to ask! 

---

**User**: Okay, great! Can you give one example for any type of asset?

**Assistant**: Sure! Let's consider an example of Overall Asset Effectiveness (OAE) for a production line in a manufacturing plant, such as a packaging line for pharmaceuticals.

###### Example: Pharmaceutical Packaging Line

To calculate OAE for a pharmaceutical packaging line, you would gather data on three main components:
1. **Availability**
2. **Performance**
3. **Quality**

###### Availability
Availability is the ratio of the actual operating time to the planned operating time. It accounts for downtime due to scheduled maintenance, breakdowns, and other stoppages.

- **Formula**: 
$\text{Availability} = \frac{\text{Operating Time}}{\text{Scheduled Production Time} - \text{Downtime}}$

###### Performance
Performance measures how well the line is running during the actual operating time compared to its designed speed.

- **Formula**: 
$\text{Performance} = \frac{\text{Actual Output}}{\text{Theoretical Output}}$

###### Quality
Quality is the ratio of the number of good units produced to the total units started. This accounts for defects and reworks.

- **Formula**: 
$\text{Quality} = \frac{\text{Good Units}}{\text{Total Units Started}}$

Finally, to calculate the Overall Asset Effectiveness:
$\text{OAE} = \text{Availability} \times \text{Performance} \times \text{Quality}$

###### Practical Example Calculation:
1. **Scheduled Production Time**: 480 minutes (8 hours shift)
2. **Downtime**: 60 minutes (breaks, maintenance)
3. **Operating Time**: 420 minutes (480 - 60)
4. **Theoretical Line Speed**: 1000 units/hour
5. **Actual Line Speed**: 900 units/hour
6. **Total Units Started**: 6000 units
7. **Good Units Produced**: 5700 units

###### Calculation Components:
* Availability: $\frac{420}{480} = 0.875$
* Performance: $\frac{900 \times 7}{1000 \times 7} = 0.9$
* Quality: $\frac{5700}{6000} = 0.95$

###### OAE Calculation:
$\text{OAE} = 0.875 \times 0.9 \times 0.95 = 0.748$.

This means the Overall Asset Effectiveness for the packaging line is 74.8%.

This example illustrates the application of OAE to measure and improve asset utilization, performance, and quality within a manufacturing setup.

For further details on the metrics, calculations, and examples, please refer to the NOSSCE metrics and handbooks provided in the documents.[^2] [^3] [^4]

[^2]: Supply Model_Stein Steriles_V6.pdf
[^3]: NOSSCE Manual Sites v4.0.pdf
[^4]: NOSSCE Metrics Handbook DP FP Sites v7.0.pdf

### Data Analytics

Some data sources that can be used for learning are sensor data from production equipment or entries in electronic batch records.

<div class="gallery" data-columns="1">
    <img src="/images/projects/digital-manufacturing/requalification_assessment.png">
    <img src="/images/projects/digital-manufacturing/requalification_assessment_1.png">
    <img src="/images/projects/digital-manufacturing/root_cause_analysis_1.png">
    <img src="/images/projects/digital-manufacturing/root_cause_analysis_2.png">
    <img src="/images/projects/digital-manufacturing/yields.png">
    <img src="/images/projects/digital-manufacturing/yields_1.png">
</div>
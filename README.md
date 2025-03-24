# GenAI-STIX2.1-Generator
GenAI-STIX2.1-Generator is a tool that leverages Azure OpenAI capabilities to transform threat intelligence reports from unstructured web input into structured STIX 2.1 format.

[Blog post](https://medium.com/@antonio.formato/from-unstructured-threat-intelligence-to-stix-2-1-bundles-with-generative-ai-1065ce399e63)

# From Unstructured Threat Intelligence to STIX 2.1 Bundles with Generative AI

## Overview

Cybersecurity relies on the rapid exchange of actionable intelligence. Yet, much of the threat intelligence shared today is unstructured, making it difficult to standardize and operationalize. This repository demonstrates how Generative AI can bridge this gap by automating the creation of STIX 2.1 bundles from unstructured threat reports.

The Structured Threat Information Expression (STIX) 2.1 standard provides a machine-readable framework for sharing cyber threat intelligence. However, creating STIX bundles manually is time-consuming and prone to errors. This project leverages GPT-4 to automate the extraction, structuring, and validation of STIX Domain Objects (SDOs), Cyber Observables (SCOs), and Relationship Objects (SROs) from unstructured text.

## Key Features

- **Automated Extraction**: Uses Generative AI to analyze unstructured threat reports and identify key indicators, relationships, and technical details.
- **STIX-Compliant Output**: Ensures generated STIX objects adhere to the STIX 2.1 schema for interoperability and standardization.
- **Flexible Configuration**: Supports Azure OpenAI GPT-4o by default but can be adapted for other LLMs.
- **Visualization**: Includes tools to render and inspect generated STIX bundles for validation and analysis.

## Getting Started

### Prerequisites

- Python 3.9 or higher
- Access to Azure OpenAI GPT-4o or an equivalent LLM
- Required Python packages:
  - `python-dotenv`
  - `stix2`
  - `httpx`
  - `BeautifulSoup`

## Usage

### Extracting STIX Bundles from Threat Reports
This project automates the process of converting unstructured threat intelligence reports into STIX 2.1 bundles. Below is an example workflow demonstrating the usage of the tool:

1. **Input Threat Report**  
   Provide the URL of a threat intelligence report. For instance, the [Midnight Blizzard campaign blog post](https://www.microsoft.com/en-us/security/blog/2024/10/29/midnight-blizzard-conducts-large-scale-spear-phishing-campaign-using-rdp-files/) by Microsoft Threat Intelligence.

2. **Run the Notebook**  
   Use the provided Jupyter Notebook to execute the following steps:
   - Extract unstructured text from the provided URL using the web scraper.
   - Generate STIX Domain Objects (SDOs), Cyber Observables (SCOs), and Relationship Objects (SROs) using Generative AI.
   - Validate the generated STIX objects against the STIX 2.1 schema.

3. **Generate the STIX Bundle**  
   The notebook combines SDOs, SCOs, and SROs into a complete STIX bundle in JSON format. The bundle is saved to a timestamped file and displayed in the console.

4. **Visualize the STIX Bundle**  
   Utilize the STIX viewer to inspect the generated data visually. For example, use the [OASIS CTI-STIX Visualization tool](https://oasis-open.github.io/cti-stix-visualization/) to render the relationships and objects.

## Contributing

We welcome contributions to enhance this project. Here's how you can help:

- **Testing and Feedback**: Try the tool and share your insights to improve its performance and usability.
- **Improving Prompts**: Help refine the AI prompts for better extraction and accuracy of STIX objects.
- **Extending Functionality**: Add support for new STIX object types, build additional features, or improve existing workflows.
- **Open Discussions**: Join the conversation to explore innovative use cases and share your ideas.

Your contributions will help make this project more robust and impactful. Thank you for your support!

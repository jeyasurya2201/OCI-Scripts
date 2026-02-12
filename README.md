# OCI Sandbox Resource Inventory

##  Overview

This repository contains a Python utility to extract a complete inventory of
Oracle Cloud Infrastructure (OCI) resources from the **Sandbox** compartment
and all of its child compartments recursively.

The script uses OCI Resource Search to collect resource metadata and exports
the results to a CSV file along with a ZIP archive.

This is a **read-only utility** intended for audit, compliance, and reference purposes.

---

## Features

- Automatically discovers the Sandbox compartment
- Recursively traverses all child compartments
- Extracts all OCI resource types
- Builds full compartment hierarchy paths
- Exports results to CSV
- Creates ZIP archive for easy sharing
- Safe to run in production tenancies

---

## Prerequisites

- Python 3.8 or later
- OCI SDK for Python

Install SDK:
```bash
pip install oci
OCI CLI configured with a valid profile:

~/.oci/config
The user must have permissions to:

List compartments

Use Resource Search

▶️ Usage
Clone the repository:

git clone https://github.com/<your-username>/oci-sandbox-resource-inventory.git
cd oci-sandbox-resource-inventory
Run the script:

python3 oci_sandbox_compartment_resource_inventory.py


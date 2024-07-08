> [!summary] 
> Business Central includes a demo tool and demo data set designed for manufacturing scenarios, featuring the fictitious company Contoso Coffee. This extension helps presales specialists demonstrate premium capabilities by installing it in any environment.

#### Definitions

- **Contoso Coffee**: A fictitious company producing coffee makers, used for demo data in Business Central.
- **Demo Tool**: An extension for demonstrating manufacturing scenarios in Business Central.
- **Demo Data**: Pre-configured data sets for various manufacturing scenarios.

> [!info] Demo Data and Tool

- Available as source code on on-premises product media.
- Can be installed on top of Cronus or My Company environments.
- Supports multiple manufacturing scenarios.

> [!example] Contoso Coffee Products

- **SP-SCM1009 Airpot**: BOM with subassembly, Routing, alternative routings for subcontractors, Standard costing.
- **SP-SCM1011 Airpot Duo**: Item tracking required, Special costing.
- **SP-SCM1004 Autodrip**: BOM with subassembly, Routing, demonstrates flushing methods, Standard costing.
- **SP-SCM1008 AutoDripLite**: Three variants, phantom BOM, Standard costing.

> [!info] Supported Scenarios

1. Create a new production BOM and BOM version
2. Create a new routing
3. Create a firm planned production order and change it
4. Combine automatic and manual flushing
5. Use order planning to create and reserve supply
6. Set up and process a subcontracting operation
7. Set up new capacity
8. Demand forecast for item variants

> [!tip] Setup Instructions

1. Install Contoso Coffee Demo Dataset and country-specific app in a relevant company.
2. Create a new company using the Tell Me functionality, name it Contoso Coffee.
3. Ensure "Production - Setup Data Only" is selected.
4. Install necessary apps from Extension Management or Marketplace.
5. Configure demo data settings (e.g., Starting Year, Manufacturing Location).

> [!example] Configuring Demo Data

- **Starting Year**: Specify the first year for demonstration data.
- **Manufacturing Location**: Default is NORTH.
- **Company Type**: Indicate if VAT or sales tax reporting is required.
- **General Posting Groups**: Define codes for domestic, capacity, retail, and raw material.
- **Base VAT Code**: Set the VAT product group for items.
- **Finished Code**: Set the product group for finished items.
- **Price Factor**: Conversion factor for currency prices.
- **Rounding Precision**: Define rounding rules for consumption quantities.

> [!info] Running Scenarios

- Once demo data is created, you can run various manufacturing scenarios.
- Ensure the user experience is set to Premium in the Company Information page.
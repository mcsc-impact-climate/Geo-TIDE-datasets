# GeoJSON files for Trucking Industry Decarbonization 

## Summary
This dataset provides GeoJSON files developed by the MIT Climate & Sustainability Consortium for geospatial visualization and analysis of opportunities to transition trucking fleets in the U.S. to low-carbon energy carriers. The layers are synthesized from diverse federal sources, including BTS, FHWA, EPA, DOE, and EIA, and have been geometry-simplified, normalized, and thematically grouped to support transition planning. 

The Geospatial Trucking Industry Decarbonization Explorer (Geo-TIDE) is an interactive web interface that allows users to geospatially visualize and overlay the GeoJSON files contained in this dataset to support opportunity identification and transition planning. 

## Data

Each GeoJSON file encodes geospatial features such as states, highways, and facilities in Web Mercator format (EPSG:3857). In most files, the geospatial features have associated attributes, which can be visualized as gradients on the Geo-TIDE interface or other GIS software such as QGIS.  

The GeoJSON files are stored on a public AWS S3 bucket, and will soon be hosted by the AWS Open Data Sponsorship Program. The table below summarizes the major categories of files included in the dataset, broken down according to their geospatial format. More information and attributions to original data sources can be found in [this Zenodo record](https://zenodo.org/records/15851359). 

Area features are bounded regions such as states, represented in the GeoJSON files as Polygon or MultiPolygon objects. Highway features are connected highway links, represented as LineString objects. Point features are localized objects such as charging/refueling stations or hydrogen production facilities, represented with Point objects.

### Summary of file categories
<table>
  <thead>
    <tr>
      <th>Data Layer</th>
      <th>Filename(s)</th>
      <th>Original Data Source(s)</th>
      <th>Reference Section in Technical Guide</th>
    </tr>
  </thead>
  <tbody>
    <tr><th colspan="4">Area Features</th></tr>
    <tr>
      <td>Truck Imports and Exports</td>
      <td>faf5_freight_flows/*.geojson</td>
      <td>FAF5, USDOT</td>
      <td>4.1, 5.3, 4.2, A.1</td>
    </tr>
    <tr>
      <td>Grid Emission Intensity</td>
      <td>grid_emission_intensity/*.geojson</td>
      <td>EPA eGRID, NREL Cambium</td>
      <td>5.1</td>
    </tr>
    <tr>
      <td>Hourly Grid Emissions</td>
      <td>daily_grid_emission_profiles/*.geojson</td>
      <td>NREL Cambium</td>
      <td>5.2</td>
    </tr>
    <tr>
      <td>Grid Generation and Capacity</td>
      <td>gen_cap_2022_state_merged.geojson</td>
      <td>EIA Form 860, 923</td>
      <td>6.1, A.2</td>
    </tr>
    <tr>
      <td>Commercial Electricity Price</td>
      <td>electricity_rates_by_state_merged.geojson</td>
      <td>EIA</td>
      <td>5.1</td>
    </tr>
    <tr>
      <td>Maximum Demand Charge (utility- and state-level)</td>
      <td>demand_charges_merged.geojson<br>demand_charges_by_state.geojson</td>
      <td>Utility Tariffs, NREL dGen</td>
      <td>5.1</td>
    </tr>
    <tr>
      <td>Planned Infrastructure Projects (regions)</td>
      <td>bayarea.geojson<br>saltlake.geojson</td>
      <td>USDOT, FHWA, State DOTs</td>
      <td>4.3</td>
    </tr>
    <tr>
      <td>State-Level Incentives and Regulations</td>
      <td>incentives_and_regulations/*.geojson</td>
      <td>DSIRE, NASEO, State Websites</td>
      <td>4.4</td>
    </tr>
    <tr>
      <td>Lifecycle Truck Emissions</td>
      <td>costs_and_emissions/*emissions_per_mile*.geojson</td>
      <td>GREET, AFLEET, ICCT</td>
      <td>7.1, A.3</td>
    </tr>
    <tr>
      <td>Total Cost of Truck Ownership</td>
      <td>costs_and_emissions/costs_per_mile*.geojson</td>
      <td>ATRI, NACFE, OEM Data</td>
      <td>7.1, A.3</td>
    </tr>
    <tr>
      <td>Energy Demand from Electrified Trucking</td>
      <td>trucking_energy_demand.geojson</td>
      <td>This Study (Geo-TIDE), EIA</td>
      <td>6.1, A.2</td>
    </tr>
    <tr><th colspan="4">Highway Features</th></tr>
    <tr>
      <td>Interstate Highway Flows</td>
      <td>highway_assignment_links_interstate.geojson</td>
      <td>FAF5</td>
      <td>4.5</td>
    </tr>
    <tr>
      <td>Planned Infrastructure Corridors</td>
      <td>northeast.geojson<br>midwest.geojson<br>la_i710.geojson<br>h2la.geojson<br>northeast.geojson</td>
      <td>USDOT, DOE Joint Office</td>
      <td>4.3</td>
    </tr>
    <tr><th colspan="4">Point Features</th></tr>
    <tr>
      <td>Charge/Fuel Stations</td>
      <td>US_*.geojson</td>
      <td>AFDC, Alternative Fuels Data Center</td>
      <td>4.6</td>
    </tr>
    <tr>
      <td>Hydrogen Production Facilities</td>
      <td>electrolyzer_*.geojson<br>refinery.geojson</td>
      <td>DOE Hydrogen Infrastructure</td>
      <td>4.7</td>
    </tr>
    <tr>
      <td>Truck Stop Parking Locations</td>
      <td>Truck_Stop_Parking.geojson</td>
      <td>Private Aggregators (e.g., Trucker Path), AFDC</td>
      <td>4.8</td>
    </tr>
    <tr>
      <td>Principal Ports</td>
      <td>Principal_Port.geojson</td>
      <td>BTS, USACE</td>
      <td>4.8</td>
    </tr>
    <tr>
      <td>Savings from Pooled Charging Infrastructure</td>
      <td>infrastructure_pooling_thought_experiment/*.geojson</td>
      <td>Geo-TIDE Analysis</td>
      <td>4.9</td>
    </tr>
    <tr><th colspan="4">Multiple Features</th></tr>
    <tr>
      <td>National ZEF Corridor Strategy</td>
      <td>ZEF_Corridor_Strategy/*.geojson</td>
      <td>DOE Joint Office, US DOT</td>
      <td>4.10</td>
    </tr>
  </tbody>
</table>



## Data Access

### Geo-TIDE

The Geo-TIDE tool provides an interactive platform to directly visualize, overlay, and download the GeoJSON files. A public version of the Geo-TIDE tool is hosted on the MIT Climate & Sustainability Consortium's DataHub website. 



The Geo-TIDE tool can also be hosted locally using the . Note that the locally-hosted version of the tool excludes the private data upload and overlay feature available on the public tool, as this is facilitated by the DataHub 

### Amazon S3

### CLI

## Tutorials

The following video tutorials provide examples of how to access 

## References


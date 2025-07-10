# GeoJSON files to Support Trucking Industry Decarbonization Planning

## Summary
This dataset provides GeoJSON files developed by the MIT Climate & Sustainability Consortium (MCSC) for geospatial visualization and analysis of opportunities to transition trucking fleets in the U.S. to low-carbon energy carriers. The layers are synthesized from diverse federal sources, including BTS, FHWA, EPA, DOE, and EIA, and have been geometry-simplified, normalized, and thematically grouped to support transition planning. 

The MCSC's Geospatial Trucking Industry Decarbonization Explorer (Geo-TIDE) is an interactive web interface that allows users to geospatially visualize and overlay the GeoJSON files contained in this dataset to support opportunity identification and transition planning. 

## Data

Each GeoJSON file encodes geospatial features such as states, highways, and facilities in Web Mercator format (EPSG:3857). In most files, the geospatial features have associated attributes, which can be visualized as gradients on the Geo-TIDE interface or other GIS software such as QGIS.  

The GeoJSON files are stored on a public AWS S3 bucket, and will soon be hosted by the AWS Open Data Sponsorship Program. The table below summarizes the major categories of files included in the dataset, broken down according to their geospatial format. More information and attributions to original data sources can be found in [this Zenodo record](https://zenodo.org/records/15851359).

Area features are bounded regions such as states, represented in the GeoJSON files as Polygon or MultiPolygon objects. Highway features are connected highway links, represented as LineString objects. Point features are localized objects such as charging/refueling stations or hydrogen production facilities, represented with Point objects.

**Table 1: Summary of GeoJSON dataset categories and sources**
<table>
  <thead>
    <tr>
      <th>Categories</th>
      <th>Filename(s)</th>
      <th>Original Data Source(s)</th>
      <th>Reference Section in the <a href=https://dspace.mit.edu/handle/1721.1/159069>Geo-TIDE Technical Guide</a></th>
    </tr>
  </thead>
  <tbody>
    <tr><th colspan="4">Area Features</th></tr>
    <tr>
      <td>Truck Imports and Exports</td>
      <td>faf5_freight_flows/*.geojson</td>
      <td>Freight Analysis Framework (ORNL, BTS, FHWA), VIUS (BTS) GREET Lifecycle Model (ANL) </td>
      <td>2.2.2, 2.2.3, 2.2, 5</td>
    </tr>
    <tr>
      <td>Grid Emission Intensity</td>
      <td>grid_emission_intensity/*.geojson</td>
      <td>eGRID (EPA)</td>
      <td>2.4.1</td>
    </tr>
    <tr>
      <td>Hourly Grid Emissions</td>
      <td>daily_grid_emission_profiles/*.geojson</td>
      <td>Electricity Maps</td>
      <td>2.4.2</td>
    </tr>
    <tr>
      <td>Grid Generation and Capacity</td>
      <td>gen_cap_2022_state_merged.geojson</td>
      <td>EIA</td>
      <td>2.6, 7</td>
    </tr>
    <tr>
      <td>Commercial Electricity Price</td>
      <td>electricity_rates_by_state_merged.geojson</td>
      <td>EIA</td>
      <td>2.4.1</td>
    </tr>
    <tr>
      <td>Maximum Demand Charge (utility- and state-level)</td>
      <td>demand_charges_merged.geojson<br>demand_charges_by_state.geojson</td>
      <td>NREL</td>
      <td>2.4.1</td>
    </tr>
    <tr>
      <td>Planned Infrastructure Projects (regions)</td>
      <td>bayarea.geojson<br>saltlake.geojson</td>
      <td>DOE</td>
      <td>2.3.1</td>
    </tr>
    <tr>
      <td>State-Level Incentives and Regulations</td>
      <td>incentives_and_regulations/*.geojson</td>
      <td>AFDC (DOE EERE)</td>
      <td>2.5</td>
    </tr>
    <tr>
      <td>Lifecycle Truck Emissions and Cost of Ownership</td>
      <td>costs_and_emissions/*.geojson</td>
      <td>NACFE, eGRID (EPA), EIA, ICCT, Minnesota DOT, motormatchup.com, notateslaapp.com </td>
      <td>2.4.3, 6</td>
    </tr>
    <tr>
      <td>Energy Demand from Electrified Trucking</td>
      <td>trucking_energy_demand.geojson</td>
      <td>Freight Analysis Framework (ORNL, BTS, FHWA) & sources listed in above row</td>
      <td>2.6, 7</td>
    </tr>
    <tr><th colspan="4">Highway Features</th></tr>
    <tr>
      <td>Interstate Highway Flows</td>
      <td>highway_assignment_links_interstate.geojson</td>
      <td>Freight Analysis Framework (ORNL, BTS, FHWA)</td>
      <td>2.2.1</td>
    </tr>
    <tr>
      <td>Planned Infrastructure Corridors</td>
      <td>northeast.geojson<br>midwest.geojson<br>la_i710.geojson<br>h2la.geojson<br>northeast.geojson</td>
      <td>DOE</td>
      <td>2.3.1</td>
    </tr>
    <tr><th colspan="4">Point Features</th></tr>
    <tr>
      <td>Charge/Fuel Stations</td>
      <td>US_*.geojson</td>
      <td>AFDC (DOE EERE)</td>
      <td>2.3.3</td>
    </tr>
    <tr>
      <td>Hydrogen Production Facilities</td>
      <td>electrolyzer_*.geojson<br>refinery.geojson</td>
      <td>DOE, PNNL</td>
      <td>2.3.4</td>
    </tr>
    <tr>
      <td>Truck Stop Parking Locations</td>
      <td>Truck_Stop_Parking.geojson</td>
      <td>BTS</td>
      <td>2.3.5</td>
    </tr>
    <tr>
      <td>Principal Ports</td>
      <td>Principal_Port.geojson</td>
      <td>BTS</td>
      <td>2.3.5</td>
    </tr>
    <tr>
      <td>Savings from Pooled Charging Infrastructure</td>
      <td>infrastructure_pooling_thought_experiment/*.geojson</td>
      <td>Freight Analysis Framework (ORNL, BTS, FHWA)</td>
      <td>None (see instead: <a href="https://dspace.mit.edu/handle/1721.1/153617">MacDonell & Borrero, 2024</a>)</td>
    </tr>
    <tr><th colspan="4">Multiple Features</th></tr>
    <tr>
      <td>National ZEF Corridor Strategy</td>
      <td>ZEF_Corridor_Strategy/*.geojson</td>
      <td>DOE, Joint Office of Energy and Transportation</td>
      <td>2.3.2</td>
    </tr>
  </tbody>
</table>

## Data Access

### Geo-TIDE

The Geo-TIDE tool provides an interactive platform to dynamically visualize, overlay, and download the GeoJSON files stored on the AWS S3 bucket. A public version of the Geo-TIDE tool is hosted on the MIT Climate & Sustainability Consortium's DataHub website. The public tool can be accessed as follows:

1. Register for a free MCSC DataHub account here: https://climatedata.mit.edu/users/register/
2. Log into your account here: https://climatedata.mit.edu/users/login/
3. Access the tool at: https://climatedata.mit.edu/faf5/transportation/

Once the tool is open, you can click on the blue 'More' button next to any layer in the Public Data selection box to view information about the layer and its sources, and click on 🔗 *Link to download the geojson file(s)* near the bottom to download the GeoJSON file (or set of files) that the layer is visualizing. This procedure is demoed in the video below:

[![Downloading GeoJSON files from Geo-TIDE](https://img.youtube.com/vi/k-r20hzqPz0/hqdefault.jpg)](https://www.youtube.com/watch?v=k-r20hzqPz0)

The Geo-TIDE tool can also be hosted locally - while still dynamically downloading the GeoJSON files from the S3 bucket - by cloning the [Geo-TIDE frontend code](https://github.com/mcsc-impact-climate/Geo-TIDE) and following the instructions in the README. 

**Note that the locally-hosted version of the tool excludes the private data upload and overlay feature available on the public tool, as this is facilitated by the DataHub website that the public tool is integrated with. 

### Access on Amazon S3

The GeoJSON dataset can also be accessed direcly on [AWS S3](https://aws.amazon.com/s3/) at s3://mcsc-datahub-public/geojsons_simplified/, where geojson files are organized into the categories described in Table 1 above. For example, to access the GeoJSON file that encodes commercial electricity prices, one would use the following S3 URI:

`s3://mcsc-datahub-public/geojsons_simplified/electricity_rates_by_state_merged.geojson`

### Download via URL

Files can also be downloaded directly, where the download url is constructed by prepending the filename with `https://mcsc-datahub-public.s3.us-west-2.amazonaws.com/geojsons_simplified/`. Eg.

[`https://mcsc-datahub-public.s3.us-west-2.amazonaws.com/geojsons_simplified/electricity_rates_by_state_merged.geojson`](https://mcsc-datahub-public.s3.us-west-2.amazonaws.com/geojsons_simplified/electricity_rates_by_state_merged.geojson)

### Download via CLI

S3 objects can also be downloaded via the AWS CLI. See these instructions for [installing the latest AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html). 

To download a specific file (eg. commercial electricity prices):

```bash
aws s3 cp s3://mcsc-datahub-public/geojsons_simplified/electricity_rates_by_state_merged.geojson .
```

To download all the GeoJSON files (appx. 1.5 GB):

```bash
mkdir geojsons_simplified
aws s3 cp s3://mcsc-datahub-public/geojsons_simplified/ geojsons_simplified --recursive
```

## Tutorials

The following tutorials walk through sample transition planning assessments that can be done with the GeoJSON files, leveraging the Geo-TIDE tool:

1. [Geo-TIDE access and getting-started exercises](https://danikam16.wixsite.com/mysite/post/accessing-and-using-the-mcsc-s-interactive-geospatial-decision-support-tool-for-trucking-fleet-decar)
2. [Which logistics facilities should a return-to-base carrier target for fleet electrification and chargers?](https://docs.google.com/presentation/d/e/2PACX-1vQZccVHZVT1QRNdhCRRI810UxGvCD3hJhxIE4CzBDbhNr9iecHV5lp2Rv87x6rik1wrCiXXUq0WfuBk/pub?start=false&loop=false&delayms=3000#slide=id.p)
3. [IWhich routes should a dry-van carrier prioritize for investment in battery electric or hydrogen trucks?](https://danikam16.wixsite.com/mysite/post/user-case-studies-for-interactive-geospatial-trucking-fleet-decision-support)

## License
[Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/legalcode)

## Suggested Attribution
Eamer, D., Borrero, M., Bashir, N., & MIT Climate & Sustainability Consortium. (2025). GeoJSON files for the MCSC's Trucking Industry Decarbonization Explorer (Geo-TIDE) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.15851359


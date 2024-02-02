
===== PURPOSE =================================================================

This document describes the format of water quality data provided as *.xlsx 
files by the GEMS/Water Data Center. 

Be advised that water quality data, for which the data provider has set a  
RESTRICTED data policy are not listed within this data export, even if they 
were visible inthe data portal. Water quality data with RESTRICTED data policy 
is only taken into account for statistical aggregates.



===== DATA DELIVERED ==========================================================

The data delivery consists of a Microsoft-Excel-file (metadata.xlsx)
containing a number of worksheets:
    
    1) A worksheet with station metadata (named Station_Metadata), containing 
       stations that satisfy the data request in terms of data availability.

    2) A worksheet with parameter metadata (named Parameter_Metadata),  
       containing a description of the requested water quality parameters.
    
    3) A worksheet with analysis methods metadata (named Methods_Metadata), 
       containing a description of the methods used for analysis of the water 
       samples.
    
    4) A variable number of worksheets, containing the actual requested water 
       quality sample data (named after the individual parameter).



===== DATA FORMAT =============================================================

The station metadata table has the following entries:

    GEMS Station Number             - GEMStat internal station number.
    
    Local Station Number            - Station number according to local station 
                                      network. 
                                      (!!! Many entries missing atm !!!)
                                      
    Historical GEMS Number          - GEMStat internal station number before
                                      migration to GEMS/Water Data Center
    
    Country Name                    - Name of country the station is located 
                                      in.
                                      
    Water Type                      - Type of water body, that is monitored by
                                      the station.
                                      
    Station Identifier              - Name of station.
    
    Station Narrative               - Description of stations location and  
                                      special conditions.
                                      
    Water Body Name                 - Name of the water body, at which the  
                                      station is located.
                                      
    Main Basin                      - Name of major river basin, that contains  
                                      the station.
                                      
    Upstream Basin Area             - Watershed area upstream of the station.
    
    Elevation                       - Mean elevation of water surface above sea
                                      level for surface waters or ground level 
                                      for groundwater stations.
                                      
    Monitoring Type                 - Type of monitoring activity.
                                      Possible entries: Baseline, Trend, 
                                      Impact, Flux.
                                      
    Date Station Opened             - Date when station was established.
                                      Format: YYYY-MM-DD
                                      
    Responsible Collection Agency   - Name of Agency responsible for the 
                                      collection of data.
                                      
    Latitude                        - Cartesian y-Coordinates in WGS84.
    
    Longitude                       - Cartesian x-Coordinates in WGS84.
    
    River Width                     - Width of river (in meters) at the station
                                      during average discharge conditions.

    Discharge                       - Average river discharge (in cubic meters 
                                      per second) at the station based on 3-5 
                                      years of data.
    
    Max. Depth                      - Maximum depth (in meters) of lake or 
                                      reservoir.
    
    Lake Area                       - Area (in square kilometers) of lake or 
                                      reservoir.

    Lake Volume                     - Volume (in cubic kilometers) of lake or 
                                      reservoir.

    Average Retention               - Retention time (in years) of water in 
                                      lake or reservoir.

    Area of Aquifer                 - Area (in square kilometers) of aquifer.

    Depth of Impermeable Lining     - Depth (in meters) of the impermeable 
                                      lining in the well (length of well 
                                      casing) from the earth surface.

    Production Zone                 - Thickness (in meters) of the layer, 
                                      through which water can enter the well.

    Mean Abstraction Rate           - Rate (in cubic meters per day) of water 
                                      abstraction from the well.

    Mean Abstraction Level          - Water level (in meters) inside well above 
                                      mean sea level during a period of normal 
                                      abstraction. 

-------------------------------------------------------------------------------

The parameter metadata table has the following entries:

    Parameter Code                  - Code of water quality parameter and 
                                      fraction that has been sampled.

    Parameter Name                  - General name of water quality parameter.
    
    Parameter Long Name             - Complete Name of water quality parameter 
                                      and fraction.
    
    Parameter Group                 - Hierarchical group that the water
                                      quality parameter is associated with.
    
    EC Number                       - Unique seven-digit identifier of the 
                                      chemical substance, as assigned by the 
                                      Ehropean Commission.
    
    CAS Number                      - Unique identifier for the chemical 
                                      substance, as assigned by Chemical 
                                      Abstracts Service (CAS) to every 
                                      chemical substance described in the open 
                                      scientific literature.
    
    ChEBI Number                    - Unique identifier for the chemical 
                                      substance, as provided by the Chemical 
                                      Entities of Biological Interest (ChEBI) 
                                      dictionary.
    
    Parameter Description           - A description of the water quality 
                                      parameter. 
                                      (!!! Be advised: Some  special characters
                                      - e.g. '�' - have been corrupted during 
                                      encoding !!!)

-------------------------------------------------------------------------------

The methods metadata table has the following entries:

    Parameter Code                  - Code of water quality parameter and 
                                      fraction that has been sampled.
    
    Analysis Method Code            - Code of analysis method used for 
                                      determination of given water quality 
                                      parameter.
    
    Unit                            - Reporting unit of the water quality 
                                      parameter, that has been analyzed by the 
                                      given method.
    
    Parameter Long Name             - Complete Name of water quality parameter 
                                      and fraction.
        
                                      
    Method Name                     - Full name of analysis method, used for
                                      determination of given water quality 
                                      parameter.
    
    Method Type                     - Type of analysis method.

    Method Number                   - Number of analysis method in method 
                                      source reference.

    Method Source                   - Reference to national or international 
                                      source of analysis method.

    
    Method Description              - A description of the analysis method, as
                                      provided by the data source. 
                                      (!!! Be advised: Some  special characters
                                      - e.g. '�' - have been corrupted during 
                                      encoding !!!)
                                      
-------------------------------------------------------------------------------

Each of the water quality sample data tables have the following entries:

    GEMS Station Number             - GEMStat internal station number.
    
    Sample Date                     - Day on which the sample has been taken.
                                      Format: YYYY-MM-DD

    Sample Time                     - Time on which sample has been taken.
                                      Format: HH:mm (24-hour clock) 
                                      
    Depth                           - Depth (in meters) below water surface,  
                                      from which sample has been taken.

    Parameter Code                  - Code of water quality parameter that has 
                                      been sampled (see parameter metadata 
                                      table).

    Analysis Method Code            - Code of analysis method used for 
                                      determination of given water quality 
                                      parameter (see parameter metadata table).
                                      
    Value Flags                     - Quality flags for analysis result.
                                      Possible entries: 
                                        <       - below method detection limit
                                        >       - above quantification limit
                                        ~       - estimated value

    Value                           - Analysis result of given sample.

    Unit                            - Unit of analysis result.

    Method Detection Limit          - The MDL is the smallest amount of a 
                                      substance detectable by given analysis 
                                      method with 99% confidence.
                                      
    Data Quality                    - Rating of the Analysis result regarding
                                      its plausibility:
                                        Fair        |
                                        Good        | plausible values 
                                        Excellent   |
                                        Suspect     - value above plausible
                                                      technical limits for the
                                                      given water quality
                                                      parameter
                                        Poor        - should be excluded

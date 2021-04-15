# CensusAPI
Steps:
Download Tract Shapefiles for California (Code: 06) 

Browse through the variable list and rename it (ex: 'P001001' renamed to 'pop') for every Tract in
   California (06), add it to the 2010 Tract-level TIGER shapefile for CA,
   and output it to 'pop_shp/tract2010.shp'.

python3 census.py \
    --db census \
    --vars P001001:pop \
    --geo state:06,'tract' \
    --tiger tl_2020_06_tract10.shp \
    --out pop_shp/tract2010.shp

Resources:
    
    Shapefiles: https://www.census.gov/cgi-bin/geo/shapefiles/index.php?year=2020&layergroup=Census+Tracts
    
    Decennial Census
    - API guide: https://www.census.gov/content/dam/Census/data/developers/api-user-guide/api-guide.pdf
    - API examples, variables, and geo hierarchies: https://api.census.gov/data/2010/dec/sf1.html
    
    5-year ACS (Data Profile tables):
    - API examples, variables, and geo hierarchies: https://api.census.gov/data/2019/acs/acs5/profile.html

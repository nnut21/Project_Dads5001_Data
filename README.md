<h1>[DADS5001] Mini Project - Living death</h1>

<a id="readme-top"></a>
<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#overview">Overview</a>
      <ul>
        <li><a href="#dataset">Dataset</a></li>
        <li><a href="#main-question">Main Question</a></li>
      </ul>
    </li>
    <li>
      <a href="#import-data">Import Data</a>
      <ul>
        <li><a href="#cause-of-death">Cause of Death</a></li>
        <li><a href="#continent">Continent</a></li>
        <li><a href="#world-population">World Population</a></li>
      </ul>
    </li>
    <li>
      <a href="#cleansing">Cleansing</a>
      <ul>
        <li><a href="#cleansing-world-population">Cleansing World Population</a></li>
        <li><a href="#cleansing-continent">Cleansing Continent</a></li>
        <li><a href="#cleansing-cause-of-death">Cleansing Cause of Death</a></li>
        <li><a href="#create-main-table">Create Main Table</a></li>
      </ul>
    </li>
    <li><a href="Markdown/Death_Cause_Analysis.md" target="_blank">Death Cause Analysis</a></li>
    <li>
      <a href="#event-analysis" target="_blank">Event Analysis</a>
      <ul>
        <li>
          <a href="#detail-of-event-during-1990---2019">Detail of Event during 1990 - 2019</a>
        </li>
        <li>
          <a href="#event-for-analyze">Event for analyze</a>
          <ul>
        <li><a href="#hiv">HIV</a></li>
        <li><a href="#rwanda-genocide">Rwanda Genocide</a></li>
        <li><a href="#asian-tsunami">Asian Tsunami</a></li>
        <li><a href="#malaria">Malaria</a></li>
        <li><a href="#diarrheal">Diarrheal</a></li>
      </ul>
        </li>
      </ul>
    </li>
    <li><a href="#summary">Summary</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->

## Data Source
Sourced from Kaggle and contains age-related data.
Age-related data.

- Title: World Wide Death Factors
- Author: ADRIAN DIAZ
- Link: [Kaggle - World Wide Death Factors](https://www.kaggle.com/datasets/adriandiazny/world-wide-death-factors)

##
Country to Continent.

- Title: Country to Continent
- Author: statchaitya
- Link: [Kaggle - Country to Continent](https://www.kaggle.com/datasets/statchaitya/country-to-continent)

##
Population data for different regions.

- Title: Population Dataset
- Author: KaggleAshwin
- Link: [Kaggle - Population Dataset](https://www.kaggle.com/datasets/kaggleashwin/population-dataset)

##
Taiwan Population data for fill missing value.

- Title: Taiwan Population data
- Author: Macrotrends
- Link: [Macrotrends - Population Dataset](https://www.macrotrends.net/global-metrics/countries/TWN/taiwan/population)

##

### Main Question
1. สาเหตุการเสียชีวิตที่พบมากที่สุดทั่วโลกตั้งแต่ปี 1990 ถึง 2019 คืออะไร
2. ปัจจัยเสี่ยงใดที่มีผลต่อการเสียชีวิตมากที่สุดในแต่ละทวีป
3. แนวโน้มของอัตราการเปลี่ยนแปลงในการเสียชีวิตจาก 4 ปัจจัยเสี่ยง มีการเพิ่มขึ้นหรือลดลงอย่างไร
4. อัตราการเสียชีวิตจากโรคเรื้อรังในภูมิภาคเอเชียตะวันออกเฉียงใต้มีแนวโน้มเป็นอย่างไร
5. แนวโน้มของอัตราการเปลี่ยนแปลงในการเสียชีวิตของประชากรประเทศไทยเทียบกับ เมียนมาร์ ฟิลิปปินส์ และเวียดนาม ในช่วงปี 1990 ถึง 2019 เป็นอย่างไร
6. เหตุการณ์สำคัญที่เกิดขึ้นในแต่ละช่วงเวลา มีความสอดคล้องและดำเนินไปในทิศทางเดียวกันกับข้อมูลจำนวนผู้เสียชีวิตหรือไม่

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- Import Data -->
## Import Data

### Cause of Death

<b>Dataset:</b> <a href="https://github.com/imyajaii/dads5001-mini-project-01/blob/develop/dataset/cause_of_deaths.csv" target="_blank">Cause of Death</a>

<b>DataFrame Info</b>

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 6120 entries, 0 to 6119
    Data columns (total 34 columns):
     #   Column                                      Non-Null Count  Dtype 
    ---  ------                                      --------------  ----- 
     0   Country/Territory                           6120 non-null   object
     1   Code                                        6120 non-null   object
     2   Year                                        6120 non-null   int64 
     3   Meningitis                                  6120 non-null   int64 
     4   Alzheimer's Disease and Other Dementias     6120 non-null   int64 
     5   Parkinson's Disease                         6120 non-null   int64 
     6   Nutritional Deficiencies                    6120 non-null   int64 
     7   Malaria                                     6120 non-null   int64 
     8   Drowning                                    6120 non-null   int64 
     9   Interpersonal Violence                      6120 non-null   int64 
     10  Maternal Disorders                          6120 non-null   int64 
     11  HIV/AIDS                                    6120 non-null   int64 
     12  Drug Use Disorders                          6120 non-null   int64 
     13  Tuberculosis                                6120 non-null   int64 
     14  Cardiovascular Diseases                     6120 non-null   int64 
     15  Lower Respiratory Infections                6120 non-null   int64 
     16  Neonatal Disorders                          6120 non-null   int64 
     17  Alcohol Use Disorders                       6120 non-null   int64 
     18  Self-harm                                   6120 non-null   int64 
     19  Exposure to Forces of Nature                6120 non-null   int64 
     20  Diarrheal Diseases                          6120 non-null   int64 
     21  Environmental Heat and Cold Exposure        6120 non-null   int64 
     22  Neoplasms                                   6120 non-null   int64 
     23  Conflict and Terrorism                      6120 non-null   int64 
     24  Diabetes Mellitus                           6120 non-null   int64 
     25  Chronic Kidney Disease                      6120 non-null   int64 
     26  Poisonings                                  6120 non-null   int64 
     27  Protein-Energy Malnutrition                 6120 non-null   int64 
     28  Road Injuries                               6120 non-null   int64 
     29  Chronic Respiratory Diseases                6120 non-null   int64 
     30  Cirrhosis and Other Chronic Liver Diseases  6120 non-null   int64 
     31  Digestive Diseases                          6120 non-null   int64 
     32  Fire, Heat, and Hot Substances              6120 non-null   int64 
     33  Acute Hepatitis                             6120 non-null   int64 
    dtypes: int64(32), object(2)
    memory usage: 1.6+ MB

<b>Example data cause of death</b>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country/Territory</th>
      <th>Code</th>
      <th>Year</th>
      <th>Meningitis</th>
      <th>Alzheimer's Disease and Other Dementias</th>
      <th>Parkinson's Disease</th>
      <th>Nutritional Deficiencies</th>
      <th>Malaria</th>
      <th>Drowning</th>
      <th>Interpersonal Violence</th>
      <th>...</th>
      <th>Diabetes Mellitus</th>
      <th>Chronic Kidney Disease</th>
      <th>Poisonings</th>
      <th>Protein-Energy Malnutrition</th>
      <th>Road Injuries</th>
      <th>Chronic Respiratory Diseases</th>
      <th>Cirrhosis and Other Chronic Liver Diseases</th>
      <th>Digestive Diseases</th>
      <th>Fire, Heat, and Hot Substances</th>
      <th>Acute Hepatitis</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>1990</td>
      <td>2159</td>
      <td>1116</td>
      <td>371</td>
      <td>2087</td>
      <td>93</td>
      <td>1370</td>
      <td>1538</td>
      <td>...</td>
      <td>2108</td>
      <td>3709</td>
      <td>338</td>
      <td>2054</td>
      <td>4154</td>
      <td>5945</td>
      <td>2673</td>
      <td>5005</td>
      <td>323</td>
      <td>2985</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>1991</td>
      <td>2218</td>
      <td>1136</td>
      <td>374</td>
      <td>2153</td>
      <td>189</td>
      <td>1391</td>
      <td>2001</td>
      <td>...</td>
      <td>2120</td>
      <td>3724</td>
      <td>351</td>
      <td>2119</td>
      <td>4472</td>
      <td>6050</td>
      <td>2728</td>
      <td>5120</td>
      <td>332</td>
      <td>3092</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>1992</td>
      <td>2475</td>
      <td>1162</td>
      <td>378</td>
      <td>2441</td>
      <td>239</td>
      <td>1514</td>
      <td>2299</td>
      <td>...</td>
      <td>2153</td>
      <td>3776</td>
      <td>386</td>
      <td>2404</td>
      <td>5106</td>
      <td>6223</td>
      <td>2830</td>
      <td>5335</td>
      <td>360</td>
      <td>3325</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>1993</td>
      <td>2812</td>
      <td>1187</td>
      <td>384</td>
      <td>2837</td>
      <td>108</td>
      <td>1687</td>
      <td>2589</td>
      <td>...</td>
      <td>2195</td>
      <td>3862</td>
      <td>425</td>
      <td>2797</td>
      <td>5681</td>
      <td>6445</td>
      <td>2943</td>
      <td>5568</td>
      <td>396</td>
      <td>3601</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>1994</td>
      <td>3027</td>
      <td>1211</td>
      <td>391</td>
      <td>3081</td>
      <td>211</td>
      <td>1809</td>
      <td>2849</td>
      <td>...</td>
      <td>2231</td>
      <td>3932</td>
      <td>451</td>
      <td>3038</td>
      <td>6001</td>
      <td>6664</td>
      <td>3027</td>
      <td>5739</td>
      <td>420</td>
      <td>3816</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 34 columns</p>

<b>Unique Country Code</b>

    array(['AFG', 'ALB', 'DZA', 'ASM', 'AND', 'AGO', 'ATG', 'ARG', 'ARM',
           'AUS', 'AUT', 'AZE', 'BHS', 'BHR', 'BGD', 'BRB', 'BLR', 'BEL',
           'BLZ', 'BEN', 'BMU', 'BTN', 'BOL', 'BIH', 'BWA', 'BRA', 'BRN',
           'BGR', 'BFA', 'BDI', 'KHM', 'CMR', 'CAN', 'CPV', 'CAF', 'TCD',
           'CHL', 'CHN', 'COL', 'COM', 'COG', 'COK', 'CRI', 'CIV', 'HRV',
           'CUB', 'CYP', 'CZE', 'COD', 'DNK', 'DJI', 'DMA', 'DOM', 'ECU',
           'EGY', 'SLV', 'GNQ', 'ERI', 'EST', 'SWZ', 'ETH', 'FJI', 'FIN',
           'FRA', 'GAB', 'GMB', 'GEO', 'DEU', 'GHA', 'GRC', 'GRL', 'GRD',
           'GUM', 'GTM', 'GIN', 'GNB', 'GUY', 'HTI', 'HND', 'HUN', 'ISL',
           'IND', 'IDN', 'IRN', 'IRQ', 'IRL', 'ISR', 'ITA', 'JAM', 'JPN',
           'JOR', 'KAZ', 'KEN', 'KIR', 'KWT', 'KGZ', 'LAO', 'LVA', 'LBN',
           'LSO', 'LBR', 'LBY', 'LTU', 'LUX', 'MDG', 'MWI', 'MYS', 'MDV',
           'MLI', 'MLT', 'MHL', 'MRT', 'MUS', 'MEX', 'FSM', 'MDA', 'MCO',
           'MNG', 'MNE', 'MAR', 'MOZ', 'MMR', 'NAM', 'NRU', 'NPL', 'NLD',
           'NZL', 'NIC', 'NER', 'NGA', 'NIU', 'PRK', 'MKD', 'MNP', 'NOR',
           'OMN', 'PAK', 'PLW', 'PSE', 'PAN', 'PNG', 'PRY', 'PER', 'PHL',
           'POL', 'PRT', 'PRI', 'QAT', 'ROU', 'RUS', 'RWA', 'KNA', 'LCA',
           'VCT', 'WSM', 'SMR', 'STP', 'SAU', 'SEN', 'SRB', 'SYC', 'SLE',
           'SGP', 'SVK', 'SVN', 'SLB', 'SOM', 'ZAF', 'KOR', 'SSD', 'ESP',
           'LKA', 'SDN', 'SUR', 'SWE', 'CHE', 'SYR', 'TWN', 'TJK', 'TZA',
           'THA', 'TLS', 'TGO', 'TKL', 'TON', 'TTO', 'TUN', 'TUR', 'TKM',
           'TUV', 'UGA', 'UKR', 'ARE', 'GBR', 'USA', 'VIR', 'URY', 'UZB',
           'VUT', 'VEN', 'VNM', 'YEM', 'ZMB', 'ZWE'], dtype=object)

  <b>Total Unique:</b> 204 contries

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Continent

<b>Dataset:</b> <a href="https://github.com/imyajaii/dads5001-mini-project-01/blob/develop/dataset/countryContinent.csv" target="_blank">Continent</a>

<b>DataFrame Info</b>


    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 249 entries, 0 to 248
    Data columns (total 9 columns):
     #   Column           Non-Null Count  Dtype  
    ---  ------           --------------  -----  
     0   country          249 non-null    object 
     1   code_2           248 non-null    object 
     2   code_3           249 non-null    object 
     3   country_code     249 non-null    int64  
     4   iso_3166_2       249 non-null    object 
     5   continent        240 non-null    object 
     6   sub_region       240 non-null    object 
     7   region_code      240 non-null    float64
     8   sub_region_code  240 non-null    float64
    dtypes: float64(2), int64(1), object(6)
    memory usage: 17.6+ KB

<b>Example data continent</b>
![png](Markdown/Import_Data_files/example_data_continent.png)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### World Population

<b>Dataset:</b> <a href="https://github.com/imyajaii/dads5001-mini-project-01/blob/develop/dataset/World-population-by-countries-dataset.csv" target="_blank">World Population</a>

<b>DataFrame Info</b>

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 266 entries, 0 to 265
    Data columns (total 64 columns):
     #   Column        Non-Null Count  Dtype  
    ---  ------        --------------  -----  
     0   Country Name  266 non-null    object 
     1   Country Code  266 non-null    object 
     2   1960          264 non-null    float64
     3   1961          264 non-null    float64
     4   1962          264 non-null    float64
     5   1963          264 non-null    float64
     6   1964          264 non-null    float64
     7   1965          264 non-null    float64
     8   1966          264 non-null    float64
     9   1967          264 non-null    float64
     10  1968          264 non-null    float64
     11  1969          264 non-null    float64
     12  1970          264 non-null    float64
     13  1971          264 non-null    float64
     14  1972          264 non-null    float64
     15  1973          264 non-null    float64
     16  1974          264 non-null    float64
     17  1975          264 non-null    float64
     18  1976          264 non-null    float64
     19  1977          264 non-null    float64
     20  1978          264 non-null    float64
     21  1979          264 non-null    float64
     22  1980          264 non-null    float64
     23  1981          264 non-null    float64
     24  1982          264 non-null    float64
     25  1983          264 non-null    float64
     26  1984          264 non-null    float64
     27  1985          264 non-null    float64
     28  1986          264 non-null    float64
     29  1987          264 non-null    float64
     30  1988          264 non-null    float64
     31  1989          264 non-null    float64
     32  1990          265 non-null    float64
     33  1991          265 non-null    float64
     34  1992          264 non-null    float64
     35  1993          264 non-null    float64
     36  1994          264 non-null    float64
     37  1995          265 non-null    float64
     38  1996          265 non-null    float64
     39  1997          265 non-null    float64
     40  1998          265 non-null    float64
     41  1999          265 non-null    float64
     42  2000          265 non-null    float64
     43  2001          265 non-null    float64
     44  2002          265 non-null    float64
     45  2003          265 non-null    float64
     46  2004          265 non-null    float64
     47  2005          265 non-null    float64
     48  2006          265 non-null    float64
     49  2007          265 non-null    float64
     50  2008          265 non-null    float64
     51  2009          265 non-null    float64
     52  2010          265 non-null    float64
     53  2011          265 non-null    float64
     54  2012          264 non-null    float64
     55  2013          264 non-null    float64
     56  2014          264 non-null    float64
     57  2015          264 non-null    float64
     58  2016          264 non-null    float64
     59  2017          264 non-null    float64
     60  2018          264 non-null    float64
     61  2019          264 non-null    float64
     62  2020          264 non-null    float64
     63  2021          264 non-null    float64
    dtypes: float64(62), object(2)
    memory usage: 133.1+ KB

<b>Example data world population</b>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country Name</th>
      <th>Country Code</th>
      <th>1960</th>
      <th>1961</th>
      <th>1962</th>
      <th>1963</th>
      <th>1964</th>
      <th>1965</th>
      <th>1966</th>
      <th>1967</th>
      <th>...</th>
      <th>2012</th>
      <th>2013</th>
      <th>2014</th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
      <th>2021</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Aruba</td>
      <td>ABW</td>
      <td>54208.0</td>
      <td>55434.0</td>
      <td>56234.0</td>
      <td>56699.0</td>
      <td>57029.0</td>
      <td>57357.0</td>
      <td>57702.0</td>
      <td>58044.0</td>
      <td>...</td>
      <td>102565.0</td>
      <td>103165.0</td>
      <td>103776.0</td>
      <td>104339.0</td>
      <td>104865.0</td>
      <td>105361.0</td>
      <td>105846.0</td>
      <td>106310.0</td>
      <td>106766.0</td>
      <td>107195.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Africa Eastern and Southern</td>
      <td>AFE</td>
      <td>130836765.0</td>
      <td>134159786.0</td>
      <td>137614644.0</td>
      <td>141202036.0</td>
      <td>144920186.0</td>
      <td>148769974.0</td>
      <td>152752671.0</td>
      <td>156876454.0</td>
      <td>...</td>
      <td>547482863.0</td>
      <td>562601578.0</td>
      <td>578075373.0</td>
      <td>593871847.0</td>
      <td>609978946.0</td>
      <td>626392880.0</td>
      <td>643090131.0</td>
      <td>660046272.0</td>
      <td>677243299.0</td>
      <td>694665117.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>8996967.0</td>
      <td>9169406.0</td>
      <td>9351442.0</td>
      <td>9543200.0</td>
      <td>9744772.0</td>
      <td>9956318.0</td>
      <td>10174840.0</td>
      <td>10399936.0</td>
      <td>...</td>
      <td>31161378.0</td>
      <td>32269592.0</td>
      <td>33370804.0</td>
      <td>34413603.0</td>
      <td>35383028.0</td>
      <td>36296111.0</td>
      <td>37171922.0</td>
      <td>38041757.0</td>
      <td>38928341.0</td>
      <td>39835428.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Africa Western and Central</td>
      <td>AFW</td>
      <td>96396419.0</td>
      <td>98407221.0</td>
      <td>100506960.0</td>
      <td>102691339.0</td>
      <td>104953470.0</td>
      <td>107289875.0</td>
      <td>109701811.0</td>
      <td>112195950.0</td>
      <td>...</td>
      <td>370243017.0</td>
      <td>380437896.0</td>
      <td>390882979.0</td>
      <td>401586651.0</td>
      <td>412551299.0</td>
      <td>423769930.0</td>
      <td>435229381.0</td>
      <td>446911598.0</td>
      <td>458803476.0</td>
      <td>470898870.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Angola</td>
      <td>AGO</td>
      <td>5454938.0</td>
      <td>5531451.0</td>
      <td>5608499.0</td>
      <td>5679409.0</td>
      <td>5734995.0</td>
      <td>5770573.0</td>
      <td>5781305.0</td>
      <td>5774440.0</td>
      <td>...</td>
      <td>25107925.0</td>
      <td>26015786.0</td>
      <td>26941773.0</td>
      <td>27884380.0</td>
      <td>28842482.0</td>
      <td>29816769.0</td>
      <td>30809787.0</td>
      <td>31825299.0</td>
      <td>32866268.0</td>
      <td>33933611.0</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 64 columns</p>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- Cleansing -->
## Cleansing

### Cleansing World Population
Drop column 1960 - 1989 , 2020 , 2021 of World Population

```python
# prompt: drop column 1960 - 1989 , 2020 , 2021 of df_population
columns_to_drop = [str(year) for year in range(1960, 1990)] + ['2020', '2021']
df_population = df_population.drop(columns=columns_to_drop)

df_population.head()

```

Example data world population after drop columns
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country Name</th>
      <th>Country Code</th>
      <th>1990</th>
      <th>1991</th>
      <th>1992</th>
      <th>1993</th>
      <th>1994</th>
      <th>1995</th>
      <th>1996</th>
      <th>1997</th>
      <th>...</th>
      <th>2010</th>
      <th>2011</th>
      <th>2012</th>
      <th>2013</th>
      <th>2014</th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Aruba</td>
      <td>ABW</td>
      <td>62152.0</td>
      <td>64623.0</td>
      <td>68240.0</td>
      <td>72495.0</td>
      <td>76705.0</td>
      <td>80324.0</td>
      <td>83211.0</td>
      <td>85450.0</td>
      <td>...</td>
      <td>101665.0</td>
      <td>102050.0</td>
      <td>102565.0</td>
      <td>103165.0</td>
      <td>103776.0</td>
      <td>104339.0</td>
      <td>104865.0</td>
      <td>105361.0</td>
      <td>105846.0</td>
      <td>106310.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Africa Eastern and Southern</td>
      <td>AFE</td>
      <td>304648010.0</td>
      <td>313394693.0</td>
      <td>322270073.0</td>
      <td>331265579.0</td>
      <td>340379934.0</td>
      <td>349605660.0</td>
      <td>358953595.0</td>
      <td>368440591.0</td>
      <td>...</td>
      <td>518468229.0</td>
      <td>532760424.0</td>
      <td>547482863.0</td>
      <td>562601578.0</td>
      <td>578075373.0</td>
      <td>593871847.0</td>
      <td>609978946.0</td>
      <td>626392880.0</td>
      <td>643090131.0</td>
      <td>660046272.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>12412311.0</td>
      <td>13299016.0</td>
      <td>14485543.0</td>
      <td>15816601.0</td>
      <td>17075728.0</td>
      <td>18110662.0</td>
      <td>18853444.0</td>
      <td>19357126.0</td>
      <td>...</td>
      <td>29185511.0</td>
      <td>30117411.0</td>
      <td>31161378.0</td>
      <td>32269592.0</td>
      <td>33370804.0</td>
      <td>34413603.0</td>
      <td>35383028.0</td>
      <td>36296111.0</td>
      <td>37171922.0</td>
      <td>38041757.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Africa Western and Central</td>
      <td>AFW</td>
      <td>204803865.0</td>
      <td>210332267.0</td>
      <td>215976366.0</td>
      <td>221754806.0</td>
      <td>227692136.0</td>
      <td>233807627.0</td>
      <td>240114179.0</td>
      <td>246613750.0</td>
      <td>...</td>
      <td>350556886.0</td>
      <td>360285439.0</td>
      <td>370243017.0</td>
      <td>380437896.0</td>
      <td>390882979.0</td>
      <td>401586651.0</td>
      <td>412551299.0</td>
      <td>423769930.0</td>
      <td>435229381.0</td>
      <td>446911598.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Angola</td>
      <td>AGO</td>
      <td>11848385.0</td>
      <td>12248901.0</td>
      <td>12657361.0</td>
      <td>13075044.0</td>
      <td>13503753.0</td>
      <td>13945205.0</td>
      <td>14400722.0</td>
      <td>14871572.0</td>
      <td>...</td>
      <td>23356247.0</td>
      <td>24220660.0</td>
      <td>25107925.0</td>
      <td>26015786.0</td>
      <td>26941773.0</td>
      <td>27884380.0</td>
      <td>28842482.0</td>
      <td>29816769.0</td>
      <td>30809787.0</td>
      <td>31825299.0</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 32 columns</p>

Convert  World Population of column 1990 - 2019 to be row of each of Column Country Code (the new name of column is Population) keep column Country Name

```python
df_population_melted = df_population.melt(id_vars=['Country Name', 'Country Code'],
                                         var_name='Year',
                                         value_name='Population')

```

DataFrame Info

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 7980 entries, 0 to 7979
    Data columns (total 4 columns):
     #   Column        Non-Null Count  Dtype  
    ---  ------        --------------  -----  
     0   Country Name  7980 non-null   object 
     1   Country Code  7980 non-null   object 
     2   Year          7980 non-null   object 
     3   Population    7939 non-null   float64
    dtypes: float64(1), object(3)
    memory usage: 249.5+ KB

Example data after convert year columns to rows<br />
![png](Markdown/Import_Data_files/df_population_melted_sort.png)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Cleansing Continent
Drop column contry, code_2, contry_code, iso_3166_2, region_code, sub_region_code

```python
df_continent = df_continent.drop(['country', 'code_2', 'country_code', 'iso_3166_2', 'region_code', 'sub_region_code'], axis=1)

```

DataFrame Info

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 249 entries, 0 to 248
    Data columns (total 3 columns):
     #   Column      Non-Null Count  Dtype 
    ---  ------      --------------  ----- 
     0   code_3      249 non-null    object
     1   continent   240 non-null    object
     2   sub_region  240 non-null    object
    dtypes: object(3)
    memory usage: 6.0+ KB

Example data after drop columns

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>code_3</th>
      <th>continent</th>
      <th>sub_region</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
    </tr>
    <tr>
      <th>1</th>
      <td>ALA</td>
      <td>Europe</td>
      <td>Northern Europe</td>
    </tr>
    <tr>
      <th>2</th>
      <td>ALB</td>
      <td>Europe</td>
      <td>Southern Europe</td>
    </tr>
    <tr>
      <th>3</th>
      <td>DZA</td>
      <td>Africa</td>
      <td>Northern Africa</td>
    </tr>
    <tr>
      <th>4</th>
      <td>ASM</td>
      <td>Oceania</td>
      <td>Polynesia</td>
    </tr>
  </tbody>
</table>
</div>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Cleansing Cause of Death

#### Merge data by country code 3 digits

```python
# prompt: check if the column Code of df_cause_of_death was all in column code_3 of df_cintinent

# Convert both columns to sets for efficient comparison
cause_of_death_codes = set(df_cause_of_death['Code'].unique())
continent_codes = set(df_continent['code_3'].unique())

# Check if all codes in df_cause_of_death are present in df_continent
all_codes_present = cause_of_death_codes.issubset(continent_codes)

print(f"Are all 'Code' values from df_cause_of_death present in 'code_3' of df_continent? {all_codes_present}")

```

    Are all 'Code' values from df_cause_of_death present in 'code_3' of df_continent? True
    

```python
df_join1 = pd.merge( df_cause_of_death, df_continent, left_on='Code', right_on='code_3', how='left' )
```
First five records
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country/Territory</th>
      <th>Code</th>
      <th>Year</th>
      <th>Meningitis</th>
      <th>Alzheimer's Disease and Other Dementias</th>
      <th>Parkinson's Disease</th>
      <th>Nutritional Deficiencies</th>
      <th>Malaria</th>
      <th>Drowning</th>
      <th>Interpersonal Violence</th>
      <th>...</th>
      <th>Protein-Energy Malnutrition</th>
      <th>Road Injuries</th>
      <th>Chronic Respiratory Diseases</th>
      <th>Cirrhosis and Other Chronic Liver Diseases</th>
      <th>Digestive Diseases</th>
      <th>Fire, Heat, and Hot Substances</th>
      <th>Acute Hepatitis</th>
      <th>code_3</th>
      <th>continent</th>
      <th>sub_region</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>1990</td>
      <td>2159</td>
      <td>1116</td>
      <td>371</td>
      <td>2087</td>
      <td>93</td>
      <td>1370</td>
      <td>1538</td>
      <td>...</td>
      <td>2054</td>
      <td>4154</td>
      <td>5945</td>
      <td>2673</td>
      <td>5005</td>
      <td>323</td>
      <td>2985</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>1991</td>
      <td>2218</td>
      <td>1136</td>
      <td>374</td>
      <td>2153</td>
      <td>189</td>
      <td>1391</td>
      <td>2001</td>
      <td>...</td>
      <td>2119</td>
      <td>4472</td>
      <td>6050</td>
      <td>2728</td>
      <td>5120</td>
      <td>332</td>
      <td>3092</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>1992</td>
      <td>2475</td>
      <td>1162</td>
      <td>378</td>
      <td>2441</td>
      <td>239</td>
      <td>1514</td>
      <td>2299</td>
      <td>...</td>
      <td>2404</td>
      <td>5106</td>
      <td>6223</td>
      <td>2830</td>
      <td>5335</td>
      <td>360</td>
      <td>3325</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>1993</td>
      <td>2812</td>
      <td>1187</td>
      <td>384</td>
      <td>2837</td>
      <td>108</td>
      <td>1687</td>
      <td>2589</td>
      <td>...</td>
      <td>2797</td>
      <td>5681</td>
      <td>6445</td>
      <td>2943</td>
      <td>5568</td>
      <td>396</td>
      <td>3601</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>1994</td>
      <td>3027</td>
      <td>1211</td>
      <td>391</td>
      <td>3081</td>
      <td>211</td>
      <td>1809</td>
      <td>2849</td>
      <td>...</td>
      <td>3038</td>
      <td>6001</td>
      <td>6664</td>
      <td>3027</td>
      <td>5739</td>
      <td>420</td>
      <td>3816</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 37 columns</p>

<b>DataFrame Info</b>

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 6120 entries, 0 to 6119
    Data columns (total 37 columns):
     #   Column                                      Non-Null Count  Dtype 
    ---  ------                                      --------------  ----- 
     0   Country/Territory                           6120 non-null   object
     1   Code                                        6120 non-null   object
     2   Year                                        6120 non-null   int64 
     3   Meningitis                                  6120 non-null   int64 
     4   Alzheimer's Disease and Other Dementias     6120 non-null   int64 
     5   Parkinson's Disease                         6120 non-null   int64 
     6   Nutritional Deficiencies                    6120 non-null   int64 
     7   Malaria                                     6120 non-null   int64 
     8   Drowning                                    6120 non-null   int64 
     9   Interpersonal Violence                      6120 non-null   int64 
     10  Maternal Disorders                          6120 non-null   int64 
     11  HIV/AIDS                                    6120 non-null   int64 
     12  Drug Use Disorders                          6120 non-null   int64 
     13  Tuberculosis                                6120 non-null   int64 
     14  Cardiovascular Diseases                     6120 non-null   int64 
     15  Lower Respiratory Infections                6120 non-null   int64 
     16  Neonatal Disorders                          6120 non-null   int64 
     17  Alcohol Use Disorders                       6120 non-null   int64 
     18  Self-harm                                   6120 non-null   int64 
     19  Exposure to Forces of Nature                6120 non-null   int64 
     20  Diarrheal Diseases                          6120 non-null   int64 
     21  Environmental Heat and Cold Exposure        6120 non-null   int64 
     22  Neoplasms                                   6120 non-null   int64 
     23  Conflict and Terrorism                      6120 non-null   int64 
     24  Diabetes Mellitus                           6120 non-null   int64 
     25  Chronic Kidney Disease                      6120 non-null   int64 
     26  Poisonings                                  6120 non-null   int64 
     27  Protein-Energy Malnutrition                 6120 non-null   int64 
     28  Road Injuries                               6120 non-null   int64 
     29  Chronic Respiratory Diseases                6120 non-null   int64 
     30  Cirrhosis and Other Chronic Liver Diseases  6120 non-null   int64 
     31  Digestive Diseases                          6120 non-null   int64 
     32  Fire, Heat, and Hot Substances              6120 non-null   int64 
     33  Acute Hepatitis                             6120 non-null   int64 
     34  code_3                                      6120 non-null   object
     35  continent                                   6120 non-null   object
     36  sub_region                                  6120 non-null   object
    dtypes: int64(32), object(5)
    memory usage: 1.7+ MB

<b>Drop duplicate column and select first five records</b>

```python
df_join1 = df_join1.drop(['code_3'], axis=1) # Drop duplicate column
df_join1.head()
```

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country/Territory</th>
      <th>Code</th>
      <th>Year</th>
      <th>Meningitis</th>
      <th>Alzheimer's Disease and Other Dementias</th>
      <th>Parkinson's Disease</th>
      <th>Nutritional Deficiencies</th>
      <th>Malaria</th>
      <th>Drowning</th>
      <th>Interpersonal Violence</th>
      <th>...</th>
      <th>Poisonings</th>
      <th>Protein-Energy Malnutrition</th>
      <th>Road Injuries</th>
      <th>Chronic Respiratory Diseases</th>
      <th>Cirrhosis and Other Chronic Liver Diseases</th>
      <th>Digestive Diseases</th>
      <th>Fire, Heat, and Hot Substances</th>
      <th>Acute Hepatitis</th>
      <th>continent</th>
      <th>sub_region</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>1990</td>
      <td>2159</td>
      <td>1116</td>
      <td>371</td>
      <td>2087</td>
      <td>93</td>
      <td>1370</td>
      <td>1538</td>
      <td>...</td>
      <td>338</td>
      <td>2054</td>
      <td>4154</td>
      <td>5945</td>
      <td>2673</td>
      <td>5005</td>
      <td>323</td>
      <td>2985</td>
      <td>Asia</td>
      <td>Southern Asia</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>1991</td>
      <td>2218</td>
      <td>1136</td>
      <td>374</td>
      <td>2153</td>
      <td>189</td>
      <td>1391</td>
      <td>2001</td>
      <td>...</td>
      <td>351</td>
      <td>2119</td>
      <td>4472</td>
      <td>6050</td>
      <td>2728</td>
      <td>5120</td>
      <td>332</td>
      <td>3092</td>
      <td>Asia</td>
      <td>Southern Asia</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>1992</td>
      <td>2475</td>
      <td>1162</td>
      <td>378</td>
      <td>2441</td>
      <td>239</td>
      <td>1514</td>
      <td>2299</td>
      <td>...</td>
      <td>386</td>
      <td>2404</td>
      <td>5106</td>
      <td>6223</td>
      <td>2830</td>
      <td>5335</td>
      <td>360</td>
      <td>3325</td>
      <td>Asia</td>
      <td>Southern Asia</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>1993</td>
      <td>2812</td>
      <td>1187</td>
      <td>384</td>
      <td>2837</td>
      <td>108</td>
      <td>1687</td>
      <td>2589</td>
      <td>...</td>
      <td>425</td>
      <td>2797</td>
      <td>5681</td>
      <td>6445</td>
      <td>2943</td>
      <td>5568</td>
      <td>396</td>
      <td>3601</td>
      <td>Asia</td>
      <td>Southern Asia</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>1994</td>
      <td>3027</td>
      <td>1211</td>
      <td>391</td>
      <td>3081</td>
      <td>211</td>
      <td>1809</td>
      <td>2849</td>
      <td>...</td>
      <td>451</td>
      <td>3038</td>
      <td>6001</td>
      <td>6664</td>
      <td>3027</td>
      <td>5739</td>
      <td>420</td>
      <td>3816</td>
      <td>Asia</td>
      <td>Southern Asia</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 36 columns</p>

```python
# prompt: move column continent and sub_region into next of column Code

cols = list(df_join1.columns)
continent_index = cols.index('continent')
sub_region_index = cols.index('sub_region')
code_index = cols.index('Code')

# Move 'continent' and 'sub_region' columns to the right of 'Code'
new_cols = cols[:code_index+1] + [cols[continent_index]] + [cols[sub_region_index]] + cols[code_index+1:continent_index] + cols[continent_index+1:sub_region_index] + cols[sub_region_index+1:]
df_join1 = df_join1[new_cols]

df_join1.head()

```
Select first five records

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country/Territory</th>
      <th>Code</th>
      <th>continent</th>
      <th>sub_region</th>
      <th>Year</th>
      <th>Meningitis</th>
      <th>Alzheimer's Disease and Other Dementias</th>
      <th>Parkinson's Disease</th>
      <th>Nutritional Deficiencies</th>
      <th>Malaria</th>
      <th>...</th>
      <th>Diabetes Mellitus</th>
      <th>Chronic Kidney Disease</th>
      <th>Poisonings</th>
      <th>Protein-Energy Malnutrition</th>
      <th>Road Injuries</th>
      <th>Chronic Respiratory Diseases</th>
      <th>Cirrhosis and Other Chronic Liver Diseases</th>
      <th>Digestive Diseases</th>
      <th>Fire, Heat, and Hot Substances</th>
      <th>Acute Hepatitis</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1990</td>
      <td>2159</td>
      <td>1116</td>
      <td>371</td>
      <td>2087</td>
      <td>93</td>
      <td>...</td>
      <td>2108</td>
      <td>3709</td>
      <td>338</td>
      <td>2054</td>
      <td>4154</td>
      <td>5945</td>
      <td>2673</td>
      <td>5005</td>
      <td>323</td>
      <td>2985</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1991</td>
      <td>2218</td>
      <td>1136</td>
      <td>374</td>
      <td>2153</td>
      <td>189</td>
      <td>...</td>
      <td>2120</td>
      <td>3724</td>
      <td>351</td>
      <td>2119</td>
      <td>4472</td>
      <td>6050</td>
      <td>2728</td>
      <td>5120</td>
      <td>332</td>
      <td>3092</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1992</td>
      <td>2475</td>
      <td>1162</td>
      <td>378</td>
      <td>2441</td>
      <td>239</td>
      <td>...</td>
      <td>2153</td>
      <td>3776</td>
      <td>386</td>
      <td>2404</td>
      <td>5106</td>
      <td>6223</td>
      <td>2830</td>
      <td>5335</td>
      <td>360</td>
      <td>3325</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1993</td>
      <td>2812</td>
      <td>1187</td>
      <td>384</td>
      <td>2837</td>
      <td>108</td>
      <td>...</td>
      <td>2195</td>
      <td>3862</td>
      <td>425</td>
      <td>2797</td>
      <td>5681</td>
      <td>6445</td>
      <td>2943</td>
      <td>5568</td>
      <td>396</td>
      <td>3601</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1994</td>
      <td>3027</td>
      <td>1211</td>
      <td>391</td>
      <td>3081</td>
      <td>211</td>
      <td>...</td>
      <td>2231</td>
      <td>3932</td>
      <td>451</td>
      <td>3038</td>
      <td>6001</td>
      <td>6664</td>
      <td>3027</td>
      <td>5739</td>
      <td>420</td>
      <td>3816</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 36 columns</p>

#### Check Invalid Country

```python
join1_codes = set(df_join1['Code'].unique())
population_codes = set(df_population_melted['Country Code'].unique())

codes_not_in_population = join1_codes - population_codes

print("Codes in df_join1['Code'] that are not in df_population['Country Code']:\n", codes_not_in_population)
```

    Codes in df_join1['Code'] that are not in df_population['Country Code']:
     {'NIU', 'TKL', 'TWN', 'COK'}

```python
join1 = set(df_join1['Code'].unique())
population = set(df_population_melted['Country Code'].unique())

# Check if all codes in df_cause_of_death are present in df_continent
all_codes_present = join1.issubset(population)

print(f"Are all 'Code' values from df_cause_of_death present in 'code_3' of df_continent? {all_codes_present}")
```

    Are all 'Code' values from df_cause_of_death present in 'code_3' of df_continent? False

##### Import Taiwan
<b>Dataset: </b> <a href="https://github.com/imyajaii/dads5001-mini-project-01/blob/develop/dataset/taiwan-population.csv" target="_blank">Taiwan Population</a>

DataFrame Info


    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 151 entries, 0 to 150
    Data columns (total 3 columns):
     #   Column            Non-Null Count  Dtype  
    ---  ------            --------------  -----  
     0   date              151 non-null    object 
     1    Population       151 non-null    int64  
     2    Annual % Change  150 non-null    float64
    dtypes: float64(1), int64(1), object(1)
    memory usage: 3.7+ KB

First five records

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>date</th>
      <th>Population</th>
      <th>Annual % Change</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>31/12/1950</td>
      <td>7623130</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>31/12/1951</td>
      <td>7934689</td>
      <td>4.09</td>
    </tr>
    <tr>
      <th>2</th>
      <td>31/12/1952</td>
      <td>8251039</td>
      <td>3.99</td>
    </tr>
    <tr>
      <th>3</th>
      <td>31/12/1953</td>
      <td>8572131</td>
      <td>3.89</td>
    </tr>
    <tr>
      <th>4</th>
      <td>31/12/1954</td>
      <td>8897776</td>
      <td>3.80</td>
    </tr>
  </tbody>
</table>

```python
# prompt: change date of column date into year
# Assuming 'df_taiwan' is your DataFrame and 'date' is the column containing dates
df_taiwan['Year'] = pd.to_datetime(df_taiwan['date']).dt.year
df_taiwan
```

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>date</th>
      <th>Population</th>
      <th>Annual % Change</th>
      <th>Year</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>31/12/1950</td>
      <td>7623130</td>
      <td>NaN</td>
      <td>1950</td>
    </tr>
    <tr>
      <th>1</th>
      <td>31/12/1951</td>
      <td>7934689</td>
      <td>4.09</td>
      <td>1951</td>
    </tr>
    <tr>
      <th>2</th>
      <td>31/12/1952</td>
      <td>8251039</td>
      <td>3.99</td>
      <td>1952</td>
    </tr>
    <tr>
      <th>3</th>
      <td>31/12/1953</td>
      <td>8572131</td>
      <td>3.89</td>
      <td>1953</td>
    </tr>
    <tr>
      <th>4</th>
      <td>31/12/1954</td>
      <td>8897776</td>
      <td>3.80</td>
      <td>1954</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>146</th>
      <td>31/12/2096</td>
      <td>15590180</td>
      <td>-0.62</td>
      <td>2096</td>
    </tr>
    <tr>
      <th>147</th>
      <td>31/12/2097</td>
      <td>15497260</td>
      <td>-0.60</td>
      <td>2097</td>
    </tr>
    <tr>
      <th>148</th>
      <td>31/12/2098</td>
      <td>15408434</td>
      <td>-0.57</td>
      <td>2098</td>
    </tr>
    <tr>
      <th>149</th>
      <td>31/12/2099</td>
      <td>15323545</td>
      <td>-0.55</td>
      <td>2099</td>
    </tr>
    <tr>
      <th>150</th>
      <td>31/12/2100</td>
      <td>15241961</td>
      <td>-0.53</td>
      <td>2100</td>
    </tr>
  </tbody>
</table>
<p>151 rows × 4 columns</p>

```python
# prompt: create column Country in first column all data was Taiwan , column Code in second column all data was TWN and move column Year into third column

# Create new columns 'Country' and 'Code'
df_taiwan['Country'] = 'Taiwan'
df_taiwan['Code'] = 'TWN'

# Get the list of column names
cols = list(df_taiwan.columns)

# Find the index of the 'Year' column
year_index = cols.index('Year')

# Remove 'Year' from its original position
cols.pop(year_index)

# Insert 'Year' at the third position (index 2)
cols.insert(2, 'Year')

# Reorder the DataFrame columns based on the new list
df_taiwan = df_taiwan[cols]

df_taiwan.head()

```
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>date</th>
      <th>Population</th>
      <th>Year</th>
      <th>Annual % Change</th>
      <th>Country</th>
      <th>Code</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>31/12/1950</td>
      <td>7623130</td>
      <td>1950</td>
      <td>NaN</td>
      <td>Taiwan</td>
      <td>TWN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>31/12/1951</td>
      <td>7934689</td>
      <td>1951</td>
      <td>4.09</td>
      <td>Taiwan</td>
      <td>TWN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>31/12/1952</td>
      <td>8251039</td>
      <td>1952</td>
      <td>3.99</td>
      <td>Taiwan</td>
      <td>TWN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>31/12/1953</td>
      <td>8572131</td>
      <td>1953</td>
      <td>3.89</td>
      <td>Taiwan</td>
      <td>TWN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>31/12/1954</td>
      <td>8897776</td>
      <td>1954</td>
      <td>3.80</td>
      <td>Taiwan</td>
      <td>TWN</td>
    </tr>
  </tbody>
</table>

```python
# prompt: drop column date , Annual % Change

df_taiwan = df_taiwan.drop(['date', ' Annual % Change'], axis=1)

```
Display first five records

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Population</th>
      <th>Year</th>
      <th>Country</th>
      <th>Code</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>7623130</td>
      <td>1950</td>
      <td>Taiwan</td>
      <td>TWN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>7934689</td>
      <td>1951</td>
      <td>Taiwan</td>
      <td>TWN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8251039</td>
      <td>1952</td>
      <td>Taiwan</td>
      <td>TWN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>8572131</td>
      <td>1953</td>
      <td>Taiwan</td>
      <td>TWN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>8897776</td>
      <td>1954</td>
      <td>Taiwan</td>
      <td>TWN</td>
    </tr>
  </tbody>
</table>

Display Taiwan DataFrame After Cleansing

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 151 entries, 0 to 150
    Data columns (total 4 columns):
     #   Column       Non-Null Count  Dtype 
    ---  ------       --------------  ----- 
     0    Population  151 non-null    int64 
     1   Year         151 non-null    int32 
     2   Country      151 non-null    object
     3   Code         151 non-null    object
    dtypes: int32(1), int64(1), object(2)
    memory usage: 4.3+ KB

```python
# prompt: change name of column

df_taiwan = df_taiwan.rename(columns={' Population': 'Population', 'Country': 'Country Name', 'Code': 'Country Code'})
df_taiwan.head()

```
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Population</th>
      <th>Year</th>
      <th>Country Name</th>
      <th>Country Code</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>7623130</td>
      <td>1950</td>
      <td>Taiwan</td>
      <td>TWN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>7934689</td>
      <td>1951</td>
      <td>Taiwan</td>
      <td>TWN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8251039</td>
      <td>1952</td>
      <td>Taiwan</td>
      <td>TWN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>8572131</td>
      <td>1953</td>
      <td>Taiwan</td>
      <td>TWN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>8897776</td>
      <td>1954</td>
      <td>Taiwan</td>
      <td>TWN</td>
    </tr>
  </tbody>
</table>

```python
# prompt: move column in this way Country Name , Country Code , Year , Population

new_order = ['Country Name', 'Country Code', 'Year', 'Population']
df_taiwan = df_taiwan[new_order]
df_taiwan.head()

```





  <div id="df-3737521d-bb46-4b78-bd3c-6e4951295099" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country Name</th>
      <th>Country Code</th>
      <th>Year</th>
      <th>Population</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>1950</td>
      <td>7623130</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>1951</td>
      <td>7934689</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>1952</td>
      <td>8251039</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>1953</td>
      <td>8572131</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>1954</td>
      <td>8897776</td>
    </tr>
  </tbody>
</table>

```python
# prompt: drop row that was Year 1950 - 1989 , 2020 - 2100 of df_taiwan

years_to_drop = list(range(1950, 1990)) + list(range(2020, 2101))
df_taiwan = df_taiwan[~df_taiwan['Year'].isin(years_to_drop)]

```
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country Name</th>
      <th>Country Code</th>
      <th>Year</th>
      <th>Population</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>40</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>1990</td>
      <td>20586174</td>
    </tr>
    <tr>
      <th>41</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>1991</td>
      <td>20770620</td>
    </tr>
    <tr>
      <th>42</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>1992</td>
      <td>20952222</td>
    </tr>
    <tr>
      <th>43</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>1993</td>
      <td>21125717</td>
    </tr>
    <tr>
      <th>44</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>1994</td>
      <td>21293437</td>
    </tr>
    <tr>
      <th>45</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>1995</td>
      <td>21455813</td>
    </tr>
    <tr>
      <th>46</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>1996</td>
      <td>21612429</td>
    </tr>
    <tr>
      <th>47</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>1997</td>
      <td>21764843</td>
    </tr>
    <tr>
      <th>48</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>1998</td>
      <td>21913672</td>
    </tr>
    <tr>
      <th>49</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>1999</td>
      <td>22057214</td>
    </tr>
    <tr>
      <th>50</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2000</td>
      <td>22194731</td>
    </tr>
    <tr>
      <th>51</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2001</td>
      <td>22333125</td>
    </tr>
    <tr>
      <th>52</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2002</td>
      <td>22469616</td>
    </tr>
    <tr>
      <th>53</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2003</td>
      <td>22593681</td>
    </tr>
    <tr>
      <th>54</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2004</td>
      <td>22703099</td>
    </tr>
    <tr>
      <th>55</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2005</td>
      <td>22796306</td>
    </tr>
    <tr>
      <th>56</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2006</td>
      <td>22874975</td>
    </tr>
    <tr>
      <th>57</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2007</td>
      <td>22942308</td>
    </tr>
    <tr>
      <th>58</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2008</td>
      <td>22998321</td>
    </tr>
    <tr>
      <th>59</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2009</td>
      <td>23044082</td>
    </tr>
    <tr>
      <th>60</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2010</td>
      <td>23083083</td>
    </tr>
    <tr>
      <th>61</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2011</td>
      <td>23143071</td>
    </tr>
    <tr>
      <th>62</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2012</td>
      <td>23234058</td>
    </tr>
    <tr>
      <th>63</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2013</td>
      <td>23330334</td>
    </tr>
    <tr>
      <th>64</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2014</td>
      <td>23422513</td>
    </tr>
    <tr>
      <th>65</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2015</td>
      <td>23512136</td>
    </tr>
    <tr>
      <th>66</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2016</td>
      <td>23594471</td>
    </tr>
    <tr>
      <th>67</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2017</td>
      <td>23665024</td>
    </tr>
    <tr>
      <th>68</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2018</td>
      <td>23726185</td>
    </tr>
    <tr>
      <th>69</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2019</td>
      <td>23777737</td>
    </tr>
  </tbody>
</table>

##### Join missing TWN
```python
# prompt: add row of df_taiwan in to df_population_melted

df_population_melted = pd.concat([df_population_melted, df_taiwan], ignore_index=True)
df_population_melted

```

  <div id="df-38e7d67b-f81b-428f-8b45-caa203a7d7e8" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country Name</th>
      <th>Country Code</th>
      <th>Year</th>
      <th>Population</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Aruba</td>
      <td>ABW</td>
      <td>1990</td>
      <td>62152.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Africa Eastern and Southern</td>
      <td>AFE</td>
      <td>1990</td>
      <td>304648010.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>1990</td>
      <td>12412311.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Africa Western and Central</td>
      <td>AFW</td>
      <td>1990</td>
      <td>204803865.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Angola</td>
      <td>AGO</td>
      <td>1990</td>
      <td>11848385.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>8005</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2015</td>
      <td>23512136.0</td>
    </tr>
    <tr>
      <th>8006</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2016</td>
      <td>23594471.0</td>
    </tr>
    <tr>
      <th>8007</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2017</td>
      <td>23665024.0</td>
    </tr>
    <tr>
      <th>8008</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2018</td>
      <td>23726185.0</td>
    </tr>
    <tr>
      <th>8009</th>
      <td>Taiwan</td>
      <td>TWN</td>
      <td>2019</td>
      <td>23777737.0</td>
    </tr>
  </tbody>
</table>

#### Check Invalid Country

```python
# prompt: show column Code in df_join1 was not in column Country Code in df_population

join1_codes = set(df_join1['Code'].unique())
population_codes = set(df_population_melted['Country Code'].unique())

codes_not_in_population = join1_codes - population_codes

print("Codes in df_join1['Code'] that are not in df_population['Country Code']:\n", codes_not_in_population)

```

    Codes in df_join1['Code'] that are not in df_population['Country Code']:
     {'NIU', 'TKL', 'COK'}
    


```python
join1_codes = set(df_join1['Year'].unique())
population_codes = set(df_population_melted['Year'].unique())

codes_not_in_population = join1_codes - population_codes

print("Codes in df_join1['Year'] that are not in df_population['Year']:\n", codes_not_in_population)
```

    Codes in df_join1['Year'] that are not in df_population['Year']:
     set()
    


```python
# prompt: check type of Year in df_join1

print(df_join1['Year'].dtype)

```

    int64
    


```python
df_population_melted['Year'].unique()
```




    array(['1990', '1991', '1992', '1993', '1994', '1995', '1996', '1997',
           '1998', '1999', '2000', '2001', '2002', '2003', '2004', '2005',
           '2006', '2007', '2008', '2009', '2010', '2011', '2012', '2013',
           '2014', '2015', '2016', '2017', '2018', '2019', 1990, 1991, 1992,
           1993, 1994, 1995, 1996, 1997, 1998, 1999, 2000, 2001, 2002, 2003,
           2004, 2005, 2006, 2007, 2008, 2009, 2010, 2011, 2012, 2013, 2014,
           2015, 2016, 2017, 2018, 2019], dtype=object)




```python
# Match type of Year before Merge

df_population_melted['Year'] = df_population_melted['Year'].astype('int64')

```


```python
df_population_melted[df_population_melted['Population'].isnull()]
```
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country Name</th>
      <th>Country Code</th>
      <th>Year</th>
      <th>Population</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>110</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>1990</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>376</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>1991</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>642</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>1992</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>659</th>
      <td>Kuwait</td>
      <td>KWT</td>
      <td>1992</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>908</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>1993</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>925</th>
      <td>Kuwait</td>
      <td>KWT</td>
      <td>1993</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1174</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>1994</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1191</th>
      <td>Kuwait</td>
      <td>KWT</td>
      <td>1994</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1440</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>1995</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1706</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>1996</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1972</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>1997</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2238</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>1998</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2504</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>1999</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2770</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2000</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3036</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2001</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3302</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2002</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3568</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2003</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3834</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2004</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4100</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2005</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4366</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2006</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4632</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2007</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4898</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2008</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5164</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2009</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5430</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2010</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5696</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2011</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5921</th>
      <td>Eritrea</td>
      <td>ERI</td>
      <td>2012</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5962</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2012</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6187</th>
      <td>Eritrea</td>
      <td>ERI</td>
      <td>2013</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6228</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2013</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6453</th>
      <td>Eritrea</td>
      <td>ERI</td>
      <td>2014</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6494</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2014</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6719</th>
      <td>Eritrea</td>
      <td>ERI</td>
      <td>2015</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6760</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2015</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6985</th>
      <td>Eritrea</td>
      <td>ERI</td>
      <td>2016</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>7026</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2016</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>7251</th>
      <td>Eritrea</td>
      <td>ERI</td>
      <td>2017</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>7292</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2017</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>7517</th>
      <td>Eritrea</td>
      <td>ERI</td>
      <td>2018</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>7558</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2018</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>7783</th>
      <td>Eritrea</td>
      <td>ERI</td>
      <td>2019</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>7824</th>
      <td>Not classified</td>
      <td>INX</td>
      <td>2019</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Create Main Table

#### Merge all data to be main Table
```python
# Merge on multiple keys: Inner join

# Alternative 1
#pd.merge(df_join1, df_population_melted, on=['StudentID', 'CourseID'], how='inner')

# Alternative 2
df_Main_data = pd.merge(df_join1, df_population_melted, left_on=['Code', 'Year'], right_on=['Country Code', 'Year'], how='outer')
df_Main_data
```

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country/Territory</th>
      <th>Code</th>
      <th>continent</th>
      <th>sub_region</th>
      <th>Year</th>
      <th>Meningitis</th>
      <th>Alzheimer's Disease and Other Dementias</th>
      <th>Parkinson's Disease</th>
      <th>Nutritional Deficiencies</th>
      <th>Malaria</th>
      <th>...</th>
      <th>Protein-Energy Malnutrition</th>
      <th>Road Injuries</th>
      <th>Chronic Respiratory Diseases</th>
      <th>Cirrhosis and Other Chronic Liver Diseases</th>
      <th>Digestive Diseases</th>
      <th>Fire, Heat, and Hot Substances</th>
      <th>Acute Hepatitis</th>
      <th>Country Name</th>
      <th>Country Code</th>
      <th>Population</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1990</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Aruba</td>
      <td>ABW</td>
      <td>62152.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1991</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Aruba</td>
      <td>ABW</td>
      <td>64623.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1992</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Aruba</td>
      <td>ABW</td>
      <td>68240.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1993</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Aruba</td>
      <td>ABW</td>
      <td>72495.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1994</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Aruba</td>
      <td>ABW</td>
      <td>76705.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>8095</th>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>Africa</td>
      <td>Eastern Africa</td>
      <td>2015</td>
      <td>1439.0</td>
      <td>754.0</td>
      <td>215.0</td>
      <td>3019.0</td>
      <td>2518.0</td>
      <td>...</td>
      <td>2990.0</td>
      <td>2373.0</td>
      <td>2751.0</td>
      <td>1956.0</td>
      <td>4202.0</td>
      <td>632.0</td>
      <td>146.0</td>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>13814642.0</td>
    </tr>
    <tr>
      <th>8096</th>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>Africa</td>
      <td>Eastern Africa</td>
      <td>2016</td>
      <td>1457.0</td>
      <td>767.0</td>
      <td>219.0</td>
      <td>3056.0</td>
      <td>2050.0</td>
      <td>...</td>
      <td>3027.0</td>
      <td>2436.0</td>
      <td>2788.0</td>
      <td>1962.0</td>
      <td>4264.0</td>
      <td>648.0</td>
      <td>146.0</td>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>14030338.0</td>
    </tr>
    <tr>
      <th>8097</th>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>Africa</td>
      <td>Eastern Africa</td>
      <td>2017</td>
      <td>1460.0</td>
      <td>781.0</td>
      <td>223.0</td>
      <td>2990.0</td>
      <td>2116.0</td>
      <td>...</td>
      <td>2962.0</td>
      <td>2473.0</td>
      <td>2818.0</td>
      <td>2007.0</td>
      <td>4342.0</td>
      <td>654.0</td>
      <td>144.0</td>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>14236599.0</td>
    </tr>
    <tr>
      <th>8098</th>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>Africa</td>
      <td>Eastern Africa</td>
      <td>2018</td>
      <td>1450.0</td>
      <td>795.0</td>
      <td>227.0</td>
      <td>2918.0</td>
      <td>2088.0</td>
      <td>...</td>
      <td>2890.0</td>
      <td>2509.0</td>
      <td>2849.0</td>
      <td>2030.0</td>
      <td>4377.0</td>
      <td>657.0</td>
      <td>139.0</td>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>14438812.0</td>
    </tr>
    <tr>
      <th>8099</th>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>Africa</td>
      <td>Eastern Africa</td>
      <td>2019</td>
      <td>1450.0</td>
      <td>812.0</td>
      <td>232.0</td>
      <td>2884.0</td>
      <td>2068.0</td>
      <td>...</td>
      <td>2855.0</td>
      <td>2554.0</td>
      <td>2891.0</td>
      <td>2065.0</td>
      <td>4437.0</td>
      <td>662.0</td>
      <td>136.0</td>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>14645473.0</td>
    </tr>
  </tbody>
</table>
<p>8100 rows × 39 columns</p>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### Drop Null and Duplicate columns
```python
# prompt: drop row in column Code that was NaN

df_Main_data = df_Main_data.dropna(subset=['Code'])
df_Main_data = df_Main_data.drop(['Country Name', 'Country Code'], axis=1)
```


```python
df_Main_data
```

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country/Territory</th>
      <th>Code</th>
      <th>continent</th>
      <th>sub_region</th>
      <th>Year</th>
      <th>Meningitis</th>
      <th>Alzheimer's Disease and Other Dementias</th>
      <th>Parkinson's Disease</th>
      <th>Nutritional Deficiencies</th>
      <th>Malaria</th>
      <th>...</th>
      <th>Chronic Kidney Disease</th>
      <th>Poisonings</th>
      <th>Protein-Energy Malnutrition</th>
      <th>Road Injuries</th>
      <th>Chronic Respiratory Diseases</th>
      <th>Cirrhosis and Other Chronic Liver Diseases</th>
      <th>Digestive Diseases</th>
      <th>Fire, Heat, and Hot Substances</th>
      <th>Acute Hepatitis</th>
      <th>Population</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>60</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1990</td>
      <td>2159.0</td>
      <td>1116.0</td>
      <td>371.0</td>
      <td>2087.0</td>
      <td>93.0</td>
      <td>...</td>
      <td>3709.0</td>
      <td>338.0</td>
      <td>2054.0</td>
      <td>4154.0</td>
      <td>5945.0</td>
      <td>2673.0</td>
      <td>5005.0</td>
      <td>323.0</td>
      <td>2985.0</td>
      <td>12412311.0</td>
    </tr>
    <tr>
      <th>61</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1991</td>
      <td>2218.0</td>
      <td>1136.0</td>
      <td>374.0</td>
      <td>2153.0</td>
      <td>189.0</td>
      <td>...</td>
      <td>3724.0</td>
      <td>351.0</td>
      <td>2119.0</td>
      <td>4472.0</td>
      <td>6050.0</td>
      <td>2728.0</td>
      <td>5120.0</td>
      <td>332.0</td>
      <td>3092.0</td>
      <td>13299016.0</td>
    </tr>
    <tr>
      <th>62</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1992</td>
      <td>2475.0</td>
      <td>1162.0</td>
      <td>378.0</td>
      <td>2441.0</td>
      <td>239.0</td>
      <td>...</td>
      <td>3776.0</td>
      <td>386.0</td>
      <td>2404.0</td>
      <td>5106.0</td>
      <td>6223.0</td>
      <td>2830.0</td>
      <td>5335.0</td>
      <td>360.0</td>
      <td>3325.0</td>
      <td>14485543.0</td>
    </tr>
    <tr>
      <th>63</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1993</td>
      <td>2812.0</td>
      <td>1187.0</td>
      <td>384.0</td>
      <td>2837.0</td>
      <td>108.0</td>
      <td>...</td>
      <td>3862.0</td>
      <td>425.0</td>
      <td>2797.0</td>
      <td>5681.0</td>
      <td>6445.0</td>
      <td>2943.0</td>
      <td>5568.0</td>
      <td>396.0</td>
      <td>3601.0</td>
      <td>15816601.0</td>
    </tr>
    <tr>
      <th>64</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1994</td>
      <td>3027.0</td>
      <td>1211.0</td>
      <td>391.0</td>
      <td>3081.0</td>
      <td>211.0</td>
      <td>...</td>
      <td>3932.0</td>
      <td>451.0</td>
      <td>3038.0</td>
      <td>6001.0</td>
      <td>6664.0</td>
      <td>3027.0</td>
      <td>5739.0</td>
      <td>420.0</td>
      <td>3816.0</td>
      <td>17075728.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>8095</th>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>Africa</td>
      <td>Eastern Africa</td>
      <td>2015</td>
      <td>1439.0</td>
      <td>754.0</td>
      <td>215.0</td>
      <td>3019.0</td>
      <td>2518.0</td>
      <td>...</td>
      <td>2108.0</td>
      <td>381.0</td>
      <td>2990.0</td>
      <td>2373.0</td>
      <td>2751.0</td>
      <td>1956.0</td>
      <td>4202.0</td>
      <td>632.0</td>
      <td>146.0</td>
      <td>13814642.0</td>
    </tr>
    <tr>
      <th>8096</th>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>Africa</td>
      <td>Eastern Africa</td>
      <td>2016</td>
      <td>1457.0</td>
      <td>767.0</td>
      <td>219.0</td>
      <td>3056.0</td>
      <td>2050.0</td>
      <td>...</td>
      <td>2160.0</td>
      <td>393.0</td>
      <td>3027.0</td>
      <td>2436.0</td>
      <td>2788.0</td>
      <td>1962.0</td>
      <td>4264.0</td>
      <td>648.0</td>
      <td>146.0</td>
      <td>14030338.0</td>
    </tr>
    <tr>
      <th>8097</th>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>Africa</td>
      <td>Eastern Africa</td>
      <td>2017</td>
      <td>1460.0</td>
      <td>781.0</td>
      <td>223.0</td>
      <td>2990.0</td>
      <td>2116.0</td>
      <td>...</td>
      <td>2196.0</td>
      <td>398.0</td>
      <td>2962.0</td>
      <td>2473.0</td>
      <td>2818.0</td>
      <td>2007.0</td>
      <td>4342.0</td>
      <td>654.0</td>
      <td>144.0</td>
      <td>14236599.0</td>
    </tr>
    <tr>
      <th>8098</th>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>Africa</td>
      <td>Eastern Africa</td>
      <td>2018</td>
      <td>1450.0</td>
      <td>795.0</td>
      <td>227.0</td>
      <td>2918.0</td>
      <td>2088.0</td>
      <td>...</td>
      <td>2240.0</td>
      <td>400.0</td>
      <td>2890.0</td>
      <td>2509.0</td>
      <td>2849.0</td>
      <td>2030.0</td>
      <td>4377.0</td>
      <td>657.0</td>
      <td>139.0</td>
      <td>14438812.0</td>
    </tr>
    <tr>
      <th>8099</th>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>Africa</td>
      <td>Eastern Africa</td>
      <td>2019</td>
      <td>1450.0</td>
      <td>812.0</td>
      <td>232.0</td>
      <td>2884.0</td>
      <td>2068.0</td>
      <td>...</td>
      <td>2292.0</td>
      <td>405.0</td>
      <td>2855.0</td>
      <td>2554.0</td>
      <td>2891.0</td>
      <td>2065.0</td>
      <td>4437.0</td>
      <td>662.0</td>
      <td>136.0</td>
      <td>14645473.0</td>
    </tr>
  </tbody>
</table>
<p>6120 rows × 37 columns</p>

```python
# prompt: show null data in column Population

df_Main_data[df_Main_data['Population'].isnull()]['Code'].unique()

```




    array(['COK', 'ERI', 'KWT', 'NIU', 'TKL'], dtype=object)




```python
# prompt: list of name of column

column_names = df_Main_data.columns.tolist()
print(column_names)
```

    ['Country/Territory', 'Code', 'continent', 'sub_region', 'Year', 'Meningitis', "Alzheimer's Disease and Other Dementias", "Parkinson's Disease", 'Nutritional Deficiencies', 'Malaria', 'Drowning', 'Interpersonal Violence', 'Maternal Disorders', 'HIV/AIDS', 'Drug Use Disorders', 'Tuberculosis', 'Cardiovascular Diseases', 'Lower Respiratory Infections', 'Neonatal Disorders', 'Alcohol Use Disorders', 'Self-harm', 'Exposure to Forces of Nature', 'Diarrheal Diseases', 'Environmental Heat and Cold Exposure', 'Neoplasms', 'Conflict and Terrorism', 'Diabetes Mellitus', 'Chronic Kidney Disease', 'Poisonings', 'Protein-Energy Malnutrition', 'Road Injuries', 'Chronic Respiratory Diseases', 'Cirrhosis and Other Chronic Liver Diseases', 'Digestive Diseases', 'Fire, Heat, and Hot Substances', 'Acute Hepatitis', 'Population']

<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### Rename Columns

```python
#change name of column of df_Main_data replace blank with "_" and Capitalized

df_Main_data = df_Main_data.rename(columns={'Country/Territory': 'Country', 'continent': 'Continent', 'sub_region': 'Sub_region', "Alzheimer's Disease and Other Dementias": 'Alzheimers_Disease_and_Other_Dementias', "Parkinson's Disease": 'Parkinsons_Disease', 'Nutritional Deficiencies': 'Nutritional_Deficiencies', 'Interpersonal Violence': 'Interpersonal_Violence', 'Maternal Disorders': 'Maternal_Disorders', 'HIV/AIDS': 'HIV', 'Drug Use Disorders': 'Drug_Use_Disorders', 'Cardiovascular Diseases': 'Cardiovascular_Diseases', 'Lower Respiratory Infections': 'Lower_Respiratory_Infections', 'Neonatal Disorders': 'Neonatal_Disorders', 'Alcohol Use Disorders': 'Alcohol_Use_Disorders', 'Self-harm': 'Self_harm', 'Exposure to Forces of Nature': 'Exposure_to_Forces_of_Nature', 'Diarrheal Diseases': 'Diarrheal_Diseases', 'Environmental Heat and Cold Exposure': 'Environmental_Heat_and_Cold_Exposure', 'Conflict and Terrorism': 'Conflict_and_Terrorism', 'Diabetes Mellitus': 'Diabetes_Mellitus', 'Chronic Kidney Disease': 'Chronic_Kidney_Disease', 'Protein-Energy Malnutrition': 'Protein_Energy_Malnutrition', 'Road Injuries': 'Road_Injuries', 'Chronic Respiratory Diseases': 'Chronic_Respiratory_Diseases', 'Cirrhosis and Other Chronic Liver Diseases': 'Cirrhosis_and_Other_Chronic_Liver_Diseases', 'Digestive Diseases': 'Digestive_Diseases', 'Fire, Heat, and Hot Substances': 'Fire_Heat_and_Hot_Substances', 'Acute Hepatitis': 'Acute_Hepatitis'})
```


```python
df_Main_data.head()
```

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>Code</th>
      <th>Continent</th>
      <th>Sub_region</th>
      <th>Year</th>
      <th>Meningitis</th>
      <th>Alzheimers_Disease_and_Other_Dementias</th>
      <th>Parkinsons_Disease</th>
      <th>Nutritional_Deficiencies</th>
      <th>Malaria</th>
      <th>...</th>
      <th>Chronic_Kidney_Disease</th>
      <th>Poisonings</th>
      <th>Protein_Energy_Malnutrition</th>
      <th>Road_Injuries</th>
      <th>Chronic_Respiratory_Diseases</th>
      <th>Cirrhosis_and_Other_Chronic_Liver_Diseases</th>
      <th>Digestive_Diseases</th>
      <th>Fire_Heat_and_Hot_Substances</th>
      <th>Acute_Hepatitis</th>
      <th>Population</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>60</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1990</td>
      <td>2159.0</td>
      <td>1116.0</td>
      <td>371.0</td>
      <td>2087.0</td>
      <td>93.0</td>
      <td>...</td>
      <td>3709.0</td>
      <td>338.0</td>
      <td>2054.0</td>
      <td>4154.0</td>
      <td>5945.0</td>
      <td>2673.0</td>
      <td>5005.0</td>
      <td>323.0</td>
      <td>2985.0</td>
      <td>12412311.0</td>
    </tr>
    <tr>
      <th>61</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1991</td>
      <td>2218.0</td>
      <td>1136.0</td>
      <td>374.0</td>
      <td>2153.0</td>
      <td>189.0</td>
      <td>...</td>
      <td>3724.0</td>
      <td>351.0</td>
      <td>2119.0</td>
      <td>4472.0</td>
      <td>6050.0</td>
      <td>2728.0</td>
      <td>5120.0</td>
      <td>332.0</td>
      <td>3092.0</td>
      <td>13299016.0</td>
    </tr>
    <tr>
      <th>62</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1992</td>
      <td>2475.0</td>
      <td>1162.0</td>
      <td>378.0</td>
      <td>2441.0</td>
      <td>239.0</td>
      <td>...</td>
      <td>3776.0</td>
      <td>386.0</td>
      <td>2404.0</td>
      <td>5106.0</td>
      <td>6223.0</td>
      <td>2830.0</td>
      <td>5335.0</td>
      <td>360.0</td>
      <td>3325.0</td>
      <td>14485543.0</td>
    </tr>
    <tr>
      <th>63</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1993</td>
      <td>2812.0</td>
      <td>1187.0</td>
      <td>384.0</td>
      <td>2837.0</td>
      <td>108.0</td>
      <td>...</td>
      <td>3862.0</td>
      <td>425.0</td>
      <td>2797.0</td>
      <td>5681.0</td>
      <td>6445.0</td>
      <td>2943.0</td>
      <td>5568.0</td>
      <td>396.0</td>
      <td>3601.0</td>
      <td>15816601.0</td>
    </tr>
    <tr>
      <th>64</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1994</td>
      <td>3027.0</td>
      <td>1211.0</td>
      <td>391.0</td>
      <td>3081.0</td>
      <td>211.0</td>
      <td>...</td>
      <td>3932.0</td>
      <td>451.0</td>
      <td>3038.0</td>
      <td>6001.0</td>
      <td>6664.0</td>
      <td>3027.0</td>
      <td>5739.0</td>
      <td>420.0</td>
      <td>3816.0</td>
      <td>17075728.0</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 37 columns</p>

```python
column_names = df_Main_data.columns.tolist()
print(column_names)
```

    ['Country', 'Code', 'Continent', 'Sub_region', 'Year', 'Meningitis', 'Alzheimers_Disease_and_Other_Dementias', 'Parkinsons_Disease', 'Nutritional_Deficiencies', 'Malaria', 'Drowning', 'Interpersonal_Violence', 'Maternal_Disorders', 'HIV', 'Drug_Use_Disorders', 'Tuberculosis', 'Cardiovascular_Diseases', 'Lower_Respiratory_Infections', 'Neonatal_Disorders', 'Alcohol_Use_Disorders', 'Self_harm', 'Exposure_to_Forces_of_Nature', 'Diarrheal_Diseases', 'Environmental_Heat_and_Cold_Exposure', 'Neoplasms', 'Conflict_and_Terrorism', 'Diabetes_Mellitus', 'Chronic_Kidney_Disease', 'Poisonings', 'Protein_Energy_Malnutrition', 'Road_Injuries', 'Chronic_Respiratory_Diseases', 'Cirrhosis_and_Other_Chronic_Liver_Diseases', 'Digestive_Diseases', 'Fire_Heat_and_Hot_Substances', 'Acute_Hepatitis', 'Population']

<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### Add Column Total amount of Death by Cause and Ratio of Death per Population

```python
# prompt: add column total_dead that sum from column Meningitis to column Acute_Hepatitis
#Use column_to_sum for represent all cause of death
columns_to_sum = ['Meningitis', 'Alzheimers_Disease_and_Other_Dementias', 'Parkinsons_Disease',
                  'Nutritional_Deficiencies', 'Malaria', 'Drowning', 'Interpersonal_Violence',
                  'Maternal_Disorders', 'HIV', 'Drug_Use_Disorders', 'Tuberculosis', 'Cardiovascular_Diseases',
                  'Lower_Respiratory_Infections', 'Neonatal_Disorders', 'Alcohol_Use_Disorders', 'Self_harm',
                  'Exposure_to_Forces_of_Nature', 'Diarrheal_Diseases', 'Environmental_Heat_and_Cold_Exposure',
                  'Neoplasms', 'Conflict_and_Terrorism', 'Diabetes_Mellitus', 'Chronic_Kidney_Disease',
                  'Poisonings', 'Protein_Energy_Malnutrition', 'Road_Injuries', 'Chronic_Respiratory_Diseases',
                  'Cirrhosis_and_Other_Chronic_Liver_Diseases', 'Digestive_Diseases', 'Fire_Heat_and_Hot_Substances', 'Acute_Hepatitis']

df_Main_data['Total_Dead'] = df_Main_data[columns_to_sum].sum(axis=1)

```


```python
df_Main_data
```

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>Code</th>
      <th>Continent</th>
      <th>Sub_region</th>
      <th>Year</th>
      <th>Meningitis</th>
      <th>Alzheimers_Disease_and_Other_Dementias</th>
      <th>Parkinsons_Disease</th>
      <th>Nutritional_Deficiencies</th>
      <th>Malaria</th>
      <th>...</th>
      <th>Poisonings</th>
      <th>Protein_Energy_Malnutrition</th>
      <th>Road_Injuries</th>
      <th>Chronic_Respiratory_Diseases</th>
      <th>Cirrhosis_and_Other_Chronic_Liver_Diseases</th>
      <th>Digestive_Diseases</th>
      <th>Fire_Heat_and_Hot_Substances</th>
      <th>Acute_Hepatitis</th>
      <th>Population</th>
      <th>Total_Dead</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>60</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1990</td>
      <td>2159.0</td>
      <td>1116.0</td>
      <td>371.0</td>
      <td>2087.0</td>
      <td>93.0</td>
      <td>...</td>
      <td>338.0</td>
      <td>2054.0</td>
      <td>4154.0</td>
      <td>5945.0</td>
      <td>2673.0</td>
      <td>5005.0</td>
      <td>323.0</td>
      <td>2985.0</td>
      <td>12412311.0</td>
      <td>147971.0</td>
    </tr>
    <tr>
      <th>61</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1991</td>
      <td>2218.0</td>
      <td>1136.0</td>
      <td>374.0</td>
      <td>2153.0</td>
      <td>189.0</td>
      <td>...</td>
      <td>351.0</td>
      <td>2119.0</td>
      <td>4472.0</td>
      <td>6050.0</td>
      <td>2728.0</td>
      <td>5120.0</td>
      <td>332.0</td>
      <td>3092.0</td>
      <td>13299016.0</td>
      <td>156844.0</td>
    </tr>
    <tr>
      <th>62</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1992</td>
      <td>2475.0</td>
      <td>1162.0</td>
      <td>378.0</td>
      <td>2441.0</td>
      <td>239.0</td>
      <td>...</td>
      <td>386.0</td>
      <td>2404.0</td>
      <td>5106.0</td>
      <td>6223.0</td>
      <td>2830.0</td>
      <td>5335.0</td>
      <td>360.0</td>
      <td>3325.0</td>
      <td>14485543.0</td>
      <td>169156.0</td>
    </tr>
    <tr>
      <th>63</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1993</td>
      <td>2812.0</td>
      <td>1187.0</td>
      <td>384.0</td>
      <td>2837.0</td>
      <td>108.0</td>
      <td>...</td>
      <td>425.0</td>
      <td>2797.0</td>
      <td>5681.0</td>
      <td>6445.0</td>
      <td>2943.0</td>
      <td>5568.0</td>
      <td>396.0</td>
      <td>3601.0</td>
      <td>15816601.0</td>
      <td>182230.0</td>
    </tr>
    <tr>
      <th>64</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1994</td>
      <td>3027.0</td>
      <td>1211.0</td>
      <td>391.0</td>
      <td>3081.0</td>
      <td>211.0</td>
      <td>...</td>
      <td>451.0</td>
      <td>3038.0</td>
      <td>6001.0</td>
      <td>6664.0</td>
      <td>3027.0</td>
      <td>5739.0</td>
      <td>420.0</td>
      <td>3816.0</td>
      <td>17075728.0</td>
      <td>194795.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>8095</th>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>Africa</td>
      <td>Eastern Africa</td>
      <td>2015</td>
      <td>1439.0</td>
      <td>754.0</td>
      <td>215.0</td>
      <td>3019.0</td>
      <td>2518.0</td>
      <td>...</td>
      <td>381.0</td>
      <td>2990.0</td>
      <td>2373.0</td>
      <td>2751.0</td>
      <td>1956.0</td>
      <td>4202.0</td>
      <td>632.0</td>
      <td>146.0</td>
      <td>13814642.0</td>
      <td>130080.0</td>
    </tr>
    <tr>
      <th>8096</th>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>Africa</td>
      <td>Eastern Africa</td>
      <td>2016</td>
      <td>1457.0</td>
      <td>767.0</td>
      <td>219.0</td>
      <td>3056.0</td>
      <td>2050.0</td>
      <td>...</td>
      <td>393.0</td>
      <td>3027.0</td>
      <td>2436.0</td>
      <td>2788.0</td>
      <td>1962.0</td>
      <td>4264.0</td>
      <td>648.0</td>
      <td>146.0</td>
      <td>14030338.0</td>
      <td>128274.0</td>
    </tr>
    <tr>
      <th>8097</th>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>Africa</td>
      <td>Eastern Africa</td>
      <td>2017</td>
      <td>1460.0</td>
      <td>781.0</td>
      <td>223.0</td>
      <td>2990.0</td>
      <td>2116.0</td>
      <td>...</td>
      <td>398.0</td>
      <td>2962.0</td>
      <td>2473.0</td>
      <td>2818.0</td>
      <td>2007.0</td>
      <td>4342.0</td>
      <td>654.0</td>
      <td>144.0</td>
      <td>14236599.0</td>
      <td>126515.0</td>
    </tr>
    <tr>
      <th>8098</th>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>Africa</td>
      <td>Eastern Africa</td>
      <td>2018</td>
      <td>1450.0</td>
      <td>795.0</td>
      <td>227.0</td>
      <td>2918.0</td>
      <td>2088.0</td>
      <td>...</td>
      <td>400.0</td>
      <td>2890.0</td>
      <td>2509.0</td>
      <td>2849.0</td>
      <td>2030.0</td>
      <td>4377.0</td>
      <td>657.0</td>
      <td>139.0</td>
      <td>14438812.0</td>
      <td>123506.0</td>
    </tr>
    <tr>
      <th>8099</th>
      <td>Zimbabwe</td>
      <td>ZWE</td>
      <td>Africa</td>
      <td>Eastern Africa</td>
      <td>2019</td>
      <td>1450.0</td>
      <td>812.0</td>
      <td>232.0</td>
      <td>2884.0</td>
      <td>2068.0</td>
      <td>...</td>
      <td>405.0</td>
      <td>2855.0</td>
      <td>2554.0</td>
      <td>2891.0</td>
      <td>2065.0</td>
      <td>4437.0</td>
      <td>662.0</td>
      <td>136.0</td>
      <td>14645473.0</td>
      <td>123540.0</td>
    </tr>
  </tbody>
</table>
<p>6120 rows × 38 columns</p>

```python
# prompt: move column Population in to last column

# Get a list of column names
cols = list(df_Main_data.columns)

# Find the index of the 'Population' column
population_index = cols.index('Population')

# Remove 'Population' from its original position
cols.pop(population_index)

# Append 'Population' to the end of the list
cols.append('Population')

# Reorder the DataFrame columns based on the new list
df_Main_data = df_Main_data[cols]

df_Main_data.head()

```

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>Code</th>
      <th>Continent</th>
      <th>Sub_region</th>
      <th>Year</th>
      <th>Meningitis</th>
      <th>Alzheimers_Disease_and_Other_Dementias</th>
      <th>Parkinsons_Disease</th>
      <th>Nutritional_Deficiencies</th>
      <th>Malaria</th>
      <th>...</th>
      <th>Poisonings</th>
      <th>Protein_Energy_Malnutrition</th>
      <th>Road_Injuries</th>
      <th>Chronic_Respiratory_Diseases</th>
      <th>Cirrhosis_and_Other_Chronic_Liver_Diseases</th>
      <th>Digestive_Diseases</th>
      <th>Fire_Heat_and_Hot_Substances</th>
      <th>Acute_Hepatitis</th>
      <th>Total_Dead</th>
      <th>Population</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>60</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1990</td>
      <td>2159.0</td>
      <td>1116.0</td>
      <td>371.0</td>
      <td>2087.0</td>
      <td>93.0</td>
      <td>...</td>
      <td>338.0</td>
      <td>2054.0</td>
      <td>4154.0</td>
      <td>5945.0</td>
      <td>2673.0</td>
      <td>5005.0</td>
      <td>323.0</td>
      <td>2985.0</td>
      <td>147971.0</td>
      <td>12412311.0</td>
    </tr>
    <tr>
      <th>61</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1991</td>
      <td>2218.0</td>
      <td>1136.0</td>
      <td>374.0</td>
      <td>2153.0</td>
      <td>189.0</td>
      <td>...</td>
      <td>351.0</td>
      <td>2119.0</td>
      <td>4472.0</td>
      <td>6050.0</td>
      <td>2728.0</td>
      <td>5120.0</td>
      <td>332.0</td>
      <td>3092.0</td>
      <td>156844.0</td>
      <td>13299016.0</td>
    </tr>
    <tr>
      <th>62</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1992</td>
      <td>2475.0</td>
      <td>1162.0</td>
      <td>378.0</td>
      <td>2441.0</td>
      <td>239.0</td>
      <td>...</td>
      <td>386.0</td>
      <td>2404.0</td>
      <td>5106.0</td>
      <td>6223.0</td>
      <td>2830.0</td>
      <td>5335.0</td>
      <td>360.0</td>
      <td>3325.0</td>
      <td>169156.0</td>
      <td>14485543.0</td>
    </tr>
    <tr>
      <th>63</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1993</td>
      <td>2812.0</td>
      <td>1187.0</td>
      <td>384.0</td>
      <td>2837.0</td>
      <td>108.0</td>
      <td>...</td>
      <td>425.0</td>
      <td>2797.0</td>
      <td>5681.0</td>
      <td>6445.0</td>
      <td>2943.0</td>
      <td>5568.0</td>
      <td>396.0</td>
      <td>3601.0</td>
      <td>182230.0</td>
      <td>15816601.0</td>
    </tr>
    <tr>
      <th>64</th>
      <td>Afghanistan</td>
      <td>AFG</td>
      <td>Asia</td>
      <td>Southern Asia</td>
      <td>1994</td>
      <td>3027.0</td>
      <td>1211.0</td>
      <td>391.0</td>
      <td>3081.0</td>
      <td>211.0</td>
      <td>...</td>
      <td>451.0</td>
      <td>3038.0</td>
      <td>6001.0</td>
      <td>6664.0</td>
      <td>3027.0</td>
      <td>5739.0</td>
      <td>420.0</td>
      <td>3816.0</td>
      <td>194795.0</td>
      <td>17075728.0</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 38 columns</p>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Death Cause Analysis
- <a href="Markdown/Death_Cause_Analysis.md" target="_blank">Death Cause Analysis</a>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

**การวิเคราะห์การเสียชีวิตจากโรคต่างๆ ตั้งแต่ปี 1990 - 2019**

การเสียชีวิตจากโรคต่างๆ ทั่วโลกในช่วงปี 1990 - 2019 มีแนวโน้มเปลี่ยนแปลงไปตามปัจจัยหลายประการ เช่น ความก้าวหน้าทางการแพทย์ วิถีชีวิตของประชากร การพัฒนาสังคม และเศรษฐกิจ รวมถึงการเพิ่มขึ้นของจำนวนประชากรสูงอายุ ข้อมูลจากการวิเคราะห์นี้จะแสดงให้เห็นถึงสาเหตุหลักของการเสียชีวิตในแต่ละภูมิภาคทั่วโลก รวมถึงแนวโน้มของการเสียชีวิตจากโรคเรื้อรังที่เกี่ยวข้องกับปัจจัยเสี่ยงต่างๆ เช่น โรคหัวใจ มะเร็ง เบาหวาน และโรคทางเดินหายใจเรื้อรังของคนภูมิภาคเอเชียตะวันออกเฉียงเหนือ

**การเสียชีวิตทั่วโลกตั้งแต่ปี 1990 - 2019**

  จากข้อมูลที่นำมาวิเคราะห์แสดงให้เห็นว่าการเสียชีวิตจากโรคต่างๆ มีการเปลี่ยนแปลงอย่างชัดเจนในช่วง 30 ปีที่ผ่านมานับตั้งแต่ปี 1990 - 2019 กราฟด้านล่างแสดงจำนวนผู้เสียชีวิตจากโรคสำคัญทั่วโลก โดยโรคที่มีปริมาณเสียชีวิตสูงสุดในช่วงเวลาดังกล่าวประกอบไปด้วย:

```markdown
![Example Plot](images1/plot.png)
```

1.   โรคหัวใจและหลอดเลือด(Cardiovascular_Diseases)
2.   เนื้องอก (Neoplasms)
3.   โรคระบบทางเดินหายใจเรื้อรัง (Chronic_Respiratory_Diseases)
4.   การติดเชื้อทางเดินหายใจส่วนล่าง (Lower_Respiratory_Infections)
5.   โรคในทารกแรกเกิด (Neonatal_Disorders)
6.   โรคอุจจาระร่วง (Diarrheal_Diseases)
7.   โรคระบบย่อยอาหาร (Digestive_Diseases)
8.   วัณโรค (Tuberculosis)
9.   ตับแข็งและโรคตับเรื้อรังอื่นๆ (Cirrhosis_and_Other_Chronic_Liver_Diseases)
10.  เอชไอวี (HIV)

### **การจัดกลุ่มปัจจัยเสี่ยงในการวิเคราะห์สาเหตุการเสียชีวิต**

เนื่องจากข้อมูลเกี่ยวกับสาเหตุการเสียชีวิตมีจำนวนมาก เราจึงได้ทำการจัดกลุ่มปัจจัยเสี่ยงออกเป็น 4 กลุ่มหลัก เพื่อนำไปวิเคราะห์ต่อ ดังนี้:

1. โรคเรื้อรัง(Chronic Diseases)
2. โรคติดต่อ (Infectious Diseases)
3. ปัจจัยภายนอกที่ทำให้เสียชีวิต (Environmental and External Causes)
4. ปัจจัยเสี่ยงจากไลฟ์สไตล์การใช้ชีวิต (Lifestyle Related Factors)
   
การจัดกลุ่มปัจจัยเหล่านี้จะช่วยให้เราสามารถพิจารณาสาเหตุที่ทำให้ผู้คนเสียชีวิตได้มากที่สุด โดยเราจะนำมาจัดอันดับจากการเสียชีวิตที่เกิดจากแต่ละปัจจัย และจำแนกเป็นทวีปเพื่อให้เห็นภาพรวมของผลกระทบจากปัจจัยเสี่ยงต่างๆ ต่อปริมาณเสียชีวิตในแต่ละทวีป

```markdown
![Example Plot](Table/plot.png)
```

```markdown
![Example Plot](Heatmap/plot.png)
```

วิธีการนี้จะทำให้การวิเคราะห์ชัดเจนขึ้นว่า ปัจจัยเสี่ยงใดที่ทำให้เกิดการเสียชีวิตมากที่สุด และแต่ละทวีปได้รับผลกระทบจากปัจจัยเหล่านี้ในรูปแบบใดบ้าง ซึ่งจะเห็นว่าทวีปเอเชียมีอัตราการเสียชีวิตมากที่สุดในทุกปัจจัย

การวิเคราะห์นี้ชี้ให้เห็นถึงความจำเป็นในการให้ความสำคัญกับการดูแลสุขภาพและการป้องกันโรคในทวีปเอเชีย รวมถึงการสร้างความตระหนักรู้เกี่ยวกับปัจจัยเสี่ยงที่สามารถควบคุมได้ เพื่อช่วยลดอัตราการเสียชีวิตในอนาคต

**แนวโน้มการเสียชีวิตของแต่ละปัจจัยเสี่ยงในแต่ละทวีปตั้งแต่ปี 1990 - 2019**

จากการวิเคราะห์ข้อมูลการเสียชีวิตของประชากรทั่วโลกตั้งแต่ปี 1990 - 2019 พบว่าแนวโน้มการเสียชีวิตมีการเปลี่ยนแปลงไปตามปัจจัยเสี่ยงหลัก 4 ประการ ได้แก่ โรคเรื้อรัง โรคติดต่อ ปัจจัยภายนอก และพฤติกรรมการใช้ชีวิต

```markdown
![Example Plot](Map3/plot.png)
```

- โรคเรื้อรัง: เช่น โรคหัวใจ มะเร็ง และโรคทางเดินหายใจเรื้อรัง มีแนวโน้มเพิ่มขึ้นอย่างต่อเนื่องในหลายทวีป
- โรคติดต่อ: แนวโน้มของการเสียชีวิตจากโรคติดต่อมีการลดลงในบางภูมิภาคที่มีการพัฒนาทางการแพทย์และการเข้าถึงวัคซีนมากขึ้น
- ปัจจัยภายนอก: การเสียชีวิตจากอุบัติเหตุและความรุนแรงทางสังคมมีการเปลี่ยนแปลงขึ้นลงตามสภาพเศรษฐกิจและความมั่นคงของแต่ละภูมิภาค
- พฤติกรรมการใช้ชีวิต: ปัจจัยเสี่ยงจากการใช้ชีวิต เช่น การสูบบุหรี่ การดื่มแอลกอฮอล์ และการรับประทานอาหารที่ไม่ดีต่อสุขภาพ ยังคงเป็นปัจจัยสำคัญที่ทำให้เกิดการเสียชีวิตเพิ่มขึ้นในหลายภูมิภาค

การเปลี่ยนแปลงของแนวโน้มเหล่านี้สะท้อนถึงความก้าวหน้าทางการแพทย์ การเปลี่ยนแปลงด้านเศรษฐกิจ และวัฒนธรรมการใช้ชีวิตของผู้คนในแต่ละทวีป

จากการนำข้อมูลผู้เสียชีวิตในแต่ละทวีปมาเทียบอัตราส่วนกับจำนวนประชากรพบว่าทวีปเอเชียไม่ใช่ทวีปที่มีอัตราการเสียชีวิตเทียบกับประชากรสูงสุด

```markdown
![Example Plot](Map4/plot.png)
```

จากการวิเคราะห์ข้อมูลผู้เสียชีวิตในแต่ละทวีปเมื่อเทียบอัตราส่วนกับจำนวนประชากร พบว่าทวีปเอเชียไม่ได้เป็นทวีปที่มีอัตราการเสียชีวิตสูงสุดเมื่อเทียบกับประชากรทั้งหมด ขณะที่ในทวีปอื่น ๆ เช่น แอฟริกาและอเมริกาใต้ พบว่ามีอัตราการเสียชีวิตสูงจากปัจจัยเสี่ยงที่เกี่ยวข้องกับโรคติดต่อ


ข้อมูลนี้แสดงถึงอัตราการเปลี่ยนแปลงของอัตราการเสียชีวิตต่อประชากรในแต่ละทวีป **โดยใช้หน่วยเป็นการคูณล้าน (x 1,000,000)** เพื่อให้อ่านเข้าใจง่ายขึ้น ซึ่งมีการคำนวณ Slope (แนวโน้ม) ของการเปลี่ยนแปลงในแต่ละปี ดังนี้:

1. ปัจจัยเสี่ยงที่เกี่ยวข้องกับไลฟ์สไตล์ (Lifestyle-Related Factors):
   
- Africa: -20
- Americas: -0.5
- Asia: -10
- Europe: -0.5
- Oceania: -0.4

2. ปัจจัยเสี่ยงจากสิ่งแวดล้อมและสาเหตุภายนอก (Environmental and External Causes):
- Africa: -10
- Americas: -4
- Asia: -5
- Europe: -6
- Oceania: -3

3. โรคติดเชื้อ (Infectious Diseases):
- Africa: -90
- Americas: -20
- Asia: -40
- Europe: -2
- Oceania: +0.05
4. โรคเรื้อรัง (Chronic Diseases):

- Africa: -40
- Americas: +30 (แนวโน้มเพิ่มขึ้น)
- Asia: +30 (แนวโน้มเพิ่มขึ้น)
- Europe: +30 (แนวโน้มเพิ่มขึ้น)
- Oceania: +1.5 (แนวโน้มเพิ่มขึ้นเล็กน้อย)

จากข้อมูลเหล่านี้สามารถเห็นได้ว่าปัจจัยเสี่ยงที่เกี่ยวข้องกับไลฟ์สไตล์และโรคเรื้อรังในทวีปต่าง ๆ มีแนวโน้มการเปลี่ยนแปลงที่แตกต่างกัน ขณะที่บางทวีปมีแนวโน้มลดลง เช่น แอฟริกา แต่ในยุโรปและอเมริกากลับมีแนวโน้มเพิ่มขึ้น

___

### **การเสียชีวิตจากโรคเรื้อรังในภูมิภาคเอเชียตะวันออกเฉียงเหนือ**

ภูมิภาคเอเชียตะวันออกเฉียงเหนือมีประชากรที่มีความหลากหลายทางวัฒนธรรมและเศรษฐกิจ การศึกษาในครั้งนี้มุ่งเน้นไปที่การวิเคราะห์การเสียชีวิตจากโรคเรื้อรังในช่วงปี 1990 ถึง 2019 ซึ่งเป็นช่วงเวลาที่มีการเปลี่ยนแปลงทางการแพทย์และการพัฒนาสังคมอย่างมีนัยสำคัญ

```markdown
![Example Plot](Map5/plot.png)
```

### **อัตราการเปลี่ยนแปลงจากอัตราส่วนผู้เสียชีวิตต่อจำนวนประชากรในภูมิภาคเอเชียตะวันออกเฉียงเหนือ**

การวิเคราะห์ข้อมูลการเสียชีวิตที่เกิดจากโรคเรื้อรังโดยเฉพาะอย่างยิ่งเราจะพิจารณาถึงอัตราส่วนผู้เสียชีวิตต่อจำนวนประชากร เพื่อให้เห็นถึงความสัมพันธ์ระหว่างจำนวนผู้เสียชีวิตและขนาดของประชากรในภูมิภาคนี้

```markdown
![Example Plot](Map6/plot.png)
```

โดยเน้นไปที่การวิเคราะห์อัตราการเปลี่ยนแปลงจากอัตราส่วนผู้เสียชีวิตต่อจำนวนประชากรในภูมิภาคเอเชียตะวันออกเฉียงเหนือ โดยเฉพาะอย่างยิ่งการเสียชีวิตจากโรคเรื้อรังที่เป็นปัญหาสำคัญในระดับภูมิภาค การวิเคราะห์นี้มีวัตถุประสงค์เพื่อให้เข้าใจถึงแนวโน้มการเปลี่ยนแปลงอัตราการเสียชีวิตในภูมิภาคนี้ในช่วง 1990 - 2019

```markdown
![Example Plot](Map7/plot.png)
```

การเปรียบเทียบกับประเทศที่มีปัจจัยคล้ายคลึงกับประเทศไทย เช่น เมียนมาร์ ฟิลิปปินส์ และเวียดนาม จะช่วยให้เราเห็นแนวโน้มและความแตกต่างในอัตราการเสียชีวิตจากโรคเรื้อรังในประเทศเพื่อนบ้าน จากข้อมูลแสดงให้เห็นว่าประเทศเมียนมาร์มีอัตราการเสียชีวิตต่อประชากรที่ลดลงอย่างน่าสนใจ ซึ่งเป็นประเด็นที่ควรศึกษาต่อไปในอนาคต เพื่อใช้ข้อมูลนี้ในการพัฒนากลยุทธ์ที่เหมาะสม นอกจากนี้ยังเป็นข้อมูลพื้นฐานในการสร้างกลยุทธ์เพื่อลดอัตราการเสียชีวิตจากโรคเรื้อรังในอนาคต

___


## Event Analysis

### Detail of Event during 1990 - 2019

Events That Increased Mortality Rates

1. เหตุการณ์ที่ทำให้มีผู้เสียชีวิตเพิ่มขึ้น **การแพร่ระบาดของ HIV/AIDS**: พ.ศ. 2533 (1990) - ตลอดทศวรรษ 1990 โดยเฉพาะในแอฟริกาและเอเชีย 
 - [WHO HIV/AIDS page](https://www.who.int/health-topics/hiv-aids#tab=tab_1)
 - [40 Years of AIDS](https://www.ucsf.edu/news/2021/06/420686/40-years-aids-timeline-epidemic)
2. **การระบาดของไข้มาลาเรียในแอฟริกา**: ทศวรรษ 1990 และ 2000 - ภูมิภาคแอฟริกาประสบปัญหาอัตราการตายจากมาลาเรียสูง จนกระทั่งมีการกระจายการใช้มุ้งและยาต้านมาลาเรียที่ช่วยลดจำนวนการเสียชีวิต [WHO Malaria Overview](https://www.who.int/health-topics/malaria)
3. **สงครามยูโกสลาเวีย**: พ.ศ. 2534-2544 (1991-2001) - ความขัดแย้งและสงครามกลางเมืองในยูโกสลาเวีย ส่งผลให้มีผู้เสียชีวิตจำนวนมาก[BBC's Balkans Conflict Overview](https://www.bbc.com/news/world-europe-17632399)
4. **การฆ่าล้างเผ่าพันธุ์ในรวันดา**: พ.ศ. 2537 (1994) - เหตุการณ์นี้ทำให้มีผู้เสียชีวิตกว่า 800,000 คนภายในเวลาไม่กี่เดือน [UN - Rwanda Genocide](https://www.un.org/en/preventgenocide/rwanda/education/rwandagenocide.shtml)
5. **ภาวะขาดแคลนอาหารในเกาหลีเหนือ**: พ.ศ. 2537-2541 (1994-1998) - การขาดแคลนอาหารอย่างรุนแรงในเกาหลีเหนือทำให้ประชากรจำนวนมากเสียชีวิตจากภาวะอดอยาก[Council on Foreign Relations - North Korea Famine](https://www.cfr.org/backgrounder/north-korea-famine)
6. **แผ่นดินไหวในโกเบ ประเทศญี่ปุ่น**: พ.ศ. 2538 (1995) - คร่าชีวิตผู้คนกว่า 6,000 คน [1995 Kobe Earthquake](https://factsanddetails.com/japan/cat26/sub160/item863.html)
7. **สงครามกลางเมืองในเซียร์ราลีโอน**: พ.ศ. 2534-2545 (1991-2002) - ความรุนแรงจากสงครามกลางเมืองส่งผลให้มีผู้เสียชีวิตและผู้พลัดถิ่นจำนวนมาก [Sierra Leone Civil War](https://www.blackpast.org/global-african-history/sierra-leone-civil-war-1991-2002/)
8. **การแพร่ระบาดของวัณโรค (TB)**: ตลอดทศวรรษ 1990 - วัณโรคกลับมาแพร่ระบาดในหลายประเทศทั่วโลก [Tuberculosis](https://bmcinfectdis.biomedcentral.com/articles/10.1186/s12879-024-09079-5)
9. **สงครามอัฟกานิสถาน**: พ.ศ. 2544-ปัจจุบัน (2001-ปัจจุบัน) - ความขัดแย้งที่ยืดเยื้อในอัฟกานิสถานทำให้มีผู้เสียชีวิตจากการสู้รบและการโจมตีทางอากาศอย่างต่อเนื่อง [BBC - War in Afghanistan](https://www.bbc.com/news/world-south-asia-11451718)
10. **แผ่นดินไหวและสึนามิในมหาสมุทรอินเดีย**: พ.ศ. 2547 (2004) - คร่าชีวิตผู้คนกว่า 230,000 คนในหลายประเทศ [Tsunami Report](https://www.britannica.com/event/Indian-Ocean-tsunami-of-2004)
11. **แผ่นดินไหวในปากีสถาน**: พ.ศ. 2548 (2005) - แผ่นดินไหวขนาดใหญ่ทำให้มีผู้เสียชีวิตประมาณ 80,000 คนในปากีสถาน [2005 Pakistan Earthquake](https://www.britannica.com/event/Kashmir-earthquake-of-2005)
12. **สงครามอิรัก**: พ.ศ. 2546-2554 (2003-2011) - สงครามและความขัดแย้งในอิรัก ส่งผลให้มีการเสียชีวิตเป็นจำนวนมาก [Iraq War](https://www.britannica.com/event/Iraq-War)
13. **ภัยพิบัติไซโคลนนาร์กีสในพม่า**: พ.ศ. 2551 (2008) - พายุไซโคลนส่งผลให้มีผู้เสียชีวิตกว่า 130,000 คนในพม่า [Cyclone Nargis](https://reliefweb.int/report/myanmar/myanmar-cyclone-nargis-2008-facts-and-figures#:~:text=Facts%20and%20figures%20On%202%20May%202008%2C%20Cyclone,37%20townships%20were%20significantly%20affected%20by%20the%20cyclone.)
14. **ไข้หวัดใหญ่ H1N1**: พ.ศ. 2552 (2009) - การแพร่ระบาดของไวรัส H1N1 ส่งผลให้มีผู้เสียชีวิตทั่วโลก [H1N1 Pandemic](https://www.britannica.com/event/influenza-pandemic-H1N1-of-2009/Pandemic-status-and-response)
15. **การแพร่ระบาดของโรค SARS**: พ.ศ. 2545-2546 (2002-2003) - ไวรัส SARS ส่งผลให้มีผู้เสียชีวิตหลายร้อยคนทั่วโลก [WHO - SARS](https://www.who.int/health-topics/severe-acute-respiratory-syndrome#tab=tab_1)
16. **สงครามกลางเมืองในซีเรีย**: พ.ศ. 2554-ปัจจุบัน (2011-ปัจจุบัน) - ความขัดแย้งในซีเรียทำให้มีผู้เสียชีวิตเป็นจำนวนมาก [UNHCR - Syrian Refugee Crisis](https://www.unhcr.org/syria-emergency.html)
17. **พายุเฮอริเคนแคทรีนา**: พ.ศ. 2548 (2005) - พายุเฮอริเคนที่ทำลายล้างบริเวณสหรัฐอเมริกา ส่งผลให้มีการเสียชีวิตและความเสียหายอย่างมาก[Hurricane Katrina](https://www.britannica.com/event/Hurricane-Katrina#:~:text=Hurricane%20Katrina%2C%20tropical%20cyclone%20that%20struck%20the%20southeastern,percent%20between%20the%20fall%20of%202005%20and%202011.) 
18. **ไฟป่าในรัสเซีย**: พ.ศ. 2553 (2010) - ไฟป่าและคลื่นความร้อนที่ตามมาส่งผลให้มีผู้เสียชีวิตจำนวนมากจากปัญหาทางเดินหายใจ [Russia Wildfires](https://reliefweb.int/disaster/wf-2010-000147-rus#:~:text=Unusual%20and%20long%20heat%20waves%20with%20temperatures%20peaking,of%20land%20and%20killing%20more%20than%2050%20people.)
19. **แผ่นดินไหวในไฮติ**: พ.ศ. 2553 (2010) - หนึ่งในเหตุการณ์แผ่นดินไหวที่ทำลายล้างมากที่สุด ส่งผลให้มีผู้เสียชีวิตกว่า 200,000 คน [Haiti Earthquake](https://www.britannica.com/event/2010-Haiti-earthquake)
20. **การระบาดของโรคไข้เลือดออกในภูมิภาคเอเชียตะวันออกเฉียงใต้**: พ.ศ. 2553-2562 (2010-2019) - ส่งผลให้มีผู้เสียชีวิตจำนวนมาก โดยเฉพาะในฟิลิปปินส์และเวียดนาม [Dengue](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9848297/)
21. **ความอดอยากในแอฟริกา**: โดยเฉพาะในโซมาเลีย พ.ศ. 2554 (2011) - ส่งผลให้มีผู้เสียชีวิตหลายหมื่นคนเนื่องจากการขาดแคลนอาหารอย่างรุนแรง[Somalia Famine](https://charityandsecurity.org/humanitarian-safeguards/somalia-2011-famine-and-its-response/#:~:text=The%202011%20Famine%20Following%20months%20of%20drought%2C%20rising,Lower%20Shabelle%2C%20were%20experiencing%20famine%20in%20July%202011.) 
22. **คลื่นความร้อนในยุโรป**: พ.ศ. 2556 (2013) - คลื่นความร้อนทำให้มีผู้เสียชีวิตจากโรคที่เกี่ยวกับอุณหภูมิสูง โดยเฉพาะในฝรั่งเศสและเยอรมนี [Heatwaves](https://academic.oup.com/eurpub/article/16/6/592/587672)
23. **การแพร่ระบาดของโรค Ebola**: พ.ศ. 2557-2559 (2014-2016) - การระบาดครั้งใหญ่ในแอฟริกาตะวันตก ส่งผลให้มีผู้เสียชีวิตนับหมื่นคน [Ebola](https://www.sciencedirect.com/science/article/pii/S1876034120304275)
24. **แผ่นดินไหวในเนปาล**: พ.ศ. 2558 (2015) - แผ่นดินไหวครั้งใหญ่ที่ทำให้มีผู้เสียชีวิตกว่า 9,000 คน [Nepal Earthquake](https://www.britannica.com/topic/Nepal-earthquake-of-2015)
25. **การแพร่ระบาดของโรคไข้เลือดออก**: ตลอดทศวรรษ 2010 - การระบาดของไข้เลือดออกในภูมิภาคเอเชียและอเมริกาใต้ ทำให้มีผู้เสียชีวิตจำนวนมาก[WHO - Dengue](https://www.who.int/news-room/fact-sheets/detail/dengue-and-severe-dengue)
   
##
เหตุการณ์ที่ทำให้มีผู้เสียชีวิตลดลง

1. **การรณรงค์เรื่องการป้องกัน HIV/AIDS**: พ.ศ. 2533-2542 (1990-1999) - การรณรงค์ใช้ถุงยางอนามัยและการตรวจเช็คสุขภาพอย่างสม่ำเสมอ รวมถึงการพัฒนายาต้านไวรัส ช่วยลดอัตราการเสียชีวิตจากโรคเอดส์ในประเทศพัฒนาแล้วและในบางประเทศในแอฟริกาและเอเชีย [HIV/AIDS](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8363183/)
2. **การขยายการฉีดวัคซีนในเด็ก**: ทศวรรษ 1990 - การฉีดวัคซีนป้องกันโรคหัด โปลิโอ และโรคปอดบวมอย่างแพร่หลายทั่วโลก ส่งผลให้อัตราการเสียชีวิตในเด็กจากโรคติดเชื้อลดลงอย่างมีนัยสำคัญ [Immunization](https://publications.aap.org/pediatrics/article/150/3/e2021056013/188495/Impact-of-Routine-Childhood-Immunization-in?autologincheck=redirected)
3. **การเข้าถึงยาต้านไวรัสสำหรับโรค HIV/AIDS**: พ.ศ. 2543-2552 (2000-2009) - ประเทศต่างๆ เริ่มเข้าถึงยาต้านไวรัสในวงกว้าง โดยเฉพาะในแอฟริกา ทำให้อัตราการเสียชีวิตจากโรคนี้ลดลง [HIV Update](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3078828/)
4. **การพัฒนาวัคซีนโรคมาลาเรีย**: พ.ศ. 2543-2552 (2000-2009) - การใช้มุ้งและยาฆ่ายุง รวมถึงการเข้าถึงยารักษามาลาเรีย ช่วยลดการเสียชีวิตจากโรคนี้ในภูมิภาคแอฟริกา [WHO Malaria Report](https://www.who.int/news-room/fact-sheets/detail/malaria)
5. **การใช้ยากันเลือดแข็งตัวและการรักษาหลอดเลือดหัวใจตีบ**: พ.ศ. 2543-2552 (2000-2009) - เทคโนโลยีทางการแพทย์และการรักษาโรคหัวใจและหลอดเลือดก้าวหน้าขึ้น ลดการเสียชีวิตจากโรคหัวใจและหลอดเลือดในหลายประเทศ [Cardiovascular](https://pubmed.ncbi.nlm.nih.gov/19571765/)
6. **การใช้ยาและวัคซีนป้องกันไข้หวัดใหญ่**: พ.ศ. 2543-2552 (2000-2009) - วัคซีนไข้หวัดใหญ่และการเข้าถึงยาต้านไวรัส ทำให้การระบาดของไข้หวัดใหญ่สามารถควบคุมได้ดีขึ้น และลดการเสียชีวิตจากโรคนี้ [Flu](https://pubmed.ncbi.nlm.nih.gov/20718130/)
7. **การรณรงค์ป้องกันการสูบบุหรี่**: พ.ศ. 2553-2562 (2010-2019) - หลายประเทศเริ่มดำเนินการนโยบายต่อต้านการสูบบุหรี่ ซึ่งช่วยลดการเสียชีวิตจากโรคที่เกี่ยวข้องกับปอด เช่น มะเร็งปอด และโรคปอดอุดกั้นเรื้อรัง[WHO - Tobacco](https://www.who.int/campaigns/world-no-tobacco-day/world-no-tobacco-day-2019/about-the-campaign) 
8. **การเข้าถึงยารักษาโรคมะเร็งที่ดีขึ้น**: พ.ศ. 2553-2562 (2010-2019) - ยาเคมีบำบัดและการรักษาด้วยเทคโนโลยีใหม่ช่วยลดการเสียชีวิตจากโรคมะเร็งในประเทศพัฒนาแล้ว [Cancer Treatments](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8366192/)
9. **การรณรงค์เรื่องความปลอดภัยทางจราจร**: พ.ศ. 2553-2562 (2010-2019) - การรณรงค์ใช้เข็มขัดนิรภัย หมวกกันน็อค และกฎหมายจำกัดความเร็วในหลายประเทศช่วยลดการเสียชีวิตจากอุบัติเหตุทางถนน[Road Safety](https://www.sciencedirect.com/science/article/pii/S0386111211000045)
10. **การพัฒนาวัคซีน HPV**: พ.ศ. 2550-2552 (2007-2009) - การฉีดวัคซีนป้องกันไวรัส HPV ที่เป็นสาเหตุของมะเร็งปากมดลูก ช่วยลดอัตราการเสียชีวิตจากมะเร็งปากมดลูกในหลายประเทศ[HPV](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8828558/) 
11. **การเข้าถึงน้ำดื่มที่สะอาด**: ทศวรรษ 2000-2010 - โครงการด้านน้ำดื่มสะอาดและสุขาภิบาลในหลายประเทศ โดยเฉพาะในแอฟริกาและเอเชีย ส่งผลให้อัตราการเสียชีวิตจากโรคติดต่อที่เกิดจากน้ำ เช่น โรคท้องร่วง ลดลงอย่างมาก
- [INDIA Water Portal](https://www.indiawaterportal.org/health-and-sanitation/sanitation/2010-unwater-global-annual-assessment-sanitation-and-drinkingwater-glaas)
- [Our World in Data](https://ourworldindata.org/diarrheal-diseases)


##
เหตุการณ์ในประเทศไทย 

เหตุการณ์ที่ทำให้มีอัตราการเสียชีวิตเพิ่มขึ้น: 

1. **การระบาดของ HIV/AIDS (1990s - ต้น 2000s)** ประเทศไทยได้รับผลกระทบอย่างมากจากวิกฤต HIV/AIDS ในช่วงทศวรรษ 1990 ก่อนที่การเข้าถึงยาต้านไวรัสจะเริ่มลดจำนวนผู้เสียชีวิตลงในทศวรรษต่อมา [UNAIDS - Thailand](https://www.unaids.org/en/regionscountries/countries/thailand)
2. **สึนามิในมหาสมุทรอินเดีย (2004)** สึนามิที่กระทบภาคใต้ของประเทศไทยในปี 2004 ทำให้มีผู้เสียชีวิตประมาณ 5,400 ราย [Tsunami Report](https://www.britannica.com/event/Indian-Ocean-tsunami-of-2004) 
3. **น้ำท่วมใหญ่ในประเทศไทย (2011)** น้ำท่วมครั้งใหญ่ในภาคกลางและภาคเหนือของประเทศไทยส่งผลให้มีผู้เสียชีวิตหลายร้อยคน[Thailand Floods](https://www.thaiwater.net/uploads/contents/current/2011/flood54Eng.html)

เหตุการณ์ที่ทำให้อัตราการเสียชีวิตลดลง: 

1. **โครงการหลักประกันสุขภาพถ้วนหน้า (2002)** การแนะนำโครงการหลักประกันสุขภาพถ้วนหน้าในปี 2002 ทำให้ประชาชนเข้าถึงบริการสุขภาพได้มากขึ้น ส่งผลให้อัตราการเสียชีวิตลดลงจากโรคที่ป้องกันและรักษาได้ [Thailand UHC](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6560367/)
2. **การลดอัตราการเสียชีวิตของมารดาและทารก (2000s)** โครงการด้านสุขภาพของมารดาและทารกมีการลงทุนเพิ่มขึ้น ทำให้อัตราการเสียชีวิตลดลง[WHO - Thailand UHC](https://www.who.int/news/item/09-05-2023-global-progress-in-tackling-maternal-and-newborn-deaths-stalls-since-2015--un)
3. **การลดการเสียชีวิตจากมาลาเรีย (2000s)** การรณรงค์ป้องกันมาลาเรียโดยเฉพาะในพื้นที่ชายแดน ช่วยลดการเสียชีวิตจากโรคมาลาเรียได้อย่างมาก [Malaria in Thailand](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6553898/)
4. **การพัฒนาวิธีการรักษาและการป้องกันโรคหัวใจและหลอดเลือด (1990s)** ทำให้อัตราการเสียชีวิตจากโรคเหล่านี้ลดลง [WHO - Cardiovascular Diseases](https://www.who.int/health-topics/cardiovascular-diseases)
5. **การรณรงค์ต่อต้านการสูบบุหรี่ (2000s)** การรณรงค์ต่อต้านการสูบบุหรี่และการออกกฎหมายควบคุมการสูบบุหรี่มีส่วนช่วยลดการเสียชีวิตที่เกี่ยวข้องกับการสูบบุหรี่

<b>Make time line for the Event during 1990 - 2019</b>


```python
import plotly.express as px
import pandas as pd

# ตัวอย่างข้อมูลเหตุการณ์
events = [
    {"event": "HIV/AIDS Epidemic", "start": 1990, "end": 2005, "category": "Increase"},
    {"event": "Malaria Outbreak in Africa", "start": 1990, "end": 2000, "category": "Increase"},
    {"event": "Yugoslav Wars", "start": 1991, "end": 2001, "category": "Increase"},
    {"event": "Rwandan Genocide", "start": 1994, "end": 1994, "category": "Increase"},
    {"event": "Food Shortage in North Korea", "start": 1994, "end": 1998, "category": "Increase"},
    {"event": "Kobe Earthquake, Japan", "start": 1995, "end": 1995, "category": "Increase"},
    {"event": "Sierra Leone Civil War", "start": 1991, "end": 2002, "category": "Increase"},
    {"event": "Tuberculosis (TB) Resurgence", "start": 1990, "end": 1999, "category": "Increase"},
    {"event": "War in Afghanistan", "start": 2001, "end": 2023, "category": "Increase"},
    {"event": "Indian Ocean Earthquake and Tsunami", "start": 2004, "end": 2004, "category": "Increase"},
    {"event": "Pakistan Earthquake", "start": 2005, "end": 2005, "category": "Increase"},
    {"event": "Iraq War", "start": 2003, "end": 2011, "category": "Increase"},
    {"event": "Cyclone Nargis in Myanmar", "start": 2008, "end": 2008, "category": "Increase"},
    {"event": "H1N1 Influenza", "start": 2009, "end": 2009, "category": "Increase"},
    {"event": "SARS Epidemic", "start": 2002, "end": 2003, "category": "Increase"},
    {"event": "Syrian Civil War", "start": 2011, "end": 2023, "category": "Increase"},
    {"event": "Hurricane Katrina", "start": 2005, "end": 2005, "category": "Increase"},
    {"event": "Wildfires in Russia", "start": 2010, "end": 2010, "category": "Increase"},
    {"event": "Haiti Earthquake", "start": 2010, "end": 2010, "category": "Increase"},
    {"event": "Dengue Fever Outbreak in Southeast Asia", "start": 2010, "end": 2019, "category": "Increase"},
    {"event": "Famine in Africa", "start": 2011, "end": 2011, "category": "Increase"},
    {"event": "Heatwave in Europe", "start": 2013, "end": 2013, "category": "Increase"},
    {"event": "Ebola Outbreak", "start": 2014, "end": 2016, "category": "Increase"},
    {"event": "Nepal Earthquake", "start": 2015, "end": 2015, "category": "Increase"},
    {"event": "Dengue Fever Epidemic", "start": 2010, "end": 2019, "category": "Increase"},
    {"event": "HIV/AIDS Prevention Campaign", "start": 1990, "end": 1999, "category": "Decrease"},
    {"event": "Expansion of Childhood Vaccination", "start": 1990, "end": 1999, "category": "Decrease"},
    {"event": "Access to Antiretroviral Drugs for HIV/AIDS", "start": 2000, "end": 2009, "category": "Decrease"},
    {"event": "Development of Malaria Vaccines", "start": 2000, "end": 2009, "category": "Decrease"},
    {"event": "Use of Anticoagulants and Treatments for Cardiovascular Diseases", "start": 2000, "end": 2009, "category": "Decrease"},
    {"event": "Use of Influenza Vaccines and Antiviral Medications", "start": 2000, "end": 2009, "category": "Decrease"},
    {"event": "Anti-Smoking Campaigns", "start": 2010, "end": 2019, "category": "Decrease"},
    {"event": "Improved Access to Cancer Treatments", "start": 2010, "end": 2019, "category": "Decrease"},
    {"event": "Traffic Safety Campaigns", "start": 2010, "end": 2019, "category": "Decrease"},
    {"event": "Development of HPV Vaccines", "start": 2007, "end": 2009, "category": "Decrease"},
    {"event": "Access to Clean Drinking Water", "start": 2000, "end": 2010, "category": "Decrease"},
    {"event": "HIV/AIDS Epidemic in Thailand", "start": 1990, "end": 2000, "category": "Increase"},
    {"event": "Indian Ocean Tsunami in Thailand", "start": 2004, "end": 2004, "category": "Increase"},
    {"event": "Severe Flooding in Thailand", "start": 2011, "end": 2011, "category": "Increase"},
    {"event": "Universal Health Coverage Scheme in Thailand", "start": 2002, "end": 2023, "category": "Decrease"},
    {"event": "Reduction in Maternal and Infant Mortality Rates in Thailand", "start": 2000, "end": 2009, "category": "Decrease"},
    {"event": "Decrease in Malaria Deaths in Thailand", "start": 2000, "end": 2009, "category": "Decrease"},
    {"event": "Advances in Treatment and Prevention of Cardiovascular Diseases in Thailand", "start": 1990, "end": 2000, "category": "Decrease"}
]

# สร้าง DataFrame
df = pd.DataFrame(events)

# แปลงวันที่เป็น datetime objects
df["start"] = pd.to_datetime(df["start"], format="%Y")
df["end"] = pd.to_datetime(df["end"], format="%Y")

# สร้าง DataFrame แยกสำหรับเหตุการณ์ที่เพิ่มขึ้นและลดลง
df_increase = df[df["category"] == "Increase"]
df_decrease = df[df["category"] == "Decrease"]

# แยกกราฟเหตุการณ์ที่เพิ่มขึ้น
df_increase_single_year = df_increase[df_increase["start"] == df_increase["end"]]
df_increase_multi_year = df_increase[df_increase["start"] != df_increase["end"]]

# สร้างกราฟระยะเวลาสำหรับเหตุการณ์ที่เพิ่มขึ้น (ปีเดียว) พร้อมสีแดง
fig_increase_single_year = px.timeline(
    df_increase_single_year,
    x_start="start",
    x_end="end",
    y="event",
    title="Timeline of Single-Year Events Increasing Mortality (1990-2023)",
    color_discrete_sequence=["red"]  # กำหนดสีเป็นสีแดง
)

# สร้างกราฟระยะเวลาสำหรับเหตุการณ์ที่เพิ่มขึ้น (หลายปี) พร้อมสีแดง
fig_increase_multi_year = px.timeline(
    df_increase_multi_year,
    x_start="start",
    x_end="end",
    y="event",
    title="Timeline of Multi-Year Events Increasing Mortality (1990-2023)",
    color_discrete_sequence=["red"]  # กำหนดสีเป็นสีแดง
)

# สร้างกราฟระยะเวลาสำหรับเหตุการณ์ที่ลดลง พร้อมสีเขียว
fig_decrease = px.timeline(
    df_decrease,
    x_start="start",
    x_end="end",
    y="event",
    title="Timeline of Events Decreasing Mortality (1990-2023)",
    color_discrete_sequence=["#0000FF"]  # กำหนดสีเป็นสีเขียว
)

# จัดเรียงเหตุการณ์ตามเวลา
fig_increase_single_year.update_yaxes(categoryorder="total ascending")
fig_increase_multi_year.update_yaxes(categoryorder="total ascending")
fig_decrease.update_yaxes(categoryorder="total ascending")

# ตั้งค่า x-axis ให้ครอบคลุมเหตุการณ์ทั้งหมด
fig_increase_single_year.update_layout(xaxis_range=[df["start"].min(), df["end"].max()])
fig_increase_multi_year.update_layout(xaxis_range=[df["start"].min(), df["end"].max()])
fig_decrease.update_layout(xaxis_range=[df["start"].min(), df["end"].max()])

# เพิ่ม categoryarray เพื่อให้แสดงทุกเหตุการณ์ในแกน Y
fig_increase_single_year.update_yaxes(categoryarray=df_increase_single_year['event'])
fig_increase_multi_year.update_yaxes(categoryarray=df_increase_multi_year['event'])
fig_decrease.update_yaxes(categoryarray=df_decrease['event'])

# เพิ่มจุดปีลงไปในกราฟ
for index, row in df_increase_single_year.iterrows():
    fig_increase_single_year.add_annotation(
        x=row["start"],
        y=row["event"],
        text=str(row["start"].year),
        showarrow=True,
        arrowhead=2,
        ax=0,
        ay=-40,
        font=dict(size=10),
        bgcolor="white",
        bordercolor="black",
        borderwidth=1,
        borderpad=4,
    )


# เพิ่ม grid แนวนอน
fig_increase_single_year.update_yaxes(showgrid=True)

# แสดงกราฟ
fig_increase_single_year.show()
fig_increase_multi_year.show()
fig_decrease.show()

```

![png](Markdown/Event_Analysis_files/Event_Duration_1990-2023_Single.png)

![png](Markdown/Event_Analysis_files/Event_Duration_1990-2023_Multi.png)

![png](Markdown/Event_Analysis_files/Event_Decrease_1990_2023.png)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Event for analyze

ในช่วงระยะเวลาที่ผ่านมา ประวัติศาสตร์โลกได้ผ่านพ้นเหตุการณ์ที่สำคัญมากมาย ซึ่งไม่เพียงแต่ส่งผลกระทบต่อชีวิตและความเป็นอยู่ของประชาชนในพื้นที่ที่เกิดเหตุการณ์เท่านั้น แต่ยังมีผลกระทบต่อสุขภาพของประชากรโลกในวงกว้าง โดยเฉพาะอย่างยิ่งเหตุการณ์ที่เกิดขึ้นระหว่างปี 1990-2010 เช่น การระบาดของโรค HIV/AIDS, การฆ่าล้างเผ่าพันธุ์ในรวันดา, และภัยพิบัติจากแผ่นดินไหวและสึนามิในเอเชีย

เหตุการณ์เหล่านี้ถูกเลือกเพื่อการวิเคราะห์เนื่องจากความสัมพันธ์ที่ชัดเจนกับอัตราการเสียชีวิต รวมถึงการดำเนินการแก้ไขปัญหาที่ส่งผลต่อการพัฒนาในด้านสุขภาพและคุณภาพชีวิตของประชาชน เช่น การเข้าถึงยาต้านไวรัส HIV/AIDS, การพัฒนาวัคซีนมาลาเรีย, และความพยายามในการจัดการน้ำดื่มที่สะอาด ซึ่งล้วนแต่มีผลกระทบที่สำคัญต่อการลดอัตราการเสียชีวิตจากโรคที่สามารถป้องกันได้

การเลือกเหตุการณ์เหล่านี้ช่วยให้เราเข้าใจถึงความซับซ้อนของการพัฒนาในด้านสุขภาพโลก และวิธีการที่เหตุการณ์แต่ละอย่างมีผลต่อกันในบริบทที่กว้างขึ้น โดยการวิเคราะห์ความสัมพันธ์ระหว่างเหตุการณ์เหล่านี้และการเปลี่ยนแปลงในอัตราการเสียชีวิต เราจะสามารถให้ข้อมูลเชิงลึกที่มีคุณค่าและเป็นประโยชน์ในการพัฒนานโยบายและกลยุทธ์เพื่อสุขภาพในอนาคต

**Events That Increased Mortality Rates**

1. **HIV/AIDS Pandemic (1990s - early 2000s)**  
   - Increased mortality globally, especially in Sub-Saharan Africa.  
   - [WHO HIV Statistics](https://www.who.int/health-topics/hiv-aids#tab=tab_1)
   
2. **Rwandan Genocide (1994)**  
   - Over 800,000 people were killed in just a few months due to ethnic violence.  
   - [UN Report on Rwanda](https://www.un.org/en/preventgenocide/rwanda)

2. **Asian Tsunami (2004)**  
   - Affected Southeast Asia, causing over 230,000 deaths.  
   - [NOAA Tsunami Report](https://www.noaa.gov/news/15-years-after-deadly-tsunami-world-better-prepared-for-disasters)

**Events That Decreased Mortality Rates**

1. **Access to Antiretroviral Drugs for HIV/AIDS** (2000-2009)
   - Widespread access to antiretroviral therapy (ART) greatly reduced the death rate from HIV/AIDS.  
   - [UNAIDS HIV Update](https://www.unaids.org/en/resources/fact-sheet)

2. **Development of Malaria Vaccines** (2000-2009)
   - Use of insecticide-treated bed nets and anti-malaria programs led to a significant decline.  
   - [WHO Malaria Report](https://www.who.int/news-room/fact-sheets/detail/malaria)

3. **Access to Clean Drinking Water** (2000-2010)
   - Global initiatives to provide clean water reduced mortality from waterborne diseases like cholera, dysentery, and diarrhea..  
   - [INDIA Water Portal](https://www.indiawaterportal.org/health-and-sanitation/sanitation/2010-unwater-global-annual-assessment-sanitation-and-drinkingwater-glaas)
   - [Our World in Data](https://ourworldindata.org/diarrheal-diseases)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### HIV


```python
# prompt: plot graph HIV by year for continent

# Assuming 'df_Main_data' is your DataFrame containing the HIV data
# and it has columns like 'Year', 'Continent', and 'HIV_Deaths'

# Group data by year and continent, summing HIV deaths
hiv_by_year_continent = df_Main_data.groupby(['Year', 'Continent'])['HIV'].sum().reset_index()

# Create the plot using Plotly Express
fig = px.line(hiv_by_year_continent, x='Year', y='HIV', color='Continent',
             title='HIV Deaths by Year and Continent')
fig.show()
```
![png](Markdown/Event_Analysis_files/HIV.png)



HIV นั้นถูกค้นพบครั้งแรกในช่วงปี 1980s และแพร่ระบาดไปทั่วโลก โดยเฉพาะอย่างยิ่ง ในแถบแอฟริกาตอนใต้ จากเหตุการณ์ดังกล่าวพบว่ากราฟในช่วงปี 1990s-2000s มีการเสียชีวิตจากโรค HIV เพิ่มขึ้น โดยเฉพาะในแถบแอฟริกา จึงทำให้ในช่วงปี 2000 - 2009 ได้มีการรณรงค์ให้ความรู้เกี่ยวกับการใช้ถุงยางอนามัยและการตรวจสุขภาพเป็นประจำช่วยลดอัตราการเสียชีวิตจากโรค HIV/AIDS ในหลายประเทศ โดยเฉพาะอย่างยิ่งในแถบแอฟริกา ซึ่งสอดคล้องกับกราฟสถิติการตายของโรค HIV ดังด้านบน

<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### Rwanda Genocide


```python
# prompt: plot graph conflict_and_terrorism of rwanda by year

# Filter for Rwanda
df_rwanda = df_Main_data[df_Main_data['Code'] == 'RWA']

# Group by year and sum conflict and terrorism deaths
df_rwanda_conflict = df_rwanda.groupby('Year')['Conflict_and_Terrorism'].sum().reset_index()

# Plot the graph
fig = px.line(df_rwanda_conflict, x='Year', y='Conflict_and_Terrorism',
             title='Conflict and Terrorism Deaths in Rwanda by Year')
fig.show()
```

![png](Markdown/Event_Analysis_files/Rwanda.png)


ในปี 1994 เกิดเหตุการณ์ฆ่าล้างเผ่าพันธุ์ซึ่งเกิดขึ้นจากความขัดแย้งทางชาติพันธุ์ระหว่างสองกลุ่มหลักในรวันดา เหตุการณ์นี้นำไปสู่การเสียชีวิตของประชาชนกว่า 800,000 คน ภายในระยะเวลาเพียง 100 วัน ส่งผลทำให้กราฟการเสียชีวิตจาก Conflict and Terrorism เพิ่มขึ้นอย่างมีนัยสำคัญในปี 1994 ดังกราฟข้างต้น

<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### Asian Tsunami


```python
# prompt: plot graph Exposure to forces of nature by year for asia

# Assuming 'df_Main_data' is your DataFrame containing the data
# and it has columns like 'Year', 'Continent', and 'Exposure_to_Forces_of_Nature'

# Filter for Asia
df_asia = df_Main_data[df_Main_data['Continent'] == 'Asia']

# Group data by year, summing Exposure_to_Forces_of_Nature
exposure_by_year_asia = df_asia.groupby(['Year'])['Exposure_to_Forces_of_Nature'].sum().reset_index()

# Create the plot using Plotly Express
fig = px.line(exposure_by_year_asia, x='Year', y='Exposure_to_Forces_of_Nature',
             title='Exposure to Forces of Nature by Year for Asia')
fig.show()
```


![png](Markdown/Event_Analysis_files/Asia_Tsunami.png)



```python
# prompt: plot graph Exposure to forces of nature top 10 country for year 2004

# Assuming df_Main_data is your DataFrame
df_2004 = df_Main_data[df_Main_data['Year'] == 2004]

# Sort by Exposure_to_Forces_of_Nature in descending order
top_10_2004 = df_2004.sort_values('Exposure_to_Forces_of_Nature', ascending=False).head(10)

# Create a bar plot
plt.figure(figsize=(12, 6))
plt.bar(top_10_2004['Country'], top_10_2004['Exposure_to_Forces_of_Nature'])
plt.xlabel('Country')
plt.ylabel('Exposure to Forces of Nature')
plt.title('Top 10 Countries with Highest Exposure to Forces of Nature in 2004')
plt.xticks(rotation=45, ha='right')
plt.tight_layout()
plt.show()
```


    
![png](Markdown/Event_Analysis_files/Event_Analysis_89_0.png)
    


ในวันที่ 26 ธันวาคม 2004 เกิดแผ่นดินไหวขนาด 9.1-9.3 แมกนิจูด นอกชายฝั่งของเกาะสุมาตรา ประเทศอินโดนีเซีย ทำให้เกิดคลื่นสึนามิขนาดใหญ่ที่ซัดเข้าถล่มชายฝั่งของหลายประเทศรอบมหาสมุทรอินเดีย ส่งผลให้มีผู้เสียชีวิตจำนวนมาก และสร้างความเสียหายทางทรัพย์สินอย่างมหาศาล เห็นได้ดังกราฟข้างต้น

<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### Malaria


```python
# prompt: plot graph Malaria by year for continent

# Assuming df_Main_data is your DataFrame
# and it has columns like 'Year', 'Continent', and 'Malaria_Deaths'

# Group data by year and continent, summing Malaria deaths
malaria_by_year_continent = df_Main_data.groupby(['Year', 'Continent'])['Malaria'].sum().reset_index()

# Create the plot using Plotly Express
fig = px.line(malaria_by_year_continent, x='Year', y='Malaria', color='Continent',
             title='Malaria Deaths by Year and Continent')
fig.show()
```
![png](Markdown/Event_Analysis_files/Malaria.png)


โรคมาลาเรียเป็นหนึ่งในโรคติดเชื้อที่ร้ายแรงที่สุดในโลก โดยเฉพาะในภูมิภาคเขตร้อนและกึ่งเขตร้อน ซึ่งแพร่เชื้อสู่มนุษย์ผ่านการกัดของยุงก้นปล่อง ช่วงปี 2000 - 2009 เป็นช่วงเวลาที่มีความก้าวหน้าอย่างมากในการพัฒนาวัคซีนมาลาเรีย แม้จะยังไม่สามารถป้องกันโรคได้อย่างสมบูรณ์ แต่การวิจัยและการทดสอบวัคซีน ก็ถือเป็นก้าวสำคัญที่ช่วยให้เกิดการพัฒนาในอนาคต เห็นได้จากกราฟข้างต้น ที่มีการลดลงของการเสียชีวิตของโรค Malaria ภายหลังช่วงปี 2009 เป็นต้นไป

<p align="right">(<a href="#readme-top">back to top</a>)</p>

#### Diarrheal


```python
# prompt: plot graph Diarrheal diseases by year for continent

# Assuming df_Main_data is your DataFrame
# and it has columns like 'Year', 'Continent', and 'Diarrheal_diseases_Deaths'

# Group data by year and continent, summing Diarrheal diseases deaths
diarrheal_by_year_continent = df_Main_data.groupby(['Year', 'Continent'])['Diarrheal_Diseases'].sum().reset_index()

# Create the plot using Plotly Express
fig = px.line(diarrheal_by_year_continent, x='Year', y='Diarrheal_Diseases', color='Continent',
             title='Diarrheal diseases Deaths by Year and Continent')
fig.show()
```

![png](Markdown/Event_Analysis_files/Diarrheal.png)


```python
# prompt: plot line graph top 5 country in Asia by year for Diarrheal Diseases

# Assuming df_Main_data is your DataFrame
# and it has columns like 'Year', 'Country', and 'Diarrheal_Diseases'

# Filter for Asia
df_asia = df_Main_data[df_Main_data['Continent'] == 'Asia']

# Group data by year and country, summing Diarrheal diseases deaths
diarrheal_by_year_country_asia = df_asia.groupby(['Year', 'Country'])['Diarrheal_Diseases'].sum().reset_index()

# Find top 5 countries in Asia by total Diarrheal diseases deaths across all years
top_5_countries = diarrheal_by_year_country_asia.groupby('Country')['Diarrheal_Diseases'].sum().nlargest(5).index.tolist()

# Filter data for the top 5 countries
df_top_5 = diarrheal_by_year_country_asia[diarrheal_by_year_country_asia['Country'].isin(top_5_countries)]

# Create the plot using Plotly Express
fig = px.line(df_top_5, x='Year', y='Diarrheal_Diseases', color='Country',
             title='Top 5 Countries in Asia by Diarrheal Diseases Deaths (1990-2019)')
fig.show()
```

![png](Markdown/Event_Analysis_files/TopContries_Diarrheal_Asia.png)


```python
# prompt: plot line graph top 5 country in Africa by year for Diarrheal Diseases

# Assuming df_Main_data is your DataFrame
# and it has columns like 'Year', 'Country', and 'Diarrheal_Diseases'

# Filter for Africa
df_africa = df_Main_data[df_Main_data['Continent'] == 'Africa']

# Group data by year and country, summing Diarrheal diseases deaths
diarrheal_by_year_country_africa = df_africa.groupby(['Year', 'Country'])['Diarrheal_Diseases'].sum().reset_index()

# Find top 5 countries in Africa by total Diarrheal diseases deaths across all years
top_5_countries = diarrheal_by_year_country_africa.groupby('Country')['Diarrheal_Diseases'].sum().nlargest(5).index.tolist()

# Filter data for the top 5 countries
df_top_5 = diarrheal_by_year_country_africa[diarrheal_by_year_country_africa['Country'].isin(top_5_countries)]

# Create the plot using Plotly Express
fig = px.line(df_top_5, x='Year', y='Diarrheal_Diseases', color='Country',
             title='Top 5 Countries in Africa by Diarrheal Diseases Deaths (1990-2019)')
fig.show()
```
![png](Markdown/Event_Analysis_files/TopContries_Diarrheal_Afarica.png)


โรคท้องร่วงเป็นหนึ่งในสาเหตุสำคัญของการเสียชีวิตของประชากรโลก เนื่องจากการขาดความเข้าถึงของน้ำสะอาดและการมีสุขาภิบาลที่ดี ในช่วงปี 2000-2010 จึงมีการริเริ่มโครงการระดับโลกที่มุ่งเน้นการเพิ่มการเข้าถึงน้ำดื่มที่สะอาดเพื่อลดการเสียชีวิตจากโรคที่เกี่ยวกับน้ำ ส่งผลให้การเสียชีวิตจากโรคท้องร่วงลดลงอย่างมีนัยสำคัญ ซึ่งเห็นได้ดังกราฟข้างต้น

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Summary
**สรุปภาพรวมการวิเคราะห์ข้อมูลการเสียชีวิตทั่วโลก (1990-2019)**

การวิเคราะห์ข้อมูลการเสียชีวิตในช่วงปี 1990-2019 แสดงให้เห็นถึงความสัมพันธ์ระหว่างอัตราการเสียชีวิตกับเหตุการณ์ต่าง ๆ เช่น การเข้าถึงน้ำดื่มสะอาดและการพัฒนาวัคซีนที่ช่วยลดอัตราการเสียชีวิตจากโรคต่าง ๆ ในภูมิภาคเอเชียตะวันออกเฉียงเหนือ การเปรียบเทียบอัตราการเสียชีวิตในประเทศเพื่อนบ้าน เช่น เมียนมาร์ ฟิลิปปินส์ และเวียดนาม ยังเผยให้เห็นแนวโน้มที่น่าสนใจ เช่น การลดลงของอัตราการเสียชีวิตในเมียนมาร์ ซึ่งข้อมูลเหล่านี้สามารถนำไปใช้ในการพัฒนากลยุทธ์เพื่อลดอัตราการเสียชีวิตจากโรคเรื้อรังในอนาคตได้อย่างมีประสิทธิภาพ

##

## Challenge

1. ข้อมูลที่มีแสดงให้เห็นถึงแนวโน้มการเปลี่ยนแปลง แต่การหาสาเหตุหรือปัจจัยที่ส่งผลต่อการเปลี่ยนแปลงนั้นจำเป็นต้องหาข้อมูลและข่าวสารเพิ่มเติมเพื่อสนับสนุนและอธิบายผลลัพธ์ให้ชัดเจนยิ่งขึ้น
2. ขั้นตอนการ Cleansing data และรวบรวมข้อมูลใช้เวลานาน เนื่องจากใช้ข้อมูลจากข้อมูลหลายชุด และต้องทำให้ข้อมูลสมบูรณ์พร้อมใช้งาน
3. การเลือกประเภทของกราฟที่เหมาะสมกับข้อมูลที่ต้องการนำเสนอเป็นสิ่งสำคัญ จึงเป็นเรื่องท้าทายในการเลือกให้ตรงกับข้อมูลที่มี
4. การทำนายแนวโน้มในอนาคตต้องอาศัยการศึกษาข้อมูลจากหลายด้าน ตัวอย่างเช่น การวิเคราะห์อัตราการตายจากโรคต้องอาศัยข้อมูลทางการแพทย์ ทำให้ต้องใช้เวลามากขึ้นในการเก็บรวบรวมข้อมูล
5. เนื่องจากข้อมูลมีความกว้างขวาง ทำให้เกิดไอเดียในการวิเคราะห์ที่หลากหลาย จึงเป็นเรื่องยากในการกำหนดขอบเขตการวิเคราะห์ที่ชัดเจน ซึ่งอาจทำให้กระบวนการทำงานใช้เวลานานขึ้น

<p align="right">(<a href="#readme-top">back to top</a>)</p>

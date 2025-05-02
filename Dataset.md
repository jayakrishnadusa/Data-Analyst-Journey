```python
import pandas as pd
```


```python
import seaborn as sns
```


```python
df=pd.read_csv('Dataset.csv')
```

    C:\Users\jayak\AppData\Local\Temp\ipykernel_17132\269941882.py:1: DtypeWarning: Columns (11) have mixed types. Specify dtype option on import or set low_memory=False.
      df=pd.read_csv('Dataset.csv')
    


```python
df.head(10)
```




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
      <th>Year of event</th>
      <th>Event dates</th>
      <th>Event name</th>
      <th>Event distance/length</th>
      <th>Event number of finishers</th>
      <th>Athlete performance</th>
      <th>Athlete club</th>
      <th>Athlete country</th>
      <th>Athlete year of birth</th>
      <th>Athlete gender</th>
      <th>Athlete age category</th>
      <th>Athlete average speed</th>
      <th>Athlete ID</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Selva Costera (CHI)</td>
      <td>50km</td>
      <td>22</td>
      <td>4:51:39 h</td>
      <td>Tnfrc</td>
      <td>CHI</td>
      <td>1978.0</td>
      <td>M</td>
      <td>M35</td>
      <td>10.286</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Selva Costera (CHI)</td>
      <td>50km</td>
      <td>22</td>
      <td>5:15:45 h</td>
      <td>Roberto Echeverría</td>
      <td>CHI</td>
      <td>1981.0</td>
      <td>M</td>
      <td>M35</td>
      <td>9.501</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Selva Costera (CHI)</td>
      <td>50km</td>
      <td>22</td>
      <td>5:16:44 h</td>
      <td>Puro Trail Osorno</td>
      <td>CHI</td>
      <td>1987.0</td>
      <td>M</td>
      <td>M23</td>
      <td>9.472</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Selva Costera (CHI)</td>
      <td>50km</td>
      <td>22</td>
      <td>5:34:13 h</td>
      <td>Columbia</td>
      <td>ARG</td>
      <td>1976.0</td>
      <td>M</td>
      <td>M40</td>
      <td>8.976</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Selva Costera (CHI)</td>
      <td>50km</td>
      <td>22</td>
      <td>5:54:14 h</td>
      <td>Baguales Trail</td>
      <td>CHI</td>
      <td>1992.0</td>
      <td>M</td>
      <td>M23</td>
      <td>8.469</td>
      <td>4</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Selva Costera (CHI)</td>
      <td>50km</td>
      <td>22</td>
      <td>6:25:01 h</td>
      <td>NaN</td>
      <td>ARG</td>
      <td>1974.0</td>
      <td>M</td>
      <td>M40</td>
      <td>7.792</td>
      <td>5</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Selva Costera (CHI)</td>
      <td>50km</td>
      <td>22</td>
      <td>6:28:00 h</td>
      <td>Los Patagones</td>
      <td>ARG</td>
      <td>1979.0</td>
      <td>F</td>
      <td>W35</td>
      <td>7.732</td>
      <td>6</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Selva Costera (CHI)</td>
      <td>50km</td>
      <td>22</td>
      <td>6:32:24 h</td>
      <td>Reaktiva Chile</td>
      <td>CHI</td>
      <td>1967.0</td>
      <td>F</td>
      <td>W50</td>
      <td>7.645</td>
      <td>7</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Selva Costera (CHI)</td>
      <td>50km</td>
      <td>22</td>
      <td>6:39:08 h</td>
      <td>Puro Trail Osorno</td>
      <td>CHI</td>
      <td>1985.0</td>
      <td>M</td>
      <td>M23</td>
      <td>7.516</td>
      <td>8</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Selva Costera (CHI)</td>
      <td>50km</td>
      <td>22</td>
      <td>6:45:11 h</td>
      <td>Marlene Flores Team</td>
      <td>CHI</td>
      <td>1976.0</td>
      <td>M</td>
      <td>M40</td>
      <td>7.404</td>
      <td>9</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.shape
```




    (7461195, 13)




```python
df.dtypes
```




    Year of event                  int64
    Event dates                   object
    Event name                    object
    Event distance/length         object
    Event number of finishers      int64
    Athlete performance           object
    Athlete club                  object
    Athlete country               object
    Athlete year of birth        float64
    Athlete gender                object
    Athlete age category          object
    Athlete average speed         object
    Athlete ID                     int64
    dtype: object




```python
#Only want USA races 50k or 50 miles
50k
50mi
```


```python
df[df['Event distance/length']=='50mi']
```




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
      <th>Year of event</th>
      <th>Event dates</th>
      <th>Event name</th>
      <th>Event distance/length</th>
      <th>Event number of finishers</th>
      <th>Athlete performance</th>
      <th>Athlete club</th>
      <th>Athlete country</th>
      <th>Athlete year of birth</th>
      <th>Athlete gender</th>
      <th>Athlete age category</th>
      <th>Athlete average speed</th>
      <th>Athlete ID</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>55</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Yankee Springs 50 Mile Winter Challenge (USA)</td>
      <td>50mi</td>
      <td>9</td>
      <td>9:53:05 h</td>
      <td>*Middleville, MI</td>
      <td>USA</td>
      <td>1983.0</td>
      <td>M</td>
      <td>M23</td>
      <td>8.141</td>
      <td>55</td>
    </tr>
    <tr>
      <th>56</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Yankee Springs 50 Mile Winter Challenge (USA)</td>
      <td>50mi</td>
      <td>9</td>
      <td>11:09:35 h</td>
      <td>*Waterloo, ON</td>
      <td>CAN</td>
      <td>1977.0</td>
      <td>F</td>
      <td>W40</td>
      <td>7.211</td>
      <td>56</td>
    </tr>
    <tr>
      <th>57</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Yankee Springs 50 Mile Winter Challenge (USA)</td>
      <td>50mi</td>
      <td>9</td>
      <td>11:33:00 h</td>
      <td>*Kitchener, ON</td>
      <td>CAN</td>
      <td>1976.0</td>
      <td>M</td>
      <td>M40</td>
      <td>6.967</td>
      <td>57</td>
    </tr>
    <tr>
      <th>58</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Yankee Springs 50 Mile Winter Challenge (USA)</td>
      <td>50mi</td>
      <td>9</td>
      <td>11:38:17 h</td>
      <td>*Utica, MI</td>
      <td>USA</td>
      <td>1986.0</td>
      <td>M</td>
      <td>M23</td>
      <td>6.914</td>
      <td>58</td>
    </tr>
    <tr>
      <th>59</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Yankee Springs 50 Mile Winter Challenge (USA)</td>
      <td>50mi</td>
      <td>9</td>
      <td>11:56:35 h</td>
      <td>*Grass Lake, MI</td>
      <td>USA</td>
      <td>1988.0</td>
      <td>M</td>
      <td>M23</td>
      <td>6.738</td>
      <td>59</td>
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
    </tr>
    <tr>
      <th>7461181</th>
      <td>1995</td>
      <td>07.01.1995</td>
      <td>Avalon Benefit 50-Mile Run (USA)</td>
      <td>50mi</td>
      <td>92</td>
      <td>11:59:37 h</td>
      <td>NaN</td>
      <td>USA</td>
      <td>1941.0</td>
      <td>M</td>
      <td>M50</td>
      <td>6709.0</td>
      <td>1045603</td>
    </tr>
    <tr>
      <th>7461182</th>
      <td>1995</td>
      <td>07.01.1995</td>
      <td>Avalon Benefit 50-Mile Run (USA)</td>
      <td>50mi</td>
      <td>92</td>
      <td>12:01:41 h</td>
      <td>NaN</td>
      <td>USA</td>
      <td>1932.0</td>
      <td>M</td>
      <td>M60</td>
      <td>6690.0</td>
      <td>1070463</td>
    </tr>
    <tr>
      <th>7461183</th>
      <td>1995</td>
      <td>07.01.1995</td>
      <td>Avalon Benefit 50-Mile Run (USA)</td>
      <td>50mi</td>
      <td>92</td>
      <td>12:03:26 h</td>
      <td>NaN</td>
      <td>USA</td>
      <td>1934.0</td>
      <td>F</td>
      <td>W60</td>
      <td>6674.0</td>
      <td>416139</td>
    </tr>
    <tr>
      <th>7461184</th>
      <td>1995</td>
      <td>07.01.1995</td>
      <td>Avalon Benefit 50-Mile Run (USA)</td>
      <td>50mi</td>
      <td>92</td>
      <td>12:03:26 h</td>
      <td>NaN</td>
      <td>USA</td>
      <td>1951.0</td>
      <td>F</td>
      <td>W40</td>
      <td>6674.0</td>
      <td>1098098</td>
    </tr>
    <tr>
      <th>7461185</th>
      <td>1995</td>
      <td>07.01.1995</td>
      <td>Avalon Benefit 50-Mile Run (USA)</td>
      <td>50mi</td>
      <td>92</td>
      <td>12:05:59 h</td>
      <td>NaN</td>
      <td>USA</td>
      <td>1947.0</td>
      <td>F</td>
      <td>W45</td>
      <td>6650.0</td>
      <td>1626367</td>
    </tr>
  </tbody>
</table>
<p>352181 rows × 13 columns</p>
</div>




```python
#combine 50k and 50 mi using isin
```


```python
df[df['Event distance/length'].isin(['50km','50mi'])]
```




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
      <th>Year of event</th>
      <th>Event dates</th>
      <th>Event name</th>
      <th>Event distance/length</th>
      <th>Event number of finishers</th>
      <th>Athlete performance</th>
      <th>Athlete club</th>
      <th>Athlete country</th>
      <th>Athlete year of birth</th>
      <th>Athlete gender</th>
      <th>Athlete age category</th>
      <th>Athlete average speed</th>
      <th>Athlete ID</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Selva Costera (CHI)</td>
      <td>50km</td>
      <td>22</td>
      <td>4:51:39 h</td>
      <td>Tnfrc</td>
      <td>CHI</td>
      <td>1978.0</td>
      <td>M</td>
      <td>M35</td>
      <td>10.286</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Selva Costera (CHI)</td>
      <td>50km</td>
      <td>22</td>
      <td>5:15:45 h</td>
      <td>Roberto Echeverría</td>
      <td>CHI</td>
      <td>1981.0</td>
      <td>M</td>
      <td>M35</td>
      <td>9.501</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Selva Costera (CHI)</td>
      <td>50km</td>
      <td>22</td>
      <td>5:16:44 h</td>
      <td>Puro Trail Osorno</td>
      <td>CHI</td>
      <td>1987.0</td>
      <td>M</td>
      <td>M23</td>
      <td>9.472</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Selva Costera (CHI)</td>
      <td>50km</td>
      <td>22</td>
      <td>5:34:13 h</td>
      <td>Columbia</td>
      <td>ARG</td>
      <td>1976.0</td>
      <td>M</td>
      <td>M40</td>
      <td>8.976</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Selva Costera (CHI)</td>
      <td>50km</td>
      <td>22</td>
      <td>5:54:14 h</td>
      <td>Baguales Trail</td>
      <td>CHI</td>
      <td>1992.0</td>
      <td>M</td>
      <td>M23</td>
      <td>8.469</td>
      <td>4</td>
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
    </tr>
    <tr>
      <th>7461181</th>
      <td>1995</td>
      <td>07.01.1995</td>
      <td>Avalon Benefit 50-Mile Run (USA)</td>
      <td>50mi</td>
      <td>92</td>
      <td>11:59:37 h</td>
      <td>NaN</td>
      <td>USA</td>
      <td>1941.0</td>
      <td>M</td>
      <td>M50</td>
      <td>6709.0</td>
      <td>1045603</td>
    </tr>
    <tr>
      <th>7461182</th>
      <td>1995</td>
      <td>07.01.1995</td>
      <td>Avalon Benefit 50-Mile Run (USA)</td>
      <td>50mi</td>
      <td>92</td>
      <td>12:01:41 h</td>
      <td>NaN</td>
      <td>USA</td>
      <td>1932.0</td>
      <td>M</td>
      <td>M60</td>
      <td>6690.0</td>
      <td>1070463</td>
    </tr>
    <tr>
      <th>7461183</th>
      <td>1995</td>
      <td>07.01.1995</td>
      <td>Avalon Benefit 50-Mile Run (USA)</td>
      <td>50mi</td>
      <td>92</td>
      <td>12:03:26 h</td>
      <td>NaN</td>
      <td>USA</td>
      <td>1934.0</td>
      <td>F</td>
      <td>W60</td>
      <td>6674.0</td>
      <td>416139</td>
    </tr>
    <tr>
      <th>7461184</th>
      <td>1995</td>
      <td>07.01.1995</td>
      <td>Avalon Benefit 50-Mile Run (USA)</td>
      <td>50mi</td>
      <td>92</td>
      <td>12:03:26 h</td>
      <td>NaN</td>
      <td>USA</td>
      <td>1951.0</td>
      <td>F</td>
      <td>W40</td>
      <td>6674.0</td>
      <td>1098098</td>
    </tr>
    <tr>
      <th>7461185</th>
      <td>1995</td>
      <td>07.01.1995</td>
      <td>Avalon Benefit 50-Mile Run (USA)</td>
      <td>50mi</td>
      <td>92</td>
      <td>12:05:59 h</td>
      <td>NaN</td>
      <td>USA</td>
      <td>1947.0</td>
      <td>F</td>
      <td>W45</td>
      <td>6650.0</td>
      <td>1626367</td>
    </tr>
  </tbody>
</table>
<p>1874790 rows × 13 columns</p>
</div>




```python
#Now lets do with the year included to 2020
df[(df['Event distance/length'].isin(['50km','50mi']))  & (df['Year of event']==2020)]
```




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
      <th>Year of event</th>
      <th>Event dates</th>
      <th>Event name</th>
      <th>Event distance/length</th>
      <th>Event number of finishers</th>
      <th>Athlete performance</th>
      <th>Athlete club</th>
      <th>Athlete country</th>
      <th>Athlete year of birth</th>
      <th>Athlete gender</th>
      <th>Athlete age category</th>
      <th>Athlete average speed</th>
      <th>Athlete ID</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2538571</th>
      <td>2020</td>
      <td>07.-09.02.2020</td>
      <td>Taipei 48hr Ultra Marathon - 50mi (TPE)</td>
      <td>50mi</td>
      <td>38</td>
      <td>7:34:19 h</td>
      <td>日本隊</td>
      <td>JPN</td>
      <td>1965.0</td>
      <td>M</td>
      <td>M50</td>
      <td>10.627</td>
      <td>53107</td>
    </tr>
    <tr>
      <th>2538572</th>
      <td>2020</td>
      <td>07.-09.02.2020</td>
      <td>Taipei 48hr Ultra Marathon - 50mi (TPE)</td>
      <td>50mi</td>
      <td>38</td>
      <td>7:43:50 h</td>
      <td>NaN</td>
      <td>AUS</td>
      <td>1974.0</td>
      <td>M</td>
      <td>M45</td>
      <td>10.409</td>
      <td>8785</td>
    </tr>
    <tr>
      <th>2538573</th>
      <td>2020</td>
      <td>07.-09.02.2020</td>
      <td>Taipei 48hr Ultra Marathon - 50mi (TPE)</td>
      <td>50mi</td>
      <td>38</td>
      <td>8:04:40 h</td>
      <td>NaN</td>
      <td>TPE</td>
      <td>1976.0</td>
      <td>M</td>
      <td>M40</td>
      <td>9.962</td>
      <td>4502</td>
    </tr>
    <tr>
      <th>2538574</th>
      <td>2020</td>
      <td>07.-09.02.2020</td>
      <td>Taipei 48hr Ultra Marathon - 50mi (TPE)</td>
      <td>50mi</td>
      <td>38</td>
      <td>8:30:49 h</td>
      <td>台灣大腳ㄚ長跑協會</td>
      <td>TPE</td>
      <td>1969.0</td>
      <td>F</td>
      <td>W50</td>
      <td>9.452</td>
      <td>63964</td>
    </tr>
    <tr>
      <th>2538575</th>
      <td>2020</td>
      <td>07.-09.02.2020</td>
      <td>Taipei 48hr Ultra Marathon - 50mi (TPE)</td>
      <td>50mi</td>
      <td>38</td>
      <td>8:34:47 h</td>
      <td>NaN</td>
      <td>TPE</td>
      <td>1964.0</td>
      <td>M</td>
      <td>M55</td>
      <td>9.379</td>
      <td>4485</td>
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
    </tr>
    <tr>
      <th>2762404</th>
      <td>2020</td>
      <td>03.10.2020</td>
      <td>Bison Ultra-Trail 50 (POL)</td>
      <td>50km</td>
      <td>271</td>
      <td>7:36:25 h</td>
      <td>AKS Polonia Warszawa</td>
      <td>POL</td>
      <td>1981.0</td>
      <td>F</td>
      <td>W35</td>
      <td>6.573</td>
      <td>860743</td>
    </tr>
    <tr>
      <th>2762405</th>
      <td>2020</td>
      <td>03.10.2020</td>
      <td>Bison Ultra-Trail 50 (POL)</td>
      <td>50km</td>
      <td>271</td>
      <td>7:36:27 h</td>
      <td>*Warszawa</td>
      <td>POL</td>
      <td>1970.0</td>
      <td>F</td>
      <td>W45</td>
      <td>6.572</td>
      <td>860744</td>
    </tr>
    <tr>
      <th>2762406</th>
      <td>2020</td>
      <td>03.10.2020</td>
      <td>Bison Ultra-Trail 50 (POL)</td>
      <td>50km</td>
      <td>271</td>
      <td>7:44:18 h</td>
      <td>Outdoor Training</td>
      <td>POL</td>
      <td>1993.0</td>
      <td>F</td>
      <td>W23</td>
      <td>6.461</td>
      <td>860745</td>
    </tr>
    <tr>
      <th>2762407</th>
      <td>2020</td>
      <td>03.10.2020</td>
      <td>Bison Ultra-Trail 50 (POL)</td>
      <td>50km</td>
      <td>271</td>
      <td>8:04:50 h</td>
      <td>PH Bysewo Gdańsk</td>
      <td>POL</td>
      <td>1976.0</td>
      <td>M</td>
      <td>M40</td>
      <td>6.188</td>
      <td>798409</td>
    </tr>
    <tr>
      <th>2762408</th>
      <td>2020</td>
      <td>03.10.2020</td>
      <td>Bison Ultra-Trail 50 (POL)</td>
      <td>50km</td>
      <td>271</td>
      <td>8:11:43 h</td>
      <td>*Nowe Aleksandrowo</td>
      <td>POL</td>
      <td>1961.0</td>
      <td>M</td>
      <td>M55</td>
      <td>6.101</td>
      <td>860746</td>
    </tr>
  </tbody>
</table>
<p>63489 rows × 13 columns</p>
</div>




```python
#df[(df['Event distance/length'].isin(['50km','50mi']))  & (df['Year of event']==2020)]
df[(df['Event distance/length'].isin(['50km','50mi'])) & (df['Year of event']==2020)]
```




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
      <th>Year of event</th>
      <th>Event dates</th>
      <th>Event name</th>
      <th>Event distance/length</th>
      <th>Event number of finishers</th>
      <th>Athlete performance</th>
      <th>Athlete club</th>
      <th>Athlete country</th>
      <th>Athlete year of birth</th>
      <th>Athlete gender</th>
      <th>Athlete age category</th>
      <th>Athlete average speed</th>
      <th>Athlete ID</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2538571</th>
      <td>2020</td>
      <td>07.-09.02.2020</td>
      <td>Taipei 48hr Ultra Marathon - 50mi (TPE)</td>
      <td>50mi</td>
      <td>38</td>
      <td>7:34:19 h</td>
      <td>日本隊</td>
      <td>JPN</td>
      <td>1965.0</td>
      <td>M</td>
      <td>M50</td>
      <td>10.627</td>
      <td>53107</td>
    </tr>
    <tr>
      <th>2538572</th>
      <td>2020</td>
      <td>07.-09.02.2020</td>
      <td>Taipei 48hr Ultra Marathon - 50mi (TPE)</td>
      <td>50mi</td>
      <td>38</td>
      <td>7:43:50 h</td>
      <td>NaN</td>
      <td>AUS</td>
      <td>1974.0</td>
      <td>M</td>
      <td>M45</td>
      <td>10.409</td>
      <td>8785</td>
    </tr>
    <tr>
      <th>2538573</th>
      <td>2020</td>
      <td>07.-09.02.2020</td>
      <td>Taipei 48hr Ultra Marathon - 50mi (TPE)</td>
      <td>50mi</td>
      <td>38</td>
      <td>8:04:40 h</td>
      <td>NaN</td>
      <td>TPE</td>
      <td>1976.0</td>
      <td>M</td>
      <td>M40</td>
      <td>9.962</td>
      <td>4502</td>
    </tr>
    <tr>
      <th>2538574</th>
      <td>2020</td>
      <td>07.-09.02.2020</td>
      <td>Taipei 48hr Ultra Marathon - 50mi (TPE)</td>
      <td>50mi</td>
      <td>38</td>
      <td>8:30:49 h</td>
      <td>台灣大腳ㄚ長跑協會</td>
      <td>TPE</td>
      <td>1969.0</td>
      <td>F</td>
      <td>W50</td>
      <td>9.452</td>
      <td>63964</td>
    </tr>
    <tr>
      <th>2538575</th>
      <td>2020</td>
      <td>07.-09.02.2020</td>
      <td>Taipei 48hr Ultra Marathon - 50mi (TPE)</td>
      <td>50mi</td>
      <td>38</td>
      <td>8:34:47 h</td>
      <td>NaN</td>
      <td>TPE</td>
      <td>1964.0</td>
      <td>M</td>
      <td>M55</td>
      <td>9.379</td>
      <td>4485</td>
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
    </tr>
    <tr>
      <th>2762404</th>
      <td>2020</td>
      <td>03.10.2020</td>
      <td>Bison Ultra-Trail 50 (POL)</td>
      <td>50km</td>
      <td>271</td>
      <td>7:36:25 h</td>
      <td>AKS Polonia Warszawa</td>
      <td>POL</td>
      <td>1981.0</td>
      <td>F</td>
      <td>W35</td>
      <td>6.573</td>
      <td>860743</td>
    </tr>
    <tr>
      <th>2762405</th>
      <td>2020</td>
      <td>03.10.2020</td>
      <td>Bison Ultra-Trail 50 (POL)</td>
      <td>50km</td>
      <td>271</td>
      <td>7:36:27 h</td>
      <td>*Warszawa</td>
      <td>POL</td>
      <td>1970.0</td>
      <td>F</td>
      <td>W45</td>
      <td>6.572</td>
      <td>860744</td>
    </tr>
    <tr>
      <th>2762406</th>
      <td>2020</td>
      <td>03.10.2020</td>
      <td>Bison Ultra-Trail 50 (POL)</td>
      <td>50km</td>
      <td>271</td>
      <td>7:44:18 h</td>
      <td>Outdoor Training</td>
      <td>POL</td>
      <td>1993.0</td>
      <td>F</td>
      <td>W23</td>
      <td>6.461</td>
      <td>860745</td>
    </tr>
    <tr>
      <th>2762407</th>
      <td>2020</td>
      <td>03.10.2020</td>
      <td>Bison Ultra-Trail 50 (POL)</td>
      <td>50km</td>
      <td>271</td>
      <td>8:04:50 h</td>
      <td>PH Bysewo Gdańsk</td>
      <td>POL</td>
      <td>1976.0</td>
      <td>M</td>
      <td>M40</td>
      <td>6.188</td>
      <td>798409</td>
    </tr>
    <tr>
      <th>2762408</th>
      <td>2020</td>
      <td>03.10.2020</td>
      <td>Bison Ultra-Trail 50 (POL)</td>
      <td>50km</td>
      <td>271</td>
      <td>8:11:43 h</td>
      <td>*Nowe Aleksandrowo</td>
      <td>POL</td>
      <td>1961.0</td>
      <td>M</td>
      <td>M55</td>
      <td>6.101</td>
      <td>860746</td>
    </tr>
  </tbody>
</table>
<p>63489 rows × 13 columns</p>
</div>




```python
#Lets try just the USA based
df[df['Event name'].str.split('(').str.get(1).str.split(')').str.get(0)=='USA']
```




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
      <th>Year of event</th>
      <th>Event dates</th>
      <th>Event name</th>
      <th>Event distance/length</th>
      <th>Event number of finishers</th>
      <th>Athlete performance</th>
      <th>Athlete club</th>
      <th>Athlete country</th>
      <th>Athlete year of birth</th>
      <th>Athlete gender</th>
      <th>Athlete age category</th>
      <th>Athlete average speed</th>
      <th>Athlete ID</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>55</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Yankee Springs 50 Mile Winter Challenge (USA)</td>
      <td>50mi</td>
      <td>9</td>
      <td>9:53:05 h</td>
      <td>*Middleville, MI</td>
      <td>USA</td>
      <td>1983.0</td>
      <td>M</td>
      <td>M23</td>
      <td>8.141</td>
      <td>55</td>
    </tr>
    <tr>
      <th>56</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Yankee Springs 50 Mile Winter Challenge (USA)</td>
      <td>50mi</td>
      <td>9</td>
      <td>11:09:35 h</td>
      <td>*Waterloo, ON</td>
      <td>CAN</td>
      <td>1977.0</td>
      <td>F</td>
      <td>W40</td>
      <td>7.211</td>
      <td>56</td>
    </tr>
    <tr>
      <th>57</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Yankee Springs 50 Mile Winter Challenge (USA)</td>
      <td>50mi</td>
      <td>9</td>
      <td>11:33:00 h</td>
      <td>*Kitchener, ON</td>
      <td>CAN</td>
      <td>1976.0</td>
      <td>M</td>
      <td>M40</td>
      <td>6.967</td>
      <td>57</td>
    </tr>
    <tr>
      <th>58</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Yankee Springs 50 Mile Winter Challenge (USA)</td>
      <td>50mi</td>
      <td>9</td>
      <td>11:38:17 h</td>
      <td>*Utica, MI</td>
      <td>USA</td>
      <td>1986.0</td>
      <td>M</td>
      <td>M23</td>
      <td>6.914</td>
      <td>58</td>
    </tr>
    <tr>
      <th>59</th>
      <td>2018</td>
      <td>06.01.2018</td>
      <td>Yankee Springs 50 Mile Winter Challenge (USA)</td>
      <td>50mi</td>
      <td>9</td>
      <td>11:56:35 h</td>
      <td>*Grass Lake, MI</td>
      <td>USA</td>
      <td>1988.0</td>
      <td>M</td>
      <td>M23</td>
      <td>6.738</td>
      <td>59</td>
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
    </tr>
    <tr>
      <th>7461181</th>
      <td>1995</td>
      <td>07.01.1995</td>
      <td>Avalon Benefit 50-Mile Run (USA)</td>
      <td>50mi</td>
      <td>92</td>
      <td>11:59:37 h</td>
      <td>NaN</td>
      <td>USA</td>
      <td>1941.0</td>
      <td>M</td>
      <td>M50</td>
      <td>6709.0</td>
      <td>1045603</td>
    </tr>
    <tr>
      <th>7461182</th>
      <td>1995</td>
      <td>07.01.1995</td>
      <td>Avalon Benefit 50-Mile Run (USA)</td>
      <td>50mi</td>
      <td>92</td>
      <td>12:01:41 h</td>
      <td>NaN</td>
      <td>USA</td>
      <td>1932.0</td>
      <td>M</td>
      <td>M60</td>
      <td>6690.0</td>
      <td>1070463</td>
    </tr>
    <tr>
      <th>7461183</th>
      <td>1995</td>
      <td>07.01.1995</td>
      <td>Avalon Benefit 50-Mile Run (USA)</td>
      <td>50mi</td>
      <td>92</td>
      <td>12:03:26 h</td>
      <td>NaN</td>
      <td>USA</td>
      <td>1934.0</td>
      <td>F</td>
      <td>W60</td>
      <td>6674.0</td>
      <td>416139</td>
    </tr>
    <tr>
      <th>7461184</th>
      <td>1995</td>
      <td>07.01.1995</td>
      <td>Avalon Benefit 50-Mile Run (USA)</td>
      <td>50mi</td>
      <td>92</td>
      <td>12:03:26 h</td>
      <td>NaN</td>
      <td>USA</td>
      <td>1951.0</td>
      <td>F</td>
      <td>W40</td>
      <td>6674.0</td>
      <td>1098098</td>
    </tr>
    <tr>
      <th>7461185</th>
      <td>1995</td>
      <td>07.01.1995</td>
      <td>Avalon Benefit 50-Mile Run (USA)</td>
      <td>50mi</td>
      <td>92</td>
      <td>12:05:59 h</td>
      <td>NaN</td>
      <td>USA</td>
      <td>1947.0</td>
      <td>F</td>
      <td>W45</td>
      <td>6650.0</td>
      <td>1626367</td>
    </tr>
  </tbody>
</table>
<p>1398540 rows × 13 columns</p>
</div>




```python
#Now lets combine 50km, 50mi and USA in the year 2020
df[(df['Event distance/length'].isin(['50km','50mi'])) & (df['Year of event']==2020) & (df['Event name'].str.split('(').str.get(1).str.split(')').str.get(0)=='USA')]
```




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
      <th>Year of event</th>
      <th>Event dates</th>
      <th>Event name</th>
      <th>Event distance/length</th>
      <th>Event number of finishers</th>
      <th>Athlete performance</th>
      <th>Athlete club</th>
      <th>Athlete country</th>
      <th>Athlete year of birth</th>
      <th>Athlete gender</th>
      <th>Athlete age category</th>
      <th>Athlete average speed</th>
      <th>Athlete ID</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2539945</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition (USA)</td>
      <td>50km</td>
      <td>20</td>
      <td>3:17:55 h</td>
      <td>*Normandy Park, WA</td>
      <td>USA</td>
      <td>1991.0</td>
      <td>M</td>
      <td>M23</td>
      <td>15.158</td>
      <td>71287</td>
    </tr>
    <tr>
      <th>2539946</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition (USA)</td>
      <td>50km</td>
      <td>20</td>
      <td>4:02:32 h</td>
      <td>*Gold Bar, WA</td>
      <td>USA</td>
      <td>1981.0</td>
      <td>M</td>
      <td>M35</td>
      <td>12.369</td>
      <td>629508</td>
    </tr>
    <tr>
      <th>2539947</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition (USA)</td>
      <td>50km</td>
      <td>20</td>
      <td>4:07:57 h</td>
      <td>*Vashon, WA</td>
      <td>USA</td>
      <td>1999.0</td>
      <td>M</td>
      <td>MU23</td>
      <td>12.099</td>
      <td>64838</td>
    </tr>
    <tr>
      <th>2539948</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition (USA)</td>
      <td>50km</td>
      <td>20</td>
      <td>4:22:02 h</td>
      <td>*Gig Harbor, WA</td>
      <td>USA</td>
      <td>1983.0</td>
      <td>M</td>
      <td>M35</td>
      <td>11.449</td>
      <td>704450</td>
    </tr>
    <tr>
      <th>2539949</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition (USA)</td>
      <td>50km</td>
      <td>20</td>
      <td>4:27:34 h</td>
      <td>*Bainbridge Island, WA</td>
      <td>USA</td>
      <td>1977.0</td>
      <td>M</td>
      <td>M40</td>
      <td>11.212</td>
      <td>810281</td>
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
    </tr>
    <tr>
      <th>2760957</th>
      <td>2020</td>
      <td>03.10.2020</td>
      <td>Yankee Springs Fall Trail Run Festival (USA)</td>
      <td>50km</td>
      <td>30</td>
      <td>7:07:48 h</td>
      <td>*East Lansing, MI</td>
      <td>USA</td>
      <td>1958.0</td>
      <td>F</td>
      <td>W60</td>
      <td>7.013</td>
      <td>816361</td>
    </tr>
    <tr>
      <th>2760958</th>
      <td>2020</td>
      <td>03.10.2020</td>
      <td>Yankee Springs Fall Trail Run Festival (USA)</td>
      <td>50km</td>
      <td>30</td>
      <td>7:27:22 h</td>
      <td>*Traverse City, MI</td>
      <td>USA</td>
      <td>1977.0</td>
      <td>F</td>
      <td>W40</td>
      <td>6.706</td>
      <td>326469</td>
    </tr>
    <tr>
      <th>2760959</th>
      <td>2020</td>
      <td>03.10.2020</td>
      <td>Yankee Springs Fall Trail Run Festival (USA)</td>
      <td>50km</td>
      <td>30</td>
      <td>7:27:24 h</td>
      <td>*Traverse City, MI</td>
      <td>USA</td>
      <td>1962.0</td>
      <td>F</td>
      <td>W55</td>
      <td>6.705</td>
      <td>372174</td>
    </tr>
    <tr>
      <th>2760960</th>
      <td>2020</td>
      <td>03.10.2020</td>
      <td>Yankee Springs Fall Trail Run Festival (USA)</td>
      <td>50km</td>
      <td>30</td>
      <td>7:38:30 h</td>
      <td>*Mason, MI</td>
      <td>USA</td>
      <td>1981.0</td>
      <td>F</td>
      <td>W35</td>
      <td>6.543</td>
      <td>860349</td>
    </tr>
    <tr>
      <th>2760961</th>
      <td>2020</td>
      <td>03.10.2020</td>
      <td>Yankee Springs Fall Trail Run Festival (USA)</td>
      <td>50km</td>
      <td>30</td>
      <td>7:59:53 h</td>
      <td>NaN</td>
      <td>USA</td>
      <td>1980.0</td>
      <td>M</td>
      <td>M35</td>
      <td>6.252</td>
      <td>770097</td>
    </tr>
  </tbody>
</table>
<p>26090 rows × 13 columns</p>
</div>




```python
#Now lets combine 50km, 50mi and USA in the year 2020 and declaring this as a df2
df2= df[(df['Event distance/length'].isin(['50km','50mi'])) & (df['Year of event']==2020) & (df['Event name'].str.split('(').str.get(1).str.split(')').str.get(0)=='USA')]
```


```python
df2.head(10)
```




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
      <th>Year of event</th>
      <th>Event dates</th>
      <th>Event name</th>
      <th>Event distance/length</th>
      <th>Event number of finishers</th>
      <th>Athlete performance</th>
      <th>Athlete club</th>
      <th>Athlete country</th>
      <th>Athlete year of birth</th>
      <th>Athlete gender</th>
      <th>Athlete age category</th>
      <th>Athlete average speed</th>
      <th>Athlete ID</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2539945</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition (USA)</td>
      <td>50km</td>
      <td>20</td>
      <td>3:17:55 h</td>
      <td>*Normandy Park, WA</td>
      <td>USA</td>
      <td>1991.0</td>
      <td>M</td>
      <td>M23</td>
      <td>15.158</td>
      <td>71287</td>
    </tr>
    <tr>
      <th>2539946</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition (USA)</td>
      <td>50km</td>
      <td>20</td>
      <td>4:02:32 h</td>
      <td>*Gold Bar, WA</td>
      <td>USA</td>
      <td>1981.0</td>
      <td>M</td>
      <td>M35</td>
      <td>12.369</td>
      <td>629508</td>
    </tr>
    <tr>
      <th>2539947</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition (USA)</td>
      <td>50km</td>
      <td>20</td>
      <td>4:07:57 h</td>
      <td>*Vashon, WA</td>
      <td>USA</td>
      <td>1999.0</td>
      <td>M</td>
      <td>MU23</td>
      <td>12.099</td>
      <td>64838</td>
    </tr>
    <tr>
      <th>2539948</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition (USA)</td>
      <td>50km</td>
      <td>20</td>
      <td>4:22:02 h</td>
      <td>*Gig Harbor, WA</td>
      <td>USA</td>
      <td>1983.0</td>
      <td>M</td>
      <td>M35</td>
      <td>11.449</td>
      <td>704450</td>
    </tr>
    <tr>
      <th>2539949</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition (USA)</td>
      <td>50km</td>
      <td>20</td>
      <td>4:27:34 h</td>
      <td>*Bainbridge Island, WA</td>
      <td>USA</td>
      <td>1977.0</td>
      <td>M</td>
      <td>M40</td>
      <td>11.212</td>
      <td>810281</td>
    </tr>
    <tr>
      <th>2539950</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition (USA)</td>
      <td>50km</td>
      <td>20</td>
      <td>4:42:06 h</td>
      <td>*Seattle, WA</td>
      <td>USA</td>
      <td>1985.0</td>
      <td>F</td>
      <td>W23</td>
      <td>10.635</td>
      <td>810282</td>
    </tr>
    <tr>
      <th>2539951</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition (USA)</td>
      <td>50km</td>
      <td>20</td>
      <td>4:49:20 h</td>
      <td>*Camano Island, WA</td>
      <td>USA</td>
      <td>1961.0</td>
      <td>M</td>
      <td>M55</td>
      <td>10.369</td>
      <td>11739</td>
    </tr>
    <tr>
      <th>2539952</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition (USA)</td>
      <td>50km</td>
      <td>20</td>
      <td>4:49:50 h</td>
      <td>*Clinton, WA</td>
      <td>USA</td>
      <td>1970.0</td>
      <td>M</td>
      <td>M45</td>
      <td>10.351</td>
      <td>80394</td>
    </tr>
    <tr>
      <th>2539953</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition (USA)</td>
      <td>50km</td>
      <td>20</td>
      <td>4:51:00 h</td>
      <td>*Seattle, WA</td>
      <td>USA</td>
      <td>1975.0</td>
      <td>F</td>
      <td>W40</td>
      <td>10.309</td>
      <td>140909</td>
    </tr>
    <tr>
      <th>2539954</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition (USA)</td>
      <td>50km</td>
      <td>20</td>
      <td>5:02:35 h</td>
      <td>*Sammamish, WA</td>
      <td>USA</td>
      <td>1979.0</td>
      <td>M</td>
      <td>M40</td>
      <td>9.915</td>
      <td>753889</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2['Event name'].str.split('(').str.get(0)
```


```python
df2['Event name']=df2['Event name'].str.split('(').str.get(0)
```

    C:\Users\jayak\AppData\Local\Temp\ipykernel_17132\2517910487.py:1: SettingWithCopyWarning: 
    A value is trying to be set on a copy of a slice from a DataFrame.
    Try using .loc[row_indexer,col_indexer] = value instead
    
    See the caveats in the documentation: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy
      df2['Event name']=df2['Event name'].str.split('(').str.get(0)
    


```python
df2.head()
```




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
      <th>Year of event</th>
      <th>Event dates</th>
      <th>Event name</th>
      <th>Event distance/length</th>
      <th>Event number of finishers</th>
      <th>Athlete performance</th>
      <th>Athlete club</th>
      <th>Athlete country</th>
      <th>Athlete year of birth</th>
      <th>Athlete gender</th>
      <th>Athlete age category</th>
      <th>Athlete average speed</th>
      <th>Athlete ID</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2539945</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition</td>
      <td>50km</td>
      <td>20</td>
      <td>3:17:55 h</td>
      <td>*Normandy Park, WA</td>
      <td>USA</td>
      <td>1991.0</td>
      <td>M</td>
      <td>M23</td>
      <td>15.158</td>
      <td>71287</td>
    </tr>
    <tr>
      <th>2539946</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition</td>
      <td>50km</td>
      <td>20</td>
      <td>4:02:32 h</td>
      <td>*Gold Bar, WA</td>
      <td>USA</td>
      <td>1981.0</td>
      <td>M</td>
      <td>M35</td>
      <td>12.369</td>
      <td>629508</td>
    </tr>
    <tr>
      <th>2539947</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition</td>
      <td>50km</td>
      <td>20</td>
      <td>4:07:57 h</td>
      <td>*Vashon, WA</td>
      <td>USA</td>
      <td>1999.0</td>
      <td>M</td>
      <td>MU23</td>
      <td>12.099</td>
      <td>64838</td>
    </tr>
    <tr>
      <th>2539948</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition</td>
      <td>50km</td>
      <td>20</td>
      <td>4:22:02 h</td>
      <td>*Gig Harbor, WA</td>
      <td>USA</td>
      <td>1983.0</td>
      <td>M</td>
      <td>M35</td>
      <td>11.449</td>
      <td>704450</td>
    </tr>
    <tr>
      <th>2539949</th>
      <td>2020</td>
      <td>02.02.2020</td>
      <td>West Seattle Beach Run - Winter Edition</td>
      <td>50km</td>
      <td>20</td>
      <td>4:27:34 h</td>
      <td>*Bainbridge Island, WA</td>
      <td>USA</td>
      <td>1977.0</td>
      <td>M</td>
      <td>M40</td>
      <td>11.212</td>
      <td>810281</td>
    </tr>
  </tbody>
</table>
</div>




```python

```

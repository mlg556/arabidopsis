```python
# !pip install pandas openpyxl
import pandas as pd
import zipfile
```


```python
# extract txt, file extension is erroneously gz, but its actually a zip file
fname = "ATH_GO_GOSLIM.txt"
fname_gz = f"{fname}.gz"

with zipfile.ZipFile(fname_gz, 'r') as z:
    z.extractall(".")
```


```python
# column data from from ATH_GO.README.txt
columns = [
    "locus_name",
    "tair_acc",
    "obj_name",
    "rel_type",
    "go_term",
    "go_id",
    "tair_id",
    "aspect",
    "go_slim",
    "evidence_code",
    "evidence_desc",
    "evidence_with",
    "reference",
    "annotator",
    "date"
]


# read into dataframe
df0 = pd.read_csv(fname, sep="\t", names=columns, skiprows=[0,1,2,3], index_col=False, header=0)
df0
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
      <th>locus_name</th>
      <th>tair_acc</th>
      <th>obj_name</th>
      <th>rel_type</th>
      <th>go_term</th>
      <th>go_id</th>
      <th>tair_id</th>
      <th>aspect</th>
      <th>go_slim</th>
      <th>evidence_code</th>
      <th>evidence_desc</th>
      <th>evidence_with</th>
      <th>reference</th>
      <th>annotator</th>
      <th>date</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AT1G01010</td>
      <td>locus:2200935</td>
      <td>AT1G01010</td>
      <td>acts upstream of or within</td>
      <td>response to oxidative stress</td>
      <td>GO:0006979</td>
      <td>6625</td>
      <td>P</td>
      <td>response to stress</td>
      <td>IEA</td>
      <td>traceable computational prediction</td>
      <td>AGI_LocusCode:AT5G19875</td>
      <td>Publication:501796011|PMID:34562334</td>
      <td>klaasvdp</td>
      <td>2022-11-14</td>
    </tr>
    <tr>
      <th>1</th>
      <td>AT1G01010</td>
      <td>locus:2200935</td>
      <td>AT1G01010</td>
      <td>acts upstream of or within</td>
      <td>response to abscisic acid</td>
      <td>GO:0009737</td>
      <td>11395</td>
      <td>P</td>
      <td>response to chemical</td>
      <td>IEA</td>
      <td>traceable computational prediction</td>
      <td>AGI_LocusCode:AT4G27410</td>
      <td>Publication:501796011|PMID:34562334</td>
      <td>klaasvdp</td>
      <td>2022-11-14</td>
    </tr>
    <tr>
      <th>2</th>
      <td>AT1G01010</td>
      <td>locus:2200935</td>
      <td>AT1G01010</td>
      <td>acts upstream of or within</td>
      <td>response to lipid</td>
      <td>GO:0033993</td>
      <td>28865</td>
      <td>P</td>
      <td>response to chemical</td>
      <td>IEA</td>
      <td>traceable computational prediction</td>
      <td>AGI_LocusCode:AT4G27410|AGI_LocusCode:AT2G0299...</td>
      <td>Publication:501796011|PMID:34562334</td>
      <td>klaasvdp</td>
      <td>2022-11-14</td>
    </tr>
    <tr>
      <th>3</th>
      <td>AT1G01010</td>
      <td>locus:2200935</td>
      <td>AT1G01010</td>
      <td>acts upstream of or within</td>
      <td>oxoacid metabolic process</td>
      <td>GO:0043436</td>
      <td>21524</td>
      <td>P</td>
      <td>other cellular processes</td>
      <td>IEA</td>
      <td>traceable computational prediction</td>
      <td>AGI_LocusCode:AT5G63790</td>
      <td>Publication:501796011|PMID:34562334</td>
      <td>klaasvdp</td>
      <td>2022-11-14</td>
    </tr>
    <tr>
      <th>4</th>
      <td>AT1G01010</td>
      <td>locus:2200935</td>
      <td>AT1G01010</td>
      <td>acts upstream of or within</td>
      <td>defense response to other organism</td>
      <td>GO:0098542</td>
      <td>46569</td>
      <td>P</td>
      <td>response to external stimulus</td>
      <td>IEA</td>
      <td>traceable computational prediction</td>
      <td>AGI_LocusCode:AT2G43510|AGI_LocusCode:AT4G1473...</td>
      <td>Publication:501796011|PMID:34562334</td>
      <td>klaasvdp</td>
      <td>2022-11-14</td>
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
    </tr>
    <tr>
      <th>456200</th>
      <td>YAK</td>
      <td>gene:1945468</td>
      <td>YAK</td>
      <td>is active in</td>
      <td>cellular_component</td>
      <td>GO:0005575</td>
      <td>163</td>
      <td>C</td>
      <td>unknown cellular components</td>
      <td>ND</td>
      <td>'Unknown' cellular component</td>
      <td>NONE</td>
      <td>Communication:1345790</td>
      <td>TAIR</td>
      <td>2022-02-01</td>
    </tr>
    <tr>
      <th>456201</th>
      <td>YAK</td>
      <td>gene:1945468</td>
      <td>YAK</td>
      <td>enables</td>
      <td>molecular_function</td>
      <td>GO:0003674</td>
      <td>3226</td>
      <td>F</td>
      <td>unknown molecular functions</td>
      <td>ND</td>
      <td>'Unknown' molecular function</td>
      <td>NaN</td>
      <td>Communication:1345790</td>
      <td>TAIR</td>
      <td>2006-10-20</td>
    </tr>
    <tr>
      <th>456202</th>
      <td>YI</td>
      <td>gene:1945470</td>
      <td>YI</td>
      <td>involved in</td>
      <td>biological_process</td>
      <td>GO:0008150</td>
      <td>5239</td>
      <td>P</td>
      <td>unknown biological processes</td>
      <td>ND</td>
      <td>'Unknown' biological process</td>
      <td>NONE</td>
      <td>Communication:1345790</td>
      <td>TAIR</td>
      <td>2022-02-01</td>
    </tr>
    <tr>
      <th>456203</th>
      <td>YI</td>
      <td>gene:1945470</td>
      <td>YI</td>
      <td>is active in</td>
      <td>cellular_component</td>
      <td>GO:0005575</td>
      <td>163</td>
      <td>C</td>
      <td>unknown cellular components</td>
      <td>ND</td>
      <td>'Unknown' cellular component</td>
      <td>NONE</td>
      <td>Communication:1345790</td>
      <td>TAIR</td>
      <td>2022-02-01</td>
    </tr>
    <tr>
      <th>456204</th>
      <td>YI</td>
      <td>gene:1945470</td>
      <td>YI</td>
      <td>enables</td>
      <td>molecular_function</td>
      <td>GO:0003674</td>
      <td>3226</td>
      <td>F</td>
      <td>unknown molecular functions</td>
      <td>ND</td>
      <td>'Unknown' molecular function</td>
      <td>NaN</td>
      <td>Communication:1345790</td>
      <td>TAIR</td>
      <td>2006-10-20</td>
    </tr>
  </tbody>
</table>
<p>456205 rows × 15 columns</p>
</div>




```python
select_columns = ["locus_name", "go_term"]

excluded_go_terms = ["molecular_function", "biological_process", "cellular_component"]

df = df0[select_columns] # select gene name and function
df = df.drop_duplicates() # drop duplicates
df = df.query("go_term not in @excluded_go_terms") # exclude go_terms

df
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
      <th>locus_name</th>
      <th>go_term</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AT1G01010</td>
      <td>response to oxidative stress</td>
    </tr>
    <tr>
      <th>1</th>
      <td>AT1G01010</td>
      <td>response to abscisic acid</td>
    </tr>
    <tr>
      <th>2</th>
      <td>AT1G01010</td>
      <td>response to lipid</td>
    </tr>
    <tr>
      <th>3</th>
      <td>AT1G01010</td>
      <td>oxoacid metabolic process</td>
    </tr>
    <tr>
      <th>4</th>
      <td>AT1G01010</td>
      <td>defense response to other organism</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>456174</th>
      <td>XRS9</td>
      <td>DNA damage response</td>
    </tr>
    <tr>
      <th>456175</th>
      <td>XRS9</td>
      <td>DNA repair</td>
    </tr>
    <tr>
      <th>456181</th>
      <td>XRS9</td>
      <td>response to X-ray</td>
    </tr>
    <tr>
      <th>456182</th>
      <td>XTC1</td>
      <td>embryo development ending in seed dormancy</td>
    </tr>
    <tr>
      <th>456189</th>
      <td>XTC2</td>
      <td>embryo development ending in seed dormancy</td>
    </tr>
  </tbody>
</table>
<p>175917 rows × 2 columns</p>
</div>




```python
dfg = df.groupby("go_term", as_index=False).apply(lambda x: x)
dfg
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
      <th></th>
      <th>locus_name</th>
      <th>go_term</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="3" valign="top">0</th>
      <th>59239</th>
      <td>AT1G36280</td>
      <td>'de novo' AMP biosynthetic process</td>
    </tr>
    <tr>
      <th>264419</th>
      <td>AT3G57610</td>
      <td>'de novo' AMP biosynthetic process</td>
    </tr>
    <tr>
      <th>301470</th>
      <td>AT4G18440</td>
      <td>'de novo' AMP biosynthetic process</td>
    </tr>
    <tr>
      <th rowspan="2" valign="top">1</th>
      <th>52412</th>
      <td>AT1G30820</td>
      <td>'de novo' CTP biosynthetic process</td>
    </tr>
    <tr>
      <th>161071</th>
      <td>AT2G34890</td>
      <td>'de novo' CTP biosynthetic process</td>
    </tr>
    <tr>
      <th>...</th>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th rowspan="3" valign="top">7460</th>
      <th>97087</th>
      <td>AT1G69770</td>
      <td>zygote asymmetric cytokinesis in embryo sac</td>
    </tr>
    <tr>
      <th>118067</th>
      <td>AT2G01210</td>
      <td>zygote asymmetric cytokinesis in embryo sac</td>
    </tr>
    <tr>
      <th>412149</th>
      <td>AT5G49160</td>
      <td>zygote asymmetric cytokinesis in embryo sac</td>
    </tr>
    <tr>
      <th rowspan="2" valign="top">7461</th>
      <th>129873</th>
      <td>AT2G17090</td>
      <td>zygote elongation</td>
    </tr>
    <tr>
      <th>157943</th>
      <td>AT2G33160</td>
      <td>zygote elongation</td>
    </tr>
  </tbody>
</table>
<p>175917 rows × 2 columns</p>
</div>




```python
dfg_sum = df.groupby("go_term").count()
dfg_sum = dfg_sum.sort_values(by=['locus_name'], ascending=False)
dfg_sum
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
      <th>locus_name</th>
    </tr>
    <tr>
      <th>go_term</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>nucleus</th>
      <td>10494</td>
    </tr>
    <tr>
      <th>chloroplast</th>
      <td>4966</td>
    </tr>
    <tr>
      <th>cytoplasm</th>
      <td>4771</td>
    </tr>
    <tr>
      <th>protein binding</th>
      <td>4519</td>
    </tr>
    <tr>
      <th>mitochondrion</th>
      <td>4449</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>organelle fission</th>
      <td>1</td>
    </tr>
    <tr>
      <th>beta,beta digalactosyldiacylglycerol galactosyltransferase activity</th>
      <td>1</td>
    </tr>
    <tr>
      <th>regulation of MAPK cascade</th>
      <td>1</td>
    </tr>
    <tr>
      <th>regulation of GTPase activity</th>
      <td>1</td>
    </tr>
    <tr>
      <th>regulation of trichome patterning</th>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>7462 rows × 1 columns</p>
</div>



<div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

In \[ \]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
data-type="inline">

<div class="CodeMirror cm-s-jupyter">

<div class="highlight hl-ipython3">

    !pip install pandas
    !pip install plotly
    !pip install cufflinks

</div>

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

In \[31\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
data-type="inline">

<div class="CodeMirror cm-s-jupyter">

<div class="highlight hl-ipython3">

    import plotly
    import pandas as pd
    import cufflinks as cf
    from IPython.display import display,HTML

    cf.set_config_file(sharing='public',theme='white',offline=True)

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper">

<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">

</div>

<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

<div class="jp-OutputPrompt jp-OutputArea-prompt">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output"
mime-type="text/html">

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
mime-type="text/markdown">

# Leer tabla de datos<a href="#Leer-tabla-de-datos" class="anchor-link">¶</a>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

In \[18\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
data-type="inline">

<div class="CodeMirror cm-s-jupyter">

<div class="highlight hl-ipython3">

    df_injuries = pd.read_csv('league-140_season-2022.csv')

</div>

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

In \[21\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
data-type="inline">

<div class="CodeMirror cm-s-jupyter">

<div class="highlight hl-ipython3">

    # Dataframe datos La Liga
    df_injuries_140_2020 = pd.read_csv('league-140_season-2020.csv')
    df_injuries_140_2021 = pd.read_csv('league-140_season-2021.csv')
    df_injuries_140_2022 = pd.read_csv('league-140_season-2022.csv')
    df_injuries_140_2023 = pd.read_csv('league-140_season-2023.csv')


    df_injuries_140 = pd.concat([df_injuries_140_2023,df_injuries_140_2020,df_injuries_140_2021,df_injuries_140_2022],axis=0)

    #Dataframe datos Premier League
    df_injuries_39_2020 = pd.read_csv('league-39_season-2020.csv')
    df_injuries_39_2021 = pd.read_csv('league-39_season-2021.csv')
    df_injuries_39_2022 = pd.read_csv('league-39_season-2022.csv')
    df_injuries_39_2023 = pd.read_csv('league-39_season-2023.csv')


    df_injuries_39 = pd.concat([df_injuries_39_2023,df_injuries_39_2020,df_injuries_39_2021,df_injuries_39_2022],axis=0)


    #Dataframe con todos los datos unificados

    df_injuries = pd.concat([df_injuries_140,df_injuries_39],axis=0)

</div>

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

In \[22\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
data-type="inline">

<div class="CodeMirror cm-s-jupyter">

<div class="highlight hl-ipython3">

    df_injuries.head()

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper">

<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">

</div>

<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child jp-OutputArea-executeResult">

<div class="jp-OutputPrompt jp-OutputArea-prompt">

Out\[22\]:

</div>

<div
class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult"
mime-type="text/html">

<div>

|     | player_id | player_name     | player_photo                                          | player_type       | player_injury_reason     | team_id | team_name        | team_logo                                             | fixture_id | fixture_timezone | fixture_date                | fixture_timestamp | league_id | league_season | league_name | league_country | league_logo                                           | league_flag                                           |
|-----|-----------|-----------------|-------------------------------------------------------|-------------------|--------------------------|---------|------------------|-------------------------------------------------------|------------|------------------|-----------------------------|-------------------|-----------|---------------|-------------|----------------|-------------------------------------------------------|-------------------------------------------------------|
| 0   | 13062     | "Leo Baptistao" | "https:\\/\\/media-4.api-sports.io\\/football\\/pl... | "Missing Fixture" | "Achilles Tendon Injury" | 723     | "Almeria"        | "https:\\/\\/media-4.api-sports.io\\/football\\/te... | 1037952    | "UTC"            | "2023-08-11T17:30:00+00:00" | 1691775000        | 140       | 2023          | "La Liga"   | "Spain"        | "https:\\/\\/media-4.api-sports.io\\/football\\/le... | "https:\\/\\/media-4.api-sports.io\\/flags\\/es.svg"} |
| 1   | 282131    | "M. Svidersky"  | "https:\\/\\/media-4.api-sports.io\\/football\\/pl... | "Missing Fixture" | "Knee Injury"            | 723     | "Almeria"        | "https:\\/\\/media-4.api-sports.io\\/football\\/te... | 1037952    | "UTC"            | "2023-08-11T17:30:00+00:00" | 1691775000        | 140       | 2023          | "La Liga"   | "Spain"        | "https:\\/\\/media-4.api-sports.io\\/football\\/le... | "https:\\/\\/media-4.api-sports.io\\/flags\\/es.svg"} |
| 2   | 47551     | "R. de Tomas"   | "https:\\/\\/media-4.api-sports.io\\/football\\/pl... | "Missing Fixture" | "Injury"                 | 728     | "Rayo Vallecano" | "https:\\/\\/media-4.api-sports.io\\/football\\/te... | 1037952    | "UTC"            | "2023-08-11T17:30:00+00:00" | 1691775000        | 140       | 2023          | "La Liga"   | "Spain"        | "https:\\/\\/media-4.api-sports.io\\/football\\/le... | "https:\\/\\/media-4.api-sports.io\\/flags\\/es.svg"} |
| 3   | 47209     | "A. Martin"     | "https:\\/\\/media-4.api-sports.io\\/football\\/pl... | "Questionable"    | "Injury"                 | 728     | "Rayo Vallecano" | "https:\\/\\/media-4.api-sports.io\\/football\\/te... | 1037952    | "UTC"            | "2023-08-11T17:30:00+00:00" | 1691775000        | 140       | 2023          | "La Liga"   | "Spain"        | "https:\\/\\/media-4.api-sports.io\\/football\\/le... | "https:\\/\\/media-4.api-sports.io\\/flags\\/es.svg"} |
| 4   | 433       | "Marcao"        | "https:\\/\\/media-4.api-sports.io\\/football\\/pl... | "Missing Fixture" | "Muscle Injury"          | 536     | "Sevilla"        | "https:\\/\\/media-4.api-sports.io\\/football\\/te... | 1037956    | "UTC"            | "2023-08-11T20:00:00+00:00" | 1691784000        | 140       | 2023          | "La Liga"   | "Spain"        | "https:\\/\\/media-4.api-sports.io\\/football\\/le... | "https:\\/\\/media-4.api-sports.io\\/flags\\/es.svg"} |

</div>

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

In \[23\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
data-type="inline">

<div class="CodeMirror cm-s-jupyter">

<div class="highlight hl-ipython3">

    #df_injuries = df_injuries.sort_values(by=['player_id'])

    df_injuries_140['row_number']= df_injuries_140.reset_index().index

    df_injuries_140 = df_injuries_140.dropna()

    pd.pivot_table(df_injuries_140, index='team_name',columns=['league_season'],values='player_name',aggfunc="count")

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper">

<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">

</div>

<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child jp-OutputArea-executeResult">

<div class="jp-OutputPrompt jp-OutputArea-prompt">

Out\[23\]:

</div>

<div
class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult"
mime-type="text/html">

<div>

| league_season     | 2020 | 2021  | 2022  | 2023  |
|-------------------|------|-------|-------|-------|
| team_name         |      |       |       |       |
| "Alaves"          | 38.0 | 66.0  | NaN   | 34.0  |
| "Almeria"         | NaN  | NaN   | 117.0 | 73.0  |
| "Athletic Club"   | 54.0 | 142.0 | 115.0 | 58.0  |
| "Atletico Madrid" | 15.0 | 124.0 | 126.0 | 94.0  |
| "Barcelona"       | 35.0 | 243.0 | 103.0 | 53.0  |
| "Cadiz"           | 31.0 | 117.0 | 226.0 | 80.0  |
| "Celta Vigo"      | 45.0 | 54.0  | 79.0  | 31.0  |
| "Eibar"           | 24.0 | NaN   | NaN   | NaN   |
| "Elche"           | 15.0 | 72.0  | 168.0 | NaN   |
| "Espanyol"        | NaN  | 90.0  | 141.0 | NaN   |
| "Getafe"          | 27.0 | 83.0  | 79.0  | 56.0  |
| "Girona"          | NaN  | NaN   | 196.0 | 116.0 |
| "Granada CF"      | 54.0 | 168.0 | NaN   | 37.0  |
| "Huesca"          | 34.0 | NaN   | NaN   | NaN   |
| "Las Palmas"      | NaN  | NaN   | NaN   | 63.0  |
| "Levante"         | 31.0 | 155.0 | NaN   | NaN   |
| "Mallorca"        | NaN  | 140.0 | 121.0 | 28.0  |
| "Osasuna"         | 22.0 | 72.0  | 97.0  | 37.0  |
| "Rayo Vallecano"  | NaN  | 83.0  | 67.0  | 20.0  |
| "Real Betis"      | 31.0 | 158.0 | 140.0 | 82.0  |
| "Real Madrid"     | 55.0 | 166.0 | 115.0 | 99.0  |
| "Real Sociedad"   | 64.0 | 188.0 | 196.0 | 60.0  |
| "Sevilla"         | 5.0  | 142.0 | 164.0 | 104.0 |
| "Valencia"        | 11.0 | 125.0 | 126.0 | 65.0  |
| "Valladolid"      | 29.0 | NaN   | 128.0 | NaN   |
| "Villarreal"      | 27.0 | 103.0 | 148.0 | 75.0  |

</div>

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

In \[ \]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
data-type="inline">

<div class="CodeMirror cm-s-jupyter">

<div class="highlight hl-ipython3">

    df_injuries_39['row_number']= df_injuries_39.reset_index().index

    df_injuries_39 = df_injuries_39.dropna()

    pd.pivot_table(df_injuries_39, index='player_injury_reason',columns=['league_season'],values='player_name',aggfunc="count")

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper">

<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">

</div>

<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child jp-OutputArea-executeResult">

<div class="jp-OutputPrompt jp-OutputArea-prompt">

Out\[ \]:

</div>

<div
class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult"
mime-type="text/html">

<div>

| league_season            | 2020  | 2021  | 2022  | 2023  |
|--------------------------|-------|-------|-------|-------|
| player_injury_reason     |       |       |       |       |
| "Abdominal strain"       | 7.0   | 20.0  | 2.0   | NaN   |
| "Achilles Tendon Injury" | 2.0   | 39.0  | 66.0  | 9.0   |
| "Ankle Injury"           | 32.0  | 239.0 | 245.0 | 185.0 |
| "Arm Injury"             | 1.0   | 1.0   | 5.0   | NaN   |
| "Back Injury"            | 5.0   | 11.0  | 35.0  | 19.0  |
| "Broken Leg"             | 11.0  | 34.0  | 38.0  | NaN   |
| "Broken ankle"           | 7.0   | NaN   | NaN   | NaN   |
| "Buttock Injury"         | 1.0   | NaN   | NaN   | NaN   |
| "Calf Injury"            | 44.0  | 142.0 | 225.0 | 101.0 |
| "Coach's decision"       | 2.0   | 9.0   | 13.0  | 3.0   |
| "Concussion"             | 8.0   | 1.0   | 7.0   | 1.0   |
| "Convalescence"          | NaN   | NaN   | 1.0   | NaN   |
| "Elbow Injury"           | NaN   | 2.0   | NaN   | NaN   |
| "Eye injury"             | 2.0   | 6.0   | 2.0   | NaN   |
| "Face Injury"            | NaN   | NaN   | 3.0   | NaN   |
| "Finger Injury"          | 2.0   | NaN   | 13.0  | NaN   |
| "Foot Injury"            | 5.0   | 43.0  | 36.0  | 25.0  |
| "Groin Injury"           | 32.0  | 127.0 | 58.0  | 42.0  |
| "Hamstring Injury"       | NaN   | NaN   | 37.0  | 19.0  |
| "Hand Injury"            | NaN   | NaN   | 1.0   | NaN   |
| "Head Injury"            | 3.0   | 12.0  | 21.0  | 3.0   |
| "Health problems"        | NaN   | NaN   | 10.0  | NaN   |
| "Heel Injury"            | NaN   | 4.0   | 7.0   | NaN   |
| "Hernia"                 | 3.0   | 8.0   | NaN   | NaN   |
| "Hip Injury"             | 15.0  | 39.0  | 7.0   | 29.0  |
| "Illness"                | 12.0  | 204.0 | 47.0  | 24.0  |
| "Inactive"               | NaN   | 16.0  | 41.0  | 6.0   |
| "Injury"                 | 14.0  | 61.0  | 210.0 | 181.0 |
| "Knee Injury"            | 165.0 | 489.0 | 690.0 | 331.0 |
| "Knock"                  | 26.0  | 79.0  | 98.0  | 44.0  |
| "Lacking Match Fitness"  | NaN   | 22.0  | 82.0  | 7.0   |
| "Leg Injury"             | 15.0  | 14.0  | 25.0  | 8.0   |
| "Loan agreement"         | 7.0   | 7.0   | 15.0  | 5.0   |
| "Lower Back Injury"      | 4.0   | 31.0  | 2.0   | 4.0   |
| "Muscle Injury"          | 62.0  | 271.0 | 346.0 | 208.0 |
| "National selection"     | NaN   | 53.0  | NaN   | NaN   |
| "Pelvis Injury"          | NaN   | NaN   | 7.0   | 2.0   |
| "Personal Reasons"       | 3.0   | 11.0  | 5.0   | NaN   |
| "Quarantine"             | NaN   | 8.0   | NaN   | NaN   |
| "Red Card"               | NaN   | 58.0  | 63.0  | 40.0  |
| "Rest"                   | NaN   | 1.0   | 9.0   | 1.0   |
| "Ribs Injury"            | 1.0   | NaN   | NaN   | NaN   |
| "Shin Injury"            | 6.0   | 6.0   | NaN   | NaN   |
| "Shoulder Injury"        | 4.0   | 25.0  | 33.0  | 36.0  |
| "Stomach Disorder"       | NaN   | 1.0   | NaN   | NaN   |
| "Surgery"                | NaN   | NaN   | NaN   | 8.0   |
| "Suspended"              | 19.0  | 35.0  | 43.0  | 38.0  |
| "Tendon Injury"          | 2.0   | 5.0   | NaN   | 3.0   |
| "Thigh Injury"           | 75.0  | 392.0 | 461.0 | 255.0 |
| "Toe Injury"             | NaN   | 5.0   | 2.0   | 1.0   |
| "Wrist Injury"           | NaN   | NaN   | 16.0  | 1.0   |
| "Yellow Cards"           | NaN   | 31.0  | 28.0  | 29.0  |

</div>

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
mime-type="text/markdown">

Vamos solo a destacar aquellas lesiones que importan pues, tarjetas
amarillas etc no nos interesan

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

In \[25\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
data-type="inline">

<div class="CodeMirror cm-s-jupyter">

<div class="highlight hl-ipython3">

    #Vamos solo a destacar aquellas lesiones que importan
    #mask = df_injuries['player_injury_reason'].isin(['\"Yellow Cards\"','\"Suspended\"','\"Rest\"','\"Red Card\"','\"Personal Reasons\"',
      #                                                            '\"National selection\"','\"Loan agreement\"','\"Injury\"','\"Coach\'s decision\"',
       #                                                           '\"Convalesquence\"'])


    df_injuries = df_injuries.where((df_injuries['player_injury_reason'] != '\"Yellow Cards\"') & (df_injuries['player_injury_reason'] != '\"Suspended\"') &
                                               (df_injuries['player_injury_reason'] != '\"Rest') & (df_injuries['player_injury_reason'] != '\"Red Card\"') & 
                                               (df_injuries['player_injury_reason'] != '\"Personal Reasons\"') & 
                                               (df_injuries['player_injury_reason'] != '\"National selection\"') & 
                                               (df_injuries['player_injury_reason'] != '\"Loan agreement\"') & (df_injuries['player_injury_reason'] != '\"Injury\"') & 
                                               (df_injuries['player_injury_reason'] != '\"Coach\'s decision\"') & 
                                               (df_injuries['player_injury_reason'] != '\"Convalesquence\"'))

</div>

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

In \[26\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
data-type="inline">

<div class="CodeMirror cm-s-jupyter">

<div class="highlight hl-ipython3">

    df_injuries['row_number']= df_injuries.reset_index().index

    df_injuries = df_injuries.dropna()

    df_injuries_pivot_table = pd.pivot_table(df_injuries, index='player_injury_reason',columns=['league_season'],values='player_name',aggfunc="count")

    df_injuries_pivot_table

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper">

<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">

</div>

<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child jp-OutputArea-executeResult">

<div class="jp-OutputPrompt jp-OutputArea-prompt">

Out\[26\]:

</div>

<div
class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult"
mime-type="text/html">

<div>

| league_season            | 2020.0 | 2021.0 | 2022.0 | 2023.0 |
|--------------------------|--------|--------|--------|--------|
| player_injury_reason     |        |        |        |        |
| "Abdominal strain"       | 7.0    | 20.0   | 2.0    | NaN    |
| "Achilles Tendon Injury" | 2.0    | 50.0   | 125.0  | 44.0   |
| "Ankle Injury"           | 89.0   | 385.0  | 425.0  | 287.0  |
| "Arm Injury"             | 1.0    | 1.0    | 6.0    | NaN    |
| "Back Injury"            | 9.0    | 39.0   | 46.0   | 28.0   |
| "Broken Hand"            | NaN    | 1.0    | NaN    | 2.0    |
| "Broken Leg"             | 11.0   | 41.0   | 38.0   | 16.0   |
| "Broken ankle"           | 7.0    | 2.0    | NaN    | NaN    |
| "Broken calfbone"        | NaN    | NaN    | NaN    | 10.0   |
| "Broken collarbone"      | NaN    | NaN    | 15.0   | NaN    |
| "Broken nose"            | NaN    | 1.0    | 2.0    | NaN    |
| "Broken rib"             | NaN    | NaN    | 1.0    | NaN    |
| "Buttock Injury"         | 1.0    | NaN    | NaN    | NaN    |
| "Calf Injury"            | 61.0   | 188.0  | 265.0  | 135.0  |
| "Collarbone injury"      | NaN    | NaN    | 8.0    | NaN    |
| "Concussion"             | 8.0    | 1.0    | 7.0    | 1.0    |
| "Contusion"              | NaN    | NaN    | 5.0    | 7.0    |
| "Convalescence"          | NaN    | 4.0    | 1.0    | NaN    |
| "Elbow Injury"           | NaN    | 2.0    | NaN    | NaN    |
| "Eye injury"             | 2.0    | 6.0    | 2.0    | NaN    |
| "Face Injury"            | NaN    | NaN    | 4.0    | 6.0    |
| "Finger Injury"          | 11.0   | 11.0   | 24.0   | NaN    |
| "Foot Injury"            | 14.0   | 53.0   | 78.0   | 37.0   |
| "Groin Injury"           | 54.0   | 151.0  | 93.0   | 62.0   |
| "Hamstring Injury"       | NaN    | NaN    | 46.0   | 31.0   |
| "Hand Injury"            | NaN    | 1.0    | 3.0    | NaN    |
| "Head Injury"            | 3.0    | 16.0   | 21.0   | 7.0    |
| "Health problems"        | NaN    | NaN    | 19.0   | NaN    |
| "Heart Problems"         | NaN    | 5.0    | 3.0    | NaN    |
| "Heel Injury"            | NaN    | 4.0    | 7.0    | NaN    |
| "Hernia"                 | 12.0   | 9.0    | NaN    | NaN    |
| "Hip Injury"             | 19.0   | 48.0   | 25.0   | 38.0   |
| "Illness"                | 38.0   | 346.0  | 68.0   | 29.0   |
| "Inactive"               | NaN    | 36.0   | 80.0   | 11.0   |
| "Knee Injury"            | 334.0  | 796.0  | 1215.0 | 695.0  |
| "Knock"                  | 26.0   | 82.0   | 98.0   | 44.0   |
| "Lacking Match Fitness"  | NaN    | 39.0   | 85.0   | 9.0    |
| "Leg Injury"             | 24.0   | 77.0   | 91.0   | 8.0    |
| "Lower Back Injury"      | 4.0    | 31.0   | 2.0    | 4.0    |
| "Muscle Injury"          | 237.0  | 886.0  | 921.0  | 463.0  |
| "Neck Injury"            | NaN    | NaN    | 9.0    | NaN    |
| "Pelvis Injury"          | NaN    | NaN    | 7.0    | 2.0    |
| "Quarantine"             | 1.0    | 11.0   | NaN    | NaN    |
| "Rest"                   | 2.0    | 5.0    | 12.0   | 1.0    |
| "Ribs Injury"            | 1.0    | NaN    | NaN    | NaN    |
| "Shin Injury"            | 6.0    | 6.0    | NaN    | 2.0    |
| "Shoulder Injury"        | 21.0   | 78.0   | 71.0   | 40.0   |
| "Stomach Disorder"       | NaN    | 12.0   | 5.0    | NaN    |
| "Surgery"                | NaN    | 15.0   | NaN    | 10.0   |
| "Tendon Injury"          | 2.0    | 44.0   | 1.0    | 3.0    |
| "Thigh Injury"           | 92.0   | 519.0  | 586.0  | 297.0  |
| "Toe Injury"             | NaN    | 5.0    | 2.0    | 1.0    |
| "Wrist Injury"           | NaN    | 17.0   | 21.0   | 1.0    |

</div>

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
mime-type="text/markdown">

Esto nos puede dar una idea de las lesiones fisicas que sufren los
jugadores, pero vamos a tratar de ver estos datos de manera grafica

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
mime-type="text/markdown">

# Gafico lineal<a href="#Gafico-lineal" class="anchor-link">¶</a>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

In \[45\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
data-type="inline">

<div class="CodeMirror cm-s-jupyter">

<div class="highlight hl-ipython3">

    df_injuries_table = pd.pivot_table(df_injuries, index='league_season',columns='player_injury_reason',values='player_name',aggfunc="count")

    df_injuries_table

    figure = df_injuries_table.iplot(kind='line')

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper">

<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">

</div>

<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

<div class="jp-OutputPrompt jp-OutputArea-prompt">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output"
mime-type="text/html">

<div>

<div id="08e413cc-e02f-4143-adbf-ec2444d82c79" class="plotly-graph-div"
style="height:525px; width:100%;">

</div>

</div>

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
mime-type="text/markdown">

Con la grafica anterior, podemos ver datos, que la verdad no son
impactantes. Pues las lesiones mas comunes son las que son mas
llamativas, como la lesion de rodilla, u otros musculos.

Ademas, la grafica no es muy visual. Y ningun dato destaca.

Por ello vamos a buscar otra clase de datos, por ejemplo, el numero de
lesiones por temporada

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

In \[28\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
data-type="inline">

<div class="CodeMirror cm-s-jupyter">

<div class="highlight hl-ipython3">

    df_injuries_table = pd.pivot_table(df_injuries, index='league_season',columns='league_name',values='player_name',aggfunc="count")

    df_injuries_table

    df_injuries_table.iplot(kind='line')

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper">

<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">

</div>

<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

<div class="jp-OutputPrompt jp-OutputArea-prompt">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output"
mime-type="text/html">

<div>

<div id="29480386-d42e-4bc6-9994-fdffa9d69858" class="plotly-graph-div"
style="height:525px; width:100%;">

</div>

</div>

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
mime-type="text/markdown">

Ahora, podemos ver datos mas que interesantes, pues como con los años, o
al menos la tendencia durante las ultimas temporadas, es que cada vez
haya mas lesiones. En la temporada 2023, como aun no hemos llegado al
ecuador de la temporada es normal que los datos sean bajos.

Aun asi, llama la atencion que la Premier League, posee mas lesiones.
Esto puede deberse a diversos factores. Entre los mas habituales, puede
ser la exigencia de la liga, pues la Premier es durante ya muchas
temporadas la liga mas competitiva y exigente del mundo. Esto puede
tener consecuencias en sus jugadores. Aunque tambien podria deberse a
los cuidados y seguimientos realizados sobre los jugadores.

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
mime-type="text/markdown">

# Gafico de Cajas y Bigotes<a href="#Gafico-de-Cajas-y-Bigotes" class="anchor-link">¶</a>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

In \[42\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
data-type="inline">

<div class="CodeMirror cm-s-jupyter">

<div class="highlight hl-ipython3">

    df_injuries_table = pd.pivot_table(df_injuries, index='league_season',columns='league_name',values='player_name',aggfunc="count")

    df_injuries_table
    df_injuries_table.iplot(kind='box')

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper">

<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">

</div>

<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

<div class="jp-OutputPrompt jp-OutputArea-prompt">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output"
mime-type="text/html">

<div>

<div id="98f5c488-0dea-4554-9677-18c3942149d9" class="plotly-graph-div"
style="height:525px; width:100%;">

</div>

</div>

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
mime-type="text/markdown">

Desde la anterior grafica, podemos confirmar la diferencia de lesionados
entre las dos ligas. Pero en esta grafica, podemos ver las medias de
lesionados en ambas ligas. Sobre todo, llama la atencion, como La liga
posee un limite superior de lesionados mas bajo, frente al alto limite
que posee la premier. Podriamos seguir estudiando, o incluso, llegar a
predecir que la Premier, va a tener una tendencia de jugadores
lesionados cada vez mas alta.

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput"
mime-type="text/markdown">

# Grafico de Barras<a href="#Grafico-de-Barras" class="anchor-link">¶</a>

</div>

</div>

</div>

</div>

<div class="jp-Cell jp-CodeCell jp-Notebook-cell">

<div class="jp-Cell-inputWrapper">

<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">

</div>

<div class="jp-InputArea jp-Cell-inputArea">

<div class="jp-InputPrompt jp-InputArea-prompt">

In \[29\]:

</div>

<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor"
data-type="inline">

<div class="CodeMirror cm-s-jupyter">

<div class="highlight hl-ipython3">

    df_injuries_table.iplot(kind='bar')

</div>

</div>

</div>

</div>

</div>

<div class="jp-Cell-outputWrapper">

<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">

</div>

<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

<div class="jp-OutputPrompt jp-OutputArea-prompt">

</div>

<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output"
mime-type="text/html">

<div>

<div id="5c6c61ad-fd26-493a-9abc-27eee073be2c" class="plotly-graph-div"
style="height:525px; width:100%;">

</div>

</div>

</div>

</div>

</div>

</div>

</div>

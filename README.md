# conda_envs_table
__Creates an overview table of the installed conda environements__ including their installed packages and `conda.pth` info. Configuration is done using the `config.yaml` file and the resulting table is stored in the `envs_table.xlsx` file.

### Example
```
(base) C:\xxx\conda_envs_table>ipython make_table.ipynb
```
| env_name   | env_path                                | conda   | matplotlib   | pandas   | python   | plotly   | openpyxl   | flask   | pytest   | ipykernel   | ruamel.yaml   | pip    | pydantic   | numpy   |
|:-----------|:----------------------------------------|:--------|:-------------|:---------|:---------|:---------|:-----------|:--------|:---------|:------------|:--------------|:-------|:-----------|:--------|
| base       | C:\Users\xxx\anaconda3                | 23.11.0 | 3.7.2        | 2.0.3    | 3.11.5   | 5.9.0    | 3.0.10     | 2.2.2   | 7.4.0    | 6.25.0      | 0.17.21       | 23.2.1 | 1.10.8     | 1.24.3  |
| build_env  | C:\Users\xxx\anaconda3\envs\build_env | 23.11.0 |              |          | 3.11.7   |          |            |         |          |             | 0.18.5        | 23.3.1 |            |         |
| google     | C:\Users\xxx\anaconda3\envs\google    | 24.9.1  |              |          | 3.11.10  |          |            |         |          | 6.29.5      | 0.18.6        | 24.2   |            |         |
| influx     | C:\Users\xxx\anaconda3\envs\influx    |         | 3.8.3        | 2.2.1    | 3.12.2   | 5.21.0   | 3.1.2      |         |          | 6.29.3      | 0.18.6        | 24.0   | 2.6.3      | 1.26.4  |
| user_env   | C:\Users\xxx\anaconda3\envs\user_env  |         |              |          | 3.12.0   |          |            |         |          |             |               | 23.3.2 |            |         |

### Configuration
List the packages to be shown in the table in the `config.yaml` file:
```yaml
packages:
- conda
- flask
- ipykernel
- matplotlib
- numpy
- openpyxl
- pandas
- pip
- plotly
- pydantic
- pytest
- python
- ruamel.yaml
```

Leave `packages` empty (or comment out all packages) to show all:
```yaml
packages:
# - conda
# - flask
# - ipykernel
# - matplotlib
# - numpy
# - openpyxl
# - pandas
# - pip
# - plotly
# - pydantic
# - pytest
# - python
# - ruamel.yaml
```
# Encoding Reparative Description

This repository contains code related to the "Encoding Reparative Description"
project, which began in 2023 with a team of researchers at the
[University of Michigan School of Information](https://www.si.umich.edu/),
the [Bentley Historical Library](https://bentley.umich.edu/),
and the University of Michigan's [Humanities Collaboratory](https://sites.lsa.umich.edu/collaboratory/).

## Usage

### Inputs

There are two basic inputs for this tool, a **required** term list and an **optional** ArchivesSpace Resource ID list.

The required term list be a `.txt` file with one term per line, e.g.:

```
Civilization
Civilized
Uncivilized
Burial
Burials
...
```

See `terms-nativeAmerican.txt` and `terms-phillipines.txt` as examples.

Optionally, you may also provide a second `.txt` file with one ArchivesSpace Resouce ID per line, e.g.:

```
229
8482
4460
256
8480
...
```

If the user does not provide a `.txt` file with a list of Resource IDs, the tool will parse ALL ArchivesSpace resources. Since this is so resource intensive, the tool defaults to expecting a `.txt` file.

### Parse Resources

Run the `parse_resources.ipynb` Python notebook first. It takes the inputs above, along with a configuration file described in the notebook, and uses them to parse ArchivesSpace via the API. It produces a `.csv` file used in later operations--see `results-nativeAmerican.csv` and `results.phillipines.csv` as examples.

### Create a Terms in Context Report or Visualizations (or both)

#### Terms in Context Report

_Note that `kwic_report.ipynb` has been deprecated._ Run the `key_term_in_context.ipynb` Python notebook to create a key term in context report from the results. See `matched_results-nativeAmerican.csv` and `matched_results-phillipines.csv` as examples.

#### Visualizations

Run the `match_visualize.ipynb` Python notebook (or its companion, `match_visualize.html`) to create visualizations from the results. Optionally, save individual visualizations as `.png` files. See the following examples:

- `element_frequency_accross_dfs`
- `element_frequency_accross_dfs_stacked`
- `term_frequency_by_repo`
- `term_frequency_by_repo_horizbar`

# TODO: Don't forget to update titles

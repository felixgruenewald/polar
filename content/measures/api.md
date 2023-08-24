---
title: "API"
subtitle: Affective Polarisation Index
authors: more info here
date: 2023-06-24
publication: or here etc.
images: 
#math: true
---

## Info
- **Polarization**: [Affective](polarization/affective)
- **Level**: [Mass](/levels/mass)
- **Data**: [CSES](/data/cses)
- **Use cases**: [@wagner_affective_2021](/usecases/@wagner_affective_2021)

# Description
The (weighted) mean distance from the most liked party is a measure suggested by [@wagner_affective_2021](/usecases/@wagner_affective_2021), although he considers it inferior to the (weighted) [[spread]]. It measures the average discrepancy between like for the most liked party and like/dislike for all other parties. Wagner computes the (weighted) distance based on the CSES dataset, but in principle it can be applied to other datasets that contain the required items, i.e., like-dislike scores.
# Operationalization
Wagner proceeds in two steps. First, they calculate the (weighted) mean distance for each respondent. Second, they aggregate to the party-system level by taking the mean of the respondents' distance scores. The unweighted and weighted distance measures are calculated as follows:

Unweighted: $$Distance_i = \sqrt{\frac{\sum_{p=1}^p (like_{ip} - like_{max,i})^2}{n_p}}$$
Weighted: $$Distance_i = \sqrt{\sum_{p=1}^p v_p (like_{ip} - like_{max,i})^2}$$

The subscript $i$ denotes an individual respondent, $p$ denotes a party, $max$ is the most liked party, and $v_p$ is the percentage of votes received by a party.

# polaR code

```r
# Illustrative R code for coding the measure based on the CSES data
cses_imd <- polaR_import(source = "cses_imd", path = "datasets/cses/cses_imd.dta")

cses_imd <- distance(cses_imd)
```

# Use cases
<div class="block-language-dataview node-insert-event" style="overflow: auto; display: block"><table class="dataview table-view-table"><thead class="table-view-thead"><tr class="table-view-tr-header"><th class="table-view-th"><span>Authors</span></span></th><th class="table-view-th"><span>Year</span></th><th class="table-view-th"><span>Title</span></th><th class="table-view-th"><span>Publication</span></th><th class="table-view-th"><span>DOI</span></th></tr></thead><tbody class="table-view-tbody"><tr><td><span>Markus Wagner</span></td><td>2021</td><td><span>Affective polarization in multiparty systems</span></td><td><span>Electoral Studies</span></td><td><span><a data-tooltip-position="top" aria-label="https://doi.org/10.1016/j.electstud.2020.102199" rel="noopener" class="external-link" href="https://doi.org/10.1016/j.electstud.2020.102199" target="_blank">10.1016/j.electstud.2020.102199</a></span></td></tr></tbody></table></div>

# Data

<iframe src="https://felixgruenewald.shinyapps.io/polarapp/?dataset=cses&measure=api"
    frameborder="0"
    scrolling="yes" 
    style="overflow:hidden;width:100%" 
    height="1000" 
    width="100%"></iframe>
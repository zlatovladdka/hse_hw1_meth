# hse_hw1_meth
https://colab.research.google.com/drive/10p2Cl654V4QIH0AIC-N_-KPiPdcWW765?usp=sharing

## Часть 1

| Bisulfite | RNA |
| :-: | :-: |
| ![](img/bs_basic.png) | ![](img/rna_basic.png) | 
| ![](img/bs_seq_cont.png) | ![](img/rna_seq_cont.png) | 
| ![](img/bs_gc.png) | ![](img/rna_gc.png) | 
| ![](img/bs_dup.png) | ![](img/rna_dup.png) | 


## Часть 2

### Количество ридов, пришедшихся на целевые регионы, и число дуплицированных чтений

| Образец | 11347700-11367700 | 40185800-40195800 | % дупликаций |
| :----- | :-: | :-: | :-: |
| 8 Cell | 1090 | 464 | 18.31% |
| Epiblast | 2328 | 1062 | 2.92% |
| ICM | 1456 | 630 | 9.08% |


### Скрипт для параллельной дедупликации

```
!ls *pe.bam | xargs -P 4 -tI{} deduplicate_bismark  --bam  --paired  -o s_{} {}
```

### M-bias plot
![](img/6473_1.png)
![](img/6473_2.png)

![](img/4222_1.png)
![](img/4222_2.png)

![](img/6475_1.png)
![](img/6475_2.png)

### Гистограммы уровня метилирования

![](img/5836473.png)
![](img/3824222.png)
![](img/5836475.png)

### Визуализация уровня метилирования и покрытия

![](img/img_meth.png)
![](img/img_cov.png)

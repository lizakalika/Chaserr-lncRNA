# Chaserr-lncRNA

## Регионы связывания Chaserr

1. Проведен подробный анализ связывания Chaserr с другими РНК с помощью ASSA в фибробластах мыши и человека. Подробно смотреть https://github.com/vanya-antonov/chaserr-human-mouse.

2. Необходимо провести аналогичный анализ для нейрональных клеток (N2a) - изначальный файл с данными - N2aMergedWithEmb_ForYulia.txt. 

В файле данные дня 4 типов клеток:

- resASO - an ASO targeting Chaserr, which leads to changes similar to those we see in the Chaserr-/- mEFs

- resGapmer - a Gapmer targeting Chaserr, which leads to largely different changes, we think its because of a technical problem in RNA extraction, which is messing things up

- resCHD2 - a Gapmer targeting (and strongly reducing) Chd2

- OEChaserr - Chaserr sequence over-expression in N2a cells

В файле даны уже нормализованные каунты и посчитаны экспрессии, вероятно, при помощи DESeq2. Также, в файле удалены все гены с нулевой экспрессией.

2.1 resASO
Если использовать результаты, уже данные в файле, то получается, всего 27 ДЕГов, из которых 5 пересекаются с ДЕГами для фибробластов (adjusted p-value < 0.05), среди них есть Chd2. При расчете дифф экспрессии при помощи limma на уже нормализованных каунтах получается, что ДЕГов нет совсем. 

2.2 Был сделан PCA

2.3. Рассчитана дифф. экспрессия для реплик 3, 4, 5 в лимме. 

padj < 0.05: 58 DEGов, из них 29 пересекаются с фибробластами

padj < 0.1: 516 DEGов, из них 247 пересекаются с фибробластами

padj (Chd2) = 0.098

2.4. Рассчитана дифф. экспрессия для реплик 1, 3, 4, 5 в лимме. 
ДЭГов нет



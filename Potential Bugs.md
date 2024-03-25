• **Improving Time-Series Momentum**

-   path \<- paste0(getwd(),"/sandbox/data/FuturesData/data/Balta-Kosowski")

-   LoadFuturesData(symbols = symbols, path = path) is bugged. There is no such folder called FuturesData in sandbox/data folder

• **Time-Series Momentum**

-   data \<- data.frame( DATE=ff.dates, data[ff.dates, ], row.names=NULL ) is bugged as there is a mismatch in data length between ff.dates and data[ff.dates, ]

-   The date in data is Jan.1927 while ff.dates can be "1927-01-01" "1927-01-29", which creates the discrepancy in length.

• **Value and Momentum Everywhere**

-   parser.path \<- system.file('parsers',\
    'Devil-in-HML-Details.R', package='ExpectedReturns') is bugged

-   The correct form should be parser.path \<- system.file('parsers',\
    ' Value--Devil-in-HMLs-Details.R’, package='ExpectedReturns')

-   #VME.FACTORS \<- VME.Factors.orig[, c('VAL.EVR', 'MOM.EVR')] VME.FACTORS \<- VME.Factors[, c('VAL.EVR', 'MOM.EVR')] is bugged

-   VME.FACTORS \<- VME.Factors.orig[, c('VAL.EVR', 'MOM.EVR')] #VME.FACTORS \<- VME.Factors[, c('VAL.EVR', 'MOM.EVR')] works for me.

-   ts.reg \<- plm::pmg(EXC.RET \~ MSCI.RF + VAL.EVR + MOM.EVR, data=portfoliosDT, index=c('PORTF.ID', 'DATE.ID') ) is bugged

-   portfoliosDT dataset does not contain MSCI.RF, VAL.EVR, MOM.EVR

• **Expected Return Replication**

-   data("factorDataSetDjia5Yrs") might be bugged. The file might be corrupted. I tried my best to open this dataset by even clicking the dataset directly.

• **Which Factors?**

-   data.qbs \<- data.qbs['1967-01/2016-12'] is bugged as data.qbs is an empty data structure by this point. It is caused by data.qbs \<- data.qbs[complete.cases(data.qbs), unique(c(q5.vars, bs6.vars))] as data.qbs contained missing or NA values that would make the result an empty structure.

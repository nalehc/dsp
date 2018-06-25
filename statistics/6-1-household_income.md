[Think Stats Chapter 6 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2007.html#toc60) (household income)

```
import numpy as np
import brfss
import thinkstats2
import thinkplot
import hinc

def InterpolateSample(df, log_upper=6.0):
    df['log_upper'] = np.log10(df.income)
    df['log_lower'] = df.log_upper.shift(1)
    df.loc[0, 'log_lower'] = 3.0
    df.loc[41, 'log_upper'] = log_upper
    arrays = []
    for _, row in df.iterrows():
        vals = np.linspace(row.log_lower, row.log_upper, row.freq)
        arrays.append(vals)
    log_sample = np.concatenate(arrays)
    return log_sample
    
income_df = hinc.ReadData()
log_sample = InterpolateSample(income_df, log_upper=6.0)

log_cdflog_cdf  ==  thinkstats2thinksta .Cdf(log_sample)
thinkplot.Cdf(log_cdf)
thinkplot.Config(xlabel='Household income (log $)',
               ylabel='CDF')
print(Mean(sample), Median(sample), Skewness(sample), PearsonMedianSkewness(sample), cdf.Prob(Mean(sample)))

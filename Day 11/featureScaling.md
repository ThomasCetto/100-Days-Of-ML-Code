# Feature scaling

Feature scaling is important because it make sure that every feature has the right weight in the model training. That's because if feature x has a range that goes from 0 to 100.000, it will have a bigger influence than feature y that goes from 0 to 30.

To solve this problem we have to normalize the values of both variables, and it can be made with different techniques:
- maximum absolute scaling
- min-max feature scaling
- z-score method
- Robust scaling


### Maximum absolute scaling

It rescales each feature between -1 and 1 by dividing every observation by its maximum absolute value.

![formula](https://miro.medium.com/v2/resize:fit:466/format:webp/1*qa_W9JzNscAXpTtc44yhow.png)

*Important:* it's very sensitive to outliers because a single outlier can influence the minumum and maximum values and have a big effect on the results.

### Min-max feature scaling
It's also called normalization, and it rescales the feature to a fixed range of [0,1] by subtracting the minimum value of the feature and then dividing by the range.

![formula](https://miro.medium.com/v2/resize:fit:480/format:webp/1*wJqdWdLdjBJqGbaDRWVZnQ.png)

*Important:* it's very sensitive to outliers because a single outlier can influence the minumum and maximum values and have a big effect on the results.


### Z-score method
It's also called standardization, and it transforms the data into a distribution with a mean of 0 and a standard deviation of 1. Each value is computed by subtracting the mean of the feature and then dividing by the standard deviation. It doesn't rescale the feature to a fixed range, but 99% of data ranges from -3.00 to 3.00 if the input is normally distributed.

![formula](https://miro.medium.com/v2/resize:fit:346/format:webp/1*Qy9qhRvqU0pOfADth0Njhw.png)

![distribution raffiguration](https://miro.medium.com/v2/resize:fit:828/format:webp/1*cDUtW2cNIZ7L5XrdOkiucQ.png)


### Robust scaling 

Every feature gets scaled by subtracting the median and then dividing by the interquartile range (the difference between the third and the first quartile, that represents 50% of the data).

![formula](https://miro.medium.com/v2/resize:fit:514/format:webp/1*IB6PRhdSwVkOR9AyI_bhyg.png)

where Q1(x) is the first quartile of the attribute x, Q2(x) is the median, and Q3(x) is the third quartile.

It's useful when working with datasets that contain many outliers, because median and interquartile range are very robust to them. 

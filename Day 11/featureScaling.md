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


# veri_bilimi_projesi

airline passenger veri setinde modelleme yapabilmek adına train.csv seti pythonla new_train.csv (ham verinin %75'i) 
ve validation.csv (ham verinin %25'i) olarak ikiye bölünmüştür. 

```python3
import pandas as pd
from sklearn.model_selection import train_test_split

train_df = pd.read_csv("train.csv")

train_part, valid_part = train_test_split(train_df, test_size=0.25, random_state=42)

train_part.to_csv("new_train.csv", index=False)
valid_part.to_csv("validation.csv", index=False)
```
 

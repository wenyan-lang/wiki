```wenyan
吾嘗觀「「算經」」之書。方悟「正弦」「餘弦」「圓周率」之義。
```

```python
from math import sin, cos, pi
```

`今有` is used for exported/public variables, while `吾有` is private/scoped.

Example:

`易經.wy` (a.k.a. Random)

```wenyan
吾有一數。曰四十二。名之曰「運數」。

今有一術。名之曰「運」。欲行是術。必先得一數。曰「甲」。乃行是術曰。
	注曰「「運者。隨機種子也」」
	昔之「運數」者。今「甲」是矣。
是謂「運」之術也。

今有一術。名之曰「占」。是術曰。
	注曰「「線性同餘方法所得隨機數也」」
	有數四十二億九千四百九十六萬七千二百九十六。名之曰「模」。
	有數二千二百六十九萬五千四百七十七。名之曰「倍」。
	有數一。名之曰「增」。
	乘「倍」以「運數」。加其以「增」。除其以「模」。所餘幾何。昔之「運數」者。今其是矣。
	除「運數」以「模」。名之曰「卦」。
	乃得「卦」。
是謂「占」之術也。
```

`some_example.wy` (where you import random)

```wenyan
吾嘗觀「「易經」」之書。方悟「占」之義。
施「占」。書之。
```

Notice that in `易經.wy` the random seed (運數) is not exported. while its setter (運) is exported, but not imported by `some_example.wy`. Only `占` the generator is exported and imported, and can be used directly.

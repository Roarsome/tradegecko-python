Issues encountered with the original codes written in Python2.

For example:
The `endpoints` cannot be found when `import tradegecko`.

Therefore, ...
1. Small modifications have been made to the `import` statement for codes to work in Python3.
2. Unnecessary files have been removed so that the modified repository is appropriate to be called directly by `pip3 install`.

In addition, the code is updated to support filtering same field with diff values. For example:

```
from tradegecko import TradeGeckoRestClient
from pprint import pprint

tg = TradeGeckoRestClient("insert-your-secret-access-token-here")

# Example to use filter() to get a few variants by the sku id
pprint(tg.variant.filter(
    ('sku[]', '1234'), 
    ('sku[]', 'abcd')
))
```


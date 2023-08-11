---
Publishing date: "2023-08-03 15:36"
Category: "Алгоритм"
aliases:
- "бутстрап"
- "бустреп"
---
#code #bootstrap #AB_test #ML 

---
## Implementation

```python
from typing import Iterable, Optional
import numpy as np
import numpy.typing as npt
from joblib.parallel import Parallel, delayed


_BS_FUNCTIONS = {
	'mean': np.mean
}

def bootstrap(
    values: Iterable[np.number],
	*,
	agg_func: str = 'mean',
	n_samples: int = 100,
	n_jobs: int = 1,
	verbose: int = 0,
	seed: Optional[int] = None

):

	def _get_random_sample(values, agg_func):
		rng = np.random.default_rng(seed=seed)
		return _BS_FUNCTIONS[agg_func](
			rng.choice(
				a=values,
				size=values.shape[0],
				replace=True
			)
		)

	return Parallel(n_jobs=n_jobs, verbose=verbose)(
		delayed(_get_random_sample)(values, agg_func)
		for _ in range(n_samples)
	)
```
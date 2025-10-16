# The dorion_francois package

* Provided along with the Dorion & François textbook
* Parts are used in the backend of the delta_vega software

## Some coding conventions

Ideally, as the code matures, it will adhere to [PEP8](https://peps.python.org/pep-0008/) and use the [github docstrings](https://github.com/google/styleguide/blob/gh-pages/pyguide.md#38-comments-and-docstrings) format. That said, perhaps the most important quote from the PEP8 is 

> Some other good reasons to ignore a particular guideline:
> When applying the guideline would make the code less
> readable, even for someone who is used to reading code
> that follows this PEP.

In particular, as this code follows a book, we'll adhere to the book's notation whenever possible. Besides, here are some specific conventions we'll adhere to herein:

* **Avoid single-letter variable names**, even for (e.g.) loop variables. Using:

```for no in range(10)```

makes it much easier to search (and potentially replace) for `no` than it would have been for `n`. 

* When single variable names are used, they should be capitalized. Somme common examples are `S`, `K`, and `T` for stock, strike, and maturity. As in the book, `T` will typically be _the_ maturity, so that a given time $t$ (often `tt` or `time_t` in the code), the time _left_ to maturity is `T - time_t`.

* We'll typically use `_` for subscripts (in line with LaTeX), and simply concatenate a superscript to the variable name. That is, for some $S^n_j$, we'll use `Sn_j` in the code.

* In general, we'll use the following conventions:

```
some_local_or_global_var = None

class ClassName(ParentClass):
    def __init__(self):
        self.field_name = "allows single ' within"
        
    def method_name(self):
        local_var = some_global_function(self.field_name)
        # do stuff...
        return local_var
```

Another important PEP8 quote is: 

> ```Capitalized_Words_With_Underscores``` (**ugly!**)

where the emphasis is my own... and should be self-explanatory.

### Time as row index, Path number as column index

Numpy is (by default) row-major (https://en.wikipedia.org/wiki/Row-_and_column-major_order).
Applications in finance usually allow vectorization across columns, but often cannot vectorize
across time. Hence, accessing array[t,:] allow using a vector that is contiguously stored in
memory, making vectorization more efficient.


### Asserts and warnings

As a rule, if your code relies on some assumption, or is expected to produce some kind of
result, make sure to
```
    assert ASSUMPTION_HOLDS, 'Assumption does not hold, will result in unexpected behaviour'
```
Even if it seems highly unlikely when writing your code that the assumption would ever be
violated, the code will evolve and sanity checks makes your bit more robust.

Besides, warnings are also important.

1. In the case of warnings arising from external libraries: **never** neglect them. Fix the code.

2. Internally, we often use warnings for features that are not stable, that need to be revisit,
or are missing altogether. Do **not** comment them while developing your code, you'd risk
forgetting to uncomment them. See how to catch them here:

https://docs.python.org/3/library/warnings.html#temporarily-suppressing-warnings

### Imports

This header (proprietary dv/score.py, as of 2023/05/09) exemplifies how imports would ideally be dealt with:

```
from datetime import date
import numpy as np
import pandas as pd
import warnings

from dorion_francois.jupyter_notebook import struct,numunique,nansum, tic,toc
from dorion_francois.toolkit import datetime2yyyymmdd, date2str

import data_management
from model import ModelDV0
from structured_note import StructuredNote

import socket
__hostname = socket.gethostname()
POOL_SIZE = 8
if __hostname.startswith('vulcan'):
    POOL_SIZE = 8
elif __hostname.startswith('svarog'):
    POOL_SIZE = 16
```

The first block consists of standard python packages, in alphabetic order.

The second block, external libraries made available locally. Note that, when importing "helper
functions", its much preferable **not** to `form [...] import *` but actually list the exact
functions needed.

The third block is local, private code.

The fourth block is an exception, where the package is imported right before some specific
treatment. This make the dependency clear, and suggests that we can simply remove this import
if/when the block is (re)moved.

### The dorion_francois package uses relative imports

It is important to note that *within* the dorion_francois package, we have opted for [relative imports](https://realpython.com/absolute-vs-relative-python-imports/). **Do not modify** this behavior locally if you plan to contribute to the project. It takes a minute becoming familiar with relative imports, but once you do, they are pretty straightforward.

## Some notes on git 

### Your first git commit

Please confirm that if you enter

`git status`

on the command line, you get a message that starts with:

```
git status
On branch <your_branch>
...
```

[Do not contribute on the main branch; those contributions would be rolled back.] Then, add a test file, performing the following operations: 

```
echo "my test" > my_test.log
git add my_test.log
git commit -m "Adding a file to test git push"
git push -v
```

Do not hesitate to contact us if you encounter an issue that your favorite chat bot cannot resolve.

### Updating a single file

```
git fetch 
git checkout FETCH_HEAD -- README.md 
```

### git pull error?

After

```
svarog % git pull
remote: Enumerating objects: 8, done.
remote: Counting objects: 100% (8/8), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 8 (delta 5), reused 8 (delta 5)
Unpacking objects: 100% (8/8), 2.33 KiB | 477.00 KiB/s, done.
From git.assembla.com:dorion-francois
   e9c7d09..96cff33  main          -> origin/main
 * [new branch]      dv_nicolas_b0 -> origin/dv_nicolas_b0
 * [new branch]      dv_weiyu_b0   -> origin/dv_weiyu_b0
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint: 
hint:   git config pull.rebase false  # merge
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint: 
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
fatal: Need to specify how to reconcile divergent branches.
```

This usually is the solution: `git pull --rebase --no-commit`. See [this page](https://stackoverflow.com/questions/2472254/when-should-i-use-git-pull-rebase). The `git pull --help` might also help you understand what is going on behind the scenes.

### git merge main into "feature" branch

Please **NEVER** merge your branch into the `main`; this is the CSO's job. But you might need code from the main branch (or we can do this for you at first...)

To get code updates from the main branch, first updating the local copy of the main:

```
$ git checkout main
$ git pull --rebase
$ git checkout your_branch
$ git merge main
$ git push
```

What if a **conflict** occurs during the merge step? A simple possibility:

`git checkout --theirs README.md`

fully disregarding the local changes, or manually resolve the conflict file and, then:

`git commit -am "Conflicts resolved"`
Please always report problems by filling an issue here on GitHub. This also covers reporting problems with the documentation (e.g. if sth is unclear).

General rules:

    1. the code style suggestions of PyCharm should be followed

Job general:

    1. If a class inherits directly/indirectly from the sisyphus class `Job` the class ends with "Job".
    2. In a Sisyphus job class the output variables end in `out_*`

Job constructor order:

    1. set inputs
    2. set outputs (should be prefixed with `out_`)
    3. define rqmt

Job function order:

    1. `__init__`
    2. `tasks()`
    3. task functions
    4. helper functions
    5. class functions
    6. `__hash__`

Rasr-Jobs:
should always accept `crp`, `extra_config` + `extra_post_config`

Import order:

    1. standard library
    2. external libraries (including sisyphus, yes I know it's not like that atm)
    3. recipies

Some general things:

    1. Don't break a jobs hash
    2. Really don't break a jobs hash
    3. very strong preference to avoid config files / scripts in the recipe repo itself. Everything should be code
    4. Jobs should be as deterministic as possible
    5. `sh` function should definitely not be used

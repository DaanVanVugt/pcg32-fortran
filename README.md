# Wrapper module for the pcg32 rng in fortran
Files pcg_basic.{c,h} are adapted from the [basic version of the PCG RNG](https://github.com/imneme/pcg-c-basic) to include an efficient way to generate doubles.

## How to use
```fortran
type(pcg_state_setseq_64), :: state

! Initialize
call pcg32_srandom_r(state, int(seed, 8), int(i_stream, 8))

! Fill out with doubles between 0 and 1
call pcg32_random_doubles_r(state, out)
```

## Authors

* Daan van Vugt <daanvanvugt@gmail.com>

## License
This code is released under the Apache license, to be found in the file LICENSE.

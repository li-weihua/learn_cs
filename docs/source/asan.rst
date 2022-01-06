asan: Address Sanitizer
=========================

Asan with NVIDIA CUDA api will fail
-------------------------------------

Ref to: https://github.com/google/sanitizers/issues/629

solution
::

    export ASAN_OPTIONS=protect_shadow_gap=0
    ./cmd

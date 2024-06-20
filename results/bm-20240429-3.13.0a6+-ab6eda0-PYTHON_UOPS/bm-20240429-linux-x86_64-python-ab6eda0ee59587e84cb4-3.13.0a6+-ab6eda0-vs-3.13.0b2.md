# Results vs. 3.13.0b2

- fork: python
- ref: ab6eda0ee59587e84cb4
- machine: linux-x86_64
- commit hash: ab6eda0
- commit date: 2024-04-29
- overall geometric mean: 1.24x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 361 ms: 1.32x slower                                                   |
| chameleon      | 7.22 ms                                                    | 8.68 ms: 1.20x slower                                                  |
| docutils       | 2.83 sec                                                   | 3.37 sec: 1.19x slower                                                 |
| html5lib       | 67.2 ms                                                    | 79.8 ms: 1.19x slower                                                  |
| tornado_http   | 94.6 ms                                                    | 105 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                      | 1.20x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 393 ms: 1.04x slower                                                   |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 651 ms: 1.06x slower                                                   |
| async_tree_io              | 939 ms                                                     | 1.00 sec: 1.07x slower                                                 |
| async_tree_io_tg           | 936 ms                                                     | 999 ms: 1.07x slower                                                   |
| async_tree_memoization_tg  | 444 ms                                                     | 476 ms: 1.07x slower                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 636 ms: 1.08x slower                                                   |
| async_tree_none_tg         | 336 ms                                                     | 366 ms: 1.09x slower                                                   |
| async_tree_memoization     | 463 ms                                                     | 526 ms: 1.13x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.08x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 194 ms: 1.01x slower                                                   |
| float          | 78.9 ms                                                    | 122 ms: 1.55x slower                                                   |
| nbody          | 88.3 ms                                                    | 198 ms: 2.25x slower                                                   |
| Geometric mean | (ref)                                                      | 1.52x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.73 ms: 1.02x slower                                                  |
| regex_v8       | 25.1 ms                                                    | 25.6 ms: 1.02x slower                                                  |
| regex_dna      | 221 ms                                                     | 226 ms: 1.02x slower                                                   |
| regex_compile  | 137 ms                                                     | 220 ms: 1.61x slower                                                   |
| Geometric mean | (ref)                                                      | 1.14x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 151 ms: 1.07x faster                                                   |
| json_loads           | 28.9 us                                                    | 27.6 us: 1.05x faster                                                  |
| unpickle_list        | 5.34 us                                                    | 5.13 us: 1.04x faster                                                  |
| pickle_dict          | 34.8 us                                                    | 35.3 us: 1.01x slower                                                  |
| pickle_pure_python   | 305 us                                                     | 318 us: 1.04x slower                                                   |
| pickle               | 11.5 us                                                    | 12.0 us: 1.04x slower                                                  |
| xml_etree_iterparse  | 107 ms                                                     | 126 ms: 1.17x slower                                                   |
| xml_etree_generate   | 87.4 ms                                                    | 104 ms: 1.18x slower                                                   |
| xml_etree_process    | 61.2 ms                                                    | 74.1 ms: 1.21x slower                                                  |
| tomli_loads          | 2.12 sec                                                   | 3.38 sec: 1.59x slower                                                 |
| unpickle_pure_python | 218 us                                                     | 396 us: 1.81x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.12x slower                                                           |

Benchmark hidden because not significant (3): pickle_list, json_dumps, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                                  |
| python_startup_no_site | 7.11 ms                                                    | 7.19 ms: 1.01x slower                                                  |
| Geometric mean         | (ref)                                                      | 1.00x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 34.8 ms                                                    | 47.3 ms: 1.36x slower                                                  |
| genshi_xml      | 51.6 ms                                                    | 80.6 ms: 1.56x slower                                                  |
| genshi_text     | 23.7 ms                                                    | 39.3 ms: 1.66x slower                                                  |
| mako            | 11.2 ms                                                    | 20.3 ms: 1.81x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.59x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse            | 162 ms                                                     | 151 ms: 1.07x faster                                                   |
| json_loads                 | 28.9 us                                                    | 27.6 us: 1.05x faster                                                  |
| unpickle_list              | 5.34 us                                                    | 5.13 us: 1.04x faster                                                  |
| json                       | 5.31 ms                                                    | 5.21 ms: 1.02x faster                                                  |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                                  |
| gc_traversal               | 3.98 ms                                                    | 3.93 ms: 1.01x faster                                                  |
| bench_mp_pool              | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.11 ms                                                    | 7.19 ms: 1.01x slower                                                  |
| pidigits                   | 191 ms                                                     | 194 ms: 1.01x slower                                                   |
| pickle_dict                | 34.8 us                                                    | 35.3 us: 1.01x slower                                                  |
| regex_effbot               | 3.67 ms                                                    | 3.73 ms: 1.02x slower                                                  |
| regex_v8                   | 25.1 ms                                                    | 25.6 ms: 1.02x slower                                                  |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.88 sec: 1.02x slower                                                 |
| regex_dna                  | 221 ms                                                     | 226 ms: 1.02x slower                                                   |
| logging_silent             | 105 ns                                                     | 108 ns: 1.03x slower                                                   |
| thrift                     | 823 us                                                     | 854 us: 1.04x slower                                                   |
| async_tree_none            | 378 ms                                                     | 393 ms: 1.04x slower                                                   |
| sqlite_synth               | 2.99 us                                                    | 3.11 us: 1.04x slower                                                  |
| pickle_pure_python         | 305 us                                                     | 318 us: 1.04x slower                                                   |
| asyncio_tcp                | 508 ms                                                     | 530 ms: 1.04x slower                                                   |
| pickle                     | 11.5 us                                                    | 12.0 us: 1.04x slower                                                  |
| djangocms                  | 31.5 us                                                    | 33.1 us: 1.05x slower                                                  |
| coroutines                 | 23.2 ms                                                    | 24.5 ms: 1.06x slower                                                  |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 651 ms: 1.06x slower                                                   |
| async_tree_io              | 939 ms                                                     | 1.00 sec: 1.07x slower                                                 |
| async_tree_io_tg           | 936 ms                                                     | 999 ms: 1.07x slower                                                   |
| async_tree_memoization_tg  | 444 ms                                                     | 476 ms: 1.07x slower                                                   |
| dask                       | 369 ms                                                     | 397 ms: 1.07x slower                                                   |
| generators                 | 29.6 ms                                                    | 31.8 ms: 1.07x slower                                                  |
| gunicorn                   | 1.28 ms                                                    | 1.37 ms: 1.07x slower                                                  |
| aiohttp                    | 1.18 ms                                                    | 1.28 ms: 1.08x slower                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 636 ms: 1.08x slower                                                   |
| async_tree_none_tg         | 336 ms                                                     | 366 ms: 1.09x slower                                                   |
| pathlib                    | 17.3 ms                                                    | 19.2 ms: 1.11x slower                                                  |
| tornado_http               | 94.6 ms                                                    | 105 ms: 1.11x slower                                                   |
| deepcopy                   | 367 us                                                     | 409 us: 1.11x slower                                                   |
| async_generators           | 442 ms                                                     | 496 ms: 1.12x slower                                                   |
| mdp                        | 2.79 sec                                                   | 3.13 sec: 1.12x slower                                                 |
| async_tree_memoization     | 463 ms                                                     | 526 ms: 1.13x slower                                                   |
| telco                      | 8.41 ms                                                    | 9.64 ms: 1.15x slower                                                  |
| dulwich_log                | 67.2 ms                                                    | 77.4 ms: 1.15x slower                                                  |
| pycparser                  | 1.16 sec                                                   | 1.34 sec: 1.15x slower                                                 |
| bench_thread_pool          | 834 us                                                     | 973 us: 1.17x slower                                                   |
| xml_etree_iterparse        | 107 ms                                                     | 126 ms: 1.17x slower                                                   |
| mypy2                      | 742 ms                                                     | 874 ms: 1.18x slower                                                   |
| xml_etree_generate         | 87.4 ms                                                    | 104 ms: 1.18x slower                                                   |
| html5lib                   | 67.2 ms                                                    | 79.8 ms: 1.19x slower                                                  |
| sqlglot_transpile          | 1.63 ms                                                    | 1.94 ms: 1.19x slower                                                  |
| docutils                   | 2.83 sec                                                   | 3.37 sec: 1.19x slower                                                 |
| chameleon                  | 7.22 ms                                                    | 8.68 ms: 1.20x slower                                                  |
| sqlglot_parse              | 1.32 ms                                                    | 1.59 ms: 1.21x slower                                                  |
| xml_etree_process          | 61.2 ms                                                    | 74.1 ms: 1.21x slower                                                  |
| logging_format             | 6.47 us                                                    | 7.88 us: 1.22x slower                                                  |
| pylint                     | 317 ms                                                     | 387 ms: 1.22x slower                                                   |
| sympy_sum                  | 156 ms                                                     | 192 ms: 1.23x slower                                                   |
| logging_simple             | 5.74 us                                                    | 7.08 us: 1.23x slower                                                  |
| sympy_expand               | 473 ms                                                     | 585 ms: 1.24x slower                                                   |
| deepcopy_memo              | 39.7 us                                                    | 50.1 us: 1.26x slower                                                  |
| sympy_str                  | 282 ms                                                     | 360 ms: 1.27x slower                                                   |
| sqlglot_normalize          | 110 ms                                                     | 142 ms: 1.29x slower                                                   |
| meteor_contest             | 110 ms                                                     | 143 ms: 1.30x slower                                                   |
| 2to3                       | 274 ms                                                     | 361 ms: 1.32x slower                                                   |
| typing_runtime_protocols   | 165 us                                                     | 217 us: 1.32x slower                                                   |
| sqlglot_optimize           | 55.5 ms                                                    | 73.5 ms: 1.32x slower                                                  |
| sympy_integrate            | 20.5 ms                                                    | 27.7 ms: 1.35x slower                                                  |
| django_template            | 34.8 ms                                                    | 47.3 ms: 1.36x slower                                                  |
| richards_super             | 57.4 ms                                                    | 78.6 ms: 1.37x slower                                                  |
| scimark_sor                | 127 ms                                                     | 178 ms: 1.39x slower                                                   |
| richards                   | 50.9 ms                                                    | 71.6 ms: 1.41x slower                                                  |
| raytrace                   | 267 ms                                                     | 376 ms: 1.41x slower                                                   |
| scimark_fft                | 392 ms                                                     | 596 ms: 1.52x slower                                                   |
| float                      | 78.9 ms                                                    | 122 ms: 1.55x slower                                                   |
| genshi_xml                 | 51.6 ms                                                    | 80.6 ms: 1.56x slower                                                  |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 8.26 ms: 1.57x slower                                                  |
| crypto_pyaes               | 77.5 ms                                                    | 122 ms: 1.57x slower                                                   |
| tomli_loads                | 2.12 sec                                                   | 3.38 sec: 1.59x slower                                                 |
| regex_compile              | 137 ms                                                     | 220 ms: 1.61x slower                                                   |
| scimark_lu                 | 122 ms                                                     | 201 ms: 1.66x slower                                                   |
| genshi_text                | 23.7 ms                                                    | 39.3 ms: 1.66x slower                                                  |
| deltablue                  | 3.25 ms                                                    | 5.41 ms: 1.66x slower                                                  |
| chaos                      | 61.3 ms                                                    | 103 ms: 1.68x slower                                                   |
| pprint_safe_repr           | 758 ms                                                     | 1.28 sec: 1.69x slower                                                 |
| pprint_pformat             | 1.56 sec                                                   | 2.65 sec: 1.71x slower                                                 |
| pyflate                    | 484 ms                                                     | 828 ms: 1.71x slower                                                   |
| fannkuch                   | 402 ms                                                     | 693 ms: 1.72x slower                                                   |
| go                         | 145 ms                                                     | 260 ms: 1.80x slower                                                   |
| mako                       | 11.2 ms                                                    | 20.3 ms: 1.81x slower                                                  |
| unpickle_pure_python       | 218 us                                                     | 396 us: 1.81x slower                                                   |
| spectral_norm              | 116 ms                                                     | 211 ms: 1.82x slower                                                   |
| nqueens                    | 81.4 ms                                                    | 151 ms: 1.86x slower                                                   |
| scimark_monte_carlo        | 69.2 ms                                                    | 134 ms: 1.94x slower                                                   |
| comprehensions             | 16.6 us                                                    | 37.2 us: 2.24x slower                                                  |
| nbody                      | 88.3 ms                                                    | 198 ms: 2.25x slower                                                   |
| hexiom                     | 6.30 ms                                                    | 15.0 ms: 2.39x slower                                                  |
| Geometric mean             | (ref)                                                      | 1.24x slower                                                           |

Benchmark hidden because not significant (7): create_gc_cycles, coverage, deepcopy_reduce, pickle_list, asyncio_websockets, json_dumps, unpickle
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.17x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 0.99x
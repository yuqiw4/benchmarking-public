# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: tier_2_yield_value
- machine: linux-x86_64
- commit hash: 3e1b870
- commit date: 2024-04-29
- overall geometric mean: 1.25x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 361 ms: 1.32x slower                                                           |
| chameleon      | 7.22 ms                                                    | 8.81 ms: 1.22x slower                                                          |
| docutils       | 2.83 sec                                                   | 3.37 sec: 1.19x slower                                                         |
| html5lib       | 67.2 ms                                                    | 81.2 ms: 1.21x slower                                                          |
| tornado_http   | 94.6 ms                                                    | 105 ms: 1.11x slower                                                           |
| Geometric mean | (ref)                                                      | 1.21x slower                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 393 ms: 1.04x slower                                                           |
| async_tree_io_tg           | 936 ms                                                     | 986 ms: 1.05x slower                                                           |
| async_tree_io              | 939 ms                                                     | 1.00 sec: 1.07x slower                                                         |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 658 ms: 1.08x slower                                                           |
| async_tree_memoization_tg  | 444 ms                                                     | 478 ms: 1.08x slower                                                           |
| async_tree_none_tg         | 336 ms                                                     | 366 ms: 1.09x slower                                                           |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 643 ms: 1.09x slower                                                           |
| async_tree_memoization     | 463 ms                                                     | 526 ms: 1.14x slower                                                           |
| Geometric mean             | (ref)                                                      | 1.08x slower                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 194 ms: 1.01x slower                                                           |
| float          | 78.9 ms                                                    | 129 ms: 1.63x slower                                                           |
| nbody          | 88.3 ms                                                    | 197 ms: 2.23x slower                                                           |
| Geometric mean | (ref)                                                      | 1.54x slower                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.74 ms: 1.02x slower                                                          |
| regex_dna      | 221 ms                                                     | 226 ms: 1.02x slower                                                           |
| regex_v8       | 25.1 ms                                                    | 26.4 ms: 1.05x slower                                                          |
| regex_compile  | 137 ms                                                     | 223 ms: 1.63x slower                                                           |
| Geometric mean | (ref)                                                      | 1.16x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| json_loads           | 28.9 us                                                    | 27.5 us: 1.05x faster                                                          |
| xml_etree_parse      | 162 ms                                                     | 154 ms: 1.05x faster                                                           |
| unpickle             | 15.1 us                                                    | 14.9 us: 1.01x faster                                                          |
| pickle_list          | 5.11 us                                                    | 5.13 us: 1.00x slower                                                          |
| pickle               | 11.5 us                                                    | 11.6 us: 1.01x slower                                                          |
| pickle_dict          | 34.8 us                                                    | 35.1 us: 1.01x slower                                                          |
| pickle_pure_python   | 305 us                                                     | 317 us: 1.04x slower                                                           |
| xml_etree_generate   | 87.4 ms                                                    | 103 ms: 1.17x slower                                                           |
| xml_etree_iterparse  | 107 ms                                                     | 127 ms: 1.19x slower                                                           |
| xml_etree_process    | 61.2 ms                                                    | 74.0 ms: 1.21x slower                                                          |
| tomli_loads          | 2.12 sec                                                   | 3.37 sec: 1.59x slower                                                         |
| unpickle_pure_python | 218 us                                                     | 398 us: 1.83x slower                                                           |
| Geometric mean       | (ref)                                                      | 1.12x slower                                                                   |

Benchmark hidden because not significant (2): unpickle_list, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                          |
| python_startup_no_site | 7.11 ms                                                    | 7.12 ms: 1.00x slower                                                          |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|-----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| django_template | 34.8 ms                                                    | 47.5 ms: 1.37x slower                                                          |
| genshi_xml      | 51.6 ms                                                    | 80.6 ms: 1.56x slower                                                          |
| genshi_text     | 23.7 ms                                                    | 38.7 ms: 1.64x slower                                                          |
| mako            | 11.2 ms                                                    | 20.3 ms: 1.81x slower                                                          |
| Geometric mean  | (ref)                                                      | 1.58x slower                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| gc_traversal               | 3.98 ms                                                    | 3.61 ms: 1.10x faster                                                          |
| json_loads                 | 28.9 us                                                    | 27.5 us: 1.05x faster                                                          |
| xml_etree_parse            | 162 ms                                                     | 154 ms: 1.05x faster                                                           |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                          |
| json                       | 5.31 ms                                                    | 5.20 ms: 1.02x faster                                                          |
| create_gc_cycles           | 1.82 ms                                                    | 1.78 ms: 1.02x faster                                                          |
| unpickle                   | 15.1 us                                                    | 14.9 us: 1.01x faster                                                          |
| coverage                   | 93.1 ms                                                    | 92.3 ms: 1.01x faster                                                          |
| python_startup_no_site     | 7.11 ms                                                    | 7.12 ms: 1.00x slower                                                          |
| pickle_list                | 5.11 us                                                    | 5.13 us: 1.00x slower                                                          |
| bench_mp_pool              | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                                          |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                                          |
| pickle_dict                | 34.8 us                                                    | 35.1 us: 1.01x slower                                                          |
| pidigits                   | 191 ms                                                     | 194 ms: 1.01x slower                                                           |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.87 sec: 1.02x slower                                                         |
| regex_effbot               | 3.67 ms                                                    | 3.74 ms: 1.02x slower                                                          |
| regex_dna                  | 221 ms                                                     | 226 ms: 1.02x slower                                                           |
| thrift                     | 823 us                                                     | 847 us: 1.03x slower                                                           |
| sqlite_synth               | 2.99 us                                                    | 3.08 us: 1.03x slower                                                          |
| logging_silent             | 105 ns                                                     | 108 ns: 1.04x slower                                                           |
| coroutines                 | 23.2 ms                                                    | 24.1 ms: 1.04x slower                                                          |
| pickle_pure_python         | 305 us                                                     | 317 us: 1.04x slower                                                           |
| async_tree_none            | 378 ms                                                     | 393 ms: 1.04x slower                                                           |
| regex_v8                   | 25.1 ms                                                    | 26.4 ms: 1.05x slower                                                          |
| async_tree_io_tg           | 936 ms                                                     | 986 ms: 1.05x slower                                                           |
| djangocms                  | 31.5 us                                                    | 33.2 us: 1.05x slower                                                          |
| asyncio_tcp                | 508 ms                                                     | 539 ms: 1.06x slower                                                           |
| async_tree_io              | 939 ms                                                     | 1.00 sec: 1.07x slower                                                         |
| dask                       | 369 ms                                                     | 396 ms: 1.07x slower                                                           |
| gunicorn                   | 1.28 ms                                                    | 1.37 ms: 1.07x slower                                                          |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 658 ms: 1.08x slower                                                           |
| async_tree_memoization_tg  | 444 ms                                                     | 478 ms: 1.08x slower                                                           |
| aiohttp                    | 1.18 ms                                                    | 1.28 ms: 1.08x slower                                                          |
| generators                 | 29.6 ms                                                    | 32.1 ms: 1.08x slower                                                          |
| async_tree_none_tg         | 336 ms                                                     | 366 ms: 1.09x slower                                                           |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 643 ms: 1.09x slower                                                           |
| pathlib                    | 17.3 ms                                                    | 19.2 ms: 1.11x slower                                                          |
| tornado_http               | 94.6 ms                                                    | 105 ms: 1.11x slower                                                           |
| deepcopy                   | 367 us                                                     | 411 us: 1.12x slower                                                           |
| async_tree_memoization     | 463 ms                                                     | 526 ms: 1.14x slower                                                           |
| async_generators           | 442 ms                                                     | 504 ms: 1.14x slower                                                           |
| telco                      | 8.41 ms                                                    | 9.63 ms: 1.14x slower                                                          |
| dulwich_log                | 67.2 ms                                                    | 77.9 ms: 1.16x slower                                                          |
| bench_thread_pool          | 834 us                                                     | 976 us: 1.17x slower                                                           |
| xml_etree_generate         | 87.4 ms                                                    | 103 ms: 1.17x slower                                                           |
| mypy2                      | 742 ms                                                     | 874 ms: 1.18x slower                                                           |
| xml_etree_iterparse        | 107 ms                                                     | 127 ms: 1.19x slower                                                           |
| sqlglot_transpile          | 1.63 ms                                                    | 1.94 ms: 1.19x slower                                                          |
| pycparser                  | 1.16 sec                                                   | 1.38 sec: 1.19x slower                                                         |
| mdp                        | 2.79 sec                                                   | 3.33 sec: 1.19x slower                                                         |
| docutils                   | 2.83 sec                                                   | 3.37 sec: 1.19x slower                                                         |
| sqlglot_parse              | 1.32 ms                                                    | 1.59 ms: 1.20x slower                                                          |
| html5lib                   | 67.2 ms                                                    | 81.2 ms: 1.21x slower                                                          |
| xml_etree_process          | 61.2 ms                                                    | 74.0 ms: 1.21x slower                                                          |
| pylint                     | 317 ms                                                     | 385 ms: 1.21x slower                                                           |
| chameleon                  | 7.22 ms                                                    | 8.81 ms: 1.22x slower                                                          |
| logging_format             | 6.47 us                                                    | 7.96 us: 1.23x slower                                                          |
| sympy_sum                  | 156 ms                                                     | 192 ms: 1.23x slower                                                           |
| sympy_expand               | 473 ms                                                     | 583 ms: 1.23x slower                                                           |
| logging_simple             | 5.74 us                                                    | 7.21 us: 1.25x slower                                                          |
| deepcopy_memo              | 39.7 us                                                    | 50.7 us: 1.28x slower                                                          |
| sqlglot_normalize          | 110 ms                                                     | 141 ms: 1.28x slower                                                           |
| sympy_str                  | 282 ms                                                     | 362 ms: 1.28x slower                                                           |
| meteor_contest             | 110 ms                                                     | 144 ms: 1.31x slower                                                           |
| 2to3                       | 274 ms                                                     | 361 ms: 1.32x slower                                                           |
| sqlglot_optimize           | 55.5 ms                                                    | 73.3 ms: 1.32x slower                                                          |
| typing_runtime_protocols   | 165 us                                                     | 219 us: 1.33x slower                                                           |
| sympy_integrate            | 20.5 ms                                                    | 27.6 ms: 1.35x slower                                                          |
| django_template            | 34.8 ms                                                    | 47.5 ms: 1.37x slower                                                          |
| richards_super             | 57.4 ms                                                    | 78.6 ms: 1.37x slower                                                          |
| scimark_sor                | 127 ms                                                     | 176 ms: 1.38x slower                                                           |
| richards                   | 50.9 ms                                                    | 71.7 ms: 1.41x slower                                                          |
| raytrace                   | 267 ms                                                     | 377 ms: 1.41x slower                                                           |
| scimark_fft                | 392 ms                                                     | 597 ms: 1.52x slower                                                           |
| genshi_xml                 | 51.6 ms                                                    | 80.6 ms: 1.56x slower                                                          |
| tomli_loads                | 2.12 sec                                                   | 3.37 sec: 1.59x slower                                                         |
| crypto_pyaes               | 77.5 ms                                                    | 125 ms: 1.62x slower                                                           |
| regex_compile              | 137 ms                                                     | 223 ms: 1.63x slower                                                           |
| float                      | 78.9 ms                                                    | 129 ms: 1.63x slower                                                           |
| genshi_text                | 23.7 ms                                                    | 38.7 ms: 1.64x slower                                                          |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 8.81 ms: 1.67x slower                                                          |
| scimark_lu                 | 122 ms                                                     | 203 ms: 1.67x slower                                                           |
| deltablue                  | 3.25 ms                                                    | 5.46 ms: 1.68x slower                                                          |
| chaos                      | 61.3 ms                                                    | 103 ms: 1.69x slower                                                           |
| pprint_safe_repr           | 758 ms                                                     | 1.29 sec: 1.70x slower                                                         |
| pprint_pformat             | 1.56 sec                                                   | 2.66 sec: 1.71x slower                                                         |
| fannkuch                   | 402 ms                                                     | 705 ms: 1.75x slower                                                           |
| pyflate                    | 484 ms                                                     | 862 ms: 1.78x slower                                                           |
| mako                       | 11.2 ms                                                    | 20.3 ms: 1.81x slower                                                          |
| go                         | 145 ms                                                     | 261 ms: 1.81x slower                                                           |
| unpickle_pure_python       | 218 us                                                     | 398 us: 1.83x slower                                                           |
| spectral_norm              | 116 ms                                                     | 215 ms: 1.85x slower                                                           |
| nqueens                    | 81.4 ms                                                    | 153 ms: 1.87x slower                                                           |
| scimark_monte_carlo        | 69.2 ms                                                    | 135 ms: 1.95x slower                                                           |
| nbody                      | 88.3 ms                                                    | 197 ms: 2.23x slower                                                           |
| comprehensions             | 16.6 us                                                    | 37.5 us: 2.26x slower                                                          |
| hexiom                     | 6.30 ms                                                    | 15.2 ms: 2.41x slower                                                          |
| Geometric mean             | (ref)                                                      | 1.25x slower                                                                   |

Benchmark hidden because not significant (4): unpickle_list, deepcopy_reduce, json_dumps, asyncio_websockets
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.18x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.16x

# Memory
- memory change: 0.99x
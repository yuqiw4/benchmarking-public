# Results vs. 3.13.0b2

- fork: Fidget-Spinner
- ref: int_constant_propaga
- machine: linux-x86_64
- commit hash: 577e8e3
- commit date: 2024-04-07
- overall geometric mean: 1.15x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 320 ms: 1.17x slower                                                             |
| chameleon      | 7.22 ms                                                    | 7.95 ms: 1.10x slower                                                            |
| docutils       | 2.83 sec                                                   | 3.18 sec: 1.12x slower                                                           |
| html5lib       | 67.2 ms                                                    | 74.9 ms: 1.11x slower                                                            |
| tornado_http   | 94.6 ms                                                    | 104 ms: 1.10x slower                                                             |
| Geometric mean | (ref)                                                      | 1.12x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io              | 939 ms                                                     | 976 ms: 1.04x slower                                                             |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 648 ms: 1.06x slower                                                             |
| async_tree_memoization_tg  | 444 ms                                                     | 471 ms: 1.06x slower                                                             |
| async_tree_io_tg           | 936 ms                                                     | 1.00 sec: 1.07x slower                                                           |
| async_tree_none_tg         | 336 ms                                                     | 363 ms: 1.08x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 635 ms: 1.08x slower                                                             |
| async_tree_memoization     | 463 ms                                                     | 515 ms: 1.11x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.06x slower                                                                     |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 202 ms: 1.05x slower                                                             |
| float          | 78.9 ms                                                    | 96.6 ms: 1.23x slower                                                            |
| nbody          | 88.3 ms                                                    | 134 ms: 1.52x slower                                                             |
| Geometric mean | (ref)                                                      | 1.25x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_dna      | 221 ms                                                     | 227 ms: 1.02x slower                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.78 ms: 1.03x slower                                                            |
| regex_v8       | 25.1 ms                                                    | 26.9 ms: 1.07x slower                                                            |
| regex_compile  | 137 ms                                                     | 208 ms: 1.52x slower                                                             |
| Geometric mean | (ref)                                                      | 1.15x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.23 us: 1.02x faster                                                            |
| pickle_list          | 5.11 us                                                    | 5.02 us: 1.02x faster                                                            |
| json_loads           | 28.9 us                                                    | 28.5 us: 1.01x faster                                                            |
| json_dumps           | 10.7 ms                                                    | 10.8 ms: 1.01x slower                                                            |
| pickle_pure_python   | 305 us                                                     | 318 us: 1.04x slower                                                             |
| pickle               | 11.5 us                                                    | 12.0 us: 1.04x slower                                                            |
| xml_etree_iterparse  | 107 ms                                                     | 115 ms: 1.07x slower                                                             |
| xml_etree_process    | 61.2 ms                                                    | 66.2 ms: 1.08x slower                                                            |
| unpickle             | 15.1 us                                                    | 16.7 us: 1.11x slower                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 98.1 ms: 1.12x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.72 sec: 1.28x slower                                                           |
| unpickle_pure_python | 218 us                                                     | 333 us: 1.53x slower                                                             |
| Geometric mean       | (ref)                                                      | 1.08x slower                                                                     |

Benchmark hidden because not significant (2): pickle_dict, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.7 ms: 1.01x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 9.09 ms: 1.28x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.13x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text    | 23.7 ms                                                    | 26.1 ms: 1.10x slower                                                            |
| genshi_xml     | 51.6 ms                                                    | 62.9 ms: 1.22x slower                                                            |
| mako           | 11.2 ms                                                    | 14.3 ms: 1.27x slower                                                            |
| Geometric mean | (ref)                                                      | 1.20x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 127 us: 1.30x faster                                                             |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                            |
| unpickle_list              | 5.34 us                                                    | 5.23 us: 1.02x faster                                                            |
| pickle_list                | 5.11 us                                                    | 5.02 us: 1.02x faster                                                            |
| json_loads                 | 28.9 us                                                    | 28.5 us: 1.01x faster                                                            |
| python_startup             | 10.8 ms                                                    | 10.7 ms: 1.01x faster                                                            |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.00x faster                                                             |
| bench_mp_pool              | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                                            |
| json_dumps                 | 10.7 ms                                                    | 10.8 ms: 1.01x slower                                                            |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                           |
| gc_traversal               | 3.98 ms                                                    | 4.03 ms: 1.01x slower                                                            |
| asyncio_tcp                | 508 ms                                                     | 518 ms: 1.02x slower                                                             |
| json                       | 5.31 ms                                                    | 5.41 ms: 1.02x slower                                                            |
| generators                 | 29.6 ms                                                    | 30.3 ms: 1.02x slower                                                            |
| thrift                     | 823 us                                                     | 843 us: 1.02x slower                                                             |
| regex_dna                  | 221 ms                                                     | 227 ms: 1.02x slower                                                             |
| regex_effbot               | 3.67 ms                                                    | 3.78 ms: 1.03x slower                                                            |
| async_tree_io              | 939 ms                                                     | 976 ms: 1.04x slower                                                             |
| pickle_pure_python         | 305 us                                                     | 318 us: 1.04x slower                                                             |
| pickle                     | 11.5 us                                                    | 12.0 us: 1.04x slower                                                            |
| coroutines                 | 23.2 ms                                                    | 24.3 ms: 1.05x slower                                                            |
| dask                       | 369 ms                                                     | 388 ms: 1.05x slower                                                             |
| pidigits                   | 191 ms                                                     | 202 ms: 1.05x slower                                                             |
| coverage                   | 93.1 ms                                                    | 98.1 ms: 1.05x slower                                                            |
| mdp                        | 2.79 sec                                                   | 2.94 sec: 1.05x slower                                                           |
| sqlite_synth               | 2.99 us                                                    | 3.15 us: 1.05x slower                                                            |
| gunicorn                   | 1.28 ms                                                    | 1.35 ms: 1.06x slower                                                            |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 648 ms: 1.06x slower                                                             |
| async_tree_memoization_tg  | 444 ms                                                     | 471 ms: 1.06x slower                                                             |
| aiohttp                    | 1.18 ms                                                    | 1.26 ms: 1.07x slower                                                            |
| xml_etree_iterparse        | 107 ms                                                     | 115 ms: 1.07x slower                                                             |
| logging_silent             | 105 ns                                                     | 112 ns: 1.07x slower                                                             |
| async_tree_io_tg           | 936 ms                                                     | 1.00 sec: 1.07x slower                                                           |
| regex_v8                   | 25.1 ms                                                    | 26.9 ms: 1.07x slower                                                            |
| deepcopy                   | 367 us                                                     | 394 us: 1.07x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 363 ms: 1.08x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 635 ms: 1.08x slower                                                             |
| xml_etree_process          | 61.2 ms                                                    | 66.2 ms: 1.08x slower                                                            |
| bench_thread_pool          | 834 us                                                     | 917 us: 1.10x slower                                                             |
| async_generators           | 442 ms                                                     | 486 ms: 1.10x slower                                                             |
| tornado_http               | 94.6 ms                                                    | 104 ms: 1.10x slower                                                             |
| genshi_text                | 23.7 ms                                                    | 26.1 ms: 1.10x slower                                                            |
| chameleon                  | 7.22 ms                                                    | 7.95 ms: 1.10x slower                                                            |
| unpickle                   | 15.1 us                                                    | 16.7 us: 1.11x slower                                                            |
| async_tree_memoization     | 463 ms                                                     | 515 ms: 1.11x slower                                                             |
| html5lib                   | 67.2 ms                                                    | 74.9 ms: 1.11x slower                                                            |
| mypy2                      | 742 ms                                                     | 827 ms: 1.12x slower                                                             |
| xml_etree_generate         | 87.4 ms                                                    | 98.1 ms: 1.12x slower                                                            |
| docutils                   | 2.83 sec                                                   | 3.18 sec: 1.12x slower                                                           |
| logging_format             | 6.47 us                                                    | 7.32 us: 1.13x slower                                                            |
| dulwich_log                | 67.2 ms                                                    | 76.5 ms: 1.14x slower                                                            |
| logging_simple             | 5.74 us                                                    | 6.61 us: 1.15x slower                                                            |
| sqlglot_transpile          | 1.63 ms                                                    | 1.90 ms: 1.16x slower                                                            |
| 2to3                       | 274 ms                                                     | 320 ms: 1.17x slower                                                             |
| sympy_sum                  | 156 ms                                                     | 183 ms: 1.17x slower                                                             |
| sympy_expand               | 473 ms                                                     | 556 ms: 1.18x slower                                                             |
| telco                      | 8.41 ms                                                    | 9.89 ms: 1.18x slower                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.56 ms: 1.18x slower                                                            |
| pathlib                    | 17.3 ms                                                    | 20.6 ms: 1.19x slower                                                            |
| sympy_str                  | 282 ms                                                     | 337 ms: 1.19x slower                                                             |
| sympy_integrate            | 20.5 ms                                                    | 24.5 ms: 1.20x slower                                                            |
| pycparser                  | 1.16 sec                                                   | 1.39 sec: 1.20x slower                                                           |
| scimark_fft                | 392 ms                                                     | 470 ms: 1.20x slower                                                             |
| deepcopy_memo              | 39.7 us                                                    | 47.8 us: 1.20x slower                                                            |
| sqlglot_normalize          | 110 ms                                                     | 133 ms: 1.21x slower                                                             |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 6.38 ms: 1.21x slower                                                            |
| genshi_xml                 | 51.6 ms                                                    | 62.9 ms: 1.22x slower                                                            |
| meteor_contest             | 110 ms                                                     | 134 ms: 1.22x slower                                                             |
| float                      | 78.9 ms                                                    | 96.6 ms: 1.23x slower                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 68.8 ms: 1.24x slower                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 96.7 ms: 1.25x slower                                                            |
| scimark_sor                | 127 ms                                                     | 160 ms: 1.26x slower                                                             |
| richards_super             | 57.4 ms                                                    | 72.2 ms: 1.26x slower                                                            |
| richards                   | 50.9 ms                                                    | 64.8 ms: 1.27x slower                                                            |
| mako                       | 11.2 ms                                                    | 14.3 ms: 1.27x slower                                                            |
| python_startup_no_site     | 7.11 ms                                                    | 9.09 ms: 1.28x slower                                                            |
| tomli_loads                | 2.12 sec                                                   | 2.72 sec: 1.28x slower                                                           |
| fannkuch                   | 402 ms                                                     | 524 ms: 1.30x slower                                                             |
| raytrace                   | 267 ms                                                     | 350 ms: 1.31x slower                                                             |
| deltablue                  | 3.25 ms                                                    | 4.28 ms: 1.32x slower                                                            |
| spectral_norm              | 116 ms                                                     | 153 ms: 1.32x slower                                                             |
| pyflate                    | 484 ms                                                     | 641 ms: 1.32x slower                                                             |
| chaos                      | 61.3 ms                                                    | 82.2 ms: 1.34x slower                                                            |
| go                         | 145 ms                                                     | 198 ms: 1.37x slower                                                             |
| scimark_monte_carlo        | 69.2 ms                                                    | 97.3 ms: 1.41x slower                                                            |
| scimark_lu                 | 122 ms                                                     | 178 ms: 1.46x slower                                                             |
| nbody                      | 88.3 ms                                                    | 134 ms: 1.52x slower                                                             |
| comprehensions             | 16.6 us                                                    | 25.3 us: 1.52x slower                                                            |
| regex_compile              | 137 ms                                                     | 208 ms: 1.52x slower                                                             |
| unpickle_pure_python       | 218 us                                                     | 333 us: 1.53x slower                                                             |
| pprint_pformat             | 1.56 sec                                                   | 2.40 sec: 1.54x slower                                                           |
| pprint_safe_repr           | 758 ms                                                     | 1.18 sec: 1.55x slower                                                           |
| hexiom                     | 6.30 ms                                                    | 10.4 ms: 1.65x slower                                                            |
| nqueens                    | 81.4 ms                                                    | 139 ms: 1.71x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.15x slower                                                                     |

Benchmark hidden because not significant (5): pylint, deepcopy_reduce, pickle_dict, xml_etree_parse, async_tree_none
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 0.99x
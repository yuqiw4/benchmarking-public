# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: return_gen_tier_2
- machine: linux-x86_64
- commit hash: fad1c67
- commit date: 2024-04-23
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 301 ms: 1.10x slower                                                          |
| chameleon      | 7.22 ms                                                    | 7.62 ms: 1.06x slower                                                         |
| docutils       | 2.83 sec                                                   | 3.07 sec: 1.08x slower                                                        |
| html5lib       | 67.2 ms                                                    | 72.4 ms: 1.08x slower                                                         |
| tornado_http   | 94.6 ms                                                    | 102 ms: 1.08x slower                                                          |
| Geometric mean | (ref)                                                      | 1.08x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 444 ms                                                     | 459 ms: 1.03x slower                                                          |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 632 ms: 1.03x slower                                                          |
| async_tree_io_tg           | 936 ms                                                     | 969 ms: 1.04x slower                                                          |
| async_tree_none_tg         | 336 ms                                                     | 351 ms: 1.05x slower                                                          |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 623 ms: 1.06x slower                                                          |
| async_tree_memoization     | 463 ms                                                     | 499 ms: 1.08x slower                                                          |
| Geometric mean             | (ref)                                                      | 1.04x slower                                                                  |

Benchmark hidden because not significant (2): async_tree_none, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 89.3 ms: 1.13x slower                                                         |
| pidigits       | 191 ms                                                     | 218 ms: 1.14x slower                                                          |
| nbody          | 88.3 ms                                                    | 120 ms: 1.36x slower                                                          |
| Geometric mean | (ref)                                                      | 1.21x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.69 ms: 1.01x slower                                                         |
| regex_v8       | 25.1 ms                                                    | 25.4 ms: 1.01x slower                                                         |
| regex_dna      | 221 ms                                                     | 228 ms: 1.03x slower                                                          |
| regex_compile  | 137 ms                                                     | 179 ms: 1.31x slower                                                          |
| Geometric mean | (ref)                                                      | 1.08x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_loads           | 28.9 us                                                    | 27.5 us: 1.05x faster                                                         |
| xml_etree_parse      | 162 ms                                                     | 154 ms: 1.05x faster                                                          |
| unpickle_list        | 5.34 us                                                    | 5.26 us: 1.02x faster                                                         |
| pickle_dict          | 34.8 us                                                    | 35.0 us: 1.01x slower                                                         |
| json_dumps           | 10.7 ms                                                    | 10.8 ms: 1.01x slower                                                         |
| pickle_list          | 5.11 us                                                    | 5.19 us: 1.02x slower                                                         |
| xml_etree_iterparse  | 107 ms                                                     | 110 ms: 1.02x slower                                                          |
| pickle_pure_python   | 305 us                                                     | 314 us: 1.03x slower                                                          |
| unpickle             | 15.1 us                                                    | 15.7 us: 1.04x slower                                                         |
| pickle               | 11.5 us                                                    | 11.9 us: 1.04x slower                                                         |
| xml_etree_process    | 61.2 ms                                                    | 64.2 ms: 1.05x slower                                                         |
| xml_etree_generate   | 87.4 ms                                                    | 93.3 ms: 1.07x slower                                                         |
| tomli_loads          | 2.12 sec                                                   | 2.53 sec: 1.20x slower                                                        |
| unpickle_pure_python | 218 us                                                     | 283 us: 1.30x slower                                                          |
| Geometric mean       | (ref)                                                      | 1.04x slower                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                                         |
| python_startup_no_site | 7.11 ms                                                    | 7.15 ms: 1.01x slower                                                         |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|-----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_text     | 23.7 ms                                                    | 25.6 ms: 1.08x slower                                                         |
| genshi_xml      | 51.6 ms                                                    | 58.7 ms: 1.14x slower                                                         |
| django_template | 34.8 ms                                                    | 39.8 ms: 1.14x slower                                                         |
| mako            | 11.2 ms                                                    | 13.8 ms: 1.23x slower                                                         |
| Geometric mean  | (ref)                                                      | 1.15x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 123 us: 1.34x faster                                                          |
| gc_traversal               | 3.98 ms                                                    | 3.64 ms: 1.09x faster                                                         |
| json_loads                 | 28.9 us                                                    | 27.5 us: 1.05x faster                                                         |
| xml_etree_parse            | 162 ms                                                     | 154 ms: 1.05x faster                                                          |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                         |
| deepcopy_reduce            | 3.35 us                                                    | 3.28 us: 1.02x faster                                                         |
| asyncio_websockets         | 567 ms                                                     | 555 ms: 1.02x faster                                                          |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                                         |
| unpickle_list              | 5.34 us                                                    | 5.26 us: 1.02x faster                                                         |
| coroutines                 | 23.2 ms                                                    | 22.8 ms: 1.01x faster                                                         |
| regex_effbot               | 3.67 ms                                                    | 3.69 ms: 1.01x slower                                                         |
| python_startup_no_site     | 7.11 ms                                                    | 7.15 ms: 1.01x slower                                                         |
| bench_mp_pool              | 23.9 ms                                                    | 24.1 ms: 1.01x slower                                                         |
| pickle_dict                | 34.8 us                                                    | 35.0 us: 1.01x slower                                                         |
| regex_v8                   | 25.1 ms                                                    | 25.4 ms: 1.01x slower                                                         |
| json_dumps                 | 10.7 ms                                                    | 10.8 ms: 1.01x slower                                                         |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.87 sec: 1.01x slower                                                        |
| pickle_list                | 5.11 us                                                    | 5.19 us: 1.02x slower                                                         |
| generators                 | 29.6 ms                                                    | 30.2 ms: 1.02x slower                                                         |
| asyncio_tcp                | 508 ms                                                     | 517 ms: 1.02x slower                                                          |
| xml_etree_iterparse        | 107 ms                                                     | 110 ms: 1.02x slower                                                          |
| deepcopy                   | 367 us                                                     | 376 us: 1.02x slower                                                          |
| pickle_pure_python         | 305 us                                                     | 314 us: 1.03x slower                                                          |
| regex_dna                  | 221 ms                                                     | 228 ms: 1.03x slower                                                          |
| async_tree_memoization_tg  | 444 ms                                                     | 459 ms: 1.03x slower                                                          |
| dask                       | 369 ms                                                     | 382 ms: 1.03x slower                                                          |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 632 ms: 1.03x slower                                                          |
| async_tree_io_tg           | 936 ms                                                     | 969 ms: 1.04x slower                                                          |
| unpickle                   | 15.1 us                                                    | 15.7 us: 1.04x slower                                                         |
| djangocms                  | 31.5 us                                                    | 32.7 us: 1.04x slower                                                         |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.04x slower                                                         |
| gunicorn                   | 1.28 ms                                                    | 1.33 ms: 1.04x slower                                                         |
| async_tree_none_tg         | 336 ms                                                     | 351 ms: 1.05x slower                                                          |
| xml_etree_process          | 61.2 ms                                                    | 64.2 ms: 1.05x slower                                                         |
| pathlib                    | 17.3 ms                                                    | 18.2 ms: 1.05x slower                                                         |
| chameleon                  | 7.22 ms                                                    | 7.62 ms: 1.06x slower                                                         |
| aiohttp                    | 1.18 ms                                                    | 1.25 ms: 1.06x slower                                                         |
| bench_thread_pool          | 834 us                                                     | 883 us: 1.06x slower                                                          |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 623 ms: 1.06x slower                                                          |
| coverage                   | 93.1 ms                                                    | 99.3 ms: 1.07x slower                                                         |
| xml_etree_generate         | 87.4 ms                                                    | 93.3 ms: 1.07x slower                                                         |
| async_tree_memoization     | 463 ms                                                     | 499 ms: 1.08x slower                                                          |
| html5lib                   | 67.2 ms                                                    | 72.4 ms: 1.08x slower                                                         |
| richards_super             | 57.4 ms                                                    | 61.8 ms: 1.08x slower                                                         |
| async_generators           | 442 ms                                                     | 478 ms: 1.08x slower                                                          |
| genshi_text                | 23.7 ms                                                    | 25.6 ms: 1.08x slower                                                         |
| tornado_http               | 94.6 ms                                                    | 102 ms: 1.08x slower                                                          |
| pylint                     | 317 ms                                                     | 343 ms: 1.08x slower                                                          |
| docutils                   | 2.83 sec                                                   | 3.07 sec: 1.08x slower                                                        |
| telco                      | 8.41 ms                                                    | 9.13 ms: 1.08x slower                                                         |
| meteor_contest             | 110 ms                                                     | 119 ms: 1.09x slower                                                          |
| mypy2                      | 742 ms                                                     | 807 ms: 1.09x slower                                                          |
| richards                   | 50.9 ms                                                    | 55.6 ms: 1.09x slower                                                         |
| 2to3                       | 274 ms                                                     | 301 ms: 1.10x slower                                                          |
| dulwich_log                | 67.2 ms                                                    | 73.8 ms: 1.10x slower                                                         |
| pycparser                  | 1.16 sec                                                   | 1.27 sec: 1.10x slower                                                        |
| deepcopy_memo              | 39.7 us                                                    | 43.8 us: 1.10x slower                                                         |
| sqlglot_transpile          | 1.63 ms                                                    | 1.80 ms: 1.10x slower                                                         |
| logging_format             | 6.47 us                                                    | 7.17 us: 1.11x slower                                                         |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.85 ms: 1.11x slower                                                         |
| scimark_fft                | 392 ms                                                     | 436 ms: 1.11x slower                                                          |
| logging_simple             | 5.74 us                                                    | 6.40 us: 1.11x slower                                                         |
| sqlglot_normalize          | 110 ms                                                     | 123 ms: 1.12x slower                                                          |
| sqlglot_parse              | 1.32 ms                                                    | 1.48 ms: 1.12x slower                                                         |
| sympy_integrate            | 20.5 ms                                                    | 23.1 ms: 1.13x slower                                                         |
| sympy_expand               | 473 ms                                                     | 534 ms: 1.13x slower                                                          |
| float                      | 78.9 ms                                                    | 89.3 ms: 1.13x slower                                                         |
| genshi_xml                 | 51.6 ms                                                    | 58.7 ms: 1.14x slower                                                         |
| sympy_str                  | 282 ms                                                     | 321 ms: 1.14x slower                                                          |
| pidigits                   | 191 ms                                                     | 218 ms: 1.14x slower                                                          |
| sympy_sum                  | 156 ms                                                     | 177 ms: 1.14x slower                                                          |
| sqlglot_optimize           | 55.5 ms                                                    | 63.3 ms: 1.14x slower                                                         |
| django_template            | 34.8 ms                                                    | 39.8 ms: 1.14x slower                                                         |
| scimark_sor                | 127 ms                                                     | 149 ms: 1.17x slower                                                          |
| spectral_norm              | 116 ms                                                     | 138 ms: 1.19x slower                                                          |
| crypto_pyaes               | 77.5 ms                                                    | 92.0 ms: 1.19x slower                                                         |
| tomli_loads                | 2.12 sec                                                   | 2.53 sec: 1.20x slower                                                        |
| raytrace                   | 267 ms                                                     | 319 ms: 1.20x slower                                                          |
| fannkuch                   | 402 ms                                                     | 487 ms: 1.21x slower                                                          |
| pyflate                    | 484 ms                                                     | 588 ms: 1.21x slower                                                          |
| mako                       | 11.2 ms                                                    | 13.8 ms: 1.23x slower                                                         |
| pprint_safe_repr           | 758 ms                                                     | 939 ms: 1.24x slower                                                          |
| scimark_monte_carlo        | 69.2 ms                                                    | 86.0 ms: 1.24x slower                                                         |
| pprint_pformat             | 1.56 sec                                                   | 1.94 sec: 1.25x slower                                                        |
| deltablue                  | 3.25 ms                                                    | 4.15 ms: 1.28x slower                                                         |
| go                         | 145 ms                                                     | 185 ms: 1.28x slower                                                          |
| chaos                      | 61.3 ms                                                    | 78.4 ms: 1.28x slower                                                         |
| nqueens                    | 81.4 ms                                                    | 105 ms: 1.29x slower                                                          |
| unpickle_pure_python       | 218 us                                                     | 283 us: 1.30x slower                                                          |
| regex_compile              | 137 ms                                                     | 179 ms: 1.31x slower                                                          |
| scimark_lu                 | 122 ms                                                     | 163 ms: 1.34x slower                                                          |
| nbody                      | 88.3 ms                                                    | 120 ms: 1.36x slower                                                          |
| comprehensions             | 16.6 us                                                    | 22.6 us: 1.36x slower                                                         |
| hexiom                     | 6.30 ms                                                    | 9.45 ms: 1.50x slower                                                         |
| Geometric mean             | (ref)                                                      | 1.09x slower                                                                  |

Benchmark hidden because not significant (7): async_tree_none, json, thrift, logging_silent, mdp, sqlite_synth, async_tree_io
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 0.99x
# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: tier_2_for_iter_gen
- machine: linux-x86_64
- commit hash: 5fbcbf4
- commit date: 2024-04-24
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 302 ms: 1.10x slower                                                            |
| chameleon      | 7.22 ms                                                    | 7.46 ms: 1.03x slower                                                           |
| docutils       | 2.83 sec                                                   | 3.07 sec: 1.08x slower                                                          |
| html5lib       | 67.2 ms                                                    | 70.1 ms: 1.04x slower                                                           |
| tornado_http   | 94.6 ms                                                    | 101 ms: 1.07x slower                                                            |
| Geometric mean | (ref)                                                      | 1.07x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_io              | 939 ms                                                     | 972 ms: 1.04x slower                                                            |
| async_tree_memoization_tg  | 444 ms                                                     | 461 ms: 1.04x slower                                                            |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 636 ms: 1.04x slower                                                            |
| async_tree_none_tg         | 336 ms                                                     | 350 ms: 1.04x slower                                                            |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 626 ms: 1.07x slower                                                            |
| async_tree_memoization     | 463 ms                                                     | 500 ms: 1.08x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.04x slower                                                                    |

Benchmark hidden because not significant (2): async_tree_none, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 195 ms: 1.02x slower                                                            |
| float          | 78.9 ms                                                    | 88.4 ms: 1.12x slower                                                           |
| nbody          | 88.3 ms                                                    | 122 ms: 1.38x slower                                                            |
| Geometric mean | (ref)                                                      | 1.16x slower                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.64 ms: 1.01x faster                                                           |
| regex_v8       | 25.1 ms                                                    | 25.4 ms: 1.01x slower                                                           |
| regex_dna      | 221 ms                                                     | 227 ms: 1.03x slower                                                            |
| regex_compile  | 137 ms                                                     | 178 ms: 1.30x slower                                                            |
| Geometric mean | (ref)                                                      | 1.08x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 153 ms: 1.06x faster                                                            |
| json_loads           | 28.9 us                                                    | 27.6 us: 1.05x faster                                                           |
| unpickle_list        | 5.34 us                                                    | 5.15 us: 1.04x faster                                                           |
| pickle_list          | 5.11 us                                                    | 5.03 us: 1.01x faster                                                           |
| json_dumps           | 10.7 ms                                                    | 10.8 ms: 1.01x slower                                                           |
| pickle_dict          | 34.8 us                                                    | 35.4 us: 1.02x slower                                                           |
| pickle_pure_python   | 305 us                                                     | 314 us: 1.03x slower                                                            |
| pickle               | 11.5 us                                                    | 11.8 us: 1.03x slower                                                           |
| xml_etree_iterparse  | 107 ms                                                     | 111 ms: 1.04x slower                                                            |
| xml_etree_process    | 61.2 ms                                                    | 64.4 ms: 1.05x slower                                                           |
| xml_etree_generate   | 87.4 ms                                                    | 93.3 ms: 1.07x slower                                                           |
| unpickle             | 15.1 us                                                    | 16.7 us: 1.10x slower                                                           |
| tomli_loads          | 2.12 sec                                                   | 2.49 sec: 1.17x slower                                                          |
| unpickle_pure_python | 218 us                                                     | 281 us: 1.29x slower                                                            |
| Geometric mean       | (ref)                                                      | 1.04x slower                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                                           |
| python_startup_no_site | 7.11 ms                                                    | 7.13 ms: 1.00x slower                                                           |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|-----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| django_template | 34.8 ms                                                    | 39.5 ms: 1.14x slower                                                           |
| genshi_text     | 23.7 ms                                                    | 27.3 ms: 1.15x slower                                                           |
| mako            | 11.2 ms                                                    | 13.1 ms: 1.17x slower                                                           |
| genshi_xml      | 51.6 ms                                                    | 62.1 ms: 1.20x slower                                                           |
| Geometric mean  | (ref)                                                      | 1.16x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 123 us: 1.34x faster                                                            |
| gc_traversal               | 3.98 ms                                                    | 3.72 ms: 1.07x faster                                                           |
| xml_etree_parse            | 162 ms                                                     | 153 ms: 1.06x faster                                                            |
| json_loads                 | 28.9 us                                                    | 27.6 us: 1.05x faster                                                           |
| unpickle_list              | 5.34 us                                                    | 5.15 us: 1.04x faster                                                           |
| create_gc_cycles           | 1.82 ms                                                    | 1.77 ms: 1.03x faster                                                           |
| coroutines                 | 23.2 ms                                                    | 22.6 ms: 1.03x faster                                                           |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                                           |
| json                       | 5.31 ms                                                    | 5.23 ms: 1.01x faster                                                           |
| pickle_list                | 5.11 us                                                    | 5.03 us: 1.01x faster                                                           |
| deepcopy_reduce            | 3.35 us                                                    | 3.32 us: 1.01x faster                                                           |
| regex_effbot               | 3.67 ms                                                    | 3.64 ms: 1.01x faster                                                           |
| python_startup_no_site     | 7.11 ms                                                    | 7.13 ms: 1.00x slower                                                           |
| json_dumps                 | 10.7 ms                                                    | 10.8 ms: 1.01x slower                                                           |
| regex_v8                   | 25.1 ms                                                    | 25.4 ms: 1.01x slower                                                           |
| thrift                     | 823 us                                                     | 834 us: 1.01x slower                                                            |
| mdp                        | 2.79 sec                                                   | 2.83 sec: 1.01x slower                                                          |
| asyncio_tcp                | 508 ms                                                     | 515 ms: 1.01x slower                                                            |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.87 sec: 1.02x slower                                                          |
| pickle_dict                | 34.8 us                                                    | 35.4 us: 1.02x slower                                                           |
| pidigits                   | 191 ms                                                     | 195 ms: 1.02x slower                                                            |
| deepcopy                   | 367 us                                                     | 376 us: 1.03x slower                                                            |
| regex_dna                  | 221 ms                                                     | 227 ms: 1.03x slower                                                            |
| pickle_pure_python         | 305 us                                                     | 314 us: 1.03x slower                                                            |
| dask                       | 369 ms                                                     | 381 ms: 1.03x slower                                                            |
| pickle                     | 11.5 us                                                    | 11.8 us: 1.03x slower                                                           |
| chameleon                  | 7.22 ms                                                    | 7.46 ms: 1.03x slower                                                           |
| async_tree_io              | 939 ms                                                     | 972 ms: 1.04x slower                                                            |
| xml_etree_iterparse        | 107 ms                                                     | 111 ms: 1.04x slower                                                            |
| async_tree_memoization_tg  | 444 ms                                                     | 461 ms: 1.04x slower                                                            |
| generators                 | 29.6 ms                                                    | 30.8 ms: 1.04x slower                                                           |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 636 ms: 1.04x slower                                                            |
| async_tree_none_tg         | 336 ms                                                     | 350 ms: 1.04x slower                                                            |
| gunicorn                   | 1.28 ms                                                    | 1.33 ms: 1.04x slower                                                           |
| djangocms                  | 31.5 us                                                    | 32.9 us: 1.04x slower                                                           |
| html5lib                   | 67.2 ms                                                    | 70.1 ms: 1.04x slower                                                           |
| aiohttp                    | 1.18 ms                                                    | 1.24 ms: 1.05x slower                                                           |
| xml_etree_process          | 61.2 ms                                                    | 64.4 ms: 1.05x slower                                                           |
| pathlib                    | 17.3 ms                                                    | 18.3 ms: 1.06x slower                                                           |
| coverage                   | 93.1 ms                                                    | 99.0 ms: 1.06x slower                                                           |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 626 ms: 1.07x slower                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 93.3 ms: 1.07x slower                                                           |
| tornado_http               | 94.6 ms                                                    | 101 ms: 1.07x slower                                                            |
| async_generators           | 442 ms                                                     | 473 ms: 1.07x slower                                                            |
| bench_thread_pool          | 834 us                                                     | 893 us: 1.07x slower                                                            |
| mypy2                      | 742 ms                                                     | 800 ms: 1.08x slower                                                            |
| async_tree_memoization     | 463 ms                                                     | 500 ms: 1.08x slower                                                            |
| richards_super             | 57.4 ms                                                    | 62.0 ms: 1.08x slower                                                           |
| pylint                     | 317 ms                                                     | 343 ms: 1.08x slower                                                            |
| docutils                   | 2.83 sec                                                   | 3.07 sec: 1.08x slower                                                          |
| richards                   | 50.9 ms                                                    | 55.3 ms: 1.09x slower                                                           |
| telco                      | 8.41 ms                                                    | 9.15 ms: 1.09x slower                                                           |
| deepcopy_memo              | 39.7 us                                                    | 43.2 us: 1.09x slower                                                           |
| meteor_contest             | 110 ms                                                     | 120 ms: 1.09x slower                                                            |
| pycparser                  | 1.16 sec                                                   | 1.27 sec: 1.09x slower                                                          |
| dulwich_log                | 67.2 ms                                                    | 73.6 ms: 1.10x slower                                                           |
| 2to3                       | 274 ms                                                     | 302 ms: 1.10x slower                                                            |
| unpickle                   | 15.1 us                                                    | 16.7 us: 1.10x slower                                                           |
| sqlglot_transpile          | 1.63 ms                                                    | 1.80 ms: 1.10x slower                                                           |
| logging_format             | 6.47 us                                                    | 7.15 us: 1.11x slower                                                           |
| logging_simple             | 5.74 us                                                    | 6.36 us: 1.11x slower                                                           |
| sqlglot_parse              | 1.32 ms                                                    | 1.47 ms: 1.12x slower                                                           |
| sqlglot_normalize          | 110 ms                                                     | 123 ms: 1.12x slower                                                            |
| float                      | 78.9 ms                                                    | 88.4 ms: 1.12x slower                                                           |
| sympy_integrate            | 20.5 ms                                                    | 23.0 ms: 1.12x slower                                                           |
| scimark_fft                | 392 ms                                                     | 443 ms: 1.13x slower                                                            |
| sympy_expand               | 473 ms                                                     | 534 ms: 1.13x slower                                                            |
| sympy_sum                  | 156 ms                                                     | 177 ms: 1.13x slower                                                            |
| django_template            | 34.8 ms                                                    | 39.5 ms: 1.14x slower                                                           |
| sqlglot_optimize           | 55.5 ms                                                    | 63.3 ms: 1.14x slower                                                           |
| sympy_str                  | 282 ms                                                     | 322 ms: 1.14x slower                                                            |
| genshi_text                | 23.7 ms                                                    | 27.3 ms: 1.15x slower                                                           |
| scimark_sor                | 127 ms                                                     | 147 ms: 1.16x slower                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 89.8 ms: 1.16x slower                                                           |
| mako                       | 11.2 ms                                                    | 13.1 ms: 1.17x slower                                                           |
| tomli_loads                | 2.12 sec                                                   | 2.49 sec: 1.17x slower                                                          |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 6.21 ms: 1.18x slower                                                           |
| pyflate                    | 484 ms                                                     | 571 ms: 1.18x slower                                                            |
| raytrace                   | 267 ms                                                     | 319 ms: 1.20x slower                                                            |
| spectral_norm              | 116 ms                                                     | 140 ms: 1.20x slower                                                            |
| fannkuch                   | 402 ms                                                     | 483 ms: 1.20x slower                                                            |
| genshi_xml                 | 51.6 ms                                                    | 62.1 ms: 1.20x slower                                                           |
| pprint_safe_repr           | 758 ms                                                     | 944 ms: 1.25x slower                                                            |
| scimark_monte_carlo        | 69.2 ms                                                    | 87.4 ms: 1.26x slower                                                           |
| pprint_pformat             | 1.56 sec                                                   | 1.97 sec: 1.27x slower                                                          |
| deltablue                  | 3.25 ms                                                    | 4.14 ms: 1.27x slower                                                           |
| go                         | 145 ms                                                     | 184 ms: 1.28x slower                                                            |
| chaos                      | 61.3 ms                                                    | 78.9 ms: 1.29x slower                                                           |
| unpickle_pure_python       | 218 us                                                     | 281 us: 1.29x slower                                                            |
| regex_compile              | 137 ms                                                     | 178 ms: 1.30x slower                                                            |
| nqueens                    | 81.4 ms                                                    | 106 ms: 1.31x slower                                                            |
| scimark_lu                 | 122 ms                                                     | 163 ms: 1.34x slower                                                            |
| comprehensions             | 16.6 us                                                    | 22.6 us: 1.36x slower                                                           |
| nbody                      | 88.3 ms                                                    | 122 ms: 1.38x slower                                                            |
| hexiom                     | 6.30 ms                                                    | 9.27 ms: 1.47x slower                                                           |
| Geometric mean             | (ref)                                                      | 1.09x slower                                                                    |

Benchmark hidden because not significant (6): async_tree_none, logging_silent, asyncio_websockets, sqlite_synth, bench_mp_pool, async_tree_io_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.00x
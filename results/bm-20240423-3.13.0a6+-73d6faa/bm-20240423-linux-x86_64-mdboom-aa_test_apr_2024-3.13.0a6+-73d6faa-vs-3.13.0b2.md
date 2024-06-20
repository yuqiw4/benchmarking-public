# Results vs. 3.13.0b2

- fork: mdboom
- ref: aa_test_apr_2024
- machine: linux-x86_64
- commit hash: 73d6faa
- commit date: 2024-04-23
- overall geometric mean: 1.01x faster
- HPT reliability: 96.16%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 271 ms: 1.01x faster                                               |
| chameleon      | 7.22 ms                                                    | 6.90 ms: 1.05x faster                                              |
| docutils       | 2.83 sec                                                   | 2.81 sec: 1.01x faster                                             |
| tornado_http   | 94.6 ms                                                    | 94.1 ms: 1.01x faster                                              |
| Geometric mean | (ref)                                                      | 1.01x faster                                                       |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 352 ms: 1.07x faster                                               |
| async_tree_io              | 939 ms                                                     | 908 ms: 1.03x faster                                               |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                               |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                       |

Benchmark hidden because not significant (5): async_tree_memoization_tg, async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                               |
| nbody          | 88.3 ms                                                    | 95.5 ms: 1.08x slower                                              |
| Geometric mean | (ref)                                                      | 1.02x slower                                                       |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 136 ms: 1.01x faster                                               |
| regex_effbot   | 3.67 ms                                                    | 3.73 ms: 1.02x slower                                              |
| regex_dna      | 221 ms                                                     | 225 ms: 1.02x slower                                               |
| regex_v8       | 25.1 ms                                                    | 25.8 ms: 1.03x slower                                              |
| Geometric mean | (ref)                                                      | 1.01x slower                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------------|:----------------------------------------------------------:|:------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.11 us: 1.05x faster                                              |
| json_loads           | 28.9 us                                                    | 27.8 us: 1.04x faster                                              |
| xml_etree_parse      | 162 ms                                                     | 159 ms: 1.02x faster                                               |
| xml_etree_process    | 61.2 ms                                                    | 60.4 ms: 1.01x faster                                              |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                              |
| pickle_list          | 5.11 us                                                    | 5.07 us: 1.01x faster                                              |
| xml_etree_generate   | 87.4 ms                                                    | 87.7 ms: 1.00x slower                                              |
| unpickle_pure_python | 218 us                                                     | 219 us: 1.00x slower                                               |
| pickle_dict          | 34.8 us                                                    | 35.3 us: 1.01x slower                                              |
| unpickle             | 15.1 us                                                    | 15.6 us: 1.03x slower                                              |
| tomli_loads          | 2.12 sec                                                   | 2.21 sec: 1.04x slower                                             |
| pickle               | 11.5 us                                                    | 12.1 us: 1.06x slower                                              |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                       |

Benchmark hidden because not significant (2): pickle_pure_python, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                              |
| python_startup_no_site | 7.11 ms                                                    | 7.09 ms: 1.00x faster                                              |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|-----------------|:----------------------------------------------------------:|:------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                              |
| django_template | 34.8 ms                                                    | 35.0 ms: 1.01x slower                                              |
| genshi_xml      | 51.6 ms                                                    | 51.9 ms: 1.01x slower                                              |
| genshi_text     | 23.7 ms                                                    | 23.9 ms: 1.01x slower                                              |
| Geometric mean  | (ref)                                                      | 1.00x faster                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 113 us: 1.45x faster                                               |
| async_tree_none            | 378 ms                                                     | 352 ms: 1.07x faster                                               |
| mdp                        | 2.79 sec                                                   | 2.60 sec: 1.07x faster                                             |
| richards                   | 50.9 ms                                                    | 48.2 ms: 1.06x faster                                              |
| richards_super             | 57.4 ms                                                    | 54.4 ms: 1.05x faster                                              |
| deepcopy_reduce            | 3.35 us                                                    | 3.19 us: 1.05x faster                                              |
| chameleon                  | 7.22 ms                                                    | 6.90 ms: 1.05x faster                                              |
| unpickle_list              | 5.34 us                                                    | 5.11 us: 1.05x faster                                              |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                              |
| json_loads                 | 28.9 us                                                    | 27.8 us: 1.04x faster                                              |
| json                       | 5.31 ms                                                    | 5.13 ms: 1.03x faster                                              |
| mako                       | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                              |
| async_tree_io              | 939 ms                                                     | 908 ms: 1.03x faster                                               |
| crypto_pyaes               | 77.5 ms                                                    | 75.1 ms: 1.03x faster                                              |
| pyflate                    | 484 ms                                                     | 469 ms: 1.03x faster                                               |
| deepcopy_memo              | 39.7 us                                                    | 38.5 us: 1.03x faster                                              |
| deepcopy                   | 367 us                                                     | 357 us: 1.03x faster                                               |
| scimark_fft                | 392 ms                                                     | 382 ms: 1.03x faster                                               |
| gc_traversal               | 3.98 ms                                                    | 3.87 ms: 1.03x faster                                              |
| scimark_sor                | 127 ms                                                     | 124 ms: 1.03x faster                                               |
| scimark_lu                 | 122 ms                                                     | 119 ms: 1.02x faster                                               |
| sqlglot_transpile          | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                              |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                              |
| xml_etree_parse            | 162 ms                                                     | 159 ms: 1.02x faster                                               |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                              |
| coroutines                 | 23.2 ms                                                    | 22.8 ms: 1.02x faster                                              |
| thrift                     | 823 us                                                     | 809 us: 1.02x faster                                               |
| fannkuch                   | 402 ms                                                     | 396 ms: 1.02x faster                                               |
| sqlite_synth               | 2.99 us                                                    | 2.95 us: 1.01x faster                                              |
| 2to3                       | 274 ms                                                     | 271 ms: 1.01x faster                                               |
| xml_etree_process          | 61.2 ms                                                    | 60.4 ms: 1.01x faster                                              |
| nqueens                    | 81.4 ms                                                    | 80.5 ms: 1.01x faster                                              |
| pprint_pformat             | 1.56 sec                                                   | 1.54 sec: 1.01x faster                                             |
| raytrace                   | 267 ms                                                     | 264 ms: 1.01x faster                                               |
| pprint_safe_repr           | 758 ms                                                     | 752 ms: 1.01x faster                                               |
| pidigits                   | 191 ms                                                     | 190 ms: 1.01x faster                                               |
| gunicorn                   | 1.28 ms                                                    | 1.27 ms: 1.01x faster                                              |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                              |
| regex_compile              | 137 ms                                                     | 136 ms: 1.01x faster                                               |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                              |
| sympy_integrate            | 20.5 ms                                                    | 20.4 ms: 1.01x faster                                              |
| asyncio_websockets         | 567 ms                                                     | 563 ms: 1.01x faster                                               |
| pickle_list                | 5.11 us                                                    | 5.07 us: 1.01x faster                                              |
| asyncio_tcp                | 508 ms                                                     | 505 ms: 1.01x faster                                               |
| docutils                   | 2.83 sec                                                   | 2.81 sec: 1.01x faster                                             |
| dulwich_log                | 67.2 ms                                                    | 66.8 ms: 1.01x faster                                              |
| tornado_http               | 94.6 ms                                                    | 94.1 ms: 1.01x faster                                              |
| sqlglot_optimize           | 55.5 ms                                                    | 55.2 ms: 1.01x faster                                              |
| go                         | 145 ms                                                     | 144 ms: 1.01x faster                                               |
| python_startup_no_site     | 7.11 ms                                                    | 7.09 ms: 1.00x faster                                              |
| xml_etree_generate         | 87.4 ms                                                    | 87.7 ms: 1.00x slower                                              |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.85 sec: 1.00x slower                                             |
| unpickle_pure_python       | 218 us                                                     | 219 us: 1.00x slower                                               |
| async_generators           | 442 ms                                                     | 444 ms: 1.00x slower                                               |
| generators                 | 29.6 ms                                                    | 29.8 ms: 1.00x slower                                              |
| sympy_sum                  | 156 ms                                                     | 157 ms: 1.01x slower                                               |
| django_template            | 34.8 ms                                                    | 35.0 ms: 1.01x slower                                              |
| genshi_xml                 | 51.6 ms                                                    | 51.9 ms: 1.01x slower                                              |
| sqlglot_normalize          | 110 ms                                                     | 111 ms: 1.01x slower                                               |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                               |
| chaos                      | 61.3 ms                                                    | 61.8 ms: 1.01x slower                                              |
| hexiom                     | 6.30 ms                                                    | 6.35 ms: 1.01x slower                                              |
| genshi_text                | 23.7 ms                                                    | 23.9 ms: 1.01x slower                                              |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.33 ms: 1.01x slower                                              |
| pickle_dict                | 34.8 us                                                    | 35.3 us: 1.01x slower                                              |
| logging_simple             | 5.74 us                                                    | 5.83 us: 1.01x slower                                              |
| regex_effbot               | 3.67 ms                                                    | 3.73 ms: 1.02x slower                                              |
| regex_dna                  | 221 ms                                                     | 225 ms: 1.02x slower                                               |
| pathlib                    | 17.3 ms                                                    | 17.6 ms: 1.02x slower                                              |
| scimark_monte_carlo        | 69.2 ms                                                    | 70.6 ms: 1.02x slower                                              |
| comprehensions             | 16.6 us                                                    | 17.0 us: 1.02x slower                                              |
| regex_v8                   | 25.1 ms                                                    | 25.8 ms: 1.03x slower                                              |
| logging_silent             | 105 ns                                                     | 108 ns: 1.03x slower                                               |
| unpickle                   | 15.1 us                                                    | 15.6 us: 1.03x slower                                              |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                               |
| pycparser                  | 1.16 sec                                                   | 1.20 sec: 1.04x slower                                             |
| tomli_loads                | 2.12 sec                                                   | 2.21 sec: 1.04x slower                                             |
| telco                      | 8.41 ms                                                    | 8.78 ms: 1.04x slower                                              |
| pickle                     | 11.5 us                                                    | 12.1 us: 1.06x slower                                              |
| coverage                   | 93.1 ms                                                    | 98.3 ms: 1.06x slower                                              |
| nbody                      | 88.3 ms                                                    | 95.5 ms: 1.08x slower                                              |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                       |

Benchmark hidden because not significant (20): async_tree_memoization_tg, async_tree_none_tg, mypy2, async_tree_memoization, spectral_norm, sympy_str, dask, bench_thread_pool, bench_mp_pool, pickle_pure_python, async_tree_cpu_io_mixed, logging_format, html5lib, float, deltablue, sympy_expand, xml_etree_iterparse, pylint, async_tree_io_tg, djangocms
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 96.16% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x
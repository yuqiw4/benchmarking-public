# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_func_simple
- machine: windows-amd64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.01x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 219 ms: 1.06x slower                                                     |
| chameleon      | 4.80 ms                                                         | 4.70 ms: 1.02x faster                                                    |
| docutils       | 1.63 sec                                                        | 1.68 sec: 1.04x slower                                                   |
| html5lib       | 35.0 ms                                                         | 35.7 ms: 1.02x slower                                                    |
| tornado_http   | 81.8 ms                                                         | 84.2 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                           | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none        | 218 ms                                                          | 222 ms: 1.02x slower                                                     |
| async_tree_memoization | 264 ms                                                          | 274 ms: 1.04x slower                                                     |
| async_tree_none_tg     | 202 ms                                                          | 214 ms: 1.06x slower                                                     |
| Geometric mean         | (ref)                                                           | 1.02x slower                                                             |

Benchmark hidden because not significant (5): async_tree_io, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 56.9 ms: 1.19x faster                                                    |
| float          | 49.7 ms                                                         | 46.5 ms: 1.07x faster                                                    |
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                           | 1.09x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 15.8 ms                                                         | 14.1 ms: 1.12x faster                                                    |
| regex_effbot   | 1.58 ms                                                         | 1.56 ms: 1.02x faster                                                    |
| regex_dna      | 119 ms                                                          | 118 ms: 1.01x faster                                                     |
| regex_compile  | 78.0 ms                                                         | 87.0 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                           | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.18 sec: 1.15x faster                                                   |
| json_dumps           | 5.61 ms                                                         | 5.51 ms: 1.02x faster                                                    |
| json_loads           | 14.2 us                                                         | 14.0 us: 1.02x faster                                                    |
| xml_etree_generate   | 53.2 ms                                                         | 52.8 ms: 1.01x faster                                                    |
| pickle_pure_python   | 175 us                                                          | 174 us: 1.01x faster                                                     |
| pickle               | 7.11 us                                                         | 7.16 us: 1.01x slower                                                    |
| xml_etree_parse      | 90.9 ms                                                         | 92.9 ms: 1.02x slower                                                    |
| pickle_dict          | 18.1 us                                                         | 18.6 us: 1.03x slower                                                    |
| unpickle_list        | 2.62 us                                                         | 2.74 us: 1.05x slower                                                    |
| unpickle_pure_python | 122 us                                                          | 129 us: 1.06x slower                                                     |
| unpickle             | 8.40 us                                                         | 9.17 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                           | 1.01x slower                                                             |

Benchmark hidden because not significant (3): xml_etree_process, xml_etree_iterparse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 21.6 ms: 1.07x slower                                                    |
| python_startup_no_site | 16.2 ms                                                         | 19.5 ms: 1.21x slower                                                    |
| Geometric mean         | (ref)                                                           | 1.13x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 6.36 ms                                                         | 5.68 ms: 1.12x faster                                                    |
| genshi_xml     | 31.6 ms                                                         | 33.2 ms: 1.05x slower                                                    |
| genshi_text    | 14.4 ms                                                         | 15.3 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                           | 1.00x slower                                                             |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|--------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols | 101 us                                                          | 70.7 us: 1.43x faster                                                    |
| spectral_norm            | 63.7 ms                                                         | 51.4 ms: 1.24x faster                                                    |
| nbody                    | 67.6 ms                                                         | 56.9 ms: 1.19x faster                                                    |
| tomli_loads              | 1.35 sec                                                        | 1.18 sec: 1.15x faster                                                   |
| scimark_sparse_mat_mult  | 2.50 ms                                                         | 2.23 ms: 1.12x faster                                                    |
| mako                     | 6.36 ms                                                         | 5.68 ms: 1.12x faster                                                    |
| regex_v8                 | 15.8 ms                                                         | 14.1 ms: 1.12x faster                                                    |
| json                     | 3.19 ms                                                         | 2.87 ms: 1.11x faster                                                    |
| pycparser                | 754 ms                                                          | 694 ms: 1.09x faster                                                     |
| float                    | 49.7 ms                                                         | 46.5 ms: 1.07x faster                                                    |
| fannkuch                 | 243 ms                                                          | 228 ms: 1.07x faster                                                     |
| pylint                   | 205 ms                                                          | 194 ms: 1.06x faster                                                     |
| deepcopy_memo            | 22.1 us                                                         | 21.0 us: 1.05x faster                                                    |
| crypto_pyaes             | 45.5 ms                                                         | 44.1 ms: 1.03x faster                                                    |
| pyflate                  | 279 ms                                                          | 272 ms: 1.03x faster                                                     |
| scimark_monte_carlo      | 39.1 ms                                                         | 38.2 ms: 1.03x faster                                                    |
| chameleon                | 4.80 ms                                                         | 4.70 ms: 1.02x faster                                                    |
| scimark_fft              | 171 ms                                                          | 167 ms: 1.02x faster                                                     |
| pidigits                 | 150 ms                                                          | 147 ms: 1.02x faster                                                     |
| json_dumps               | 5.61 ms                                                         | 5.51 ms: 1.02x faster                                                    |
| regex_effbot             | 1.58 ms                                                         | 1.56 ms: 1.02x faster                                                    |
| sqlite_synth             | 1.60 us                                                         | 1.57 us: 1.02x faster                                                    |
| json_loads               | 14.2 us                                                         | 14.0 us: 1.02x faster                                                    |
| logging_simple           | 5.78 us                                                         | 5.70 us: 1.01x faster                                                    |
| logging_format           | 6.22 us                                                         | 6.15 us: 1.01x faster                                                    |
| deepcopy_reduce          | 1.99 us                                                         | 1.98 us: 1.01x faster                                                    |
| pprint_pformat           | 966 ms                                                          | 958 ms: 1.01x faster                                                     |
| xml_etree_generate       | 53.2 ms                                                         | 52.8 ms: 1.01x faster                                                    |
| regex_dna                | 119 ms                                                          | 118 ms: 1.01x faster                                                     |
| pickle_pure_python       | 175 us                                                          | 174 us: 1.01x faster                                                     |
| pickle                   | 7.11 us                                                         | 7.16 us: 1.01x slower                                                    |
| pprint_safe_repr         | 474 ms                                                          | 479 ms: 1.01x slower                                                     |
| create_gc_cycles         | 888 us                                                          | 898 us: 1.01x slower                                                     |
| generators               | 19.6 ms                                                         | 19.8 ms: 1.01x slower                                                    |
| async_tree_none          | 218 ms                                                          | 222 ms: 1.02x slower                                                     |
| telco                    | 4.67 ms                                                         | 4.75 ms: 1.02x slower                                                    |
| coroutines               | 12.8 ms                                                         | 13.0 ms: 1.02x slower                                                    |
| html5lib                 | 35.0 ms                                                         | 35.7 ms: 1.02x slower                                                    |
| xml_etree_parse          | 90.9 ms                                                         | 92.9 ms: 1.02x slower                                                    |
| aiohttp                  | 889 us                                                          | 911 us: 1.03x slower                                                     |
| pickle_dict              | 18.1 us                                                         | 18.6 us: 1.03x slower                                                    |
| pathlib                  | 75.9 ms                                                         | 78.0 ms: 1.03x slower                                                    |
| tornado_http             | 81.8 ms                                                         | 84.2 ms: 1.03x slower                                                    |
| richards_super           | 30.2 ms                                                         | 31.1 ms: 1.03x slower                                                    |
| meteor_contest           | 69.9 ms                                                         | 72.1 ms: 1.03x slower                                                    |
| docutils                 | 1.63 sec                                                        | 1.68 sec: 1.04x slower                                                   |
| richards                 | 26.7 ms                                                         | 27.7 ms: 1.04x slower                                                    |
| async_tree_memoization   | 264 ms                                                          | 274 ms: 1.04x slower                                                     |
| sqlglot_normalize        | 173 ms                                                          | 180 ms: 1.04x slower                                                     |
| async_generators         | 223 ms                                                          | 233 ms: 1.04x slower                                                     |
| sqlglot_parse            | 748 us                                                          | 781 us: 1.04x slower                                                     |
| sympy_expand             | 271 ms                                                          | 283 ms: 1.04x slower                                                     |
| sqlglot_transpile        | 955 us                                                          | 998 us: 1.05x slower                                                     |
| bench_mp_pool            | 64.8 ms                                                         | 67.7 ms: 1.05x slower                                                    |
| unpickle_list            | 2.62 us                                                         | 2.74 us: 1.05x slower                                                    |
| sympy_str                | 159 ms                                                          | 167 ms: 1.05x slower                                                     |
| genshi_xml               | 31.6 ms                                                         | 33.2 ms: 1.05x slower                                                    |
| bench_thread_pool        | 768 us                                                          | 806 us: 1.05x slower                                                     |
| sympy_sum                | 84.4 ms                                                         | 89.2 ms: 1.06x slower                                                    |
| 2to3                     | 207 ms                                                          | 219 ms: 1.06x slower                                                     |
| nqueens                  | 56.7 ms                                                         | 60.1 ms: 1.06x slower                                                    |
| unpickle_pure_python     | 122 us                                                          | 129 us: 1.06x slower                                                     |
| async_tree_none_tg       | 202 ms                                                          | 214 ms: 1.06x slower                                                     |
| comprehensions           | 10.4 us                                                         | 11.0 us: 1.06x slower                                                    |
| sqlglot_optimize         | 32.7 ms                                                         | 34.8 ms: 1.06x slower                                                    |
| asyncio_tcp_ssl          | 1.48 sec                                                        | 1.58 sec: 1.06x slower                                                   |
| python_startup           | 20.3 ms                                                         | 21.6 ms: 1.07x slower                                                    |
| genshi_text              | 14.4 ms                                                         | 15.3 ms: 1.07x slower                                                    |
| mypy2                    | 418 ms                                                          | 449 ms: 1.08x slower                                                     |
| dulwich_log              | 38.0 ms                                                         | 41.0 ms: 1.08x slower                                                    |
| thrift                   | 8.11 ms                                                         | 8.79 ms: 1.08x slower                                                    |
| sympy_integrate          | 12.2 ms                                                         | 13.3 ms: 1.09x slower                                                    |
| unpickle                 | 8.40 us                                                         | 9.17 us: 1.09x slower                                                    |
| scimark_sor              | 75.3 ms                                                         | 82.8 ms: 1.10x slower                                                    |
| regex_compile            | 78.0 ms                                                         | 87.0 ms: 1.12x slower                                                    |
| mdp                      | 1.31 sec                                                        | 1.46 sec: 1.12x slower                                                   |
| go                       | 82.1 ms                                                         | 92.1 ms: 1.12x slower                                                    |
| coverage                 | 42.1 ms                                                         | 47.5 ms: 1.13x slower                                                    |
| deltablue                | 1.88 ms                                                         | 2.16 ms: 1.15x slower                                                    |
| hexiom                   | 3.72 ms                                                         | 4.42 ms: 1.19x slower                                                    |
| python_startup_no_site   | 16.2 ms                                                         | 19.5 ms: 1.21x slower                                                    |
| scimark_lu               | 56.6 ms                                                         | 71.4 ms: 1.26x slower                                                    |
| Geometric mean           | (ref)                                                           | 1.01x slower                                                             |

Benchmark hidden because not significant (14): raytrace, chaos, asyncio_tcp, gc_traversal, deepcopy, async_tree_io, logging_silent, xml_etree_process, xml_etree_iterparse, pickle_list, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown